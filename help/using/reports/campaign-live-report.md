---
solution: Journey Optimizer
product: journey optimizer
title: Rapport dynamique de campagne
description: Découvrez comment utiliser les données du rapport dynamique de campagne
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 6bceccc561daac594f5c84d3d3250d887a349b7b
workflow-type: tm+mt
source-wordcount: '2063'
ht-degree: 40%

---

# Rapport dynamique de campagne {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="Rapport dynamique de campagne"
>abstract="Le rapport dynamique de campagne vous permet de mesurer et de visualiser en temps réel l’efficacité et les performances de vos campagnes (limité aux dernières 24 heures). Le rapport dyamique de campagne est composé de plusieurs widgets présentant le succès et les erreurs de votre campagne. Vous pouvez modifier chaque tableau de bord de reporting en redimensionnant ou en supprimant des widgets."

Les rapports dynamiques, accessibles à partir de l’onglet Dernières 24 heures, affichent les événements qui se sont produits au cours des dernières 24 heures, avec un intervalle de temps minimal de deux minutes à compter de l’occurrence de l’événement. En comparaison, les rapports globaux portent sur les événements qui se sont produits il y a au moins deux heures et couvrent les événements sur une période sélectionnée.

Vous pouvez accéder directement au rapport dynamique de campagne à partir de votre campagne à l’aide du bouton **[!UICONTROL Vue dynamique]**.

La page **[!UICONTROL Rapport dynamique]** de la campagne s&#39;affiche avec les onglets suivants :

* [Campagne](#campaign-live)
* [E-mail](#email-live)
* [In-app](#inapp-live)
* [Push](#push-live)
* [SMS](#sms-live)
* [Web](#web-tab)
* [Courrier](#direct-mail-tab)

Le **[!UICONTROL rapport dyamique]** de campagne est divisé en différents widgets présentant le succès et les erreurs de votre campagne. Chaque widget peut être redimensionné et supprimé si nécessaire. Pour plus d&#39;informations à ce propos, consultez cette [section](../reports/live-report.md#modify-dashboard).

Pour obtenir la liste détaillée de chaque mesure disponible dans Adobe Journey Optimizer, reportez-vous à [cette page](live-report.md#list-of-components-live).

## Onglet Campagne {#campaign-live}

### Diffusion {#delivery-live}

Le widget **[!UICONTROL Statistiques de la campagne]** présente les principales informations relatives à votre campagne :

* **[!UICONTROL Profils entrés]** : nombre de profils ayant commencé le parcours.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## Onglet E-mail {#email-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_sending_statistics"
>title="Email - Statistiques d&#39;envoi"
>abstract="Le graphique Email - Statistiques d’envoi résume les données essentielles relatives à votre email, telles que Ciblés ou Délivrés, depuis les dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_statistics"
>title="Email - Statistics"
>abstract="Le tableau Email - Statistiques fournit des données sur l’activité de profil de votre email au cours des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_categories"
>title="Email - Catégories de rebond"
>abstract="Le tableau et les graphiques des catégories Email - Bounce fournissent des données sur les erreurs temporaires et permanentes des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_performance_bydate"
>title="Email - Performance par date"
>abstract="Le graphique Email - Performances par date présente des données complètes relatives aux derniers 24 heures concernant les emails envoyés, en fournissant des informations sur les mesures clés telles que les diffusions et les bounces, ce qui permet une analyse détaillée du processus de diffusion des emails."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_reasons"
>title="Email - Raisons des rebonds"
>abstract="Les graphiques et tableaux Email - Raisons des bounces contiennent les données disponibles relatives aux messages rebonds des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_error_reasons"
>title="Email - Raisons de l’erreur"
>abstract="Le tableau Email - Raisons de l’erreur vous permet d’identifier les erreurs spécifiques qui se sont produites au cours du processus d’envoi au cours des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_excluded_reasons"
>title="Email - Exclu"
>abstract="Les graphiques et tableaux Exclus des motifs illustrent les différents facteurs qui ont conduit à des profils d’utilisateurs, exclus de l’audience ciblée, et qui n’ont pas reçu le message au cours des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_best_recipient"
>title="Email - Meilleur domaine de destinataire"
>abstract="Le tableau et graphique Email - Meilleur domaine de destinataire fournit une ventilation détaillée des domaines que les destinataires utilisent le plus souvent pour ouvrir l&#39;email, offrant des informations précieuses sur le comportement des destinataires au cours des dernières 24 heures."

Depuis votre campagne **[!UICONTROL Rapport en direct]**, la variable **[!UICONTROL Email]** Cet onglet présente les informations principales relatives à l&#39;email envoyé dans votre campagne.

![](assets/campaign_report_live_1.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport d’e-mail.

Le widget **[!UICONTROL Statistiques d’envoi des e-mails]** présente les principales informations relatives à votre message :

* **[!UICONTROL Livrés]** : nombre de messages envoyés avec succès.

* **[!UICONTROL Rebonds]**: Nombre total d&#39;erreurs cumulées lors du processus d&#39;envoi et du traitement automatique des retours.

* **[!UICONTROL Erreurs]**: nombre total d&#39;erreurs qui se sont produites pendant le processus d&#39;envoi et qui l&#39;ont empêché d&#39;être envoyé aux profils.

La variable **[!UICONTROL Envoi de mesures par courrier électronique]** table et **[!UICONTROL Email Summary]** graph détaille le succès de votre email :

* **[!UICONTROL Envoyés]** : nombre total d’e-mails envoyés.

* **[!UICONTROL Livrés]** : nombre de messages envoyés avec succès.

* **[!UICONTROL Rebonds]**: Nombre total d&#39;erreurs cumulées lors du processus d&#39;envoi et du traitement automatique des retours.

* **[!UICONTROL Erreurs]**: nombre total d&#39;erreurs qui se sont produites pendant le processus d&#39;envoi et qui l&#39;ont empêché d&#39;être envoyé aux profils.

* **[!UICONTROL Ouvertures]**: nombre d’ouvertures d’un message.

* **[!UICONTROL Clics]**: nombre de clics sur un contenu.

* **[!UICONTROL Désabonnements]** : nombre de clics sur le lien de désabonnement.

* **[!UICONTROL Plaintes contre le spal]** : nombre de fois où un message a été déclaré comme spam ou courrier indésirable.

Les widgets **[!UICONTROL Raisons de rebond]** et **[!UICONTROL Catégories de rebond]** contiennent les données disponibles relatives aux messages de rebond, telles que :

* **[!UICONTROL Hard bounce]** : nombre total d’erreurs permanentes, telles qu’une adresse e-mail incorrecte. Un message d&#39;erreur indique explicitement que l&#39;adresse n&#39;est pas valide, comme Utilisateur inconnu.

* **[!UICONTROL Soft bounces]** : nombre total d&#39;erreurs temporaires, telles qu&#39;une boîte de réception pleine.

* **[!UICONTROL Ignorées]** : nombre total d&#39;erreurs temporaires (par exemple, Absent(e) du bureau) ou techniques (par exemple, si le type d&#39;expéditeur est administrateur).

La variable **[!UICONTROL Raisons de l’erreur]** et **[!UICONTROL Exclure les raisons]** les graphiques et les tableaux vous permettent de voir quelles erreurs et exclusions se sont produites au cours du processus d’envoi.

Le graphique et le tableau **[!UICONTROL Email - Meilleur domaine destinataire]** indiquent les domaines les plus utilisés par les destinataires pour ouvrir l&#39;email.
+++

## Onglet In-app {#inapp-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="Performances in-app"
>abstract="Les indicateurs de performance clés des performances in-app fournissent des informations essentielles sur l’engagement des visiteurs avec les messages in-app au cours des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="Interactions par type"
>abstract="Les interactions par type de graphiques et de tableau détaillent la manière dont les utilisateurs ont interagi avec votre message in-app en suivant les clics, les rejets ou les interactions des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="Résumé in-app"
>abstract="Le graphique de synthèse in-app illustre la progression de vos impressions et interactions in-app au cours des 24 dernières heures."

Depuis votre campagne **[!UICONTROL Rapport en direct]**, la variable **[!UICONTROL In-app]** Cet onglet présente les informations principales relatives aux messages In-App envoyés dans votre campagne.

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport in-app.

Les KPI **[!UICONTROL Performances in-app]** détaillent les informations principales relatives à l’engagement des visiteurs et visiteuses en lien avec vos messages in-app. Cela concerne notamment les éléments suivants :

* **[!UICONTROL Impressions]**: nombre total de messages In-App envoyés à tous les utilisateurs.

* **[!UICONTROL Interactions]** : nombre total d’engagements en lien avec votre message in-app. Cela inclut toutes les actions entreprises par les personnes, telles que les clics, les rejets ou toute autre interaction.

Le graphe **[!UICONTROL Résumé in-app]** présente l’évolution de vos impressions et interactions in-app pour la période concernée.

Les graphes et le tableau **[!UICONTROL Interactions par type]** détaillent la manière dont les personnes ont interagi avec votre message in-app en suivant les clics, les rejets ou les interactions.

+++

## Onglet Notification push {#push-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="Notification push - Envoi des performances"
>abstract="Le graphique Performance d’envoi de notifications push résume les données essentielles relatives à votre notification push, telles que les erreurs ou les messages délivrés au cours des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="Notification push - Statistiques"
>abstract="Le tableau Statistiques push fournit des données sur l&#39;activité des destinataires pour votre notification push depuis les dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="Notification push - Synthèse des envois"
>abstract="Le graphique Résumé de l’envoi des notifications push affiche les données disponibles pour les notifications push envoyées des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="Notification push - Raisons exclues"
>abstract="Les graphiques et tableaux Exclus des motifs illustrent les différents facteurs qui ont conduit à des profils d’utilisateurs, exclus de l’audience ciblée, et qui n’ont pas reçu le message au cours des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="Notification push - Raisons de l&#39;erreur"
>abstract="Les graphiques et tableaux Raisons d’erreur vous permettent d’identifier les erreurs spécifiques qui se sont produites au cours des dernières 24 heures du processus d’envoi."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="Notification push - Répartition par plateforme"
>abstract="Le tableau et les graphiques Ventilation par plateforme fournissent une répartition du succès de vos notifications push au cours des dernières 24 heures en fonction du système d’exploitation du destinataire."

Depuis votre campagne **[!UICONTROL Rapport en direct]**, la variable **[!UICONTROL Notification push]** Cet onglet présente les informations principales relatives à la notification push envoyée dans votre campagne.

![](assets/campaign_report_live_2.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport push.

**[!UICONTROL Performances d&#39;envoi des notifications push]**, **[!UICONTROL Synthèse des notifications push]** et **[!UICONTROL Notification push - Statistiques]** Les widgets détaillent les informations principales relatives à votre message :

* **[!UICONTROL Envoyés]** : nombre total d’e-mails envoyés.

* **[!UICONTROL Livrés]** : nombre de messages envoyés avec succès.

* **[!UICONTROL Rebonds]**: Nombre total d&#39;erreurs cumulées lors du processus d&#39;envoi et du traitement automatique des retours.

* **[!UICONTROL Erreurs]**: nombre total d&#39;erreurs qui se sont produites pendant le processus d&#39;envoi et qui l&#39;ont empêché d&#39;être envoyé aux profils.

* **[!UICONTROL Ouvertures]**: nombre d’ouvertures d’un message.

* **[!UICONTROL Actions]** : nombre total d&#39;actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

* **[!UICONTROL Engagements]** : nombre total d&#39;ouvertures et d&#39;actions pour cette notification push, c&#39;est-à-dire si le profil a ouvert la notification ou si un utilisateur a cliqué sur un bouton.

La variable **[!UICONTROL Raisons de l’erreur]** et **[!UICONTROL Exclure les raisons]** les graphiques et les tableaux vous permettent de voir quelles erreurs et exclusions se sont produites au cours du processus d’envoi .

Le widget **[!UICONTROL Statistiques d’envoi - Échec]** vous permet de voir combien d’erreurs et de bounces se sont produits.

Les graphiques et tableaux **[!UICONTROL Suivi par plateforme]**, **[!UICONTROL Envoi par plateforme]** et **[!UICONTROL Répartition par plateforme]** décrivent le succès de votre notification push en fonction du système opérationnel.
+++

## Onglet SMS {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="SMS - Statistiques"
>abstract="Le tableau Statistiques d’envoi de SMS récapitule les données essentielles relatives à vos messages SMS, telles que les messages ciblés ou délivrés au cours des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="SMS : performance par date"
>abstract="Le widget Performances des SMS par date fournit des informations clés des dernières 24 heures sur vos messages par le biais d’une représentation graphique."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="SMS - Raisons de l’erreur"
>abstract="Les graphiques et tableaux SMS - Raisons d’erreur vous permettent d’identifier les erreurs spécifiques qui se sont produites au cours des dernières 24 heures pendant le processus d’envoi."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="SMS - Motifs exclus"
>abstract="Les graphiques et tableaux Exclus des motifs illustrent les différents facteurs qui ont conduit à des profils d’utilisateurs, exclus de l’audience ciblée, et qui n’ont pas reçu le message au cours des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="SMS - Raisons des rebonds"
>abstract="Les graphiques et les tableaux Rebonds contiennent les données disponibles depuis les dernières 24 heures relatives aux messages rebonds."

Depuis votre campagne **[!UICONTROL Rapport en direct]**, la variable **[!UICONTROL SMS]** Cet onglet présente les informations principales relatives au SMS envoyé dans votre campagne.

![](assets/campaign_report_live_3.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport SMS.

La variable **[!UICONTROL SMS - Statistiques]** Le tableau décrit le succès de votre SMS :

* **[!UICONTROL Ciblés]**: nombre de profils utilisateur qualifiés comme profils cibles.

* **[!UICONTROL Exclus]** : nombre de profils utilisateur, exclus des profils ciblés, qui n’ont pas reçu le message.

* **[!UICONTROL Envoyés]** : nombre total d’e-mails envoyés.

* **[!UICONTROL Rebonds]**: Nombre total d&#39;erreurs cumulées lors du processus d&#39;envoi et du traitement automatique des retours.

* **[!UICONTROL Erreurs]**: nombre total d&#39;erreurs qui se sont produites pendant le processus d&#39;envoi et qui l&#39;ont empêché d&#39;être envoyé aux profils.

* **[!UICONTROL Clics]** : nombre total de visites d’URL.

Le widget **[!UICONTROL Performances de SMS par date]** détaille les informations principales relatives à votre message sous forme de graphique :

* **[!UICONTROL Envoyés]** : nombre total d’e-mails envoyés.

* **[!UICONTROL Rebonds]**: Nombre total d&#39;erreurs cumulées lors du processus d&#39;envoi et du traitement automatique des retours.

* **[!UICONTROL Erreurs]**: nombre total d&#39;erreurs qui se sont produites pendant le processus d&#39;envoi et qui l&#39;ont empêché d&#39;être envoyé aux profils.

La variable **[!UICONTROL Exclure les raisons]**, **[!UICONTROL Raisons des rebonds]** et **[!UICONTROL Raisons de l’erreur]** les graphiques et les tableaux vous permettent de voir quelles erreurs et exclusions se sont produites au cours du processus d’envoi.
+++

## Onglet Web {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="Performances web"
>abstract="Les IPC de performances web fournissent des informations complètes sur l’engagement de vos visiteurs avec vos expériences web au cours des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="Résumé web"
>abstract="Le graphique Résumé web illustre la progression de vos expériences web, y compris les impressions, les impressions uniques et les interactions, depuis les dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="Interactions par élément"
>abstract="Le tableau Interactions par élément fournit des informations clés sur l’engagement de vos visiteurs avec différents éléments de vos pages web au cours des dernières 24 heures."

Dans votre **[!UICONTROL rapport dynamique]** Campaign, l’onglet **[!UICONTROL Web]** présente les informations principales relatives à vos pages web.

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport web.

Les KPI de **[!UICONTROL Performances web]** détaillent les informations principales relatives à l’engagement de vos visiteurs et visiteuses avec vos expériences web, telles que :

* **[!UICONTROL Impressions]** : nombre total d’expériences web diffusées à tous les utilisateurs et utilisatrices.

* **[!UICONTROL Interactions]** : nombre total d’engagements en lien avec votre page web. Cela inclut toutes les actions entreprises par les personnes, telles que les clics ou toute autre interaction.

Le graphe **[!UICONTROL Résumé web]** présente l’évolution de vos expériences web (impressions, impressions et interactions uniques) pour les dernières 24 heures.

Le tableau **[!UICONTROL Interactions par élément]** présente les informations principales relatives à l’engagement des visiteurs et visiteuses en lien avec les différents éléments de vos pages web.
+++

## Onglet Courrier {#direct-mail-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="Courrier - Statistiques d’envoi"
>abstract="Le tableau Statistiques d’envoi de courrier récapitule les données essentielles des dernières 24 heures relatives à vos messages de courrier, telles que les messages ciblés ou délivrés."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="Courrier - Raisons de l’erreur"
>abstract="Le tableau Courrier - Raisons d’erreur vous permet d’identifier les erreurs spécifiques qui se sont produites au cours des dernières 24 heures."

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="Courrier - Motifs exclus"
>abstract="Le tableau et les graphiques des motifs d’exclusion du courrier illustrent les différents facteurs qui ont conduit aux profils utilisateur, exclus de l’audience ciblée, et qui n’ont pas reçu le message au cours des dernières 24 heures."

Depuis votre campagne **[!UICONTROL Rapport en direct]**, la variable **[!UICONTROL Canal Courrier]** Cet onglet présente les informations principales relatives à votre courrier.

![](assets/direct-mail-report_2.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport de courrier.

La variable **[!UICONTROL Courrier - Statistiques d’envoi]** Le tableau décrit le succès de votre canal Courrier :

* **[!UICONTROL Ciblés]**: nombre de profils utilisateur qualifiés comme profils cibles.

* **[!UICONTROL Envoyés]** : nombre total d’e-mails envoyés.

* **[!UICONTROL Erreurs]**: nombre total d&#39;erreurs qui se sont produites pendant le processus d&#39;envoi et qui l&#39;ont empêché d&#39;être envoyé aux profils.

* **[!UICONTROL Exclu]**: nombre de profils utilisateur, exclus des profils ciblés, qui n’ont pas reçu votre courrier.

La variable **[!UICONTROL Courrier - Motifs exclus]** et **[!UICONTROL Courrier - Raisons de l’erreur]** les graphiques et les tableaux vous permettent de voir quelles erreurs et exclusions se sont produites au cours du processus d’envoi.
+++

## Ressources supplémentaires

* [Prise en main des campagnes](../campaigns/get-started-with-campaigns.md)
* [Création d’une campagne](../campaigns/create-campaign.md)
* [Créer des campagnes déclenchées par API](../campaigns/api-triggered-campaigns.md)
* [Modification ou arrêt d’une campagne](../campaigns/modify-stop-campaign.md)
* [Rapport global de campagne](campaign-global-report.md)
