---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
source-git-commit: c9fa07efd03e84bf38fb1d67fabba4b6066c4179
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 29%

---


# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter les dernières [mises à jour de la documentation](documentation-updates.md).

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
<p>Adobe Experience Platform vous permet de définir des relations entre les schémas afin d’utiliser un jeu de données comme table de recherche pour un autre. [!DNL Journey Optimizer] peut désormais exploiter les données provenant d’un schéma lié.</p>
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
<p>Vous pouvez maintenant définir une liste spécifique de sécurité d’envoi au niveau de l’environnement de test, afin d’avoir un environnement sûr à des fins de test. Sur une instance hors production, où des erreurs peuvent se produire, la liste autorisée vous garantit que vous n’avez aucun risque d’envoyer des messages indésirables à vos clients. Cette fonctionnalité est activée en utilisant les API de suppression.</p>
<p>Pour plus d'informations, consultez la <a href="allow-list.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Le taux de ralentissement global de tous les segments lus exécutés simultanément dans le même environnement de test est limité à 17 000 messages par seconde. [En savoir plus](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Le champ **Durée du cache** a été supprimé du volet de configuration de la source de données. [En savoir plus](datasource/about-data-sources.md)
* Pour les sources de données externes, une règle de limitation de 15 appels par seconde est maintenant définie automatiquement. [En savoir plus](configuration/external-systems.md#capping)
* Pour les parcours actifs, l’écran des propriétés du parcours affiche la date de publication et le nom de l’utilisateur qui a publié le parcours. [En savoir plus](building-journeys/journey-gs.md#change-properties)
* Dans l&#39;écran Liste des parcours, le filtre de type de parcours a été ajouté. [En savoir plus](user-interface.md#section_lgm_hpz_pgb)
* Le paramètre **[!UICONTROL Taux de limitation]** a été ajouté à l’activité Lecture de segment . [En savoir plus](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Prévisualiser et tester les messages**
* L’identité et l’espace de noms sont désormais visibles dans l’écran **[!UICONTROL Aperçu]**. [En savoir plus](preview.md#preview-your-messages)
* Le nombre d’emails de test pour les bons à tirer est désormais limité à 10.
* Les caractères autorisés pour le **préfixe de ligne d’objet** dans les bons à tirer sont désormais limités. [En savoir plus](preview.md#send-proofs)

**Éditeur d’expression de personnalisation**
* La liste déroulante Aide a été renommée et réorganisée.

### Correctifs

* Correction d’un problème qui entraînait la diffusion de messages en double pour la diffusion d’emails par lots.
* Les événements sont désormais générés en conséquence lorsque l’envoi d’emails n’est pas effectué une fois la période de reprise terminée.
* Correction d’un problème en raison duquel les informations IP manquaient dans l’écran Enregistrements PTR.
* La localisation dans le rail des offres dans l’éditeur d’expression est désormais implémentée.
* Correction d’un espacement incorrect dans les fenêtres contextuelles d’informations.
