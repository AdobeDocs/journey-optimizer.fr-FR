---
title: Mécanismes de sécurisation et limitations de la gestion des décisions
description: En savoir plus sur les mécanismes de sécurisation et les limitations de la gestion des décisions.
feature: Decisioning
role: User
level: Intermediate
source-git-commit: b6c31528784c0c8576e3200e7611a6b6cd43d7a7
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 15%

---


# Mécanismes de sécurisation et limitations de la gestion des décisions {#decision-management-guardrails}

Pour garantir une utilisation optimale de la gestion des décisions, gardez à l’esprit les mécanismes de sécurisation et limites suivantes.

La liste complète des mécanismes de sécurisation et limitations de [!DNL Journey Optimizer] est disponible dans [cette section](../start/guardrails.md).

## Demandes de décision

Le débit de diffusion correspond au nombre de réponses de décision qui peuvent être diffusées par le service de l&#39;application de gestion des décisions dans une période spécifiée.

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Requêtes d’API Decisioning par seconde | 500 |
| Requêtes de l’API Edge Decisioning par seconde avec la segmentation Edge | 1500 |
| Requêtes de l’API Edge Decisioning par seconde sans segmentation Edge | 5000 |
| Offres renvoyées par réponse | Jusqu’à 30 par portée de décision ou 100 au total |
| Nombre maximal de règles d’offre impliquées par requête | 100 |

## Décisions

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre total de décisions | 10K |
| Décisions en direct | 1K |
| Stages par décision | 30 |

## Collections

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Offres par collection | 500 |
| Collections | 10K |
| Collections par décision | 30 |

## Qualificateurs de collection

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Qualificateur de collection par offre ou collection | 20 |
| Nombre total de qualificateurs de collection | 1000 |

## Offres

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Total des offres | 10K |
| Nombre maximal d’offres **actives** par sandbox | 10K |
| Taille maximale des offres incluant les attributs (1 Ko), 30 attributs max. | 1 KO |
| Taille maximale de représentation de l&#39;offre (total pour tous les emplacements) | 1 KO |

## Règles d’éligibilité

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Total des règles de décision et des formules de classement | 10K combinés |
| Nombre maximal d’attributs de profil par règle | 25 |
| Nombre maximal d’attributs de données contextuelles par règle | 30 |
| Taille max de la règle PQL | 15K (UTF-8) |
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
| Emplacements | 1000 |
| Modèle de classement IA | 5 |
| Capping de la fréquence - Nombre maximal de règles de limitation par offre | 10 |
