---
title: Création d’expériences de canal personnalisé
description: Découvrez comment utiliser un canal personnalisé dans un parcours, une campagne ou une campagne orchestrée dans Adobe Journey Optimizer.
feature: Channel Configuration
topic: Content Management
role: User
level: Experienced
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 9%

---


# Création d’expériences de canal personnalisé {#create-custom-channel}

>[!AVAILABILITY]
>
>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en bénéficier.

Dans [!DNL Journey Optimizer], vous pouvez diffuser des messages à l’aide de canaux personnalisés dans les campagnes, les parcours et les campagnes orchestrées. Suivez les étapes ci-dessous pour configurer votre expérience de canal personnalisé.

>[!NOTE]
>
>Avant de créer une expérience de canal personnalisé, assurez-vous qu’un canal personnalisé a été configuré par votre administrateur. [En savoir plus](configure-custom-channel.md)

## Ajout d’une action personnalisée par le biais d’un parcours ou d’une campagne {#create-custom-channel-experience}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_channel"
>title="Action de canal personnalisée"
>abstract="Une action de canal personnalisée diffuse un message aux profils lorsqu’ils atteignent cette étape du parcours. Le libellé identifie l’activité dans la zone de travail de parcours et l’action fait référence à une configuration de canal personnalisée qui définit le point d’entrée, la payload et les informations d’identification utilisés pour diffuser le message. La section **Optimisation** peut inclure des expériences de contenu ou des règles de ciblage, et la section **Temporisation ou erreur** peut définir un autre chemin d’accès en cas d’échec de l’action."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/orchestrate-journeys/about-journey-building/journey-action#add-action" text="Commencer avec les canaux personnalisés"



>[!BEGINTABS]

>[!TAB Ajouter un canal personnalisé à un parcours ]

Les canaux personnalisés apparaissent dans la section **[!UICONTROL Actions]** de la palette Zone de travail de parcours, répertoriés par leur nom d’affichage et leur icône personnalisée, tels que définis dans le Créateur de canaux.

Pour ajouter une action de canal personnalisée à un parcours :

1. [Créez un parcours](../building-journeys/journey-gs.md).

1. Débutez votre parcours avec une activité [Événement](../building-journeys/general-events.md) ou [Lecture d’audience](../building-journeys/read-audience.md).

1. Effectuez un glisser-déposer d&#39;une activité **[!UICONTROL Action]** depuis la section **[!UICONTROL Actions]** de la palette. En savoir plus sur l’activité [Action](../building-journeys/journey-action.md).

1. Dans la liste déroulante **[!UICONTROL Action]**, sélectionnez le canal personnalisé que vous souhaitez utiliser. Les canaux personnalisés sont répertoriés par le nom et l’icône attribués dans le Créateur de canaux.

   ![](assets/custom_channel_journey_action.png){width="80%"}

1. Ajoutez un libellé à votre action, cliquez sur **[!DNL Configure action]** dans le panneau de droite, puis sélectionnez la **[!UICONTROL configuration du canal]** à utiliser. [Découvrez comment créer une configuration de canal personnalisée](custom-channel-configuration.md#create-channel-config)

1. Dans la section **[!UICONTROL Message]**, cliquez sur **[!UICONTROL Modifier le contenu]** pour ouvrir l’éditeur de payload et créer votre message. [Découvrez comment créer du contenu](#author-content)

1. Complétez votre flux de parcours en ajoutant des étapes supplémentaires si nécessaire, puis publiez le parcours. [En savoir plus](../building-journeys/journey-gs.md)

>[!TAB Créer une campagne de canal personnalisée]

Pour utiliser un canal personnalisé dans une campagne :

1. [Créer une campagne](../campaigns/create-campaign.md).

1. Sélectionnez le type de campagne :

   * **[!UICONTROL Planifié - Marketing]** - Exécuté immédiatement ou à une date spécifiée. Conçu pour les messages marketing, configuré à partir de l’interface utilisateur.
   * **[!UICONTROL Déclenché par API - Marketing/Transactionnel]** - Exécuté via un appel API. Conçu pour la messagerie déclenchée par un événement (par exemple, les confirmations de commande ou les réinitialisations de mot de passe). [En savoir plus](../campaigns/api-triggered-campaigns.md)

1. Terminez la configuration de la campagne : propriétés de la campagne, [audience](../audience/about-audiences.md) et [planning](../campaigns/create-campaign.md#schedule).

1. Dans la section **[!UICONTROL Actions]**, sélectionnez le canal personnalisé à partir du sélecteur de canaux. Tous les canaux personnalisés configurés sur votre sandbox apparaissent à côté des canaux natifs.

   ![](assets/custom_channel_campaign_action.png){width="80%"}

1. Sélectionnez ou créez la **[!UICONTROL configuration de canal]** à utiliser. [Découvrez comment créer une configuration de canal](custom-channel-configuration.md#create-channel-config)

1. Vous pouvez éventuellement activer le **[!UICONTROL Suivi des actions]** pour suivre automatiquement les liens inclus dans la payload de votre message (nécessite un sous-domaine configuré pour les canaux personnalisés). [Découvrez comment déléguer un sous-domaine pour les canaux personnalisés](custom-channel-subdomains.md#subdomain-delegation)

1. Dans la section **[!UICONTROL Optimisation]**, vous pouvez :

   * **[!UICONTROL Créez des règles de ciblage]** pour envoyer différents messages à différents segments de votre audience. [En savoir plus](../campaigns/create-campaign.md#targeting)
   * Cliquez sur **[!UICONTROL Créer une expérience]** pour exécuter des tests A/B sur vos messages de canal personnalisés. [En savoir plus](../campaigns/create-campaign.md#content-experiment)

1. Cliquez sur **[!UICONTROL Modifier le contenu]** pour ouvrir l’éditeur de payload et créer votre message. [Découvrez comment créer du contenu](#author-content)

1. Examinez et activez la campagne. [En savoir plus](../campaigns/create-campaign.md)

<!--
>[!TAB Add a custom channel to an orchestrated campaign]

Custom channels appear in the channel selection list in the orchestrated Campaigns canvas, below the native channels, with their custom icon and display name.

To add a custom channel in an orchestrated campaign:

1. Open or create an orchestrated campaign.

1. In the canvas, add a channel action node and select your custom channel from the list.

1. Select the **[!UICONTROL Channel configuration]** to use. Ensure the configuration includes the **[!UICONTROL Execution details]** section required for orchestrated campaigns.

1. Click **[!UICONTROL Edit content]** to open the payload editor and author your message. [Learn how to author content](#author-content)
-->

>[!ENDTABS]

## Créer le contenu de votre canal personnalisé {#author-content}

L’éditeur de contenu reflète la structure de payload que vous avez définie lors de la configuration du canal personnalisé. Cliquez sur **[!UICONTROL Modifier le code]** pour ouvrir l’éditeur de payload et saisissez le contenu de votre message.

![](assets/custom_channel_payload_editor.png){width="80%"}

Les champs que vous pouvez créer et personnaliser s’affichent. Vous pouvez utiliser l’éditeur de personnalisation de [!DNL Journey Optimizer] et toutes ses fonctionnalités de personnalisation et de création. [En savoir plus](../personalization/personalization-build-expressions.md)

>[!NOTE]
>
>Seules les payloads JSON sont prises en charge. Si la payload de votre canal personnalisé n’est pas de type JSON, vous pouvez utiliser un wrapper JSON pour encapsuler votre contenu. Par exemple, si votre payload est XML, vous pouvez l’encapsuler dans un objet JSON comme suit :
>
>```json
>{
>   "payload": "<xml>...</xml>"
>}
>```

### Personnalisation de la payload {#personalize}

Les fonctionnalités complètes de personnalisation de [!DNL Journey Optimizer] sont disponibles dans l’éditeur de payload :

* **Attributs de profil** - Injectez un attribut de profil XDM, tel qu’`{{profile.person.name.firstName}}` ou une identité personnalisée telle qu’un identifiant utilisateur de plateforme de messagerie stocké dans un espace de noms personnalisé.
* **Attributs contextuels** - Utilisez des attributs d’événement de parcours ou des données contextuelles de campagne résolus au moment de l’envoi.
* **Fonctions helper** - Formatez les valeurs à l’aide de fonctions de chaîne, de date ou arithmétiques intégrées. [En savoir plus](../personalization/functions/helpers.md)
* **Fragments d’expression** - Réutilisez la logique de personnalisation partagée sur plusieurs canaux et campagnes. [En savoir plus](../content-management/customizable-fragments.md)

>[!CAUTION]
>
>Actuellement, la payload n’est pas validée au moment de la création. Vous pouvez utiliser la fonction **[!UICONTROL Simuler du contenu]** pour vérifier que la payload est au format JSON et que toutes les expressions de personnalisation sont correctement résolues pour vos profils de test. [En savoir plus](test-custom-channel.md#simulate-content)

### Exemple de payload {#example-payload}

L’exemple suivant illustre une payload JSON avec la personnalisation de profil pour un canal de messagerie personnalisé <!--(to be replaced with a meaningful realistic example)--> :

```json
{
  "recipient_id": "{{profile.mobilePhone.number}}",
  "message_text": "Hello {{profile.person.name.firstName}}, your order {{context.journey.events.0.commerce.order.purchaseID}} has been confirmed.",
  "channel": "my-custom-channel",
  "image": {
    "id": "{{profile.preferences.imageId | default('default-image-001')}}"
  }
}
```

### Suivi des liens dans la payload {#track-links}

Pour inclure un lien suivi dans la payload de votre canal personnalisé (de sorte que les clics soient automatiquement suivis et visibles dans les tableaux de bord de rapports du canal), encapsulez l’URL à l’aide de la syntaxe de barre de contrôle suivante :

```
{{url trackedUrl='' originalUrl='https://example.com/' type='TRACKED'}}
```

* `originalUrl` - URL de destination vers laquelle vous souhaitez rediriger le destinataire.
* `trackedUrl` - Laissez ce champ vide ; [!DNL Journey Optimizer] le renseigne automatiquement avec l’URL de redirection compatible avec le tracking au moment de l’envoi.
* `type` - Doit être défini sur `TRACKED`.

>[!NOTE]
>
>Le suivi des liens nécessite un sous-domaine configuré pour les canaux personnalisés. [Découvrez comment déléguer un sous-domaine pour les canaux personnalisés](custom-channel-subdomains.md#subdomain-delegation)

**Exemple - Lien suivi dans une payload LINE :**

```json
{
  "to": "{{profile.mobilePhone.number}}",
  "messages": [
    {
      "type": "text",
      "text": "Hello! Check out our latest offer: {{url trackedUrl='' originalUrl='https://example.com/' type='TRACKED'}}"
    }
  ]
}
```

<!--
### Strict JSON mode {#strict-json}

The editor supports a **[!UICONTROL Strict JSON]** toggle:

* **Strict JSON: Off (default)** – The editor accepts any payload content, including personalization helpers and functions that may temporarily produce non-JSON syntax. A warning is displayed at the **Review to Activate** step if the payload is not well-formed JSON, prompting you to simulate and proof before publishing.
* **Strict JSON: On** – The editor validates that the payload is well-formed JSON as you type. At the **Review to Activate** step, [!DNL Journey Optimizer] validates the payload against the channel schema and flags missing required fields or type mismatches as errors that must be resolved before activation.
-->

## Activer votre expérience de canal personnalisé {#activate}

>[!IMPORTANT]
>
>Prévisualisez et testez la payload de votre canal personnalisé avant l’activation. [Voici comment procéder](test-custom-channel.md)
>
>Si votre campagne ou parcours est soumis à une politique de validation, vous devez demander une validation avant l’activation. [En savoir plus](../test-approve/gs-approval.md)

* **À partir d’un parcours** - Cliquez sur **[!UICONTROL Publier]** dans la zone supérieure droite. Le parcours est activé et commence à appeler votre point d’entrée externe pour les profils admissibles.
* **À partir d’une campagne** - Cliquez sur **[!UICONTROL Vérifier pour activer]**, vérifiez vos paramètres, puis cliquez sur **[!UICONTROL Activer]**. La campagne adopte le statut **[!UICONTROL Actif]** (ou **[!UICONTROL Planifié]** si une date de début ultérieure a été définie).
