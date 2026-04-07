---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 5683fc646985a9b3c9557a52ca2ffdf3861561e2
workflow-type: tm+mt
source-wordcount: '2100'
ht-degree: 21%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**** fournit en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continu, ce qui permet à Adobe de fournir en continu de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements.

En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Mises à jour d’avril 2026 {#april-26-rn}

### Nouvelles fonctionnalités {#april-26-features}

<table>
<thead>
<tr>
<th><strong>Boîte de réception</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Boîte de réception</strong> est une fonctionnalité mobile, disponible avec les cartes de contenu, qui permet aux clients de créer un emplacement centralisé dans leur application ou site web pour afficher les messages envoyés à leurs utilisateurs. Cela prolonge la durée de vie des communications marketing en s’assurant que les messages restent accessibles même après leur rejet.</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../inbox/inbox-gs.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 7 avril 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Optimiser le texte des e-mails pour les boîtes de réception d’IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer comprend désormais une nouvelle fonctionnalité qui garantit que vos e-mails sont structurés de manière optimale pour les boîtes de réception optimisées par l’IA telles qu’Apple Intelligence et Google Gemini dans Gmail.</p>
<p>Comme les assistants d’IA contrôlent de plus en plus la manière dont les destinataires lisent et agissent sur les e-mails, cette fonctionnalité vous permet de créer du contenu qui s’exécute correctement dans les tâches d’IA en aval, notamment la synthèse, le tri, la hiérarchisation et l’extraction d’intention.</p>
<p><img src="assets/do-not-localize/text-optimizer.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../content-management/llm-email-optimizer.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : samedi 3 avril 2026</p>
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
<p>Vous pouvez désormais utiliser <strong>Decisioning</strong> pour personnaliser et optimiser le contenu de vos e-mails. Tirez parti des scores de priorité, des formules ou des modèles d’IA pour afficher les offres et le contenu les plus pertinents pour chaque destinataire.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale). Avec cette version de disponibilité générale, les pages miroir sont désormais prises en charge.</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/create-decision-policy.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mardi 6 avril 2026</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#april-26-improv}

#### Intégrations Adobe Experience Manager

<!--* **Adobe Experience Manager Content Fragment context while authoring** - Your Content Fragment selection stays active as you move between text fields and content blocks, so you can add more fragment fields without reopening **Open AEM Content advisor** each time. [Read more](../integrations/aem-fragments.md)

  Availability date: April 1, 2026-->

* **Prise en charge des variations de fragments de contenu Adobe Experience Manager** - Vous pouvez sélectionner **Variations de fragments de contenu** (par exemple, variantes de langue ou de canal) lors de l’insertion de fragments de contenu Adobe Experience Manager, avec une gestion améliorée pour les scénarios régionaux et multilingues. [En savoir plus](../integrations/aem-fragments.md#aem-variations)

  Date de disponibilité : samedi 3 avril 2026


## Notes de mise à jour de mars 2026 {#march-26-rn}

Les sections [Nouvelles fonctionnalités](#march-26-features) et [Améliorations](#march-26-improv) couvrent les fonctionnalités déjà disponibles. La section [bientôt disponible](#coming-soon) répertorie les fonctionnalités et améliorations dont la publication est prévue pour mars.

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

**Date de publication** : 24-25 mars 2026

### Nouvelles fonctionnalités {#march-26-features}

<table>
<thead>
<tr>
<th><strong>Chiffrement des paramètres d'URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les paramètres d’URL dans les liens de tracking et de page de destination ajoutés à vos e-mails peuvent désormais être chiffrés, fournissant ainsi une couche de sécurité supplémentaire pour les données de paramètres sensibles.</p>
<ul>
<li>Enregistrez et gérez les clés de chiffrement dans le registre <strong>Administration</strong> dédié.</li>
<li>Utilisez la nouvelle fonction d’assistance « Encrypt » dans les expressions pour chiffrer les données sensibles dans les URL pour les paramètres de requête que vous souhaitez protéger au moment du rendu.</li>
</ul>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p><img src="assets/do-not-localize/encrypt-helper.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../personalization/url-parameter-encryption.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 31 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Convertir des images en modèles de contenu d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais convertir des images en modèles de contenu d’e-mail directement dans Journey Optimizer. Utilisez l’analyse optimisée par l’IA pour générer automatiquement des modèles HTML structurés à partir de références visuelles, ce qui réduit considérablement le temps de conception des e-mails.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/image-converter.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../content-management/image-to-html.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 31 mars 2026</p>
</td>
</tr>
</tbody>
</table>
<table>
<thead>
<tr>
<th><strong>Boîte de réception</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Boîte de réception</strong> est une fonctionnalité mobile, disponible avec les cartes de contenu, qui permet aux clients de créer un emplacement centralisé dans leur application ou site web pour afficher les messages envoyés à leurs utilisateurs. Cela prolonge la durée de vie des communications marketing en s’assurant que les messages restent accessibles même après leur rejet.</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../inbox/inbox-gs.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 31 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formulaires personnalisés de la page de destination</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec [!DNL Journey Optimizer], vous pouvez capturer les attributs de profil par le biais de vos pages de destination.</p>
<p>Créez, concevez et gérez des formulaires personnalisés adaptés à vos besoins en fonction d’un jeu de données spécifique. Vous pouvez ensuite utiliser ces formulaires dans les pages de destination pour ajouter les attributs de profil de votre choix au jeu de données défini pour chaque formulaire.</p>
<p>Publiée précédemment en disponibilité limitée pour les clients et clientes des États-Unis et d’Australie, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../landing-pages/lp-forms.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : vendredi 26 mars 2026.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activité Test dans les campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle activité <strong>Test</strong> est désormais disponible dans les campagnes orchestrées. Cette activité achemine l’exécution du workflow vers différentes branches en fonction de conditions définies, ce qui vous permet de valider la logique de campagne et les configurations avant d’activer les diffusions actives.</p>
<p><img src="../orchestrated/assets/test-1.png"></p>
<p>Pour plus d’informations, consultez la <a href="../orchestrated/activities/test.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prise en charge de la recherche de jeux de données dans parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle activité <strong>Recherche de jeu de données</strong> dans les parcours vous permet de récupérer dynamiquement des données des jeux de données d’enregistrement Adobe Experience Platform au moment de l’exécution, ce qui vous donne accès à des informations qui ne font pas partie de la payload du profil ou de l’événement, afin que les interactions des clients restent pertinentes et opportunes.</p>
<p>Publiée précédemment en disponibilité limitée pour un ensemble restreint d’organisations, l’activité de recherche de jeu de données dans parcours est désormais disponible pour tous les clients autorisés à effectuer une [recherche de jeu de données](../data/lookup-aep-data.md), tout en restant en disponibilité limitée.</p>
<p><img src="../building-journeys/assets/aep-data-activity.png"></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/dataset-lookup.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>L’activité Action remplace les activités de parcours spécifiques à un canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Suite à la disponibilité générale de l’activité <strong>Action</strong> en février 2026, les activités de canal natives héritées (e-mail, notification push, SMS, in-app, web, expérience basée sur le code et carte de contenu) dans la zone de travail de parcours sont désormais obsolètes.</p>
<p>Vous devez maintenant utiliser l’activité Action unique pour configurer toutes les actions de canal, en remplaçant le besoin de nœuds distincts spécifiques au canal.</p>
<p>Les parcours existants qui utilisent les activités de canal héritées continuent à fonctionner sans aucune modification ni migration requise.</p>
<p><img src="assets/do-not-localize/action-activity.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-action.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Éditeur HTML avancé pour les modèles d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le mode HTML avancé pour les modèles de contenu d’e-mail permet de modifier la source HTML de votre contenu dans le Designer d’e-mail, d’ajouter des expressions avancées (telles que des conditions) dans la source et de basculer entre les vues HTML et Bureau sans perdre vos modifications.</p>
<p>Cette fonctionnalité est disponible dans les modèles de contenu pour le canal E-mail uniquement. Il est actuellement à disponibilité limitée. Contactez votre représentant Adobe pour y accéder.</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../content-management/email-template-expert-mode.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 10 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Intégration de modèles Firefly personnalisés et de modèles de génération d’images tiers</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Activez l’intégration transparente des modèles Firefly standard et personnalisés, ainsi que des modèles d’image tiers approuvés, afin d’offrir une plus grande flexibilité, un meilleur contrôle et un meilleur alignement de la marque lors de la génération d’images.</p>
<p>Choisissez le modèle adapté à vos besoins :</p>
<ul><li> <strong>Adobe model</strong> (optimisé par Firefly Image Model 4) pour la génération immédiate d’images sans configuration supplémentaire</li><li> <strong>Modèle partenaire</strong> (optimisé par Gemini 2.5 Flash) pour des fonctionnalités spécialisées</li><li><strong>Modèles personnalisés</strong> (modèles spécifiques à la marque entraînés sur vos propres ressources) pour une génération sur la marque qui s’aligne précisément sur l’identité, le style et les directives visuelles de votre marque.</li></ul>
<p>Pour plus d’informations, consultez la <a href="../content-management/generative-models.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mardi 2 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activité en direct pour iOS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Proposez des expériences en temps réel directement sur Lock Screens et Dynamic Island de vos clients avec l’<strong>activité iOS Live</strong> dans Adobe Journey Optimizer. Diffusez des mises à jour en direct, depuis le suivi des commandes et du statut des vols jusqu’au décompte des événements, aux scores en direct et à la progression de la diffusion, sans demander aux utilisateurs d’ouvrir votre application. Tenez votre public informé et engagé au bon moment, exactement où il se trouve.</p>
<p>Publiée précédemment en version bêta, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../mobile-live/get-started-mobile-live.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 3 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent : création de contenu de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Optimisé par <strong></strong> <strong>Journey Agent</strong> est disponible dans Journey Optimizer et vous permet d’analyser les parcours par le biais d’une interface en langage naturel. Vous pouvez désormais également générer et gérer du contenu spécifique à un canal directement dans Journey Agent, ce qui permet de créer du contenu pour des canaux tels que les e-mails et les notifications push, d’appliquer et de prévisualiser des modèles, d’affiner le ton et le style par le biais d’invites et d’ouvrir le contenu dans <strong>Content Designer</strong> pour une modification contextuelle.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html" target="_blank">documentation détaillée</a>.</p>
<p>Date de disponibilité : jeudi 4 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Surveillance des modèles d’IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer vous permet désormais de surveiller l’intégrité, le statut de la formation et les performances de vos modèles d’IA de prise de décision. Vous pouvez ainsi vérifier le succès de la formation, résoudre les problèmes et comprendre l’impact sur vos résultats afin de sélectionner les meilleures offres pour chaque client à l’aide de l’IA. Notez que cette fonctionnalité est disponible uniquement pour <strong>Decisioning</strong> (et non pour les modèles de gestion des décisions hérités).</p>
<p>Cette fonctionnalité est actuellement disponible uniquement pour les modèles <strong>optimisation personnalisée</strong> (et non pour l’optimisation automatique).</p>
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/ranking/ai-model-observability.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mardi 9 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Déclencher des campagnes orchestrées à l’aide d’un signal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les campagnes orchestrées peuvent désormais être déclenchées via un signal <strong>API</strong>. Pour configurer ce paramètre, configurez la campagne cible comme <strong>Déclenchée par un signal</strong>, publiez-la, puis déclenchez-la à l’aide d’un appel API. Tous les paramètres inclus dans l’appel API sont disponibles en tant que variables dans la campagne en cours d’exécution. Notez que les campagnes orchestrées déclenchées par signal restent des campagnes <strong>par lots</strong> et sont distinctes des campagnes déclenchées par API.</p>
<p><img src="assets/do-not-localize/oc-triggered.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../orchestrated/trigger-orchestrated-campaign.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Catégorie transactionnelle dans les campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dans les campagnes orchestrées, vous pouvez désormais définir une activité de canal dans la catégorie <strong>Transactionnel</strong>. Cela applique des configurations de canal transactionnel à cette activité. Cette fonctionnalité est utile lorsque les règles métier ne doivent pas s’appliquer ou lorsque l’accord préalable des clients n’est pas requis.</p>
<p><img src="assets/do-not-localize/oc-transactional.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../orchestrated/activities/channels.md#add">documentation détaillée</a>.</p>
<p>Cette fonctionnalité sera progressivement déployée dans toutes les régions au cours des prochains jours.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#march-26-improv}

Les améliorations de cette version sont présentées ci-dessous.

#### Personnalisation

* **Personnalisation complète/de base des URL** - Vous pouvez personnaliser les URL de destination à l’aide d’attributs de profil (par exemple, pour le domaine ou le chemin d’accès). Pour activer cette fonctionnalité, fournissez à Adobe votre liste de domaines acceptés. [En savoir plus](../personalization/personalization-build-expressions.md#where)

  Publiée précédemment en disponibilité limitée et destinée aux parcours, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).

  Date de disponibilité : jeudi 1 avril 2026

#### Création de rapports

* **Optimisation de l’heure d’envoi : emplacement des contrôles mis à jour et nouveau rapport d’effet élévateur** - Les contrôles de l’optimisation de l’heure d’envoi (STO) ont été déplacés vers le menu de configuration des actions. De plus, un nouveau rapport d’effet élévateur est désormais disponible dans les rapports Parcours afin de mesurer l’impact de la STO sur les mesures de performances de vos campagnes. [En savoir plus](../reports/channel-report-cja.md#optimization-models)

  Date de disponibilité : samedi 27 mars 2026

<!--


* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.

#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.-->
<!--
#### Decisioning

* **Optional fragments in decision items** - When using fragments in decision items, you can now make a fragment optional so that if it is temporarily unavailable on Edge, it is skipped and the journey or campaign continues rendering instead of failing.
-->

#### Configuration

<!--* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.-->

* **Échec du renouvellement des certificats de domaine AJO** - Vous pouvez désormais vous abonner pour recevoir des alertes système, par e-mail ou dans le centre de notifications Journey Optimizer, lorsqu’un certificat de domaine utilisé pour la délivrabilité des e-mails approche de son expiration ou a déjà expiré. [En savoir plus](../reports/alerts.md#alert-certificates-renewal-unsuccessful)

  Date de disponibilité : vendredi 26 mars 2026

* **Renommage du jeu de données d’événement de retour du destinataire Secondaire AJO** - Le jeu de données `AJO Email BCC Feedback Event` a été renommé jeu de données `AJO Secondary Recipient Feedback Event`. L’impact varie en fonction de votre situation :

   * **Utilisateurs existants** : seul le nom d’affichage est mis à jour. Le nom de la table sous-jacente reste inchangé.
   * **Nouveaux utilisateurs et sandbox** : le nom d’affichage et le nom du tableau reflètent le nouveau nom.
   * **Utilisateurs existants avec de nouveaux sandbox** : le nom d’affichage et le nom du tableau sont mis à jour vers le nouveau nom.

  Date de disponibilité : mardi 2 mars 2026


#### Parcours

* **Action Mettre à jour le profil : prise en charge de plusieurs attributs de profil** - L’activité d’action **Mettre à jour le profil** prend désormais en charge la mise à jour de cinq attributs de profil au maximum dans un seul nœud. Auparavant, chaque action ne pouvait mettre à jour qu’un seul attribut à la fois, ce qui nécessitait que plusieurs nœuds mettent à jour plusieurs attributs. Utilisez le nouveau bouton **Mettre à jour un autre champ** pour ajouter des paires champ/valeur supplémentaires, ce qui réduit la complexité de la zone de travail et améliore les performances. [En savoir plus](../building-journeys/update-profiles.md)

* **Vague d’envoi des messages sortants dans les parcours** - Vous pouvez désormais planifier la diffusion des messages des parcours Journey Optimizer par lots contrôlés dans le temps. [En savoir plus](../building-journeys/send-using-waves.md)

  Publiée précédemment en disponibilité limitée et destinée aux parcours, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).

  Date de disponibilité : mardi 16 mars 2026

* **Détails de pause et de reprise dans les détails techniques du parcours** - Le parcours **détails techniques** inclut désormais des informations supplémentaires sur la pause et la reprise : la date et l’heure de la dernière pause et reprise, le nom d’affichage et l’identifiant interne de l’utilisateur ou de l’utilisatrice qui a effectué chaque action, ainsi qu’un ensemble complet de paramètres de parcours en pause, tels que le comportement de la pause, la durée maximale de la pause et l’état de reprise automatique. [En savoir plus](../building-journeys/journey-properties.md)

  Date de disponibilité : mardi 2 mars 2026

#### Prise de décision

* **Migration de prise de décision - Attributs d’offre et de contexte** - Le mappage d’entité de l’API de migration répertorie désormais **attributs d’offre** (`migratedofferattributes` sur le schéma d’élément d’offre personnalisée) et **attributs de contexte** (`migratedcontextattributes` sur le schéma du jeu de données de migration). [En savoir plus](../experience-decisioning/decisioning-migration-api.md#entity-mapping)

  Date de disponibilité : mercredi 31 mars 2026

## Bientôt disponible {#coming-soon}

Les fonctionnalités et améliorations ci-dessous devraient être publiées plus tard dans le mois de mars ou début avril. Les dates et la portée des versions sont **modifiables sans préavis**.

<table>
<thead>
<tr>
<th><strong>Expérimentation du chemin du parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilisez le nouveau nœud <strong>Optimiser</strong> pour exécuter des tests A/B ou des expériences de bandit à plusieurs bras afin de déterminer le meilleur moyen d’atteindre vos indicateurs de performance clés orientés métier. Cet outil vous permet de tester, varier et personnaliser les communications, le séquencement et les délais afin d’atteindre avec précision votre clientèle.
</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale). <a href="../building-journeys/optimize.md">En savoir plus</a></p>
<p><img src="assets/do-not-localize/optimize.gif"></p>
<p>Dans le cadre de la disponibilité générale, cette version introduit la sélection <strong>type d’expérience</strong> (A/B ou bandit manchot) et <strong>Mettre à l’échelle le gagnant</strong> pour les parcours unitaires.</p>
<p>Date de disponibilité : mercredi 7 avril 2026</p>
</td>
</tr>
</tbody>
</table>

<!--WAITING RELEASE DATE CONFIRMATION * **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.-->
<!--
WAITING RELEASE DATE CONFIRMATION
* **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.

<--
TO ADD when Path optimization is GA:

* **Experiment type** - You can now choose between A/B experiment (fixed split at the start) or Multi-armed bandit (automatic split with weekly weight updates) when configuring a path experiment.

* **Path experimentation: Scale the Winner** - You can now automatically or manually roll out the winning path of an experiment to your full audience. Once a winner is determined, you can amplify its reach and effectiveness without constantly monitoring the experiment.
This capability is available only in unitary journeys (event-triggered and Audience qualifications). It is not available for Read audience journeys.

-->
