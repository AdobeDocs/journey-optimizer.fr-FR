---
title: Champs d’identité des événements journeyStep
description: Champs d’identité des événements journeyStep
feature: Création de rapports
topic: Gestion de contenu
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 100%

---

# Champs d’identité des événements journeyStep {#sharing-identity-fields}

![](../assets/do-not-localize/badge.png)

Ce mixin est spécifique à journeyStepEvent : cet événement est en relation avec le parcours, et ne dispose pas de l’identityMap décrivant l’identité du profil, le cas échéant.

Pour un événement journeyStepEvent, nous devons également ajouter des champs liés à l’identité :

## profileID

Identifiant de profil

Type : Chaîne

## profileNamespace

Espace de noms de l’identifiant de profil

Type : Chaîne
