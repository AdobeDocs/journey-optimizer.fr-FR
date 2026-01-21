---
solution: Journey Optimizer
product: journey optimizer
title: Export de messages dans Journey Optimizer
description: Découvrir comment exporter des messages
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: export, messages, HIPAA, e-mails, SMS, configuration
badge: label="Disponibilité limitée" type="Informative"
hide: true
hidefromtoc: true
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
source-git-commit: 8bc0d28ea3e7c26bd8f7a35d00a73e41f35720d0
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 85%

---

# Exporter le contenu du message {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Conserver et exporter votre contenu envoyé"
>abstract="La sélection de cette option vous permet d’écrire le contenu de l’e-mail ou du SMS envoyé à l’aide de cette configuration dans un jeu de données [!DNL Experience Platform]. Les enregistrements sont conservés pendant 7 jours calendaires à partir de l’ingestion, pendant lesquels vous pouvez les exporter vers votre propre espace de stockage."

>[!AVAILABILITY]
>
>Cette fonctionnalité n’est actuellement disponible que pour un ensemble spécifique d’organisations (disponibilité limitée). Pour en savoir plus, contactez votre représentant Adobe.

**L’export de messages** vous permet de transférer le contenu des e-mails et des SMS envoyés à partir de [!DNL Journey Optimizer] vers votre propre espace de stockage via des destinations [!DNL Adobe Experience Platform], qui permettent de diffuser des données provenant d’[!DNL Experience Platform] vers des points d’entrée externes. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/home){target="_blank"}

Grâce à cette fonctionnalité, le contenu des e-mails et des SMS envoyés via [!DNL Journey Optimizer] marqués pour l’export est écrit dans le **jeu de données d’export de messages AJO** d’[!DNL Experience Platform].

Les enregistrements sont ensuite conservés dans le **jeu de données d’exportation de messages AJO** pendant sept jours calendaires à partir de l’ingestion, pendant lesquels vous pouvez les exporter vers le système externe de votre choix.
<!--
## Terminology

* **[!DNL Experience Platform] destinations** - Framework to deliver data out of Experience Platform into external endpoints. [Learn more](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/home){target="_blank"}
* **AJO Message Export Dataset** - An [!DNL Experience Platform] dataset which stores the message content of email and SMS messages sent via [!DNL Journey Optimizer] which have been marked for export.
* **Retention**: Records in the AJO Message Export Dataset are retained for 3 calendar days from ingestion.-->

## Mécanismes de sécurisation

* Cette fonctionnalité prend uniquement en charge les canaux E-mail et SMS.
* Les enregistrements du jeu de données d’exportation de messages d’AJO sont conservés pendant sept jours calendaires à compter de l’ingestion.
* Le renvoi n’est pas pris en charge pour les messages envoyés avant l’activation de l’export des messages, comme décrit ci-dessous.

## Activer l’export des messages {#enable-message-export}

Le processus d’intégration de la fonctionnalité d’export de messages comporte deux étapes :

1. [Configurer le flux de données d’export](#set-up-export-dataflow) dans [!DNL Experience Platform] ;
1. [Activer l’export des messages](#config-message-export) au niveau de la configuration du canal dans [!DNL Journey Optimizer].

>[!WARNING]
>
>Seuls les nouveaux enregistrements s’affichent après l’activation des exports et l’envoi des messages. Les renvois de contenu avant la configuration du processus d’export et l’activation de l’option Export des messages ne sont pas pris en charge.

### Configurer le flux de données d’export {#set-up-export-dataflow}

Avant de pouvoir exporter vos données, vous devez configurer le processus d’export en définissant la destination [!DNL Experience Platform] et le jeu de données qui sera utilisé. Suivez les étapes ci-après.

>[!NOTE]
>
>Cette configuration doit être effectuée pour chaque sandbox.

1. Choisissez un [type de destination](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/destination-types){target="_blank"} Experience Platform. Une liste des plateformes de destination disponibles prêtes à recevoir des données est disponible sur [cette page](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/catalog/overview){target="_blank"}.

1. Dans [!DNL Experience Platform], configurez votre destination en définissant les informations d’identification, le compartiment/conteneur, le préfixe du chemin d’accès et les options de sécurité. [Voici comment procéder](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. Créez un flux d’export de jeu de données à l’aide des données suivantes :

   * Jeu de données source : sélectionnez **jeu de données d’export de messages AJO**.
   * Format de fichier : sélectionnez JSON ou Parquet (choisissez-le en fonction des outils déployés).
   * Planification : assurez-vous qu’elle s’exécute dans la fenêtre de conservation de 7 jours.

### Activer l’export des messages dans la configuration de canal {#config-message-export}

Pour appliquer l’export des messages à vos campagnes et à vos parcours, vous devez activer l’option dédiée au niveau de la configuration des canaux. Suivez les étapes ci-après.

1. Dans [!DNL Journey Optimizer], modifiez ou créez la [configuration de canal](channel-surfaces.md#create-channel-surface) E-mail ou SMS souhaitée.

1. Sélectionnez l’option **[!UICONTROL Activer l’export des messages]**.

   ![](assets/config-message-export.png)

1. Enregistrez vos modifications et validez votre configuration de canal.

Les e-mails et les SMS envoyés via des campagnes ou des parcours à l’aide de cette configuration de canal sont écrits dans le **jeu de données d’export de messages AJO**. Les enregistrements sont ensuite exportés vers la destination de stockage sélectionnée en fonction du flux de données d’export que vous avez défini.

La désactivation de l’option **[!UICONTROL Activer l’export des messages]** empêche l’ingestion dans le jeu de données de nouveaux enregistrements pour cette configuration de canal. Les enregistrements existants sont conservés jusqu’à l’expiration de la période de rétention.
