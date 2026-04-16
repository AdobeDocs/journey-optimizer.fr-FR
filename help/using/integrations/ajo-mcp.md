---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation des clients MCP (Beta)
description: Découvrez comment connecter Adobe Journey Optimizer aux clients MCP à l’aide du serveur MCP
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 9450ff7b477ef3ef6825eb2c2feec77ffaec389f
workflow-type: tm+mt
source-wordcount: '1370'
ht-degree: 4%

---

# Utilisation des clients MCP (Beta) {#ajo-mcp}

>[!CAUTION]
>
>**Remarque sur la documentation de Beta :** cette documentation couvre une fonctionnalité de Beta et ne constitue pas la documentation finale. Le contenu décrit ici se rapporte à une version de Beta et peut être modifié avant sa disponibilité générale. Adobe ne fait aucune déclaration quant à l’exhaustivité ou l’exactitude de cette documentation.
>
>© Adobe Inc. All rights reserved. Adobe, le logo Adobe et Adobe Journey Optimizer sont des marques déposées ou des marques commerciales d’Adobe aux États-Unis et/ou dans d’autres pays.
>
>En utilisant le serveur Adobe Journey Optimizer MCP (Beta) (« Beta »), vous reconnaissez que le Beta est fourni **« tel quel », sans garantie d’aucune sorte**. Adobe n’a aucune obligation de tenir à jour, corriger, mettre à jour, modifier, remplacer ou prendre en charge Beta. Il est recommandé de faire preuve de prudence et de ne pas se fier, de quelque manière que ce soit, au bon fonctionnement ou aux performances de ce Beta et/ou des éléments qui l’accompagnent. Le Beta est considéré comme des informations confidentielles d’Adobe. Tout « commentaire » (informations relatives à la version Beta, y compris, mais sans s’y limiter, les problèmes ou défauts rencontrés lors de son utilisation, les suggestions, les améliorations et les recommandations) que vous fournissez à Adobe est par la présente cédé à Adobe. Cela inclut tous les droits, titres et intérêts relatifs à ces commentaires.

L’intégration MCP [!DNL Adobe Journey Optimizer] vous permet d’interroger des campagnes, des parcours et des offres à l’aide d’invites en langage clair, sans écrire d’appels API ni parcourir les écrans de produit. Cette page explique le fonctionnement de l’intégration, ce que vous pouvez en faire et comment commencer.

>[!AVAILABILITY]
>
>Le serveur MCP [!DNL Adobe Journey Optimizer] est actuellement disponible uniquement dans **Claude Web** et **Claude Desktop**. La prise en charge d’autres applications compatibles avec MCP sera ajoutée dans les prochaines versions.

## Qu&#39;est-ce que le protocole de contexte du modèle ? {#mcp-overview}

Les équipes de marketing et d’expérience client s’appuient de plus en plus sur des applications de chat et des outils de développement tels qu’Anthropic Claude, OpenAI ChatGPT, Cursor et Microsoft Copilot Studio pour rationaliser leur travail quotidien. Ces applications prennent en charge le **Model Context Protocol (MCP)**, une norme ouverte qui permet aux applications d’exposer de manière uniforme les outils back-end à des modèles de langage (LLM) volumineux.

[!DNL Adobe Journey Optimizer] fournit désormais un serveur MCP qui surfacie les opérations de campagne, de parcours, de fidélité et de sandbox directement dans toute application compatible MCP. Grâce à l’intégration MCP [!DNL Adobe Journey Optimizer], différentes personnes peuvent collaborer autour des mêmes données d’orchestration, sans écrire de requêtes sur l’API REST [!DNL Adobe Journey Optimizer] ni parcourir plusieurs écrans d’interface utilisateur. Les clients peuvent décrire leur intention par la conversation et laisser le LLM appeler les outils MCP appropriés.

## Fonctionnalités principales {#mcp-capabilities}

Le serveur MCP [!DNL Adobe Journey Optimizer] vous permet d’inspecter, de résumer et de résoudre les problèmes liés aux parcours, aux campagnes et aux offres directement à partir de l’assistant d’IA. Toutes les opérations sont **lecture seule** — les surfaces du serveur MCP récupèrent les API comme réponses en langage clair afin que vous puissiez :

<!--* **Understand journey logic** — Get a human-readable summary of any journey's branching, conditions, and actions.-->
* **Obtenez une visibilité instantanée de la campagne** — Renseignez-vous sur les statuts de la campagne, les performances du parcours ou les configurations des canaux en langage clair et obtenez des réponses instantanément, sans parcourir les menus ni extraire manuellement les rapports.
* **Repérer les problèmes dès le début** — Faites apparaître les campagnes arrêtées, les brouillons orphelins et les problèmes de configuration des canaux au moment où vous posez la question, afin que votre équipe puisse agir rapidement.
* **Collaborer autour des données actives** — Les spécialistes du marketing, les responsables de campagne et les parties prenantes peuvent tous interroger les mêmes données de [!DNL Adobe Journey Optimizer] actives par l’intermédiaire de leur assistant d’IA, ce qui facilite l’alignement, la prise de décision et le déplacement entre les différentes parties.
* **Auditer votre portfolio d’orchestration** — Consulter le statut complet des campagnes et des parcours sans analyser le JSON ni passer d’un écran de produit à l’autre.

## Outils disponibles {#mcp-tools}

Les outils suivants sont exposés par le serveur MCP [!DNL Adobe Journey Optimizer] :

| Outil | Description |
|---|---|
| **Liste des campagnes** | Parcourez vos campagnes marketing [!DNL Adobe Journey Optimizer]. Prend en charge le filtrage par statut (BROUILLON, ACTIF, ARRÊTÉ, TERMINÉ). |
| **Obtenir la campagne** | Récupérez des détails complets et la configuration d’une campagne spécifique par identifiant, y compris le ciblage de l’audience, le planning, le canal et les paramètres de contenu. |
| **Liste des Parcours** | Affichez vos parcours client [!DNL Adobe Journey Optimizer] (workflows automatisés), avec un filtrage facultatif par statut : BROUILLON, ACTIF, FERMÉ ou TERMINÉ. |
| **Liste des configurations de canal** | Affichez les paramètres prédéfinis de surface et les paramètres de branding pour les canaux e-mail, SMS, notification push ou WhatsApp. |

>[!NOTE]
>
>Tous les outils sont en lecture seule. Les opérations d’écriture (création, mise à jour ou suppression d’objets) ne sont pas prises en charge dans la version actuelle de Beta.

## Cas d’utilisation {#mcp-use-cases}

Les exemples suivants montrent comment interagir avec le serveur MCP [!DNL Adobe Journey Optimizer] à l’aide du langage naturel :

| Objectif | Exemple d’invite |
|---|---|
| **Présentation de Campaign** | « Afficher toutes mes campagnes AJO » / « Combien de campagnes sont configurées dans AJO ? » |
| **Audit de statut** | « Quelles sont les campagnes actuellement actives ? » / « Répertoriez toutes les campagnes en pause ou arrêtées. » |
| **Détails de la campagne** | « Obtenez les détails complets de la campagne [ID] » / « Découvrez-moi tout ce qui est configuré dans la campagne [ID]. » |
| **Audience et ciblage** | « Quelle audience est ciblée dans l’[ de campagne ] ? » / « Quelles règles d’éligibilité sont définies sur l’[ID] de campagne ? » |
| **Planning et minutage** | « Quand l’exécution de la campagne [ID] est-elle planifiée ? » / « L’identifiant de campagne [ID] est-il un envoi unique ou récurrent ? » |
| **Dépannage** | « Pourquoi l’identifiant de campagne [ID] n’est-il pas envoyé ? » / « Vérifiez la configuration de l’[ID] de campagne pour tout problème. » |
| **Inventaire des Parcours** | « Répertorier tous les parcours dynamiques » / « Afficher les parcours au statut de brouillon ». |
| **Configuration des canaux** | « Quels préréglages de canal sont disponibles dans mon sandbox ? » / « Afficher toutes mes configurations de canal e-mail ». |
| **Audit des canaux** | « Quelles configurations de canal sont manquantes ou incomplètes ? » / « Combien de configurations de canal ai-je sur tous les canaux ? » |

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

## Limites connues (Beta) {#mcp-limitations}

Les restrictions suivantes s’appliquent à la version Beta actuelle du serveur MCP [!DNL Adobe Journey Optimizer] :

| Limite | Description | Solution de contournement |
|---|---|---|
| **Aucune mesure d’engagement ou de performances** | Le serveur MCP n’expose aucune donnée de rapport. Les outils ne renvoient pas d’impressions, de taux de clics publicitaires, de conversions ni de statistiques de diffusion. | Utilisez l’interface utilisateur de création de rapports d’AJO, CJA MCP ou Adobe Analytics MCP pour les mesures. AEP Query Service peut interroger les données brutes des événements à l’aide de l’identifiant d’exécution de campagne. |
| **La pagination de la liste Campaign est limitée** | `List Campaigns` renvoie toujours la première page de résultats (jusqu’à 50 campagnes, triées par ordre alphabétique). Les valeurs de décalage et de limite ne sont pas appliquées, ce qui rend l’énumération complète peu pratique pour les sandbox volumineux. | Utilisez `Get Campaign` directement si l’identifiant ou le nom de la campagne est connu. Utilisez l’interface utilisateur d’AJO pour parcourir et filtrer la liste complète. |
| **Aucun filtrage côté serveur par date, canal ou planning** | `List Campaigns` ne prend en charge que le filtrage par statut. Le filtrage par date de publication, date de planification, canal ou type de campagne n’est pas disponible côté serveur. | Utilisez la liste des campagnes de l’interface utilisateur d’AJO, qui prend en charge le filtrage des dates et des canaux natifs. |
| **Récupération du contenu du message non disponible** | L’outil de contenu du message renvoie un HTTP 502 pour tous les types de canal (e-mail, code, etc.). Les messages HTML, les objets, les jetons de personnalisation et le contenu de l’offre ne peuvent pas être récupérés via MCP. | Affichez le contenu du message et les jetons de personnalisation directement dans l’interface utilisateur d’AJO sous **Campagnes > [Campagne] > Contenu**. |

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

