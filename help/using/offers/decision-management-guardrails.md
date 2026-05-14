---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Mécanismes de sécurisation et limitations de la gestion des décisions
description: En savoir plus sur les mécanismes de sécurisation et sur les limitations de la gestion des décisions.
badge: label="Hérité" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: d2872bd3-42f8-4744-bb5b-41c49340098a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/teZQ3GKXJoj05ZD7bCCzKSzwLdUbgF8DXp8csDostOw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: a37e4ecd-c740-426a-addf-cb1b483c5c5aid: ad78185d-8f79-40ad-9bad-cbde74af74eeid: c132d929-fa62-4271-803e-b823be07b914id: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: e5ae22e3-a3b0-46ed-804f-9abf1bbe3e74
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 402
ht-degree: 83%

---

# Mécanismes de sécurisation et limitations de la gestion des décisions {#decision-management-guardrails}

>[!IMPORTANT]
>
>Cette page présente les mécanismes de sécurisation pour l’ancienne fonctionnalité **Gestion des décisions**. Si vous utilisez **Prise de décision**, la fonctionnalité de prise de décision actuelle d’[!DNL Adobe Journey Optimizer] disponible via une expérience basée sur le code et des canaux e-mail, reportez-vous à la section [ Mécanismes de sécurisation et limitations de prise de décision](../experience-decisioning/decisioning-guardrails.md) à la place.
>
>Vous ne savez pas quelle fonctionnalité vous utilisez ? [En savoir plus sur Decisioning](../experience-decisioning/gs-experience-decisioning.md).

Cette page s’applique aux utilisateurs qui travaillent toujours avec l’ancien système de gestion des décisions. Pour garantir une utilisation optimale, gardez à l’esprit les mécanismes de sécurisation et limitations suivantes.

La liste complète des mécanismes de sécurisation et limitations de [!DNL Journey Optimizer] est disponible dans [cette section](../start/guardrails.md).

## Requêtes de décision

Le débit de diffusion correspond au nombre de réponses de décision qui peuvent être diffusées par le service de l’application de gestion des décisions dans un délai spécifié.

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Requêtes de l’API Decisioning par seconde | 500 par organisation |
| Requêtes de l’API Edge Decisioning par seconde avec la segmentation Edge | 1 500 par organisation |
| Requêtes de l’API Edge Decisioning par seconde sans la segmentation Edge | 5 000 par organisation |
| Offres renvoyées par réponse | Jusqu’à 30 par portée de décision ou 100 au total |
| Nombre maximal de règles d’offre impliquées par requête | 100 |

## Décisions

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre total de décisions | 10 000 |
| Décisions actives | 1 000 |
| Emplacements par décision | 30 |

## Collections

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Offres par collection | 500 |
| Collections | 10 000 |
| Collections par décision | 30 |

## Qualificateurs de collection

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Qualificateur de collection par offre ou collection | 20 |
| Nombre total de qualificateurs de collection | 1 000 |

## Offres

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre total d’offres | 10 000 |
| Nombre maximal d’offres **actives** par sandbox | 10 000 |
| Taille maximale des offres incluant les attributs (1 Ko), 30 attributs maximum | 1 Ko |
| Taille maximale de rendu de l’offre (pour tous les emplacements) | 1 Ko |

## Règles d’éligibilité

| Mécanisme de sécurisation | Limite |
| ------- | ------- |
| Nombre total de règles de décision et de formules de classement | 10 000 au total |
| Nombre maximal d’attributs de profil par règle | 25 |
| Nombre maximal d’attributs de données contextuelles par règle | 30 |
| Taille maximale de la règle PQL | 15 000 (UTF-8) |
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
| Emplacements | 1 000 |
| Modèle de classement AI | 5 |
| Capping de la fréquence : nombre maximal de règles de limitation par offre | 10 |

## Configurations {#configurations}

Le nombre total de configurations prises en charge par la gestion des décisions ne peut pas dépasser 20 000.

Le nombre total de configurations correspond au nombre total de [règles de limitation](offer-library/add-constraints.md#capping) qui existent dans votre sandbox. Pour chaque règle de limitation appliquée à tous les [emplacements](offer-library/creating-placements.md), la règle doit être multipliée par tous les emplacements associés à l’offre spécifiée.
