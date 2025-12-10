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
source-git-commit: 24d66f146ea3ed0e89a3b928b805bc53a70a8895
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 52%

---

# Audience Activation dans [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Vous pouvez sélectionner dans des campagnes et des parcours n’importe quelle audience générée à l’aide de définitions de segment, de chargement personnalisé, de workflows de composition ou de composition d’audiences fédérées.

## Mécanismes de sécurisation et limitations {#guardrails}

* **Healthcare Shield ou Privacy and Security Shield** - L’utilisation des audiences et des attributs de la composition de l’audience n’est actuellement pas disponible avec Healthcare Shield ou Privacy and Security Shield. [Découvrez comment utiliser les attributs d’enrichissement des audiences dans  [!DNL Journey Optimizer]](../audience/about-audiences.md#enrichment)

* **Chargement personnalisé et composition d’audience fédérée** - Pour les audiences de chargement personnalisé et de composition d’audience fédérée, veuillez noter les mécanismes de sécurisation suivants :

   * **Prise en charge de l’aperçu et du BAT :** actuellement, l’aperçu et le BAT ne sont pas pris en charge pour les audiences créées à l’aide du chargement CSV ou de la composition d’audience fédérée. Gardez cela à l’esprit lors de la planification de vos campagnes.

   * **Ciblage de nouveaux profils :** lorsqu’une correspondance est introuvable entre un enregistrement et un profil du service de profil unifié, un profil vide est créé. Ce profil est lié aux attributs d’enrichissement stockés dans le lac de données. Comme ce nouveau profil est vide, les champs de ciblage généralement utilisés dans [!DNL Journey Optimizer] (par exemple, personalEmail.address, mobilePhone.number) sont vides. Par conséquent, ces champs ne peuvent pas être utilisés pour le ciblage.

     Pour résoudre ce problème, vous pouvez spécifier le « champ d’exécution » (ou « adresse d’exécution » selon le canal) dans la configuration des canaux en tant que « identityMap ». Cela permet de s’assurer que l’attribut choisi comme identité lors de la création de l’audience sera celui utilisé pour le ciblage dans [!DNL Journey Optimizer].

   * **Enregistrements activés et rapprochement d’identités :** chaque enregistrement de l’audience est activé, y compris les doublons. Lors de la prochaine exportation de profil Unified Profile Service, ces enregistrements passent par la combinaison d’identités. En conséquence, le nombre d’enregistrements activés peut être différent du nombre de profils après le rapprochement d’identités.

## Délai d’activation des audiences {#activation}

Une fois l’ingestion terminée, les audiences sont prêtes à être utilisées dans [!DNL Journey Optimizer]. Ce délai est généralement de moins d’une heure, mais il peut varier. Les audiences obtenues à partir de compositions devraient être disponibles 24 heures après leur publication.

Pour les audiences résultant de tâches de segmentation par lots, l’activation peut être retardée en raison de la variabilité de l’ingestion par lots. Pour les parcours en lecture d’audience planifiés tous les jours, vous pouvez définir une fenêtre temporelle dans les propriétés du parcours pour vous assurer que les nouvelles données d’audience sont disponibles avant l’exécution du parcours.

Si le traitement de la segmentation ne se termine pas dans la fenêtre temporelle définie, le parcours sera ignoré jusqu’à sa prochaine occurrence. [Découvrir la planification d’un parcours de lecture d’audience](../building-journeys/read-audience.md)

## Cibler des audiences dans [!DNL Journey Optimizer]

Vous pouvez utiliser les audiences dans **[!DNL Journey Optimizer]** de différentes manières :

* Choisissez une audience d’une **campagne**, où le message est envoyé à toutes les personnes appartenant à l’audience sélectionnée. [Découvrez comment définir l’audience d’une campagne](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilisez une activité d’orchestration **Lecture d’audience** dans un parcours pour faire en sorte que toutes les personnes de l’audience rejoignent le parcours et reçoivent les messages inclus dans votre parcours. Supposons que vous ayez une audience « cliente ou cliente Silver ». Avec cette activité, vous pouvez faire en sorte que tous les clients Silver rejoignent un parcours. Vous pouvez ensuite leur envoyer une série de messages personnalisés. [Découvrez comment configurer une activité Lecture d’audience](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

  Pour les parcours utilisant des audiences de composition d’audience ou de chargement personnalisé, les attributs de profil sont aussi récents que la dernière évaluation par lot à l’entrée du parcours. Cependant, après une activité **Attente**, le parcours actualise les attributs de profil depuis l’UPS (Unified Profile Service) en récupérant les dernières données disponibles, ce qui signifie que les attributs de profil peuvent changer pendant l’exécution du parcours. [En savoir plus sur l’actualisation du profil après une activité Attente &#x200B;](../building-journeys/wait-activity.md#profile-refresh)

* Utilisez l’activité **Condition** dans un parcours afin de créer des conditions basées sur l’appartenance à une audience. [Découvrez comment utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-a-segment).

* Utilisez l’activité d’événement **Qualification d’audience** dans un parcours pour faire en sorte que des personnes rejoignent le parcours ou y progressent en fonction des entrées et des sorties d’audiences Adobe Experience Platform. Par exemple, vous pouvez faire en sorte que tous les nouveaux clientes et clients Silver rejoignent un parcours et leur envoyer des messages. [Découvrez comment configurer une activité Qualification d’audience](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >En raison de la nature par lots des audiences créées à l’aide de workflows de composition, du chargement personnalisé et de la composition d’audiences fédérées, vous ne pouvez pas cibler ces audiences dans une activité « Qualification de l’audience ». Seules les audiences créées à l’aide de définitions de segment peuvent être utilisées dans cette activité.

## Activation des types d’audience non pris en charge dans [!DNL Journey Optimizer]

Seules les audiences créées dans le portail Audience peuvent être ciblées directement dans les parcours et campagnes [!DNL Journey Optimizer]. [En savoir plus sur les types d’audience disponibles](../audience/about-audiences.md#types).

Si vous devez cibler des profils d’une audience non prise en charge, telle qu’une audience Customer Journey Analytics, vous devez les encapsuler dans une nouvelle définition de segment dans le portail Audience. Vous trouverez des informations détaillées sur l’ajout d’audiences dans une définition de segment dans la [documentation du créateur de segments](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#adding-audiences){target="_blank"}

Une fois l’évaluation terminée, attendez qu’elle soit terminée pour l’utiliser dans vos parcours et campagnes.
