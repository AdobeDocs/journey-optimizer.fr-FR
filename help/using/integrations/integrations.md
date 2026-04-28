---
solution: Journey Optimizer
product: journey optimizer
title: Activer les intégrations externes
description: Intégrez des intégrations externes au processus de création de canal pour enrichir le contenu avec des informations personnalisées et dynamiques
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: Intégration
hide: true
exl-id: 104f283e-f6a5-431b-919a-d97b83d19632
source-git-commit: 16eb46843d0369ae14f004a5e0f9e743cad3170b
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 57%

---

# Utiliser des intégrations {#external-sources}

>[!BEGINSHADEBOX]

Table des matières :

* **[Utilisation des intégrations](integrations.md)**
* [Commencer](vendor-integration-gs.md)
* [Fournisseurs disponibles](vendor-integration.md)
* [FAQ](vendor-integration-faq.md)

>[!ENDSHADEBOX]

## Vue d’ensemble

La fonctionnalité **Intégrations** relie Adobe Journey Optimizer à des systèmes tiers dont vous gérez déjà les données et le contenu composable ailleurs. Vous pouvez surfacer ce contenu pendant la création et au moment de l’envoi, ce qui permet d’offrir des expériences plus réactives et personnalisées sur les canaux que vous utilisez dans Journey Optimizer.

Vous pouvez utiliser cette fonctionnalité pour accéder à des données externes et extraire du contenu à partir d’outils tiers tels que :

* **Points de récompense** issus des systèmes de fidélité.
* **Informations sur les prix** pour les produits.
* **Recommandations de produits** à partir des moteurs de recommandation.
* **Mises à jour logistiques** comme le statut de la diffusion.

Pour commencer à utiliser les intégrations, les utilisateurs doivent disposer des autorisations **[!UICONTROL Gérer la configuration de l’intégration AJO]** et **[!UICONTROL Afficher l’intégration AJO]**. [En savoir plus sur les autorisations](../administration/permissions.md)

+++ Découvrez comment attribuer des autorisations liées aux intégrations

1. Dans le produit **[!UICONTROL Autorisations]**, accédez à l’onglet **[!UICONTROL Rôles]** et sélectionnez le **[!UICONTROL Rôle]** de votre choix.

1. Cliquez sur **[!UICONTROL Modifier]** pour modifier les autorisations.

1. Ajoutez la ressource **[!UICONTROL Configuration de l’intégration AJO]**, puis sélectionnez les autorisations d’intégration appropriées dans le menu déroulant.

   ![](assets/external-integration-config-9.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** pour appliquer vos modifications.

   Les autorisations des personnes déjà affectées à ce rôle seront automatiquement mises à jour.

1. Pour attribuer ce rôle à de nouvelles personnes, accédez à l’onglet **[!UICONTROL Utilisateurs et utilisatrices]** du tableau de bord **[!UICONTROL Rôles]** et cliquez sur **[!UICONTROL Ajouter un utilisateur ou une utilisatrice]**.

1. Saisissez le nom de la personne, son adresse e-mail ou choisissez dans la liste, puis cliquez sur **[!UICONTROL Enregistrer]**.

Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez [cette documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Configurer votre intégration {#configure}

>[!AVAILABILITY]
>
> Cette fonctionnalité d’intégration est limitée aux canaux sortants (e-mail, SMS et notification push) et fournit des données aux formats JSON ou HTML. Notez que l’API est en lecture seule et ne prend en charge que les opérations de récupération.

En tant qu’administrateur ou administratrice, vous pouvez configurer des intégrations externes en procédant comme suit :

1. Accédez à la section **[!UICONTROL Configurations]** dans le menu de gauche, puis cliquez sur **[!UICONTROL Gérer]** dans la carte **[!UICONTROL Intégrations]**.

   Cliquez ensuite sur **[!UICONTROL Créer une intégration]** pour démarrer une nouvelle configuration.

   ![](assets/external-integration-config-1.png)

1. Vous pouvez éventuellement coller une commande **cURL** pour remplir automatiquement l’URL, la méthode HTTP, les en-têtes et les paramètres de requête.

1. Indiquez un **[!UICONTROL nom]** et une **[!UICONTROL description]** pour votre intégration.

   >[!NOTE]
   >
   >Ces champs ne peuvent pas contenir d’espaces.

1. Saisissez l’**[!UICONTROL URL]** du point d’entrée API, qui peut inclure des paramètres de chemin comportant des variables définissables à l’aide de libellés et de valeurs par défaut.

1. Configurez le **[!UICONTROL Modèle de chemin]** avec son **[!UICONTROL Nom]** et sa **[!UICONTROL Valeur par défaut]**.

   ![](assets/external-integration-config-2.png)

1. Sélectionnez la **[!UICONTROL méthode HTTP]** entre GET et POST.

1. Cliquez sur **[!UICONTROL Ajouter un en-tête]** et/ou **[!UICONTROL Ajouter des paramètres de requête]** selon les besoins de votre intégration. Pour chaque paramètre, fournissez les détails suivants :

   * **[!UICONTROL Paramètre]** : un identifiant unique utilisé en interne pour référencer le paramètre.

   * **[!UICONTROL Nom]** : le nom réel du paramètre, comme attendu par l’API.

   * **[!UICONTROL Type]** : choisissez **Constante** pour une valeur fixe ou **Variable** pour une entrée dynamique.

   * **[!UICONTROL Valeur]** : saisissez directement la valeur pour les constantes ou sélectionnez un mappage de variables.

   * **[!UICONTROL Obligatoire]** : indiquez si ce paramètre est obligatoire.

   ![](assets/external-integration-config-3.png)

1. Choisissez un **[!UICONTROL type d’authentification]** :

   * **[!UICONTROL Aucune authentification]** : pour les API ouvertes qui ne nécessitent aucune information d’identification.

   * **[!UICONTROL Clé API]** : authentifiez les requêtes à l’aide d’une clé API statique. Saisissez votre **[!UICONTROL nom de clé API &#x200B;]**, la **[!UICONTROL valeur de la clé API &#x200B;]** et spécifiez votre **[!UICONTROL emplacement]**.

   * **[!UICONTROL Authentification de base]** : utilisez l’authentification HTTP de base standard. Saisissez le **[!UICONTROL nom d’utilisateur]** et le **[!UICONTROL mot de passe]**.

   * **[!UICONTROL OAuth 2.0]** : authentifiez-vous à l’aide du protocole OAuth 2.0. Cliquez sur l’icône ![modifier](assets/do-not-localize/Smock_Edit_18_N.svg) pour configurer ou mettre à jour la **[!UICONTROL payload]**.

   ![](assets/external-integration-config-4.png)

1. Définissez la **[!UICONTROL Configuration de la politique]** comme le **[!UICONTROL Délai d’expiration]** pour les requêtes API et choisissez d’activer le ralentissement, la mise en cache et/ou la reprise.

   Lorsque la limitation est activée, les taux pris en charge vont de **50** TPS (minimum) à **5 000** TPS (maximum).
Lorsque la reprise est activée, d’autres échecs suivent **trois** reprises par défaut, avec **200 ms**, **400 ms** et **800 ms** entre les tentatives successives.

1. Avec le champ **[!UICONTROL payload de réponse]**, vous pouvez déterminer quels champs de l’exemple de sortie doivent être utilisés pour la personnalisation des messages.

   Cliquez sur l’icône ![modifier](assets/do-not-localize/Smock_Edit_18_N.svg) et collez un exemple de payload de réponse JSON pour détecter automatiquement les types de données.

1. Choisissez les champs à exposer pour la personnalisation et spécifiez leurs types de données correspondants.

   ![](assets/external-integration-config-5.png)

1. Utilisez **[!UICONTROL Envoyer une connexion de test]** pour valider l’intégration.

   Une fois la validation effectuée, cliquez sur **[!UICONTROL Activer]**.

### Limites de l’heure d’envoi et comportement {#configure-send-time}

Au moment de l’envoi, les réponses de l’API externe peuvent être jusqu’à **4 Mo** par défaut. Toute valeur supérieure est traitée comme une erreur d’intégration et **aucune tentative n’est effectuée** lorsque l’échec est dû à la taille de la réponse.

Les appels respectent le taux **de limitation** que vous avez configuré : Journey Optimizer planifie les tentatives jusqu’à cette limite même lorsque le système externe est en panne ou renvoie des erreurs. Si le **cache** est activé, seules les réponses **réussies** sont stockées et réutilisées jusqu’à l’expiration du cache **TTL** que vous avez défini ; les réponses en échec ne sont jamais mises en cache.

Chaque message mis en file d’attente comporte également une fenêtre de validité (TTL). Si le traitement prend du retard et qu’un message reste au-delà de cette fenêtre, le système **ignore** et émet un événement **`MessageValidityExclusion`** afin que le travail obsolète soit effacé de la file d’attente et que les ressources restent disponibles.

## Utiliser des intégrations externes pour la personnalisation {#personalization}

En tant que responsable marketing, vous pouvez utiliser des intégrations configurées pour personnaliser votre contenu. Procédez comme suit :

1. Accédez au contenu de votre campagne et cliquez sur **[!UICONTROL Ajouter une personnalisation]** dans le champ **[!UICONTROL Composants]** Texte ou HTML.

   [En savoir plus sur les composants](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Accédez à la section **[!UICONTROL Intégrations]** et cliquez sur **[!UICONTROL Ouvrir les intégrations]** pour afficher toutes les intégrations actives.

   Notez que les fragments de contenu sont disponibles avec les intégrations , mais prennent uniquement en charge les canaux sortants. La publication entrante ne réussit pas. Une fois qu’un fragment est publié, l’ajout et l’enregistrement de nouvelles intégrations sont désactivés afin d’éviter tout impact sur les parcours et campagnes existants.

   ![](assets/external-integration-content-2.png)

1. Sélectionnez une intégration et cliquez sur **[!UICONTROL Enregistrer]**.

   ![](assets/external-integration-content-3.png)

1. Activez le mode **[!UICONTROL Pastilles]** pour déverrouiller le menu d’intégration avancé.

   ![](assets/external-integration-content-4.png)

1. Lorsque vous créez la personnalisation de l’intégration, l’assistant Intégrations inclut un champ **`required`** qui définit la manière dont les données manquantes ou en échec interagissent avec le contenu par défaut :

   * **`required=true`** (par défaut) : le rendu s’arrête pour ce message. L’envoi est exclu avec **`ExternalDataLookupExclusion`** et cette exclusion est enregistrée dans le jeu de données de commentaires de messages **message**.
   * **`required=false`** : la variable de résultat est définie sur **`null`** et le rendu se poursuit. Utilisez du texte par défaut, des secours ou une logique conditionnelle dans votre modèle afin que les profils ne reçoivent pas de contenu vide lorsque l’intégration ne renvoie pas de données.

     ![](assets/external-integration-content-8.png)

1. Pour terminer la configuration de votre intégration, définissez les attributs d’intégration, qui ont été précédemment spécifiés lors de la [configuration](#configure).

   Vous pouvez attribuer des valeurs à ces attributs à l’aide de valeurs statiques, qui restent constantes, ou d’attributs de profil, qui extraient dynamiquement des informations des profils utilisateur.

   ![](assets/external-integration-content-5.png)

1. Une fois les attributs d’intégration définis, vous pouvez utiliser les champs d’intégration de votre contenu pour envoyer des messages personnalisés en cliquant sur l’icône ![ajouter](assets/do-not-localize/Smock_Add_18_N.svg).

   ![](assets/external-integration-content-6.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Votre personnalisation d’intégration est maintenant appliquée avec succès à votre contenu, en veillant à ce que chaque destinataire reçoive une expérience adaptée et pertinente en fonction des attributs que vous avez configurés.

![](assets/external-integration-content-7.png)

