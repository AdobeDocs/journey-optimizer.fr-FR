---
solution: Journey Optimizer
product: journey optimizer
title: Questions fréquentes sur les intégrations
description: Questions fréquentes sur les intégrations Journey Optimizer pour les données externes et le contenu dans les messages.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: intégration, FAQ, données externes, personnalisation
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 852
ht-degree: 1%

---

# Questions fréquentes sur les intégrations {#vendor-integration-faq}

Vous trouverez ci-dessous des questions fréquentes sur **Intégrations** dans Adobe Journey Optimizer.


## Commencer

+++ Que font les intégrations dans Journey Optimizer ?

Il connecte des sources de données externes à Journey Optimizer afin que vous puissiez extraire du contenu et des données de systèmes tiers dans vos campagnes et parcours, et personnaliser les messages à l’aide de ces données.

➡️ [En savoir plus sur la présentation des intégrations](integrations.md)

+++

+++ Qui configure les intégrations et qui les utilise dans le contenu ?

Les administrateurs créent et activent la configuration technique (**[!UICONTROL Configurations]** > **[!UICONTROL Intégrations]** > **[!UICONTROL Gérer]** > **[!UICONTROL Créer l’intégration]**). Les marketeurs utilisent **[!UICONTROL Ajouter une personnalisation]** dans les composants Texte ou HTML, ouvrent **[!UICONTROL Intégrations]**, choisissent une intégration active et mappent les attributs.

➡️ [En savoir plus sur les workflows d’administration et de marketing](integrations.md)

+++

+++ Où puis-je créer ou gérer des intégrations dans l’interface utilisateur en tant qu’administrateur ?

Accédez à la section **[!UICONTROL Configurations]** dans le menu de gauche, ouvrez **[!UICONTROL Gérer]** à partir de la vignette **[!UICONTROL Intégrations]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

➡️ [En savoir plus sur la création d’une intégration](integrations.md#configure)

+++

+++ Quels sont les cas d’utilisation courants des intégrations ?

Il s’agit par exemple des points de récompense des systèmes de fidélité, des informations sur les prix des produits, des recommandations des moteurs de recommandation et des mises à jour logistiques telles que le statut de livraison.

➡️ [En savoir plus sur les exemples de données provenant de systèmes tiers](integrations.md)

➡️ [En savoir plus sur les exemples d’intégration de fournisseur](vendor-integration.md)

+++

## Configuration

+++ Comment configurer une intégration à un haut niveau en tant qu’administrateur ?

Vous indiquez un nom et une description, une URL de point d’entrée de l’API (éventuellement avec des variables de chemin d’accès), des valeurs de modèle de chemin d’accès, **[!UICONTROL GET]** ou **[!UICONTROL POST]**, des en-têtes facultatifs et des paramètres de requête, une méthode d’authentification, des paramètres de politique (tels que le délai d’expiration et le cache facultatif ou une nouvelle tentative), un exemple de réponse JSON pour mapper des champs, puis vous exécutez **[!UICONTROL Envoyer la connexion de test]** et **[!UICONTROL Activer]**, le cas échéant.

➡️ [En savoir plus sur la configuration de l&#39;intégration](integrations.md#configure)

+++

+++ Quels types d’authentification sont pris en charge ?

Ces types d’authentification sont disponibles : **[!UICONTROL Aucune authentification]**, **[!UICONTROL Clé API]**, **[!UICONTROL Authentification de base]** et **[!UICONTROL OAuth 2.0]** (avec la configuration de la payload pour OAuth, le cas échéant).

➡️ [En savoir plus sur les types d’authentification](integrations.md#configure)

+++

+++ Dans quel cas l’étape de payload de réponse est-elle utilisée ?

Collez un exemple de réponse JSON afin que le système puisse détecter les types de données et que vous puissiez choisir les champs exposés pour la personnalisation dans les messages. Vous pouvez limiter les champs disponibles pour les marketeurs lors de la création.

➡️ [En savoir plus sur le mappage de la payload de réponse](integrations.md#configure)

+++

+++ Comment les professionnels du marketing ajoutent-ils une intégration à un message ?

Dans le contenu de campagne ou de parcours, utilisez **[!UICONTROL Ajouter une personnalisation]** sur un composant Texte ou HTML, accédez à **[!UICONTROL Intégrations]**, sélectionnez une intégration et enregistrez. Grâce au mode Pilules de l’éditeur de personnalisation, vous pouvez mapper des valeurs à des variables de configuration (comme les paramètres d’en-tête ou de requête, ou les variables de chemin d’accès dans l’URL).

➡️ [En savoir plus sur la personnalisation avec les intégrations](integrations.md#personalization)

+++

## Fonctionnalités et cas d’utilisation

+++ Puis-je utiliser des intégrations dans les parcours et les campagnes ?

Oui. Cette fonctionnalité est disponible pour les parcours et les campagnes pour les canaux **sortants** (par exemple, les e-mails, les SMS et les notifications push), dans les limites des produits actuels.

➡️ [En savoir plus sur les parcours et les campagnes](integrations.md#limitations)

+++

+++ Puis-je utiliser des intégrations dans des fragments réutilisables ?

La fonctionnalité Intégrations est prise en charge dans les fragments.

➡️ [En savoir plus sur les fragments](aem-fragments-gs.md)

+++

## Limites

+++ Quels canaux prennent en charge les intégrations ?

Les canaux **sortants** sont pris en charge (par exemple e-mail, SMS et notification push).

➡️ [En savoir plus sur les canaux pris en charge](integrations.md#limitations)

+++

+++ Quels formats de réponse d’API sont pris en charge ?

Pour les réponses d’appel API, **JSON** et **HTML** sont pris en charge pour le mappage des champs. La sortie d’image binaire brute et les formats qui ne sont pas JSON ne sont pas disponibles pour ce workflow.

➡️ [En savoir plus sur les formats JSON et de réponse](integrations.md#limitations)

+++

+++ À quels modèles d’API puis-je me connecter ?

Les API **Retrieval** qui ciblent un contenu spécifique sont prises en charge. Les API **de liste** (liste large ou modèles de pagination) ne sont pas prises en charge pour ce modèle d’intégration.

➡️ [En savoir plus sur la récupération ou sur la liste des API](integrations.md#limitations)

+++

## Autorisations et fonctionnalités associées

+++ De quelles autorisations ai-je besoin pour configurer les intégrations ?

Pour commencer à utiliser les intégrations, les utilisateurs doivent disposer des autorisations **[!UICONTROL Gérer la configuration de l’intégration AJO]** et **[!UICONTROL Afficher la configuration de l’intégration AJO]**.

➡️ [En savoir plus sur les autorisations d’intégration](integrations.md#overview)

+++

+++ Les intégrations remplacent-elles les connecteurs Adobe Journey Optimizer vers les sources Experience Platform ?

Non. Les **intégrations** concernent les champs de personnalisation du contenu des messages que vous générez à partir des API. **Sources** et d’autres fonctionnalités d’ingestion de données ont des objectifs différents (par exemple, l’ingestion de données par lots et l’enrichissement des profils). Utilisez chaque fonctionnalité selon la portée prévue.

➡️ [En savoir plus sur l’utilité des intégrations](integrations.md)

➡️ [En savoir plus sur les sources Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=fr){target="_blank"}

+++

## Résolution des problèmes

+++ Pourquoi la connexion de test échoue-t-elle ou reste-t-elle non valide ?

Vérifiez l’URL du point d’entrée, la méthode HTTP, les modèles de chemin, les en-têtes et les paramètres de requête, l’authentification et le délai d’expiration de la politique. Utilisez **[!UICONTROL Envoyer une connexion de test]** après les réglages. En cas de problèmes de payload, assurez-vous que l’exemple reflète un fichier JSON valide et que les champs sélectionnés correspondent à ce que l’API renvoie.

➡️ [En savoir plus sur le test de la connexion et la validation de la payload](integrations.md#configure)

+++

+++ Pourquoi les professionnels du marketing ne voient-ils pas mon intégration dans le sélecteur ?

Les intégrations doivent être **activées** après un test réussi. Seules les intégrations actives s’affichent lorsque les marketeurs ouvrent **[!UICONTROL Intégrations]**. Si l’intégration est toujours en version brouillon ou inactive, commencez par terminer l’activation.

➡️ [En savoir plus sur les tests de connexion et d’activation](integrations.md#configure)

+++

## Fournisseurs tiers

+++ Quels exemples de fournisseurs sont disponibles et qui sécurise l’API ?

Vous pouvez intégrer à n’importe quelle plateforme tierce qui expose un point d’entrée d’API compatible. **Illustratif** les modèles de fournisseur et les exemples de configuration peuvent vous aider à modéliser des API compatibles. La responsabilité de la sécurisation des points d’entrée incombe à la plateforme tierce et à votre équipe.

➡️ [En savoir plus sur les procédures d&#39;intégration des fournisseurs](vendor-integration.md)

+++
