---
title: Prise en main de la prise de décision basée sur l’expérience
description: En savoir plus sur Experience Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Version Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 98e3e770530facac6f9c69a72e77fc663ef5ed0c
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 100%

---

# Prise en main de la prise de décision basée sur l’expérience {#get-started-experience-decisioning}

>[!BEGINSHADEBOX « Ce guide couvre les sujets suivants »]

* **[Commencer avec Experience Decisioning](gs-experience-decisioning.md)**
* Gérer les éléments de décision : [Configurer le catalogue d’éléments](catalogs.md) – [Créer des éléments de décision](items.md) – [Gérer des collections d’éléments](collections.md)
* Configurer la sélection des éléments : [Créer des règles de décision](rules.md) – [Créer des méthodes de classement](ranking.md)
* [Créer des stratégies de sélection](selection-strategies.md)
* [Créer des politiques de décision](create-decision.md)

>[!ENDSHADEBOX]

## Présentation d’Experience Decisioning {#about}

>[!AVAILABILITY]
>
>La fonctionnalité de décision basée sur l’expérience est actuellement disponible en version Beta pour certains utilisateurs et utilisatrices. Pour rejoindre le programme Beta, contactez l’assistance clientèle d’Adobe.
>
>Les stratégies de décision ne peuvent être utilisées que dans des campagnes d’expérience basées sur du code.

Experience Decisioning simplifie la personnalisation en offrant un catalogue centralisé d’offres marketing connues sous le nom d’« éléments de décision » et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque individu.

Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes grâce au nouveau canal d’expérience basé sur le code, désormais accessible dans les campagnes Journey Optimizer.

## Étapes clés d’Experience Decisioning {#steps}

Les principales étapes pour travailler avec Experience Decisioning sont les suivantes :

1. **Configurez des attributs personnalisés** : personnalisez le catalogue des éléments de décision selon vos besoins spécifiques en configurant des attributs personnalisés dans le schéma du catalogue.

1. **Créez des éléments de décision** pour l’afficher à l’audience ciblée.

1. **Organisez des collections** : utilisez des collections pour classer les éléments de décision en fonction de règles basées sur des attributs. Incorporez des collections dans vos stratégies de sélection afin de déterminer la collection d’éléments de décision à prendre en compte.

1. **Créez des règles de décision** : les règles de décision sont utilisées dans les éléments de décision et/ou les stratégies de sélection pour déterminer qui a accès à un élément de décision.

1. **Mettez en œuvre des méthodes de classement** : créez des méthodes de classement et appliquez-les dans les stratégies de décision afin de déterminer l’ordre de priorité de sélection des éléments de décision.

1. **Créez des stratégies de sélection** : créez des stratégies de sélection qui tirent parti des collections, des règles de décision et des méthodes de classement afin d’identifier les éléments de décision pouvant être affichés dans les profils.

1. **Incorporez une politique de décision dans une campagne basée sur du code** : les politiques de décision combinent plusieurs stratégies de sélection pour déterminer les éléments de décision éligibles à afficher pour l’audience prévue.
