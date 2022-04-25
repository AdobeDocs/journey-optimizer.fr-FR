---
title: Diffuser des offres à l’aide de l’API Edge Decisioning
description: Le SDK web Adobe Experience Platform vous permet de récupérer et de générer des offres personnalisées que vous avez créées à l’aide des API ou de la bibliothèque des offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: b02981f2c0cf74c8dba657570157709bc422d94c
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 21%

---


# Diffuser des offres à l’aide de l’API Edge Decisioning {#edge-decisioning-api}

## Prise en main et conditions préalables {#aep-web-sdk-overview-and-prerequisites}

Le [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr#vue-d%E2%80%99ensemble-des-vid%C3%A9os) est une bibliothèque JavaScript côté client qui permet aux clients Adobe Experience Cloud d’interagir avec les différents services de l’Experience Cloud par le biais du réseau Edge Experience Platform.

Le SDK web  Experience Platform prend en charge la demande des solutions de personnalisation auprès d’Adobe, dont la gestion des décisions, ce qui vous permet de récupérer et de générer des offres personnalisées que vous avez créées à l’aide des API ou de la bibliothèque des offres.
Pour des instructions plus détaillées, consultez la documentation sur [créer une offre](../../get-started/starting-offer-decisioning.md).

Il existe deux façons de mettre en oeuvre l’Offer decisioning avec la variable [SDK Web Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). Une méthode est orientée vers les développeurs et nécessite une connaissance des sites web et de la programmation. L’autre méthode consiste à utiliser l’interface utilisateur de Adobe Experience Platform pour configurer des offres qui ne nécessitent qu’un petit script à référencer dans l’en-tête de la page HTML.

Reportez-vous à la documentation relative à la [offer decisioning](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=fr#enabling-offer-decisioning) pour plus d’informations sur la diffusion d’offres personnalisées à l’aide du SDK Web de Platform.

>[!NOTE]
>
>L’utilisation de la gestion des décisions dans le SDK web Adobe Experience Platform est actuellement possible en accès anticipé pour certains utilisateurs.
Cette fonctionnalité n’est pas disponible pour toutes les organisations IMS.

## SDK web Adobe Experience Platform  {#aep-web-sdk-overview-and-prerequisites}

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


## Limites

Certaines contraintes d’offre ne sont actuellement pas prises en charge avec les workflows Experience Edge mobiles, par exemple la limitation. La valeur du champ de limitation indique le nombre de fois où une offre peut être présentée à tous les utilisateurs. Pour plus d’informations, voir [Ajouter des contraintes à une offre](../../offer-library/add-constraints.md#capping).
