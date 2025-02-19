---
title: Mécanismes de sécurisation et limitations des décisions
description: En savoir plus sur les mécanismes de sécurisation et limitations de Decisioning.
feature: Decisioning
role: User
level: Intermediate
source-git-commit: b6c31528784c0c8576e3200e7611a6b6cd43d7a7
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 15%

---


# Mécanismes de sécurisation et limitations des décisions {#decisioning-guardrails}

Pour garantir une utilisation optimale de Decisioning, gardez à l’esprit les mécanismes de sécurisation et limites suivantes.

La liste complète des mécanismes de sécurisation et limitations de [!DNL Journey Optimizer] est disponible dans [cette section](../start/guardrails.md).

## Demandes de décision

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Requête d’API d’expérience basée sur du code avec politique de décision utilisant la segmentation Edge | 1500 |
| Requête d’API d’expérience basée sur du code avec politique de décision n’utilisant pas la segmentation Edge | 5000 |

## Collections d&#39;éléments

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Collections d’éléments | 10K |
| Nombre total d’éléments d’offre par collection d’éléments | 500 |

## Politique de décision

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre de stratégies de sélection et d&#39;éléments manuels par politique de décision | 10 |
| Nombre maximal d’éléments d’offre renvoyés par politique de décision | 30 |

## Règles d’éligibilité

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Total des règles de décision et des formules de classement | 10K combinés |
| Nombre maximal d’attributs de profil par règle | 25 |
| Nombre maximal d’attributs de données contextuelles par règle | 30 |
| Taille max de la règle pql | 15K (UTF-8) |
| Nbre max. de niveaux d’imbrication | 30 |

## Formules de classement

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Taille max. du PQL de formule de classement | 8K (UTF-8) |
| Nombre maximal d’attributs de profil | 25 |
| Nombre maximal d’attributs de données contextuelles | 30 |
| Nbre max. de niveaux d’imbrication | 30 |

## Autres

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre d&#39;attributs personnalisés par schéma de catalogue d&#39;offres | 100 |
| Total des éléments d’offre | 10K |
| Total des placements | 1K |
| Modèle de classement AI | 5 |
| Règles de fréquence - Nombre maximal de règles de limitation par offre | 10 |
