---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des jeux de règles
description: Découvrir comment créer et appliquer des jeux de règles
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: message, fréquence, règles, pression
exl-id: 80bd5a61-1368-435c-9a9a-dd84b9e4c208
source-git-commit: 43fe7ca22a7685944b2b11ca3d1872641d1f4694
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 49%

---

# Capping de la fréquence par canal et type de communication {#rule-sets}

Les ensembles de règles **Canal** appliquent des règles de limitation aux canaux de communication. Par exemple, ne pas envoyer plus d’un e-mail ou d’un SMS par jour.

L’utilisation des ensembles de règles de canal vous permet de définir le capping de la fréquence par type de communication afin d’éviter de surcharger les clients avec des messages similaires. Vous pouvez par exemple créer un jeu de règles pour limiter le nombre de **communications promotionnelles** envoyées à votre clientèle et créer un autre jeu de règles pour limiter le nombre de **newsletters** qu’elle reçoit. Selon le type de campagne que vous créez, vous pouvez ensuite choisir d’appliquer la communication promotionnelle ou le jeu de règles des newsletters.

>[!IMPORTANT]
>
>Pour garantir le bon fonctionnement de la limitation au niveau des canaux, veillez à choisir l’espace de noms de priorité la plus élevée lors de la création d’une campagne ou d’un parcours. Pour en savoir plus sur la priorité des espaces de noms, consultez le [guide sur le service d’identités Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}.

## Créer une règle de limitation de canal

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="Définissez le ou les canaux auxquels la règle s’applique."
>abstract="Sélectionnez au moins un canal. La limitation est calculée sur l’ensemble des canaux."

Pour créer un ensemble de règles de canal, procédez comme suit :

>[!NOTE]
>
>Vous pouvez créer jusqu’à 10 ensembles de règles locales actifs pour chaque domaine de canal et pour le domaine de parcours.

1. Accédez à la liste **[!UICONTROL Jeux de règles]**, puis cliquez sur **[!UICONTROL Créer un jeu de règles]**.

   ![](assets/rule-sets-create-button.png)

1. Sélectionnez le jeu de règles dans lequel vous souhaitez ajouter la règle de limitation ou créez un nouveau jeu de règles :

   * Pour utiliser un jeu de règles existant, sélectionnez-le dans la liste. Les règles de limitation de canal ne peuvent être ajoutées qu’aux ensembles de règles avec le domaine « channel ». Vous pouvez vérifier ces informations dans les listes des jeux de règles, dans la colonne **[!UICONTROL Domaine]**.

     ![](assets/journey-capping-list.png)

   * Pour créer la règle de limitation dans un nouvel ensemble de règles, cliquez sur **[!UICONTROL Créer un ensemble de règles]**, attribuez un nom unique à l’ensemble de règles et sélectionnez « Canal » dans la liste déroulante **[!UICONTROL Domaine de l’ensemble de règles]**, puis cliquez sur **[!UICONTROL Enregistrer]**.

     ![](assets/rule-sets-create.png)

1. Dans l’écran d’ensemble de règles, cliquez sur le bouton **[!UICONTROL Ajouter une règle]** et définissez un nom unique pour la règle.

1. Le champ **Catégorie** spécifie la catégorie de message à laquelle la règle s’applique. Pour l’instant, ce champ est en lecture seule, car seule la catégorie **[!UICONTROL Marketing]** est disponible.

   ![](assets/rule-set-channels.png)

1. Dans le champ **[!UICONTROL Nombre de limitations]**, définissez la limitation de votre règle, c’est-à-dire le nombre maximal de messages qui peuvent être envoyés à un profil utilisateur individuel chaque mois, semaine, jour ou heure, en fonction de votre sélection dans les champs suivants.

1. Dans la liste déroulante **[!UICONTROL Réinitialiser la fréquence de limitation]**, choisissez si vous souhaitez que la limitation soit appliquée toutes les heures, tous les jours, toutes les semaines ou tous les mois. La limite de fréquence est basée sur la période calendaire sélectionnée. Elle est réinitialisée au début de la période correspondante.

   L’expiration du compteur pour chaque période est la suivante :

   * **[!UICONTROL Par heure]** - La limite de fréquence est valide pour le nombre d’heures sélectionné (minimum 3 heures). Le compteur se réinitialise automatiquement au début de chaque fenêtre temporelle. Pour une limitation de fréquence de 3 heures, elle se réinitialise toutes les 3 heures, coïncidant avec la fin d’une heure UTC.

     >[!AVAILABILITY]
     >
     >Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Contactez l’assistance clientèle pour l’activer.

   * **[!UICONTROL Quotidien]** - La limite de fréquence quotidienne est valide pour la journée jusqu’à 23:59:59 UTC et se réinitialise à 0 au début de la journée suivante.
   * **[!UICONTROL Hebdomadaire]** - La limite de fréquence est valide jusqu’au samedi 23:59:59 UTC de cette semaine, car la semaine civile commence le dimanche. La date d’expiration s’applique quelle que soit la date de création de la règle. Par exemple, si la règle est créée le jeudi, cette règle est valide jusqu’au samedi à 23:59:59.
   * **[!UICONTROL Mensuel]** - La limite de fréquence est valide jusqu’au dernier jour du mois, à 23:59:59 UTC. Par exemple, la date d’expiration mensuelle pour janvier est le 31 janvier à 23:59:59 UTC.

   >[!IMPORTANT]
   >
   >* Pour garantir la précision, veillez à choisir l’espace de noms de priorité la plus élevée lors de la création d’une campagne ou d’un parcours. Pour en savoir plus sur la priorité des espaces de noms, consultez le [guide sur le service d’identités Platform.](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}<br/>
   >
   >* La valeur du compteur de profil est mise à jour une fois la communication diffusée. Gardez cela à l’esprit lorsque vous envoyez de grands volumes de communications, car le débit peut entraîner l’obtention de l’e-mail par le destinataire quelques minutes, voire des heures, après le lancement de la communication (dans le cas où vous envoyez des millions de communications simultanément). Cela est important dans le cas où des personnes destinataires reçoivent deux communications de manière rapprochée. Nous vous conseillons d’espacer les communications d’au moins deux heures afin que les personnes destinataires disposent de suffisamment de temps pour recevoir la communication et que la valeur de compteur soit mise à jour en conséquence.

1. Le champ **[!UICONTROL Chaque]** vous permet de répéter les règles de limitation de la fréquence sur plusieurs heures, jours, semaines ou mois, selon la durée spécifiée. Exemple : appliquez la règle de limitation de la fréquence pendant 2 semaines.

   Veillez à saisir une valeur correspondant au type de durée sélectionné : 3-23 pour Horaire, 1-30 pour Quotidien, 1-4 pour Hebdomadaire et 1-3 pour Mensuel.

   Le compteur se réinitialise automatiquement à 0 lorsqu’une nouvelle fenêtre temporelle commence. Pour une limitation de fréquence de 2 jours, cette réinitialisation se produit tous les deux jours à minuit UTC.

1. Sélectionnez le canal à utiliser pour cette règle : **[!UICONTROL E-mail]**, **[!UICONTROL SMS]**, **[!UICONTROL Notification push]** ou **[!UICONTROL Courrier]**.

1. Sélectionnez plusieurs canaux si vous souhaitez appliquer une limitation sur tous les canaux sélectionnés en tant que nombre total.

   Par exemple, définissez la limitation sur 5 et sélectionnez les canaux e-mail et SMS. Si un profil a déjà reçu 3 e-mails marketing et 2 SMS marketing pour la période sélectionnée, ce profil sera exclu de la prochaine diffusion de tout e-mail ou SMS marketing.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer la création de la règle. Votre message est ajouté au jeu de règles, au statut **[!UICONTROL Brouillon]**.

   ![](assets/rule-set-rule-created.png)

1. Répétez les étapes ci-dessus pour ajouter autant de règles que nécessaire au jeu de règles.

1. Lorsque la règle de limitation est prête à être appliquée aux messages, activez l’ensemble de règles et la règle où elle a été ajoutée. [Découvrez comment activer des ensembles de règles](../conflict-prioritization/rule-sets.md#create)

## Appliquer des ensembles de règles à un message {#apply-frequency-rule}

Pour appliquer un ensemble de règles à un message, procédez comme suit :

1. Lors de la création d’un message de parcours ou de campagne, sélectionnez l’un des canaux que vous avez définis pour votre ensemble de règles et modifiez le contenu de votre message

1. Dans l’écran de modification du contenu, cliquez sur le bouton **[!UICONTROL Ajouter une règle métier]**.

1. Sélectionnez l’ensemble de règles que vous avez créé.

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >Seuls les jeux de règles [activés](#activate-rule) s’affichent dans la liste.

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. Avant d’activer votre parcours ou votre campagne, veillez à planifier son exécution au moins 10 minutes à l’avenir.

   Cela laisse suffisamment de temps pour renseigner les valeurs de compteur sur le profil pour la règle métier que vous avez sélectionnée. Si vous activez la campagne immédiatement, les valeurs du compteur de l’ensemble de règles ne seront pas renseignées sur les profils des destinataires et le message ne sera pas comptabilisé dans leurs règles de limitation de la fréquence pour les ensembles de règles personnalisés. En outre, la limitation peut ne pas fonctionner correctement pour les parcours et les campagnes activés immédiatement et les campagnes déclenchées par API.

   ![](assets/rule-set-schedule-campaign.png)

1. Vous pouvez visualiser le nombre de profils exclus de la diffusion dans le [rapport Customer Journey Analytics](../reports/report-gs-cja.md) et dans le [rapport dynamique](../reports/live-report.md), où les règles de fréquence seront répertoriées comme une raison possible pour les personnes exclues de la diffusion.

>[!NOTE]
>
>Plusieurs règles peuvent s’appliquer au même canal, mais une fois la limite inférieure atteinte, le profil sera exclu des prochaines diffusions.

Lors du test des règles de fréquence, il est recommandé d’utiliser un nouveau [profil de test](../audience/creating-test-profiles.md), car une fois la limitation de fréquence d’un profil atteinte, il n’est pas possible de réinitialiser le compteur avant la période suivante. La désactivation d’une règle permet aux profils limités de recevoir des messages, mais elle ne supprime pas les incréments de compteur.

<!--add a new section for default priority namespace.-->

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

## Vidéo pratique {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435531?quality=12)
