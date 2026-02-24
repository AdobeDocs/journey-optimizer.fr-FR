---
solution: Journey Optimizer
product: Journey Optimizer
title: Définir les règles de limitation des messages et des parcours
description: Définir les règles de limitation des messages et des parcours
redpen-status: CREATED_||_2025-08-11_20-28-34
exl-id: 630e252a-aab2-4a27-ad46-d4dbfbc3f3a4
source-git-commit: 9e23162373564e7866af115ee2cd706527336e4a
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 38%

---

# Définir les règles de limitation des messages et des parcours{#section-overview}

Les règles de limitation font partie de la [gestion des conflits et hiérarchisation](../using/conflict-prioritization/gs-conflict-prioritization.md). Elles permettent de s’assurer que les clients reçoivent le montant de communication approprié sans se sentir dépassés. Avant d’appliquer des règles, utilisez l’outil [&#x200B; de détection des conflits &#x200B;](../using/conflict-prioritization/conflicts.md) pour identifier les parcours et les campagnes qui se chevauchent. Lorsque plusieurs communications sont qualifiées pour le même profil, [scores de priorité](../using/conflict-prioritization/priority-scores.md) déterminent quel message est diffusé en premier.

Vous pouvez définir des limites sur la fréquence d’envoi des messages (capping de la fréquence), le nombre de parcours qu’un profil peut entrer (limitation des parcours) et le moment de blocage des messages (heures creuses). Les règles sont regroupées en **ensembles de règles** et appliquées aux campagnes ou aux parcours. Pour le contrôle programmatique à partir de systèmes externes, reportez-vous à la section [API de limitation](../using/configuration/capping.md).

## Définir les règles de limitation des messages et des parcours

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=fr)

Utiliser des jeux de règles

Découvrez comment créer, gérer et activer des jeux de règles pour contrôler la fréquence des messages et les règles relatives aux parcours dans Adobe Journey Optimizer.

[Explorer les jeux de règles](../using/conflict-prioritization/rule-sets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=fr)

Limitation et arbitrage des parcours

Découvrez comment définir des limitations d’entrée de parcours et de simultanéité, hiérarchiser les parcours et surveiller les exclusions afin d’éviter une surcharge de communication.

[Découvrir la limitation des parcours](../using/conflict-prioritization/journey-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=fr)

Capping de la fréquence par canal

Découvrez comment créer et appliquer des règles de capping de la fréquence spécifiques aux canaux pour optimiser la diffusion des messages et éviter la surcommunication.

[Définir le capping de la fréquence](../using/conflict-prioritization/channel-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=fr)

Définir des heures calmes

Définissez des exclusions temporelles pour les e-mails, SMS, notifications push et WhatsApp afin qu’aucun message ne soit envoyé pendant des périodes spécifiques, en respectant les préférences des clients et la conformité.

[Définir des heures creuses](../using/conflict-prioritization/quiet-hours.md)
:::

::::

## Ressources supplémentaires

- **[Prise en main de la gestion des conflits et de la hiérarchisation](../using/conflict-prioritization/gs-conflict-prioritization.md)** - Présentation de la détection des conflits, des scores de priorité et des ensembles de règles.
- **[Identifier les conflits potentiels](../using/conflict-prioritization/conflicts.md)** - Détectez les parcours et campagnes qui se chevauchent avant d’appliquer les règles de limitation.
- **[Attribuer des scores de priorité](../using/conflict-prioritization/priority-scores.md)** - Contrôlez quel parcours ou campagne est prioritaire lorsqu’un profil est qualifié pour plusieurs communications.
