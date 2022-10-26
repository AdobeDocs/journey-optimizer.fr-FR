---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 95%

---

# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.


## Octobre 2022 {#oct-2022-release}

### Améliorations{#oct-2022-improvements}

**Parcours**

* Le **Force une réentrée sur une période récurrente** a été ajoutée dans les paramètres de planification de segments de lecture récurrente. Cette option permet de faire en sorte que tous les profils toujours présents dans le parcours le quittent automatiquement lors de la prochaine exécution. Lorsque l’option est désactivée, les profils doivent terminer le parcours avant de pouvoir entrer à nouveau dans une autre occurrence. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

## Version de septembre 2022{#sept-2022-release}

### Nouvelles fonctionnalités{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>Contenu dynamique et nouveau créateur de règles conditionnelles</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant créer du contenu dynamique pour adapter le contenu de vos messages selon des règles conditionnelles.</p> 
<p>Les règles conditionnelles sont créées à l’aide d’un créateur de règles visuel dans l’éditeur d’expression, où vous pouvez les stocker pour les réutiliser ultérieurement dans vos parcours et campagnes.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>Pour plus d’informations, consultez la <a href="../personalization/get-started-dynamic-content.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campagnes déclenchées par l’API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Outre les campagnes planifiées existantes, vous pouvez désormais créer des campagnes déclenchées par l’API dans Journey Optimizer et les appeler à partir d’un système externe à l’aide d’API.</p>
<p>Vous pouvez ainsi couvrir divers besoins de messagerie opérationnelle et transactionnelle tels que les réinitialisations de mot de passe, le jeton OTP, etc.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Pour plus d’informations, consultez la <a href="../campaigns/api-triggered-campaigns.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Contrôle d’accès aux données</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce au contrôle d’accès basé sur les attributs, les administrateurs peuvent contrôler l’accès à des objets spécifiques en fonction de certains attributs. Ces attributs peuvent être des métadonnées ajoutées à un objet, comme des libellés. À compter de cette version, les administrateurs peuvent également définir des rôles utilisateur ayant accès à des champs et/ou des objets spécifiques, ainsi qu’aux données qui correspondent à ces champs et/ou objets.</p>
<p> L’utilisation du contrôle d’accès basé sur les attributs est actuellement limitée à certains clients et sera déployée dans tous les environnements dans une prochaine version.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>Pour plus d’informations, consultez la <a href="../administration/object-based-access.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Gouvernance et confidentialité des données</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce à son cadre de gouvernance DULE (Data Usage Labelling and Enforcement), Journey Optimizer peut désormais tirer parti des politiques de gouvernance d’Adobe Experience Platform pour empêcher l’exportation de champs sensibles vers des systèmes tiers au moyen d’actions personnalisées. Si le système identifie un champ restreint dans les paramètres d’action personnalisée, une erreur s’affiche, vous empêchant de publier le parcours.</p>
<p>L’utilisation de l’outil DULE (Data Usage Labelling and Enforcement) est actuellement limitée à certains clients et sera déployée dans tous les environnements dans une prochaine version.</p>
<p>Pour plus d’informations, consultez la <a href="../action/action-privacy.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Application du consentement automatisée (politiques de consentement)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform vous permet d’adopter et d’appliquer facilement des stratégies marketing afin de respecter les préférences de consentement de vos clients. Les stratégies de consentement sont définies dans Adobe Experience Platform. Dans Journey Optimizer, vous pouvez appliquer ces politiques de consentement à vos actions personnalisées. Par exemple, vous pouvez définir des politiques de consentement pour exclure les clients qui n’ont pas consenti à recevoir des communications par e-mail, push ou SMS.
<p>L’application automatisée du consentement n’est actuellement disponible que pour les organisations qui ont acheté le module complémentaire Healthcare Shield.</p>
<p>Pour plus d’informations, consultez la <a href="../action/consent.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestion des autorisations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer prend en charge la définition des rôles utilisateur et des stratégies d’accès pour gérer les autorisations des fonctionnalités et des objets. Grâce aux <strong>autorisations Adobe Experience Cloud</strong>, vous pouvez créer et gérer des rôles, ainsi qu’attribuer les autorisations de ressource souhaitées pour ces rôles. Les autorisations vous permettent également de gérer les libellés, les sandbox et les utilisateurs associés à un rôle spécifique.</p>
<p> L’utilisation des autorisations est actuellement limitée à certains utilisateurs et sera déployée dans tous les environnements dans une prochaine version.</p>
<p>Pour plus d’informations, consultez la <a href="../administration/attribute-based-access.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alertes et surveillance</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En tant qu’utilisateur de Journey Optimizer, vous pouvez désormais accéder aux alertes système par le biais de l’interface utilisateur afin d’être averti lorsque les parcours ne fonctionnent pas comme prévu. Vous pouvez afficher les alertes disponibles et vous y abonner. La première alerte disponible dans cette version vous avertit si une activité Lecture de segment n’a traité aucun profil pendant la période définie. D’autres informations seront disponibles maintenant que ce workflow est déverrouillé.</p>
<p>Pour plus d'informations, consultez la <a href="../reports/alerts.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Améliorations{#sept-2022-improvements}

**Parcours**

* Le **jeu de données d’entité** est désormais disponible en tant que jeu de données prêt à l’emploi dans Adobe Journey Optimizer. Ce jeu de données de recherche comprend des métadonnées pour enrichir les informations des jeux de données de tracking et de commentaires. Vous pourrez ainsi améliorer vos rapports et requêtes avec des données plus compréhensibles. [En savoir plus](../start/datasets-query-examples.md#entity-dataset)
* Une nouvelle barrière de sécurité a été ajoutée aux parcours unitaires (commençant par un événement ou une qualification de segment) pour empêcher que les parcours ne soient déclenchés par erreur plusieurs fois pour le même événement. La reprise du profil sera désormais temporairement bloquée par défaut pendant 5 minutes. [En savoir plus](../start/guardrails.md#events-g)

**Administration**

* Lors de l’activation ou de la désactivation de la liste autorisée, un nouveau message d’avertissement s’affiche désormais pour détailler les impacts de chaque action. [En savoir plus](../configuration/allow-list.md#enable-allow-list)
* Mise à jour de l’interface utilisateur pour la création de surfaces de canal, la création de groupes d’adresses IP, la gestion de la liste de suppression et de la liste autorisée, ainsi que la configuration du canal SMS.
* Désormais, lors de la création de la première surface de canal pour un sous-domaine donné, le temps de traitement prendra entre 10 minutes et 10 jours, et jusqu’à 3 heures uniquement pour les surfaces suivantes utilisant ce sous-domaine. [En savoir plus](../configuration/channel-surfaces.md#create-channel-surface)

<!--* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.-->
* Mise à jour de l’interface utilisateur pour la création de préréglages de pages de destination et de sous-domaines de pages de destination. [En savoir plus](../configuration/lp-subdomains.md)

**Contrôles d’audit**

* Avec Journey Optimizer, vous pouvez identifier les actions effectuées par les utilisateurs du système sur divers services et fonctionnalités tels que les campagnes, les parcours, les messages, les pages de destination, etc. Les ressources du journal d’audit incluent désormais des modifications sur diverses autres actions et sont enregistrées automatiquement au fur et à mesure de l’activité. En savoir plus [sur cette page](../privacy/audit-logs.md).

**Prise en charge de l’archivage**

* Le nouveau **jeu de données d’entité** inclut un champ Modèle qui permet d&#39;exporter le format et la structure des messages envoyés sur tous les canaux à des fins d&#39;archivage. [En savoir plus](../configuration/archiving-support.md)

**Pages de destination**

* Vous pouvez désormais utiliser des données contextuelles provenant d&#39;une autre page dans la même page de destination. Par exemple, si vous associez une case à cocher à une liste d’abonnements sur la page de destination principale, vous pouvez utiliser cette liste d’abonnements sur la sous-page « merci ». [En savoir plus](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Autres modifications{#sept-2022-other}

* Le mode de parcours en rafale a été remplacé par le mode de diffusion rapide des campagnes. [En savoir plus](../campaigns/create-campaign.md#rapid-delivery)
* Pour améliorer les performances, les groupes de champs d’événement d’expérience ne peuvent plus être utilisés dans les parcours commençant par un segment Lecture, une qualification de segment ou une activité d’événement métier. Cette modification s’applique uniquement aux nouveaux parcours. Ceux qui existent déjà conserveront le comportement actuel. [En savoir plus](../start/guardrails.md#expression-editor)
* La limitation d’une heure pour les parcours de segment de lecture planifiés a été supprimée. Ces parcours peuvent désormais être exécutés sans délai.

