---
solution: Journey Optimizer
product: journey optimizer
title: Liste des composants
description: Découvrir comment utiliser les données du rapport
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: aa060d8e-23e2-4bab-b709-636077eb5d20
source-git-commit: 7945ab9369498f23685aa2f727542c7367c2d830
workflow-type: tm+mt
source-wordcount: '2189'
ht-degree: 97%

---

# Liste de mesures {#list-of-components-global}

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
<td>Engagement du parcours</td> 
<td>Nombre total de personnes uniques ayant reçu des messages envoyés depuis le parcours et représentant des profils distincts ayant atteint un point d’action désigné dans le parcours.</td> 
</tr> 
<tr> 
<td>Entrées de parcours</td> 
<td>Nombre total de personnes ayant atteint l’événement d’entrée du parcours.</td> 
</tr>
<tr> 
<td>Sorties du parcours</td> 
<td>Nombre total de personnes ayant quitté le parcours.</td> 
</tr>
<tr> 
<td>Échecs de parcours</td> 
<td>Nombre total de parcours individuels dont l’exécution a échoué.</td> 
</tr>
<tr> 
<td>Entrées de parcours uniques</td> 
<td>Nombre total de personnes ayant atteint l’événement d’entrée du parcours, sans prendre en compte les interactions multiples d’un même profil.</td> 
</tr>
<tr> 
<td>Sorties de parcours uniques</td> 
<td>Nombre total de personnes ayant quitté le parcours, sans prendre en compte les interactions multiples d’un même profil.</td> 
</tr>
<tr> 
<td>Échecs de parcours uniques</td> 
<td>Nombre total de parcours individuels dont l’exécution a échoué, sans prendre en compte les interactions multiples d’un même profil.</td> 
</tr>
 </tbody> 
</table>

## Mesures relatives aux e-mails {#email-metrics}

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
   <td> Nombre total d’erreurs cumulées au cours du processus d’envoi et du traitement automatique des retours par rapport au nombre total de messages envoyés.<br/> </td> 
  </tr>
  <tr> 
   <td> Taux de rebond<br/> </td> 
   <td> Pourcentage d’e-mails ayant entraîné un rebond, par rapport au nombre total d’e-mails envoyés.<br/> </td> 
  </tr> 
  <tr> 
   <td> Taux d’ouvertures par clic (CTOR)<br/> </td> 
   <td> Nombre d’ouvertures de l’e-mail.<br/> </td> 
  </tr>
  <tr> 
   <td> Taux de clics (CTR)<br/> </td> 
   <td> Pourcentage d’utilisateurs et d’utilisatrices ayant interagi avec l’e-mail.<br/> </td> 
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
   <td> Motif de l’erreur<br/> </td> 
   <td> Nom de la cause initiale spécifique de l’erreur. <a href="exclusion-list.md">En savoir plus sur les motifs des erreurs</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Estimation des ouvertures dʼe-mails<br/> </td> 
   <td>Estimation du nombre total d’ouvertures d’e-mails, prenant en compte les ouvertures directes par les profils et les ouvertures automatisées déclenchées par les serveurs de messagerie. Cette mesure prend en compte les ouvertures déclenchées par les serveurs de messagerie à des fins d’analyse de la confidentialité ou de la sécurité en appliquant un taux d’ouverture calculé à partir des destinataires qui ont ouvert manuellement l’e-mail par rapport à ceux dont les e-mails n’ont été ouverts que par des serveurs de messagerie.<br/> </td> 
  </tr>
  <tr> 
   <td> Taux de clics sur les offres<br/> </td> 
   <td> Pourcentage d’utilisateurs ayant interagi avec l’offre.<br/> </td> 
  </tr>
  <tr> 
   <td> Taux d’impression des offres<br/> </td> 
   <td> Pourcentage d’offres ouvertes par rapport au nombre d’offres envoyées.<br/> </td> 
  </tr>
  <tr> 
   <td> Nom de l’offre<br/> </td> 
   <td> Nom de l’offre ajoutée dans la diffusion. Pour plus d’informations sur les emplacements, consultez cette <a href="../offers/offer-library/creating-personalized-offers.md">page</a>.<br/> </td> 
  </tr>
  <tr> 
   <td> Offre envoyée<br/> </td> 
   <td> Nombre total d’envois pour l’offre.<br/> </td> 
  </tr> 
  <tr> 
   <td> Ouvertures<br/> </td> 
   <td> Nombre d’ouvertures du message.<br/> </td> 
  </tr> 
  <tr> 
   <td> Erreurs d’envoi<br/> </td> 
   <td> Nombre total d’erreurs qui se sont produites au cours du processus d’envoi, empêchant l’envoi à des profils.<br/> </td> 
  </tr> 
  <tr> 
   <td> Exclusions d’envois<br/> </td> 
   <td> Nombre de profils qui ont été exclus par Adobe Journey Optimizer. <a href="exclusion-list.md">En savoir plus sur la comptabilisation des exclusions</a>.<br/> </td> 
  </tr>
  <tr> 
   <td> Nom de l’emplacement<br/> </td> 
   <td> Nom de l’emplacement utilisé pour afficher votre offre. Pour plus d’informations sur les emplacements, consultez cette <a href="../offers/offer-library/creating-placements.md">page</a>. </td> 
  </tr>
  <tr> 
   <td> Plaintes contre le spam<br/> </td> 
   <td> Nombre de fois où un message a été déclaré comme spam ou courrier indésirable.<br/> </td> 
  </tr> 
  <tr> 
   <td> Ciblés<br/> </td> 
   <td> Nombre de profils qualifiés pour l’audience avant l’application des exclusions, des suppressions ou des suppressions de consentement. Dans les parcours dont la rentrée est activée, un profil peut être ciblé plusieurs fois.<br/> </td> 
  </tr>
  <tr> 
   <td>Rebonds uniques<br/> </td> 
   <td> Nombre de profils uniques pour lesquels au moins un e-mail a entraîné un rebond.</td> 
  </tr>
  <tr> 
   <td>Taux de rebond unique<br/> </td> 
   <td>Pourcentage de profils uniques dont l’e-mail a fait au moins une fois l’objet d’un rebond, en fonction du nombre total d’envois uniques.</td> 
  </tr>
  <tr> 
   <td> Clics uniques<br/> </td> 
   <td> Nombre de profils qui ont cliqué sur le contenu d’un e-mail.<br> Notez que lors du calcul des clics uniques, les 10 derniers jours sont pris en compte. Si un profil enregistre plusieurs clics au cours de la période de 10 jours, ils sont comptés comme des clics uniques. Cependant, si un profil a deux clics à plus de 10 jours d’intervalle, ceux-ci ne seront pas considérés comme des clics uniques.<br/> </td> 
  </tr>
  <tr> 
   <td>Taux d’ouvertures de clics uniques<br/> </td> 
   <td> Pourcentage de profils uniques qui ont cliqué sur un lien après l’ouverture de l’e-mail, en fonction des ouvertures uniques. </td> 
  </tr>
  <tr> 
   <td> Taux de clics uniques<br/> </td> 
   <td> Pourcentage de profils uniques qui ont cliqué sur au moins un lien dans l’e-mail, par rapport au nombre d’e-mails diffusés uniques. </td> 
  </tr>
  <tr> 
   <td> Diffusions uniques<br/> </td> 
   <td> Nombre de profils uniques ayant reçu au moins un e-mail.</td> 
  </tr>
  <tr> 
   <td> Désabonnements uniques des e-mails<br/> </td> 
   <td> Nombre de profils qui se sont désabonnés de vos e-mails.<br/> </td> 
  </tr>
  <tr> 
   <td> Estimation des ouvertures dʼe-mails uniques<br/> </td> 
   <td> Estimation du nombre de destinataires uniques des e-mails qui ont probablement ouvert l’e-mail. Cette mesure vise à fournir un nombre plus précis d’engagements individuels déclenchés par des serveurs de messagerie pour l’analyse de la confidentialité ou de la sécurité en appliquant un taux d’ouverture unique calculé à partir des profils uniques qui ont ouvert manuellement l’e-mail par rapport à ceux dont les e-mails n’ont été ouverts que par des serveurs de messagerie.<br/> </td> 
  </tr>
  <tr> 
   <td> Ouvertures uniques<br/> </td> 
   <td> Nombre de profils ayant ouvert la diffusion. <br> Notez que lors du calcul des ouvertures uniques, les 10 derniers jours sont pris en compte. Si un profil enregistre plusieurs ouvertures au cours de la période de 10 jours, celles-ci sont comptées comme des ouvertures uniques. Cependant, si un profil a 2 ouvertures à plus de 10 jours d’intervalle, celles-ci ne seront pas considérées comme des ouvertures uniques.<br/> </td> 
  </tr> 
  <tr>
  <tr> 
   <td> Envois uniques<br/> </td> 
   <td>Nombre de profils uniques pour lesquels au moins une tentative d’envoi d’e-mail a eu lieu.<br/> </td> 
  </tr>
  <tr> 
   <td> Erreurs d’envoi unique<br/> </td> 
   <td>Nombre de profils uniques ayant rencontré au moins une erreur d’envoi lors du processus sortant.<br/> </td> 
  </tr>
  <tr> 
   <td> Exclusions d’envois uniques<br/> </td> 
   <td>Nombre de profils uniques exclus de la réception des messages en raison de règles d’éligibilité, de la segmentation d’audience ou du statut de profil. <a href="exclusion-list.md">En savoir plus sur la comptabilisation des exclusions</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Ciblages uniques<br/> </td> 
   <td>Nombre de profils uniques qualifiés pour l’audience avant l’application des exclusions, des suppressions ou des suppressions de consentement.<br/> </td> 
  </tr> 
  <tr> 
   <td> Désabonnements<br/> </td> 
   <td> Nombre de clics sur le lien de désabonnement.<br/> </td> 
  </tr> 
 </tbody> 
</table>

## Mesures relatives aux SMS

<table> 
  <thead> 
    <tr> 
      <th> Mesure relative aux SMS </th> 
      <th> Définition </th> 
    </tr>
  </thead> 
  <tbody> 
    <tr> 
      <td>Délivrés</td> 
      <td>Nombre de SMS dont l’envoi a réussi par rapport au nombre total de SMS envoyés.</td> 
    </tr>
    <tr> 
      <td>Clics</td> 
      <td>Nombre de clics sur un lien dans un SMS.</td> 
    </tr>
    <tr> 
      <td>Rebonds des SMS sortants</td> 
      <td>Nombre total d’erreurs cumulées lors de la procédure d’envoi et du traitement automatique des retours par rapport au nombre total de SMS envoyés.</td> 
    </tr>
    <tr> 
      <td>Erreurs de SMS sortants</td> 
      <td>Nombre total d’erreurs qui se sont produites, empêchant l’envoi du SMS aux destinataires.</td> 
    </tr>
    <tr> 
      <td>Exclusions de SMS sortants</td> 
      <td>Nombre de profils qui ont été exclus de la réception de SMS par Adobe Journey Optimizer. <a href="exclusion-list.md">En savoir plus sur la comptabilisation des exclusions</a>.</td> 
    </tr>
    <tr> 
      <td>Clics uniques</td> 
      <td>Nombre de destinataires qui ont cliqué sur un lien dans un SMS.</td> 
    </tr>
    <tr> 
      <td>Affichages</td> 
      <td>Nombre d’affichages ou d’ouvertures d’un SMS.</td> 
    </tr>
    <tr> 
      <td>Affichages uniques</td> 
      <td>Nombre de destinataires ayant ouvert le SMS, sans prendre en compte les interactions multiples d’un même utilisateur ou d’une même utilisatrice.</td> 
    </tr>
    <tr> 
      <td>Personnes</td> 
      <td>Nombre de profils d’utilisateurs et d’utilisatrices uniques ayant reçu un SMS ou interagi avec celui-ci.</td> 
    </tr>
  </tbody> 
</table>

<!--
## Experimentation metrics {#experimentation-metrics}
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
   <td>Number of times the email was opened.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td>Number of clicks on the unsubscription link.<br/> </td> 
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
   <td>Number of profiles who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of profiles who clicked on the unsubscription link.<br/> </td>
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

## Mesures in-app {#inapp-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Mesure<br/> </th> 
   <th> Définition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
  <tr> 
   <td>Clics<br/> </td> 
   <td>Nombre total de profils ayant interagi avec les boutons inclus dans le message in-app.<br/> </td> 
  </tr>
  <tr> 
   <td>Taux de clics<br/> </td> 
   <td>Pourcentage d’utilisateurs et d’utilisatrices ayant interagi avec les boutons inclus dans le message in-app par rapport au nombre d’utilisateurs et d’utilisatrices ayant vu le message.<br/> </td> 
  </tr>
  <tr> 
   <td>Taux d’ignorance<br/> </td> 
   <td>Pourcentage de messages in-app ignorés par les profils.<br/> </td> 
  </tr>
  <tr> 
   <td>Impressions<br/> </td> 
   <td>Nombre total de messages in-app diffusés à tous les utilisateurs et utilisatrices.<br/> </td>
  </tr>
  <tr> 
   <td>Impressions uniques<br/> </td> 
   <td>Nombre d’utilisateurs et d’utilisatrices uniques auxquels le message in-app a été diffusé.<br/> </td>
  </tr>
  <tr> 
   <td>Affichages<br/> </td>
   <td>Nombre d’ouvertures du message in-app.<br/> </td>
  </tr>
  <tr> 
   <td>Affichages uniques<br/> </td>
   <td>Nombre d’ouvertures du message in-app, sans prendre en compte les interactions multiples d’un même profil.<br/> </td>
  </tr>
  <tr> 
   <td>Clics uniques<br/> </td>
   <td>Nombre de profils ayant cliqué sur le contenu de vos messages in-app.<br/> </td>
  </tr>
  <tr> 
   <td>Clics<br/> </td>
   <td>Nombre de clics sur le contenu de vos messages in-app.<br/> </td>
  </tr>
  <tr> 
   <td>Taux de clics (CTR)<br/> </td>
   <td>Pourcentage d’utilisateurs et d’utilisatrices ayant interagi avec les messages in-app.<br/> </td>
  </tr>
  <tr> 
   <td>Taux d’ouvertures par clic (CTOR)<br/> </td>
   <td>Nombre d’ouvertures du message in-app.<br/> </td>
  </tr>
  <tr> 
   <td>Envois<br/> </td>
   <td>Nombre total de messages in-app envoyés.<br/> </td>
  </tr>
  <tr> 
   <td>Entrants déclenchés<br/> </td>
   <td>Nombre de fois qu’un message in-app a été déclenché par une interaction d’utilisateur ou d’utilisatrice ou un événement prédéfini.<br/> </td>
  </tr>
  <tr> 
   <td>Entrants ignorés<br/> </td>
   <td>Nombre de fois où les utilisateurs et utilisatrices ont ignoré le message in-app sans interagir avec celui-ci.<br/> </td>
  </tr>
 </tbody> 
</table>

## Mesures des notifications push

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
   <td> Motif de l’erreur<br/> </td> 
   <td> Nom de la cause initiale spécifique de l’erreur. <a href="exclusion-list.md">En savoir plus sur les motifs des erreurs</a>.<br/> </td> 
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
   <td> Actions push personnalisées<br/> </td> 
   <td>Nombre d’actions personnalisées effectuées par les profils en réponse aux notifications push.<br/> </td> 
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
   <td>Taux de rebond<br/> </td> 
   <td>Pourcentage de personnes qui ont consulté la page de destination mais n’ont pas interagi ou ne se sont pas abonnées, par rapport au nombre total de visites.<br/> </td> 
</tr>
 <tr> 
   <td>Clics<br/> </td> 
   <td>Nombre de clics sur un contenu de la page de destination.<br/> </td> 
</tr>

<tr> 
   <td>Conversion de la page de destination<br/> </td> 
   <td>Nombre de personnes ayant interagi avec la page de destination, par exemple celles qui se sont inscrites à un formulaire.<br/> </td> 
</tr>
<tr> 
   <td>Taux de conversion de la page de destination<br/> </td> 
   <td>Nombre de personnes ayant interagi avec la page de destination, par exemple le nombre dʼinscriptions à un formulaire par rapport au nombre total de visites.<br/> </td> 
</tr>
 <tr> 
   <td>Vues de la page de destination<br/> </td> 
   <td>Nombre total de visites sur votre page de destination provenant de parcours et de sources externes, y compris les visites multiples dʼun même profil.<br/> </td> 
</tr>
<tr> 
   <td>Conversions uniques de la page de destination<br/> </td> 
   <td>Nombre de personnes uniques ayant interagi avec la page de destination, sans prendre en compte les interactions multiples d’un même profil.<br/> </td> 
</tr>
 <tr> 
   <td>Vues uniques de la page de destination<br/> </td> 
   <td>Nombre de personnes uniques qui ont visité votre page de destination, sans prendre en compte les visites multiples d’un même profil.<br/> </td> 
</tr>
 </tbody> 
</table>

## Courrier {#direct-mail}

<table> 
 <thead> 
  <tr> 
   <th> Mesure<br/> </th> 
   <th> Définition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Diffusés<br/> </td> 
   <td>Nombre de messages de publipostage direct qui ont été correctement diffusés aux destinataires.<br/> </td> 
</tr>
<tr> 
   <td>Erreurs sortantes<br/> </td> 
   <td>Nombre de messages de publipostage direct qui ont rencontré des erreurs lors du traitement ou de l’envoi, entraînant l’échec de la diffusion.<br/> </td> 
</tr>
<tr> 
   <td>Exclusions sortantes<br/> </td> 
   <td>Nombre de profils exclus de la réception du courrier en raison de critères prédéfinis ou d’un filtrage par Adobe Journey Optimizer. <a href="exclusion-list.md">En savoir plus sur la comptabilisation des exclusions</a>.<br/> </td> 
</tr>
<tr> 
   <td>Profils<br/> </td> 
   <td>Nombre de profils d’utilisateurs et d’utilisatrices identifiés comme audience cible pour la campagne de publipostage direct.<br/> </td> 
</tr>
<tr> 
   <td>Envoyés<br/> </td> 
   <td>Nombre total de messages de publipostage direct dont l’envoi a réussi dans le cadre de la campagne.<br/> </td> 
</tr>
<tr> 
   <td>Ciblés<br/> </td> 
   <td>Nombre total de messages de publipostage direct préparés et traités pour l’envoi.<br/> </td> 
</tr>
 </tbody> 
</table>


## Mesures de la vignette de contenu {#content-based}

<table> 
 <thead> 
  <tr> 
   <th> Mesure<br/> </th> 
   <th> Définition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Taux de clics (CTR)<br/> </td> 
   <td>Pourcentage d’utilisateurs et d’utilisatrices ayant interagi avec la vignette de contenu.<br/> </td> 
</tr>
<tr> 
   <td>Clics<br/> </td> 
   <td>Nombre de clics sur le contenu de votre vignette de contenu.<br/> </td> 
</tr>
<tr> 
   <td>Affichages<br/> </td> 
   <td>Nombre d’ouvertures du message.<br/> </td> 
</tr>
<tr> 
   <td>Personnes<br/> </td> 
   <td>Nombre de profils d’utilisateurs et d’utilisatrices considérés comme profils cibles pour vos cartes de contenu.<br/> </td> 
</tr>
<tr> 
   <td>Clics uniques<br/> </td> 
   <td>Nombre de profils ayant cliqué sur le contenu de votre vignette de contenu.<br/> </td> 
</tr>
<tr> 
   <td>Affichages uniques<br/> </td> 
   <td>Nombre dʼouvertures du message, sans prendre en compte les interactions multiples dʼun même profil.<br/> </td> 
</tr>
 </tbody> 
</table>

## Mesures des pages web {#web}

<table> 
 <thead> 
  <tr> 
   <th> Mesure<br/> </th> 
   <th> Définition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Clics<br/> </td> 
   <td>Nombre de clics sur le contenu de vos pages web.<br/> </td> 
</tr>
<tr> 
   <td>Taux de clics (CTR)<br/> </td> 
   <td>Pourcentage d’utilisateurs et d’utilisatrices ayant interagi avec les pages web.<br/> </td> 
</tr>
<tr> 
   <td>Affichages<br/> </td> 
   <td>Nombre d’ouvertures de la page web.<br/> </td> 
</tr>
<tr> 
   <td>Personnes<br/> </td> 
   <td>Nombre de profils d’utilisateurs et d’utilisatrices considérés comme profils cibles pour vos pages web.<br/> </td> 
</tr>
<tr> 
   <td>Clics uniques<br/> </td> 
   <td>Nombre de profils qui ont cliqué sur le contenu de vos pages web.<br/> </td> 
</tr>
<tr> 
   <td>Affichages uniques<br/> </td> 
   <td>Nombre d’ouvertures de la page web, sans prendre en compte les interactions multiples d’un même profil.<br/> </td> 
</tr>
 </tbody> 
</table>

## Mesures d’expériences basées sur du code {#code-based}

<table> 
 <thead> 
  <tr> 
   <th> Mesure<br/> </th> 
   <th> Définition<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Clics<br/> </td> 
   <td>Nombre total de fois où des utilisateurs et des utilisatrices ont cliqué sur des expériences personnalisées qui leur ont été présentées.<br/> </td> 
</tr>
<tr> 
   <td>Taux de clic (CTR)<br/> </td> 
   <td>Pourcentage des utilisateurs et des utilisatrices qui cliquent sur un lien, une annonce publicitaire ou une recommandation par rapport au nombre d’affichages de ces derniers.<br/> </td> 
</tr>
<tr> 
   <td>Taux de conversion<br/> </td> 
   <td>Pourcentage d’affichages qui ont généré des actions de l’utilisateur ou de l’utilisatrice (par exemple, des clics), indiquant la capacité du modèle à générer de l’engagement des utilisateurs et des utilisatrices.<br/> </td> 
</tr>
<tr> 
   <td>Performances des éléments de décision<br/> </td> 
   <td>Évalue les performances de chaque élément concernant leur capacité à générer de l’engagement de la part des utilisateurs et des utilisatrices et à produire des actions souhaitées, telles que des achats, des clics ou d’autres types de réactions.<br/> </td> 
</tr>
<tr> 
   <td>KPI de prise de décision<br/> </td> 
   <td>Informations clés sur l’engagement des visiteurs et visiteuses avec les expériences, y compris le nombre total d’éléments, de clics, d’affichages au total et le taux d’offres de secours.<br/> </td> 
</tr>
<tr> 
   <td>Affichages<br/> </td> 
   <td>Nombre total de fois où des expériences personnalisées ont été affichées ou présentées aux utilisateurs et aux utilisatrices via les différents points de contact.<br/> </td> 
</tr>
<tr> 
   <td>Entonnoir d’engagement<br/> </td> 
   <td>Surveille les performances des expériences personnalisées en évaluant l’efficacité de chaque étape de l’entonnoir pour susciter des interactions des utilisateurs et des utilisatrices.<br/> </td> 
</tr>
<tr> 
   <td>Entonnoir d’engagement par stratégie de sélection<br/> </td> 
   <td>Surveille et analyse l’efficacité avec laquelle différentes stratégies de sélection impliquent les utilisateurs et utilisatrices avec des expériences personnalisées.<br/> </td> 
</tr>
<tr> 
   <td>Personnes<br/> </td> 
   <td>Nombre de profils d’utilisateurs et d’utilisatrices considérés comme profils cibles pour vos expériences basées sur du code.<br/> </td> 
</tr>
<tr> 
   <td>Stratégie de classement<br/> </td> 
   <td>Des informations sur les performances des modèles de classement basés sur l’IA comparant deux types de trafic : avec modèle et validation non-croisée.<br/> </td> 
</tr>
<tr> 
   <td>Principaux éléments de décision par rapport au CTR<br/> </td> 
   <td>Souligne les performances de chaque élément en fonction de son taux de clic (CTR), ce qui permet d’évaluer les éléments les plus efficaces pour engager les utilisateurs et les utilisatrices.<br/> </td> 
</tr>
<tr> 
   <td>Clics uniques<br/> </td> 
   <td>Nombre de profils qui ont cliqué sur le contenu de vos expériences basées sur du code.<br/> </td> 
</tr>
<tr> 
   <td>Affichages uniques<br/> </td> 
   <td>Nombre dʼouvertures de l’expérience, sans prendre en compte les interactions multiples dʼun même profil.<br/> </td> 
</tr>
 </tbody> 
</table>
