---
solution: Journey Optimizer
product: journey optimizer
title: Rapport global de parcours
description: Découvrez comment utiliser les données du rapport global de parcours
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1732'
ht-degree: 0%

---

# Rapport global de parcours {#journey-global-report}

Le rapport global de parcours est accessible directement depuis votre parcours à l’aide de la variable **[!UICONTROL View report]** bouton .

![](assets/report_journey.png)

Le parcours **[!UICONTROL Global report]** s’affiche avec les onglets suivants :

* [Parcours](#journey-global)
* [Email](#email-global)
* [Push](#push-global)
* [SMS](#sms-global)

Le parcours **[!UICONTROL Global report]** est divisé en différents widgets détaillant le succès et les erreurs de votre parcours. Chaque widget peut être redimensionné et supprimé si nécessaire. Voir à ce sujet la section [section](global-report.md#modify-dashboard).

Pour obtenir la liste détaillée de chaque mesure disponible dans Adobe Journey Optimizer, reportez-vous à la section [cette page](global-report.md#list-of-components-global).

## Onglet Parcours {#journey-global}

À partir du parcours **[!UICONTROL Global report]**, la variable **[!UICONTROL Journey]** vous donne une vue claire des données de suivi les plus importantes pour votre parcours.

![](assets/journey_global_1.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport Parcours.

Le **[!UICONTROL Journey Performance]** vous permet de voir le chemin d’accès de vos profils ciblés pas à pas tout au long de votre parcours.

Le **[!UICONTROL Journey Statistics]** Le widget affiche les IPC suivants :

* **[!UICONTROL Entered profiles]**: Nombre total d’individus ayant atteint l’événement d’entrée du parcours.

* **[!UICONTROL Exited profiles]**: Nombre total d’individus ayant quitté le parcours.

* **[!UICONTROL Failed individual journey]**: Nombre total de parcours individuels qui n’ont pas été exécutés avec succès.

Le **[!UICONTROL Events received by event]**, **[!UICONTROL Events by origin]** et **[!UICONTROL Top events]** Les widgets vous permettent de voir laquelle de vos **[!UICONTROL Events]** a été exécuté avec succès dans les graphiques et les tableaux.

**[!UICONTROL Action Performance]**, **[!UICONTROL Action Error Reasons]** et **[!UICONTROL Top Actions]** Les widgets représentent l’action et les erreurs les plus réussies survenues lors de la **[!UICONTROL Actions]** ont été déclenchées.

Le **[!UICONTROL Top Actions]** Le tableau contient les données disponibles pour **[!UICONTROL Actions]**, par exemple :

* **[!UICONTROL Actions successfully executed]**: Nombre total de **[!UICONTROL Actions]** exécuté avec succès pour un parcours.

* **[!UICONTROL Error in action]**: Nombre total d’erreurs qui se sont produites pour **[!UICONTROL Actions]**.

Le **[!UICONTROL Consent policies]** le tableau et le graphique affichent le nombre de profils exclus de chaque stratégie dans vos actions personnalisées.
Pour plus d’informations sur les actions personnalisées, reportez-vous à la section [la documentation détaillée ;](../action/about-custom-action-configuration.md).

Notez que pour que ces widgets s’affichent dans vos rapports Parcours, vous devez réinitialiser vos tableaux de bord. Pour ce faire, cliquez sur **[!UICONTROL Modify]** then **[!UICONTROL Reset]** en haut de votre rapport.
+++

## Onglet Email {#email-global}

À partir du parcours **[!UICONTROL Global report]**, la variable **[!UICONTROL Email]** Cet onglet présente les informations principales relatives aux diffusions email envoyées dans votre parcours.

![](assets/journey_global_2.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport Email.

Le **[!UICONTROL Email Sending Statistics]** graph détaille le succès de votre diffusion :

* **[!UICONTROL Targeted]**: Nombre de profils ciblés par Adobe Journey Orchestration pour toute action telle que l’envoi d’emails ou de SMS.

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Delivery Rate]**: Pourcentage de messages envoyés avec succès.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounce Rate]**: Pourcentage d&#39;emails qui ont fait l&#39;objet d&#39;un bounce par rapport au nombre d&#39;emails envoyés.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

* **[!UICONTROL Error Rate]**: Pourcentage d&#39;erreurs qui se sont produites pendant une diffusion empêchant son envoi par rapport au nombre d&#39;emails envoyés.

Le **[!UICONTROL Email - Tracking statistics]** contient les données disponibles pour l&#39;activité des destinataires pour votre diffusion :

* **[!UICONTROL Opens]**: Nombre de fois où la diffusion a été ouverte dans une diffusion.

* **[!UICONTROL Unique Opens]**: Pourcentage de diffusions ouvertes.

* **[!UICONTROL Unique Open Rate]**: Nombre total d&#39;emails ouverts par rapport au nombre d&#39;emails délivrés.

* **[!UICONTROL Clicks]**: Nombre de clics sur un contenu dans un email.

* **[!UICONTROL Unique Clicks]**: nombre de destinataires ayant cliqué sur un contenu dans un email.

* **[!UICONTROL Click through rate]**: Pourcentage d’utilisateurs ayant interagi avec le parcours.

* **[!UICONTROL Unsubscribe]**: Nombre de clics sur le lien de désinscription.

* **[!UICONTROL Spam complaints]**: Nombre de fois où un message a été déclaré comme spam ou courrier indésirable.

Le **[!UICONTROL Sending Statistics]** Le graphique contient les données disponibles pour les emails envoyés, telles que :

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

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

>[!NOTE]
>
>Les widgets et mesures Offres ne sont disponibles que si une décision a été insérée dans un courrier électronique. Pour plus d’informations sur la gestion des décisions, reportez-vous à cette section [page](../offers/get-started/starting-offer-decisioning.md).

Le **[!UICONTROL Offers statistic]** et **[!UICONTROL Offers statistics]** au fil du temps, les widgets mesurent le succès et l’impact de votre offre sur votre audience ciblée. Il détaille les informations principales relatives à votre message avec les KPI :

* **[!UICONTROL Offer sent]**: Nombre total d&#39;envois pour l&#39;offre.

* **[!UICONTROL Offer impression]**: Nombre d’ouvertures de l’offre dans une diffusion.

* **[!UICONTROL Offer clicks]**: Nombre de clics sur une offre dans une diffusion.

Le **[!UICONTROL Offers detailed statistic]** contient les données disponibles pour l&#39;activité des destinataires avec votre offre :

* **[!UICONTROL Placement name]**: Nom de l’emplacement utilisé pour afficher votre offre. Pour plus d’informations sur l’emplacement, reportez-vous à cette section [page](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: Nom de l&#39;offre ajoutée dans la diffusion. Pour plus d’informations sur l’emplacement, reportez-vous à cette section [page](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Nombre total d&#39;envois pour l&#39;offre.

* **[!UICONTROL Offer impression rate]**: Pourcentage d&#39;offres ouvertes par rapport au nombre d&#39;offres envoyées.

* **[!UICONTROL Offer click rate]**: Pourcentage d&#39;utilisateurs ayant interagi avec l&#39;offre.
+++

## Onglet Notification push {#push-global}

À partir du parcours **[!UICONTROL Global report]**, la variable **[!UICONTROL Push notification]** Cet onglet présente les informations principales relatives aux diffusions push envoyées dans votre parcours.

![](assets/journey_global_3.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport push.

Le **[!UICONTROL Push notification - Sending statistics]** Le tableau présente les informations principales relatives à vos notifications push avec des graphiques et des indicateurs de performance clés :

* **[!UICONTROL Targeted]**: Nombre de profils ciblés par Adobe Journey Orchestration pour toute action telle que l’envoi d’emails ou de SMS.

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Delivery Rate]**: Pourcentage de messages envoyés avec succès.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounce Rate]**: Pourcentage de notifications push qui ont fait l&#39;objet d&#39;un bounce par rapport au nombre de notifications push envoyées.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

* **[!UICONTROL Error Rate]**: Pourcentage d&#39;erreurs qui se sont produites pendant une diffusion empêchant son envoi par rapport au nombre de notifications push envoyées.

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

Le SMS **[!UICONTROL Global report]** est divisé en différents widgets détaillant le succès et les erreurs de votre diffusion. Chaque widget peut être redimensionné et supprimé si nécessaire. Voir à ce sujet la section [section](global-report.md#modify-dashboard).
+++

## Onglet SMS {#sms-global}

![](assets/journey_global_4.png)

+++En savoir plus sur les différentes mesures et widgets disponibles pour le rapport SMS.

Le **[!UICONTROL SMS - Sending statistics]** le tableau détaille le succès de votre diffusion :

* **[!UICONTROL Targeted]**: Nombre de profils utilisateur qui remplissent les critères de ciblage pour cette diffusion.

* **[!UICONTROL Excluded]**: Nombre de profils utilisateur, exclus des profils ciblés, qui n’ont pas reçu le message.

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

Le **[!UICONTROL SMS summary]** avec un graphique, vous trouverez les informations principales relatives à votre message :

* **[!UICONTROL Sent]**: Nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Delivered]**: Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]**: Nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Errors]**: Nombre total d&#39;erreurs qui se sont produites au cours d&#39;une diffusion et qui l&#39;ont empêché d&#39;être envoyée aux profils.

Le **[!UICONTROL Exclude Reasons]** les graphiques et les tableaux vous permettent de voir quelles erreurs et exclusions ont eu lieu au cours de votre diffusion.
+++
