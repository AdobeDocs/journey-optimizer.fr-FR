---
title: Créer des politiques de décisions
description: Découvrir comment créer des politiques de décisions
feature: Decisioning
topic: Integrations
role: User
level: Experienced
source-git-commit: 2960ed9c9f7a65cbd7122424c2438a461ee8beab
workflow-type: tm+mt
source-wordcount: '1721'
ht-degree: 70%

---


# Créer des politiques de décision {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Définir le nombre d’éléments à renvoyer"
>abstract="Sélectionnez le nombre d’éléments de décision à renvoyer. Par exemple, si vous sélectionnez 2, les 2 meilleures offres éligibles seront présentées pour la configuration actuelle."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Sélectionner une offre de secours"
>abstract="Un élément d’offre de secours s’affiche pour l’utilisateur ou l’utilisatrice lorsqu’aucune des stratégies de sélection définies pour cette politique de décision n’est qualifiée."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="Qu’est-ce qu’une stratégie ?"
>abstract="La séquence de stratégies de sélection détermine la stratégie qui sera évaluée en premier. Au moins une stratégie est requise. Les éléments de décision des stratégies combinées seront évalués ensemble."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Créer des stratégies"

Pour présenter la meilleure offre et expérience dynamique à vos clients, ajoutez une politique de décision à votre contenu dans une campagne ou un parcours, puis configurez les éléments à renvoyer et la stratégie de sélection à utiliser. Procédez comme suit :

1. [Ajouter une politique de décision](#add) - À partir de l’éditeur Personalization ou du Designer d’e-mail.
1. [Configurer la politique de décision](#configurre) - Ajoutez un nom et indiquez le nombre d’éléments à renvoyer.
1. [Configurer une séquence de stratégie](#strategy) - Sélectionnez les éléments à renvoyer avec la politique de décision.
1. [Sélectionner des offres de secours](#fallback) (facultatif) - Sélectionnez les éléments à afficher si aucun élément ou stratégie de sélection n’est qualifié.
1. [Examiner et enregistrer](#review) la stratégie de sélection

>[!AVAILABILITY]
>
>Pour l’instant, les politiques de décision sont disponibles pour tous les clients pour le canal **Expérience basée sur le code**. Ils sont disponibles pour le canal **E-mail** en tant que Disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

## Ajouter une politique de décision {#add}

1. Ouvrez un parcours ou une campagne, sélectionnez une [action de canal](../building-journeys/journeys-message.md) et modifiez le contenu de votre message.

1. Pour les e-mails, activez/désactivez l’option **[!UICONTROL Activer la prise de décision]**.

   ![](assets/decision-policy-enable.png)

   >[!IMPORTANT]
   >
   >L’activation de la prise de décision efface le contenu d’e-mail existant. Si vous avez déjà conçu votre e-mail, veillez à enregistrer votre contenu en tant que modèle au préalable.
   >
   >Notez qu’aucune politique de décision configurée dans l’e-mail ne sera enregistrée dans le modèle. Si vous appliquez le modèle à un autre e-mail, vous devez reconfigurer la politique.

1. Ouvrez l’**éditeur de personnalisation** pour créer la politique de décision. Pour les e-mails, vous pouvez également utiliser un menu dédié dans le **Concepteur d’e-mail** pour créer une politique de décision. Développez les sections ci-dessous pour explorer les deux méthodes.

   +++Création d’une politique de décision à partir de l’éditeur Personalization

   1. Ouvrez l’éditeur de personnalisation et sélectionnez **[!UICONTROL Politique de décision]**.
   1. Cliquez sur le bouton **[!UICONTROL Ajouter une politique de décision]** pour créer une nouvelle politique.

      ![](assets/decision-code-based-create.png)

   +++

   +++Création d’une politique de décision à partir du Designer d’e-mail

   Sélectionnez un composant dans le contenu de votre e-mail, cliquez sur l’icône **[!UICONTROL Prise de décision]** dans la barre d’outils ou le volet des propriétés, puis sélectionnez **[!UICONTROL Ajouter une nouvelle politique]**.

   La **[!UICONTROL sortie Réutiliser la décision]** vous permet de réutiliser une politique de décision déjà créée dans cet e-mail.

   ![](assets/decision-policy-email-designer.png)

   +++

## Configurer la politique de décision {#configure}

Une fois que vous avez ajouté une nouvelle politique de décision dans votre contenu, l’écran de configuration de la politique de décision s’ouvre.

1. Attribuez un nom à la politique de décision et sélectionnez un catalogue (actuellement limité au catalogue **[!UICONTROL Offres]** par défaut).

1. Sélectionnez le nombre d’éléments à renvoyer. Par exemple, si vous sélectionnez 2, les 2 meilleures offres éligibles seront présentées pour la configuration actuelle.

   ![](assets/decision-code-based-details.png)

   Pour le canal E-mail, le champ **[!UICONTROL Nombre d’éléments]** est défini sur 1 par défaut et ne peut pas être modifié à moins que la politique de décision ne soit ajoutée à partir d’un composant **[!UICONTROL Grille de répétition]**. Pour plus d’informations, développez la section ci-dessous :

   +++Renvoi de plusieurs éléments de décision dans des e-mails à l’aide d’un composant **[!UICONTROL Grille de répétition]**

   1. Faites glisser un composant **[!UICONTROL Grille de répétition]** dans votre e-mail et configurez-le selon vos besoins à l’aide du volet **[!UICONTROL Paramètres]**.

      ![](assets/decision-policy-repeat.png)

   1. Cliquez sur l’icône **[!UICONTROL Prise de décision]** dans la barre d’outils de la zone de travail ou ouvrez le volet **[!UICONTROL Prise de décision]** et sélectionnez **[!UICONTROL Ajouter une politique de décision]**.

   1. Indiquez le nombre d’éléments à renvoyer dans le champ **[!UICONTROL Nombre d’éléments]**, puis configurez la politique de décision comme indiqué ci-dessous. Le nombre maximal d’éléments que vous pouvez sélectionner est limité par le nombre de tuiles définies dans le composant **[!UICONTROL Grille de répétition]**.

   ![](assets/decision-policy-repeat-number.png)

   +++

1. Cliquez sur **[!UICONTROL Suivant]**.

## Configurer une séquence de stratégie {#strategy}

La section **[!UICONTROL Séquence de stratégie]** vous permet de sélectionner les éléments de décision et de configurer des stratégies de sélection à présenter avec la politique de décision.

1. Cliquez sur **[!UICONTROL Ajouter]**, puis sélectionnez le type d’objet à inclure dans la politique :

   ![](assets/decision-code-based-strategy-sequence.png)

   * **[!UICONTROL Stratégie de sélection]** - Les stratégies de décision exploitent les collections associées aux contraintes d’éligibilité et aux méthodes de classement afin de déterminer les éléments à afficher. Vous pouvez sélectionner une ou plusieurs stratégies de sélection existantes ou en créer une à l&#39;aide du bouton **[!UICONTROL Créer une stratégie de sélection]**. [Découvrir comment créer des stratégies de sélection](selection-strategies.md)

   * **[!UICONTROL Élément de décision]** - Sélectionnez des éléments de décision uniques sans avoir à exécuter une stratégie de sélection. Vous pouvez sélectionner un seul élément de décision à la fois. Toutes les contraintes d’éligibilité définies pour l’élément s’appliquent.

   >[!NOTE]
   >
   >Une politique de décision prend en charge jusqu’à 10 stratégies de sélection et éléments de décision combinés. [En savoir plus sur les mécanismes de sécurisation et sur les limitations de la prise de décisions](gs-experience-decisioning.md#guardrails)

1. Lorsque vous ajoutez plusieurs éléments et/ou stratégies de décision, ils sont évalués dans un ordre spécifique. Le premier objet ajouté à la séquence sera évalué en premier, et ainsi de suite. Pour modifier la séquence par défaut, faites glisser et déposez les objets et/ou les groupes afin de les réorganiser selon vos besoins. Pour plus d’informations, développez la section ci-dessous.

   +++Gestion de l’ordre d’évaluation dans une politique de décision

   Une fois que vous avez ajouté des éléments de décision et des stratégies de sélection à votre politique, vous pouvez les organiser pour déterminer leur ordre d’évaluation et combiner des stratégies de sélection à évaluer ensemble.

   L’**ordre séquentiel** dans lequel les éléments et les stratégies seront évalués est indiqué par des chiffres à gauche de chaque objet ou groupe d’objets. Pour déplacer la position d’une stratégie de sélection (ou d’un groupe de stratégies) dans la séquence, effectuez un glisser-déposer vers une autre position.

   ![](assets/decision-code-based-strategy-groups.png)

   >[!NOTE]
   >
   >Seules les stratégies de sélection peuvent être glissées-déposées dans une séquence. Pour modifier la position d’un élément de décision, vous devez le supprimer et l’ajouter à nouveau à l’aide du bouton **[!UICONTROL Ajouter]** après avoir ajouté les autres éléments à évaluer auparavant.

   Vous pouvez également **combiner** plusieurs stratégies de sélection en groupes afin qu’elles soient évaluées ensemble et non séparément. Pour ce faire, cliquez sur le bouton **`+`** sous une stratégie de sélection pour la combiner à une autre. Vous pouvez également effectuer un glisser-déposer d’une stratégie de sélection sur une autre afin de regrouper les deux stratégies dans un groupe.

   >[!NOTE]
   >
   >Les éléments de décision ne peuvent pas être regroupés avec d’autres éléments ou stratégies de sélection.

   Plusieurs stratégies et leur regroupement déterminent la priorité des stratégies et le classement des offres éligibles. La première stratégie a la priorité la plus élevée et les stratégies combinées au sein d’un même groupe ont la même priorité.

   Prenons l’exemple suivant : vous disposez de deux collections, l’une dans la stratégie A et l’autre dans la stratégie B. La demande concerne le renvoi de deux éléments de décision. Supposons qu&#39;il y ait deux offres éligibles pour la stratégie A et trois offres éligibles pour la stratégie B.

   * Si les deux stratégies ne sont **pas combinées** ni dans l’ordre séquentiel (1 et 2), les deux meilleures offres éligibles de la première stratégie seront renvoyées dans la première ligne. S’il n’y a pas deux offres éligibles pour la première stratégie, le moteur de décision passera à la stratégie suivante dans la séquence pour trouver autant d’offres que nécessaire, et renverra finalement une offre de secours si nécessaire.

     ![](assets/decision-code-based-consecutive-strategies.png)

   * Si les deux collections sont **évaluées en même temps**, étant donné qu’il y a deux offres éligibles pour la stratégie A et trois offres éligibles pour la stratégie B, les cinq offres seront regroupées et classées selon la valeur déterminée par leurs méthodes de classement respectives. Comme deux offres sont demandées, les deux meilleures offres éligibles parmi ces cinq offres seront renvoyées.

     ![](assets/decision-code-based-combined-strategies.png)

   **Exemple avec plusieurs stratégies**

   Prenons un exemple où plusieurs stratégies sont divisées en différents groupes. Vous avez défini trois stratégies. Les stratégies 1 et 2 sont combinées dans le groupe 1 et la stratégie 3 est indépendante (groupe 2). Les offres éligibles pour chaque stratégie et leur priorité (utilisée dans l’évaluation de la fonction de classement) sont les suivantes :

   * Groupe 1 :
      * Stratégie 1 - (offre 1, offre 2 et offre 3) - Priorité 1
      * Stratégie 2 - (offre 3, offre 4 et offre 5) - Priorité 1

   * Groupe 2 :
      * Stratégie 3 - (offre 5 et offre 6) - Priorité 0

   Les offres de stratégie ayant la priorité la plus élevée sont évaluées en premier et ajoutées à la liste des offres classées.

   * **Itération 1 :**

     Les offres des stratégies 1 et 2 sont évaluées ensemble (offre 1, offre 2, offre 3, offre 4 et offre 5). Nous arrivons au résultat suivant :

     Offre 1 - 10
Offre 2 - 20
Offre 3 - 30 pour la stratégie 1, 45 pour la stratégie 2. Le critère le plus élevé des deux sera pris en compte (45).
Offre 4 - 40
Offre 5 - 50

     Les offres classées se présentent désormais comme suit : offre 5, offre 3, offre 4, offre 2 et offre 1.

   * **Itération 2 :**

     Les offres de la stratégie 3 sont évaluées (offre 5 et offre 6). Nous arrivons au résultat suivant :

      * Offre 5 : non évaluée, car elle existe déjà dans le résultat ci-dessus.
      * Offre 6 - 60

     Les offres classées sont désormais les suivantes : offre 5 , offre 3, offre 4, offre 2, offre 1 et offre 6.

   +++

1. Lorsque votre stratégie de sélection est prête, cliquez sur **[!UICONTROL Suivant]**.

## Ajouter des offres de secours {#fallback}

Une fois que vous avez sélectionné des éléments de décision et/ou des stratégies de sélection, vous pouvez ajouter des offres de secours qui s’afficheront si aucun des éléments ou aucune des stratégies de sélection ci-dessus n’est qualifié.

Vous pouvez sélectionner n’importe quel élément de la liste, qui affiche tous les éléments de décision créés dans le sandbox actuel. Si aucune stratégie de sélection n’est qualifiée, l’offre de secours est affichée pour l’utilisateur ou utilisatrice, quelles que soient les dates et les contraintes d’éligibilité appliquées à l’élément sélectionné.<!--nor frequency capping when available - TO CLARIFY-->.

![](assets/decision-code-based-strategy-fallback.png)

>[!NOTE]
> Les secours sont facultatifs. Vous pouvez sélectionner jusqu’au nombre d’éléments demandés. Si aucun n’est éligible et qu’aucune solution de secours n’est définie, rien ne s’affiche.

## Vérifier et enregistrer la politique de décision {#review}

Après avoir configuré une stratégie de sélection et ajouté des offres de secours, cliquez sur **[!UICONTROL Suivant]** pour vérifier et enregistrer votre politique de décision, puis cliquez sur **[!UICONTROL Créer]** pour confirmer la création de la politique.

Vous pouvez modifier ou supprimer une politique de décision à tout moment à l’aide du bouton représentant des points de suspension dans l’éditeur de personnalisation, ou dans le menu **[!UICONTROL Prise de décision]** dans le volet des propriétés du composant.

>[!BEGINTABS]

>[!TAB Modifier ou supprimer une politique à partir de l’éditeur de personnalisation]

![](assets/decision-policy-edit.png)

>[!TAB Modifier ou supprimer une politique à partir des propriétés du composant]

![](assets/decision-policy-edit-properties.png)

>[!ENDTABS]

## Attribuer un emplacement (e-mail) {#placement}

Pour les e-mails, vous devez définir un emplacement pour le composant associé à la politique de décision. Pour ce faire, cliquez sur le bouton **[!UICONTROL Prise de décision]** dans le volet des propriétés du composant et sélectionnez **[!UICONTROL Attribuer l&#39;emplacement]**. [En savoir plus sur l’utilisation des emplacements](../experience-decisioning/placements.md)

![](assets/decision-policy-rail.png)

## Étapes suivantes {#next-steps}

Maintenant que vous comprenez comment créer une politique de décision, vous êtes prêt à l’utiliser dans [!DNL Journey Optimizer] canaux pour diffuser des offres.

➡️ [Découvrez comment utiliser les politiques de décision dans les messages](../experience-decisioning/use-decision-policy.md)

