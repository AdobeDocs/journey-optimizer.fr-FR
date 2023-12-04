---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 299b34dec2e864fff5eb874b3fd491da80bc0c16
workflow-type: ht
source-wordcount: '418'
ht-degree: 100%

---

# Notes de mise à jour {#release-notes}


>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour.

Les notes de mise à jour précédentes sont disponibles sur [cette page](release-notes-2023.md). Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.

## Notes de mise à jour d’octobre 2023 {#oct-rn-2023}

### Nouvelles fonctionnalités{#oct-2023-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Outil Sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’outil Sandbox vous permet de copier des objets sur plusieurs sandbox en exploitant l’export et l’import de packages. Un package peut se composer d’un ou de plusieurs objets. Tous les objets inclus dans un package doivent provenir du même sandbox.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<p>Pour plus d’informations, consultez la <a href="../building-journeys/copy-to-sandbox.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>MMS (Multimedia Message Service, service de messagerie multimédia) dans les SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec le canal SMS, vous pouvez maintenant améliorer votre communication en envoyant des MMS, ce qui permet le partage d’images, de GIF ou de vidéos avec vos clientes et clients. Notez que cette fonctionnalité est actuellement disponible avec Sinch uniquement.</p>
<img src="assets/do-not-localize/mms.gif"/>
<p>Pour plus d’informations, consultez la <a href="../sms/create-sms.md#mms-content">documentation détaillée</a>.</p>
</tr>
</tbody>
</table>

### Améliorations {#oct-2023-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Audiences**

* Vous pouvez désormais cibler les audiences chargées à partir d’un fichier CSV dans les parcours et les campagnes. [En savoir plus](../audience/about-audiences.md#segments-in-journey-optimizer)
* Vous pouvez désormais cibler les audiences créées par le biais de la composition de l’audience et utiliser les attributs d’enrichissement dans les parcours. [En savoir plus](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>Ces fonctionnalités sont actuellement disponibles en version bêta privée.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Campagnes**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* Lorsqu’une erreur se produit dans l’une de vos campagnes, une icône d’avertissement s’affiche désormais dans la liste des campagnes avec le statut de la campagne. [En savoir plus](../campaigns/modify-stop-campaign.md#statuses)

**Parcours**

* La durée maximale que vous pouvez définir dans n’importe quel temps d’attente est désormais de 29 jours au lieu de 30. Cette amélioration a été introduite afin d’éviter que les temps d’attente ne dépassent la durée de vie de 30 jours du parcours. Cela s’applique aux éléments suivants :

   * Le champ **Durée** dans l’[activité d’attente](../building-journeys/wait-activity.md).
   * La **période d’attente de reprise** dans les [propriétés du parcours](../building-journeys/journey-gs.md#entrance).
   * Le champ **Attendre pendant** dans la définition du délai d’expiration des [activités d’événement](../building-journeys/general-events.md#events-specific-time).

<!--
**Consent in channel configuration**

* You can now select a marketing action at the channel surface level. When used in a surface, all consent policies associated with that marketing action are leveraged in order to respect the preferences of your customers.-->

**Gestion des décisions**

* Plusieurs libellés relatifs à la limitation des offres dans l’interface de gestion des décisions ont été mis à jour. [En savoir plus](../offers/offer-library/add-constraints.md#capping)

