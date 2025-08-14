---
solution: Journey Optimizer
product: journey optimizer
title: Exportation de messages dans Journey Optimizer
description: Découvrez comment exporter des messages.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: exportation, messages, HIPAA, e-mails, SMS, configuration
badge: label="Disponibilité limitée" type="Informative"
hide: true
hidefromtoc: true
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
source-git-commit: c62653af3c1eacaaf55dcf181d33f2253521e33d
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 4%

---

# Exporter le contenu du message {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Conserver et exporter le contenu envoyé"
>abstract="La sélection de cette option vous permet d’écrire le contenu de l’e-mail ou du SMS envoyé à l’aide de cette configuration dans un jeu de données [!DNL Experience Platform]. Les enregistrements sont conservés pendant 3 jours calendaires, au cours desquels vous pouvez les exporter vers votre propre espace de stockage."

>[!AVAILABILITY]
>
>Actuellement, cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour plus d’informations, contactez votre représentant ou représentante Adobe.

**Exportation de messages** permet de transférer le contenu des e-mails et des SMS envoyés depuis [!DNL Journey Optimizer] vers votre propre stockage via des destinations [!DNL Adobe Experience Platform], qui permettent de diffuser des données provenant de [!DNL Experience Platform] vers des points d’entrée externes. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/destinations/home){target="_blank"}

Grâce à cette fonctionnalité, le contenu des e-mails et des SMS envoyés par l’intermédiaire de [!DNL Journey Optimizer] marqués pour l’exportation est écrit dans le jeu de données d’exportation de messages AJO [!DNL Experience Platform]****.

Les enregistrements sont ensuite conservés dans le **jeu de données d&#39;exportation de messages AJO** pendant trois jours calendaires, au cours desquels vous pouvez les exporter vers le système externe de votre choix.
<!--
## Terminology

* **[!DNL Experience Platform] destinations** - Framework to deliver data out of Experience Platform into external endpoints. [Learn more](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home){target="_blank"}
* **AJO Message Export Dataset** - An [!DNL Experience Platform] dataset which stores the message content of email and SMS messages sent via [!DNL Journey Optimizer] which have been marked for export.
* **Retention**: Records in the AJO Message Export Dataset are retained for 3 calendar days from ingestion.-->

## Mécanismes de sécurisation

* Cette fonctionnalité prend uniquement en charge les canaux E-mail et SMS.
* Les enregistrements du jeu de données d’exportation de messages AJO sont conservés pendant trois jours calendaires à compter de l’ingestion.
* Le renvoi n’est pas pris en charge pour les messages envoyés avant l’activation de l’exportation des messages, comme décrit ci-dessous.

## Activer L’Exportation Des Messages {#enable-message-export}

Le processus d’intégration de la fonctionnalité d’exportation de messages se compose de deux étapes :

1. [Configurer le flux de données d’exportation](#set-up-export-dataflow) dans [!DNL Experience Platform] ;
1. [Activez l’exportation des messages](#config-message-export) au niveau de la configuration du canal dans [!DNL Journey Optimizer].

>[!WARNING]
>
>Seuls de nouveaux enregistrements s’affichent après l’activation des exportations et l’envoi des messages. Les renvois de contenu avant de configurer le processus d’exportation et d’activer l’option Exporter le message ne sont pas pris en charge.

### Configurer le flux de données d’exportation {#set-up-export-dataflow}

Avant de pouvoir exporter vos données, vous devez configurer le processus d’exportation en définissant la destination [!DNL Experience Platform] et le jeu de données qui sera utilisé. Suivez les étapes ci-après.

>[!NOTE]
>
>Cette configuration doit être configurée pour chaque sandbox.

1. Choisissez un Experience Platform [type de destination](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/destination-types){target="_blank"}. Une liste des plateformes de destination disponibles et prêtes à recevoir des données est disponible sur [cette page](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/overview){target="_blank"}.

1. Dans [!DNL Experience Platform], configurez la destination en définissant les informations d’identification, le compartiment/conteneur, le préfixe de chemin d’accès et les options de sécurité. [Voici comment procéder](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. Créez un flux d’exportation de jeu de données à l’aide des données suivantes :

   * Jeu de données Source : sélectionnez **Jeu de données d’exportation de messages AJO**.
   * Format de fichier : sélectionnez JSON ou Parquet (choisissez-en un en fonction des outils en aval).
   * Planification : assurez-vous qu’elle s’exécute dans la fenêtre de conservation de 3 jours.

### Activer l’exportation de messages dans la configuration des canaux {#config-message-export}

Pour appliquer l’exportation de messages à vos campagnes et parcours, vous devez activer l’option dédiée au niveau de la configuration des canaux. Suivez les étapes ci-après.

1. Dans [!DNL Journey Optimizer], modifiez ou créez la configuration de canal E-mail ou SMS souhaitée [configuration de canal](channel-surfaces.md#create-channel-surface).

1. Sélectionnez l’option **[!UICONTROL Activer l’exportation des messages]**.

   ![](assets/config-message-export.png)

1. Enregistrez vos modifications et envoyez la configuration de votre canal.

Les e-mails et SMS envoyés via des campagnes ou des parcours à l’aide de cette configuration de canal sont écrits dans le **Jeu de données d’exportation de messages AJO**. Les enregistrements sont ensuite exportés vers la destination de stockage sélectionnée en fonction du flux de données d’exportation que vous avez défini.

La désactivation du bouton (bascule) **[!UICONTROL Activer l’exportation des messages]** empêche l’ingestion de nouveaux enregistrements pour cette configuration de canal dans le jeu de données. Les enregistrements existants restent jusqu’à l’expiration de la rétention.
