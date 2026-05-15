---
solution: Journey Optimizer
product: journey optimizer
title: Publication du parcours
description: Découvrez comment créer des rapports sur votre parcours
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: publication, parcours, dynamique, validité, vérifier
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/pclOxVDnQikU-2nLYMJ8mqEog9QL4WZBC7-NbvhuzIg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 566
ht-degree: 0%

---

# Rapport dynamique dans la zone de travail du parcours {#report-journey}

Une fois votre parcours publié, une fois le [mode d’exécution d’essai](journey-dry-run.md) activé, **Rapports dynamiques** fournit les mesures des dernières 24 heures, directement dans la zone de travail du parcours.


>[!AVAILABILITY]
>
>Si vous ne pouvez pas voir de données dans votre rapport dynamique de parcours, vos droits d’accès doivent être étendus pour inclure l’autorisation **[!UICONTROL Afficher le rapport des parcours]**. [&#x200B; En savoir plus &#x200B;](../administration/permissions.md)


Les événements affichés se sont produits au cours des dernières 24 heures, avec un intervalle minimum de deux minutes entre l’événement et son affichage, généralement dans les cinq minutes.

![Tableau de bord de rapports dynamiques de Parcours affichant les mesures de performances en temps réel](assets/journey_live_report.png)

Pour vos parcours en mode d’exécution Live ou [Dry](journey-dry-run.md), vous pouvez vérifier les éléments suivants :

* **[!UICONTROL Profils entrés]** : nombre total de particuliers ayant rejoint le parcours.
* **[!UICONTROL Profils sortis]** : nombre total de personnes ayant quitté le parcours (erreurs comprises).
* **[!UICONTROL Profils en erreur]** : nombre total de personnes ayant rencontré une erreur lors de leur parcours.
* **[!UICONTROL Profils ignorés]** : nombre total de personnes qui ont été ignorées du parcours pour l’une des raisons suivantes :

   * Pour les activités **Qualification d’audience**, un abandon peut se produire si le verbe attendu pour la qualification d’audience ne correspond pas à ce que le parcours a reçu (par exemple, « sorti » au lieu de « réalisé »).
   * Pour les parcours **déclenchés par un événement** un rejet peut se produire si l’individu a tenté de rejoindre à nouveau le parcours trop tôt ou si la rentrée n’a pas été autorisée.
   * Sur les parcours **récurrents** une annulation est comptabilisée à chaque récurrence si la personne est déjà dans le parcours et que la politique de rentrée n’est pas définie sur « forcer la rentrée ».
   * Dans les activités **Lecture d’audience**, un abandon se produit si aucune identité n’est définie pour l’individu exporté ou si l’espace de noms d’identité reçu ne correspond pas à celui attendu pour le parcours.

Pour chaque activité de chaque parcours en mode d’exécution actif ou [essai](journey-dry-run.md), vous avez accès aux éléments suivants :

* **[!UICONTROL Entrées]** : nombre total de personnes ayant participé à cette activité. Pour les activités **Action**, étant donné qu’elles ne sont pas exécutées en mode d’exécution d’essai, cette mesure indique le passage des profils.
* **[!UICONTROL Sorti (satisfait aux critères de sortie)]** : nombre total de personnes ayant quitté le parcours de cette activité en raison d’un critère de sortie (y compris les erreurs).
* **[!UICONTROL Sorti (sortie forcée)]** : nombre total de personnes ayant quitté le parcours alors qu’il était en pause en raison d’une configuration de praticien de parcours. Cette mesure est toujours égale à zéro pour les parcours en mode d’exécution d’essai.
* **[!UICONTROL Erreur]** : nombre total de personnes ayant rencontré une erreur dans cette activité.

## Résolution des problèmes liés aux données de rapport manquantes {#troubleshooting-missing-data}

Si vous ne voyez pas les données attendues dans vos rapports de parcours, tenez compte des points suivants :

* **Synchronisation des noms de Parcours** : vérifiez que le nom du parcours dans [!DNL Adobe Journey Optimizer] correspond au nom stocké dans le jeu de données de rapports. Une incohérence entre ces noms peut empêcher l’affichage correct des données de rapport.

* **Délai d’actualisation des données** : après la mise à jour d’un nom ou d’une configuration de parcours, patientez suffisamment longtemps pour actualiser les données. Les données de création de rapports apparaissent généralement en quelques minutes, mais peuvent prendre plus de temps dans certains cas.

* **Autorisations d’accès** : vérifiez que vous disposez des autorisations nécessaires pour afficher les rapports de parcours. Si vous ne voyez aucune donnée, vérifiez auprès de votre administrateur que l’autorisation **[!UICONTROL Afficher le rapport des parcours]** est activée. [En savoir plus sur les autorisations](../administration/permissions.md)

* **Statut du Parcours** : les données de rapport ne sont disponibles que pour les parcours publiés ou les parcours s’exécutant en [mode d’exécution d’essai](journey-dry-run.md). Les brouillons de parcours ne génèrent pas de données de rapport.

Si les problèmes persistent après avoir vérifié ces éléments, contactez votre administrateur Adobe ou [l’assistance Adobe](../start/user-interface.md#support-ticket-guidelines) pour obtenir de l’aide.

>[!MORELIKETHIS]
>
>* [Prise en main du reporting](../reports/gs-reports.md)
>* [Publier votre parcours &#x200B;](publish-journey.md)
>* [Exécution d’essai de Parcours &#x200B;](journey-dry-run.md)
>* [Configurer et suivre les mesures de parcours &#x200B;](success-metrics.md)
>* [&#x200B; Rapports de parcours personnalisés &#x200B;](../reports/sharing-overview.md)
