---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 2fe963b43f08a99e000a916571f5b04a4a96c845
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 47%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.

## Notes de mise à jour anticipées d’août 2024 {#e-2024}

**Date de publication** : 20-21 août 2024

>[!CAUTION]
>
>**Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les écrans et la documentation mise à jour sont publiés à la date de publication.
>

### Nouvelles fonctionnalités {#e-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

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
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Cartes de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La carte de contenu est une nouvelle fonctionnalité de messagerie numérique de Adobe Journey Optimizer qui fournit du contenu personnalisé et attrayant directement dans les applications mobiles et les sites web. Contrairement aux notifications push traditionnelles, les cartes de contenu s’intègrent de manière transparente à l’interface utilisateur, offrant des mises à jour persistantes et non intrusives qui améliorent l’interaction et l’expérience utilisateur.</p>
<p>Grâce à cette fonctionnalité, les marketeurs peuvent présenter du contenu multimédia pertinent aux utilisateurs, augmenter l’engagement des utilisateurs et veiller à ce que les messages importants soient affichés sans interrompre le parcours de l’utilisateur.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Amélioration des configurations de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les fonctionnalités actuelles de surface de canal ont été améliorées pour une approche cohérente sur tous les canaux. Vous pouvez désormais définir, gérer et réutiliser ces configurations pour l’un de vos canaux, y compris les expériences web, les messages in-app ou basées sur le code.</p>
<p><ul>
<li>Les surfaces de canal sont désormais renommées <strong>Configurations de canal</strong></li>
<li>Vous pouvez joindre une ou plusieurs actions marketing pour appliquer des stratégies de consentement et de gouvernance des données.</li>
<li>Le contrôle d’accès au niveau de l’objet (OLAC) est désormais disponible pour chaque configuration de canal, ce qui vous permet de décider lequel de vos utilisateurs est autorisé à créer ou à utiliser des configurations spécifiques.</li>
<li>Pour certains canaux, vous pouvez créer des configurations de canal qui ciblent plusieurs plateformes. Il peut s’agir, par exemple, d’une configuration de canal de messagerie in-app pouvant cibler une page web, une application iOS et une application Android.</li>
</ul></p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Action personnalisée Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais intégrer Adobe Journey Optimizer à Adobe Marketo Engage pour créer vos cas d’utilisation B2B. Depuis un parcours, une nouvelle action personnalisée vous permet d’ingérer des données dans Marketo.</p>
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
<p>Les fragments peuvent désormais utiliser des variables d’entrée, à la fois dans les <a href="../personalization/use-expression-fragments.md">fragments d’expression</a> et les <a href="../email/use-visual-fragments.md">fragments visuels</a>. Vous pouvez utiliser ces variables pour personnaliser le contenu et les paramètres de vos messages, dans vos campagnes et parcours.</p>
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
<p>Date de disponibilité : 13 août</p>
<p>Si vous envoyez des e-mails sur une toute nouvelle adresse IP, vous pouvez désormais facilement exécuter des workflows de préchauffage d’adresses IP directement à partir de l’interface d’utilisation. Adobe Journey Optimizer offre un moyen standardisé et efficace de préchauffer vos adresses IP en respectant les bonnes pratiques de délivrabilité optimale.</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/ip-warmup-gs.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


### Améliorations {#e-improvements}

Cette version apporte les améliorations répertoriées ci-dessous.

**Parcours**

* Dans l’activité **Condition**, par défaut, la condition Heure est désormais définie par heure, de 00:00 à 12:00. [En savoir plus](../building-journeys/condition-activity.md#time_condition)
* Lors de la création de vos parcours, les alertes s’affichent désormais dans une liste déroulante, afin de s’aligner sur les alertes de campagne et d’offrir une expérience utilisateur cohérente. [En savoir plus](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Les options de zoom de la barre d’outils de parcours ont été améliorées : le pourcentage de zoom est désormais visible et vous pouvez désormais facilement réinitialiser la valeur de zoom sur 100 %.

**Audiences**

* L’utilisation d’audiences issues d’un téléchargement personnalisé (fichier CSV) est désormais disponible avec le module complémentaire de protection des données et de protection.
* Lors du ciblage d’une audience de téléchargement personnalisée (fichier CSV), vous pouvez désormais utiliser les attributs du fichier dans vos campagnes et parcours. Ces attributs sont disponibles dans l’éditeur de personnalisation, pour personnaliser vos messages et dans l’éditeur d’expression avancé de parcours.

## Notes de mise à jour de juillet 2024 {#24-7-2024}

**Date de version** : 30-31 juillet 2024

### Nouvelles fonctionnalités {#27-4-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.

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
<th><strong>Composition d’audiences fédérées (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La composition d’audiences fédérées est désormais disponible dans Adobe Journey Optimizer. Elle permet aux entreprises de composer des données pour améliorer leur emploi dans divers cas d’utilisation. Grâce à cette nouvelle approche, en tant qu’utilisateur ou utilisatrice d’Adobe Real-Time Customer Data Platform et/ou d’Adobe Journey Optimizer, vous pouvez fédérer les jeux de données directement à partir de votre entrepôt de données existant pour créer et enrichir les audiences et les attributs Adobe Experience Platform dans un seul système.</p>
<p>Pour plus d’informations, consultez la <a href="https://experienceleague.adobe.com/fr/docs/federated-audience-composition/using/home"  target="_blank">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#27-4-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Parcours**

* (Date de disponibilité : 8 juillet) **Éditeur d’expression avancé dans la configuration des événements des parcours** : vous pouvez désormais utiliser l’éditeur d’expression avancé lors de la configuration d’un événement, ce qui vous permet de définir des expressions plus complexes ou d’utiliser des fonctions dans la condition d’identifiant d’événement. [En savoir plus](../event/about-creating.md#adv-exp-editor)

