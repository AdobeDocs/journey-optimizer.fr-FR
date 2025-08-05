---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour préliminaires de Journey Optimizer
description: Notes de mise à jour préliminaires de Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 46%

---

# Notes de mise à jour préliminaires {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

**Les notes de mise à jour préliminaires ci-dessous peuvent être modifiées sans préavis jusqu’à la date de disponibilité de la version**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md) à la date de publication.


## Notes de mise à jour préliminaires du 25 août {#25-7-rn}

**Les notes de mise à jour préliminaires ci-dessous peuvent être modifiées sans préavis jusqu’à la date de disponibilité de la version**. Les liens, les copies d’écran et la documentation mise à jour sont publiés à la date de publication.

Voir également les [notes de mise à jour préliminaires de Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Date de publication** : mercredi 19 août 2025


### Nouvelles fonctionnalités {#Aug-25-8-features}

Les nouvelles fonctionnalités de cette version sont présentées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Suspendre et reprendre les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant suspendre et reprendre les parcours. Cette fonctionnalité offre aux concepteurs et conceptrices du parcours un meilleur contrôle et une plus grande flexibilité en leur permettant de suspendre temporairement les parcours actifs sans perturber l’expérience client. Lorsque le parcours est suspendu, aucune communication n’est envoyée et les profils restent suspendus jusqu’à la reprise du parcours.</p>
<p>Vous pouvez suspendre et reprendre un seul parcours ou un groupe de parcours par le biais d’opérations en bloc.</p>
<p>En outre, vous pouvez appliquer des filtres globaux aux parcours suspendus afin d’exclure les profils en fonction de leurs attributs.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Auparavant disponible pour un nombre limité de clientes et clients (disponibilité limitée), cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-pause.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Mode Calendrier</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une vue Calendrier est désormais disponible dans les listes des parcours et des campagnes. Elle vous permet de visualiser toutes les activations de parcours et de campagnes dans les listes respectives.</p>
<p>Auparavant disponible en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements. Avec cette version de disponibilité générale, la fonctionnalité inclut :</p>
<ul>
<li>Améliorations de la conception pour la navigation dans les dates</li>
<li>La possibilité de voir les brouillons de campagne si vous avez défini une date de début et de fin</li>
<li>Nouveau paramètre permettant de masquer et d’afficher les éléments de calendrier s’exécutant depuis longtemps</li>
</ul>
<img src="assets/do-not-localize/calendar.gif">
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-ui.md#journeys-calendar">documentation détaillée</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Mode sombre dans le Concepteur d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Designer d’e-mail de Journey Optimizer permet désormais de passer en mode sombre, où vous pouvez définir des paramètres personnalisés spécifiques qui s’afficheront uniquement pour les destinataires qui lisent leurs e-mails en mode sombre.</p>
<p>Prenez note des points suivants :</p>
<ul>
<li>Le rendu final en mode sombre peut varier et dépend du client de messagerie du destinataire.</li>
<li>Les clients de messagerie ne prennent pas tous en charge le mode sombre personnalisé. De plus, certains clients de messagerie appliquent uniquement leur propre mode sombre par défaut pour tous les e-mails reçus. Dans les deux cas, le rendu des paramètres personnalisés que vous avez définis dans le Concepteur d’e-mail ne pourra pas être affiché.</li>
</ul>
<P>Cette fonctionnalité est actuellement en version Beta et disponible uniquement pour les clientes et clients Beta. Pour rejoindre le programme bêta, contactez votre représentant ou représentante Adobe.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../email/dark-mode.md">documentation détaillée</a>. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Optimisation des campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer vous fournit désormais les outils nécessaires pour diffuser du contenu personnalisé et optimisé à l’audience de vos campagnes. Vous pouvez ainsi exécuter des expériences de contenu, créer un ciblage basé sur des règles et utiliser des combinaisons avancées des deux pour maximiser l’efficacité de vos campagnes.</p>
<p>Avec l’optimisation, vous pouvez :</p>
<ul>
<li>Testez plusieurs variations de contenu pour identifier le message le plus efficace.</li>
<li>Diffusez du contenu personnalisé en fonction des attributs de l’utilisateur et des données contextuelles.</li>
<li>Combinez le ciblage et l’expérimentation pour obtenir des stratégies de campagne avancées.</li>
<li>Filtrez les utilisateurs qui ne correspondent pas aux critères de variante.</li>
<li>Garantissez des mécanismes de secours pour maintenir l’interaction client.</li>
</ul>
<P>Une fois la campagne active, les profils sont évalués en fonction des critères définis. Ensuite, en fonction des critères correspondants, ils sont diffusés avec l’expérience ou le contenu approprié de la campagne.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p-->
</td>
</tr>
</tbody>
</table>

### Améliorations {#Aug-25-8-improv}

Les améliorations de cette version sont présentées ci-dessous.