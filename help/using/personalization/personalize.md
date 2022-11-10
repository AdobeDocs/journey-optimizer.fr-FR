---
solution: Journey Optimizer
product: journey optimizer
title: Personnalisation du contenu dans Journey Optimizer
description: Prise en main de la personnalisation.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 6014088011c41fd5f673eb3d36fb0609c4a01270
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 100%

---

# Prise en main de la personnalisation{#add-personalization}

Découvrez les fonctionnalités de personnalisation de [!DNL Adobe Journey Optimizer] pour adapter vos messages à chaque destinataire spécifique en exploitant les données et informations que vous possédez à son sujet. Il peut s’agir de son prénom, de ses centres d’intérêt, de son lieu de vie, de ce qu’il a acheté, etc.

➡️ [Découvrir comment personnaliser un message dans ces vidéos](#video-perso)
➡️ [Découvrir des cas d’utilisation de la personnalisation](personalization-use-case.md)

## Créer des expressions de personnalisation à l’aide d’une syntaxe dédiée {#syntax}

[!DNL Journey Optimizer] utilise une syntaxe de personnalisation simple **intégrée** basée sur Handlebars, qui vous permet de créer des expressions avec du contenu placé entre des accolades doubles **{{}}**. Vous pouvez ajouter plusieurs expressions dans le même contenu ou champ sans restriction. En savoir plus dans [Syntaxe de personnalisation](personalization-syntax.md).

**Exemples :**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

Lors du traitement du message (e-mail et push), Journey Optimizer remplace l’expression par les données contenues dans la base de données Experience Platform : `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` devient « Bonjour Jean Dupont ».

## Utiliser les données de profil pour personnaliser les messages {#data}

La personnalisation est basée sur les données de profil gérées par le schéma **Profil individuel XDM** défini dans Adobe Experience Platform. Pour en savoir plus, consultez la [documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target=&quot;_blank&quot;}.

>[!CAUTION]
>Le schéma **Profil individuel XDM** est le seul que vous pouvez utiliser pour personnaliser le contenu dans [!DNL Journey Optimizer].

## Ajouter la personnalisation dans différents contextes {#contexts}

[!DNL Journey Optimizer] permet de personnaliser le contenu et l’affichage des messages de plusieurs manières différentes. Apprenez-en plus sur les contextes dans lesquels vous pouvez effectuer une personnalisation dans [cette section](personalization-contexts.md).

## Utiliser l’éditeur d’expression {#editor}

[!DNL Journey Optimizer] fournit un éditeur d’expression dans lequel vous sélectionnez, organisez, personnalisez et validez toutes les données afin de personnaliser le contenu.

Plusieurs outils sont disponibles pour vous aider à créer votre contenu de personnalisation (fonctions d’assistance, bibliothèque d’expressions prédéfinies, favorisation d’attributs, etc.).

En savoir plus sur l’éditeur d’expression de [!DNL Journey Optimizer] dans [cette section](personalization-build-expressions.md).

## Tutoriels vidéo{#video-perso}

Découvrez comment utiliser les informations d’événement contextuelles d’un parcours pour personnaliser un message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Découvrez comment ajouter une personnalisation basée sur un profil à un message et comment utiliser l’appartenance à un segment comme condition préalable à un bloc de personnalisation.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
