---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour préliminaires pour Journey Optimizer
description: Notes de mise à jour préliminaires pour Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1a5f6be689c9e91ee0dc0b5f024dbe8020424337
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 29%

---

# Notes de mise à jour préliminaires {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).


## Notes de mise à jour préliminaires du 25 octobre {#25-10-rn}

**Les notes de version préliminaire ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les notes de mise à jour, à la date de publication.

Voir également les [Notes de mise à jour préliminaires d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Date de publication** : 21-22 octobre 2025

### Nouvelles fonctionnalités {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>Canal Courrier dans parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Auparavant limité aux campagnes, le canal Publipostage direct est désormais disponible sur la zone de travail du parcours, ce qui vous permet d’incorporer le publipostage direct dans vos parcours. Le publipostage direct peut désormais être utilisé dans les scénarios de lot et de parcours 1:1, avec la prise en charge de la configuration de l’extraction de fichiers et des paramètres de fréquence basés sur le temps.</p>
<p> Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouvelle API pour récupérer les campagnes d’action</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle API Journey Optimizer est désormais disponible, ce qui vous permet de récupérer et d’inspecter par programmation les données liées à la campagne, telles que les détails, les versions et les configurations.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Surveillance et reporting des actions personnalisées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Cette fonctionnalité offre une meilleure visibilité sur l’intégrité et l’exécution du parcours, y compris le statut du cycle de vie et les alertes de performances. Vous pouvez désormais rapidement comprendre quand, où et pourquoi une situation anormale se produit dans une action personnalisée.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Messagerie de base RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec la nouvelle offre de module complémentaire RCS Basic, vous pouvez désormais diffuser des messages RCS (Rich Communication Services) de base dans Journey Optimizer, ce qui permet d’utiliser les fonctionnalités de messagerie améliorées suivantes, sous réserve de la prise en charge géographique et par le fournisseur :</p>
<ul>
<li><strong>Prise en charge des expéditeurs marqués et vérifiés :</strong> envoyez des messages à l’aide de profils professionnels vérifiés avec des éléments de branding (logo, nom de l’expéditeur, etc.).</li>
<li><strong>Informations sur la diffusion des messages :</strong> recevez des rapports de diffusion détaillés comprenant les mises à jour de l’état des messages (par exemple, envoyé, diffusé, lu).</li>
<li><strong>Suivi des liens :</strong> permet d’incorporer et de suivre les URL dans les messages RCS pour l’analyse de l’engagement.</li>
<li><strong>Secours aux SMS :</strong> secours automatique aux SMS lorsque l’appareil du destinataire ne prend pas en charge RCS ou est temporairement inatteignable via RCS.</li>
<li><strong>Composition de base du message :</strong> envoyez des messages RCS de base basés sur du texte.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal courrier dans les campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le canal Courrier est désormais disponible dans les campagnes orchestrées. L’activité Courrier facilite l’envoi de courrier depuis votre campagne orchestrée pour les messages ponctuels et récurrents. Elle permet d’automatiser le processus de génération du fichier d’extraction requis par les fournisseurs de services postaux. Vous pouvez combiner des activités de canal dans la zone de travail de campagne orchestrée afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouveaux connecteurs source pour les applications de fidélité</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De nouveaux connecteurs source sont désormais disponibles dans Adobe Experience Platform pour les applications de fidélité Talon.One, Capillary et Kobie. Ces connecteurs vous permettent de diffuser facilement des données de fidélité dans Adobe Experience Platform et d’exploiter ces données dans Journey Optimizer.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prise en charge de la prise de décision dans le canal e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais ajouter des politiques de décision dans des parcours et des campagnes par e-mail. Les politiques de décision sont des conteneurs pour vos offres qui tirent profit du moteur de prise de décision afin d’effectuer un rendu dynamique du meilleur contenu à diffuser, pour chaque membre de l’audience.</p>
<p> Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mode à débit élevé pour les campagnes par e-mail déclenchées par l’API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Un nouveau mode à débit élevé est désormais disponible dans les campagnes déclenchées par API. Ce mode est conçu pour la messagerie en temps réel à grande échelle (jusqu’à 5 000 transactions par seconde) et offre une disponibilité supérieure avec une latence plus faible.</p>
<p>Cette fonctionnalité n’est disponible que pour le canal e-mail, pour les organisations qui ont acheté l’offre complémentaire de messagerie transactionnelle à haut débit d’Adobe. Pour plus d’informations, contactez votre représentant ou représentante Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Heures calmes/exclusions temporelles</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les heures calmes vous permettent de définir des exclusions temporelles pour les canaux E-mail, SMS, Notification push et WhatsApp. Ils garantissent qu’aucun message n’est envoyé pendant des périodes spécifiques, ce qui vous aide à respecter les préférences des clients et les exigences de conformité.</p>
<p>Vous pouvez appliquer des heures calmes par le biais d’ensembles de règles, qui peuvent être affectés à des actions individuelles dans des campagnes ou des parcours pour un contrôle précis. En rationalisant ces processus.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouvelle fonction d’assistance de métadonnées d’exécution</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle fonction d’assistance executionMetadata est disponible dans l’éditeur de personnalisation. Il vous permet d’ajouter des informations contextuelles à toute action native et de les capturer dans un jeu de données pour les exporter vers des systèmes externes.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Date de disponibilité : 13 octobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Agent d’expérience</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’agent d’expérimentation est un outil optimisé par l’IA qui modernise la manière dont vous pouvez exécuter et gérer des expériences numériques sur des sites web, des e-mails, des messages push et des applications. Basé sur la plateforme d’IA et les outils d’expérimentation de Adobe Experience Platform, l’agent d’expérimentation vous permet d’exécuter des expériences plus efficacement, d’organiser les objectifs commerciaux et de générer des informations exploitables, en mettant en évidence ce qui a fonctionné, ce qui n’a pas fonctionné et où tester ensuite.</p>
<p>Dans le cadre de la nouvelle fonctionnalité d’Experimentation Accelerator, l’agent fournit :</p>
<ul>
<li><strong>Performances :</strong> une vue claire de ce qui s’est passé dans l’expérience.</li>
<li><strong>Insights :</strong> une explication de la raison pour laquelle les résultats se sont produits.</li>
<li><strong>Opportunités :</strong> conseils sur les prochaines actions à entreprendre</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Date de disponibilité : 9 octobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API publique pour récupérer les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle API Journey Optimizer est désormais disponible pour récupérer les parcours et leurs objets associés tels que les campagnes et les surfaces.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<p>Date de disponibilité : 25 septembre 2025</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

- **Campagnes, Experience Decisioning, Parcours**
   - **Sélectionner des règles réutilisables dans le ciblage** - Vous pouvez désormais tirer parti du créateur de règles lors de l’utilisation des règles de ciblage avec la fonctionnalité d’optimisation des messages dans les parcours et les campagnes. <!-- [Read more](../FILE.md) -->

- **Canal - WhatsApp**
   - **Champ d&#39;exécution pour le canal WhatsApp** - En plus des e-mails et des SMS, il est désormais possible de mettre à jour le champ d&#39;exécution par défaut de WhatsApp. Il est également possible de remplacer le champ d&#39;exécution défini globalement dans les paramètres avancés de l&#39;activité parcours WhatsApp ou dans la configuration du canal WhatsApp. <!-- [Read more](../FILE.md) -->

- **Autorisations**
   - **Le créateur du Parcours/de la campagne ne doit pas pouvoir approuver** - Ajout d’une option lors de la création ou de la définition de la stratégie d’approbation, pour empêcher les créateurs du Parcours/de la campagne d’approuver leurs propres objets. <!-- [Read more](../FILE.md) -->

- **Canal - Push**
   - **Mobile Live Activities - Private Beta** - Les activités en direct fournissent des mises à jour en temps réel et des expériences interactives dans les applications mobiles, ce qui permet aux utilisateurs et aux utilisatrices de rester informés des événements ou tâches en cours directement sur l’écran de leur appareil. Cette fonctionnalité améliore l’engagement en fournissant des informations en direct, telles que le suivi de la progression, les mises à jour d’événement ou le contenu interactif, sans que les utilisateurs aient à ouvrir l’application. <!-- [Read more](../FILE.md) -->

- **Parcours**
   - **New Parcours Alerts** - Date de disponibilité : 14 octobre 2025
De nouvelles alertes préconfigurées sont disponibles pour les parcours : Taux de rejet du profil dépassé (ratio des rejets de profil par rapport aux profils entrés au cours des 5 dernières minutes ayant dépassé le seuil), Taux d’erreur de l’action personnalisée dépassé (ratio des erreurs d’action personnalisée par rapport aux appels HTTP réussis au cours des 5 dernières minutes ayant dépassé le seuil), Taux d’erreur du profil dépassé (ratio des profils en erreur par rapport aux profils entrés au cours des 5 dernières minutes ayant dépassé le seuil). <!-- [Read more](../FILE.md) -->

- **Configuration**
   - **Prise en charge des attributs personnalisés avec une URL de désabonnement en un clic** - Date de disponibilité : 6 octobre 2025
Avec Journey Optimizer, si vous gérez le consentement en dehors d’Adobe, vous pouvez définir un point d’entrée personnalisé externe en définissant votre propre lien de désabonnement en un clic dans la configuration du courrier électronique. Lorsque vos destinataires cliquent sur le lien de désabonnement, Journey Optimizer ajoute certains paramètres par défaut spécifiques au profil à l’événement de mise à jour du consentement. Pour personnaliser davantage l’e-mail de désabonnement, vous pouvez maintenant définir des attributs personnalisés qui seront ajoutés à l’événement de consentement. Cette fonctionnalité est déjà disponible pour l’URL de désabonnement en un clic personnalisée depuis le 25 août. Elle est désormais disponible pour l’option Mailto (désabonnement) en disponibilité limitée. Contactez votre représentant Adobe pour obtenir l’accès. <!-- [Read more](../FILE.md) -->

- **Canal - E-mail**
   - **Pièces jointes de PDF aux e-mails** - Date de disponibilité : 30 septembre 2025
Vous pouvez désormais joindre un fichier PDF statique à un e-mail envoyé avec Journey Optimizer. Vous pouvez envoyer jusqu&#39;à 6 messages avec une pièce jointe PDF par profil et par an. La taille de fichier maximale autorisée pour chaque pièce jointe est de 5 Mo. Pour toute taille ou volume supplémentaire, vous pouvez acheter le module complémentaire de pièce jointe PDF . Pour plus d’informations, contactez votre représentant ou représentante Adobe.

  >[!AVAILABILITY]
  >
  >Publiée précédemment en disponibilité limitée, cette amélioration est désormais disponible dans tous les environnements (disponibilité générale).

  <!-- [Read more](../FILE.md) -->

