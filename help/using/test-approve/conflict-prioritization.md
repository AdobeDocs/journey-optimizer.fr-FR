---
title: Gestion des conflits et hiérarchisation
description: Découvrez comment prévisualiser et tester votre contenu.
feature: Preview, Proofs
role: User
level: Beginner
badge: label="Disponibilité limitée"
hide: true
hidefromtoc: true
source-git-commit: e1121d998711ea4751da5293efdd7c1578ee44a2
workflow-type: tm+mt
source-wordcount: '1187'
ht-degree: 100%

---


# Gestion des conflits et hiérarchisation {#conflict-prioritization}

>[!AVAILABILITY]
>
>Les outils de gestion des conflits et de hiérarchisation sont actuellement disponibles en version bêta pour certains utilisateurs et utilisatrices uniquement.

Dans Journey Optimizer, la gestion du volume et du calendrier des campagnes et des parcours est essentielle pour éviter de submerger les clientes et clients avec un trop grand nombre d’interactions. Les deux sections suivantes présentent des outils clés pour vous aider à maintenir l’équilibre et à hiérarchiser efficacement les communications.

## Identifier les conflits potentiels dans les parcours et les campagnes {#conflict}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Visionneuse de conflits dans les campagnes"
>abstract="Cet outil peut vous aider à déterminer le chevauchement avec d’autres parcours, campagnes ou configurations de canal. Si vous souhaitez identifier le chevauchement sur l’audience, la date de début et de fin, la configuration des canaux, le canal ou le jeu de règles, vous pouvez afficher les conflits potentiels ici."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Visionneuse de conflits dans les parcours"
>abstract="Cet outil peut vous aider à déterminer le chevauchement avec d’autres parcours, campagnes ou configurations de canal. Si vous souhaitez identifier le chevauchement sur l’audience, la date de début et de fin, la configuration des canaux, le canal ou le jeu de règles, vous pouvez afficher les conflits potentiels ici."

À mesure que les personnes spécialisées dans le marketing augmentent le volume des campagnes et des parcours dans Journey Optimizer, il devient de plus en plus difficile pour elles de savoir si leurs clientes et clients sont submergés par un trop grand nombre d’interactions marketing. Il est donc essentiel d’identifier facilement les chevauchements des campagnes et des parcours pour s’assurer d’un bon équilibre dans les communications marketing tout en atténuant le risque de lassitude des clientes et clients.

Les principaux domaines à surveiller pour détecter un chevauchement potentiel sont les suivants :

* **Chronologie** (dates de début et de fin) : trop de parcours s’exécutent-ils simultanément ?
* **Audience** : quel pourcentage de mon audience de parcours fait également partie d’autres parcours ?
* **Canal** : existe-t-il d’autres communications programmées pour la même période, et si oui, combien ?
* **Jeu de règles de capping** : quels types de parcours suis-je en train de limiter et se chevauchent-ils ?
* **Configuration des canaux** : existe-t-il d’autres parcours ou campagnes utilisant une configuration des canaux utilisée dans le même parcours ou la même campagne qui peut empêcher l’affichage du parcours ou de la campagne aux utilisateurs et utilisatrices finaux ?

### Détection des conflits par Journey Optimizer {#detection}

Vous trouverez ci-dessous un résumé de la manière dont Journey Optimizer identifie les conflits potentiels pour les parcours et les campagnes :

* **Portée d’identification des conflits** : les conflits s’affichent uniquement pour les campagnes et les parcours en ligne ou planifiés.
* **Parcours unitaires** : si le parcours sélectionné est unitaire, les autres parcours commençant par le même événement s’affichent, car cet événement déclenchera tous ces parcours.
* Parcours **Qualification d’audience et Lecture d’audience/événement métier** : si le parcours sélectionné est un parcours Qualification d’audience ou Lecture d’audience/événement métier, tous les autres parcours du même type avec une audience valide sont affichés, car il peut y avoir des chevauchements entre les audiences.
* **Campagnes** : comme toutes les campagnes ciblent des audiences et qu’il n’existe aucun concept d’événement, toutes les campagnes peuvent entrer en conflit avec des parcours déclenchés par un segment (en commençant par une activité Lecture d’audience).
* **Campagnes en ligne/planifiées** : les campagnes en ligne et planifiées peuvent entrer en conflit les unes avec les autres en raison d’un chevauchement d’audiences potentiel. Pour une campagne donnée, toutes les campagnes en ligne ou planifiées sont répertoriées dans la visionneuse de conflits.

### Afficher les conflits identifiés pour un parcours ou une campagne spécifique {#view}

Lors de la création d’un parcours ou d’une campagne, Journey Optimizer vous permet de vérifier chaque fois qu’il existe un risque de chevauchement avec d’autres parcours ou campagnes. Pour ce faire, procédez comme suit :

1. Au moment de créer un parcours ou une campagne, cliquez sur le bouton **[!UICONTROL Afficher les conflits potentiels]** dans les propriétés du parcours ou de la campagne.

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >Vous pouvez sélectionner le bouton **[!UICONTROL Afficher les conflits potentiels]** dès que vous avez attribué l’un des paramètres suivants : **[!UICONTROL Date de début/fin]**, **[!UICONTROL Audience]**, **[!UICONTROL Canal]**, **[!UICONTROL Configuration des canaux]** et **[!UICONTROL Jeu de règles]**. Assurez-vous de sélectionner **[!UICONTROL Enregistrer]** après avoir affecté ces paramètres, car le bouton ne sera pas sélectionnable tant que les modifications ne seront pas enregistrées.

1. La fenêtre **[!UICONTROL Conflits potentiels]** s’ouvre, ce qui vous permet de visualiser tous les éléments en chevauchement avec la campagne ou le parcours actuel.

   Vous pouvez ouvrir un parcours ou une campagne en chevauchement directement à partir de cet écran en sélectionnant son nom.

   ![](assets/potential-conflicts.png)

   >[!NOTE]
   >
   >L’affichage des nouvelles campagnes publiées peut prendre jusqu’à 5 minutes dans la visionneuse de conflits en raison de la mise en cache implémentée.

Pour affiner davantage votre recherche de chevauchements potentiels, vous pouvez filtrer votre liste de campagnes et de parcours en fonction des champs pertinents. Pour ce faire, sélectionnez l’icône de filtre dans la vue d’inventaire. [Découvrir comment utiliser les filtres](../start/search-filter-categorize.md#filter-lists)

### Résoudre les conflits {#resolve}

Voici quelques conseils pour réduire les conflits potentiels une fois qu’ils sont identifiés :

* Ajustez les **dates de début/fin** pour éviter le chevauchement de campagnes ou de parcours.
* Affinez le **ciblage d’audience** afin de minimiser le chevauchement entre les parcours.
* Mettez en œuvre des **limitations de la fréquence** pour empêcher les clientes et clients de recevoir trop de communications.
* Réduisez le nombre de **parcours actifs** pour gérer plus efficacement l’expérience des clientes et clients.
* Définissez les **priorités** sur les actions entrantes pour vous assurer que l’action la plus importante s’affiche pour les clientes et les clients.

En utilisant ces fonctionnalités, vous pouvez vous assurer que vos efforts marketing sont harmonisés et que vous maintenez le bon équilibre dans votre politique de communication.

## Attribuer des scores de priorité aux parcours et aux campagnes {#priority}

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Priorité"
>abstract="Attribuez un score de priorité au parcours, allant de 0 à 100. Les nombres plus élevés signalent une priorité plus élevée. La valeur de priorité insérée ici est héritée par toute action entrante (in-app, par exemple) contenue dans ce parcours. Dans les cas où cette même configuration de canal entrant est utilisée dans d’autres campagnes ou parcours, l’action entrante ayant le score de priorité le plus élevé est présentée aux destinataires. Si plusieurs parcours ou campagnes ont le même score, l’élément qui a été modifié le plus récemment est sélectionné."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Priorité"
>abstract="Attribuez un score de priorité à la campagne, allant de 0 à 100. Les nombres plus élevés signalent une priorité plus élevée. Dans les cas où cette même configuration de canal entrant (in-app, par exemple) est utilisée dans d’autres campagnes ou parcours, l’action entrante ayant le score de priorité le plus élevé est présentée aux destinataires. Si plusieurs parcours ou campagnes ont le même score, l’élément qui a été modifié le plus récemment est sélectionné."

Journey Optimizer vous permet d’attribuer un score de priorité à un parcours ou à une campagne. La priorité est essentielle pour donner la priorité à un parcours, à une campagne ou à une action lorsqu’une contrainte est imposée (par exemple, une limitation de la fréquence). Dans les cas où une personne est admissible pour plusieurs parcours, campagnes ou communications et que vous souhaitez choisir ceux qu’elle doit rejoindre et recevoir, vous devez utiliser ce champ.

>[!NOTE]
>
>Le score de priorité est disponible pour les canaux entrants : web, in-app et basé sur du code. Dans le parcours, le score de priorité est disponible uniquement pour les canaux **in-app** et **basés sur du code**.

L’attribution d’un score de priorité est essentielle pour la communication entrante, par exemple web, mobile et in-app. Si plusieurs campagnes utilisent la même configuration des canaux (une bannière dans la partie supérieure de votre page web, par exemple), cela peut s’avérer problématique, car seul le contenu d’une campagne peut être affiché. Le score de priorité est l’emplacement où vous insérerez vos préférences pour la campagne qui doit s’afficher lorsque les destinataires peuvent être admissibles pour plusieurs campagnes.

Pour attribuer un score de priorité à un parcours ou à une campagne, saisissez une valeur numérique (de 0 à 100) dans le champ **[!UICONTROL Score de priorité]** situé dans les propriétés du parcours ou de la campagne. Notez que plus le nombre est élevé, plus la priorité est élevée. Si vous créez cette campagne et souhaitez vous assurer que le contenu de cette campagne s’affiche, donnez-lui un score de 100.

![](assets/priority-score.png)

Dans les cas où deux campagnes ont le même score de priorité, la campagne qui a été activée en premier s’affiche.
