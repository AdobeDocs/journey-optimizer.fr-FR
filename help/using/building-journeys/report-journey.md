---
solution: Journey Optimizer
product: journey optimizer
title: Publier le parcours
description: Découvrez comment créer des rapports sur votre parcours
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publication, parcours, dynamique, validité, vérifier
source-git-commit: 59a597a563074fa4daa74c64e97f6bb5c0f6834d
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 3%

---

# Rapport en direct dans le canevas de parcours {#report-journey}

>[!NOTE]
>
>Si vous ne pouvez pas voir les données dans votre rapport en direct parcours, vos droits d’accès doivent être étendus afin d’inclure l’autorisation **[!UICONTROL Afficher le rapport parcours]** . [En savoir plus](../administration/permissions.md)

Une fois votre parcours publié, la fonction **Création de rapports en direct** fournit des mesures des dernières 24 heures, directement dans la zone de travail du parcours.

Les événements affichés se sont produits au cours des dernières 24 heures, avec un intervalle minimum de deux minutes entre l’événement et son affichage, généralement dans les cinq minutes.

![](assets/journey_live_report.png)

Pour votre parcours de vie, vous avez accès aux éléments suivants :

* **[!UICONTROL Profils entrés]** : nombre total d’individus ayant participé à cette activité.
* **[!UICONTROL Profiles d’attente]** : nombre total d’individus ayant quitté le parcours de cette activité en raison d’un critère de sortie.
* **[!UICONTROL Profils en erreur]** : nombre total d&#39;individus ayant rencontré une erreur au cours de leur parcours.
* **[!UICONTROL Profils ignorés]** : nombre total d’individus qui ont été ignorés du parcours pour l’une des raisons suivantes :

   * Pour les activités **Qualification de l’audience**, un abandon peut se produire si le verbe attendu pour la qualification de l’audience ne correspond pas au parcours reçu (par exemple &quot;sortant&quot; au lieu de &quot;réalisé&quot;).
   * Pour les parcours **déclenchés par un événement**, un abandon peut se produire si l’individu a tenté de revenir trop tôt au parcours ou lorsque le retour n’a pas été autorisé.
   * Sur les **parcours récurrents**, une remise est comptabilisée à chaque périodicité si l’individu figure déjà dans le parcours et que la stratégie de retour n’est pas définie sur &quot;forcer la réentrée&quot;.
   * Sur les activités **Lecture d’audience**, une exception se produit si aucune identité n’est définie pour la personne exportée ou si l’espace de noms d’identité reçu ne correspond pas à celui attendu pour le parcours.

Pour chaque activité au sein de chaque parcours actif, vous avez accès aux éléments suivants :

* **[!UICONTROL Profils entrés]** : nombre total d’individus ayant participé à cette activité.
* **[!UICONTROL Profil de sortie]** : nombre total d’individus ayant quitté le parcours de cette activité, en raison d’un critère de sortie.
* **[!UICONTROL Erreur]** : nombre total d’individus ayant rencontré une erreur sur cette activité.
