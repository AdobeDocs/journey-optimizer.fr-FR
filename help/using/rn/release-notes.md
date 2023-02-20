---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d160baac2eb454cfd10097e29147562f83c1cd50
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 59%

---

# Notes de mise à jour {#release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour.

Les notes de mise à jour précédentes sont disponibles sur [cette page](release-notes-2022.md). Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.


## Notes de mise à jour initiales de février 2023 {#feb-2023}

Cette section contient des informations sur les versions préliminaires. Les dates de publication, fonctions et autres informations peuvent changer sans préavis. La documentation détaillée sera disponible à la date de publication.

Disponibilité : **22 février 2023**

### Améliorations {#feb-2023-improvements}

**Parcours**

* Le **Période d’attente de rentrée** a été ajouté aux propriétés du parcours. Ce champ vous permet de définir le temps d’attente avant qu’un profil puisse à nouveau entrer dans le parcours en parcours unitaires (en commençant par un événement ou une qualification de segment). Cela empêche les parcours d’être déclenchés plusieurs fois par erreur pour le même événement. Par défaut, le champ est défini sur 5 minutes.

* Des améliorations ont été apportées aux **Dates de début et de fin parcours**. Si vous n’avez pas spécifié de date de début, elle est désormais automatiquement ajoutée au moment de la publication. Pour **Lecture de segment** parcours, vous pouvez maintenant ajouter une date de fin. Cela permet aux profils de se fermer automatiquement lorsque la date est atteinte.

* Le canevas de Parcours a été amélioré pour une expérience utilisateur plus simple et améliorée. À la fin de chaque chemin d’accès dans la zone de travail, les espaces réservés vides ont été supprimés. Vous pouvez désormais simplement ajouter vos activités en les faisant glisser n’importe où entre les noeuds.

* La gestion des délais et des erreurs a été améliorée dans parcours. Les chemins d’expiration et d’erreur sont désormais toujours ajoutés sur la zone de travail. Un nouveau bouton de barre d’outils est disponible pour afficher/masquer ces chemins.

* Introduction d’un nouveau type d’alerte système. Vous pouvez désormais être averti en cas d’échec d’une action personnalisée.


**Administration**

* **Liste autorisée** - Vous pouvez désormais télécharger la liste autorisée sous la forme d’un fichier .csv .

* **Surface des emails** - Une vérification supplémentaire a été ajoutée aux paramètres de surface de l&#39;email : si l’enregistrement MX pour le sous-domaine utilisé dans la variable **Répondre à (email)** ou dans la variable **Adresse email en Cci** n’est pas correctement configuré, la surface de l’email ne peut plus être créée. Vous devez le configurer ou en utiliser un autre.

* **Surface des emails** - Dans la section Paramètres de suivi des URL des paramètres de surface de l’email, la limite pour chaque **Valeur** a été mis à jour de 255 caractères à 5 Ko pour des raisons de compatibilité avec le suivi Adobe Analytics.

**Gestion des décisions**

* **Emplacements** - Des paramètres supplémentaires ont été ajoutés à l’écran de création d’emplacements. Ils vous permettent de contrôler si une offre peut être dupliquée à plusieurs emplacements et de spécifier si le contenu et les métadonnées de l’offre doivent être inclus dans la réponse de l’API.

* **Personnalisation des URL** - Lorsque vous ajoutez des URL en tant que contenu aux représentations de vos offres, vous pouvez désormais personnaliser ces URL à l’aide de l’éditeur d’expression.



## Version de janvier 2023 {#jan-2023-release}

### Nouvelles fonctionnalités{#jan-2023-features}


<table>
<thead>
<tr>
<th><strong>Hygiène des données</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform offre toute une gamme de fonctionnalités d’hygiène des données. Celles-ci vous permettent de gérer vos données stockées par le biais de suppressions programmées d’enregistrements et de jeux de données de consommateurs et consommatrices. Cette fonctionnalité est désormais disponible pour Adobe Journey Optimizer. </p>
<p>Vous pouvez gérer vos stocks de données pour vous assurer que les informations sont utilisées comme prévu, qu’elles sont mises à jour lorsque des données incorrectes doivent être corrigées et qu’elles sont supprimées lorsque les stratégies d’entreprise le jugent nécessaire.</p>
<p><strong>Attention</strong> - Les fonctionnalités d’hygiène des données ne sont actuellement disponibles que pour les organisations qui ont acheté les offres complémentaires <strong>Healthcare Shield</strong> et <strong>Privacy and Security Shield</strong>.</p><p>Pour plus d’informations, consultez la <a href="../privacy/data-hygiene.md">documentation détaillée</a>.

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modèles de contenu d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer des modèles de contenu autonomes qui peuvent être utilisés dans plusieurs parcours et campagnes pour une réutilisation rapide.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Découvrez comment créer, modifier et utiliser des modèles de contenu dans <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=fr">cette vidéo</a>. Pour plus d’informations, consultez la <a href="../email/content-templates.md">documentation détaillée</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#jan-2023-improvements}

**Parcours**

<!--
* The **Re-entrance wait period** field has been added to the journey properties. This field allows you to define the time to wait before allowing a profile to enter the journey again in unitary journeys (starting with an event or a segment qualification). This prevents journeys from being erroneously triggered multiple times for the same event. By default the field is set to 5 minutes. [Learn more](../building-journeys/journey-gs.md#entrance)

* Improvements have been made for **journey start and end dates**. If you have not specified a start date, it is now automatically added at publication time. For **Read segment** journeys, you can now add an end date. This allows profiles to exit automatically when the date is reached. [Learn more](../building-journeys/journey-gs.md#dates)
-->

* Lors de l’ajout d’une **Qualification de segment** ou **Lecture de segment** dans un parcours, l’espace de noms est maintenant prérempli par défaut avec le dernier espace de noms utilisé. Reportez-vous aux sections [Qualification de segment](../building-journeys/segment-qualification-events.md#about-segment-qualification) et [Lecture de segment](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Dans la zone de travail du parcours, un nouveau bouton est disponible dans la barre d’outils. Il permet de télécharger une copie d’écran de votre parcours.

**Concepteur d’e-mail**

* Vous pouvez désormais exporter le contenu de l’e-mail à partir du menu **Exporter le HTML**. Les fichiers exportés sont disponibles dans un fichier d’archive (.ZIP).

**Administration**

* Une nouvelle sous-section fournit des recommandations sur la création de l’adresse **Répondre à (e-mail)** et sur la garantie d’une gestion adéquate des réponses. [En savoir plus](../email/email-settings.md#reply-to-email)

* Lors de la création ou de la modification des **Groupes d’adresses IP**, les enregistrements PTR associés sont désormais affichés dans la liste des adresses IP et lorsque vous passez la souris sur les adresses IP sélectionnées. [En savoir plus](../configuration/ip-pools.md#create-ip-pool)

* Une fois qu’un groupe d’adresses IP a été sélectionné dans la surface d’un canal, les informations d’enregistrement PTR sont désormais visibles lorsque vous passez la souris sur les adresses IP. [En savoir plus](../email/email-settings.md#subdomains-and-ip-pools)

* L’interface utilisateur pour la modification des [enregistrements PTR](../configuration/ptr-records.md#edit-ptr-record) et des [champs d’exécution](../configuration/primary-email-addresses.md) a été mise à jour.

* L’interface utilisateur de création et de modification des sous-domaines a été améliorée. [En savoir plus](../configuration/delegate-subdomain.md)

* La liste de suppression de l’écran **Téléchargements récents** a été mise à jour. [En savoir plus](../configuration/manage-suppression-list.md#recent-uploads)

**Campagnes**

* Un exemple de requête cURL permettant l’exécution de campagnes déclenchées par l’API est désormais généré automatiquement et rendu disponible dans l’écran de la campagne. [En savoir plus](../campaigns/api-triggered-campaigns.md)

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**Personnalisation**

* De nouvelles fonctions d’assistance sont disponibles : formatCurrency, charCodeAt, stringToDate, toString, formatNumber et toHexString. De plus, la fonction toDateTimeOnly accepte désormais les types de champs chaîne, date, long et int. [En savoir plus](../personalization/functions/functions.md)
