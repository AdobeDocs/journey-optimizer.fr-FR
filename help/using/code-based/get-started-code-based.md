---
title: Prise en main des expériences basées sur le code
description: En savoir plus sur les expériences basées sur le code dans Journey Optimizer
feature: Code-based Experiences
topic: Content Management
role: User, Developer, Admin
level: Experienced
exl-id: 987de2bf-cebe-4753-98b4-01eb3fded492
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 100%

---

# Commencer avec le canal basé sur le code {#get-sarted-code-based}

[!DNL Journey Optimizer] vous permet de personnaliser et de tester les expériences que vous souhaitez diffuser à votre clientèle sur tous vos touchpoints : applications web, applications mobiles, applications de bureau, consoles vidéo, appareils connectés à la télévision, téléviseurs intelligents, kiosques, guichets automatiques, assistants vocaux, appareils IdO, etc.

Avec la fonctionnalité d’**expérience basée sur le code**, vous pouvez définir des expériences entrantes à l’aide d’un éditeur non visuel simple et intuitif. Cela vous permet d’insérer et de modifier des éléments spécifiques à des emplacements individuels et plus granulaires de vos applications ou pages web, quel que soit le type d’applications dont vous disposez, plutôt que d’appliquer des modifications à l’ensemble d’un contenu.

<!--[!DNL Journey Optimizer] allows you to compose and deliver content on any inbound surface in a developer-focused workflow. You can leverage all the personalization capabilities, and preview what will be published. The content can be static (images, text, JSON, HTML) or dynamic (offers, decisions, recommendations). You can also insert custom content actions in your omni-channel journeys.-->

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
* L’expérience basée sur le code nécessite un travail de développement en aval de votre implémentation pour s’assurer que vos surfaces peuvent interpréter et diffuser le contenu publié sur Edge par [!DNL Journey Optimizer] pour ces surfaces. [En savoir plus](#surface-definition)
* Cela nécessite davantage de planification et ne peut modifier que les éléments spécifiés par les développeurs et développeuses. Il est donc essentiel d’identifier les composants (bannière d’accueil, image principale, barre de menus, etc.) sur les surfaces qui doivent être modifiées pour la personnalisation ou le test, et collaborez avec votre équipe de développement pour créer l’implémentation nécessaire pour gérer ces modifications.
* Cela vous permet d’utiliser du contenu de code JSON.
* Cette fonctionnalité est axée sur le persona-développeur.

## Fonctionnement {#how-it-works}

>[!CAUTION]
>
>Cette fonctionnalité est destinée aux développeurs et développeuses et/ou aux personnes expérimentées. Elle peut être utilisée par les spécialistes du marketing qui possèdent certaines compétences en écriture de code, à condition que les mises en œuvre en surface et la configuration initiale soient gérées par votre équipe de développement.

Pour modifier votre contenu à l’aide de la fonctionnalité d’expérience basée sur le code [!DNL Journey Optimizer], vos pages ou applications doivent être instrumentées. Pour ce faire, vous devez déclarer à l’avance les emplacements spécifiques (appelés « [surfaces](#surface-definition) ») où vous souhaitez insérer ou remplacer du contenu<!--HOW??-->.

>[!NOTE]
>
>Actuellement, le contenu associé à une surface ne peut être que de type HTML ou JSON. <!--WILL COME LATER: text, image or another format depending on the application-->

Les étapes clés de mise en œuvre d’une campagne basée sur le code sont les suivantes.

1. Définissez une [surface](#surface-definition), qui est essentiellement l’emplacement où vous souhaitez ajouter votre expérience basée sur le code, et créez une campagne dans [!DNL Journey Optimizer] en utilisant cette surface. [Voici comment procéder.](create-code-based.md#create-code-based-campaign)

1. Composez une expérience en spécifiant du contenu pour la surface sélectionnée à l’aide de l’éditeur de personnalisation [!DNL Journey Optimizer]. [Voici comment procéder.](create-code-based.md#edit-code)

1. Votre équipe de mise en œuvre d’application effectue des appels d’API ou de SDK explicites pour récupérer du contenu pour les surfaces nommées, « Texte de bannière » ou « Barre d’état de recommendations 1 », ou des points de décision non liés à l’interface utilisateur dans une application, comme « paramètres d’algorithme de recherche ». Dans ce cas, l’équipe de mise en œuvre est chargée du rendu, de l’interprétation et de l’action sur le contenu renvoyé.<!--TBC with Robert - should link to a new section with API/SDK call samples-->

## Qu’est-ce qu’une surface ? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Définition d’une surface d’expérience basée sur le code"
>abstract="Une surface basée sur le code est toute entité conçue pour l’interaction de la personne utilisatrice ou du système, qui est identifiée de manière unique par un URI."

Une **surface d’expérience basée sur le code** est toute entité conçue pour l’interaction de la personne utilisatrice ou du système<!--ask Robert to explain further-->, qui est identifiée de manière unique par un **URI**.

Autrement dit, une surface peut être considérée comme un conteneur à n’importe quel niveau de hiérarchie ayant une entité (touchpoint) qui existe.<!--good idea to illustrate how it can be seen, but to clarify-->

* Il peut s’agir d’une page web, d’une application mobile, d’une appli de bureau, d’un emplacement de contenu spécifique au sein d’une entité plus grande (par exemple, une `div`) ou d’un modèle d’affichage non standard (par exemple, un kiosque ou une bannière d’application de bureau).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Elle peut également s’étendre à des éléments spécifiques de conteneurs de contenu à des fins de non-affichage ou d’affichage abstrait (par exemple, des objets blob JSON fournis à des services).

* Il peut également s’agir d’une surface de caractères génériques qui correspond à diverses définitions de surface client (par exemple, un emplacement d’image principale sur chaque page de votre site web peut se traduire en un URI de surface comme : web://mondomaine.com/*#image_principale).

Fondamentalement, un URI de surface est composé de plusieurs sections :
1. **Type** : web, application mobile, ATM, kiosque, tvcd, service, etc.
1. **Propriété** : URL de page ou bundle d’applications.
1. **Conteneur** : emplacement sur l’activité page/application.

Les tableaux ci-dessous répertorient quelques exemples de définition d’URI de surface pour divers appareils.

**Web et mobile**

| Type | URI | Description |
| --------- | ----------- | ------- | 
| Web | `web://domain.com/path/page.html#element` | Représente un élément individuel dans une page spécifique d’un domaine spécifique, où un élément peut être un libellé comme dans les exemples suivants : hero_banner, top_nav, menu, pied de page, etc. |
| Application iOS | `mobileapp://com.vendor.bundle/activity#element` | Représente un élément spécifique dans une activité application native, tel qu’un bouton ou un autre élément de vue. |
| Application Android | `mobileapp://com.vendor.bundle/#element` | Représente un élément spécifique dans une application native. |

**Autres types d’appareils**

| Type | URI | Description |
| --------- | ----------- | ------- | 
| Bureau | `desktop://com.vendor.bundle/#element` | Représente un élément spécifique dans une application, tel qu’un bouton, un menu, une bannière principale, etc. |
| Application TV | `tvcd://com.vendor.bundle/#element` | Représente un élément spécifique dans un identifiant de bundle spécifique à l’application d’un appareil connecté à la télévision ou à la télévision intelligente. |
| Service | `service://servicename/#element` | Représente un processus côté serveur ou une autre entité manuelle. |
| Kiosque | `kiosk://location/screen#element` | Exemple de types de surfaces supplémentaires potentiels pouvant être ajoutés facilement. |
| ATM | `atm://location/screen#element` | Exemple de types de surfaces supplémentaires potentiels pouvant être ajoutés facilement. |

**Surfaces de caractères génériques**

| Type | URI | Description |
| --------- | ----------- | ------- | 
| Caractère générique web | `wildcard:web://domain.com/*#element` | Surface de caractères génériques : représente un élément individuel dans chacune des pages sous un domaine spécifique. |
| Caractère générique web | `wildcard:web://*domain.com/*#element` | Surface de caractères génériques : représente un élément individuel dans chacune des pages sous tous les domaines se terminant par « domain.com ». |
