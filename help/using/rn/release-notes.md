---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d93b7ce225294257f49caee6ac08cfb575611a93
workflow-type: tm+mt
source-wordcount: '1122'
ht-degree: 45%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continue, ce qui permet à Adobe de diffuser régulièrement de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements.

En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles.  Une section dédiée [Dernières mises à jour](#updates-rn) met en évidence les nouvelles fonctionnalités et améliorations apportées lors de leur déploiement en production. Vous êtes ainsi toujours informé de tous les changements en temps réel. <!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Notes de mise à jour du 25 octobre {#oct-25-10-rn}

**Date de publication** : jeudi 22 octobre 2025

### Nouvelles fonctionnalités {#oct-25-10-features}

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
<p>Vous pouvez appliquer des heures calmes par le biais d’ensembles de règles, qui peuvent être affectés à des actions individuelles dans des campagnes ou des parcours pour un contrôle précis.</p>
<p>Actuellement, les règles relatives aux heures creuses ne sont disponibles que pour un ensemble d’organisations (disponibilité limitée). Pour être ajouté à la liste d’attente, contactez votre représentant Adobe.</p>
<img src="assets/do-not-localize/quiet-hour.gif">
<p>Pour plus d’informations, consultez la <a href="../conflict-prioritization/quiet-hours.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : jeudi 22 octobre 2025</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new Journey Optimizer API is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
<p>For more information, refer to the <a href="../start/get-started-sources.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table>-->

<!--table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<img src="assets/do-not-localize/FILE.gif">
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p>
<p>Availability date: October 22, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Messagerie à haut débit pour les campagnes par e-mail déclenchées par l’API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Un nouveau mode de messagerie transactionnelle à débit élevé est disponible dans les campagnes déclenchées par l’API. Ce mode est conçu pour les messages transactionnels en temps réel à grande échelle et prend en charge jusqu’à 5 000 transactions par seconde avec une disponibilité supérieure. Ce mode prend également en charge les messages transactionnels sans référencer ni créer de profils client, tels que le passage en caisse des invités, la confirmation de commande, les réinitialisations de mot de passe, les notifications de sécurité et autres notifications de service/exploitation.</p>
<p>Cette fonctionnalité n’est disponible que pour le canal e-mail, pour les organisations qui ont acheté l’offre complémentaire de messagerie transactionnelle à haut débit d’Adobe . Pour plus d’informations, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../campaigns/api-triggered-high-throughput.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : jeudi 22 octobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Règles de ciblage réutilisables</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Pour vous faire gagner du temps et économiser des efforts, Journey Optimizer vous permet désormais de créer des règles réutilisables à partir d’un menu d’interface utilisateur dédié et de les exploiter lors de la création de ciblage, dans le cadre de l’optimisation de contenu dans une campagne ou un parcours, dans l’activité Optimiser le parcours .</p>
<p>Les règles de ciblage sont actuellement en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour obtenir l’accès. Notez que cette fonctionnalité n’est disponible que pour les organisations qui ont acheté le module complémentaire Decisioning. Il sera progressivement déployé auprès de tous les clients.</p>
<img src="assets/do-not-localize/targeting-rules.gif">
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/rules.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : jeudi 22 octobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouvelles alertes de Parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De nouvelles alertes préconfigurées sont disponibles pour surveiller l’exécution de votre parcours :</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">Taux de rejet du profil dépassé </a> : ratio de rejets de profil par rapport aux profils entrés au cours des 5 dernières minutes ayant dépassé le seuil</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">Taux d’erreur des actions personnalisées dépassé</a> : ratio des erreurs d’actions personnalisées par rapport aux appels HTTP réussis au cours des 5 dernières minutes ayant dépassé le seuil</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">Taux d’erreur de profil dépassé</a> : ratio de profils en erreur par rapport aux profils saisis au cours des 5 dernières minutes qui a dépassé le seuil.</li></ul> <p>Vous pouvez modifier les valeurs de seuil et vous abonner à des alertes individuelles au niveau du parcours et non globalement.</p>
<p>Pour plus d’informations, consultez la <a href="../reports/alerts.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 14 octobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistant Métadonnées d’exécution</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle fonction d’assistance « executionMetadata » est disponible dans l’éditeur de personnalisation. Il vous permet d’ajouter des informations contextuelles à toute action native et de les capturer dans un jeu de données pour les exporter vers des systèmes externes.</p>
<p>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour obtenir l’accès.</p>
<img src="assets/do-not-localize/execution-metadata.gif">
<p>Pour plus d’informations, consultez la <a href="../personalization/functions/helpers.md#execution-metadata">documentation détaillée</a>.</p>
<p>Date de disponibilité : mardi 13 octobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Experimentation Accelerator avec l’agent d’expérience</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator comprend désormais l’agent d’expérimentation, un outil de conversation optimisé par l’IA qui vous permet d’interagir avec vos expériences, informations et opportunités. Elle améliore l’expérience Journey Optimizer Experimentation Accelerator, ce qui vous permet d’exécuter plus efficacement des expériences, de découvrir ce qui fonctionne et de découvrir où optimiser la suite.</p>
<p>Pour plus d’informations, consultez la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html" target="_blank">documentation détaillée</a>.</p>
<p>Date de disponibilité : samedi 10 octobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Pièces jointes PDF aux e-mails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais joindre un fichier PDF statique à un e-mail envoyé avec Journey Optimizer.</p>
<ul>
<li>Vous pouvez envoyer jusqu’à 6 messages avec une pièce jointe PDF par profil et par an.</li>
<li>La taille maximale autorisée pour chaque fichier joint est de 5 Mo.</li>
<li>Pour augmenter la taille ou le volume, vous pouvez acheter le module complémentaire Pièces jointes PDF. Pour plus d’informations, contactez votre représentant ou représentante Adobe.</li>
</ul>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../email/pdf-attachments.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 30 septembre 2025</p>
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
<p>Pour plus d’informations, consultez la <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">documentation détaillée</a>.</p>
<p>Date de disponibilité : 25 septembre 2025</p>
</td>
</tr>
</tbody>
</table>

<!--
## Latest updates {#updates-rn}

New capabilities and improvements released in the past weeks are listed below, with their availability date. They will be grouped with the next release notes content at the end of the month. See also the latest [release notes below](#latest-rn).
-->

### Améliorations {#updates-improvements}

<!--Availability date: October 22, 2025-->

**Champ d’exécution pour le canal WhatsApp**

Outre les e-mails et les SMS, vous pouvez savoir mettre à jour le champ d’exécution par défaut de vos diffusions WhatsApp au niveau du sandbox. Il est également possible de remplacer le champ d&#39;exécution défini globalement en le modifiant dans les paramètres avancés de l&#39;activité parcours WhatsApp ou dans la configuration du canal WhatsApp. [En savoir plus](../configuration/primary-email-addresses.md)

Date de disponibilité : jeudi 22 octobre 2025

**Prise en charge des attributs personnalisés avec l’adresse Mailto (désabonnement)**

Avec Journey Optimizer, si vous gérez le consentement en dehors d’Adobe, vous pouvez définir des points d’entrée personnalisés externes en définissant votre propre lien de désabonnement en un clic ainsi qu’une adresse e-mail de désabonnement personnalisée dans la configuration du canal e-mail. Lorsque les personnes destinataires cliquent sur le lien de désabonnement, Journey Optimizer ajoute certains paramètres par défaut, spécifiques au profil, à l’événement de mise à jour du consentement.

Pour personnaliser davantage vos points d’entrée personnalisés, vous pouvez maintenant définir des attributs personnalisés qui seront également ajoutés à l’événement de consentement. [En savoir plus](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Cette fonctionnalité est déjà disponible pour l’**[!UICONTROL URL de désabonnement en un clic]** personnalisée depuis août 2025 et est désormais disponible pour l’option **[!UICONTROL Mailto (désabonnement)]** en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour obtenir l’accès.

Date de disponibilité : 6 octobre 2025

### Bientôt disponible {#oct-25-10-soon}

La publication des fonctionnalités et améliorations suivantes est prévue dans les prochains jours. **Les informations peuvent faire l’objet de modifications**. Les liens, les écrans et la documentation mis à jour seront partagés une fois que ces mises à jour seront en production.

#### Nouvelles fonctionnalités {#oct-25-10-soon-features}

<table>
<thead>
<tr>
<th><strong>Thèmes dans le concepteur d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais appliquer rapidement des thèmes préapprouvés pour garantir la cohérence de la marque dans tous les e-mails, accélérer le processus de création de vos campagnes et produire de manière autonome des e-mails de haute qualité tout en réduisant la dépendance à l’égard des équipes de conception.</p>
<p>Publiée auparavant en version bêta, cette fonctionnalité est désormais disponible pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<!--img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p>Availability date: November 4, 2025</p-->
</td>
</tr>
</tbody>
</table>

#### Améliorations {#oct-25-10-soon-improvements}

**Prise de décision dans les e-mails via les modèles d’IA**

Vous pouvez désormais utiliser des modèles d’IA pour optimiser le meilleur contenu de votre e-mail grâce à l’utilisation de Decisioning. Par exemple, cette fonctionnalité vous permet de proposer le meilleur contenu en fonction d’événements personnalisés tels que des achats, des clics sur des boutons, des ajouts au panier, etc.

<!--
<table>
<thead>
<tr>
<th><strong>New Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports Web Push notifications, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app.</p>
<p>This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Custom action monitoring and reporting is now available. This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary, and Kobie loyalty apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>
-->
