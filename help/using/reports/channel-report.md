---
solution: Journey Optimizer
product: journey optimizer
title: Rapports au niveau des canaux
description: Découvrez comment utiliser les données des rapports Canal
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ead9359b-cdab-43ed-a469-d98b0ca19a17
source-git-commit: 5671f510d8be80b53d57b1ff90a101e500773243
workflow-type: tm+mt
source-wordcount: '3683'
ht-degree: 62%

---

# Rapports sur les canaux {#channel-report}

>[!CONTEXTUALHELP]
>id="ajo_channel_level_report"
>title="Rapport au niveau des canaux"
>abstract="Les rapports au niveau des canaux offrent une vue d’ensemble complète des mesures de trafic et d’engagement sur tous les canaux. Vos rapports sont composés de plusieurs widgets présentant le succès et les erreurs de votre campagne et de vos parcours. Vous pouvez modifier chaque tableau de bord de reporting en redimensionnant ou en supprimant des widgets."

>[!IMPORTANT]
>
> Pour accéder au menu **Rapport**, vous devez disposer de l’autorisation **[!UICONTROL Afficher les rapports du canal]**. [En savoir plus](channel-report-gs.md#before-starting-manage-reports-prereq)

Les rapports au niveau des canaux offrent aux utilisateurs et aux utilisatrices une vue d’ensemble complète des mesures de trafic et d’engagement au niveau des canaux. Les mesures sont agrégées afin de présenter des valeurs consolidées pour les actions provenant du canal choisi, couvrant plusieurs campagnes et parcours.

Vous pouvez accéder aux rapports au niveau des canaux en accédant au menu **Rapports** dans la section **Gestion des parcours**. Il est entièrement personnalisable. Vous pouvez filtrer vos données en fonction de la date du rapport ou de l’action. [En savoir plus](channel-report-gs.md)

La page Rapport s’affiche avec les onglets suivants :

* [E-mail](#email)
* [Notifications push](#push)
* [SMS](#sms)
* [In-app](#inapp)
* [Web](#web)
* [Publipostage direct](#direct-mail)

➡️ [Découvrez cette fonctionnalité en vidéo](#channel-report-video)

## E-mail {#email}

Dans les rapports au niveau des canaux, le menu E-mail présente les informations principales relatives aux e-mails envoyés dans vos campagnes et parcours. Les mesures sont détaillées ci-dessous.

### E-mail - Statistiques totales d’envoi {#email-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics"
>title="E-mail - Statistiques totales d’envoi"
>abstract="Les indicateurs de performance clés des statistiques d’envoi totales résument les données essentielles relatives à vos emails, telles que les messages ciblés ou délivrés."

![](assets/channel_email_total_sending.png)

La variable **[!UICONTROL Statistiques d’envoi total des emails]** widget offre un aperçu complet des performances de vos emails, avec des indicateurs de performances clés (IPC) qui résument les données essentielles sur vos emails.

+++ En savoir plus sur les mesures Statistiques d’envoi total des emails

* **[!UICONTROL Ciblés]** : nombre total d’e-mails traités.

* **[!UICONTROL Envoyés]** : nombre total d’e-mails envoyés.

* **[!UICONTROL Diffusés]** : nombre d’e-mails envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux de diffusion]** : pourcentage d’e-mails envoyés avec succès.

* **[!UICONTROL Rebonds]** : nombre total d’erreurs cumulées lors du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux de rebond]** : pourcentage d’e-mails ayant rebondi par rapport aux e-mails envoyés.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues empêchant l’e-mail d’être envoyé à des profils.

* **[!UICONTROL Taux d’erreurs]** : pourcentage d’erreurs survenues empêchant l’envoi des e-mails, par rapport aux e-mails envoyés.

* **[!UICONTROL Exclus]** : nombre de profils qui ont été exclus par Adobe Journey Optimizer.

* **[!UICONTROL Exclus]** : pourcentage de profils qui ont été exclus par Adobe Journey Optimizer.

+++

### E-mail - Statistiques totales de tracking {#email-total-tracking}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics"
>title="E-mail - Statistiques totales de tracking"
>abstract="Les KPI E-mail - Statistiques totales de tracking fournissent des données sur l’activité de profil pour vos e-mails."

![](assets/channel_email_total_tracking.png)

La variable **[!UICONTROL Statistiques de tracking total des emails]** widget offre un instantané détaillé de l’activité de profil liée à vos e-mails, fournissant des informations essentielles sur l’engagement et l’efficacité des e-mails.

+++ En savoir plus sur les mesures Statistiques de suivi total des emails

* **[!UICONTROL Ouvertures]** : nombre de fois que le message a été ouvert.

* **[!UICONTROL Taux d’ouvertures]** : nombre total de messages ouverts par rapport au nombre de messages diffusés.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans un message.

* **[!UICONTROL Taux de clics]** : pourcentage d’utilisateurs et d’utilisatrices ayant interagi avec l’e-mail.

* **[!UICONTROL Plaintes contre le spam]** : nombre de fois où un message a été déclaré comme spam ou courrier indésirable.

* **[!UICONTROL Taux de plaintes relatives aux spam]** : pourcentage de messages déclarés comme spam ou courrier indésirable par rapport au nombre d’e-mails envoyés.

* **[!UICONTROL Désabonnements]** : nombre de clics sur le lien de désabonnement.

* **[!UICONTROL Taux de désabonnement]** : pourcentage de désinscription par rapport au nombre d’e-mails envoyés.

+++

### E-mail - Statistiques d’envoi dans le temps {#email-sending-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics_overtime"
>title="E-mail - Statistiques d’envoi dans le temps"
>abstract="Le graphique E-mail - Statistiques d’envoi dans le temps présente des données concernant les e-mails envoyés, ventilées par heure, jour, semaine ou mois."

![](assets/channel_email_sending_statistics.png)

La variable **[!UICONTROL Email - Envoi de statistiques au fil du temps]** le graphique offre une représentation dynamique, affichant une analyse de votre activité de courrier électronique. Cette représentation graphique fournit une ventilation complète des emails envoyés, ce qui vous permet d’observer les tendances et les modèles à l’échelle horaire, quotidienne, hebdomadaire ou mensuelle.

+++ En savoir plus sur les e-mails - statistiques d’envoi au fil du temps

* **[!UICONTROL Envoyés]** : nombre total d’e-mails envoyés.

* **[!UICONTROL Diffusés]** : nombre d’e-mails envoyés avec succès, par rapport au nombre total d’e-mails envoyés.

* **[!UICONTROL Rebonds]** : nombre total d&#39;erreurs cumulées lors du traitement automatique des retours par rapport au nombre total d’e-mails envoyés.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues empêchant l’e-mail d’être envoyé à des profils.

+++

### E-mail - Statistiques de tracking dans le temps {#email-tracking-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics_overtime"
>title="E-mail - Statistiques de tracking dans le temps"
>abstract="Le graphique E-mail - Statistiques de tracking dans le temps fournit des données sur l’activité de profil de vos e-mails, ventilées par heure, jour, semaine ou mois."

![](assets/channel_email_tracking_overtime.png)

La variable **[!UICONTROL Email - Statistiques de tracking dans le temps]** Le graphique présente un aperçu détaillé de l’activité de profil liée à vos emails. Cette représentation graphique ventile les données sur une base horaire, quotidienne, hebdomadaire ou mensuelle, offrant de précieuses informations sur l’évolution de l’engagement des destinataires à différents intervalles de temps.

+++ En savoir plus sur les e-mails - statistiques de suivi dans les mesures de temps

* **[!UICONTROL Ouvertures]** : nombre d’ouvertures du message.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans un message.

+++

### Email - Catégories et motifs de rebond {#bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_categories"
>title="Catégories de rebond"
>abstract="Le tableau et les graphiques Catégories de rebond fournissent des données sur les erreurs temporaires et permanentes."

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons"
>title="Raisons de rebond"
>abstract="Les graphiques et le tableau Causes de rebonds contiennent les données disponibles sur les messages ayant fait l’objet d’un rebond."

![](assets/channel_email_bounce_categories.png)

La variable **[!UICONTROL Catégories rebonds]** et **[!UICONTROL Raisons de rebond]** Les widgets encapsulent les données associées aux messages rebonds, fournissant un aperçu complet des différentes catégories et des raisons spécifiques sous-jacentes aux messages rebonds.

Pour plus d’informations sur les rebonds, consultez la page [Liste de suppression](../reports/suppression-list.md).

+++ En savoir plus sur les mesures des catégories de rebond

* **[!UICONTROL Rebond définitif]** : nombre total d’erreurs permanentes, telles qu’une adresse e-mail incorrecte. Un message d&#39;erreur indique explicitement que l&#39;adresse n&#39;est pas valide, comme Utilisateur inconnu.

* **[!UICONTROL Rebond temporaire]** : nombre total d’erreurs temporaires, telles qu’une boîte de réception pleine.

* **[!UICONTROL Ignorées]** : nombre total d&#39;erreurs temporaires (par exemple, Absent(e) du bureau) ou techniques (par exemple, si le type d&#39;expéditeur est administrateur).

+++

### Raisons de l’erreur {#error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_error_reasons"
>title="Raisons de l’erreur"
>abstract="Les graphiques et le tableau Causes d’erreur vous permettent d’identifier les erreurs spécifiques qui se sont produites au cours du processus d’envoi."

![](assets/channel_email_error.png)

La variable **[!UICONTROL Raisons de l’erreur]** grâce aux graphiques et aux tableaux, vous pouvez identifier précisément les erreurs qui se sont produites tout au long du processus d’envoi, ce qui vous permet de comprendre facilement les problèmes rencontrés.

### Raisons des exclusions {#excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_excluded_reasons"
>title="Raisons des exclusions"
>abstract="Les graphiques et le tableau Causes d’exclusion illustrent les différents facteurs qui ont conduit à ce que des profils de personnes, exclus de l’audience ciblée, ne reçoivent pas le message."

![](assets/channel_email_excluded.png)

La variable **[!UICONTROL Exclure des motifs]** les graphiques et les tableaux présentent une vue d’ensemble complète des différents facteurs qui ont abouti à l’exclusion des profils utilisateur de l’audience ciblée, ce qui a pour effet que le message n’a pas été reçu.

Voir [cette page](exclusion-list.md) pour la liste complète des motifs d&#39;exclusion.

### Envoyés et diffusés par domaines {#sent-delivered-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_delivered_domains"
>title="Envoyés et diffusés par domaines"
>abstract="Le tableau et le graphique Envoyés et diffusés par domaines représentent la répartition au niveau du domaine de toutes les données importantes relatives à l’envoi d’e-mails."

![](assets/channel_email_sent_domains.png)

La variable **[!UICONTROL Envoyé et diffusé par domaines]** tableau et graphique fournissent une ventilation détaillée des diffusions email au niveau du domaine, offrant des informations complètes sur les performances de vos emails.

+++ En savoir plus sur les mesures Envoyés et distribués par domaines

* **[!UICONTROL Envoyés]** : nombre total d’e-mails envoyés.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

+++

### Rebonds et erreurs par domaine {#bounces-errors-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounces_errors_domains"
>title="Rebonds et erreurs par domaine"
>abstract="Le graphique et le tableau Rebonds et erreurs par domaines représentent la répartition au niveau du domaine des erreurs spécifiques survenues au cours du processus d’envoi."

![](assets/channel_email_bounces_domain.png)

La variable **[!UICONTROL Rebonds et erreurs par domaine]** Le graphique et le tableau offrent une ventilation au niveau du domaine des erreurs spécifiques rencontrées lors du processus d’envoi, fournissant une analyse détaillée des problèmes qui se sont produits.

+++ En savoir plus sur les mesures Rebonds et erreurs par domaine

* **[!UICONTROL Rebonds]** : nombre total d’erreurs cumulées lors de la procédure d’envoi et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours de la procédure d’envoi, empêchant le message d’être envoyé à des profils.

+++

### Ouvertures et clics par domaines {#open-clicks-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_open_clicks_domains"
>title="Ouvertures et clics par domaines"
>abstract="Le tableau et le graphique Ouvertures et clics par domaines représentent la répartition au niveau du domaine de l’engagement de vos visiteurs et visiteuses avec votre e-mail."

![](assets/channel_email_open_domains.png)

La variable **[!UICONTROL Ouverture et clics par domaine]** Le graphique et le tableau présentent une ventilation au niveau du domaine de l’engagement de vos visiteurs avec votre email, fournissant des informations précieuses sur la manière dont différents domaines interagissent avec votre contenu.

+++ En savoir plus sur les mesures Ouverture et clics par domaine

* **[!UICONTROL Ouvertures]** : nombre de fois que l’e-mail a été ouvert.

* **[!UICONTROL Clics]** : nombre de fois où un contenu a fait l&#39;objet d&#39;un clic dans un e-mail.

+++

### Raisons de rebond par domaine {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons_domains"
>title="Raisons de rebond par domaine"
>abstract="Le graphique et le tableau Raisons de rebond par domaine représentent la répartition au niveau du domaine des données sur les erreurs temporaires et permanentes."

![](assets/channel_email_bounce_domain.png)

La variable **[!UICONTROL Raisons des bounces par domaine]** le graphique et le tableau offrent une ventilation au niveau du domaine des données concernant les erreurs temporaires et permanentes, fournissant des informations détaillées sur les raisons des messages rebonds.

Pour plus d’informations sur les rebonds, consultez la page [Liste de suppression](../reports/suppression-list.md).

## Notification push {#push}

Dans vos rapports Canal , la variable **Notification push** détaille les informations principales relatives aux notifications push envoyées dans vos campagnes et Parcours. Les mesures sont présentées ci-dessous.

### Notifications push - Statistiques totales d’envoi {#push-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics"
>title="Notifications push - Statistiques totales d’envoi"
>abstract="Les KPI Notifications push - Statistiques totales d’envoi résument les données essentielles sur vos notifications push, telles que Ciblés ou Diffusés."

![](assets/channel_push_total_sending.png)

La variable **[!UICONTROL Notifications push - Statistiques totales d&#39;envoi]** Les indicateurs de performance clés constituent un résumé complet qui contient les données essentielles liées à vos notifications push. Ces mesures comprennent des informations détaillées sur l’audience ciblée et l’état réel de la diffusion, ce qui vous permet d’avoir une vue exhaustive de l’efficacité et de la portée de vos notifications push.

+++ En savoir plus sur les notifications push - Nombre total de statistiques d&#39;envoi

* **[!UICONTROL Ciblées]** : nombre total de notifications push traitées.

* **[!UICONTROL Envoyées]** : nombre total de notifications push envoyées.

* **[!UICONTROL Délivrées]** : nombre de notifications push envoyées avec succès, par rapport au nombre total de notifications push envoyées.

* **[!UICONTROL Taux de diffusion]** : pourcentage de notifications push envoyées avec succès.

* **[!UICONTROL Rebonds]** : nombre total d&#39;erreurs cumulées lors du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux de rebond]** : pourcentage de notifications push ayant rebondi par rapport aux notifications push envoyées.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues empêchant l’e-mail d’être envoyé à des profils.

* **[!UICONTROL Taux d’erreurs]** : pourcentage d’erreurs survenues empêchant l’envoi, par rapport aux notifications push envoyées.

* **[!UICONTROL Exclus]** : nombre de profils qui ont été exclus par Adobe Journey Optimizer.

* **[!UICONTROL Exclus]** : pourcentage de profils qui ont été exclus par Adobe Journey Optimizer.

+++

### Notification push - Statistiques totales de tracking {#push-total-tracking}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics"
>title="Notification push - Statistiques totales de tracking"
>abstract="Les Notification push - Statistiques totales de tracking fournissent des données sur l’activité de profil pour vos notifications push."

La variable **[!UICONTROL Notification push - Statistiques totales de tracking]** widget offre un instantané détaillé de l’activité de profil liée à vos notifications push, fournissant des informations essentielles sur l’engagement et l’efficacité des notifications push.

+++ En savoir plus sur les notifications push - Mesures de statistiques de suivi totales

* **[!UICONTROL Ouvertures]** : nombre de fois qu’une notification push a été ouverte.

* **[!UICONTROL Taux d&#39;ouverture]** : pourcentage de notifications push ouvertes.

* **[!UICONTROL Actions]** : nombre total d&#39;actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

* **[!UICONTROL Taux d&#39;action]** : pourcentage d’actions sur la notification push diffusée par rapport aux notifications push envoyées.

+++

### Notifications push - Statistiques d’envoi dans le temps {#push-sending-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_overtime"
>title="Notifications push - Statistiques d’envoi dans le temps"
>abstract="Le graphique Notification push - Statistiques d’envoi dans le temps présente des données concernant les notifications push envoyées, ventilées par heure, jour, semaine ou mois."

![](assets/channel_push_sending_statistics.png)

La variable **[!UICONTROL Notifications push - Envoi de statistiques au fil du temps]** le graphique offre une représentation dynamique, affichant une analyse de votre activité de notifications push. Cette représentation graphique fournit une ventilation complète des notifications push envoyées, ce qui vous permet d’observer les tendances et les modèles à l’échelle horaire, quotidienne, hebdomadaire ou mensuelle.

+++ En savoir plus sur les notifications push - Envoi de statistiques au fil du temps

* **[!UICONTROL Envoyées]** : nombre total de notifications push envoyées.

* **[!UICONTROL Délivrées]** : nombre de notifications push envoyées avec succès, par rapport au nombre total de notifications push envoyées.

* **[!UICONTROL Rebonds]** : nombre total d&#39;erreurs cumulées lors du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues empêchant l’e-mail d’être envoyé à des profils.

+++

### Notifications push - Statistiques de tracking dans le temps {#push-tracking-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_overtime"
>title="Notifications push - Statistiques de tracking dans le temps"
>abstract="Le graphe Notifications push - Statistiques de tracking dans le temps fournit des données sur l’activité de profil de vos notifications push, ventilées par heure, jour, semaine ou mois."

La variable **[!UICONTROL Notifications push - Statistiques de suivi dans le temps]** graph fournit un aperçu détaillé de l’activité de profil liée à vos notifications push. Cette représentation graphique ventile les données sur une base horaire, quotidienne, hebdomadaire ou mensuelle, offrant de précieuses informations sur l’évolution de l’engagement des destinataires à différents intervalles de temps.

+++ En savoir plus sur les notifications push - Statistiques de suivi sur les mesures de temps

* **[!UICONTROL Ouvertures]** : nombre de fois que votre notification push a été ouverte.

* **[!UICONTROL Actions]** : nombre total d’actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

+++

### Notifications push - Raisons exclues {#push-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_excluded_reasons"
>title="Raisons des exclusions"
>abstract="Les graphiques et le tableau Causes d’exclusion illustrent les différents facteurs qui ont conduit à ce que des profils de personnes, exclus de l’audience ciblée, ne reçoivent pas le message."

![](assets/channel_push_excluded.png)

La variable **[!UICONTROL Exclure des motifs]** les graphiques et les tableaux affichent les différentes raisons qui ont empêché les profils utilisateur, exclus des profils ciblés, de recevoir vos notifications push.

Voir [cette page](exclusion-list.md) pour la liste complète des motifs d&#39;exclusion.

### Notifications push - Raisons de l’erreur {#push-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_error_reasons"
>title="Raisons de l’erreur"
>abstract="Les graphiques et le tableau Causes d’erreur vous permettent d’identifier les erreurs spécifiques qui se sont produites au cours du processus d’envoi."

![](assets/channel_push_error.png)

La variable **[!UICONTROL Raisons de l’erreur]** les graphiques et les tableaux vous permettent d’identifier les erreurs spécifiques qui se sont produites pendant le processus d’envoi de vos notifications push, en fournissant des informations détaillées sur les problèmes rencontrés en cours de route.

### Notifications push - Suivi par plateforme {#push-tracking-platform}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_platform"
>title="Statistiques de tracking par plateforme"
>abstract="Le tableau et le graphique Statistiques de tracking par plateforme fournissent des données sur l’activité de profil pour vos notifications push en fonction du système opérationnel de votre profil."

La variable **[!UICONTROL Notifications push - Suivi par plateforme]** les graphiques et les tableaux détaillent l’activité des destinataires pour votre notification push en fonction du système opérationnel de votre profil.

### Notifications push - Envoi par plateforme {#push-sending-platform}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_platform"
>title="Statistiques d’envoi par plateforme"
>abstract="Le tableau et le graphique Statistiques d’envoi par plateforme présente les données concernant les notifications push envoyées."

![](assets/channel_push_sending_platform.png)

La variable **[!UICONTROL Notifications push - Envoi par plateforme]** les graphiques et les tableaux fournissent une ventilation complète détaillant le succès de vos notifications push par rapport aux systèmes opérationnels de vos profils. Cette analyse approfondie offre des informations précieuses sur l’efficacité de vos notifications push sur différentes plateformes.

## SMS {#sms}

Dans **Canal** , le menu SMS présente les informations principales relatives aux SMS envoyés dans vos campagnes et Parcours. Les mesures sont détaillées ci-dessous.

### SMS - Statistiques totales d’envoi {#sms-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics"
>title="SMS - Statistiques totales d’envoi"
>abstract="Les KPI SMS - Statistiques totales d’envoi résument les données essentielles relatives à vos SMS, telles que Ciblés ou Diffusés."

![](assets/channel_sms_total_sending.png)

La variable **[!UICONTROL SMS - Statistiques totales d’envoi]** Les indicateurs de performance clés constituent un résumé complet qui encapsule les données essentielles liées à votre SMS. Ces mesures comprennent des informations détaillées sur l’audience ciblée et l’état réel de la diffusion, ce qui vous permet d’avoir une vue exhaustive de l’efficacité et de la portée de vos SMS.

+++ En savoir plus sur les notifications push - Nombre total de statistiques d&#39;envoi

* **[!UICONTROL Ciblés]** : nombre de profils utilisateur qui sont qualifiés en tant que profils cibles pour le canal SMS.

* **[!UICONTROL Envoyés]** : nombre total de SMS envoyés.

* **[!UICONTROL Délivrés]** : nombre de messages SMS envoyés avec succès, par rapport au nombre total de SMS envoyés.

* **[!UICONTROL Taux de diffusion]** : pourcentage de SMS envoyés avec succès.

* **[!UICONTROL Rebonds]** : nombre total d’erreurs cumulées lors du traitement automatique des retours par rapport au nombre total de SMS envoyés.

* **[!UICONTROL Taux de rebond]** : pourcentage de SMS qui ont fait l’objet d’un rebond par rapport au nombre de SMS envoyés.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues, l’empêchant d’être envoyé à des profils.

* **[!UICONTROL Taux d’erreurs]** : pourcentage d’erreurs survenues empêchant l’envoi, par rapport aux SMS envoyés.

* **[!UICONTROL Exclus]** : nombre de profils utilisateur, exclus des profils ciblés, qui n’ont pas reçu le message.

* **[!UICONTROL Taux d’exclusion]** : pourcentage de profils qui ont été exclus par Adobe Journey Optimizer.

+++

### SMS - Statistiques totales de tracking {#sms-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics"
>title="SMS - Statistiques totales de tracking"
>abstract="Les statistiques totales de tracking des SMS fournissent des données sur l’activité de profil pour vos SMS."

![](assets/channel_sms_tracking.png)

La variable **[!UICONTROL SMS - Statistiques totales de tracking]** Ce widget fournit un aperçu détaillé des informations clés relatives à l’engagement de vos visiteurs vis-à-vis de vos URL, en vous offrant des informations sur l’efficacité de vos SMS :

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans un SMS.

### SMS - Statistiques d’envoi dans le temps {#sms-sending-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics_overtime"
>title="SMS - Statistiques d’envoi dans le temps"
>abstract="Le graphique SMS - Statistiques d’envoi dans le temps présente des données concernant les SMS envoyés, ventilées par heure, jour, semaine ou mois."

![](assets/channel_sms_sending_overtime.png)

La variable **[!UICONTROL SMS - Envoi de statistiques dans le temps]** graph offre une vue complète des SMS envoyés, avec des données ventilées par heure, jour, semaine ou mois. Cette représentation graphique vous permet de suivre et d&#39;analyser les tendances de votre activité de messagerie SMS sur différents intervalles de temps.

+++ En savoir plus sur les SMS - Envoi de statistiques au fil du temps

* **[!UICONTROL Envoyés]** : nombre total de SMS envoyés.

* **[!UICONTROL Rebonds]** : nombre total d’erreurs cumulées lors du traitement automatique des retours par rapport au nombre total de SMS envoyés.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues, l’empêchant d’être envoyé à des profils.

+++

### SMS - Statistiques de tracking dans le temps {#sms-tracking-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics_overtime"
>title="SMS - Statistiques de tracking dans le temps"
>abstract="Le graphique SMS - Statistiques de tracking dans le temps fournit des données sur l’activité de profil de vos SMS, ventilées par heure, jour, semaine ou mois."

![](assets/channel_sms_tracking_overtime.png)

La variable **[!UICONTROL SMS : statistiques de suivi dans le temps]** Le graphique fournit des données sur l’activité de profil liée à vos SMS, en fournissant une ventilation détaillée sur une base horaire, quotidienne, hebdomadaire ou mensuelle. Cette représentation graphique vous permet d’analyser et de comprendre les schémas de l’engagement des utilisateurs à différents intervalles de temps.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans un SMS.

### Raisons des exclusions {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_excluded_reasons"
>title="Raisons des exclusions"
>abstract="Les graphiques et le tableau Causes d’exclusion illustrent les différents facteurs qui ont conduit à ce que des profils de personnes, exclus de l’audience ciblée, ne reçoivent pas le message."

![](assets/channel_sms_excluded.png)

La variable **[!UICONTROL Exclut les motifs]** les graphiques et les tableaux décrivent visuellement les différents facteurs qui ont conduit à l’exclusion des profils d’utilisateur de l’audience ciblée, ce qui les empêche de recevoir vos SMS.

Voir [cette page](exclusion-list.md) pour la liste complète des motifs d&#39;exclusion.

### Raisons de rebond {#sms-bounce-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_bounce_reasons"
>title="Raisons de rebond"
>abstract="Les graphiques et le tableau Causes de rebonds contiennent les données disponibles sur les messages ayant fait l’objet d’un rebond."

![](assets/channel_sms_bounce_reasons.png)

La variable **[!UICONTROL Raisons des rebonds]** Les graphiques et les tableaux fournissent un aperçu complet des données relatives aux messages SMS rebonds, fournissant des informations précieuses sur les raisons spécifiques à l’origine des bounces de messages SMS.

### Raisons de l’erreur {#sms-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_error_reasons"
>title="Raisons de l’erreur"
>abstract="Les graphiques et le tableau Causes d’erreur vous permettent d’identifier les erreurs spécifiques qui se sont produites au cours du processus d’envoi."

La variable **[!UICONTROL Raisons de l’erreur]** les graphiques et les tableaux permettent d&#39;identifier les erreurs spécifiques qui se sont produites pendant le processus d&#39;envoi de vos SMS, ce qui facilite l&#39;analyse approfondie de tous les problèmes rencontrés.

## Publipostage direct {#direct-mail}

Dans **Canal** les rapports, **Canal Courrier** détaille les informations principales relatives aux messages de courrier envoyés dans votre **Campagnes** et **Parcours**. Les mesures sont détaillées ci-dessous.

### Courrier - Statistiques totales d’envoi {#direct-mail-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_sending_statistics"
>title="Courrier - Statistiques totales d’envoi"
>abstract="Les KPI Courrier - Statistiques totales d’envoi résument les données essentielles relatives à votre courrier, telles que Ciblés ou Diffusés."

![](assets/channel_direct_sending.png)

La variable **[!UICONTROL Courrier - Statistiques totales d’envoi]** widget offre un aperçu complet des performances de vos messages postaux, avec des indicateurs de performances clés (IPC) qui résument les données essentielles relatives à vos messages postaux.

+++ En savoir plus sur les mesures de statistiques d’envoi total

* **[!UICONTROL Ciblés]** : nombre de profils utilisateur qui sont qualifiés en tant que profils cibles pour les messages de courrier.

* **[!UICONTROL Envoyés]** : nombre total d’envois.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues empêchant l’e-mail d’être envoyé à des profils.

* **[!UICONTROL Taux d’erreurs]** : pourcentage d’erreurs survenues empêchant l’envoi de l’e-mail, par rapport aux notifications push envoyées.

* **[!UICONTROL Exclus]** : nombre de profils utilisateur, exclus des profils ciblés, qui n’ont pas reçu le message.

* **[!UICONTROL Taux d’exclusion]** : pourcentage de profils qui ont été exclus par Adobe Journey Optimizer.

+++

### Raisons des exclusions {#direct-mail-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_excluded_reasons"
>title="Raisons des exclusions"
>abstract="Les graphiques et le tableau Causes d’exclusion illustrent les différents facteurs qui ont conduit à ce que des profils de personnes, exclus de l’audience ciblée, ne reçoivent pas le message."

![](assets/channel_direct_excluded.png)

La variable **[!UICONTROL Courrier - Motifs exclus]** les graphiques et les tableaux illustrent visuellement les différents facteurs qui ont abouti à l’exclusion des profils utilisateur de l’audience ciblée, ce qui les empêche de recevoir vos courriers.

Voir [cette page](exclusion-list.md) pour la liste complète des motifs d&#39;exclusion.

### Raisons de l’erreur {#direct-mail-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_error_reasons"
>title="Raisons de l’erreur"
>abstract="Les graphiques et le tableau Causes d’erreur vous permettent d’identifier les erreurs spécifiques qui se sont produites au cours du processus d’envoi."

![](assets/channel_direct_error.png)

La variable **[!UICONTROL Courrier - Raisons de l’erreur]** fournir les moyens d’identifier les erreurs spécifiques qui se sont produites pendant le processus d’envoi de vos messages postaux, afin de permettre une analyse détaillée de tous les problèmes rencontrés.

## In-app {#in-app}

Dans les rapports au niveau des canaux, le menu In-app présente les informations principales relatives aux messages in-app envoyés dans vos campagnes et parcours. Les mesures sont détaillées ci-dessous.

### Engagement total dans l’application {#inapp-total-engagement}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement"
>title="In-app - Engagement total"
>abstract="Les KPI In-app - Engagement total fournissent des informations complètes sur l’engagement de vos visiteurs et visiteuses avec vos messages in-app, y compris des mesures telles que les impressions et les interactions."

![](assets/channel_inapp_engagement.png)

La variable **[!UICONTROL Engagement total dans l’application]** Les indicateurs de performance clés fournissent des informations complètes sur l’engagement des visiteurs avec vos messages in-app, notamment des mesures clés telles que **Impressions** et **Interactions**.

+++ En savoir plus sur les mesures d’engagement total in-app

* **[!UICONTROL Impressions]** : nombre total de messages in-app diffusés à tous les utilisateurs et utilisatrices.

* **[!UICONTROL Interactions]** : nombre total d’engagements en lien avec votre message in-app. Cela inclut toutes les actions entreprises par les personnes, telles que les clics, les rejets ou toute autre interaction.

+++

### Heures supplémentaires liées à l’engagement dans l’application {#inapp-engagement-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement_overtime"
>title="In-app - Engagement dans le temps"
>abstract="Le graphique In-app - Engagement dans le temps effectue le suivi des impressions et interactions in-app, fournissant des ventilations par heure, jour, semaine et mois."

![](assets/channel_inapp_engagement_overtime.png)

Le graphique **[!UICONTROL Engagement in-app dans le temps]** montre l’évolution de vos impressions et interactions in-app pour la période concernée en suivant toute impression, abandon ou interaction.

+++ En savoir plus sur les mesures d’engagement in-app au fil du temps

* **[!UICONTROL Impressions]** : nombre total de messages in-app diffusés à tous les utilisateurs et utilisatrices.

* **[!UICONTROL Interactions]** : nombre total d’engagements en lien avec votre message in-app. Cela inclut toutes les actions entreprises par les personnes, telles que les clics, les rejets ou toute autre interaction.

+++

## Web {#web}

Dans **Canal** , le menu Web détaille les informations principales relatives aux pages Web incluses dans votre **Campagnes** et **Parcours**. Les mesures sont détaillées ci-dessous.

### Web - Engagement total {#web-engagement-total}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement"
>title="Web - Engagement total"
>abstract="Les KPI Web - Engagement total fournissent des informations complètes sur l’engagement de vos visiteurs et visiteuses avec vos pages web, y compris des mesures telles que les impressions et les interactions."

![](assets/channel_web_engagement.png)

La variable **[!UICONTROL Engagement total sur le web]** Les indicateurs de performance clés offrent des informations complètes sur l’engagement des visiteurs de vos pages web, notamment des mesures clés telles que les impressions et les interactions.

+++ En savoir plus sur les mesures d’engagement total sur le web

* **[!UICONTROL Impressions]** : nombre total d’expériences web diffusées à tous les utilisateurs et utilisatrices.

* **[!UICONTROL Interactions]** : nombre total d’engagements en lien avec votre page web. Cela inclut toutes les actions entreprises par les personnes, telles que les clics ou toute autre interaction.

+++

### Web - Engagement total dans le temps {#web-engagement-total-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement_overtime"
>title="Web - Engagement total dans le temps"
>abstract="Le graphique Web - Engagement dans le temps effectue le suivi des impressions et interactions de vos pages web, fournissant des ventilations par heure, jour, semaine et mois."

![](assets/channel_web_engagement_overtime.png)

La variable **[!UICONTROL Heures supplémentaires d’engagement web]** surveille le graphique **Impressions** et **Interactions** de vos pages web, avec des ventilations détaillées toutes les heures, tous les jours, toutes les semaines et tous les mois.

+++ En savoir plus sur les mesures d&#39;heures supplémentaires d&#39;engagement web

* **[!UICONTROL Impressions]** : nombre total d’expériences web diffusées à tous les utilisateurs et utilisatrices.

* **[!UICONTROL Interactions]** : nombre total d’engagements en lien avec votre page web. Cela inclut toutes les actions entreprises par les personnes, telles que les clics ou toute autre interaction.

+++

## Rapport au niveau des canaux (vidéo) {#channel-report-video}

Découvrez comment accéder aux rapports, les parcourir et les exporter au niveau des canaux sur cette vidéo.

>[!VIDEO](https://video.tv.adobe.com/v/3424537?quality=12)
