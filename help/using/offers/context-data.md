---
product: experience platform
solution: Experience Platform
title: Commencer avec les données contextuelles
description: Découvrez comment utiliser les données contextuelles dans la gestion des décisions.
badge: label="Hérité" type="Informative"
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 99%

---

# Commencer avec les données contextuelles {#context-data}

Les données envoyées dans le cadre de la requête de prise de décision sont considérées comme des données contextuelles. Vous pouvez exploiter les données contextuelles dans le moteur de décision, par exemple pour concevoir une règle de décision qui nécessite que la météo actuelle soit supérieure à 20 degrés au moment de la demande de décision.

Les données contextuelles sont définies différemment entre les requêtes des API **Decisioning** et **Edge Decisioning**. Pour les deux types de requêtes, les données contextuelles peuvent être utilisées dans les règles d’éligibilité ou dans les formules de classement, mais seules les requêtes de l’API Edge Decisioning peuvent utiliser les données contextuelles pour personnaliser le contenu.

Avant de commencer, vérifiez les mécanismes de sécurisation et limitations suivants :

* En raison de la différence de méthode de transmission du contexte entre les appels Decisioning et Edge Decisioning, les règles d&#39;éligibilité basées sur le contexte et les formules de classement ne sont pas interchangeables entre les appels Decisioning et Edge Decisioning.
* Les demandes de test comportant le paramètre `dryrun` ne sont possibles qu’avec l’API Decisioning. L’API Edge Decisioning ne les prend pas en charge. Notez que la définition de ce paramètre sur `true` avec l’API Decisioning n’a aucune incidence sur les limitations et le nombre de propositions.

Pour plus d’informations sur l’utilisation des données contextuelles dans chaque API, reportez-vous aux sections suivantes :

* [Utiliser des données contextuelles dans les requêtes Edge Decisioning](context-data-edge.md)
* [Utiliser des données contextuelles dans les requêtes Decisioning](context-data-decisioning.md)
