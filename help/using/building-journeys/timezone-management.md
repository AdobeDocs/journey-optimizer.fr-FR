---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des fuseaux horaires
description: En savoir plus sur la gestion des fuseaux horaires
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: fuseau horaire, propriétés, parcours, condition, heure, date, personnalisé
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: ht
source-wordcount: '291'
ht-degree: 100%

---

# Gestion des fuseaux horaires {#timezone_management}

Vous pouvez définir un fuseau horaire dans les [propriétés](../building-journeys/journey-gs.md#change-properties) de votre parcours.

Pour accéder aux propriétés du parcours, cliquez sur l&#39;icône en forme de crayon dans le coin supérieur droit de l&#39;écran.

Ce fuseau horaire sera utilisé pour chaque activité du parcours contenant un élément temporel tel que :

* [Condition de temps](../building-journeys/condition-activity.md#time_condition)
* [Condition de date](../building-journeys/condition-activity.md#date_condition)
* [Attente personnalisée](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Vous pouvez sélectionner un [fuseau horaire fixe](#fixed-timezone) ou choisir d’utiliser celui [défini dans le profil d’utilisateur ou d’utilisatrice](#timezone-from-profiles).

## Définition d&#39;un fuseau horaire fixe {#fixed-timezone}

Le fuseau horaire peut également être fixe. Effacez le fuseau horaire prédéfini et sélectionnez-en un dans la liste déroulante. Si vous utilisez un fuseau horaire fixe, il sera identique pour tous les individus qui participent au parcours.

Pour cela, dans le volet **[!UICONTROL Propriétés du parcours]**, sélectionnez un fuseau horaire.

![](assets/journey72.png)

## Utilisation de profils pour définir le fuseau horaire du parcours {#timezone-from-profiles}

Si l’événement d’entrée du parcours comporte un espace de noms, ce qui signifie que le parcours peut accéder au service de profil client en temps réel d’Adobe Experience Platform, vous pouvez utiliser le fuseau horaire défini au niveau du profil. Pour cela, dans **Propriétés**, cochez la case **Utiliser le fuseau horaire du profil dans les attentes et conditions**. Cette option n’est pas cochée par défaut.

Si un fuseau horaire a été défini pour un profil, il sera récupéré et utilisé par le parcours. Dans le cas contraire, le fuseau horaire utilisé sera celui défini dans le champ du fuseau horaire.

![](assets/journey73.png)

>[!NOTE]
>
>Le fuseau horaire de profil fonctionne avec le champ **timeZone** existant dans le groupe de champs **Détails des préférences**.

## Utilisation de fuseaux horaires dans les expressions {#timezone-in-expressions}

Les dates de début et de fin d&#39;un parcours ne peuvent pas être liées à un fuseau horaire spécifique. Elles sont automatiquement associées à celui de l&#39;instance.
