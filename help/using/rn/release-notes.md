---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 902458ec78df9a885b144bf19425c7865c208c28
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 54%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.

## Mises à jour de septembre {#9-2024}

<table>
<thead>
<tr>
<th><strong>Configuration de canal guidée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La configuration guidée du canal vous permet d’automatiser et de valider la configuration du canal dans une expérience unifiée, ce qui accélère le processus de prise en main de Journey Optimizer. Cette nouvelle configuration assistée simplifie la configuration rapide des canaux, en s’assurant que toutes les ressources nécessaires sont facilement installées et qu’elles fonctionnent dans Experience Platform, Journey Optimizer et Data Collection. Cela permet aux équipes d’ingénierie marketing, produit et données de commencer rapidement par la création de campagnes et de parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/set-mobile-config.md">documentation détaillée</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

## Notes de mise à jour d’août 2024 {#8-2024}

**Date de publication** : 20-21 août 2024

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

### Nouvelles fonctionnalités {#8-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<!--
<table>
<thead>
<tr>
<th><strong>Content Cards (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content cards are a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</br>
<p>Content card are currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Amélioration des configurations de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les fonctionnalités actuelles de surface de canal ont été améliorées afin de fournir une approche cohérente sur tous les canaux. Vous pouvez désormais définir, gérer et réutiliser ces configurations pour l’un de vos canaux, y compris les expériences web, les messages in-app ou basées sur le code.</p>
<p><ul>
<li>Les surfaces de canal sont désormais renommées <strong>Configurations de canal</strong>.</li>
<li>Vous pouvez joindre une ou plusieurs actions marketing pour appliquer des stratégies de consentement et de gouvernance des données.</li>
<li>Le contrôle d’accès au niveau de l’objet (OLAC) est désormais disponible pour chaque configuration de canal, ce qui vous permet de décider qui parmi vos utilisateurs et utilisatrices peut créer ou utiliser des configurations spécifiques.</li>
<li>Pour certains canaux, vous pouvez créer des configurations de canal qui ciblent plusieurs plateformes. Il peut s’agir, par exemple, d’une configuration de canal de messagerie in-app pouvant cibler une page web, une application iOS et une application Android.</li>
</ul></p>
<p>Pour plus d’informations, consultez la <a href="../configuration/channel-surfaces.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Action personnalisée Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais intégrer Adobe Journey Optimizer à Adobe Marketo Engage pour créer vos cas d’utilisation B2B. Depuis un parcours, une nouvelle action personnalisée vous permet d’ingérer des données dans Marketo.</p>
<p>Pour plus d’informations, consultez la <a href="../action/marketo-engage.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Variables dans les fragments de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les variables globales de fragment améliorent la fonctionnalité de fragment existante afin d’améliorer l’efficacité pour la réutilisation du contenu et les cas d’utilisation de script. Les fragments peuvent désormais utiliser des variables d’entrée et créer des variables de sortie utilisables dans le contenu des campagnes et des parcours. Les fragments peuvent utiliser des variables d’entrée, à la fois dans les <a href="../personalization/use-expression-fragments.md">fragments d’expression</a> et les <a href="../email/use-visual-fragments.md">fragments visuels</a>. Vous pouvez utiliser ces variables pour personnaliser le contenu et les paramètres de vos messages, dans vos campagnes et parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../personalization/use-expression-fragments.md">documentation détaillée</a>.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Workflow de préchauffage d’adresses IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Date de disponibilité : 13 août</p>
<p>Si vous envoyez des e-mails sur une toute nouvelle adresse IP, vous pouvez désormais facilement exécuter des workflows de préchauffage d’adresses IP directement à partir de l’interface d’utilisation. Adobe Journey Optimizer offre un moyen standardisé et efficace de préchauffer vos adresses IP en respectant les bonnes pratiques de délivrabilité optimale.</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/ip-warmup-gs.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#8-improvements}

Cette version apporte les améliorations répertoriées ci-dessous.

**Parcours**

* Dans l’activité **Condition**, par défaut, la **[!UICONTROL condition de temps]** est désormais définie par heure, de 00:00 à 12:00. [En savoir plus](../building-journeys/condition-activity.md#time_condition)
* Lors de la création de vos parcours, les alertes s’affichent désormais à partir du bouton **Alertes**, afin de s’aligner sur d’autres alertes et d’offrir une expérience utilisateur cohérente. [En savoir plus](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Les options de zoom de la barre d’outils de parcours ont été améliorées : le pourcentage de zoom est désormais visible et vous pouvez désormais réinitialiser plus facilement la valeur de zoom.

<!--**Audiences and Profiles**-->

<!--* The use of audiences from custom upload (CSV file) is now available for use with Privacy and Security Shield add-on.-->
<!--* When targeting a custom upload (CSV file) audience, you can now use attributes from the file in your campaigns and journeys. These attributes are available in the personalization editor, to personalize your messages, and the journey advanced expression editor.-->
<!--* The License usage dashboard now shows the count of Engageable Profiles. [Read more](../audience/license-usage.md)-->

**Canal push**

* Vous pouvez maintenant ajouter vos informations d’identification push d’application mobile dans les paramètres de configuration du canal Adobe Journey Optimizer. La création d’une surface d’application dans la collecte de données Adobe Experience Platform n’est plus nécessaire.

### Autres modifications {#changes}

**Création de rapports**

* L’expérience de création de rapports actuelle sera abandonnée à compter de la version d’octobre. À compter de cette date, la nouvelle expérience de création de rapports deviendra la norme. Nous vous recommandons de vous familiariser avec les nouvelles fonctionnalités pour garantir une transition fluide.

[Prise en main de la nouvelle interface de reporting de Journey Optimizer](../reports/report-gs-cja.md)

* De nouveaux cas d’utilisation ont été ajoutés à la nouvelle expérience de création de rapports :

   * Créez des mesures calculées personnalisées directement dans vos rapports.
   * Création d’une audience à partir des données de rapport.
   * Utilisez l’outil d’analyse exploratoire pour créer facilement des tableaux et des visualisations à partir des **[!UICONTROL Dimensions]** et **[!UICONTROL Mesures]** sélectionnées.

  Pour plus d’informations, consultez la [documentation détaillée](../reports/report-cja-manage.md).
