---
title: Utiliser les fragments dans les politiques de décision
description: Découvrez comment exploiter les fragments dans les politiques de décision
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 70f64348-092b-4350-91dc-72c3c07300f9
TQID: https://experienceleague.adobe.com/5Vpngi03UnC9YPlB5tdTRcd0NoT7iglH2pRDkmeZKOg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: f816ee04639846ffd18c3d6723f4616ada24892d
workflow-type: tm+mt
source-wordcount: 1114
ht-degree: 22%

---

# Utiliser les fragments dans les politiques de décision {#fragments}

Les éléments de décision prennent en charge deux types de contenu de fragment qui peuvent être utilisés lors de la création de messages dans une politique de décision :

* **Fragments de contenu Journey Optimizer** — fragments d&#39;expression réutilisables créés dans Journey Optimizer et ajoutés à la section **[!UICONTROL Fragments]** de l&#39;élément de décision. [En savoir plus sur les fragments de contenu AJO](../content-management/fragments.md)
* **Fragments de contenu AEM** — contenu créé dans Adobe Experience Manager, mappé aux attributs de l’élément de décision et sélectionné dans l’éditeur de personnalisation par nom de clé. [Découvrez comment lier un fragment de contenu AEM à un élément de décision](items.md#aem-fragments)

## Fragments de contenu Journey Optimizer {#ajo-fragments}

Si votre politique de décision contient des éléments de décision, y compris des fragments de contenu AJO, vous pouvez exploiter ces fragments lors de la création d’un message dans la politique de décision sur tous les canaux où la prise de décision est disponible (expérience basée sur le code, e-mail, notification push, SMS et parcours).

Supposons, par exemple, que vous souhaitiez afficher différents contenus pour plusieurs modèles d’appareils mobiles. Ajoutez les fragments spécifiés, chacun appartenant à un modèle téléphonique différent, à l’élément de décision que vous utilisez dans la politique de décision. [Découvrez comment ajouter des fragments à un élément de décision](items.md#attributes).

![Section Fragments d’un élément de décision affichant les références aux fragments et les clés d’emplacement.](assets/item-fragments.png){width=70%}

Une fois cette opération terminée, vous pouvez utiliser l’une des méthodes suivantes :

>[!BEGINTABS]

>[!TAB Insérer directement le code]

Il vous suffit de copier-coller le bloc de code ci-dessous dans le code de la politique de décision. Remplacez `variable` par l’ID de fragment et `placement` par la clé de référence du fragment :

```handlebars
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable required=false}}
```

>[!TAB Suivre les étapes détaillées]

1. Accédez aux **[!UICONTROL Fonctions d’assistance]** et ajoutez la fonction **Let** `{% let variable = expression %} {{variable}}` au volet de code, où vous pouvez déclarer la variable pour votre fragment.

   ![Éditeur de code de politique de décision affichant la fonction d’assistance Let ajoutée au volet de code.](assets/decision-let-function.png)

1. Utilisez la fonction **Map** > **Get** `{%= get(map, string) %}`pour créer votre expression. La carte est le fragment référencé dans l’élément de décision. La chaîne peut être le modèle d’appareil que vous avez saisi dans l’élément de décision en tant que **[!UICONTROL clé de référence du fragment]**.

   ![Fonctions Map et Get utilisées pour référencer le mappage de fragment et la clé de référence de fragment.](assets/decision-map-function.png)

1. Vous pouvez également utiliser un attribut contextuel qui contiendra cet identifiant de modèle d’appareil.

   ![Attribut contextuel sélectionné pour l’identifiant du modèle d’appareil.](assets/decision-contextual-attribute.png)

1. Ajoutez la variable que vous avez choisie pour votre fragment en tant qu’ID de fragment.

   ![Variable d’ID de fragment définie à partir de l’élément de décision dans le code de politique de décision.](assets/decision-fragment-id.png)

>[!ENDTABS]

L’ID de fragment et la clé de référence sont sélectionnés dans la section **[!UICONTROL Fragments]** de l’élément de décision.

>[!WARNING]
>
>Si la clé du fragment est incorrecte ou si le contenu du fragment n’est pas valide, le rendu peut échouer et provoquer une erreur dans l’appel Edge.
>
>Pour éviter les échecs lorsqu’un fragment est temporairement indisponible, l’indicateur `required=false` est utilisé afin que le fragment soit ignoré à la place. [En savoir plus sur les fragments temporairement indisponibles](#temporary-unavailable-fragments)

### Utilisation et mécanismes de sécurisation {#fragments-guardrails}

Les mécanismes de sécurisation suivants s’appliquent spécifiquement aux **fragments de contenu** utilisés dans les éléments de décision.

+++Simuler des fragments de contenu et d’expression dans des e-mails

Pour le canal **E-mail**, les fragments d’expression associés à un élément de décision s’affichent correctement lorsque vous **[!UICONTROL Envoyez le BAT]** ou lorsque la campagne est activée. Toutefois, la mention **[!UICONTROL Simuler du contenu]** n’affiche pas le fragment d’expression de l’élément de décision.

+++

+++Fragments visuels et éléments de décision dans les e-mails

Vous ne pouvez pas affecter un **[!UICONTROL fragment visuel]** à un élément de décision. Seuls les **fragments d&#39;expression** sont pris en charge dans ce contexte.

+++

+++Attributs d’élément de décision et de contexte

Les attributs d’élément de décision et les attributs contextuels ne sont pas pris en charge par défaut dans les fragments de [!DNL Journey Optimizer]. Cependant, vous pouvez utiliser des variables globales à la place, comme décrit ci-dessous.

Supposons que vous souhaitiez utiliser la variable *sport* dans votre fragment.

1. Référencez cette variable dans le fragment, par exemple :

   ```text
   Elevate your practice with new {{sport}} gear!
   ```

1. Définissez la variable avec la fonction **Let** dans le bloc de politique de décision. Dans l’exemple ci-dessous, *sport* est défini avec l’attribut d’élément de décision :

   ```handlebars
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

+++

+++Validation du contenu du fragment d’élément de décision

* En raison de la nature dynamique de ces fragments, lorsqu’ils sont utilisés dans une campagne, la validation du message lors de la création du contenu de la campagne est ignorée pour les fragments référencés dans les éléments de décision.

* La validation du contenu du fragment se produit uniquement lors de la création et de la publication du fragment.

* Pour les fragments d’expression de type JSON, le contenu est validé par la syntaxe lors de l’enregistrement du fragment. Les erreurs de validation s’affichent sous forme d’alertes.

Au moment de l’exécution, le contenu de la campagne (y compris le contenu du fragment des éléments de décision) est validé. En cas d’échec de validation, la campagne ne sera pas rendue.

+++

+++Les fragments temporairement indisponibles sont ignorés {#temporary-unavailable-fragments}

Lorsque des parcours ou des campagnes référencent des fragments joints à des éléments de décision, il peut y avoir de courts délais de synchronisation avant que les fragments mis à jour ne soient disponibles sur Edge.

Pour éviter les échecs lorsqu’un fragment est temporairement indisponible, l’indicateur de `required` des fragments est désormais défini sur `false` par défaut afin qu’ils soient ignorés au lieu de provoquer l’échec du parcours ou de la campagne.

Cela signifie que si le fragment est temporairement indisponible sur Edge, il est simplement ignoré. Si le fragment est disponible, il s’affiche normalement.

**Exemple**

Si votre politique de décision est admissible pour deux offres et que chacune d’elles comporte un fragment, par exemple « 20 % de réduction » et « 30 % de réduction », et que le deuxième fragment est temporairement indisponible, avec `required=false` le système effectue le rendu de l’offre disponible (20 % de réduction) et ignore l’autre fragment (30 % de réduction) au lieu d’échouer le parcours ou la campagne. Cela améliore la fiabilité lorsque le contenu se synchronise toujours.

+++

>[!NOTE]
>
>Vous pouvez toujours marquer un fragment comme obligatoire en définissant l’indicateur `required` sur `true`. Cependant, si un fragment est temporairement manquant, cela peut entraîner l’échec du parcours ou du rendu de campagne.

## Fragments de contenu AEM {#aem-fragments-decisioning}

>[!AVAILABILITY]
>
>Cette fonctionnalité est disponible en disponibilité limitée pour les canaux sortants avec prise en charge de la prise de décision. Pour obtenir l’accès, contactez votre représentant ou représentante Adobe.

Avant d’utiliser des fragments de contenu AEM dans une politique de décision, vérifiez que vous disposez des éléments suivants :

* Vous avez créé votre fragment de contenu dans Adobe Experience Manager et l’avez balisé avec `ajo-enabled:{OrgId}/{SandboxName}` afin qu’il soit détectable par Journey Optimizer. [Découvrez comment créer et affecter une balise](../integrations/aem-fragments.md#create-tag)
* Liez le fragment à la section **[!UICONTROL Fragments]** de l’élément d’offre en lui attribuant un nom de référence unique. [Découvrez comment lier un fragment de contenu AEM à un élément de décision](items.md#attributes)

Dans l’éditeur de personnalisation, tous les fragments de contenu AEM associés aux éléments de décision sélectionnés par la politique sont disponibles. Un dossier s’affiche par nom de clé de fragment.

Dans cet exemple, la politique de décision comprend deux éléments de décision auxquels des fragments AEM sont liés par leur nom de référence.

![](assets/aem-fragment-select.png)

1. Cliquez sur le bouton + pour ajouter le fragment souhaité à votre expression.

   Comme un seul nom de référence peut être associé à plusieurs fragments dans différents éléments d’offre, Decisioning détermine le meilleur nom à fournir à chaque client en fonction des critères de classement de la politique de décision.

1. Une fois le fragment sélectionné, vous pouvez exploiter ses attributs, tels que les URL d’image, les champs de texte ou d’autres contenus, et utiliser Decisioning pour faire apparaître le contenu approprié au bon client au bon moment.

   ![](assets/aem-fragment-attribute.png)

1. Avant d’activer votre campagne ou votre parcours, vous pouvez utiliser **[!UICONTROL Simuler du contenu]** pour prévisualiser la manière dont les valeurs de champ de fragment de contenu AEM seront rendues pour un profil de test spécifique. [En savoir plus sur la simulation de contenu](../content-management/preview-test.md)
