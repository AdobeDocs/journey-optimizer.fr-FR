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
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: bfb28a935dffca7c381fe72339abc840d2ab297b
workflow-type: tm+mt
source-wordcount: 10185
ht-degree: 6%

---

# Exemples de configurations de fournisseur {#vendor-integration}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment utiliser les intégrations Adobe Journey Optimizer avec toute plateforme externe qui expose une API compatible, avec des mécanismes de sécurisation opérationnels et des modèles de fournisseur illustratifs pour guider votre configuration.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Il est de la responsabilité des clients de s’assurer que leur utilisation de la fonctionnalité Intégrations AJO et des fournisseurs tiers ou intégrations associés est conforme à toutes les lois et réglementations applicables, telles que la loi HIPAA.

>[!ENDSHADEBOX]

## Navigation rapide {#quick-navigation}

Utilisez ces liens groupés pour accéder rapidement au modèle de fournisseur approprié :

* **Système de gestion de contenu :** [Contentful](#contentful), [Sitecore](#sitecore), [Salsify](#salsify), [Contentstack](#contentstack), [Akeneo](#akeneo), [Magnolia](#magnolia)
* **Fidélité et récompenses :** [Voucherify](#voucherify), [Talon.One](#talon-one), [Antavo](#antavo), [Fidélité Salesforce](#salesforce-loyalty), [Capillaire](#capillary)
* **Modèles, personnalisation et recommandations :** [Stensul](#stensul), [Marigold](#marigold), [Adobe Target Recommendations](#adobe-target-recommendations)
* **Données, météo et opérations :** [AccuWeather](#accuweather), [ShipStation](#shipstation), [RevenueCat](#revenuecat), [Databricks](#databricks)
* **Examens, consentement et réseaux sociaux :** [Bynder](#bynder), [Trustpilot](#trustpilot), [Bazaarvoice](#bazaarvoice), [OneTrust](#onetrust), [Meta](#meta), [Aprimo](#aprimo), [Epsilon (Epsilon3)](#epsilon)

## Contenu et CMS {#content-and-cms}

### Content {#contentful}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par ou formellement pris en charge par Contentful. Confirmez les détails actuels de l’API avec la documentation Contentful.

>[!BEGINSHADEBOX]

Contentful est un CMS découplé pour les entrées structurées et les ressources sur REST ou GraphQL, de sorte que Journey Optimizer puisse extraire du contenu au moment de l’envoi ou de l’ouverture.

Les cas d’utilisation standard incluent des blocs principaux localisés, du texte de remplacement et des CTA dans des e-mails, ainsi que des entrées de produit ou de promotion dans des modules dynamiques. Une autre tendance courante consiste à récupérer une entrée spécifique par ID pour les messages personnalisés.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de Contentful.

Les prérequis suivants sont requis :

* Espace contenu avec accès à l’API de diffusion et clé API orientée lecture.
* Effacer les types de contenu et les identifiants de champ ; accès administrateur dans Journey Optimizer pour créer des intégrations.

Les restrictions et exclusions suivantes s’appliquent :

* Les API Contentful paginées ou à liste large conviennent mal à ce modèle ; préférez les appels de récupération qui ciblent une entrée ou une ressource spécifique.
* L’écriture différée ou la synchronisation bidirectionnelle ne font pas partie de cet exemple.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Configurez **GET** avec l’API de diffusion de contenu et votre jeton de diffusion, collez l’exemple JSON, mappez les champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’URL de l’API de diffusion de contenu (CDA) `https://cdn.contentful.com/spaces/{space_id}/environments/{environment_id}/entries/{entry_id}`

1. Sélectionnez la méthode HTTP : **GET**.

1. Ajoutez une authentification. Définissez le paramètre **`access_token`** **requête** sur votre jeton API de diffusion de contenu, comme illustré dans **Exemples de champs d’intégration** ci-dessous. Contentful accepte également le même jeton dans un en-tête `Authorization: Bearer` ; utilisez la prise en charge de vos champs d’intégration quelle qu’elle soit.

1. Ajoutez des variables de chemin d’accès si nécessaire (par exemple, ID d’entrée, paramètre régional).

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation.

1. Configurez le délai d’expiration et la mise en cache selon vos besoins.

1. Tester la connexion et activer.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Exemples de champs d’intégration (alignez-vous sur l’[API de diffusion de contenu](https://www.contentful.com/developers/docs/references/content-delivery-api/){target="_blank"} pour votre espace et votre environnement) :

| Champ | Valeur |
| -- | -- |
| **URL** | `https://cdn.contentful.com/spaces/{{spaceID}}/environments/{{environment_id}}/entries/{{entry_id}}` |
| Payload de réponse | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |
| Stratégie | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Méthode HTTP** | `GET` |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `spaceID` | `spaceID` | `<YOUR_SPACE_ID>` |
| `environment_id` | `environment_id` | `<YOUR_ENV_ID>` |
| `entry_id` | `entry_id` | `<YOUR_ENTRY_ID>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | `access_token` | `<YOUR_API_KEY>` | Paramètre de requête |

+++

### Sitecore {#sitecore}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par Sitecore ni formellement pris en charge par celui-ci. Confirmez les détails actuels de l’API avec la documentation Sitecore.

>[!BEGINSHADEBOX]

Sitecore Content Hub et les API cloud associées prennent en charge les flux de métadonnées et de téléchargement de type gestion des ressources numériques. L’exemple de modèle ci-dessous est centré sur un identifiant d’ordre de téléchargement.

Les cas d’utilisation standard incluent les métadonnées de ressource ou de téléchargement dans le contenu des e-mails et l’alignement sur les workflows de gestion des ressources numériques gérés dans Sitecore.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de Sitecore.

Les prérequis suivants sont requis :

* URL et informations d’identification du client (porteur ou jeton selon votre surface API).
* Accès administrateur dans Journey Optimizer pour la création d’intégrations.

Les restrictions et exclusions suivantes s’appliquent :

* Les noms d&#39;hôtes et les chemins varient selon le produit Sitecore. Utilisez uniquement les points d’entrée exposés par votre client.
* Les jetons d’accès OAuth, l’actualisation et les durées de vie doivent respecter la politique de sécurité de Sitecore.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Configurez **GET** sur votre chemin d’accès d’ordre de téléchargement, définissez les en-têtes d’autorisation par Sitecore, mappez les `id` à partir du contexte, collez l’exemple JSON, mappez les champs et ajustez les délais d’expiration pour la latence des ressources.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API Content Hub (exemple : télécharger l’ordre par ID). Exemple de modèle d’URL :

   `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{id}`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Utilisez les champs suivants lorsque vous configurez cet exemple d’appel dans Journey Optimizer. Confirmez le nom d’hôte et la version de l’API pour votre produit (Content Hub, XM Cloud, etc.) dans la [documentation de Sitecore](https://doc.sitecore.com/){target="_blank"}.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{{id}}` |
| **Méthode HTTP** | `GET` |
| Payload de réponse | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |
| Stratégie | Configurez les détails au niveau de la politique en fonction de vos besoins. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `id` | `id` | `<id_of_download_order>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |
| Autorisation | Autorisation | Constant | `<token>` du porteur | Oui (activé) |
| If-Modified-Since | If-Modified-Since | Variable | 2019-08-:15:22Z | Non (désactivé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | X-Auth-Token | `<token>` | Header |

+++

### Salsifier {#salsify}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n&#39;est pas maintenu par Salsify ni formellement soutenu par lui. Confirmez les détails actuels de l’API avec la documentation Salsify.

>[!BEGINSHADEBOX]

Salsify est un PIM avec des API pour les produits, les canaux et les ressources numériques.

Les cas d’utilisation standard incluent les attributs de produit ou les URL de médias dans les e-mails et les messages alignés sur les données de catalogue syndiquées.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de Salsify.

Les prérequis suivants sont requis :

* Jeton API et contexte de l’organisation ; ID de produit résolvables à partir du profil ou du contexte.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Catalogues très volumineux : évitez les points d’entrée de liste en bloc si les intégrations s’attendent à une récupération par entité.
* La visibilité des attributs peut être limitée par les autorisations des rôles Salsify.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Préférez la récupération d’un seul produit aux appels de catalogue en bloc, définissez l’authentification du porteur, collez l’exemple JSON, mappez les champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API du produit Salsify. Exemple de modèle d’URL :

   `https://api.salsify.com/v1/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Certaines références plus anciennes ont réutilisé un chemin de style d’ordre de téléchargement pour Salsify ; votre client peut plutôt utiliser `https://app.salsify.com/api/v1/orgs/{org_id}/products/{salsify_id}` ou un chemin similaire. Confirmez dans [Développement Salsify](https://developers.salsify.com/){target="_blank"}.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://app.salsify.com/api/v1/orgs/{{org_id}}/products/{{salsify_id}}` |
| **Méthode HTTP** | `GET` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Payload de réponse** | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `org_id` | `org_id` | `<org_id>` |
| `salsify_id` | `salsify_id` | `<salsify_id>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (paramètre par défaut) | Content-Type | Constant | application/json | Oui (activé) |
| Autorisation | Autorisation | Constant | `Bearer <YOUR_TOKEN_HERE>` | Oui (activé) |
| If-Modified-Since | If-Modified-Since | Variable | 2019-08-:15:22Z | Non (désactivé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | `apiKey` | `<your_api_key>` | Header |

+++

### Contentstack {#contentstack}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par ou formellement pris en charge par Contentstack. Confirmez les détails de l’API actuelle avec la documentation de Contentstack.

>[!BEGINSHADEBOX]

Contentstack est un CMS découplé ; la diffusion REST est typique du mappage de champs JSON dans Journey Optimizer.

Un cas d’utilisation type consiste à utiliser des entrées pour des bannières ou des promotions avec des paramètres qui incluent le paramètre régional.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de Contentstack.

Les prérequis suivants sont requis :

* Clé API de pile, jeton de diffusion, nom d’environnement et UID de type de contenu.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Ce modèle utilise le format JSON REST pour le mappage des champs ; la diffusion GraphQL suit un chemin d’intégration différent.
* Utilisez des jetons de diffusion appropriés pour la production ; les flux de prévisualisation et de publication ne sont pas interchangeables.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Ajoutez des en-têtes `api_key` et `access_token` comme Contentstack l’exige, incluez le paramètre de requête `environment`, collez un exemple de code JSON, mappez des champs, testez et activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API de diffusion de contenu. Exemple de modèle d’URL :

   `https://cdn.contentstack.io/v3/content_types/{content_type_uid}/entries/{entry_uid}`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Exemples de champs d’intégration. Voir [API de diffusion de contenu Contentstack](https://www.contentstack.com/docs/developers/apis/content-delivery-api/){target="_blank"}.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://cdn.contentstack.io/v3/content_types/{{content_type_uid}}/entries/{{entry_uid}}` |
| **Méthode HTTP** | `GET` |
| Payload de réponse | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |
| Stratégie | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| En-têtes | Aucun en-tête supplémentaire nécessaire. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `content_type_uid` | Type de contenu UID | `<your_content_type_uid>` |
| `entry_uid` | UID d’entrée | `<your_entry_uid>` |

**Authentification**

| Nom de la clé | Valeur de clé | Ajouter à |
| --- | --- | --- |
| `api_key` | `<YOUR_STACK_API_KEY>` | Header |
| `access_token` | `<YOUR_DELIVERY_TOKEN>` | Header |

Contentstack attend **les deux** clés comme en-têtes pour les demandes de diffusion.

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `environment` | Nom de l’environnement | Variable | `<your_environment_name>` | Oui (activé) |

+++

### Akeneo {#akeneo}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Elle n’est pas gérée par Akeneo et n’est pas officiellement soutenue par celui-ci. Confirmez les détails actuels de l’API avec la documentation Akeneo.

>[!BEGINSHADEBOX]

Akeneo PIM expose les API REST pour les produits, les attributs et les médias.

Les cas d’utilisation standard incluent les données de produit régies dans les modules d’e-mail et les attributs pour un canal donné dans les parcours.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites d’Akeneo.

Les prérequis suivants sont requis :

* URL de base PIM et client OAuth ; UUID de produit ou stratégie d’identifiant.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Les réponses PIM peuvent être volumineuses. Mappez uniquement les attributs requis pour la personnalisation.
* Les opérations d’écriture se situent en dehors des exemples de personnalisation en lecture seule standard.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Utilisez **GET** avec le jeton porteur, demandez uniquement les options d’attribut nécessaires dans les indicateurs de requête, collez l’exemple JSON, mappez un jeu d’attributs minimal, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API REST Akeneo. Exemple de modèle d’URL :

   `https://{pim-host}/api/rest/v1/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Exemple de modèle : `https://{pim-host}/api/rest/v1/products-uuid/{uuid}` avec `Accept: application/json`. Voir [ API Akeneo ](https://api.akeneo.com/){target="_blank"}.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://{{your-akeneo-domain}}.com/api/rest/v1/products-uuid/{{uuidProduct}}` |
| **Méthode HTTP** | `GET` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Payload de réponse** | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `uuidProduct` | UUID | `<product_uuid>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Autorisation | Autorisation | Constant | `Bearer <YOUR_TOKEN>` | Oui (activé) |
| Accept | Accept | Constant | application/json | Oui (activé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `with_attribute_options` | Inclure les options d’attribut | Variable | False | Non (désactivé) |
| `with_quality_scores` | Inclure les scores de qualité | Variable | False | Non (désactivé) |
| `with_completenesses` | Inclure les éléments complets | Variable | False | Non (désactivé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | Autorisation | `Bearer <YOUR_ACCESS_TOKEN>` | Header |

+++

### Magnolia {#magnolia}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par Magnolia et n’est pas formellement soutenu par celle-ci. Confirmez les détails actuels de l’API avec la documentation de Magnolia.

>[!BEGINSHADEBOX]

Magnolia offre des points d’entrée de diffusion découplés et REST en fonction du déploiement.

Un cas d’utilisation type consiste à diffuser des nœuds de contenu ou des fragments pour les modules marketing.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de Magnolia.

Les prérequis suivants sont requis :

* URL de l’instance et jeton ou authentification de base ; espace de travail et chemins de diffusion.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Les URL de diffusion REST dépendent des modules et de la configuration Magnolia installés.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Utilisez le modèle d’URL de diffusion publique que vos modules exposent, authentifiez selon les conseils de Magnolia (diffusion anonyme par rapport au jeton pour le contenu protégé), collez un exemple de JSON, mappez des champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide du REST Magnolia (diffusion). Exemple de modèle d’URL :

   `https://{author-or-public}/.rest/delivery/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Exemple de modèle : URL de type tour de diffusion `https://{domain}/magnoliaAuthor/.rest/delivery/...` ou publique. Vos chemins d’accès dépendent des modules installés. Voir la [documentation Magnolia](https://docs.magnolia-cms.com/){target="_blank"}.

| Champ | Valeur |
| --- | --- |
| **URL** | `http://{{your-domain}}/magnoliaAuthor/.rest/delivery/<myEndpoint>/travel/@nodes` |
| **Méthode HTTP** | `GET` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Payload de réponse** | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | Constant | application/json | Oui (activé) |
| Accept | Accept | Constant | application/json | Oui (activé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | Autorisation | `<bearer_token>` | Header |

Remarque : l’API de diffusion doit utiliser le rôle rest-anonyme pour le contenu qui ne nécessite pas de connexion. Pour un accès sécurisé aux données protégées, une méthode plus robuste telle que les jetons API ou OAuth 2.0 est préférable.

+++


## Fidélité et récompenses {#loyalty-and-rewards}

### Voucherify {#voucherify}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par Voucherify ni formellement pris en charge par celui-ci. Confirmez les détails actuels de l’API avec la documentation de la pièce jointe.

>[!BEGINSHADEBOX]

Voucherify fournit des API REST de promotion et de fidélité (campagnes, bons, programmes de fidélité).

Les cas d’utilisation standard incluent la lecture de l’état de fidélité ou de promotion des offres dans le contenu et l’affichage du niveau ou de la balance le cas échéant.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de la bon.

Les prérequis suivants sont requis :

* Identifiant et secret de l’application (par région/cluster) ; clarté sur les points d’entrée de fidélité ou de campagne que vous appelez.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Évitez d’exposer les identifiants de promotion ou de campagne internes dans les erreurs rencontrées par le client ou la cliente ou le contenu du message.
* Des limites tarifaires au niveau de l’application s’appliquent. Configurez les reprises et la mise en cache selon les conseils de Bons.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Définissez l’URL de base de votre cluster, ajoutez les en-têtes requis (`X-APP-ID`, `X-APP-TOKEN`), limitez les points d’entrée de liste avec des filtres ou des identifiants, collez un exemple de JSON, mappez des champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide des API REST/Loyalty. Par [Voucherify](https://docs.voucherify.io/){target="_blank"}, définissez l’hôte **cluster** et les chemins d’accès pour votre région. Exemple de modèle d’URL :

   `https://{cluster}.voucherify.io/`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Exemples de champs d’intégration. Référence complète : [API Voucherify](https://docs.voucherify.io/reference/introduction){target="_blank"}.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://{{cluster}}.voucherify.io/v1/loyalties/{{campaignId}}/members` |
| **Méthode HTTP** | `GET` |
| Payload de réponse | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |
| Stratégie | Configurez les détails au niveau de la politique en fonction de vos besoins. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `cluster` | `cluster` | `<your_cluster>` |
| `campaignId` | `campaignId` | `<loyalty_campaign_Id>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |
| X-APP-ID | X-APP-ID | Constant | `<YOUR-APP-ID>` | Oui (activé) |
| X-Voucherify-Channel | X-Voucherify-Channel | Constant | Documentation de la confirmation | Non (désactivé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `limit` | `limit` | Variable | 10 | Non (désactivé) |
| `page` | `page` | Variable | 1 | Non (désactivé) |
| `customer` | `customer` | Variable | `<customer_identifier>` | Non (désactivé) |
| `created_at` | `created_at` | Variable | `<iso8601_date>` | Non (désactivé) |
| `updated_at` | `updated_at` | Variable | `<iso8601_date>` | Non (désactivé) |
| `order` | `order` | Variable | `<sort_field>` | Non (désactivé) |
| `code` | `code` | Variable | `<loyalty_card_code>` | Non (désactivé) |
| `ids` | `ids` | Variable | `<array_of_ids>` | Non (désactivé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | X-APP-TOKEN | `<YOUR-APP-TOKEN>` | Header |

+++

### Talon.One {#talon-one}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par Talon.One et n’est pas formellement pris en charge par celui-ci. Confirmez les détails actuels de l’API avec la documentation de Talon.One.

>[!BEGINSHADEBOX]

Talon.One est un moteur de règles de promotion et de fidélité qui comprend des API REST pour les sessions, les effets et les profils.

Les cas d’utilisation standard incluent des promotions au niveau du panier ou du profil dans du contenu personnalisé et une progression de la fidélité ou un affichage de récompenses.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de Talon.One.

Les prérequis suivants sont requis :

* Clé API et URL de base spécifique au déploiement ; identifiants de la portée de l’application ou de la campagne.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Les flux de sessions volumineux peuvent nécessiter un mappage soigneux au modèle de requête d’intégration .
* Observez les limites de taux de Talon.One et les conseils d&#39;idempotence.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Utilisez **GET** sur le profil ou le chemin d’accès dont vous avez besoin, définissez les `Authorization: ApiKey-v1 <key>` comme documenté, collez un exemple de JSON, mappez des champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API d’intégration Talon.One. Exemple de modèle d’URL :

   `https://{your-domain}.talon.one/v1/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

| Champ | Valeur |
| --- | --- |
| **URL** | `https://{{your-deployment}}.talon.one/v1/customer_profiles/{{integrationId}}/achievements/{{achievementId}}` |
| **Méthode HTTP** | `GET` |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `your-deployment` | `your-deployment` | `<your_deployment>` |
| `integrationId` | `integrationId` | `<integrationId>` |
| `achievementId` | `achievementId` | `<achievementId>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `progressStatus` | `progressStatus` | Variable | en cours / terminé / expiré | Non (désactivé) |
| `startDate` | `startDate` | Variable | 2024-05-:04:05+07:00 | Non (désactivé) |
| `endDate` | `endDate` | Variable | 2024-05-:04:05+07:00 | Non (désactivé) |
| `pageSize` | `pageSize` | Variable | `<default_page_size>` | Non (désactivé) |
| `skip` | `skip` | Variable | `<items_to_skip>` | Non (désactivé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | Autorisation | `<YOUR_API_KEY>` ApiKey-v1 | Header |

+++

### Antavo {#antavo}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par Antavo et n’est pas formellement soutenu par celui-ci. Confirmez les détails actuels de l’API avec la documentation Antavo.

>[!BEGINSHADEBOX]

Antavo est une plateforme de fidélité d’entreprise avec des API REST pour les membres, les récompenses et les événements.

Les cas d’utilisation standard incluent les points, le niveau ou les récompenses dans les e-mails ou les notifications push et les offres pilotées par l’état de fidélité.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites d’Antavo.

Les prérequis suivants sont requis :

* Empilage des identifiants d’URL et d’API ; identifiants de programme ou de boutique selon les besoins.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Les PII des clients doivent être traitées dans le cadre des accords Antavo et de vos politiques de confidentialité.
* Confirmez les versions d’API et les points d’entrée stables avec Antavo pour votre environnement.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Configurez **GET** avec l’authentification du fournisseur (par exemple, la clé API dans la requête), évitez d’exposer les informations d’identification personnelles dans la politique, collez l’exemple JSON, mappez les champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API Antavo Enterprise.

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Les exemples de champs d’intégration utilisent l’hôte **staging** ; la production utilise votre nom d’hôte de pile Antavo. Voir la [documentation Antavo](https://antavo.com/docs/){target="_blank"}.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://api.staging.antavo.com/customers/{{customer_id}}/activities/offers` |
| **Méthode HTTP** | `GET` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Payload de réponse** | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `customer_id` | `customer_id` | `<customer_id>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |
| Accept | Accept | Constant | application/json | Non (désactivé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | `api_key` | `<YOUR_API_KEY>` | Paramètre de requête |

+++

### Fidélité à Salesforce {#salesforce-loyalty}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par Salesforce ni formellement pris en charge par celui-ci. Confirmez les détails actuels de l’API avec la documentation de Salesforce.

>[!BEGINSHADEBOX]

La gestion de la fidélité Salesforce expose les API REST sur la plateforme Salesforce pour les membres, les programmes et les transactions.

Les cas d’utilisation standard incluent l’affichage du niveau, des points ou des avantages dans les parcours et l’alignement des messages avec les données de gestion de la relation client et de fidélité.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de la fidélité à Salesforce.

Les prérequis suivants sont requis :

* Instance Salesforce, application connectée ou utilisateur de l’intégration, et OAuth approprié à votre organisation.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Les limites de l’API Salesforce et l’actualisation du jeton OAuth doivent être conçues dans votre intégration.
* Les règles de sécurité et de partage au niveau du champ régissent les champs qui apparaissent dans les réponses de l’API.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Utilisez le point d’entrée d’intégration de fidélité approuvé par votre équipe, exécutez Salesforce OAuth, collez l’exemple JSON, mappez des champs, respectez les limites d’API composites, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide du REST Salesforce Loyalty Management. Exemple de modèle d’URL :

   `https://{instance}.salesforce.com/services/data/vXX.X/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Utilisez l’opération GET Loyalty Management **profil de membre** documentée pour la version de l’API de votre organisation. Les chemins incluent le programme et les identifiants des membres. Voir [Développeurs ](https://developer.salesforce.com/){target="_blank"}.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://{{your-instance}}.my.salesforce.com/services/data/{{version}}/connect/loyalty/management/members` |
| **Méthode HTTP** | `GET` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Payload de réponse** | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |
| `version` | `version` | `version` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |
| Accept | Accept | Constant | application/json | Non (désactivé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `membershipNumber` | `membershipNumber` | Variable | `<membership_number>` | Non (désactivé) * |
| `membershipId` | `membershipId` | Variable | `<membership_id>` | Non (désactivé) * |
| `posMemId` | `posMemId` | Variable | `<pos_mem_id>` | Non (désactivé) * |

\* Au moins un des trois est requis.

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | Autorisation | `<access_token>` | Header |

+++

### Capillaire {#capillary}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par Capillary ni formellement soutenu par celle-ci. Confirmez les détails actuels de l’API avec la documentation Capillary.

>[!BEGINSHADEBOX]

Capillary fournit des API de fidélité et d’engagement courantes dans les piles de vente au détail.

Les cas d’utilisation standard incluent des points, des niveaux ou des offres dans des parcours personnalisés.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de Capillary.

Les prérequis suivants sont requis :

* Hôte et authentification de l’API (requêtes souvent signées ; suivez la documentation Capillary).
* Identifiants de programme pour votre point d’entrée.

Les restrictions et exclusions suivantes s’appliquent :

* Les schémas d’authentification et les hôtes régionaux varient selon le déploiement. Confirmez avec Capillary pour votre pile.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Configurez des en-têtes tels que `CAP-API-ACCESS-TOKEN` selon les besoins, collez l’exemple JSON, mappez des champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide des API Capillary.

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Exemple : `https://ushc.intouch.capillarytech.com/api/v3/rewards/{reward_id}` (l’hôte varie selon la région). Validez le schéma d’hôte et d’authentification avec [Capillaire](https://capillarytech.com/){target="_blank"}.


| Champ | Valeur |
| --- | --- |
| **URL** | `https://ushc.intouch.capillarytech.com/api/v3/rewards/{{reward_id}}` |
| **Méthode HTTP** | `GET` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Payload de réponse** | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `reward_id` | ID de récompense | `<your_reward_id>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | Constant | application/json | Oui (activé) |
| CAP-API-ACCESS-TOKEN | Jeton d’accès | Constant | `<YOUR_ACCESS_TOKEN>` | Oui (activé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | CAP-API-ACCESS-TOKEN | `<YOUR_ACCESS_TOKEN>` | Header |

+++


## Modèles et messages {#templates-and-messaging}

### Stensul {#stensul}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n&#39;est pas entretenu par Stensul ou formellement soutenu par lui. Confirmez les détails actuels de l’API avec la documentation de Stensul.

>[!BEGINSHADEBOX]

Stensul est une plateforme de création d’e-mails pour les modèles approuvés ; Journey Optimizer peut utiliser des métadonnées de modèle et des régions structurées par le biais de son API.

Les cas d’utilisation standard incluent l’importation de modèles approuvés et le mappage de régions à des attributs de profil, ainsi que la réutilisation de blocs régis pour des versions de campagne évolutives.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de Stensul.

Les prérequis suivants sont requis :

* Compte Stensul avec accès à l’API et modèles publiés avec jetons définis.
* Accès administrateur dans Journey Optimizer pour la création d’intégrations.

Les restrictions et exclusions suivantes s’appliquent :

* La modification statique par WYSIWYG des modèles Stensul dans Journey Optimizer n’est pas abordée ici.
* HTML volumineux ou complexe dans les payloads de modèle peut nécessiter une révision et une désinfection de la sécurité.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration.

1. Configurez le point d’entrée à l’aide de l’URL de l’API Modèles Stensul . Exemple de modèle d’URL :

   `https://api.stensul.com/v1/templates/{template_id}`

1. Configurez l’authentification (clé API ou documentation OAuth par API Stensul).

1. Définir des variables de chemin d’accès , par exemple un identifiant de modèle.

1. Collez un exemple de réponse JSON pour la détection de champ.

1. Mappez les champs de modèle obligatoires aux champs de personnalisation Journey Optimizer.

1. Tester la connexion et activer.

### Marigold {#marigold}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n&#39;est pas entretenu par Marigold ou formellement soutenu par lui. Confirmez les détails actuels de l’API avec la documentation Marigold .

>[!BEGINSHADEBOX]

Marigold expose les API de fidélité et d’engagement ; les hôtes diffèrent selon la géographie (noms d’hôtes de modules UE et US).

Un cas d’utilisation type consiste à enrichir les messages avec des données de fidélité ou de préférence provenant des programmes Marigold.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limitations de Marigold.

Les prérequis suivants sont requis :

* URL de base et informations d’identification provenant de votre contrat ; utilisateur de l’API avec les moindres privilèges lorsque cela est possible.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Les points d’entrée varient selon le produit Marigold. Effectuez la validation avec la prise en charge de Marigold pour votre déploiement.
* Les données personnelles contenues dans les réponses doivent être conformes à votre DPA et à vos politiques de conservation.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Pointez sur l’hôte Marigold pour votre région, définissez l’authentification (l’exemple ci-dessous utilise `X-Api-Key` avec la clé et le secret), collez l’exemple JSON, mappez des champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API REST Marigold.

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

1. Marigold utilise 2 points d’entrée en fonction de la zone géographique pour laquelle l’instance client est active :

   * Europe : `https://{{customername}}.module.slgnt.eu`
   * USA : `https://{{customername}}.module.slgnt.us`

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

L’hôte de base dépend de la région (par exemple, `https://{{customername}}.module.slgnt.eu` ou `https://{{customername}}.module.slgnt.us`). Confirmez les chemins avec Marigold pour votre déploiement.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://{{customername}}.module.slgnt.{{locale}}/Portal/Api/organizations/{{organization}}/content/{{api_name}}` |
| **Méthode HTTP** | `GET` |
| Payload de réponse | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |
| Stratégie | Configurez les détails au niveau de la politique en fonction de vos besoins. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `customername` | `customername` | `<your_name>` |
| `locale` | `locale` | `eu` / `us` |
| `organization` | `organization` | `<your_organization>` |
| `api_name` | `api_name` | `<api_name>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | X-Api-Key | `<apiKey>:<apiSecret>` | Header |

+++

### Recommandations Adobe Target {#adobe-target-recommendations}

>[!IMPORTANT]
>
>Cette configuration est un modèle fourni à titre d’illustration et testé par l’équipe Adobe Journey Optimizer. Adobe Target Recommendations est un produit Adobe distinct avec son propre cycle de publication et son propre contrôle de version des API. Confirmez toujours les détails actuels de l’API avec la [documentation Adobe Target destinée aux développeurs](https://experienceleague.adobe.com/en/docs/target-dev/developer/overview) avant de procéder au déploiement en production.

>[!BEGINSHADEBOX]

Adobe Target comprend des recommandations et des API de diffusion pour les expériences côté serveur ou intégrées, sous réserve des droits.

Les cas d’utilisation standard incluent l’injection de recommandations dans les expériences que vous créez dans Journey Optimizer et l’alignement des clés avec le contexte du profil ou d’Experience Platform.

<!--
➡️ After you activate the integration, learn how to [use Adobe Target data in message templates](integrations-personalization.md#use-adobe-target-in-templates).
-->

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites des recommandations Adobe Target.

Les prérequis suivants sont requis :

* Target avec Recommendations ; organisation IMS et authentification prise en charge.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Les API de recommandation et de diffusion nécessitent des paramètres spécifiques (par exemple, des identifiants de mbox ou de produit). Consultez la documentation d’Adobe Target.
* Réglez la latence et la mise en cache pour votre volume d’envoi et votre cas d’utilisation.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Les appels de diffusion sont souvent **POST** avec un corps JSON. Configurez OAuth par [authentification de la cible](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication){target="_blank"}, collez un exemple de réponse, mappez des champs, testez sous le volume attendu.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide des API Target Recommendations/delivery.

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

| Champ | Valeur |
| --- | --- |
| **URL** | `https://{{client}}.tt.omtrdc.net/rest/v1/delivery` |
| Stratégie | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Méthode HTTP** | `POST` |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `client` | `client` | `<client_name>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| client | client | Variable | `<customer_client_code>` | Oui (activé) |
| sessionId | sessionId | Variable | ` <session_identifier>` | Oui (activé) |

**Authentification**

Reportez-vous à [Configuration de l’authentification Target](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication) et ajoutez JSON à la payload.

**Payload de requête**

```Sample Request Payload JSON
{
  "id": {
    "tntId": "<YOUR_TENANT_ID>"
  },
  "context": {
    "channel": "web",
    "address": {
      "url": "https://example.com/store.html"
    },
    "screen": {
      "width": 1200,
      "height": 1400
    }
  },
  "experienceCloud": {
    "analytics": {
      "logging": "server_side",
      "supplementalDataId": "<supDataId>",
      "trackingServer": "sstats.adobe.com"
    }
  },
  "execute": {
    "pageLoad": {
      "parameters": {
        "pageType": "checkout",
        "preferredCurrency": "$"
      }
    },
    "mboxes": [
      {
        "index": 1,
        "name": "orderConfirmPage"
      }
    ]
  },
  "prefetch": {
    "views": [
      {
        "parameters": {
          "ad": "view"
        }
      }
    ],
    "mboxes": {
      "index": 1,
      "name": "SummerOffer"
    }
  }
}
```

+++


## Données, météo et opérations {#data-weather-and-operations}

### AccuWeather {#accuweather}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par AccuWeather et n’est pas formellement pris en charge par celle-ci. Confirmez les détails actuels de l’API avec la documentation AccuWeather.

>[!BEGINSHADEBOX]

AccuWeather expose les API REST de prévision et d’emplacement afin que les messages puissent inclure des fragments de code prenant en compte la météo.

Les cas d’utilisation standard incluent des prévisions courtes dans les e-mails ou les notifications push, et personnalisent le contenu en utilisant des valeurs de prévision liées au profil ou au contexte.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites d’AccuWeather.

Les prérequis suivants sont requis :

* Clé et abonnement à l’API ; clé d’emplacement pour un flux de recherche de ville.
* Accès administrateur dans Journey Optimizer pour la création d’intégrations.

Les restrictions et exclusions suivantes s’appliquent :

* Confirmez la forme de réponse JSON pour votre niveau d’abonnement AccuWeather. Les intégrations mappent les champs des réponses JSON.
* Respectez les limites de débit AccuWeather et la mise en cache recommandée.
* La résolution des `locationKey` nécessite souvent une géolocalisation distincte ou une requête de recherche de ville avant les appels de prévision.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Utilisez **GET** à moins que votre abonnement n’en exige autrement, joignez le paramètre de requête `apiKey`, mappez les `locationKey` et d’autres variables de profile/context, collez l’exemple JSON, mappez des champs, puis testez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API Daily Forecasts. Exemple de modèle d’URL :

   `https://dataservice.accuweather.com/forecasts/v1/daily/{days}day/{locationKey}`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++Exemples de champs d’intégration

Exemples de champs d’intégration. Les détails et les niveaux sont décrits dans la section [API AccuWeather](https://developer.accuweather.com/apis){target="_blank"}. Vous résolvez souvent les `locationKey` avec un appel de recherche d’emplacements distinct (par exemple, `.../locations/v1/cities/search?q={{cityName}}`).

| Champ | Valeur |
| --- | --- |
| **URL** | `https://dataservice.accuweather.com/forecasts/v1/daily/{{days}}day/{{locationKey}}` |
| **Méthode HTTP** | `GET` |
| Payload de réponse | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |
| Stratégie | Configurez les détails au niveau de la politique en fonction de vos besoins. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `days` | `days` | `15` |
| `locationKey` | `locationKey` | `<desired_location_key>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `format` | `format` | Variable | json | Non (désactivé) |
| `language` | `language` | Variable | en-US | Non (désactivé) |
| `details` | `details` | Variable | False | Non (désactivé) |
| `metric` | `metric` | Variable | False | Non (désactivé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | `apiKey` | `<YOUR_API_KEY>` | Paramètre de requête |

+++

### ShipStation {#shipstation}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n&#39;est pas entretenu par ShipStation ni officiellement pris en charge par celle-ci. Confirmez les détails actuels de l&#39;API avec la documentation ShipStation.

>[!BEGINSHADEBOX]

ShipStation propose des API d&#39;expédition et de commande pour les transporteurs, les étiquettes et le suivi.

Les cas d’utilisation standard incluent le statut de la commande, les liens de suivi ou les ETA de diffusion dans les messages transactionnels.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limitations de ShipStation.

Les prérequis suivants sont requis :

* Clé API et secret (authentification de base par documents ShipStation).
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* N’exposez pas les clés API ShipStation dans le contenu du message ; conservez uniquement les informations d’identification dans la configuration de l’intégration.
* Les points d’entrée de liste paginés peuvent ne pas convenir aux intégrations ; préférez les GET à ressource unique lorsque cela est possible.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Ciblez la ressource dont vous avez besoin (commandes ou expéditions), authentifiez-la par [API ShipStation](https://www.shipstation.com/docs/api/){target="_blank"}, collez l’exemple JSON, mappez des champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API REST ShipStation. Exemple de modèle d’URL :

   `https://ssapi.shipstation.com/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

L’exemple suivant **Get Timer** illustre un appel de minutage d’automatisation ShipStation. Utilisez le chemin d’accès et l’authentification exacts de votre guide d’intégration ShipStation lors de leur reproduction dans Journey Optimizer.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://dashboard.sendtric.com/api/v1/timers/{{id}}` |
| **Méthode HTTP** | `POST` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | apiKey | `<your_api_key>` | Header |

**Payload de requête**

```Sample Request Payload
{
    "external_batch_id": "se-28529731",
    "batch_notes": "This is my batch",
    "shipment_ids": [
      "se-28529731"
    ],
    "rate_ids": [
      "se-28529731"
    ]
}
```

+++

### RevenueCat {#revenuecat}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par RevenueCat ni formellement pris en charge par celui-ci. Confirmez les détails actuels de l’API avec la documentation RevenueCat .

>[!BEGINSHADEBOX]

RevenueCat fournit des API de statut d’abonnement et de droits pour les applications.

Un cas d’utilisation type reflète le statut d’abonnement dans les campagnes de cycle de vie lorsque la politique le permet.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de RevenueCat.

Les prérequis suivants sont requis :

* Clé API secrète et identifiants d’application ; mappage stable entre les profils et les ID client RevenueCat.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Protégez les clés API secrètes et suivez vos politiques de rotation.
* Les données d’abonnement et de droit sont sensibles. Respectez les exigences de confidentialité et de consentement.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Appelez le REST **GET** modélisé ci-dessous, authentifiez-vous avec l’en-tête de clé secrète, collez l’exemple JSON, mappez les champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API REST RevenueCat. Exemple de modèle d’URL :

   `https://api.revenuecat.com/v1/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Exemple de modèle : utilisez la méthode **Get a Product** de RevenueCat (ou une méthode GET de produit/droit équivalente) à partir de la [RevenueCat docs](https://docs.revenuecat.com/){target="_blank"} avec l’URL de base et la version de votre projet.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://api.revenuecat.com/projects/{{project_id}}/products/{{product_id}}` |
| **Méthode HTTP** | `GET` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Payload de réponse** | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `project_id` | `project_id` | `<project_id>` |
| `product_id` | `product_id` | `<product_id>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | Non (désactivé) |
| `locale` | `locale` | Variable | `<locale_code>` | Non (désactivé) |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | Non (désactivé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | Autorisation | `Bearer <token>` | Header |

+++

### Databricks {#databricks}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par ou formellement pris en charge par les Databricks. Confirmez les détails actuels de l’API avec la documentation relative aux briques de données .

>[!BEGINSHADEBOX]

Databricks fournit des API SQL et REST sur les données d’entrepôt de données ; les brouillons précédents combinaient des conseils d’exécution d’instructions avec un exemple **jobs/get**.

Un cas d’utilisation type consiste à utiliser de petits attributs dénormalisés provenant de tables gouvernées pour la personnalisation avec les privilèges les plus stricts.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites des briques de données.

Les prérequis suivants sont requis :

* Hôte Workspace, jeton ou OAuth par politique d’organisation ; principal de service avec portée minimale.
* Accès administrateur dans Journey Optimizer.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Préférez les chemins de lecture étroits. Si vous utilisez l’exécution d’instruction **POST**, incluez le corps JSON dont l’API a besoin, collez un exemple de réponse de réussite pour le mappage, testez soigneusement la latence, puis activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API d’exécution d’instruction SQL Databricks. Exemple de modèle d’URL :

   `https://{workspace-host}/api/2.0/sql/statements/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++Exemples de champs d’intégration

L’exemple de tâche **GET** ci-dessous est donné à titre d’illustration. Pour la personnalisation pilotée par SQL, préférez le modèle [API d’exécution d’instruction](https://docs.databricks.com/api/workspace/statementexecution){target="_blank"} pris en charge par votre espace de travail.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://<databricks-instance>/api/2.0/jobs/get` |
| **Méthode HTTP** | `GET` |
| Payload de réponse | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |
| Stratégie | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| Authentification | OAuth |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Accept | Accept | Constant | application/json | Oui (activé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `job_id` | `job_id` | Variable | `12` | Oui |

+++

## Révisions, consentement et réseaux sociaux {#reviews-consent-and-social}

### Bynder {#bynder}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par Bynder ni formellement soutenu par lui. Confirmez les détails actuels de l’API avec la documentation Bynder.

>[!BEGINSHADEBOX]

Bynder est une gestion des ressources numériques (DAM) avec des API REST ; les intégrations utilisent généralement OAuth 2.0 pour les métadonnées en lecture seule ou les URL de ressources.

Les cas d’utilisation standard incluent l’extraction de métadonnées de ressource ou d’URL de diffusion dans les messages et la validation des créations dans Bynder en fonction des parcours.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de Bynder.

Les prérequis suivants sont requis :

* Domaine de portail et client OAuth (ou approche par jeton approuvée).
* Portées pour l’accès en lecture seule ; accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* La pagination et l’actualisation du jeton OAuth doivent respecter les règles de l’API de Bynder.
* Réponses paginées volumineuses : mappez uniquement les champs requis pour la personnalisation.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Configurez **GET** sur le point d’entrée choisi (un modèle courant est la liste des utilisateurs), exécutez OAuth par [Bynder](https://developer.bynder.com/){target="_blank"}, évitez d’extraire des pages de données inutiles, mappez des champs, testez, puis activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API Bynder v4. Exemple de modèle d’URL :

   `https://{your-bynder-domain}/api/v4/users/`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Exemples de champs d’intégration. Voir [Documentation de l’API Bynder](https://developer.bynder.com/){target="_blank"} pour obtenir plus d’informations sur la payload OAuth 2.0.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://{{your-bynder-domain}}/api/v4/users/` |
| **Méthode HTTP** | `GET` |
| Payload de réponse | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |
| Stratégie | Configurez les détails au niveau de la politique en fonction de vos besoins. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `your-bynder-domain` | `your-bynder-domain` | `<your-bynder-domain>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |
| Autorisation | Autorisation | Constant | `<token>` du porteur | Oui (activé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `includeInActive` | `includeInActive` | Variable | False | Non (désactivé) |
| `limit` | `limit` | Variable | 100 | Non (désactivé) |
| `page` | `page` | Variable | 1 | Non (désactivé) |

**Authentification**

| Type | Payload |
| --- | --- |
| OAuth 2.0 | Payload OAuth 2.0 (voir la documentation Bynder) |

```
{
    "type": "oauth2",
    "endpoint": {
        "uri": ""
    },
    "method": "get",
    "response": {
        "type": "json"
    },
    "request": {
        "header": [
            {
                "key": "client_id",
                "value": ""
            },
            {
                "key": "client_secret",
                "value": ""
            }
        ],
        "queryParams": [
            {
                "key": "grant_type",
                "value": ""
            },
            {
                "key": "scope",
                "value": ""
            }
        ],
        "payload": {
            "type": "json",
            "content": {}
        }
    },
    "credentialPaths": [
        "header.client_id",
        "header.client_secret",
        "queryParam.scope"
    ],
    "tokenPath": "message.token",
    "policy": {
        "timeoutInMilliseconds": 30000,
        "cache": {
            "enabled": true,
            "ttlInSeconds": 300
        },
        "retry": {
            "enabled": false
        }
    },
    "locationConfig": {
        "key": "x-token",
        "location": "query"
    }
}
```

+++

### Trustpilot {#trustpilot}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n&#39;est pas géré par Trustpilot ou formellement soutenu par lui. Confirmez les détails actuels de l&#39;API avec la documentation Trustpilot.

>[!BEGINSHADEBOX]

Trustpilot fournit des API pour les données commerciales et de synthèse de révision lorsque votre cas d&#39;utilisation et votre contrat le permettent.

Un cas d’utilisation type affiche le nombre de révisions ou les évaluations dans le contenu marketing conforme aux termes de Trustpilot.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de Trustpilot.

Les prérequis suivants sont requis :

* Clé API et cas pratique approuvé ; identifiants d’entreprise pour les requêtes.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* L&#39;utilisation des données de Trustpilot doit être conforme aux politiques de marque et d&#39;utilisation des données de Trustpilot.
* Des limites de taux s’appliquent au résumé de révision et aux points d’entrée associés.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Configurez **GET** avec l’authentification de requête requise, mappez les identifiants du profil ou du contexte, collez l’exemple JSON, mappez les champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide des API Trustpilot. Exemple de modèle d’URL :

   `https://api.trustpilot.com/v1/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Utilisez l’opération de liste de catégories de [développeurs Trustpilot](https://developers.trustpilot.com/){target="_blank"} pour votre modèle d’intégration ; les paramètres varient selon la ressource.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://api.trustpilot.com/v1/categories` |
| **Méthode HTTP** | `GET` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Payload de réponse** | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | Non (désactivé) |
| `locale` | `locale` | Variable | `<locale_code>` | Non (désactivé) |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | Non (désactivé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | apiKey | `<your_api_key>` | Header |

+++

### Bazaarvoice {#bazaarvoice}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n&#39;est pas maintenu par Bazaarvoice, ni formellement soutenu par lui. Confirmez les détails actuels de l’API avec la documentation de Bazaarvoice.

>[!BEGINSHADEBOX]

Bazaarvoice fournit des évaluations, des avis et des API UGC.

Un cas d’utilisation type consiste à afficher des résumés de révision ou des évaluations dans les e-mails lorsque la politique le permet.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limitations de Bazaarvoice.

Les prérequis suivants sont requis :

* Clé de sécurité API et identifiants client de votre contrat.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* L&#39;affichage des évaluations et des avis doit suivre les politiques de contenu de Bazaarvoice.
* Des limites de débit et des règles de mise en cache s’appliquent par clé API.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Utilisez **GET** avec `passkey` comme paramètre de requête sur l’API Conversations, définissez `Accept: application/json`, collez l’exemple JSON, mappez des champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API Bazaarvoice Conversations. Exemple de modèle d’URL :

   `https://api.bazaarvoice.com/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Exemple de point d’entrée : `https://api.bazaarvoice.com/data/products.json` avec des paramètres de requête de version et de filtre. Voir [développeur Bazaarvoice](https://developer.bazaarvoice.com/){target="_blank"}.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://api.bazaarvoice.com/data/products.json` |
| **Méthode HTTP** | `GET` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Payload de réponse** | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Accept | Accept | Constant | application/json | Oui (activé) |

**Authentification**

| Type | Valeur de clé | Emplacement |
| --- | --- | --- |
| mot de passe | `<YOUR_ACCESS_TOKEN>` | Paramètre de requête |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `apiversion` | apiversionNumber | Constant | 5.4 | Oui (activé) |
| `filter` | `filter` | Variable | Id :47950830 | Non (désactivé) |
| `stats` | `stats` | Variable | tout | Non (désactivé) |

+++

### OneTrust {#onetrust}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par OneTrust et n’est pas formellement pris en charge par celui-ci. Confirmez les détails actuels de l’API avec la documentation OneTrust.

>[!BEGINSHADEBOX]

OneTrust expose les API de confidentialité et de consentement (URL et schémas spécifiques aux produits).

Un cas d’utilisation type consiste à lire des signaux de consentement ou de préférence pour du contenu conditionnel lorsque l’architecture et la révision juridique le permettent.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de OneTrust.

Les prérequis suivants sont requis :

* Informations d’identification d’API et URL de base régionale ; approbation légale des champs utilisés dans la messagerie.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Les données relatives au consentement et aux préférences sont très réglementées. Coordonnez-vous avec les équipes juridiques et de confidentialité.
* Les chemins d’accès et les payloads des API diffèrent selon le produit OneTrust. Utilisez la documentation pour votre abonnement.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Utilisez le schéma publié ou le chemin d’accès au centre de préférences de vos documents d’abonnement, renseignez OAuth si nécessaire, collez un exemple de code JSON, mappez des champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API OneTrust. Votre client, votre produit et votre chemin d’accès proviennent de la documentation [OneTrust](https://developer.onetrust.com/){target="_blank"} de votre abonnement. Exemple de modèle d’URL :

   `https://{tenant}.my.onetrust.com/api/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

| Champ | Valeur |
| --- | --- |
| **URL** | `https://customer.my.onetrust.com/api/consentmanager/v2/preferencecenters/{{preferencecenterid}}/schema` |
| **Méthode HTTP** | `GET` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Payload de réponse** | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |
| **Authentification** | OAuth |

**Paramètres de chemin**

| Paramètre | Nom | Valeur |
| --- | --- | --- |
| `preferencecenterid` | `preferencecenterid` | `<pref-id>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Accept | Accept | Constant | application/json | Oui (activé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `state` | `state` | constant | PUBLIÉ | Oui |

+++

#### Schéma du centre de préférences (publié)

Exemple de modèle (fragment) : `https://{tenant}.my.onetrust.com/api/consentmanager/v2/preferencecenters/{preferencecenterid}/schema?state=PUBLISHED`. Confirmez le chemin exact dans [OneTrust Developer](https://developer.onetrust.com/){target="_blank"}.

### Meta {#meta}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par Meta ni formellement pris en charge par celui-ci. Confirmez les détails actuels de l’API avec la documentation de Meta.

>[!BEGINSHADEBOX]

Les API Graph et Marketing de Meta exposent les objets de catalogue et de campagne pour les intégrations commerciales autorisées.

Un cas d’utilisation type consiste à enrichir le contenu avec des attributs provenant de Meta, lorsque les jetons et les politiques le permettent.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites de Meta.

Les prérequis suivants sont requis :

* Utilisateur système ou jeton d’application avec les autorisations appropriées ; alignement de Business Manager.
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Les jetons d’accès de courte durée nécessitent une stratégie de renouvellement ou de longue durée adaptée aux intégrations côté serveur.
* Respectez les conditions générales de la plateforme Meta ; ne consignez pas de jetons ou d’autres secrets dans les payloads des messages.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Les appels graphiques sont souvent **GET** avec un chemin versionné. Gérez l’expiration des jetons, collez un exemple de JSON, mappez des champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API Meta Graph. Exemple de modèle d’URL :

   `https://graph.facebook.com/vXX.X/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Exemples de champs d’intégration. Voir [API Graph](https://developers.facebook.com/docs/graph-api){target="_blank"} pour le contrôle de version et les jetons d’accès.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://graph.facebook.com/{{API_VERSION}}/{{PRODUCT_CATALOG_ID}}/products` |
| **Méthode HTTP** | `GET` |
| Payload de réponse | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |
| Stratégie | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| Authentification | OAuth |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `API_VERSION` | `API_VERSION` | `v19.0` |
| `PRODUCT_CATALOG_ID` | `PRODUCT_CATALOG_ID` | `12345` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Accept | Accept | Constant | application/json | Oui (activé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `fields` | `fields` | Variable | identifiant | Non |
| `filter` | `filter` | Variable | — | Non |

+++

### Aprimo {#aprimo}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par Aprimo et n’est pas formellement soutenu par lui. Confirmez les détails actuels de l’API avec la documentation d’Aprimo.

>[!BEGINSHADEBOX]

Aprimo combine des opérations marketing et des API de gestion des ressources numériques pour les enregistrements, les ressources et les métadonnées.

Les cas d’utilisation standard incluent les champs d’enregistrement ou de ressource approuvés dans le contenu dynamique et les workflows de gestion des ressources numériques régis dans les secteurs réglementés.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites d’Aprimo.

Les prérequis suivants sont requis :

* URL et informations d’identification du client (OAuth ou clé API selon votre configuration).
* Accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* La sécurité au niveau du champ Aprimo doit s’aligner sur les attributs que vous mappez dans Journey Optimizer.
* Payloads HAL ou JSON volumineuses : limitez les champs mappés à l’ensemble minimum requis.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Utilisez **GET** sur le chemin d’enregistrement dont vous avez besoin, envoyez les en-têtes requis tels que `API-VERSION`, collez l’exemple JSON (HAL ou JSON tel que renvoyé), mappez un ensemble de champs minimal, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API Enregistrements / DAM Aprimo. Utilisez l’URL de base de l’API et le chemin d’accès aux enregistrements pour votre **client** (selon Aprimo). Exemple de modèle d’URL :

   `https://{tenant}.dam.aprimo.com/`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

| Champ | Valeur |
| --- | --- |
| **URL** | `https://productstrategy1.dam.aprimo.com/api/core/record/{{recordID}}` |
| **Méthode HTTP** | `GET` |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `recordId` | `recordId` | `<record_identifier>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |
| API-VERSION | API-VERSION | Constant | 1 | Oui (activé) |
| Accept | Accept | Constant | application/hal+json OU application/json | Non (désactivé) |
| select-record | select-record | Variable | `<selection_type>` | Non (désactivé) |
| select-record-fields | select-record-fields | Variable | `<field_list>` | Non (désactivé) |
| select-field | select-field | Variable | `<field_selection>` | Non (désactivé) |

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | Autorisation | `<token>` du porteur | Header |

+++

### Epsilon (Epsilon3) {#epsilon}

>[!IMPORTANT]
>
>Cet exemple de configuration a été testé indépendamment par Adobe en tant que modèle. Il n’est pas géré par Epsilon et n’est pas formellement pris en charge par celui-ci. Confirmez les détails actuels de l’API avec la documentation Epsilon.

>[!BEGINSHADEBOX]

Epsilon expose les API par contrat d’entreprise ; les URL de base et les authentifications proviennent de votre équipe de compte (l’exemple d’API d’événements ci-dessous est illustratif).

Un cas d’utilisation type expose les attributs de fidélité ou d’offre par le biais d’API JSON prises en charge.

>[!ENDSHADEBOX]

+++ En savoir plus sur les conditions préalables et les limites d’Epsilon (Epsilon3).

Les prérequis suivants sont requis :

* Informations d’identification et points d’entrée d’Epsilon ; accès administrateur dans Journey Optimizer.

Les restrictions et exclusions suivantes s’appliquent :

* Les points d’entrée et les hôtes sont spécifiques au client. Ne déployez pas sans la documentation de l’équipe de votre compte Epsilon.

+++

Suivez la procédure ci-dessous pour configurer cette intégration dans Journey Optimizer. Voir **Exemples de champs d’intégration** par exemple les détails de la demande et confirmer ces valeurs avec la documentation du fournisseur pour votre environnement.

1. Suivez [Utilisation des intégrations](integrations.md). Ne devinez pas les URL publiques. Utilisez la spécification Epsilon, collez l’exemple JSON, mappez les champs, testez, activez.

1. Dans Journey Optimizer, accédez à **[!UICONTROL Configurations]** > **[!UICONTROL Gérer]**, puis sélectionnez **[!UICONTROL Créer une intégration]**.

1. Saisissez un nom d’intégration sans espaces.

1. Configurez le point d’entrée à l’aide de l’API Epsilon (conformément à votre spécification d’intégration). L’URL de base et les chemins d’accès aux ressources sont fournis par l’équipe de votre compte Epsilon. Exemple de modèle d’URL :

   `https://{your-instance}.epsilon3.io/api/...`

1. Sélectionnez la méthode HTTP affichée dans le tableau de configuration, généralement GET, sauf indication contraire.

1. Configurez l’authentification (en-têtes, paramètres de requête ou OAuth) exactement comme spécifié dans le tableau et dans la documentation du fournisseur.

1. Définissez les paramètres de chemin, de requête et d’en-tête, et mappez les variables aux données de profil ou contextuelles, si nécessaire.

1. Collez un exemple de réponse JSON afin que les champs puissent être détectés et mappés.

1. Sélectionnez les champs requis pour la personnalisation dans le mappage de la payload de réponse.

1. Configurez les politiques de temporisation, de reprise et de mise en cache en fonction du volume attendu.

1. Testez la connexion, puis activez l’intégration.

Le tableau ci-dessous répertorie les exemples de valeurs pour cette demande d’intégration.

+++ Exemples de champs d’intégration

Exemple de modèle : `https://{your-instance}.epsilon3.io/api/v1/planning/events` avec des paramètres de requête `start` et `end` et une clé API basée sur l’en-tête . Confirmez avec Epsilon avant la production.

| Champ | Valeur |
| --- | --- |
| **URL** | `https://{{your-instance}}.epsilon3.io/api/v1/planning/events` |
| **Méthode HTTP** | `GET` |
| **Politique** | Configurez les détails au niveau de la politique en fonction de vos besoins. |
| **Payload de réponse** | Sélectionnez et configurez les champs de réponse souhaités à utiliser lors de la création, en fonction de la réponse de l’API. |

**Paramètres de chemin**

| Paramètre de chemin | Nom | Valeur par défaut |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |

**En-têtes**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| Type de contenu (par défaut) | Content-Type | Constant | application/json | Oui (activé) |

**Paramètres de requête**

| Paramètre | Nom | Type | Valeur | Obligatoire |
| --- | --- | --- | --- | --- |
| `start` | `start` | Variable | 2019-08-:15:22Z | Oui (activé) * |
| `end` | `end` | Variable | 2019-08-:15:22Z | Oui (activé) * |
| `eventType` | `eventType` | Variable | planifié/non planifié | Non (désactivé) |
| `exclude_recurrences` | `exclude_recurrences` | Variable | true/false | Non (désactivé) |

\* Facultatif pour `eventType` = `unscheduled` et pour `exclude_recurrences` = `true`.

**Authentification**

| Type | Nom de la clé API | Valeur de clé API | Emplacement |
| --- | --- | --- | --- |
| Clé API | `<your_username>` | `<EPSILON3_API_KEY>` | Header |

+++

