---
solution: Journey Optimizer
product: journey optimizer
title: Rapport de campagne
description: Découvrez comment utiliser les données d’activité dynamique du rapport de campagne.
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 58034ec4-62dc-406c-99c4-d6b7aa107140
source-git-commit: 7983480646eb49f32716cda19001ef7b9a95ba82
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 95%

---

# Rapport de campagne d’activité dynamique {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

Vous pouvez accéder au rapport de campagne d’activité dynamique en cliquant sur le bouton **[!UICONTROL Rapports]** de votre campagne, puis en sélectionnant **[!UICONTROL Afficher le rapport de toutes les périodes]**. [En savoir plus](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Statistiques d’envoi {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

Le tableau **[!UICONTROL Statistiques d’envoi]** fournit une vue d’ensemble détaillée des mesures clés liées à vos campagnes d’activité dynamique. Il affiche des informations essentielles telles que la taille de l’audience ciblée et le nombre de notifications push correctement diffusées, ce qui vous permet d’évaluer la portée et les performances globales de vos notifications push dynamiques.

+++ En savoir plus sur les mesures de statistiques d’envoi

* **[!UICONTROL Ciblés]** : nombre de profils qui remplissent les critères de l’audience avant l’application des exclusions, des suppressions ou des suppressions de consentement.

* **[!UICONTROL Envois]** : nombre total de tentatives d’envoi de notifications push aux profils ciblés.

* **[!UICONTROL Diffusés]** : nombre de notifications push diffusées avec succès aux appareils, par rapport au nombre total de tentatives d’envoi.

* **[!UICONTROL Erreurs d’envoi]** : nombre total de notifications push qui n’ont pas pu être envoyées en raison d’erreurs (par exemple, jetons non valides ou problèmes de connectivité).

* **[!UICONTROL Exclusions d’envoi]** : nombre de profils exclus de l’envoi par Adobe Journey Optimizer (par exemple, en raison du statut d’opt-out ou des règles d’éligibilité).

+++

## Cycle de vie d’une activité dynamique {#lifecycle}

![](assets/activity-lifecycle.png)

Le tableau **[!UICONTROL Cycle de vie des activités dynamiques]** offre une vue complète de la progression de vos activités dynamiques au fil du temps. Il offre une visibilité sur les événements clés, tels que le moment où les activités sont démarrées, mises à jour ou terminées, ce qui vous permet de mieux comprendre l’interaction clientèle et le cycle de vie global de vos campagnes d’activités dynamiques.

+++ En savoir plus sur les mesures de cycle de vie des activités dynamiques

* **[!UICONTROL Démarrages à distance]** : nombre d’activités dynamiques lancées à distance, généralement déclenchées par le serveur ou le système principal.

* **[!UICONTROL Démarrages locaux]** : nombre d’activités dynamiques démarrées localement sur l’appareil d’une personne, souvent suite à une interaction ou à des déclencheurs côté clientèle.

**[!UICONTROL Mises à jour]** : nombre total de mises à jour d’activité dynamique envoyées aux appareils. Les mises à jour peuvent inclure des changements de statut, du nouveau contenu ou des notifications de progression.

**[!UICONTROL Se termine]** : nombre d’activités dynamiques qui se sont terminées, soit automatiquement à la fin de l’opération, soit manuellement par le biais d’un déclencheur ou d’une temporisation définis.

**[!UICONTROL Totaux]** : total général de tous les événements du cycle de vie d’une activité dynamique, y compris les démarrages, les mises à jour et les fins, fournissant une mesure complète du volume d’activité dynamique.

+++

## Raisons des erreurs {#error-reasons}

![](assets/error-reasons-activity.png)

Le tableau **[!UICONTROL Raisons des erreurs]** offre une visibilité des erreurs spécifiques survenues pendant le processus d’envoi de vos SMS, fournissant une analyse minutieuse de tout problème rencontré.

## Causes d’exclusion {#excluded-reasons}

![](assets/excluded-activity.png)

Le tableau **[!UICONTROL Causes d’exclusion]** décrit visuellement les différents facteurs qui ont conduit à l’exclusion des profils d’utilisateurs et d’utilisatrices de l’audience ciblée, ce qui les empêche de recevoir votre activité dynamique.
