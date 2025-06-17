---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: c00d5a97e7bedf6f1a22a59cc3bd7588eb9ad32e
workflow-type: tm+mt
source-wordcount: '2164'
ht-degree: 71%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour. [!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.


## Notes de mise à jour anticipées du 25 juin {#25-6-rn}


**Les notes de mise à jour anticipée ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version**. Les liens, les copies d’écran et la documentation mise à jour sont publiés à la date de publication.

**Date de publication** : 17-18 juin 2025

Voir également les [Notes de mise à jour préliminaires de Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

### Nouvelles fonctionnalités {#25-06-features}

Les nouvelles fonctionnalités de cette version sont présentées ci-dessous.


<table>
<thead>
<tr>
<th><strong>Messagerie RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les services de messagerie RCS (Rich Communication Services) sont désormais pris en charge dans Journey Optimizer, ce qui permet d’utiliser les fonctionnalités de messagerie améliorées suivantes, sous réserve de la prise en charge par le fournisseur et l’opérateur :</p>
<ul>
<li>Prise en charge des expéditeurs marqués et vérifiés : envoyez des messages à l’aide de profils métier vérifiés avec des éléments de branding (logo, nom de l’expéditeur, etc.).</li>
<li>Informations sur la diffusion des messages : recevez des rapports de diffusion détaillés comprenant les mises à jour de l’état des messages (par exemple, envoyé, diffusé, lu).</li>
<li>Suivi des liens : incorporez et suivez les URL dans les messages RCS pour l’analyse de l’engagement.</li>
<li>Secours aux SMS : secours automatique aux SMS lorsque l’appareil du profil ne prend pas en charge RCS ou est temporairement inatteignable via RCS.</li>
<li>Composition de base du message : envoyez des messages RCS textuels avec des médias facultatifs et des éléments riches, en fonction de la prise en charge du fournisseur.</li>
</ul>
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Champs de formulaire dans le contenu d’expérience basé sur le code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des champs modifiables spécifiques dans les modèles de contenu JSON ou HTML qui permettent aux utilisateurs non techniques de modifier facilement le contenu d’une vue de formulaire dans la création de canal d’expérience basée sur le code, sans avoir à manipuler le code. En outre, lors de la définition des modèles de contenu d’expérience basés sur du code, vous pouvez désormais insérer des politiques de décision dans le modèle, ce qui accroît la réutilisation et la facilité d’utilisation.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Méthode de délégation personnalisée pour les sous-domaines</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Outre la délégation complète et la méthode CNAME, une nouvelle méthode de configuration de sous-domaine est désormais disponible : la méthode de délégation personnalisée, qui vous permet de posséder entièrement le contrôle et la maintenance de tous les aspects du DNS nécessaires à la diffusion, au rendu et au suivi des messages.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Activité Prise de décision de contenu dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais inclure des offres personnalisées dans vos parcours par le biais d’une activité de prise de décision de contenu dédiée dans la zone de travail de parcours et les utiliser dans des activités de parcours, y compris des conditions et des actions personnalisées.</p>
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera déployée à l’échelle mondiale dans une prochaine version.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Test à blanc du parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’essai de parcours est un mode de publication de parcours spécial dans Adobe Journey Optimizer qui permet aux praticiens du parcours de tester un parcours à l’aide de données de production réelles sans contacter de vrais clients ou mettre à jour les informations de profil. Cette fonctionnalité permet aux utilisateurs et utilisatrices du parcours d’avoir confiance dans leur conception de parcours et leur ciblage d’audience avant de le publier en direct.</p>
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera déployée à l’échelle mondiale dans une prochaine version.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suspendre et reprendre les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant suspendre et reprendre vos parcours. Cette fonctionnalité offre aux professionnels du parcours un meilleur contrôle et une plus grande flexibilité en permettant de suspendre temporairement les parcours en direct sans interrompre l’expérience client. En pause, aucune communication n’est envoyée et les profils restent suspendus jusqu’à la reprise du parcours.</p>
<p>Vous pouvez suspendre et reprendre un seul parcours ou effectuer des opérations de pause et de reprise en bloc sur un groupe de parcours.</p>
<p>En outre, vous pouvez appliquer des filtres globaux aux parcours en pause afin d’exclure les profils en fonction de leurs attributs.</p>
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera déployée à l’échelle mondiale dans une prochaine version.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mettre à l’échelle le gagnant de l’expérimentation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Mettre à l’échelle le gagnant de l’expérimentation vous permet de déployer automatiquement ou manuellement la variation gagnante d’une expérience sur l’ensemble de votre audience. Cette fonctionnalité vous permet d’optimiser la portée et l’efficacité d’un système performant identifié, sans surveillance manuelle constante.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/content-experiment.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 2 juin 2025</p></td>
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
<p>Date de disponibilité : 3 juin 2025</p>
</td>
</tr>
</tbody>
</table>


### Améliorations {#25-06-improv}

Les améliorations de cette version sont présentées ci-dessous.

* **Jeux de règles de canal**

   * **Fenêtre de durée personnalisée** pour la limitation - Un nouveau champ **Nombre de répétitions** est désormais disponible dans l’écran de configuration des jeux de règles de canal. Il vous permet d’appliquer des règles de limitation de fréquence sur plusieurs jours, semaines ou mois, selon la durée spécifiée.

   * **Durée horaire** - Vous pouvez désormais appliquer une limitation toutes les heures pour les ensembles de règles de canal.

* **Expériences basées sur le code**

  Les politiques de décision sont désormais disponibles dans les modèles de contenu d’expérience basés sur du code et dans le rail de droite de l’éditeur de code.

* **Concepteur d’e-mail**

   * **Prise en charge d’un CSS personnalisé** - Journey Optimizer vous permet désormais d’ajouter un CSS personnalisé au contenu de votre e-mail directement dans le Concepteur d’e-mail.
   * **Prise en charge du mode sombre** - Le Concepteur d’e-mail Journey Optimizer offre désormais la possibilité de passer en mode sombre où vous pouvez définir des paramètres spécifiques.

* **Campagnes** - Nouvelle navigation à onglets pour les campagnes d’action. Ce nouveau modèle de navigation permet un accès plus rapide à la création de contenu et prend en charge une extension supplémentaire des paramètres dans les campagnes.

* **Prise de décision** - Date de disponibilité : 3 juin 2025

  Les objets de prise de décision peuvent désormais être copiés entre les sandbox, ce qui simplifie les workflows de test et de déploiement. [En savoir plus](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Prise en charge des attributs d’élément de décision pour les règles de prise de décision** - Date de disponibilité : 4 juin 2025

  Vous pouvez désormais tirer parti des attributs d’élément de décision pour créer des règles de prise de décision. [En savoir plus](../experience-decisioning/rules.md#create)

* **Mise à jour de l’API d’exécution de message interactif** - Date de disponibilité : 6 juin 2025

  L’API d’exécution de message interactif vous permet désormais de supprimer le planning d’exécution des campagnes à venir. [En savoir plus](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}

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
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/exd-ranking-formulas.md">documentation détaillée</a>.</p>
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

