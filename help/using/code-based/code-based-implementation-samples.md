---
title: Exemples de mises en œuvre basées sur le code
description: Cette page présente des exemples de la méthode de mise en œuvre de la fonctionnalité basée sur le code Journey Optimizer.
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
exl-id: e5ae8b4e-7cd2-4a1d-b2c0-8dafd5c4cdfd
source-git-commit: 30241f4504ad82bf8ef9f6b58d3bb9482f572dae
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 81%

---

# Exemples de méthodes de mise en œuvre basées sur le code {#implementation-samples}

L’expérience basée sur le code est compatible avec n’importe quelle mise en œuvre du client ou de la cliente. Sur cette page, vous trouverez des exemples pour chaque méthode de mise en œuvre :

* [Côté client](#client-side-implementation)
* [Côté serveur](#server-side-implementation)
* [Hybride](#hybrid-implementation)

>[!IMPORTANT]
>
>Suivez [ce lien](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} pour trouver des exemples de mise en œuvre pour différents cas de personnalisation et d’expérimentation. Consultez-les et exécutez-les afin de mieux comprendre les étapes de mise en œuvre nécessaires et le fonctionnement du flux de personnalisation de bout en bout.

➡️ Pour en savoir plus sur la configuration du SDK web pour les expériences et la prise de décision basées sur du code, consultez [ces tutoriels](code-based-decisioning-implementations.md#tutorials).

## Mise en œuvre côté client {#client-side-implementation}

Si vous disposez d’une implémentation côté client, vous pouvez utiliser l’un des SDK AEP client : SDK AEP Web ou SDK AEP Mobile.

* Les étapes [ci-dessous](#client-side-how) décrivent le processus de récupération du contenu publié en périphérie par les campagnes et parcours d’expériences basées sur du code dans un exemple d’implémentation du **SDK Web** et de l’affichage du contenu personnalisé.

* Les étapes d’implémentation du canal basé sur du code à l’aide du **SDK mobile** sont décrites dans [ce tutoriel](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"}.

  >[!NOTE]
  >
  >Des exemples d’implémentation pour des cas d’utilisation mobiles sont disponibles dans l’[application iOS](https://github.com/adobe/aepsdk-messaging-ios/tree/main/TestApps/MessagingDemoAppSwiftUI){target="_blank"} et l’[application Android](https://github.com/adobe/aepsdk-messaging-android/tree/main/code/testapp){target="_blank"}.

### Fonctionnement - SDK Web {#client-side-how}

1. Le [SDK web](https://experienceleague.adobe.com/fr/docs/experience-platform/collection/home){target="_blank"} est inclus dans la page.

1. Vous devez utiliser la commande `sendEvent` et spécifier l’[URI de surface](code-based-surface.md)<!--( or location/path)--> pour récupérer le contenu de personnalisation.

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. Les éléments d’expériences basées sur du code doivent être appliqués manuellement par le code de mise en œuvre (à l’aide de la méthode [`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"}) pour mettre à jour le modèle DOM en fonction de la décision.

1. Pour les campagnes et parcours d’expériences basées sur du code, les événements d’affichage doivent être envoyés manuellement pour indiquer le moment où le contenu a été affiché. Cela s’effectue via la commande `sendEvent`.

   ```javascript
   function sendDisplayEvent(decision) {
     const { id, scope, scopeDetails = {} } = decision;
   
     alloy("sendEvent", {
   
       xdm: {
         eventType: "decisioning.propositionDisplay",
         _experience: {
           decisioning: {
             propositions: [
               {
                 id: id,
                 scope: scope,
                 scopeDetails: scopeDetails,
               },
             ],
           },
         },
       },
     });
   }
   ```

1. Pour les campagnes et parcours d’expériences basées sur du code, les événements d’interaction doivent être envoyés manuellement pour indiquer le moment où un utilisateur ou une utilisatrice a interagi avec le contenu. Cela s’effectue via la commande `sendEvent`.

   ```javascript
   function sendInteractEvent(label, proposition) {
     const { id, scope, scopeDetails = {} } = proposition;
   
     alloy("sendEvent", {
   
       xdm: {
         eventType: "decisioning.propositionInteract",
         _experience: {
           decisioning: {
             propositions: [
               {
                 id: id,
                 scope: scope,
                 scopeDetails: scopeDetails,
               },
             ],
             propositionEventType: {
               interact: 1
             },
             propositionAction: {
               id: label,
               label: label,
               tokens: proposition.items?.[0]?.characteristics?.tokens || []
             },
           },
         },
       },
     });
   }
   ```

   >[!IMPORTANT]
   >
   >Le champ `tokens` dans `propositionAction` est essentiel pour le suivi et l’attribution précis dans Adobe Journey Optimizer Decisioning (AJO-D). Ces jetons permettent :
   >- Attribution des clics appropriée pour les activités de prise de décision
   >- Création de rapports précis sur les interactions utilisateur avec du contenu décisionnel
   >- Optimisation des performances des offres en fonction de l’interaction client
   >
   >Les jetons se trouvent généralement dans `proposition.items[0].characteristics.tokens` et doivent toujours être inclus lors du suivi des interactions des utilisateurs avec le contenu décidé.

### Principales observations

**Cookies**

Les cookies sont utilisés pour conserver l’identité de l’utilisateur ou de l’utilisatrice et les informations de cluster. Lors de l’utilisation d’une mise en œuvre côté client, le SDK Web gère le stockage et l’envoi automatiques de ces cookies pendant le cycle de vie des requêtes.

| Cookie | Rôle | Stocké par | Envoyé par |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kndctr_AdobeOrg_identity | Contient des détails de l’identité de l’utilisateur ou de l’utilisatrice | SDK Web | SDK Web |
| kndctr_AdobeOrg_cluster | Indique quel cluster Edge d’expérience doit être utilisé pour répondre aux requêtes | SDK Web | SDK Web |

**Demander l’emplacement**

Les requêtes envoyées à l’API Adobe Experience Platform sont nécessaires pour obtenir des propositions et envoyer une notification d’affichage. Lors de l’utilisation d’une mise en œuvre côté client, le SDK Web effectue ces requêtes lorsque la commande `sendEvent` est utilisée.

| Requête | Créée par |
| ---------------------------------------------- | ----------------------------------- |
| requête d’interaction pour obtenir des propositions | SDK Web utilisant la commande sendEvent |
| requête d’interaction pour envoyer des notifications d’affichage | SDK Web utilisant la commande sendEvent |

**Diagramme de flux**

![](assets/code-based-client-side-implementation.png)

## Mise en œuvre côté serveur {#server-side-implementation}

Si vous disposez d’une implémentation côté serveur, vous pouvez utiliser l’une des API AEP Edge Network.

Les étapes ci-dessous décrivent le processus de récupération du contenu publié en périphérie par les campagnes et parcours d’expériences basées sur du code dans un exemple de mise en œuvre de l’API Edge Network pour une page web et de l’affichage du contenu personnalisé.

### Fonctionnement

1. La page web est demandée et tous les cookies précédemment stockés par le navigateur, précédés du préfixe `kndctr_`, sont inclus.
1. Lorsque la page est demandée auprès du serveur d’applications, un événement est envoyé au [point d’entrée de la collecte de données interactive](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=fr) pour récupérer du contenu de personnalisation. Cet exemple d’application utilise des méthodes d’assistance pour simplifier la création et l’envoi de requêtes à l’API (voir [aepEdgeClient.js](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js){target="_blank"}). Mais la requête est simplement un `POST` avec une payload contenant un événement et une requête. Les cookies (s’ils sont disponibles) de l’étape précédente sont inclus avec la requête dans le tableau `meta>state>entries`.

   ```javascript
   fetch(
     "https://edge.adobedc.net/ee/v2/interact?dataStreamId=abc&requestId=123",
     {
       headers: {
         accept: "*/*",
         "accept-language": "en-US,en;q=0.9",
         "cache-control": "no-cache",
         "content-type": "text/plain; charset=UTF-8",
         pragma: "no-cache",
         "sec-fetch-dest": "empty",
         "sec-fetch-mode": "cors",
         "sec-fetch-site": "cross-site",
         "sec-gpc": "1",
         "Referrer-Policy": "strict-origin-when-cross-origin",
         Referer: "https://localhost/",
       },
       body: JSON.stringify({
         event: {
           xdm: {
             eventType: "decisioning.propositionFetch",
             web: {
               webPageDetails: {
                 URL: "https://localhost/",
               },
               webReferrer: {
                 URL: "",
               },
             },
             identityMap: {
               FPID: [
                 {
                   id: "xyz",
                   authenticatedState: "ambiguous",
                   primary: true,
                 },
               ],
             },
             timestamp: "2022-06-23T22:21:00.878Z",
           },
           data: {},
         },
         query: {
           identity: {
             fetch: ["ECID"],
           },
           personalization: {
             schemas: [
               "https://ns.adobe.com/personalization/default-content-item",
               "https://ns.adobe.com/personalization/html-content-item",
               "https://ns.adobe.com/personalization/json-content-item",
               "https://ns.adobe.com/personalization/redirect-item",
               "https://ns.adobe.com/personalization/dom-action",
             ],
             surfaces: ["web://localhost/","web://localhost/#sample-json-content"],
           },
         },
         meta: {
           state: {
             domain: "localhost",
             cookiesEnabled: true,
             entries: [
               {
                 key: "kndctr_XXX_AdobeOrg_identity",
                 value: "abc123",
               },
               {
                 key: "kndctr_XXX_AdobeOrg_cluster",
                 value: "or2",
               },
             ],
           },
         },
       }),
       method: "POST",
     }
   ).then((res) => res.json());
   ```

1. L’expérience JSON de la campagne et du parcours d’expériences basées sur le code est lue à partir de la réponse et utilisée lors de la production de la réponse HTML.

1. Pour les campagnes et parcours d’expériences basées sur le code, les événements d’affichage doivent être envoyés manuellement dans la mise en œuvre pour indiquer le moment où le contenu du parcours ou de la campagne a été affiché. Dans cet exemple, la notification est envoyée côté serveur, pendant le cycle de vie de la requête.

   ```javascript
   function sendDisplayEvent(aepEdgeClient, req, propositions, cookieEntries) {
     const address = getAddress(req);
   
     aepEdgeClient.interact(
       {
         event: {
           xdm: {
             web: {
               webPageDetails: { URL: address },
               webReferrer: { URL: "" },
             },
             timestamp: new Date().toISOString(),
             eventType: "decisioning.propositionDisplay",
             _experience: {
               decisioning: {
                 propositions: propositions.map((proposition) => {
                   const { id, scope, scopeDetails } = proposition;
   
                   return {
                     id,
                     scope,
                     scopeDetails,
                   };
                 }),
               },
             },
           },
         },
         query: { identity: { fetch: ["ECID"] } },
         meta: {
           state: {
             domain: "",
             cookiesEnabled: true,
             entries: [...cookieEntries],
           },
         },
       },
       {
         Referer: address,
       }
     );
   }
   ```

1. Lorsque la réponse HTML est renvoyée, les cookies d’identité et de cluster sont définis sur la réponse par le serveur d’applications.

### Principales observations

**Cookies**

Les cookies sont utilisés pour conserver l’identité de l’utilisateur ou de l’utilisatrice et les informations de cluster. Lors de l’utilisation d’une mise en œuvre côté serveur, le serveur d’applications doit gérer le stockage et l’envoi de ces cookies pendant le cycle de vie des requêtes.

| Cookie | Rôle | Stocké par | Envoyé par |
| ------------------------ | -------------------------------------------------------------------------- | ------------------ | ------------------ |
| kndctr_AdobeOrg_identity | Contient des détails de l’identité de l’utilisateur ou de l’utilisatrice | serveur d’applications | serveur d’applications |
| kndctr_AdobeOrg_cluster | Indique quel cluster Edge d’expérience doit être utilisé pour répondre aux requêtes | serveur d’applications | serveur d’applications |

**Emplacement de la requête**

Les requêtes envoyées à l’API Adobe Experience Platform sont nécessaires pour obtenir des propositions et envoyer une notification d’affichage. Lors de l’utilisation d’une mise en œuvre côté client, le SDK Web effectue ces requêtes lorsque la commande `sendEvent` est utilisée.

| Requête | Créée par |
| ---------------------------------------------- | ------------------------------------------------------------ |
| requête d’interaction pour obtenir des propositions | serveur d’applications appelant l’API Adobe Experience Platform |
| requête d’interaction pour envoyer des notifications d’affichage | serveur d’applications appelant l’API Adobe Experience Platform |

**Diagramme de flux**

![](assets/code-based-server-side-implementation.png)

## Implémentation hybride {#hybrid-implementation}

Si vous disposez d’une mise en œuvre hybride, consultez les liens ci-dessous.

* Blog sur les technologies Adobe : [Personnalisation hybride dans le SDK web d’Adobe Experience Platform](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}
* Documentation SDK : [Personnalisation hybride à l’aide du SDK web et de l’API Edge Network Server](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html?lang=fr){target="_blank"}

## Déboguer les appels d’API réseau d’Edge avec Adobe Experience Platform Assurance {#debugging-edge-api-assurance}

Lors de l’utilisation directe de l’API Edge Network pour les expériences basées sur le code (sans utiliser Web SDK ou Mobile SDK), vous pouvez déboguer vos appels API avec Adobe Experience Platform Assurance en incluant l’ID de session Assurance comme en-tête de jeton de validation.

1. Obtenez votre ID de session Assurance à partir d’une session Adobe Experience Platform Assurance active ou créez-en un à l’aide de l’API Assurance.

1. Ajoutez l’en-tête `x-adobe-aep-validation-token` avec votre ID de session Assurance pour acheminer vos requêtes API Edge Network via la session Assurance.

   **Exemple :**

   ```bash
   curl -v 'https://edge.adobedc.net/ee/v1/interact?configId={DATASTREAM_ID}&requestId={REQUEST_ID}' \
   --header 'Content-Type: application/json' \
   --header 'x-adobe-aep-validation-token: {ASSURANCE_SESSION_ID}' \
   --data-raw '{
       "xdm": {
         "identityMap": {
               "ECID": [
                   {
                       "id": "{ECID_VALUE}"
                   }
               ]
           }
       },
       "events": [
           {
               "xdm": {
                   "eventType": "test",
                   "timestamp": "{TIMESTAMP}"
               }
           }
       ]
   }'
   ```

1. Une fois la configuration effectuée, ouvrez votre session Assurance et sélectionnez la vue **[!UICONTROL Edge Delivery]** pour afficher les requêtes et les réponses de l’API Edge Network en temps réel, y compris les payloads de la requête, le contenu de la réponse, les propositions de personnalisation et les messages d’erreur.


<!--
## Implementation guides and tutorials {#implementation-guides}

To help you get started with implementing code-based experiences, refer to the comprehensive step-by-step tutorials below:

* **Mobile SDK implementation**: Follow [this tutorial](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/code-based/tutorial/){target="_blank"} to learn how to set up code-based experiences on mobile apps using the Adobe Experience Platform Mobile SDK.

* **Web SDK implementation**: Learn how to configure the Web SDK for decisioning and code-based experiences in [these tutorials](code-based-decisioning-implementations.md#tutorials).

* **Decisioning implementation**: To learn how to implement decisioning capabilities on a code-based campaign, follow [this use case tutorial](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/experience-decisioning/experience-decisioning-uc){target="_blank"}.-->
