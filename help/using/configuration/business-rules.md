---
solution: Journey Optimizer
product: journey optimizer
title: Règles métier
description: Découvrir comment créer et appliquer des règles métier
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: message, fréquence, règles, pression
hide: true
hidefromtoc: true
badge: label="Version bêta"
exl-id: 07f5f0b4-417e-408e-8d9e-86615c8a3fbf
source-git-commit: f8d257b04d8682bb16fcccd3fd0ef9d5389a058d
workflow-type: ht
source-wordcount: '1426'
ht-degree: 100%

---

# Règles métier {#business-rules}

>[!AVAILABILITY]
>
>Les règles métier sont actuellement disponibles en version bêta pour certains utilisateurs et utilisatrices uniquement.

[!DNL Journey Optimizer] vous permet de contrôler la fréquence à laquelle les personnes recevront un message en définissant des règles cross-canal qui excluront automatiquement les profils sur-sollicités des messages et actions.

Par exemple, pour une marque, une règle peut consister à ne pas envoyer plus de 4 messages marketing par mois à sa clientèle. Pour cela, vous pouvez utiliser une règle de fréquence qui limite le nombre de messages envoyés sur un ou plusieurs canaux au cours d’une période calendaire mensuelle.

Grâce à la création de différents jeux de règles pour améliorer la granularité, [!DNL Journey Optimizer] vous permet d’appliquer le capping de fréquence à différents types de communications marketing. Vous pouvez par exemple créer un jeu de règles pour limiter le nombre de **communications promotionnelles** envoyées à votre clientèle et créer un autre jeu de règles pour limiter le nombre de **newsletters** qu’elle reçoit.

>[!NOTE]
>
>Les règles métier sont différentes de la gestion des désinscriptions, qui permet aux utilisateurs et utilisatrices de se désinscrire de la réception des communications de la part d’une marque. [En savoir plus](../privacy/opt-out.md#opt-out-management)

## Accéder aux jeux de règles {#access-rule-sets}

Les jeux de règles sont disponibles dans le menu **[!UICONTROL Administration]** > **[!UICONTROL Règles métier (version bêta)]**. Toutes les règles sont répertoriées et triées par date de création.

![](assets/rule-sets-list.png)

Cliquez sur le nom d’un jeu de règles pour afficher et modifier son contenu. Toutes les règles incluses dans ce jeu de règles sont répertoriées.

Le menu contextuel en haut à droite vous permet d’effectuer les opérations suivantes :

* Modifier le nom et la description du jeu de règles
* Activer le jeu de règles - [en savoir plus](#activate-rule)
* Supprimer le jeu de règles

![](assets/rule-set-example.png)

Pour chaque règle du jeu de règles, le bouton **[!UICONTROL Autres actions]** vous permet d’effectuer les opérations suivantes :

* Modifier la règle
* Activer la règle [en savoir plus](#activate-rule)
* Supprimer la règle

![](assets/rule-set-example-rules.png)

<!--### Permissions{#permissions-frequency-rules}

To access, create, edit or delete message frequency rules, you must have the **[!UICONTROL Manage frequency rules]** permission. 

Users with the **[!UICONTROL View frequency rules]** permission are able to view rules, but not to modify or delete them.

![](assets/message-rules-access.png)

Learn more about permissions in [this section](../administration/high-low-permissions.md).-->

## Créer un jeu de règles {#create-rule-set}

Pour créer un jeu de règles, procédez comme suit.

1. Accédez à la liste **[!UICONTROL Jeux de règles]**, puis cliquez sur **[!UICONTROL Créer un jeu de règles]**.

   ![](assets/rule-sets-create-button.png)

1. Définissez le nom du jeu de règles, ajoutez une description si nécessaire, puis cliquez sur **[!UICONTROL Enregistrer]**.

   ![](assets/rule-sets-create.png)

   >[!NOTE]
   >
   >Le nom du jeu de règles doit être unique.

1. Vous pouvez maintenant [définir les règles](#create-new-rule) que vous souhaitez ajouter à ce jeu de règles, puis l’[activer](#activate-rule).

   >[!NOTE]
   >
   >Assurez-vous que toutes les règles que vous souhaitez appliquer à vos messages sont également activées dans le jeu de règles.

## Créer une règle {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_category"
>title="Sélectionner la catégorie de règle du message"
>abstract="Lorsqu’elle sont activées et appliquées à un message, toutes les règles de fréquence correspondant à la catégorie sélectionnée seront automatiquement appliquées à ce message. Actuellement, seule la catégorie Marketing est disponible."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_capping"
>title="Définir la limitation de votre règle"
>abstract="Spécifiez le nombre maximal de messages envoyés à un profil client au cours de la période choisie. La limite de fréquence sera basée sur la période calendaire sélectionnée et sera réinitialisée au début de la période correspondante."

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="Définissez le ou les canaux auxquels la règle s’applique."
>abstract="Sélectionnez au moins un canal. Le plafond est calculé sur l’ensemble des canaux."

Pour ajouter une règle à un jeu de règles, procédez comme suit :

1. Dans le jeu de règles que vous venez de créer, cliquez sur **[!UICONTROL Ajouter une règle]**.

   ![](assets/rule-sets-create-rule-button.png)

1. Définissez le nom de la règle.

   >[!NOTE]
   >
   >Le nom du jeu de règles doit être unique.

1. Sélectionnez la catégorie de règle du message.

   >[!NOTE]
   >
   >Actuellement, seule la catégorie **[!UICONTROL Marketing]** est disponible.

1. Dans la liste déroulante **[!UICONTROL Durée]**, sélectionnez une période pour la limitation à appliquer. [En savoir plus](#frequency-cap)

1. Définissez la limitation de votre règle, c’est-à-dire le nombre maximum de messages qui peuvent être envoyés à un profil utilisateur individuel chaque mois, chaque semaine ou chaque jour en fonction de votre sélection ci-dessous.

1. Sélectionnez le canal à utiliser pour cette règle : **[!UICONTROL E-mail]**, **[!UICONTROL SMS]**, **[!UICONTROL Notification push]** ou **[!UICONTROL Courrier]**.

   ![](assets/rule-set-channels.png)

   >[!NOTE]
   >
   >Vous devez sélectionner au moins un canal pour pouvoir créer la règle.

1. Sélectionnez plusieurs canaux si vous souhaitez appliquer une limitation sur tous les canaux sélectionnés en tant que nombre total.

   Par exemple, définissez la limitation sur 5 et sélectionnez les canaux e-mail et SMS. Si un profil a déjà reçu 3 e-mails marketing et 2 SMS marketing pour la période sélectionnée, ce profil sera exclu de la prochaine diffusion de tout e-mail ou SMS marketing.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer la création de la règle. Votre message est ajouté au jeu de règles, au statut **[!UICONTROL Brouillon]**.

   ![](assets/rule-set-rule-created.png)

1. Répétez les étapes ci-dessus pour ajouter autant de règles que nécessaire au jeu de règles.

Vous devez maintenant activer chaque règle avant de pouvoir l’appliquer à n’importe quel message. [En savoir plus](#activate-rule)

>[!NOTE]
>
>Assurez-vous que le jeu de règles est également activé pour pouvoir le sélectionner dans vos messages.

### Limite de fréquence {#frequency-cap}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_duration"
>title="Sélectionner la catégorie de règle du message"
>abstract="Lorsqu’elle sont activées et appliquées à un message, toutes les règles de fréquence correspondant à la catégorie sélectionnée seront automatiquement appliquées à ce message. Actuellement, seule la catégorie Marketing est disponible."

Dans la liste déroulante **[!UICONTROL Durée]**, sélectionnez si vous souhaitez que la limitation soit appliquée tous les mois, toutes les semaines ou chaque jour.

La limite de fréquence est basée sur la période calendaire sélectionnée. Elle est réinitialisée au début de la période correspondante.

![](assets/rule-set-capping-duration.png)

L’expiration du compteur pour chaque période se présente comme suit :

* **[!UICONTROL Mensuelle]** : la limite de fréquence est valable jusqu’au dernier jour du mois à 23:59:59 UTC. Par exemple, la date d’expiration mensuelle pour janvier est le 31 janvier à 23:59:59 UTC.

* **[!UICONTROL Hebdomadaire]** : la limite de fréquence est valable jusqu’au samedi à 23:59:59 UTC de cette semaine, car la semaine calendaire commence le dimanche. L’expiration est indépendante de la création de la règle. Par exemple, si la règle est créée le jeudi, cette règle est valide jusqu’au samedi à 23:59:59.

* **[!UICONTROL Quotidienne]** : la limite de fréquence quotidienne est valable pour la journée jusqu’à 23:59:59 UTC et est réinitialisée à 0 au début de la journée suivante.

### Limite de fréquence quotidienne {#daily-frequency-cap}

>[!CAUTION]
>
>Pour garantir la précision des règles de capping de la fréquence quotidien, l’utilisation de la [Segmentation en streaming](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html?lang=fr){target="_blank"} est obligatoire. En savoir plus sur les méthodes d’évaluation de l’audience dans [cette section](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

Pour toute taille de segment pouvant aller jusqu’à 60 millions de messages par heure<!--not clear-->, vérifiez que vos campagnes sont espacées d’au moins 2 heures.


<!-- Journey example:

* If customer sets a Daily rule under the Global Ruleset for email <= 2/day:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for noon)
   * Journey 789 (scheduled for 1 pm)

   In this example, the Daily Frequency cap will not guarantee <= 2/day. The rule will only be guaranteed when Journeys are at least 2 hours apart:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for 2 pm)
   * Journey 789 (scheduled for 4 pm)-->

Prenons l’exemple suivant : si vous définissez une règle quotidienne dans un jeu de règles pour le canal e-mail qui est inférieur ou égal à 2 jours et que vous créez les campagnes suivantes :
* Campagne A (planifiée à midi)
* Campagne A (planifiée à 15 h 00)
* Campagne B (planifiée à 13 h 00)

Cette configuration ne fonctionnera pas pour deux raisons :
* La limite de fréquence quotidienne n’est pas garantie, car les campagnes ne sont pas distantes de 2 heures.
* Il n’est pas recommandé de planifier la même campagne plusieurs fois par jour pour tirer parti de la limite quotidienne.

L’exemple ci-dessous doit être respecté par la limite de fréquence quotidienne :
* Campagne A (planifiée à midi)
* Campagne B (planifiée à 14 h 00)

<!--* To use the Daily Cap with a Journey, customers can use either an Event Triggered Journey or an Audience Qualified Journey. If customers wish to use the Daily Cap with a Read Audience Journey, they should use a Campaign instead and associate a Local Ruleset with the campaign, following the example given above.-->

## Activer les règles et les jeux de règles {#activate-rule}

Une fois créée, la règle affiche le statut **[!UICONTROL Brouillon]** et n’a encore aucune incidence sur le message. Pour l’activer, cliquez sur le bouton **[!UICONTROL Autres actions]** en regard de la règle et sélectionnez **[!UICONTROL Activer]**.

![](assets/rule-set-activate-rule.png)

Vous devez également activer le jeu de règles pour pouvoir y accéder dans les campagnes ou parcours et l’appliquer à vos messages.

![](assets/rule-set-activate-set.png)

L’activation d’un jeu de règles aura un impact sur tous les messages auxquels il s’applique lors de leur exécution suivante. Découvrez comment [appliquer un jeu de règles à un message](#apply-rule-set).

>[!NOTE]
>
>L’activation complète d’un jeu de règles peut prendre jusqu’à 10 minutes. Vous n’avez pas besoin de modifier des messages ou de republier des parcours pour qu’une règle prenne effet.

<!--Currently, once a rule set is activated, no more rules can be added to that rule set.-->

## Désactiver les règles et les jeux de règles {#deactivate-rule}

Pour désactiver une règle ou un jeu de règles, cliquez sur le bouton **[!UICONTROL Autres actions]** en regard de l’élément souhaité et sélectionnez **[!UICONTROL Désactiver]**.

![](assets/rule-set-inactive-rule.png)

Le statut de la règle devient **[!UICONTROL Inactif]** et la règle ne s’appliquera pas aux futures exécutions de messages. Les messages en cours d&#39;exécution ne seront pas affectés.

>[!NOTE]
>
>La désactivation d’une règle ou d’un jeu de règles n’affecte ou ne réinitialise aucun comptage sur les profils individuels.

## Appliquer une règle de fréquence à un message {#apply-frequency-rule}

Pour appliquer une règle de fréquence à un message, procédez comme suit.

1. Lors de la création d’une [campagne](../campaigns/create-campaign.md), sélectionnez l’un des canaux que vous avez définis pour votre jeu de règles et modifiez le contenu de votre message.

1. Dans l’écran de modification du contenu, cliquez sur le bouton **[!UICONTROL Ajouter une règle métier]**.

1. Sélectionnez le [jeu de règles que vous avez créé](#create-rule-set).

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >Seuls les jeux de règles [activés](#activate-rule) s’affichent dans la liste.

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. Vous pouvez visualiser le nombre de profils exclus de la diffusion dans le [rapport global](../reports/global-report.md) et dans le [rapport dynamique](../reports/live-report.md), où les règles de fréquence seront répertoriées comme une raison possible pour les utilisateurs exclus de la diffusion.

>[!NOTE]
>
>Plusieurs règles peuvent s’appliquer au même canal, mais une fois la limite inférieure atteinte, le profil sera exclu des prochaines diffusions.

<!--
## Example: combine several rules {#frequency-rule-example}

You can combine several message frequency rules, such as described in the example below.

1. [Create a rule](#create-new-rule) called *Overall Marketing Capping*:

   * Select all channels.
   * Set capping to 12 monthly.

   ![](assets/message-rules-ex-overall-cap.png)

1. To further restrict the number of marketing-based push notifications that a user is sent, create a second rule called *Push Marketing Cap*:

   * Select Push channel.
   * Set capping to 4 monthly.

   ![](assets/message-rules-ex-push-cap.png)

1. Save and [activate](#activate-rule) the rule.

1. [Create a message](../building-journeys/journeys-message.md) for every channel you want to communicate through and select the **[!UICONTROL Marketing]** category for each message. [Learn how to apply a frequency rule](#apply-frequency-rule)

   ![](assets/journey-message-category.png)

In this scenario, an individual profile:
* can receive up to 12 marketing messages per month;
* but will be excluded from marketing push notifications after they have received 4 push notifications.-->

Lors du test des règles de fréquence, il est recommandé d’utiliser un nouveau [profil de test](../audience/creating-test-profiles.md), car une fois la limitation de fréquence d’un profil atteinte, il n’est pas possible de réinitialiser le compteur avant la période suivante. La désactivation d’une règle permet aux profils limités de recevoir des messages, mais elle ne supprime pas les incréments de compteur.
