---
title: Gestion des conflits et hiérarchisation
description: Découvrez comment tirer parti des outils de gestion des conflits et de hiérarchisation de Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: 8146221975b7460bf1deaca9363d1624b719b480
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 100%

---

# Gestion des conflits et hiérarchisation {#conflict-prioritization}

## Outils de gestion des conflits et de hiérarchisation {#tools}

Dans Journey Optimizer, la gestion du volume et du calendrier des campagnes et des parcours est essentielle pour éviter de submerger les clientes et clients avec un trop grand nombre d’interactions. Journey Optimizer propose plusieurs outils de gestion des conflits et de hiérarchisation.

Ces outils sont disponibles pour les parcours de campagnes et unitaires, de qualification d’audience et de lecture d’audience.

En utilisant ces outils, vous pouvez garantir des efforts marketing plus réguliers et plus ciblés, en délivrant le bon message au bon moment tout en évitant les conflits et la surcharge.

### Outil de détection des conflits

Grâce à l’**outil de détection des conflits**, vous pouvez identifier les chevauchements potentiels dans les parcours et les campagnes. Cela est essentiel, car trop de communications simultanées peuvent entraîner une fatigue des clientes et des clients. Journey Optimizer vous permet de surveiller les éléments tels que les chronologies, le chevauchement des audiences et les configurations de canaux. En identifiant les conflits de manière précoce, vous pouvez affiner vos campagnes pour éviter de bombarder les clientes et les clients avec de nombreux messages en même temps.

➡️ [Découvrir comment détecter des conflits potentiels dans les parcours et les campagnes](conflicts.md)

### Scores de priorité

Les **scores de priorité** vous aident à contrôler les campagnes ou les parcours qui sont prioritaires lorsqu’un client ou une cliente est admissible à plusieurs communications. Cela s’avère particulièrement utile pour les canaux entrants, tels que le Web et les appareils mobiles, où une seule campagne peut être affichée à un moment donné. En attribuant un score de priorité à chaque parcours ou campagne, vous pouvez vous assurer que le message le plus important est diffusé en premier.

➡️ [Découvrir comment attribuer des scores de priorité aux parcours et campagnes](priority-scores.md)

### Jeux de règles

Les jeux de règles vous permettent de **regrouper plusieurs règles en jeux de règles** et de les appliquer aux parcours et aux campagnes de votre choix. Cela permet d’améliorer la granularité afin de limiter la fréquence et le nombre de parcours qu’un client ou une cliente peut rejoindre au cours d’une certaine période ou de contrôler la fréquence à laquelle les utilisateurs et utilisatrices recevront un message selon le type de communication. [Découvrir comment utiliser les jeux de règles](../conflict-prioritization/rule-sets.md)

* **Limitation et arbitrage des parcours**

  Les jeux de règles permettent de limiter la fréquence et le nombre de parcours qu’un client ou une cliente peut rejoindre au cours d’une période donnée. Vous pouvez configurer des règles afin de limiter le nombre d’entrées dans un parcours pour un profil ou le nombre de parcours auxquels un client ou une cliente peut être inscrit en même temps.

  De plus, vous pouvez utiliser les paramètres d’arbitrage pour décider du parcours qu’un client ou une cliente doit rejoindre s’il remplit les conditions requises pour plusieurs parcours, à l’aide de scores de priorité permettant de déterminer la meilleure correspondance.

  ➡️ [Découvrir comment utiliser la limitation et l’arbitrage de parcours](journey-capping.md)

* **Capping de la fréquence par type de canal et de communication**

  Vous pouvez également utiliser des jeux de règles pour définir le capping de la fréquence par type de communication (par exemple, ventes, promotionnel) afin d’éviter de surcharger les clientes et les clients avec des messages redondants. Vous pouvez contrôler la fréquence sur plusieurs canaux, en excluant automatiquement les profils sur-sollicités afin d’offrir une meilleure expérience client.

  ➡️ [Découvrir comment définir un capping de la fréquence par type de canal et de communication](../conflict-prioritization/channel-capping.md)

## Mécanismes de sécurisation et limitations

* **Campagnes et scores de priorité** - Dans les campagnes, le score de priorité est disponible uniquement pour les canaux entrants **web**, **in-app** et **basés sur du code**.

* **Latence de mise à jour du compteur de profils**

  La mise à jour de la valeur du compteur de profils peut prendre jusqu’à 10 minutes après qu’un client ou une cliente a rejoint un parcours.

  Si un profil rejoint deux parcours dans un laps de temps réduit, le second parcours peut ne pas détecter correctement que la limitation de fréquence a déjà été atteinte, ce qui risque d’autoriser le profil à rejoindre les deux parcours.

* **Priorité de l’espace de nommage pour la limitation des entrées de parcours**

  La limitation des entrées n’est prise en charge que si l’espace de nommage sélectionné dans le parcours est celui ayant la priorité la plus élevée dans le sandbox. Si la priorité de l’espace de noms n’a pas été configurée explicitement, la priorité la plus élevée par défaut est celle des e-mails.

* **Activations simultanées dans les parcours de qualification d’audience**

  Lorsque plusieurs parcours de qualification d’audience sont activés par le même événement de qualification d’audience, les décomptes pour la limitation des entrées ne seront pas précis. Si les décomptes sont inférieurs à la limite, le parcours poursuivra l’arbitrage, mais il ne pourra pas obtenir les décomptes les plus récents avec des activations simultanées.
