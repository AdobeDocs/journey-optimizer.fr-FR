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
source-git-commit: c30a74ccdaec81cbbb28e3129d5c351a0fe64bfc
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 90%

---

# Audience Activation dans [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Vous pouvez sélectionner dans des campagnes et des parcours n’importe quelle audience générée à l’aide de définitions de segment, de chargement personnalisé, de workflows de composition ou de composition d’audiences fédérées.

>[!AVAILABILITY]
>
>L’utilisation des audiences et des attributs de la composition d’audiences est actuellement indisponible avec Healthcare Shield ou Privacy and Security Shield. [Découvrez comment utiliser les attributs d’enrichissement d’audiences dans Journey Optimizer](../audience/about-audiences.md#enrichment)

## Délai d’activation des audiences {#activation}

Les audiences sont prêtes à être utilisées dans Journey Optimizer une fois l’ingestion terminée. Ce délai est généralement de moins d’une heure, mais il peut varier. Les audiences obtenues à partir de compositions devraient être disponibles 24 heures après leur publication.

Pour les audiences résultant de tâches de segmentation par lots, l’activation peut être retardée en raison de la variabilité de l’ingestion par lots. Pour les parcours de lecture d’audience planifiés tous les jours, vous pouvez définir une fenêtre temporelle dans les propriétés du parcours pour vous assurer que les nouvelles données d’audience sont disponibles avant l’exécution du parcours. Si le traitement de la segmentation ne se termine pas dans la fenêtre temporelle définie, le parcours sera ignoré jusqu’à sa prochaine occurrence. [Découvrir la planification d’un parcours de lecture d’audience](../building-journeys/read-audience.md)

## Chargement personnalisé et composition d’audiences fédérées

Pour les audiences de chargement personnalisé et de composition d’audiences fédérées, notez les mécanismes de sécurisation suivants :

* **Prise en charge de la prévisualisation et du BAT :** actuellement, la prévisualisation et le BAT ne sont pas pris en charge pour les audiences créées à l’aide du chargement CSV ou de la composition d’audiences fédérées. Gardez cela à l’esprit lors de la planification de vos campagnes.

* **Ciblage de nouveaux profils :** lorsqu’une correspondance est introuvable entre un enregistrement et un profil du service de profil unifié, un profil vide est créé. Ce profil est lié aux attributs d’enrichissement stockés dans le lac de données. Ce nouveau profil étant vide, les champs de ciblage généralement utilisés dans Journey Optimizer (par exemple, personalEmail.address, mobilePhone.number) sont vides et ne peuvent donc pas être utilisés pour le ciblage.

  Pour résoudre ce problème, vous pouvez spécifier le « champ d’exécution » (ou « adresse d’exécution » selon le canal) dans la configuration des canaux en tant que « identityMap ». Ainsi, l’attribut choisi comme identité lors de la création de l’audience sera celui utilisé pour le ciblage dans Journey Optimizer.

* **Enregistrements activés et rapprochement d’identités :** chaque enregistrement de l’audience est activé, y compris les doublons. Lors du prochain export de profils du service de profil unifié, ces enregistrements feront l’objet d’un rapprochement d’identités. En conséquence, le nombre d’enregistrements activés peut être différent du nombre de profils après le rapprochement d’identités.

## Cibler des audiences dans [!DNL Journey Optimizer]

Vous pouvez utiliser les audiences dans **[!DNL Journey Optimizer]** de différentes manières :

* Choisissez une audience d’une **campagne**, où le message est envoyé à toutes les personnes appartenant à l’audience sélectionnée. [Découvrez comment définir l’audience d’une campagne](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilisez une activité d’orchestration **Lecture d’audience** dans un parcours pour faire en sorte que toutes les personnes de l’audience rejoignent le parcours et reçoivent les messages inclus dans votre parcours. Supposons que vous ayez une audience « cliente ou cliente Silver ». Avec cette activité, vous pouvez faire en sorte que tous les clientes et clients Silver rejoignent un parcours et leur envoyer une série de messages personnalisés. [Découvrez comment configurer une activité Lecture d’audience](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

  Pour les parcours utilisant des audiences de composition d’audience ou de chargement personnalisé, les attributs de profil sont aussi récents que la dernière évaluation par lot à l’entrée du parcours. Cependant, après une activité **Attente**, le parcours actualise les attributs de profil depuis l’UPS (Unified Profile Service) en récupérant les dernières données disponibles, ce qui signifie que les attributs de profil peuvent changer pendant l’exécution du parcours. [En savoir plus sur l’actualisation du profil après une activité Attente &#x200B;](../building-journeys/wait-activity.md#profile-refresh)

* Utilisez l’activité **Condition** dans un parcours afin de créer des conditions basées sur l’appartenance à une audience. [Découvrez comment utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-a-segment).

* Utilisez l’activité d’événement **Qualification d’audience** dans un parcours pour faire en sorte que des personnes rejoignent le parcours ou y progressent en fonction des entrées et des sorties d’audiences Adobe Experience Platform. Par exemple, vous pouvez faire en sorte que tous les nouveaux clientes et clients Silver rejoignent un parcours et leur envoyer des messages. Pour plus d’informations sur l’utilisation de cette activité, reportez-vous à la section [Découvrez comment configurer une activité de qualification d’audience](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >En raison de la nature par lots des audiences créées à l’aide de workflows de composition, du chargement personnalisé et de la composition d’audiences fédérées, vous ne pouvez pas cibler ces audiences dans une activité « Qualification de l’audience ». Seules les audiences créées à l’aide de définitions de segment peuvent être utilisées dans cette activité.
