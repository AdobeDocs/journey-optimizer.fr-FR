---
solution: Journey Optimizer
product: journey optimizer
title: Basculer vers le mode sombre
description: Découvrez comment utiliser le mode sombre dans le Concepteur d’e-mail.
badge: label="Beta" type="Informative"
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: mode sombre, e-mail, couleur, éditeur
hide: true
hidefromtoc: true
exl-id: 27442cb0-5027-4d9c-9d3c-9ec33af7c9ff
source-git-commit: 95e50386d4190d0b967d133a327c25ab1681b5c1
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 100%

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
>Cette fonctionnalité est actuellement en version Beta et disponible uniquement pour les clientes et clients Beta. Pour rejoindre le programme Beta, contactez votre représentant ou représentante Adobe.

Lorsque vous concevez vos e-mails, le [Concepteur d’e-mail](get-started-email-design.md) [!DNL Journey Optimizer] vous permet de passer en **[!UICONTROL mode sombre]**, dans lequel vous pouvez définir des paramètres personnalisés spécifiques. Lorsque le mode sombre est activé, les clients de messagerie pris en charge affichent les paramètres que vous avez définis pour ce mode.

>[!WARNING]
>
>Le rendu final du mode sombre dépend du client de messagerie de la personne destinataire.
>
>Les clients de messagerie ne prennent pas tous en charge le mode sombre personnalisé. <!--[See the list](#non-supporting-email-clients)-->De plus, certains clients de messagerie appliquent uniquement leur propre mode sombre par défaut pour tous les e-mails reçus. Dans ce cas, les paramètres personnalisés que vous avez définis dans le Concepteur d’e-mail ne pourront pas être affichés.

La liste des clients de messagerie prenant en charge le mode sombre figure dans [cette section](#supporting-email-clients).

## Présentation du mode sombre {#what-is-dark-mode}

Le mode sombre permet aux clients de messagerie et aux applications pris en charge d’afficher les e-mails avec des arrière-plans plus sombres et des couleurs plus claires pour le texte, les boutons et les autres éléments de l’interface d’utilisation. Il permet de réduire la fatigue oculaire, d’économiser la batterie et d’améliorer la lisibilité dans les environnements peu éclairés pour une expérience visuelle plus confortable.

<!--Dark Mode uses a dark color palette with light text and UI elements to reduce eye strain, save battery life, and improve readability in low-light environments.-->

Étant donné qu’il s’agit d’une tendance croissante dans les principaux systèmes d’exploitation et applications (Apple Mail, Gmail, Outlook, Twitter, Slack), cette fonctionnalité est devenue un point important à prendre en compte dans la conception d’e-mails modernes pour veiller à ce que le contenu reste lisible et visuellement attrayant pour tous les utilisateurs et utilisatrices.

Cependant, il n’est pas possible de garantir que votre e-mail s’affichera exactement de la même manière en mode sombre sur tous les appareils. Certaines variations visuelles peuvent également être provoquées par la modification forcée de la conception d’origine par l’application ou l’appareil de messagerie.

En effet, la manière dont le mode sombre est appliqué par les clients de messagerie peut varier comme suit<!--between different devices and apps--> :

* Les clients de messagerie ne prennent pas tous en charge cette fonctionnalité.

  >[!NOTE]
  >
  >La liste des clients de messagerie ne prenant pas en charge le mode sombre figure dans [cette section](#non-supporting-email-clients).

* Certains clients de messagerie ajustent automatiquement les couleurs, les arrière-plans et les images. Dans ce cas, si vous définissez des paramètres personnalisés dans le Concepteur d’e-mail, le rendu de ces paramètres ne sera probablement pas affiché.

* D’autres clients de messagerie offrent la possibilité d’afficher un mode sombre personnalisé (par exemple avec la méthode `@media (prefers-color-scheme: dark)`). Dans ce cas, les paramètres spécifiques que vous définissez dans le Concepteur d’e-mail doivent s’afficher. Découvrez dans [cette section](#define-custom-dark-mode) comment définir les paramètres personnalisés du mode sombre dans le Concepteur d’e-mail.

## Mode sombre dans le Concepteur d’e-mail {#dark-mode-email-designer}

En ce qui concerne le mode sombre dans le Concepteur d’e-mail, deux aspects doivent être pris en compte :

* Vous pouvez prévisualiser la manière dont le mode sombre par défaut s’affichera dans la plupart des clients de messagerie pris en charge. [En savoir plus](#preview-dark-mode)

<!--
    >[!CAUTION]
    >
    >The final rendering may vary according to the recipient's email client. To see the exact rendering for each email client, use the [Email rendering](../content-management/rendering.md) option.-->

* Si vous souhaitez remplacer les paramètres par défaut des clients de messagerie pris en charge, vous pouvez définir des paramètres de mode sombre personnalisés qui s’appliquent à l’e-mail que vous être en train de modifier. [En savoir plus](#define-custom-dark-mode)

<!--
    >[!WARNING]
    >
    >Not all email clients support custom dark mode. Some email clients only apply their own default dark mode for all emails that are received. In this case, the custom settings that you defined in the Email Designer cannot be rendered. [Learn more](#guardrails)-->

### Prévisualiser le mode sombre par défaut {#preview-dark-mode}

Pour accéder au mode sombre dans le Concepteur d’e-mail et prévisualiser les paramètres par défaut du mode sombre, procédez comme suit.

1. Dans la page d’accueil du Concepteur d’e-mail, cliquez sur le bouton **[!UICONTROL Créer à partir de zéro]**. [En savoir plus](content-from-scratch.md)

<!--Should work with templates and themes, NOT for LP and fragments - but TBC with eng.
    >[!NOTE]
    >
    >Currently you may not be able to switch to dark mode if you select an [email template](use-email-templates.md) or if you apply a [theme](apply-email-themes.md).-->

1. Ajoutez des [structures](content-from-scratch.md) et des [composants de contenu](content-components.md) à votre contenu.

1. En haut à droite de la zone de travail centrale, cliquez sur le bouton pour passer en **[!UICONTROL mode sombre]**.

   ![](assets/light-mode-toggle.png)

1. La prévisualisation du mode sombre par défaut s’affiche.

   ![](assets/dark-mode-default.png)

Par défaut, l’aperçu en mode sombre du Concepteur d’e-mail applique le modèle de couleurs « inversion complète des couleurs » à tous les éléments, à l’exception des images et des icônes.

Cela signifie qu’il détecte les zones comportant des éléments clairs et sombres et les inverse, de sorte que les arrière-plans clairs deviennent sombres et que le texte sombre devient clair, tandis que les arrière-plans sombres deviennent clairs et que le texte clair devient sombre.

>[!CAUTION]
>
>Le rendu final peut varier en fonction du client de messagerie de la personne destinataire. Pour visualiser une simulation qui se rapproche le plus possible du résultat final pour chaque client de messagerie, utilisez l’option [Rendu des e-mails](../content-management/rendering.md).

<!--This is custom dark mode:

  ![](assets/dark-mode-custom.png)

Here you can see that we have applied a different background, defined another image and change the color of the text and button.-->

### Définir le mode sombre personnalisé {#define-custom-dark-mode}

Après avoir activé le **[!UICONTROL mode sombre]**, vous pouvez choisir de modifier des éléments de style spécifiques dans votre contenu qui s’afficheront uniquement si le mode sombre est activé dans le client de messagerie de la personne destinataire, à condition que le client prenne en charge cette fonctionnalité.

>[!WARNING]
>
>Les clients de messagerie ne prennent pas tous en charge le mode sombre. De plus, certains clients de messagerie appliquent uniquement leur propre mode sombre par défaut pour tous les e-mails reçus. Dans les deux cas, le rendu des paramètres personnalisés que vous avez définis dans le Concepteur d’e-mail ne pourra pas être affiché.

Pour tirer parti du style du mode sombre personnalisé du Concepteur d’e-mail, Journey Optimizer utilise la requête CSS<!-- `@media (prefers-color-scheme: dark)` method--> `@media (prefers-color-scheme: dark)`, qui détecte si le client de messagerie de l’utilisateur ou de l’utilisatrice est en mode sombre et applique le thème sombre défini dans votre e-mail.

Pour définir les paramètres du mode sombre personnalisé, procédez comme suit.

1. Veillez à basculer vers l’aperçu en **[!UICONTROL mode sombre]** dans le Concepteur d’e-mail. [Voici comment procéder](#preview-dark-mode)

1. Modifiez les attributs de couleurs du style, tels que le texte, les arrière-plans, les boutons, etc.

1. Vous ne pouvez pas modifier les couleurs des images et des icônes, mais vous pouvez définir des ressources spécifiques au mode sombre. Pour ce faire, sélectionnez une image. Passez en **[!UICONTROL mode sombre]** à l’aide du bouton dédié dans le volet **[!UICONTROL Paramètres]** et sélectionnez une autre ressource.

   ![](assets/dark-mode-image.png)

   <!--![](assets/dark-mode-custom.png)-->

1. Vous pouvez à tout moment **[!UICONTROL Passer en mode en direct]** afin de vérifier comment votre contenu s’affiche sur les différentes tailles d’appareils. Dans cette vue, cliquez sur le bouton Mode sombre en haut de l’écran pour prévisualiser la version en mode sombre de votre contenu sur les différents appareils.

   ![](assets/dark-mode-live-view.png){width="80%" align="center"}

   >[!CAUTION]
   >
   >Le mode en direct est une prévisualisation générique conçue pour comparer l’aspect du rendu sur différentes tailles d’appareils. Le rendu final peut varier en fonction du client de messagerie de la personne destinataire.

1. Une fois que vous avez apporté les modifications souhaitées pour le mode sombre, cliquez sur **[!UICONTROL Simuler le contenu]**.

   ![](assets/dark-mode-simulate.png)

1. Sélectionnez **[!UICONTROL Rendu d’e-mail]** et connectez-vous à votre compte Litmus. Vous pouvez voir le rendu final en mode sombre pour divers clients de messagerie. En savoir plus sur le [rendu des e-mails](../content-management/rendering.md).

   >[!WARNING]
   >
   >Bien que la simulation se rapproche beaucoup de la façon dont les e-mails s’afficheront en mode sombre, le rendu réel peut être différent en raison de variations au niveau des paramètres des fournisseurs de services de messagerie ou au niveau des paramètres des appareils.

## Bonnes pratiques {#best-practices}

À mesure que l’adoption du mode sombre augmente dans les principaux clients de messagerie, il est essentiel d’examiner le rendu de vos e-mails à la fois dans les environnements clairs et sombres, que vous utilisiez le [mode sombre personnalisé](#define-custom-dark-mode) ou non.

Le mode sombre peut modifier les couleurs, les arrière-plans et les images, parfois en remplaçant les choix définis lors de la conception. Pour garantir la cohérence visuelle, l’accessibilité et l’intégrité de la marque, suivez les bonnes pratiques répertoriées ci-dessous.

**Optimiser vos images et vos logos**

* Évitez les images avec des fonds blancs ou clairs codés en dur.

* Enregistrez les logos et les icônes au format PNG avec des arrière-plans transparents pour éviter la présence de zones blanches visibles en mode sombre.

* Si vous ne pouvez pas utiliser la transparence, placez les images sur un arrière-plan uni dans votre conception pour éviter des inversions de couleurs inappropriées.

**Vérifier vos arrière-plans**

* Vérifiez que le contraste entre le texte et les couleurs d’arrière-plan est suffisant pour garantir une bonne lisibilité en mode clair et en mode sombre.

* Évitez de vous fier uniquement aux couleurs d’arrière-plan pour du contenu important. Certains clients remplacent les couleurs d’arrière-plan en mode sombre ; veillez donc à ce que les informations clés soient toujours visibles.

**Concevoir du contenu accessible en mode sombre**

<!--KEEP dark mode accessibility best practices IN ONE SINGLE LOCATION - for now listed on this page.
If needed, it can be moved to the Design accessible content page:
The best practices for designing accesible content in dark mode are listed in [this section](accessible-content.md#dark-mode).-->

* Utilisez des combinaisons de couleurs faciles à distinguer pour les personnes atteintes de daltonisme.

* Utilisez une palette de tons moyens pour garantir un contraste adéquat par rapport à des arrière-plans clairs et sombres.

* Utilisez des combinaisons de couleurs accessibles à fort contraste pour améliorer la lisibilité et respecter les normes WCAG. Utilisez des outils tels que le vérificateur de contraste de WebAIM pour vérifier le contraste des couleurs.

* Évitez les polices de caractères fines, car elles peuvent affecter la lisibilité. Si votre marque nécessite l’utilisation d’une police fine, mettez-la en gras en mode sombre.

* N’utilisez pas de blanc pur sur du noir pur, car cela peut entraîner une fatigue oculaire et peut être automatiquement inversé par certains clients de messagerie.

* Fournissez un style de secours accessible si le mode sombre n’est pas pris en charge.

**Tester vos e-mails dans un environnement en mode sombre**

* Utilisez la [prévisualisation du mode sombre](#preview-dark-mode) du Concepteur d’e-mail, qui utilise des modèles de couleurs inversées, pour repérer les problèmes en amont.

* Utilisez l’option [Rendu d’e-mail](../content-management/rendering.md) qui tire parti de Litmus pour simuler vos conceptions sur les principaux clients de messagerie (Apple Mail, Gmail, Outlook) et voir comment les couleurs et les images se comportent en mode sombre.

<!--**Inline critical styles**

Inline CSS helps maintain more control over styling, as some clients strip external styles in dark mode.-->

## Clients de messagerie prenant en charge le mode sombre {#supporting-email-clients}

Vous trouverez ci-dessous la liste des principaux clients de messagerie prenant en charge le mode sombre.

>[!NOTE]
>
>Certaines versions de ces clients de messagerie ne prennent pas en charge le mode sombre. Elles sont donc également présentées dans ce tableau par souci de clarté.

| Clients de messagerie prenant en charge le mode sombre | Versions compatibles | *Versions non prises en charge* |
|---------|----------|---------|
| Apple Mail macOS | 12.4, 16.0 | *10.3* |
| Apple Mail iOS | 13.0, 16.1 | *12.2* |
| Outlook macOS | 2019, 16.70, 16.80 | Non applicable |
| Outlook.com | 2019-07, 2022-12 | Non applicable |
| Outlook iOS | 2020-01, 2022-12 | Non applicable |
| Outlook Android | 2023-03 | *2020-01, 2022-12* |
| Samsung Email (Android) | 6.1 | *6.0* |
| Mozilla Thunderbird (macOS) | 68.4 | *60.8, 78.5, 91.13* |
| Fastmail (client de messagerie web de bureau) | 2022-12 | *2021-07* |
| HEY (client de messagerie web de bureau) | 2020-06 | *2022-12* |
| Orange (client de messagerie web de bureau) | 2019-08, 2021-03, 2022-12, 2024-04 | Non applicable |
| Orange iOS | 2022-12, 2024-04 | *2020-01* |
| Orange Android | 2024-04 | *2020-01, 2022-12* |
| LaPoste.net | 2021-08, 2022-12 | Non applicable |
| SFR (client de messagerie web de bureau) | 2019-08, 2022-12 | Non applicable |
| GMX (iOs et Android) | 2022-06 | Non applicable |
| 1&amp;1 (client de messagerie web de bureau et Android) | 2022-06 | Non applicable |
| WEB.DE (iOs et Android) | 2022-06 | Non applicable |
| Free.fr | 2022-12 | Non applicable |

>[!WARNING]
>
>Le rendu final en mode sombre dépend de chaque client de messagerie. Le résultat peut donc varier d’un client à l’autre.

<!--
* Check out the list of [email clients supporting dark mode](https://www.caniemail.com/search/?s=dark){target="_blank"}

* Learn more on Dark mode in this [Litmus blog post](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers){target="_blank"}
-->

## Clients de messagerie ne prenant pas en charge le mode sombre {#non-supporting-email-clients}

Certains clients de messagerie permettent aux utilisateurs de basculer leur interface en mode sombre, mais ce paramètre n’affecte pas la manière dont les e-mails HTML sont affichés. Que l’interface soit en mode clair ou en mode sombre, votre e-mail s’affichera de la même manière. Voici la liste de ces clients :

| Clients de messagerie ne prenant pas en charge le mode sombre |
|---------|
| Gmail (client de messagerie web de bureau, iOS, Android, client de messagerie web mobile) |
| Outlook Windows |
| Outlook Windows Mail |
| Yahoo!Mail |
| AOL |
| ProtonMail |
| SFR iOS |
| SFR Android |
| GMX (client de messagerie web de bureau) |
| Mail.ru |
| WEB.DE (client de messagerie web de bureau) |
| T-online.de |
