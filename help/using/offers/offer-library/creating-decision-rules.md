---
title: Créer des règles de décision
description: Découvrez comment créer des règles de décision pour définir à qui les offres peuvent être affichées
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 55d9befff9b9bf1bc81c6553cd76f015fdd3116e
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Créer des règles de décision {#create-decision-rules}

Vous pouvez créer des règles de décision d’offre basées sur les données disponibles dans Adobe Experience Platform. Les règles de décision déterminent pour qui une offre peut être affichée.

Par exemple, vous pouvez indiquer que vous souhaitez qu’une &quot;offre vêtements d’hiver pour femmes&quot; soit affichée uniquement lorsque (Genre = &quot;Femme&quot;) et (Région = &quot;Northeast&quot;).

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

La liste des règles de décision créées est accessible dans le **[!UICONTROL Components]** .

![](../assets/decision_rules_list.png)

Pour créer une règle de décision, procédez comme suit :

1. Accédez au **[!UICONTROL Rules]** , puis cliquez sur **[!UICONTROL Create rule]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Nommez votre règle et décrivez-la, puis configurez-la selon vos besoins.

   Pour ce faire, la variable **Créateur de segments** est disponible pour vous aider à créer les conditions de la règle. [En savoir plus](../../segment/about-segments.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >Le créateur de segments fourni pour créer des règles de décision présente certaines spécificités par rapport à celui utilisé avec la variable **[!UICONTROL Audience Destinations]** service. Par exemple, la variable **[!UICONTROL Segments]** n’est pas disponible. Toutefois, le processus global décrit dans la section [Créateur de segments](../../segment/about-segments.md) La documentation est toujours valide pour créer des règles de décision d’offres. En savoir plus dans la section [Documentation d’Adobe Experience Platform Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html).

1. À mesure que vous ajoutez et configurez de nouveaux champs dans l’espace de travail, la variable **[!UICONTROL Segment properties]** affiche des informations sur les profils estimés appartenant au segment. Cliquez sur **[!UICONTROL Refresh estimate]** pour mettre à jour les données.

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >Les estimations de profil ne sont pas disponibles lorsque les paramètres de règle incluent des données qui ne figurent pas dans le profil, telles que des données contextuelles. Par exemple, une règle d’éligibilité qui exige que la météo actuelle soit de ≥80 degrés.

1. Cliquez sur **[!UICONTROL Save]** pour confirmer.

1. Une fois créée, la règle s’affiche dans la variable **[!UICONTROL Rules]** liste. Vous pouvez la sélectionner pour afficher ses propriétés, puis la modifier ou la supprimer.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>Les offres basées sur un événement ne sont actuellement pas prises en charge dans [!DNL Journey Optimizer]. Si vous créez une règle de décision basée sur une [event](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}, vous ne pourrez pas l’exploiter dans une offre.

## Tutoriel vidéo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
