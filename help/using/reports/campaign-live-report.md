---
solution: Journey Optimizer
product: journey optimizer
title: Rapport en direct de Campaign
description: Découvrez comment utiliser les données du rapport en direct de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# Rapport en direct de Campaign {#campaign-live-report}

Le rapport en direct de Campaign est accessible directement depuis votre campagne à l’aide de la fonction **[!UICONTROL Live view]** bouton .

La campagne **[!UICONTROL Live report]** s’affiche avec les onglets suivants :

* [Campagne](#campaign-live)
* [Email](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)


La campagne **[!UICONTROL Live report]** est divisé en différents widgets détaillant le succès et les erreurs de votre campagne. Chaque widget peut être redimensionné et supprimé si nécessaire. Voir à ce sujet la section [section](../reports/live-report.md#modify-dashboard).

Pour obtenir la liste détaillée de chaque mesure disponible dans Adobe Journey Optimizer, reportez-vous à la section [cette page](live-report.md#list-of-components-live).

## Onglet Campagne {#campaign-global}

### Diffusion {#delivery-global}

Le **[!UICONTROL Campaign Statistics]** widget détaille les informations principales relatives à votre campagne :

* **[!UICONTROL Entered profiles]**: Nombre de profils ayant démarré le parcours.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Onglet Email {#email-live}

Depuis votre campagne **[!UICONTROL Live report]**, la variable **[!UICONTROL Email]** Cet onglet présente les informations principales relatives aux diffusions email envoyées dans votre campagne.

![](assets/campaign_report_live_1.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport Email.

Le **[!UICONTROL Email Sending Statistics]** widget détaille les informations principales relatives à votre message :

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

Le **[!UICONTROL Sending metrics by Email]** table et **[!UICONTROL Email Summary]** graph détaille le succès de votre diffusion :

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

* **[!UICONTROL Opens]**: Nombre d’ouvertures d’un message dans une diffusion.

* **[!UICONTROL Clicks]**: Nombre de clics sur un contenu dans une diffusion.

* **[!UICONTROL Unsubscribe]**: Nombre de clics sur le lien de désinscription.

* **[!UICONTROL Spam complaints]**: Nombre de fois où un message a été déclaré comme spam ou courrier indésirable.

Le **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** et **[!UICONTROL Hard and bounce - by Email]** Les widgets contiennent les données disponibles relatives aux messages rebonds, telles que :

* **[!UICONTROL Hard bounce]**: Nombre total d’erreurs permanentes, telles qu’une adresse email incorrecte. Il s’agit d’un message d’erreur indiquant explicitement que l’adresse n’est pas valide, tel qu’Utilisateur inconnu.

* **[!UICONTROL Soft bounce]**: Nombre total d’erreurs temporaires, telles qu’une boîte de réception pleine.

* **[!UICONTROL Ignored]**: Nombre total de messages temporaires, tels que Absence du bureau, ou une erreur technique, par exemple si le type d’expéditeur est Postmaster.

Le **[!UICONTROL Error Reasons]** et **[!UICONTROL Exclude Reasons]** les graphiques et les tableaux vous permettent de voir quelles erreurs et exclusions ont eu lieu au cours de votre diffusion.

Le **[!UICONTROL Email - Top recipient domain]** le graphique et le tableau détaillent les domaines les plus utilisés par les destinataires pour ouvrir l’email.
+++

## Onglet Notification push {#push-live}

Depuis votre campagne **[!UICONTROL Live report]**, la variable **[!UICONTROL Push notification]** Cet onglet présente les informations principales relatives aux diffusions push envoyées dans votre campagne.

![](assets/campaign_report_live_2.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport push.

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** et **[!UICONTROL Sending metrics - by Push]** Les widgets détaillent les informations principales relatives à votre message :

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

* **[!UICONTROL Opens]**: Nombre d’ouvertures d’un message dans une diffusion.

* **[!UICONTROL Actions]**: Nombre total d&#39;actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

* **[!UICONTROL Engagements]**: Nombre total d&#39;ouvertures et d&#39;actions pour cette notification push, c&#39;est-à-dire si le profil a ouvert la notification push ou si un utilisateur a cliqué sur un bouton.

Le **[!UICONTROL Error Reasons]** et **[!UICONTROL Exclude Reasons]** les graphiques et les tableaux vous permettent de voir quelles erreurs et exclusions ont eu lieu au cours de votre diffusion.

Le **[!UICONTROL Sending statistics - Failed]** widget vous permet de voir le nombre d’erreurs et de rebonds qui se sont produits.

Le **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** et **[!UICONTROL Breakdown by platform]** les graphiques et les tableaux décrivent le succès de votre notification push en fonction du système opérationnel.
+++

## Onglet SMS {#sms-live}

Depuis votre campagne **[!UICONTROL Live report]**, la variable **[!UICONTROL SMS]** Cet onglet présente les informations principales relatives aux diffusions SMS envoyées dans votre campagne.

![](assets/campaign_report_live_3.png)

+++En savoir plus sur les différentes mesures et widgets disponibles pour le rapport SMS.

Le **[!UICONTROL SMS - Sending statistics]** le tableau détaille le succès de votre diffusion :

* **[!UICONTROL Targeted]**: Nombre de profils utilisateur qui remplissent les critères de ciblage pour cette diffusion.

* **[!UICONTROL Excluded]**: Nombre de profils utilisateur, exclus des profils ciblés, qui n’ont pas reçu le message.

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

Le **[!UICONTROL SMS Performance by date]** avec un graphique, vous trouverez les informations principales relatives à votre message :

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

Le **[!UICONTROL Exclude Reasons]**, **[!UICONTROL Bounces Reasons]** et **[!UICONTROL Error Reasons]** les graphiques et les tableaux vous permettent de voir quelles erreurs et exclusions ont eu lieu au cours de votre diffusion.
+++

## Ressources supplémentaires

* [Prise en main des campagnes](../campaigns/get-started-with-campaigns.md)
* [Créer une campagne](../campaigns/create-campaign.md)
* [Création de campagnes déclenchées par l’API](../campaigns/api-triggered-campaigns.md)
* [Modifier ou arrêter une campagne](../campaigns/modify-stop-campaign.md)
* [Rapport global de campagnes](campaign-global-report.md)
