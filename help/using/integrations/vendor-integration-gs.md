---
solution: Journey Optimizer
product: journey optimizer
title: Intégration fournisseur
description: Utilisez les intégrations Adobe Journey Optimizer avec toute plateforme externe qui expose une API valide, ainsi que des modèles de fournisseur testés par l’ingénierie pour vous assurer de la fiabilité de votre configuration.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: intégration, fournisseur, tiers
source-git-commit: 3733c9ab401f85b22e1d6e07dbf4db535ff8a96d
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---


# Prise en main de l’intégration des fournisseurs {#vendor-integration}

>[!BEGINSHADEBOX]

Table des matières :

* [Utiliser des intégrations](external-sources.md)
* **[Prise en main de l’intégration des fournisseurs](vendor-integration-gs.md)**
* [Fournisseurs disponibles](vendor-integration.md)
* [FAQ](vendor-integration-faq.md)

>[!ENDSHADEBOX]

Vous pouvez utiliser **Integrations** dans Adobe Journey Optimizer pour appeler des **systèmes externes via HTTP** lorsque chaque système expose un point d’entrée **API** qui convient à votre cas d’utilisation et est compatible avec la manière dont Integrations émet des requêtes et consomme des réponses. Pour connaître le workflow complet, voir [Utilisation des intégrations](external-sources.md).

La liste des solutions tierces décrites est fournie à titre d’illustration et n’est pas exhaustive. D&#39;autres plates-formes peuvent être utilisées lorsqu&#39;elles répondent aux exigences du produit.

## Mécanismes de sécurisation opérationnels {#operational-guardrails}

Appliquez les règles suivantes lorsque vous configurez une intégration dans ce guide ou un fournisseur similaire :

* **Format de réponse :** intégrations mappent les champs des réponses **JSON**. Appels de conception afin que l’API renvoie un JSON adapté au mappage au moment de la création.
* **Payload et champs :** demandez et mappez uniquement les attributs dont vous avez besoin. Des réponses plus petites réduisent la latence et limitent l’exposition des données sensibles.
* **Forme Point d’entrée :** préférez la récupération stable **à ressource unique** (par exemple une entrée, un produit ou un membre) à des points d’entrée de liste large ou de pagination lorsque le produit s’attend à des recherches ciblées. Voir [Limitations et exclusions](#limitations-exclusions) et [Utilisation des intégrations](external-sources.md).
* **Volume et fiabilité :** respecter les **limites tarifaires** du fournisseur. Configurez la politique **délai d’expiration**, **reprise** et **cache** pour votre canal (par exemple, e-mail par lot par rapport aux envois transactionnels) et validez en cas de charge.
* **Sécurité :** stockez et faites pivoter les jetons, les clés API et les informations d’identification OAuth en fonction des politiques de votre entreprise. N’incorporez pas de secrets dans le contenu des messages.

## Restrictions et exclusions {#limitations-exclusions}

La liste des solutions tierces est **à titre d’illustration** et non exhaustive. Les API du fournisseur, les hôtes, les limites de débit et les formes de réponse JSON peuvent changer. Confirmez les points d’entrée, l’authentification et le mappage des champs avec la documentation actuelle du fournisseur et votre abonnement. Les modèles supposent ici que les appels **orientés lecture** conviennent à la personnalisation. L’écriture différée, les exportations par lots ou les réponses non JSON peuvent être hors de portée, sauf indication contraire.

## Navigation rapide {#quick-navigation}

Utilisez ces liens groupés pour accéder rapidement au modèle de fournisseur approprié :

* **Content and CMS :** [Contentful](#contentful), [Sitecore](#sitecore), [Salsify](#salsify), [Contentstack](#contentstack), [Akeneo](#akeneo), [Magnolia](#magnolia)
* **Fidélité et récompenses :** [Voucherify](#voucherify), [Talon.One](#talon-one), [Antavo](#antavo), [Fidélité Salesforce](#salesforce-loyalty), [Capillaire](#capillary)
* **Modèles et messages :** [Stensul](#stensul), [Marigold](#marigold), [Adobe Target Recommendations](#adobe-target-recommendations)
* **Données, météo et opérations :** [AccuWeather](#accuweather), [ShipStation](#shipstation), [RevenueCat](#revenuecat), [Databricks](#databricks)
* **Examens, consentement et réseaux sociaux :** [Bynder](#bynder), [Trustpilot](#trustpilot), [Bazaarvoice](#bazaarvoice), [OneTrust](#onetrust), [Meta](#meta), [Aprimo](#aprimo), [Epsilon (Epsilon3)](#epsilon)
