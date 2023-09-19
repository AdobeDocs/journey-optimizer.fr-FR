---
title: Méthodes de classement
description: Découvrez comment utiliser les méthodes de classement
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Version Beta"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 8%

---

# Méthodes de classement {#rankings}

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* [Prise en main d’Experience Decisioning](gs-experience-decisioning.md)
* Gestion des éléments de décision
   * [Configuration du catalogue d’éléments](catalogs.md)
   * [Création d’éléments de décision](items.md)
   * [Gestion des collections d’éléments](collections.md)
* Configuration de la sélection d’éléments
   * [Créer des règles de décision](rules.md)
   * **[Création de méthodes de classement](ranking.md)**
* [Créer des stratégies de sélection](selection-strategies.md)
* [Création de stratégies de décision](create-decision.md)

>[!ENDSHADEBOX]

Les méthodes de classement vous permettent de classer les éléments à afficher pour un profil donné. Une fois qu’une méthode de classement a été créée, vous pouvez l’affecter à une stratégie de décision afin de définir les éléments à sélectionner en premier.

Les méthodes de classement sont accessibles à partir de la variable **[!UICONTROL Configuration]** / **[!UICONTROL Méthodes de classement]** . Deux types de méthodes de classement sont disponibles :

* **Formules** vous permettent de définir des règles qui déterminent quel élément doit être présenté en premier, plutôt que de prendre en compte les scores de priorité de l’élément.

* **Modèles AI** vous permettent d’utiliser des systèmes de modèle formés qui exploitent plusieurs points de données pour déterminer quel élément doit être présenté en premier.

![](assets/ranking-create.png)

Vous trouverez des informations détaillées sur chaque type de méthode de classement et sur la manière de les créer dans la documentation de la gestion des décisions, accessible ici :

* [Formules de classement](../offers/ranking/create-ranking-formulas.md)
* [Modèles d’IA](../offers/ranking/ai-models.md)
