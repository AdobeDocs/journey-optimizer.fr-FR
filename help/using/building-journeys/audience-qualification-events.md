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
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '1487'
ht-degree: 73%

---

# Événements de qualification d’audience {#segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Événements de qualification d’audience"
>abstract="Cette activité écoute les entrées et les sorties des profils dans les audiences [!DNL Adobe Experience Platform] pour déplacer les individus à travers un parcours."

## À propos des événements de qualification d’audience{#about-segment-qualification}

Cette activité écoute les entrées et les sorties des profils dans les audiences [!DNL Adobe Experience Platform]. Il peut faire entrer des individus dans un parcours ou aller de l&#39;avant. Pour plus d’informations sur la création d’audiences, consultez cette [section](../audience/about-audiences.md).

Supposons que vous ayez une audience « client ou cliente Silver ». Avec cette activité, vous pouvez faire entrer tous les nouveaux clients Silver dans un parcours et leur envoyer une série de messages personnalisés.

Il est possible de positionner ce type d’événement dès la première étape, ou plus tard dans le parcours.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)


>[!CAUTION]
>
>Avant de commencer à configurer une qualification d’audience, [lisez la section relative aux mécanismes de sécurisation et aux limitations](#audience-qualification-guardrails).


## Configurer l’activité {#configure-segment-qualification}

Pour configurer l’activité **[!UICONTROL Qualification d’audience]**, procédez comme suit :

1. Développez la catégorie **[!UICONTROL Événements]** et déposez une activité de **[!UICONTROL qualification d’audience]** dans la zone de travail.

   ![Événement de qualification d’audience dans la palette de parcours](assets/segment5.png)

1. Ajoutez un **[!UICONTROL libellé]** à l’activité. Cette étape est facultative.

1. Cliquez dans le champ **[!UICONTROL Audience]** et sélectionnez les audiences à exploiter.

   >[!NOTE]
   >
   >Vous pouvez personnaliser les colonnes affichées dans la liste et les trier.

   ![Liste déroulante de sélection de l’audience pour la configuration de l’événement de qualification](assets/segment6.png)

   Une fois l’audience ajoutée, le bouton **[!UICONTROL Copier]** permet de copier son nom et son ID :

   `{"name":"Loyalty membership","id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![Bouton Copier pour copier le nom et l’ID de l’audience au format JSON](assets/segment-copy.png)

1. Dans le champ **[!UICONTROL Comportement]**, choisissez d’écouter les entrées de l’audience, les sorties ou les deux.

   >[!NOTE]
   >
   >**[!UICONTROL Entrée]** et **[!UICONTROL Sortie]** correspondent aux statuts de participation d’audience **Réalisé** et **Sorti** de [!DNL Adobe Experience Platform].
   >Voir la [documentation de Segmentation Service](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=fr#interpret-segment-results){target="_blank"}.

1. Sélectionnez un espace de noms. Cela n’est nécessaire que si l’événement est considéré comme la première étape du parcours. Par défaut, le champ est prérempli avec le dernier espace de noms utilisé.

   >[!NOTE]
   >
   >Vous pouvez uniquement sélectionner un espace de noms d’identité basé sur les personnes.
   >Les espaces de noms de table de recherche (par exemple, ProductID pour une recherche de produit) ne sont pas disponibles dans la liste déroulante **Espace de noms**.

   ![Sélection d’un espace de noms pour l’identité de qualification d’audience](assets/segment7.png)

La payload contient les informations contextuelles suivantes, utilisables dans des conditions et des actions :

* le comportement (entrée, sortie)
* l’horodatage de la qualification
* l’ID de l’audience

Lorsque vous utilisez l’éditeur d’expression dans une condition ou une action qui suit une activité de **[!UICONTROL qualification d’audience]**, vous avez accès au nœud **[!UICONTROL AudienceQualification]**. Vous pouvez choisir entre **[!UICONTROL l’heure de la dernière qualification]** et le **[!UICONTROL statut]** (entrée ou sortie).

Voir [Activité de condition](../building-journeys/condition-activity.md#about_condition).

Un nouveau parcours contenant un événement de **qualification d’audience** est opérationnel dix minutes après sa publication. Cet intervalle correspond à l’intervalle d’actualisation du cache du service dédié. Patientez dix minutes avant d’utiliser ce parcours.

## Bonnes pratiques {#best-practices-segments}

L’activité **[!UICONTROL Qualification de l’audience]** permet une entrée immédiate sur les parcours pour les personnes qui remplissent les critères pour une audience [!DNL Adobe Experience Platform] ou qui ne les remplissent pas.

La vitesse de réception de ces informations est élevée. Les mesures indiquent 10 000 événements reçus par seconde. Prévoyez les pics d’entrée, évitez-les lorsque cela est possible, puis préparez votre parcours à les gérer. Pour en savoir plus sur les taux de traitement de parcours et les limites de débit, consultez [cette section](entry-management.md#journey-processing-rate).

### Audiences par lots {#batch-speed-segment-qualification}

Lorsque vous utilisez la qualification d’audience pour une audience par lot, notez qu’un pic d’entrée se produit au moment du calcul quotidien. La taille du pic dépend du nombre d’individus qui rejoignent ou quittent l’audience chaque jour.

De plus, si l’audience par lot est nouvellement créée et utilisée immédiatement dans un parcours, le premier lot de calculs peut générer de nombreuses entrées. Prévoyez ce pic.

### Audiences en flux continu {#streamed-speed-segment-qualification}

Lors de l’utilisation de la qualification de l’audience pour les audiences en flux continu, il y a moins de risque de pics d’entrée et de sortie importants car l’évaluation est continue. Si la définition d’audience qualifie plusieurs clients à la fois, un pic peut toujours se produire.

Évitez d’utiliser des événements d’ouverture et d’envoi avec la segmentation par streaming. Utilisez plutôt les signaux d’activité des utilisateurs et utilisatrices, tels que les clics, les achats ou les données de balise. Pour la logique de fréquence ou de suppression, utilisez des règles métier au lieu d’envoyer des événements. [En savoir plus](../audience/about-audiences.md)

Voir la [[!DNL Adobe Experience Platform] documentation sur la segmentation en flux continu](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/methods/streaming-segmentation){target="_blank"}.

>[!NOTE]
>
>Pour la segmentation en flux continu, les données nouvellement ingérées peuvent prendre jusqu’à **2 heures** pour se propager entièrement en [!DNL Adobe Experience Platform] pour une utilisation en temps réel. Les audiences qui reposent sur des conditions basées sur un jour ou sur l’heure (par exemple, « événements survenus aujourd’hui ») peuvent présenter une complexité supplémentaire dans le timing de la qualification. Si votre parcours dépend de la qualification immédiate de l’audience, pensez à ajouter une courte [activité d’attente](wait-activity.md) au début. Vous pouvez également prévoir un temps de mémoire tampon pour garantir une qualification précise.

#### Pourquoi tous les profils qualifiés ne peuvent-ils pas rejoindre le parcours ? {#streaming-entry-caveats}

Lors de l’utilisation d’audiences en streaming avec l’activité **Qualification d’audience**, tous les profils qui remplissent les critères de l’audience ne rejoindront pas nécessairement le parcours. Ce comportement peut se produire pour les raisons suivantes :

* **Profils déjà dans l’audience** : seuls les profils nouvellement qualifiés pour l’audience après la publication du parcours déclencheront l’entrée. Les profils déjà présents dans l’audience avant la publication ne pourront pas y entrer.

* **Temps d’activation de parcours** : lorsque vous publiez un parcours, l’activité **Qualification d’audience** prend jusqu’à **10 minutes** pour devenir active et commencer à écouter les entrées et les sorties de profil. [En savoir plus sur l’activation des parcours](#configure-segment-qualification).

* **Sorties rapides de l’audience** : si un profil remplit les conditions de l’audience mais qu’il la quitte avant le déclenchement de l’entrée dans le parcours, il se peut que ce profil ne rejoigne pas le parcours.

* **Délai entre la qualification et le traitement du parcours** : en raison de la nature distribuée des [!DNL Adobe Experience Platform], il peut y avoir des écarts de délai. Un profil peut être qualifié avant que le parcours ne traite l’événement de qualification.

**Recommandations :**

* Après la publication d’un parcours, attendez au moins 10 minutes avant d’envoyer des événements ou des données qui déclencheront la qualification du profil. Cela permet de s’assurer que le parcours est entièrement activé et prêt à traiter les entrées.

* Pour les cas d’utilisation critiques où vous devez vous assurer que tous les profils qualifiés entrent, pensez à utiliser une activité [Lecture d’audience](read-audience.md) à la place. Il traite tous les profils d’une audience à un moment spécifique.

* Surveillez le [débit et taux d’entrée](entry-management.md#profile-entrance-rate) de votre parcours pour comprendre les modèles de flux de profil.

* Si les profils n’entrent pas comme prévu, consultez le [guide de dépannage](troubleshooting-execution.md#checking-if-people-enter-the-journey) pour obtenir des instructions supplémentaires.

### Éviter les surcharges {#overloads-speed-segment-qualification}

Voici quelques bonnes pratiques qui permettront d’éviter de surcharger les systèmes utilisés dans les parcours (sources de données, actions personnalisées, activités d’action de canal) :

* N’utilisez pas une audience par lots immédiatement après sa création dans une activité **[!UICONTROL Qualification d’audience]**. Cela permet d’éviter le premier pic de calcul. Un avertissement jaune apparaît dans la zone de travail du parcours si vous êtes sur le point d’utiliser une audience qui n’a jamais été calculée.

  ![Message d’erreur indiquant que l’audience est introuvable dans [!DNL Adobe Experience Platform]](assets/segment-error.png)

* Mettez en place une règle de capping pour les sources de données et les actions utilisées dans les parcours pour éviter de les surcharger. Pour en savoir plus, consultez la [documentation de Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html?lang=fr){target="_blank"}. Notez que la règle de capping ne permet pas de nouvelle tentative. Si vous avez besoin d’effectuer une nouvelle tentative, utilisez un autre chemin dans le parcours en cochant la case **[!UICONTROL Ajouter un itinéraire alternatif en cas de temporisation ou d’erreur]** dans les conditions ou les actions.

* Avant d’utiliser l’audience dans un parcours en production, évaluez quotidiennement le nombre de personnes qualifiées pour cette audience. Pour ce faire, accédez au menu **[!UICONTROL Audiences]**, ouvrez l’audience, puis consultez le graphique **[!UICONTROL Profils dans le temps]**.

  ![Message d’avertissement lorsque l’audience comporte trop d’événements pour le traitement en temps réel](assets/segment-overload.png)

Pour en savoir plus sur les limites de débit d’entrée, consultez [cette section](entry-management.md#profile-entrance-rate).

## Mécanismes de sécurisation et limitations {#audience-qualification-guardrails}

Utilisez les mécanismes de sécurisation et suivez les recommandations ci-dessous pour créer des parcours de qualification d’audience. Consultez également les [Bonnes pratiques en matière de qualification d’audience](#best-practices-segments).


* Les parcours de qualification d’audience sont principalement conçus pour fonctionner avec les audiences en streaming. Cette combinaison garantit une meilleure expérience en temps réel. Il est vivement recommandé d’utiliser des **audiences en streaming** dans l’activité Qualification d’audience.

  Cependant, si vous souhaitez utiliser des attributs basés sur l’ingestion par lots dans votre audience en streaming ou une audience par lots dans un parcours de qualification d’audience, tenez compte de la période d’évaluation/d’activation de l’audience. Une audience par lots ou une audience en streaming utilisant des attributs ingérés par lots est prête à être utilisée dans l’activité **Qualification d’audience** environ **2 heures** après la fin de votre traitement de segmentation. Ce traitement s’exécute une fois par jour, à l’heure définie par l’administrateur ou l’administratrice de votre organisation Adobe.

* Les audiences [!DNL Adobe Experience Platform] sont calculées une fois par jour (audiences **par lot**) ou en temps réel (pour les audiences **en flux continu**, à l’aide de l’option Audiences haute fréquence de [!DNL Adobe Experience Platform]).

   * Si l’audience sélectionnée est en streaming, les personnes appartenant à cette audience peuvent éventuellement rejoindre le parcours en temps réel.
   * Si l’audience est par lot, les personnes nouvellement qualifiées pour cette audience peuvent éventuellement rejoindre le parcours lorsque le calcul de l’audience est exécuté le [!DNL Adobe Experience Platform].

  Afin d’appliquer les bonnes pratiques, utilisez uniquement des audiences en streaming dans une activité **Qualification d’audience**. Pour les cas d’utilisation par lots, utilisez une activité **[Lecture d’audience](read-audience.md)**.

  >[!NOTE]
  >
  >En raison de la nature par lots des audiences créées à l’aide de workflows de composition et de chargements personnalisés, ces audiences ne peuvent pas être ciblées dans une activité « Qualification d’audience ». Seules les audiences créées à l’aide de définitions de segment peuvent être utilisées dans cette activité.


* Vous ne pouvez pas utiliser les groupes de champs d’événement d’expérience dans les parcours qui commencent par une activité **Lecture d’audience**, **Qualification d’audience** ou **Événement métier**.

* Lorsque vous utilisez une activité de **qualification d’audience** dans un parcours, cette activité peut prendre jusqu’à 10 minutes avant d’être active et d’écouter les profils entrant ou sortant de l’audience.


>[!CAUTION]
>
>[Les mécanismes de sécurisation pour la segmentation et les données du profil client en temps réel](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=fr){target="_blank"} s’appliquent également à [!DNL Adobe Journey Optimizer].



## Vidéo pratique {#video}

Découvrez des cas d’utilisation des parcours de qualification d’audience dans cette vidéo. Découvrez comment créer un parcours avec qualification d’audience et les bonnes pratiques à appliquer.

>[!VIDEO](https://video.tv.adobe.com/v/3425028?quality=12)
