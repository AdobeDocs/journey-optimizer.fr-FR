---
title: Prise en main des expériences basées sur le code
description: En savoir plus sur les expériences basées sur le code dans Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: ht
source-wordcount: '789'
ht-degree: 100%

---

# Commencer avec le canal basé sur le code {#get-sarted-code-based}

[!DNL Journey Optimizer] vous permet de personnaliser et de tester les expériences que vous souhaitez diffuser à votre clientèle sur tous vos touchpoints : applications web, applications mobiles, applications de bureau, consoles vidéo, appareils connectés à la télévision, téléviseurs intelligents, kiosques, guichets automatiques, assistants vocaux, appareils IdO, etc.

Avec la fonctionnalité d’**expérience basée sur le code**, vous pouvez définir des expériences entrantes à l’aide d’un éditeur non visuel simple et intuitif. Cela vous permet d’insérer et de modifier des éléments spécifiques à des emplacements individuels et plus granulaires de vos applications ou pages web, quel que soit le type d’applications dont vous disposez, plutôt que d’appliquer des modifications à l’ensemble d’un contenu.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound device in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

>[!IMPORTANT]
>
>Des recommandations spécifiques pour les expériences basées sur du code sont présentées dans [cette page](code-based-prerequisites.md).


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
<a href="code-based-configuration.md">
<img alt="Validation" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="code-based-implementation-samples.md"><strong>Configuration du canal basé sur du code</strong></a>
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
</tr></table>

<!--[Learn how to create a code-based campaign in this video](#video)-->

➡️ Un cas d’utilisation de bout en bout montrant comment utiliser les expériences de contenu pour comparer les décisions avec le canal d’expérience basé sur le code est présenté dans [cette section](../experience-decisioning/experience-decisioning-uc.md).

## Quand utiliser un canal basé sur le code ou d’autres canaux {#code-based-vs-other-channels}

### Canaux basés sur le code et autres canaux

Quand utiliser le canal basé sur le code plutôt que d’autres canaux [!DNL Journey Optimizer] ?

* Vous pouvez envisager d’utiliser des expériences basées sur du code lorsque votre propriété numérique n’est pas accessible par le biais d’un navigateur web ou d’une application mobile, dans des cas où vous pouvez probablement mieux utiliser le [canal web](../web/get-started-web.md){target="_blank"} [!DNL Journey Optimizer] ou le canal de ](../in-app/get-started-in-app.md){target="_blank"}messagerie in-app[ [!DNL Journey Optimizer].

<!--* You can use the code-based channel as an alternative to the [!DNL Journey Optimizer] web channel if your website cannot be loaded into the [web designer](../web/web-visual-editor.md){target="_blank"} visual editor or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} that powers visual authoring for web channel.-->

* Vous pouvez également utiliser le canal basé sur du code comme alternative aux canaux web ou in-app [!DNL Journey Optimizer] si vous disposez d’une implémentation basée sur une API, découplée ou côté serveur.

* Vous pouvez également utiliser le canal basé sur du code sur les applications mobiles natives en tant qu’alternative au canal in-app si vous souhaitez modifier du contenu dans votre application native au lieu d’afficher des fenêtres modales, contextuelles ou superposées.

### Canal basé sur le code ou canal web {#code-based-vs-web}

Pour exécuter des cas d’utilisation web, vous pouvez utiliser le canal web ou l’expérience basée sur du code, mais selon votre contexte, l’un peut être plus approprié que l’autre. Les principales différences sont répertoriées ci-dessous afin que vous puissiez prendre une décision éclairée sur ce qu’il convient d’utiliser et à quel moment.

**Web**

* Modifiez votre contenu à l’aide de l’éditeur visuel du [concepteur web](../web/web-visual-editor.md){target="_blank"} ou de l’[éditeur non visuel](../web/web-non-visual-editor.md) web.
* Vous avez besoin du [SDK web Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"}, qui est une implémentation côté client.
  <!--* You need the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}-->
* Le canal web vous permet de tout modifier sur votre page et dispose d’une liste prédéfinie des actions que vous pouvez utiliser pour apporter des modifications. [En savoir plus](../web/web-visual-editor.md){target="_blank"}
* Il est facile à configurer et à optimiser.
* Cette fonctionnalité est axée sur le persona-spécialiste du marketing.

**Expérience basée sur le code**

* Modifiez votre contenu à l’aide de l’[éditeur de personnalisation](create-code-based.md#edit-code).
* Vous avez besoin du [SDK web Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"}, qui est une implémentation côté client, ou de l’[API serveur AEP Edge Network](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"}, qui est une implémentation côté serveur.
* L’expérience basée sur le code nécessite un travail de développement en aval de votre implémentation pour que vos applications puissent interpréter et diffuser le contenu publié sur Edge par [!DNL Journey Optimizer] pour ces emplacements. [En savoir plus](code-based-surface.md)
* Cela nécessite davantage de planification et ne peut modifier que les éléments spécifiés par les développeurs et développeuses. Par conséquent, il est essentiel d’identifier les composants (bannière d’accueil, image principale, barre de menus, etc.) sur les applications qui doivent être modifiées pour la personnalisation ou le test, et de collaborer avec votre équipe de développement pour créer l’implémentation nécessaire pour gérer ces modifications.
* Cela vous permet d’utiliser du contenu de code JSON.
* Cette fonctionnalité est axée sur le persona-développeur.

## Fonctionnement {#how-it-works}

>[!CAUTION]
>
>Cette fonctionnalité est destinée aux développeurs et développeuses et/ou aux personnes expérimentées. Elle peut être utilisée par les spécialistes marketing qui possèdent certaines compétences en écriture de code, à condition que les configurations de canaux et la configuration initiale soient gérées par votre équipe de développement.

Pour modifier votre contenu à l’aide de la fonctionnalité d’expérience basée sur le code [!DNL Journey Optimizer], vos pages ou applications doivent être instrumentées. Pour ce faire, vous devez déclarer à l’avance les emplacements individuels spécifiques (appelés « [surfaces](code-based-surface.md) ») où vous souhaitez insérer ou remplacer du contenu.

>[!NOTE]
>
>Actuellement, le contenu associé à une configuration ne peut être que de type HTML ou JSON.

Les étapes clés pour créer et diffuser une expérience basée sur du code sont les suivantes.

1. Assurez-vous de respecter les conditions préalables spécifiques au canal. [En savoir plus](code-based-prerequisites.md)

1. Définissez une [surface](code-based-surface.md#surface-definition) dans l’implémentation de votre application, qui correspond essentiellement à l’emplacement où vous souhaitez ajouter votre expérience.

1. Créez une configuration de canal basée sur du code qui référence cet emplacement. [Voici comment procéder](code-based-configuration.md#create-code-based-configuration)

1. Créez un parcours ou une campagne dans [!DNL Journey Optimizer] à l’aide de cette configuration. [Voici comment procéder](create-code-based.md#create-code-based-campaign)

1. Composez une expérience en spécifiant du contenu pour la configuration sélectionnée à l’aide de l’éditeur de personnalisation [!DNL Journey Optimizer]. [Voici comment procéder](create-code-based.md#edit-code)

1. Testez votre expérience basée sur du code. [Voici comment procéder](test-code-based.md)

1. Publiez-la. [Voici comment procéder](publish-code-based.md)

1. Une fois que vous avez activé votre parcours ou votre campagne d’expérience basée sur du code, l’implémentation de l’application ou de la page qui demande le contenu pour la surface doit être en place pour que le contenu soit récupéré et affiché.

   >[!INFO]
   >
   >Pour s’assurer que cela soit effectué, votre équipe d’implémentation d’application effectue des appels API ou de SDK explicites pour récupérer du contenu pour la surface définie dans la configuration basée sur du code, telle que « Texte de bannière » ou « Barre de recommandations 1 », ou des points de décision non liés à l’interface d’utilisation dans une application, tels que « paramètres d’algorithme de recherche ». <!--In this case, the implementation team is responsible for rendering or otherwise interpreting and acting on the returned content.--> [En savoir plus](code-based-implementation-samples.md)

