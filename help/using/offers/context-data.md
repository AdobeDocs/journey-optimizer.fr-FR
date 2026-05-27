---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Commencer avec les données contextuelles
description: Découvrez comment utiliser les données contextuelles dans la gestion des décisions.
badge: label="Hérité" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/aVm2FFqkJWN-k1qngYsp94FgKIZWaLCMUneFd0rVNpA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 100%

---

# Commencer avec les données contextuelles {#context-data}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../experience-decisioning/gs-experience-decisioning.md)

Les données envoyées dans le cadre de la requête de prise de décision sont considérées comme des données contextuelles. Vous pouvez exploiter les données contextuelles dans le moteur de décision, par exemple pour concevoir une règle de décision qui nécessite que la météo actuelle soit supérieure à 20 degrés au moment de la demande de décision.

Les données contextuelles sont définies différemment entre les requêtes des API **Decisioning** et **Edge Decisioning**. Pour les deux types de requêtes, les données contextuelles peuvent être utilisées dans les règles d’éligibilité ou dans les formules de classement, mais seules les requêtes de l’API Edge Decisioning peuvent utiliser les données contextuelles pour personnaliser le contenu.

Avant de commencer, vérifiez les mécanismes de sécurisation et limitations suivants :

* En raison de la différence de méthode de transmission du contexte entre les appels Decisioning et Edge Decisioning, les règles d&#39;éligibilité basées sur le contexte et les formules de classement ne sont pas interchangeables entre les appels Decisioning et Edge Decisioning.
* Les demandes de test comportant le paramètre `dryrun` ne sont possibles qu’avec l’API Decisioning. L’API Edge Decisioning ne les prend pas en charge. Notez que la définition de ce paramètre sur `true` avec l’API Decisioning n’a aucune incidence sur les limitations et le nombre de propositions.

Pour plus d’informations sur l’utilisation des données contextuelles dans chaque API, reportez-vous aux sections suivantes :

* [Utiliser des données contextuelles dans les requêtes Edge Decisioning](context-data-edge.md)
* [Utiliser des données contextuelles dans les requêtes Decisioning](context-data-decisioning.md)
