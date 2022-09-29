---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 056ff0d4532126e22884d73e92fb2e7d3a2319b9
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 28%

---

# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){{target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.

## Version de septembre 2022{#sept-2022-release}

### Nouvelles fonctionnalités{#sept-2022-features}


<!--
<table>
<thead>
<tr>
<th><strong>Dynamic content & new conditional rule builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create dynamic content to adapt the content of your messages based on conditional rules.</p> 
<p>Conditional rules are created using a visual rule builder within the Expression Editor, where you can store them for further reuse across your journeys and campaigns.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>For more information, refer to the <a href="../personalization/get-started-dynamic-content.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Campagnes déclenchées par l’API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Outre les campagnes planifiées existantes, vous pouvez désormais créer des campagnes déclenchées par l’API dans Journey Optimizer et les appeler à partir d’un système externe à l’aide d’API.</p>
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
<p>Grâce au contrôle d’accès basé sur les attributs, les administrateurs peuvent contrôler l’accès à des objets spécifiques en fonction de certains attributs. Ces attributs peuvent être des métadonnées ajoutées à un objet, comme des libellés. À compter de cette version, les administrateurs peuvent également définir des rôles utilisateur ayant accès à des champs et/ou des objets spécifiques, ainsi qu’à des données correspondant à ces champs et/ou objets.</p>
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
<p>Grâce à son cadre de gouvernance DULE (Data Usage Labelling and Enforcement), Journey Optimizer peut désormais tirer parti des stratégies de gouvernance de Adobe Experience Platform pour empêcher l’exportation de champs sensibles vers des systèmes tiers au moyen d’actions personnalisées. Si le système identifie un champ restreint dans les paramètres d’action personnalisée, une erreur s’affiche vous empêchant de publier le parcours.</p>
<p>L’utilisation de l’outil DULE (Data Usage Labelling and Enforcement) est actuellement limitée à certains clients et sera déployée dans tous les environnements dans une prochaine version.</p>
<p>Pour plus d’informations, consultez la <a href="../action/action-privacy.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Application du consentement automatisée (stratégies de consentement)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform vous permet d’adopter et d’appliquer facilement des stratégies marketing afin de respecter les préférences de consentement de vos clients. Les stratégies de consentement sont définies dans Adobe Experience Platform. Dans Journey Optimizer, vous pouvez appliquer ces stratégies de consentement à vos actions personnalisées. Vous pouvez, par exemple, définir des stratégies de consentement afin d’exclure les clients qui n’ont pas consenti à recevoir des communications par courrier électronique, push ou SMS.
<p>L’application automatisée du consentement n’est actuellement disponible que pour les organisations qui ont acheté l’offre complémentaire du Bouclier de santé.</p>
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
<p>Journey Optimizer prend en charge la définition des rôles utilisateur et des stratégies d’accès pour gérer les autorisations des fonctionnalités et des objets. Via <strong>Autorisations Adobe Experience Cloud</strong>, vous pouvez créer et gérer des rôles, ainsi qu’affecter les autorisations de ressources souhaitées pour ces rôles. Les autorisations vous permettent également de gérer les libellés, les sandbox et les utilisateurs associés à un rôle spécifique.</p>
<p> L’utilisation des autorisations est actuellement limitée à certains clients et sera déployée dans tous les environnements dans une version ultérieure.</p>
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
<p>En tant qu’utilisateur de Journey Optimizer, vous pouvez désormais accéder aux alertes système par le biais de l’interface utilisateur afin d’être averti lorsque les parcours ne fonctionnent pas comme prévu. Vous pouvez afficher les alertes disponibles et vous y abonner. La première alerte disponible dans cette version vous avertit si une activité Lecture de segment n’a traité aucun profil pendant la période définie. D’autres informations seront disponibles maintenant que ce workflow est déverrouillé.</p>
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

* Le **Jeu de données d’entité** est désormais disponible en tant que jeu de données d’usine dans Adobe Journey Optimizer. Ce jeu de données de recherche comprend des métadonnées pour enrichir les informations sur les jeux de données de suivi et de retour. Vous pourrez ainsi améliorer vos rapports et requêtes avec des données plus compréhensibles. [En savoir plus](../start/datasets-query-examples.md#entity-dataset)
* Une nouvelle barrière de sécurité a été ajoutée aux parcours unitaires (commençant par un événement ou une qualification de segment) pour empêcher que les parcours ne soient déclenchés par erreur plusieurs fois pour le même événement. La rentrée du profil sera désormais temporairement bloquée par défaut pendant 5 minutes. [En savoir plus](../start/guardrails.md#events-g)

**Administration**

* Lors de l’activation ou de la désactivation de la liste autorisée, un nouvel avertissement s’affiche maintenant pour détailler les impacts de chaque action. [En savoir plus](../configuration/allow-list.md#enable-allow-list)
* Mise à jour de l’interface utilisateur pour la création de surfaces de canal, la création de pools d’adresses IP, la gestion de la liste de suppression et de la liste autorisée, ainsi que la configuration du canal SMS -
<!--* Now when creating the first channel surface for a given subdomain, the processing time will take 10 minutes to 10 days, and only up to 3 hours for subsequent surfaces using that subdomain. Learn more
* Now when downloading the suppression list as a CSV file, you can choose the file that was previously generated, or generate a new file.
* The user interface for creating landing page presets and landing page subdomains has been improved. Learn more -->

**Contrôles de contrôle**

* Avec Journey Optimizer, vous pouvez identifier les actions effectuées par les utilisateurs du système sur différents services et fonctionnalités tels que des campagnes, des parcours, des messages, des landing pages, etc. Les ressources du journal d’audit incluent désormais des modifications sur diverses autres actions et sont enregistrées automatiquement au fur et à mesure de l’activité. En savoir plus [sur cette page](../privacy/audit-logs.md).

**Prise en charge de l’archivage**

* La nouvelle **Jeu de données d’entité** inclut un champ Modèle qui permet d&#39;exporter le format et la structure des messages envoyés sur tous les canaux à des fins d&#39;archivage. [En savoir plus](../configuration/archiving-support.md)

**Pages de destination**

* Vous pouvez désormais utiliser des données contextuelles provenant d&#39;une autre page dans la même landing page. Par exemple, si vous associez une case à cocher à une liste d’abonnements sur la Principale page d’entrée, vous pouvez utiliser cette liste d’abonnements sur la sous-page &quot;merci&quot;. [En savoir plus](../landing-pages/lp-content.md#use-primary-page-context)

* Lors du paramétrage de la Principale page, vous pouvez désormais créer des données additionnelles afin de permettre le stockage des informations lors de l&#39;envoi de la landing page. [En savoir plus](../landing-pages/lp-content.md#use-additional-data)

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Autres modifications{#sept-2022-other}

* Le mode de parcours en rafale a été remplacé par le mode de livraison rapide de Campaign. [En savoir plus](../campaigns/create-campaign.md#rapid-delivery)
* Pour améliorer les performances, les groupes de champs d’événement d’expérience ne peuvent plus être utilisés dans les parcours commençant par un segment Lecture, une qualification de segment ou une activité d’événement professionnel. Cette modification s’applique uniquement aux nouveaux parcours. Ceux qui existent déjà conserveront le comportement actuel. [En savoir plus](../start/guardrails.md#expression-editor)
* La limitation d’une heure pour les parcours de segment de lecture planifiés a été supprimée. Ces parcours peuvent désormais être exécutés sans délai.

