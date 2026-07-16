---
title: Commencer avec les canaux personnalisés
description: Découvrez comment l [!DNL Journey Optimizer]'s Channel Builder to bring any outbound messaging channel into [!DNL Journey Optimizer] utiliser et l’utiliser dans des campagnes, des parcours et des campagnes orchestrées.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 5%

---


# Commencer avec les canaux personnalisés {#get-started-custom-channel}

>[!AVAILABILITY]
>
>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en bénéficier.

<!--Multilingual support, business rules enforcement, and [!DNL Adobe Experience Decisioning] integration are planned for a future release.-->

La fonctionnalité **Canaux personnalisés** de [!DNL Journey Optimizer] vous permet d’importer n’importe quel canal sortant dans [!DNL Journey Optimizer] afin de l’utiliser dans des campagnes, des parcours et des campagnes orchestrées, comme tout canal natif. Grâce au **Channel Builder**, les administrateurs peuvent créer et configurer de nouveaux canaux sans intervention de l’ingénierie, et les spécialistes marketing peuvent immédiatement commencer à les utiliser pour communiquer avec les clients.

## Quel problème cela résout-il ? {#why-custom-channels}

[!DNL Journey Optimizer] prend en charge de manière native les e-mails, SMS, notifications push, WhatsApp, LINE et d’autres canaux. Cependant, de nombreuses entreprises utilisent des plateformes de messagerie qui ne sont pas intégrées nativement (telles que WeChat, Kakao Talk, Messenger ou un fournisseur externe) et souhaitent les utiliser en [!DNL Journey Optimizer] pour l’orchestration et la création de campagnes tout en continuant à fournir des services avec leur propre fournisseur.

<!--TBC: Another use case is when organizations have a legacy messaging gateway that exposes an HTTP endpoint, and they want to use it in [!DNL Journey Optimizer] without having to build a custom integration.-->

Les canaux personnalisés comblent ce vide : ils vous permettent d’utiliser n’importe quel point d’entrée HTTP sortant en tant que canal [!DNL Journey Optimizer] complet, en déverrouillant :

* **Fonctionnalités de canal complet** - Optimisation (expérimentation et ciblage de contenu), rapports et surveillance prêts à l’emploi, application du consentement et de la gouvernance, et fragments d’expression. <!--Multilingual and business rules are planned for a future release.-->
* **Orchestration unifiée** - Gérez tous vos canaux de messagerie en un seul endroit, quel que soit le fournisseur de diffusion sous-jacent.
* **Configuration sans code** - Les administrateurs configurent le canal par le biais de l’interface utilisateur du Channel Builder ; aucun code personnalisé ni effort d’ingénierie n’est nécessaire.

## Canal personnalisé par rapport aux actions personnalisées {#custom-channel-vs-custom-action}

Si vous avez déjà utilisé des [actions personnalisées](../action/action.md) dans des parcours [!DNL Journey Optimizer], les canaux personnalisés traitent un ensemble différent de cas d’utilisation.

**Utilisez des canaux personnalisés lorsque** vous devez envoyer des messages aux utilisateurs finaux par le biais d’une plateforme non prise en charge nativement dans [!DNL Journey Optimizer], telle que WeChat, Kakao Talk ou une passerelle de messagerie personnalisée. Les canaux personnalisés sont disponibles dans les campagnes, les parcours et les campagnes orchestrées, ainsi que la prise en charge des éléments suivants :

* Personnalisation complète via l’éditeur de personnalisation, comme pour les canaux sortants natifs
* Éditeur de payload visuel/de formulaire, aperçu et BAT
* Expérimentation et ciblage de contenu
* Rapports et surveillance d’usine
* Plusieurs informations d’identification d’API et configurations de canal
* RBAC/ABAC

Les canaux personnalisés prennent en charge POST comme seule méthode HTTP.

**Utilisez des actions personnalisées lorsque** en tant qu’étape d’un parcours, vous devez récupérer des données d’un système externe ou envoyer des informations à un système externe, tel qu’un centre d’appel, une plateforme de journalisation ou une base de données hors ligne. Les actions personnalisées sont disponibles dans parcours uniquement et prennent en charge les méthodes GET, PUT et POST.

<!--
| | Custom Action | Custom Channel |
| --- | --- | --- |
| **Primary use case** | Retrieve data from or send information to external systems (call centers, offline systems, logging) | Send messages to end users through channels not natively supported in [!DNL Journey Optimizer] |
| **Available in** | Journeys only | Campaigns, journeys, and orchestrated campaigns |
| **Supported HTTP methods** | GET, PUT, POST | POST only |
| **Full personalization (PE)** | No | Yes, through the personalization editor, similar to native outbound channels |
| **Visual/form editor** | No | Yes |
| **Preview and proof** | No | Yes |
| **Content experimentation** | No | Yes |
| **Targeting** | No | Yes |
| **OOTB Reporting** | Yes | Yes |
| **Multiple API credentials and channel configurations** | No | Yes |
| **RBAC/ABAC** | No | Yes |
-->

>[!TIP]
>
>Il est recommandé d’utiliser des canaux personnalisés dans les cas d’utilisation de canal où vous envoyez des messages aux utilisateurs finaux. Pour d’autres cas d’utilisation de type connecteur nécessaires dans les parcours, tels que la récupération de données ou le déclenchement de systèmes externes, vous pouvez continuer à utiliser des actions personnalisées.

## Cas d’utilisation {#use-cases}

Les canaux personnalisés sont idéaux pour :

* **Plateformes de messagerie non prises en charge** - Canaux tels que WeChat, Kakao Talk, Messenger, Telegram ou services de messagerie régionaux qui n’ont pas de canal [!DNL Journey Optimizer] natif.
* **Fournisseurs de diffusion personnalisés** - Les organisations qui ont investi dans un fournisseur externe qu’elles souhaitent continuer à utiliser pour la diffusion de messages, mais préfèrent l’utilisation de [!DNL Journey Optimizer] pour l’orchestration, la personnalisation et la gestion de campagnes.
* **Canaux hérités** - Passerelles de messagerie propriétaires ou héritées qui exposent un point d’entrée HTTP.
* **Canaux spécifiques au secteur** - Messagerie sécurisée pour les services de santé, les systèmes d’alerte bancaire ou les services de notification gouvernementaux.

## Fonctionnement {#how-it-works}

La configuration et l’utilisation d’un canal personnalisé suivent les étapes principales ci-dessous :

1. **Configurer** (Administrateur) - Un administrateur crée un canal personnalisé dans le **Créateur de canaux**, définissant le point d’entrée, l’authentification, la politique de limitation et la structure de la payload du message. Une configuration de canal est ensuite créée et liée au canal personnalisé. [En savoir plus](configure-custom-channel.md)
1. **Créer** (marketeur) - Un marketeur ajoute le canal personnalisé à un parcours, une campagne ou une campagne orchestrée, sélectionne une configuration de canal et crée la payload du message à l’aide de l’éditeur de personnalisation de [!DNL Journey Optimizer]. [En savoir plus](create-custom-experience.md)
1. **Envoyer** - Lorsqu’un profil est qualifié, [!DNL Journey Optimizer] envoie la payload personnalisée au point d’entrée configuré. Le système externe traite l’appel et diffuse le message.
1. **Surveiller** (administrateur/marketeur) : les administrateurs et les spécialistes du marketing peuvent surveiller les performances et la fiabilité du canal personnalisé par le biais des tableaux de bord de reporting et de surveillance de [!DNL Journey Optimizer]. [En savoir plus](monitor-custom-channel.md)

<!--
## Next steps {#next-steps}

* Review the prerequisites and permissions before setting up your first custom channel. [Learn more](custom-channel-prerequisites.md)
* Configure your first custom channel using the Channel Builder. [Learn more](custom-channel-configuration.md)
* Create a custom channel experience in a journey or campaign. [Learn more](create-custom-experience.md)
-->
