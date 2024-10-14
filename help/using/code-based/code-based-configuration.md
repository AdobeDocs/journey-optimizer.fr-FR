---
title: Configuration basée sur le code
description: Créer une configuration basée sur le code
feature: Code-based Experiences, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
exl-id: 1aff2f6f-914c-4088-afd8-58bd9edfe07d
source-git-commit: 83c8417d4aee278eba33e4adf6ccd033bcc6be1a
workflow-type: tm+mt
source-wordcount: '1531'
ht-degree: 42%

---

# Configurer votre expérience basée sur le code {#code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_code_based_surface"
>title="Définir une configuration d’expérience basée sur le code"
>abstract="Une configuration basée sur le code définit le chemin et l’emplacement dans votre application, identifiés de manière unique par un URI dans la mise en œuvre de l’application, où le contenu sera diffusé et consommé."

Avant de [créer votre expérience](create-code-based.md), vous devez créer une configuration d’expérience basée sur le code dans laquelle vous définissez où le contenu sera diffusé et utilisé dans votre application.

Une configuration d’expérience basée sur du code doit faire référence à la surface, qui est essentiellement l’emplacement où vous souhaitez effectuer le rendu de vos modifications. Selon la plateforme sélectionnée, vous devez saisir un emplacement/chemin ou l’URI de surface complet. [En savoir plus](#surface-definition)

## Création d’une configuration d’expérience basée sur du code {#create-code-based-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_location"
>title="Saisissez l’emplacement spécifique."
>abstract="Ce champ indique la destination exacte sur la page ou dans l’application à laquelle vous souhaitez que les utilisateurs accèdent. Il peut s’agir d’une section ou d’une page spécifique au coeur de la structure de navigation."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_mobile_url"
>title="Définition d’une URL pour la création et la prévisualisation de contenu"
>abstract="Ce champ garantit que les pages générées ou mises en correspondance par la règle ont une URL désignée, essentielle pour la création et la prévisualisation efficaces du contenu."

Pour créer une configuration de canal d’expérience basée sur du code, procédez comme suit :

1. Accédez au menu **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres généraux]** > **[!UICONTROL Configurations des canaux]**, puis cliquez sur **[!UICONTROL Créer une configuration des canaux]**.

   ![](assets/code_config_1.png)

1. Saisissez un nom et une description (facultatif) pour la configuration.

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à la configuration, vous pouvez sélectionner **[!UICONTROL Gérer l’accès]**. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../administration/object-based-access.md)

1. Sélectionnez une **[!UICONTROL Action marketing]** ou plusieurs pour associer des politiques de consentement aux messages utilisant cette configuration. Toutes les politiques de consentement associées à cette action marketing sont utilisées afin de respecter les préférences de vos clientes et clients. [En savoir plus](../action/consent.md#surface-marketing-actions)

1. Sélectionnez le canal **Expérience basée sur le code** .

   ![](assets/code_config_2.png)

1. Sélectionnez la plateforme pour laquelle l’expérience basée sur le code sera appliquée :

   * [Web](#web)
   * [iOS et/ou Android](#mobile)
   * [Autre](#other)

   >[!NOTE]
   >
   >Vous pouvez sélectionner plusieurs plateformes. Lorsque vous choisissez plusieurs plateformes, le contenu est diffusé sur toutes les pages ou applications sélectionnées.

1. Choisissez le format attendu par l’application pour cet emplacement particulier. Cela sera utilisé lors de la création de l’expérience basée sur le code dans les campagnes et les parcours.

   ![](assets/code_config_4.png)

1. Cliquez sur **[!UICONTROL Submit]** pour enregistrer vos modifications.

Vous pouvez maintenant sélectionner cette configuration lors de la [création d’une expérience basée sur le code](create-code-based.md) dans vos campagnes et parcours.

>[!NOTE]
>
>Votre équipe de mise en oeuvre d’application est chargée d’effectuer des appels d’API ou de SDK explicites pour récupérer du contenu pour les surfaces définies dans la configuration d’expérience basée sur le code sélectionnée. Pour en savoir plus sur les différentes mises en oeuvre client, consultez [cette section](code-based-implementation-samples.md).

### Plateformes web {#web}

>[!CONTEXTUALHELP]
>id="ajo_admin_default_web_url"
>title="Définition d’une URL pour la création et la prévisualisation de contenu"
>abstract="Ce champ garantit que les pages générées ou mises en correspondance par la règle ont une URL désignée, essentielle pour la création et la prévisualisation efficaces du contenu."

Pour définir les paramètres de configuration de l’expérience basés sur du code pour les plateformes web, procédez comme suit.

1. Sélectionnez l’une des options suivantes :

   * **[!UICONTROL Page unique]** - Si vous souhaitez appliquer les modifications à une seule page exclusivement, saisissez une **[!UICONTROL URL de page]**.

     ![](assets/code_config_single_page.png)

   * **[!UICONTROL Règle de correspondance de pages]** - Pour cibler plusieurs URL correspondant à la même règle, créez une ou plusieurs règles. [En savoir plus](../web/web-configuration.md#web-page-matching-rule)

     <!--This could be used to apply changes universally across a website, such as updating a hero banner across all pages or adding a top image to display on every product page.-->

     Par exemple, si vous souhaitez modifier des éléments qui s’affichent sur toutes les pages de produits pour femmes de votre site web Luma, sélectionnez **[!UICONTROL Domaine]** > **[!UICONTROL Commence par]** > `luma` et **[!UICONTROL Page]** > **[!UICONTROL Contient]** > `women`.

     ![](assets/code_config_matching_rules.png)

1. Les conditions suivantes s’appliquent à l’URL d’aperçu :

   * Si une seule URL de page est saisie, cette URL sera utilisée pour l’aperçu ; il n’est pas nécessaire de saisir une autre URL.
   * Si une [page correspondant à la règle](../web/web-configuration.md#web-page-matching-rule) est sélectionnée, vous devez saisir une **[!UICONTROL URL de création et d’aperçu par défaut]** qui sera utilisée pour prévisualiser l’expérience dans le navigateur.

     ![](assets/code_config_matching_rules_preview.png)

1. Le champ **[!UICONTROL Emplacement sur la page]** spécifie la destination exacte à laquelle les utilisateurs doivent accéder dans le site Web. Il peut s’agir d’une section ou d’une page spécifique au plus profond de la structure de navigation du site.

   ![](assets/code_config_location_on_page.png)

### Plateformes mobiles (iOS et Android) {#mobile}

>[!CONTEXTUALHELP]
>id="ajo_admin_app_id"
>title="Fournir votre ID d’application"
>abstract="Saisissez l’ID de l’application pour une identification et une configuration précises au sein de l’environnement opérationnel de l’application, afin d’assurer une intégration et des fonctionnalités homogènes."

>[!CONTEXTUALHELP]
>id="ajo_admin_mobile_url_preview"
>title="Saisissez l&#39;URL de prévisualisation du contenu"
>abstract="Ce champ est essentiel pour activer la simulation et la prévisualisation de votre contenu directement sur votre appareil au sein de votre application."

Pour définir les paramètres de configuration d’expérience basés sur du code pour les plateformes mobiles, procédez comme suit.

1. Saisissez votre **[!UICONTROL ID d’application]**. Cela permet une identification et une configuration précises au sein de l’environnement opérationnel de l’application et garantit une intégration et des fonctionnalités homogènes.

1. Indiquez l’ **[!UICONTROL emplacement ou chemin d’accès dans l’application]**. Ce champ indique la destination exacte à laquelle les utilisateurs doivent accéder dans l’application. Il peut s’agir d’une section ou d’une page spécifique au cœur de la structure de navigation de l’application.

   ![](assets/code_config_3.png){width="500"}

1. Renseignez le champ **[!UICONTROL URL de prévisualisation]** pour activer les prévisualisations sur l’appareil. Cette URL informe le service d’aperçu de l’URL spécifique à utiliser lors du déclenchement d’un aperçu<!--on device. Learn more-->.

   L’URL d’aperçu est un lien profond configuré par le développeur de l’application dans votre application. Cela garantit que toutes les URL correspondant au modèle de lien profond s’ouvriront dans l’application plutôt que dans un navigateur web mobile. Contactez le développeur de votre application pour obtenir le schéma de lien profond configuré pour votre application.

+++  Les ressources suivantes peuvent vous aider à configurer des liens profonds pour l’implémentation de votre application.

   * Pour Android :

      * [Créer des liens profonds vers le contexte de l’application](https://developer.android.com/training/app-links/deep-linking)

   * Pour iOS :

      * [Définir un schéma d’URL personnalisé pour votre application](https://developer.apple.com/documentation/xcode/defining-a-custom-url-scheme-for-your-app)

      * [Prendre en charge des liens universels dans votre application](https://developer.apple.com/documentation/xcode/supporting-universal-links-in-your-app)

+++

   >[!NOTE]
   >
   >Si vous rencontrez des problèmes lors de la prévisualisation de l’expérience, reportez-vous à [cette documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/troubleshooting#app-does-not-open-link).

### Autres plateformes {#other}

Pour définir les paramètres de configuration de l’expérience basés sur du code pour d’autres plateformes (telles que les consoles vidéo, les appareils connectés à la télévision, les téléviseurs intelligents, les kiosques, les distributeurs automatiques de billets, les assistants vocaux, les appareils IoT, etc.), suivez les étapes ci-dessous.

1. Sélectionnez **[!UICONTROL Autre]** comme plateforme si votre mise en oeuvre n’est pas destinée au Web, à iOS ou à Android, ou si vous devez cibler des URI spécifiques.

1. Saisissez l’ **[!UICONTROL URI de surface]**. Un URI de surface est un identifiant unique correspondant à l’entité dans laquelle vous souhaitez diffuser votre expérience. [En savoir plus](#surface-definition)

   ![](assets/code_config_5.png)

   >[!CAUTION]
   >
   >Veillez à saisir un URI de surface correspondant à celui utilisé dans votre propre mise en oeuvre. Dans le cas contraire, les modifications ne peuvent pas être diffusées.

1. **[!UICONTROL Ajoutez un autre URI de surface]** si nécessaire. Vous pouvez ajouter jusqu’à dix URI.

   >[!NOTE]
   >
   >Lors de l’ajout de plusieurs URI, le contenu est diffusé à tous les composants répertoriés.

## Qu’est-ce qu’une surface ? {#surface-definition}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_uri"
>title="Ajout de l’URI de surface pour votre composant"
>abstract="Si votre mise en oeuvre n’est pas destinée au Web, à iOS ou à Android, ou si vous devez cibler des URI spécifiques, saisissez un URI de surface, qui est un identifiant unique qui dirige vers l’entité où vous souhaitez diffuser votre expérience. Veillez à saisir un URI de surface correspondant à celui utilisé dans votre propre mise en oeuvre."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/code-based-configuration#other" text="Création d’une configuration d’expérience basée sur du code pour d’autres plateformes"

Une expérience basée sur du code **surface** est toute entité conçue pour l’interaction de l’utilisateur ou du système, qui est identifiée de manière unique par un **URI**. La surface est spécifiée dans l’implémentation de l’application et doit correspondre à la surface référencée dans la configuration de votre canal d’expérience basée sur le code.

Une surface peut être vue comme un conteneur à n’importe quel niveau de hiérarchie avec une entité (point de contact) qui existe.

* Il peut s’agir d’une page web, d’une application mobile, d’une appli de bureau, d’un emplacement de contenu spécifique au sein d’une entité plus grande (par exemple, une `div`) ou d’un modèle d’affichage non standard (par exemple, un kiosque ou une bannière d’application de bureau).<!--In retail, a kiosk is a digital display or small structure that businesses often place in high-traffic areas to engage customers.-->

* Elle peut également s’étendre à des éléments spécifiques de conteneurs de contenu à des fins de non-affichage ou d’affichage abstrait (par exemple, des objets blob JSON fournis à des services).

* Il peut également s’agir d’une surface de caractères génériques qui correspond à diverses définitions de surface client (par exemple, un emplacement d’image principale sur chaque page de votre site web peut se traduire en un URI de surface comme : web://mondomaine.com/*#image_principale).

Lors de la création d’une configuration de canal d’expérience basée sur du code, vous avez deux manières de spécifier la surface en fonction de la plateforme sélectionnée :

* Pour les plateformes **[!UICONTROL Web]**, **[!UICONTROL iOS]** et **[!UICONTROL Android]**, vous devez saisir un **emplacement ou chemin** pour composer la surface.

* Si la plateforme est **[!UICONTROL Autre]**, vous devez saisir l’ **URI de surface** complet, comme dans les exemples ci-dessous.

Un URI de surface sert d’identifiant précis orientant vers des éléments ou des composants d’interface utilisateur distincts au sein d’une application. Fondamentalement, un URI de surface est composé de plusieurs sections :

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
