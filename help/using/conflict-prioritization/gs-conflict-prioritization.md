---
title: Gestion des conflits et hiérarchisation
description: Découvrez comment tirer parti des outils de gestion des conflits et de hiérarchisation de Journey Optimizer.
role: User
level: Beginner
badge: label="Disponibilité limitée"
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: f55f985375cf360ce55074cb227b6c424db05b5c
workflow-type: ht
source-wordcount: '677'
ht-degree: 100%

---

# Gestion des conflits et hiérarchisation {#conflict-prioritization}

>[!AVAILABILITY]
>
>Les capacités de gestion des conflits et de hiérarchisation sont actuellement accessibles en disponibilité limitée pour un groupe sélectionné de clientes et de clients. Notez que ces fonctionnalités seront progressivement déployées vers d’autres utilisateurs et utilisatrices à l’avenir. Contactez votre équipe de compte si vous souhaitez qu’elle vous ajoute à la liste d’attente pour ces fonctionnalités.

Dans Journey Optimizer, la gestion du volume et du calendrier des campagnes et des parcours est essentielle pour éviter de submerger les clientes et clients avec un trop grand nombre d’interactions. Journey Optimizer propose plusieurs outils de gestion des conflits et de hiérarchisation.

Ces outils sont disponibles pour les parcours de campagnes et unitaires, de qualification d’audience et de lecture d’audience.

En utilisant ces outils, vous pouvez garantir des efforts marketing plus réguliers et plus ciblés, en délivrant le bon message au bon moment tout en évitant les conflits et la surcharge.

## Outils de gestion des conflits et de hiérarchisations {#tools}

Grâce à l’**outil de détection des conflits**, vous pouvez identifier les chevauchements potentiels dans les parcours et les campagnes. Cela est essentiel, car trop de communications simultanées peuvent entraîner une fatigue des clientes et des clients. Journey Optimizer vous permet de surveiller les éléments tels que les chronologies, le chevauchement des audiences et les configurations de canaux. En identifiant les conflits de manière précoce, vous pouvez affiner vos campagnes pour éviter de bombarder les clientes et les clients avec plusieurs messages en même temps. [Découvrir comment détecter des conflits potentiels dans les parcours et campagnes](conflicts.md)

En outre, les **scores de priorité** vous aident à contrôler les campagnes ou les parcours qui sont prioritaires lorsqu’un client ou une cliente est admissible pour plusieurs communications. Cela s’avère particulièrement utile pour les canaux entrants, tels que le Web et les appareils mobiles, où une seule campagne peut être affichée à un moment donné. En attribuant un score de priorité à chaque parcours ou campagne, vous pouvez vous assurer que le message le plus important est diffusé en premier. [Découvrir comment attribuer des scores de priorité aux parcours et campagnes](priority-scores.md)

La **limitation et l’arbitrage des parcours** vous permettent de limiter la fréquence et le nombre de parcours qu’un client ou une cliente peut rejoindre au cours d’une période donnée. Vous pouvez configurer des règles afin de limiter le nombre d’entrées de parcours pour un profil ou le nombre de parcours auxquels une personne cliente peut être inscrite en même temps. De plus, vous pouvez utiliser les paramètres d’arbitrage pour décider quel parcours une personne cliente doit rejoindre si elle remplit les conditions requises pour plusieurs parcours, à l’aide de scores de priorité pour déterminer la meilleure approximation. [Découvrir comment utiliser la limitation et l’arbitrage de parcours](journey-capping.md)

Enfin, vous pouvez également utiliser des ensembles de règles pour définir la **capping de la fréquence par type de communication** (par exemple, ventes, promotionnelle) afin d’éviter de surcharger les clientes et les clients avec des messages redondants. Vous pouvez contrôler la fréquence sur plusieurs canaux, en excluant automatiquement les profils sur-sollicités afin d’offrir une meilleure expérience clientèle. [Découvrir comment utiliser les jeux de règles](../configuration/rule-sets.md)</li></ul>

En utilisant ces fonctionnalités, vous pouvez garantir des efforts marketing plus réguliers et plus ciblés, en délivrant le bon message au bon moment tout en évitant les conflits et la surcharge.

## Mécanismes de sécurisation et limitations

**Capping de la fréquence et audiences par lots**

Pour le capping de la fréquence, à la fois du canal ou du parcours, si vous utilisez une audience par lots, la valeur du compteur de profil référencée au moment de l’entrée dans le parcours ou l’envoi du message pour une communication de canal proviendra de l’instantané quotidien.

Cela peut s’avérer problématique, car les clientes et clients peuvent dépasser le capping de la fréquence s’ils ont rejoint un autre parcours ou s’ils ont reçu une autre communication entre l’heure de l’instantané quotidien et l’heure d’entrée dans le parcours (ou de la diffusion du message).

**Capping de la fréquence et audiences en flux continu**

Pour les audiences en flux continu, le système peut prendre jusqu’à deux heures pour reconnaître une valeur de compteur mise à jour. Nous vous recommandons donc d’espacer les communications et les parcours d’au moins deux heures afin de réduire ce risque.

**Heure de début des parcours**

Pour que les fonctions de gestion des conflits et de hiérarchisation fonctionnent correctement, nous vous recommandons de définir l’heure de début du parcours au moins 10 minutes à l’avance, afin de permettre au système de mettre à jour le compteur.

Si les clientes et clients ont déjà atteint la limite au moment de rejoindre un parcours, l’entrée leur sera refusée, mais s’ils n’ont pas atteint la limite, le compteur d’entrée n’augmentera pas.

**Arbitrage de parcours**

Pour l’instant, seuls les parcours d’audience en lecture seule sont pris en charge pour l’arbitrage de parcours. Les paramètres d’arbitrage ne peuvent pas être utilisés pour les parcours unitaires ou de qualification d’audience.
