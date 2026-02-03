---
solution: Journey Optimizer
product: journey optimizer
title: Guide de délivrabilité du préchauffage des adresses IP
description: Découvrez les principes de base de la délivrabilité et les bonnes pratiques pour le préchauffage des adresses IP.
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: adresse IP, délivrabilité, réputation, FAI, engagement
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: ht
source-wordcount: '1064'
ht-degree: 100%

---

# Guide de délivrabilité du préchauffage des adresses IP {#ip-warmup-deliverability-guide}

Lors du lancement de campagnes par e-mail avec de nouvelles adresses IP ou de nouveaux domaines dans Adobe Journey Optimizer, il est essentiel de comprendre les principes de base de la délivrabilité pour bâtir une réputation solide en tant qu’expéditeur. Ce guide aborde les concepts clés, les étapes de préparation et les bonnes pratiques pour vous aider à passer d’une réputation inexistante à un placement optimal en boîte de réception.

➡️ Découvrez dans la vidéo de cet [article de blog Adobe](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950){target="_blank"} les principes de base de la délivrabilité, comment bâtir une réputation solide et les bonnes pratiques pour le préchauffage des adresses IP.

>[!NOTE]
>
>Pour obtenir des instructions détaillées sur l’implémentation de plans de préchauffage d’adresses IP dans Adobe Journey Optimizer, reportez-vous à la section [Commencer avec les plans de préchauffage d’adresses IP](ip-warmup-gs.md).

## Importance de la réputation des adresses IP et des domaines {#reputation-matters}

Les fournisseurs de messagerie (Gmail, Yahoo, Microsoft, Apple Mail, etc.) évaluent chaque expéditeur en fonction de quatre critères :

* **Plaintes** : les destinataires ont-ils marqué vos messages comme spam ?
* **Engagement** : les destinataires ouvrent-ils, cliquent-ils ou répondent-ils à vos e-mails ?
* **Infrastructure** : votre infrastructure d’envoi est-elle authentifiée, stable et fiable ?
* **Contenu** : le contenu de votre message est-il légitime et utile ?

Le préchauffage des adresses IP renforce principalement les trois premiers critères en démontrant progressivement aux fournisseurs de messagerie que votre nouvelle infrastructure est légitime et sollicitée avant que vous n’augmentiez le volume d’envoi.

## Liste de contrôle en amont {#pre-flight-checklist}

Avant de commencer à préchauffer les adresses IP, assurez-vous que tout est en place. Le tableau ci-dessous décrit les tâches essentielles à effectuer avant de démarrer le plan de préchauffage d’adresses IP.

| Tâche | Objectif | Méthode |
|------|----------------|-------------------|
| Réserver des adresses IP fixes et déléguer des sous-domaines dans AJO | Votre future réputation dépend de ces éléments d’infrastructure. | Accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres d’e-mail]** > **[!UICONTROL Sous-domaines]**. [En savoir plus](delegate-subdomain.md) |
| Configurer SPF et DKIM | Permet de confirmer que votre serveur d’envoi est légitime et autorisé. | Géré automatiquement par Adobe après la [délégation de sous-domaine](delegate-subdomain.md) et la [création de la configuration des canaux](channel-surfaces.md). |
| Vérifier que l’enregistrement DMARC est configuré (p=none) | Permet d’activer le rapport d’authentification des e-mails et de préparer l’application des politiques. | Vérifiez que l’enregistrement DMARC est configuré pour tous les sous-domaines délégués. Lorsque vous déléguez un nouveau sous-domaine, vous pouvez configurer DMARC directement dans l’interface. [En savoir plus](dmarc-record.md) |
| Configurer la surveillance des listes de contrôle | Permet de détecter rapidement les problèmes de délivrabilité lors du processus de préchauffage. | Ajoutez des adresses de contrôle lors de la création de votre configuration des canaux. [En savoir plus](seed-lists.md) |
| Créer une audience à fort engagement pour la phase 1 | Permet d’améliorer les mesures d’engagement précoce de vos destinataires les plus actifs. | Créez une audience de moins de 5 000 contacts qui ont ouvert ou cliqué au cours des 30 derniers jours. [En savoir plus](../audience/creating-a-segment-definition.md) |

>[!CAUTION]
>
>Les problèmes d’authentification (SPF, DKIM, DMARC) ne peuvent pas être résolus par l’augmentation progressive du volume. Assurez-vous qu’ils sont correctement configurés avant de commencer les envois.

## Exemple de calendrier de préchauffage sur quatre semaines {#warmup-calendar}

Cet exemple de calendrier propose une augmentation progressive du volume en fonction du pourcentage de votre volume quotidien maximal (UDV). Ajustez ces chiffres en fonction de vos exigences en matière d’envoi et collaborez avec votre consultant ou votre consultante en délivrabilité pour créer un plan personnalisé.

| Jours | % d’UDV | Audience cible | Recommandations de contenu |
|------|----------|-----------------|------------------------|
| 1-3 | 0,5 % | Les personnes destinataires les plus engagées | Utilisez un format court en texte brut avec un appel à l’action visible dès l’ouverture. |
| 4-7 | 1 % | Utilisateurs et utilisatrices engagés et clientèle récente | Ajoutez une image principale légère, limitez le nombre de liens à 3 ou moins. |
| 8-14 | 5 % | Liste de personnes abonnées actives plus large | Utilisez votre modèle d’e-mail standard, mais évitez le contenu promotionnel trop chargé. |
| 15-21 | 25 % | Personnes abonnées actives et légèrement inactives | Utilisez du contenu marketing normal tout en surveillant de près les taux de plaintes. |
| 22-28 | 50-100 % | Liste complète (en respectant les listes de suppression) | Passez à votre cadence d’envoi normale. |

## Utilisation de la fonctionnalité de plans de préchauffage d’adresses IP {#ajo-warmup-feature}

Adobe Journey Optimizer comprend une fonctionnalité simplifiée de [plans de préchauffage d’adresses IP](ip-warmup-gs.md) qui évite de limiter manuellement le volume avec des configurations de parcours complexes. Cette fonctionnalité permet d’adopter une approche standardisée pour bâtir la réputation en tant qu’expéditeur.

### Fonctionnement

1. **Créer des campagnes de préchauffage d’adresses IP** : créez une ou plusieurs campagnes avec l’option **[!UICONTROL Activation du plan de préchauffage d’adresses IP]** activée. [En savoir plus](ip-warmup-campaign.md)

1. **Configurer votre plan** : accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres d’e-mail]** > **[!UICONTROL Plans de préchauffage d’adresses IP]** et chargez le modèle de préchauffage en plusieurs phases que vous avez préparé avec votre consultant ou consultante en délivrabilité. [En savoir plus](ip-warmup-plan.md)

1. **Exécuter les phases** : sélectionnez une campagne pour chaque phase et activez les exécutions correspondantes. Le système exclut automatiquement les profils des exécutions précédentes pour éviter les contacts excessifs. [En savoir plus](ip-warmup-execution.md)

1. **Surveiller et ajuster** : utilisez le tableau de bord de rapports consolidés pour suivre la progression, surveiller les statuts d’exécution et modifier votre plan en cas de problème. [En savoir plus](ip-warmup-execution.md#monitor-plan)

## Surveillance en temps réel et mesures clés {#monitoring}

Adobe Journey Optimizer fournit des fonctionnalités de création de rapports intégrées pour suivre les performances du préchauffage des adresses IP :

* **Rapports dynamiques** : consultez les mesures et graphiques de vos campagnes en temps réel dans l’onglet **[!UICONTROL Dernières 24 heures]**. [En savoir plus](../reports/campaign-live-report.md#email-live)

* **Rapports complets** : pour obtenir des informations plus détaillées, utilisez Customer Journey Analytics pour analyser les données d’Adobe Experience Platform et créer des graphiques personnalisés. [En savoir plus](../reports/report-gs-cja.md)

### Mesures cibles

Surveillez les indicateurs clés de performances suivants tout au long du préchauffage :

| Mesure | Seuil cible | Mesure corrective |
|--------|-----------------|-------------------|
| Taux de plaintes | ≤ 0,1 % | En cas de dépassement du seuil, auditez le segment et supprimez les profils qui se plaignent régulièrement. |
| Taux de rebond définitif | ≤ 2 % | En cas de dépassement du seuil, contrôlez la qualité de la liste et si elle est correctement mise à jour. |
| Taux dʼouverture | ≥ 10 % | Si le taux est trop faible, vérifiez que vous avez ciblé des audiences engagées. |

## Playbook de résolution des problèmes {#troubleshooting}

Utilisez la matrice de décision suivante pour résoudre les problèmes les plus courants lors du préchauffage :

| Symptôme | Cause probable | Action recommandée |
|---------|--------------|-------------------|
| Échecs temporaires de Yahoo (erreurs 421) | Augmentation trop rapide du volume | Arrêtez les envois pendant 24 heures, puis redémarrez au niveau précédent. |
| Taux d’ouverture inférieur à 2 % sur les comptes de contrôle | Adresse IP sur la liste bloquée | Consultez [Google Postmaster Tools](https://postmaster.google.com/) et [Microsoft SNDS](https://sendersupport.olc.protection.outlook.com/snds/) ; ouvrez un ticket de délivrabilité si nécessaire. |
| Taux de plaintes supérieure à 0,3 % | Audience mal ciblée ou obsolète | Vérifiez les définitions de segment et excluez les profils qui se plaignent régulièrement de votre [liste de suppression](manage-suppression-list.md). |

>[!IMPORTANT]
>
>Il est préférable de ralentir le préchauffage plutôt que d’avoir à rétablir plus tard une réputation d’expéditeur compromise. Mieux vaut assurer des mesures saines plutôt que d’augmenter le volume de manière trop abrupte.

## Bonnes pratiques après le préchauffage {#post-warmup}

Une fois le plan de préchauffage terminé et les mesures stabilisées :

* **Assurer la régularité** : limitez l’augmentation du volume quotidien à moins de 30 % d’une semaine sur l’autre afin de préserver votre réputation.

* **Surveiller en permanence** : planifiez des contrôles trimestriels de la réputation afin d’identifier et de résoudre les problèmes de manière proactive.

* **Respecter les signaux d’engagement** : continuez à donner la priorité aux destinataires engagés et à mettre en œuvre des campagnes de réengagement pour les personnes abonnées inactives.

* **Garder l’authentification à jour** : vérifiez régulièrement que vos enregistrements SPF, DKIM et DMARC sont correctement configurés.

## Points essentiels à retenir {#key-takeaways}

* **Le préchauffage des adresses IP est essentiel** : ignorer ce processus fait perdre plus de temps et de réputation que l’investissement nécessaire pour le mener à bien correctement.

* **Décisions axées sur les données** : suivez quotidiennement les taux de plaintes, de rebond et d’engagement et ajustez votre stratégie avant que les FAI ne vous pénalisent.

* **L’authentification d’abord, le volume ensuite** : résolvez tous les problèmes SPF, DKIM et DMARC avant de commencer à augmenter le volume.

* **La régularité est importante** : les fournisseurs de messagerie préfèrent des modèles d’envoi prévisibles ; évitez les pics de volume ou les plannings d’envoi irréguliers.

<!--
>[!NOTE]
>
>For more guidance, explore the [Adobe Journey Optimizer Deliverability Guide blog post](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950).-->

## Rubriques connexes {#related-topics}

* [Commencer avec les plans de préchauffage d’adresses IP](ip-warmup-gs.md)
* [Créer des campagnes de préchauffage d’adresses IP](ip-warmup-campaign.md)
* [Créer un plan de préchauffage d’adresses IP](ip-warmup-plan.md)
* [Exécuter le plan de préchauffage d’adresses IP](ip-warmup-execution.md)
* [Paramétrer des configurations de canal](channel-surfaces.md)
* [Déléguer des sous-domaines](delegate-subdomain.md)
* [Gérer la liste de suppression](manage-suppression-list.md)
* [Guide des bonnes pratiques en matière de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=fr)

