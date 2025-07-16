---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser les données Adobe Experience Platform (version Beta)
description: Découvrez comment utiliser des jeux de données Adobe Experience Platform dans les fonctionnalités de prise de décision et de personnalisation de  [!DNL Journey Optimizer] .
badge: label="Beta" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, éditeur
exl-id: 44a8bc87-5ab0-45cb-baef-e9cd75432bde
source-git-commit: 416f82a932f0b484d8463ff24090a7061461822f
workflow-type: ht
source-wordcount: '435'
ht-degree: 100%

---

# Utiliser des données Adobe Experience Platform {#aep-data}

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement disponible en version Beta publique pour l’ensemble des clientes et clients.
>
>Pour utiliser cette fonctionnalité, vous devez d’abord accepter les conditions générales de la version Beta pour votre entreprise.

Journey Optimizer vous permet d’exploiter les données d’Adobe Experience Platform dans [!DNL Journey Optimizer]. Pour ce faire, les jeux de données nécessaires à la personnalisation de la recherche doivent d’abord être activés par le biais d’un appel API, comme décrit ci-dessous. Une fois cette opération terminée, vous pouvez utiliser leurs données avec les fonctionnalités de personnalisation et de prise de décision de [!DNL Journey Optimizer].

## Restrictions et directives de la version Beta {#guidelines}

Avant de commencer, consultez les restrictions et les directives suivantes :

* **La taille d’un jeu de données** est limitée à 5 Go pour les jeux de données de production et à 1 Go pour les jeux de données de sandbox de développement.
* **Un maximum de 50 jeux de données peuvent être activés** en même temps pour la recherche, pour une organisation donnée.
* **Le nombre d’enregistrements** est limité à 5M dans les jeux de données de production et à 1M dans les jeux de données de sandbox de développement.
* **L’étiquetage et l’application de l’utilisation des données** n’est pas appliquée pour l’instant pour les jeux de données activés pour la recherche.
* **Les jeux de données activés pour la recherche et utilisés dans la personnalisation ne sont pas protégés contre la suppression**. Il vous appartient de noter les jeux de données utilisés pour la personnalisation afin de vous assurer qu’ils ne seront pas supprimés ou retirés.

## Activer un jeu de données pour la recherche de données {#enable}

Afin d’exploiter les données de votre jeu de données pour la personnalisation, vous devez utiliser un appel API pour récupérer son statut et activer le service de recherche.

### Conditions préalables {#prerequisites-enable}

* Suivez les instructions détaillées dans [cette documentation](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) pour configurer votre environnement afin d’envoyer des commandes d’API.
* Les API Adobe Journey Optimizer et Adobe Experience Platform doivent être ajoutées au projet de développement.

  ![](assets/aep-data-api.png)

* Vous devez disposer de l’autorisation « Gérer des jeux de données » dans le cadre de votre rôle.
* Le schéma sur lequel le jeu de données est basé doit contenir une **identité principale** pouvant servir de clé de recherche.

### Structure de l’appel API {#call}

```
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}"
```

Où ce qui suit est vrai :

* **L’URL** est `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`.
* **L’identifiant du jeu de données** est le jeu de données que vous souhaitez activer.
* **L’action** est Activer OU Désactiver.
* **Le jeton d’accès** peut être récupéré à partir de Developer Console.
* **La clé d’API** peut être récupérée à partir de Developer Console.
* L’**identifiant d’organisation IMS** est votre organisation Adobe.
* Le **nom du sandbox** est le nom du sandbox dans lequel se trouve le jeu de données (c’est-à-dire prod, dev, etc.).

>[!NOTE]
>
>Si vous rencontrez l’erreur ci-dessous lors de la tentative d’un appel API pour activer des jeux de données, essayez de supprimer les API Adobe Journey Optimizer de votre projet Developer Console, puis de les rajouter.
>
>```
>
>"error_code": "403003", 
>"message": "Api Key is invalid"
>
>```

Une fois qu’un jeu de données a été activé pour la recherche à l’aide d’un appel API, vous pouvez utiliser ses données dans les fonctionnalités de personnalisation et de prise de décision de [!DNL Journey Optimizer].

* [Utiliser des données Adobe Experience Platform à des fins de personnalisation](../personalization/aep-data-perso.md)
* [Utiliser des données Adobe Experience Platform à des fins de prise de décision](../experience-decisioning/aep-data-exd.md)
