---
title: Prise en main de Journey Optimizer pour l’ingénieur de données
description: En tant qu’ingénieur de données, découvrez comment utiliser Journey Optimizer
level: Intermediate
source-git-commit: a27a6d7ab96bd08e7a2601c2e86d1d9f0fc4be0a
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 47%

---

# Prise en main de l’ingénieur de données {#data-engineer}

![ingénieur en données](assets/do-not-localize/user-1.png)

En tant que **Ingénieur de données Adobe Journey Optimizer**, préparez et conservez les données de profil client pour alimenter les expériences orchestrées par [!DNL Journey Optimizer], modélisez les données clients et commerciales dans les schémas et configurez les connecteurs source pour l’ingestion de données. Vous pouvez commencer à utiliser [!DNL Adobe Journey Optimizer] une fois que la variable [Administrateur système](administrator.md) vous avez accordé l’accès et préparé votre environnement.


Découvrez comment **identifier des données et créer un schéma et un jeu de données ;** pour intégrer vos données dans Adobe Experience Platform dans cette page.

>[!NOTE]
>
>En savoir plus sur l’**ingestion de données** dans la [documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=fr){target=&quot;_blank&quot;}.

Les étapes de création d’un espace de noms d’identité et d’un jeu de données activé pour les profils et les profils de test sont détaillées dans les sections ci-dessous :

1. **Création d’un espace de noms d’identité**. En Adobe [!DNL Journey Optimizer], **Identités** lier les consommateurs sur plusieurs appareils et canaux, le résultat est un graphique d’identités. Le graphique d’identité lié est utilisé pour personnaliser les expériences en fonction des interactions entre tous les points de contact de votre entreprise.  En savoir plus sur les identités et les espaces de noms d’identité [dans cette page](../get-started-identity.md).

1. **Création d’un schéma** et l’activer pour les profils. Un schéma est un jeu de règles qui représente et valide la structure et le format des données. À un niveau élevé, les schémas fournissent une définition abstraite d’un objet du monde réel (une personne, par exemple) et indiquent les données à inclure dans chaque instance de cet objet (comme le prénom, le nom, l’anniversaire, etc.).  En savoir plus sur les schémas [dans cette page](../get-started-schemas.md).

1. **Création de jeux de données** et l’activer pour les profils. Un jeu de données est une structure de stockage et de gestion pour la collecte de données, généralement sous la forme d&#39;un tableau, qui contient un schéma (des colonnes) et des champs (des lignes). Les jeux de données contiennent également des métadonnées qui décrivent divers aspects des données stockées. Une fois qu’un jeu de données est créé, vous pouvez le mapper à un schéma existant et y ajouter des données. En savoir plus sur les jeux de données [dans cette page](../get-started-datasets.md).

1. **Configuration des connecteurs de sources**. Adobe Parcours Optimzer permet d’ingérer des données à partir de sources externes tout en vous permettant de structurer, d’étiqueter et d’améliorer les données entrantes à l’aide des services Platform. Vous pouvez ingérer des données provenant de diverses sources telles que les applications Adobe, les stockages dans le cloud, des bases de données, etc. En savoir plus sur les connecteurs source [dans cette page](../get-started-sources.md).

1. **Création de profils de test**. Les profils de test sont requis lors de l’utilisation de la variable [mode test](../building-journeys/testing-the-journey.md) dans un parcours et à [prévisualiser et tester vos messages](../preview.md) avant l’envoi. Découvrez les étapes de création de profils de test [dans cette page](../../using/building-journeys/creating-test-profiles.md).


En outre, pour pouvoir envoyer des messages dans des parcours, vous devez configurer les **[!UICONTROL sources de données]**, les **[!UICONTROL événements]** et les **[!UICONTROL actions]**. En savoir plus dans [cette section](../../using/configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* La configuration des **sources de données** vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours. En savoir plus sur les sources de données [dans cette section](../datasource/about-data-sources.md).

* **Les événements vous permettent de déclencher vos parcours de manière unitaire pour envoyer des messages, en temps réel, à l&#39;individu progressant dans le parcours.** Dans la configuration des événements, vous configurez les événements attendus dans les parcours. Les données des événements entrants sont normalisées conformément au modèle de données Adobe Experience (XDM). Les événements authentifiés et non authentifiés proviennent des API d&#39;ingestion en flux continu (notamment ceux issus du kit de développement Adobe Mobile SDK). En savoir plus sur les événements [dans cette section](../event/about-events.md).

* [!DNL Journey Optimizer] est fourni avec des fonctionnalités de message intégrées : vous pouvez concevoir votre contenu et publier votre message. Si vous utilisez un système tiers pour envoyer vos messages, par exemple Adobe Campaign, créez une **action personnalisée**. En savoir plus sur les actions dans cette section [dans cette section](../action/action.md).
