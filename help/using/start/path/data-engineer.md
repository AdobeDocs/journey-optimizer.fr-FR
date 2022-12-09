---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main de Journey Optimizer pour l’ingénieur de données
description: En tant qu’ingénieur de données, découvrez comment utiliser Journey Optimizer.
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Prise en main de l’ingénieur de données {#data-engineer}

En tant que **Ingénieur de données Adobe Journey Optimizer**, préparez et conservez les données de profil client pour alimenter les expériences orchestrées par [!DNL Journey Optimizer], modélisez les données clients et commerciales dans les schémas et configurez les connecteurs source pour l’ingestion de données. Vous pouvez commencer à utiliser [!DNL Adobe Journey Optimizer] une fois que la variable [Administrateur système](administrator.md) vous avez accordé l’accès et préparé votre environnement.


Découvrez comment **identifier des données et créer un schéma et un jeu de données ;** pour intégrer vos données dans Adobe Experience Platform dans cette page.

>[!NOTE]
>
>En savoir plus sur **ingestion de données** in [Documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html){target=&quot;_blank&quot;}.

Les étapes de création d’un espace de noms d’identité et d’un jeu de données activé pour les profils et les profils de test sont détaillées dans les sections ci-dessous :

1. **Création d’un espace de noms d’identité**. Dans Adobe [!DNL Journey Optimizer], **Identités** lier les consommateurs sur plusieurs appareils et canaux, le résultat est un graphique d’identités. Le graphique d’identités lié est utilisé pour personnaliser les expériences en fonction des interactions entre tous les points de contact de votre entreprise.  En savoir plus sur les identités et les espaces de noms d’identité [dans cette page](../../segment/get-started-identity.md).

1. **Création d’un schéma** et l’activer pour les profils. Un schéma est un ensemble de règles qui représente et valide la structure et le format des données. À un niveau élevé, les schémas fournissent une définition abstraite d’un objet du monde réel (une personne, par exemple) et indiquent les données à inclure dans chaque instance de cet objet (prénom, nom, anniversaire, etc.).  En savoir plus sur les schémas [dans cette page](../../data/get-started-schemas.md).

1. **Création de jeux de données** et l’activer pour les profils. Un jeu de données est une structure de stockage et de gestion pour une collecte de données, généralement sous la forme d’un tableau, qui contient un schéma (des colonnes) et des champs (des lignes). Les jeux de données contiennent également des métadonnées qui décrivent divers aspects des données qu’ils stockent. Une fois qu’un jeu de données est créé, vous pouvez le mapper à un schéma existant et y ajouter des données. En savoir plus sur les jeux de données [dans cette page](../../data/get-started-datasets.md).

1. **Configuration des connecteurs de sources**. Adobe Journey Optimzer permet d’ingérer des données à partir de sources externes tout en vous permettant de structurer, d’étiqueter et d’améliorer les données entrantes à l’aide des services Platform. Vous pouvez ingérer des données à partir de diverses sources telles que des applications Adobe, des entrepôts dans le cloud, des bases de données, etc. En savoir plus sur les connecteurs source [dans cette page](../get-started-sources.md).

1. **Créer des profils de test**. Les profils de test sont requis lors de l’utilisation de la variable [mode test](../../building-journeys/testing-the-journey.md) dans un parcours, et à [prévisualiser et tester vos messages](../../email/preview.md) avant l’envoi. Les étapes de création des profils de test sont détaillées [dans cette page](../../segment/creating-test-profiles.md).


En outre, pour pouvoir envoyer des messages dans les parcours, vous devez configurer les **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** et **[!UICONTROL Actions]**. En savoir plus [dans cette section](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* Le **Source de données** La configuration vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours. En savoir plus sur les sources de données [dans cette section](../../datasource/about-data-sources.md).

* **Événements** vous permettent de déclencher vos parcours de manière unitaire pour envoyer des messages, en temps réel, à l’individu qui participe au parcours. Dans la configuration des événements, vous configurez les événements prévus dans les parcours. Les données des événements entrants sont normalisées conformément au modèle de données d’expérience Adobe (XDM). Les événements proviennent des API d’ingestion en flux continu pour les événements authentifiés et non authentifiés (tels que les événements du SDK Adobe Mobile). En savoir plus sur les événements [dans cette section](../../event/about-events.md).

* [!DNL Journey Optimizer] est fourni avec les fonctionnalités de message intégrées : vous pouvez créer vos messages dans un parcours et concevoir votre contenu. Si vous utilisez un système tiers pour envoyer vos messages, par exemple Adobe Campaign, créez une **action personnalisée**. En savoir plus sur les actions dans cette section [dans cette section](../../action/action.md).
