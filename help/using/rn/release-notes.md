---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0fc693054ad7931545e0053249f310aed031c8c4
workflow-type: tm+mt
source-wordcount: '1295'
ht-degree: 90%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.


## Notes de mise à jour anticipées de juillet 2024 {#27-4-2024}

**Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version**. Les liens, les écrans et la documentation mise à jour sont publiés sur cette page à la date de publication.

**Date de version** : 30-31 juillet 2024

### Nouvelles fonctionnalités {#27-4-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Canal SMS avec n’importe quel fournisseur (version bêta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais configurer d’autres fournisseurs de SMS dans Journey Optimizer, en plus des fournisseurs par défaut Sinch, Infobip et Twilio.</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>Pour plus d’informations, consultez la <a href="../sms/sms-configuration-custom.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Composition d’audience fédérée (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La composition d’audiences fédérées est désormais disponible dans Adobe Journey Optimizer. Il permet aux entreprises de composer des données pour une meilleure utilisation dans divers cas d’utilisation. Grâce à cette nouvelle approche, en tant qu’utilisateur Adobe Real-Time Customer Data Platform et/ou Adobe Journey Optimizer, vous pouvez fédérer les jeux de données directement à partir de votre entrepôt de données existant pour créer et enrichir les audiences et attributs Adobe Experience Platform dans un seul système.</p>
<p>Pour plus d’informations, consultez la <a href="https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home"  target="_blank">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#27-4-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Parcours**

* (Date de disponibilité : 8 juillet) **Éditeur d’expression avancé dans la configuration d’événement de parcours** - Vous pouvez désormais utiliser l’éditeur d’expression avancé lors de la configuration d’un événement, ce qui vous permet de définir des expressions plus complexes ou d’utiliser des fonctions dans la condition d’identifiant d’événement. [En savoir plus](../event/about-creating.md#adv-exp-editor)

**Audiences**

* L’utilisation d’audiences issues d’un chargement personnalisé (fichier CSV) est désormais disponible avec Privacy and Security Shield.

## Notes de mise à jour de juin 2024 {#24-6-2024}

**Date de publication** : 18-19 juin 2024

### Nouvelles fonctionnalités {#june-24-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Personnalisation des fragments de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des champs spécifiques dans un fragment qui peuvent être modifiés lors de l’ajout du fragment à une campagne ou à un parcours. Cela permet d’ajuster les portions de contenu au moment de l’utilisation, ce qui offre la possibilité de remplacer les valeurs par défaut par des informations spécifiques au contexte.</p>
<img src="../content-management/assets/do-not-localize/gif-fragments.gif"/>
<p>Pour plus d’informations, consultez la <a href="../content-management/customizable-fragments.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Créer des rapports avec Customer Journey Analytics (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La création de rapports Journey Optimizer est fournie avec une interopérabilité améliorée avec les fonctionnalités de Customer Journey Analytics, ce qui permet de normaliser la création de rapports sur les deux plateformes et d’améliorer la cohérence et la fiabilité des données. Cette intégration transparente entre Journey Optimizer et Customer Journey Analytics offre une vue plus claire des mesures de performances, ce qui permet aux utilisateurs et utilisatrices de prendre des décisions plus éclairées.</p>
<img src="assets/do-not-localize/ajo-cja.gif"/>
<p>Pour plus d’informations, consultez la <a href="../reports/report-gs-cja.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Assistant IA dans Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’assistant IA est une fonctionnalité de l’interface d’utilisation qui vous permet de parcourir et de comprendre les concepts Adobe et d’obtenir des informations opérationnelles sur votre environnement spécifique. Il est disponible dans plusieurs produits Adobe Experience Cloud, y compris Adobe Journey Optimizer.</p>
<p>Pour plus d’informations, consultez la <a href="../start/ai-assistant.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Messages multilingues dans les parcours et les campagnes (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer facilement du contenu dans plusieurs langues au sein d’une campagne ou d’un parcours. Grâce à cette fonctionnalité, vous pouvez passer d’une langue à une autre lors de la modification de votre campagne ou de votre parcours, ce qui optimise l’ensemble du processus de modification et améliore votre capacité à gérer efficacement du contenu multilingue.</p>
<p>Le contenu multilingue n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Expérimentation dans les parcours (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Déjà disponible dans les campagnes, Adobe Journey Optimizer prend désormais en charge les expérimentations dans les parcours. Les expériences sont des essais randomisés, ce qui, dans le cadre des tests en ligne, signifie que vous exposez certains utilisateurs et utilisatrices sélectionnés de manière aléatoire à une variante donnée d’un message et un autre ensemble d’utilisateurs et utilisatrices sélectionnés de manière aléatoire à une autre variation de traitement. Après l’exposition, vous pouvez ensuite mesurer les mesures de résultats qui vous intéressent, par exemple les ouvertures d’e-mails, les abonnements ou les achats.</p>
<p>L’expérimentation dans les parcours n’est actuellement disponible que pour un ensemble donné d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Améliorations {#june24-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

#### Gestion des décisions

* **Prise en charge de plusieurs règles dans la gestion des décisions** : vous pouvez désormais ajouter jusqu’à 10 règles de limitation pour une offre donnée dans la gestion des décisions. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées. [En savoir plus](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

#### Fragments de contenu

>[!AVAILABILITY]
>
>Notez que ces améliorations seront progressivement déployées dans les jours qui suivront la version initiale. Certains utilisateurs et utilisatrices auront un accès immédiat, mais d’autres peuvent rencontrer un retard avant que cela ne soit disponible dans leurs environnements.

* Les fragments peuvent désormais être modifiés et les modifications peuvent être propagées dans tous les parcours actifs et toutes les campagnes dans lesquels elles sont utilisées.
* De nouveaux statuts pour les fragments de contenu ont été ajoutés : **Brouillon**, **Actif**, **Publication** et **Archivé**.
* Pour utiliser un fragment dans un parcours ou une campagne, il doit maintenant se trouver au statut **Actif**. Une nouvelle étape a été ajoutée au processus de création de fragment, permettant de publier le fragment et de le rendre disponible à l’utilisation dans les parcours et les campagnes. Notez que la publication de fragments nécessite une nouvelle autorisation.

  **ATTENTION** : depuis l’introduction des statuts **Brouillon** et **Actif** avec la version de juin de Journey Optimizer, tous les fragments créés avant cette version ont le statut **Brouillon**, même s’ils sont utilisés dans un parcours ou une campagne. Si vous apportez des modifications à ces fragments, vous devez [les publier](../content-management/create-fragments.md#publish) pour les rendre « actives » et les propager aux campagnes et parcours associés. Vous devez également créer une version de parcours/campagne et la publier.

En savoir plus dans la documentation sur les [fragments de contenu](../content-management/fragments.md).

#### Parcours

* Le délai d’expiration global des parcours a été étendu à 91 jours. [En savoir plus](../building-journeys/journey-properties.md#global_timeout)

  Ce nouveau délai d’expiration sera pris en compte pour tous les nouveaux parcours créés. Consultez cette [section Questions fréquentes](../building-journeys/journey-properties.md#timeout-faq) pour en savoir plus. Notez que ces modifications seront progressivement appliquées au cours du mois de juin.


* Adobe Journey Optimizer prend désormais en charge les demandes de suppression/d’accès pour les informations personnelles ainsi que les demandes de gestion du cycle de vie des données. [En savoir plus](../privacy/requests.md)
* Vous pouvez désormais redimensionner les colonnes de l’inventaire des parcours.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* **Les politiques de fusion** sont maintenant disponibles de manière générale : les politiques de fusion utilisées par un parcours sont désormais visibles et cohérentes dans l’ensemble du parcours. [En savoir plus](../building-journeys/journey-properties.md#merge-policies)



#### Campagnes

* Lors de la création d’une campagne dans Adobe Journey Optimizer, vous pouvez désormais choisir le type de campagne (planifiée ou déclenchée) dans une nouvelle boîte de dialogue modale. [En savoir plus](../campaigns/create-campaign.md)

#### Canal e-mail

* **Désabonnement de la liste** : comme suite aux récentes annonces Gmail et Yahoo! concernant les expéditions en masse, Journey Optimizer prend en charge l’option de désabonnement de la liste « post/1-click ». Consultez les pages suivantes : [Gestion du processus de désinscription aux e-mails](../email/email-opt-out.md#unsubscribe-header) et [Configurer les paramètres d’e-mail](../email/email-settings.md#list-unsubscribe).

  **NOTE** : pour toute nouvelle surface de canal, l’option d’en-tête de désabonnement de la liste est activée par défaut. Pour les surfaces existantes, l’option URL de désabonnement en un clic dans les paramètres de surface de canal est décochée par défaut. Si vous utilisiez précédemment une URL d’opt-out en un clic dans le corps de l’e-mail, ce paramètre est toujours valide. Si l’URL de désabonnement en un clic est cochée dans les paramètres de surface de canal, Adobe Journey Optimizer préférera utiliser l’URL de désabonnement en un clic générée par défaut dans les paramètres de surface de canal.

#### Canal SMS

* Vous pouvez désormais ajouter des codes courts uniques pour chaque sandbox avec une seule configuration d’API, ce qui rend le processus plus efficace et plus simple. [En savoir plus](../sms/sms-configuration.md)

* Après la création, le champ **Jeton API** sur le page **Détails des informations d’identification de l’API** est désormais masqué.

<!--* You can now modify existing SMS configurations.-->

#### Canal in-app

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* Vous pouvez désormais utiliser le plug-in Edge Delivery pour obtenir les informations nécessaires pour comprendre et résoudre les problèmes liés à vos implémentations entrantes. [En savoir plus sur la vue Edge Delivery](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


#### Canal de publipostage direct

* Le canal de publipostage direct est désormais disponible pour l’ensemble des clientes et clients. [En savoir plus](../direct-mail/get-started-direct-mail.md)

