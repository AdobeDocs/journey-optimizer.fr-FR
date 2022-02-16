---
title: Création de formules de classement
description: Apprenez à créer des formules pour classer les offres
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: 2d859a5dab19a419d424acefd17d254473c00818
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 100%

---

# Création de formules de classement {#create-ranking-formulas}

## À propos des formules de classement {#about-ranking-formulas}

Les **formules de classement** vous permettent de définir des règles déterminant quelle offre doit être présentée en premier pour un emplacement donné au lieu de prendre en compte les scores de priorité des offres.

Les formules de classement sont exprimées en **syntaxe PQL** et peuvent exploiter les attributs de profil, les données contextuelles et les attributs d&#39;offre. Pour plus d&#39;informations sur l&#39;utilisation de la syntaxe PQL, reportez-vous à la [documentation dédiée](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=fr).

Après avoir créé une formule de classement, vous pouvez l’affecter à un emplacement dans une décision. Voir à ce propos la section [Configurer la sélection des offres dans les décisions](../offer-activities/configure-offer-selection.md).

## Création d&#39;une formule de classement {#create-ranking-formula}

Pour créer une formule de classement, procédez comme suit :

1. Accédez au menu **[!UICONTROL Composants]**, puis sélectionnez l&#39;onglet **[!UICONTROL Classements.]** La liste des classements précédemment créés s&#39;affiche.

   ![](../../assets/rankings-list.png)

1. Cliquez sur **[!UICONTROL Créer un classement]** pour créer une formule de classement.

   ![](../../assets/ranking-create-formula.png)

1. Spécifiez le nom, la description et la formule de la formule de classement.

   Dans cet exemple, nous voulons augmenter la priorité de toutes les offres contenant l&#39;attribut « chaud » en cas de météo avec températures chaudes. Pour ce faire, **contextData.weather=hot** a été transmis dans l&#39;appel de décision.

   ![](../../assets/ranking-syntax.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**. Votre formule de classement est créée. Vous pouvez la sélectionner dans la liste pour obtenir des détails et la modifier ou la supprimer.

   Elle est maintenant prête à être utilisée dans une décision pour classer les offres éligibles à un emplacement (voir [Configurer la sélection des offres dans les décisions](../offer-activities/configure-offer-selection.md)).

   ![](../../assets/ranking-formula-created.png)

## Exemples de formules de classement {#ranking-formula-examples}

Vous pouvez créer de nombreuses formules de classement différentes en fonction de vos besoins. Voici quelques exemples.

<!--
Boost by offer ID

Boost the priority of an offer with the offer ID *xcore:personalized-offer:13d213cd4cb328ec* by 5.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec", offer.rank.priority + 5, offer.rank.priority)
```

Change the offer priority based on a certain profile attribute

Set the offer priority to 30 for offer *xcore:personalized-offer:13d213cd4cb328ec* if the user lives in the city of Bondi.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec" and homeAddress.city.equals("Bondi", false), 30, offer.rank.priority)
```

Boost multiple offers by offer ID based on the presence of a profile's segment membership

Boost the priority of offers based on whether the user is a member of a priority segment, which is configured as an attribute in the offer.

**Ranking formula:**

```
if( segmentMembership.get("ups").get(offer.characteristics.prioritySegmentId).status in (["realized","existing"]), offer.rank.priority + 10, offer.rank.priority)
```
-->

### Booster les offres avec un attribut d’offre spécifique basé sur l’attribut de profil

Si le profil réside dans la ville correspondant à l’offre, doublez la priorité de toutes les offres de cette ville.

**Formule de classement:**

```
if( offer.characteristics.city = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

### Booster les offres pour lesquelles la date de fin est inférieure à 24 heures

**Formule de classement:**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

### Booster les offres avec un attribut d’offre spécifique basé sur les données contextuelles

Boostez certaines offres en fonction des données contextuelles transmises dans l’appel de prise de décision. Par exemple, si la valeur `contextData.weather=hot` est transmise dans l’appel de prise de décision, la priorité de toutes les offres avec la valeur `attribute=hot` doit être augmentée.

**Formule de classement:**

```
if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull()
and offer.characteristics.weather=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority + 5, offer.rank.priority)
```

Notez que lorsque vous utilisez l’API de prise de décision, les données contextuelles sont ajoutées à l’élément de profil dans le corps de la requête, comme dans l’exemple ci-dessous.

**Extrait de code du corps de la requête :**

```
"xdm:profiles": [
{
    "xdm:identityMap": {
        "crmid": [
            {
            "xdm:id": "CRMID1"
            }
        ]
    },
    "xdm:contextData": [
        {
            "@type":"_xdm.context.additionalParameters;version=1",
            "xdm:data":{
                "xdm:weather":"hot"
            }
        }
    ]
 }],
```

### Booster les offres en fonction de la propension des clients à acheter le produit proposé

Si nous avons 2 instances de *CustomerAI* calculant la propension à acheter *travelInsurance* et *extraBBagage* pour une compagnie aérienne, la formule de classement suivante augmentera la priorité (de 50 points) de l’offre spécifique à l’assurance ou aux bagages si le score de propension du client à acheter ce produit est supérieur à 90.

Cependant, comme chaque instance *CustomerAI* crée son propre objet dans le schéma de profil unifié, il n’est pas possible de sélectionner dynamiquement le score en fonction du type de propension à l’offre. Vous devez donc chaîner les instructions `if` pour d’abord vérifier le type de propension de l’offre, puis extraire le score à partir du champ de profil approprié.

**Formule de classement:**

```
if ( offer.characteristics.propensityType = "extraBaggagePropensity" and _salesvelocity.CustomerAI.extraBaggagePropensity.score > 90, offer.rank.priority + 50,
    (
        if ( offer.characteristics.propensityType = "travelInsurancePropensity" and _salesvelocity.CustomerAI.insurancePropensity.score > 90, offer.rank.priority + 50, offer.rank.priority )
    )
)
```

Une meilleure solution consiste à stocker les scores dans un tableau du profil. L’exemple suivant illustre plusieurs scores de propension différents en utilisant une formule de classement simple. Il est attendu que vous disposiez d’un schéma de profil avec un tableau de scores. Dans cet exemple, le client d’instance est *_salesvelocity* et le schéma de profil contient les éléments suivants :

![](../../assets/ranking-example-schema.png)

Ainsi, pour un profil tel que :

```
{"_salesvelocity": {"individualScoring": [
                    {"core": {
                            "category":"insurance",
                            "propensityScore": 96.9
                        }},
                    {"core": {
                            "category":"personalLoan",
                            "propensityScore": 45.3
                        }},
                    {"core": {
                            "category":"creditCard",
                            "propensityScore": 78.1
                        }}
                    ]}
}
```

Les offres contiennent un attribut pour *propensionType* correspondant à la catégorie des scores :

![](../../assets/ranking-example-propensityType.png)

Votre formule de classement peut alors définir la priorité de chaque offre pour qu’elle soit égale aux clients *propensionScore* pour ce *propensionType*. Si aucun score n’est trouvé, utilisez la priorité statique définie sur l’offre :

```
let score = (select _Individual_Scoring1 from _salesvelocity.individualScoring
             where _Individual_Scoring1.core.category.equals(offer.characteristics.propensityType, false)).head().core.propensityScore
in if(score.isNotNull(), score, offer.rank.priority)
```
