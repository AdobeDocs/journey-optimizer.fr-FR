---
solution: Journey Optimizer
product: journey optimizer
title: Rapport global de campagne
description: Découvrez comment utiliser les données du rapport global de campagne
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: c9941a800783b399b587b952c4191ce906b70552
workflow-type: tm+mt
source-wordcount: '2262'
ht-degree: 100%

---

# Rapport global de campagne {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Rapport global de campagne"
>abstract="Le rapport global de campagne permet de mesurer l’efficacité de vos campagnes au cours d’une période donnée. Le rapport dyamique de campagne est composé de plusieurs widgets présentant le succès et les erreurs de votre campagne. Vous pouvez modifier chaque tableau de bord de reporting en redimensionnant ou en supprimant des widgets."

Pour accéder directement au rapport global de campagne à partir de votre campagne, cliquez sur le bouton **[!UICONTROL Afficher le rapport]**.

![](assets/campaign_report_global_5.png)

La page **[!UICONTROL Rapport global]** de la campagne s&#39;affiche avec les onglets suivants :

* [Campagne](#campaign-global)
* [E-mail](#email-global)
* [In-app](#inapp-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [Web](#web-tab)

Le **[!UICONTROL Rapport global]** de campagne est divisé en différents widgets présentant le succès et les erreurs de votre campagne. Chaque widget peut être redimensionné et supprimé si nécessaire. Pour plus d&#39;informations à ce propos, consultez cette [section](../reports/global-report.md#modify-dashboard).

Pour obtenir la liste détaillée de chaque mesure disponible dans Adobe Journey Optimizer, reportez-vous à [cette page](global-report.md#list-of-components-global.md).

## Onglet Campagne {#campaign-global}

### Diffusion {#delivery-global}

![](assets/campaign_report_global_1.png)

Le widget **[!UICONTROL Statistiques de la campagne]** présente les principales informations relatives à votre Campagne :

* **[!UICONTROL Profils entrés]** : nombre de profils ayant commencé le parcours.

* **[!UICONTROL Actions réalisées]** : nombre total de fois uniques où une action dans le parcours a été réalisée.

* **[!UICONTROL Échec des actions en %]** : nombre total de fois uniques où une action a échoué dans le parcours par rapport au nombre total de fois uniques où une action a été réalisée.

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../campaigns/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.
-->

### Rapport d’expérience {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Mesure de succès"
>abstract="Valeur totale de la mesure de succès, précédemment sélectionnée lors de la création de vos expériences, divisée par le nombre de profils."

![](assets/experimentation_report_3.png)

L’onglet **[!UICONTROL Expérimentation]** fournit des informations clés sur les performances de chaque variante et identifie la variante la plus réussie.

Notez que la définition de meilleure performance peut prendre un certain temps, elle sera représentée par cette icône ![](assets/experimentation_report_1.png).

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport d’expérience.

Le widget **[!UICONTROL Résultat de l’expérience]** décrit les performances de chaque variante. Vous pouvez modifier votre ligne de base en sélectionnant l’un des traitements du menu déroulant **[!UICONTROL Ligne de base]**. Le meilleur traitement sera signalé par une icône en forme d’étoile.

Le tableau présente les mesures suivantes :

* **[!UICONTROL Élévation de la ligne de base]** : mesure de l’amélioration en pourcentage du taux de conversion d’un traitement donné par rapport à la ligne de base.

* **[!UICONTROL Confiance]** : preuves qu’un traitement donné est le même que le traitement de la ligne de base. [En savoir plus](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Clics sortants uniques]** : nombre total de clics sur les canaux sortants.

* **[!UICONTROL Profils]** : nombre de profils ciblés pour ce traitement.

* **[!UICONTROL Clips sortants uniques/profils]** : valeur totale de la mesure de succès, précédemment sélectionnée lors de la création de vos expériences, divisée par le nombre de profils.

Le graphe **[!UICONTROL Intervalle de confiance]** mesure l’incertitude quant à l’amélioration. Il indique la différence de performance en pourcentage entre la ligne de base et le traitement le plus performant. [En savoir plus](../campaigns/experiment-calculations.md#confidence-intervals).
+++

Pour un examen approfondi de ces résultats et de leur interprétation, reportez-vous à [cette page](../campaigns/get-started-experiment.md#interpret-results).

## Onglet E-mail {#email-global}

![](assets/campaign_report_global_2.png)

Dans le **[!UICONTROL Rapport global]** de campagne, l&#39;onglet **[!UICONTROL E-mail]** détaille les principales informations relatives aux diffusions par e-mail envoyées dans votre campagne.

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport d’e-mail.

Le graphique **[!UICONTROL Statistiques d&#39;envoi d’e-mail]** détaille la réussite de votre diffusion :

* **[!UICONTROL Ciblés]** : nombre total de messages traités lors de l’analyse de la diffusion.

* **[!UICONTROL Envoyés]** : nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux de diffusion]** : pourcentage de messages envoyés avec succès.

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux de rebond]** : pourcentage d&#39;e-mails ayant rebondi par rapport aux e-mails envoyés.

* **[!UICONTROL Erreurs]** : nombre total d&#39;erreurs survenues au cours d&#39;une diffusion, l&#39;empêchant d&#39;être envoyée à des profils.

* **[!UICONTROL Taux d&#39;erreurs]** : pourcentage d&#39;erreurs survenues au cours d&#39;une diffusion, l&#39;empêchant d&#39;être envoyée, par rapport aux e-mails envoyés.

* **[!UICONTROL Reprises]** : nombre d’e-mails dans la file d’attente pour les reprises.

* **[!UICONTROL Exclus]** : nombre de profils qui ont été exclus par Adobe Journey Optimizer.

Le widget **[!UICONTROL E-mail - Statistiques de suivi]** contient les données disponibles pour l’activité destinataire de votre diffusion :

* **[!UICONTROL Ouvertures]** :nombre de fois où la diffusion a été ouverte dans une diffusion.

* **[!UICONTROL Ouvertures uniques]** : pourcentage de diffusions ouvertes.

* **[!UICONTROL Taux d&#39;ouvertures]** : nombre total de messages ouverts par rapport au nombre de messages diffusés.

* **[!UICONTROL Clics]** : nombre de fois où un contenu a fait l&#39;objet d&#39;un clic dans un e-mail.

* **[!UICONTROL Clics uniques]** : nombre de destinataires qui ont cliqué sur un contenu dans un email.

* **[!UICONTROL Taux de clics uniques]** : pourcentage d’utilisateurs ayant interagi avec la diffusion.

* **[!UICONTROL Désabonnements]** : nombre de clics sur le lien de désabonnement.

* **[!UICONTROL Plaintes contre le spam]** : nombre de fois où un message a été déclaré comme spam ou courrier indésirable.

Le graphique **[!UICONTROL Statistiques d&#39;envoi]** contient les données disponibles pour les e-mails envoyés, telles que :

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Reprises]** : nombre d’e-mails dans la file d’attente pour les reprises.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.

Les widgets **[!UICONTROL Raisons de rebond]** et **[!UICONTROL Catégories de rebond]** contiennent les données disponibles relatives aux messages de rebond, telles que :

* **[!UICONTROL Hard bounce]** : nombre total d&#39;erreurs permanentes, telles qu&#39;une adresse email incorrecte. Un message d&#39;erreur indique explicitement que l&#39;adresse n&#39;est pas valide, comme Utilisateur inconnu.

* **[!UICONTROL Soft bounces]** : nombre total d&#39;erreurs temporaires, telles qu&#39;une boîte de réception pleine.

* **[!UICONTROL Ignorées]** : nombre total d&#39;erreurs temporaires (par exemple, Absent(e) du bureau) ou techniques (par exemple, si le type d&#39;expéditeur est administrateur).

Pour plus d&#39;informations sur les bounces, consultez la page [Liste de suppression](../reports/suppression-list.md).

Le graphique et le tableau **[!UICONTROL Causes des erreurs]** vous permettent de voir quelle erreur s&#39;est produite au cours de votre diffusion.

Le graphique et le tableau **[!UICONTROL Exclure des raisons]** affichent les différentes raisons qui ont empêché les profils utilisateur, à part les profils ciblés, de recevoir le message.

Le graphique et le tableau **[!UICONTROL E-mail - Principales URL]** indiquent les URL de votre diffusion les plus visitées.

Le graphique et le tableau **[!UICONTROL E-mail - Meilleur domaine destinataire]** indiquent les domaines les plus utilisés par les destinataires pour ouvrir l&#39;e-mail.

>[!NOTE]
>
>Les widgets **[!UICONTROL Optimisé ou non optimisé]** et **[!UICONTROL Optimisation de l’heure d’envoi]** ne sont disponibles que si l’option Optimisation de l’heure d’envoi est activée pour votre diffusion. Pour plus d’informations sur l’optimisation de l’heure d’envoi, consultez [cette page](../building-journeys/journeys-message.md#send-time-optimization).

Le graphique **[!UICONTROL Optimisé ou non optimisé]** détaille les informations principales relatives à votre message, qu’elles soient optimisées ou non :

* **[!UICONTROL Envoyés]** : nombre total d’envois pour la diffusion.
* **[!UICONTROL Ouvertures]** : nombre de fois où la diffusion a été ouverte dans une diffusion.
* **[!UICONTROL Clics]** : nombre de fois où un contenu a fait l’objet d’un clic dans un e-mail.

L’**[!UICONTROL Optimisation de l’heure d’envoi]** détaille le succès de votre diffusion selon la méthode d’envoi : optimisé ou normal.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.
* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.
+++

## Onglet in-app {#inapp-global}

Dans le **[!UICONTROL Rapport global]** de campagne, l’onglet **[!UICONTROL In-app]** détaille les principales informations relatives aux diffusions in-app envoyées dans votre campagne.

![](assets/campaign_report_global_6.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport in-app.

Les KPI **[!UICONTROL Performances in-app]** détaillent les informations principales relatives à l’engagement des visiteurs avec vos messages in-app, telles que :

* **[!UICONTROL Impressions uniques]** : nombre d’utilisateurs uniques auxquels le message in-app a été délivré.

* **[!UICONTROL Impressions]** : nombre total de messages in-app diffusés à tous les utilisateurs.

* **[!UICONTROL Taux de clics]** : pourcentage d&#39;utilisateurs ayant interagi avec les boutons inclus dans le message in-app par rapport au nombre d’utilisateurs ayant vu le message.

* **[!UICONTROL Taux d’ignorance]** : pourcentage de messages in-app ignorés par les destinataires.

Le graphique du **[!UICONTROL Résumé in-app]** présente l’évolution de vos impressions in-app pour la période concernée.

Le graphique et le tableau **[!UICONTROL Clics par bouton]** contiennent les données disponibles pour le comportement des destinataires par bouton :

* **[!UICONTROL Clics]** : nombre total de destinataires ayant interagi avec les boutons inclus dans le message in-app.

* **[!UICONTROL Taux de clics]** : pourcentage d’utilisateurs ayant interagi avec les boutons inclus dans le message in-app par rapport au nombre d’utilisateurs ayant vu le message.
+++

## Onglet Notification push {#push-global}

Dans le **[!UICONTROL Rapport global]** de campagne, l’onglet **[!UICONTROL Notification push]** détaille les principales informations relatives aux diffusions push envoyées dans votre campagne.

![](assets/campaign_report_global_3.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport push.

Le tableau **[!UICONTROL Notification push - Statistiques d&#39;envoi]** présente les principales informations relatives à vos notifications push avec un graphique et des KPI :

* **[!UICONTROL Ciblés]** : nombre total de messages traités lors de l’analyse de la diffusion.

* **[!UICONTROL Envoyés]** : nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux de diffusion]** : pourcentage de messages envoyés avec succès.

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux de rebond]** : pourcentage de notifications push ayant rebondi par rapport aux notifications push envoyées.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.

* **[!UICONTROL Taux d&#39;erreurs]** : pourcentage d&#39;erreurs survenues pendant une diffusion qui l&#39;empêchent d&#39;être envoyée par rapport aux notifications push envoyées.

* **[!UICONTROL Exclus]** : nombre de profils qui ont été exclus par Adobe Journey Optimizer.

Les **[!UICONTROL Statistiques de suivi - push]** contiennent les données disponibles pour l&#39;activité destinataire de votre diffusion :

* **[!UICONTROL Ouvertures]** : nombre de fois qu&#39;un message a été ouvert dans une diffusion.

* **[!UICONTROL Taux d&#39;ouverture]** : pourcentage de notifications push ouvertes.

* **[!UICONTROL Actions]** : nombre total d&#39;actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

* **[!UICONTROL Engagements]** : nombre total d&#39;ouvertures et d&#39;actions pour cette notification push, c&#39;est-à-dire si le profil a ouvert la notification ou si un utilisateur a cliqué sur un bouton.

* **[!UICONTROL Taux d&#39;engagement]** : pourcentage d&#39;ouvertures et d&#39;actions pour cette notification push, c&#39;est-à-dire si le profil a ouvert la notification push ou si un utilisateur a cliqué sur un bouton.

Le graphique **[!UICONTROL Résumé des notifications push]** contient les données disponibles pour les notifications push envoyées, telles que :

* **[!UICONTROL Ouvertures]** : nombre d’ouvertures d’un message dans une diffusion.

* **[!UICONTROL Actions]** : nombre total d’actions sur la notification push diffusée (par exemple, clic sur un bouton ou rejet).

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.

>[!NOTE]
>
>Les widgets **[!UICONTROL Optimisé ou non optimisé]** et **[!UICONTROL Optimisation de l’heure d’envoi]** ne sont disponibles que si l’option Optimisation de l’heure d’envoi est activée pour votre diffusion. Pour plus d’informations sur l’optimisation de l’heure d’envoi, consultez [cette page](../building-journeys/journeys-message.md#send-time-optimization).

Le graphique **[!UICONTROL Optimisé ou non optimisé]** détaille les informations principales relatives à votre message, qu’elles soient optimisées ou non :

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.
* **[!UICONTROL Ouvertures]** :nombre de fois où la diffusion a été ouverte dans une diffusion.
* **[!UICONTROL Actions]** : nombre total d’actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

L’**[!UICONTROL Optimisation de l’heure d’envoi]** détaille le succès de votre diffusion selon la méthode d’envoi : optimisé ou normal.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.
* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

Le graphique et le tableau **[!UICONTROL Causes des erreurs]** vous permettent de voir quelle erreur s&#39;est produite au cours de votre diffusion.

Le graphique et le tableau **[!UICONTROL Exclure des raisons]** affichent les différentes raisons qui ont empêché les profils utilisateur, à part les profils ciblés, de recevoir le message.

Les graphiques et tableaux **[!UICONTROL Suivi par plateforme]**, **[!UICONTROL Envoi par plateforme]** et **[!UICONTROL Répartition par plateforme]** décrivent le succès de votre notification push en fonction du système d&#39;exploitation de votre destinataire.
+++

## Onglet SMS {#sms-global}

Dans le **[!UICONTROL Rapport global]** de campagne, l’onglet **[!UICONTROL SMS]** détaille les principales informations relatives aux diffusions SMS envoyées dans votre campagne.

![](assets/campaign_report_global_4.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport SMS.

Le tableau **[!UICONTROL SMS - Statistiques d’envoi]** détaille la réussite de votre diffusion :

* **[!UICONTROL Ciblés]** : nombre de profils utilisateur qui sont qualifiés en tant que profils cibles pour cette diffusion.

* **[!UICONTROL Exclus]** : nombre de profils utilisateur, exclus des profils ciblés, qui n’ont pas reçu le message.

* **[!UICONTROL Envoyés]** : nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours d&#39;une diffusion, l’empêchant d&#39;être envoyée à des profils.

Le widget **[!UICONTROL Performances de SMS par date]** détaille les informations principales relatives à votre message sous forme de graphique :

* **[!UICONTROL Envoyés]** : nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours d&#39;une diffusion, l’empêchant d&#39;être envoyée à des profils.

Les graphiques et tableaux **[!UICONTROL Motifs d’exclusion]**, **[!UICONTROL Causes des bounces]** et **[!UICONTROL Raisons des erreurs]** vous permettent de voir quelles erreurs et exclusions ont eu lieu au cours de votre diffusion.

Les widgets **[!UICONTROL SMS - Clics par liens]** et **[!UICONTROL SMS - Statistiques de tracking]** affichent les principales informations relatives à l’engagement des visiteurs et des visiteuses sur vos URL.

+++

## Onglet Web {#web-tab}

Depuis votre **[!UICONTROL rapport global]** de campagne, l’onglet **[!UICONTROL Web]** présente les informations principales relatives à vos pages web.

![](assets/web-report.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport web.

Les KPI de **[!UICONTROL Performances web]** détaillent les informations principales relatives à l’engagement de vos visiteurs avec vos expériences web, telles que :

* **[!UICONTROL Impressions uniques]** : nombre d’utilisateurs uniques auxquels l’expérience web a été diffusée.

* **[!UICONTROL Impressions]** : nombre total d’expériences web diffusées à tous les utilisateurs.

* **[!UICONTROL Taux de clics]** : pourcentage des visiteurs et visiteuses qui ont interagi avec les différents éléments de vos pages web.

Le graphique **[!UICONTROL Résumé web]** présente l’évolution de vos expériences web (impressions, impressions uniques et clics) pour la période concernée.

Le tableau **[!UICONTROL Clics par élément]** présente les informations principales relatives à l’engagement des visiteurs et visiteuses avec les différents éléments de vos pages web.
+++

## Ressources supplémentaires

* [Prise en main des campagnes](../campaigns/get-started-with-campaigns.md)
* [Création d’une campagne](../campaigns/create-campaign.md)
* [Créer des campagnes déclenchées par API](../campaigns/api-triggered-campaigns.md)
* [Modification ou arrêt d’une campagne](../campaigns/modify-stop-campaign.md)
* [Rapport dynamique de campagne](campaign-live-report.md)
