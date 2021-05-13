---
title: Personnalisation du contenu dans Journey Optimizer
description: Prise en main de la personnalisation
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 5%

---

# Prise en main {#add-personalization}

![](../assets/do-not-localize/badge.png)

La personnalisation, dans le contexte de Journey Optimizer, est l&#39;action de ciblage d&#39;un message à un abonné spécifique en exploitant les données et informations que vous avez sur lui. Il peut s&#39;agir de son prénom, de ses intérêts, de l&#39;endroit où il vit, et plus encore.

Journey Optimizer utilise une syntaxe de personnalisation simple **inline** basée sur les barres de contrôle qui vous permet de créer des expressions avec des contenus encadrés par des accolades de doublon **{{}}**. Vous pouvez ajouter plusieurs expressions dans le même contenu ou champ sans restriction. Reportez-vous à [Syntaxe de la personnalisation](personalization-syntax.md).

La personnalisation est basée sur les données de profil gérées par le schéma **XDM Individuel** défini dans Adobe Experience Platform. Pour plus d’informations à ce sujet, consultez la [documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr).

>[!CAUTION]
>Le schéma **XDM Individuel** est le seul à pouvoir utiliser pour personnaliser le contenu dans Journey Optimizer.

**Exemples :**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Au cours du **traitement des messages** (courrier électronique et push), l’expression est remplacée par les données contenues dans les bases de données de la plateforme Experience Cloud.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
