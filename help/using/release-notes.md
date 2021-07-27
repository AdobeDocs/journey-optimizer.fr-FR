---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
source-git-commit: 4d3352184aac7fe19096c21650982e29506f2bff
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 40%

---


# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations de Journey Optimizer.
Vous pouvez également consulter les dernières [mises à jour de la documentation](documentation-updates.md).

## Version de juillet 2021 {#july-2021-release}

<table>
<thead>
<tr>
<th><strong>Utilisation des relations de schéma</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform vous permet de définir des relations entre les schémas afin d’utiliser un jeu de données comme table de recherche pour un autre. Journey Optimizer peut désormais exploiter les données provenant d’un schéma lié.</p>
<p>Ces champs sont disponibles dans la configuration unitaire des événements, les conditions de parcours, la personnalisation des messages et la personnalisation des actions personnalisées.</p>
<p>Pour plus d'informations, consultez la <a href="event/experience-event-schema.md#leverage_schema_relationships">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Liste autorisée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant définir une liste de sécurité d’envoi spécifique au niveau des environnements de test afin d’éviter d’envoyer des emails indésirables à vos destinataires dans un environnement de test, par exemple.
</p>
<p>Pour plus d'informations, consultez la <a href="allow-list.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

* Le taux de ralentissement global de tous les segments lus exécutés simultanément dans le même environnement de test est limité à 17 000 messages par seconde. [En savoir plus](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Le champ **Durée du cache** a été supprimé du volet de configuration de la source de données. [En savoir plus](datasource/about-data-sources.md)
* Pour les sources de données externes, une règle de limitation de 15 appels par seconde est maintenant définie automatiquement. [En savoir plus](configuration/external-systems.md#capping)
* Pour les parcours actifs, l’écran des propriétés du parcours affiche maintenant la date de publication et le nom de l’utilisateur qui a publié le parcours. [En savoir plus](building-journeys/journey-gs.md#change-properties)
* Dans l&#39;écran Liste des parcours, le filtre de type parcours a été ajouté. [En savoir plus](user-interface.md#section_lgm_hpz_pgb)
* Le paramètre [!UICONTROL Taux de limitation] a été ajouté à l’activité Lecture de segment . [En savoir plus](building-journeys/read-segment.md#configuring-segment-trigger-activity)
