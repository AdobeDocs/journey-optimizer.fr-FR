---
title: Gestion des conflits et hiérarchisation
description: Découvrez comment tirer parti des outils de gestion des conflits et de hiérarchisation de Journey Optimizer.
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
TQID: https://experienceleague.adobe.com/vx-CmsYwj7QyN2sVMrpJ9VUNDgnXq8qt1nT9lHOFV3s
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: fd59660e-de8a-4bfb-85dc-7fa546030c49
subfeature_v2: id: e23d48b5-7858-4d45-9c56-9e2b4be8500eid: f3fe4813-f254-4f8f-99cc-24bd67f119e1id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
source-git-commit: 49542ca70e8899061bc79772cf96069ab2587ab2
workflow-type: tm+mt
source-wordcount: 896
ht-degree: 95%

---

# Gestion des conflits et hiérarchisation {#conflict-prioritization}

>[!BEGINSHADEBOX]

**Sur cette page :** Découvrez comment la détection des conflits, les scores de priorité et les ensembles de règles fonctionnent ensemble afin d’éviter les communications qui se chevauchent et de contrôler la fréquence des messages envoyés aux clients.

>[!ENDSHADEBOX]

Dans Journey Optimizer, la gestion du volume et du calendrier des campagnes et des parcours est essentielle pour éviter de submerger les clientes et clients avec un trop grand nombre d’interactions. Les outils de gestion des conflits et de hiérarchisation vous permettent de diffuser des communications réfléchies et opportunes en prévenant la lassitude des clients et clientes et en veillant à ce que les bons messages atteignent votre audience. Grâce à la détection des conflits, les scores de priorité et les jeux de règles, vous pouvez rationaliser les campagnes et les parcours afin d’éviter les chevauchements et équilibrer la fréquence sur l’ensemble des canaux.

Ces outils sont disponibles pour les parcours de campagnes et unitaires, de qualification d’audience et de lecture d’audience. Que vous définissiez des limites sur la fréquence d’envoi des messages ou décidiez quelles campagnes sont prioritaires, ces fonctionnalités s’associent pour simplifier la prise de décision et optimiser votre stratégie marketing.

## Par où commencer {#where-to-start}

| Votre objectif | Outil | Action |
|-----------|------|--------|
| Vérifier si les parcours ou les campagnes se chevauchent (chronologie, audience, canal) | **Détection des conflits** | [Identifier les conflits potentiels](conflicts.md) |
| Choisir le message qui gagne lorsqu’un profil se qualifie pour plusieurs | **Scores de priorité** | [Attribuer des scores de priorité](priority-scores.md) |
| Limiter la fréquence ou le nombre de messages reçus par un profil | **Jeux de règles** (capping de la fréquence, limitation du parcours, heures de tranquillité) | [Définir les règles de limitation des messages et des parcours](../../rp_landing_pages/capping-rules-landing-page.md) |

**Flux standard :** utilisez la détection des conflits pour repérer les chevauchements, puis appliquez des scores de priorité et des ensembles de règles pour contrôler quels messages sont envoyés et à quelle fréquence.

## Outils de gestion et de hiérarchisation des conflits {#tools}

### Outil de détection des conflits

Grâce à l’**outil de détection des conflits**, vous pouvez identifier les chevauchements potentiels dans les parcours et les campagnes. Cela est essentiel, car trop de communications simultanées peuvent entraîner une fatigue des clientes et des clients. Journey Optimizer vous permet de surveiller les éléments tels que les chronologies, le chevauchement des audiences et les configurations de canaux. En identifiant les conflits de manière précoce, vous pouvez affiner vos campagnes pour éviter de bombarder les clientes et les clients avec de nombreux messages en même temps.

[Découvrez comment détecter des conflits potentiels dans les parcours et les campagnes.](conflicts.md)

### Scores de priorité

Les **scores de priorité** vous aident à contrôler les campagnes ou les parcours qui sont prioritaires lorsqu’un client ou une cliente est admissible à plusieurs communications. Cela s’avère particulièrement utile pour les canaux entrants, tels que le Web et les appareils mobiles, où une seule campagne peut être affichée à un moment donné. En attribuant un score de priorité à chaque parcours ou campagne, vous pouvez vous assurer que le message le plus important est diffusé en premier.

[Découvrez comment attribuer des scores de priorité aux parcours et campagnes.](priority-scores.md)

### Jeux de règles

Les jeux de règles vous permettent de **regrouper plusieurs règles en jeux de règles** et de les appliquer aux parcours et aux campagnes de votre choix. Cela permet d’améliorer la granularité afin de limiter la fréquence et le nombre de parcours qu’un client ou une cliente peut rejoindre au cours d’une certaine période ou de contrôler la fréquence à laquelle les utilisateurs et utilisatrices recevront un message selon le type de communication.

* **Limitation et arbitrage des parcours** – Les jeux de règles permettent de limiter la fréquence et le nombre de parcours qu’un client ou une cliente peut rejoindre au cours d’une période donnée. Vous pouvez limiter le nombre d’entrées dans un parcours pour un profil ou le nombre de parcours auxquels un client ou une cliente peut s’inscrire en même temps. Utilisez les paramètres d’arbitrage pour décider du parcours qu’un client ou une cliente doit rejoindre s’il ou elle remplit les conditions requises pour plusieurs parcours, à l’aide de scores de priorité permettant de déterminer la meilleure correspondance. [Découvrez comment utiliser la limitation et l’arbitrage de parcours.](journey-capping.md)

* **Limitation de la fréquence par canal et type de communication** : définissez le capping de la fréquence par type de communication (par exemple, commerciale, promotionnelle) pour éviter de surcharger les clientes et clients avec des messages répétitifs. Contrôlez la fréquence sur plusieurs canaux, en excluant automatiquement les profils sur-sollicités. [Découvrez comment définir un capping de la fréquence par type de canal et de communication](channel-capping.md)

* **Heures de tranquillité** : définissez des exclusions temporelles afin qu’aucun message ne soit envoyé pendant certains créneaux (e-mail, SMS, notification push, WhatsApp). [Découvrez comment définir des heures de tranquillité.](quiet-hours.md)

[Découvrir comment utiliser les jeux de règles](rule-sets.md)

## Mécanismes de sécurisation et limitations {#guardrails}

* **Campagnes et scores de priorité** - Dans les campagnes, le score de priorité est disponible uniquement pour les canaux entrants **web**, **in-app** et **basés sur du code**.

* **Latence de mise à jour du compteur de profils** - La mise à jour de la valeur du compteur de profils peut prendre jusqu’à 10 minutes après qu’un client ou une cliente a rejoint un parcours. Si un profil rejoint deux parcours dans un laps de temps réduit, le second parcours peut ne pas détecter correctement que la limitation de fréquence a déjà été atteinte, ce qui risque d’autoriser le profil à rejoindre les deux parcours.

* **Priorité de l’espace de noms pour la limitation des entrées de parcours** - La limitation des entrées n’est prise en charge que si l’espace de noms sélectionné dans le parcours est celui ayant la priorité la plus élevée dans le sandbox. Si la priorité de l’espace de noms n’a pas été configurée explicitement, la priorité la plus élevée par défaut est celle des e-mails.

* **Activations simultanées dans les parcours de qualification d’audience** - Lorsque plusieurs parcours de qualification d’audience sont activés par le même événement de qualification d’audience, les décomptes pour la limitation des entrées ne seront pas précis. Si les décomptes sont inférieurs à la limite, le parcours poursuivra l’arbitrage, mais il ne pourra pas obtenir les décomptes les plus récents avec des activations simultanées.

## Ressources supplémentaires

* **[Identifier les conflits possibles](conflicts.md)** - Découvrez comment identifier et résoudre les conflits entre les campagnes et les parcours qui se chevauchent.
* **[Affecter les scores de priorité](priority-scores.md)** - Découvrez comment attribuer et utiliser des scores de priorité pour contrôler la priorité de diffusion des messages.
* **[Créer des jeux de règles](rule-sets.md)** - Découvrez comment créer et appliquer des jeux de règles pour la gestion des conflits et la gouvernance des messages.
* **[Limitation et arbitrage des parcours](journey-capping.md)** - Définissez des règles de limitation et des arbitrages au niveau des parcours.
* **[Limitation de la fréquence par canal](channel-capping.md)** - Définissez des cappings de fréquence au niveau du canal pour éviter les messages excessifs.
* **[Définir les heures de tranquillité](quiet-hours.md)** - Définissez des exclusions temporelles pour la diffusion des messages.
* **[Tutoriels sur la gestion des conflits](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/conflict-management/identify-potential-conflicts){target="_blank"}** - Tutoriels vidéo détaillés.
* **[Cas d’utilisation de Journey Optimizer](../building-journeys/jo-use-cases.md)** - Parcourez les modèles pratiques, y compris la logique de limitation de la fréquence et de suppression des parcours.
