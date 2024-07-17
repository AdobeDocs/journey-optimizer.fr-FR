---
solution: Journey Optimizer
product: journey optimizer
title: Personnalisation du contenu dans Journey Optimizer
description: Commencez avec la personnalisation.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: expression, éditeur, commencer, personnalisation
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 100%

---

# Commencer avec la personnalisation{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personnaliser des expériences"
>abstract="Utilisez **Adobe Journey Optimizer** pour adapter vos messages à chaque personne destinataire spécifique en exploitant les données et informations que vous possédez à son sujet. Il peut s’agir de son prénom, de ses centres d’intérêt, de son lieu de vie, de ce qu’il a acheté, etc."

Découvrez les fonctionnalités de personnalisation de [!DNL Adobe Journey Optimizer] pour adapter vos messages à chaque destinataire spécifique en exploitant les données et informations que vous possédez à son sujet. Il peut s’agir de son prénom, de ses centres d’intérêt, de son lieu de vie, de ce qu’il a acheté, etc.

➡️ [Découvrir comment personnaliser un message dans ces vidéos](#video-perso)
➡️ [Découvrir des cas d’utilisation de la personnalisation](personalization-use-case.md)

## Créer des expressions de personnalisation à l’aide d’une syntaxe dédiée {#syntax}

[!DNL Journey Optimizer] utilise une syntaxe de personnalisation simple **intégrée** basée sur Handlebars, qui vous permet de créer des expressions avec du contenu placé entre des accolades doubles **{{}}**. Vous pouvez ajouter plusieurs expressions dans le même contenu ou champ sans restriction. [En savoir plus sur la syntaxe de personnalisation](personalization-syntax.md).

**Exemples :**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Lors du traitement du message (e-mail et notification push), Journey Optimizer remplace l’expression par les données contenues dans la base de données Experience Platform : `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` devient « Bonjour, Jean Dupont ».

## Utiliser les données de profil pour personnaliser les messages {#data}

La personnalisation est basée sur les données de profil gérées par le schéma **Profil individuel XDM** défini dans Adobe Experience Platform. Pour en savoir plus, consultez la [documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"}.

>[!CAUTION]
>Le schéma **Profil individuel XDM** est le seul que vous pouvez utiliser pour personnaliser le contenu dans [!DNL Journey Optimizer].

En outre, vous pouvez également tirer parti des **attributs calculés** pour personnaliser votre contenu. Les attributs calculés sont basés sur des jeux de données d’événements d’expérience activés pour le profil et ingérés dans Adobe Experience Platform. Ils servent de points de données agrégés stockés dans les profils clients qui résument les événements comportementaux individuels. [Découvrez comment utiliser les attributs calculés](../audience/computed-attributes.md).

## Utiliser l’éditeur de personnalisation {#editor}

[!DNL Journey Optimizer] fournit un éditeur de personnalisation dans lequel vous sélectionnez, organisez, personnalisez et validez toutes les données afin de personnaliser votre contenu. Plusieurs outils sont disponibles pour vous aider à créer votre contenu de personnalisation (fonctions d’assistance, bibliothèque d’expressions prédéfinies, favorisation d’attributs, etc.).

* [Découvrez comment utiliser l’éditeur de personnalisation](personalization-build-expressions.md)
* [Découvrez où vous pouvez appliquer la personnalisation](personalization-contexts.md).

## Tutoriels vidéo{#video-perso}

Découvrez comment utiliser les informations d’événement contextuelles d’un parcours pour personnaliser un message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Découvrez comment ajouter une personnalisation basée sur un profil à un message et comment utiliser l’appartenance à une audience comme condition préalable à un bloc de personnalisation.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

