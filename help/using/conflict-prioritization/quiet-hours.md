---
solution: Journey Optimizer
product: journey optimizer
title: Définir des heures d’inactivité
description: Découvrez comment créer et appliquer des heures creuses
feature: Rules
topic: Content Management
role: User
level: Intermediate
badge: label="Disponibilité limitée" type="Informative"
keywords: message, fréquence, règles, pression
source-git-commit: f69e482daf457f1c331d158d1bf04b4cfb392197
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 5%

---


# Définir des heures d’inactivité {#quiet-hours}

## Que sont les heures calmes ?

Les **Heures calmes** vous permettent de définir des exclusions temporelles pour les canaux **E-mail**, **SMS**, **Push** et **WhatsApp**. Ils garantissent qu’aucun message n’est envoyé pendant des périodes spécifiques, ce qui vous aide à respecter les préférences des clients et les exigences de conformité.

Vous pouvez appliquer des heures calmes par le biais d’**ensembles de règles** qui peuvent être affectés à des actions individuelles dans des campagnes ou des parcours pour un contrôle précis.

En rationalisant ces processus, vous pouvez améliorer l’expérience client, gagner du temps et garantir la conformité aux règles de communication :

* **Ne réveillez pas votre client** - *Le bon client, le bon canal, le bon moment* est le mantra de nombreux professionnels du marketing. Il est donc logique que le timing soit une partie essentielle du parcours client. En définissant une règle « Heures calmes », les marques contrôlent mieux le moment où les contacts reçoivent les messages, s&#39;assurant qu&#39;ils les reçoivent lorsqu&#39;ils sont plus susceptibles d&#39;agir sur votre message.
* **Convivialité** - Interceptez facilement les communications entre les campagnes et les parcours lorsque vous devez empêcher une audience de recevoir un message sans avoir à arrêter l’ensemble du parcours ou de la campagne.
* **Gain de temps** - Gérez les exclusions au même endroit en créant une **règle basée sur l’heure**, au lieu d’ajouter plusieurs nœuds de condition avec des expressions personnalisées.\
  <!--* **Extra Safeguard** - Benefit from an extra safeguard in case audience criteria or time-window configurations were incorrectly set, ensuring individuals are still excluded when they should be.-->

>[!AVAILABILITY]
>
>Actuellement, les règles relatives aux heures creuses ne sont disponibles que pour un ensemble d’organisations (disponibilité limitée). Pour être ajouté à la liste d’attente, contactez votre représentant Adobe.


➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Mécanismes de sécurisation et limitations

* **Canaux pris en charge** - E-mail, SMS, notification push et WhatsApp.
  <!--* **Custom actions** – For custom actions, only quiet hours rules are enforced. If a rule set also includes other rules (e.g., frequency capping), those rules are ignored.-->
* **Délai de propagation** - Les mises à jour d’une règle d’heures calmes peuvent prendre jusqu’à 12 heures pour être appliquées aux actions de canal qui utilisent déjà cette règle.
  <!--* **Pre-suppression window** – The system begins suppressing communications 30 minutes before quiet hours start, ensuring that no messages are delivered once the quiet period begins.-->
* **Latence de volume élevé** - Dans le cas de communications à volume élevé, le système peut prendre un temps supplémentaire pour commencer à appliquer avec succès les suppressions d’heures calmes.

## Créer des règles d&#39;heures silencieuses

Pour définir des heures de silence, créez une règle dans un ensemble de règles personnalisé. Procédez comme suit :

1. Accédez à **[!UICONTROL Règles métier]** pour accéder à l’inventaire des jeux de règles.

1. Choisissez un ensemble de règles personnalisé existant ou créez-en un :

   +++Créer une règle Heures silencieuses dans un ensemble de règles existant

   Sélectionnez l’ensemble de règles dans l’inventaire. Les règles d’heures creuses ne peuvent être ajoutées qu’aux ensembles de règles avec le domaine « channel ». Vous pouvez vérifier ces informations dans la colonne **[!UICONTROL Domaine]**.

   ![](assets/journey-capping-list.png)

   +++

   +++Création d’une règle « Heures silencieuses » dans un nouvel ensemble de règles

   Cliquez sur **[!UICONTROL Créer un jeu de règles]**, saisissez un nom unique, puis sélectionnez « Canal » dans le menu déroulant **[!UICONTROL Domaine du jeu de règles]**.

   ![](assets/rule-sets-create.png)

   +++

   >[!NOTE]
   >
   >Les heures calmes ne peuvent être définies que dans **ensembles de règles personnalisés**. L’ensemble de règles global ne prend pas en charge la configuration des heures creuses.

1. Dans l’écran d’ensemble de règles, cliquez sur **[!UICONTROL Ajouter une règle]** et attribuez un nom unique à la règle.

1. Le champ **Catégorie** spécifie la catégorie de message à laquelle la règle s’applique. Pour l’instant, ce champ est en lecture seule et est défini par défaut sur **[!UICONTROL Marketing]**.

1. Dans le menu déroulant **[!UICONTROL Type de règle]**, sélectionnez **[!UICONTROL Heures creuses]**.

   ![](assets/quiet-hours-type.png)

1. Dans la section **[!UICONTROL Dates et heures]**, définissez quand appliquer des heures calmes :

   1. Choisissez le **[!UICONTROL Fuseau horaire]** à utiliser :

      * **[!UICONTROL UTC/GMT]** - Appliquez une fenêtre temporelle GMT standard à tous les destinataires de l’audience, quels que soient leurs fuseaux horaires individuels.
      * **[!UICONTROL Utiliser le fuseau horaire local des destinataires]** - Utilisez le champ de fuseau horaire de chaque profil. [En savoir plus sur la gestion des fuseaux horaires dans parcours](../building-journeys/timezone-management.md#timezone-from-profiles)

        >[!IMPORTANT]
        >
        >Si un profil ne dispose d’aucune valeur de fuseau horaire, les heures calmes ne sont pas appliquées pour ce profil.

   1. Spécifiez la période à laquelle les heures calmes doivent s’appliquer.

      * **[!UICONTROL Hebdomadaire]** - Sélectionnez des jours spécifiques de la semaine et un créneau horaire. Vous pouvez également appliquer la règle **[!UICONTROL Toute la journée]** (cette option n’est disponible que pendant 3 jours consécutifs maximum).

        ![](assets/quiet-hours-weekly.png)

      * **[!UICONTROL Date personnalisée]** - Sélectionnez des dates spécifiques dans le calendrier et un intervalle de temps. Vous pouvez également appliquer la règle **[!UICONTROL Toute la journée]** (cette option n’est disponible que pendant 3 jours consécutifs maximum).

        ![](assets/quiet-hours-custom.png)

   1. Cliquez sur le bouton **[!UICONTROL Ajouter d’autres dates]** pour ajouter jusqu’à 5 périodes distinctes.

      ![](assets/quiet-hours-date.png)

1. Dans la section **[!UICONTROL Gérer les actions pendant les heures calmes]**, choisissez comment les messages sont traités pendant la période sélectionnée :

   ![](assets/quiet-hours-queue.png)

   * **[!UICONTROL Message en file d’attente]** - Les messages sont envoyés à la fin de la période d’heures calmes, sauf s’ils sont en pause.

     >[!NOTE]
     >
     >Cette option est disponible uniquement pour les actions de parcours. Si elle est appliquée à une action de campagne, elle se comporte de la même manière que si vous sélectionniez l’option **[!UICONTROL Ignorer le message]**.

   * **[!UICONTROL Ignorer le message]** - Les messages ne sont jamais envoyés. Si vous souhaitez que le parcours ou la campagne contenant le message se termine par l’annulation de l’envoi, sélectionnez **[!UICONTROL Ignorer et quitter le parcours ou la campagne]**.

## Appliquer des heures creuses aux parcours et aux campagnes {#apply}

Une fois votre règle enregistrée et l’ensemble de règles activé, vous pouvez l’appliquer aux actions des parcours et des campagnes. Canaux pris en charge : **E-mail, SMS, Push, WhatsApp**. Parcourez les onglets ci-dessous pour plus d’informations.

>[!BEGINTABS]

>[!TAB Appliquer des actions de canal des heures creuses dans parcours]

1. Ouvrez votre parcours, sélectionnez une [action de canal](../building-journeys/journeys-message.md) et modifiez le contenu de votre message.
1. Cliquez sur le bouton **[!UICONTROL Ajouter une règle métier]** et sélectionnez l’ensemble de règles contenant la règle Heures creuses.

   ![](assets/quiet-hours-apply.png)

   >[!NOTE]
   >
   >Seuls les jeux de règles [activés](#activate-rule) s’affichent dans la liste.

1. Activez votre parcours.

>[!TAB Appliquer des heures calmes aux actions de campagne]

1. Modifiez votre campagne et accédez à l’onglet **[!UICONTROL Actions]**.
1. Dans la section **[!UICONTROL Règles métier]**, sélectionnez l’ensemble de règles contenant la règle Heures creuses.

   ![](assets/quiet-hours-campaign.png)

   >[!NOTE]
   >
   >Seuls les jeux de règles [activés](#activate-rule) s’affichent dans la liste.

1. Activez votre campagne.

>[!ENDTABS]

## Étapes suivantes

Une fois que votre ou vos parcours ont été activés et exécutés, vous pouvez visualiser le nombre de profils exclus de la diffusion dans le rapport [Customer Journey Analytics](../reports/report-gs-cja.md) et dans le [Rapport dynamique](../reports/live-report.md), où les règles relatives aux heures creuses seront répertoriées comme une raison possible pour les utilisateurs exclus de la diffusion.

![](assets/quiet-hours-report.png)





<!--

>[!TAB Apply Quiet hours to custom actions]

1. Open your journey and add or select a custom action in the canvas.

1. In the **[!UICONTROL Business rules]** section, select the rule set containing the Quiet hours rule.

   ![](assets/quiet-hours-custom-action.png)

   >[!NOTE]
   >
   >Only [activated](#activate-rule) rule sets display in the list.

1. Activate your journey.

-->


## Vidéo pratique {#video}

Découvrez comment utiliser la fonction Heures calmes dans Adobe Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3475854?captions=fre_fr&quality=12)
