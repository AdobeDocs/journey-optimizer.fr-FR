---
title: Personnalisation du contenu dans Journey Optimizer
description: Prise en main de la personnalisation
translation-type: tm+mt
source-git-commit: ae0d32c271a77a859ee04d678c884e0203b6a256
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---

# Prise en main de la personnalisation{#add-personalization}

![](../assets/do-not-localize/badge.png)

Les fonctionnalités de personnalisation de Discover Parcours Optimier permettent d&#39;adapter vos messages à chaque destinataire en exploitant les données et informations dont vous disposez à son sujet. Cela peut être son prénom, ses intérêts, où il vit, ce qu&#39;il a acheté, et plus encore.

Journey Optimizer utilise une syntaxe de personnalisation simple **inline** basée sur les barres de contrôle qui vous permet de créer des expressions avec des contenus encadrés par des accolades de doublon **{{}}**. Vous pouvez ajouter plusieurs expressions dans le même contenu ou champ sans restriction. En savoir plus sur [la syntaxe de personnalisation](personalization-syntax.md).

La personnalisation est basée sur les données de profil gérées par le schéma **XDM Individuel** défini dans Adobe Experience Platform. Pour plus d’informations à ce sujet, consultez la [documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

>[!CAUTION]
>Le schéma **Profil individuel XDM** est le seul schéma que vous pouvez utiliser pour personnaliser le contenu dans Journey Optimizer.

**Exemples:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

Lors du traitement du message (courrier électronique et push), Journey Optimizer remplace l’expression par les données contenues dans la base de données de la plate-forme Experience Cloud.

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
