---
solution: Journey Optimizer
product: journey optimizer
title: Rapport dynamique sur les parcours
description: Découvrez comment utiliser les données du rapport dynamique sur les parcours
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 9245d6a93aaaa85bee56e2291a53ca7495b6ba9e
workflow-type: tm+mt
source-wordcount: '1344'
ht-degree: 89%

---

# Rapport dynamique sur les parcours {#journey-live-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_live_report"
>title="Rapport dynamique sur les parcours"
>abstract="Le rapport dynamique sur les parcours vous permet de mesurer et de visualiser en temps réel l’efficacité et les performances de vos parcours (limité aux dernières 24 heures). Celui-ci est composé de plusieurs widgets présentant le succès et les erreurs de votre parcours. Vous pouvez modifier chaque tableau de bord de reporting en redimensionnant ou en supprimant des widgets."

Les rapports dynamiques, accessibles à partir de l’onglet Dernières 24 heures, affichent les événements qui se sont produits au cours des dernières 24 heures, avec un intervalle de temps minimal de deux minutes à compter de l’occurrence de l’événement. En comparaison, les rapports globaux portent sur les événements qui se sont produits il y a au moins deux heures et couvrent les événements sur une période sélectionnée.

Vous pouvez accéder directement au rapport dynamique sur les parcours depuis votre parcours en cliquant sur le bouton **[!UICONTROL Afficher le rapport]**.

![](assets/report_journey.png)

La page **[!UICONTROL Rapport dynamique]** sur les parcours s’affiche avec les onglets suivants :

* [Parcours](#journey-live)
* [E-mail](#email-live)
* [Push](#push-live)
* [SMS](#sms-live)
* [In-app](#in-app-live)

Le **[!UICONTROL Rapport dynamique]** sur les parcours est divisé en différents widgets présentant le succès et les erreurs de votre parcours. Chaque widget peut être redimensionné et supprimé si nécessaire. Pour plus d&#39;informations à ce propos, consultez cette [section](live-report.md#modify-dashboard).

Pour obtenir la liste détaillée de chaque mesure disponible dans Adobe Journey Optimizer, reportez-vous à [cette page](live-report.md#list-of-components-live).

## Onglet Parcours {#journey-live}

Dans le **[!UICONTROL Rapport dynamique]** de votre parcours, l&#39;onglet **[!UICONTROL Parcours]** vous donne une vue claire des données de suivi les plus importantes concernant votre parcours.

![](assets/journey_live_1.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport de parcours.

**[!UICONTROL Performances du parcours]** vous permet de voir le cheminement détaillé de vos profils ciblés tout au long du parcours.

Le widget **[!UICONTROL Statistiques du parcours]** affiche les KPI suivants :

* **[!UICONTROL Profils entrés]** : nombre total de personnes ayant atteint l&#39;événement d&#39;entrée du parcours.

* **[!UICONTROL Profils sortis]** : nombre total de personnes ayant quitté le parcours.

* **[!UICONTROL Parcours individuels en échec]** : nombre total de parcours individuels qui n’ont pas été exécutés avec succès.

Les widgets **[!UICONTROL Événement exécuté au cours des 24 dernières heures]** et **[!UICONTROL Événements]** vous permettent de voir quel événement a été exécuté avec succès au moyen d’un chiffre récapitulatif, d’un graphique et d’un tableau.

Les widgets **[!UICONTROL Action exécutée au cours des 24 dernières heures]** et **[!UICONTROL Actions exécutées et erreurs]** représentent l’action avec le plus de succès et les erreurs qui sont produites au moment où les actions ont été déclenchées. Le graphique Action, le tableau et les chiffres récapitulatifs contiennent les données disponibles pour les actions, notamment :

* **[!UICONTROL Actions exécutées]** : nombre total d’actions exécutées avec succès pour un parcours.

* **[!UICONTROL Erreurs lors des actions]** : nombre total d’erreurs qui se sont produites pour les actions.
+++

## Onglet E-mail {#email-live}

Dans le **[!UICONTROL Rapport dynamique]** de votre parcours, l’onglet **[!UICONTROL E-mail]** présente les principales informations relatives aux diffusions email envoyées dans votre parcours.

![](assets/journey_live_2.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport d’e-mail.

Le widget **[!UICONTROL Statistiques d’envoi des e-mails]** présente les principales informations relatives à votre message :

* **[!UICONTROL Livrés]** : nombre de messages envoyés avec succès.

* **[!UICONTROL Bounces]** : nombre total des erreurs comptabilisées lors de la diffusion et du traitement automatique des retours.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.

Le tableau **[!UICONTROL Envoi de mesures par e-mail]** et le graphique **[!UICONTROL Résumé des e-mails]** détaillent le succès de votre diffusion :

* **[!UICONTROL Envoyés]** : nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Livrés]** : nombre de messages envoyés avec succès.

* **[!UICONTROL Bounces]** : nombre total des erreurs comptabilisées lors de la diffusion et du traitement automatique des retours.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.

* **[!UICONTROL Ouvertures]** : nombre d’ouvertures d’un message dans une diffusion.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans une diffusion.

* **[!UICONTROL Désabonnements]** : nombre de clics sur le lien de désabonnement.

* **[!UICONTROL Plaintes contre le spal]** : nombre de fois où un message a été déclaré comme spam ou courrier indésirable.

Les widgets **[!UICONTROL Causes des bounces]**, **[!UICONTROL Catégories des bounces]** et **[!UICONTROL Hard bounce et bounce - par e-mail]** contiennent les données disponibles relatives aux messages ayant fait l&#39;objet d&#39;un rebond, notamment :

* **[!UICONTROL Hard bounce]** : nombre total d’erreurs permanentes, telles qu’une adresse e-mail incorrecte. Un message d&#39;erreur indique explicitement que l&#39;adresse n&#39;est pas valide, comme Utilisateur inconnu.

* **[!UICONTROL Soft bounces]** : nombre total d&#39;erreurs temporaires, telles qu&#39;une boîte de réception pleine.

* **[!UICONTROL Ignorées]** : nombre total d&#39;erreurs temporaires (par exemple, Absent(e) du bureau) ou techniques (par exemple, si le type d&#39;expéditeur est administrateur).

Les graphiques et tableaux **[!UICONTROL Raisons de l&#39;erreur]** et **[!UICONTROL Exclure des raisons]** vous permettent de voir quelles erreurs et exclusions ont eu lieu au cours de votre diffusion.

Le graphique et le tableau **[!UICONTROL E-mail - Meilleur domaine destinataire]** indiquent les domaines les plus utilisés par les destinataires pour ouvrir l&#39;e-mail.

>[!NOTE]
>
>Les widgets et mesures Offres ne sont disponibles que si une décision a été insérée dans un e-mail. Pour plus d’informations sur la gestion des décisions, consultez cette [page](../offers/get-started/starting-offer-decisioning.md).

Les widgets sur le long terme **[!UICONTROL Statistique des offres]** et **[!UICONTROL Statistiques des offres]** mesurent le succès et l’impact de votre offre sur votre audience ciblée. Il détaille les informations principales relatives à votre message avec les KPI :

* **[!UICONTROL Offre envoyée]** : nombre total d’envois pour l’offre.

* **[!UICONTROL Impression de l’offre]** : nombre d’ouvertures de l’offre dans une diffusion.

* **[!UICONTROL Clics sur les offres]** : nombre de clics sur une offre dans une diffusion.
+++

## Onglet Notification push {#push-live}

Dans le **[!UICONTROL Rapport dynamique]** de votre parcours, l’onglet **[!UICONTROL Notification push]** présente les principales informations relatives aux diffusions push envoyées dans votre parcours.

![](assets/journey_live_3.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport push.

Les widgets **[!UICONTROL Performances d’envoi des notifications push]**, **[!UICONTROL Résumé des notifications push]** et **[!UICONTROL Mesures d’envoi par notification push]** présentent les informations principales relatives à votre message :

* **[!UICONTROL Envoyés]** : nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Livrés]** : nombre de messages envoyés avec succès.

* **[!UICONTROL Bounces]** : nombre total des erreurs comptabilisées lors de la diffusion et du traitement automatique des retours.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.

* **[!UICONTROL Ouvertures]** : nombre d’ouvertures d’un message dans une diffusion.

* **[!UICONTROL Actions]** : nombre total d’actions sur la notification push diffusée (par exemple, clic sur un bouton ou rejet).

* **[!UICONTROL Engagements]** : nombre total d&#39;ouvertures et d&#39;actions pour cette notification push, c&#39;est-à-dire si le profil a ouvert la notification ou si un utilisateur a cliqué sur un bouton.

Les graphiques et tableaux **[!UICONTROL Raisons de l&#39;erreur]** et **[!UICONTROL Exclure des raisons]** vous permettent de voir quelles erreurs et exclusions ont eu lieu au cours de votre diffusion.

Le widget **[!UICONTROL Statistiques d’envoi - Échec]** vous permet de voir combien d’erreurs et de bounces se sont produits.

Les graphiques et tableaux **[!UICONTROL Suivi par plateforme]**, **[!UICONTROL Envoi par plateforme]** et **[!UICONTROL Répartition par plateforme]** décrivent le succès de votre notification push en fonction du système opérationnel.
+++

## Onglet SMS {#sms-live}

![](assets/journey_live_4.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport SMS.

Le tableau **[!UICONTROL SMS - Statistiques d’envoi]** détaille la réussite de votre diffusion :

* **[!UICONTROL Ciblés]** : nombre de profils utilisateur qui sont qualifiés en tant que profils cibles pour cette diffusion.

* **[!UICONTROL Exclus]** : nombre de profils utilisateur, exclus des profils ciblés, qui n’ont pas reçu le message.

* **[!UICONTROL Envoyés]** : nombre total d&#39;envois pour la diffusion.

* **[!UICONTROL Ouvertures]** : nombre d’ouvertures d’un message dans une diffusion.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans une diffusion.

* **[!UICONTROL Bounces]** : nombre total des erreurs comptabilisées lors de la diffusion et du traitement automatique des retours.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.

Le graphique **[!UICONTROL Synthèse des SMS]** détaille la réussite de votre diffusion :

* **[!UICONTROL Bounces]** : nombre total des erreurs comptabilisées lors de la diffusion et du traitement automatique des retours.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.

Les graphiques et tableaux **[!UICONTROL Motifs d’exclusion]** vous permettent de voir quelles erreurs et exclusions ont eu lieu au cours de votre diffusion.
+++

## Onglet In-app {#in-app-live}

![](assets/journey_live_5.png)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport in-app.

La variable **[!UICONTROL Performances in-app]** Les indicateurs de performance clés détaillent les informations principales relatives à l’engagement des visiteurs avec vos messages In-App, telles que :

* **[!UICONTROL Impressions]** : nombre total de messages in-app diffusés à tous les utilisateurs.

  >[!NOTE]
  >
  >Pour s’assurer qu’une impression est comptabilisée, l’utilisateur doit répondre à deux critères :
  >* Qualification au sein de l’expérience in-app, obtenue en atteignant l’activité in-app spécifique dans leur parcours.
  >* Respecter les conditions spécifiées dans les règles Trigger.
  > 
  >En raison du deuxième critère, il peut y avoir des variations notables entre le nombre de profils ciblés et le nombre d’impressions uniques.

* **[!UICONTROL Interactions]**: nombre total d’engagements avec votre message in-app. Cela inclut toutes les actions entreprises par les utilisateurs, telles que les clics, les rejets ou toute autre interaction.

La variable **[!UICONTROL Résumé in-app]** Le graphique montre l’évolution de vos impressions et interactions In-App pendant la période concernée.

La variable **[!UICONTROL Interactions par type]** les graphiques et les tableaux détaillent la manière dont les utilisateurs ont interagi avec votre message in-app en suivant les clics, les rejets ou les interactions.

+++
