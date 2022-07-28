---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3188bc97b8103d2a01101a23d8c242a3e2924f76
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 26%

---

# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){{target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.

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
<p>Journey Optimizer fournit un nouveau flux pour la création de messages dans Parcours. La messagerie en ligne permet aux utilisateurs de gagner du temps et de rationaliser le processus de création et de diffusion d’un email, d’une notification push ou d’un SMS dans Journey Optimizer. En supprimant les messages comme une étape distincte et en les rendant modifiables en ligne dans le cadre d’une action sur le canevas de Parcours, les utilisateurs devront cliquer sur moins de boutons et parcourir moins d’écrans pour concevoir et modifier leur contenu.</p>
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
<p>Vous pouvez désormais identifier les champs de schéma avec des libellés qui définissent les portées d’utilisation des données ou de l’organisation. Les administrateurs peuvent utiliser l’interface Autorisations pour définir des stratégies d’accès couvrant les champs de schéma XDM et mieux gérer l’accès attribué aux utilisateurs ou groupes d’utilisateurs (utilisateurs internes, externes ou tiers) et gérer l’accès à des types de données spécifiques (c’est-à-dire des données personnelles sensibles/SPD).</p>
<p>L’utilisation du contrôle d’accès basé sur les attributs est actuellement limitée à certains utilisateurs et sera déployée dans tous les environnements dans une prochaine version.</p>
<p>Pour plus d’informations, consultez la <a href="../administration/attribute-based-access.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Tâches de prise de décision par lots</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais exécuter des tâches de prise de décision par lots à partir de l’interface utilisateur, de sorte que je n’ai pas besoin d’un développeur pour exécuter des tâches d’api par lots et que je puisse réduire le temps nécessaire au marketing. Cette nouvelle interface vous permet de créer des tâches et de gérer les tâches actuelles/antérieures.</p>
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
<p>Vous pouvez désormais utiliser des systèmes de modèles d’optimisation personnalisés dans la gestion de la décision. Ce nouveau type de modèle permet d’optimiser et de personnaliser les offres en fonction des segments et des performances des offres.</p>
<p>L’utilisation des modèles d’optimisation personnalisée d’AI est actuellement limitée à certains utilisateurs et sera déployée dans tous les environnements dans une prochaine version.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Pour plus d'informations, consultez la <a href="../offers/ranking/personalized-optimization-model.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

<!--
**Journeys**

* **Ending a journey** - In the journey canvas, the **End** activity has been removed from the palette. End tags are now added by default at the end of each path and cannot be removed. This improvement allows better reporting of where a customer dropped out of the journey, without any action from the user.
-->

**Messages**

* Les paramètres de message prédéfinis sont désormais **surfaces des canaux**. [En savoir plus](../configuration/channel-surfaces.md)

**Administration**

* **Modification des enregistrements PTR** - Désormais, lors de la mise à jour d’un enregistrement PTR, le temps de traitement ne prendra que 3 heures. [En savoir plus](../configuration/ptr-records.md#processing)

* **Interface utilisateur de Liste autorisée** - Vous pouvez désormais utiliser l’interface utilisateur de Journey Optimizer pour ajouter de nouvelles adresses électroniques ou de nouveaux domaines à la liste autorisée. [En savoir plus](../configuration/allow-list.md)

* **Mise à jour de la logique de liste autorisée** - Désormais, la logique de liste autorisée s’applique dès que la fonction est activée, même si la liste est vide. [En savoir plus](../configuration/allow-list.md#logic)

* **Paramètres de suivi des URL** - Vous pouvez désormais utiliser l’éditeur d’expression pour configurer les paramètres de suivi d’URL sur vos surfaces d’email (c’est-à-dire les paramètres prédéfinis de message). [En savoir plus](../configuration/email-settings.md#url-tracking)

**Offer Decisioning**

* **Taille de l’audience** - Un nouveau composant d’estimation de la taille de l’audience s’affiche désormais dans l’interface utilisateur lors de la création d’une règle de décision, lors de la sélection d’un segment ou d’une règle pour définir l’éligibilité d’une offre ou lors de l’ajout d’un segment ou d’une règle à une portée de décision.