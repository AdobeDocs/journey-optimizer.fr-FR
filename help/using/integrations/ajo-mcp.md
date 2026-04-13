---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser les assistants d’IA via MCP
description: Découvrez comment connecter Adobe Journey Optimizer aux assistants AI à l’aide du serveur MCP (Model Context Protocol)
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Disponibilité limitée" type="Informative"
role: User, Developer
level: Beginner, Intermediate
source-git-commit: b92ef33b03e0bdcd6e615846cd7654aaab1b4a1a
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 1%

---

# Utiliser les assistants d’IA via MCP {#ajo-mcp}

>[!AVAILABILITY]
>
>Le serveur MCP [!DNL Adobe Journey Optimizer] est actuellement disponible uniquement dans **Claude Web** et **Claude Desktop**.

## Qu’est-ce que le protocole de contexte de modèle ? {#mcp-overview}

Les équipes de marketing et d’expérience client s’appuient de plus en plus sur des applications de chat et des outils de développement tels qu’Anthropic Claude, OpenAI ChatGPT, Cursor et Microsoft Copilot Studio pour rationaliser leur travail quotidien. Ces applications prennent en charge le **Model Context Protocol (MCP)**, une norme ouverte qui permet aux applications d’exposer de manière uniforme les outils back-end à des modèles de langage (LLM) volumineux.

[!DNL Adobe Journey Optimizer] fournit désormais un serveur MCP qui surfacie les opérations de campagne, de parcours, de fidélité et de sandbox directement dans toute application compatible MCP. Grâce à l’intégration MCP [!DNL Adobe Journey Optimizer], différentes personnes peuvent collaborer autour des mêmes données d’orchestration, sans écrire de requêtes sur l’API REST [!DNL Adobe Journey Optimizer] ni parcourir plusieurs écrans d’interface utilisateur. Les clients peuvent décrire leur intention par la conversation et laisser le LLM appeler les outils MCP appropriés.

## Fonctionnalités principales {#mcp-capabilities}

Le serveur MCP [!DNL Adobe Journey Optimizer] vous permet d’inspecter, de résumer et de résoudre les problèmes liés aux parcours, campagnes et offres [!DNL Adobe Journey Optimizer] directement à partir de l’assistant d’IA. Les API de récupération de [!DNL Adobe Journey Optimizer] sont transformées en réponses en langage clair afin que vous puissiez :

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

Avant de connecter le serveur MCP [!DNL Adobe Journey Optimizer] à votre assistant d’IA, vérifiez les points suivants :

* Vous disposez d&#39;une licence [!DNL Adobe Journey Optimizer] active.
* Vous avez accès à une application compatible avec MCP prise en charge (actuellement Claude Web ou Claude Desktop).
* Vous disposez des autorisations nécessaires dans [!DNL Adobe Journey Optimizer] pour afficher les campagnes, les parcours et les offres.

## Connexion du serveur MCP [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Des étapes de configuration détaillées seront ajoutées une fois l’intégration disponible. Contactez votre représentant Adobe pour un accès anticipé.

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## Questions fréquentes {#mcp-faq}

+++Quels assistants d’IA sont pris en charge ?

Le serveur MCP [!DNL Adobe Journey Optimizer] est actuellement disponible pour **Claude Web** et **Claude Desktop**. Il est possible que la prise en charge d’autres applications compatibles avec MCP soit ajoutée dans les prochaines versions.
+++

+++À quels objets de [!DNL Adobe Journey Optimizer] puis-je accéder via MCP ?

Vous pouvez accéder aux campagnes, aux parcours, aux offres, aux données de fidélité et aux informations sur le sandbox. Les opérations sont en lecture seule (récupération des API) ; les opérations d’écriture ne sont pas prises en charge dans la version actuelle.
+++

+++Ai-je besoin d’un accès développeur pour utiliser le serveur MCP [!DNL Adobe Journey Optimizer] ?

Non. Le serveur MCP est conçu à la fois pour les professionnels du marketing et pour les techniciens. Les marketeurs peuvent interagir avec celui-ci à l’aide d’invites en langage naturel dans Claude, tandis que les développeurs peuvent également l’utiliser dans les outils de développement qui prennent en charge MCP.
+++

+++Mes données sont-elles envoyées au fournisseur d’assistant d’IA ?

Lorsque vous envoyez une invite, l’assistant d’IA peut envoyer le contexte approprié (y compris [!DNL Adobe Journey Optimizer] données renvoyées par le serveur MCP) à son modèle pour traitement. Consultez les politiques de confidentialité et de gestion des données de votre fournisseur d’assistant d’IA avant de vous connecter aux données de production.
+++

