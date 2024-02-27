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
source-git-commit: 2edff0123084fa1736fb8198c3b4e8ff4e40341d
workflow-type: tm+mt
source-wordcount: '1083'
ht-degree: 85%

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

Une audience est un ensemble de personnes qui partagent des comportements et/ou des caractéristiques similaires. Pour en savoir plus sur les audiences, consultez la [documentation du service de segmentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr){target="_blank"}.

[!DNL Journey Optimizer] vous permet de créer des audiences Adobe Experience Platform directement à partir du menu **[!UICONTROL Audiences]** et de les utiliser dans vos parcours ou campagnes.

Les audiences peuvent être générées à l’aide de différentes méthodes :

* **Définitions de segment** : créez une définition d’audience à l’aide du Service de segmentation d’Adobe Experience Platform. [Découvrir comment créer des définitions de segment](creating-a-segment-definition.md)
* **Import de fichiers CSV** : importez une audience à l’aide d’un fichier CSV. Découvrez comment importer des audiences dans la [documentation du service de segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=fr#import-audience){target="_blank"} d’Adobe Experience Platform.
* **Composition de l’audience** : créez un workflow de composition afin de combiner les audiences d’Adobe Experience Platform existantes dans une zone de travail visuelle et d’exploiter diverses activités (telles que le partage, l’exclusion, etc.) pour créer de nouvelles audiences. [Prise en main de la composition de l’audience](get-started-audience-orchestration.md)

## Cibler des audiences dans [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Vous pouvez sélectionner dans des campagnes et des parcours toute audience générée à l’aide de définitions de segment, de workflows d’import de fichier CSV ou de composition.

>[!AVAILABILITY]
>
>L’utilisation d’audiences et d’attributs provenant de la composition de l’audience et des audiences de téléchargement personnalisées (fichier CSV) n’est actuellement pas disponible avec Healthcare Shield ou Privacy and Security Shield. [Découvrez comment utiliser les attributs d’enrichissement d’audience dans Journey Optimizer](../audience/about-audiences.md#enrichment)

Vous pouvez utiliser les audiences dans **[!DNL Journey Optimizer]** de différentes manières :

* Choisissez une audience d’une **campagne**, où le message est envoyé à toutes les personnes appartenant à l’audience sélectionnée. [Découvrez comment définir l’audience d’une campagne](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilisez une activité d’orchestration **Lecture d’audience** dans un parcours pour faire en sorte que toutes les personnes de l’audience rejoignent le parcours et reçoivent les messages inclus dans votre parcours.

  Supposons que vous ayez une audience « cliente ou cliente Silver ». Avec cette activité, vous pouvez faire en sorte que tous les clientes et clients Silver rejoignent un parcours et leur envoyer une série de messages personnalisés. [Découvrez comment configurer une activité Lecture d’audience](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Utilisez l’activité d’événement **Qualification d’audience** dans un parcours pour faire en sorte que des personnes rejoignent le parcours ou y progressent en fonction des entrées et des sorties d’audiences Adobe Experience Platform.

  Par exemple, vous pouvez faire en sorte que tous les nouveaux clientes et clients Silver rejoignent un parcours et leur envoyer des messages. Pour plus d’informations sur l’utilisation de cette activité, reportez-vous à la section [Découvrez comment configurer une activité de qualification d’audience](../building-journeys/audience-qualification-events.md).

* Utilisez l’activité **Condition** dans un parcours afin de créer des conditions basées sur l’appartenance à une audience. [Découvrez comment utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-a-segment).

## Utilisation des attributs d’enrichissement d’audience dans Journey Optimizer {#enrichment}

Lors du ciblage d’une audience générée à l’aide de workflows de composition, vous pouvez exploiter les attributs d’enrichissement de ces audiences pour créer votre parcours et personnaliser vos messages.

* Créez plusieurs chemins dans un parcours en fonction de règles qui exploitent les attributs d’enrichissement de l’audience ciblée. Pour ce faire, ciblez l’audience à l’aide d’une [Lecture d’audience](../building-journeys/read-audience.md) puis créer des règles dans une [Condition](../building-journeys/condition-activity.md) activité basée sur les attributs d’enrichissement de l’audience.

  ![](assets/audience-enrichment-attribute-condition.png){zoomable=&quot;yes&quot;}

* Personnalisez vos messages dans des parcours ou des campagnes en ajoutant les attributs d&#39;enrichissement de l&#39;audience ciblée dans l&#39;éditeur d&#39;expression. [Découvrez comment utiliser l’éditeur d’expression](../personalization/personalization-build-expressions.md)

  ![](assets/audience-enrichment-attribute-perso.png){zoomable=&quot;yes&quot;}

## Méthodes d’évaluation d’audience {#evaluation-method-in-journey-optimizer}

Dans Adobe Journey Optimizer, les audiences sont générées à partir des définitions de segment à l’aide de l’une des trois méthodes d’évaluation ci-dessous :

+++ Segmentation par streaming

La liste des profils de l’audience est actualisée en temps réel pendant que de nouvelles données affluent dans le système.

La segmentation par flux est un processus continu de sélection des données qui met à jour vos audiences en réponse à l’activité des utilisateurs et utilisatrices. Une fois qu’une définition de segment a été créée et que l’audience obtenue a été enregistrée, la définition du segment s’applique aux données entrantes dans Journey Optimizer. Cela signifie que des personnes sont ajoutées ou supprimées de l’audience au fur et à mesure que leurs données de profil changent, permettant de toujours assurer la pertinence de votre audience cible. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html?lang=fr){target="_blank"}.

>[!NOTE]
>
>Veillez à utiliser les événements appropriés comme critères de segmentation par streaming. [En savoir plus](#streaming-segmentation-events-guardrails)

+++

+++ Segmentation par lots

L’évaluation de la liste des profils de l’audience se fait toutes les 24 heures.

La segmentation par lots est une alternative à la segmentation par flux qui traite toutes les données de profil à la fois par le biais de définitions de segment. Cela crée un instantané de l’audience qui peut être enregistré et exporté pour utilisation. Cependant, contrairement à la segmentation par streaming, la segmentation par lots ne met pas à jour la liste des audiences en temps réel, et les nouvelles données qui entrent après le traitement par lots ne seront pas répercutées dans l’audience avant le traitement par lots suivant. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr#batch){target="_blank"}.

+++

+++ Segmentation Edge

La segmentation Edge permet d’évaluer instantanément les segments dans Adobe Experience Platform [sur le serveur Edge](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr){target="_blank"}, enabling same-page and next-page personalization use cases. Currently only select query types can be evaluated with edge segmentation. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html?lang=fr#query-types){target="_blank"}.

+++

Si vous savez quelle méthode d’évaluation utiliser, sélectionnez-la à l’aide de la liste déroulante. Vous pouvez également cliquer sur l’icône Parcourir du dossier (loupe) pour afficher la liste des méthodes d’évaluation de la définition de segment disponibles. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=fr#segment-properties){target="_blank"}.

![](assets/evaluation-methods.png)

<!--The determination between batch segmentation and streaming segmentation is made by the system for each audience, based on the complexity and the cost of evaluating the segment definition rule. You can view the evaluation method for each audience in the **[!UICONTROL Evaluation method]** column of the audience list.
    
![](assets/evaluation-method.png)

>[!NOTE]
>
>If the **[!UICONTROL Evaluation method]** column does not display, you  need to add it using configuration button on the top right of the list.-->

Une fois que vous avez défini une audience pour la première fois, les profils sont ajoutés à l’audience lorsqu’ils remplissent les critères.

Le renvoi de l’audience à partir de données antérieures peut prendre jusqu’à 24 heures. Une fois l’audience renvoyée, elle est constamment tenue à jour et toujours prête pour le ciblage.

### Utilisation des événements avec la segmentation par streaming {#streaming-segmentation-events-guardrails}

La segmentation par streaming est utile pour la personnalisation en temps réel avec des cas d’utilisation à forte valeur ajoutée. Cependant, il est important de choisir les bons [événements](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=fr#events){target="_blank"} à utiliser comme critères de segmentation.

Par conséquent, pour obtenir des performances optimales en matière de segmentation par streaming, évitez d’utiliser les événements suivants :

* Événement Type d’interaction **Message ouvert**

  Lors de la création d’une audience, l’utilisation d’événements d’interaction **Message ouvert** est peu fiable, car ces derniers ne sont pas des indicateurs réels de l’activité des personnes et peuvent avoir un impact négatif sur les performances de segmentation. Découvrez pourquoi dans cet [article de blog](https://blog.adobe.com/en/publish/2021/06/24/what-apples-mail-privacy-protection-means-for-email-marketers){target="_blank"}.

  Par conséquent, Adobe recommande de ne pas utiliser les événements d’interaction **Message ouvert** avec la segmentation par streaming. Utilisez plutôt les signaux d’activité des utilisateurs et utilisatrices, tels que les clics, les achats ou les données de balise.

* Événement Statut des commentaires **Message envoyé**

  L’événement de commentaire **Message envoyé** est souvent utilisé pour la vérification de la fréquence ou de la suppression avant l’envoi d’un e-mail. Adobe recommande de l’éviter du fait de la pression engendrée sur les performances et la dégradation du système qui peut s’en suivre.

  Par conséquent, pour la logique de fréquence ou de suppression, utilisez des règles métier plutôt que les événements de commentaire **Message envoyé**. Notez que des limites de fréquence quotidiennes pour les profils individuels seront bientôt disponibles, en complément de la cadence mensuelle existante des règles métier.

>[!NOTE]
>
>Vous pouvez utiliser les événements **Message ouvert** et **Message envoyé** dans la segmentation par lots sans souci de performances.
