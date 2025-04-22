---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour de 2025
description: Notes de mise à jour de 2025 pour Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: aa8c74de-748b-4947-a972-14703f6ab4a7
source-git-commit: 9d87d133bb580ebed94a265beded5895f7fd0301
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 94%

---

# Notes de mise à jour de 2025 {#release-notes-2025}

Cette page répertorie toutes les fonctionnalités et améliorations pour [!DNL Journey Optimizer] publiées en 2025.

## Notes de mise à jour de février 2025 {#25-02-rn}

**Date de publication** : 18 et 19 février 2025


### Nouvelles fonctionnalités {#25-02-features}

Les nouvelles fonctionnalités de cette version sont présentées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Créer et gérer des règles métier</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer des règles métier à l’aide de jeux de règles. Les jeux de règles sont des groupes de règles qui vous permettent de limiter les messages envoyés dans les campagnes et les actions de parcours sur plusieurs canaux, ainsi que de contrôler les entrées de profils dans les parcours.<p>
<p><ul><li>Créez des jeux de règles de canal pour limiter le nombre de messages envoyés sur un ou plusieurs canaux. Appliquez-les à des campagnes ou à des actions de parcours pour appliquer les règles définies dans le jeu de règles. Le jeu de règles de canal vous permet d’appliquer des règles de limitation en fonction des types de communications. Par exemple, définissez un jeu de règles pour limiter les « messages promotionnels » et un autre pour les « newsletters ». Appliquez le jeu de règles approprié dans votre campagne ou action de parcours en fonction du type de communication que vous envoyez.</li>
<li> Créez des jeux de règles de parcours pour contrôler les entrées de profil dans les parcours. Limitez la fréquence à laquelle un profil peut rejoindre un parcours au cours d’une période donnée ou le nombre de parcours auxquels un profil peut être inscrit simultanément. Appliquez-les au niveau du parcours pour assurer une bonne gestion des entrées.</li></ul></p>
<p>Disponibles auparavant pour un ensemble d’organisations (disponibilité limitée), les règles métier sont désormais disponibles pour tous les utilisateurs et utilisatrices (disponibilité générale). Les règles métier de domaine parcours restent disponibles uniquement pour un nombre restreint d’organisations (disponibilité limitée).</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/rule-sets.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Générer des pages de destination avec l’assistant AI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce à l’assistant d’IA, vous pouvez désormais concevoir du contenu attrayant pour vos pages de destination, notamment des conceptions de pages complètes, du texte personnalisé et des visuels personnalisés.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>Pour plus d’informations, consultez la <a href="../content-management/generative-lp.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Marques avec assistant AI (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais choisir vos propres marques pour définir l’identité visuelle et verbale de votre marque. </p>
<p>Cette fonctionnalité est disponible en version Private Beta pour un nombre limité de clientes et clients. Elle sera progressivement disponible pour l’ensemble de la clientèle dans les versions ultérieures.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/brands.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Résoudre les problèmes liés aux actions personnalisées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais valider une configuration d’action personnalisée en effectuant des appels API réels directement depuis Adobe Journey Optimizer. Cette nouvelle fonctionnalité vous permet de résoudre les problèmes liés à vos actions personnalisées avant ou après leur utilisation dans un parcours. </p>
<p>Pour plus d’informations, consultez la <a href="../action/troubleshoot-custom-action.md">documentation détaillée</a>.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Évaluation flexible des audiences (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’évaluation flexible des audiences vous permet d’exécuter une tâche de segmentation à la demande pour des audiences sélectionnées, en vous assurant de toujours disposer des données d’audience les plus récentes avant de les cibler dans des parcours et des campagnes Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Pour plus d’informations, consultez la <a href="../audience/creating-a-segment-definition.md#flexible">documentation détaillée</a>.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Date de disponibilité : 28 janvier 2025</p>
</tr>
</tbody>
</table>
</table>


### Améliorations {#25-02-improvements}

Les améliorations ci-dessous proviennent de la mise à jour de février.

* **Durée de vie du jeu de données (TTL)** : à compter de ce mois-ci, un mécanisme de sécurisation sur la durée de vie (TTL) sera déployé sur les jeux de données générés par le système Journey Optimizer dans les nouveaux sandbox et les nouvelles organisations comme suit :

   * 90 jours pour les données dans la banque de profils
   * 13 mois pour les données du lac de données

  Cette modification sera déployée sur les sandbox des clientes et clients existants au cours d’une phase ultérieure.

  En savoir plus sur cette mise à jour dans [les questions fréquentes](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Publipostage direct** : un nouveau type de serveur, la zone d’atterrissage des données, est désormais pris en charge pour le routage des fichiers dans la configuration du canal de publipostage direct. [En savoir plus](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS** : vous pouvez désormais gérer la diffusion de SMS à partir de points d’entrée multi-régionaux en remplaçant les URL de diffusion, de retour, d’entrée et de rappel. Pour ce faire, une nouvelle URL de remplacement de champ a été ajoutée à la configuration des informations d’identification d’API. Cette modification est disponible uniquement auprès du fournisseur Sinch. [En savoir plus](../sms/sms-configuration-sinch.md)

* **Personalisation** (date de disponibilité : 29 janvier 2025) : de nouvelles fonctions d’assistance date/heure sont disponibles dans l’éditeur de personnalisation. [En savoir plus](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **Configuration du canal e-mail** : si vous gérez le consentement en dehors d’Adobe, vous pouvez désormais définir une adresse e-mail de désabonnement personnalisée et une URL de désabonnement en un clic personnalisée dans les paramètres de configuration du canal e-mail.[En savoir plus](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Prise de décision** (date de disponibilité : 28 janvier 2025) : la prise de décision prend désormais en charge les types de données d’objet lors de la modification du schéma du catalogue d’éléments. [En savoir plus](../experience-decisioning/catalogs.md)
