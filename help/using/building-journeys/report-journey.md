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
source-git-commit: 59a597a563074fa4daa74c64e97f6bb5c0f6834d
workflow-type: ht
source-wordcount: '317'
ht-degree: 100%

---

# Rapport dynamique dans la zone de travail du parcours {#report-journey}

>[!NOTE]
>
>Si vous ne pouvez pas voir les données dans le rapport dynamique de votre parcours, vos droits d’accès doivent être étendus afin d’inclure l’autorisation **[!UICONTROL Afficher le rapport des parcours]**. [En savoir plus](../administration/permissions.md)

Une fois votre parcours publié, la fonction **Rapports dynamiques** fournit des mesures des dernières 24 heures, directement dans la zone de travail du parcours.

Les événements affichés se sont produits au cours des dernières 24 heures, avec un intervalle minimal de deux minutes entre l’événement et son affichage, généralement dans les cinq minutes.

![](assets/journey_live_report.png)

Pour votre parcours dynamique, vous avez accès aux éléments suivants :

* **[!UICONTROL Profils entrés]** : nombre total de personnes ayant participé à cette activité.
* **[!UICONTROL Profils sortis]** : nombre total de personnes ayant quitté le parcours de cette activité en raison d’un critère de sortie.
* **[!UICONTROL Profils en erreur]** : nombre total de personnes ayant rencontré une erreur au cours de leur parcours.
* **[!UICONTROL Profils rejetés]** : nombre total de personnes qui ont été exclues du parcours pour l’une des raisons suivantes :

   * Pour les activités **Qualification de l’audience**, un rejet peut survenir si le verbe attendu pour la qualification de l’audience ne correspond pas au parcours reçu (par exemple « sorti » au lieu de « réalisé »).
   * Pour les parcours **déclenchés par un événement**, un rejet peut survenir si la personne a tenté de rejoindre trop tôt le parcours ou si elle n’y a pas été autorisée.
   * Sur les parcours **récurrents**, un rejet est comptabilisé à chaque périodicité si la personne figure déjà dans le parcours et que la politique de rentrée n’est pas définie sur « Forcer une rentrée ».
   * Sur les activités **Lecture d’audience**, un rejet survient si aucune identité n’est définie pour la personne exportée ou si l’espace de noms d’identité reçu ne correspond pas à celui attendu pour le parcours.

Pour chaque activité au sein de chaque parcours dynamique, vous avez accès aux éléments suivants :

* **[!UICONTROL Profils entrés]** : nombre total de personnes ayant participé à cette activité.
* **[!UICONTROL Profils sortis]** : nombre total de personnes ayant quitté le parcours de cette activité en raison d’un critère de sortie.
* **[!UICONTROL Erreur]** : nombre total de personnes ayant rencontré une erreur pour cette activité.
