---
solution: Journey Optimizer
product: journey optimizer
title: Rapport global
description: Découvrez comment utiliser les données du rapport global
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: 7c7faa5e672d5ed6d7a083db50b206d11ecc4184
workflow-type: tm+mt
source-wordcount: '1441'
ht-degree: 100%

---

# Prise en main du rapport global {#global-report}

>[!NOTE]
>
> Si des requêtes personnalisées sont effectuées par le biais d&#39;API lors de l&#39;utilisation du service Query, attendez-vous à une certaine attente pour vos rapports.

Le **[!UICONTROL rapport global]** vous permet de mesurer l&#39;impact de vos parcours et diffusions sur une période sélectionnée.

* Si vous souhaitez cibler un parcours ou des diffusions dans le contexte d’un parcours, dans le menu **[!UICONTROL Parcours]**, accédez à votre parcours et cliquez sur le bouton **[!UICONTROL Afficher le rapport]**. Vous trouverez ensuite les rapports globaux Parcours, E-mail, SMS et Push.

   ![](assets/report_journey.png)

* Si vous souhaitez cibler une campagne, dans le menu **[!UICONTROL Campagnes]**, accédez à votre campagne et cliquez sur le bouton **[!UICONTROL Rapports]**.

   ![](assets/report_campaign.png)

* Si vous souhaitez basculer du **[!UICONTROL Rapport dynamique]** au **[!UICONTROL Rapport global]** pour votre diffusion, cliquez sur **[!UICONTROL À toute heure]** dans le sélecteur d’onglets.

   ![](assets/report_5.png)

Pour obtenir la liste détaillée de chaque mesure disponible dans Adobe Journey Optimizer, reportez-vous à [cette page](#list-of-components-global).

## Personnalisation du tableau de bord {#modify-dashboard}

Chaque tableau de bord de reporting peut être modifié en modifiant la période et en redimensionnant ou en supprimant des widgets. La modification des widgets n&#39;a un impact que sur le tableau de bord de l&#39;utilisateur actuel. Les autres utilisateurs voient leurs propres tableaux de bord ou ceux définis par défaut.

1. Dans votre rapport global, sélectionnez une heure de début et une heure de fin pour cibler des données spécifiques.

   ![](assets/report_modify_1.png)

1. Choisissez si vous souhaitez exclure les événements de test de vos rapports avec la barre de bascule. Pour plus d’informations sur les événements de test, consultez [cette page](../building-journeys/testing-the-journey.md).

   Notez que l&#39;option **[!UICONTROL Exclure les événements de test]** n&#39;est disponible que pour les rapports de parcours.

   ![](assets/report_modify_2.png)

1. Cliquez sur **[!UICONTROL Modifier]** pour commencer à personnaliser votre tableau de bord.

   ![](assets/report_modify_3.png)

1. Ajustez la taille des widgets en faisant glisser leur coin inférieur droit.

   ![](assets/report_modify_4.png)

1. Cliquez sur **[!UICONTROL Supprimer]** pour supprimer tout widget dont vous n’avez pas besoin.

   ![](assets/report_modify_5.png)

1. Une fois satisfait de l&#39;ordre d&#39;affichage et de la taille de vos widgets, cliquez sur **[!UICONTROL Enregistrer]**.

Votre tableau de bord est maintenant enregistré. Vos différentes modifications seront réappliquées pour une utilisation ultérieure de vos rapports dynamiques. Si nécessaire, utilisez l’option **[!UICONTROL Réinitialiser]** pour restaurer les widgets par défaut et leur ordre.

## Liste des composants {#list-of-components-global}

Les tableaux ci-dessous contiennent la liste des mesures utilisées dans les différents rapports et leur définition en fonction du type de diffusion.

### Mesures de parcours {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Mesure<br/> </th> 
   <th> Définition<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>Actions exécutées avec succès<br/> </td> 
   <td> Nombre total d’actions exécutées avec succès pour un parcours.<br/> </td> 
</tr> 
  <tr> 
   <td> Profils ayant accédé à l’entrée<br/> </td> 
   <td> Nombre total de personnes ayant atteint l’événement d’entrée du parcours.<br/> </td> 
</tr>
  <tr> 
   <td> Erreur lors de l’action<br/> </td> 
   <td>Nombre total d’erreurs qui se sont produites lors des actions.<br/> </td> 
</tr> 
  <tr> 
   <td> Profils ayant quitté le parcours<br/> </td> 
   <td> Nombre total de personnes qui ont quitté le parcours.<br/> </td> 
</tr> 
  <tr> 
   <td> Parcours individuel ayant échoué<br/> </td> 
   <td> Nombre total de parcours individuels qui n’ont pas été exécutés avec succès.<br/> </td> 
</tr> 
 </tbody> 
</table>

### Mesures des e-mails et SMS   {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Mesure<br/> </th> 
   <th> Définition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> Rebonds<br/> </td> 
   <td> Nombre total d’erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux de rebond<br/> </td> 
   <td> Pourcentage d’e-mails ayant fait l’objet d’un rebond par rapport aux e-mails envoyés.<br/> </td> 
</tr>
  <tr> 
   <td> Clics<br/> </td> 
   <td> Nombre de fois où un contenu a fait l’objet d’un clic dans un e-mail.<br/> </td> 
</tr> 
  <tr> 
   <td> Diffusés <br/> </td> 
   <td> Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.<br/></td> 
</tr> 
  <tr> 
   <td> Taux de diffusion<br/> </td> 
   <td> Pourcentage de messages envoyés avec succès.<br/> </td> 
</tr>
  <tr> 
   <td> Erreurs<br/> </td> 
   <td> Nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux d’erreur<br/> </td> 
   <td> Pourcentage d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée, par rapport aux e-mails envoyés.<br/> </td> 
</tr>
  <tr> 
   <td> Exclus<br/> </td> 
   <td> Nombre de profils qui ont été exclus par Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Hard bounce<br/> </td> 
   <td> Le nombre total d’erreurs permanentes, telles qu’une adresse e-mail incorrecte. Un message d'erreur indique explicitement que l'adresse n'est pas valide, comme Utilisateur inconnu.<br/> </td>
</tr>
  <tr> 
   <td> Ignorés<br/> </td> 
   <td> Nombre total d’erreurs temporaires, telles que l’absence du bureau, ou une erreur technique, par exemple si le type d’expéditeur est Postmaster.<br/> </td> 
</tr>
   <tr> 
   <td>Taux de clics sur les offres<br/> </td> 
   <td>Pourcentage d’utilisateurs ayant interagi avec l’offre.<br/> </td> 
</tr>
   <tr> 
   <td>Taux d’impression des offres<br/> </td> 
   <td>Pourcentage d’offres ouvertes par rapport au nombre d’offres envoyées.<br/> </td> 
</tr>
   <tr> 
   <td>Nom de l’offre<br/> </td> 
   <td> Nom de l’offre ajoutée dans la diffusion. Pour plus d’informations sur les emplacements, consultez cette <a href="../offers/offer-library/creating-personalized-offers.md">page</a>.<br/> </td> 
</tr>
   <tr> 
   <td>Offre envoyée<br/> </td> 
   <td>Nombre total d’envois pour l’offre.<br/> </td> 
</tr> 
  <tr>
   <td>Ouvertures<br/> </td> 
   <td> Nombre d’ouvertures du message.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux d’ouverture<br/> </td> 
   <td> Nombre total de messages ouverts par rapport au nombre de messages diffusés.<br/> </td> 
</tr>
  <tr> 
   <td>Nom de l’emplacement<br/> </td> 
   <td> Nom de l’emplacement utilisé pour afficher votre offre. Pour plus d’informations sur les emplacements, consultez cette <a href="../offers/offer-library/creating-placements.md">page</a>. </td> 
</tr> 
  <tr> 
   <td> Reprises<br/> </td> 
   <td> Nombre d’e-mails dans la file d’attente pour les reprises.<br/> </td> 
</tr> 
  <tr> 
   <td> Envoyés<br/> </td> 
   <td> Nombre total d’envois pour la diffusion.<br/> </td> 
</tr>
  <tr> 
   <td> Soft bounce<br/> </td> 
   <td> Nombre total d’erreurs temporaires, telles qu’une boîte de réception pleine.<br/> </td> 
</tr>
  <tr> 
   <td> Plaintes contre le spam<br/> </td> 
   <td> Nombre de fois où un message a été déclaré comme spam ou courrier indésirable.<br/> </td> 
</tr>
  <tr> 
   <td> Ciblés<br/> </td> 
   <td> Nombre total de messages traités lors de l’analyse de la diffusion.<br/> </td> 
</tr> 
  <tr> 
   <td> Clics uniques<br/> </td> 
   <td> Nombre de destinataires qui ont cliqué sur un contenu dans un e-mail.<br/> </td> 
</tr> 
  <tr> 
   <td>Taux de clics uniques<br/> </td> 
   <td> Pourcentage d’utilisateurs ayant interagi avec la diffusion.<br/> </td> 
</tr>
  <tr> 
   <td> Ouvertures uniques<br/> </td> 
   <td>Nombre de destinataires ayant ouvert la diffusion.<br/> </td> 
</tr> 
  <tr> 
   <td> Désabonnements<br/> </td> 
   <td> Nombre de clics sur le lien de désabonnement.<br/> </td> 
</tr> 
 </tbody> 
</table>

<!--
### Experimentation metrics {#experimentation-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td>App installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>App launches<br/> </td> 
   <td><br/> </td> 
</tr>
 <tr> 
   <td>Average lift<br/> </td> 
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../campaigns/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../campaigns/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../campaigns/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>First app launches<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Outbound Clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Profiles<br/> </td> 
   <td>Number of profiles targeted for this treatment.<br/> </td> 
</tr>
  <tr> 
   <td>Unique email opens<br/> </td> 
   <td><br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td><br/> </td>
</tr>
  <tr> 
   <td>Unique installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique launches<br/> </td> 
   <td><br/> </td> 
</tr> 
  <tr> 
   <td>Unique outbound clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique upgrades<br/> </td> 
   <td><br/> </td> 
</tr>
   <td>Upgrades<br/> </td> 
   <td><br/> </td> 
</tr> 
</tbody> 
</table>
-->

### Mesures des notifications push  

<table> 
 <thead> 
  <tr> 
   <th> Mesure<br/> </th> 
   <th> Définition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Actions<br/> </td> 
   <td> Nombre total d’actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.<br/> </td> 
</tr>
  <tr> 
   <td>Rebonds<br/> </td> 
   <td> Nombre total d’erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux de rebond<br/> </td> 
   <td> Pourcentage de notifications push ayant rebondi par rapport aux notifications push envoyées.<br/> </td>
</tr>
  <tr> 
   <td> Diffusés<br/> </td> 
   <td> Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux de diffusion<br/> </td> 
   <td> Pourcentage de notifications push envoyées avec succès.<br/> </td> 
</tr>
  <tr> 
   <td>Engagements<br/> </td> 
   <td> Nombre total d’ouvertures et d’actions pour cette notification push, c’est-à-dire si le profil a ouvert la notification push ou si un utilisateur a cliqué sur un bouton.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux d’engagement<br/> </td> 
   <td> Pourcentage d’ouvertures et d’actions pour cette notification push, c’est-à-dire si le profil a ouvert la notification push ou si un utilisateur a cliqué sur un bouton.<br/> </td> 
</tr>
  <tr> 
   <td> Erreurs<br/> </td> 
   <td> Nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.<br/> </td> 
</tr>
  <tr> 
   <td> Taux d’erreur<br/> </td> 
   <td> Pourcentage d’erreurs survenues pendant une diffusion qui l’empêchent d’être envoyée par rapport aux notifications push envoyées.<br/> </td> 
</tr> 
  <tr> 
   <td> Exclus<br/> </td> 
   <td> Nombre de profils qui ont été exclus par Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Ouvertures<br/> </td> 
   <td> Nombre total de notifications push diffusées sur l'appareil et ayant fait l'objet d'un clic par les utilisateurs ouvrant l'application. Cette mesure est similaire au Clic push, sauf qu'une Ouverture push ne sera pas déclenchée si la notification a été ignorée.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux d'ouverture<br/> </td> 
   <td> Pourcentage de notifications push ouvertes.<br/> </td> 
</tr> 
  <tr> 
   <td> Envoyés<br/> </td> 
   <td> Nombre total d’envois pour la diffusion.<br/> </td> 
</tr> 
  <tr> 
   <td> Ciblés<br/> </td> 
   <td> Nombre total de messages push traités lors de l’analyse de la diffusion.<br/> </td> 
</tr>  
 </tbody> 
</table>

### Mesures de page de destination {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Mesure<br/> </th> 
   <th> Définition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>Rebonds<br/> </td> 
   <td>Nombre de personnes qui n’ont pas interagi avec la page de destination et n’ont pas effectué l’action d’inscription.<br/> </td> 
</tr>
 <tr> 
   <td>Taux de rebond<br/> </td> 
   <td>Nombre de personnes nʼayant pas interagi avec la page de destination ni effectué lʼaction dʼinscription, par rapport au nombre total de visites.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Clics<br/> </td> 
   <td>Nombre de clics sur un contenu de la page de destination.<br/> </td> 
</tr>
 <tr> 
   <td>Taux de clics<br/> </td> 
   <td>Pourcentage de clics sur la page de destination.<br/> </td>
</tr>
<tr>
<td>Conversion<br/> </td> 
   <td>Nombre de personnes ayant interagi avec la page de destination, par exemple celles qui se sont inscrites à un formulaire.<br/> </td> 
</tr>
<tr>
   <td>Taux de conversion<br/> </td> 
   <td>Nombre de personnes ayant interagi avec la page de destination, par exemple le nombre dʼinscrits à un formulaire par rapport au nombre total de visites.<br/> </td> 
</tr>
 <tr> 
   <td>Parcours<br/> </td> 
   <td>Nombre de visites sur votre page de destination provenant dʼun parcours.<br/> </td> 
</tr>
 <tr> 
   <td>Autres sources<br/> </td> 
   <td>Nombre de visites de votre page de destination provenant d’une source externe au lieu d’un parcours.<br/> </td> 
</tr>
 <tr> 
   <td>Nombre total de visites<br/> </td> 
   <td> Nombre total de visites sur votre page de destination provenant de parcours et de sources externes, y compris les visites multiples dʼun seul destinataire.<br/> </td> 
</tr>
 <tr> 
   <td>Visiteurs uniques<br/> </td> 
   <td>Nombre de personnes ayant visité votre page de destination, les visites multiples dʼun même destinataire ne sont pas prises en compte.<br/> </td> 
</tr>
 <tr> 
   <td>Visites<br/> </td> 
   <td>Nombre de visites sur votre page de destination, y compris les visites multiples d’un seul destinataire.<br/> </td> 
</tr>
 </tbody> 
</table>

### Mesures des notifications push  

<table> 
 <thead> 
  <tr> 
   <th> Mesure<br/> </th> 
   <th> Définition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Actions<br/> </td> 
   <td> Nombre total d’actions sur la notification push diffusée, par exemple clic sur un bouton ou rejet.<br/> </td> 
</tr>
  <tr> 
   <td>Rebonds<br/> </td> 
   <td> Nombre total d’erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux de rebond<br/> </td> 
   <td> Pourcentage de notifications push ayant rebondi par rapport aux notifications push envoyées.<br/> </td>
</tr>
  <tr> 
   <td> Diffusés<br/> </td> 
   <td> Nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux de diffusion<br/> </td> 
   <td> Pourcentage de notifications push envoyées avec succès.<br/> </td> 
</tr>
  <tr> 
   <td>Engagements<br/> </td> 
   <td> Nombre total d’ouvertures et d’actions pour cette notification push, c’est-à-dire si le profil a ouvert la notification push ou si un utilisateur a cliqué sur un bouton.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux d’engagement<br/> </td> 
   <td> Pourcentage d’ouvertures et d’actions pour cette notification push, c’est-à-dire si le profil a ouvert la notification push ou si un utilisateur a cliqué sur un bouton.<br/> </td> 
</tr>
  <tr> 
   <td> Erreurs<br/> </td> 
   <td> Nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.<br/> </td> 
</tr>
  <tr> 
   <td> Taux d’erreur<br/> </td> 
   <td> Pourcentage d’erreurs survenues pendant une diffusion qui l’empêchent d’être envoyée par rapport aux notifications push envoyées.<br/> </td> 
</tr> 
  <tr> 
   <td> Exclus<br/> </td> 
   <td> Nombre de profils qui ont été exclus par Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Ouvertures<br/> </td> 
   <td> Nombre total de notifications push diffusées sur l'appareil et ayant fait l'objet d'un clic par les utilisateurs ouvrant l'application. Cette mesure est similaire au Clic push, sauf qu'une Ouverture push ne sera pas déclenchée si la notification a été ignorée.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux d'ouverture<br/> </td> 
   <td> Pourcentage de notifications push ouvertes.<br/> </td> 
</tr> 
  <tr> 
   <td> Envoyés<br/> </td> 
   <td> Nombre total d’envois pour la diffusion.<br/> </td> 
</tr> 
  <tr> 
   <td> Ciblés<br/> </td> 
   <td> Nombre total de messages push traités lors de l’analyse de la diffusion.<br/> </td> 
</tr>  
 </tbody> 
</table>

<!--
### In-app metrics {#inapp-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Clicks<br/> </td> 
   <td>Total number of recipients who interacted with the buttons included in the In-app message.<br/> </td> 
</tr>
  <tr> 
   <td>Click rate<br/> </td> 
   <td>Percentage of users who interacted with the buttons included in the In-app message compared to users who saw the message.<br/> </td> 
</tr> 
  <tr> 
   <td>Dismiss rate<br/> </td> 
   <td> Percentage of In-app messages that recipients dismissed.<br/> </td> 
</tr> 
  <tr> 
   <td>Impressions<br/> </td> 
   <td> Total number of In-app messages delivered to all users.<br/> </td>
</tr>
  <tr> 
   <td>Unique impressions<br/> </td> 
   <td>Number of unique users to whom the In-app message was delivered.<br/> </td>
</tr>
 </tbody> 
</table>
-->
