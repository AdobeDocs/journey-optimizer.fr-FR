---
solution: Journey Optimizer
product: journey optimizer
title: Optimisation de l’heure d’envoi pour les messages mobiles
description: Découvrez comment configurer et utiliser l’optimisation de l’heure d’envoi pour les messages mobiles dans Adobe Journey Optimizer.
feature: SMS
topic: Send Time Optimization
role: User
level: Intermediate
exl-id: 56ff1000-7799-40ff-8f03-2f5868d05e7b
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: f03a3a13-9e99-4c7c-a1ae-0f4d07ced35c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 84aa39bfd480e5bcaa8a58c5ec29f1990e5ddc6f
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 1%

---


# Optimisation de l’heure d’envoi pour les messages mobiles {#sms-send-time-optimization}

>[!AVAILABILITY]
>
>L’optimisation de l’heure d’envoi pour les messages mobiles (SMS, RCS et WhatsApp) est disponible à partir du 2e semestre 2026 et s’applique aux Parcours et aux campagnes.

## Vue d’ensemble {#overview}

L’optimisation de l’heure d’envoi (STO) pour les messages mobiles permet aux spécialistes marketing de dépasser la planification « par lots et par explosion » en utilisant des informations basées sur l’IA pour déterminer l’heure de diffusion optimale pour chaque profil individuel. Plutôt que d’envoyer des messages à l’ensemble de votre audience en même temps, Adobe Journey Optimizer analyse les schémas d’engagement historiques de chaque profil et prédit le moment où cet individu est le plus susceptible d’ouvrir, de cliquer ou de répondre à un SMS, un RCS ou un message WhatsApp.

En diffusant les messages au moment de l’engagement prédit le plus élevé, STO permet d’augmenter les taux d’ouverture, les taux de clics publicitaires et le retour sur investissement global de la campagne, sans nécessiter de segmentation manuelle de l’audience par fuseau horaire ou cohorte comportementale. STO pour la messagerie mobile est pris en charge sur les canaux SMS, RCS et WhatsApp et est disponible dans les contextes d’exécution de Parcours et de campagne.

## Conditions préalables {#prerequisites}

Avant d’activer l’optimisation de l’heure d’envoi pour les messages mobiles, vérifiez les points suivants :

- Votre organisation est configurée pour Adobe Journey Optimizer et pour au moins l’un des canaux SMS, RCS ou WhatsApp.
- Il existe un volume suffisant de données historiques d’engagement mobile, notamment des événements d’envoi, des ouvertures, des clics sur les liens et des réponses, pour l’audience cible dans Adobe Experience Platform (AEP). Le modèle d’IA nécessite un historique d’interactions antérieur pour générer des prédictions fiables par profil.
- La surface de canal appropriée (SMS, RCS ou WhatsApp) est configurée et active dans votre instance AJO. Voir [Configurer des surfaces de canal SMS](../sms/sms-configuration.md) pour obtenir des instructions de configuration.
- Pour les cas d’utilisation basés sur des Parcours, le Parcours doit être conçu de sorte que le nœud d’action du message ne soit pas limité par les nœuds d’attente ou d’événement en amont dont les délais entrent en conflit avec la fenêtre de diffusion STO.

>[!NOTE]
>
>Les profils dont les données historiques d’engagement sont insuffisantes reviennent à une heure d’envoi par défaut que vous définissez lors de la configuration. Les prédictions STO sont générées et notées au niveau du profil individuel.

## Fonctionnement {#how-it-works}

La STO pour les messages mobiles repose sur un modèle d’IA personnalisé qui traite les signaux d’engagement historiques de chaque profil pour prévoir la fenêtre de diffusion optimale. Les étapes suivantes décrivent le flux de bout en bout.

### &#x200B;1. Ingestion de données et entraînement de modèles

Le modèle d’IA ingère en permanence des événements d’engagement mobile stockés dans Adobe Experience Platform, notamment les horodatages d’ouverture des messages, les événements de clic sur les liens, les heures de réponse et les enregistrements historiques de diffusion. Ces signaux constituent les données d’apprentissage utilisées pour apprendre les modèles comportementaux de chaque profil, tels que les heures d’interaction préférées, les tendances du jour de la semaine et la réactivité entre les fuseaux horaires. Le modèle est recyclé sur une base continue pour rester sensible aux changements de comportement d&#39;engagement.

### &#x200B;2. Score de prédiction par profil

Une fois formé, le modèle attribue un score à chaque profil dans l’audience cible et produit une fenêtre d’heure d’envoi optimale. Cette prédiction est réécrite dans le profil dans AEP sous la forme d’un attribut calculé, ce qui la rend disponible pour les Parcours et les campagnes au moment de l’exécution sans nécessiter d’appels d’API supplémentaires ou de recherches en temps réel pendant l’envoi du message.

### &#x200B;3. Planification de l’exécution du parcours

Lorsqu’un Parcours contenant un nœud d’action SMS, RCS ou WhatsApp activé pour STO est actif, l’exécution du Parcours lit l’attribut d’heure d’envoi prévu de chaque profil éligible lorsque ce dernier atteint le nœud d’action. Le message est conservé dans la fenêtre d’optimisation configurée et distribué lorsque l’heure optimale prévue arrive. Si le temps prévu est déjà écoulé ou s’il ne s’écoule pas, le comportement de secours que vous avez configuré est appliqué.

### &#x200B;4. Distribution d’envoi de la campagne

Pour les campagnes, STO distribue l’envoi à travers l’audience en fonction des prédictions par profil plutôt que d’émettre une seule répartition en bloc. AJO échelonne la diffusion dans la fenêtre d’envoi configurée de la campagne, en respectant l’heure optimale prévue de chaque profil tout en restant dans les limites de la fenêtre que vous définissez.

>[!NOTE]
>
>Si l’heure optimale prévue d’un profil se situe en dehors de la fenêtre d’envoi configurée, le message est envoyé à la limite la plus proche (le début ou la fin de la fenêtre), selon ce qui est le plus proche de la prédiction.

## Configurer l’optimisation de l’heure d’envoi {#configure}

### Activer la STO dans une campagne {#configure-campaign}

1. Dans Journey Optimizer, accédez à **Campagnes** et créez une campagne ou ouvrez un brouillon existant.
2. Sélectionnez **SMS**, **RCS** ou **WhatsApp** comme canal et effectuez les étapes de contenu de l’audience et du message.
3. Dans la section **Planification**, sélectionnez **Optimisation de l’heure d’envoi** au lieu d’une date et d’une heure d’envoi fixes.
4. Utilisez le bouton (bascule) **Optimisation de l’heure d’envoi** pour activer la fonctionnalité.
5. Configurez la **fenêtre Envoyer** : définissez les heures de début et de fin pendant lesquelles AJO est autorisé à diffuser des messages. La fenêtre doit s’étendre sur au moins une heure et peut durer jusqu’à 24 heures.
6. Définissez une **heure d’envoi de secours** pour les profils qui n’ont pas un historique d’engagement suffisant pour générer une prédiction. Vous pouvez choisir d’effectuer l’envoi immédiatement à l’ouverture de la fenêtre ou à une heure fixe dans la fenêtre.
7. Effectuez les étapes de capping de la fréquence, de révision et d’activation, puis activez la campagne.

### Activer la STO dans un Parcours {#configure-journey}

1. Ouvrez ou créez un Parcours dans la zone de travail du Parcours.
2. Ajoutez ou sélectionnez un nœud d’action **SMS**, **RCS** ou **WhatsApp**.
3. Dans le panneau de configuration du nœud d’action, développez les paramètres **Heure d’envoi**.
4. Activez le bouton (bascule) **Optimisation de l’heure d’envoi**.
5. Définissez la **fenêtre d’optimisation** : durée maximale (en heures) pendant laquelle l’exécution peut contenir un message en attendant l’heure de diffusion optimale prévue. La fenêtre par défaut est de six heures ; la valeur maximale est de 24 heures.
6. Configurez le **Comportement de secours** — à envoyer immédiatement lorsqu’un profil entre dans le nœud ou attendre la prochaine fenêtre prédite disponible — pour les profils qui ne disposent d’aucune donnée de prédiction.
7. Enregistrez la configuration du nœud et publiez le Parcours.

>[!NOTE]
>
>Lorsque la STO est active sur un nœud d’action de Parcours, le délai de diffusion effectif d’un profil peut différer du moment où le profil accède au nœud jusqu’à la longueur complète de la fenêtre d’optimisation configurée. Tenez compte de ce délai lors de la conception des nœuds d’attente en amont et de la définition des délais d’expiration au niveau du Parcours pour éviter les sorties de parcours prématurées.

## Mécanismes de sécurisation et limitations {#guardrails}

- STO s&#39;applique uniquement aux SMS sortants, RCS et WhatsApp. Les flux de réponse entrants et les sessions de messagerie bidirectionnelle ne sont pas soumis à la planification STO.
- Chaque nœud d’action Campaign ou Parcours prend en charge une surface de canal par message compatible STO. La coordination cross-canal STO (par exemple, SMS et WhatsApp dans un seul nœud) n’est pas prise en charge.
- Le modèle d’IA nécessite au moins 30 jours de données historiques d’engagement mobile par profil pour produire une prédiction. Les profils inférieurs à ce seuil utilisent l’heure d’envoi de secours configurée.
- La STO interagit avec les règles de limitation de fréquence. Si la fenêtre de diffusion prévue d’un profil limité entre en conflit avec une limite de limitation, le message est supprimé conformément à la règle de limitation et n’est pas replanifié dans une fenêtre ultérieure.
- Les indicateurs de consentement, les enregistrements d’opt-out et les listes de suppression globales sont toujours appliqués, quelle que soit la planification de l’arrêt. Un message conservé pour une diffusion optimisée est toujours soumis à des vérifications de consentement au moment de l’envoi.
- La STO n’est pas disponible pour les messages transactionnels lorsque la diffusion immédiate est requise par des exigences commerciales ou réglementaires.

## Rubriques connexes {#related-topics}

- [Prise en main des SMS, RCS et WhatsApp dans Journey Optimizer](../sms/create-sms.md)
- [Configurer des surfaces de canal SMS](../sms/sms-configuration.md)
- [Optimisation de l’heure d’envoi des e-mails et des notifications push](../building-journeys/send-time-optimization.md)
- [Classement optimisé par l’IA dans Journey Optimizer](../offers/offer-activities/ai-ranking.md)
- [Notes de mise à jour de Journey Optimizer](../rn/release-notes.md)
