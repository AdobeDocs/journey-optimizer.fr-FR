---
solution: Journey Optimizer
product: journey optimizer
title: À propos des segments Adobe Experience Platform
description: Découvrez comment configurer un segment Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 6c255d66fb89ba756add062d8a4315dd622fd8e7
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 100%

---

# Commencer avec les segments d’Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Segment"
>abstract="En utilisant les données du profil client en temps réel, Adobe Experience Platform vous permet de créer facilement des segments ciblés qui capturent les comportements et préférences uniques de vos clientes et clients."

[!DNL Journey Optimizer] vous permet de créer des segments Adobe Experience Platform à l’aide des données de profil client en temps réel directement à partir du menu **[!UICONTROL Segments]** et d’utiliser ces segments dans vos parcours ou campagnes.

De plus, les segments peuvent également être créés à partir du service de segmentation lui-même. Pour en savoir plus, consultez la [documentation du service de segmentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr).

## Utiliser les segments dans [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Vous pouvez exploiter les segments dans **[!DNL Journey Optimizer]** de différentes manières :

* Choisissez un segment comme **audience d’une campagne**, où le message est envoyé à tous les individus appartenant au segment sélectionné. [Découvrez comment définir l’audience d’une campagne](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilisez une activité d’orchestration **Lecture de segment** dans un parcours pour faire en sorte que tous les individus du segment rejoignent le parcours et reçoivent les messages inclus dans votre parcours.

  Supposons que vous ayez un segment « client(e) Silver ». Avec cette activité, vous pouvez faire en sorte que tous les clients et clientes Silver rejoignent un parcours et leur envoyer une série de messages personnalisés. [Découvrez comment configurer une activité Lecture de segment](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilisez l’activité d’événement **Qualification de segment** dans un parcours pour faire en sorte que des individus rejoignent le parcours ou y progressent en fonction des entrées et des sorties de segments Adobe Experience Platform.

  Par exemple, vous pouvez faire en sorte que tous les nouveaux clients et clientes Silver rejoignent un parcours et leur envoyer des messages. Pour plus d’informations sur l’utilisation de cette activité, reportez-vous à la section [Découvrez comment configurer une activité de qualification de segment](../building-journeys/segment-qualification-events.md).

* Utilisez l’activité **Condition** dans un parcours afin de créer des conditions basées sur l’appartenance à un segment. [Découvrez comment utiliser des segments dans des conditions](../building-journeys/condition-activity.md#using-a-segment).

## Méthodes d’évaluation d’audience{#evaluation-method-in-journey-optimizer}

Dans Adobe Journey Optimizer, les audiences sont générées à partir des définitions de segment à l’aide de l’une des deux méthodes d’évaluation :

* **Segmentation par flux** : la liste des audiences du segment est actualisée en temps réel pendant que de nouvelles données affluent dans le système.

  La segmentation par flux en continu est un processus continu de sélection des données qui met à jour vos segments en réponse à l’activité des utilisateurs et des utilisatrices. Une fois qu’un segment a été créé et enregistré, la définition du segment s’applique aux données entrantes dans Journey Optimizer. Cela signifie que des individus sont ajoutés ou supprimés du segment au fur et à mesure que leurs données de profil changent, permettant de toujours assurer la pertinence de votre audience cible.

* **Segmentation par lots** : l’évaluation de la liste des audiences du segment se fait toutes les 24 heures.

  La segmentation par lots est une alternative à la segmentation par flux qui traite toutes les données de profil à la fois par le biais de définitions de segment. Cela crée un instantané de l’audience qui peut être enregistré et exporté pour utilisation. Cependant, contrairement à la segmentation par flux, la segmentation par lots ne met pas à jour la liste des audiences en temps réel, et les nouvelles données qui entrent après le traitement par lots ne seront pas répercutées dans le segment avant le traitement par lots suivant.

Le système détermine la segmentation par lots et la segmentation par flux pour chaque définition de segment, en fonction de la complexité et du coût de l’évaluation de la règle de segment. Vous pouvez afficher la méthode d’évaluation pour chaque segment dans la colonne **[!UICONTROL Méthode d’évaluation]** de la liste des segments.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Si la colonne **[!UICONTROL Méthode d’évaluation]** ne s’affiche pas, vous devez l’ajouter à l’aide du bouton de configuration situé en haut à droite de la liste.

Une fois que vous avez défini un segment pour la première fois, les profils sont ajoutés à l’audience lorsqu’ils remplissent les critères.

Le renvoi de l’audience à partir de données antérieures peut prendre jusqu’à 24 heures. Une fois l’audience renvoyée, elle est constamment tenue à jour et toujours prête pour le ciblage.
