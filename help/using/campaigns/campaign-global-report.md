---
title: Rapport global de campagnes
description: Découvrez comment utiliser les données du rapport global de Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 0036c905b9344a6f99e8525acbe9caab5932f361
workflow-type: tm+mt
source-wordcount: '1736'
ht-degree: 65%

---

# Rapport global de campagnes {#campaign-global-report}

Le rapport global de campagnes est accessible directement depuis votre campagne à l’aide de la variable **[!UICONTROL Vue globale]** bouton .

La campagne **[!UICONTROL Rapport global]** s’affiche avec les onglets suivants :

* [Campaign](#campaign-global)
* [Email](#email-global)
* [Push](#push-global)

La campagne **[!UICONTROL Rapport global]** est divisé en différents widgets détaillant le succès et les erreurs de votre campagne. Chaque widget peut être redimensionné et supprimé en cas de besoin. Pour plus d&#39;informations à ce propos, consultez cette [section](../reports/global-report.md#modify-dashboard).

## Onglet Campagne {#campaign-global}

### Diffusion {#delivery-global}

![](assets/campaign_report_global_1.png)

Le **[!UICONTROL Statistiques de la campagne]** widget détaille les informations principales relatives à votre campagne :

* **[!UICONTROL Profils entrés]**: Nombre de profils ayant démarré le parcours.

* **[!UICONTROL Actions réalisées]**: Nombre total de fois uniques où une action dans le parcours a été diffusée.

* **[!UICONTROL Les actions ont échoué en %]**: Nombre total de fois uniques où une action a échoué dans le parcours par rapport au nombre total de fois uniques où une action a été diffusée.

### Objectifs (#objectives-global)

>[!AVAILABILITY]
>
>Actuellement, la fonctionnalité d’expérience de contenu n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en savoir plus, contactez votre représentant Adobe.

![](assets/performance_report.gif)

Le **[!UICONTROL Objectifs]** de votre rapport Campagne , qui vous permet d’affiner davantage les rapports de vos diffusions en ciblant une mesure spécifique.

Le **[!UICONTROL Objectifs]** répertoriés sont liés à **[!UICONTROL Jeux de données]** qui définissent une connexion à un système afin de récupérer des informations supplémentaires. Liste des éléments intégrés **[!UICONTROL Objectifs]** est disponible, mais vous pouvez ajouter le vôtre en ajoutant un nouveau **[!UICONTROL Jeu de données]**. Pour la procédure détaillée, consultez cette documentation.

Après avoir sélectionné les objectifs que vous souhaitez cibler, les deux **[!UICONTROL Présentation des performances]** et **[!UICONTROL Objectif de la campagne]** Les widgets fournissent un résumé détaillé des performances de votre diffusion.

Avec le **[!UICONTROL Objectif de la campagne]** vous pouvez également choisir de comparer votre objectif principal à une autre mesure.

Notez que chaque widget peut être redimensionné et supprimé si nécessaire. Pour plus d&#39;informations à ce propos, consultez cette [section](../reports/global-report.md#modify-dashboard).

### Expérimentation (#experimentation-global)

>[!AVAILABILITY]
>
>Actuellement, la fonctionnalité d’expérience de contenu n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en savoir plus, contactez votre représentant Adobe.

![](assets/experimentation_report_3.png)

Depuis votre campagne **[!UICONTROL Rapport global]**, la variable **[!UICONTROL Expérience]** l’onglet détaille les informations principales relatives aux performances de chaque variante et s’il y a un meilleur résultat.

Notez que la définition du meilleur performant peut prendre un certain temps, elle sera représentée par cette icône . ![](assets/experimentation_report_1.png).

Le **[!UICONTROL Résultat de l’expérience]** décrit les performances de chaque variante. Vous pouvez modifier votre ligne de base en sélectionnant l’un des traitements de la **[!UICONTROL Ligne de base]** la liste déroulante. Le meilleur traitement sera représenté par une icône en forme d’étoile.

Le tableau présente les mesures suivantes :

* **[!UICONTROL Profils]**: Nombre de profils ciblés pour ce traitement.

* **[!UICONTROL Clics sortants uniques]**: Nombre total de clics sur les canaux sortants.

* **[!UICONTROL Comptage par profil]**: Valeur totale de la mesure de l’objectif de l’expérience divisée par le nombre de profils.

* **[!UICONTROL Intervalle de confiance]**: Différence en pourcentage de performance entre la ligne de base et le traitement le plus performant. [En savoir plus](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Effet élévateur moyen]**: Pourcentage d’amélioration du taux de conversion d’un traitement donné par rapport à la ligne de base. [En savoir plus](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confiance]**: Preuves qu&#39;un traitement donné est le même que le traitement de base. [En savoir plus](../campaigns/experiment-calculations.md#understand-confidence)

Pour un examen approfondi de ces résultats et de leur interprétation, reportez-vous à la section [cette page](../campaigns/get-started-experiment.md#interpret-results).

## Onglet E-mail {#email-global}

Depuis votre campagne **[!UICONTROL Rapport global]**, la variable **[!UICONTROL Email]** Cet onglet présente les informations principales relatives aux diffusions email envoyées dans votre campagne.

Le graphique **[!UICONTROL Statistiques d&#39;envoi d&#39;e-mail]** détaille la réussite de votre diffusion :

* **[!UICONTROL Ciblés]**: Nombre total de messages traités lors de l&#39;analyse de la diffusion.

* **[!UICONTROL Envoyés]** : nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux de diffusion]** : pourcentage de messages envoyés avec succès.

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux de rebond]** : pourcentage d&#39;e-mails ayant rebondi par rapport aux e-mails envoyés.

* **[!UICONTROL Erreurs]** : nombre total d&#39;erreurs survenues au cours d&#39;une diffusion, l&#39;empêchant d&#39;être envoyée à des profils.

* **[!UICONTROL Taux d&#39;erreurs]** : pourcentage d&#39;erreurs survenues au cours d&#39;une diffusion, l&#39;empêchant d&#39;être envoyée, par rapport aux e-mails envoyés.

* **[!UICONTROL Reprises]**: Nombre de courriers électroniques dans la file d’attente pour les reprises.

* **[!UICONTROL Exclu]**: Nombre de profils qui ont été exclus par Adobe Journey Optimizer.

Le **[!UICONTROL Email - Statistiques de tracking]** Le widget contient les données disponibles pour l’activité des destinataires pour votre diffusion :

* **[!UICONTROL Ouvertures]** :nombre de fois où la diffusion a été ouverte dans une diffusion.

* **[!UICONTROL Ouvertures uniques]** : pourcentage de diffusions ouvertes.

* **[!UICONTROL Taux d&#39;ouvertures]** : nombre total de messages ouverts par rapport au nombre de messages diffusés.

* **[!UICONTROL Clics]** : nombre de fois où un contenu a fait l&#39;objet d&#39;un clic dans un e-mail.

* **[!UICONTROL Clics uniques]** : nombre de destinataires qui ont cliqué sur un contenu dans un email.

* **[!UICONTROL Taux de clics uniques]**: Pourcentage d&#39;utilisateurs ayant interagi avec la diffusion.

* **[!UICONTROL Désabonnements]** : nombre de clics sur le lien de désabonnement.

* **[!UICONTROL Plaintes contre le spal]** : nombre de fois où un message a été déclaré comme spam ou courrier indésirable.

Le graphique **[!UICONTROL Statistiques d&#39;envoi]** contient les données disponibles pour les e-mails envoyés, telles que :

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Reprises]**: Nombre de courriers électroniques dans la file d’attente pour les reprises.

* **[!UICONTROL Erreurs]** : nombre total d&#39;erreurs survenues au cours d&#39;une diffusion, l&#39;empêchant d&#39;être envoyée à des profils.

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
>Les widgets **[!UICONTROL Optimisé ou non optimisé]** et **[!UICONTROL Optimisation de l’heure d’envoi]** ne sont disponibles que si l’option Optimisation de l’heure d’envoi est activée pour votre diffusion. Pour plus d’informations sur l’optimisation du temps d’envoi, reportez-vous à la section [cette page](../messages/send-time-optimization.md).

Le graphique **[!UICONTROL Optimisé ou non optimisé]** détaille les informations principales relatives à votre message, qu’elles soient optimisées ou non :

* **[!UICONTROL Envoyés]** : nombre total d’envois pour la diffusion.
* **[!UICONTROL Ouvertures]** : nombre de fois où la diffusion a été ouverte dans une diffusion.
* **[!UICONTROL Clics]** : nombre de fois où un contenu a fait l’objet d’un clic dans un e-mail.

L’**[!UICONTROL Optimisation de l’heure d’envoi]** détaille le succès de votre diffusion selon la méthode d’envoi : optimisé ou normal.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.
* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

## Onglet Push {#push-global}

Depuis votre campagne **[!UICONTROL Rapport global]**, la variable **[!UICONTROL Push]** Cet onglet présente les informations principales relatives aux diffusions push envoyées dans votre campagne.

Le tableau **[!UICONTROL Notification push - Statistiques d&#39;envoi]** présente les principales informations relatives à vos notifications push avec un graphique et des KPI :

* **[!UICONTROL Ciblés]**: Nombre total de messages traités lors de l&#39;analyse de la diffusion.

* **[!UICONTROL Envoyés]** : nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux de diffusion]** : pourcentage de messages envoyés avec succès.

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux de rebond]** : pourcentage de notifications push ayant rebondi par rapport aux notifications push envoyées.

* **[!UICONTROL Erreurs]** : nombre total d&#39;erreurs survenues au cours d&#39;une diffusion, l&#39;empêchant d&#39;être envoyée à des profils.

* **[!UICONTROL Taux d&#39;erreurs]** : pourcentage d&#39;erreurs survenues pendant une diffusion qui l&#39;empêchent d&#39;être envoyée par rapport aux notifications push envoyées.

* **[!UICONTROL Exclu]**: Nombre de profils qui ont été exclus par Adobe Journey Optimizer.

Les **[!UICONTROL Statistiques de suivi - push]** contiennent les données disponibles pour l&#39;activité destinataire de votre diffusion :

* **[!UICONTROL Ouvertures]** : nombre de fois qu&#39;un message a été ouvert dans une diffusion.

* **[!UICONTROL Taux d&#39;ouverture]** : pourcentage de notifications push ouvertes.

* **[!UICONTROL Actions]** : nombre total d&#39;actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

* **[!UICONTROL Engagements]** : nombre total d&#39;ouvertures et d&#39;actions pour cette notification push, c&#39;est-à-dire si le profil a ouvert la notification ou si un utilisateur a cliqué sur un bouton.

* **[!UICONTROL Taux d&#39;engagement]** : pourcentage d&#39;ouvertures et d&#39;actions pour cette notification push, c&#39;est-à-dire si le profil a ouvert la notification push ou si un utilisateur a cliqué sur un bouton.

Le graphique **[!UICONTROL Résumé des notifications push]** contient les données disponibles pour les notifications push envoyées, telles que :

* **[!UICONTROL Ouvertures]** : nombre de fois qu&#39;un message a été ouvert dans une diffusion.

* **[!UICONTROL Actions]** : nombre total d&#39;actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs]** : nombre total d&#39;erreurs survenues au cours d&#39;une diffusion, l&#39;empêchant d&#39;être envoyée à des profils.

>[!NOTE]
>
>Les widgets **[!UICONTROL Optimisé ou non optimisé]** et **[!UICONTROL Optimisation de l’heure d’envoi]** ne sont disponibles que si l’option Optimisation de l’heure d’envoi est activée pour votre diffusion. Pour plus d’informations sur l’optimisation du temps d’envoi, reportez-vous à la section [cette page](../messages/send-time-optimization.md).

Le graphique **[!UICONTROL Optimisé ou non optimisé]** détaille les informations principales relatives à votre message, qu’elles soient optimisées ou non :

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.
* **[!UICONTROL Ouvertures]** : nombre de fois où la diffusion a été ouverte dans une diffusion.
* **[!UICONTROL Actions]** : nombre total d’actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.

L’**[!UICONTROL Optimisation de l’heure d’envoi]** détaille le succès de votre diffusion selon la méthode d’envoi : optimisé ou normal.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.
* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

Le graphique et le tableau **[!UICONTROL Causes des erreurs]** vous permettent de voir quelle erreur s&#39;est produite au cours de votre diffusion.

Le graphique et le tableau **[!UICONTROL Exclure des raisons]** affichent les différentes raisons qui ont empêché les profils utilisateur, à part les profils ciblés, de recevoir le message.

Les graphiques et tableaux **[!UICONTROL Suivi par plateforme]**, **[!UICONTROL Envoi par plateforme]** et **[!UICONTROL Répartition par plateforme]** décrivent le succès de votre notification push en fonction du système d&#39;exploitation de votre destinataire.

## Ressources supplémentaires

* [Prise en main des campagnes](get-started-with-campaigns.md)
* [Créer une campagne](create-campaign.md)
* [Création de campagnes déclenchées par l’API](api-triggered-campaigns.md)
* [Modifier ou arrêter une campagne](modify-stop-campaign.md)
* [Rapport dynamique de la campagne](campaign-live-report.md)
