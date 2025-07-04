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
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '3117'
ht-degree: 100%

---

# Notes de mise à jour de 2025 {#release-notes-2025}

Cette page répertorie toutes les fonctionnalités et améliorations pour [!DNL Journey Optimizer] publiées en 2025.


## Notes de mise à jour de mai 2025 {#25-5-rn}

<!--**Release date**: May 20-21, 2025-->

### Nouvelles fonctionnalités {#25-05-features}

Les nouvelles fonctionnalités de cette version sont présentées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Vue Calendrier pour l’inventaire des campagnes et des parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une vue Calendrier est désormais disponible dans les listes des parcours et des campagnes. Elle vous permet de visualiser toutes les activations de parcours et de campagnes dans les listes respectives.</p>
<p>Ce changement n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour demander l’accès, utilisez <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">ce formulaire</a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Pour plus d’informations, reportez-vous aux sections suivantes : <a href="../building-journeys/journey-ui.md">Parcourir et filtrer vos parcours</a>, <a href="../campaigns/modify-stop-campaign.md">Accéder aux campagnes</a>.</p>
<p>Date de disponibilité : 28 mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Intégration de fragments de contenu Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce à l’intégration d’Adobe Experience Manager et d’Adobe Journey Optimizer, vous pouvez désormais utiliser facilement des fragments de contenu Adobe Experience Manager dans votre contenu Journey Optimizer. Cette connexion transparente facilite l’accès et l’utilisation de votre contenu AEM directement dans Journey Optimizer.</p>
<p>Auparavant disponible pour un nombre limité d’organisations (LA), cette fonctionnalité est désormais disponible en version GA avec l’amélioration suivante : vous pouvez maintenant définir des espaces réservés et mapper des valeurs de personnalisation dans la signature du fragment à l’aide du mode Éditeur.</p>
<ul>
<!--li>Create offers by directly selecting an AEM Content Fragment.</li>
<li>Define placeholders and map personalization values within the fragment signature using the Editor mode.</li-->
</ul>
</br>
<img src="assets/do-not-localize/content-fragment.gif">
<p>Pour plus d’informations, consultez la <a href="../integrations/aem-fragments.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 23 mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Intégration d’Adobe Experience Manager Dynamic Media</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les ressources Dynamic Media sont désormais directement disponibles et accessibles dans Journey Optimizer. Cette intégration vous permet d’effectuer les opérations suivantes :</p>
<ul>
<li>Gérez de manière centralisée des ressources avec mises à jour en temps réel.</li>
<li>Modifiez instantanément les paramètres de vos ressources, tels que la largeur et la hauteur.</li>
<li>Personnalisez des modèles Dynamic Media en mettant à jour votre contenu et en ajoutant des champs de personnalisation.</li>
</ul>
</br>
<img src="assets/do-not-localize/dynamic_media_template_html.gif">
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../integrations/aem-dynamic.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 23 mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>ID supplémentaire pour les parcours déclenchés par un événement</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais déclencher des parcours à l’aide d’un identifiant de profil ainsi que d’un autre identifiant, tel qu’un identifiant de commande, d’abonnement ou de prescription, ce qui permet au même profil de se trouver plusieurs fois dans le même parcours à la fois. Cela permet des scénarios tels que la gestion de plusieurs commandes ou abonnements en parallèle, chaque instance suivant son propre chemin d’accès dans le parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/supplemental-identifier.md">documentation détaillée</a>.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Date de disponibilité : 23 mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simuler des variations de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<!--p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p-->
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements. Avec la sortie en disponibilité générale, la fonctionnalité prend désormais en charge le contenu multilingue et les expériences de contenu, ce qui vous permet de tester des variations dans différentes langues et configurations. En outre, elle prend désormais en charge les attributs contextuels (en plus des attributs de profil), ce qui permet d’effectuer des tests de contenu encore plus dynamiques et situationnels.</p>
<img src="assets/do-not-localize/variants.gif">
<p>Pour plus d’informations, consultez la <a href="../test-approve/simulate-sample-input.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 23 mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Synchroniser le planning de lecture d’audience avec la tâche de segmentation par lots</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais déclencher des parcours quotidiens après la fin de la segmentation par lots. Cette option est désormais disponible dans les parcours planifiés quotidiennement pour toute la clientèle. Cette option vous permet de définir une fenêtre temporelle allant jusqu’à 6 heures pour attendre les données d’audience des tâches de segmentation par lots, en vous assurant que les parcours s’exécutent avec les données les plus récentes ou sont ignorés s’ils ne sont pas prêts.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
<p>Pour plus d’informations, consultez la <a href="../building-journeys/read-audience.md#schedule">documentation détaillée</a>.</p>
<p>Date de disponibilité : 20 mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Fournisseur de SMS personnalisé</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer vous permet désormais de configurer des fournisseurs SMS supplémentaires au-delà des options par défaut : Sinch, Infobip et Twilio. Grâce à la configuration personnalisée des fournisseurs SMS, vous pouvez intégrer directement des fournisseurs tiers, utiliser la personnalisation avancée de la payload pour la messagerie dynamique et gérer les préférences de consentement (opt-in/opt-out) pour garantir la conformité.</p>
<p>Pour plus d’informations, consultez la <a href="../sms/sms-configuration-custom.md">documentation détaillée</a>.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p>Date de disponibilité : 20 mai 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

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
<p>Cette fonctionnalité est actuellement en version Beta et disponible uniquement pour les clientes et clients Beta. Pour rejoindre le programme bêta, contactez votre représentant ou représentante Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Pour plus d’informations, consultez la <a href="../email/apply-email-themes.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 14 mai 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prise de décision : nouveau créateur de formules IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer des formules de classement de prise de décision spécifiques en définissant et en combinant des critères à partir d’une nouvelle interface améliorée. Au lieu de vous fier uniquement à une priorité d’offre statique, vous pouvez définir des formules de classement personnalisées qui combinent les scores du modèle d’IA, les priorités d’offre, les attributs de profil, les attributs d’offre et les signaux contextuels par le biais d’une interface guidée.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/ranking/ranking-formulas.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 14 mai 2025</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#25-05-improv}

Les améliorations de cette version sont présentées ci-dessous.


* **Nouvelle prise en charge des objets de campagne pour la copie dans les sandbox** - Date de disponibilité : 15 mai 2025

  Lors de la copie de campagnes sur plusieurs sandbox à l’aide des fonctionnalités d’export et d’import de package, les dépendances suivantes sont désormais également copiées : configurations de canal, variantes et paramètres d’expérience, politiques et éléments de décision. [En savoir plus](../configuration/copy-objects-to-sandbox.md)

* **Dossiers pour les pages de destination** - date de disponibilité : 9 mai 2025

  Pour gérer facilement les pages de destination, vous pouvez désormais utiliser des dossiers pour mieux les organiser dans une hiérarchie structurée. [En savoir plus](../landing-pages/manage-lp.md)

* **Courrier : prise en charge de la clé SSH pour les connexions SFTP** - date de disponibilité : 5 mai 2025

  Dans la configuration du routage des fichiers de courrier, outre le type d’authentification SFTP avec mot de passe existant, vous pouvez désormais exporter votre fichier de courrier vers un serveur SFTP avec authentification par clé SSH. [En savoir plus](../direct-mail/direct-mail-configuration.md)

* **Activation des pastilles pour la personnalisation** - date de disponibilité : 5 mai 2025

  Le nouveau bouton « Pastilles » a été ajouté à l’éditeur de personnalisation. Une fois activés, les attributs de profil et contextuels s’affichent sous forme de pastilles, ce qui améliore la lisibilité de votre code. [En savoir plus](../personalization/personalization-build-expressions.md#options)

  >[!AVAILABILITY]
  >
  >Cette fonctionnalité sera progressivement déployée dans tous les environnements au cours des 30 prochains jours.

* **Prise en charge de la « redirection vers une URL » dans le canal web** - Date de disponibilité : 20 mai 2025

  Le canal web Journey Optimizer vous permet désormais de rediriger les visiteurs et visiteuses vers une autre URL existante plutôt que de créer une nouvelle variation dans l’éditeur visuel. Cette fonctionnalité peut être utilisée pour exécuter des expériences en comparant deux pages complètement différentes au lieu de simplement modifier quelques éléments dans une page. [En savoir plus](../web/create-web.md#web-redirect-to-url)

* **Dossiers pour les modèles et fragments** - Date de disponibilité : 20 mai 2025

  Les dossiers vous permettent d’organiser vos objets plus facilement et plus efficacement dans une hiérarchie structurée. Auparavant disponibles pour un certain nombre d’organisations (disponibilité limitée), les dossiers sont désormais accessibles à tous les utilisateurs et utilisatrices (disponibilité générale) pour gérer les modèles et fragments de contenu. Pour en savoir plus, consultez les sections [Modèles de contenu](../content-management/access-content-templates.md#folders) et [Fragments](../content-management/manage-fragments.md#folders).

* **Suivi des clics dans les modèles d’e-mail** - Date de disponibilité : 20 mai 2025

  Le suivi des clics sur les éléments `<area>` dans les cartes d’image des contenus d’e-mail est désormais pris en charge de manière native dans [!DNL Journey Optimizer]. Cela permet de s’assurer que les zones cliquables reçoivent le même modèle, les mêmes données de suivi et les mêmes paramètres ajoutés que les liens hypertexte standard. [En savoir plus sur le suivi des messages](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Rail droit dans la liste des campagnes** - Date de disponibilité : 20 mai 2025

  Dans la liste des campagnes, la sélection d’une campagne ouvre désormais un volet affichant ses détails.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.-->

<!--* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->



## Notes de mise à jour d’avril 2025 {#25-4-rn}

**Date de publication** : 29-30 avril 2025

### Nouvelles fonctionnalités {#25-04-features}

Les nouvelles fonctionnalités de cette version sont présentées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Éditeur de personnalisation - Apprendre par la pratique</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Un terrain de jeu de personnalisation est désormais disponible, où vous pouvez tester les expressions de personnalisation. Il vous permet d’explorer des exemples de modèles et de payloads pour que vous puissiez commencer vos propres expressions de personnalisation et les tester.</p>
<p>Pour plus d’informations, consultez la <a href="../personalization/personalize.md#playground">documentation détaillée</a>.</p>
<p>Date de disponibilité : 24 avril 2025</p>
<img src="assets/do-not-localize/templating-playground.gif"/>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Adobe Experience Manager as a Cloud Service integration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The integration between Adobe Journey Optimizer and Adobe Experience Manager as a Cloud Service is now released in General Availability (GA). This integration enables seamless content sourcing and management for personalized customer journeys.</p>
<p>For more information, refer to the <a href="../integrations/aem-templates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--<table>
<thead>
<tr>
<th><strong>Simulate content variations (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously available in beta, content variations simulation is now generally available (GA). It allows you to preview different variations of your content using sample input data uploaded from a CSV or JSON file or added manually. All the attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>With the General Availability release, the feature now includes support for multilingual content and content experiments, enabling you to test variations across different languages and treatments. Additionally, it now supports contextual attributes (in addition to profile attributes), allowing for even more dynamic and situational content testing.</p>
<img src="assets/do-not-localize/variants.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Canal LINE</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer a étendu ses fonctionnalités cross-canal afin d’inclure la prise en charge du canal LINE. Cette amélioration vous permet de créer, de modifier et de prévisualiser des expériences LINE offrant des interactions davantage personnalisées et plus attrayantes. Avec LINE, vous pouvez entrer en contact avec davantage de clientes et clients, envoyer du contenu pertinent et améliorer votre engagement.</p>
<p>Le canal LINE est activé sur demande pour les clientes et clients Adobe Journey Optimizer. Pour activer la fonctionnalité pour votre organisation, contactez l’assistance clientèle d’Adobe ou votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../line/get-started-line.md">documentation détaillée</a>.</p></td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Custom SMS provider (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports custom SMS providers, allowing you to integrate your preferred SMS services for enhanced communication flexibility.</p>
<p>For more information, refer to the <a href="../sms/sms-configuration-custom.md">detailed documentation</a>.</p></td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Mesures de parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les mesures de parcours vous permettent de mesurer l’impact de vos activités sur les mesures les plus importantes de votre entreprise et de fournir des informations plus claires sur vos performances.</p>
</br>
<img src="assets/do-not-localize/success-metric.gif"/>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/success-metrics.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 9 avril 2025</p>
</td>
</tr>
</tbody>
</table>



<!--<table>
<thead>
<tr>
<th><strong>Calendar view for campaign and journey inventory (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new calendar view is now available for campaigns and journey activations. This feature provides a visual representation of scheduled activities, allowing you to view and manage your campaigns and journeys more effectively. Selecting a calendar item opens a right rail with detailed information. This feature is currently in Limited Availability.</p>
<img src="assets/do-not-localize/calendar.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Intégration d’Adobe Express (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer s’intègre désormais à Adobe Express, ce qui vous permet de connecter facilement vos ressources de création à l’orchestration de parcours. Cette intégration simplifie le processus de conception et de déploiement de contenu personnalisé dans les campagnes. </p>
<p>Cette intégration n’est actuellement pas disponible pour une utilisation avec Healthcare Shield ou Privacy and Security Shield.</p>
<img src="assets/do-not-localize/express_resize.gif">
<p>Pour plus d’informations, consultez la <a href="../integrations/express.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Le parcours quotidien Déclencheur s’exécute après la fin de la segmentation par lots (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Pour les parcours planifiés par jour, une nouvelle option vous permet de définir une fenêtre temporelle allant jusqu’à 6 heures pour attendre les données d’audience des tâches de segmentation par lots, en vous assurant que les parcours s’exécutent avec les données les plus récentes ou sont ignorés s’ils ne sont pas prêts. L’option Déclencheur après l’évaluation de l’audience par lots n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/read-audience.md#schedule">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/trigger-journeys.gif">
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Themes in the Email Designer (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply pre-approved styling themes to your email content to ensure brand consistency across all emails, speed up your campaign creation process and independently produce hight-quality emails while reducing dependency on design teams.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Score d’alignement de la marque (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le score d’alignement de la marque fournit des commentaires clairs directement dans le concepteur d’e-mail, ce qui vous permet de vérifier que votre contenu correspond au ton, au style et aux règles de votre marque. Cette fonctionnalité est actuellement en version Beta.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/brands-score.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/brand-score.gif">
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decisioning - New AI formula builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create specific Decisioning ranking formulas by defining and combining criteria from a new improved interface. Ranking formulas allow you to define rules that will determine which decision items should be presented first, rather than taking into account the priority scores.</p>
<p>For more information, refer to the <a href="../content-management/brands-score.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/formula-builder.gif">
<p>Availability date: May 5, 2025</p>
</td>
</tr>
</tbody>
</table>
-->

### Améliorations {#25-04-improv}

**API d’aperçu des campagnes**

De nouvelles API sont disponibles pour prévisualiser les campagnes, en plus des fonctionnalités existantes d’envoi de BAT. [En savoir plus](https://developer.adobe.com/journey-optimizer-apis/references/simulations/#operation/createCampaignPreview){target="_blank"}.

**Outils relatifs aux sandbox**

* **Outils relatifs aux sandbox pour les actions personnalisées**

  Les actions personnalisées sont désormais incluses dans la liste des objets Adobe Journey Optimizer qui peuvent être copiés à l’aide de la fonctionnalité d’outils relatifs aux sandbox, ce qui simplifie les tests et le déploiement. [En savoir plus](../configuration/copy-objects-to-sandbox.md)

* **Outils relatifs aux sandbox** - Date de disponibilité : 3 avril 2025

  Vous pouvez désormais copier des campagnes dans plusieurs sandbox à l’aide des fonctionnalités d’export et d’import de packages. Les campagnes sont copiées avec tous les éléments liés au profil, à l’audience, au schéma, aux messages en ligne et aux objets dépendants. Certains éléments ne sont pas copiés, tels que les éléments de décision, les libellés d’utilisation des données et les paramètres de langue. [En savoir plus](../configuration/copy-objects-to-sandbox.md#custom-actions)

**Personnalisation**

* **Nouvel attribut contextuel**

  Un nouvel attribut contextuel, **ID de profil du message**, est disponible dans l’éditeur de personnalisation. Il s’agit d’un attribut orienté message qui identifie de manière unique chaque message envoyé à chaque profil ciblé dans une diffusion. Cet identifiant unique peut notamment être utilisé comme paramètre de tracking des URL pour distinguer chaque lien ouvert ou sur lequel les destinataires ont cliqué.

* **Attributs renseignés dans le volet Attributs** - Date de disponibilité : 2 avril 2025

  Le volet Attributs de l’éditeur de personnalisation affiche désormais uniquement les attributs renseignés par défaut. Pour afficher tous les attributs, utilisez le bouton des paramètres pour activer ou désactiver l’option **[!UICONTROL Afficher uniquement les attributs renseignés]**. [En savoir plus](../personalization/personalization-build-expressions.md)

**Canal e-mail**

* **Tracking personnalisé des URL** - Date de disponibilité : 30 avril 2025

  Pour plus de flexibilité et de contrôle sur vos paramètres d’e-mail, vous pouvez désormais personnaliser tous vos paramètres de suivi des URL en même temps au niveau de la configuration des canaux e-mail, au lieu de le faire dans le concepteur d’e-mail pour chaque lien de votre contenu. [En savoir plus](../email/surface-personalization.md#personalize-url-tracking)

* **Concepteur d’e-mail** - Date de disponibilité : 1er avril 2025

  Pour améliorer l’accessibilité dans Journey Optimizer, deux nouveaux champs sont désormais disponibles dans le concepteur d’e-mail : ils correspondent à l’élément `<title>` et à l’attribut `lang` dans l’élément `<html>` du contenu de votre e-mail. Vous pouvez définir ces paramètres en plus du champ **[!UICONTROL Pré-en-tête]**, dans la section **[!UICONTROL Corps]** de l’e-mail. [En savoir plus](../email/email-metadata.md)

**Playbooks de cas d’utilisation**

* **Création et partage de playbooks (Private Beta)** : vous pouvez désormais créer, gérer et partager vos propres playbooks de cas d’utilisation. Actuellement, cette fonctionnalité n’est disponible que pour un ensemble d’organisations sous la forme d’une version Private Beta. Pour en bénéficier, contactez votre représentant ou représentante Adobe. [En savoir plus](../start/playbooks.md)

**Navigation**

* **Gestion de contenu** - Date de disponibilité : 2 avril 2025

  Pour gérer facilement vos fragments et vos modèles de contenu, vous pouvez désormais utiliser des dossiers pour mieux les organiser dans une hiérarchie structurée. Pour en savoir plus, consultez les sections [Modèles de contenu](../content-management/access-content-templates.md#folders) et [Fragments](../content-management/manage-fragments.md#folders).

  >[!AVAILABILITY]
  >
  >Cette amélioration est disponible uniquement pour un ensemble d’organisations (disponibilité limitée).

<!--- **Folders for content templates and fragments** - Availability date: May 5, 2025

  Previously available for a set of organizations (LA), folders are now available to all users (GA) to manage their content templates and fragments. Folders let you organize your content templates and fragments more easily and effectively into a structured hierarchy.



<!--- **Right rail in campaigns list**  

  A right rail has been added to the campaigns list, providing detailed information when a campaign is selected.-->

<!--**Playbooks**

- **Create your own playbooks (Beta)**
  
  You can now create your own playbooks in Adobe Journey Optimizer, enabling greater customization and flexibility in journey planning.-->



## Notes de mise à jour de mars 2025 {#25-3-rn}

### Nouvelles fonctionnalités {#25-03-features}

Les nouvelles fonctionnalités de cette version sont présentées ci-dessous.

<!--table>
<thead>
<tr>
<th><strong>Integration with Adobe Express (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Adobe Express integration in Adobe Journey Optimizer lets you use Adobe Express's editing tools directly during content creation, enabling you to resize, remove backgrounds, crop, and convert assets to JPEG or PNG.<p>
<p>Adobe Express integration in Adobe Journey Optimizer is currently only available for a set of organizations (Limited Availability). It cannot be deployed for use with Healthcare Shield or Privacy and Security Shield.</p>
<p>For more information, refer to the <a href="../integrations/express.md">detailed documentation</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Journey metrics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey metrics are now available, allowing you to measure the impact of your activities across the key metrics of your business and to provide clearer insights into your performance.</p>
<p>For more information, refer to the <a href="../building-journeys/success-metrics.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table-->

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Intégration à Dynamic Media (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les ressources Dynamic Media sont désormais directement disponibles et accessibles dans Journey Optimizer. Cette intégration vous permet d’effectuer les opérations suivantes :
<ul>
<li>Gérer de manière centralisée des ressources avec mises à jour en temps réel</li>
<li>Modifier instantanément les paramètres de vos ressources, tels que la largeur et la hauteur</li>
<li>Personnaliser des modèles Dynamic Media en mettant à jour votre contenu et en ajoutant des champs de personnalisation</li>
</ul>
<p>
<p>Cette intégration est disponible uniquement pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../integrations/aem-dynamic.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Intégration avec Adobe GenStudio (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Pour améliorer l’efficacité marketing et maintenir la cohérence de la marque, vous pouvez désormais intégrer facilement des expériences GenStudio for Performance Marketing à Journey Optimizer. Vous pouvez ainsi tirer parti de la création de contenu optimisée par l’IA de GenStudio ainsi que des fonctionnalités d’orchestration avancées de Journey Optimizer.<p>
<p>L’utilisation de l’intégration de GenStudio dans Journey Optimizer n’est actuellement pas disponible pour une utilisation avec Healthcare Shield ou Privacy and Security Shield (disponibilité limitée).</p>
<p>Pour plus d’informations, consultez la <a href="../integrations/genstudio.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Évaluation d’audience flexible (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Auparavant disponible pour un ensemble d’organisations (LA), l’évaluation d’audience flexible est désormais disponible pour tous les utilisateurs et toutes les utilisatrices (GA). Cette fonctionnalité vous permet d’exécuter le traitement de la segmentation à la demande pour des audiences sélectionnées, en vous assurant de toujours disposer des données d’audience les plus récentes avant de les cibler dans des parcours et des campagnes Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Pour plus d’informations, consultez la <a href="../audience/creating-a-segment-definition.md#flexible">documentation détaillée</a>.</p>
</tr>
</tbody>
</table>
</table>

<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../conflict-prioritization/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### Améliorations {#25-03-improv}

**Éditeur de personnalisation** (date de disponibilité : 12 mars)

L’éditeur de personnalisation Journey Optimizer a été mis à jour avec de nouvelles fonctionnalités :
* **Mise à jour de la conception de l’éditeur de code** : une interface moderne plus épurée pour une expérience plus conviviale et intuitive.
* **Rechercher et remplacer** : ajout d’une fonctionnalité pour rechercher et remplacer rapidement du contenu dans l’éditeur.
* **Prise en charge de l’annulation et de la restauration** : vous permet d’annuler ou de rétablir facilement les modifications.
* **Taille de police personnalisable** : permet d’ajuster la taille de police de l’éditeur pour une meilleure lisibilité.
* **Validation JSON intégrée** : fournit une validation côté client en temps réel du contenu JSON pour accélérer la détection des erreurs.
* **Saisie automatique pour les attributs de profil et de contexte** : propose des suggestions intelligentes pour optimiser la création de contenu.
* **Amélioration de la mise en surbrillance de la syntaxe** : améliore la lisibilité en rendant la structure du code plus identifiable visuellement.

![Vidéo présentant la nouvelle fonctionnalité dans l’éditeur de personnalisation](assets/do-not-localize/personalization-editor.gif)

Pour plus d’informations, consultez la [documentation détaillée](../personalization/personalization-build-expressions.md).

**Validations**

Lors de la définition des conditions d’une politique d’approbation, vous avez désormais la possibilité de filtrer par balise et/ou catégorie d’objet.

Pour plus d’informations, consultez la [documentation détaillée](../test-approve/approval-policies.md).

**Configuration**

* Vous pouvez désormais attribuer des balises unifiées Adobe Experience Platform à vos configurations de canaux. Vous pouvez ainsi les classer facilement et améliorer la recherche et la navigation dans toutes les listes. [En savoir plus](../configuration/channel-surfaces.md#channel-config-tags)

* Lors de la configuration ou de la modification d’un sous-domaine d’e-mail dans Journey Optimizer, vous pouvez désormais choisir de gérer vous-même l’enregistrement DMARC associé, s’il est disponible sur le domaine parent. [En savoir plus](../configuration/dmarc-record.md#set-up-dmarc)

**Règles métier**

Vous pouvez désormais utiliser le capping de la fréquence quotidienne dans les parcours et les campagnes avec la segmentation par lots. Pour garantir la précision des règles de capping de la fréquence quotidienne, veillez à choisir l’espace de noms de priorité la plus élevée lors de la création d’une campagne ou d’un parcours. Pour en savoir plus sur la priorité des espaces de noms, consultez le [guide sur le service d’identités Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}.

Pour rappel, le capping de la fréquence quotidienne dans les jeux de règles n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

Pour plus d’informations sur les règles métier, consultez la [documentation détaillée](../conflict-prioritization/rule-sets.md).

**Modèles de contenu**

Les modèles de contenu de type HTML sont désormais obsolètes. Notez que vous pouvez toujours utiliser les modèles de contenu HTML existants, précédemment créés dans [!DNL Journey Optimizer]. [En savoir plus sur les modèles de contenu](../content-management/content-templates.md)


<!--**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->




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
<p>Pour plus d’informations, consultez la <a href="../conflict-prioritization/rule-sets.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Générer des pages de destination avec l’Assistant IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce à l’Assistant IA, vous pouvez désormais concevoir du contenu attrayant pour vos pages de destination, notamment des conceptions de pages complètes, du texte et des visuels personnalisés.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>Pour plus d’informations, consultez la <a href="../content-management/generative-lp.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Marques avec l’Assistant IA (Beta)</strong><br/></th>
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
