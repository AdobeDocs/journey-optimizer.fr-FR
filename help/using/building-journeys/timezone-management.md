---
title: Gestion des fuseaux horaires
description: En savoir plus sur la gestion des fuseaux horaires
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Gestion des fuseaux horaires {#timezone_management}

![](../assets/do-not-localize/badge.png)

Vous pouvez définir un fuseau horaire dans les [propriétés](../building-journeys/journey-gs.md#change-properties) de votre parcours.

Pour accéder aux propriétés, cliquez sur l’icône en forme de crayon dans le coin supérieur droit de l’écran.

Ce fuseau horaire sera utilisé pour chaque activité du parcours contenant un élément temporel tel que :

* [Condition de temps](../building-journeys/condition-activity.md#time_condition)
* [Condition de date](../building-journeys/condition-activity.md#date_condition)
* [Attente personnalisée](../building-journeys/wait-activity.md#custom)
* [Attente à date fixe](../building-journeys/wait-activity.md#fixed_date)

Vous pouvez sélectionner un fuseau horaire ou choisir d’utiliser celui défini dans le profil utilisateur.

## Définition d’un fuseau horaire fixe {#fixed-timezone}

Le fuseau horaire peut également être fixe. Effacez le fuseau horaire prédéfini et sélectionnez-en un dans la liste déroulante. Si vous utilisez un fuseau horaire fixe, il sera identique pour tous les individus qui participent au parcours.

Pour cela, dans **[!UICONTROL Propriétés]**, sélectionnez un fuseau horaire.

![](../assets/journey73.png)

## Utilisation de profils pour définir le fuseau horaire du parcours {#timezone-from-profiles}

Si le événement d&#39;entrée du parcours a un espace de nommage, ce qui signifie que le parcours peut atteindre le service de Profil client en temps réel de Adobe Experience Platform, le fuseau horaire est prédéfini avec celui spécifié dans le profil de la personne qui s&#39;écoule dans le parcours.

Si un fuseau horaire est défini dans le profil Adobe Experience Platform, il peut être récupéré dans le parcours.

Si le profil de l’individu ne contient pas de fuseau horaire, celui qui sera récupéré sera celui défini dans le champ du fuseau horaire.

Pour cela, dans **[!UICONTROL Propriétés]**, cochez la case **[!UICONTROL Utiliser le fuseau horaire du profil dans les retardateurs et conditions]**.

![](../assets/journey72.png)

## Utilisation des fuseaux horaires dans les expressions {#timezone-in-expressions}

Les dates de début et de fin d’un parcours ne peuvent pas être liées à un fuseau horaire spécifique. Elles sont automatiquement associées à celui de l’instance.
