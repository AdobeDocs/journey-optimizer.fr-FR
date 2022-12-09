---
solution: Journey Optimizer
product: journey optimizer
title: Rapport global de campagnes
description: Découvrez comment utiliser les données du rapport global de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1468'
ht-degree: 0%

---

# Rapport global de campagnes {#campaign-global-report}

Le rapport global de campagnes est accessible directement depuis votre campagne à l’aide de la variable **[!UICONTROL All time]** bouton .

![](assets/campaign_report_global_5.png)

La campagne **[!UICONTROL Global report]** s’affiche avec les onglets suivants :

* [Campagne](#campaign-global)
* [Email](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)

La campagne **[!UICONTROL Global report]** est divisé en différents widgets détaillant le succès et les erreurs de votre campagne. Chaque widget peut être redimensionné et supprimé si nécessaire. Voir à ce sujet la section [section](../reports/global-report.md#modify-dashboard).

Pour obtenir la liste détaillée de chaque mesure disponible dans Adobe Journey Optimizer, reportez-vous à la section [cette page](global-report.md#list-of-components-global.md)

## Onglet Campagne {#campaign-global}

### Diffusion {#delivery-global}

![](assets/campaign_report_global_1.png)

Le **[!UICONTROL Campaign's Statistics]** widget détaille les informations principales relatives à votre campagne :

* **[!UICONTROL Entered profiles]**: Nombre de profils ayant démarré le parcours.

* **[!UICONTROL Actions delivered]**: Nombre total de fois uniques où une action du parcours a été diffusée.

* **[!UICONTROL Actions failed in %]**: Nombre total de fois uniques où une action a échoué dans le parcours par rapport au nombre total de fois uniques où une action a été diffusée.

## Onglet Email {#email-global}

![](assets/campaign_report_global_2.png)

Depuis votre campagne **[!UICONTROL Global report]**, la variable **[!UICONTROL Email]** Cet onglet présente les informations principales relatives aux diffusions email envoyées dans votre campagne.

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport Email.

Le **[!UICONTROL Email Sending Statistics]** graph détaille le succès de votre diffusion :

* **[!UICONTROL Targeted]**: Nombre total de messages traités lors de l&#39;analyse de la diffusion.

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Delivery Rate]**: Pourcentage de messages envoyés avec succès.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounce Rate]**: Pourcentage d&#39;emails qui ont fait l&#39;objet d&#39;un bounce par rapport au nombre d&#39;emails envoyés.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

* **[!UICONTROL Error Rate]**: Pourcentage d&#39;erreurs qui se sont produites pendant une diffusion empêchant son envoi par rapport au nombre d&#39;emails envoyés.

* **[!UICONTROL Retries]**: Nombre de courriers électroniques dans la file d’attente pour les reprises.

* **[!UICONTROL Excluded]**: Nombre de profils qui ont été exclus par Adobe Journey Optimizer.

Le **[!UICONTROL Email - Tracking statistics]** Le widget contient les données disponibles pour l’activité des destinataires pour votre diffusion :

* **[!UICONTROL Opens]**: Nombre de fois où la diffusion a été ouverte dans une diffusion.

* **[!UICONTROL Unique Opens]**: Pourcentage de diffusions ouvertes.

* **[!UICONTROL Open Rate]**: Nombre total d&#39;emails ouverts par rapport au nombre d&#39;emails délivrés.

* **[!UICONTROL Clicks]**: Nombre de clics sur un contenu dans un email.

* **[!UICONTROL Unique Clicks]**: nombre de destinataires ayant cliqué sur un contenu dans un email.

* **[!UICONTROL Unique Click Rate]**: Pourcentage d&#39;utilisateurs ayant interagi avec la diffusion.

* **[!UICONTROL Unsubscriptions]**: Nombre de clics sur le lien de désinscription.

* **[!UICONTROL Spam complaints]**: Nombre de fois où un message a été déclaré comme spam ou courrier indésirable.

Le **[!UICONTROL Sending Statistics]** Le graphique contient les données disponibles pour les emails envoyés, telles que :

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Retries]**: Nombre de courriers électroniques dans la file d’attente pour les reprises.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

Le **[!UICONTROL Bounce Reasons]** et **[!UICONTROL Bounce categories]** Les widgets contiennent les données disponibles relatives aux messages rebonds, telles que :

* **[!UICONTROL Hard bounce]**: Nombre total d’erreurs permanentes, telles qu’une adresse email incorrecte. Il s’agit d’un message d’erreur indiquant explicitement que l’adresse n’est pas valide, tel qu’Utilisateur inconnu.

* **[!UICONTROL Soft bounce]**: Nombre total d’erreurs temporaires, telles qu’une boîte de réception pleine.

* **[!UICONTROL Ignored]**: Nombre total de messages temporaires, tels que Absence du bureau, ou une erreur technique, par exemple si le type d’expéditeur est Postmaster.

Pour plus d’informations sur les rebonds, reportez-vous à la section [Liste de suppression](../reports/suppression-list.md) page.

Le **[!UICONTROL Error Reasons]** le graphique et le tableau vous permettent de voir quelle erreur s’est produite au cours de votre diffusion.

Le **[!UICONTROL Excluded reasons]** le graphique et le tableau affichent les différentes raisons qui ont empêché les profils utilisateur, exclus des profils ciblés, de recevoir le message.

Le **[!UICONTROL Email - Top Url]** détails graphiques et tableaux des URL de votre diffusion les plus visitées.

Le **[!UICONTROL Email - Top recipient domain]** le graphique et le tableau détaillent les domaines les plus utilisés par les destinataires pour ouvrir l’email.

>[!NOTE]
>
>Le **[!UICONTROL Optimized vs non optimized]** et **[!UICONTROL Send time optimization]**  Les widgets ne sont disponibles que si l’option Optimisation du temps d’envoi est activée pour votre diffusion. Pour plus d’informations sur l’optimisation du temps d’envoi, reportez-vous à la section [cette page](../building-journeys/journeys-message.md#send-time-optimization).

Le **[!UICONTROL Optimized vs non optimized]** graph détaille les informations principales relatives à votre message, qu’elles soient optimisées ou non :

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.
* **[!UICONTROL Opens]**: Nombre de fois où la diffusion a été ouverte dans une diffusion.
* **[!UICONTROL Clicks]**: Nombre de clics sur un contenu dans un email.

Le **[!UICONTROL Send time optimization]** détaille le succès de votre diffusion selon la méthode d&#39;envoi : optimisé ou normal.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.
* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.
+++

## Onglet Notification push {#push-global}

Depuis votre campagne **[!UICONTROL Global report]**, la variable **[!UICONTROL Push notification]** Cet onglet présente les informations principales relatives aux diffusions push envoyées dans votre campagne.

![](assets/campaign_report_global_3.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport push.

Le **[!UICONTROL Push notification - Sending statistics]** Le tableau présente les informations principales relatives à vos notifications push avec des graphiques et des indicateurs de performance clés :

* **[!UICONTROL Targeted]**: Nombre total de messages traités lors de l&#39;analyse de la diffusion.

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Delivery Rate]**: Pourcentage de messages envoyés avec succès.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounce Rate]**: Pourcentage de notifications push qui ont fait l&#39;objet d&#39;un bounce par rapport au nombre de notifications push envoyées.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

* **[!UICONTROL Error Rate]**: Pourcentage d&#39;erreurs qui se sont produites pendant une diffusion empêchant son envoi par rapport au nombre de notifications push envoyées.

* **[!UICONTROL Excluded]**: Nombre de profils qui ont été exclus par Adobe Journey Optimizer.

Le **[!UICONTROL Push - Tracking statistics]** contient les données disponibles pour l&#39;activité des destinataires pour votre diffusion :

* **[!UICONTROL Opens]**: Nombre d’ouvertures d’un message dans une diffusion.

* **[!UICONTROL Open Rate]**: Pourcentage de notifications push ouvertes.

* **[!UICONTROL Actions]**: Nombre total d&#39;actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

* **[!UICONTROL Engagements]**: Nombre total d&#39;ouvertures et d&#39;actions pour cette notification push, c&#39;est-à-dire si le profil a ouvert la notification push ou si un utilisateur a cliqué sur un bouton.

* **[!UICONTROL Engagement Rate]**: Pourcentage d&#39;ouvertures et d&#39;actions pour cette notification push, c&#39;est-à-dire si le profil a ouvert la notification push ou si un utilisateur a cliqué sur un bouton.

Le **[!UICONTROL Push notification summary]** Le graphique contient les données disponibles pour les notifications push envoyées, telles que :

* **[!UICONTROL Opens]**: Nombre d’ouvertures d’un message dans une diffusion.

* **[!UICONTROL Actions]**: Nombre total d&#39;actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

>[!NOTE]
>
>Le **[!UICONTROL Optimized vs non optimized]** et **[!UICONTROL Send time optimization]**  Les widgets ne sont disponibles que si l’option Optimisation du temps d’envoi est activée pour votre diffusion. Pour plus d’informations sur l’optimisation du temps d’envoi, reportez-vous à la section [cette page](../building-journeys/journeys-message.md#send-time-optimization).

Le **[!UICONTROL Optimized vs non optimized]** graph détaille les informations principales relatives à votre message, qu’elles soient optimisées ou non :

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.
* **[!UICONTROL Opens]**: Nombre de fois où la diffusion a été ouverte dans une diffusion.
* **[!UICONTROL Actions]**: Nombre total d&#39;actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

Le **[!UICONTROL Send time optimization]** détaille le succès de votre diffusion selon la méthode d&#39;envoi : optimisé ou normal.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.
* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

Le **[!UICONTROL Error Reasons]** le graphique et le tableau vous permettent de voir quelle erreur s’est produite au cours de votre diffusion.

Le **[!UICONTROL Excluded reasons]** le graphique et le tableau affichent les différentes raisons qui ont empêché les profils utilisateur, exclus des profils ciblés, de recevoir le message.

Le **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** et **[!UICONTROL Breakdown by platform]** les graphiques et les tableaux détaillent le succès de votre notification push en fonction du système opérationnel du destinataire.
+++

## Onglet SMS {#sms-global}

Depuis votre campagne **[!UICONTROL Global report]**, la variable **[!UICONTROL SMS]** Cet onglet présente les informations principales relatives aux diffusions SMS envoyées dans votre campagne.

![](assets/campaign_report_global_4.png)

+++En savoir plus sur les différentes mesures et widgets disponibles pour le rapport SMS.

Le **[!UICONTROL SMS - Sending statistics]** le tableau détaille le succès de votre diffusion :

* **[!UICONTROL Targeted]**: Nombre de profils utilisateur qui remplissent les critères de ciblage pour cette diffusion.

* **[!UICONTROL Excluded]**: Nombre de profils utilisateur, exclus des profils ciblés, qui n’ont pas reçu le message.

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

Le **[!UICONTROL SMS Performance by date]** avec un graphique, vous trouverez les informations principales relatives à votre message :

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

Le **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** et **[!UICONTROL Error Reasons]** les graphiques et les tableaux vous permettent de voir quelles erreurs et exclusions ont eu lieu au cours de votre diffusion.
+++

## Ressources supplémentaires

* [Prise en main des campagnes](../campaigns/get-started-with-campaigns.md)
* [Créer une campagne](../campaigns/create-campaign.md)
* [Création de campagnes déclenchées par l’API](../campaigns/api-triggered-campaigns.md)
* [Modifier ou arrêter une campagne](../campaigns/modify-stop-campaign.md)
* [Rapport en direct de Campaign](campaign-live-report.md)
