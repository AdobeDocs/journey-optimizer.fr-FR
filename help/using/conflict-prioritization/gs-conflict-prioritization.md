---
title: Gestion des conflits et hiérarchisation
description: Découvrez comment tirer parti des outils de gestion des conflits et de hiérarchisation de Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: 6da1d9a3edb8a30b8f13fd0cb6a138f22459ad00
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 28%

---

# Gestion des conflits et hiérarchisation {#conflict-prioritization}

## Outils de gestion des conflits et de hiérarchisations {#tools}

Dans Journey Optimizer, la gestion du volume et du calendrier des campagnes et des parcours est essentielle pour éviter de submerger les clientes et clients avec un trop grand nombre d’interactions. Journey Optimizer propose plusieurs outils de gestion des conflits et de hiérarchisation.

Ces outils sont disponibles pour les parcours de campagnes et unitaires, de qualification d’audience et de lecture d’audience.

En utilisant ces outils, vous pouvez garantir des efforts marketing plus réguliers et plus ciblés, en délivrant le bon message au bon moment tout en évitant les conflits et la surcharge.

### Outil de détection des conflits

Grâce à l’**outil de détection des conflits**, vous pouvez identifier les chevauchements potentiels dans les parcours et les campagnes. Cela est essentiel, car trop de communications simultanées peuvent entraîner une fatigue des clientes et des clients. Journey Optimizer vous permet de surveiller les éléments tels que les chronologies, le chevauchement des audiences et les configurations de canaux. En identifiant les conflits de manière précoce, vous pouvez affiner vos campagnes pour éviter de bombarder les clients de plusieurs messages en même temps.

➡️ [Découvrez comment détecter des conflits potentiels dans les parcours et les campagnes](conflicts.md)

### Scores de priorité

**Les scores de priorité** vous permettent de contrôler les campagnes ou les parcours prioritaires lorsqu’un client est éligible à plusieurs communications. Cela s’avère particulièrement utile pour les canaux entrants, tels que le Web et les appareils mobiles, où une seule campagne peut être affichée à un moment donné. En attribuant un score de priorité à chaque parcours ou campagne, vous pouvez vous assurer que le message le plus important est diffusé en premier.

➡️ [Découvrez comment attribuer des scores de priorité aux parcours et aux campagnes](priority-scores.md)

### Jeux de règles

Les ensembles de règles vous permettent de **regrouper plusieurs règles en ensembles de règles** et de les appliquer aux parcours et aux campagnes de votre choix. Cela permet d’obtenir une granularité améliorée afin de limiter la fréquence et le nombre de parcours qu’un client peut entrer au cours d’une certaine période ou de contrôler la fréquence à laquelle les utilisateurs et utilisatrices recevront un message selon le type de communication.

* **Limitation et arbitrage des parcours**

  Les ensembles de règles vous permettent de limiter la fréquence et le nombre de parcours qu’un client peut entrer au cours d’une certaine période. Vous pouvez également configurer des règles pour limiter le nombre d’entrées de parcours pour un profil ou le nombre de parcours auxquels un client peut être inscrit en même temps.

  De plus, vous pouvez utiliser les paramètres d’arbitrage pour décider quel parcours un client doit entrer s’il est éligible à plusieurs parcours, à l’aide des scores de priorité pour déterminer le meilleur ajustement.

  ➡️ [Découvrez comment utiliser la limitation et l’arbitrage des parcours ](journey-capping.md)

* **Capping de la fréquence par canal et type de communication**

  Vous pouvez également utiliser des ensembles de règles pour définir le capping de la fréquence par type de communication (par exemple, Ventes, Promotionnel) afin d’éviter de surcharger les clients avec des messages similaires. Vous pouvez contrôler la fréquence sur plusieurs canaux, en excluant automatiquement les profils sur-sollicités afin d’offrir une meilleure expérience client.

  ➡️ [Découvrez comment définir le capping de la fréquence par canal et type de communication](../conflict-prioritization/channel-capping.md)

## Mécanismes de sécurisation et limitations

* **Campagnes et scores de priorité** - Dans les campagnes, le score de priorité est disponible uniquement pour les canaux entrants **web**, **in-app** et **basés sur du code**.

* **Latence de mise à jour du compteur de profils**

  La mise à jour de la valeur du compteur de profil peut prendre jusqu’à 20 minutes après qu’un client a rejoint un parcours.

  Si un profil entre dans deux parcours dans une courte fenêtre, le deuxième parcours peut ne pas reconnaître correctement que la limitation de fréquence a déjà été atteinte, ce qui peut permettre au profil d’entrer dans les deux parcours.

* **Priorité de l’espace de noms pour le capping des entrées de parcours**

  La limitation des entrées n’est prise en charge que si l’espace de noms sélectionné dans le parcours est l’espace de noms avec la priorité la plus élevée défini dans le sandbox. Si la priorité de l’espace de noms n’a pas été configurée explicitement, la priorité la plus élevée par défaut est e-mail.

* **Activations simultanées dans les parcours de qualification d’audience**

  Lorsque plusieurs parcours de qualification d’audience sont activés par le même événement de qualification d’audience, les décomptes pour la limitation d’entrée ne seront pas précis. Si les décomptes sont inférieurs au plafond, le parcours continuera à arbitrer, mais il ne pourra pas obtenir les décomptes les plus récents avec des activations simultanées.
