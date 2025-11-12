---
solution: Journey Optimizer
product: journey optimizer
title: Rapport de campagne
description: Découvrez comment utiliser les données d’activité dynamiques du rapport de campagne
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 4%

---

# Rapport de campagne d’activité dynamique {#campaign-global-report-cja-activity}

>[!BEGINSHADEBOX]

Pour accéder au rapport de campagne d’activités dynamiques, cliquez sur le bouton **[!UICONTROL Rapports]** de votre campagne, puis sélectionnez **[!UICONTROL Afficher le rapport à toute heure]**. [En savoir plus](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## Statistiques d’envoi {#sending-statistics-mobile}

![](assets/sending-statistics-mobile-live.png)

Le tableau **[!UICONTROL Statistiques d’envoi]** fournit un aperçu détaillé des mesures clés liées à vos campagnes d’activité dynamiques . Il affiche des informations essentielles telles que la taille de l’audience ciblée et le nombre de notifications push correctement diffusées, ce qui vous permet d’évaluer la portée et les performances globales de vos notifications push actives.

+++ En savoir plus sur les mesures de statistiques d’envoi

* **[!UICONTROL Ciblés]** : nombre total de profils ciblés pendant l&#39;activité Live.

* **[!UICONTROL Envois]** : nombre total de tentatives d&#39;envoi de notifications push aux profils ciblés.

* **[!UICONTROL Diffusés]** : nombre de notifications push diffusées avec succès aux appareils, par rapport au nombre total de tentatives d’envoi.

* **[!UICONTROL Erreurs d’envoi]** : nombre total de notifications push qui n’ont pas pu être envoyées en raison d’erreurs (par exemple, jetons non valides ou problèmes de connectivité).

* **[!UICONTROL Exclusions d’envoi]** : nombre de profils exclus de l’envoi par Adobe Journey Optimizer (par exemple, en raison du statut d’opt-out ou des règles d’éligibilité).

+++

## Cycle de vie d’une activité en direct {#lifecycle}

![](assets/activity-lifecycle.png)

Le tableau **[!UICONTROL Cycle de vie des activités dynamiques]** offre une vue complète de la progression de vos activités dynamiques au fil du temps. Il offre une visibilité sur les événements clés, tels que le moment où les activités sont démarrées, mises à jour ou terminées, ce qui vous permet de mieux comprendre l’interaction client et le cycle de vie global de vos campagnes d’activités dynamiques.

+++ En savoir plus sur les mesures de cycle de vie des activités dynamiques

* **[!UICONTROL Démarrages à distance]** : nombre d’activités dynamiques lancées à distance, généralement déclenchées par le serveur ou le système principal.

* **[!UICONTROL démarrages locaux]** : nombre d’activités en direct démarrées localement sur l’appareil d’un utilisateur, souvent suite à une interaction utilisateur ou à des déclencheurs côté client.

**[!UICONTROL Mises à jour]** : nombre total de mises à jour d’activité active envoyées aux appareils. Les mises à jour peuvent inclure des changements de statut, du nouveau contenu ou des notifications de progression.

**[!UICONTROL Se termine]** : nombre d’activités dynamiques qui se sont terminées, soit automatiquement à la fin de l’opération, soit manuellement par le biais d’un déclencheur ou d’une temporisation définis.

**[!UICONTROL Nombre de totaux]** : total général de tous les événements du cycle de vie d’une activité active, y compris les démarrages, les mises à jour et les fins, fournissant une mesure complète du volume d’activité active.

+++

## Raisons des erreurs {#error-reasons}

![](assets/error-reasons-activity.png)

Le tableau **[!UICONTROL Causes des erreurs]** vous permet d’identifier les erreurs spécifiques qui se sont produites au cours du processus d’envoi de vos activités dynamiques, ce qui facilite une analyse approfondie des problèmes rencontrés.

## Causes d’exclusion {#excluded-reasons}

![](assets/excluded-activity.png)

Le tableau **[!UICONTROL Causes d’exclusion]** décrit visuellement les différents facteurs qui ont conduit à l’exclusion des profils utilisateur de l’audience ciblée, ce qui les empêche de recevoir votre activité en direct.
