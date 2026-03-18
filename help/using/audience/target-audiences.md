---
solution: Journey Optimizer
product: journey optimizer
title: À propos des audiences Adobe Experience Platform
description: Découvrez comment utiliser les audiences Adobe Experience Platform.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 78b95ccd-bc28-46cd-937a-f68e3f34cc1e
source-git-commit: 04f6ad6d75c182c6c29744810c0461ccc947b5e5
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 94%

---

# Audience Activation dans [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Vous pouvez sélectionner dans des campagnes et des parcours n’importe quelle audience générée à l’aide de définitions de segment, de chargement personnalisé, de workflows de composition ou de composition d’audiences fédérées.

## Mécanismes de sécurisation et limitations {#guardrails}

* **Healthcare Shield ou Privacy and Security Shield** : l’utilisation des audiences et des attributs de la composition d’audiences n’est actuellement pas disponible avec Healthcare Shield ou Privacy and Security Shield. [En savoir plus sur l’utilisation des attributs d’enrichissement des audiences dans  [!DNL Journey Optimizer]](../audience/about-audiences.md#enrichment)

* **Chargement personnalisé et composition d’audiences fédérées** : pour les audiences de chargement personnalisé et de composition d’audiences fédérées, notez les mécanismes de sécurisation suivants :

   * **Prise en charge de la prévisualisation et des BAT :** actuellement, la prévisualisation et les BAT ne sont pas pris en charge pour les audiences créées à l’aide du chargement CSV ou de la composition d’audiences fédérées. Gardez cela à l’esprit lors de la planification de vos campagnes.

   * **Ciblage de nouveaux profils :** lorsqu’une correspondance est introuvable entre un enregistrement et un profil du service de profil unifié, un profil vide est créé. Ce profil est lié aux attributs d’enrichissement stockés dans le lac de données. Comme ce nouveau profil est vide, les champs de ciblage généralement utilisés dans [!DNL Journey Optimizer] (par exemple, personalEmail.address, mobilePhone.number) sont vides. Par conséquent, ces champs ne peuvent pas être utilisés pour le ciblage.

     Pour résoudre ce problème, vous pouvez spécifier le « champ d’exécution » (ou « adresse d’exécution » selon le canal) dans la configuration des canaux en tant que « identityMap ». Ainsi, l’attribut choisi comme identité lors de la création de l’audience sera celui utilisé pour le ciblage dans [!DNL Journey Optimizer].

   * **Enregistrements activés et rapprochement d’identités :** chaque enregistrement de l’audience est activé, y compris les doublons. Lors du prochain export de profils du service de profil unifié, ces enregistrements feront l’objet d’un rapprochement d’identités. En conséquence, le nombre d’enregistrements activés peut être différent du nombre de profils après le rapprochement d’identités.

## Délai d’activation des audiences {#activation}

Les audiences sont prêtes à être utilisées dans [!DNL Journey Optimizer] une fois l’ingestion terminée. Ce délai est généralement de moins d’une heure, mais il peut varier. Les audiences obtenues à partir de compositions devraient être disponibles 24 heures après leur publication.

Pour les audiences résultant de tâches de segmentation par lots, l’activation peut être retardée en raison de la variabilité de l’ingestion par lots. Pour les parcours de lecture d’audience planifiés tous les jours, vous pouvez définir une fenêtre temporelle dans les propriétés du parcours pour vous assurer que les nouvelles données d’audience sont disponibles avant l’exécution du parcours.

Si le traitement de la segmentation ne se termine pas dans la fenêtre temporelle définie, le parcours sera ignoré jusqu’à sa prochaine occurrence. [Découvrir la planification d’un parcours de lecture d’audience](../building-journeys/read-audience.md)

## Cibler des audiences dans [!DNL Journey Optimizer]

Vous pouvez utiliser les audiences dans **[!DNL Journey Optimizer]** de différentes manières :

* Choisissez une audience d’une **campagne**, où le message est envoyé à toutes les personnes appartenant à l’audience sélectionnée. [Découvrez comment définir l’audience d’une campagne](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilisez une activité d’orchestration **Lecture d’audience** dans un parcours pour faire en sorte que toutes les personnes de l’audience rejoignent le parcours et reçoivent les messages inclus dans votre parcours. Supposons que vous ayez une audience « client ou cliente Silver ». Avec cette activité, vous pouvez faire en sorte que l’ensemble des clientes et clients Silver rejoignent un parcours. Vous pouvez ensuite leur envoyer une série de messages personnalisés. [Découvrez comment configurer une activité Lecture d’audience](../building-journeys/read-audience.md#configuring-segment-trigger-activity). Pour segmenter, exclure ou fusionner des branches après leur entrée, consultez la section [Ciblage des audiences dans les parcours ](../building-journeys/read-audience.md#audience-targeting-in-journeys).

  Après l’entrée, utilisez les activités **Condition** pour [segmenter par attributs ou comportement, exclure une partie de la population ou fusionner des branches](../building-journeys/read-audience.md#audience-targeting-in-journeys).

  Pour les parcours utilisant des audiences de composition d’audiences ou de chargement personnalisé, les attributs de profil sont aussi récents que la dernière évaluation par lots à l’entrée du parcours. Cependant, après une activité **Attente**, le parcours actualise les attributs de profil depuis le service de profil unifié en récupérant les dernières données disponibles, ce qui signifie que les attributs de profil peuvent changer pendant l’exécution du parcours. [En savoir plus sur l’actualisation des profils après une activité Attente](../building-journeys/wait-activity.md#profile-refresh)

* Utilisez l’activité **Condition** dans un parcours afin de créer des conditions basées sur l’appartenance à une audience. [Découvrez comment utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-a-segment).

* Utilisez l’activité d’événement **Qualification d’audience** dans un parcours pour faire en sorte que des personnes rejoignent le parcours ou y progressent en fonction des entrées et des sorties d’audiences Adobe Experience Platform. Par exemple, vous pouvez faire en sorte que l’ensemble de la nouvelle clientèle Silver rejoigne un parcours et lui envoyer des messages. [Découvrir comment configurer une activité Qualification d’audience](../building-journeys/audience-qualification-events.md)

  >[!NOTE]
  >
  >En raison de la nature par lots des audiences créées à l’aide de workflows de composition, du chargement personnalisé et de la composition d’audiences fédérées, vous ne pouvez pas cibler ces audiences dans une activité « Qualification de l’audience ». Seules les audiences créées à l’aide de définitions de segment peuvent être utilisées dans cette activité.

## Activation des types d’audiences non pris en charge dans [!DNL Journey Optimizer]

Seules les audiences générées à l’aide d’une **définition de segment**, de **compositions d’audience**, d’un **chargement personnalisé (fichier CSV)** et d’une **composition d’audiences fédérées** peuvent être ciblées directement dans les parcours et campagnes Journey Optimizer. [Découvrir les types d’audiences disponibles](../audience/about-audiences.md#types)

Si vous devez cibler des profils d’une audience non prise en charge, telle qu’une audience Customer Journey Analytics, vous devez l’intégrer dans une nouvelle définition de segment dans le portail Audience. Vous trouverez des informations détaillées sur l’ajout d’audiences dans une définition de segment dans la [documentation du Créateur de segments](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#adding-audiences){target="_blank"}.

Une fois cela fait, attendez que l’évaluation soit terminée avant de l’utiliser dans vos parcours et campagnes.
