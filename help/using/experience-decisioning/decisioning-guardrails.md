---
title: Mécanismes de sécurisation et limitations de la prise de décisions
description: En savoir plus sur les mécanismes de sécurisation et sur les limitations de la prise de décisions
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: e539d694e8fb91b6a8c7ba7ff5a2bb0905651f81
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 89%

---

# Mécanismes de sécurisation et limitations de la prise de décisions {#decisioning-guardrails}

Pour garantir une utilisation optimale de la prise de décision, gardez à l’esprit les mécanismes de sécurisation et les limitations suivants.

La liste complète des mécanismes de sécurisation et limitations de [!DNL Journey Optimizer] est disponible dans [cette section](../start/guardrails.md).

## Requêtes de décision

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Requête d’API d’expérience basée sur le code avec politique de décision utilisant la segmentation Edge | 1 500 |
| Requête d’API d’expérience basée sur du code avec politique de décision n’utilisant pas la segmentation Edge | 5 000 |

## Collections d’éléments

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Collections d’éléments | 10 000 |
| Nombre total d’éléments d’offre par collection d’éléments | 500 |

## Politique de décision

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre de stratégies de sélection et d’éléments manuels par politique de décision | 10 |
| Nombre maximal d’éléments d’offre renvoyés par politique de décision | 30 |

## Règles d’éligibilité

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre total de règles de décision et de formules de classement | 10 000 au total |
| Nombre maximal d’attributs de profil par règle | 25 |
| Nombre maximal d’attributs de données contextuelles par règle | 30 |
| Taille maximale de la règle pql | 15 000 (UTF-8) |
| Nombre maximal de niveaux d’imbrication | 30 |

## Formules de classement

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Taille maximale du PQL de formule de classement | 8 000 (UTF-8) |
| Nombre maximal d’attributs de profil | 25 |
| Nombre maximal d’attributs de données contextuelles | 30 |
| Nombre maximal de niveaux d’imbrication | 30 |

## Autres

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre d&#39;attributs personnalisés par schéma de catalogue d&#39;offres | 100 |
| Nombre total d’éléments d’offre | 10 000 |
| Nombre total d’emplacements | 1 000 |
| Modèle de classement AI | 5 |
| Règles de fréquence : nombre maximal de règles de limitation par offre | 10 |
