---
solution: Journey Optimizer
product: journey optimizer
title: À propos des audiences Adobe Experience Platform
description: Découvrez comment utiliser les audiences Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 28%

---

# Prise en main des audiences Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Audience   "
>abstract="En exploitant les données de Real-time Customer Profile, Adobe Experience Platform vous permet de créer facilement des définitions de segment afin de créer des audiences ciblées qui capturent les comportements et les préférences uniques de vos clients."

[!DNL Journey Optimizer] vous permet de créer et d’exploiter des audiences Adobe Experience Platform à l’aide de données Real-time Customer Profile directement à partir de la variable **[!UICONTROL Audiences]** et les utiliser dans vos parcours ou campagnes.

Pour en savoir plus, consultez la [documentation du service de segmentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr).

## Utilisation des audiences dans [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Vous pouvez exploiter les audiences dans **[!DNL Journey Optimizer]** de différentes manières :

* Choisissez une audience pour une **campaign**, où le message est envoyé à tous les individus appartenant à l’audience sélectionnée. [Découvrez comment définir l’audience d’une campagne](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilisez une **Lecture d’audience** activité d’orchestration dans un parcours pour faire entrer toutes les personnes de l’audience dans le parcours et recevoir les messages inclus dans votre parcours.

  Disons que vous avez un public &quot;client Silver&quot;. Avec cette activité, vous pouvez faire en sorte que tous les clients et clientes Silver rejoignent un parcours et leur envoyer une série de messages personnalisés. [Découvrez comment configurer une activité Lecture d’audience](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Utilisez la variable **Qualification de l’audience** activité d’événement dans un parcours pour faire entrer ou avancer des individus dans le parcours en fonction des entrées et des sorties d’audience Adobe Experience Platform.

  Par exemple, vous pouvez faire en sorte que tous les nouveaux clients et clientes Silver rejoignent un parcours et leur envoyer des messages. Pour plus d&#39;informations sur l&#39;utilisation de cette activité, reportez-vous à la section [Découvrez comment configurer une activité de qualification d’audience](../building-journeys/audience-qualification-events.md).

* Utilisez la variable **Condition** dans un parcours afin de créer des conditions basées sur l’appartenance à une audience. [Découvrez comment utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-a-segment).

## Méthodes d’évaluation d’audience{#evaluation-method-in-journey-optimizer}

Dans Adobe Journey Optimizer, les audiences sont générées à partir des définitions de segment à l’aide de l’une des deux méthodes d’évaluation :

* **Segmentation par flux**: La liste des profils de l’audience est actualisée en temps réel à mesure que de nouvelles données entrent dans le système.

  La segmentation par flux est un processus continu de sélection des données qui met à jour vos audiences en réponse à l’activité des utilisateurs. Une fois qu’une définition de segment a été créée et que l’audience qui en résulte a été enregistrée, la définition de segment est appliquée aux données entrantes vers Journey Optimizer. Cela signifie que les individus sont ajoutés ou supprimés de l’audience au fur et à mesure que leurs données de profil changent, en veillant à ce que votre audience cible soit toujours pertinente.

* **Segmentation par lots**: La liste des profils de l’audience est évaluée toutes les 24 heures.

  La segmentation par lots est une alternative à la segmentation par flux qui traite toutes les données de profil à la fois par le biais de définitions de segment. Cela crée un instantané de l’audience qui peut être enregistré et exporté pour utilisation. Cependant, contrairement à la segmentation par flux, la segmentation par lots ne met pas à jour en temps réel la liste des audiences, et les nouvelles données qui arrivent après le traitement par lots ne seront pas répercutées dans l’audience avant le traitement par lots suivant.&quot;

Le système détermine la segmentation par lots et la segmentation par flux pour chaque audience en fonction de la complexité et du coût de l’évaluation de la règle de définition de segment. Vous pouvez afficher la méthode d’évaluation pour chaque audience dans la variable **[!UICONTROL Méthode d’évaluation]** de la liste des audiences.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Si la colonne **[!UICONTROL Méthode d’évaluation]** ne s’affiche pas, vous devez l’ajouter à l’aide du bouton de configuration situé en haut à droite de la liste.

Une fois que vous avez défini une audience pour la première fois, les profils sont ajoutés à l’audience lorsqu’ils remplissent les critères.

Le renvoi de l’audience à partir de données antérieures peut prendre jusqu’à 24 heures. Une fois l’audience renvoyée, elle est constamment tenue à jour et toujours prête pour le ciblage.
