---
title: Formules de classement
description: Apprenez à créer des formules pour classer les offres
feature: Ranking, Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 35d7488b-e7d8-402f-b337-28a0c869bff0
version: Journey Orchestration
source-git-commit: 626d83c872f2900de7b11337faab5012bc346e34
workflow-type: tm+mt
source-wordcount: '1731'
ht-degree: 64%

---

# Créer des formules de classement {#create-ranking-formulas}

Les **formules de classement** vous permettent de définir des règles déterminant quelle offre doit être présentée en premier, plutôt que de prendre en compte les scores de priorité.

Pour créer ces règles, le créateur de formules d’IA d’**[!UICONTROL Adobe Journey Optimizer]** offre une plus grande flexibilité et un meilleur contrôle du classement des offres. Au lieu de vous fier uniquement à une priorité d’offre statique, vous pouvez à présent définir des formules de classement personnalisées qui combinent les scores du modèle d’IA, les priorités d’offre, les attributs de profil, les attributs d’offre et les signaux contextuels par le biais d’une interface guidée.

Cette approche vous permet d’ajuster dynamiquement le classement des offres en fonction de n’importe quelle combinaison entre la propension pilotée par l’IA, la valeur commerciale et le contexte en temps réel, ce qui facilite l’alignement de la prise de décisions sur les objectifs marketing et les besoins de la clientèle. Le créateur de formules d’IA prend en charge les formules simples ou avancées en fonction du niveau de contrôle que vous souhaitez appliquer.

Après avoir créé une formule de classement, vous pouvez l’affecter à une [stratégie de sélection](../selection-strategies.md). Si plusieurs offres sont éligibles à la présentation lors de l’utilisation de cette stratégie de sélection, le moteur de décision emploiera la formule sélectionnée pour calculer l’offre à présenter en premier.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Mécanismes de sécurisation et limitations {#ranking-guardrails}

Avant de créer des formules de classement, tenez compte des contraintes suivantes :

* Le créateur de formules d’IA ne prend pas en charge les [modèles d’optimisation personnalisés](personalized-optimization-model.md) qui utilisent des mesures continues.
* Lorsqu’un modèle d’IA est utilisé dans une formule de classement, les données ne sont pas reflétées dans le rapport [&#x200B; Taux de conversion du trafic d’exclusion et piloté par le modèle &#x200B;](../../reports/campaign-global-report-cja-code.md#conversion-rate).
* La profondeur d’imbrication dans une formule de classement est limitée à 30 niveaux, mesurés par le comptage des `)` dans la chaîne PQL.
* Une chaîne de formule de classement peut contenir jusqu’à 8 Ko pour les caractères codés au format UTF-8 (8 000 caractères ASCII ou 2 000 à 4 000 caractères non-ASCII).
* Les périodes de recherche en amont ne sont pas prises en charge dans les formules de classement (par exemple, les événements d’expérience du mois dernier). Les tentatives d’enregistrement de telles formules déclenchent une erreur.
* [Optimisation des formules basée sur l’IA](#optimize) s’applique uniquement aux formules de classement dont l’expression PQL basée sur le code est supérieure à **2 Ko** en taille codée au format UTF-8 ; les formules plus petites ne sont pas analysées.

## Création de la formule de classement et définition des propriétés {#create-ranking-formula}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Créer des formules de classement"
>abstract="Les formules vous permettent de définir des règles déterminant la décision qui doit être présentée en premier au lieu de prendre en compte les scores de priorité de l’élément. Après avoir créé une formule de classement, vous pouvez l’affecter à une stratégie de sélection."

Pour créer une formule de classement, procédez comme suit :

1. Accédez au menu **[!UICONTROL Configuration de la stratégie]**, puis sélectionnez l’onglet **[!UICONTROL Formules de classement]**. La liste des formules créées précédemment s’affiche.

   ![](../assets/ranking-formulas-list.png)

1. Cliquez sur **[!UICONTROL Créer une formule]**.

1. Spécifiez le nom de la formule et ajoutez une description, le cas échéant.

   ![](../assets/create-formula.png){width="80%"}

1. Si vous le souhaitez, cliquez sur **[!UICONTROL Sélectionner un modèle d’IA]** pour définir le modèle à utiliser comme référence pour créer votre formule de classement.

   Chaque fois que vous vous référez à un score de modèle lors de la définition de votre formule ci-dessous, le modèle d’IA que vous avez sélectionné est utilisé.

1. Définissez les conditions qui détermineront le score de classement pour les éléments de décision correspondants. Vous pouvez :

   * Renseignez la section **[!UICONTROL Critères]** à l’aide du [créateur de formules](#ranking-select-criteria) et/ou
   * Cliquez sur **[!UICONTROL Basculer vers l’éditeur de code]** pour définir ou affiner la logique de classement avec [PQL dans l’éditeur de code](#ranking-code-editor).

## Utiliser des données Adobe Experience Platform {#aep-data}

Dans la section **[!UICONTROL Recherche de jeu de données]** vous pouvez utiliser les données de Adobe Experience Platform pour ajuster dynamiquement la logique de classement afin de refléter des conditions réelles.

Cela s’avère particulièrement utile pour les attributs qui changent fréquemment, tels que la disponibilité des produits ou la tarification en temps réel. [Découvrez comment utiliser des données Adobe Experience Platform pour la prise de décision.](../aep-data-exd.md)

![](../assets/ranking-formula-dataset.png)

## Définir des critères à l’aide du créateur de formules {#ranking-select-criteria}

Définissez les **critères** qui déterminent le score de classement des éléments de décision correspondants.

Grâce à une interface intuitive, vous pouvez affiner la prise de décisions en ajustant les scores de l’IA (propension), la valeur de l’offre (priorité), les leviers contextuels et les propensions des profils externes, individuellement ou en combinaison, afin d’optimiser chaque interaction. <!--Whether you are maximizing revenue, promoting strategic offers, or balancing business goals with real-time context, the formula builder gives you total control in defining ranking strategies.-->

<!--![](../assets/ranking-formula-criteria.png){width="80%"}-->

1. Si nécessaire, cliquez sur **[!UICONTROL Basculer vers l’éditeur de code]** pour ajouter une expression qui utilise la syntaxe **PQL** avec le créateur de formules. Cette option complète les champs de l’interface utilisateur dans les étapes ci-dessous, afin que vous puissiez combiner les deux approches dans la même formule de classement. Pour plus d’informations sur l’utilisation de la syntaxe PQL, consultez la [documentation dédiée](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=fr). La syntaxe des attributs d’élément de décision et des exemples de copier-coller sont fournis dans la section [&#x200B; Utiliser l’éditeur de code &#x200B;](#ranking-code-editor).

   ![](../assets/ranking-formula-code-editor-button.png)

   >[!NOTE]
   >
   >Le passage à l’éditeur de code ajoute une entrée basée sur l’expression à vos critères et ne supprime pas les autres champs de l’interface utilisateur.

1. Dans la section **[!UICONTROL Critère 1]**, spécifiez les éléments de décision auxquels vous souhaitez appliquer un score de classement en procédant comme suit :
   * sélectionnez un [attribut d’élément de décision](../items.md#attributes)
   * sélectionner un opérateur logique
   * ajouter une condition correspondante - vous pouvez saisir une valeur ou sélectionner un attribut de profil ou [des données contextuelles](../context-data.md)

   ![](../assets/ranking-formula-criterion-1.png){width="70%"}

1. Vous pouvez éventuellement spécifier des éléments supplémentaires pour affiner les conditions correspondantes afin que vos critères soient vrais.

   ![](../assets/ranking-formula-addtional-conditions.png){width="80%"}

   Par exemple, vous avez défini le critère 1 tel que l’attribut personnalisé *Météo* *Est égal à* la condition *Chaud*. De plus, vous pouvez ajouter une autre condition, par exemple si la première condition est remplie et si la température dépasse 75 degrés Fahrenheit au moment de la requête, alors le critère 1 est vrai.<!--Add a screenshot with the example-->

1. Créez une expression qui attribuera un score de classement aux éléments de décision qui répondent à la condition définie ci-dessus. Vous pouvez référencer l’un des éléments suivants :

   * le score provenant du modèle d’IA que vous avez éventuellement sélectionné dans la section **[!UICONTROL Détails]** [ci-dessus](#create-ranking-formula) ;
   * la priorité de l’élément de décision, qui est une valeur affectée manuellement lors de la [création d’un élément de décision](../items.md#attributes) ; <!--If a profile qualifies for multiple decision items, a higher priority grants the item precedence over others.-->
   * tout attribut susceptible de résider sur le profil, tel qu’un score de propension dérivé de l’extérieur ;
   * une valeur statique que vous pouvez attribuer dans un format libre ;
   * une combinaison des options ci-dessus.

   ![](../assets/ranking-formula-expression.png){width="70%"}

   >[!NOTE]
   >
   >Cliquez sur l’icône en regard du champ pour ajouter des variables prédéfinies.

1. Cliquez sur **[!UICONTROL Ajouter un critère]** pour ajouter un ou plusieurs critères autant de fois que nécessaire. La logique se présente comme suit :
   * Si le premier critère est vrai pour un élément de décision donné, il est prioritaire sur les suivants.
   * Si ce n’est pas le cas, le moteur de décision passe au deuxième critère, et ainsi de suite.

1. Dans le dernier champ, vous pouvez créer une expression qui sera affectée à tous les éléments de décision qui ne répondent pas aux critères ci-dessus.

   ![](../assets/ranking-formula-criteria-not-met.png){width="70%"}

   +++Exemple de formule de classement

   ![](../assets/ranking-formula-example.png){width="80%"}

   Si la région de l’élément de décision (attribut personnalisé) est égale au libellé géographique du profil (attribut de profil), le score de classement exprimé ici (qui est une combinaison de la priorité de l’élément de décision, du score du modèle d’IA et d’une valeur statique) sera appliqué à tous les éléments de décision répondant à cette condition.

   +++

1. Lorsque votre formule est prête, cliquez sur **[!UICONTROL Créer]**.

Vous pouvez désormais accéder à la formule de classement à partir de la liste pour en afficher les détails et la modifier ou la supprimer. Elle est maintenant prête à être utilisée dans une [stratégie de sélection](../selection-strategies.md) pour classer les éléments de décision éligibles.

## Définir des critères à l’aide de l’éditeur de code {#ranking-code-editor}

Utilisez **[!UICONTROL Basculer vers l’éditeur de code]** lorsque vous souhaitez écrire ou modifier la logique de classement en tant qu’expression **PQL**.

![](../assets/ranking-formula-switch.png)

>[!NOTE]
>
>Cette action vous empêchera de revenir à l’affichage du créateur par défaut pour cette formule.

Vous pouvez exploiter les attributs de profil, [données contextuelles](../context-data.md) et [attributs d&#39;élément de décision](../items.md#attributes).

Dans cet exemple, nous voulons augmenter la priorité de toutes les offres contenant l’attribut « hot » en cas de météo avec températures chaudes. Pour ce faire, **contextData.weather=hot** a été transmis dans l’appel de prise de décisions.

![](../assets/ranking-formula-code-editor.png){width="80%"}

Pour utiliser des attributs liés à vos éléments de décision dans des formules, veillez à respecter la syntaxe correcte dans le code de votre formule de classement. Pour plus d’informations, développez chaque section :

+++Utiliser des attributs standard d’éléments de décision

![](../assets/formula-attribute.png)

+++

+++Utiliser des attributs personnalisés d’éléments de décision

![](../assets/formula-attribute-custom.png)

+++

Vous pouvez créer de nombreuses formules de classement basées sur du code différentes en fonction de vos besoins. Voici quelques exemples.

+++Booster les offres avec un attribut d’offre spécifique basé sur l’attribut de profil

Si le profil réside dans la ville correspondant à l’offre, doublez la priorité de toutes les offres de cette ville.

**Formule de classement:**

```
if( offer.characteristics.get("city") = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

+++

+++Booster les offres pour lesquelles la date de fin est inférieure à 24 heures

**Formule de classement:**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

+++

+++Booster les offres en fonction de la propension des clients à acheter le produit proposé

Vous pouvez augmenter le score d’une offre en fonction d’un score de propension du client.

Dans cet exemple, le client d’instance est *_salesvelocity* et le schéma de profil contient une plage de scores stockés dans un tableau :

![](../assets/ranking-example-schema.png)

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

+++

+++Mettre en avant des offres en fonction du code postal et du revenu annuel d’un profil

Dans cet exemple, le système tente toujours de présenter en premier une offre avec un code postal identique, puis utilise une offre générale si aucune correspondance n’est trouvée. Cela évite de présenter les offres destinées aux autres codes postaux.

```pql
if( offer._luma.offerDetails.zipCode = _luma.zipCode,luma.annualIncome / 1000 + 10000, if( not offer.luma.offerDetails.zipCode,_luma.annualIncome / 1000, -9999) )
```

Fonction de la formule :

* Si l’offre possède le même code postal que l’utilisateur ou l’utilisatrice, attribuez-lui un score très élevé afin qu’elle soit sélectionnée en premier.
* Si l’offre ne comporte aucun code postal (s’il s’agit d’une offre générale), attribuez-lui un score normal en fonction du revenu de l’utilisateur ou de l’utilisatrice.
* Si le code postal de l’offre est différent de celui de l’utilisateur ou de l’utilisatrice, attribuez-lui un score très faible afin qu’elle ne soit pas sélectionnée.

+++

+++Booster les offres basées sur des données contextuelles

[!DNL Journey Optimizer] permet de booster certaines offres en fonction des données contextuelles transmises dans l’appel. Par exemple, si la valeur `contextData.weather=hot` est transmise, la priorité de toutes les offres avec la valeur `attribute=hot` doit être boostée.

>[!NOTE]
>
>Pour obtenir des informations détaillées sur la transmission de données contextuelles<!-- using the **Edge Decisioning** and **Decisioning** APIs-->, consultez [cette section](../context-data.md).

Notez que lorsque vous utilisez l’API **Decisioning**, les données contextuelles sont ajoutées à l’élément de profil dans le corps de la requête, comme dans l’exemple ci-dessous.

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

+++

## Optimisation des formules basées sur l’IA {#optimize}

[!DNL Journey Optimizer] pouvez automatiquement analyser les formules de classement et suggérer des simplifications qui préservent la logique d’origine. Seules les formules dont l’expression PQL est supérieure à **2 Ko** (codées au format UTF-8) sont éligibles, les expressions plus petites ne sont pas analysées. Lorsqu’une simplification est trouvée, un indicateur rouge s’affiche en regard du nom de la formule dans la liste.

![](../assets/ranking-formula-ai.png)

>[!NOTE]
>
>L’optimisation des formules optimisée par l’IA repose sur les mêmes fonctionnalités d’IA génératives que l’**assistant IA** et utilise les mêmes contrôles d’accès. Les utilisateurs doivent disposer de l’autorisation **[!UICONTROL Générer du contenu]** sur la ressource **[!UICONTROL Assistant IA]**. Pour plus d’informations, voir [Accéder à l’assistant AI](../../content-management/gs-generative.md#generative-access).

Pour optimiser une formule de classement :

1. Dans la liste des formules de classement, cliquez sur l’icône d’indicateur rouge en regard du nom de la formule.

1. La fenêtre **[!UICONTROL Optimiser]** s’ouvre, affichant l’expression PQL d’origine avec la version suggérée par l’IA.

   ![](../assets/ranking-formula-ai-details.png)

1. Pour vérifier que les deux expressions produisent des résultats de classement identiques, cliquez sur **[!UICONTROL Download Optimization Analysis (TSV)]** afin de télécharger un fichier montrant comment les profils simulés sont évalués par rapport à chaque version.

1. Une fois satisfait, cliquez sur **[!UICONTROL Appliquer]** pour remplacer l’expression d’origine par l’expression optimisée.

## Vidéo pratique {#video}

Découvrez comment utiliser le créateur de formules IA dans Adobe Journey Optimizer pour créer des stratégies de classement d’offres personnalisées.

>[!VIDEO](https://video.tv.adobe.com/v/3464446/?learn=on&enablevpops)
