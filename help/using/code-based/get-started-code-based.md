---
title: Prise en main des expériences basées sur le code
description: En savoir plus sur les expériences basées sur le code dans Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: b8a71c43ad5b456bfc9ec9b9d3fba06049e604ed
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 100%

---

# Commencer avec le canal basé sur le code {#get-sarted-code-based}

[!DNL Journey Optimizer] vous permet de personnaliser et de tester les expériences que vous souhaitez diffuser à votre clientèle sur tous vos touchpoints : applications web, applications mobiles, applications de bureau, consoles vidéo, appareils connectés à la télévision, téléviseurs intelligents, kiosques, guichets automatiques, assistants vocaux, appareils IdO, etc.

Avec la fonctionnalité d’**expérience basée sur le code**, vous pouvez définir des expériences entrantes à l’aide d’un éditeur non visuel simple et intuitif. Cela vous permet d’insérer et de modifier des éléments spécifiques à des emplacements individuels et plus granulaires de vos applications ou pages web, quel que soit le type d’applications dont vous disposez, plutôt que d’appliquer des modifications à l’ensemble d’un contenu.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>Des mécanismes de sécurisation et recommandations spécifiques pour les expériences basées sur le code sont détaillés dans [cette page](code-based-prerequisites.md).


<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="Lead" src="../assets/do-not-localize/privacy-audit.jpeg">
</a>
<div><a href="#how-it-works"><strong>Fonctionnement</strong>
</div>
<p>
</td>
<td>
<a href="code-based-prerequisites.md">
<img alt="Validation" src="../assets/do-not-localize/web-prerequisites.jpg">
</a>
<div>
<a href="code-based-prerequisites.md"><strong>Mécanismes de sécurisation et conditions préalables</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="Peu fréquent" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>Créer une expérience basée sur le code</strong></a>
</div>
<p></td>
<td>
<a href="code-based-implementation-samples.md">
<img alt="Validation" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>Exemples de mises en œuvre</strong></a>
</div>
<p>
</td>
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

## Quand utiliser un canal basé sur le code ou d’autres canaux {#code-based-vs-other-channels}

### Canaux basés sur le code et autres canaux

Quand utiliser le canal basé sur le code plutôt que d’autres canaux [!DNL Journey Optimizer] ?

* Vous pouvez envisager d’utiliser des expériences basées sur du code lorsque votre propriété numérique n’est pas accessible par le biais d’un navigateur web ou d’une application mobile, dans des cas où vous pouvez probablement mieux utiliser le [canal web](../web/get-started-web.md){target="_blank"} [!DNL Journey Optimizer] ou le canal de ](../in-app/get-started-in-app.md){target="_blank"}messagerie in-app[ [!DNL Journey Optimizer].

* Vous pouvez utiliser le canal basé sur le code comme alternative au canal web [!DNL Journey Optimizer] si votre site web ne peut pas être chargé dans l’éditeur visuel du [concepteur web](../web/edit-web-content.md#work-with-web-designer){target="_blank"} ou si vous ne pouvez pas utiliser l’[extension du navigateur](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} qui alimente la création visuelle pour le canal web.

* Vous pouvez également utiliser le canal basé sur le code comme alternative aux canaux web ou in-app [!DNL Journey Optimizer] si vous disposez d’une mise en œuvre basée sur une API, découplée ou côté serveur.

### Canal basé sur le code ou canal web

Pour exécuter des cas d’utilisation web, vous pouvez utiliser le canal web ou l’expérience basée sur du code, mais selon votre contexte, l’un peut être plus approprié que l’autre. Les principales différences sont répertoriées ci-dessous afin que vous puissiez prendre une décision éclairée sur ce qu’il convient d’utiliser.

**Web**

* Modifiez votre contenu à l’aide de l’éditeur visuel du [concepteur web](../web/edit-web-content.md#work-with-web-designer){target="_blank"}.
* Vous avez besoin de la mise en œuvre du [SDK web Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} et que l’extension [Visual Editing Helper d’Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} soit installée sur votre navigateur web. [En savoir plus](../web/web-prerequisites.md){target="_blank"}
* Le canal web vous permet de tout modifier sur votre page et dispose d’une liste prédéfinie des actions que vous pouvez utiliser pour apporter des modifications. [En savoir plus](../web/edit-web-content.md#work-with-web-designer){target="_blank"}
* Il est facile à configurer et à optimiser.
* Cette fonctionnalité est axée sur le persona-spécialiste du marketing.

**Expérience basée sur le code**

* Modifiez votre contenu à l’aide de l’[éditeur de personnalisation](create-code-based.md#edit-code).
* L’expérience basée sur le code nécessite un travail de développement en aval de votre implémentation pour que vos applications puissent interpréter et diffuser le contenu publié sur Edge par [!DNL Journey Optimizer] pour ces emplacements. [En savoir plus](code-based-configuration.md#surface-definition)
* Cela nécessite davantage de planification et ne peut modifier que les éléments spécifiés par les développeurs et développeuses. Il est donc essentiel d’identifier les composants (bannière d’accueil, image principale, barre de menus, etc.) sur les applications qui doivent être modifiées pour la personnalisation ou le test, et de collaborer avec votre équipe de développement pour créer l’implémentation nécessaire pour gérer ces modifications.
* Cela vous permet d’utiliser du contenu de code JSON.
* Cette fonctionnalité est axée sur le persona-développeur.

## Fonctionnement {#how-it-works}

>[!CAUTION]
>
>Cette fonctionnalité est destinée aux développeurs et développeuses et/ou aux personnes expérimentées. Elle peut être utilisée par les spécialistes du marketing qui possèdent certaines compétences en écriture de code, à condition que les mises en œuvre en surface et la configuration initiale soient gérées par votre équipe de développement.

Pour modifier votre contenu à l’aide de la fonctionnalité d’expérience basée sur le code [!DNL Journey Optimizer], vos pages ou applications doivent être instrumentées. Pour ce faire, vous devez déclarer à l’avance les emplacements spécifiques (appelés « [surfaces](code-based-configuration.md#surface-definition) ») où vous souhaitez insérer ou remplacer du contenu<!--HOW??-->.

>[!NOTE]
>
>Actuellement, le contenu associé à une configuration ne peut être que de type HTML ou JSON. <!--WILL COME LATER: text, image or another format depending on the application-->

Les étapes clés de mise en œuvre d’une campagne basée sur le code sont les suivantes.

1. Définissez une [surface](code-based-configuration.md#surface-definition) dans l’implémentation de votre application, qui est essentiellement l’emplacement où vous souhaitez ajouter votre expérience basée sur le code, puis créez une configuration de canal d’expérience basée sur le code qui référence cet emplacement, et créez une campagne dans [!DNL Journey Optimizer] à l’aide de cette configuration. [Voici comment procéder](create-code-based.md#create-code-based-campaign)

1. Composez une expérience en spécifiant du contenu pour la configuration sélectionnée à l’aide de l’éditeur de personnalisation [!DNL Journey Optimizer]. [Voici comment procéder.](create-code-based.md#edit-code)

1. Votre équipe de mise en œuvre d’application effectue des appels d’API ou de SDK explicites pour récupérer du contenu pour les surfaces nommées, « Texte de bannière » ou « Barre d’état de recommendations 1 », ou des points de décision non liés à l’interface utilisateur dans une application, comme « paramètres d’algorithme de recherche ». Dans ce cas, l’équipe de mise en œuvre est chargée du rendu, de l’interprétation et de l’action sur le contenu renvoyé.<!--TBC with Robert - should link to a new section with API/SDK call samples-->
