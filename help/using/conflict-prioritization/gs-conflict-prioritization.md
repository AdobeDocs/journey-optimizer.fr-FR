---
title: Gestion des conflits et hiérarchisation
description: Découvrez comment tirer parti des outils de gestion des conflits et de hiérarchisation de Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: a0eda2e1d021af37eb54f3ffa5bac0ac6e8ef6ce
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 31%

---

# Gestion des conflits et hiérarchisation {#conflict-prioritization}

Dans Journey Optimizer, la gestion du volume et du calendrier des campagnes et des parcours est essentielle pour éviter de submerger les clientes et clients avec un trop grand nombre d’interactions. Les outils de gestion des conflits et de hiérarchisation vous permettent de diffuser des communications réfléchies et opportunes, de prévenir la fatigue des clients et de garantir que les bons messages parviennent à votre audience. Grâce à la détection des conflits, aux scores de priorité et aux ensembles de règles, vous pouvez rationaliser les campagnes et les parcours afin d’éviter les chevauchements et d’équilibrer la fréquence sur l’ensemble des canaux.

Ces outils sont disponibles pour les campagnes et pour les parcours unitaires, de qualification d’audience et de lecture d’audience. Que vous définissiez des limites sur la fréquence d’envoi des messages ou décidiez quelles campagnes sont prioritaires, ces fonctionnalités s’associent pour simplifier la prise de décision et optimiser votre stratégie marketing.

## Par où commencer {#where-to-start}

| Votre objectif | Outil | Action |
|-----------|------|--------|
| Vérifiez si les parcours ou les campagnes se chevauchent (chronologie, audience, canal). | **Détection des conflits** | [Identifier les conflits potentiels](conflicts.md) |
| Choisir le message qui gagne lorsqu’un profil se qualifie pour plusieurs | **Scores de priorité** | [Attribuer des scores de priorité](priority-scores.md) |
| Limiter la fréquence ou le nombre de messages reçus par un profil | **Ensembles de règles** (limitation de la fréquence, limitation du parcours, heures calmes) | [Définir des règles de limitation des messages et des parcours &#x200B;](../../rp_landing_pages/capping-rules-landing-page.md) |

**Flux standard :** utilisez la détection des conflits pour repérer les chevauchements, puis appliquez des scores de priorité et des ensembles de règles pour contrôler quels messages sont envoyés et à quelle fréquence.

## Outils de gestion des conflits et de hiérarchisation {#tools}

### Outil de détection des conflits

Grâce à l’**outil de détection des conflits**, vous pouvez identifier les chevauchements potentiels dans les parcours et les campagnes. Cela est essentiel, car trop de communications simultanées peuvent entraîner une fatigue des clientes et des clients. Journey Optimizer vous permet de surveiller les éléments tels que les chronologies, le chevauchement des audiences et les configurations de canaux. En identifiant les conflits de manière précoce, vous pouvez affiner vos campagnes pour éviter de bombarder les clientes et les clients avec de nombreux messages en même temps.

[Découvrez comment détecter des conflits potentiels dans les parcours et les campagnes](conflicts.md)

### Scores de priorité

Les **scores de priorité** vous aident à contrôler les campagnes ou les parcours qui sont prioritaires lorsqu’un client ou une cliente est admissible à plusieurs communications. Cela s’avère particulièrement utile pour les canaux entrants, tels que le Web et les appareils mobiles, où une seule campagne peut être affichée à un moment donné. En attribuant un score de priorité à chaque parcours ou campagne, vous pouvez vous assurer que le message le plus important est diffusé en premier.

[Découvrez comment attribuer des scores de priorité aux parcours et aux campagnes](priority-scores.md)

### Jeux de règles

Les ensembles de règles vous permettent de **regrouper plusieurs règles** et de les appliquer aux parcours et aux campagnes de votre choix. Vous obtenez ainsi une granularité améliorée qui permet de limiter la fréquence et le nombre de parcours qu’un client peut entrer au cours d’une certaine période ou de contrôler la fréquence à laquelle les utilisateurs et utilisatrices reçoivent des messages en fonction du type de communication.

* **Limitation et arbitrage des Parcours** - Limitez la fréquence et le nombre de parcours qu’un client peut entrer au cours d’une période donnée. Vous pouvez limiter le nombre d’entrées de parcours pour un profil ou le nombre de parcours auxquels un client peut être inscrit en même temps. Utilisez les paramètres d’arbitrage pour décider quel parcours un client doit entrer s’il est éligible à plusieurs parcours, à l’aide des scores de priorité pour déterminer le meilleur ajustement. [Découvrir comment utiliser la limitation et l’arbitrage de parcours](journey-capping.md)

* **Capping de la fréquence par canal et type de communication** - Définissez le capping de la fréquence par type de communication (par exemple, Ventes, Promotionnel) pour éviter de surcharger les clients avec des messages similaires. Contrôlez la fréquence sur plusieurs canaux, en excluant automatiquement les profils sur-sollicités. [Découvrez comment définir le capping de la fréquence par canal et type de communication](channel-capping.md)

* **Heures calmes** - Définissez des exclusions temporelles afin qu’aucun message ne soit envoyé pendant des périodes spécifiques (e-mail, SMS, notification push, WhatsApp). [Découvrez comment définir des heures de calme](quiet-hours.md)

[Découvrir comment utiliser les jeux de règles](rule-sets.md)

## Mécanismes de sécurisation et limitations {#guardrails}

* **Campagnes et scores de priorité** - Dans les campagnes, le score de priorité est disponible uniquement pour les canaux entrants **web**, **in-app** et **basés sur du code**.

* **Latence de mise à jour du compteur de profil** - La mise à jour de la valeur du compteur de profil peut prendre jusqu’à 10 minutes après qu’un client a saisi un parcours. Si un profil rejoint deux parcours dans un laps de temps réduit, le second parcours peut ne pas détecter correctement que la limitation de fréquence a déjà été atteinte, ce qui risque d’autoriser le profil à rejoindre les deux parcours.

* **Priorité des espaces de noms pour le capping des entrées de parcours** - Le capping des entrées n’est pris en charge que si l’espace de noms sélectionné dans le parcours est l’espace de noms avec la priorité la plus élevée défini dans le sandbox. Si la priorité de l’espace de noms n’a pas été configurée explicitement, la priorité la plus élevée par défaut est celle des e-mails.

* **Activations simultanées dans les parcours de qualification d’audience** - Lorsque plusieurs parcours de qualification d’audience sont activés par le même événement de qualification d’audience, les décomptes pour la limitation d’entrée ne seront pas précis. Si les décomptes sont inférieurs au plafond, le parcours continuera à arbitrer, mais il ne pourra pas obtenir les décomptes les plus récents avec des activations simultanées.

## Ressources supplémentaires

* **[Identifier les conflits potentiels](conflicts.md)** - Découvrez comment détecter et résoudre les conflits entre les campagnes et les parcours qui se chevauchent.
* **[Attribuer des scores de priorité](priority-scores.md)** - Découvrez comment attribuer et utiliser des scores de priorité pour contrôler la priorité de diffusion des messages.
* **[Utiliser des ensembles de règles](rule-sets.md)** - Découvrez comment créer et appliquer des ensembles de règles pour la gestion des conflits et la gouvernance des messages.
* **[Limitation et arbitrage des Parcours](journey-capping.md)** - Configurez des règles de limitation et d’arbitrage au niveau du parcours.
* **[Capping de la fréquence par canal](channel-capping.md)** - Définissez des limitations de fréquence au niveau du canal pour éviter les messages excessifs.
* **[Définir des heures creuses](quiet-hours.md)** - Définissez des exclusions temporelles pour la diffusion des messages.
* **[Tutoriels sur la gestion des conflits](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}** - Tutoriels vidéo détaillés.
