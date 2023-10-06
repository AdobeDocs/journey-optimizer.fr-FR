---
title: Prise en main de la prise de décision basée sur l’expérience
description: En savoir plus sur Experience Decisioning
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Version Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 18%

---

# Prise en main de la prise de décision basée sur l’expérience {#get-started-experience-decisioning}

>[!BEGINSHADEBOX]

Ce guide couvre les sujets suivants :

* **[Prise en main de la prise de décision basée sur l’expérience](gs-experience-decisioning.md)**
* Gérer les éléments de décision
   * [Configurer le catalogue d’éléments](catalogs.md)
   * [Créer des éléments de décision](items.md)
   * [Gérer des collections d’éléments](collections.md)
* Configurer la sélection d’éléments
   * [Créer des règles de décision](rules.md)
   * [Créer des méthodes de classement](ranking.md)
* [Créer des stratégies de sélection](selection-strategies.md)
* [Créer des stratégies de décision](create-decision.md)

>[!ENDSHADEBOX]

## Présentation d’Experience Decisioning {#about}

>[!AVAILABILITY]
>
>La fonction de prise de décision relative aux expériences est actuellement disponible en version bêta pour sélectionner uniquement les utilisateurs. Pour rejoindre le programme Beta, contactez l’assistance clientèle d’Adobe.

Experience Decisioning simplifie la personnalisation en offrant un catalogue centralisé d’offres marketing connues sous le nom d’&quot;éléments de décision&quot; et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque individu.

Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes grâce au nouveau canal d’expérience basé sur le code, désormais accessible dans les campagnes Journey Optimizer.

**Limites:**

* Les stratégies de décision ne peuvent être utilisées que dans des campagnes d’expérience basées sur du code.
* Pour l’instant, la limitation de fréquence n’est pas disponible dans Experience Decisioning.

## Étapes clés de la prise de décision d’expérience {#steps}

Les principales étapes pour travailler avec Experience Decisioning sont les suivantes :

1. **Configuration des attributs personnalisés**: personnalisez le catalogue des éléments de décision selon vos besoins spécifiques en configurant des attributs personnalisés dans le schéma du catalogue.

1. **Création d’éléments de décision** pour l’afficher à l’audience ciblée.

1. **Organisation avec des collections**: utilisez des collections pour classer les éléments de décision en fonction de règles basées sur des attributs. Incorporez des collections dans vos stratégies de sélection afin de déterminer la collection d’éléments de décision à prendre en compte.

1. **Créer des règles de décision**: les règles de décision sont utilisées dans les éléments de décision et/ou les stratégies de sélection pour déterminer à qui un élément de décision peut être affiché.

1. **Mise en oeuvre des méthodes de classement**: créez des méthodes de classement et appliquez-les dans les stratégies de décision afin de déterminer l’ordre de priorité de sélection des éléments de décision.

1. **Créer des stratégies de sélection**: créez des stratégies de sélection qui tirent parti des collections, des règles de décision et des méthodes de classement afin d’identifier les éléments de décision pouvant être affichés aux profils.

1. **Incorporation d’une stratégie de décision dans une campagne basée sur du code**: les stratégies de décision combinent plusieurs stratégies de sélection pour déterminer les éléments de décision éligibles à afficher pour l’audience prévue.
