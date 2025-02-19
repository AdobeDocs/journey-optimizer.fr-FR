---
product: experience platform
solution: Experience Platform
title: Prise en main des données contextuelles
description: Découvrez comment exploiter les données contextuelles dans la gestion des décisions.
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Prise en main des données contextuelles {#context-data}

Les données envoyées dans le cadre de la requête de prise de décision sont considérées comme des données contextuelles. Vous pouvez exploiter les données contextuelles dans le moteur de décision, par exemple pour concevoir une règle de décision qui nécessite que la météo actuelle soit de ≥80 degrés au moment où la demande de décision est prise.

Les données contextuelles sont définies différemment entre les requêtes API **Decisioning** et **Edge Decisioning**. Pour les deux types de requêtes, les données contextuelles peuvent être utilisées dans les règles d’éligibilité ou dans les formules de classement, mais seules les requêtes de l’API Edge Decisioning peuvent utiliser les données contextuelles pour personnaliser le contenu.

Avant de commencer, vérifiez les mécanismes de sécurisation et limitations suivantes :

* En raison de la différence de méthode de transmission du contexte entre les appels Decisioning et Edge Decisioning, les règles d&#39;éligibilité basées sur le contexte et les formules de classement ne sont pas interchangeables entre les appels Decisioning et Edge Decisioning.
* Le test avec le paramètre `dryrun` est possible uniquement avec l’API Decisioning. Elle n’est pas disponible avec l’API Edge Decisioning. Notez que la définition de ce paramètre sur `true` avec l’API Decisioning n’a aucune incidence sur les limites et le nombre de propositions.

Pour plus d’informations sur l’utilisation des données contextuelles dans chaque API, reportez-vous aux sections suivantes :

* [Utilisation de données contextuelles dans les requêtes Edge Decisioning](context-data-edge.md)
* [Utilisation de données contextuelles dans les requêtes de prise de décision](context-data-decisioning.md)

