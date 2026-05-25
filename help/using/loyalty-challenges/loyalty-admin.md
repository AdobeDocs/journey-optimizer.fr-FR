---
solution: Journey Optimizer
product: journey optimizer
title: Configuration du programme de fidélité
description: Découvrez comment configurer les fournisseurs de récompenses, les définitions d’événement, l’inventaire de produits, les exclusions et les paramètres au niveau de l’organisation pour votre programme de fidélité dans  [!DNL Journey Optimizer].
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: 863c3405e5509938cb6b9180c16d5c89fb439814
workflow-type: tm+mt
source-wordcount: '1631'
ht-degree: 1%

---

# Configuration du programme de fidélité {#loyalty-admin}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](get-started.md)
* [Accéder aux défis et aux tâches et les gérer](access-loyalty-challenges.md)
* [Créer des défis](create-challenges.md)
* [Création de tâches](create-tasks.md)
* [Surveillance des performances des défis de fidélité](loyalty-reporting.md)
* **Configurer le programme de fidélité** ◀︎ **Vous êtes ici**
* [Référence de l’API pour les défis de fidélité](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version bêta **privée**. Pour plus d’informations sur le cycle de publication et les phases de disponibilité dans [!DNL Journey Optimizer], voir [cycle de publication](../rn/releases.md).

## Vue d’ensemble {#access-loyalty-admin}

La configuration du programme de fidélité [!DNL Journey Optimizer] connecte à vos systèmes de fidélité externes en configurant l’exécution des récompenses, le mappage des événements, l’inventaire des produits et les exclusions avant que les spécialistes marketing ne lancent des défis de création.

>[!NOTE]
>
>La configuration du programme de fidélité nécessite un accès administrateur à votre instance [!DNL Journey Optimizer], en plus des autorisations nécessaires pour les défis de fidélité. Contactez votre administrateur Adobe pour obtenir l’accès.

Pour ouvrir l’interface de configuration, accédez à **[!UICONTROL Fidélité]** et sélectionnez **[!UICONTROL Administrateur fidèle]**. L’interface est organisée en onglets :

* **Paramètres globaux** — Sélectionnez l’espace de noms d’identité Experience Platform de votre programme. [Découvrez comment configurer des paramètres globaux](#global-settings)
* **Fournisseurs de récompenses** : connectez les API qui offrent des récompenses lorsque les clients réalisent des progrès ou relèvent des défis. [Découvrez comment configurer des fournisseurs de récompenses](#reward-providers)
* **Définitions d’événement** — Mappez les événements d’expérience entrants aux activités utilisées dans les tâches **[!UICONTROL Événement personnalisé]**. [Découvrez comment configurer des définitions d’événement](#event-definitions)
* **Inventaire des produits** — Chargez les mappings article/groupe à utiliser dans les règles d&#39;éligibilité des tâches. [Découvrez comment configurer l’inventaire des produits](#product-inventory)
* **Exclusions** — Chargez les exclusions d&#39;articles et de groupes à l&#39;échelle de l&#39;organisation pour la configuration des tâches. [Découvrez comment configurer des exclusions](#exclusions)

## Paramètres globaux {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Paramètres globaux"
>abstract="Les paramètres globaux définissent la configuration au niveau de l’organisation de votre programme de fidélité, y compris l’espace de noms d’identité utilisé pour identifier les membres à travers les événements et les défis."

Ouvrez l’onglet **[!UICONTROL Paramètres globaux]** et sélectionnez le Adobe Experience Platform [espace de noms d’identité](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces) de votre programme de fidélité dans le menu déroulant **[!UICONTROL Espace de noms]**. Cet espace de noms doit correspondre à la manière dont les profils membres sont identifiés dans vos données .

![](assets/admin-global-settings.png)

➡️ [Découvrez comment utiliser les espaces de noms d’identité](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces){target="_blank"}

## Fournisseurs de récompenses {#reward-providers}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers"
>title="Fournisseurs de récompenses"
>abstract="Un fournisseur de récompense définit le système externe que [!DNL Journey Optimizer] appelle pour offrir des récompenses lorsque les clients relèvent des défis. Configurez le point d’entrée du fournisseur, les définitions de récompense, les paramètres de proxy et l’authentification pour chaque intégration."

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers_connection"
>title="Connexion du fournisseur de récompense"
>abstract="Configurez comment [!DNL Journey Optimizer] se connecte à votre API de récompense : nom du fournisseur, description, URL du point d’entrée et en-têtes HTTP requis pour les appels d’exécution."

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers_details"
>title="Définitions de récompense"
>abstract="Les définitions de récompense spécifient chaque type de récompense que ce fournisseur peut émettre (par exemple, des points ou des étoiles) et la payload [!DNL Journey Optimizer] envoie lorsque les récompenses sont remplies."

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_reward_providers_proxy"
>title="Proxy de récompense"
>abstract="Vous pouvez éventuellement acheminer les appels d’exécution via un serveur proxy au lieu de les envoyer directement à votre point d’entrée de l’API de récompense. Configurez l’hôte, le port, les informations d’identification et indiquez si le proxy est activé. La valeur des informations d’identification ressemble généralement à : `{ "userName": "test", "password": "xxxx" }`"

Un **fournisseur de récompense** [!DNL Journey Optimizer] indique où envoyer des appels d’exécution lorsqu’une progression du défi est enregistrée ou qu’un défi est terminé. Par exemple, une API qui attribue des points de fidélité ou des étoiles à un compte de membre.

Pour créer un fournisseur de récompense, procédez comme suit :

1. Ouvrez l’onglet **[!UICONTROL Fournisseurs de récompenses]** et sélectionnez **[!UICONTROL Créer un fournisseur de récompense]**.

   ![](assets/admin-reward.png)

1. Saisissez un **[!UICONTROL Nom]** et un **[!UICONTROL Description]**.

1. Dans le champ **[!UICONTROL URL]**, saisissez le point d’entrée de l’API qui reçoit les demandes d’exécution.

1. Ajoutez des **[!UICONTROL en-têtes]** selon les besoins de votre API (par exemple, des clés API ou des types de contenu).

1. Configurez les ressources associées à votre fournisseur de récompense. Développez chaque section ci-dessous pour afficher les détails du champ :

   +++Définitions de récompense

   Ajoutez une entrée par type de récompense pris en charge par votre fournisseur (points de programme, étoiles ou crédit d’argent, par exemple). Pour chaque définition :

   * Saisissez un **[!UICONTROL Nom]** et un **[!UICONTROL Description]**.
   * Indiquez si la définition est **[!UICONTROL Activée]**.
   * Activez le bouton (bascule) **[!UICONTROL Par défaut]** pour marquer une définition comme définition par défaut pour ce fournisseur.
   * Définissez la **payload** envoyée avec des appels d’exécution.

   ![](assets/admin-reward-definition.png)

   +++

   +++Proxy de récompense

   Acheminez les appels d’exécution via un serveur intermédiaire au lieu de les envoyer directement à votre point d’entrée . Sur les écrans Fournisseur de récompense et **[!UICONTROL Créer un proxy]**, utilisez le champ **[!UICONTROL Informations d’identification]** pour l’authentification du proxy.

   * Saisissez un **[!UICONTROL Nom]** et un **[!UICONTROL Description]**.
   * Saisissez **[!UICONTROL Host]** et **[!UICONTROL Port]**.
   * Spécifiez si le proxy est **[!UICONTROL Activé]**.
   * Dans **[!UICONTROL Informations d’identification]**, saisissez le nom d’utilisateur et le mot de passe du proxy au format JSON. La valeur des informations d’identification ressemble généralement à ce qui suit :

     ```json
     { "userName": "test", "password": "xxxx" }
     ```

   ![](assets/admin-reward-proxies.png)

   +++

   +++Générateur de jeton d’authentification

   À utiliser lorsque votre API nécessite un jeton porteur ou une authentification similaire.

   * Saisissez un **[!UICONTROL Nom]** et un **[!UICONTROL Description]**.
   * Dans **[!UICONTROL Type d’authentification]**, saisissez le type d’authentification (par exemple, porteur).
   * Sélectionnez la méthode HTTP (par exemple, POST).
   * Saisissez l’URL du point d’entrée du jeton et la **[!UICONTROL clé du jeton]** dans la réponse (par exemple, `access_token`).
   * Spécifiez si le générateur de jetons d’authentification est **[!UICONTROL Activé]**.
   * Ajoutez les en-têtes requis par le point d’entrée du jeton.

   [!DNL Journey Optimizer] utilise cette configuration pour obtenir un nouveau jeton avant chaque appel à votre API de récompense.

   ![](assets/admin-reward-auth.png)

   +++

1. Sélectionnez **[!UICONTROL Créer un fournisseur de récompense]**. Le fournisseur et toutes les ressources configurées sont enregistrés ensemble.

Après l’enregistrement, le fournisseur apparaît dans la liste des fournisseurs de récompenses. Les marketeurs peuvent le sélectionner lors de la configuration des récompenses du défi. [Découvrez comment configurer les récompenses du défi](create-challenges.md#rewards)

Pour modifier un fournisseur de récompense, ouvrez l’onglet **[!UICONTROL Fournisseurs de récompense]**, sélectionnez le fournisseur et mettez à jour les champs en place. Les modifications apportées aux définitions de récompense, aux proxys et aux générateurs de jetons d’authentification sont automatiquement enregistrées lorsque vous les mettez à jour.

>[!NOTE]
>
>**[!UICONTROL Apportez vos propres données]** les défis génèrent des récompenses grâce à votre propre intégration de données. Les fournisseurs de récompenses configurés ici ne s’appliquent pas à ces défis. [Découvrez comment créer vos propres défis de données](create-challenges.md#create-the-challenge)

## Définitions des événements {#event-definitions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_event_definitions"
>title="Définitions des événements"
>abstract="Les définitions d’événement [!DNL Journey Optimizer] indiquent comment identifier et interpréter les données d’événement entrantes provenant de vos sources externes. Chaque définition mappe un type d’événement spécifique, tel qu’un achat ou un enregistrement, afin que le système puisse suivre la progression du client vers les tâches de défi."

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_event_schema"
>title="Schéma d’événement et transformateur"
>abstract="Lorsque votre entreprise envoie des événements au format JSON personnalisé, utilisez **[!UICONTROL Schéma]** pour valider la payload et **[!UICONTROL Transformateur]** (par exemple, une expression JSONata) pour mapper les champs au format attendu par les défis de fidélité."

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_event_identification"
>title="Identification des événements"
>abstract="Indiquez comment [!DNL Journey Optimizer] reconnaît l’événement dans les payloads entrants à l’aide d’un chemin d’accès d’identifiant, de valeurs d’identifiant, d’un identifiant de schéma XDM ou d’une combinaison de ces champs."

**[!UICONTROL Définitions d’événement]** [!DNL Journey Optimizer] les événements d’expérience Adobe Experience Platform entrants à traiter. Par exemple, un achat ou un enregistrement à l’hôtel. Les marketeurs référencent ces définitions lorsqu’ils créent des tâches **[!UICONTROL Événement personnalisé]**. Les événements qui ne correspondent à aucune définition sont ignorés.

Lorsque votre organisation envoie des événements au format JSON, les options **[!UICONTROL Schéma]** et **[!UICONTROL Transformateur]** [!DNL Journey Optimizer] aident à valider la payload, à l’analyser et à décider de suivre ou non l’activité.

Pour créer une définition d’événement, procédez comme suit :

1. Ouvrez l’onglet **[!UICONTROL Définitions d’événement]** et créez une définition.

   ![](assets/admin-event-definition.png)

1. Saisissez un **[!UICONTROL Nom]** pour l’événement (par exemple, `Coffee purchase`). Les marketeurs voient ce nom lors de la configuration d’une tâche **[!UICONTROL Événement personnalisé]**.

1. Spécifiez la manière dont [!DNL Journey Optimizer] reconnaît l’événement dans les payloads entrants. Fournissez un **[!UICONTROL chemin d’accès à l’identifiant]**, un **[!UICONTROL identifiant de schéma XDM]** ou les deux :

   * **[!UICONTROL Chemin de l&#39;identifiant]** — Chemin d&#39;accès à un champ de la payload (par exemple, `data.memberId`). Utilisez cette option lors de la mise en correspondance des événements par valeurs dans la payload.
   * **[!UICONTROL Valeurs de l&#39;identifiant]** — Valeurs du chemin d&#39;accès de l&#39;identifiant qui doit être présent pour que cette définition corresponde.
   * **[!UICONTROL Identifiant du schéma XDM]** : identifiant du schéma XDM Experience Platform pour ce type d’événement. Utilisez cette option lorsque des événements sont capturés par rapport à un schéma connu.

1. Si nécessaire, collez les chaînes dans **[!UICONTROL Schema]** et **[!UICONTROL Transformer]** :

   * **[!UICONTROL Schéma]** — Chaîne de validation de la payload entrante.
   * **[!UICONTROL Transformateur]** — Expression de transformation (par exemple, JSONata) qui mappe votre payload au format attendu par Loyalty Challenges.

1. Enregistrez la définition de l’événement. Elle apparaît dans la liste **[!UICONTROL Définitions d’événement]** et est disponible lorsque les spécialistes marketing créent des tâches **[!UICONTROL Événement personnalisé]**. [Découvrez comment créer des tâches](create-tasks.md#choose-activity)

## Inventaire des produits {#product-inventory}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_product_inventory"
>title="Inventaire des produits"
>abstract="Chargez un fichier CSV qui mappe les identifiants d’élément aux groupes de produits. Les marketeurs peuvent référencer ces groupes lors de la configuration des articles éligibles pour les tâches d&#39;achat et de dépenses sans saisir chaque ID d&#39;article."

L’onglet **[!UICONTROL Inventaire de produits]** regroupe les articles du catalogue afin que les marketeurs puissent les cibler dans les tâches sans saisir chaque ID d’article. Chargez un **fichier CSV** qui mappe chaque identifiant d’élément à un ou plusieurs **groupes de produits** (un même élément peut appartenir à plusieurs groupes). Les groupes importés sont disponibles lors de la configuration de l&#39;éligibilité des tâches. [Découvrez comment créer des tâches](create-tasks.md)

Pour charger un fichier d’inventaire de produit, procédez comme suit :

1. Préparez un fichier CSV qui mappe chaque identifiant d’élément à un ou plusieurs groupes de produits. Développez la section ci-dessous pour afficher un exemple.

   +++Exemple de fichier CSV d’inventaire de produit

   ![](assets/admin-inventory-csv.png)

   +++

1. Ouvrez l’onglet **[!UICONTROL Inventaire des produits]**.

1. Sélectionnez **[!UICONTROL Charger]** et choisissez votre fichier CSV.

   ![](assets/admin-inventory-upload.png)

1. Vérifier les données importées dans la liste d&#39;inventaire. La liste affiche une ligne par élément. La colonne **[!UICONTROL Groupes inclus dans]** affiche chaque groupe de produits pour cet article sous la forme d’une pilule ou de plusieurs pilules lorsque l’article appartient à plusieurs groupes.

   ![](assets/admin-inventory-imported.png)

1. Pour afficher tous les éléments d’un groupe de produits, sélectionnez le pilule de ce groupe dans la colonne **[!UICONTROL Groupes inclus dans]** sur n’importe quelle ligne. La vue Détails du groupe répertorie tous les éléments du groupe.

   ![](assets/admin-inventory-group.png)

1. Ouvrez **[!UICONTROL Historique de chargement]** pour afficher les chargements de fichiers CSV précédents.

## Exclusions {#exclusions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_exclusions"
>title="Exclusions"
>abstract="Chargez un fichier CSV qui définit les éléments de catalogue et les groupes exclus à l’échelle du programme. Les groupes d’exclusions importés s’affichent lorsque les marketeurs configurent des éléments éligibles et des exclusions sur des tâches."

L’onglet **[!UICONTROL Exclusions]** définit les éléments de catalogue et les groupes qui sont exclus à l’échelle du programme, de sorte que les marketeurs n’ont pas à répertorier les mêmes exclusions sur chaque tâche. Chargez un **fichier CSV** qui mappe chaque identifiant d’élément à un ou plusieurs **groupes d’exclusion** (un même élément peut appartenir à plusieurs groupes).

Après l’importation, les éléments et groupes exclus apparaissent dans le créateur de tâches lorsque les spécialistes marketing configurent **[!UICONTROL Éléments et exclusions éligibles]**. [Découvrez comment définir des éléments éligibles et des exclusions sur les tâches](create-tasks.md#eligible-items-exclusions)

Pour charger des exclusions, procédez comme suit :

1. Préparez un fichier CSV qui mappe chaque identifiant d’élément à un ou plusieurs groupes d’exclusion. Développez la section ci-dessous pour afficher un exemple.

   +++Exemple CSV d’exclusions

   ![](assets/admin-exclusions-csv.png)

   +++

1. Ouvrez l’onglet **[!UICONTROL Exclusions]**.

1. Sélectionnez **[!UICONTROL Charger]** et choisissez votre fichier CSV.

   ![](assets/admin-exclusions-upload.png)

1. Passez en revue les données importées dans la liste d’exclusions. La liste affiche une ligne par élément. La colonne **[!UICONTROL Groupes inclus dans]** affiche chaque groupe d’exclusion de cet élément sous la forme d’une pilule ou de plusieurs pilules lorsque l’élément appartient à plusieurs groupes.

<!-- SCREENSHOT: Exclusions list after CSV upload -->

1. Pour afficher tous les éléments d’un groupe d’exclusion, sélectionnez le cachet de ce groupe dans la colonne **[!UICONTROL Groupes inclus dans]** sur n’importe quelle ligne. La vue Détails du groupe répertorie tous les éléments du groupe.

<!-- SCREENSHOT: Exclusion group details -->

1. Ouvrez **[!UICONTROL Historique de chargement]** pour afficher les chargements de fichiers CSV précédents.
