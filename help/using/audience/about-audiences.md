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
source-git-commit: 3de42084d849047f218cf8dca2ad7e510759fb1c
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 55%

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

[!DNL Journey Optimizer] vous permet de créer d’utiliser des audiences Adobe Experience Platform à l’aide des données de profil client en temps réel directement à partir du menu **[!UICONTROL Audiences]** et de les utiliser dans vos parcours ou campagnes. Pour en savoir plus, consultez la [documentation du service de segmentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr){target="_blank"}.

## Utiliser des audiences dans [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Vous pouvez sélectionner dans des campagnes et des parcours toute audience Adobe Experience Platform générée à l’aide de [définitions de segment](../audience/creating-a-segment-definition.md).

>[!NOTE]
>
>Vous pouvez également cibler les audiences Adobe Experience Platform créées à l’aide de [compositions d&#39;audience](../audience/get-started-audience-orchestration.md) ou [téléchargé à partir d’un fichier CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=fr#import-audience){target="_blank"}. Ces fonctionnalités sont actuellement disponibles en version Private Beta.

Vous pouvez utiliser les audiences dans **[!DNL Journey Optimizer]** de différentes manières :

* Choisissez une audience d’une **campagne**, où le message est envoyé à toutes les personnes appartenant à l’audience sélectionnée. [Découvrez comment définir l’audience d’une campagne](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilisez une activité d’orchestration **Lecture d’audience** dans un parcours pour faire en sorte que toutes les personnes de l’audience rejoignent le parcours et reçoivent les messages inclus dans votre parcours.

  Supposons que vous ayez une audience « cliente ou cliente Silver ». Avec cette activité, vous pouvez faire en sorte que tous les clientes et clients Silver rejoignent un parcours et leur envoyer une série de messages personnalisés. [Découvrez comment configurer une activité Lecture d’audience](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Utilisez l’activité d’événement **Qualification d’audience** dans un parcours pour faire en sorte que des personnes rejoignent le parcours ou y progressent en fonction des entrées et des sorties d’audiences Adobe Experience Platform.

  Par exemple, vous pouvez faire en sorte que tous les nouveaux clientes et clients Silver rejoignent un parcours et leur envoyer des messages. Pour plus d’informations sur l’utilisation de cette activité, reportez-vous à la section [Découvrez comment configurer une activité de qualification d’audience](../building-journeys/audience-qualification-events.md).

* Utilisez l’activité **Condition** dans un parcours afin de créer des conditions basées sur l’appartenance à une audience. [Découvrez comment utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-a-segment).

## Méthodes d’évaluation d’audience{#evaluation-method-in-journey-optimizer}

Dans Adobe Journey Optimizer, les audiences sont générées à partir des définitions de segment à l’aide de l’une des trois méthodes d’évaluation ci-dessous.

+++ Segmentation en flux continu

La liste des profils de l’audience est actualisée en temps réel à mesure que de nouvelles données entrent dans le système.

La segmentation par flux est un processus continu de sélection des données qui met à jour vos audiences en réponse à l’activité des utilisateurs et utilisatrices. Une fois qu’une définition de segment a été créée et que l’audience obtenue a été enregistrée, la définition du segment s’applique aux données entrantes dans Journey Optimizer. Cela signifie que des personnes sont ajoutées ou supprimées de l’audience au fur et à mesure que leurs données de profil changent, permettant de toujours assurer la pertinence de votre audience cible. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html#query-types){target="_blank"}.

>[!NOTE]
>
>Veillez à utiliser les événements appropriés comme critères de segmentation par flux. [En savoir plus](#open-and-send-event-guardrails)

+++

+++ Segmentation par lots

La liste des profils de l’audience est évaluée toutes les 24 heures.

La segmentation par lots est une alternative à la segmentation par flux qui traite toutes les données de profil à la fois par le biais de définitions de segment. Cela crée un instantané de l’audience qui peut être enregistré et exporté pour utilisation. Cependant, contrairement à la segmentation par flux, la segmentation par lots ne met pas à jour en temps réel la liste des audiences, et les nouvelles données qui arrivent après le traitement par lots ne seront pas répercutées dans l’audience avant le traitement par lots suivant. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#batch){target="_blank"}.

+++

+++ Segmentation Edge

La segmentation Edge permet d’évaluer instantanément les segments dans Adobe Experience Platform. [sur le bord](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr){target="_blank"}, enabling same-page and next-page personalization use cases. Currently only select query types can be evaluated with edge segmentation. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html#query-types){target="_blank"}

+++

Si vous savez quelle méthode d’évaluation vous souhaitez utiliser, sélectionnez-la à l’aide de la liste déroulante. Vous pouvez également cliquer sur l’icône du dossier de l’icône Parcourir avec une loupe pour afficher la liste des méthodes d’évaluation de la définition de segment disponibles. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#segment-properties){target="_blank"}.

![](assets/evaluation-methods.png)

<!--The determination between batch segmentation and streaming segmentation is made by the system for each audience, based on the complexity and the cost of evaluating the segment definition rule. You can view the evaluation method for each audience in the **[!UICONTROL Evaluation method]** column of the audience list.
    
![](assets/evaluation-method.png)

>[!NOTE]
>
>If the **[!UICONTROL Evaluation method]** column does not display, you  need to add it using configuration button on the top right of the list.-->

Une fois que vous avez défini une audience pour la première fois, les profils sont ajoutés à l’audience lorsqu’ils remplissent les critères.

Le renvoi de l’audience à partir de données antérieures peut prendre jusqu’à 24 heures. Une fois l’audience renvoyée, elle est constamment tenue à jour et toujours prête pour le ciblage.

### Utilisation des événements avec la segmentation par flux {#open-and-send-event-guardrails}

La segmentation par flux est utile pour la personnalisation en temps réel avec des cas d’utilisation à forte valeur ajoutée. Cependant, il est important de choisir la [events](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=fr#events){target="_blank"} à utiliser comme critères de segmentation.

Par conséquent, pour optimiser les performances de la segmentation par flux, évitez d’utiliser les événements suivants :

* **Message ouvert** Événement Type d’interaction

  Lors de la création de votre audience, l’utilisation de **Message ouvert** les événements d’interaction sont devenus peu fiables, car ils ne sont pas des indicateurs réels de l’activité de l’utilisateur et peuvent avoir un impact négatif sur les performances de segmentation. Découvrez pourquoi dans cette section [Publication de blog d’Adobe](https://blog.adobe.com/en/publish/2021/06/24/what-apples-mail-privacy-protection-means-for-email-marketers){target="_blank"}.

  Par conséquent, Adobe recommande de ne pas utiliser **Message ouvert** événements d’interaction avec la segmentation par flux. Utilisez plutôt des signaux d’activité utilisateur réels tels que des clics, des achats ou des données de balise.

* **Message envoyé** Événement d’état de retour

  La variable **Message envoyé** l’événement feedback est souvent utilisé pour la vérification de la fréquence ou de la suppression avant l’envoi d’un email. Adobe recommande de l’éviter si possible, car la capacité globale actuelle du nombre d’événements pouvant être diffusés par seconde prend de l’espace.

  Par conséquent, pour la logique de fréquence ou de suppression, utilisez des règles de fonctionnement plutôt que **Message envoyé** événements de retour . Notez que des limites de fréquence quotidiennes pour les profils individuels seront bientôt disponibles, en complément de la cadence mensuelle existante pour les règles de fonctionnement.

>[!NOTE]
>
>Vous pouvez utiliser **Message ouvert** et **Message envoyé** dans la segmentation par lots sans souci de performances.
