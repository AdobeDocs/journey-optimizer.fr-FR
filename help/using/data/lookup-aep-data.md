---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des données Adobe Experience Platform
description: Découvrez comment utiliser des jeux de données Adobe Experience Platform dans les fonctionnalités de prise de décision et de personnalisation de  [!DNL Journey Optimizer] .
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, éditeur
mini-toc-levels: 1
exl-id: 44a8bc87-5ab0-45cb-baef-e9cd75432bde
source-git-commit: e3c6b00ccc0d034fc42dd1294a9b3a72054a48d3
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 17%

---

# Utiliser des données Adobe Experience Platform {#aep-data}

>[!CONTEXTUALHELP]
>id="lookup-aep-data"
>title="Activer pour la recherche"
>abstract="L’activation d’un jeu de données pour la recherche permet d’exploiter ses données dans les fonctionnalités de personnalisation, de prise de décision et d’orchestration de parcours de Journey Optimizer."

Journey Optimizer vous permet d’exploiter les données des données Adobe Experience Platform avec des fonctionnalités de personnalisation, de prise de décision et d’orchestration des parcours. Pour ce faire, les jeux de données basés sur des enregistrements nécessaires à la personnalisation de la recherche doivent d’abord être activés pour le service de recherche, comme décrit ci-dessous.

## À lire absolument

### Mécanismes de sécurisation et directives {#guidelines}

Avant de commencer, consultez les restrictions et les directives suivantes :

* Les jeux de données activés pour la recherche ne doivent contenir aucune information d’identification personnelle (PII).
* Les jeux de données activés pour la recherche et utilisés dans la personnalisation ne sont pas protégés contre la suppression. Il vous appartient de noter les jeux de données utilisés pour la personnalisation afin de vous assurer qu’ils ne seront pas supprimés ou retirés.
* Les jeux de données doivent être associés à un schéma qui n’est PAS de type Profil ou Événement .
* Les schémas doivent avoir une identité principale. Une seule clé primaire peut être utilisée pour les recherches.

### Droit pour le service de recherche

| Composant de fonction | Limites | Notes |
| ------- | ------- | ------- |
| Jeux de données de recherche activés | 10 max. par organisation | Nombre maximal de jeux de données pouvant être configurés pour la recherche à un moment donné. Cette limite s’applique au nombre total combiné de jeux de données de recherche dans les sandbox de production et de développement au sein de l’instance client. |
| Nombre d’enregistrements du jeu de données | Jusqu’à 2 millions d’enregistrements par jeu de données | Nombre maximal d’enregistrements autorisés dans un seul jeu de données, calculé comme le nombre total sur tous les lots de ce jeu de données. |
| Taille d’enregistrement | Jusqu’à 2 Ko par enregistrement | Taille maximale d’enregistrement par défaut prise en charge. |
| Taille du jeu de données | Jusqu’à 4 Go | Taille maximale d’un jeu de données individuel, et non de la taille combinée de tous les jeux de données d’un sandbox. Le nombre d’enregistrements et les limites de taille du jeu de données sont des mécanismes de sécurisation indépendants ; les deux doivent être respectés. |
| Mises à jour de la fréquence des jeux de données | Jusqu’à 5 mises à jour par jour et par jeu de données | Fréquence maximale des opérations de mise à jour autorisée pour un seul jeu de données par jour. |

>[!NOTE]
>
>Si des volumes supplémentaires sont nécessaires au-delà des mécanismes de sécurisation répertoriés ci-dessus, contactez votre représentant Adobe.

## Activer un jeu de données pour la recherche de données {#enable}

Pour exploiter les données de votre jeu de données à des fins de personnalisation, vous devez activer le jeu de données pour la recherche.

### Conditions préalables {#prerequisites-enable}

Le schéma associé à votre jeu de données que vous souhaitez activer pour la recherche doit être de type enregistrement. Le schéma ne doit PAS appartenir à une classe de profil ou d’événement.

+++Exemple

![](assets/data-lookup-schema.png)

+++

Une identité principale doit être définie pour le schéma.

+++Exemple

![](assets/data-lookup-primary.png)

+++

Si aucun espace de noms personnalisé n’a été défini, assurez-vous que l’identité est un identifiant non-personne.

+++Exemple

![](assets/aep-data-namespace.png)

+++

### Activer le jeu de données pour la recherche dans l’interface de gestion des jeux de données

Dans l’interface utilisateur de gestion des jeux de données, utilisez le bouton pour activer le jeu de données pour la recherche.

![](assets/aep-data-enable.png)

>[!NOTE]
>
>Il est recommandé que le jeu de données NE soit PAS également activé pour le profil, car cela peut entraîner une augmentation de la richesse du profil et n’est pas nécessaire à l’exécution des recherches.

### Méthode API

Suivez les instructions détaillées dans [cette documentation](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) pour configurer votre environnement afin d’envoyer des commandes API.

#### Conditions préalables

* Les API Adobe Journey Optimizer et Adobe Experience Platform doivent être ajoutées au projet de développement.

  ![](assets/aep-data-api.png)

* Vous devez disposer de l’autorisation « Gérer des jeux de données » dans le cadre de votre rôle.

* Le schéma sur lequel est basé le jeu de données doit contenir une identité principale qui peut servir de clé de recherche.

#### Structure de l’appel API

```shell
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}" 
```

Où ce qui suit est vrai :

* L’URL est `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* L’identifiant du jeu de données est le jeu de données pour lequel vous souhaitez activer.
* L’action est activer OU désactiver.
* Le jeton d’accès peut être récupéré à partir de Developer Console.
* La clé API peut être récupérée à partir de Developer Console.
* L’ID d’organisation IMS est votre organisation Adobe.
* Nom du sandbox correspond au nom du sandbox dans lequel se trouve le jeu de données (c’est-à-dire prod, dev, etc.).

>[!NOTE]
>
>Si vous rencontrez l’erreur ci-dessous lors d’un appel API pour activer des jeux de données, essayez de supprimer les API Adobe Journey Optimizer de votre projet Developer Console, puis ajoutez-les à nouveau :
>
>`"error_code": "403003",`
>`"message": "Api Key is invalid"`

## Surveillance des jeux de données

Une fois qu’un jeu de données a été activé pour la recherche, vous pouvez consulter le statut de l’ingestion dans le service de recherche en accédant au menu **[!UICONTROL Surveillance]** et en sélectionnant l’onglet **[!UICONTROL Journey Optimizer]**.

Cet indicateur de processus permet de comprendre à quel moment de nouveaux lots de données sont disponibles dans le service de recherche.

![](assets/aep-data-monitoring.png)

## Étapes suivantes

Une fois qu’un jeu de données a été activé pour la recherche à l’aide d’un appel API, vous pouvez utiliser les données avec des fonctionnalités de personnalisation et de prise de décision [!DNL Journey Optimizer]. Pour plus d’informations, consultez les sections suivantes :

* [Utiliser des données Adobe Experience Platform à des fins de personnalisation](../personalization/aep-data-perso.md)
* [Utiliser des données Adobe Experience Platform à des fins de prise de décision](../experience-decisioning/aep-data-exd.md)
* [Utilisation des données Adobe Experience Platform pour l’orchestration des parcours](../building-journeys/dataset-lookup.md)
