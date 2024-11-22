---
title: Surface basée sur le code
description: Découvrez ce qu’est une surface d’expérience basée sur du code
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
source-git-commit: e9181c333fb9188cdfcee3fd96c1d3bb94b8dd75
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 56%

---

# Surfaces d’expérience basées sur le code {#code-based-surface}

## Qu’est-ce qu’une surface ? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="Ajouter l’URI de surface pour votre composant"
>abstract="Si votre mise en œuvre n’est pas destinée au Web, à iOS ou à Android, ou si vous devez cibler des URI spécifiques, saisissez un URI de surface, c’est-à-dire un identifiant unique qui dirige vers l’entité où vous souhaitez diffuser votre expérience. Veillez à saisir un URI de surface correspondant à celui utilisé dans votre propre mise en œuvre."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/code-based-experience/configure-code-based-channel/code-based-configuration#other" text="Création d’une configuration d’expérience basée sur du code pour d’autres plateformes"

Une expérience basée sur du code **surface** est toute entité conçue pour l’interaction de l’utilisateur ou du système, identifiée de manière unique par un [URI](#surface-uri). La surface est spécifiée dans l’ [implémentation de l’application](code-based-prerequisites.md#implementation-prerequisites) et doit correspondre à la surface référencée dans votre [ configuration de canal d’expérience basée sur le code](code-based-configuration.md).

Une surface peut être considérée comme un conteneur à n’importe quel niveau de hiérarchie ayant une entité (point de contact) qui existe.

* Il peut s’agir d’une page web, d’une application mobile, d’une appli de bureau, d’un emplacement de contenu spécifique au sein d’une entité plus grande (par exemple, une `div`) ou d’un modèle d’affichage non standard (par exemple, un kiosque ou une bannière d’application de bureau).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Elle peut également s’étendre à des éléments spécifiques de conteneurs de contenu à des fins de non-affichage ou d’affichage abstrait (par exemple, des objets blob JSON fournis à des services).

* Il peut également s’agir d’une surface de caractères génériques qui correspond à diverses définitions de surface client (par exemple, un emplacement d’image principale sur chaque page de votre site web peut se traduire en un URI de surface comme : web://mondomaine.com/*#image_principale).

## Identifiant de surface {#surface-uri}

Un **URI de surface** sert d’identifiant précis pour diriger vers des éléments ou des composants d’interface utilisateur distincts au sein d’une application. Fondamentalement, un URI de surface est composé de plusieurs sections :

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

## composition d’URI {#uri-composition}

Dans [!DNL Journey Optimizer], le canal d’expérience basé sur le code prend en charge deux types d’implémentations client :

* Basé sur le [ SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target="_blank"} pour vos sites Web ou sur le [ SDK Mobile Adobe Experience Platform ](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} pour vos applications mobiles ;
* Côté serveur ou hybride à l’aide des [API de serveur Edge Network AEP](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr){target="_blank"}.

>[!NOTE]
>
>Pour en savoir plus sur les conditions préalables à la mise en oeuvre, consultez [cette section](code-based-prerequisites.md#implementation-prerequisites).

À l’aide d’expériences basées sur du code, vous pouvez modifier du contenu sur des emplacements granulaires <!--(such as a specific location on a page, or inside a mobile native app)--> qui sont identifiés de manière unique par [!DNL Journey Optimizer] à l’aide des [URI de surface](#surface-uri).

Ces URI de surface sont composés et gérés selon la méthode d’implémentation :

* **SDK Web/Mobile** : votre développeur web/mobile doit définir ces emplacements granulaires sous la forme de chaînes simples, car le SDK Web/Mobile est capable de composer automatiquement l’URI de surface en fonction de l’URL/de l’application actuelle et de la chaîne d’emplacement.

* **API Edge Network** : le développeur d’applications/de pages doit définir des URI de surface complets qui incluent le chemin et l’emplacement complets où le contenu sera utilisé, car les URI complets sont requis dans ce type d’implémentation.

C’est pourquoi, lors de la création d’une [ configuration de canal d’expérience basée sur le code ](code-based-configuration.md), vous avez deux manières de spécifier la surface en fonction de la plateforme sélectionnée :

* Pour les plateformes **[!UICONTROL Web]**, **[!UICONTROL iOS]** et **[!UICONTROL Android]**, vous devez saisir l’ **URL/app ID** et un **emplacement ou chemin** pour composer la surface. En savoir plus sur la configuration des expériences basées sur le code pour les plateformes [web](code-based-configuration.md#web) et [mobile](code-based-configuration.md#mobile)

* Si la plateforme est **[!UICONTROL Autre]**, vous devez saisir l’ **URI de surface** complet, comme dans les exemples [ci-dessus](#surface-uri). En savoir plus sur la configuration d’expériences basées sur le code pour [autres](code-based-configuration.md#other) plateformes
