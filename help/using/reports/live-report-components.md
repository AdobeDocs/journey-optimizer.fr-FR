---
solution: Journey Optimizer
product: journey optimizer
title: Liste des composants
description: Découvrez comment utiliser les données du rapport dynamique.
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 12168cdf-f517-49b5-958b-ba689ade6982
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 100%

---

# Liste des composants {#list-of-components-live}

>[!AVAILABILITY]
>
>L’expérience actuelle de création de rapports sera abandonnée à compter de la version d’octobre. À partir de cette date, la nouvelle expérience de création de rapports deviendra la norme. Nous vous recommandons de vous familiariser avec les nouvelles fonctionnalités pour garantir une transition fluide. [Commencez avec la nouvelle interface de création de rapports de Journey Optimizer.](report-gs-cja.md)

Les tableaux ci-dessous contiennent la liste des mesures utilisées dans les différents rapports et leur définition en fonction du type de diffusion.

## Mesures de parcours {#journey-metrics}

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

## Dimensions et mesures des e-mails et SMS {#email-and-sms-metrics}

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
   <td> Nombre total d’erreurs comptabilisées lors de la diffusion et du traitement automatique des retours.<br/> </td> 
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
   <td> Nombre de messages envoyés avec succès.<br/></td> 
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
   <td> Rebond définitif<br/> </td> 
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
   <td> Rebond temporaire<br/> </td> 
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

## Mesures de page de destination {#landing-page-metrics}

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
  <tr> 
   <td>Clics<br/> </td> 
   <td>Nombre de clics sur un contenu de la page de destination.<br/> </td> 
</tr>
<tr>
<td>Conversion<br/> </td> 
   <td>Nombre de personnes ayant interagi avec la page de destination, par exemple celles qui se sont inscrites à un formulaire.<br/> </td> 
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

## Mesures des notifications push {#push-notification-metrics}

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
   <td> Nombre total d’erreurs comptabilisées lors de la diffusion et du traitement automatique des retours.<br/> </td> 
</tr> 
  <tr> 
   <td> Diffusés<br/> </td> 
   <td> Nombre de messages envoyés avec succès.<br/> </td> 
</tr> 
  <tr> 
   <td>Engagements<br/> </td> 
   <td> Nombre total d’ouvertures et d’actions pour cette notification push, c’est-à-dire si le profil a ouvert la notification push ou si un utilisateur a cliqué sur un bouton.<br/> </td> 
</tr> 
  <tr> 
   <td> Erreurs<br/> </td> 
   <td> Nombre total d’erreurs survenues au cours d’une diffusion, l’empêchant d’être envoyée à des profils.<br/> </td> 
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
## In-app metrics {#inapp-metrics}
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
