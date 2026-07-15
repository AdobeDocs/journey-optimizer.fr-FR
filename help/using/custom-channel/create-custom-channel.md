---
title: Création d’un canal personnalisé
description: Découvrez comment créer et configurer un canal personnalisé dans Adobe Journey Optimizer à l’aide du Channel Builder.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '1555'
ht-degree: 1%

---


# Configurer un canal personnalisé {#create-custom-channel}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_settings"
>title="À propos des canaux personnalisés"
>abstract="Un canal personnalisé permet à Adobe Journey Optimizer d’envoyer des messages personnalisés à un système externe via votre propre point d’entrée d’API. Définissez les propriétés générales, le point d’entrée, l’authentification et la payload, puis testez et activez votre nouveau canal personnalisé. Une fois cette opération terminée, vous pouvez l’utiliser lors de la création d’une configuration de canal afin que les marketeurs puissent l’utiliser dans les parcours et les campagnes."
>additional-url="" text="Commencer avec les canaux personnalisés"

<!--Contextual help final location TBC (here or in Settings subsection-->

Pour pouvoir utiliser un canal personnalisé dans les campagnes et les parcours, un administrateur doit d’abord le créer. Cela implique de définir le point d’entrée, l’authentification, la politique de limitation et la structure de la payload du message.

La section **Créateur de canaux** est l’interface centrale pour définir de nouveaux canaux personnalisés. <!--It is accessible to users with the **[!UICONTROL Administrator]** role. -->Il vous permet de créer et de configurer des canaux personnalisés, mais aussi de gérer les informations d’identification d’API et de déléguer des sous-domaines.

>[!IMPORTANT]
>
>Pour accéder au Créateur de canaux, créer et gérer des canaux personnalisés, vous devez disposer des autorisations **Afficher les canaux personnalisés** et **Gérer les canaux personnalisés** accordées. <!--[Learn more](../administration/high-low-permissions.md)--> Découvrez comment gérer les autorisations dans [ cette section ](../administration/permissions.md).

## Accéder aux canaux personnalisés et les gérer {#access-channel-builder}

Pour accéder au **Créateur de canaux** et gérer vos canaux personnalisés, procédez comme suit.

1. Accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** dans le rail de navigation de gauche.

1. Sélectionnez **[!UICONTROL Canaux personnalisés]** sous la section **[!UICONTROL Créateur de canaux]**.

   ![Inventaire des canaux personnalisés](assets/custom_channels_inventory.png){width="70%"}

1. L’inventaire répertorie tous les canaux personnalisés de votre sandbox, y compris leur statut actuel et le type d’authentification utilisé pour se connecter au point d’entrée externe.

1. Vous pouvez filtrer les canaux personnalisés par statut (**Brouillon**, **Actif** ou **Archivé**), par auteur et par nom.

1. Pour modifier un canal, cliquez sur son nom dans l’inventaire, apportez vos modifications et enregistrez-le. Pour les canaux actifs, vous ne pouvez modifier que certains champs. En [ plus](#test-activate).

   >[!CAUTION]
   >
   >La modification des paramètres de limitation ou de reprise sur un canal actif prend effet immédiatement pour toutes les exécutions en cours et futures.

1. Pour archiver un canal, ouvrez-le dans l’inventaire et cliquez sur **[!UICONTROL Archiver]**.

   L’archivage d’un canal actif le supprime de toutes les listes déroulantes de sélection : sélecteur d’actions de campagne, palette d’actions de parcours, liste de canaux des campagnes orchestrées, configurations de canal et modèles de contenu. Les parcours et campagnes existants qui utilisent déjà le canal continuent à fonctionner normalement.

## Création d’un canal personnalisé {#create-channel}

Pour créer un canal personnalisé, procédez comme suit.

1. Cliquez sur le bouton **[!UICONTROL Créer un canal personnalisé]** pour ouvrir le formulaire de création de canal. Commencez par définir les paramètres généraux de votre canal personnalisé.

   ![ Paramètres généraux ](assets/custom_channel_properties.png){width="70%"}

1. Dans la section **[!UICONTROL Propriétés]** , saisissez un **[!UICONTROL Nom]** pour votre canal personnalisé. Ce nom apparaît dans la zone de travail des parcours, le sélecteur d’actions de campagne et la liste des canaux des campagnes orchestrées.

   >[!NOTE]
   >
   >Le nom doit être unique, commencer par une lettre (A-Z), inclure uniquement des caractères alphanumériques ou spéciaux ( _, ., -) et doit comporter plus de 1 caractère.

1. Vous pouvez sélectionner une icône dans la bibliothèque d’icônes par défaut ou sélectionner un fichier SVG sur votre ordinateur.

   >[!NOTE]
   >
   >La taille du fichier ne doit pas dépasser 150KB.

   Cette icône s’affiche en regard du nom du canal dans la zone de travail de parcours. Si aucune icône n’est chargée, l’icône par défaut est utilisée.

1. Saisissez une **[!UICONTROL Description]** facultative.

<!--
1. Optionally, assign **[!UICONTROL Access labels]** to restrict access to this channel based on data usage policies. Learn more
-->

## Définir la configuration du point d’entrée {#endpoint-configuration}

Vous devez configurer le point d’entrée , qui est l’URL HTTP de votre système de messagerie externe. [!DNL Journey Optimizer] envoie une requête POST à ce point d’entrée avec la payload personnalisée lorsqu’un profil est qualifié dans une campagne ou un parcours.

![Configuration du point d’entrée](assets/custom_channel_endpoint_configuration.png){width="70%"}

1. Dans la section **[!UICONTROL Configuration du point d’entrée]**, saisissez l’hôte **[!UICONTROL URL]** de votre système de messagerie externe.

   <!--The HTTP method to is currently set to **POST**.-->

   >[!IMPORTANT]
   >Votre système de messagerie externe doit exposer un point d’entrée HTTPS que [!DNL Journey Optimizer] pouvez appeler via HTTP POST. Le point d’entrée doit :
   >
   >* Acceptez le format de payload défini par votre canal (JSON).
   >* Prend en charge l’une des méthodes d’authentification disponibles dans le créateur de canaux. [En savoir plus](#authentication-settings)
   >* Renvoyer une réponse HTTP 2xx pour accuser réception de la requête.

1. Ajoutez des **[!UICONTROL en-têtes]** si nécessaire. Les en-têtes sont des paires clé-valeur transmises au niveau de la requête HTTP. Ils sont envoyés avec chaque requête à votre point d’entrée et sont généralement utilisés pour les jetons d’authentification, la spécification du type de contenu ou toute autre métadonnée requise par votre système externe.

   <!--At minimum, `Content-Type` and `Charset` are available as default headers.-->

   ![ Configuration des en-têtes ](assets/custom_channel_endpoint_headers.png)

   Pour chaque en-tête, vous pouvez définir si sa valeur est :

   * **[!UICONTROL Constant]** - Une valeur statique définie une fois et incluse dans chaque requête. Par exemple, vous pouvez définir le paramètre `Content-Type` avec la valeur `application/json` ou le paramètre `Charset` avec la valeur `UTF-8`.
   * **[!UICONTROL Variable]** - Si une valeur par défaut est saisie ici, elle est utilisée, sauf si elle est remplacée dans la configuration du canal. Par exemple, vous pouvez définir une variable pour l’ID utilisateur qui est résolue au moment de l’exécution. [En savoir plus](custom-channel-configuration.md) <!--From Custom actions section: For these parameters, you can define where to get this information (example: events, data sources), pass values manually or use the advanced expression editor for advanced use cases. Advanced uses cases can be data manipulation and other function usage. Refer to this [page](expression/expressionadvanced.md).-->

1. Vous pouvez éventuellement ajouter des **[!UICONTROL paramètres de requête]** en utilisant le même modèle de constante/variable. Les paramètres de requête sont ajoutés à l’URL du point d’entrée au moment de la diffusion. Les paramètres constants sont toujours ajoutés avec la même valeur ; les paramètres variables sont résolus au moment de l’envoi, par exemple pour transmettre un identifiant utilisateur du profil.

   ![Paramètres de requête](assets/custom_channel_endpoint_query_param.png){width="70%"}

1. Dans la section **[!UICONTROL Configuration de la politique]**, définissez comment [!DNL Journey Optimizer] gère le débit et les échecs des requêtes. Cela est important pour vous assurer que votre système externe peut gérer le volume de requêtes et éviter de le surcharger.

   ![Configuration de la politique](assets/custom_channel_endpoint_policy_config.png)

   * **[!UICONTROL Activer le ralentissement]** - Désactivé par défaut. Définissez le nombre maximal de requêtes par seconde (par défaut : 5 000 **c**). Une fois la limite atteinte, les requêtes sont mises en file d’attente et envoyées dès que possible.
   * **[!UICONTROL Activer la reprise]** - Activé par défaut. Définissez le nombre maximal de reprises (valeur par défaut : **3**, plage configurable : 0-10) pour les requêtes ayant échoué. Cela permet d’éviter de surcharger le point d’entrée lors d’échecs transitoires.
   * **[!UICONTROL Délai d’expiration]** - Valeur par défaut : **5 000 millisecondes**. Définissez la durée maximale d’attente d’une réponse du point d’entrée avant de considérer que la requête a échoué.     <!--* **[!UICONTROL Enable cache]** – Disabled by default. Set the caching duration (default TTL: **600 seconds**). After the TTL (Time To Live) expires, the next request is sent to the endpoint. Caching is useful for endpoints that return the same response for identical requests, reducing load and improving performance.-->

## Paramètres d’authentification {#authentication-settings}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_authentication"
>title="Définition du type d’authentification"
>abstract="L’authentification garantit que seules les requêtes autorisées sont envoyées à votre système de messagerie externe. Vous pouvez choisir parmi plusieurs méthodes d’authentification, notamment la clé API, l’authentification de base et OAuth 2.0. Lors de l’activation, Adobe Journey Optimizer génère automatiquement un jeu initial d’informations d’identification d’API pour le canal, qui peuvent être gérées dans l’inventaire des informations d’identification d’API. Cependant, même si vous pouvez modifier les informations d’identification ultérieurement, vous devez fournir les détails d’authentification ici pour tester la connexion à votre point d’entrée avant d’activer le canal."
>additional-url="" text="En savoir plus sur les informations d’identification de l’API"

Sélectionnez le **[!UICONTROL Type d’authentification]** que vous devez utiliser pour ce canal. Les options disponibles dépendent des méthodes d’authentification prises en charge par votre système de messagerie externe.

![Type d’authentification](assets/custom_channel_authentication_type.png){width="70%"}

Fournissez les détails d’authentification requis par le point d’entrée.

* **[!UICONTROL Aucune]** - La requête est envoyée sans informations d’identification.
* **[!UICONTROL Clé API]** - Indiquez le nom, la valeur et l’emplacement de la clé (paramètre de requête ou en-tête).
* **[!UICONTROL Authentification de base]** - Indiquez un nom d’utilisateur et un mot de passe.
* **[!UICONTROL OAuth 2.0]** - Configurez la payload pour l’authentification OAuth 2.0.
  <!--* **[!UICONTROL Custom]** – Define the authentication configuration using a JSON payload.-->

Lorsque le type d’authentification est autre chose que **Aucun**, [!DNL Journey Optimizer] génère automatiquement un jeu initial d’informations d’identification d’API pour ce canal lorsqu’il est activé. Vous pouvez modifier ces informations d’identification et en créer de nouvelles dans l’inventaire des informations d’identification de l’API. [En savoir plus](custom-channel-api-credentials.md) <!--TBC-->

Toutefois, les détails d’authentification sont nécessaires ici pour tester la connexion à votre point d’entrée avant d’activer le canal. Un bouton **[!UICONTROL Tester la connexion]** est disponible pour valider la configuration de l’authentification. [En savoir plus](#test-activate)

## Configuration de la payload {#payload-configuration}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_payload_config"
>title="Activer le champ pour la configuration du canal"
>abstract="Si cette option est activée, les champs de cette colonne apparaissent dans la configuration du canal, ce qui permet aux administrateurs de définir des valeurs différentes par configuration (par exemple, un identifiant d’expéditeur différent par marque ou région). Cela s’avère utile pour les champs qui peuvent varier en fonction du contexte de la campagne ou du parcours, tels que les informations de l’expéditeur ou les modèles de message."
>additional-url="" text="Configuration des paramètres dynamiques dans la configuration de canal personnalisé"

<!--Create a page on Custom channel config to explain how to use the payload in a channel configuration.-->

La payload est envoyée au point d’entrée lorsqu’un profil est qualifié dans une campagne ou un parcours.

Dans la configuration de la payload, définissez la structure de la payload du message et les champs que les marketeurs peuvent créer et personnaliser.

1. Cliquez sur **[!UICONTROL Définir la payload]** et choisissez comment la définir :

   * **[!UICONTROL Coller un exemple de payload JSON]** - Collez un objet JSON représentatif et [!DNL Journey Optimizer] en déduit automatiquement un schéma.
   * **[!UICONTROL Importer un schéma JSON]** (bientôt disponible) - Téléchargez un fichier de schéma JSON complet.

     >[!AVAILABILITY]
     >
     >Cette fonctionnalité n’est pas encore disponible. Elle sera ajoutée dans une version ultérieure.

1. Une fois le schéma généré, [!DNL Journey Optimizer] affiche tous les champs détectés dans une vue de formulaire.

   ![](assets/custom_channel_payload_configuration.png)

1. Pour chaque champ, configurez les paramètres suivants :

   | Paramètre | Description |
   | --- | --- |
   | **[!UICONTROL Valeur par défaut]** | Facultatif. Utilisé si aucune valeur personnalisée n’est fournie au moment de la création. |
   | **[!UICONTROL Type]** | Lecture seule, dérivée de la payload. Types pris en charge : `string`, `integer`, `decimal`, `boolean`, `dateTime`, `dateTimeOnly`, `dateOnly`, `listObject`, `listString`, `listInteger`, `listDecimal`, `listBoolean`, `listDateTime`, `listDateTimeOnly`, `listDateOnly`,. |
   | **[!UICONTROL Obligatoire]** | Si cette option est activée, le champ doit avoir une valeur lorsque le canal est utilisé dans une campagne ou un parcours. Les champs obligatoires manquants déclenchent une erreur de validation qui empêche l’activation. |
   | **[!UICONTROL Configuration du canal]** | Si cette option est activée, le champ s’affiche dans la configuration du canal, ce qui permet aux administrateurs de définir des valeurs différentes par configuration (par exemple, un identifiant d’expéditeur différent par marque ou région). [Voici comment procéder](custom-channel-configuration.md) |

   Les champs imbriqués sont représentés à l’aide de la notation par points (par exemple, `image.id`).<!--TBC-->

## Tester et activer {#test-activate}

Lorsque le canal a le statut **[!UICONTROL Brouillon]**, utilisez le bouton **[!UICONTROL Tester la connexion]** en haut de l’écran pour envoyer une requête de test à votre point d’entrée et valider la connexion de bout en bout.

![Bouton Tester la connexion](assets/custom_channel_test_connection.png){width="70%"}

Vérifiez les journaux de votre système externe pour vous assurer que la demande a été reçue avec l’authentification et la payload attendues.

Une fois le test réussi, vous pouvez enregistrer ou activer le canal.

* Cliquez sur **[!UICONTROL Enregistrer en tant que brouillon]** pour enregistrer votre progression sans rendre le canal disponible.
* Cliquez sur **[!UICONTROL Activer]** pour rendre le canal disponible pour une utilisation dans les configurations de canal, les campagnes et les parcours.

>[!IMPORTANT]
>
>Une fois qu’un canal est activé, seuls les champs suivants restent modifiables : nom, description, icône, limitation et configuration de la reprise. L’URL du point d’entrée, les en-têtes, les paramètres de requête, l’authentification et la structure de payload sont verrouillés.<!--TBC-->

<!--TBC: An activated channel can be **archived** (hidden from all selection drop-downs while existing journeys and campaigns continue to function), but it cannot be **deleted**. Deletion is only possible while the channel is in **[!UICONTROL Draft]** status.TBC-->

## Étapes suivantes {#next-steps}

Votre canal personnalisé est maintenant créé. Effectuez la configuration en suivant les étapes restantes :

* [Configurer les informations d’identification de l’API](custom-channel-api-credentials.md) (si le canal utilise l’authentification)
* [Déléguer un sous-domaine](custom-channel-subdomains.md) (facultatif, obligatoire pour le suivi des liens)
* [Créer une configuration des canaux](custom-channel-configuration.md)
