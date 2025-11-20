---
solution: Journey Optimizer
product: journey optimizer
title: Événements de qualification d’audience
description: Découvrez comment utiliser et configurer des événements de qualification d’audience.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: qualification, événements, audience, parcours, platform
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
version: Journey Orchestration
source-git-commit: b8fb0c0fd9e9e119428b430563cbb35d1961516e
workflow-type: tm+mt
source-wordcount: '1344'
ht-degree: 88%

---

# Événements de qualification d’audience {#segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Événements de qualification d’audience"
>abstract="Cette activité permet à votre parcours d’écouter les entrées et les sorties des profils dans les audiences Adobe Experience Platform pour que les personnes puissent rejoindre le parcours ou y progresser."

## À propos des événements de qualification d’audience{#about-segment-qualification}

Cette activité permet à votre parcours d’écouter les entrées et les sorties des profils dans les audiences Adobe Experience Platform pour que les personnes puissent rejoindre le parcours ou y progresser. Pour plus d’informations sur la création d’audiences, consultez cette [section](../audience/about-audiences.md).

Supposons que vous ayez une audience « cliente ou cliente Silver ». Avec cette activité, vous pouvez faire entrer tous les nouveaux clients Silver dans un parcours et leur envoyer une série de messages personnalisés.

Il est possible de positionner ce type d’événement dès la première étape, ou plus tard dans le parcours.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)


>[!CAUTION]
>
>Avant de commencer à configurer une qualification d’audience, [lisez la section relative aux mécanismes de sécurisation et aux limitations](#audience-qualification-guardrails).


## Configurer l’activité {#configure-segment-qualification}

Pour configurer l’activité **[!UICONTROL Qualification d’audience]**, procédez comme suit :

1. Développez la catégorie **[!UICONTROL Événements]** et déposez une activité de **[!UICONTROL qualification d’audience]** dans la zone de travail.

   ![Événement de qualification d’audience dans la palette de parcours &#x200B;](assets/segment5.png)

1. Ajoutez un **[!UICONTROL libellé]** à l’activité. Cette étape est facultative.

1. Cliquez dans le champ **[!UICONTROL Audience]** et sélectionnez les audiences à exploiter.

   >[!NOTE]
   >
   >Vous pouvez personnaliser les colonnes affichées dans la liste et les trier.

   ![Liste déroulante de sélection de l’audience pour la configuration de l’événement de qualification](assets/segment6.png)

   Une fois l’audience ajoutée, le bouton **[!UICONTROL Copier]** permet de copier son nom et son ID :

   `{"name":"Loyalty membership","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![Bouton Copier pour copier le nom et l’identifiant de l’audience au format JSON](assets/segment-copy.png)

1. Dans le champ **[!UICONTROL Comportement]**, choisissez d’écouter les entrées de l’audience, les sorties ou les deux.

   >[!NOTE]
   >
   >**[!UICONTROL Rejoindre]** et **[!UICONTROL Quitter]** correspondent aux statuts de participation d’audience **Réalisé** et **Sorti** d’Adobe Experience Platform. Pour plus d’informations sur l’évaluation d’une audience, consultez la [documentation du service de segmentation](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=fr#interpret-segment-results){target="_blank"}.

1. Sélectionnez un espace de noms. Cela n’est nécessaire que si l’événement est considéré comme la première étape du parcours. Par défaut, le champ est prérempli avec le dernier espace de noms utilisé.

   >[!NOTE]
   >
   >Vous pouvez uniquement sélectionner un espace de noms d’identité basé sur les personnes. Si vous avez défini un espace de noms pour une table de correspondance (par exemple : espace de noms ProductID pour une recherche de produit), il ne sera pas disponible dans la liste déroulante **Espace de noms**.

   ![Sélection d’un espace de noms pour l’identité de qualification d’audience](assets/segment7.png)

La payload contient les informations contextuelles suivantes, utilisables dans des conditions et des actions :

* le comportement (entrée, sortie)
* l’horodatage de la qualification
* l’ID de l’audience

Lorsque vous utilisez l’éditeur d’expression dans une condition ou une action qui suit une activité de **[!UICONTROL qualification d’audience]**, vous avez accès au nœud **[!UICONTROL AudienceQualification]**. Vous pouvez choisir entre **[!UICONTROL l’heure de la dernière qualification]** et le **[!UICONTROL statut]** (entrée ou sortie).

Voir [Activité de condition](../building-journeys/condition-activity.md#about_condition).

Un nouveau parcours contenant un événement de **qualification d’audience** est opérationnel dix minutes après sa publication. Cet intervalle de temps correspond à l&#39;intervalle d&#39;actualisation du cache du service dédié. Par conséquent, vous devez attendre dix minutes avant d&#39;utiliser ce parcours.

## Bonnes pratiques {#best-practices-segments}

L’activité **[!UICONTROL Qualification d’audience]** permet une entrée immédiate dans les parcours des personnes qualifiées ou disqualifiées d’une audience Adobe Experience Platform.

La vitesse de réception de ces informations est élevée. Les mesures effectuées montrent une vitesse de 10 000 événements reçus par seconde. Par conséquent, assurez-vous de comprendre comment les pics d’entrée peuvent se produire, comment les éviter et comment y préparer votre parcours. Pour en savoir plus sur les taux de traitement de parcours et les limites de débit, consultez [cette section](entry-management.md#journey-processing-rate).

### Audiences par lots {#batch-speed-segment-qualification}

Lorsque vous utilisez la qualification d’audience pour une audience par lot, notez qu’un pic d’entrée se produit au moment du calcul quotidien. La taille du pic dépend du nombre de personnes qui rejoignent (ou quittent) l’audience quotidiennement.

De plus, si l’audience par lot est créée et utilisée immédiatement dans un parcours, le premier lot de calculs peut faire qu’un très grand nombre de personnes rejoignent le parcours.

### Audiences en flux continu {#streamed-speed-segment-qualification}

Lorsque vous utilisez la qualification d’audience pour les audiences en flux continu, il y a moins de risque d’obtenir d’importants pics d’entrées et de sorties en raison de l’évaluation continue de l’audience. Cependant, si la définition de l’audience mène à un grand volume de personnes se qualifiant simultanément, un pic peut toujours se produire.

Évitez d’utiliser des événements d’ouverture et d’envoi avec la segmentation par streaming. Utilisez plutôt les signaux d’activité des utilisateurs et utilisatrices, tels que les clics, les achats ou les données de balise. Pour la logique de fréquence ou de suppression, utilisez des règles métier plutôt que des événements d&#39;envoi. [En savoir plus](../audience/about-audiences.md)

Pour plus d’informations sur la segmentation par streaming, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/methods/streaming-segmentation){target="_blank"}.

>[!NOTE]
>
>Pour la segmentation en flux continu, les données nouvellement ingérées peuvent prendre jusqu’à **2 heures** pour se propager entièrement dans Adobe Experience Platform pour une utilisation en temps réel. Les audiences qui reposent sur des conditions basées sur un jour ou sur l’heure (par exemple, « événements survenus aujourd’hui ») peuvent présenter une complexité supplémentaire dans le minutage de la qualification. Si votre parcours dépend de la qualification immédiate de l’audience, pensez à ajouter une courte [activité d’attente](wait-activity.md) au début ou à laisser un temps de mémoire tampon pour garantir une qualification précise.

### Éviter les surcharges {#overloads-speed-segment-qualification}

Voici quelques bonnes pratiques qui permettront d’éviter de surcharger les systèmes utilisés dans les parcours (sources de données, actions personnalisées, activités d’action de canal) :

* N’utilisez pas une audience par lots immédiatement après sa création dans une activité **[!UICONTROL Qualification d’audience]**. Cela permet d’éviter le premier pic de calcul. Un avertissement jaune apparaît dans la zone de travail du parcours si vous êtes sur le point d’utiliser une audience qui n’a jamais été calculée.

  ![Message d’erreur indiquant que l’audience est introuvable dans Adobe Experience Platform](assets/segment-error.png)

* Mettez en place une règle de capping pour les sources de données et les actions utilisées dans les parcours pour éviter de les surcharger. Pour en savoir plus, consultez la [documentation de Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html?lang=fr){target="_blank"}. Notez que la règle de capping ne permet pas de nouvelle tentative. Si vous avez besoin d’effectuer une nouvelle tentative, utilisez un autre chemin dans le parcours en cochant la case **[!UICONTROL Ajouter un itinéraire alternatif en cas de dépassement de délai ou d’erreur]** dans les conditions ou les actions.

* Avant d’utiliser l’audience dans un parcours en production, évaluez quotidiennement le nombre de personnes qualifiées pour cette audience. Pour ce faire, accédez au menu **[!UICONTROL Audiences]**, ouvrez l’audience, puis consultez le graphique **[!UICONTROL Profils dans le temps]**.

  ![Message d’avertissement lorsque l’audience comporte trop d’événements pour le traitement en temps réel](assets/segment-overload.png)

En savoir plus sur les limites de débit d’entrée dans [cette section](entry-management.md#profile-entrance-rate).

## Mécanismes de sécurisation et limitations {#audience-qualification-guardrails}

Utilisez les mécanismes de sécurisation et suivez les recommandations ci-dessous pour créer des parcours de qualification d’audience. Consultez également les [Bonnes pratiques en matière de qualification d’audience](#best-practices-segments).


* Les parcours de qualification d’audience sont principalement conçus pour fonctionner avec les audiences en streaming. Cette combinaison garantit une meilleure expérience en temps réel. Il est vivement recommandé d’utiliser des **audiences en streaming** dans l’activité Qualification d’audience.

  Cependant, si vous souhaitez utiliser des attributs basés sur l’ingestion par lots dans votre audience en streaming ou une audience par lots dans un parcours de qualification d’audience, tenez compte de la période d’évaluation/d’activation de l’audience. Une audience par lots ou une audience en streaming utilisant des attributs ingérés par lots est prête à être utilisée dans l’activité **Qualification d’audience** environ **2 heures** après la fin de votre traitement de segmentation. Ce traitement s’exécute une fois par jour, à l’heure définie par l’administrateur ou l’administratrice de votre organisation Adobe.

* Les audiences Adobe Experience Platform sont calculées une fois par jour (audiences **par lots**) ou en temps réel (audiences **en streaming** à l’aide de l’option Audiences haute fréquence d’Adobe Experience Platform).

   * Si l’audience sélectionnée est en streaming, les personnes appartenant à cette audience peuvent éventuellement rejoindre le parcours en temps réel.
   * Si l’audience est par lots, les personnes qui viennent d’être qualifiées pour cette audience peuvent éventuellement rejoindre le parcours lorsque le calcul de l’audience est exécuté sur Adobe Experience Platform.

  Afin d’appliquer les bonnes pratiques, utilisez uniquement des audiences en streaming dans une activité **Qualification d’audience**. Pour les cas d’utilisation par lots, utilisez une activité **[Lecture d’audience](read-audience.md)**.

  >[!NOTE]
  >
  >En raison de la nature par lots des audiences créées à l’aide de workflows de composition et de chargements personnalisés, ces audiences ne peuvent pas être ciblées dans une activité « Qualification d’audience ». Seules les audiences créées à l’aide de définitions de segment peuvent être utilisées dans cette activité.


* Vous ne pouvez pas utiliser les groupes de champs d’événement d’expérience dans les parcours qui commencent par une activité **Lecture d’audience**, **Qualification d’audience** ou **Événement métier**.

* Lorsque vous utilisez une activité de **qualification d’audience** dans un parcours, cette activité peut prendre jusqu’à 10 minutes avant d’être active et d’écouter les profils entrant ou sortant de l’audience.


>[!CAUTION]
>
>[Les mécanismes de sécurisation pour les données et la segmentation du profil client en temps réel](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=fr){target="_blank"} s’appliquent également à Adobe Journey Optimizer.



## Vidéo pratique {#video}

Découvrez des cas d’utilisation des parcours de qualification d’audience dans cette vidéo. Découvrez comment créer un parcours avec qualification d’audience et les bonnes pratiques à appliquer.

>[!VIDEO](https://video.tv.adobe.com/v/3446206?captions=fre_fr&quality=12)
