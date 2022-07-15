---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ac3c49c16a2496b3d5bc9b803589644b69c6565c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){{target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.

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
<img src="assets/do-not-localize/SMS.gif"/>
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
<img src="assets/do-not-localize/stock-rn.gif"/>
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
<img src="assets/do-not-localize/bcc-rn.gif"/>
<p>Pour plus d’informations, consultez la <a href="../configuration/bcc-email.md">documentation détaillée</a>.</p>
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

<!--table>
<thead>
<tr>
<th><strong>Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content. In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Améliorations

**Gestion des décisions**

* **Prise en charge des fichiers HTML et JSON** - Vous pouvez désormais glisser-déposer des fichiers HTML et JSON externes de la bibliothèque de ressources d’Adobe Experience Cloud au contenu de rendu de l’offre. [En savoir plus](../offers/offer-library/add-representations.md#html-json)


**E-mail**

* **Enregistrer en tant que modèle** - Vous pouvez désormais enregistrer un contenu d’e-mail en tant que modèle et le réutiliser lors de la création d’autres messages. [En savoir plus](../design/email-templates.md)

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.

-->

**Administration**

<!--* **Allowed list in the UI** - You can now use the Journey Optimizer user interface to add new email addresses or domains to the allowed list.-->

* **Aperçu des paramètres d’URL de suivi** - Lors de la configuration d’un préréglage de message, si vous définissez des paramètres de suivi des URL, un aperçu dynamique de l’URL de suivi résultante s’affiche désormais. [En savoir plus](../configuration/email-settings.md#url-tracking)

* **Modification des préréglages de message** : lors de la mise à jour d’un préréglage de message, le temps de traitement ne peut désormais excéder 3 heures. [En savoir plus](../configuration/message-presets.md#edit-message-preset)

* **Modification du groupe d’adresses IP** : lors de la mise à jour d’un groupe d’adresses IP, le temps de traitement ne peut désormais excéder 3 heures. [En savoir plus](../configuration/ip-pools.md#edit-ip-pool)

<!--* **Personalize tracking URL parameters** - You can now use the Expression Editor to configure URL tracking parameters in your message presets. [Learn more](../configuration/email-settings.md#url-tracking)-->

<!--
**Reporting**

* **Performance measurement** - A new **Reporting** tab is now available in the Administration > Configurations menu to set up reporting data sources.
-->
