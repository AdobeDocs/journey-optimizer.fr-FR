---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 4df89a36705fb53984ba04ba1ae2f45554e47f77
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 19%

---

# Notes de mise à jour {#release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour.

Les notes de mise à jour précédentes sont disponibles dans [cette page](release-notes-2022.md). Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous au [newsletter trimestrielle Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour de produits, des articles passionnants, des cas d’utilisation, des conseils, etc. directement dans votre boîte de réception tous les trimestres.


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
<p>Adobe Experience Platform fournit une suite de fonctionnalités d’hygiène des données qui vous permet de gérer vos données stockées par le biais de suppressions programmatiques des enregistrements de consommateurs et des jeux de données. Cette fonctionnalité est désormais disponible pour Adobe Journey Optimizer. </p>
<p>Vous pouvez gérer vos entrepôts de données pour vous assurer que les informations sont utilisées comme prévu, qu’elles sont mises à jour lorsque des données incorrectes doivent être corrigées et qu’elles sont supprimées lorsque les stratégies d’entreprise le jugent nécessaire.</p>
<p><strong>Attention</strong> - Les fonctionnalités d’hygiène des données ne sont actuellement disponibles que pour les organisations qui ont acheté la variable <strong>Bouclier de santé</strong> et <strong>Protection de la vie privée et protection</strong> offres complémentaires.</p><p>Pour plus d’informations, consultez la <a href="../privacy/data-hygiene.md">documentation détaillée</a>.

</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modèles de contenu email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer des modèles de contenu autonomes qui peuvent être utilisés dans plusieurs parcours et campagnes pour une réutilisation rapide.</p> 
</p>
<!--img src="assets/do-not-localize/"/-->
<p>Découvrez comment créer, modifier et utiliser des modèles de contenu dans <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html">cette vidéo</a>.
<p>Pour plus d'informations, consultez la <a href="../email/content-templates.md">documentation détaillée</a>.
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

* Lors de l’ajout d’une **Qualification du segment** ou **Lecture de segment** dans un parcours, l’espace de noms est maintenant prérempli par défaut avec le dernier espace de noms utilisé. Reportez-vous à la section [Qualification du segment](../building-journeys/segment-qualification-events.md#about-segment-qualification) et [Lecture de segment](../building-journeys/read-segment.md#configuring-segment-trigger-activity) sections.

* Dans la zone de travail du parcours, un nouveau bouton est disponible dans la barre d’outils. Il permet de télécharger une capture d’écran de votre parcours.

**Concepteur d’email**

* Vous pouvez désormais exporter le contenu de l’email à partir du **HTML d’exportation** . Les fichiers exportés sont disponibles dans un fichier d’archive (.ZIP).

**Administration**

* Une nouvelle sous-section fournit des recommandations sur la création de la variable **Répondre à (email)** et assurer une gestion adéquate des réponses. [En savoir plus](../email/email-settings.md#reply-to-email).

* Lors de la création ou de la modification **Groupes IP**, les enregistrements PTR associés sont désormais affichés dans la liste des adresses IP et lorsque vous passez la souris sur les adresses IP sélectionnées. [En savoir plus](../configuration/ip-pools.md#create-ip-pool).

* Une fois qu’un pool d’adresses IP a été sélectionné à la surface d’un canal, les informations d’enregistrement du PTR sont désormais visibles lorsque vous pointez sur les adresses IP. [En savoir plus](../email/email-settings.md#subdomains-and-ip-pools).

* Interface utilisateur pour la modification [Enregistrements PTR](../configuration/ptr-records.md#edit-ptr-record) et [Champs d&#39;exécution](../configuration/primary-email-addresses.md) a été mis à jour.

* L’interface utilisateur de création et de modification des sous-domaines a été améliorée. [En savoir plus](../configuration/delegate-subdomain.md).

* Liste de suppression **Chargements récents** a été mis à jour. [En savoir plus](../configuration/manage-suppression-list.md#recent-uploads)

**Campagnes**

* Un exemple de requête cURL permettant l’exécution de campagnes déclenchées par l’API est désormais généré automatiquement et rendu disponible dans l’écran de la campagne. [En savoir plus](../campaigns/api-triggered-campaigns.md)

<!--
**Decision management**

* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--* It is now possible to reset the offer capping counter on a daily, weekly or monthly basis. [Learn more](../offers/offer-library/add-constraints.md#capping)-->

**Personnalisation**

* De nouvelles fonctions d’assistance sont disponibles : formatCurrency, charCodeAt, stringToDate, toString, formatNumber et toHexString. De plus, la fonction toDateTimeOnly accepte désormais les types de champs string, date, long et int. [En savoir plus](../personalization/functions/functions.md).
