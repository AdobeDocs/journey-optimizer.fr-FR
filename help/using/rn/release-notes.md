---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 4945e2fb37b54683f56ca3b832553345486d0a80
workflow-type: tm+mt
source-wordcount: '1416'
ht-degree: 89%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour. [!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Mises à jour du 25 juin {#25-6-rn}

<table>
<thead>
<tr>
<th><strong>Mettre à l’échelle le gagnant de l’expérimentation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le gagnant de l’expérience vous permet de déployer automatiquement ou manuellement la variation gagnante d’une expérience sur l’ensemble de votre audience. Cette fonctionnalité vous permet d’optimiser la portée et l’efficacité d’un système performant identifié, sans surveillance manuelle constante.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/content-experiment.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 2 juin 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflit et hiérarchisation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dans Journey Optimizer, la gestion du volume et du calendrier des campagnes et des parcours est essentielle pour éviter de submerger les clientes et clients avec un trop grand nombre d’interactions. Journey Optimizer propose désormais plusieurs outils de gestion des conflits et de hiérarchisation, auparavant réservés aux organisations à accès limité (LA), qui sont désormais accessibles au public (GA).</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements. Les améliorations suivantes ont été apportées à cette version à disponibilité générale :</p>
<ul>
<li>Prise en charge étendue : les outils de gestion des conflits prennent désormais en charge les Parcours unitaires et les Parcours de qualification d’audience, en plus des parcours Lecture d’audience.</li>
<li>Amélioration de la résolution des problèmes : deux nouveaux champs d’événement d’étape sont désormais disponibles dans Query Service, ce qui vous permet d’analyser pourquoi un profil a été rejeté d’un parcours ou d’une campagne.</li>
<li>Amélioration des rapports : les rapports indiquent désormais quelle règle spécifique a exclu un profil d’un parcours ou d’une campagne, ce qui offre une plus grande transparence et des informations exploitables.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Pour plus d’informations, consultez la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 3 juin 2025</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

* **Decisioning** - Date de disponibilité : 3 juin 2025

  Les objets de prise de décision peuvent désormais être copiés entre les sandbox, ce qui simplifie les workflows de test et de déploiement. [En savoir plus](../configuration/copy-objects-to-sandbox.md#decisioning)


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
<p>Cette modification n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour demander l’accès, utilisez <a href="https://forms.cloud.microsoft/r/FC49afuJVi" target="_blank">ce formulaire</a>.</p>
<img src="assets/do-not-localize/calendar.gif">
<p>Pour plus d’informations, reportez-vous aux sections suivantes : <a href="../building-journeys/journey-ui.md">Parcourir et filtrer vos parcours </a> <a href="../campaigns/modify-stop-campaign.md">Accéder aux campagnes</a>.</p>
<p>Date de disponibilité : jeudi 28 mai 2025</p>
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
<p>Auparavant disponible pour un nombre limité d’organisations (LA), cette fonctionnalité est désormais disponible en version GA avec l’amélioration suivante : vous pouvez désormais définir des espaces réservés et mapper des valeurs de personnalisation dans la signature de fragment à l’aide du mode Éditeur.</p>
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
<th><strong>Simuler les variations de contenu</strong><br/></th>
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
<p>Date de disponibilité : mercredi 20 mai 2025</p>
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
<p>Date de disponibilité : mercredi 20 mai 2025</p>
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
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/exd-ranking-formulas.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 14 mai 2025</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#25-05-improv}

Les améliorations de cette version sont présentées ci-dessous.


* **Nouvelle prise en charge des objets de campagne pour la copie de sandbox** - Date de disponibilité : 15 mai 2025

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

* **&#39;Prise en charge de la redirection vers une URL&#39; dans le canal web** - Date de disponibilité : 20 mai 2025

  Le canal web Journey Optimizer vous permet désormais de rediriger les visiteurs et visiteuses vers une autre URL existante plutôt que de créer une nouvelle variation dans l’éditeur visuel. Cette fonctionnalité peut être utilisée pour exécuter des expériences en comparant deux pages complètement différentes au lieu de simplement modifier quelques éléments dans une page. [En savoir plus](../web/create-web.md#web-redirect-to-url)

* **Dossiers pour modèles et fragments** - Date de disponibilité : 20 mai 2025

  Les dossiers vous permettent d’organiser vos objets plus facilement et plus efficacement dans une hiérarchie structurée. Auparavant disponibles pour un certain nombre d’organisations (disponibilité limitée), les dossiers sont désormais accessibles à tous les utilisateurs et utilisatrices (disponibilité générale) pour gérer les modèles et fragments de contenu. Pour en savoir plus, consultez les sections [Modèles de contenu](../content-management/access-content-templates.md#folders) et [Fragments](../content-management/manage-fragments.md#folders).

* **Suivi des clics dans les modèles d’e-mail** - Date de disponibilité : 20 mai 2025

  Le suivi des clics sur les éléments `<area>` dans les cartes d’image des contenus d’e-mail est désormais pris en charge de manière native dans [!DNL Journey Optimizer]. Cela permet de s’assurer que les zones cliquables reçoivent le même modèle, les mêmes données de suivi et les mêmes paramètres ajoutés que les liens hypertexte standard. [En savoir plus sur le suivi des messages](../email/message-tracking.md#manage-tracking)

<!--
* **Decisioning - Leverage Adobe Experience Platform datasets** 
  
  Journey Optimizer now allows you to leverage Adobe Experience Platform datasets in the following Decisioning objects: eligibility rules, ranking formulas, and capping rules.-->

* **Rail droit dans la liste des campagnes** - Date de disponibilité : 20 mai 2025

  Dans la liste des campagnes, la sélection d’une campagne ouvre désormais un volet affichant ses détails.

<!--* **Form fields in code-based experience content**

  In content templates, you can now define specific JSON or HTML fields which enable non-technical users to easily edit content in code-based experiences without the need to manipulate code.

* **Decision item attribute support for decisioning rules**
  
  You can now leverage decision item attributes to create decisioning rules.

* **Subdomains - 'Custom delegation' method**  
  In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering, and tracking messages.
  -->

