---
title: Créer des politiques de décisions
description: Découvrir comment créer des politiques de décisions
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: 56a7f3be7777e1c9f73a1c473bd6babf952333f1
workflow-type: tm+mt
source-wordcount: '2745'
ht-degree: 89%

---

# Créer des politiques de décision {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Qu’est-ce qu’une décision ?"
>abstract="Les politiques de décision contiennent toute la logique de sélection afin que le moteur de prise de décision choisisse le meilleur contenu. Les politiques de décision sont spécifiques aux campagnes. Leur objectif est de sélectionner les meilleures offres pour chaque profil, tandis que la création de campagne vous permet d’indiquer comment les éléments de décision sélectionnés doivent être présentés, y compris les attributs d’élément à inclure dans le message."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="À propos de la prise de décision"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="Définir une politique de décision"
>abstract="Une politique de décision vous permet de sélectionner les meilleurs éléments du moteur de prise de décision et de les diffuser à l’audience appropriée."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="À propos de la prise de décision"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="Politique de décision"
>abstract="Une politique de décision vous permet de sélectionner les meilleurs éléments du moteur de décision et de les diffuser à chaque audience."

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="Emplacement"
>abstract="Un emplacement détermine où les éléments renvoyés par le moteur de décision apparaissent dans un message. Vous pouvez suivre leurs performances sur les différents emplacements dans les rapports."

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="Sélectionner des attributs de décision dans un catalogue"
>abstract="Les attributs de décision sont stockés dans le schéma du catalogue. Sélectionnez un attribut que vous souhaitez utiliser ici dans le catalogue sélectionné."

Les politiques de décision sont des conteneurs pour vos offres qui tirent profit du moteur de prise de décision afin de renvoyer dynamiquement le meilleur contenu à diffuser pour chaque membre de l’audience. Leur objectif est de sélectionner les meilleures offres pour chaque profil, tandis que la création de campagne et de parcours vous permet d’indiquer comment les éléments de décision sélectionnés doivent être présentés, y compris les attributs d’élément à inclure dans le message.

## Principales étapes {#key}

Les principales étapes pour utiliser les politiques de décision dans vos messages sont les suivantes :

1. [Créer une politique de décision dans un e-mail ou une expérience basée sur du code](#add-decision)

   Configurez une politique de décision dans votre e-mail ou votre expérience basée sur du code en choisissant le nombre d’éléments à renvoyer, en configurant des stratégies de sélection, des options de secours et l’ordre d’évaluation.

1. [Utiliser la politique de décision dans votre contenu](#use-decision-policy)

   Personnalisez votre contenu avec la sortie et les attributs de la politique de décision des éléments de décision que vous souhaitez afficher dans le message.

1. [Créer des tableaux de bord de reporting](cja-reporting.md)

   Créez des tableaux de bord Customer Journey Analytics personnalisés pour mesurer les performances et obtenir des informations sur la manière dont vos politiques de décision et vos offres sont diffusées et utilisées.

## Mécanismes de sécurisation et limitations

* **Disponibilité limitée - Politique de décision dans les e-mails** : pour l’instant, la création de politique de décision dans les e-mails est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.
* **Pages miroir** : pour l’instant, les éléments de décision ne s’affichent pas dans les pages miroir des e-mails.
* **Type de suivi et de liens** : pour suivre les liens générés par la prise de décision, définissez-les dans le schéma comme « Ressources de prise de décision ». Les liens basés sur les attributs ne pevent pas faire l’objet d’un suivi.
* **Imbrication de politiques de décision dans des e-mails** : vous ne pouvez pas imbriquer plusieurs politiques de décision dans un composant d’e-mail parent auquel est déjà associée une politique de décision.
* **Parcours ou campagnes dupliqués avec prise de décision** : si vous dupliquez un parcours ou une campagne qui inclut une politique de décision, la version dupliquée fait référence à l’e-mail ou à l’expérience basée sur du code d’origine, ce qui entraîne des erreurs. Reconfigurez toujours la politique de décision après la duplication.
* **Politiques de consentement** – les mises à jour des politiques de consentement prennent jusqu’à 48 heures. Si une politique de décision fait référence à un attribut lié à une politique de consentement récemment mise à jour, les modifications ne sont pas appliquées immédiatement.

  De même, si de nouveaux attributs de profil soumis à une politique de consentement sont ajoutés à une politique de décision, ils seront utilisables, mais la politique de consentement qui leur est associée ne sera pas appliquée tant que le délai ne sera pas écoulé.

  Les politiques de consentement ne sont actuellement disponibles que pour les organisations disposant des modules complémentaires Adobe Healthcare Shield et Privacy and Security Shield.

* **Classement AI** : pour l’instant, le classement AI n’est pas pris en charge pour le canal E-mail dans les parcours avec prise de décision.

## Créer une politique de décision dans un e-mail ou une expérience basée sur du code {#add-decision}

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

Pour présenter la meilleure offre dynamique et expérience aux personnes destinataires de vos e-mails et aux visiteurs et visiteuses de votre site web ou de votre application mobile, ajoutez une politique de décision à une campagne ou à un parcours basés sur des e-mails ou du code. Pour ce faire, procédez comme suit.

### Créer une politique de décision {#add}

1. Dans un parcours ou une campagne, ajoutez une action **[!UICONTROL E-mail]** ou **[!UICONTROL Expérience basée sur du code]**.

1. Pour les e-mails, activez **[!UICONTROL Activer la prise de décision]** dans l’écran de configuration.

   ![](assets/decision-policy-enable.png)

   >[!IMPORTANT]
   >
   >L’activation de la prise de décision efface le contenu d’e-mail existant. Si vous avez déjà conçu votre e-mail, veillez à enregistrer votre contenu en tant que modèle au préalable.
   >
   >Notez qu’aucune politique de décision configurée dans l’e-mail ne sera enregistrée dans le modèle. Si vous appliquez le modèle à un autre e-mail, vous devez reconfigurer la politique.

1. Il est possible de créer des politiques dans des expériences basées sur des e-mails et du code à l’aide de l’éditeur de personnalisation. Elles peuvent également être créées dans les e-mails à partir d’un menu dédié dans le Concepteur d’e-mail. Pour plus d’informations, développez les sections ci-dessous.

   +++Éditeur Personalization

   1. Ouvrez l’éditeur de personnalisation et sélectionnez **[!UICONTROL Politique de décision]**.
   1. Cliquez sur le bouton **[!UICONTROL Ajouter une politique de décision]** pour créer une nouvelle politique.

      ![](assets/decision-code-based-create.png)

   +++

   +++Menu Designer d’e-mail **[!UICONTROL prise de décision]**

   1. Sélectionnez un composant, cliquez sur l’icône **[!UICONTROL Prise de décision]** dans la barre d’outils ou le volet des propriétés, puis sélectionnez **[!UICONTROL Ajouter une nouvelle politique]**.

   1. Sélectionnez **[!UICONTROL Réutiliser la sortie de décision]** pour réutiliser une politique de décision déjà créée dans cet e-mail.

      ![](assets/decision-policy-email-designer.png)

   +++

1. Attribuez un nom et sélectionnez un catalogue (actuellement limité au catalogue par défaut **[!UICONTROL Offres]**).

1. Sélectionnez le nombre d’éléments à renvoyer. Par exemple, si vous sélectionnez 2, les 2 meilleures offres éligibles seront présentées pour la configuration actuelle.

   ![](assets/decision-code-based-details.png)

   Pour les e-mails, plusieurs éléments ne peuvent être renvoyés que dans un composant de contenu **[!UICONTROL Grille de répétition]**. Pour plus d’informations, développez la section ci-dessous :

   +++ Renvoyer plusieurs éléments de décision dans les e-mails

   1. Placez un composant **[!UICONTROL Grille de répétition]** dans la zone de travail et configurez-le selon vos besoins à l’aide du volet **[!UICONTROL Paramètres]**.

      ![](assets/decision-policy-repeat.png)

   1. Cliquez sur l’icône **[!UICONTROL Prise de décision]** dans la barre d’outils de la zone de travail ou ouvrez le volet **[!UICONTROL Prise de décision]** et sélectionnez **[!UICONTROL Ajouter une politique de décision]**.

   1. Indiquez le nombre d’éléments à renvoyer dans le champ **[!UICONTROL Nombre d’éléments]**, puis configurez la politique de décision comme indiqué ci-dessous. Le nombre maximal d’éléments que vous pouvez sélectionner est limité par le nombre de tuiles définies dans le composant **[!UICONTROL Grille de répétition]**.

   ![](assets/decision-policy-repeat-number.png)

   +++

1. Cliquez sur **[!UICONTROL Suivant]**.

### Sélection des éléments et des stratégies de sélection {#select}

La section **[!UICONTROL Séquence de stratégies]** vous permet de sélectionner les éléments de décision et les stratégies de sélection à inclure avec la politique de décision.

1. Cliquez sur **[!UICONTROL Ajouter]**, puis sélectionnez le type d’objet à inclure dans la politique :

   * **[!UICONTROL Stratégie de sélection]** : ajoutez une ou plusieurs stratégies de sélection. Les stratégies de décision tirent parti des collections associées aux contraintes d’éligibilité et aux méthodes de classement pour déterminer les éléments à afficher. Vous pouvez sélectionner une stratégie de sélection existante ou en créer une à l’aide du bouton **[!UICONTROL Créer une stratégie de sélection]**. [Découvrir comment créer des stratégies de sélection](selection-strategies.md)

   * **[!UICONTROL Élément de décision]** : ajoutez des éléments de décision uniques à présenter sans avoir à exécuter une stratégie de sélection. Vous pouvez sélectionner un seul élément de décision à la fois. Toutes les contraintes d’éligibilité définies pour l’élément s’appliquent.

   ![](assets/decision-code-based-strategy-sequence.png)

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

1. Cliquez sur **[!UICONTROL Suivant]**.

### Ajouter des offres de secours {#fallback}

Une fois que vous avez sélectionné des éléments de décision et/ou des stratégies de sélection, vous pouvez ajouter des offres de secours qui s’afficheront si aucun des éléments ou aucune des stratégies de sélection ci-dessus n’est qualifié.

Vous pouvez sélectionner n’importe quel élément de la liste, qui affiche tous les éléments de décision créés dans le sandbox actuel. Si aucune stratégie de sélection n’est qualifiée, l’offre de secours est affichée pour l’utilisateur ou utilisatrice, quelles que soient les dates et les contraintes d’éligibilité appliquées à l’élément sélectionné.<!--nor frequency capping when available - TO CLARIFY-->.

![](assets/decision-code-based-strategy-fallback.png)

>[!NOTE]
> Les secours sont facultatifs. Vous pouvez sélectionner jusqu’au nombre d’éléments demandés. Si aucun n’est éligible et qu’aucune solution de secours n’est définie, rien ne s’affiche.

### Enregistrer et gérer les politiques de décision {#save}

Lorsque votre politique de décision est prête, enregistrez-la et cliquez sur **[!UICONTROL Créer]**.

Pour les e-mails, vous devez définir un emplacement pour le composant associé à la politique de décision. Pour ce faire, cliquez sur le bouton **[!UICONTROL Prise de décision]** dans le volet des propriétés du composant et sélectionnez **[!UICONTROL Attribuer un emplacement]**. [En savoir plus sur l’utilisation des emplacements](../experience-decisioning/placements.md)

![](assets/decision-policy-rail.png)

Vous pouvez modifier ou supprimer une politique de décision à tout moment à l’aide du bouton représentant des points de suspension dans l’éditeur de personnalisation, ou dans le menu **[!UICONTROL Prise de décision]** dans le volet des propriétés du composant.

>[!BEGINTABS]

>[!TAB Modifier ou supprimer une politique à partir de l’éditeur de personnalisation]

![](assets/decision-policy-edit.png)

>[!TAB Modifier ou supprimer une politique à partir des propriétés du composant]

![](assets/decision-policy-edit-properties.png)

>[!ENDTABS]

## Utiliser une politique de décision dans votre contenu {#use-decision-policy}

Après création, la politique de décision et les attributs liés aux éléments de décision renvoyés peuvent être utilisés dans votre contenu pour le personnaliser. Pour ce faire, procédez comme suit :

### Insérer le code de la politique de décision {#insert-code}

1. Ouvrez l’éditeur de personnalisation et accédez au menu **[!UICONTROL Politique de décision]**.

1. Pour les e-mails, cliquez sur **[!UICONTROL Insérer une syntaxe]** pour ajouter le code correspondant à la politique de décision. Pour les expériences basées sur du code, cliquez sur **[!UICONTROL Insérer une politique]**.

   +++Insertion du code de la politique de décision dans les e-mails

   ![](assets/decision-policy-add.png)

   Pour les e-mails, si aucun emplacement n’a été associé au préalable au composant, sélectionnez-en un dans la liste et cliquez sur **[!UICONTROL Attribuer]**.

   ![](assets/decision-policy-placement.png)

   +++

   +++Insertion du code de la politique de décision dans l’expérience basée sur le code

   ![](assets/decision-code-based-add-decision.png)

   +++

   >[!NOTE]
   >
   >Si le bouton d’insertion de code ne s’affiche pas, il se peut qu’une politique de décision ait déjà été configurée pour le composant parent.

1. Le code de la politique de décision est ajouté. Cette séquence sera répétée selon le nombre de renvoi de la politique de décision que vous choisissez. Par exemple, si vous avez choisi de renvoyer 2 éléments lors de la [création de la décision](#add-decision), la même séquence sera répétée deux fois.

### Utiliser des attributs d’éléments de décision {#attributes}

Vous pouvez désormais ajouter tous les attributs de décision que vous souhaitez dans ce code. Les attributs disponibles sont stockés dans le schéma du catalogue **[!UICONTROL Offres]**. Les attributs personnalisés sont stockés dans le dossier **`_<imsOrg`>**, et les attributs standard dans le dossier **`_experience`**. [En savoir plus sur le schéma du catalogue Offres](catalogs.md)

![](assets/decision-code-based-decision-attributes.png)

>[!NOTE]
>
>Pour le suivi des éléments de la politique de décision, l’attribut `trackingToken` doit être ajouté comme suit pour le contenu de la politique de décision :
>&#x200B;>`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

1. Cliquez sur chaque dossier pour le développer. Placez le curseur de votre souris à l’emplacement souhaité, puis cliquez sur l’icône + en regard de l’attribut à ajouter. Vous pouvez ajouter au code autant d’attributs que vous le souhaitez.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. Veillez à placer la boucle `#each` à l’intérieur d’une paire de crochets `[ ]`, ajoutez une virgule juste avant l’élément `/each` de fermeture.

   ![](assets/decision-code-based-wrap-code.png)

1. Vous pouvez également ajouter tout autre attribut disponible dans l’éditeur de personnalisation, tel que des attributs de profil.

   ![](assets/decision-code-based-decision-profile-attribute.png)

### Utiliser les fragments {#fragments}

Si votre politique de décision contient des éléments de décision, y compris des fragments, vous pouvez exploiter ces fragments dans le code de la politique de décision. [En savoir plus sur les fragments](../content-management/fragments.md)

>[!AVAILABILITY]
>
>Actuellement, cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour plus d’informations, contactez votre représentant ou représentante Adobe.

Supposons, par exemple, que vous souhaitiez afficher différents contenus pour plusieurs modèles d’appareils mobiles. Veillez à ajouter des fragments correspondant à ces appareils à l’élément de décision que vous utilisez dans la politique de décision. [Découvrez comment procéder](items.md#attributes).

![](assets/item-fragments.png){width=70%}

Une fois cette opération terminée, vous pouvez utiliser l’une des méthodes suivantes :

>[!BEGINTABS]

>[!TAB Insérer directement le code]

Il vous suffit de copier-coller le bloc de code ci-dessous dans le code de la politique de décision. Remplacez `variable` par l’ID de fragment et `placement` par la clé de référence du fragment :

```
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable}}
```

>[!TAB Suivez les étapes détaillées ]

1. Accédez à la **[!UICONTROL Fonctions d’assistance]** et ajoutez la fonction **Let** `{% let variable = expression %} {{variable}}` au volet de code, où vous pouvez déclarer la variable pour votre fragment.

   ![](assets/decision-let-function.png)

1. Utilisez la **de fonction** Map **>** Get`{%= get(map, string) %}` pour créer votre expression. La carte est le fragment référencé dans l’élément de décision et la chaîne peut être le modèle d’appareil que vous avez saisi dans l’élément de décision en tant que **[!UICONTROL clé de référence du fragment]**.

   ![](assets/decision-map-function.png)

1. Vous pouvez également utiliser un attribut contextuel qui contiendra cet identifiant de modèle d’appareil.

   ![](assets/decision-contextual-attribute.png)

1. Ajoutez la variable que vous avez choisie pour votre fragment en tant qu’ID de fragment.

   ![](assets/decision-fragment-id.png)

>[!ENDTABS]

L’identifiant du fragment et la clé de référence sont sélectionnés dans la section **[!UICONTROL Fragments]** de l’élément de décision.

>[!WARNING]
>
>Si la clé du fragment est incorrecte ou si le contenu du fragment n’est pas valide, le rendu échoue, ce qui entraîne une erreur dans l’appel Edge.

## Dernières étapes {#final-steps}

Une fois que votre contenu est prêt, passez en revue et publiez votre campagne ou votre parcours :

* [Publier un parcours](../building-journeys/publishing-the-journey.md)
* [Vérifier et activer une campagne](../campaigns/review-activate-campaign.md)
* [Publier et activer une expérience basée sur du code](../code-based/publish-code-based.md)

Pour les expériences basées sur du code, dès que votre développeur ou développeuse effectue un appel d’API ou de SDK pour récupérer du contenu pour la surface définie dans votre configuration de canal, les modifications sont appliquées à votre page web ou votre application.

>[!NOTE]
>
>Actuellement, vous ne pouvez pas simuler le contenu de l’interface d’utilisation dans une campagne ou un parcours d’[expérience basée sur du code](../code-based/create-code-based.md) à l’aide de décisions. Une solution de contournement est proposée dans [cette section](../code-based/code-based-decisioning-implementations.md).

Pour évaluer les performances de vos décisions, vous pouvez créer des [tableaux de bord de rapports Customer Journey Analytics personnalisés](cja-reporting.md).
