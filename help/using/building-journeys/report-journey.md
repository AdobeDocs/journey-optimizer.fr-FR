---
solution: Journey Optimizer
product: journey optimizer
title: Publier le parcours
description: Découvrir comment obtenir des rapports sur votre parcours
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: publication, parcours, dynamique, validité, vérifier
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/pclOxVDnQikU-2nLYMJ8mqEog9QL4WZBC7-NbvhuzIg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 566
ht-degree: 94%

---

# Rapport dynamique dans la zone de travail du parcours {#report-journey}

Une fois votre parcours publié et une fois le [mode Test à blanc](journey-dry-run.md) activé, la fonction **Rapports dynamiques** fournit les mesures des dernières 24 heures, directement dans la zone de travail du parcours.


>[!AVAILABILITY]
>
>Si vous ne pouvez pas voir les données dans le rapport dynamique de votre parcours, vos droits d’accès doivent être étendus afin d’inclure l’autorisation **[!UICONTROL Afficher le rapport des parcours]**. [En savoir plus](../administration/permissions.md)


Les événements affichés se sont produits au cours des dernières 24 heures, avec un intervalle minimal de deux minutes entre l’événement et son affichage, généralement dans les cinq minutes.

![Tableau de bord Rapports dynamiques du parcours affichant les mesures de performances en temps réel](assets/journey_live_report.png)

Pour vos parcours actifs ou en mode [Test à blanc](journey-dry-run.md), vous pouvez vérifier les éléments suivants :

* **[!UICONTROL Profils entrés]** : nombre total de personnes ayant rejoint le parcours.
* **[!UICONTROL Profils sortis]** : nombre total de personnes ayant quitté le parcours (y compris les erreurs).
* **[!UICONTROL Profils en erreur]** : nombre total de personnes ayant rencontré une erreur au cours de leur parcours.
* **[!UICONTROL Profils rejetés]** : nombre total de personnes qui ont été exclues du parcours pour l’une des raisons suivantes :

   * Pour les activités **Qualification de l’audience**, un rejet peut survenir si le verbe attendu pour la qualification de l’audience ne correspond pas au parcours reçu (par exemple « sorti » au lieu de « réalisé »).
   * Pour les parcours **déclenchés par un événement**, un rejet peut survenir si la personne a tenté de rejoindre trop tôt le parcours ou si elle n’y a pas été autorisée.
   * Sur les parcours **récurrents**, un rejet est comptabilisé à chaque périodicité si la personne figure déjà dans le parcours et que la politique de rentrée n’est pas définie sur « Forcer une rentrée ».
   * Sur les activités **Lecture d’audience**, un rejet survient si aucune identité n’est définie pour la personne exportée ou si l’espace de noms d’identité reçu ne correspond pas à celui attendu pour le parcours.

Pour chaque activité de chaque parcours actif ou en [mode Test à blanc](journey-dry-run.md), vous avez accès aux éléments suivants :

* **[!UICONTROL Entrées]** : nombre total de personnes qui ont atteint cette activité. Pour les activités **Action**, étant donné qu’elles ne sont pas exécutées en mode Test à blanc, cette mesure indique les profils qui passent par celles-ci.
* **[!UICONTROL Sorties (critères de sortie remplis)]** : nombre total de personnes ayant quitté le parcours de cette activité en raison d’un critère de sortie (y compris les erreurs).
* **[!UICONTROL Sorties (sorties forcées)]** : nombre total de personnes ayant quitté le parcours alors qu’il était en pause en raison d’une configuration opérée par la personne responsable du parcours. Cette mesure est toujours égale à zéro pour les parcours en mode Test à blanc.
* **[!UICONTROL Erreur]** : nombre total de personnes ayant rencontré une erreur pour cette activité.

## Résolution des problèmes liés aux données de rapport manquantes {#troubleshooting-missing-data}

Si les rapports de parcours ne contiennent pas les données attendues, tenez compte des points suivants :

* **Synchronisation des noms de Parcours** : vérifiez que le nom du parcours dans [!DNL Adobe Journey Optimizer] correspond au nom stocké dans le jeu de données de rapports. Une incohérence entre ces noms peut empêcher l’affichage correct des données de rapport.

* **Délai d’actualisation des données** : après la mise à jour d’un nom ou d’une configuration de parcours, patientez suffisamment longtemps pour actualiser les données. Les données de rapports apparaissent généralement en quelques minutes, mais peuvent prendre plus de temps dans certains cas.

* **Autorisations d’accès** : vérifiez que vous disposez des autorisations nécessaires pour afficher les rapports de parcours. Si vous ne voyez aucune donnée, vérifiez auprès de votre administrateur ou administratrice que l’autorisation **[!UICONTROL Afficher le rapport des parcours]** est activée. [En savoir plus sur les autorisations](../administration/permissions.md)

* **Statut de parcours** : les données de rapport ne sont disponibles que pour les parcours publiés ou les parcours s’exécutant en [mode test à blanc](journey-dry-run.md). Les brouillons de parcours ne génèrent pas de données de rapport.

Si les problèmes persistent après avoir vérifié ces éléments, contactez votre administrateur Adobe ou [l’assistance Adobe](../start/user-interface.md#support-ticket-guidelines) pour obtenir de l’aide.

>[!MORELIKETHIS]
>
>* [Commencer la création de rapports](../reports/gs-reports.md)
>* [Publier votre parcours](publish-journey.md)
>* [Test à blanc d’un parcours](journey-dry-run.md)
>* [Configurer et suivre les mesures de votre parcours](success-metrics.md)
>* [Rapports sur les parcours personnalisés](../reports/sharing-overview.md)
