---
title: Surveillance de l’exécution des messages
description: Découvrez les directives de surveillance
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Surveillance des messages {#monitor-message-execution}

![](assets/do-not-localize/badge.png)

Pour vous assurer que vos messages sont exécutés, envoyés et remis avec succès, [!DNL Journey Optimizer] offre les capacités de surveillance des messages actuellement publiés et déclenchés. Vous pouvez voir comment vos messages se comportent entre les parcours <!--and APIs--> en temps réel à partir de la liste **[!UICONTROL Exécutions]**.

Pour accéder à cette liste, dans la page d&#39;accueil **[!DNL Journey Optimizer]**, sélectionnez **[!UICONTROL Messages]**, puis cliquez sur l&#39;onglet **[!UICONTROL Exécutions]**.

Cet onglet contient deux vues : **[!UICONTROL vue en direct]** et **[!UICONTROL vue globale]**.

* L&#39;onglet **[!UICONTROL vue en direct]** fournit un **aperçu en temps réel de tous les messages exécutés** déclenchés par un ou plusieurs [parcours](building-journeys/journey.md) **au cours des dernières 24 heures seulement**.

   ![](assets/message-execution-tab-live.png)

   Cette liste est automatiquement actualisée toutes les soixante secondes. Si aucune exécution n’a eu lieu au cours des dernières 24 heures pour un message spécifique, toutes les colonnes afficheront des valeurs nulles (0) pour ce message.

* L&#39;onglet **[!UICONTROL vue globale]** fournit un **aperçu de tous les messages exécutés** déclenchés par un ou plusieurs [parcours](building-journeys/journey.md) **depuis la date du début du message**.

   ![](assets/message-execution-tab-global.png)

   Cette liste est automatiquement actualisée toutes les quatre-vingt-dix minutes. Les données sont agrégées au fil du temps depuis chaque date de début du message.

Si un message est publié mais n’est pas encore déclenché par un parcours, il n’est répertorié dans aucun des onglets. Seuls les éléments suivants sont répertoriés :
* Messages qui ont été déclenchés mais pas encore démarrés (en attente).
* Messages qui ont été déclenchés et qui sont en cours d’exécution (en cours d’exécution).

Pour les messages multicanaux, une ligne par canal est affichée pour chaque message.

![](assets/message-execution-multichannel.png)

Si un message a été utilisé dans plusieurs parcours, la colonne **[!UICONTROL Source]** affiche **[!UICONTROL Multiple]**.

Par défaut, les messages s’affichent à partir de la date d’exécution la plus récente. Cliquez sur l&#39;icône **[!UICONTROL Filtres]** pour rechercher les messages en fonction du canal, de la date de début et/ou de la date de fin.

![](assets/message-execution-tab-filters.png)

La deuxième colonne <!--**[!UICONTROL Quick action]**-->permet d&#39;ouvrir le [message](create-message.md) correspondant et d&#39;accéder au [rapport dynamique](reports/live-report.md) si vous êtes dans la **[!UICONTROL vue dynamique]** ou au [rapport global](reports/global-report.md) si vous êtes dans la **[!UICONTROL vue globale]**.

![](assets/message-execution-open-live-report.png)

Pour chaque exécution de message, plusieurs indicateurs s’affichent :

* **[!UICONTROL Libellé]** du message : Titre du message que vous avez défini lors de  [la création du message](create-message.md).
* **[!UICONTROL ID]** d&#39;exécution : Identificateur généré automatiquement.
* **[!UICONTROL Source]** : Nom du parcours qui exploite ce message.
* **[!UICONTROL Date]** du début : Date et heure auxquelles le message a été exécuté à partir du parcours.
* **[!UICONTROL Exclus]** : Nombre de profils qui ont été exclus de la cible initiale en raison de règles d’exclusion.
* **[!UICONTROL Envoyé]** : Nombre de messages qui ont été envoyés.
* **[!UICONTROL Livré]** : Nombre de messages remis avec succès dans la boîte aux lettres du destinataire (courrier électronique) ou sur le périphérique (push) sans générer de rebond ni d’erreur de diffusion.
* **[!UICONTROL Rebonds]** : Nombre de messages qui ne peuvent pas être remis en raison d’un échec de diffusion. [En savoir plus sur les rebonds](suppression-lists.md#delivery-failures).
* **[!UICONTROL Ouvre]** : Nombre de messages qui ont été ouverts.
* **[!UICONTROL Clics]** : Nombre de clics sur des liens dans un courrier électronique.

   >[!NOTE]
   >
   >Les clics n’existent pas pour les notifications Push : lorsqu’un utilisateur clique sur une notification Push, l’application s’ouvre, qui ne peut être considérée que comme ouverte.

* **[!UICONTROL Erreurs]** : Nombre de messages qui ne peuvent pas être envoyés en raison d&#39;une défaillance technique.

Cliquez sur chaque hyperlien pour ouvrir la vue de résumé du message correspondante. [En savoir plus sur les messages](create-message.md).
