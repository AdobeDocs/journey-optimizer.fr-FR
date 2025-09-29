---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser les données d’Adobe Experience Platform
description: Découvrez comment utiliser des jeux de données Adobe Experience Platform dans les fonctionnalités de prise de décision et de personnalisation de  [!DNL Journey Optimizer] .
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, éditeur
mini-toc-levels: 1
exl-id: 44a8bc87-5ab0-45cb-baef-e9cd75432bde
source-git-commit: e9ed993dd5957adb305b582b30e6675d2bb4526f
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 90%

---

# Utiliser les données d’Adobe Experience Platform {#aep-data}

>[!CONTEXTUALHELP]
>id="lookup-aep-data"
>title="Activer pour la recherche"
>abstract="L’activation d’un jeu de données pour la recherche permet d’exploiter ses données dans les fonctionnalités de personnalisation, de prise de décision et d’orchestration de parcours de Journey Optimizer."

Journey Optimizer vous permet d’exploiter les données des données Adobe Experience Platform avec des fonctionnalités de personnalisation, de prise de décision et d’orchestration des parcours. Pour ce faire, les jeux de données basés sur des enregistrements nécessaires à la personnalisation de la recherche doivent d’abord être activés pour le service de recherche, comme décrit ci-dessous.

## À lire impérativement

### Mécanismes de sécurisation et directives {#guidelines}

Avant de commencer, consultez les restrictions et les directives suivantes :

* Les jeux de données activés pour la recherche ne doivent contenir aucune information d’identification personnelle (PII).
* Les jeux de données activés pour la recherche et utilisés dans la personnalisation ne sont pas protégés contre la suppression. Il vous appartient de noter les jeux de données utilisés pour la personnalisation afin de vous assurer qu’ils ne seront pas supprimés ou retirés.
* Les jeux de données doivent être associés à un schéma qui N’est PAS de type Profil ou Événement.
* L’ingestion de données en flux continu est prise en charge pour les jeux de données activés pour la recherche. Gardez à l’esprit que le traitement de l’ingestion doit toujours être terminé avant que les données ne soient disponibles pour la personnalisation ou la prise de décision.

### Droit pour le service de recherche

| Composant de fonctionnalité | Limites | Remarques |
| ------- | ------- | ------- |
| Jeux de données de recherche activés | Max. 10 par organisation | Nombre maximal de jeux de données pouvant être configurés pour la recherche à un moment donné. Cette limite s’applique au nombre total cumulé de jeux de données de recherche dans les sandbox de production et de développement au sein de l’instance client. |
| Nombre d’enregistrements de jeux de données | Jusqu’à 2 millions d’enregistrements par jeu de données | Nombre maximal d’enregistrements autorisés dans un seul jeu de données, calculé comme le nombre total de tous les lots de ce jeu de données. |
| Taille des enregistrements | Jusqu’à 2 Ko par enregistrement | Taille maximale d’enregistrement par défaut prise en charge. |
| Taille des jeux de données | Jusqu’à 4 Go | Taille maximale d’un jeu de données, et non la taille cumulée de tous les jeux de données d’un sandbox. Les limites de nombre d’enregistrements et de taille des jeux de données sont des mécanismes de sécurisation indépendants, et les deux doivent être respectées. |
| Mises à jour de la fréquence des jeux de données | Jusqu’à 5 mises à jour par jour et par jeu de données | Fréquence maximale des opérations de mise à jour autorisée pour un seul jeu de données par jour. |

>[!NOTE]
>
>Si vous avez besoin de volumes supplémentaires au-delà des mécanismes de sécurisation répertoriés ci-dessus, contactez votre représentant ou représentante Adobe.

## Activer un jeu de données pour la recherche de données {#enable}

Pour utiliser les données d’un jeu de données à des fins de personnalisation, vous devez l’activer pour la recherche.

### Conditions préalables {#prerequisites-enable}

Le schéma associé au jeu de données que vous souhaitez activer pour la recherche doit être de type Enregistrement. Le schéma NE doit PAS appartenir à une classe Profil ou Événement.

+++Exemple

![](assets/data-lookup-schema.png)

+++

Une identité principale doit être définie pour le schéma.

+++Exemple

![](assets/data-lookup-primary.png)

+++

Si aucun espace de noms personnalisé n’a été défini, assurez-vous que l’identité est un identifiant qui ne concerne pas une personne.

+++Exemple

![](assets/aep-data-namespace.png)

+++

### Activer le jeu de données pour la recherche dans l’interface de gestion des jeux de données

Dans l’interface d’utilisation de la gestion des jeux de données, utilisez le bouton (bascule) pour activer le jeu de données pour la recherche.

![](assets/aep-data-enable.png)

>[!NOTE]
>
>Il est recommandé de NE PAS activer également le jeu de données pour le profil, car cela peut augmenter la richesse du profil, ce qui n’est pas nécessaire pour effectuer des recherches.

### Méthode API

Suivez les instructions détaillées dans [cette documentation](https://developer.adobe.com/journey-optimizer-apis/references/authentication/) pour configurer votre environnement afin d’envoyer des commandes d’API.

#### Conditions préalables

* Les API Adobe Journey Optimizer et Adobe Experience Platform doivent être ajoutées au projet de développement.

  ![](assets/aep-data-api.png)

* Vous devez disposer de l’autorisation « Gérer des jeux de données » dans le cadre de votre rôle.

* Le schéma sur lequel le jeu de données est basé doit contenir une identité principale pouvant servir de clé de recherche.

#### Structure de l’appel API

```shell
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}" 
```

Où ce qui suit est vrai :

* L’URL est `https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`.
* L’ID du jeu de données est le jeu de données que vous souhaitez activer.
* L’action est Activer OU Désactiver.
* Le jeton d’accès peut être récupéré à partir de Developer Console.
* La clé d’API peut être récupérée à partir de Developer Console.
* L’ID d’organisation IMS est votre organisation Adobe.
* Le nom du sandbox est celui du sandbox dans lequel se trouve le jeu de données (c’est-à-dire prod, dev, etc.).

>[!NOTE]
>
>Si vous rencontrez l’erreur ci-dessous lors d’une tentative d’appel API pour activer des jeux de données, essayez de supprimer les API Adobe Journey Optimizer de votre projet Developer Console, puis de les rajouter :
>
>`"error_code": "403003",`
>`"message": "Api Key is invalid"`

## Surveillance du jeu de données

Une fois qu’un jeu de données a été activé pour la recherche, vous pouvez consulter le statut de l’ingestion dans le service de recherche en accédant au menu **[!UICONTROL Surveillance]** et en sélectionnant l’onglet **[!UICONTROL Journey Optimizer]**.

Cet indicateur de processus permet de déterminer quand de nouveaux lots de données sont disponibles dans le service de recherche.

![](assets/aep-data-monitoring.png)

## Étapes suivantes

Une fois qu’un jeu de données a été activé pour la recherche à l’aide d’un appel API, vous pouvez utiliser ses données dans les fonctionnalités de personnalisation et de prise de décision de [!DNL Journey Optimizer]. Pour plus d’informations, consultez les sections suivantes :

* [Utiliser des données Adobe Experience Platform à des fins de personnalisation](../personalization/aep-data-perso.md)
* [Utiliser des données Adobe Experience Platform à des fins de prise de décision](../experience-decisioning/aep-data-exd.md)
* [Utilisation des données Adobe Experience Platform pour l’orchestration des parcours](../building-journeys/dataset-lookup.md)
