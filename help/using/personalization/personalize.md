---
title: Personnalisation du contenu dans Journey Optimizer
description: Prise en main de la personnalisation
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 51%

---

# Prise en main de la personnalisation{#add-personalization}

![](../assets/do-not-localize/badge.png)

Découvrez les fonctionnalités de personnalisation de Parcours Optimier pour adapter vos messages à chaque destinataire spécifique en exploitant les données et informations que vous possédez à son sujet. Il peut s&#39;agir de son prénom, de ses centres d&#39;intérêt, de son lieu de vie, de ce qu&#39;il a acheté, etc.

Journey Optimizer utilise une syntaxe de personnalisation simple **intégrée** basée sur des barres de contrôle, qui vous permet de créer des expressions avec du contenu encadré par des accolades doubles **{{}}**. Vous pouvez ajouter plusieurs expressions dans le même contenu ou champ sans restriction. En savoir plus dans [Syntaxe de personnalisation](personalization-syntax.md).

La personnalisation est basée sur les données de profil gérées par le schéma **Profil individuel XDM** défini dans Adobe Experience Platform. Pour plus d’informations à ce sujet, consultez la [documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr).

>[!CAUTION]
>Le schéma **XDM Individual Profile** est le seul schéma que vous pouvez utiliser pour personnaliser le contenu dans Journey Optimizer.

**Exemples :**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Lors du traitement du message (email et push), Journey Optimizer remplace l’expression par les données contenues dans la base de données Platform Experience Cloud.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
