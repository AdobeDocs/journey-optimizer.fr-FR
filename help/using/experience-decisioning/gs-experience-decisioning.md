---
title: Prise en main de la prise de décision
description: En savoir plus sur la prise de décision
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 6b0735f619379e01e87012ba4300c0ec41334fd4
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 45%

---

# Prise en main de la prise de décision {#get-started-experience-decisioning}

## Présentation de la prise de décision {#about}

La prise de décision simplifie la personnalisation en offrant un catalogue centralisé d’offres marketing connues sous le nom d’« éléments de décision » et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque individu.

Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes grâce au [nouveau canal d’expérience basé sur le code](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/code-based-experience/get-started-code-based), désormais accessible dans les campagnes Journey Optimizer. Les stratégies de décision ne peuvent être utilisées que dans des campagnes d’expérience basées sur du code.

## Mécanismes de sécurisation et limitations {#guardrails}

Pour garantir une utilisation optimale de la prise de décision, gardez à l’esprit les barrières de sécurité et les limites suivantes :

### Barrières de sécurité générales {#general}

* **Éléments d’offre** : chaque collection d’éléments peut contenir jusqu’à 500 éléments d’offre.
* **Attributs personnalisés** : un élément de décision peut inclure un maximum de 100 attributs personnalisés.
* **Stratégies de sélection et éléments de décision par stratégie** : une stratégie de décision prend en charge jusqu’à 10 stratégies de sélection et éléments de décision combinés.

### Règles d’éligibilité {#eligibility}

* **Niveaux d’imbrication** : la profondeur d’imbrication est limitée à 30 niveaux. Ceci est mesuré en comptant les parenthèses fermantes `)` dans la chaîne PQL.
* **Taille de chaîne de règle** : la taille d’une chaîne de règle peut aller jusqu’à 15 Ko pour les caractères codés en UTF-8. Cela équivaut à 15 000 caractères ASCII (1 octet chacun) ou 3 750 à 7 500 caractères non ASCII (2 à 4 octets chacun).

### Formules de classement {#ranking}

* **Niveaux d’imbrication** : la profondeur d’imbrication est limitée à 30 niveaux. Ceci est mesuré en comptant les parenthèses fermantes `)` dans la chaîne PQL.
* **Taille de chaîne de formule** : la taille d’une chaîne de règle peut aller jusqu’à 8 Ko pour les caractères codés en UTF-8. Cela équivaut à 8 000 caractères ASCII (1 octet chacun) ou 2 000 à 4 000 caractères non ASCII (2 à 4 octets chacun).

## Étapes clés de prise de décision {#steps}

Les principales étapes à suivre pour utiliser le service de prise de décision sont les suivantes :

1. **Attribuez les autorisations appropriées**. La prise de décision n’est disponible que pour les utilisateurs ayant accès à un **[!UICONTROL rôle]** lié à la prise de décision, tel que les gestionnaires de décision. Si vous ne pouvez pas accéder à la prise de décision, vos autorisations doivent être étendues.

   +++Découvrir comment attribuer le rôle de personne gestionnaire de décision

   1. Pour attribuer un rôle à un utilisateur ou une utilisatrice dans le produit [!DNL Permissions], accédez à l’onglet **[!UICONTROL Rôles]** et sélectionnez le rôle de personne gestionnaire de décision.

      ![](assets/decision_permission_1.png)

   1. Dans l’onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter un utilisateur]**.

      ![](assets/decision_permission_2.png)

   1. Saisissez le nom ou l’adresse e-mail de votre utilisateur ou utilisatrice, ou sélectionnez l’utilisateur ou l’utilisatrice dans la liste, puis cliquez sur **[!UICONTROL Enregistrer]**.

      Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez la [documentation relative à l’ajout d’utilisateurs et d’utilisatrices](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   La personne doit alors recevoir un e-mail la redirigeant vers votre instance.

+++

1. **Configurez des attributs personnalisés** : personnalisez le catalogue d’éléments selon vos besoins spécifiques en configurant des attributs personnalisés dans le schéma du catalogue.

   ➡️ [Découvrez comment configurer le catalogue d’éléments ](catalogs.md)

1. **Créez des éléments de décision** pour l’afficher à l’audience ciblée.

   ➡️ [Découvrez comment créer des éléments de décision](items.md) ([documentation de l’API](api-reference/decisions-items/create.md))

1. **Organisez des collections** : utilisez des collections pour classer les éléments de décision en fonction de règles basées sur des attributs. Incorporez des collections dans vos stratégies de sélection afin de déterminer la collection d’éléments de décision à prendre en compte.

   ➡️ [Découvrez comment gérer les collections d’éléments](collections.md) ([documentation de l’API](api-reference/items-collections/create.md))

1. **Créez des règles de décision** : les règles de décision sont utilisées dans les éléments de décision et/ou les stratégies de sélection pour déterminer qui a accès à un élément de décision.

   ➡️ [Découvrez comment créer des règles de décision](rules.md)

1. **Mettez en œuvre des méthodes de classement** : créez des méthodes de classement et appliquez-les dans les stratégies de décision afin de déterminer l’ordre de priorité de sélection des éléments de décision.

   ➡️ [Découvrez comment créer des méthodes de classement](ranking.md)

1. **Créez des stratégies de sélection** : créez des stratégies de sélection qui tirent parti des collections, des règles de décision et des méthodes de classement afin d’identifier les éléments de décision pouvant être affichés dans les profils.

   ➡️ [Découvrez comment créer des stratégies de sélection](selection-strategies.md) ([documentation de l’API](api-reference/selection-strategies/create.md))

1. **Créez une stratégie de décision et incorporez-la dans votre campagne basée sur le code** : les stratégies de décision combinent plusieurs stratégies de sélection pour déterminer les éléments de décision admissibles à afficher pour l’audience prévue.

   ➡️ [Découvrez comment utiliser les stratégies de décision](create-decision.md)
