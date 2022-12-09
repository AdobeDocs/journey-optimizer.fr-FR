---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des fuseaux horaires
description: En savoir plus sur la gestion des fuseaux horaires
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# Gestion des fuseaux horaires {#timezone_management}

Vous pouvez définir un fuseau horaire dans la variable [properties](../building-journeys/journey-gs.md#change-properties) de votre parcours.

Pour accéder aux propriétés du parcours, cliquez sur l’icône en forme de crayon dans le coin supérieur droit de l’écran.

Ce fuseau horaire sera utilisé pour chaque activité du parcours contenant un élément temporel tel que :

* [Condition de temps](../building-journeys/condition-activity.md#time_condition)
* [Condition de date](../building-journeys/condition-activity.md#date_condition)
* [Attente personnalisée](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Vous pouvez sélectionner un fuseau horaire ou choisir d’utiliser celui défini dans le profil utilisateur.

>[!NOTE]
>
>Le fuseau horaire du profil fonctionne avec la variable **timeZone** existant dans le champ **Détails des préférences** groupe de champs.

## Définition d’un fuseau horaire fixe {#fixed-timezone}

Le fuseau horaire peut également être fixe. Effacez le fuseau horaire prédéfini et sélectionnez-en un dans la liste déroulante. Si vous utilisez un fuseau horaire fixe, il sera identique pour tous les individus qui participent au parcours.

Pour ce faire, dans le **[!UICONTROL Journey Properties]** sélectionnez un fuseau horaire.

![](assets/journey72.png)

## Utilisation de profils pour définir le fuseau horaire du parcours {#timezone-from-profiles}

Si l’événement d’entrée du parcours comporte un espace de noms, ce qui signifie que le parcours peut accéder au service de profil client en temps réel d’Adobe Experience Platform, vous pouvez utiliser le fuseau horaire défini au niveau du profil. Pour ce faire, reportez-vous à la section **Propriétés**, vérifier **Utilisation du fuseau horaire du profil dans les conditions d’attente**. Cette option n’est pas cochée par défaut.

Si un fuseau horaire a été défini pour un profil, il sera récupéré et utilisé par le parcours. Dans le cas contraire, le fuseau horaire utilisé sera celui défini dans le champ du fuseau horaire.

![](assets/journey73.png)

## Utilisation des fuseaux horaires dans les expressions {#timezone-in-expressions}

Les dates de début et de fin d’un parcours ne peuvent pas être liées à un fuseau horaire spécifique. Elles sont automatiquement associées au fuseau horaire de l’instance.
