---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
TQID: https://experienceleague.adobe.com/YJKQFYUi8Kw7yZZKm8blcM-1G9uYsqcsEsopH0hOMhA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 691dcd9cdb98ca4bfd6c13dc5b4c92d71805c852
workflow-type: tm+mt
source-wordcount: 3693
ht-degree: 25%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continue, ce qui permet à Adobe de proposer régulièrement de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements. En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

>[!NOTE]
>
>Les fonctionnalités répertoriées dans ces notes de mise à jour incluent une **date de disponibilité** indiquant le moment auquel chaque modification devient accessible dans votre environnement. Des entrées dans les accordéons **Bientôt disponible** sont attendues dans les prochains jours ou les prochaines semaines. Les informations de cette section peuvent faire l’objet de modifications.

## Notes de mise à jour du 26 juin {#june-26-rn}

La version de juin 2026 offre plusieurs fonctionnalités phares à la disponibilité générale, notamment la **simulation de Parcours**, le **ciblage de l’optimisation des chemins de Parcours** et les **fragments de Parcours**, ainsi que de nouvelles fonctions de création assistées par l’IA dans les parcours et le contenu, une prise en charge étendue de la prise de décision pour le canal Courrier, et des contrôles de sécurité et d’administration supplémentaires. Les fonctionnalités et améliorations ci-dessous sont organisées par thème. D’autres modifications sont également attendues dans les jours ou semaines à venir.

### Parcours {#june-26-journeys}

Les fonctionnalités et améliorations suivantes ont été ajoutées aux parcours dans cette version. D’autres modifications sont également attendues dans les jours ou semaines à venir.


<table>
<thead>
<tr>
<th><strong>Simulation de parcours (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant définir votre parcours sur Simulation. Ce mode permet de valider la logique à l’aide d’utilisateurs et d’utilisatrices simulés. Il s’agit de profils temporaires créés spécifiquement pour la simulation, qui vous permettent de tester librement sans avoir à gérer de profils de test persistants dans Adobe Experience Platform. </p>
<p>Publiée précédemment en disponibilité limitée, la simulation de parcours est désormais disponible dans tous les environnements. Avec cette version de disponibilité générale, vous pouvez désormais utiliser l’agent Journey pour générer des utilisateurs et utilisatrices et des événements simulés directement dans le menu Simulation.</p>
<p><img src="assets/do-not-localize/journey-simulation.gif"></p>
<p>Pour plus d'informations, consultez la <a href="../building-journeys/simulate-journey-gs.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 9 juin 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Fragments De parcours (Disponibilité Générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer des <strong>fragments de parcours</strong> dans Adobe Journey Optimizer. Les fragments de parcours sont des ensembles réutilisables de nœuds de parcours que vous pouvez créer une fois et déposer dans n’importe quel parcours de votre sandbox. Qu’il s’agisse d’une vérification d’éligibilité, d’une logique de routage de canal préféré ou d’une séquence de bienvenue, les fragments permettent aux équipes de se déplacer plus rapidement et de rester cohérentes, sans devoir reconstruire la même logique à chaque fois.</p>
<p>Une fois créés, les fragments sont stockés dans un <strong>inventaire des fragments</strong> dédié et peuvent être insérés dans n’importe quel parcours à l’aide de l’activité <strong>Fragments de parcours</strong>.</p>
<p>Auparavant disponible en disponibilité limitée, cette fonctionnalité est désormais disponible pour tous les clients et clientes. Les fragments de parcours prennent également en charge <strong>l’outil Sandbox</strong>, ce qui vous permet de compresser et d’exporter des fragments dans les sandbox.</p>
<p>Pour plus d'informations, consultez la <a href="../building-journeys/journey-fragments.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 9 juin 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Optimisation des chemins de parcours - Ciblage (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’activité <strong>Optimiser</strong> prend désormais en charge <strong>les règles de ciblage</strong> qui permettent de définir des critères spécifiques que les clients et clientes doivent remplir pour être qualifiés pour un chemin de parcours particulier, en fonction des segments d’audience ou des attributs de profil.</p>
<p>Contrairement à l’expérimentation, où les clients sont affectés à des chemins de manière aléatoire, le ciblage utilise une logique déterministe pour s’assurer que l’audience ou le profil client approprié est acheminé vers le chemin prévu.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/optimize.gif"></p>
<p>Pour plus d'informations, consultez la <a href="../building-journeys/path-targeting.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 8 juin 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistant IA pour les expressions de parcours (version Beta publique)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’assistant IA fonctionne désormais dans l’éditeur d’expression avancé de parcours pour convertir les prompts en langage naturel en expressions valides et en logique conditionnelle. Décrivez l’expression que vous souhaitez créer. L’assistant IA génère un code prêt à l’emploi que vous pouvez appliquer immédiatement ou affiner à l’aide de prompts supplémentaires.</p>
<p>Cette fonctionnalité est disponible en version Beta publique pour l’ensemble des clientes et clients.</p>
<p><img src="assets/do-not-localize/expression-assistant.gif"></p>
<p>Pour plus d'informations, consultez la <a href="../building-journeys/expression/expression-agent.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 3 juin 2026</p> 
</td>
</tr>
</tbody>
</table>

* **Prise en charge des identifiants supplémentaires pour les audiences externes** : les identifiants supplémentaires dans les parcours sont désormais pris en charge pour les audiences externes, y compris les audiences importées depuis un fichier CSV et les audiences créées avec la composition d’audiences fédérées. Vous pouvez désigner un attribut non identitaire ou un attribut d’identité non personnel de l’audience comme identifiant supplémentaire. Aucun étiquetage de schéma n’est nécessaire. [En savoir plus](../building-journeys/supplemental-identifier.md)

  Date de disponibilité : 11 juin 2026

* **Arrêt automatique pour les parcours de lecture d’audience non récurrents** - Les parcours non récurrents **lecture d’audience** passent désormais automatiquement au statut **Arrêté** une fois le dernier profil actif quitté. Auparavant, ces parcours restaient **actifs** jusqu’à l’expiration du délai d’expiration global de 91 jours, même lorsqu’aucun profil n’y circulait plus. Grâce à cette amélioration, le statut du parcours reflète le statut d’exécution réel dès qu’il est terminé, ce qui permet de conserver un inventaire précis de vos parcours sans intervention manuelle.

  Notez que ce comportement ne s’applique pas aux parcours qui incluent des nœuds provoquant des périodes d’attente, tels que les nœuds d’attente, les nœuds de réaction ou les transitions déclenchées par un événement. Ces parcours restent soumis au délai d’expiration global standard de 91 jours. [En savoir plus](../building-journeys/end-journey.md#auto-stop-non-recurring)

  Date de disponibilité : 9 juin 2026

* **Authentification personnalisée basée sur un certificat dans les actions personnalisées** : les actions personnalisées prennent désormais en charge l’authentification personnalisée basée sur un certificat. En ajoutant `subType: "certificateCredential"` à une configuration d’autorisation personnalisée, Journey Optimizer utilise un certificat géré Adobe pour signer une assertion client JWT et l’échanger contre un jeton d’accès (aucun secret client requis). Conçu pour les API d’entreprise qui appliquent la vérification d’identité avec certificat, comme Microsoft Entra ID. [En savoir plus](../datasource/external-data-sources.md#certificate-credential)

  Date de disponibilité : 4 juin 2026

* **Augmentation du nombre maximal de parcours actifs et nouveaux mécanismes de sécurisation** - Vous pouvez désormais disposer de **200 parcours actifs**, contre 100 auparavant. [En savoir plus](../start/guardrails.md#journeys-guardrails-journeys)

  Date de disponibilité : 18 juin 2026. Cette fonctionnalité sera progressivement déployée dans toutes les régions au cours des prochains jours.

+++ Prochainement — **Les informations ci-dessous peuvent faire l’objet de modifications.**

* **Dates de début et de fin dans l’en-tête du parcours** - Lorsque les dates de début et/ou de fin sont configurées sur un parcours dynamique, elles sont désormais affichées dans l’en-tête du parcours **** à côté du badge de statut dynamique. Le libellé affiché s’adapte selon que chaque date est à venir ou est déjà dépassée.

+++

### Campagnes orchestrées {#june-26-oc}

Les fonctionnalités et améliorations suivantes seront bientôt disponibles pour les campagnes orchestrées dans cette version.

+++ Prochainement — **Les informations ci-dessous peuvent faire l’objet de modifications.**

<table>
<thead>
<tr>
<th><strong>Ciblage basé sur des fichiers dans des campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les campagnes orchestrées prennent désormais en charge le chargement d’un fichier <strong>CSV ou TXT</strong> directement dans la zone de travail de campagne en tant qu’audience de ciblage, sans avoir à ingérer le fichier dans Adobe Experience Platform au préalable. Les données du fichier sont utilisées au moment de l’exécution et ne sont pas conservées en tant que jeu de données Adobe Experience Platform. Lors de la configuration de fichiers, vous pouvez définir des mappages de colonnes, des types de données, une gestion des NULL et des politiques d’erreur par colonne. Les lignes dont la validation a échoué sont rejetées et consignées avant l’exécution de la campagne, ce qui permet de garder l’audience propre sans pré-traitement manuel. Cela est particulièrement adapté aux envois ad hoc ou aux campagnes de liste de partenaires pour lesquelles la création d’un pipeline d’ingestion complet n’est pas pratique.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p> Date de disponibilité : 30 juin 2026</p>
</td>
</tr>
</tbody>
</table>

* **Personnalisation en boucle des données relationnelles** - L’éditeur de personnalisation prend désormais en charge un bloc Boucle qui effectue une itération sur les collections relationnelles, telles que les commandes, les comptes ou les réservations, et effectue le rendu d’un bloc de contenu par enregistrement dans un seul e-mail ou SMS. Les collections sont configurées par le biais du sélecteur de données à l’aide de jetons de personnalisation, sans écriture d’expression requise. [En savoir plus](../orchestrated/add-personalization.md#enrichment-collections)

  Date de disponibilité : Fin juin 2026

* **Personnaliser les détails de l’expéditeur de l’e-mail par destinataire et campagne** - Les campagnes orchestrées prennent désormais en charge la personnalisation des **champs d’en-tête des e-mails**, y compris le nom de l’expéditeur, l’adresse de l’expéditeur et la réponse, à l’aide d’attributs de profil ou de données relationnelles. Cela permet aux détails de l’expéditeur de refléter le conseiller, l’emplacement ou la filiale approprié(e) pour chaque destinataire, plutôt que de router tous les envois via une seule adresse d’entreprise. Les valeurs d’en-tête peuvent être définies au niveau du canal et remplacées par campagne à l’aide de données contextuelles pour un contrôle plus précis.

+++

### Prise de décision {#june-26-decisioning}

Les fonctionnalités et améliorations suivantes ont été ajoutées à la prise de décision dans cette version.

<table>
<thead>
<tr>
<th><strong>Prise en charge de la prise de décision dans le canal Courrier</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais ajouter des politiques de décision dans des parcours et des campagnes par courrier. Les politiques de décision sont des conteneurs pour vos offres qui tirent profit du moteur de prise de décision afin d’effectuer un rendu dynamique du meilleur contenu, pour chaque membre de l’audience. La prise de décision pour le courrier prend également en charge les cas d’utilisation de prise de décision par lots, ce qui vous permet d’exporter les éléments d’offre correspondants pour chaque profil dans une audience Adobe Experience Platform donnée. </p>
<p><img src="assets/do-not-localize/exd-dm.gif"></p>
<p>Pour plus d'informations, consultez la <a href="../experience-decisioning/use-decision-policy.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 3 juin 2026</p>
</td>
</tr>
</tbody>
</table>

+++ Prochainement — **Les informations ci-dessous peuvent faire l’objet de modifications.**

* **Attributs d’élément dynamiques** - Les attributs personnalisés d’élément de décision peuvent désormais être personnalisés au moment de la diffusion à l’aide des données de profil, contextuelles et d’audience. Cela supprime la nécessité de conserver des offres en double pour les variations de contenu mineures, ce qui permet aux spécialistes marketing de gérer moins d’éléments de décision et plus flexibles.

  Date de disponibilité : 22 juin 2026

+++

### Gestion de contenu {#june-26-content}

Les fonctionnalités et améliorations suivantes ont été ajoutées à la gestion de contenu dans cette version.

<table>
<thead>
<tr>
<th><strong>Simuler des variations de contenu : génération de variantes d’expérience et d’IA mises à jour</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Deux mises à jour sont désormais disponibles pour le workflow <strong> Simuler du contenu </strong> :</p>
<ul>
<li><strong>Nouveau chemin par défaut</strong> — Cliquez sur <strong>Simuler du contenu</strong> pour ouvrir désormais l’expérience <strong>Simuler des variations de contenu</strong> par défaut. À partir d’un seul écran, vous pouvez ajouter un exemple d’entrée manuellement ou à partir d’un fichier CSV/JSON, réutiliser des utilisateurs simulés, prévisualiser le rendu et envoyer des BAT. Pour prévisualiser avec des profils de test Adobe Experience Platform, envoyer des BAT avec des données de profil de test ou vérifier le rendu des boîtes de réception d’e-mails et les rapports de spam, cliquez sur <strong>Simuler du contenu</strong>, puis sélectionnez <strong>Simuler du contenu (profils AEP)</strong> dans la liste déroulante.</li>
<li><strong>Variantes de contenu générées par l’IA</strong> — Dans l’expérience <strong>Simuler des variations de contenu</strong>, cliquez sur <strong>Générer</strong> pour utiliser l’IA pour créer automatiquement des variantes de contenu. Le système analyse votre message, détecte les champs de personnalisation et les branches conditionnelles et remplit des valeurs réalistes afin que vous puissiez valider le rendu sans créer manuellement chaque variante.</li>
</ul>
<p>Pour plus d'informations, consultez la <a href="../test-approve/simulate-sample-input.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 9 juin 2026</p>
</td>
</tr>
</tbody>
</table>


+++ Prochainement — **Les informations ci-dessous peuvent faire l’objet de modifications.**

<table>
<thead>
<tr>
<th><strong>Simuler des variations de contenu : génération de variantes d’expérience et d’IA mises à jour</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Deux mises à jour sont désormais disponibles pour le workflow <strong> Simuler du contenu </strong> :</p>
<ul>
<li><strong>Nouveau chemin par défaut</strong> — Cliquez sur <strong>Simuler du contenu</strong> pour ouvrir désormais l’expérience <strong>Simuler des variations de contenu</strong> par défaut. À partir d’un seul écran, vous pouvez ajouter un exemple d’entrée manuellement ou à partir d’un fichier CSV/JSON, réutiliser des utilisateurs simulés, prévisualiser le rendu et envoyer des BAT. Pour prévisualiser avec des profils de test Adobe Experience Platform, envoyer des BAT avec des données de profil de test ou vérifier le rendu des boîtes de réception d’e-mails et les rapports de spam, cliquez sur <strong>Simuler du contenu</strong>, puis sélectionnez <strong>Simuler du contenu (profils AEP)</strong> dans la liste déroulante.</li>
<li><strong>Variantes de contenu générées par l’IA</strong> — Dans l’expérience <strong>Simuler des variations de contenu</strong>, cliquez sur <strong>Générer</strong> pour utiliser l’IA pour créer automatiquement des variantes de contenu. Le système analyse votre message, détecte les champs de personnalisation et les branches conditionnelles et remplit des valeurs réalistes afin que vous puissiez valider le rendu sans créer manuellement chaque variante.</li>
</ul>
<p>Pour plus d'informations, consultez la <a href="../test-approve/simulate-sample-input.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 9 juin 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Améliorations apportées aux fragments de contenu Adobe Experience Manager dans Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Cette version comprend plusieurs améliorations pour rendre les <strong>fragments de contenu </strong> plus utilisables, plus gouvernables et plus prêts pour la production dans les workflows de création de Journey Optimizer :</p>
<ul>
<li>Journey Optimizer prend désormais en charge la récupération de fragments de contenu à partir de plusieurs configurations Adobe Experience Manager, y compris les niveaux de création, de publication et de publication authentifiée.</li>
<li>Une fois qu’un fragment est sélectionné, son contexte est conservé tout au long du message, ce qui permet aux auteurs de réutiliser les champs de fragment sur les blocs de contenu sans avoir à les sélectionner de nouveau.</li>
<li>Une nouvelle page de liste dédiée aux fragments de contenu a été introduite dans Journey Optimizer pour une meilleure gestion du cycle de vie. Les utilisateurs et utilisatrices peuvent identifier les fragments non synchronisés et déclencher des synchronisations manuelles pour rester à jour.</li>
<li>La prise en charge des paramètres régionaux et des variations permet désormais aux marketeurs de travailler plus délibérément avec d’autres versions du même fragment de contenu.</li>
<li>Vous disposez désormais d’une certaine flexibilité quant à la manière dont Adobe Journey Optimizer accède à votre contenu Adobe Experience Manager. Cette version offre la possibilité de <strong>changer de référentiel source</strong> pour les fragments de contenu utilisés dans vos parcours et campagnes.</li>
<li>Désormais compatible avec <b></b>, vous pouvez afficher des fragments de contenu Adobe Experience Manager, y accéder et les utiliser directement dans Journey Optimizer à des fins de personnalisation. Il vous suffit d’ajouter votre URL de référentiel Adobe Experience Manager Managed Services dans les paramètres de configuration pour une configuration ponctuelle.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Intégration de l’assistant AI à Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’assistant AI récupère désormais automatiquement les <b>images approuvées par la marque</b> directement depuis votre Adobe Experience Manager Assets lors de la génération d’e-mails, de pages web et de notifications push. Cela élimine la nécessité de rechercher manuellement dans Assets ou de recourir à des solutions de secours d’IA génériques, en s’assurant que chaque élément visuel est parfaitement précis et conforme à la marque.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistant d’IA pour les améliorations de la génération de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Cette version améliore l’expérience de génération de contenu de l’<strong>assistant AI</strong> avec une modification d’image plus puissante, une extraction de marque plus fiable et une prise en charge de l’authenticité du contenu dans le flux d’image :</p>
<ul>
<li>La <strong>modification d’image par l’IA</strong> est désormais disponible dans le flux de génération d’images, y compris la prise en charge des modèles tiers Firefly, afin que vous puissiez affiner les images sources sans quitter l’assistant.</li>
<li><strong>extraction du signal de marque</strong> offre des résultats de meilleure qualité. Lorsque les pages sélectionnées ne reçoivent pas suffisamment de signal, les basculements améliorés renseignent désormais les couleurs, la typographie, les directives d’écriture et d’autres attributs de marque.</li>
<li><strong>l’extraction de marque web</strong> est plus fiable. L’amélioration de la gestion du délai d’expiration empêche les pages lentes, les fenêtres contextuelles et les bannières de cookies de bloquer l’extraction.</li>
<li><strong> L’authenticité du contenu (CAI)</strong> est désormais prise en charge dans le flux d’images. Cette version corrige également les problèmes de chargement d’images de référence et améliore la gestion des images sans manifeste C2PA existant.</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++


### Canal e-mail {#june-26-email}

Les améliorations suivantes ont été ajoutées au canal e-mail dans cette version.

* **Chiffrement des paramètres d’URL** : vous pouvez désormais chiffrer les paramètres d’URL dans les liens de tracking et de page de destination ajoutés à vos e-mails. Cela ajoute un niveau de sécurité supplémentaire pour les données de paramètres sensibles. Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale). [En savoir plus](../personalization/url-parameter-encryption.md)

  Date de disponibilité : 1er juin 2026

* **Nouvelles autorisations pour le registre des clés** deux nouvelles autorisations sont désormais requises pour accéder et gérer les clés nécessaires au chiffrement des paramètres d’URL : **Gérer le registre des clés** et **Afficher le registre des clés**. [En savoir plus](../administration/high-low-permissions.md#administration-permissions)

  Date de disponibilité : 1er juin 2026

<table>
<thead>
<tr>
<th><strong>Texte enrichi dans les champs modifiables pour les fragments</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais ajouter du texte enrichi aux fragments personnalisables utilisés dans le contenu de vos e-mails.</p>
<p>Par exemple, lorsque vous utilisez le composant Texte comme champ modifiable dans le Designer d’e-mail, vous pouvez directement mettre en forme le contenu (en gras et en italique, par exemple) et insérer des liens hypertexte.</p>
<p><img src="assets/do-not-localize/rich-text-editable-fields.gif"></p>
<p>Pour plus d'informations, consultez la <a href="../content-management/customizable-fragments.md#rich-text-visual">documentation détaillée</a>.</p>
<p>Date de disponibilité : Fin juin 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vérification de contenu dans le Designer Email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer inclut désormais une validation technique automatisée directement dans le Designer d’e-mail, ce qui vous permet de détecter les problèmes HTML et CSS avant l’envoi.</p>
<p>Les contrôles couvrent les éléments non pris en charge, tels que les balises <code>&lt;script&gt;</code> et <code>&lt;base&gt;</code>, les balises div vides qui peuvent rompre la disposition dans Microsoft Outlook, les balises de méta-actualisation HTML et les seuils de taille CSS ou HTML qui déclenchent des échecs de rendu dans Gmail.</p>
<p>Les résultats sont affichés sous la forme d’erreurs, d’avertissements ou d’informations directement dans le panneau de création, avec des détails contextuels et des correctifs en un clic le cas échéant, afin que les problèmes puissent être résolus sans quitter l’éditeur.</p>
<p><img src="assets/do-not-localize/content-check.gif"></p>
<p>Pour plus d'informations, consultez la <a href="../email/content-check.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 18 juin 2026</p>
</td>
</tr>
</tbody>
</table>

* **Convertisseur Image vers HTML amélioré** - Une nouvelle version de la fonctionnalité de convertisseur Image vers HTML est désormais disponible, offrant une précision améliorée pour la génération HTML. Cette mise à jour exploite des modèles LLM de niveau supérieur pour fournir une sortie HTML plus précise et plus fiable à partir des entrées d’image.

  Date de disponibilité : 18 juin 2026

+++ Prochainement — **Les informations ci-dessous peuvent faire l’objet de modifications.**

<table>
<thead>
<tr>
<th><strong>Activer la réduction de la taille des e-mails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer comprend désormais une option permettant de réduire la taille de l’HTML de votre e-mail en supprimant les espaces blancs, les commentaires et le code redondant inutiles, sans affecter le rendu de l’e-mail.</p>
<p>Cela peut améliorer la délivrabilité en évitant les seuils de taille que certains fournisseurs de messagerie utilisent pour marquer ou rejeter les messages et peut réduire le temps de chargement des destinataires.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modules dans le Designer Email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Designer d’e-mail comprend désormais une bibliothèque de modules de disposition prêts à l’emploi, tels que des en-têtes, des cartes de produits, des blocs d’informations et des pieds de page, que vous pouvez faire glisser directement dans la zone de travail de votre e-mail.</p>
<p>Chaque module est préconfiguré avec des propriétés modifiables (image, titre, texte, bouton, liens) et peut être entièrement personnalisé via l’interface de WYSIWYG, ce qui accélère la création d’e-mails sans que vous ayez à créer des structures à partir de zéro.</p>
<p>Date de disponibilité : 22 juin 2026</p>
</td>
</tr>
</tbody>
</table>

+++

### Contenu et intégrations {#june-26-integration}

Les fonctionnalités et améliorations suivantes vont être apportées à la gestion de contenu et aux intégrations dans cette version.

<table>
<thead>
<tr>
<th><strong>Améliorations apportées aux fragments de contenu Adobe Experience Manager dans Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Cette version comprend plusieurs améliorations pour rendre les <strong>fragments de contenu </strong> plus utilisables, plus gouvernables et plus prêts pour la production dans les workflows de création de Journey Optimizer :</p>
<ul>
<li>Journey Optimizer prend désormais en charge la récupération de fragments de contenu à partir de plusieurs configurations Adobe Experience Manager, y compris les niveaux de création, de publication et de publication authentifiée.</li>
<li>Une fois qu’un fragment est sélectionné, son contexte est conservé tout au long du message, ce qui permet aux auteurs de réutiliser les champs de fragment sur les blocs de contenu sans avoir à les sélectionner de nouveau.</li>
<li>Une nouvelle page de liste dédiée aux fragments de contenu a été introduite dans Journey Optimizer pour une meilleure gestion du cycle de vie. Les utilisateurs et utilisatrices peuvent identifier les fragments non synchronisés et déclencher des synchronisations manuelles pour rester à jour.</li>
<li>La prise en charge des paramètres régionaux et des variations permet désormais aux marketeurs de travailler plus délibérément avec d’autres versions du même fragment de contenu.</li>
<li>Vous disposez désormais d’une certaine flexibilité quant à la manière dont Adobe Journey Optimizer accède à votre contenu Adobe Experience Manager. Cette version offre la possibilité de <strong>changer de référentiel source</strong> pour les fragments de contenu utilisés dans vos parcours et campagnes.</li>
<li>Désormais compatible avec <b></b>, vous pouvez afficher des fragments de contenu Adobe Experience Manager, y accéder et les utiliser directement dans Journey Optimizer à des fins de personnalisation. Il vous suffit d’ajouter votre URL de référentiel Adobe Experience Manager Managed Services dans les paramètres de configuration pour une configuration ponctuelle.</li>
</ul>
<p>Pour plus d'informations, consultez la <a href="../integrations/aem-fragments-gs.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 18 juin 2026</p>
</td>
</tr>
</tbody>
</table>

+++ Prochainement — **Les informations ci-dessous peuvent faire l’objet de modifications.**

<table>
<thead>
<tr>
<th><strong>Intégration de l’assistant AI à Adobe Experience Manager Asset Essentials</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’assistant AI récupère désormais automatiquement les <b>images approuvées par la marque</b> directement depuis votre Adobe Experience Manager Assets lors de la génération d’e-mails, de pages web et de notifications push. Cela élimine la nécessité de rechercher manuellement dans Assets ou de recourir à des solutions de secours d’IA génériques, en s’assurant que chaque élément visuel est parfaitement précis et conforme à la marque.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistant d’IA pour les améliorations de la génération de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Cette version améliore l’expérience de génération de contenu de l’<strong>assistant AI</strong> avec une modification d’image plus puissante, une extraction de marque plus fiable et une prise en charge de l’authenticité du contenu dans le flux d’image :</p>
<ul>
<li>La <strong>modification d’image par l’IA</strong> est désormais disponible dans le flux de génération d’images, y compris la prise en charge des modèles tiers Firefly, afin que vous puissiez affiner les images sources sans quitter l’assistant.</li>
<li><strong>extraction du signal de marque</strong> offre des résultats de meilleure qualité. Lorsque les pages sélectionnées ne reçoivent pas suffisamment de signal, les basculements améliorés renseignent désormais les couleurs, la typographie, les directives d’écriture et d’autres attributs de marque.</li>
<li><strong>l’extraction de marque web</strong> est plus fiable. L’amélioration de la gestion du délai d’expiration empêche les pages lentes, les fenêtres contextuelles et les bannières de cookies de bloquer l’extraction.</li>
<li><strong> L’authenticité du contenu (CAI)</strong> est désormais prise en charge dans le flux d’images. Cette version corrige également les problèmes de chargement d’images de référence et améliore la gestion des images sans manifeste C2PA existant.</li>
</ul>
</td>
</tr>
</tbody>
</table>

+++

### Création de rapports {#june-26-reporting}

+++ Prochainement — **Les informations ci-dessous peuvent faire l’objet de modifications**

* **Estimation des clics pour la création de rapports par e-mail et SMS** — Une nouvelle mesure **Estimation des clics** est désormais disponible dans les Parcours, les campagnes et les rapports de canal pour les e-mails et les SMS. Cette mesure exclut le trafic d’interactions non humaines (NHI) et identifiées afin de fournir une vue plus claire de l’engagement réel des clients. La mesure Clics existante reste disponible et continue de signaler le nombre total de clics.

* **Nouvelles mesures de clic estimées pour les rapports par e-mail et SMS** - Afin de fournir une vue plus précise de l’engagement réel des clients, de nouvelles mesures estimées sont désormais disponibles dans les Parcours, les campagnes et les rapports de canal. Ces mesures permettent de filtrer les interactions non humaines (NHI) et les clics de robots à partir des données de rapport :

   * CTR estimé : nombre estimé de clics par rapport au total des diffusions.
   * Taux de clics estimé pour les e-mails uniquement : estimations des clics par rapport aux ouvertures estimées.

  Date de disponibilité : Fin juin 2026

+++

### Administration {#june-26-administration}

Les améliorations suivantes ont été apportées à l’administration et à la gestion des données dans cette version.

* [!BADGE Important ]{type=Informative} **Le jeu de données d’événement de retour de message AJO passe à l’ingestion par lots** - Le **jeu de données d’événement de retour de message AJO** passe de l’ingestion par flux à l’ingestion par lots. Par conséquent, attendez-vous à une latence des données allant jusqu’à 2 heures pour ce jeu de données. Si vous avez créé des rapports dans Customer Journey Analytics ou exécuté des requêtes à l’aide de ce jeu de données, tenez compte de cette latence accrue à l’avenir. [En savoir plus](../data/datasets-query-examples.md#message-feedback-event-dataset)

  Date de disponibilité : 10 juin 2026

* **Alertes client pour les événements de cycle de vie de campagne** : les nouvelles alertes système vous informent désormais des événements de cycle de vie clés pour les campagnes déclenchées par action et par API. Abonnez-vous au niveau du sandbox. [En savoir plus](../reports/alerts.md)

  Date de disponibilité : 1er juin 2026


+++ Prochainement — **Les informations ci-dessous peuvent faire l’objet de modifications**

* **whitelistage d’adresses IP de Web Application Firewall (WAF)** - Adobe Journey Optimizer prend désormais en charge le whitelistage d’adresses IP de Web Application Firewall (WAF) pour les pages de destination, ce qui permet aux entreprises de s’assurer que toutes les requêtes entrantes sont acheminées exclusivement via leur infrastructure WAF configurée. Grâce à cette amélioration, les clients peuvent configurer Journey Optimizer pour rejeter toute demande directe qui contourne la couche WAF, en s’assurant que les politiques de sécurité définies dans des outils tels qu’Imperva sont appliquées de manière cohérente. Cette fonctionnalité renforce la position de sécurité des entreprises ayant des exigences strictes en matière d’accès au réseau, leur permettant de contrôler entièrement le flux de trafic vers leurs pages de destination hébergées dans AJO.

  Date de disponibilité : Fin juin 2026

+++


### Messages mobiles (SMS, MMS, RCS et LINE) {#june-26-mobile}

Les améliorations suivantes seront apportées à la messagerie mobile dans cette version.

* **Clics uniques pour les rapports SMS** - Un nouveau module **Clics uniques** a été ajouté aux rapports SMS, apportant le même niveau de suivi granulaire des performances aux SMS que celui actuellement disponible pour les rapports par e-mail.

* **SMS - Afficher les mesures d’utilisation** - Pour les clients et clientes qui achètent des SMS directement via Adobe Journey Optimizer, un nouveau **tableau de bord d’utilisation des SMS** a été introduit. Vous pouvez désormais afficher et suivre vos 90 derniers jours de mesures d’envoi de messages, catégorisées par messages mobiles d’origine (MO) et messages mobiles d’interruption (MT). Ces données peuvent également être téléchargées au format CSV, pour une meilleure visibilité et un meilleur contrôle des dépenses liées à vos SMS.

* **Estimation des clics pour le rapport SMS** - Une nouvelle mesure Estimation des clics est désormais disponible dans les Parcours, les campagnes et les rapports Canal pour les e-mails et les SMS. Cette mesure exclut le trafic d’interactions non humaines (NHI) et identifiées afin de fournir une vue plus claire de l’engagement réel des clients. La mesure Clics existante reste disponible et continue de signaler le nombre total de clics.

+++ Prochainement — **Les informations ci-dessous peuvent faire l’objet de modifications.**

* **Canal LINE - Modifications de création** - L’interface utilisateur du canal LINE a été mise à niveau avec des fonctionnalités avancées de création de messages. Cette version introduit la prise en charge de **plusieurs formats de message**, notamment Texte, Image, Image, Plan d’image, Carrousel et Flex (éditeur JSON), ainsi que des aperçus d’appareils en temps réel. Les utilisateurs peuvent désormais gérer des messages groupés comportant jusqu&#39;à cinq commandes (avec ajout, suppression et réorganisation des commandes) et tirer parti de l&#39;éditeur de personnalisation intégré pour une messagerie dynamique et validée.

+++

### Améliorations de la convivialité {#june-26-usability}

+++ Prochainement — **Les informations ci-dessous peuvent faire l’objet de modifications.**

* **Dossiers pour les Parcours et les campagnes** - Vous pouvez désormais organiser vos parcours et campagnes en **dossiers** pour améliorer la navigation et la gestion dans l’interface.

+++

<!--
+++ Coming soon — **Information below is subject to change.**

* **Override the default execution field in campaigns** - Previously available at the journey level, you can now override the default execution field set globally for your Email, SMS and WhatsApp deliveries in the campaign parameters.

  Availability date: Early June, 2026

+++
-->
