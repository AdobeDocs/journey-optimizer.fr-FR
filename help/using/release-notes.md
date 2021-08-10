---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
source-git-commit: a1800c333bfbee178682d773c729aad7e23d86d0
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 94%

---


# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter les dernières [mises à jour de la documentation](documentation-updates.md).

## Version de juillet 2021 {#july-2021-release}

<table>
<thead>
<tr>
<th><strong>Utilisation des relations de schéma</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform vous permet de définir des relations entre les schémas afin d'utiliser un jeu de données comme table de choix pour un autre. [!DNL Journey Optimizer] peut maintenant exploiter les données provenant d'un schéma lié.</p>
<p>Ces champs sont disponibles dans la configuration d'événements unitaires, les conditions de parcours, la personnalisation des messages et la personnalisation d'actions personnalisées.</p>
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
<p>Vous pouvez maintenant définir une liste d'envoi sécurisé spécifique au niveau de l'environnement Sandbox, afin d'avoir un environnement sécurisé à des fins de test. Sur une instance hors production, où des erreurs peuvent se produire, la liste autorisée garantit que vous n'avez aucun risque d'envoyer des messages indésirables à vos clients. Cette fonctionnalité est activée en utilisant les API de suppression.</p>
<p>Pour plus d'informations, consultez la <a href="allow-list.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Le taux de limitation global de toutes les lectures de segment qui s&#39;exécutent simultanément dans le même environnement Sandbox est limité à 17 000 messages par seconde. [En savoir plus](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Le champ **Durée de mise en cache** a été supprimé du panneau de configuration de la source de données. [En savoir plus](datasource/about-data-sources.md)
* Pour les sources de données externes, une règle de limitation de 15 appels par seconde est maintenant définie automatiquement. [En savoir plus](configuration/external-systems.md#capping)
* Pour les parcours actifs, l’écran des propriétés du parcours affiche la date de publication et le nom de l’utilisateur qui a publié le parcours. [En savoir plus](building-journeys/journey-gs.md#change-properties)
* Dans l&#39;écran Liste des parcours, le filtre de type de parcours a été ajouté. [En savoir plus](user-interface.md#section_lgm_hpz_pgb)
* Le paramètre **[!UICONTROL Taux de limitation]** a été ajouté à l&#39;activité Lecture de segment. [En savoir plus](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Prévisualiser et tester les messages**

* L&#39;identité et l&#39;espace de noms sont maintenant visibles dans l&#39;écran **[!UICONTROL Aperçu]**. [En savoir plus](preview.md#preview-your-messages)
* Le nombre d&#39;e-mails de test pour les BAT est maintenant limité à 10.
* Les caractères autorisés pour le **préfixe de ligne d&#39;objet** dans les BAT sont maintenant limités. [En savoir plus](preview.md#send-proofs)

**Personnalisation de l&#39;éditeur d&#39;expression**

* La liste déroulante des helpers a été renommée et réorganisée.

### Correctifs

* Correction d&#39;un problème qui entraînait la diffusion de messages en double pour la diffusion d&#39;e-mails par lots.
* Les événements sont maintenant générés en conséquence lorsque l&#39;envoi d&#39;e-mails n&#39;est pas effectué une fois la période de reprise terminée.
* Correction d&#39;un problème en raison duquel les informations IP manquaient dans l&#39;écran Enregistrements PTR.
* La localisation est maintenant implémentée dans le rail des offres au sein de l&#39;éditeur d&#39;expression.
* Correction d&#39;un espacement incorrect dans les fenêtres contextuelles d&#39;informations.
* Correction d’un problème dans le concepteur d’emails lors du téléchargement d’un fichier HTML en raison duquel la feuille de style interne avec la propriété `background-image` n’était pas prise en charge.

