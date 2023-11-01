---
solution: Journey Optimizer
product: journey optimizer
title: À propos des audiences Adobe Experience Platform
description: Découvrez comment utiliser les audiences Adobe Experience Platform.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 100%

---

# Commencer avec les audiences Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Audience"
>abstract="En utilisant les données du profil client en temps réel, Adobe Experience Platform vous permet de créer facilement des définition de segment pour créer des audiences ciblées qui capturent les comportements et préférences uniques de vos clientes et clients."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Sélectionner l’audience de la campagne"
>abstract="Cette liste affiche toutes les audiences Adobe Experience Platform disponibles. Sélectionnez l’audience à cibler avec votre campagne. Le message configuré dans l’opération sera envoyé à toutes les personnes appartenant à l’audience sélectionnée. [En savoir plus sur les audiences](../audience/about-audiences.md)."

[!DNL Journey Optimizer] vous permet de créer d’utiliser des audiences Adobe Experience Platform à l’aide des données de profil client en temps réel directement à partir du menu **[!UICONTROL Audiences]** et de les utiliser dans vos parcours ou campagnes.

Pour en savoir plus, consultez la [documentation du service de segmentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr).

## Utiliser des audiences dans [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Vous pouvez utiliser les audiences dans **[!DNL Journey Optimizer]** de différentes manières :

* Choisissez une audience d’une **campagne**, où le message est envoyé à toutes les personnes appartenant à l’audience sélectionnée. [Découvrez comment définir l’audience d’une campagne](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilisez une activité d’orchestration **Lecture d’audience** dans un parcours pour faire en sorte que toutes les personnes de l’audience rejoignent le parcours et reçoivent les messages inclus dans votre parcours.

  Supposons que vous ayez une audience « cliente ou cliente Silver ». Avec cette activité, vous pouvez faire en sorte que tous les clientes et clients Silver rejoignent un parcours et leur envoyer une série de messages personnalisés. [Découvrez comment configurer une activité Lecture d’audience](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Utilisez l’activité d’événement **Qualification d’audience** dans un parcours pour faire en sorte que des personnes rejoignent le parcours ou y progressent en fonction des entrées et des sorties d’audiences Adobe Experience Platform.

  Par exemple, vous pouvez faire en sorte que tous les nouveaux clientes et clients Silver rejoignent un parcours et leur envoyer des messages. Pour plus d’informations sur l’utilisation de cette activité, reportez-vous à la section [Découvrez comment configurer une activité de qualification d’audience](../building-journeys/audience-qualification-events.md).

* Utilisez l’activité **Condition** dans un parcours afin de créer des conditions basées sur l’appartenance à une audience. [Découvrez comment utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-a-segment).

## Méthodes d’évaluation d’audience{#evaluation-method-in-journey-optimizer}

Dans Adobe Journey Optimizer, les audiences sont générées à partir des définitions de segment à l’aide de l’une des deux méthodes d’évaluation :

* **Segmentation par flux** : la liste des profils de l’audience est actualisée en temps réel pendant que de nouvelles données affluent dans le système.

  La segmentation par flux est un processus continu de sélection des données qui met à jour vos audiences en réponse à l’activité des utilisateurs et utilisatrices. Une fois qu’une définition de segment a été créée et que l’audience obtenue a été enregistrée, la définition du segment s’applique aux données entrantes dans Journey Optimizer. Cela signifie que des personnes sont ajoutées ou supprimées de l’audience au fur et à mesure que leurs données de profil changent, permettant de toujours assurer la pertinence de votre audience cible.

* **Segmentation par lots** : l’évaluation de la liste des profils de l’audience se fait toutes les 24 heures.

  La segmentation par lots est une alternative à la segmentation par flux qui traite toutes les données de profil à la fois par le biais de définitions de segment. Cela crée un instantané de l’audience qui peut être enregistré et exporté pour utilisation. Cependant, contrairement à la segmentation par flux, la segmentation par lots ne met pas à jour la liste des audiences en temps réel, et les nouvelles données qui entrent après le traitement par lots ne seront pas répercutées dans l’audience avant le traitement par lots suivant.

Le système détermine la segmentation par lots et la segmentation par flux pour chaque audience, en fonction de la complexité et du coût de l’évaluation de la règle de définition de segment. Vous pouvez afficher la méthode d’évaluation pour chaque audience dans la colonne **[!UICONTROL Méthode d’évaluation]** de la liste des audiences.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Si la colonne **[!UICONTROL Méthode d’évaluation]** ne s’affiche pas, vous devez l’ajouter à l’aide du bouton de configuration situé en haut à droite de la liste.

Une fois que vous avez défini une audience pour la première fois, les profils sont ajoutés à l’audience lorsqu’ils remplissent les critères.

Le renvoi de l’audience à partir de données antérieures peut prendre jusqu’à 24 heures. Une fois l’audience renvoyée, elle est constamment tenue à jour et toujours prête pour le ciblage.
