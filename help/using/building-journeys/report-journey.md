---
solution: Journey Optimizer
product: journey optimizer
title: Publier le parcours
description: Découvrir comment obtenir des rapports sur votre parcours
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publication, parcours, dynamique, validité, vérifier
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 98%

---

# Rapport dynamique dans la zone de travail du parcours {#report-journey}

Une fois votre parcours publié et une fois le [mode Test à blanc](journey-dry-run.md) activé, la fonction **Rapports dynamiques** fournit les mesures des dernières 24 heures, directement dans la zone de travail du parcours.


>[!AVAILABILITY]
>
>Si vous ne pouvez pas voir les données dans le rapport dynamique de votre parcours, vos droits d’accès doivent être étendus afin d’inclure l’autorisation **[!UICONTROL Afficher le rapport des parcours]**. [En savoir plus](../administration/permissions.md)


Les événements affichés se sont produits au cours des dernières 24 heures, avec un intervalle minimal de deux minutes entre l’événement et son affichage, généralement dans les cinq minutes.

![Tableau de bord de rapports dynamiques de Parcours affichant les mesures de performances en temps réel](assets/journey_live_report.png)

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


>[!MORELIKETHIS]
>
>* [Commencer la création de rapports](../reports/gs-reports.md)
>* [Publier votre parcours](publish-journey.md)
>* [Test à blanc d’un parcours](journey-dry-run.md)
>* [Configurer et suivre les mesures de votre parcours](success-metrics.md)
>* [Rapports sur les parcours personnalisés](../reports/sharing-overview.md)