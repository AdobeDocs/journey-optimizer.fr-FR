---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser les clients MCP
description: Découvrez comment connecter Adobe Journey Optimizer aux clients MCP à l’aide du serveur MCP
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 90904fa1fb27782ac1deafb09f56a9abf5ceeb6e
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 1%

---

# Utiliser les clients MCP {#ajo-mcp}

>[!AVAILABILITY]
>
>Le serveur MCP [!DNL Adobe Journey Optimizer] est actuellement disponible uniquement dans **Claude Web** et **Claude Desktop**. La prise en charge d’autres applications compatibles avec MCP sera ajoutée dans les prochaines versions.

L’intégration MCP [!DNL Adobe Journey Optimizer] vous permet d’interroger des campagnes, des parcours et des offres à l’aide d’invites en langage clair, sans écrire d’appels API ni parcourir les écrans de produit. Cette page explique le fonctionnement de l’intégration, ce que vous pouvez en faire et comment commencer.

## Qu’est-ce que le protocole de contexte de modèle ? {#mcp-overview}

Les équipes de marketing et d’expérience client s’appuient de plus en plus sur des applications de chat et des outils de développement tels qu’Anthropic Claude, OpenAI ChatGPT, Cursor et Microsoft Copilot Studio pour rationaliser leur travail quotidien. Ces applications prennent en charge le **Model Context Protocol (MCP)**, une norme ouverte qui permet aux applications d’exposer de manière uniforme les outils back-end à des modèles de langage (LLM) volumineux.

[!DNL Adobe Journey Optimizer] fournit désormais un serveur MCP qui surfacie les opérations de campagne, de parcours, de fidélité et de sandbox directement dans toute application compatible MCP. Grâce à l’intégration MCP [!DNL Adobe Journey Optimizer], différentes personnes peuvent collaborer autour des mêmes données d’orchestration, sans écrire de requêtes sur l’API REST [!DNL Adobe Journey Optimizer] ni parcourir plusieurs écrans d’interface utilisateur. Les clients peuvent décrire leur intention par la conversation et laisser le LLM appeler les outils MCP appropriés.

## Fonctionnalités principales {#mcp-capabilities}

Le serveur MCP [!DNL Adobe Journey Optimizer] vous permet d’inspecter, de résumer et de résoudre les problèmes liés aux parcours, aux campagnes et aux offres directement à partir de l’assistant d’IA. Toutes les opérations sont **lecture seule** — les surfaces du serveur MCP récupèrent les API comme réponses en langage clair afin que vous puissiez :

* **Comprendre la logique des parcours** — Obtenez un résumé lisible par l&#39;utilisateur des embranchements, des conditions et des actions d&#39;un parcours.
* **Vérifier la préparation de la campagne** — Identifier les bloqueurs qui empêchent la publication d&#39;une campagne.
* **Lacunes de couverture par spot** — Identifiez les canaux couverts dans vos parcours et campagnes en direct et repérez les lacunes éventuelles.
* **Auditer votre portfolio d’orchestration** — Consulter le statut complet des campagnes et des parcours sans analyser le JSON ni passer d’un écran de produit à l’autre.

## Cas d’utilisation {#mcp-use-cases}

Les exemples suivants montrent comment interagir avec le serveur MCP [!DNL Adobe Journey Optimizer] à l’aide du langage naturel :

| Objectif | Exemple d’invite |
|---|---|
| **Résumé des détails de la campagne** | « Obtenez la campagne cmp456 et résumez l’audience, le planning, le statut et les packages. » |
| **Inventaire et audit de statut** | « Qu&#39;avons-nous et dans quel état ? Affichez les décomptes en direct, brouillon, terminé, arrêté ou archivé des campagnes. » |
| **Vérifier la préparation de la publication** | « Pourquoi la campagne cmp456 n’est-elle pas prête à être publiée ? Montre-moi les bloqueurs. » |
| **Comparer des objets** | « Comparer les campagnes abc123 et xyz789 — Qu’est-ce qui a changé dans le statut et le planning ? » |
| **Audit de votre portefeuille** | « Quels canaux sont couverts dans tous les parcours et campagnes en direct et où sont les lacunes ? » |
| **Couverture et mix des canaux** | « Affichez l’empreinte du canal sur les parcours, les campagnes et les emplacements d’offres : e-mail uniquement par rapport à multicanal, utilisation des notifications push/SMS/in-app et incohérences entre les canaux de parcours. » |

## Conditions préalables {#mcp-prerequisites}

Avant de connecter le serveur MCP [!DNL Adobe Journey Optimizer] à votre client MCP, vérifiez les points suivants :

* Vous disposez d&#39;une licence [!DNL Adobe Journey Optimizer] active.
* Vous avez accès à une application compatible avec MCP prise en charge (actuellement Claude Web ou Claude Desktop).
* Vous disposez des autorisations nécessaires dans [!DNL Adobe Journey Optimizer] pour afficher les campagnes, les parcours et les offres.

## Connexion du serveur MCP [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Cette intégration est disponible dans Beta. Les étapes de configuration détaillées seront publiées lorsqu’il sera mis à disposition. Contactez votre représentant Adobe pour demander un accès anticipé et recevoir les instructions de configuration.

Au cours de la phase Beta, votre représentant Adobe fournira :

* URL du point d’entrée du serveur MCP spécifique à votre organisation.
* Informations d’authentification pour connecter votre assistant d’IA à [!DNL Adobe Journey Optimizer].
* Conseils sur la configuration du serveur MCP dans Claude Desktop ou Claude Web.

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## Questions fréquentes {#mcp-faq}

+++Quels clients MCP sont pris en charge ?

Le serveur MCP [!DNL Adobe Journey Optimizer] est actuellement disponible pour **Claude Web** et **Claude Desktop**. Il est possible que la prise en charge d’autres applications compatibles avec MCP soit ajoutée dans les prochaines versions.
+++

+++À quels objets de [!DNL Adobe Journey Optimizer] puis-je accéder via MCP ?

Vous pouvez accéder aux campagnes, aux parcours, aux offres, aux données de fidélité et aux informations sur le sandbox. Les opérations sont en lecture seule (récupération des API) ; les opérations d’écriture ne sont pas prises en charge dans la version actuelle.
+++

+++Ai-je besoin d’un accès développeur pour utiliser le serveur MCP [!DNL Adobe Journey Optimizer] ?

Non. Le serveur MCP est conçu à la fois pour les professionnels du marketing et pour les techniciens. Les marketeurs peuvent interagir avec celui-ci à l’aide d’invites en langage naturel dans tout client MCP pris en charge, tandis que les développeurs peuvent également l’utiliser dans les outils de développement qui prennent en charge MCP.
+++

+++Mes données sont-elles envoyées au fournisseur du client MCP ?

Lorsque vous envoyez une invite, le client MCP peut envoyer le contexte approprié (y compris [!DNL Adobe Journey Optimizer] données renvoyées par le serveur MCP) à son modèle pour traitement. Consultez les politiques de confidentialité et de gestion des données de votre fournisseur client MCP avant de vous connecter aux données de production.
+++

+++De quelles autorisations ai-je besoin dans [!DNL Adobe Journey Optimizer] ?

Vous avez besoin au minimum d’autorisations **Vue** pour les objets que vous souhaitez interroger : des campagnes, des parcours ou des offres. Aucune autorisation d’écriture n’est requise, car le serveur MCP effectue uniquement des opérations de lecture. Contactez votre administrateur [!DNL Adobe Journey Optimizer] si vous n’êtes pas sûr de votre niveau d’accès actuel.
+++

+++Puis-je utiliser le serveur MCP dans les environnements Sandbox ?

Oui. Le serveur MCP respecte la configuration de votre sandbox [!DNL Adobe Journey Optimizer]. Vous pouvez interroger les données spécifiques au sandbox en spécifiant le sandbox dans votre invite ou en vous connectant à des informations d’identification limitées à un sandbox spécifique.
+++
