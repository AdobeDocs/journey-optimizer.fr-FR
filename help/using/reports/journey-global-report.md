---
title: Rapport global parcours
description: Découvrez comment utiliser les données du rapport global parcours
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 5%

---

# Rapport global parcours {#journey-global-report}

![](../assets/do-not-localize/badge.png)

Vous pouvez accéder directement au rapport parcours global à partir de votre parcours à l&#39;aide du bouton **[!UICONTROL Rapport global]**.

![](../assets/global_report_1.png)

La page **[!UICONTROL Rapport global]** du parcours s’affiche avec les onglets suivants :

* [Parcours](#journey-global)
* [E-mail](#email-global)
* [Push](#push-global)

Le rapport **[!UICONTROL global]** parcours est divisé en différents widgets détaillant la réussite et les erreurs de votre parcours. Chaque widget peut être redimensionné et supprimé si nécessaire. Pour plus d&#39;informations à ce sujet, consultez cette [section](global-report.md#modify-dashboard).

## Onglet parcours {#journey-global}

À partir de votre parcours **[!UICONTROL rapport global]**, l&#39;onglet **[!UICONTROL Parcours]** vous donne une vue claire des données de suivi les plus importantes concernant votre parcours.

![](../assets/global_report_2.png)

Le widget **[!UICONTROL performances du Parcours]** vous permet de voir le chemin de vos profils ciblés pas à pas dans votre parcours.

Le widget **[!UICONTROL statistiques du Parcours]** affiche les IPC suivants :

* **[!UICONTROL Profils]** entrés : Nombre total de personnes ayant atteint le événement d&#39;entrée du parcours.

* **[!UICONTROL Profils]** de sortie : Nombre total de personnes ayant quitté le parcours.

* **[!UICONTROL Parcours]** individuel en échec : Nombre total de parcours individuels qui n’ont pas été exécutés avec succès.

Les widgets **[!UICONTROL Performances du Événement]** et **[!UICONTROL Principaux événements]** vous permettent de savoir lequel de vos **[!UICONTROL Événements]** a été exécuté avec succès par le biais de graphiques et de tableaux.

**[!UICONTROL Les]** performances de l’action et les  **[!UICONTROL principales actions représentent l’action et les erreurs les plus réussies survenues lorsque vos]**   **** actions ont été déclenchées. Le tableau **[!UICONTROL Principales actions]** contient les données disponibles pour **[!UICONTROL Actions]**, telles que :

* **[!UICONTROL Actions exécutées]** avec succès : Nombre total d’ **** actions exécutées avec succès pour un parcours.

* **[!UICONTROL Erreur lors de l&#39;action]** : Nombre total d&#39;erreurs survenues pour  **[!UICONTROL les actions]**.

Le graphique **[!UICONTROL Raisons de l&#39;erreur]** détaille le type d&#39;erreurs survenues pour **[!UICONTROL Actions]**.

<!--Events by origin-->

## Onglet Courriel {#email-global}

À partir de votre parcours **[!UICONTROL Rapport global]**, l&#39;onglet **[!UICONTROL E-mail]** détaille les principales informations relatives aux diffusions de courriel envoyées dans votre parcours.

Pour obtenir un rapport détaillé sur une diffusion de courriel spécifique, consultez la section [Envoyer le rapport global par courriel](#email-global-report).

Le graphique **[!UICONTROL Statistiques d&#39;envoi de courriel]** détaille la réussite de votre diffusion :

* **[!UICONTROL Envoyé]** : Nombre total d’envois pour la diffusion.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux]** de diffusion : Pourcentage de messages envoyés avec succès.

* **[!UICONTROL Rebonds]** : Nombre total d&#39;erreurs cumulées pendant la diffusion et le traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux]** de rebonds : Pourcentage de courriers électroniques ayant rebondi par rapport aux courriers électroniques envoyés.

* **[!UICONTROL Erreurs]** : Nombre total d’erreurs survenues au cours d’une diffusion qui l’empêchait d’être envoyée aux profils.

* **[!UICONTROL Taux]** d’erreurs : Pourcentage d’erreurs survenues au cours d’une diffusion qui l’empêchaient d’être envoyées par rapport aux courriers électroniques envoyés.

**[!UICONTROL E-mail - Statistiques de suivi]** contient les données disponibles pour l&#39;activité destinataire de votre diffusion :

* **[!UICONTROL Ouvre]** : Nombre de fois où la diffusion a été ouverte dans une diffusion.

* **[!UICONTROL Ouverture]** unique : Pourcentage de diffusions ouvertes.

* **[!UICONTROL Taux]** d&#39;ouverture : Nombre total de courriers électroniques ouverts par rapport au nombre de courriers électroniques distribués.

* **[!UICONTROL Clics]** : Nombre de fois où un contenu a été cliqué dans un courrier électronique.

* **[!UICONTROL Clics]** uniques : nombre de destinataires qui ont cliqué sur un contenu d’un courrier électronique.

* **[!UICONTROL Taux]** de clics publicitaires : Pourcentage d’utilisateurs qui ont interagi avec le parcours.

Le graphique **[!UICONTROL Statistiques d&#39;envoi]** contient les données disponibles pour les courriers électroniques envoyés, telles que :

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Rebonds]** : Nombre total d&#39;erreurs cumulées pendant la diffusion et le traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs]** : Nombre total d’erreurs survenues au cours d’une diffusion qui l’empêchait d’être envoyée aux profils.

Les widgets **[!UICONTROL Raisons de rebond]** et **[!UICONTROL catégories de rebond]** contiennent les données disponibles relatives aux messages rebonds, telles que :

* **[!UICONTROL Rebond]** dur : Nombre total d’erreurs permanentes, telles qu’une adresse électronique incorrecte. Ceci implique un message d’erreur qui indique explicitement que l’adresse n’est pas valide, tel qu’Utilisateur inconnu.

* **[!UICONTROL Rebond]** léger : Nombre total d’erreurs temporaires, par exemple une boîte de réception complète.

* **[!UICONTROL Ignoré]** : Nombre total de données temporaires, telles que Absence du bureau, ou d’une erreur technique, par exemple si le type d’expéditeur est Postmaster.

Pour plus d&#39;informations sur les rebonds, consultez la [page Gérer les listes de suppression](../suppression-lists.md).

Le graphique **[!UICONTROL E-mail - URL supérieure]** et le tableau indiquent les URL de votre diffusion les plus visitées.

Le graphique **[!UICONTROL E-mail - Domaine du meilleur destinataire]** et la table indiquent les domaines les plus utilisés par les destinataires pour ouvrir le courriel.

## Onglet Push {#push-global}

Dans le rapport **[!UICONTROL global]** de votre parcours, l&#39;onglet **[!UICONTROL Push]** détaille les informations principales par rapport aux diffusions Push envoyées dans votre parcours.

Pour obtenir un rapport détaillé sur une diffusion Push spécifique, reportez-vous à ce rapport [Push Global report](#push-global-report).

Le tableau **[!UICONTROL Notification Push - Envoi de statistiques]** détaille les principales informations relatives à vos notifications Push avec graphique et IPC :

* **[!UICONTROL Envoyé]** : Nombre total d’envois pour la diffusion.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux]** de diffusion : Pourcentage de messages envoyés avec succès.

* **[!UICONTROL Rebonds]** : Nombre total d&#39;erreurs cumulées pendant la diffusion et le traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Taux]** de rebonds : Pourcentage de notifications Push ayant rebondi par rapport aux notifications Push envoyées.

* **[!UICONTROL Erreurs]** : Nombre total d’erreurs survenues au cours d’une diffusion qui l’empêchait d’être envoyée aux profils.

* **[!UICONTROL Taux]** d’erreurs : Pourcentage d’erreurs survenues pendant une diffusion qui l’empêchaient d’être envoyée par rapport aux notifications Push envoyées.

Les **[!UICONTROL statistiques Push - Tracking]** contiennent les données disponibles pour l&#39;activité destinataire de votre diffusion :

* **[!UICONTROL Ouvre]** : Nombre de fois où un message a été ouvert dans une diffusion.

* **[!UICONTROL Taux]** d&#39;ouverture : Pourcentage de notifications Push ouvertes.

* **[!UICONTROL Actions]** : Nombre total d’actions sur la notification Push envoyée, par exemple clic sur un bouton ou rejet.

* **[!UICONTROL Engagements]** : Nombre total d’ouvertures et d’actions pour cette notification Push, c’est-à-dire si le profil a ouvert la notification ou si un utilisateur a cliqué sur un bouton.

* **[!UICONTROL Taux]** d’engagement : Pourcentage d’ouvertures et d’actions pour cette notification Push, c’est-à-dire si le profil a ouvert la notification Push ou si un utilisateur a cliqué sur un bouton.

Le graphique **[!UICONTROL Résumé des notifications Push]** contient les données disponibles pour les notifications Push envoyées, telles que :

* **[!UICONTROL Ouvre]** : Nombre de fois où un message a été ouvert dans une diffusion.

* **[!UICONTROL Actions]** : Nombre total d’actions sur la notification Push envoyée, par exemple clic sur un bouton ou rejet.

* **[!UICONTROL Rebonds]** : Nombre total d&#39;erreurs cumulées pendant la diffusion et le traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs]** : Nombre total d’erreurs survenues au cours d’une diffusion qui l’empêchait d’être envoyée aux profils.

Le graphique et le tableau **[!UICONTROL Raisons de l&#39;erreur]** vous permettent de voir quelle erreur s&#39;est produite au cours de votre diffusion.

Les graphiques et tableaux **[!UICONTROL Suivi par plate-forme]**, **[!UICONTROL Envoi par plate-forme]** et **[!UICONTROL Ventilation par plate-forme]** décrivent le succès de votre notification Push en fonction du système opérationnel de votre destinataire.
