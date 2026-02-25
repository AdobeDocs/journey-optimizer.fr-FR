---
title: formules de classement par arbitrage de parcours
description: Découvrez comment créer des formules pour classer les parcours en vue de l’arbitrage, de sorte que le meilleur parcours soit sélectionné par profil en fonction des règles et du contexte.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 20%

---

# Utilisation de formules pour classer les parcours {#journey-ranking-formulas}

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

[!DNL Adobe Journey Optimizer] vous permet de contrôler les parcours qu’un profil peut entrer lorsqu’ils sont qualifiés pour plus que ce que le système autorise. Pour ce faire, vous pouvez utiliser [ensembles de règles](rule-sets.md) pour définir des limites sur l’entrée de parcours ou la simultanéité. Lorsqu’un profil est éligible à plus de parcours que la limite ne le permet, la priorité attribuée à chaque parcours détermine les parcours sélectionnés.

Au lieu d’utiliser la priorité, vous pouvez également utiliser des **formules de classement** pour ajuster dynamiquement le classement des parcours en fonction des attributs de parcours, des attributs de profil ou des scores de modèle d’IA.

Les formules vous offrent plus de flexibilité que la priorité statique. Par exemple, vous pouvez stimuler un parcours pour les membres fidèles Gold.

<!--
>[!NOTE]
>
>Journey ranking formulas follow the same guardrails as decisioning ranking formulas (nesting depth, rule string size). [Learn more about Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md#ranking-formulas).-->

## Créer une formule de classement {#create-journey-ranking-formula}

Pour créer une formule de classement pour vos parcours, procédez comme suit.

1. Accédez à la section **[!UICONTROL Classement d&#39;orchestration]**, puis sélectionnez l&#39;onglet **[!UICONTROL Formules de classement]**. La liste des formules créées précédemment s’affiche.

1. Cliquez sur **[!UICONTROL Créer une formule]**.

1. Indiquez le nom de la formule et ajoutez une description, le cas échéant.

   ![Volet de détails de formule avec les champs de nom et de description](assets/journey-formula-details.png){width="80%"}


   >[!NOTE]
   >
   >L&#39;objet de classement est l&#39;entité à laquelle la formule de classement s&#39;appliquera. Par défaut, l&#39;objet de classement est défini sur **[!UICONTROL Parcours]**.

   <!--
    Selecting a formula entity specifies which type of item—such as journeys or other entities—the ranking formula will apply to. This determines the context in which the formula operates, allowing you to define rules that influence how those items are ranked.-->

1. Si vous le souhaitez, cliquez sur **[!UICONTROL Sélectionner un modèle d’IA]** pour définir le modèle à utiliser comme référence pour créer votre formule de classement.

<!--
    >[!NOTE]
    >
    >[Personalized optimization models](../experience-decisioning/ranking/personalized-optimization-model.md) using continuous metrics are not supported with the AI formula builder.

    Every time you refer to a model score when defining your formula below, the AI model that you selected will be used. [Learn more on AI models](../experience-decisioning/ranking/ai-models.md)-->

1. Dans la section **[!UICONTROL Critère 1]**, indiquez à quels parcours vous souhaitez appliquer un score de classement en procédant comme suit :

   * sélectionner un attribut de parcours [&#128279;](../building-journeys/journey-properties.md) (par exemple le nom du parcours, les balises, la priorité ou d’autres propriétés de parcours) ;
   * sélectionner un opérateur logique;
   * ajouter une condition correspondante - vous pouvez saisir/sélectionner une valeur ou choisir un attribut de profil.

   ![Section du critère 1 avec attribut de parcours, opérateur et condition correspondante](assets/journey-formula-criterion-1.png){width="70%"}

1. Vous pouvez éventuellement spécifier des éléments supplémentaires pour affiner les conditions correspondantes afin que vos critères soient vrais.

   ![Condition supplémentaire pour affiner les critères de correspondance](assets/journey-formula-additional-condition.png){width="70%"}

   Par exemple, vous avez défini *Critère 1* tel que *Balises de Parcours* contenir *Fidélité*. De plus, vous pouvez ajouter une autre condition, telle que si le *Statut de fidélité* est égal à *Or*, alors *Critère 1* est vrai.

1. Créez une expression qui attribuera un score de classement aux parcours qui remplissent la condition définie ci-dessus. Vous pouvez référencer l’un des éléments suivants :
   * une variable :
      * la priorité du parcours, qui est une valeur manuelle attribuée au parcours lors de la [création d’un parcours &#x200B;](../building-journeys/journey-gs.md) ;
      * le score provenant du modèle d’IA que vous avez éventuellement sélectionné ci-dessus ;
   * un attribut :
      * tout attribut susceptible de résider sur le profil, tel qu’un score de propension dérivé de l’extérieur ;
      * un attribut de parcours ;
   * une valeur statique que vous pouvez attribuer dans un format libre ;
   * une combinaison de tous les éléments ci-dessus.

   ![Générateur d’expression pour attribuer un score de classement à l’aide de variables, d’attributs ou de valeurs statiques](assets/journey-formula-expression.png){width="70%"}

1. Cliquez sur **[!UICONTROL Ajouter un critère]** pour ajouter un ou plusieurs critères autant de fois que nécessaire. La logique se présente comme suit :
   * Si le premier critère est vrai pour un élément de décision donné, il est prioritaire sur les suivants.
   * Si ce n’est pas le cas, le moteur de décision passe au deuxième critère, et ainsi de suite.

1. Une fois tous vos critères définis, dans le dernier champ, vous pouvez créer une expression qui sera affectée à tous les parcours qui ne répondent pas aux critères ci-dessus.

   ![Champ d’expression pour les parcours qui ne répondent à aucun critère](assets/journey-formula-criteria-not-met.png){width="70%"}

1. Cliquez sur **[!UICONTROL Créer]** pour terminer votre formule de classement.

Vous pouvez maintenant sélectionner cette formule dans la liste pour en afficher les détails et la modifier ou la supprimer. Il est ensuite disponible lorsque vous configurez un ensemble de règles. [Voici comment procéder](#assign-formula-to-ruleset)

### Exemples de formules de classement {#journey-ranking-formula-example}

Examinons les exemples ci-dessous.

+++Exemple 1 : utilisez la priorité de parcours ou le score d’IA en fonction des balises de parcours

![Formule de classement : la balise marketing utilise la priorité du parcours &#x200B;](assets/journey-formula-ex-1.png){width="60%"}

Si le parcours comporte une balise « Marketing », le score de classement est la priorité du parcours.

![Formule de classement : la balise de promotion utilise le score du modèle d’IA](assets/journey-formula-ex-2.png){width="60%"}

Si le parcours comporte une balise « Promo », le score de classement est le score du modèle d’IA.

+++

+++Exemple 2 : booster les parcours de fidélité par statut de profil


![Formule de classement : la balise de fidélité avec le statut Gold utilise la priorité du parcours plus 5](assets/journey-formula-ex-3.png){width="60%"}

Si le parcours comporte une balise « Loyalty » et que le statut de fidélité du profil est Gold, le score de classement utilisé est la priorité du parcours plus 5.

![Formule de classement : la balise de fidélité au statut Argent utilise la priorité parcours plus 2](assets/journey-formula-ex-4.png){width="60%"}

Si le parcours comporte une balise « Fidélité » et que le statut de fidélité du profil est Argent, le score de classement est la priorité du parcours plus 2.

Si aucune des conditions ci-dessus n’est remplie, le score de classement utilisé est la priorité du parcours.

+++

### Utiliser l’éditeur de code {#journey-ranking-formula-code-editor}

Pour exprimer les formules de classement dans la **syntaxe PQL**, basculez vers l’éditeur de code à l’aide du bouton dédié en haut à droite de l’écran. Pour plus d&#39;informations sur l&#39;utilisation de la syntaxe PQL, reportez-vous à la [documentation dédiée](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=fr).

>[!CAUTION]
>
>Cette action vous empêchera de revenir à l’affichage du créateur par défaut pour cette formule.

Vous pouvez ensuite exploiter les attributs de parcours, les attributs de profil et les valeurs statiques pour créer votre formule de classement.

<!--The code editor is similar to the one used in Decisioning ranking formulas. [Learn more](../experience-decisioning/ranking/ranking-formulas.md#ranking-code-editor)-->

## Affectation de la formule à un ensemble de règles {#assign-formula-to-ruleset}

Pour utiliser une formule pour classer vos parcours, vous devez l’affecter à un ensemble de règles.

>[!NOTE]
>
>Les formules sont attribuées au niveau de l’ensemble de règles et non sur des parcours individuels.

1. Dans le menu **[!UICONTROL Business rules]**, créez un jeu de règles à utiliser pour l&#39;arbitrage de parcours. [Voici comment procéder](rule-sets.md#Create)

1. Veillez à sélectionner le domaine **[!UICONTROL Parcours]**.

   ![Propriétés du jeu de règles avec le domaine de Parcours sélectionné](assets/journey-formula-rule-set-journey.png){width="60%"}

1. Dans les propriétés de l’ensemble de règles, définissez la **[!UICONTROL méthode de classement]** sur **[!UICONTROL Formule]** (au lieu de la valeur par défaut **[!UICONTROL Priorité]**).

1. Sélectionnez la formule de classement que vous avez créée dans la liste déroulante.

   ![Ensemble de règles avec formule de classement sélectionné dans la liste déroulante](assets/journey-rule-set-formula.png){width="60%"}

1. Créez les règles de limitation de parcours à ajouter au jeu de règles. [Voici comment procéder](journey-capping.md#create-rule)

1. Enregistrez l’ensemble de règles.

La formule est maintenant affectée à l’ensemble de règles. Vous pouvez ensuite appliquer cet ensemble de règles à vos parcours.

## Application du jeu de règles à un parcours {#assign-rule-set-to-journey}

Pour attribuer l’ensemble de règles à un parcours, procédez comme suit.

1. Créez ou ouvrez le parcours auquel vous souhaitez affecter l’ensemble de règles. [Découvrez comment créer un parcours.](../building-journeys/journey-gs.md)

1. Dans les propriétés du parcours, sélectionnez l’ensemble de règles dans la liste déroulante.  [Découvrez comment procéder](journey-capping.md#apply-capping).

   >[!NOTE]
   >
   >Un seul ensemble de règles à la fois peut être appliqué à un parcours.

1. Enregistrez le parcours.

Tous les parcours qui utilisent cet ensemble de règles seront classés selon la formule sélectionnée lors de l&#39;application de la limitation.

Pour surveiller les performances de vos ensembles de règles et formules de classement, consultez la section [Limitation et conflits de Parcours &#x200B;](../reports/channel-report-cja.md#rule-sets) dans le rapport de présentation.

<!--
## Reporting {#reporting}

Reporting for journey arbitration helps you understand how rule sets and ranking formulas perform:

* **Exclusions** – Whether journeys were excluded from users and which rule set (and reason) prevented entry.
* **Rule set performance** – For each rule set, metrics such as journey enters, journey exclusions, journey engagement, and other optimization metrics.
* **Cross-journey view** – Time-based view of profiles across journeys (e.g. journey enters, failures, exclusions) to see the impact of capping and ranking.

Use these reports to validate that your formulas and caps are behaving as intended and to tune ranking logic over time.-->

