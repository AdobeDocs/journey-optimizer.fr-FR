---
title: Notes de mise à jour 2022
description: Notes de mise à jour 2022 pour Journey Optimizer
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: cdaa6def25adcb63318c272efbfc6d7c4212a9dc
workflow-type: ht
source-wordcount: '2519'
ht-degree: 100%

---

# Notes de mise à jour 2022 {#release-notes-2022}

Cette page répertorie toutes les fonctionnalités et améliorations pour [!DNL Journey Optimizer] publiées en 2022.

## Version d’août 2022 {#aug-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Créer et gérer des campagnes dans Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilisez les campagnes de Journey Optimizer pour diffuser du contenu ponctuel sur un segment spécifique à l’aide de divers canaux. Lors de l’utilisation de parcours, les actions sont conçues pour être exécutées en séquence. Avec les campagnes, les actions sont exécutées simultanément, immédiatement ou selon un planning spécifié. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>Découvrez comment créer une campagne dans la <a href="../campaigns/get-started-with-campaigns.md">documentation détaillée</a> et la <a href="https://video.tv.adobe.com/v/346680">vidéo sur les fonctionnalités</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envoyer des SMS à vos utilisateurs (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer, personnaliser et envoyer des SMS dans Journey Optimizer, grâce à une intégration à <b>Sinch</b> ou <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Découvrez comment créer et envoyer un SMS dans cette <a href="../messages/create-sms.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Améliorations

**Reporting**

* Le tableau et le graphique des stratégies de consentement sont désormais disponibles dans les rapports globaux de parcours. Ces widgets vous permettent de suivre les profils exclus des stratégies de vos actions personnalisées. [En savoir plus](../reports/journey-global-report.md#journey-global)

   Pour avoir accès aux derniers widgets, vous devrez réinitialiser les différents tableaux de bord de rapports. Pour plus d’informations sur la personnalisation des tableaux de bord, consultez la [documentation détaillée](../reports/global-report.md).

**Administration**

* Il est désormais possible de mettre à jour le principal numéro de téléphone à utiliser pour le canal SMS. [En savoir plus](../configuration/primary-email-addresses.md)


## Version de juillet 2022 {#july-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Nouveau flux de messagerie en ligne</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer fournit un nouveau flux pour la création de messages dans les parcours. La messagerie en ligne permet aux utilisateurs de gagner du temps et de rationaliser le workflow de création et de diffusion d’un e-mail, d’une notification push ou d’un SMS dans Journey Optimizer. Parce que les messages ne sont plus une étape distincte et qu’ils sont désormais modifiables en ligne dans le cadre d’une action sur la zone de travail du parcours, les utilisateurs devront cliquer sur moins de boutons et parcourir moins d’écrans pour concevoir et modifier leur contenu.</p>
<img src="assets/do-not-localize/inline.gif"/>
<p>Pour plus d’informations, consultez la <a href="../messages/get-started-content.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Contrôle d’accès basé sur les attributs (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais identifier les champs de schéma avec des étiquettes qui définissent les portées d’utilisation des données ou de l’organisation. Les administrateurs peuvent utiliser l’interface Autorisations pour définir des stratégies d’accès couvrant les champs de schéma XDM et mieux gérer l’accès attribué aux utilisateurs ou groupes d’utilisateurs (utilisateurs internes, externes ou tiers) et gérer l’accès à des types de données spécifiques (c’est-à-dire des données personnelles sensibles/SPD).</p>
<p>L’utilisation du contrôle d’accès basé sur les attributs est actuellement limitée à certains clients et sera déployée dans tous les environnements dans une prochaine version.</p>
<p>Pour plus d’informations, consultez la <a href="../administration/attribute-based-access.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Traitements de prise de décision par lots</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais exécuter des traitements de prise de décision par lots à partir de l’interface utilisateur. Vous n’avez ainsi plus besoin d’un développeur pour exécuter des traitements d’API par lots et le temps consacré au marketing est réduit. Cette nouvelle interface vous permet de créer des traitements et de gérer les traitements actuels/antérieurs.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Pour plus d’informations, consultez la <a href="../offers/batch-delivery.md">documentation détaillée.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utiliser automatiquement l’offre la plus performante dans vos décisions (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser des systèmes de modèles d’optimisation personnalisés dans la gestion des décisions. Ce nouveau type de modèle permet d’optimiser et de personnaliser les offres en fonction des segments et des performances des offres.</p>
<p>L’utilisation des modèles d’IA d’optimisation personnalisés est actuellement limitée à certains utilisateurs et sera déployée dans tous les environnements dans une prochaine version.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Pour plus d'informations, consultez la <a href="../offers/ranking/personalized-optimization-model.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* **Terminaison d’un parcours** : dans la zone de travail du parcours, l’activité **Fin** a été supprimée de la palette. Les balises de fin sont désormais ajoutées par défaut à la fin de chaque chemin et ne peuvent pas être supprimées. Cette amélioration permet de créer un rapport plus optimal sur le moment où un client a quitté le parcours, sans aucune action requise de la part du praticien de parcours. Reportez-vous à la [documentation](../building-journeys/journey-end.md) et à la [vidéo sur les fonctionnalités](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.


* L’option **Fuseau horaire du profil** est désormais décochée par défaut dans les propriétés de parcours. [En savoir plus](../building-journeys/timezone-management.md#timezone-from-profiles)

**Messages**

* Les préréglages des messages sont désormais les **surfaces de canal**. [En savoir plus](../configuration/channel-surfaces.md)

**Administration**

* **Modification des enregistrements PTR** : désormais, lors de la mise à jour d’un enregistrement PTR, le temps de traitement ne prend que 3 heures. [En savoir plus](../configuration/ptr-records.md#processing)

* **Interface utilisateur de la liste autorisée** : vous pouvez désormais utiliser l’interface utilisateur de Journey Optimizer pour ajouter de nouvelles adresses e-mail ou de nouveaux domaines à la liste autorisée. [En savoir plus](../configuration/allow-list.md)

* **Mise à jour de la logique de la liste autorisée** : désormais, la logique de la liste autorisée s’applique dès que la fonctionnalité est activée, même si la liste est vide. [En savoir plus](../configuration/allow-list.md#logic)

* **Paramètres de tracking des URL** : vous pouvez désormais utiliser l’éditeur d’expression pour configurer les paramètres de tracking d’URL sur vos surfaces d’e-mail (c’est-à-dire les préréglages). [En savoir plus](../configuration/email-settings.md#url-tracking)

**Gestion des décisions**

* **Taille de l’audience** : un nouveau composant d’estimation de la taille de l’audience s’affiche désormais dans l’interface utilisateur lors de la création d’une règle de décision, lors de la sélection d’un segment ou d’une règle pour définir l’éligibilité d’une offre ou lors de l’ajout d’un segment ou d’une règle à une portée de décision.


## Version de juin 2022 {#june-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Envoyer des SMS à vos utilisateurs (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer, personnaliser et envoyer des SMS dans Journey Optimizer, grâce à une intégration à <b>Sinch</b> ou <b>Twilio</b>.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>Le canal SMS est actuellement disponible uniquement pour un ensemble d’organisations (disponibilité limitée). Pour en savoir plus, contactez votre représentant Adobe.</p>
<p>Découvrez comment créer et envoyer un SMS dans cette <a href="../messages/create-sms.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Trouvez des images plus percutantes plus rapidement grâce à l’intégration d’Adobe Stock.</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le module d’intégration du Concepteur d’e-mail Adobe Stock et Adobe Journey Optimizer fournit aux clients une façon simple de naviguer, d’acquérir des produits sous licence et d’enregistrer des images en vue de les utiliser dans la création de messages. </br>La nouvelle option <b>Rechercher des photos Stock similaires</b> vous permet également de localiser les photos Stock qui correspondent au contenu, à la couleur et à la composition de vos images. </p>
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>Pour plus d’informations, consultez la <a href="../design/stock.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utiliser la fonctionnalité E-mail Cci sur tous vos e-mails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser la fonctionnalité Email Cci (copie carbone invisible) pour stocker les e-mails envoyés par Adobe Journey Optimizer. Activez cette option dans vos préréglages d’e-mail de sorte que chaque e-mail envoyé soit copié de façon invisible vers votre adresse Cci.</p>
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
<p>Pour plus d’informations, consultez la <a href="../configuration/archiving-support.md#bcc-email">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Copier des objets entre sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais recréer les expériences d’une sandbox Journey Optimizer à une autre, par exemple d’une sandbox hors production vers une sandbox de production. Cette nouvelle fonctionnalité permet de copier d’une sandbox à une autre un parcours complet, y compris tous les objets nécessaires à son bon fonctionnement. Outre les parcours, vous pouvez également copier d’autres composants, tels que les offres, les messages, les schémas, les jeux de données, les sources de données, les événements et les actions.</p>
<p>Pour plus d'informations, consultez la <a href="../building-journeys/copy-to-sandbox.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>




### Améliorations

**Gestion des décisions**

* **Prise en charge des fichiers HTML et JSON** - Vous pouvez désormais glisser-déposer des fichiers HTML et JSON externes de la bibliothèque de ressources d’Adobe Experience Cloud au contenu de rendu de l’offre. [En savoir plus](../offers/offer-library/add-representations.md#html-json)


**E-mail**

* **Enregistrer en tant que modèle** - Vous pouvez désormais enregistrer un contenu d’e-mail en tant que modèle et le réutiliser lors de la création d’autres messages. [En savoir plus](../design/email-templates.md)


**Administration**

* **Aperçu des paramètres d’URL de suivi** - Lors de la configuration d’un préréglage de message, si vous définissez des paramètres de suivi des URL, un aperçu dynamique de l’URL de suivi résultante s’affiche désormais. [En savoir plus](../configuration/email-settings.md#url-tracking)

* **Modification des préréglages de message** : lors de la mise à jour d’un préréglage de message, le temps de traitement ne peut désormais excéder 3 heures. [En savoir plus](../configuration/channel-surfaces.md#edit-channel-surface)

* **Modification du groupe d’adresses IP** : lors de la mise à jour d’un groupe d’adresses IP, le temps de traitement ne peut désormais excéder 3 heures. [En savoir plus](../configuration/ip-pools.md#edit-ip-pool)




## Version de mai 2022 {#may-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Règles de fréquence des messages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des règles métier cross-canal qui excluront automatiquement les profils sursollicités des messages et actions.</p>
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>Pour plus d’informations, consultez la <a href="../configuration/frequency-rules.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestion des décisions - Modèle d’optimisation automatique du classement IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser des systèmes de modèle formés dans la gestion des décisions. Cette nouvelle fonctionnalité permet de classer les offres à afficher pour un profil donné.</p>
<!--img src="assets/do-not-localize/optimization.gif"/-->
<p>Pour plus d’informations, consultez la <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journaux d’audit Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais surveiller les actions effectuées par les utilisateurs sur les ressources Adobe Journey Optimizer.</p>
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>Pour plus d'informations, consultez la <a href="../privacy/audit-logs.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Personnalisation**

* **Nouvelle fonction d’assistance pour le masquage des caractères** : la fonction d’assistance `mask` vous permet de remplacer une partie d’une chaîne par des caractères « X ». [En savoir plus](../personalization/functions/string.md#mask)

**Pages de destination**

* **Pages de destination sans formulaire** : vous pouvez maintenant créer et publier une page de destination qui ne contient pas de formulaire et ne nécessite aucune action de la part des visiteurs.
* **Modèles de page de destination** : vous pouvez maintenant enregistrer une page de destination en tant que modèle et la réutiliser lors de la création d’autres pages de destination. [En savoir plus](../landing-pages/lp-templates.md)
* **Retour à la page principale** : vous pouvez maintenant ajouter un lien vers la page principale à partir de n’importe quelle sous-page de la même page de destination.
* **Prise en charge de code JavaScript personnalisé** : vous pouvez désormais ajouter du code JavaScript personnalisé au contenu de votre page de destination pour appliquer un style avancé ou ajouter des comportements personnalisés à vos pages de destination.    [En savoir plus](../landing-pages/lp-custom-js.md)

**Parcours**

* **Lecture de segment** : les parcours de lecture de segment en une seule fois sont désormais mis à l’état Terminé 30 jours après l’exécution du parcours. Pour la lecture de segment planifiée, cela se passe 30 jours après l’exécution de la dernière occurrence. [En savoir plus](../building-journeys/read-segment.md)
* **Éditeur d&#39;expression** : la fonction [limit](../building-journeys/functions/functionlimit.md) a été ajoutée pour vous permettre de limiter le nombre d’éléments d’une liste. La fonction [sort](../building-journeys/functions/functionsort.md) vous permet désormais de trier un objet de liste. La prise en charge de listObject a également été ajoutée aux fonctions [Disctinct](../building-journeys/functions/functiondistinct.md) et [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md).

**Administration**

* **Mise à jour du tableau de bord d’utilisation des licences** : le tableau de bord d’utilisation des licences disponible dans l’interface utilisateur [!DNL Adobe Journey Optimizer] reflète désormais la valeur exacte de la richesse moyenne du profil **sous licence**. Une baisse de cette représentation de mesure s’affiche, ce qui signifie que la limite de licence est désormais correctement signalée. [En savoir plus](../segment/license-usage.md)


## Version d&#39;avril 2022 {#april-2022-release}

### Améliorations

**Pages de destination**

* **Nouvelle option pour les cases à cocher de type opt-in/opt-out** : vous pouvez désormais insérer une seule case à cocher de type opt-in/opt-out dans les pages de destination des abonnements. Les utilisateurs doivent cocher la case pour donner leur consentement (opt-in), et la décocher pour supprimer leur consentement (opt-out). [En savoir plus](../landing-pages/design-lp.md#define-lp-specific-content)

* **Préremplir les champs des pages de destination** : il est désormais possible de donner aux utilisateurs la possibilité de préremplir les champs des pages de destination avec des informations de profil. [En savoir plus](../landing-pages/create-lp.md#configure-primary-page)

**Gestion des décisions**

* **API Decisioning sur Edge** : l’API Edge Decisioning peut diffuser et générer des offres personnalisées qui sont gérées dans la gestion des décisions. Vous pouvez créer vos offres et d’autres objets connexes en utilisant l’interface utilisateur de gestion de décisions ou les API. [En savoir plus](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administration**

* **Durée d’envoi des PTR** : la durée pour que la modification des PTR soit effective est maintenant de quelques heures. [En savoir plus](../configuration/ptr-records.md#processing)

**Conception d’e-mail**

* **20 nouveaux modèles d’e-mail** sont maintenant disponibles pour concevoir le contenu de vos e-mails dans Journey Optimizer.

**Interface utilisateur**

* **Aide contextuelle dans l’interface utilisateur de Journey Optimizer** : des liens d’aide contextuelle ont été ajoutés à plusieurs pages de Journey Optimizer. Lorsqu’ils sont disponibles, cliquez sur l’icône « i » pour afficher une description rapide de la fonctionnalité en cours et accéder aux articles connexes.

**Intégration à Adobe Campaign Standard**

En tant que client d’Adobe Campaign Standard, vous pouvez désormais envoyer des e-mails, des notifications push et des SMS à l’aide de Journey Optimizer. Utilisez les nouvelles actions intégrées pour tirer profit des fonctionnalités de messagerie transactionnelle de Campaign Standard dans Journey Optimizer.  [En savoir plus](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Version de mars 2022 {#march-2022-release}

### Améliorations

**Parcours**

* Pour éviter d’avoir des champs inutiles dans le schéma de profil unifié, le schéma Événement d’étape du parcours n’est plus activé par défaut pour les profils. Si nécessaire, vous pouvez l’activer. [En savoir plus](../reports/sharing-overview.md)
* Les nouveaux événements d’étape liés aux traitements d’exportation sont désormais envoyés par Journey Optimizer à Adobe Experience Platform. Des exemples de requêtes ont été ajoutés à la documentation. [En savoir plus](../reports/query-examples.md)

**Gestion des décisions**

* Vous pouvez désormais spécifier si la limitation de l’offre est appliquée à tous les utilisateurs ou à un profil spécifique, à tous les emplacements ou par emplacement. [En savoir plus](../offers/offer-library/add-constraints.md#capping)
* L’API Batch Decisioning permet aux entreprises d’utiliser la fonctionnalité Gestion des décisions pour tous les profils d’un segment donné en un seul appel. Le contenu de l’offre pour chaque profil du segment est placé dans un jeu de données AEP où il est disponible pour les workflows par lots personnalisés. [En savoir plus](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administration**

* Vous pouvez maintenant activer/désactiver le lien de désabonnement dans/à partir de l’en-tête de l’e-mail au niveau du paramètre de message prédéfini, et définir une URL de désabonnement personnalisée au niveau du message. [En savoir plus](../configuration/channel-surfaces.md#list-unsubscribe)
* La liste autorisée peut désormais être activée et désactivée via l’interface [!DNL Journey Optimizer] sur les sandbox de production et hors production. [En savoir plus](../configuration/allow-list.md#enable-allow-list)

**Personnalisation**

* Vous pouvez désormais enregistrer plus de 40 expressions de personnalisation dans la bibliothèque. [En savoir plus](../personalization/personalization-library.md)

## Version de février 2022 {#feb-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Pages de destination d’abonnement</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer et concevoir des pages de destination dans Journey Optimizer afin de diriger vos utilisateurs vers des formulaires en ligne où ils pourront s’inscrire ou se désinscrire de la réception de vos communications, ou s’abonner à un service spécifique, tel qu’une newsletter.</p>
<p>Pour plus d’informations, consultez la <a href="../landing-pages/create-lp.md">documentation détaillée</a> et le <a href="../landing-pages/lp-use-cases.md">cas d’utilisation type</a> correspondant.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouvelle bibliothèque d’expressions de personnalisation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer propose désormais une bibliothèque qui vous donne accès à des expressions de personnalisation prédéfinies. Ces expressions sont configurées par les utilisateurs administrateurs.</p>
<p>Pour plus d’informations, consultez la <a href="../personalization/personalization-library.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs' feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Transmettre des informations pour suivre vos messages avec les paramètres de tracking UTM</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dans le contenu des messages Journey Optimizer, vous pouvez maintenant ajouter des paramètres UTM à vos liens : ils peuvent fournir des données supplémentaires sur ce lien et vous aider à identifier où et pourquoi une personne a cliqué sur ce lien.</p>
<p>Pour plus d'informations, consultez la <a href="../configuration/channel-surfaces.md#configure-email-settings">documentation détaillée</a>.</p-->
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Pour optimiser les performances, tous les parcours en mode test qui n’ont pas été déclenchés depuis une semaine repassent désormais au statut de brouillon. [En savoir plus](../building-journeys/testing-the-journey.md#important_notes)
* L’intégration entre Journey Optimizer et Adobe Campaign Classic a été optimisée pour améliorer les performances. La configuration par défaut de limitation a été remplacée par 4 000 appels/5 minutes.    [En savoir plus](../action/acc-action.md#important-notes)

**Reporting**

* Les diffusions peuvent désormais être filtrées en fonction de leur statut :
   * Dans la liste Exécution des messages, vous pouvez désormais exclure les BAT de la liste de vos diffusions.
   * Dans vos rapports dynamiques/globaux, vous pouvez choisir d’exclure les événements de test.

* Vous pouvez désormais accéder aux rapports sur les données d’optimisation de l’heure d’envoi : le nombre de personnes qui ont reçu immédiatement des messages et le nombre de personnes qui ont reçu des messages avec une optimisation d’une heure, une optimisation de 2 heures, etc.

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Gestion des décisions**

* Les classements et le classement IA sont désormais regroupés dans un seul onglet.

## Version de janvier 2022 {#january-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Parcours : optimisation de la montée en puissance des adresses IP à lʼaide des conditions de limite de profils</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Lors de la configuration d’une activité <strong>Condition</strong> dans un parcours, vous pouvez désormais définir une limite de profils. Utilisez ce nouveau type de condition pour définir un nombre maximal de profils pour le chemin dʼun parcours. Lorsque cette limite est atteinte, les profils entrants prennent un autre chemin. Vous pouvez ainsi augmenter le volume de vos diffusions (montée en puissance des adresses IP). Par exemple, vous pouvez augmenter le nombre de diffusions sur un domaine en fractionnant lʼexécution : envoi de 1 000 messages le premier jour, 2 000 le deuxième jour, etc.</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/condition-activity.md#profile_cap">documentation détaillée</a> et le <a href="../building-journeys/ramp-up-deliveries-uc.md">cas d’utilisation type</a> correspondant.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Parcours : amélioration apportée à la lecture de segment</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Lʼoption <strong>Lecture incrémentielle</strong> a été ajoutée aux activités <strong>Lecture de segment</strong> récurrentes. Cette option permet de cibler uniquement les individus qui sont entrés dans le segment depuis la dernière exécution du parcours. La première exécution cible toujours tous les membres du segment.</p>
<p>Pour plus d'informations, consultez la <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Les événements d’étape Journey Optimizer peuvent désormais être liés à d’autres jeux de données dans [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=fr). Le champ **profileID**, dans le schéma intégré d’événement d’étape du parcours, est désormais défini comme un champ d’identité. [En savoir plus](../reports/sharing-overview.md#integration-cja)

**Gestion des décisions**

* La mise à jour dʼune offre, dʼune offre de secours, dʼune collection d’offres ou dʼune décision d’offre, directement ou indirectement référencée dans un message publié, est désormais automatiquement répercutée dans le message correspondant, sans quʼil soit nécessaire de le republier. [En savoir plus](../offers/offers-e2e.md#insert-decision-in-email)

* Lors de la simulation des offres qui seront diffusées pour un profil de test donné, vous pouvez maintenant modifier les paramètres de simulation par défaut et afficher le code correspondant à vos simulations qui peut être utilisé à des fins de dépannage. [En savoir plus](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administration**

* Les administrateurs peuvent désormais modifier les enregistrements PTR avec un sous-domaine configuré en CNAME. [En savoir plus](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personnalisation**

* **Ajouter aux favoris** : pour aider à améliorer lʼefficacité lors de lʼutilisation de la personnalisation, nous avons introduit le concept d’enregistrement en tant que favoris. L’ajout de différents attributs à votre menu de favoris vous permet dʼaccéder rapidement aux éléments que vous utilisez le plus fréquemment. [En savoir plus](../personalization/personalize.md#fav)
