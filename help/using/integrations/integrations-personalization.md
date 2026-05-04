---
solution: Journey Optimizer
product: journey optimizer
title: Activer les intégrations externes
description: Intégrez des intégrations externes au processus de création de canal pour enrichir le contenu avec des informations personnalisées et dynamiques
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: Intégration
source-git-commit: 4cc3c959fe08c1d574a5d041bf7721441bc96f97
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 43%

---


# Utiliser des intégrations externes pour la personnalisation {#integrations-personalization}

Avant d’utiliser des intégrations externes dans votre contenu, vérifiez qu’un administrateur a **configuré et activé** chaque intégration (point d’entrée, authentification, politiques, payload de réponse et activation), comme décrit dans la section [&#x200B; Utiliser les intégrations &#x200B;](integrations.md).

Vous pouvez ajouter jusqu’à **3** intégrations par **[!UICONTROL fragment]** et jusqu’à **5** sur le message. Les intégrations qui proviennent uniquement de fragments ne sont pas comptabilisées dans le **5**.

## Application de la personnalisation de l’intégration à votre contenu {#apply-integration-personalization}

En tant que responsable marketing, vous pouvez utiliser des intégrations configurées pour personnaliser votre contenu. Procédez comme suit :

1. Accédez au contenu de votre campagne et cliquez sur **[!UICONTROL Ajouter une personnalisation]** dans le champ **[!UICONTROL Composants]** Texte ou HTML.

   [En savoir plus sur les composants](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Accédez à la section **[!UICONTROL Intégrations]** et cliquez sur **[!UICONTROL Ouvrir les intégrations]** pour afficher toutes les intégrations actives.

   Notez que **les fragments** sont disponibles avec les intégrations , mais prennent uniquement en charge les canaux sortants. Une fois qu’un fragment est publié, l’ajout et l’enregistrement de nouvelles intégrations sont désactivés afin d’éviter tout impact sur les parcours et campagnes existants.

   ![](assets/external-integration-content-2.png)

1. Sélectionnez une intégration et cliquez sur **[!UICONTROL Enregistrer]**.

   ![](assets/external-integration-content-3.png)

1. Activez le mode **[!UICONTROL Pastilles]** pour déverrouiller le menu d’intégration avancé.

   ![](assets/external-integration-content-4.png)

1. Lorsque vous créez la personnalisation de l’intégration, l’assistant Intégrations inclut un champ **`required`** qui définit la manière dont les données manquantes ou en échec interagissent avec le contenu par défaut :

   * **`required=true`** (par défaut) : le rendu s’arrête pour ce message. L’envoi est exclu avec **`ExternalDataLookupExclusion`** et cette exclusion est enregistrée dans le jeu de données de commentaires de messages **message**.
   * **`required=false`** : la variable de résultat est définie sur **`null`** et le rendu se poursuit. Utilisez du texte par défaut, des secours ou une logique conditionnelle dans votre modèle afin que les profils ne reçoivent pas de contenu vide lorsque l’intégration ne renvoie pas de données.

     ![](assets/external-integration-content-8.png)

1. Pour terminer la configuration de votre intégration, définissez les attributs d’intégration, qui ont été précédemment spécifiés lors de la [configuration](integrations.md#configure).

   Vous pouvez attribuer des valeurs à ces attributs à l’aide de valeurs statiques, qui restent constantes, ou d’attributs de profil, qui extraient dynamiquement des informations des profils utilisateur.

   ![](assets/external-integration-content-5.png)

1. Une fois les attributs d’intégration définis, vous pouvez utiliser les champs d’intégration de votre contenu pour envoyer des messages personnalisés en cliquant sur l’icône ![ajouter](assets/do-not-localize/Smock_Add_18_N.svg).

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >Les jetons de votre modèle doivent utiliser uniquement les champs exposés par l’administrateur dans la configuration de l’intégration. Par exemple, `{{weatherResponse.temperature}}` est valide lorsque `temperature` est exposé ; `{{weatherResponse.humidity}}` est rejeté dans l’éditeur si `humidity` n’a pas été exposé.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Votre personnalisation d’intégration est maintenant appliquée avec succès à votre contenu, en veillant à ce que chaque destinataire reçoive une expérience adaptée et pertinente en fonction des attributs que vous avez configurés.

![](assets/external-integration-content-7.png)

<!--

## Map one API call to another {#map-integration-chain}

You can **chain** integrations so that values returned by one active integration drive the inputs (path, headers, or query parameters) of another. That lets you build a real-time data flow in a single message without custom code.

Before you start, make sure that:

* An administrator has configured and activated every integration you need. See [Configure your Integration](integrations.md).
* Variable path placeholders, headers, and query parameters are set up in the integration configuration with marketer-facing labels.
* The administrator exposed the response fields you need in each integration's **[!UICONTROL Response payload]** so they appear when authoring.

In the below example, a reservation system integration returns a flight booking reference from the profile context. A separate flight-information integration expects that reference as a **path variable**. In the personalization editor, you map the second integration's variable to a field from the first integration's response, instead of a static value or profile attribute alone.

1. Open your message or fragment and place the cursor where you want personalized content (for example, a **[!UICONTROL Text]** field).

1. Open the personalization editor and go to **[!UICONTROL Integrations]** → **[!UICONTROL Open integrations]**.

1. Select the integration whose output will supply the downstream input (in the example, the reservation or profile API that returns the flight identifier).

1. Define that integration's inputs as usual—static values, profile attributes, or other allowed mappings—then save so its response is available for chaining.

    >[!NOTE]
    >
    > Fields must appear in the administrator-defined response payload for each integration. You cannot reference response properties that were not exposed in configuration.

1. Select the **second** integration (for example, the API that needs the flight number or booking reference on the URL path).

1. For each input that must come from the first call—often a **path variable** or **variable** header/query parameter—choose the mapping source that references the **first integration's response** (for example, the flight booking reference field from the reservation payload). Do not use a static test value if you need live, profile-specific data.

1. Insert the response tokens you need in the content (for example, destination name from the flight API, loyalty balance from a loyalty integration) using the ![add](assets/do-not-localize/Smock_Add_18_N.svg) control.

1. Save the personalization.

When you **simulate** or send, Journey Optimizer resolves integrations in order: the first call runs with the profile context you configured; its output is used to build the second request. Different integrations may run at simulation time and at send time according to your setup and channel behavior.

-->

## Vidéo pratique {#video}

Cette vidéo montre comment **Intégrations** connecter Adobe Journey Optimizer à des API externes afin d’extraire des données et du contenu en direct dans des canaux **sortants**, des e-mails, des SMS et des notifications push, pour une personnalisation plus pertinente.

>[!VIDEO](https://video.tv.adobe.com/v/3484118/?learn=on)
