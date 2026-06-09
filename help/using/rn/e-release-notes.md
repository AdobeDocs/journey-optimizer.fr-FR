---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour préliminaires pour Journey Optimizer
description: Notes de mise à jour préliminaires pour Adobe Journey Optimizer
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 361e8f77dc32fb9154cc5ed156822bc402934595
workflow-type: tm+mt
source-wordcount: 2169
ht-degree: 7%

---


# Notes de version préliminaire {#e-release-notes}

Adobe Journey Optimizer offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

## Notes de mise à jour préliminaires du 26 juin {#june-26-rn}

**Les notes de version préliminaire ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les écrans et la documentation mise à jour sont publiés une fois les modifications mises en production. Bien que la plupart des modifications soient diffusées à la date de publication, quelques-unes peuvent être déployées ultérieurement. Pour plus d’informations, reportez-vous à la date de disponibilité répertoriée pour chaque entrée.

Voir également les [Notes de mise à jour préliminaires d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Date de publication** : 16 et 17 juin 2026

### Fidélité {#june-26-loyalty}

Dans cette version, la fonctionnalité suivante sera bientôt disponible pour la fidélité.

### Parcours {#june-26-journeys}

Les fonctionnalités et améliorations suivantes seront bientôt disponibles dans les parcours de cette version.

<table>
<thead>
<tr>
<th><strong>Optimisation du chemin de parcours - Ciblage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilisez le nouveau nœud <strong>Optimiser</strong> pour cibler des audiences spécifiques afin de déterminer le meilleur moyen d’atteindre vos indicateurs de performance clés orientés métier.</p>
<p>Cet outil vous permet de développer des campagnes marketing plus efficaces, plus susceptibles de résonner au niveau 1:1, d’améliorer les efforts de personnalisation marketing pour les clients et d’améliorer les KPI d’engagement client essentiels, tels que les conversions et les recettes.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Arbitrage de parcours - Formules</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser des <strong>formules</strong> pour augmenter automatiquement les <strong>scores de priorité de parcours </strong> en fonction des attributs du profil client et des facteurs contextuels, afin que les clients accèdent aux parcours les plus pertinents.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>

* **Augmentation du nombre maximal de parcours actifs et nouveaux mécanismes de sécurisation** - Vous pouvez désormais disposer de **200 parcours actifs**, contre 100 auparavant.

* **Dates de début et de fin dans l’en-tête du parcours** - Lorsque les dates de début et/ou de fin sont configurées sur un parcours dynamique, elles sont désormais affichées dans l’en-tête du parcours **** à côté du badge de statut dynamique. Le libellé affiché s’adapte selon que chaque date est à venir ou est déjà dépassée.

* **Arrêter ou fermer un parcours en pause directement** - Vous pouvez désormais **arrêter un parcours ou le fermer aux nouvelles entrées** directement à partir de l’état **En pause**. Auparavant, un parcours en pause devait reprendre pour passer en ligne avant de pouvoir être arrêté ou fermé.

* **Prise en charge des identifiants supplémentaires dans les parcours pour les audiences externes** - **Les identifiants supplémentaires** dans les parcours sont désormais pris en charge pour les **audiences externes**, y compris les audiences importées à partir d’un fichier CSV et les audiences créées avec la composition d’audiences fédérées. Vous pouvez désigner n’importe quel attribut de non-identité ou attribut d’identité non-personne de l’audience comme ID supplémentaire. Aucun étiquetage de schéma n’est nécessaire.

### Campagnes orchestrées {#june-26-oc}

Les fonctionnalités et améliorations suivantes seront bientôt disponibles pour les campagnes orchestrées dans cette version.

<table>
<thead>
<tr>
<th><strong>Activité Chargement de fichier dans les campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les campagnes orchestrées prennent désormais en charge le chargement d’un fichier <strong>CSV ou TXT</strong> directement dans la zone de travail de campagne en tant qu’audience de ciblage, sans avoir à ingérer le fichier dans Adobe Experience Platform au préalable. Les données du fichier sont utilisées au moment de l’exécution et ne sont pas conservées en tant que jeu de données Adobe Experience Platform. Lors de la configuration de fichiers, vous pouvez définir des mappages de colonnes, des types de données, une gestion des NULL et des politiques d’erreur par colonne. Cela prend en charge les campagnes de listes de partenaires ou d’envois ad hoc pour lesquelles la création d’un pipeline d’ingestion complet n’est pas pratique.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prise en charge des heures creuses pour les campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais appliquer des <strong>heures creuses</strong> aux campagnes orchestrées. Les heures calmes vous permettent de définir des <strong>exclusions temporelles</strong> pour empêcher l’envoi de messages pendant des périodes spécifiques, ce qui vous aide à respecter les préférences des clients et les exigences de conformité dans les cas d’utilisation de l’orchestration des campagnes.</p>
</td>
</tr>
</tbody>
</table>

* **Personnalisation en boucle des données relationnelles dans les campagnes orchestrées** - L’éditeur de personnalisation prend désormais en charge un **bloc de boucle** qui effectue une itération sur les collections relationnelles, telles que les commandes, les comptes ou les réservations, et effectue le rendu d’un bloc de contenu par enregistrement dans un seul e-mail ou SMS. Les collections sont configurées par le biais du sélecteur de données à l’aide de jetons de personnalisation, sans écriture d’expression requise.

* **Personnaliser les détails de l’expéditeur de l’e-mail par destinataire et campagne** - Les campagnes orchestrées prennent désormais en charge la personnalisation des **champs d’en-tête des e-mails**, y compris le nom de l’expéditeur, l’adresse de l’expéditeur et la réponse, à l’aide d’attributs de profil ou de données relationnelles. Cela permet aux détails de l’expéditeur de refléter le conseiller, l’emplacement ou la filiale approprié(e) pour chaque destinataire, plutôt que de router tous les envois via une seule adresse d’entreprise. Les valeurs d’en-tête peuvent être définies au niveau du canal et remplacées par campagne à l’aide de données contextuelles pour un contrôle plus précis.

* **Simplification de la dimension de cible dans les campagnes orchestrées** - La **dimension de ciblage** active s’affiche désormais sur la zone de travail du workflow, de sorte que vous pouvez voir quelle dimension est utilisée par une activité de canal. Le flux de segmentation d’entités multiples est plus simple, car vous n’avez plus besoin d’une activité « Changement de dimension » distincte. De plus, vous pouvez désormais choisir explicitement si les messages sont envoyés au niveau du profil ou au niveau d’une dimension secondaire.

* **Remplacer le champ d’exécution par défaut dans les campagnes** - Auparavant disponible au niveau du parcours, vous pouvez désormais remplacer le champ par défaut **champ d’exécution** défini globalement pour vos diffusions e-mail, SMS et WhatsApp dans les paramètres de la campagne.

### Prise de décision {#june-26-decisioning}

La fonctionnalité suivante est proposée dans Prise de décision dans cette version.

<table>
<thead>
<tr>
<th><strong>Utilisation du fragment de contenu Adobe Experience Manager dans la prise de décision</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais mapper <strong>les fragments de contenu </strong> aux <strong>éléments de décision</strong> dans Decisioning et les exploiter dans les politiques de décision pour diffuser le fragment approprié au bon client au bon moment.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>

### Canal E-mail {#june-26-email}

Les fonctionnalités et améliorations suivantes seront apportées au canal e-mail dans cette version.

<table>
<thead>
<tr>
<th><strong>Composants Avancés - Mises En Page (Super Composants)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Designer d’e-mail comprend désormais une <strong>bibliothèque de composants de disposition prêts à l’emploi</strong> tels que des en-têtes, des cartes de produits (1, 2 ou 3 colonnes), des blocs d’informations et des pieds de page, que vous pouvez faire glisser directement dans la zone de travail de votre e-mail. Chaque composant est préconfiguré avec des propriétés modifiables (image, titre, texte, bouton, liens) et peut être entièrement personnalisé via l’interface de WYSIWYG, ce qui accélère la création d’e-mails sans que vous ayez à créer des structures à partir de zéro.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vérification de contenu dans Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer permet désormais aux utilisateurs de valider leur <strong>qualité du contenu des e-mails</strong> (notamment la lisibilité, l’efficacité et la cohésion du contenu) directement dans l’interface de Designer d’e-mail.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activer la réduction de la taille des e-mails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Cette nouvelle option permet de <strong>réduire la taille de l’HTML</strong> dans un e-mail en supprimant les espaces blancs, les commentaires et le code redondant inutiles, sans modifier l’aspect de l’e-mail. Cela permet d’améliorer la délivrabilité (certains fournisseurs de messagerie rejettent ou signalent les e-mails surdimensionnés) et d’accélérer le temps de chargement des destinataires.</p>
<p>Date de disponibilité : 10 juin 2026</p>
</td>
</tr>
</tbody>
</table>

* **Prise en charge du mode texte dans les fragments** - Pour prendre en charge les workflows d’e-mail textuels, vous pouvez désormais créer et gérer des **versions textuelles** de vos fragments visuels pour une utilisation optimale dans la version en texte brut des e-mails qui incluent ce fragment. Lors de l’utilisation d’un fragment créé avant la version actuelle, le rendu de la version texte du fragment peut être incorrect, à la fois dans le Designer d’e-mail et dans l’e-mail final envoyé à vos destinataires. Pour de meilleurs résultats avec des fragments plus anciens, modifiez, enregistrez et republiez chaque fragment.

* **Mise à jour des références de débit d’envoi par lots avec les scénarios destinés aux clients** - Adobe Journey Optimizer **références de débit d’envoi par lots** ont été mises à jour pour refléter les performances de niveau production dans plusieurs scénarios de personnalisation, des envois de base au contenu dynamique complexe avec une logique conditionnelle. Les mesures actualisées sont désormais disponibles dans la documentation du produit pour aider les clients à planifier avec précision leurs volumes de messagerie.

* **Processus OTP de boucle de retour pour les sous-domaines personnalisés** - Le processus de configuration des sous-domaines personnalisés de boucle de retour (FBL) a été amélioré en faisant apparaître le hub d&#39;expéditeur Yahoo **mot de passe à usage unique (OTP)** directement dans l&#39;interface utilisateur du produit. Les utilisateurs peuvent désormais récupérer et afficher automatiquement le mot de passe à usage unique généré lors de la vérification de la propriété du domaine du hub d’expéditeur Yahoo.

### Messages mobiles (SMS, MMS, RCS et LINE) {#june-26-mobile}

Les améliorations suivantes seront apportées à la messagerie mobile dans cette version.

* **Clics uniques pour les rapports SMS** - Un nouveau module **Clics uniques** a été ajouté aux rapports SMS, apportant le même niveau de suivi granulaire des performances aux SMS que celui actuellement disponible pour les rapports par e-mail.

* **Canal LINE - Modifications de création** - L’interface utilisateur du canal LINE a été mise à niveau avec des fonctionnalités avancées de création de messages. Cette version introduit la prise en charge de **plusieurs formats de message**, notamment Texte, Image, Image, Plan d’image, Carrousel et Flex (éditeur JSON), ainsi que des aperçus d’appareils en temps réel. Les utilisateurs peuvent désormais gérer des messages groupés comportant jusqu&#39;à cinq commandes (avec ajout, suppression et réorganisation des commandes) et tirer parti de l&#39;éditeur de personnalisation intégré pour une messagerie dynamique et validée.

* **Revente Journey Optimizer - Afficher les mesures d&#39;utilisation** - Pour les clients qui achètent des SMS directement via Adobe Journey Optimizer, un nouveau **tableau de bord d&#39;utilisation des SMS** a été introduit. Vous pouvez désormais afficher et suivre vos 90 derniers jours de mesures d’envoi de messages, catégorisées par messages mobiles d’origine (MO) et messages mobiles d’interruption (MT). Ces données peuvent également être téléchargées au format CSV, pour une meilleure visibilité et un meilleur contrôle des dépenses liées à vos SMS.

### Contenu et intégrations {#june-26-content}

Les fonctionnalités et améliorations suivantes vont être apportées à la gestion de contenu et aux intégrations dans cette version.

<table>
<thead>
<tr>
<th><strong>Fragments de contenu avec Adobe Experience Manager</strong><br/></th>
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
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configuration du référentiel Adobe Experience Manager</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous disposez désormais d’une certaine flexibilité quant à la manière dont Adobe Journey Optimizer accède à votre contenu Adobe Experience Manager. Cette version offre la possibilité de <strong>changer de référentiel source</strong> pour les fragments de contenu utilisés dans vos parcours et campagnes.</p>
</td>
</tr>
</tbody>
</table>

* **Intégration native des fragments de contenu Adobe Experience Manager (Managed Services)** - Désormais compatible avec **Managed Services**, vous pouvez afficher les fragments de contenu Adobe Experience Manager, y accéder et les utiliser directement dans Journey Optimizer à des fins de personnalisation. Il vous suffit d’ajouter votre URL de référentiel Adobe Experience Manager Managed Services dans les paramètres de configuration pour une configuration ponctuelle.

* **Intégration de l’assistant AI à Adobe Experience Manager Asset Essentials** - L’assistant AI récupère désormais automatiquement les **images approuvées par la marque** directement depuis votre Adobe Experience Manager Assets lors de la génération d’e-mails, de pages web et de notifications push. Cela élimine la nécessité de rechercher manuellement dans Assets ou de recourir à des solutions de secours d’IA génériques, en s’assurant que chaque élément visuel est parfaitement précis et conforme à la marque.

### Canaux personnalisés {#june-26-channels}

La fonctionnalité suivante est proposée aux canaux dans cette version.

<table>
<thead>
<tr>
<th><strong>Canal sortant personnalisé</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer introduit désormais <strong>Canaux personnalisés</strong>, une nouvelle fonctionnalité qui permet aux administrateurs d’importer n’importe quel canal de messagerie HTTP sortant (tel que WeChat, Kakao Talk, Messenger ou un fournisseur propriétaire) directement dans AJO par le biais d’un <strong>créateur de canaux sans code</strong>. Une fois configurés, les canaux personnalisés sont disponibles dans les campagnes, les Parcours et les campagnes orchestrées, avec le même ensemble complet de fonctionnalités que les canaux natifs : personnalisation avec l’éditeur d’expression, expérimentation de contenu, prévisualisation et BAT, rapports d’usine, et application du consentement et de la gouvernance. Cela comble le vide précédemment comblé par les actions personnalisées, qui se limitaient aux Parcours et manquaient de création de contenu dédiée.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

### Création de rapports {#june-26-reporting}

Les améliorations suivantes ont été apportées aux rapports dans cette version.

* **Exclure les clics de robots pour les rapports par e-mail et SMS** - Afin de fournir une vue plus précise de l’engagement réel des clients, de nouvelles mesures estimées sont désormais disponibles dans les Parcours, les campagnes et les rapports de canal. Ces mesures permettent de filtrer les interactions non humaines (NHI) et les clics de robots à partir des données de rapport :
   * Estimation des clics : nombre total de clics comptabilisés après suppression du trafic non humain et robots identifié.
   * CTR estimé : nombre estimé de clics par rapport au total des diffusions.
   * Taux de clics estimé pour les e-mails uniquement : estimations des clics par rapport aux ouvertures estimées.

### Configuration {#june-26-configuration}

Dans cette version, les améliorations suivantes ont été apportées à la configuration et à l’administration.

* **Whitelistage d’adresses IP du pare-feu d’applications web (WAF) pour les pages de destination d’AJO** - Adobe Journey Optimizer prend désormais en charge le **whitelistage d’adresses IP du pare-feu d’applications web (WAF)** pour les pages de destination, ce qui permet aux entreprises de s’assurer que toutes les requêtes entrantes sont acheminées exclusivement via leur infrastructure WAF configurée. Grâce à cette amélioration, les clients peuvent configurer AJO pour rejeter toute demande directe qui contourne la couche WAF, en s’assurant que les politiques de sécurité définies dans des outils tels que Imperva sont appliquées de manière cohérente. Cette fonctionnalité renforce la position de sécurité des entreprises ayant des exigences strictes en matière d’accès au réseau, leur permettant de contrôler entièrement le flux de trafic vers leurs pages de destination hébergées dans AJO.

* **Jeu de données passant de la diffusion en continu au mode par lots** - Le jeu de données d’événement de retour de message AJO passe de la diffusion en continu au **mode d’ingestion par lots**. Cette modification garantit que l’ingestion de données ne dépasse pas les limites d’ingestion en flux continu. Si vous utilisez ce jeu de données dans des rapports Customer Journey Analytics ou si vous exécutez des requêtes sur celui-ci, attendez-vous à une augmentation de la latence des données allant jusqu’à 2 heures.

### Améliorations de la convivialité {#june-26-usability}

L’amélioration de la convivialité suivante est apportée à cette version.

* **Dossiers pour les Parcours et les campagnes** - Vous pouvez désormais organiser vos parcours et campagnes en **dossiers** pour améliorer la navigation et la gestion dans l’interface.

