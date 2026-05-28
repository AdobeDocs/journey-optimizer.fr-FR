---
title: Commencer à utiliser les API Decisioning
description: Découvrez comment commencer à utiliser les API Decisioning pour gérer par programmation les éléments de décision et diffuser des offres personnalisées.
feature: API, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 78ed06a3-7787-4aab-8373-df7eb40c1727
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/01NgEXGvNxeb1MNkjeB55VNFZFuSiTfQMKeNahfuHWE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 339
ht-degree: 87%

---

# Guide de développement des API Decisioning {#decisioning-api-developer-guide}

Les API Decisioning vous permettent de créer et de gérer par programmation les composants utilisés pour diffuser des offres personnalisées à votre clientèle. Ces API RESTful fournissent des opérations CRUD complètes (Create, Read, Update, Delete) pour les éléments de décision, les stratégies de sélection, les règles d’éligibilité et d’autres composants de prise de décision.

## Authentification {#authentication}

Avant d’utiliser les API Decisioning, vous devez configurer l’authentification pour accéder aux points d’entrée des API. Reportez-vous au [guide d’authentification Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"} pour obtenir des instructions détaillées.

## Opérations d’API disponibles {#available-operations}

Les API Decisioning fournissent des fonctionnalités de gestion complètes pour les composants Decisioning. Les catégories d’opérations suivantes sont disponibles :

* **Éléments de décision** : créez, lisez, mettez à jour, supprimez et répertoriez les éléments de décision qui représentent les offres ou le contenu que vous souhaitez diffuser à la clientèle.

  ➡️ [Découvrez comment gérer les éléments de décision.](decisions-items/create.md)

* **Collections d’éléments** : organisez les éléments de décision en collections pour une gestion et un ciblage plus faciles à l’aide de règles d’éligibilité.

  ➡️ [Découvrez comment gérer les collections d’éléments.](items-collections/create.md)

* **Stratégies de sélection** : définissez la manière dont les éléments de décision sont sélectionnés et classés lorsque plusieurs éléments sont qualifiés pour la diffusion.

  ➡️ [Découvrez comment gérer des stratégies de sélection.](selection-strategies/create.md)

* **Règles d’éligibilité** : définissez des conditions qui déterminent les profils éligibles pour recevoir des éléments de décision spécifiques.

  ➡️ [Découvrez comment gérer les règles d’éligibilité.](eligibility-rules/create.md)

* **Formules de classement** : créez une logique de classement personnalisée pour déterminer l’ordre dans lequel les éléments de décision sont présentés.

  ➡️ [Découvrez comment gérer les formules de classement.](ranking-formulas/create.md)

* **Emplacements** : définissez les emplacements ou les contextes où les éléments de décision peuvent être affichés dans vos expériences.

  ➡️ [Découvrez comment gérer les emplacements.](exd-placements/create.md)

## Étapes suivantes {#next-steps}

Maintenant que vous avez acquis les principes de base des API Decisioning, vous pouvez passer aux opérations spécifiques :

* [Créer des éléments de décision](decisions-items/create.md)
* [Répertorier les éléments de décision](decisions-items/decision-items-list.md)
* [Créer des stratégies de sélection](selection-strategies/create.md)
* [Créer des règles d’éligibilité](eligibility-rules/create.md)

Pour plus d’informations sur l’utilisation de la prise de décision dans vos campagnes et parcours, reportez-vous à la [documentation sur la prise de décision](../gs-experience-decisioning.md).

>[!NOTE]
>
>Si vous devez migrer des objets de gestion des décisions existants vers Decisioning, utilisez l’API dédiée [Migration Decisioning](../decisioning-migration-api.md). Cette API spécialisée fournit des fonctionnalités automatisées de résolution et de restauration des dépendances spécifiquement conçues pour la migration des entités de prise de décision entre les sandbox.
