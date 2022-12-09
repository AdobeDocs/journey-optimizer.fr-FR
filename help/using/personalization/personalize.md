---
solution: Journey Optimizer
product: journey optimizer
title: Personnalisation du contenu dans Journey Optimizer
description: Prise en main de la personnalisation.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 6014088011c41fd5f673eb3d36fb0609c4a01270
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Prise en main de la personnalisation{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] fonctionnalités de personnalisation pour adapter vos messages à chaque destinataire spécifique en exploitant les données et informations que vous disposez à leur sujet. Il peut s&#39;agir de leur prénom, de leurs centres d&#39;intérêt, de leur lieu de vie, de ce qu&#39;ils ont acheté, etc.

➡️ [Découvrez comment personnaliser un message dans ces vidéos](#video-perso)
➡️ [Découvrir les cas d’utilisation à l’aide de la personnalisation](personalization-use-case.md)

## Créer des expressions de personnalisation à l’aide d’une syntaxe dédiée {#syntax}

[!DNL Journey Optimizer] utilise une **inline** syntaxe de personnalisation simple basée sur Handlebars qui permet de créer des expressions avec des contenus entourés de deux accolades **{{}**. Vous pouvez ajouter plusieurs expressions dans le même contenu ou champ sans restriction. En savoir plus dans [Syntaxe de la personnalisation](personalization-syntax.md).

**Exemples :**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Lors du traitement du message (email et push), Journey Optimizer remplace l’expression par les données contenues dans la base de données Experience Platform :  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` devient &quot;Bonjour John Doe&quot;.

## Utiliser les données de profil pour personnaliser vos messages {#data}

La personnalisation est basée sur les données de profil gérées par la variable **XDM Individual Profile** schéma défini dans Adobe Experience Platform. En savoir plus dans [Documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

>[!CAUTION]
>Le **XDM Individual Profile** schéma est le seul schéma que vous pouvez utiliser pour personnaliser le contenu dans [!DNL Journey Optimizer].

## Ajout de la personnalisation dans différents contextes {#contexts}

[!DNL Journey Optimizer] permet de personnaliser le contenu et l&#39;affichage des messages de plusieurs manières différentes. En savoir plus sur les contextes dans lesquels vous pouvez effectuer une personnalisation dans [cette section](personalization-contexts.md).

## Utilisation de l’éditeur d’expression {#editor}

[!DNL Journey Optimizer] fournit un éditeur d’expression dans lequel vous pouvez sélectionner, organiser, personnaliser et valider toutes les données afin de créer une personnalisation personnalisée de votre contenu.

Plusieurs outils sont disponibles pour vous aider à créer votre contenu de personnalisation (fonctions d’assistance, bibliothèque d’expressions prédéfinies, attributs favorisant l’écriture, etc.).

En savoir plus sur [!DNL Journey Optimizer] éditeur d’expression dans [cette section](personalization-build-expressions.md)

## Vidéos pratiques{#video-perso}

Découvrez comment utiliser les informations d’événement contextuelles d’un parcours pour personnaliser un message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Découvrez comment ajouter une personnalisation basée sur un profil à un message et comment utiliser l’appartenance à un segment comme condition préalable à un bloc de personnalisation.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
