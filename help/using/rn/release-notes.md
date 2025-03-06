---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 155ae8ef14e5482d94e54b15962afa09aa6826fc
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 27%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour. [!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.


## Notes de mise à jour de février 2025 {#25-02-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**Date de publication** : 18 et 19 février 2025


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
<p>Vous pouvez désormais créer des règles métier à l’aide d’ensembles de règles. Les ensembles de règles sont des groupes de règles qui vous permettent de limiter les messages envoyés dans les campagnes et les actions de parcours sur plusieurs canaux, ainsi que de contrôler les entrées de profils dans les parcours.<p>
<p><ul><li>Créez des ensembles de règles de canal pour limiter le nombre de messages envoyés sur un ou plusieurs canaux. Appliquez-les à des campagnes ou à des actions de parcours pour appliquer les règles définies dans l’ensemble de règles. L’ensemble de règles de canal vous permet d’appliquer des règles de limitation en fonction des types de communication. Par exemple, définissez un ensemble de règles pour limiter les « messages promotionnels » et un autre pour les « newsletters ». Appliquez le jeu de règles approprié dans votre campagne ou action de parcours en fonction du type de communication que vous envoyez.</li>
<li> Créez des ensembles de règles de parcours pour contrôler les entrées de profil dans les parcours. Limiter la fréquence à laquelle un profil peut rejoindre un parcours au cours d’une période donnée ou le nombre de parcours auxquels un profil peut être inscrit simultanément. Appliquez-les au niveau du parcours pour assurer une bonne gestion des entrées.</li></p>
<p>Auparavant disponibles pour un ensemble d’organisations (LA), les règles métier sont désormais disponibles pour tous les utilisateurs (GA).</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/rule-sets.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Générer des pages de destination avec l’assistant d’IA</strong><br/></th>
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
<th><strong>Marques avec l’assistant AI (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir vos propres marques pour définir l’identité visuelle et verbale de votre marque. </p>
<p>Cette fonctionnalité est disponible en version bêta privée pour un nombre limité de clientes et clients. Elle sera progressivement disponible pour tous les clients dans les prochaines versions.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/brands.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Résolution des problèmes liés aux actions personnalisées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais valider une configuration d’action personnalisée en effectuant des appels API réels directement depuis Adobe Journey Optimizer. </p>
<p>Pour plus d’informations, consultez la <a href="../action/troubleshoot-custom-action.md">documentation détaillée</a>.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Évaluation d’audience flexible (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’évaluation flexible des audiences vous permet d’exécuter une tâche de segmentation à la demande pour des audiences sélectionnées, en vous assurant de toujours disposer des données d’audience les plus récentes avant de les cibler dans des parcours et des campagnes Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Pour plus d’informations, consultez la <a href="../audience/creating-a-segment-definition.md#flexible">documentation détaillée</a>.</p>
<p>Cette fonctionnalité est réservée à un nombre restreint d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Date de disponibilité : 28 janvier 2025</p>
</tr>
</tbody>
</table>
</table>


### Améliorations {#25-02-improvements}

Les améliorations ci-dessous accompagnent la mise à jour de février.

* **Parcours** - Vous pouvez désormais tester vos actions personnalisées en envoyant des appels d’API à partir de la section administration. Cette nouvelle fonctionnalité vous permet de résoudre les problèmes liés à vos actions personnalisées avant ou après leur utilisation dans un parcours. [En savoir plus](../action/troubleshoot-custom-action.md)

* **Durée de vie (TTL) du jeu de données** - À compter de ce mois-ci, un mécanisme de sécurisation de durée de vie (TTL) sera déployé vers les jeux de données générés par le système Journey Optimizer dans de nouveaux sandbox et de nouvelles organisations, comme suit :

   * 90 jours pour les données dans la banque de profils
   * 13 mois pour les données du lac de données

  Cette modification sera déployée dans les sandbox clients existants au cours d’une phase ultérieure.

  En savoir plus sur cette mise à jour dans [la FAQ dédiée](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Publipostage direct** - Un nouveau type de serveur, la zone d’entrée des données, est désormais pris en charge pour le routage des fichiers dans la configuration du canal de publipostage direct. [En savoir plus](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS** - Vous pouvez désormais gérer la diffusion de messages SMS à partir de points d’entrée multi-régionaux en remplaçant les URL de diffusion, de retour, d’entrée et de rappel. Pour ce faire, une nouvelle URL de remplacement de champ a été ajoutée à la configuration des informations d’identification d’API. Cette modification est disponible uniquement auprès du fournisseur Sinch. [En savoir plus](../sms/sms-configuration-sinch.md)

* **Personalization** (Date de disponibilité : 29 janvier 2025) - De nouvelles fonctions d’assistance date/heure sont disponibles dans l’éditeur de personnalisation. [En savoir plus](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **Configuration du canal e-mail** - Si vous gérez le consentement en dehors d’Adobe, vous pouvez désormais définir une adresse e-mail de désabonnement personnalisée et une URL de désabonnement en un clic personnalisée dans le cadre des paramètres de configuration de votre canal e-mail.[En savoir plus](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Prise de décision** (date de disponibilité : 28 janvier 2025) - La prise de décision prend désormais en charge les types de données d’objet lors de la modification du schéma du catalogue d’articles. [En savoir plus](../experience-decisioning/catalogs.md)

