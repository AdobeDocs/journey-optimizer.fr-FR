---
solution: Journey Optimizer
product: journey optimizer
title: Jeu de données personnalisé pour les mots-clés entrants
description: Découvrez comment stocker des mots-clés SMS entrants dans un jeu de données personnalisé activé pour un profil dans Adobe Journey Optimizer à l’aide de schémas, de jeux de données et d’informations d’identification d’API SMS Experience Platform.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: d6e5c7fd-c1d6-4137-98cd-138ccde6752f
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
source-git-commit: 07322bd265647528f8e2e4a5f39d7806fd03b565
workflow-type: tm+mt
source-wordcount: 517
ht-degree: 16%

---

# Utiliser un jeu de données personnalisé pour les mots-clés entrants {#custom-dataset-inbound-keywords}

Les mots-clés de SMS entrants peuvent être stockés dans un jeu de données personnalisé activé par profil. La configuration se compose d’un schéma Adobe Experience Platform, d’un jeu de données créé à partir de ce schéma et des informations d’identification de l’API SMS Journey Optimizer qui font référence au jeu de données pour les messages entrants.

>[!NOTE]
>
>Si aucun jeu de données personnalisé n’est configuré, les mots-clés entrants sont stockés par défaut dans le _jeu de données de suivi d’e-mail_ système. Un profil doit avoir au moins un message envoyé par [!DNL Journey Optimizer] avant que les messages entrants ne soient capturés dans ce jeu de données. [En savoir plus sur les jeux de données système](../data/get-started-datasets.md#system-datasets)

Pour plus d’informations sur les schémas, les groupes de champs et les jeux de données, consultez la documentation Adobe Experience Platform suivante :

* [Présentation du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"}
* [Principes de base de la composition des schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=fr){target="_blank"}
* [Présentation des jeux de données](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=fr){target="_blank"}

Pour utiliser un jeu de données personnalisé pour les mots-clés entrants, vous devez effectuer les opérations suivantes :

1. [Créer un schéma](#create-schema)
1. [Créer un jeu de données](#create-dataset)
1. [Configuration des informations d’identification d’API](#configure-api-credentials)

## Créer un schéma {#create-schema}

Un schéma définit la structure et les règles de validation qui s’appliquent aux données ingérées. Composez un schéma d’événement d’expérience pour la collecte de mots-clés entrants en ajoutant les groupes de champs existants répertoriés ci-dessous.

➡️ [En savoir plus sur la création de schémas dans la documentation Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/schema/composition)

1. Dans Adobe Experience Platform, à partir de **[!UICONTROL Gestion des données]**, accédez à **[!UICONTROL Schémas]** et sélectionnez **[!UICONTROL Créer un schéma]**.

   ![](assets/schema-sms-1.png)

1. Choisissez **[!UICONTROL Schéma standard]**.

1. Sélectionnez **[!UICONTROL Événement d’expérience]**.

   ![](assets/schema-sms-2.png)

1. Saisissez un **[!UICONTROL Nom d’affichage]** pour le schéma, puis cliquez sur **[!UICONTROL Terminer]**.

   Le schéma est enregistré et l’éditeur de schémas s’ouvre.

1. Ouvrez **[!UICONTROL Propriétés du schéma]** et activez le schéma pour **[!UICONTROL Profil]**.

   ![](assets/schema-sms-3.png)

1. Dans **[!UICONTROL Groupes de champs]**, ajoutez les groupes de champs existants suivants :

   * [!DNL Adobe CJM ExperienceEvent - Message interaction details]
   * [!DNL Adobe CJM ExperienceEvent - Message Execution Details]
   * [!DNL Adobe CJM ExperienceEvent - Message Profile Details]

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Créer un jeu de données {#create-dataset}

Un jeu de données est le conteneur de stockage pour les données ingérées. Chaque jeu de données est associé à un schéma exactement. Les enregistrements écrits dans le jeu de données doivent être conformes à ce schéma.

1. Dans Adobe Experience Platform, à partir de **[!UICONTROL Gestion des données]**, accédez à **[!UICONTROL Jeux de données]** et sélectionnez **[!UICONTROL Créer un jeu de données]**.

   ![](assets/schema-sms-4.png)

1. Choisissez **[!UICONTROL Créer un jeu de données à partir d’un schéma]**.

1. Sélectionnez le schéma créé dans la section précédente et cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/schema-sms-5.png)

1. Saisissez un **[!UICONTROL Nom]** puis cliquez sur **[!UICONTROL Terminer]**.

1. Dans l’onglet **[!UICONTROL Activité des données]**, activez les données pour **[!UICONTROL Profil]**.

   Sélectionnez la politique **[!UICONTROL Conservation des données]** appropriée aux exigences de gouvernance de l’entreprise.

   ![](assets/schema-sms-6.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Configuration des informations d’identification d’API {#configure-api-credentials}

Configurez les informations d’identification en fonction de votre fournisseur SMS à l’aide de [Prise en main de la configuration des SMS/MMS/RCS](mobile-configuration.md). Suivez ensuite les étapes ci-dessous pour sélectionner le jeu de données entrant personnalisé.

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** `>` **[!UICONTROL Paramètres des SMS]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Créez ou modifiez des informations d’identification en fonction de votre fournisseur.

1. Activez l’option **[!UICONTROL Utiliser un jeu de données personnalisé pour le trafic entrant]**.

1. Sélectionnez le **[!UICONTROL Jeu de données]** créé dans la section précédente.

   ![](assets/schema-sms-7.png)

1. Renseignez les autres champs obligatoires et cliquez sur **[!UICONTROL Enregistrer]**.

   >[!NOTE]
   >
   >Lors de l’enregistrement des informations d’identification d’API, Journey Optimizer vérifie que le jeu de données de mot-clé entrant est correctement configuré. Si la validation échoue, un message d’erreur indique la correction requise.

Une fois les informations d’identification enregistrées, le comportement des messages sortants et entrants reste inchangé ; les mots-clés entrants pour ces informations d’identification sont enregistrés dans le jeu de données personnalisé sélectionné.
