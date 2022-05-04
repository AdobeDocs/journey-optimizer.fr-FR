---
title: Diffuser des offres à l’aide de l’API Edge Decisioning
description: Le SDK web Adobe Experience Platform vous permet de récupérer et de générer des offres personnalisées que vous avez créées à l’aide des API ou de la bibliothèque des offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: 2038cb9d8ffe3048f6f5ab476c164bdc861c1149
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 14%

---

# Diffuser des offres à l’aide de l’API Edge Decisioning {#edge-decisioning-api}

## Prise en main et conditions préalables {#edge-overview-and-prerequisites}

Le [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr#vue-d%E2%80%99ensemble-des-vid%C3%A9os) est une bibliothèque JavaScript côté client qui permet aux clients Adobe Experience Cloud d’interagir avec les différents services de l’Experience Cloud par le biais du réseau Edge Experience Platform.

Le SDK web  Experience Platform prend en charge la demande des solutions de personnalisation auprès d’Adobe, dont la gestion des décisions, ce qui vous permet de récupérer et de générer des offres personnalisées que vous avez créées à l’aide des API ou de la bibliothèque des offres.
Pour des instructions plus détaillées, consultez la documentation sur [créer une offre](../../get-started/starting-offer-decisioning.md).

Il existe deux façons de mettre en oeuvre l’Offer decisioning avec la variable [SDK Web Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). Une méthode est orientée vers les développeurs et nécessite une connaissance des sites web et de la programmation. L’autre méthode consiste à utiliser l’interface utilisateur de Adobe Experience Platform pour configurer des offres qui ne nécessitent qu’un petit script à référencer dans l’en-tête de la page HTML.

Reportez-vous à la documentation relative à la [offer decisioning](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=fr#enabling-offer-decisioning) pour plus d’informations sur la diffusion d’offres personnalisées à l’aide du SDK Web de Platform.

>[!NOTE]
>
>L’utilisation de la gestion des décisions dans le SDK web Adobe Experience Platform est actuellement possible en accès anticipé pour certains utilisateurs.
Cette fonctionnalité n’est pas disponible pour toutes les organisations IMS.

## SDK web Adobe Experience Platform {#aep-web-sdk}

Le SDK Web Platform remplace les SDK suivants :

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

Le SDK n’a pas combiné ces bibliothèques. Il s’agit d’une nouvelle mise en oeuvre de base. Pour l’utiliser, vous devez d’abord suivre les étapes suivantes :

1. Assurez-vous que votre entreprise dispose des autorisations appropriées pour utiliser le SDK et que vous avez correctement configuré les autorisations.

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [Configuration de votre flux de données](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=fr) dans l’onglet Collecte de données de votre compte dans Adobe Experience Cloud.

1. Installation du SDK. Il existe plusieurs méthodes pour ce faire, qui sont décrites dans la section [Installation de la page SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en). Cette page se poursuit avec chaque méthode de mise en oeuvre différente.

Pour utiliser le SDK, vous devez disposer d’un [schema](../../../start/get-started-schemas.md) et un [datastream](../../../start/get-started-datasets.md) définie.

<!-- ****TODO - Configure schema**** -->

Pour personnaliser des offres, vous devez configurer séparément votre/vos profils de personnalisation.

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

Pour configurer le SDK pour Offer Decisioning, procédez comme suit :

## Option 1 - Installation de l’extension et de la mise en oeuvre de Tag à l’aide de Launch

Cette option est plus conviviale pour les personnes qui peuvent avoir moins d’expérience de codage.

1. [Création d’une propriété de balise](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [Ajout du code incorporé de ](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. Installez et configurez l’extension SDK Web Platform avec le Datastream que vous avez créé en sélectionnant la configuration dans la liste déroulante &quot;Datastream&quot;. Consultez la documentation relative à [extensions](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en).

   ![SDK web Adobe Experience Platform](../../assets/installed-catalog-web-sdk.png)

   ![Configurer l’extension](../../assets/configure-sdk-extension.png)

1. Créez les [Éléments de données](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en). Au minimum, vous devez créer une carte d’identité SDK Web Platform et un élément de données XDM d’objet SDK Web Platform.

   ![Mappage d’identités](../../assets/sdk-identity-map.png)

   ![Objet XDM](../../assets/xdm-object.png)

1. Créez votre [Règles](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en):

   Ajoutez une action Envoyer l’événement du SDK Web Platform et ajoutez les étendues de décision appropriées à la configuration de cette action.

   ![Offre de rendu](../../assets/rule-render-offer.png)

   ![Demander l’offre](../../assets/rule-request-offer.png)

1. [Créer et publier](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) une bibliothèque contenant toutes les règles, éléments de données et extensions que vous avez configurés.

## Option 2 - Mise en oeuvre manuelle à l’aide de la version autonome préconfigurée

Voici les étapes nécessaires à l’utilisation d’Offer Decisioning à l’aide de l’installation autonome prédéfinie du SDK web. Ce guide suppose qu’il s’agit de la première mise en oeuvre du SDK. Il se peut donc que toutes les étapes ne vous soient pas applicables. Ce guide suppose également une expérience de développement.

Incluez le fragment de code JavaScript suivant de l’option 2 : La version autonome prédéfinie sur [cette page](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) dans le `<head>` de votre page de HTML.

```
javascript
    <script>
        !function(n,o){o.forEach(function(o){n[o]||((n.__alloyNS=n.__alloyNS||
        []).push(o),n[o]=function(){var u=arguments;return new Promise(
        function(i,l){n[o].q.push([i,l,u])})},n[o].q=[])})}
        (window,["alloy"]);
    </script>
    <script src="https://cdn1.adoberesources.net/alloy/2.6.4/alloy.js" async></script>
```

Vous aurez besoin de deux ID depuis votre compte Adobe pour configurer la configuration du SDK : votre edgeConfigId et votre orgId. edgeConfigId est le même que votre identifiant de flux de données, que vous devez avoir configuré dans les Conditions préalables.

Pour trouver votre edgeConfigID/datastream ID, accédez à Collecte de données et sélectionnez votre Datastream. Pour trouver votre orgId, accédez à votre profil.

Configurez le SDK dans JavaScript en suivant les instructions de cette page. Vous utiliserez toujours vos edgeConfigId et orgId dans la fonction de configuration. La documentation décrit également les paramètres facultatifs qui existent pour votre configuration. Votre configuration finale peut se présenter comme suit :

```
javascript
    alloy("configure", {
        "edgeConfigId": "12345678-0ABC-DEF-GHIJ-KLMNOPQRSTUV",                            
        "orgId":"ABCDEFGHIJKLMNOPQRSTUVW@AdobeOrg",
        "debugEnabled": true,
        "edgeDomain": "edge.adobedc.net",
        "clickCollectionEnabled": true,
        "idMigrationEnabled": true,
        "thirdPartyCookiesEnabled": true,
        "defaultConsent":"in"  
    });
```

Installez l’extension Chrome Debugger à utiliser avec le débogage. On peut le trouver ici : <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

Ensuite, connectez-vous à votre compte dans le débogueur. Ensuite, accédez à Journaux et vérifiez que vous êtes connecté à l’espace de travail approprié. Copiez maintenant la version codée en base64 de la portée de décision de votre offre.

Lorsque vous modifiez votre site web, incluez le script avec la configuration et la variable `sendEvent` pour envoyer la portée de la décision à l’Adobe.

**Exemple**:

```
javascript
    alloy("sendEvent", {
        "decisionScopes": 
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    });
```

Consultez l’exemple suivant pour savoir comment gérer la réponse :

```
javascript
    alloy("sendEvent", {
        "decisionScopes":
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    }).then(function(result) {
        Object.entries(result).forEach(([key, value]) => {
            console.log(key, value);
        });
    });
```

Vous pouvez utiliser le débogueur pour vérifier que vous êtes bien connecté au réseau Edge.

>[!NOTE]
>
>Si vous ne voyez pas de connexion à la périphérie dans les journaux, vous devrez peut-être désactiver le bloqueur d’annonces publicitaires.

Reportez-vous à la façon dont vous avez créé votre offre et au formatage utilisé. Selon les critères satisfaits dans la décision, une offre vous sera renvoyée, contenant les informations que vous avez spécifiées lors de sa création dans Adobe Experience Platform.

Dans cet exemple, le JSON à renvoyer est :

```
json
{
   "name":"ABC Test",
   "description":"This is a test offer", 
   "link":"https://sampletesting.online/",
   "image":"https://sample-demo-URL.png"
}
```

Gérez l’objet de réponse et analysez les données dont vous avez besoin. Comme vous pouvez envoyer plusieurs portées de décision en une seule `sendEvent` , votre réponse peut paraître légèrement différente.

```
json
    {
        "id": "abrxgl843d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"ABC Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
]
}
```

```
json
{
    "propositions": 
    [
    {
        "renderAttempted": false,
        "id": "e15ecb09-993e-4b66-93d8-0a4c77e3d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"Claire Hubacek Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
    ]
}
```

Dans cet exemple, le chemin d’accès nécessaire pour gérer et utiliser les détails spécifiques à l’offre dans la page web était : `result['decisions'][0]['items'][0]['data']['content']`

Pour définir les variables JS :

```
javascript
const offer = JSON.parse(result['decisions'][0]['items'][0]['data']['content']);

let offerURL = offer['link'];
let offerDescription = offer['description'];
let offerImageURL = offer['image'];

document.getElementById("offerDescription").innerHTML = offerDescription;
document.getElementById('offerImage').src = offerImageURL;
```

## Limites

Certaines contraintes d’offre ne sont actuellement pas prises en charge avec les workflows Experience Edge mobiles, par exemple la limitation. La valeur du champ de limitation indique le nombre de fois où une offre peut être présentée à tous les utilisateurs. Pour plus d’informations, voir [Ajouter des contraintes à une offre](../../offer-library/add-constraints.md#capping).
