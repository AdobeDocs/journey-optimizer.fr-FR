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
subfeature_v2: []
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 7ced44f92f816d83d9a9ad667b4322dcb5930741
workflow-type: tm+mt
source-wordcount: 1369
ht-degree: 5%

---

# Utiliser les clients MCP {#ajo-mcp}

>[!BEGINSHADEBOX]

**Sur cette page :** obtenez un aperçu détaillé du serveur MCP [!DNL Adobe Journey Optimizer], des bases du protocole Model Context Protocol et des clients pris en charge, aux outils disponibles, aux exemples d’invites, aux conditions préalables de configuration, aux étapes de connexion et aux réponses aux questions courantes.

>[!ENDSHADEBOX]

L’intégration MCP [!DNL Adobe Journey Optimizer] vous permet d’interroger des campagnes, des parcours et des offres à l’aide d’invites en langage clair, sans écrire d’appels API ni parcourir les écrans de produit. Cette page explique le fonctionnement de l’intégration, ce que vous pouvez en faire et comment commencer.

>[!AVAILABILITY]
>
>Le serveur MCP [!DNL Adobe Journey Optimizer] est actuellement disponible en **Claude Web**, **Claude Desktop** et **Cursor**. La prise en charge d’autres applications compatibles avec MCP sera ajoutée dans les prochaines versions.

## Beta, sécurité et mentions légales {#mcp-notices}

**Remarque sur la documentation de Beta :** cette documentation couvre une fonctionnalité de Beta et ne constitue pas la documentation finale. Le contenu décrit ici se rapporte à une version de Beta et peut être modifié avant sa disponibilité générale. Adobe ne fait aucune déclaration quant à l’exhaustivité ou l’exactitude de cette documentation.

En utilisant le serveur Adobe Journey Optimizer MCP (Beta) (« Beta »), vous reconnaissez que le Beta est fourni **« tel quel », sans garantie d’aucune sorte**. Adobe n’a aucune obligation de tenir à jour, corriger, mettre à jour, modifier, remplacer ou prendre en charge Beta. Il est recommandé de faire preuve de prudence et de ne pas se fier, de quelque manière que ce soit, au bon fonctionnement ou aux performances de ce Beta et/ou des éléments qui l’accompagnent. La version Beta est considérée comme étant une information confidentielle dʼAdobe. Tout « commentaire » (informations relatives à la version Beta, y compris, mais sans s’y limiter, les problèmes ou défauts rencontrés lors de son utilisation, les suggestions, les améliorations et les recommandations) que vous fournissez à Adobe est par la présente cédé à Adobe. Cela inclut tous les droits, titres et intérêts relatifs à ces commentaires.

>[!WARNING]
>
>Le protocole MCP (Model Context Protocol) est une norme open source émergente qui peut présenter des risques pour la sécurité ou la fiabilité. Les intégrations de serveurs Adobe MCP et la documentation associée sont fournies « en l’état », sans garantie d’aucune sorte.
>
>La connexion des clients ou serveurs MCP aux produits Adobe est une configuration choisie par le client. Les clients sont chargés d’évaluer la sécurité et la pertinence de toute intégration MCP. Adobe n’est pas responsable des problèmes résultant d’une mauvaise configuration, d’une utilisation abusive du MCP, de vulnérabilités dans les implémentations tierces ou d’actions involontaires effectuées par le biais de workflows prenant en charge MCP.
>
>Pour réduire les risques, Adobe encourage à tester les intégrations dans un environnement Sandbox avant une utilisation productive, et à examiner et valider soigneusement toutes les actions et réponses initiées par MCP avant de les confirmer ou de s’y fier.

## Qu&#39;est-ce que le protocole de contexte du modèle ? {#mcp-overview}

Les équipes de marketing et d’expérience client s’appuient de plus en plus sur des applications de chat et des outils de développement tels qu’Anthropic Claude, OpenAI ChatGPT, Cursor et Microsoft Copilot Studio pour rationaliser leur travail quotidien. Ces applications prennent en charge le **Model Context Protocol (MCP)**, une norme ouverte qui permet aux applications d’exposer de manière uniforme les outils back-end à des modèles de langage (LLM) volumineux.

[!DNL Adobe Journey Optimizer] fournit désormais un serveur MCP qui surface les opérations de campagne et de sandbox directement dans toute application compatible MCP. Grâce à l’intégration MCP [!DNL Adobe Journey Optimizer], différentes personnes peuvent collaborer autour des mêmes données d’orchestration, sans écrire de requêtes sur l’API REST [!DNL Adobe Journey Optimizer] ni parcourir plusieurs écrans d’interface utilisateur. Les clients peuvent décrire leur intention par la conversation et laisser le LLM appeler les outils MCP appropriés.

## Fonctionnalités principales {#mcp-capabilities}

Le serveur MCP [!DNL Adobe Journey Optimizer] vous permet d’inspecter, de résumer et de résoudre les problèmes liés aux campagnes, aux parcours et aux offres directement à partir de l’assistant d’IA. Toutes les opérations sont **lecture seule** — les surfaces du serveur MCP récupèrent les API comme réponses en langage clair afin que vous puissiez :

* **Comprendre la logique des parcours** — Obtenez un résumé lisible par l&#39;utilisateur des embranchements, des conditions et des actions d&#39;un parcours.
* **Obtenez une visibilité instantanée de la campagne** — Renseignez-vous sur les statuts de campagne et les configurations de canal en langage clair et obtenez des réponses instantanément, sans parcourir les menus ni extraire manuellement les rapports.
* **Repérer les problèmes dès le début** — Faites apparaître les campagnes arrêtées, les brouillons orphelins et les problèmes de configuration des canaux au moment où vous posez la question, afin que votre équipe puisse agir rapidement.
* **Collaborer autour des données actives** — Les spécialistes du marketing, les responsables de campagne et les parties prenantes peuvent tous interroger les mêmes données de [!DNL Adobe Journey Optimizer] actives par l’intermédiaire de leur assistant d’IA, ce qui facilite l’alignement, la prise de décision et le déplacement entre les différentes parties.
* **Auditer votre portfolio d’orchestration** — Examiner le statut complet des campagnes sans analyser le JSON ni passer d’un écran de produit à l’autre.

## Outils disponibles {#mcp-tools}

Les outils suivants sont exposés par le serveur MCP [!DNL Adobe Journey Optimizer] :

**Outils Campaign**

| Outil | Description |
|---|---|
| **Liste des campagnes** | Parcourez vos campagnes marketing [!DNL Adobe Journey Optimizer]. Prend en charge le filtrage par statut (BROUILLON, ACTIF, ARRÊTÉ, TERMINÉ). |
| **Obtenir la campagne** | Récupérez des détails complets et la configuration d’une campagne spécifique par identifiant, y compris le ciblage de l’audience, le planning, le canal et les paramètres de contenu. |
| **Liste des configurations de canal** | Affichez les paramètres prédéfinis de surface et les paramètres de branding pour les canaux e-mail, SMS, notification push ou WhatsApp. |

**outils de Parcours**

| Outil | Description |
|---|---|
| **Obtenir tous les Parcours** | Parcourez tous les parcours de votre sandbox [!DNL Adobe Journey Optimizer]. |
| **Obtenir un Parcours** | Récupérez des détails complets sur un parcours spécifique par ID, y compris son embranchement, ses conditions et ses actions. |
| **Visualiser vos parcours** | Effectuez le rendu de vos parcours à l’aide d’outils interactifs afin d’explorer leur structure et leur flux visuellement. |

>[!NOTE]
>
>Tous les outils sont en lecture seule. Les opérations d’écriture (création, mise à jour ou suppression d’objets) ne sont pas prises en charge dans la version actuelle de Beta.

## Cas d’utilisation {#mcp-use-cases}

Les exemples suivants montrent comment interagir avec le serveur MCP [!DNL Adobe Journey Optimizer] à l’aide du langage naturel :

| Objectif | Exemple d’invite |
|---|---|
| **Présentation de Campaign et parcours** | Afficher toutes mes campagnes/parcours Journey Optimizer / Combien de campagnes/parcours sont configurés dans Journey Optimizer ? |
| **Audit de statut** | Quelles campagnes/parcours sont actuellement actifs ? / Répertoriez toutes les campagnes/parcours en pause ou arrêtés. |
| **Détails de la campagne et du parcours** | Obtenez les détails complets de la campagne [ID] / Découvrez tout ce qui est configuré dans la campagne [ID]. / Obtenez les détails complets du parcours [ID] / Parcourez tout ce qui est configuré dans le parcours [ID]. |
| **Audience et ciblage** | Quelle audience est ciblée dans la campagne/le parcours [ID] ? / Quelles sont les règles d&#39;éligibilité définies sur la campagne/le parcours [ID] ? |
| **Planning et minutage** | Quand l’exécution de la campagne [ID] est-elle planifiée ? / La campagne [ID] est-elle une opération unique d’envoi ou récurrente ? |
| **Dépannage** | Pourquoi l’identifiant de campagne [ID] n’est-il pas envoyé ? / Vérifiez la configuration de la campagne [ID] pour tout problème. |
| **Configuration du canal** | Quels préréglages de canal sont disponibles dans mon sandbox ? / Afficher toutes mes configurations de canal e-mail. |
| **Audit des canaux** | Quelles configurations de canal sont manquantes ou incomplètes ? / Combien de configurations de canal ai-je sur tous les canaux ? |

## Conditions préalables {#mcp-prerequisites}

Avant de connecter le serveur MCP [!DNL Adobe Journey Optimizer] à votre client MCP, vérifiez les points suivants :

* Vous disposez d&#39;une licence [!DNL Adobe Journey Optimizer] active.
* Vous avez accès à une application compatible avec MCP prise en charge (actuellement Claude Web, Claude Desktop ou Cursor).
* Vous disposez des autorisations nécessaires dans [!DNL Adobe Journey Optimizer] pour afficher les campagnes, les parcours et les offres.

## Connexion du serveur MCP [!DNL Adobe Journey Optimizer] {#mcp-connect}

>[!NOTE]
>
>Cette intégration est disponible dans Beta.

Vous pouvez connecter le serveur MCP [!DNL Adobe Journey Optimizer] via votre client MCP préféré, y compris **Claude Web**, **Claude Desktop** et **Cursor**.

**Connexion via un client MCP**

Lors de la configuration du serveur MCP dans votre client MCP, utilisez l’URL de point d’entrée du serveur suivante :

`https://ajo-mcp.adobe.io/mcp`

**Connexion via Claude Web ou Claude Desktop**

Pour configurer le serveur MCP dans Claude Web ou Claude Desktop, accédez à **Connecteurs** et sélectionnez **Adobe Journey Optimizer**.

## Questions fréquentes {#mcp-faq}

+++Quels clients MCP sont pris en charge ?

Le serveur MCP [!DNL Adobe Journey Optimizer] est actuellement disponible pour **Claude Web**, **Claude Desktop** et **Cursor**. Il est possible que la prise en charge d’autres applications compatibles avec MCP soit ajoutée dans les prochaines versions.
+++

+++À quels objets de [!DNL Adobe Journey Optimizer] puis-je accéder via MCP ?

Vous pouvez accéder aux informations sur les campagnes, les parcours, les offres et les sandbox. Les opérations sont en lecture seule (récupération des API) ; les opérations d’écriture ne sont pas prises en charge dans la version actuelle.
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

