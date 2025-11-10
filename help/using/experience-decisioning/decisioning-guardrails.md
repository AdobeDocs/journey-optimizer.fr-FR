---
title: Mécanismes de sécurisation et limitations de la prise de décisions
description: En savoir plus sur les mécanismes de sécurisation et sur les limitations de la prise de décisions
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 19%

---

# Mécanismes de sécurisation et limitations de la prise de décisions {#decisioning-guardrails}

Pour garantir une utilisation optimale de la prise de décision, gardez à l’esprit les mécanismes de sécurisation et les limitations suivants.

La liste complète des mécanismes de sécurisation et limitations de [!DNL Journey Optimizer] est disponible dans [cette section](../start/guardrails.md).

## Requêtes de décision {#decision-requests}

|| Mécanisme De Sécurisation | Limite |
|| ------- | ------- |
|| Requête d’API d’expérience basée sur le code avec politique de décision utilisant la segmentation Edge | 1500 |
|| Requête d’API d’expérience basée sur du code avec politique de décision n’utilisant pas la segmentation Edge | 5000 |
|| Nombre maximal d’URI de surface par requête de prise de décision Edge | 30 |

## Collections d’éléments {#item-collections}

|| Mécanisme De Sécurisation | Limite |
|| ------- | ------- |
|| Collections d’éléments | 10K |
|| Nombre total d’éléments d’offre par collection d’éléments | 50 |

## Politique de décision {#decision-policy}

|| Mécanisme De Sécurisation | Limite |
|| ------- | ------- |
|| Nombre de stratégies de sélection et d&#39;éléments manuels par politique de décision | 10 |
|| Nombre maximal d’éléments d’offre renvoyés par politique de décision | 30 |

## Règles d’éligibilité {#eligibility-rules}

|| Mécanisme De Sécurisation | Limite |
|| ------- | ------- |
|| Total des règles de décision et des formules de classement | 10K combinés |
|| Nombre maximal d’attributs de profil par règle | 25 |
|| Nombre maximal d’attributs de données contextuelles par règle | 30 |
|| Taille max de la règle pql | 15K (UTF-8) |
|| Nbre max. de niveaux d’imbrication | 30 |

## Formules de classement {#ranking-formulas}

|| Mécanisme De Sécurisation | Limite |
|| ------- | ------- |
|| Taille max. du PQL de formule de classement | 8K (UTF-8) |
|| Nombre maximal d’attributs de profil |25 |
|| Nombre maximal d’attributs de données contextuelles | 30 |
|| Nbre max. de niveaux d’imbrication | 30 |

## Autres {#others}

|| Mécanisme De Sécurisation | Limite |
|| ------- | ------- |
|| Nombre d&#39;attributs personnalisés par schéma de catalogue d&#39;offres | 100 |
|| Total des éléments d’offre | 10K |
|| Total des placements | 1K |
|| Modèle de classement AI | 5 |
|| Règles de fréquence - Nombre maximal de règles de limitation par offre | 10 |

## Configurations  {#configurations}

Le nombre total de configurations prises en charge par Decisioning ne peut pas dépasser 20 000.

Le nombre total de configurations correspond au nombre total de [règles de limitation](items.md#capping) qui existent dans votre sandbox.
