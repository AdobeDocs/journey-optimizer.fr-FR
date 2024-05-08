---
title: Méthodes de classement
description: Découvrez comment utiliser les méthodes de classement.
feature: Experience Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilité limitée"
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 37%

---

# Méthodes de classement {#rankings}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_formulas"
>title="Créer des formules de classement"
>abstract="Les formules vous permettent de définir des règles déterminant l’élément qui doit être présenté en premier au lieu de prendre en compte les scores de priorité de l’élément. Une fois qu’une méthode de classement a été créée, vous pouvez l’affecter à une stratégie de sélection afin de définir les éléments à sélectionner en premier."

Les méthodes de classement vous permettent de classer les éléments à afficher pour un profil donné. Une fois qu’une méthode de classement a été créée, vous pouvez l’affecter à une stratégie de sélection afin de définir les éléments à sélectionner en premier.

Deux types de méthodes de classement sont disponibles :

* Les **formules** vous permettent de définir des règles déterminant l’élément qui doit être présenté en premier au lieu de prendre en compte les scores de priorité de l’élément.

* Les **modèles d’IA** vous permettent d’utiliser des systèmes de modèles entraînés qui exploitent plusieurs points de données pour déterminer l’élément qui doit être présenté en premier.

## Créer des méthodes de classement {#create}

Pour créer une méthode de classement, procédez comme suit :

1. Accédez au **[!UICONTROL Configuration de la stratégie]** , puis sélectionnez **[!UICONTROL Formules]** ou **[!UICONTROL Modèles AI]** selon le type de classement à utiliser.

1. Cliquez sur le bouton **[!UICONTROL Créer une formule]** ou **[!UICONTROL Création d’un modèle AI]** dans le coin supérieur droit de l’écran.

   ![](assets/ranking-create.png)

1. Configurez la formule ou le modèle AI en fonction de vos besoins, puis enregistrez-le.

   Des informations détaillées sur la création de formules de classement et de modèles d’AI sont disponibles dans la documentation de la gestion des décisions :

   * [Formules de classement](../offers/ranking/create-ranking-formulas.md)
   * [Modèles d’IA](../offers/ranking/ai-models.md)


## Utilisation des attributs d’éléments de décision dans les formules {#items}

Les formules de classement sont exprimées dans **Syntaxe PQL** et peut utiliser divers attributs, tels que les attributs de profil, [données contextuelles](context-data.md) et les attributs liés à vos éléments de décision.

Pour exploiter les attributs liés à vos éléments de décision dans des formules, veillez à respecter la syntaxe ci-dessous dans le code de votre formule de classement. Développez chaque section pour plus d’informations :

+++Utilisation des attributs standard des éléments de décision

![](assets/formula-attribute.png)

+++

+++Utilisation des attributs personnalisés des éléments de décision

![](assets/formula-attribute-custom.png)

+++
