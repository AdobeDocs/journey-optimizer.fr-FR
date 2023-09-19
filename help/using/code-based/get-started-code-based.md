---
title: Prise en main des expériences basées sur le code
description: En savoir plus sur les expériences basées sur le code dans Journey Optimizer
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Version Beta"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 7%

---

# Prise en main du canal basé sur le code {#get-sarted-code-based}

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* **[Prise en main du canal basé sur le code](get-started-code-based.md)**
* [Conditions préalables basées sur le code](code-based-prerequisites.md)
* [Exemples de mise en oeuvre basés sur le code](code-based-implementation-samples.md)
* [Création d’expériences basées sur du code](create-code-based.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Le canal d’expérience basé sur le code est actuellement disponible en version bêta pour sélectionner uniquement les utilisateurs. Pour rejoindre le programme Beta, contactez l’assistance clientèle d’Adobe.

[!DNL Journey Optimizer] vous permet de personnaliser et de tester les expériences que vous souhaitez diffuser à vos clients sur tous vos points de contact : applications web, applications mobiles, applications de bureau, consoles vidéo, appareils connectés à la télévision, téléviseurs intelligents, kiosques, guichets automatiques, assistants vocaux, appareils IoT, etc.

Avec la variable **expérience basée sur le code** , vous pouvez définir des expériences entrantes à l’aide d’un éditeur non visuel simple et intuitif. Il vous permet d’insérer et de modifier des éléments spécifiques à des emplacements individuels et plus granulaires de vos applications ou pages web, quel que soit le type d’applications dont vous disposez, plutôt que d’appliquer des modifications à l’ensemble d’un contenu.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

Lorsque vous [création d’une campagne](../campaigns/create-campaign.md#configure), sélectionnez **Expérience basée sur le code (bêta)** comme action et définissez les paramètres de base.

>[!NOTE]
>
>Si c’est la première fois que vous créez une expérience web, veillez à respecter les conditions préalables décrites dans [cette section](code-based-prerequisites.md).

<!--Discover the detailed steps to create a code-based campaign in this video.-->

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="#how-it-works">
<img alt="Prospect" src="../assets/do-not-localize/privacy-audit.jpeg">
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
<a href="code-based-prerequisites.md"><strong>Conditions préalables</strong></a>
</div>
<p>
</td>
<td>
<a href="create-code-based.md#create-code-based-campaign">
<img alt="Peu fréquent" src="../assets/do-not-localize/web-create.jpg">
</a>
<div>
<a href="create-code-based.md#create-code-based-campaign"><strong>Création d’une expérience basée sur du code</strong></a>
</div>
<p></td>
<td>
<a href="create-code-based.md#edit-code">
<img alt="Validation" src="../assets/do-not-localize/web-design.jpg">
</a>
<div>
<a href="create-code-based.md#edit-code"><strong>Modifier votre code</strong></a>
</div>
<p>
</td>
</tr></table>



<!--[Learn how to create a code-based campaign in this video](#video)-->

## Quand utiliser un canal basé sur le code ou d’autres canaux {#code-based-vs-other-channels}

### Canaux basés sur le code et autres

Quand utiliser le canal basé sur le code plutôt que l’autre [!DNL Journey Optimizer] canaux ?

* Vous pouvez envisager d’utiliser des expériences basées sur du code à tout moment lorsque votre propriété numérique n’est pas accessible par le biais d’un navigateur web ou d’une application mobile, dans des cas où vous pouvez probablement mieux utiliser la variable [!DNL Journey Optimizer] [canal web](../web/get-started-web.md){target="_blank"} or the [!DNL Journey Optimizer] [in-app messaging](../in-app/get-started-in-app.md){target="_blank"} canal.

* Vous pouvez utiliser le canal basé sur le code comme alternative au [!DNL Journey Optimizer] canal web si votre site web ne peut pas être chargé dans [éditeur visuel web](../web/author-web.md){target="_blank"} or if you cannot use the [browser extension](../web/web-prerequisites.md#visual-authoring-prerequisites){target="_blank"} qui alimente la création visuelle pour le canal web.

* Vous pouvez également utiliser le canal basé sur le code comme alternative au [!DNL Journey Optimizer] canaux web ou in-app si vous disposez d’une mise en oeuvre basée sur une API, sans interface ou côté serveur.

### Canal web ou basé sur le code

Pour exécuter des cas d’utilisation web, vous pouvez utiliser le canal web ou l’expérience basée sur du code, mais selon votre contexte, l’expérience serait plus appropriée que l’autre. Les principales différences sont répertoriées ci-dessous afin que vous puissiez prendre une décision éclairée sur ce qu’il convient d’utiliser.

**Web**
* Modifiez votre contenu à l’aide du [éditeur visuel](../web/author-web.md){target="_blank"}.
* Vous avez besoin de [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} implementation and the [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} extension installed on your web browser. [Learn more](../web/web-prerequisites.md){target="_blank"}
* Le canal web vous permet de tout modifier sur votre page et dispose d’une liste prédéfinie des actions que vous pouvez utiliser pour apporter des modifications. [En savoir plus](../web/author-web.md){target="_blank"}
* C&#39;est facile à configurer et à accélérer.
* Il est axé sur le marketeur-persona.

**Expérience basée sur le code**
* Modifiez votre contenu à l’aide du [éditeur de code](create-code-based.md#edit-code).
* L’expérience basée sur le code nécessite un travail de développement précédent sur votre implémentation pour s’assurer que vos surfaces peuvent interpréter et diffuser le contenu publié sur le serveur Edge par [!DNL Journey Optimizer] pour ces surfaces. [En savoir plus](#surface-definition)
* Il nécessite davantage de planification et ne peut modifier que les éléments spécifiés par les développeurs. Il est donc essentiel d’identifier les composants (bannière d’accueil, image principale, barre de menus, etc.) sur les surfaces qui doivent être modifiées pour la personnalisation ou le test, et collaborez avec votre équipe de développement pour créer l’implémentation nécessaire pour gérer ces modifications.
* Il vous permet d’utiliser du contenu de code JSON.
* Il est axé sur le développeur et le personnage.

## Fonctionnement {#how-it-works}

>[!CAUTION]
>
>Cette fonctionnalité est destinée aux développeurs et/ou aux utilisateurs expérimentés. Il peut être utilisé par les marketeurs qui possèdent certaines compétences en écriture de code, à condition que les mises en oeuvre en surface et la configuration initiale soient gérées par votre équipe de développement.

Pour modifier votre contenu à l’aide du [!DNL Journey Optimizer] fonction d’expérience basée sur le code, vos pages ou applications doivent être instrumentées. Pour ce faire, vous devez déclarer à l’avance les emplacements spécifiques (appelés &quot;[surfaces](#surface-definition)&quot;) où vous souhaitez insérer ou remplacer du contenu<!--HOW??-->.

>[!NOTE]
>
>Actuellement, le contenu associé à une surface ne peut être que HTML ou JSON. <!--WILL COME LATER: text, image or another format depending on the application-->

Les étapes clés de mise en oeuvre d’une campagne basée sur du code sont les suivantes.

1. Définition d’une [surface](#surface-definition), qui est essentiellement l’emplacement où vous souhaitez ajouter votre expérience basée sur le code, et créer une campagne dans [!DNL Journey Optimizer] en utilisant cette surface. [Voici comment procéder.](create-code-based.md#create-code-based-campaign)

1. Composition d’une expérience en spécifiant du contenu pour la surface sélectionnée à l’aide de la propriété [!DNL Journey Optimizer] éditeur de code. [Voici comment procéder.](create-code-based.md#edit-code)

1. Votre équipe de mise en oeuvre d’application effectue des appels d’API ou de SDK explicites pour récupérer du contenu pour les surfaces nommées, comme &quot;Texte de bannière&quot; ou &quot;Bac Recommendations 1&quot;, ou des points de décision non liés à l’interface utilisateur dans une application, comme &quot;paramètres d’algorithme de recherche&quot;. Dans ce cas, l’équipe de mise en oeuvre est chargée du rendu ou de l’interprétation ou de l’action sur le contenu renvoyé.<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## Qu&#39;est-ce qu&#39;une surface ? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Définition d’une surface d’expérience basée sur du code"
>abstract="Une surface basée sur du code est toute entité conçue pour l’interaction de l’utilisateur ou du système, qui est identifiée de manière unique par un URI."

A **surface d’expérience basée sur le code** est toute entité conçue pour l’interaction utilisateur ou système<!--ask Robert to explain further-->, qui est identifié de manière unique par un **URI**.

En d’autres termes, une surface peut être vue comme un conteneur à n’importe quel niveau de hiérarchie avec une entité (point de contact) qui existe.<!--good idea to illustrate how it can be seen, but to clarify-->

* Il peut s’agir d’une page web, d’une application mobile, d’une appli de bureau, d’un emplacement de contenu spécifique au sein d’une entité plus grande (par exemple, une `div`) ou un modèle d’affichage non standard (par exemple, un kiosque ou une bannière d’application de bureau).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Il peut également s’étendre à des éléments spécifiques de conteneurs de contenu à des fins de non-affichage ou d’affichage abstrait (par exemple, des objets blob JSON fournis à des services).

* Il peut également s’agir d’une surface de caractères génériques qui correspond à diverses définitions de surface client (par exemple, un emplacement d’image principale sur chaque page de votre site web peut se traduire dans un URI de surface comme : web://mydomain.com/*#hero_image).

Fondamentalement, un URI de surface est composé de plusieurs sections :
1. **Type**: web, application mobile, service, kiosque, tvcd, etc.
1. **Propriété**: domaine ou lot d’applications
1. **Chemin**: activité page/application + emplacement sur l’activité page/application <!--to clarify-->

Le tableau ci-dessous répertorie quelques exemples de définition d’URI de surface pour divers appareils.

| Type | URI | Description |
| --------- | ----------- | ------- |   
| Web | web://domain.com/path/page.html | Représente un chemin et une page individuels d’un site web. |
| Web | web://domain.com/path/page.html#element | Représente un élément individuel dans une page spécifique d’un domaine spécifique. |
| Web | web://domain.com/*#element | Surface de caractères génériques : représente un élément individuel dans chacune des pages sous un domaine spécifique. |
| Bureau | desktop://com.vendor.bundle | Représente une application de bureau spécifique. |
| Bureau | desktop://com.vendor.bundle#element | Représente un élément spécifique dans une application, tel qu’un bouton, un menu, une bannière principale, etc. |
| Application iOS | ios://com.vendor.bundle | Représente une application mobile spécifique pour une seule plateforme, dans ce cas l’application iOS. |
| Application iOS | ios://com.vendor.bundle/activity | Représente une activité spécifique (vue) dans une application mobile. |
| Application iOS | ios://com.vendor.bundle/activity#element | Représente un élément spécifique dans une activité, tel qu’un bouton ou un autre élément de vue. |
| Application Android | android://com.vendor.bundle | Représente une application mobile spécifique pour une seule plateforme, dans ce cas une application Android. |
| application tvOS | tvos://com.vendor.bundle | Représente une application tvOS spécifique. |
| application TV | tvcd://com.vendor.bundle | Représente un identifiant de lot spécifique à l’application d’appareil connectée à la télévision ou à la télévision. |
| Service | service://servicename | Représente un processus côté serveur ou une autre entité manuelle. |
| Kiosque | kiosk://location/screen | Exemple de types de surface supplémentaires potentiels pouvant être ajoutés facilement. |
| ATM | atm://location/screen | Exemple de types de surface supplémentaires potentiels pouvant être ajoutés facilement. |