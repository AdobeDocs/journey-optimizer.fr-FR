---
title: Mécanismes de sécurisation et limitations de la prise de décisions
description: En savoir plus sur les mécanismes de sécurisation et sur les limitations de la prise de décisions
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/oTljriepwffzR-LIAc2kWjTQx9Oj0QMgJpbghkSEsmY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee394c77b226dd35a9c27f4a02e3b8d7a997ccbd
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 71%

---

# Mécanismes de sécurisation et limitations de la prise de décisions {#decisioning-guardrails}

>[!BEGINSHADEBOX]

**Sur cette page :** passez en revue les mécanismes de sécurisation et les limites qui s&#39;appliquent à Decisioning sur les demandes de décision, les éléments, les politiques, les règles d&#39;éligibilité et les formules de classement, afin que vous puissiez concevoir des configurations de prise de décision qui respectent les seuils pris en charge.

>[!ENDSHADEBOX]

Pour garantir une utilisation optimale de la prise de décision, gardez à l’esprit les mécanismes de sécurisation et les limitations suivants.

La liste complète des mécanismes de sécurisation et limitations de [!DNL Journey Optimizer] est disponible dans [cette section](../start/guardrails.md).

## Requêtes de décision {#decision-requests}

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Requête API d’expérience basée sur du code avec politique de décision utilisant la segmentation Edge | 1 500 |
| Requête API d’expérience basée sur du code avec politique de décision n’utilisant pas la segmentation Edge | 5 000 |
| Nombre maximal d’URI de surface par requête de prise de décision Edge | 30 |

## Éléments de décision {#decision-items}

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Total des éléments de décision | 10 000 |
| Taille maximale des éléments, y compris les attributs (1 Ko), 30 attributs max. | 1 Ko |
| Règles de fréquence - Nombre maximal de règles de limitation par élément de décision | 10 |
| Nombre maximal de fragments de contenu AEM par élément de décision | 5 |

## Collections d’éléments {#item-collections}

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Collections d’éléments | 10 000 |
| Total des éléments de décision par collection | 500 |

## Politique de décision {#decision-policy}

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre de stratégies de sélection et d’éléments manuels par politique de décision | 10 |
| Nombre maximal d’éléments de décision renvoyés par politique de décision | 30 |
| Stratégies de décision max. par e-mail | 10 |

## Règles d’éligibilité {#eligibility-rules}

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre total de règles de décision et de formules de classement | 10 000 au total |
| Nombre maximal d’attributs de profil par règle | 25 |
| Nombre maximal d’attributs de données contextuelles par règle | 30 |
| Taille maximale de la règle pql | 15 000 (UTF-8) |
| Nombre maximal de niveaux d’imbrication | 30 |

## Formules de classement {#ranking-formulas}

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Taille maximale du PQL de formule de classement | 8 000 (UTF-8) |
| Nombre maximal d’attributs de profil | 25 |
| Nombre maximal d’attributs de données contextuelles | 30 |
| Nombre maximal de niveaux d’imbrication | 30 |

## Autres {#others}

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre d’attributs personnalisés par schéma de catalogue d’articles | 100 |
| Nombre total d’emplacements | 1 000 |
| Modèle de classement AI | 5 |

## Configurations {#configurations}

Le nombre total de configurations acceptées par prise de décision ne peut pas dépasser 20 000.

Le nombre total de configurations correspond au nombre total de [règles de limitation](items.md#capping) qui existent dans votre sandbox.
