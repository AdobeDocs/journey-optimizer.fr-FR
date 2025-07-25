---
solution: Journey Optimizer
product: journey optimizer
title: Basculer vers le mode sombre
description: Découvrez comment utiliser le mode sombre dans le Designer d’e-mail
badge: label="Beta" type="Informative"
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: mode sombre, e-mail, couleur, éditeur
hide: true
hidefromtoc: true
exl-id: 27442cb0-5027-4d9c-9d3c-9ec33af7c9ff
source-git-commit: 23684c906d11c7f54eb28cac7c2697964e723a2e
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 10%

---

# Gérer le contenu en mode sombre {#dark-mode}

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode"
>title="Basculer vers le mode sombre"
>abstract="Basculez vers le mode sombre pour prévisualiser le rendu et définir des paramètres personnalisés spécifiques. <br>Attention : le rendu final dépend du client de messagerie de la personne destinataire. Les clients de messagerie ne prennent pas tous en charge le mode sombre personnalisé."

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode_image"
>title="Utiliser une image spécifique pour le mode sombre"
>abstract="Vous pouvez sélectionner une autre image qui s’affichera lorsque le mode sombre sera activé. <br>Attention : l’ajout d’une image spécifique pour le mode sombre ne garantit pas qu’elle s&#39;affichera correctement dans tous les clients de messagerie. Les clients de messagerie ne prennent pas tous en charge le mode sombre personnalisé."

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode_preview"
>title="Basculer vers le mode sombre"
>abstract="Basculez vers le mode sombre pour prévisualiser le rendu sur les clients de messagerie pris en charge. <br>Attention : le rendu final dépend du client de messagerie de la personne destinataire. Les clients de messagerie ne prennent pas tous en charge le mode sombre personnalisé."

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version Beta et disponible uniquement pour les clientes et clients Beta. Pour rejoindre le programme bêta, contactez votre représentant ou représentante Adobe.

Lors de la conception de vos e-mails, le [!DNL Journey Optimizer] [Email Designer](get-started-email-design.md) vous permet de passer en **[!UICONTROL mode sombre]** où vous pouvez définir des paramètres personnalisés spécifiques. Lorsque le mode sombre est activé, les clients de messagerie de prise en charge affichent les paramètres que vous avez définis pour ce mode.

>[!WARNING]
>
>Le rendu final en mode sombre dépend du client de messagerie du destinataire.
>
>Tous les clients de messagerie ne prennent pas en charge le mode sombre personnalisé. <!--[See the list](#non-supporting-email-clients)-->De plus, certains clients de messagerie n’appliquent leur propre mode sombre par défaut que pour tous les e-mails reçus. Dans ce cas, les paramètres personnalisés que vous avez définis dans le Designer Email ne peuvent pas être rendus.

Une liste des clients de messagerie prenant en charge le mode sombre est présentée dans [cette section](#supporting-email-clients).

## Qu’est-ce que le mode sombre ? {#what-is-dark-mode}

Le mode sombre permet aux clients de messagerie et aux applications pris en charge d’afficher les e-mails avec des arrière-plans plus sombres et des couleurs plus claires pour le texte, les boutons et autres éléments de l’interface utilisateur. Il permet de réduire la fatigue visuelle, d’économiser l’autonomie de la batterie et d’améliorer la lisibilité dans les environnements peu éclairés pour une expérience de visionnage plus confortable.

<!--Dark Mode uses a dark color palette with light text and UI elements to reduce eye strain, save battery life, and improve readability in low-light environments.-->

Tendance croissante dans les principaux systèmes d’exploitation et applications (Apple Mail, Gmail, Outlook, Twitter, Slack), la conception d’e-mails modernes prend désormais en compte l’importance de veiller à ce que le contenu reste lisible et visuellement attrayant pour tous les utilisateurs et utilisatrices.

Cependant, il n’est pas possible de garantir que votre e-mail se présentera exactement de la même manière en mode sombre sur tous les appareils. Certaines modifications visuelles peuvent également être provoquées par le remplacement de la conception d’origine par l’application ou l’appareil de messagerie.

En effet, la manière dont le mode sombre est appliqué par les clients de messagerie peut varier comme suit <!--between different devices and apps-->

* Tous les clients de messagerie ne prennent pas en charge cette fonctionnalité.

  >[!NOTE]
  >
  >Une liste des clients de messagerie ne prenant pas en charge le mode sombre est présentée dans [cette section](#non-supporting-email-clients).

* Certains clients de messagerie ajustent automatiquement les couleurs, les arrière-plans et les images. Dans ce cas, si vous définissez des paramètres personnalisés dans le Designer Email, ces paramètres ne seront probablement pas rendus.

* D’autres clients de messagerie offrent la possibilité de rendre le mode sombre personnalisé (par exemple avec la méthode `@media (prefers-color-scheme: dark)`). Dans ce cas, les paramètres spécifiques que vous définissez dans le Designer Email doivent être affichés. Découvrez comment définir les paramètres personnalisés du mode sombre dans le Designer d’e-mail dans [cette section](#define-custom-dark-mode).

## Mode sombre dans le Designer Email {#dark-mode-email-designer}

Lorsqu&#39;il s&#39;agit du mode sombre dans le Designer Email, deux aspects doivent être pris en compte :

* Vous pouvez obtenir un aperçu de la manière dont le mode sombre par défaut s’affichera dans la plupart des clients de messagerie de prise en charge. [En savoir plus](#preview-dark-mode)

<!--
    >[!CAUTION]
    >
    >The final rendering may vary according to the recipient's email client. To see the exact rendering for each email client, use the [Email rendering](../content-management/rendering.md) option.-->

* Si vous souhaitez remplacer les paramètres par défaut des clients de messagerie de prise en charge, vous pouvez définir des paramètres de mode sombre personnalisés s’appliquant à l’e-mail que vous modifiez. [En savoir plus](#define-custom-dark-mode)

<!--
    >[!WARNING]
    >
    >Not all email clients support custom dark mode. Some email clients only apply their own default dark mode for all emails that are received. In this case, the custom settings that you defined in the Email Designer cannot be rendered. [Learn more](#guardrails)-->

### Aperçu du mode sombre par défaut {#preview-dark-mode}

Pour accéder au mode sombre dans le Designer Email et obtenir un aperçu des paramètres par défaut du mode sombre, procédez comme suit.

1. Sur la page d&#39;accueil de Designer Email, sélectionnez l&#39;option **[!UICONTROL Créer en partant de zéro]**. [En savoir plus](content-from-scratch.md)

<!--Should work with templates and themes, NOT for LP and fragments - but TBC with eng.
    >[!NOTE]
    >
    >Currently you may not be able to switch to dark mode if you select an [email template](use-email-templates.md) or if you apply a [theme](apply-email-themes.md).-->

1. Ajoutez [structures](content-from-scratch.md) et [composants de contenu](content-components.md) à votre contenu.

1. En haut à droite de la zone de travail centrale, activez le bouton bascule en **[!UICONTROL mode sombre]**.

   ![](assets/light-mode-toggle.png)

1. L’aperçu du mode sombre par défaut s’affiche.

   ![](assets/dark-mode-default.png)

Par défaut, l’aperçu du mode sombre d’Email Designer applique le modèle de couleurs « inverser toutes les couleurs » à tous les éléments, à l’exception des images et des icônes.

Cela signifie qu’il détecte les zones comportant des éléments clairs et sombres et les inverse, de sorte que les arrière-plans clairs deviennent sombres et que le texte sombre devient clair, tandis que les arrière-plans sombres deviennent clairs et que le texte clair devient sombre.

>[!CAUTION]
>
>Le rendu final peut varier en fonction du client de messagerie du destinataire. Pour voir une simulation qui se rapproche le plus possible du résultat final pour chaque client de messagerie, utilisez l’option [ Rendu des e-mails ](../content-management/rendering.md).

<!--This is custom dark mode:

  ![](assets/dark-mode-custom.png)

Here you can see that we have applied a different background, defined another image and change the color of the text and button.-->

### Définition du mode sombre personnalisé {#define-custom-dark-mode}

Après avoir basculé en **[!UICONTROL mode sombre]**, vous pouvez choisir de modifier des éléments de style spécifiques de votre contenu qui s’afficheront uniquement lorsque le mode sombre sera activé dans le client de messagerie du destinataire, à condition qu’il prenne en charge cette fonctionnalité.

>[!WARNING]
>
>Tous les clients de messagerie ne prennent pas en charge le mode sombre. De plus, certains clients de messagerie n’appliquent leur propre mode sombre par défaut que pour tous les e-mails reçus. Dans les deux cas, les paramètres personnalisés que vous avez définis dans le Designer Email ne peuvent pas être rendus.

Pour tirer parti du style du mode sombre personnalisé Designer d’e-mail, Journey Optimizer utilise <!-- `@media (prefers-color-scheme: dark)` method--> `@media (prefers-color-scheme: dark)` requête CSS, qui détecte si le client de messagerie de l’utilisateur est en mode sombre et applique la conception avec thème sombre définie dans votre e-mail.

Pour définir les paramètres personnalisés du mode sombre, procédez comme suit.

1. Veillez à passer à l’aperçu **[!UICONTROL Mode sombre]** dans le Designer d’e-mail. [Voici comment procéder](#preview-dark-mode)

1. Modifiez les attributs de couleur de style, tels que le texte, les arrière-plans, le bouton, etc.

1. Vous ne pouvez pas modifier les couleurs des images et des icônes, mais vous pouvez définir des ressources spécifiques pour le mode sombre uniquement. Pour ce faire, sélectionnez une image. Passez en **[!UICONTROL mode sombre]** à l’aide du bouton dédié dans le volet **[!UICONTROL Paramètres]** et sélectionnez une autre ressource.

   ![](assets/dark-mode-image.png)

   <!--![](assets/dark-mode-custom.png)-->

1. Vous pouvez à tout moment **[!UICONTROL Basculer vers la vue en direct]** afin de vérifier comment votre contenu peut s’afficher sur différentes tailles d’appareil. Dans cet affichage, sélectionnez le bouton (bascule) Mode sombre en haut de l’écran pour prévisualiser la version en mode sombre de votre contenu sur les différents appareils.

   ![](assets/dark-mode-live-view.png){width="80%" align="center"}

   >[!CAUTION]
   >
   >L’aperçu en direct est un aperçu générique conçu pour comparer l’apparence du rendu sur différentes tailles d’appareil. Le rendu final peut varier en fonction du client de messagerie du destinataire.

1. Une fois que vous êtes satisfait des modifications pour le mode sombre, cliquez sur **[!UICONTROL Simuler du contenu]**.

   ![](assets/dark-mode-simulate.png)

1. Sélectionnez **[!UICONTROL Rendu d’e-mail]** et connectez-vous à votre compte Litmus. Vous pouvez voir le rendu final en mode sombre pour divers clients de messagerie. En savoir plus sur le [Rendu des emails](../content-management/rendering.md).

   >[!WARNING]
   >
   >Bien que la simulation se rapproche beaucoup de la façon dont les e-mails apparaîtront en mode sombre, le rendu réel peut différer en raison de variations au niveau des fournisseurs de services de messagerie ou des paramètres au niveau de l’appareil.

## Bonnes pratiques {#best-practices}

À mesure que l’adoption du mode sombre augmente sur les principaux clients de messagerie, il est essentiel d’examiner le rendu de vos e-mails dans des environnements clairs et sombres, que vous utilisiez le [mode sombre personnalisé](#define-custom-dark-mode) ou non.

Le mode sombre peut modifier les couleurs, les arrière-plans et les images, parfois en remplaçant les choix de conception. Pour garantir la cohérence visuelle, l’accessibilité et l’intégrité de la marque, suivez les bonnes pratiques répertoriées ci-dessous.

**Optimiser vos images et logos**

* Évitez les images avec des fonds blancs ou clairs codés en dur.

* Enregistrez les logos et les icônes en tant que PNG avec des arrière-plans transparents pour éviter les zones blanches visibles en mode sombre.

* Si la transparence n&#39;est pas une option, placez les images sur un arrière-plan solide dans votre conception pour éviter les inversions de couleurs gênantes.

**Surveillez vos antécédents**

* Assurez-vous que le contraste entre le texte et les couleurs d’arrière-plan est suffisant pour garantir la lisibilité dans les modes clair et sombre.

* Évitez de vous fier uniquement aux couleurs de fond pour les contenus critiques. Certains clients remplacent les couleurs de fond en mode sombre, afin de s’assurer que les informations clés sont toujours visibles.

**Conception de contenu accessible en mode sombre**

* Utilisez des combinaisons de couleurs faciles à distinguer pour les personnes atteintes de daltonisme.

* Utilisez une palette de tons moyens pour garantir un contraste sur des fonds clairs et sombres.

* Utilisez des combinaisons de couleurs accessibles à fort contraste pour améliorer la lisibilité et respecter les normes WCAG (Web Content Accessibility Guidelines). Utilisez des outils tels que le vérificateur de contraste de WebAIM pour vérifier le contraste des couleurs.

* Évitez les polices légères, car elles peuvent avoir un impact sur la lisibilité. Si votre marque nécessite une police fine, mettez-la en gras en mode sombre.

* Ignorez le blanc pur sur le noir pur, car cela peut entraîner une fatigue oculaire et peut être automatiquement inversé par certains clients de messagerie.

* Fournissez un style de secours accessible si le mode sombre n’est pas pris en charge.

**Tester vos e-mails dans un environnement en mode sombre**

* Utilisez le Designer d’e-mail [aperçu en mode sombre](#preview-dark-mode) qui utilise des modèles de couleurs inversés pour repérer les problèmes dès le début.

* Utilisez l’option [Rendu des e-mails](../content-management/rendering.md) qui utilise Litmus pour simuler vos conceptions sur les principaux clients de messagerie (Apple Mail, Gmail, Outlook) et voir comment les couleurs et les images se comportent en mode sombre.

<!--**Inline critical styles**

Inline CSS helps maintain more control over styling, as some clients strip external styles in dark mode.-->

## Clients de messagerie prenant en charge le mode sombre {#supporting-email-clients}

Vous trouverez ci-dessous une liste des principaux clients de messagerie prenant en charge le mode sombre.

>[!NOTE]
>
>Certaines versions de ces clients de messagerie ne prennent pas en charge le mode sombre. Par souci de clarté, elles sont donc également présentées dans ce tableau.

| Clients de messagerie prenant en charge le mode sombre | Versions compatibles | *Versions non prises en charge* |
|---------|----------|---------|
| Apple Mail macOS | 12,4, 16,0 | 10,3 ** |
| Apple Mail iOS | 13.0, 16.1 | 12,2 ** |
| MacOS Outlook | 2019, 16.70, 16.80 | NA |
| Outlook.com | 2019-07, 2022-12 | NA |
| Outlook iOS | 2020-01, 2022-12 | NA |
| Outlook Android | 2023-2003 | *2020-01, 2022-12* |
| E-mail Samsung (Android) | 6,1 | 6,0 ** |
| Mozilla Thunderbird (macOS) | 68,4 | *60,8, 78,5, 91,13* |
| Fastmail (Messagerie Web De Bureau) | 2022-2012 | *021-07* |
| HEY (Messagerie web pour ordinateur de bureau) | 2020-2006 | *2022-12* |
| Orange Desktop Webmail | 2019-08, 2021-03, 2022-12, 2024-04 | NA |
| Orange iOS | 2022-12, 2024-04 | *020-01* |
| Orange Android | 2024-2004 | *2020-01, 2022-12* |
| LaPoste.net | 2021-08, 2022-12 | NA |
| Messagerie Web pour ordinateur de bureau SFR | 2019-08, 2022-12 | NA |
| GMX (iOS et Android) | 2022-2006 | NA |
| 1&amp;1 (Messagerie web pour poste de travail et Android) | 2022-2006 | NA |
| WEB.DE (iOS et Android) | 2022-2006 | NA |
| Free.fr | 2022-2012 | NA |

>[!WARNING]
>
>Le rendu final en mode sombre dépend de chaque client de messagerie. Les résultats peuvent donc varier d&#39;un client à l&#39;autre.

<!--
* Check out the list of [email clients supporting dark mode](https://www.caniemail.com/search/?s=dark){target="_blank"}

* Learn more on Dark mode in this [Litmus blog post](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers){target="_blank"}
-->

## Clients de messagerie ne prenant pas en charge le mode sombre {#non-supporting-email-clients}

Certains clients de messagerie permettent aux utilisateurs de basculer leur interface en mode sombre, mais ce paramètre n’affecte pas l’affichage des e-mails HTML. Que l’interface soit en mode clair ou sombre, votre e-mail affichera le même rendu. Voici une liste de ces clients :

| Clients de messagerie ne prenant pas en charge le mode sombre |
|---------|
| Gmail (messagerie de bureau, iOS, Android, messagerie web mobile) |
| Fenêtres Outlook |
| Outlook Windows Mail |
| Yahoo!Mail |
| AOL |
| ProtonMail |
| SFR IOS |
| SFR ANDROID |
| Messagerie web de bureau GMX |
| Mail.ru |
| Web.DE Desktop Webmail |
| T-online.de |
