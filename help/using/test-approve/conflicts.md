---
title: Identifier les conflits potentiels dans les parcours et campagnes
description: Découvrez comment identifier les conflits potentiels dans les parcours et les campagnes.
role: User
level: Beginner
badge: label="Disponibilité limitée"
hide: true
hidefromtoc: true
source-git-commit: e1121d998711ea4751da5293efdd7c1578ee44a2
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 3%

---


# Détecter les conflits potentiels dans les parcours et campagnes {#conflict}

>[!BEGINSHADEBOX]

Ce guide couvre les sujets suivants :

* [Prise en main de la gestion des conflits et de la hiérarchisation](gs-conflict-prioritization.md)
* **[Détecter les conflits potentiels dans les parcours et les campagnes](conflicts.md)**
* [Attribuer des scores de priorité aux parcours et aux campagnes](priority-scores.md)
* [Limitation et arbitrage des parcours](journey-capping.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Les outils de gestion des conflits et de hiérarchisation des conflits sont actuellement disponibles en tant que disponibilité limitée pour certains utilisateurs uniquement.

À mesure que les marketeurs augmentent le volume des campagnes et des Parcours dans Journey Optimizer, il devient de plus en plus difficile pour un marketeur de savoir s’il bombarde ses clients avec un trop grand nombre d’interactions marketing. il est donc essentiel d’identifier facilement les chevauchements des campagnes et des parcours pour s’assurer qu’ils trouvent le bon équilibre dans les communications marketing tout en atténuant le risque de fatigue client.

Les principaux domaines à surveiller pour détecter un chevauchement potentiel sont les suivants :

* **Chronologie** (dates de début et de fin) : Trop de parcours s’exécutent simultanément ?
* **Audience** : quel pourcentage de mon audience de parcours fait également partie d’autres parcours ?
* **Canal** : Existe-t-il d’autres communications programmées pour la même période, et si oui, combien ?
* **Jeu de règles de limitation** : quels types de parcours suis-je en train de plafonner et y a-t-il chevauchement dans ceux-ci ?
* **Configuration de canal** : existe-t-il d’autres parcours ou campagnes utilisant une configuration de canal utilisée dans le même parcours ou la même campagne qui peut empêcher l’affichage du parcours ou de la campagne à l’utilisateur final ?

## Détection des conflits par Journey Optimizer {#detection}

Vous trouverez ci-dessous un résumé de la manière dont Journey Optimizer identifie les conflits potentiels pour les parcours et les campagnes :

* **Portée d’identification des conflits** : les conflits s’affichent uniquement pour les campagnes et les parcours en direct ou planifiés.
* **parcours unitaires** : si le parcours sélectionné est unitaire, d’autres parcours commençant par le même événement s’affichent, car cet événement déclenchera tous ces parcours.
* **Qualification de l’audience et Lecture de l’audience/de l’événement professionnel** parcours : si le parcours sélectionné est une qualification d’audience ou un parcours Lecture d’audience/d’événement professionnel, tous les autres parcours du même type avec une audience valide sont affichés, car il peut y avoir des chevauchements entre les audiences.
* **Campagnes** : comme toutes les campagnes ciblent des audiences et qu’il n’existe aucun concept d’événement, toutes les campagnes peuvent entrer en conflit avec des parcours déclenchés par un segment (en commençant par une activité Lecture d’audience).
* **Campagnes en direct/planifiées** : les campagnes en direct et planifiées peuvent entrer en conflit les unes avec les autres en raison d’un chevauchement d’audiences potentiel. Pour une campagne donnée, toutes les campagnes en direct ou planifiées sont répertoriées dans la visionneuse de conflits.

## Affichage des conflits identifiés pour un parcours ou une campagne spécifique {#view}

Lors de la création d’un parcours ou d’une campagne, Journey Optimizer vous permet de vérifier chaque fois qu’il existe un risque de chevauchement avec d’autres parcours ou campagnes. Pour ce faire, procédez comme suit :

1. Au moment de créer un parcours ou une campagne, cliquez sur le bouton **[!UICONTROL Afficher les conflits potentiels]** dans les propriétés du parcours ou de la campagne.

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >Le bouton **[!UICONTROL Afficher les conflits potentiels]** devient disponible pour sélection dès que vous avez attribué l’un des paramètres suivants : **[!UICONTROL Date de début/fin]**, **[!UICONTROL Audience]**, **[!UICONTROL Canal]**, **[!UICONTROL Configuration de canal]** et **[!UICONTROL Ensemble de règles]**. Assurez-vous de sélectionner **[!UICONTROL Enregistrer]** après avoir affecté ces paramètres, car le bouton ne sera pas sélectionnable tant que les modifications ne seront pas enregistrées.

1. La fenêtre **[!UICONTROL Conflits potentiels]** s’ouvre, ce qui vous permet de visualiser tous les éléments qui chevauchent le parcours/la campagne actuel.

   Vous pouvez ouvrir un parcours ou une campagne se chevauchant directement à partir de cet écran en sélectionnant son nom.

   ![](assets/potential-conflicts.png)

   >[!NOTE]
   >
   >Les nouvelles campagnes publiées peuvent prendre jusqu’à 5 minutes pour s’afficher dans la visionneuse de conflits en raison de la mise en cache implémentée.

Pour affiner davantage votre recherche de superpositions potentielles, vous pouvez filtrer votre liste de campagnes et de parcours en fonction du ou des champs pertinents. Pour ce faire, sélectionnez l’icône de filtre dans la vue de stock. [Découvrez comment utiliser les filtres](../start/search-filter-categorize.md#filter-lists)

## Résoudre les conflits {#resolve}

Voici quelques conseils pour réduire les conflits potentiels une fois identifiés :

* Ajustez les **dates de début/fin** pour éviter le chevauchement de campagnes ou de parcours.
* Affinez le **ciblage d’audience** afin de minimiser le chevauchement entre les parcours.
* Mettez en oeuvre des **plafonds de fréquence** pour empêcher les clients de recevoir trop de communications.
* Réduisez le nombre de **parcours actifs** pour gérer plus efficacement l’expérience client.
* Définissez **priorités** sur les actions entrantes pour vous assurer que l’action la plus importante s’affiche pour les clients.

En exploitant ces fonctionnalités, vous pouvez vous assurer que vos efforts marketing sont harmonisés et que vous maintenez le bon équilibre dans votre stratégie de communication.
