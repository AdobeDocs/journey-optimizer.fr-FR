---
solution: Journey Optimizer
product: journey optimizer
title: Événements de qualification d’audience
description: En savoir plus sur les événements de qualification d’audience
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: qualification, événements, audience, parcours, platform
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: e45ec5f0e1bbcc73892f9cde5923627886f44ef6
workflow-type: tm+mt
source-wordcount: '1081'
ht-degree: 100%

---

# Événements de qualification d’audience {#segment-qualification}

## À propos des événements de qualification d’audience{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Événements de qualification d’audience"
>abstract="Cette activité permet à votre parcours d’écouter les entrées et les sorties des profils dans les audiences Adobe Experience Platform pour que les personnes puissent rejoindre le parcours ou y progresser."

Cette activité permet à votre parcours d’écouter les entrées et les sorties des profils dans les audiences Adobe Experience Platform pour que les personnes puissent rejoindre le parcours ou y progresser. Pour plus d’informations sur la création d’audiences, consultez cette [section](../audience/about-audiences.md).

Supposons que vous ayez une audience « cliente ou cliente Silver ». Avec cette activité, vous pouvez faire entrer tous les nouveaux clients Silver dans un parcours et leur envoyer une série de messages personnalisés.

Il est possible de positionner ce type d’événement dès la première étape, ou plus tard dans le parcours.

➡️ [Découvrir cette fonctionnalité en vidéo](#video)

### Remarques importantes{#important-notes-segment-qualification}

* N’oubliez pas que les audiences Adobe Experience Platform sont calculées une fois par jour (audiences **par lots**) ou en temps réel (audiences **en flux continu** à l’aide de l’option Audiences haute fréquence d’Adobe Experience Platform).

   * Si l’audience sélectionnée est en flux continu, les personnes appartenant à cette audience peuvent éventuellement rejoindre le parcours en temps réel.
   * Si l’audience est par lots, les personnes qui viennent d’être qualifiées pour cette audience peuvent éventuellement rejoindre le parcours lorsque le calcul de l’audience est exécuté sur Adobe Experience Platform.

  En guise de bonne pratique, nous recommandons donc de n’utiliser que des audiences en streaming dans une activité **Qualification de l’audience**. Pour les cas d’utilisation par lots, utilisez une activité **[Lecture d’audience](read-audience.md)**.

  >[!NOTE]
  >
  >En raison de la nature par lots des audiences créées à l’aide de workflows de composition et du chargement personnalisé, vous ne pouvez pas cibler ces audiences dans une activité « Qualification de l’audience ». Seules les audiences créées à l’aide de définitions de segment peuvent être utilisées dans cette activité.

* Les groupes de champs d’événement d’expérience ne peuvent pas être utilisés dans les parcours commençant par une activité Lecture d’audience, Qualification d’audience ou événement métier.

* Lorsque vous utilisez une qualification d’audience dans un parcours, cette activité de qualification d’audience peut demander jusqu’à 10 minutes avant d’être active et d’écouter les profils entrant ou sortant de l’audience.

### Configurer l’activité{#cnfigure-segment-qualification}

1. Développez la catégorie **[!UICONTROL Événements]** et déposez une activité de **[!UICONTROL qualification d’audience]** dans la zone de travail.

   ![](assets/segment5.png)

1. Ajoutez un **[!UICONTROL libellé]** à l’activité. Cette étape est facultative.

1. Cliquez dans le champ **[!UICONTROL Audience]** et sélectionnez les audiences à exploiter.

   >[!NOTE]
   >
   >Notez que vous pouvez personnaliser les colonnes affichées dans la liste et les trier.

   ![](assets/segment6.png)

   Une fois l’audience ajoutée, le bouton **[!UICONTROL Copier]** permet de copier son nom et son ID :

   `{"name":"Loyalty membership","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. Dans le champ **[!UICONTROL Comportement]**, choisissez d’écouter les entrées de l’audience, les sorties ou les deux.

   >[!NOTE]
   >
   >Notez que **[!UICONTROL Rejoindre]** et **[!UICONTROL Quitter]** correspondent aux statuts de participation d’audience **Réalisé** et **Sorti** d’Adobe Experience Platform. Pour plus d’informations sur l’évaluation d’une audience, consultez la [documentation du service de segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=fr#interpret-segment-results){target="_blank"}.

1. Sélectionnez un espace de noms. Cela n’est nécessaire que si l’événement est considéré comme la première étape du parcours. Par défaut, le champ est prérempli avec le dernier espace de noms utilisé.

   >[!NOTE]
   >
   >Vous pouvez uniquement sélectionner un espace de noms d’identité basé sur les personnes. Si vous avez défini un espace de noms pour une table de correspondance (par exemple : espace de noms ProductID pour une recherche de produit), il ne sera pas disponible dans la liste déroulante **Espace de noms**.

   ![](assets/segment7.png)

La payload contient les informations contextuelles suivantes, utilisables dans des conditions et des actions :

* le comportement (entrée, sortie)
* l’horodatage de la qualification
* l’ID de l’audience

Lorsque vous utilisez l’éditeur d’expression dans une condition ou une action qui suit une activité de **[!UICONTROL qualification d’audience]**, vous avez accès au nœud **[!UICONTROL AudienceQualification]**. Vous pouvez choisir entre **[!UICONTROL l’heure de la dernière qualification]** et le **[!UICONTROL statut]** (entrée ou sortie).

Voir [Activité de condition](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Un nouveau parcours contenant un événement de qualification d’audience est opérationnel dix minutes après sa publication. Cet intervalle de temps correspond à l&#39;intervalle d&#39;actualisation du cache du service dédié. Par conséquent, vous devez attendre dix minutes avant d&#39;utiliser ce parcours.

## Bonnes pratiques {#best-practices-segments}

L’activité **[!UICONTROL Qualification d’audience]** permet une entrée immédiate dans les parcours des personnes qualifiées ou disqualifiées d’une audience Adobe Experience Platform.

La vitesse de réception de ces informations est élevée. Les mesures effectuées montrent une vitesse de 10 000 événements reçus par seconde. Par conséquent, vous devez veiller à comprendre comment les pics d’entrée peuvent se produire, comment les éviter et comment y préparer votre parcours.

### Audiences par lots{#batch-speed-segment-qualification}

Lorsque vous utilisez la qualification d’audience pour une audience par lots, notez qu’un pic d’entrée se produit au moment du calcul quotidien. La taille du pic dépend du nombre de personnes qui rejoignent (ou quittent) l’audience quotidiennement.

De plus, si l’audience par lots est créée et utilisée immédiatement dans un parcours, le premier lot de calculs peut faire qu’un très grand nombre de personnes rejoignent le parcours.

### Audiences en flux continu{#streamed-speed-segment-qualification}

Lors de l’utilisation de la qualification d’audience pour les audiences en flux continu, il y a moins de risque d’obtenir d’importants pics d’entrées/sorties en raison de l’évaluation continue de l’audience. Néanmoins, si la définition de l’audience conduit à qualifier un grand nombre de clientes et clients en même temps, un pic peut également se produire.

Évitez d’utiliser des événements d’ouverture et d’envoi avec la segmentation par streaming. Utilisez plutôt les signaux d’activité des utilisateurs et utilisatrices, tels que les clics, les achats ou les données de balise. Pour la logique de fréquence ou de suppression, utilisez des règles métier plutôt que des événements d&#39;envoi. [En savoir plus](../audience/about-audiences.md#open-and-send-event-guardrails)

Pour plus d’informations sur la segmentation par streaming, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html?lang=fr#api).

### Éviter les surcharges{#overloads-speed-segment-qualification}

Voici quelques bonnes pratiques qui permettront d’éviter de surcharger les systèmes utilisés dans les parcours (sources de données, actions personnalisées, activités d’action de canal).

Dans une activité **[!UICONTROL Qualification d’audience]**, n’utilisez pas une audience par lots immédiatement après sa création. Cela permettra d’éviter le premier pic de calcul. Notez qu’un avertissement jaune apparaît dans la zone de travail du parcours si vous êtes sur le point d’utiliser une audience qui n’a jamais été calculée.

![](assets/segment-error.png)

Mettez en place une règle de limitation pour les sources de données et les actions utilisées dans les parcours pour éviter de les surcharger. Pour en savoir plus, consultez la [documentation de Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html?lang=fr){target="_blank"}. Notez que la règle de limitation ne permet pas de nouvelle tentative. Si vous avez besoin d’effectuer une nouvelle tentative, vous devez utiliser un autre chemin dans le parcours en cochant la case **[!UICONTROL Ajouter un itinéraire alternatif en cas de temporisation ou d’erreur]** dans les conditions ou les actions.

Avant d’utiliser l’audience dans un parcours en production, évaluez d’abord toujours le nombre de personnes qualifiées pour cette audience tous les jours. Pour ce faire, vous pouvez vérifier le menu **[!UICONTROL Audiences]**, ouvrir l’audience, puis consulter le graphe **[!UICONTROL Profils sur toute la durée]**.

![](assets/segment-overload.png)

## Vidéo pratique {#video}

Comprenez les cas d’utilisation applicables pour les parcours de qualification d’audience. Découvrez comment créer un parcours avec qualification d’audience et les bonnes pratiques à appliquer.

>[!VIDEO](https://video.tv.adobe.com/v/3425028?quality=12)
