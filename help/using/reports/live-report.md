---
title: Rapport dynamique
description: Découvrez comment utiliser les données du rapport dynamique
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 8dd48bb2-a805-4c46-a16c-c68173a9ac08
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 36%

---

# Prise en main du rapport dynamique {#live-report}

Utilisez le **[!UICONTROL rapport dynamique]** pour mesurer et visualiser en temps réel l’impact et les performances de vos parcours et de vos messages dans un tableau de bord natif.
Les données sont disponibles dans la variable **[!UICONTROL Rapport en direct]** dès que votre diffusion est envoyée ou que votre parcours est exécuté à partir de la variable **[!UICONTROL 24 dernières heures]** .

* Si vous souhaitez cibler un parcours dans le contexte d’un parcours, dans la variable **[!UICONTROL Parcours]** , accédez à votre parcours et cliquez sur le bouton **[!UICONTROL Afficher le rapport]** bouton .

   ![](assets/report_journey.png)

* Si vous souhaitez cibler une campagne, dans la variable **[!UICONTROL Campagnes]** , accédez à votre campagne et cliquez sur le bouton **[!UICONTROL Rapports]** bouton .

   ![](assets/report_campaign.png)

* Si vous souhaitez basculer entre le **[!UICONTROL Rapport global]** au **[!UICONTROL Rapport en direct]** pour votre diffusion, cliquez sur **[!UICONTROL 24 dernières heures]** dans le sélecteur d’onglets.

   ![](assets/report_3.png)

Pour obtenir la liste détaillée de chaque mesure disponible dans Adobe Journey Optimizer, reportez-vous à la section [cette page](#list-of-components-live).

## Personnalisation du tableau de bord {#modify-dashboard}

Vous pouvez modifier chaque tableau de bord de reporting en redimensionnant ou en supprimant des widgets. La modification des widgets n’a un impact que sur le tableau de bord de l’utilisateur actuel. Les autres utilisateurs voient leurs propres tableaux de bord ou ceux définis par défaut.

1. Choisissez si vous souhaitez exclure les événements de test de vos rapports avec la barre de bascule. Pour plus d’informations sur les événements de test, consultez [cette page](../building-journeys/testing-the-journey.md).

   Notez que l&#39;option **[!UICONTROL Exclure les événements de test]** n&#39;est disponible que pour les rapports de parcours.

   ![](assets/report_modify_6.png)

1. Pour redimensionner ou supprimer des widgets, cliquez sur **[!UICONTROL Modifier]**.

   ![](assets/report_modify_7.png)

1. Ajustez la taille des widgets en faisant glisser leur coin inférieur droit.

   ![](assets/report_modify_8.png)

1. Cliquez sur **[!UICONTROL Supprimer]** pour supprimer tout widget dont vous n’avez pas besoin.

   ![](assets/report_modify_9.png)

1. Une fois satisfait de l&#39;ordre d&#39;affichage et de la taille de vos widgets, cliquez sur **[!UICONTROL Enregistrer]**.

Votre tableau de bord est maintenant enregistré. Vos différentes modifications seront réappliquées pour une utilisation ultérieure de vos rapports dynamiques. Si nécessaire, utilisez l’option **[!UICONTROL Réinitialiser]** pour restaurer les widgets par défaut et leur ordre.

## Liste des composants {#list-of-components-live}

Les tableaux ci-dessous contiennent la liste des mesures utilisées dans les différents rapports et leur définition.

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
   <td>Actions exécutées<br/> </td> 
   <td> Nombre total d’actions exécutées avec succès pour un parcours.<br/> </td> 
</tr> 
  <tr> 
   <td> Profils entrés<br/> </td> 
   <td> Nombre total d’individus ayant atteint l’événement d’entrée du parcours.<br/> </td> 
</tr>
  <tr> 
   <td> Erreur lors de l’action<br/> </td> 
   <td>Nombre total d’erreurs qui se sont produites pour les actions.<br/> </td> 
</tr> 
  <tr> 
   <td> Profils sortis<br/> </td> 
   <td> Nombre total d’individus ayant quitté le parcours.<br/> </td> 
</tr> 
  <tr> 
   <td> Parcours individuel en échec<br/> </td> 
   <td> Nombre total de parcours individuels qui n’ont pas été exécutés avec succès.<br/> </td> 
</tr> 
 </tbody> 
</table>

### Mesures des emails et SMS   {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Mesure<br/> </th> 
   <th> Définition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> Bounces<br/> </td> 
   <td> Nombre total d'erreurs cumulées lors des diffusions et du traitement automatique des retours.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux de rebond<br/> </td> 
   <td> Pourcentage d'emails qui ont fait l'objet d'un bounce par rapport au nombre d'emails envoyés.<br/> </td> 
</tr>
  <tr> 
   <td> Clics<br/> </td> 
   <td> Nombre de clics sur un contenu dans un email.<br/> </td> 
</tr> 
  <tr> 
   <td> Délivrés <br/> </td> 
   <td> Nombre de messages envoyés avec succès.<br/></td> 
</tr> 
  <tr> 
   <td> Taux de diffusion<br/> </td> 
   <td> Pourcentage de messages envoyés avec succès.<br/> </td> 
</tr>
  <tr> 
   <td> Erreurs<br/> </td> 
   <td> Nombre total d'erreurs qui se sont produites au cours d'une diffusion et qui l'ont empêché d'être envoyée aux profils.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux d’erreur<br/> </td> 
   <td> Pourcentage d'erreurs qui se sont produites pendant une diffusion empêchant son envoi par rapport au nombre d'emails envoyés.<br/> </td> 
</tr>
  <tr> 
   <td> Exclu<br/> </td> 
   <td> Nombre de profils qui ont été exclus par Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Hard bounce<br/> </td> 
   <td> Nombre total d’erreurs permanentes, telles qu’une adresse email incorrecte. Un message d'erreur indique explicitement que l'adresse n'est pas valide, comme Utilisateur inconnu.<br/> </td>
</tr>
  <tr> 
   <td> Ignoré<br/> </td> 
   <td> Nombre total de messages temporaires, tels que Absence du bureau, ou une erreur technique, par exemple si le type d’expéditeur est Postmaster.<br/> </td> 
</tr>
   <tr> 
   <td>Taux de clics des offres<br/> </td> 
   <td>Pourcentage d'utilisateurs ayant interagi avec l'offre.<br/> </td> 
</tr>
   <tr> 
   <td>Taux d'impression des offres<br/> </td> 
   <td>Pourcentage d'offres ouvertes par rapport au nombre d'offres envoyées.<br/> </td> 
</tr>
   <tr> 
   <td>Nom de l’offre<br/> </td> 
   <td> Nom de l'offre ajoutée dans la diffusion. Pour plus d’informations sur les emplacements, consultez cette <a href="../offers/offer-library/creating-personalized-offers.md">page</a>.<br/> </td> 
</tr>
   <tr> 
   <td>Offre envoyée<br/> </td> 
   <td>Nombre total d'envois pour l'offre.<br/> </td> 
</tr> 
  <tr>
   <td>Ouvertures<br/> </td> 
   <td> Nombre d’ouvertures du message.<br/> </td> 
</tr> 
  <tr> 
   <td> Taux d’ouverture<br/> </td> 
   <td> Nombre total d'emails ouverts par rapport au nombre d'emails délivrés.<br/> </td> 
</tr>
  <tr> 
   <td>Nom de l’emplacement<br/> </td> 
   <td> Nom de l’emplacement utilisé pour afficher votre offre. Pour plus d’informations sur les emplacements, consultez cette <a href="../offers/offer-library/creating-placements.md">page</a>. </td> 
</tr> 
  <tr> 
   <td> Reprises<br/> </td> 
   <td> Nombre de courriers électroniques dans la file d’attente pour les reprises.<br/> </td> 
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
   <td> Nombre total de messages traités lors de l'analyse de la diffusion.<br/> </td> 
</tr> 
  <tr> 
   <td> Clics uniques<br/> </td> 
   <td> Nombre de destinataires ayant cliqué sur un contenu dans un email.<br/> </td> 
</tr> 
  <tr> 
   <td>Taux de clics uniques<br/> </td> 
   <td> Pourcentage d'utilisateurs ayant interagi avec la diffusion.<br/> </td> 
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

### Mesures de landing page {#landing-page-metrics}

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
   <td>Nombre de personnes qui n’ont pas interagi avec la landing page et n’ont pas effectué l’action d’inscription.<br/> </td> 
</tr>
 <tr> 
   <td>Taux de rebond<br/> </td> 
   <td>Nombre de personnes qui n’ont pas interagi avec la landing page et n’ont pas effectué l’action d’inscription.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Clics<br/> </td> 
   <td>Nombre de clics sur un contenu dans la landing page.<br/> </td> 
</tr>
 <tr> 
   <td>Taux de clics<br/> </td> 
   <td>Pourcentage de clics dans la landing page.<br/> </td>
</tr>
<tr>
<td>Conversion<br/> </td> 
   <td>Nombre de personnes ayant interagi avec la landing page, par exemple inscrites à un formulaire.<br/> </td> 
</tr>
<tr>
   <td>Taux de conversion<br/> </td> 
   <td>Nombre de personnes ayant interagi avec la landing page, par exemple inscrites à un formulaire.<br/> </td> 
</tr>
 <tr> 
   <td>Parcours(s)<br/> </td> 
   <td>Nombre de visites de votre landing page provenant d'un parcours.<br/> </td> 
</tr>
 <tr> 
   <td>Autres sources<br/> </td> 
   <td>Nombre de visites de votre page d’entrée provenant d’une source externe au lieu d’un parcours.<br/> </td> 
</tr>
 <tr> 
   <td>Nombre total de visites<br/> </td> 
   <td> Nombre total de visites de votre landing page provenant de parcours et de sources externes, y compris plusieurs visites d’un seul destinataire.<br/> </td> 
</tr>
 <tr> 
   <td>Visiteurs uniques<br/> </td> 
   <td>Nombre de personnes ayant consulté votre landing page, plusieurs visites d'un même destinataire ne sont pas prises en compte.<br/> </td> 
</tr>
 <tr> 
   <td>Visites<br/> </td> 
   <td>Nombre de visites sur votre landing page, y compris plusieurs visites d’un seul destinataire.<br/> </td> 
</tr>
 </tbody> 
</table>

