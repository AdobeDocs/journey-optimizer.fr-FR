---
title: Exemples de mise en oeuvre basés sur le code
description: Cette page présente des exemples de la méthode de mise en oeuvre de la fonctionnalité basée sur le code Journey Optimizer.
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Version Beta"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 17%

---

# Exemples de méthodes de mise en oeuvre basées sur le code {#implementation-samples}

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* [Prise en main du canal basé sur le code](get-started-code-based.md)
* [Conditions préalables basées sur le code](code-based-prerequisites.md)
* **[Exemples de mise en oeuvre basés sur le code](code-based-implementation-samples.md)**
* [Création d’expériences basées sur du code](create-code-based.md)

>[!ENDSHADEBOX]

L’expérience basée sur le code prend en charge n’importe quel type d’implémentation client. Sur cette page, vous trouverez des exemples pour chaque méthode d’implémentation :

* [Côté client](#client-side-implementation)
* [Côté serveur](#server-side-implementation)
* [Hybride](#hybrid-implementation)

Vous pouvez également suivre [ce lien](https://github.com/adobe/alloy-samples/tree/main/ajo){target="_blank"} pour trouver des exemples de mise en oeuvre pour différents cas d’utilisation de personnalisation et d’expérimentation. Consultez-les et exécutez-les afin de mieux comprendre les étapes de mise en oeuvre nécessaires et le fonctionnement du flux de personnalisation de bout en bout.

## Mise en oeuvre côté client {#client-side-implementation}

Si vous disposez d’une mise en oeuvre côté client, vous pouvez utiliser l’un des SDK client AEP : SDK Web AEP ou SDK mobile AEP. Les étapes ci-dessous décrivent le processus de récupération du contenu publié en périphérie par les campagnes d’expérience basées sur le code dans un exemple d’implémentation du SDK Web et l’affichage du contenu personnalisé.

### Fonctionnement

1. [SDK Web](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr){target="_blank"} est inclus dans la page.

1. Vous devez utiliser la variable `sendEvent` et spécifiez l’URI de surface pour récupérer le contenu de personnalisation.

   ```javascript
   alloy("sendEvent", {
   renderDecisions: true,
   personalization: {
       surfaces: ["#sample-json-content"],
   },
   }).then(applyPersonalization("#sample-json-content"));
   ```

1. Les éléments d’expérience basés sur le code doivent être appliqués manuellement par le code d’implémentation (à l’aide de la variable [`applyPersonalization`](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/ajo/personalization-client-side/public/script.js){target="_blank"} ) pour mettre à jour le modèle DOM en fonction de la décision.

1. Pour les campagnes d’expérience basées sur du code, les événements d’affichage doivent être envoyés manuellement pour indiquer le moment où le contenu a été affiché. Cela s’effectue via la commande `sendEvent`.

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

### Principales observations

**Cookies**

Les cookies sont utilisés pour conserver l’identité de l’utilisateur et les informations de cluster. Lors de l’utilisation d’une mise en oeuvre côté client, le SDK Web gère automatiquement le stockage et l’envoi de ces cookies pendant le cycle de vie de la requête.

| Cookie | Rôle | Stocké par | Envoyé par |
| ------------------------ | -------------------------------------------------------------------------- | --------- | ------- |
| kndctr_AdobeOrg_identity | Contient des détails de l’identité de l’utilisateur | SDK Web | SDK Web |
| kndctr_AdobeOrg_cluster | Indique quelle grappe d’expériences doit être utilisée pour répondre aux requêtes. | SDK Web | SDK Web |

**Demander l’emplacement**

Les requêtes envoyées à l’API Adobe Experience Platform sont nécessaires pour obtenir des propositions et envoyer une notification d’affichage. Lors de l’utilisation d’une mise en oeuvre côté client, le SDK Web effectue ces requêtes lorsque la variable `sendEvent` est utilisée.

| Requête | Créée par |
| ---------------------------------------------- | ----------------------------------- |
| requête d’interaction pour obtenir des propositions | SDK web à l’aide de la commande sendEvent |
| demande d’interaction pour envoyer des notifications d’affichage | SDK web à l’aide de la commande sendEvent |

**Diagramme de flux**

![](assets/code-based-client-side-implementation.png)

## Mise en œuvre côté serveur {#server-side-implementation}

Si vous disposez d’une mise en oeuvre côté serveur, vous pouvez utiliser l’une des API réseau AEP Edge. Les étapes ci-dessous décrivent le processus de récupération du contenu publié en périphérie par les campagnes d’expérience basées sur le code dans un exemple d’implémentation de l’API réseau Edge pour une page web et l’affichage du contenu personnalisé.

### Fonctionnement

1. La page web est demandée et tous les cookies précédemment stockés par le navigateur, précédés du préfixe `kndctr_` sont inclus.
1. Lorsque la page est demandée auprès du serveur d’applications, un événement est envoyé au [point d’entrée de la collecte de données interactive](https://experienceleague.adobe.com/docs/experience-platform/edge-network-server-api/data-collection/interactive-data-collection.html?lang=en) pour récupérer du contenu de personnalisation. Cet exemple d’application utilise certaines méthodes d’assistance pour simplifier la création et l’envoi de requêtes à l’API (voir [aepEdgeClient.js](https://github.com/adobe/alloy-samples/blob/ac83b6927d007dc456caad2c6ce0b324c99c26c9/common/aepEdgeClient.js){target="_blank"}). Mais la demande est simplement une `POST` avec un payload contenant un événement et une requête. Les cookies (s’ils sont disponibles) de l’étape précédente sont inclus avec la requête dans la variable `meta>state>entries` tableau.

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

1. L’expérience JSON de la campagne d’expérience basée sur le code est lue à partir de la réponse et utilisée lors de la production de la réponse de HTML.
1. Pour les campagnes d’expérience basées sur du code, les événements d’affichage doivent être envoyés manuellement dans l’implémentation pour indiquer le moment où le contenu de la campagne a été affiché. Dans cet exemple, la notification est envoyée côté serveur pendant le cycle de vie de la requête.

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

Les cookies sont utilisés pour conserver l’identité de l’utilisateur et les informations de cluster. Lors de l’utilisation d’une mise en oeuvre côté serveur, le serveur d’applications doit gérer le stockage et l’envoi de ces cookies pendant le cycle de vie de la demande.

| Cookie | Rôle | Stocké par | Envoyé par |
| ------------------------ | -------------------------------------------------------------------------- | ------------------ | ------------------ |
| kndctr_AdobeOrg_identity | Contient des détails de l’identité de l’utilisateur | serveur applicatif | serveur applicatif |
| kndctr_AdobeOrg_cluster | Indique quelle grappe d’expériences doit être utilisée pour répondre aux requêtes. | serveur applicatif | serveur applicatif |

**Demander l’emplacement**

Les requêtes envoyées à l’API Adobe Experience Platform sont nécessaires pour obtenir des propositions et envoyer une notification d’affichage. Lors de l’utilisation d’une mise en oeuvre côté client, le SDK Web effectue ces requêtes lorsque la variable `sendEvent` est utilisée.

| Requête | Créée par |
| ---------------------------------------------- | ------------------------------------------------------------ |
| requête d’interaction pour obtenir des propositions | serveur d’applications appelant l’API Adobe Experience Platform |
| demande d’interaction pour envoyer des notifications d’affichage | serveur d’applications appelant l’API Adobe Experience Platform |

**Diagramme de flux**

![](assets/code-based-server-side-implementation.png)

## Implémentation hybride {#hybrid-implementation}

Si vous disposez d’une mise en oeuvre hybride, consultez les liens ci-dessous.

* Adobe Tech Blog : [Personnalisation hybride dans le SDK Web de Adobe Experience Platform](https://blog.developer.adobe.com/hybrid-personalization-in-the-adobe-experience-platform-web-sdk-6a1bb674bf41){target="_blank"}
* Documentation du SDK : [Personnalisation hybride à l’aide du SDK Web et de l’API Edge Network Server](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/hybrid-personalization.html){target="_blank"}

