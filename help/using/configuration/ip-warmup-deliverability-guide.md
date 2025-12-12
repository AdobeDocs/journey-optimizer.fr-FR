---
solution: Journey Optimizer
product: journey optimizer
title: Guide de délivrabilité du préchauffage d’adresses IP
description: Découvrez les principes fondamentaux de la délivrabilité et les bonnes pratiques pour le préchauffage des adresses IP
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, délivrabilité, réputation, FAI, engagement
source-git-commit: 07896931a7c06e1b712f3b65e1dcf939b521ba83
workflow-type: tm+mt
source-wordcount: '1088'
ht-degree: 6%

---

# Guide de délivrabilité du préchauffage d’adresses IP {#ip-warmup-deliverability-guide}

Lors du lancement de campagnes par e-mail avec de nouvelles adresses IP ou de nouveaux domaines dans Adobe Journey Optimizer, il est essentiel de comprendre les principes de base de la délivrabilité pour établir une réputation solide envers les expéditeurs. Ce guide couvre les concepts clés, les étapes de préparation et les bonnes pratiques pour vous aider à passer de la réputation zéro à un emplacement de boîte de réception réussi.

➡️ [Regardez cette vidéo pour en savoir plus sur les principes de base de la délivrabilité du réchauffement des adresses IP](#video)

>[!NOTE]
>
>Pour obtenir des instructions détaillées sur l’implémentation de plans de préchauffage d’adresses IP dans Adobe Journey Optimizer, reportez-vous à la section [Prise en main des plans de préchauffage d’adresses IP](ip-warmup-gs.md).

## Importance de la réputation des adresses IP et des domaines {#reputation-matters}

Les fournisseurs de messagerie (Gmail, Yahoo, Microsoft, Apple Mail, etc.) évaluent chaque expéditeur en fonction de quatre piliers principaux :

* **Plaintes** : les destinataires ont-ils marqué vos messages comme spam ?
* **Engagement** : les destinataires ouvrent-ils, cliquent-ils ou répondent-ils à vos e-mails ?
* **Infrastructure** : votre infrastructure d&#39;envoi est-elle authentifiée, stable et fiable ?
* **Contenu** : le contenu de votre message semble-t-il légitime et utile ?

Le préchauffage des adresses IP répond principalement aux trois premiers piliers en démontrant progressivement aux fournisseurs de boîtes aux lettres que votre nouvelle infrastructure est légitime et souhaitée avant que vous ne passiez à un volume d&#39;envoi complet.

## Liste de vérification avant vol {#pre-flight-checklist}

Avant de commencer à préchauffer vos adresses IP, assurez-vous que tous les éléments fondamentaux sont en place. Le tableau ci-dessous décrit les tâches essentielles à effectuer avant de démarrer votre plan de préchauffage d’adresses IP.

| Tâche | Importance de ces éléments | Comment accomplir |
|------|----------------|-------------------|
| Réserver des adresses IP fixes et déléguer des sous-domaines dans AJO | Toute réputation future s’attache à ces éléments d’infrastructure | Accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres d’e-mail]** > **[!UICONTROL Sous-domaines]**. [En savoir plus](delegate-subdomain.md) |
| Configuration de SPF et DKIM | Confirme que votre serveur d’envoi est légitime et autorisé | Géré automatiquement par Adobe après la création de la délégation de sous-domaine et de la configuration de canal. [En savoir plus](delegate-subdomain.md) |
| Configurer l’enregistrement DMARC | Active le rapport d’authentification des e-mails et les futures politiques d’application | Géré automatiquement par Adobe après la création de la délégation de sous-domaine et de la configuration de canal. [En savoir plus](dmarc-record.md) |
| Configuration de la surveillance des listes de contrôle | Détecte les problèmes d’emplacement de la boîte de réception au début de votre processus de préchauffage | Ajoutez des adresses de contrôle lors de la création de votre configuration de canal. [En savoir plus](seed-lists.md) |
| Créer une audience à fort engagement de phase 1 | Améliore les mesures d’engagement précoce avec vos destinataires les plus actifs | Créez une audience de moins de 5 000 contacts qui ont ouvert ou cliqué au cours des 30 derniers jours |

>[!CAUTION]
>
>Les problèmes d’authentification (SPF, DKIM, DMARC) ne peuvent pas être résolus par l’augmentation progressive du volume. Assurez-vous qu’ils sont correctement configurés avant de commencer l’envoi.

## Exemple de calendrier de préchauffage de quatre semaines {#warmup-calendar}

Cet exemple de calendrier fournit une rampe de volume progressive en fonction du pourcentage de votre volume quotidien ultime (UDV). Ajustez ces chiffres en fonction de vos besoins d’envoi spécifiques et collaborez avec votre consultant en délivrabilité pour créer un plan personnalisé.

| Jours | % des UDV | Audience cible | Recommandations de contenu |
|------|----------|-----------------|------------------------|
| 1-3 | 0,5 % | Vos destinataires les plus engagés | Utilisez un format court en texte brut avec un call-to-action clair au-dessus du pli. |
| 4-7 | 1 % | Utilisateurs engagés et acheteurs récents | Ajoutez une image principale légère, limitez les liens à 3 ou moins. |
| 8-14 | 5 % | Liste d&#39;abonnés actifs plus large | Présentation de votre modèle d’e-mail standard, mais évitez le contenu promotionnel volumineux |
| 15-21 | 25 % | Abonnés actifs et légèrement inactifs | Utiliser du contenu marketing normal tout en surveillant de près les taux de plaintes |
| 22-28 | 50-100 % | Liste complète (concernant les listes de suppression) | Transition vers votre cadence d’envoi d’état stable |

>[!NOTE]
>
>Adobe Journey Optimizer fournit une fonctionnalité dédiée [plan de préchauffage d’adresses IP](ip-warmup-gs.md) qui automatise la gestion des volumes et simplifie le processus de préchauffage sans nécessiter de configurations de parcours complexes.

## Utilisation de la fonctionnalité de plans de préchauffage d’adresses IP d’AJO {#ajo-warmup-feature}

Adobe Journey Optimizer comprend une fonctionnalité de plans de préchauffage d’adresses IP rationalisée qui élimine la nécessité d’une limitation manuelle du volume par le biais de configurations de parcours complexes. Cette fonctionnalité garantit une approche normalisée de la création de la réputation de l&#39;expéditeur.

### Fonctionnement

1. **Créer des campagnes de préchauffage d’adresses IP** : créez une ou plusieurs campagnes avec l’option **[!UICONTROL Activation du plan de préchauffage d’adresses IP]** activée. [En savoir plus](ip-warmup-campaign.md)

1. **Configurez votre plan** : accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres d’e-mail]** > **[!UICONTROL Plans de préchauffage d’adresses IP]** et téléchargez votre modèle de préchauffage par phases préparé avec votre consultant en délivrabilité. [En savoir plus](ip-warmup-plan.md)

1. **Exécuter des phases** : sélectionnez une campagne pour chaque phase et activez les exécutions correspondantes. Le système exclut automatiquement les profils des exécutions précédentes pour éviter le surcontact. [En savoir plus](ip-warmup-execution.md)

1. **Surveiller et ajuster** : utilisez le tableau de bord de rapports consolidés pour suivre la progression, surveiller les statuts d’exécution et modifier votre plan en cas de problème. [En savoir plus](ip-warmup-execution.md#monitor-plan)

## Surveillance en temps réel et mesures clés {#monitoring}

Adobe Journey Optimizer fournit des fonctionnalités de création de rapports intégrées pour suivre les performances de préchauffage des adresses IP :

* **Rapports dynamiques** : accédez à la mesure et à la visualisation en temps réel de vos campagnes à partir de l’onglet **[!UICONTROL Dernières 24 heures]**. [En savoir plus](../reports/live-report.md)

* **Intégration de Customer Journey Analytics** : pour obtenir des informations plus précises, utilisez Customer Journey Analytics pour analyser les données de Adobe Experience Platform et créer des visualisations personnalisées. [En savoir plus](../reports/report-gs-cja.md)

### Mesures cibles

Surveillez ces indicateurs clés de performances tout au long de votre préchauffage :

| Mesure | Seuil cible | Action si dépassée |
|--------|-----------------|-------------------|
| Taux de plaintes | ≤ 0,1 % | Contrôler le segment et supprimer les plaignants chroniques |
| Taux de hard bounces | ≤ 2 % | Consulter la liste des pratiques en matière de qualité et d&#39;hygiène |
| Taux dʼouverture | ≥ 10 % | Vérifier que vous ciblez des audiences engagées |

>[!TIP]
>
>Pour des analyses de campagne complètes, utilisez les fonctionnalités [rapport dynamique de campagne](../reports/campaign-live-report.md#email-live) et [rapport Customer Journey Analytics](../reports/campaign-global-report-cja-email.md).

## Guide de dépannage {#troubleshooting}

Utilisez cette matrice de décision pour résoudre les problèmes courants lors de votre préchauffage :

| Symptôme | Cause probable | Action recommandée |
|---------|--------------|-------------------|
| Échecs temporaires de Yahoo (erreurs 421) | Volume augmenté trop rapidement | Suspendre l’envoi pendant 24 heures, puis redémarrer au niveau précédent |
| Taux d’ouverture inférieur à 2 % sur les comptes de contrôle | PLACER SUR LA LISTE BLOQUÉE IP en cours de traitement | Vérifiez [Google Postmaster Tools](https://postmaster.google.com/) et [Microsoft SNDS](https://sendersupport.olc.protection.outlook.com/snds/) ; ouvrez un ticket de délivrabilité si nécessaire |
| Le taux de plaintes dépasse 0,3 % | Audience mal ciblée ou obsolète | Contrôlez les définitions de segment et excluez les plaignants chroniques de votre [liste de suppression](manage-suppression-list.md) |

>[!IMPORTANT]
>
>Il est préférable de ralentir votre réchauffement plutôt que d&#39;essayer de réparer ultérieurement la réputation d&#39;un expéditeur endommagée. Privilégiez toujours le maintien de mesures saines plutôt que l’augmentation agressive du volume.

## Bonnes pratiques après le préchauffage {#post-warmup}

Une fois que vous avez terminé votre plan de préchauffage et que les mesures se sont stabilisées :

* **Maintenir la cohérence** : Maintenez les augmentations de volume quotidiennes en dessous de 30 % semaine après semaine pour préserver votre réputation établie

* **Surveiller en permanence** : planifier des contrôles d’intégrité de la réputation trimestriels pour identifier et résoudre les problèmes de manière proactive

* **Respectez les signaux d’engagement** : continuez à donner la priorité aux destinataires engagés et à mettre en œuvre des campagnes de réengagement pour les abonnés inactifs

* **Garder l’authentification à jour** : vérifiez régulièrement que vos enregistrements SPF, DKIM et DMARC restent correctement configurés

## Principaux points à retenir {#key-takeaways}

* **Le réchauffement des adresses IP est essentiel** : ignorer le processus de réchauffement coûte plus de temps et de réputation que l’effort requis pour le faire correctement

* **Décisions axées sur les données** : suivez les taux de plaintes, de bounces et d’engagement quotidiennement et ajustez votre stratégie avant que les FAI ne vous pénalisent

* **Authentification d’abord, volume ensuite** : résolvez tous les problèmes SPF, DKIM et DMARC avant de commencer à ramper le volume

* **La cohérence est importante** : les fournisseurs de messagerie préfèrent des modèles d’envoi prévisibles ; évitez les pics de volume soudains ou les plannings d’envoi irréguliers

## Vidéo pratique {#video}

Découvrez les principes de base de la délivrabilité, l’établissement de la réputation et les bonnes pratiques pour le préchauffage des adresses IP dans Adobe Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3457695/?learn=on)

<!--
>[!NOTE]
>
>For more guidance, explore the [Adobe Journey Optimizer Deliverability Guide blog post](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950?profile.language=fr).-->

## Rubriques connexes {#related-topics}

* [Commencer avec les plans de préchauffage d’adresses IP](ip-warmup-gs.md)
* [Créer des campagnes de préchauffage d’adresses IP](ip-warmup-campaign.md)
* [Créer un plan de préchauffage d’adresses IP](ip-warmup-plan.md)
* [Exécuter le plan de préchauffage d’adresses IP](ip-warmup-execution.md)
* [Paramétrer des configurations de canal](channel-surfaces.md)
* [Délégation de sous-domaines](delegate-subdomain.md)
* [Gestion de la liste de suppression](manage-suppression-list.md)
* [&#x200B; Guide des bonnes pratiques en matière de délivrabilité &#x200B;](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=fr)

