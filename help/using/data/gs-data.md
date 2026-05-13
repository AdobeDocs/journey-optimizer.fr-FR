---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec la gestion des données dans Journey Optimizer
description: Découvrez comment les données entrent et sortent d’Adobe Journey Optimizer, notamment les concepts clés, les étapes de configuration et les mécanismes de sécurisation.
feature: Data Management
role: Developer, Admin, User
level: Beginner, Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
TQID: https://experienceleague.adobe.com/Dq8mzkfuxvcoAPI1vjq9lFHjz4Z5j9s42-kfMy59PeI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080bid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 2612
ht-degree: 100%

---

# Commencer avec la gestion des données {#about-data}

Les données sont la base de chaque parcours, décision et message que vous diffusez avec [!DNL Adobe Journey Optimizer].

Cette page vous donne un point de départ pratique pour comprendre :

* les blocs de création de données principaux utilisés par Journey Optimizer (schémas, jeux de données, identités, profils) ;
* comment Journey Optimizer utilise les données Adobe Experience Platform ;
* les étapes de configuration des données que votre équipe doit effectuer avant de créer des parcours et des campagnes ;
* où trouver des informations détaillées sur la configuration et les bonnes pratiques.

Utilisez ce guide avec vos ingénieures et ingénieurs de données, administrateurs et administratrices, et responsables marketing afin que tout le monde ait une vue d’ensemble de la manière dont les données entrent et sortent de Journey Optimizer.

>[!TIP]
>Vous découvrez la gestion des données dans Journey Optimizer ? Regardez le [tutoriel sur la vue d’ensemble de la configuration des données](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"} pour une présentation pratique adaptée aux novices des schémas, des jeux de données et des sources.

## comment Journey Optimizer utilise les données Adobe Experience Platform ; {#aep-data}

[!DNL Adobe Journey Optimizer] repose sur [!DNL Adobe Experience Platform]. Il ne conserve pas de magasin de données séparé et isolé. Il utilise plutôt les mêmes données que les autres applications Experience Cloud.

Les schémas et les jeux de données résident dans Adobe Experience Platform. Les identités et le [profil client en temps réel](../audience/get-started-profiles.md) sont gérés par le service d’identités et le service de profil. Journey Optimizer extrait les données de profil et d’événement à partir d’Adobe Experience Platform pour évaluer les conditions de parcours, personnaliser les messages et sélectionner des offres. Il enregistre des données d’interaction, telles que des événements d’envoi, d’ouverture, de clic et de rebond, ainsi que des événements d’étape de parcours, dans les jeux de données Experience Platform. Il peut également rechercher des jeux de données supplémentaires au moment de l’exécution sans copier ces données dans le profil.

>[!TIP]
>Considérez Adobe Experience Platform comme votre couche de données principale et Journey Optimizer comme une application qui orchestre les parcours et les messages à l’aide de cette base de données partagée.

➡️ [En savoir plus sur l’architecture Journey Optimizer](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/get-started/essentials/understanding-ajo#architecture-details){target="_blank"}

## Concepts clés des données dans Journey Optimizer {#key-concepts}

Lorsque vous utilisez des données dans Journey Optimizer, vous rencontrez plusieurs concepts associés. Le tableau ci-dessous vous donne une vue d’ensemble rapide. Les sections qui suivent expliquent chaque concept plus en détail.

| Concept | Signification | Utilisation principale dans Journey Optimizer |
|---|---|---|
| Schéma XDM | Règles qui représentent, valident et mettent en forme vos données (créées à partir d’une classe et de groupes de champs) | Modéliser les attributs de profil et les événements comportementaux |
| Jeu de données | Table de stockage des données conformes à un schéma | Conserver les données de profil, d’événement et générées par le système |
| Connecteur source | Diffusion en continu ou par lots de données à partir de systèmes externes dans AEP | Ingérer les données CRM, analytiques et web |
| Source de données | Exposition d’AEP ou des champs externes dans les parcours | Alimenter les conditions de parcours et la personnalisation des messages |
| Identité | Identifiant qui représente de manière unique un client ou une cliente individuel | Regrouper les profils sur plusieurs canaux |
| Rechercher un jeu de données | Référence d’exécution aux données AEP sans stockage de profil | Enrichir les messages avec des données de référence actives |

### Schéma (schéma XDM) {#schema}

Un schéma est un jeu de règles qui représente et valide la structure et le format des données. Il se compose d’une **classe** (qui définit le comportement de base : enregistrement ou série temporelle) et de **groupes de champs** facultatifs (qui ajoutent des champs spécifiques). Les schémas sont définis à l’aide des normes du modèle de données d’expérience (XDM) et se trouvent dans Adobe Experience Platform.

XDM existe pour résoudre un réel problème : le même concept (un client ou une cliente, un achat, un produit) est nommé et structuré différemment selon les systèmes sources. XDM fournit un langage partagé qui regroupe ces concepts sous une seule définition, quelle que soit la provenance des données. C’est ce qui permet à Journey Optimizer de fonctionner de manière cohérente avec les données de votre CRM, de votre site web, de votre application mobile et de votre entrepôt de données en même temps.

Dans Journey Optimizer, vous utilisez généralement des schémas **XDM Individual Profile** pour les attributs client (nom, préférences, consentement) et des schémas **XDM ExperienceEvent** pour les événements comportementaux (achats, pages vues, inscriptions).

➡️ [En savoir plus sur les schémas](get-started-schemas.md)

### Jeu de données {#dataset}

Un jeu de données est une structure de stockage et de gestion pour les données conformes à un schéma : considérez-le comme un tableau avec un ensemble défini de colonnes et de lignes. Toutes les données utilisées par Journey Optimizer sont stockées dans des jeux de données Adobe Experience Platform. Il peut s’agir de jeux de données de profil (contribuant au profil client en temps réel), de jeux de données d’événement (stockant les données comportementales pour les parcours et les analyses) ou de jeux de données système automatiquement créés par Journey Optimizer pour le suivi, les commentaires et les événements d’étape de parcours.

➡️ [En savoir plus sur les jeux de données](get-started-datasets.md)

### Connecteur source {#source-connector}

Un connecteur source (également appelé **source**) vous permet d’ingérer des données provenant de plusieurs systèmes tels qu’Adobe Analytics, le SDK web Adobe Experience Platform, l’espace de stockage dans le cloud (S3, Azure Blob) ou des bases de données CRM dans Adobe Experience Platform. Au-delà de l’ingestion brute, les connecteurs permettent la structuration, l’étiquetage et l’amélioration des données à l’aide des services Experience Platform, y compris le mappage des champs vers vos schémas XDM et l’étiquetage de la gouvernance des données.

➡️ [En savoir plus sur les connecteurs sources](../start/get-started-sources.md)

### Source de données (Journey Optimizer) {#data-source}

Une source de données dans Journey Optimizer définit les champs à partir d’Adobe Experience Platform (ou les API externes) exposés dans les parcours et les messages. Configurées dans l’interface d’utilisation de Journey Optimizer, les sources de données incluent généralement la source de données Adobe Experience Platform intégrée (exposant les attributs de profil client en temps réel) et des sources de données externes ou personnalisées facultatives appelées au moment de l’exécution du parcours pour un enrichissement supplémentaire. Elles sont utilisées pour les conditions de parcours, les actions personnalisées et la personnalisation des messages.

➡️ [En savoir plus sur les sources de données](../datasource/about-data-sources.md)

>[!NOTE]
>Le [glossaire Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/glossary){target="_blank"} définit de manière générique le terme « source de données » comme l’origine des données (un CRM, une application mobile, etc.). Dans Journey Optimizer, le terme **source de données** a une signification spécifique : une configuration de l’interface d’utilisation qui contrôle les champs exposés dans les parcours et les messages.

### Identité et profil client en temps réel {#identity}

Une identité est un identifiant qui représente de manière unique un client ou une cliente individuel, tel qu’un identifiant de cookie, un identifiant d’appareil, une adresse e-mail ou un identifiant CRM. Les identités sont organisées en espaces de noms (e-mail, ECID, CRMID) et plusieurs identités pour la même personne sont regroupées dans un graphique d’identités unifié. Le profil client en temps réel utilise ce graphique pour conserver une vue d’ensemble de chaque client ou cliente en combinant des données issues de plusieurs canaux, notamment des sources en ligne, hors ligne, CRM et tierces.

Le modèle **fragment de profil** est un concept clé pour les personnes qui débutent. Chaque fois qu’un client ou qu’une cliente interagit avec votre marque sur un appareil ou un canal spécifique (votre site web, votre application mobile, un magasin), cette interaction est enregistrée en tant que fragment de profil : une vue partielle de ce client ou cette cliente en fonction de ce point de contact spécifique. Le profil client en temps réel regroupe en permanence ces fragments en fonction des valeurs d’identité partagées, créant ainsi un profil complet et à jour. Journey Optimizer s’appuie sur ce profil assemblé pour évaluer les conditions, sélectionner des offres et personnaliser les messages en temps réel.

➡️ [En savoir plus sur les identités dans Journey Optimizer](../audience/get-started-identity.md)

### Rechercher un jeu de données {#lookup-dataset}

Un jeu de données de recherche permet à Journey Optimizer de récupérer des données de référence ou transactionnelles au moment de l’exécution à partir d’un jeu de données Adobe Experience Platform, sans stocker ces données sur le profil client en temps réel. Cela s’avère utile pour les données de référence qui changent fréquemment (prix, inventaire, heures du magasin) ou les données transactionnelles qui sont nécessaires au moment du message, mais qui n’appartiennent pas au profil. Journey Optimizer effectue la recherche lors de l’exécution du parcours ou du message en fonction d’une clé telle qu’un identifiant de produit.

➡️ [En savoir plus sur les jeux de données de recherche](lookup-aep-data.md)

## Liste de contrôle relative à la préparation des données {#checklist}

Avant que les responsables marketing ne commencent à créer des parcours et des campagnes, votre organisation doit suivre un ensemble d’étapes de préparation des données. Cela permet à Journey Optimizer d’utiliser les données appropriées, au bon moment et de manière conforme.

>[!NOTE]
>Les étapes ci-dessous impliquent plusieurs rôles : ingénieures et ingénieurs de données, administrateurs et administratrices, et responsables marketing. Utilisez cette liste de contrôle comme plan commun pour préparer votre environnement. Les étapes 1 à 4 sont effectuées dans Adobe Experience Platform. Les étapes 5 à 6 sont configurées dans Journey Optimizer.

Les six étapes ci-dessous vous guident tout au long du processus de configuration des données, de la configuration des identités à la vérification du flux correct des données dans Journey Optimizer :

1. Définir votre stratégie d’identité
1. Concevoir des schémas pour les données de profil et d’événement
1. Créer des jeux de données activés pour les profils
1. Ingérer des données à partir de vos sources
1. Configurer des sources de données dans Journey Optimizer
1. Vérifier les jeux de données de suivi, de commentaires et de parcours

+++ Définir votre stratégie d’identité

Choisissez une identité principale pour vos clientes et clients (telle que l’ECID, l’e-mail ou le CRMID) et configurez les espaces de noms correspondants dans le Service d’identités Adobe Experience Platform. Assurez-vous que les champs d’identité sont présents dans vos schémas activés pour les profils et vérifiez que les profils sont correctement assemblés dans le graphique d’identité.

➡️ [En savoir plus sur les identités dans Journey Optimizer](../audience/get-started-identity.md)

+++

+++ Concevoir des schémas pour les données de profil et d’événement

Créez des schémas **Profil individuel XDM** pour capturer les attributs du client, tels que le nom et les coordonnées, les préférences et centres d’intérêt, ainsi que l’étape du cycle de vie ou l’état de consentement. Créez des schémas **XDM ExperienceEvent** pour capturer des données comportementales et transactionnelles telles que des événements web et d’application, des achats et des interactions hors ligne. Marquez les champs corrects en tant qu’identités et attributs de profil, le cas échéant.

➡️ [En savoir plus sur les schémas](get-started-schemas.md)

+++

+++ Créer des jeux de données activés pour les profils

Dans Adobe Experience Platform, créez des jeux de données basés sur vos schémas XDM et activez le profil sur n’importe quel jeu de données qui doit contribuer au profil client en temps réel. Vérifiez que les jeux de données générés par le système et créés par Journey Optimizer sont visibles dans l’espace de travail Jeux de données.

➡️ [En savoir plus sur les jeux de données](get-started-datasets.md)

+++

+++ Ingérer des données à partir de vos sources

Configurez les connecteurs source pour vos systèmes d’entreprise, tels qu’Adobe Analytics, Adobe Experience Platform SDK Web ou vos plateformes CRM et POS, et mappez les champs entrants à vos schémas XDM. Vérifiez que les données arrivent dans les jeux de données corrects et apparaissent dans le profil client en temps réel, là où cela est prévu.

➡️ [En savoir plus sur les connecteurs source](../start/get-started-sources.md)

➡️ [Tutoriel : créer des jeux de données et ingérer des données](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}

+++

+++ Configurer des sources de données dans Journey Optimizer

Les sources de données relèvent d’un concept spécifique à Journey Optimizer : elles ne se trouvent pas à l’endroit où se situent vos données, mais bien là où vous déclarez les champs que Journey Optimizer est autorisé à lire lors de l’exécution des parcours et des messages. Avant qu’un parcours puisse évaluer une condition telle que « est-ce que le client ou la cliente est membre du programme de fidélité ? », ou personnaliser un message avec un prénom, les champs de profil pertinents doivent être exposés via une configuration de source de données.

Journey Optimizer comprend une [source de données Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) intégrée qui donne un accès direct aux attributs du profil client en temps réel. Cela couvre la grande majorité des cas d’utilisation : la lecture des attributs de profil pour la personnalisation ou la vérification des champs de consentement et de préférence. Vous pouvez également configurer des [sources de données externes](../datasource/external-data-sources.md) pour appeler des API tierces au moment de l’exécution du parcours, par exemple pour récupérer un score de fidélité en temps réel, une recommandation de produit ou un niveau de stock de magasin qui n’est pas enregistré dans Adobe Experience Platform.

>[!NOTE]
>L’accès direct aux données d’événement d’expérience via la source de données Adobe Experience Platform intégrée est obsolète et progressivement désactivé. [En savoir plus](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/orchestrate-journeys/journey-use-cases/exp-event-lookup){target="_blank"}.

La configuration des sources de données est une tâche administrative qui déverrouille la couche de données complète pour les créateurs et créatrices de parcours et les spécialistes du marketing. Une fois qu’un champ est exposé via une source de données, il devient disponible dans le créateur de conditions de parcours, dans les éditeurs de personnalisation de message et dans les règles de prise de décision sur les offres, sans nécessiter de travail d’ingénierie supplémentaire au moment de la création du parcours.

➡️ [En savoir plus sur la configuration des sources de données](../datasource/about-data-sources.md)

+++

+++ Vérifier les jeux de données de suivi, de commentaires et de parcours

Vérifiez que les jeux de données générés par le système Journey Optimizer sont disponibles dans l’espace de travail Jeux de données. Exécutez des parcours et des campagnes de test, puis utilisez le requêteur pour vérifier que les événements d’envoi, d’ouverture, de clic et de rebond sont enregistrés et que les événements et les états d’étape de parcours sont capturés correctement. Utilisez ces jeux de données pour la surveillance, le dépannage et l’optimisation des parcours en continu.

➡️ [En savoir plus sur les requêtes dans Journey Optimizer](get-started-queries.md)

+++

## Considérations relatives aux mécanismes de sécurisation et à la conception des données {#guardrails}

Certains mécanismes de sécurisation et limitations du produit peuvent influencer la manière dont vous concevez votre modèle de données et vos parcours. Révisez-les au plus tôt pour éviter d’avoir à les retravailler ultérieurement.

>[!IMPORTANT]
>Reportez-vous toujours à la page [Mécanismes de sécurisation et limitations de Journey Optimizer](../start/guardrails.md) pour obtenir les dernières informations. Les résumés ci-dessous mettent en évidence des éléments clés, mais ils peuvent évoluer au fil du temps.

### Jeux de données système et TTL Journey Optimizer {#datasets-ttl}

Journey Optimizer crée plusieurs jeux de données générés par le système pour le tracking, les commentaires et les événements d’étape de parcours. Depuis février 2025, un mécanisme de sécurisation de durée de vie (TTL) est déployé sur certains de ces jeux de données, ce qui peut affecter la durée de conservation des données à des fins d’analyse et de dépannage.

➡️ [En savoir plus sur les mécanismes de sécurisation de la TTL du jeu de données](datasets-ttl.md)

### Segmentation en streaming et événements Journey Optimizer {#streaming-segmentation}

À compter du 1er novembre 2024, la segmentation en streaming ne prend plus en charge les événements d’envoi et d’ouverture provenant des jeux de données de tracking et de feedback de Journey Optimizer. Pour des cas d’utilisation tels que le capping de la fréquence et la gestion de la fatigue, utilisez les [Règles métier](../conflict-prioritization/rule-sets.md) au lieu des segments de streaming en fonction des événements d’envoi/d’ouverture.

➡️ [En savoir plus sur les jeux de données](get-started-datasets.md)

### Recherche et prise de décision sur le jeu de données {#lookup-guardrails}

La recherche de jeux de données est idéale pour les attributs qui changent fréquemment (inventaire, tarification, météo) ou les données qui n’ont pas besoin d’être stockées sur le profil client en temps réel. Consultez les mécanismes de sécurisation spécifiques au produit, tels que les limites de taille des jeux de données et les limites de requête dans la documentation appropriée avant de concevoir votre stratégie de recherche.

➡️ [En savoir plus sur les jeux de données de recherche](lookup-aep-data.md)

## Exemple : préparation de données pour un parcours d’accueil {#example}

L’exemple suivant montre le fonctionnement conjoint des concepts de cette page dans un scénario simple.

1. Un ou une spécialiste de l’ingénierie de données crée un [schéma de profil individuel XDM](get-started-schemas.md) pour les attributs clientèle (nom, e-mail, niveau de fidélité, consentement) et un schéma XDM ExperienceEvent pour les événements d’inscription web.
1. Des [jeux de données activés pour le profil](get-started-datasets.md) sont créés pour chaque schéma : un pour les attributs CRM et un pour les événements d’inscription.
1. Les équipes web et mobiles diffusent les événements d’inscription via le SDK Web Adobe Experience Platform. Les données de CRM sont ingérées via un [ connecteur source](../start/get-started-sources.md).
1. Un administrateur ou une administratrice configure la [source de données Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md) dans Journey Optimizer et expose les champs tels que `profile.person.name.firstName`, `profile.personalEmail.address` et `profile.loyaltyTier`.
1. Un ou une spécialiste marketing [crée un parcours de bienvenue](../building-journeys/journey-gs.md) qui écoute un événement d’inscription et utilise ces attributs de profil pour [personnaliser l’e-mail de bienvenue](../personalization/personalize.md). Journey Optimizer écrit des événements d’envoi et d’ouverture dans les jeux de données de tracking et consigne la progression du parcours dans les jeux de données d’événement d’étape de parcours.
1. Un développeur ou une développeuse utilise le [requêteur](get-started-queries.md) pour vérifier que les événements se suivent correctement et analyse les performances (ouvertures, clics, délai d’envoi). L’équipe ajuste le parcours et le contenu en fonction de ces informations.

Ce flux illustre la manière dont les schémas, les jeux de données, les sources de données et les requêtes sont associés dans un cas d’utilisation complet et accessible aux débutantes et débutants.

## Ressources connexes {#related-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

**Commencer avec les schémas**

Découvrez comment créer des schémas XDM dans Adobe Experience Platform, choisissez la classe et les groupes de champs appropriés, et modélisez vos attributs de profil et vos événements comportementaux.

[En savoir plus](get-started-schemas.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg)

**Utiliser les jeux de données**

Découvrez comment créer des jeux de données d’événement et activés pour les profils, surveillez l’ingestion des données et explorez les jeux de données générés par le système que Journey Optimizer crée automatiquement pour le tracking, les commentaires et les événements d’étape de parcours.

[En savoir plus](get-started-datasets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Configuration des sources de données**

Conseils détaillés sur la configuration de la source de données Adobe Experience Platform intégrée et des sources de données externes facultatives pour exposer les champs de profil et les réponses d’API externes dans vos parcours.

[En savoir plus](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

**Utiliser des données Adobe Experience Platform (recherche)**

Découvrez comment enrichir les messages au moment de l’exécution avec des données de référence ou transactionnelles provenant de jeux de données AEP, sans stocker ces données sur le profil client en temps réel.

[En savoir plus](lookup-aep-data.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Commencer avec les requêtes**

Utilisez le service de requête pour analyser les jeux de données Journey Optimizer, vérifier que les événements se déroulent correctement et créer des requêtes de création de rapports sur les données d’envoi, d’ouverture, de clic et de rebond.

[En savoir plus](get-started-queries.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Commencer avec les profils**

Découvrez le fonctionnement du profil client en temps réel dans Journey Optimizer et comment parcourir, inspecter et valider les profils clientèle individuels dans l’UI de Platform.

[En savoir plus](../audience/get-started-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Tutoriel : vue d’ensemble de la configuration des données**

Une vidéo destinée aux débutants et débutantes sur la configuration des données dans Journey Optimizer, présentant les schémas, les jeux de données et les sources de bout en bout.

[Regarder le tutoriel](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/data-management/set-up-data-overview){target="_blank"}
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

**Tutorial sur la création de jeux de données et l’ingestion de données**

Tutoriel pratique montrant comment créer des jeux de données dans Adobe Experience Platform et ingérer des données à l’aide des connecteurs source, avec des instructions détaillées que vous pouvez suivre dans votre propre sandbox.

[Regarder le tutoriel](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/data-management/create-datasets-and-ingest-data){target="_blank"}
:::

::::
