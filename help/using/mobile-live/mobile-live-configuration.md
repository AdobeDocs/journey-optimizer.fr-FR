---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le canal d’activité en direct
description: Découvrez comment configurer votre environnement pour envoyer des activités en direct avec Journey Optimizer.
feature: Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: db85a563-9630-4d87-bf10-9f2515fe8a45
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 100%

---

# Commencer la configuration des activités en direct {#mobile-live-config}

Avant d’envoyer une activité en direct, vous devez configurer votre environnement Adobe Journey Optimizer. Pour ce faire, procédez comme suit :

## Étape 1 : ajouter les informations d’identification push de votre application dans Journey Optimizer (facultatif){#push-credentials-launch}

L&#39;enregistrement des informations d&#39;identification push de l’application mobile est nécessaire pour autoriser Adobe à envoyer des notifications push en votre nom.

L’étape 1 est facultative si vos informations d’identification push ont déjà été configurées, car elles peuvent être réutilisées pour la configuration du canal d’activité en direct. Si aucune information d’identification push n’est définie pour votre application, vous devez les créer. Reportez-vous aux étapes détaillées ci-dessous :

1. Accédez au menu **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres push]** > **[!UICONTROL Informations d’identification push]**.

1. Cliquez sur **[!UICONTROL Créer des informations d’identification push]**.

   ![](assets/credential-1.png)

1. Dans la liste déroulante **[!UICONTROL Plateforme]**, sélectionnez le système d’exploitation :

1. Saisissez l’**[!UICONTROL ID d’application]** de l’application mobile.

   ![](assets/credential-2.png)

1. Activez l’option **[!UICONTROL Appliquer à tous les sandbox]** pour mettre ces informations d’identification push à disposition dans tous les sandbox. Si un sandbox spécifique possède ses propres informations d’identification pour la même paire d’identifiants de plateforme et d’application, ces informations d’identification spécifiques au sandbox sont prioritaires.

1. Activez le bouton **[!UICONTROL Saisir manuellement les informations d’identification push]** pour ajouter vos informations d’identification.

1. Effectuez un glisser-déposer de votre fichier de clé d’authentification de notification push Apple .p8. Cette clé peut être obtenue à partir de la page **Certificats**, **Identifiants** et **Profils**.

1. Indiquez l&#39;**identifiant de clé**. Il s&#39;agit d&#39;une chaîne de 10 caractères attribuée lors de la création de la clé d&#39;authentification p8. Elle se trouve sous l&#39;onglet **Clés** de la page **Certificats**, **Identifiants** et **Profils**.

1. Indiquez l&#39;**identifiant d&#39;équipe**. Il s&#39;agit d&#39;une valeur de chaîne qui se trouve sous l&#39;onglet Abonnement.

1. Cliquez sur **[!UICONTROL Envoyer]** pour créer votre configuration d’application.

## Étape 2 : créer la configuration de votre activité en direct {#config-live-activity}

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez **[!UICONTROL Paramètres généraux]** > **[!UICONTROL Configurations de canal]**. Cliquez sur le bouton **[!UICONTROL Créer une configuration de canal]**.

   ![](assets/config-1.png)

1. Saisissez un nom et une description (facultatif) pour la configuration, puis sélectionnez le canal WhatsApp.

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Sélectionnez **[!DNL Live activity]** en tant que canal.

   ![](assets/config-2.png)

1. Sélectionnez une ou plusieurs **[!UICONTROL actions marketing]** pour associer des politiques de consentement aux messages qui utilisent cette configuration. Toutes les politiques de consentement associées à cette action marketing sont utilisées afin de respecter les préférences de vos clientes et clients. En savoir plus

1. Choisissez iOS comme **[!UICONTROL Plateforme]**.

1. Dans la liste déroulante, sélectionnez le même **[!UICONTROL ID d’application]** que pour les [informations d’identification push](#push-credentials-launch) configurées ci-dessus ou choisissez-en un existant.

   ![](assets/config-3.png)

1. Une fois tous les paramètres configurés, cliquez sur **[!UICONTROL Envoyer]** pour confirmer. Vous pouvez également enregistrer la configuration de canal en tant que brouillon et reprendre son paramétrage ultérieurement.

1. Une fois la configuration de canal créée, elle s’affiche dans la liste avec le statut **[!UICONTROL En cours de traitement]**.

   >[!NOTE]
   >
   >Si les vérifications ne réussissent pas, découvrez les raisons possibles de l’échec dans [cette section](../configuration/channel-surfaces.md).

1. Une fois les contrôles réussis, la configuration de canal obtient le statut **[!UICONTROL Actif]**. Elle est prête à être utilisée pour diffuser des messages.

Vous pouvez maintenant commencer l’intégration avec le SDK mobile d’Adobe Experience Platform pour activer les mises à jour dynamiques en temps réel sur l’écran de verrouillage et la Dynamic Island.

➡️ [En savoir plus sur l&#39;intégration du SDK mobile d’Adobe Experience Platform](mobile-live-configuration-sdk.md)
