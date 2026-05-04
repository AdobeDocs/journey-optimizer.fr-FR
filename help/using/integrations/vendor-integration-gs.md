---
solution: Journey Optimizer
product: journey optimizer
title: Intégration fournisseur
description: Utilisez les intégrations Adobe Journey Optimizer avec toute plateforme externe qui expose une API valide, ainsi que des modèles de fournisseur testés par l’ingénierie pour vous assurer de la fiabilité de votre configuration.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: intégration, fournisseur, tiers
source-git-commit: 4cc3c959fe08c1d574a5d041bf7721441bc96f97
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---


# Intégration des fournisseurs {#vendor-integration}

Vous pouvez utiliser **Integrations** dans Adobe Journey Optimizer pour appeler des **systèmes externes via HTTP** lorsque chaque système expose un point d’entrée **API** qui convient à votre cas d’utilisation et est compatible avec la manière dont Integrations émet des requêtes et consomme des réponses. Pour connaître le workflow complet, voir [Utilisation des intégrations](integrations.md).

La liste des solutions tierces décrites est fournie à titre d’illustration et n’est pas exhaustive. D&#39;autres plates-formes peuvent être utilisées lorsqu&#39;elles répondent aux exigences du produit.

## Mécanismes de sécurisation opérationnels {#operational-guardrails}

Appliquez les règles suivantes lorsque vous configurez une intégration dans ce guide ou un fournisseur similaire :

* **Format de réponse :** intégrations mappent les champs des réponses **JSON** ou **HTML**. Appels de conception afin que l’API renvoie un JSON ou un HTML adapté au mappage au moment de la création.
* **Payload et champs :** demandez et mappez uniquement les attributs dont vous avez besoin. Des réponses plus petites réduisent la latence et limitent l’exposition des données sensibles.
* **Forme Point d’entrée :** préférez la récupération stable **à ressource unique** (par exemple une entrée, un produit ou un membre) à des points d’entrée de liste large ou de pagination lorsque le produit s’attend à des recherches ciblées. Voir [Limitations et exclusions](#limitations-exclusions) et [Utilisation des intégrations](integrations.md).
* **Volume et fiabilité :** respecter les **limites tarifaires** du fournisseur. Configurez la politique **délai d’expiration**, **reprise** et **cache** pour votre canal (par exemple, e-mail par lot par rapport aux envois transactionnels) et validez en cas de charge.
* **Sécurité :** stockez et faites pivoter les jetons, les clés API et les informations d’identification OAuth en fonction des politiques de votre entreprise. N’incorporez pas de secrets dans le contenu des messages.


## Restrictions et exclusions {#limitations-exclusions}

La liste des solutions tierces est **à titre d’illustration** et non exhaustive. Les API du fournisseur, les hôtes, les limites de débit et les formes de réponse JSON ou HTML peuvent changer. Confirmez les points d’entrée, l’authentification et le mappage des champs avec la documentation actuelle du fournisseur et votre abonnement. Les modèles supposent ici que les appels **orientés lecture** conviennent à la personnalisation. Les intégrations prennent uniquement en charge le mappage à partir des réponses **JSON** et **HTML**. **Écriture différée**, **exportations par lots** et les réponses dans tout autre format ne sont pas prises en charge.

## Navigation rapide {#quick-navigation}

Utilisez ces liens groupés pour accéder rapidement au modèle de fournisseur approprié :

* **Système de gestion de contenu :** [Contentful](vendor-integration.md#contentful), [Sitecore](vendor-integration.md#sitecore), [Salsify](vendor-integration.md#salsify), [Contentstack](vendor-integration.md#contentstack), [Akeneo](vendor-integration.md#akeneo), [Magnolia](vendor-integration.md#magnolia)
* **Fidélité et récompenses :** [Voucherify](vendor-integration.md#voucherify), [Talon.One](vendor-integration.md#talon-one), [Antavo](vendor-integration.md#antavo), [Fidélité Salesforce](vendor-integration.md#salesforce-loyalty), [Capillaire](vendor-integration.md#capillary)
* **Modèles, personnalisation et recommandations :** [Stensul](vendor-integration.md#stensul), [Marigold](vendor-integration.md#marigold), [Adobe Target Recommendations](vendor-integration.md#adobe-target-recommendations)
* **Données, météo et opérations :** [AccuWeather](vendor-integration.md#accuweather), [ShipStation](vendor-integration.md#shipstation), [RevenueCat](vendor-integration.md#revenuecat), [Databricks](vendor-integration.md#databricks)
* **Examens, consentement et réseaux sociaux :** [Bynder](vendor-integration.md#bynder), [Trustpilot](vendor-integration.md#trustpilot), [Bazaarvoice](vendor-integration.md#bazaarvoice), [OneTrust](vendor-integration.md#onetrust), [Meta](vendor-integration.md#meta), [Aprimo](vendor-integration.md#aprimo), [Epsilon (Epsilon3)](vendor-integration.md#epsilon)
