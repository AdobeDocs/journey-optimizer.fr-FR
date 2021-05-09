---
title: Créer des règles de décision
description: Découvrez comment créer des règles de décision dans Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Créer des règles de décision {#creating-decision-rules}

Vous pouvez créer des règles de décision d’offre basées sur les données disponibles dans Adobe Experience Platform. Les règles de décision déterminent à qui une offre peut être affichée.

Par exemple, vous pouvez indiquer que vous souhaitez uniquement qu’une &quot;Offre Vêtements d’hiver pour femmes&quot; soit affichée lorsque (Genre = &#39;Femme&#39;) et (Région = &#39;Northeast&#39;).

![](../assets/do-not-localize/how-to-video.png) [Découvrez cette fonctionnalité dans la vidéo](#video)

La liste des règles de décision créées est accessible dans le menu **[!UICONTROL Composants]**.

![](../assets/decision_rules_list.png)

Pour créer une règle de décision, procédez comme suit :

1. Accédez à l&#39;onglet **[!UICONTROL Règles]**, puis cliquez sur **[!UICONTROL Créer une règle]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Nommez votre règle et fournissez une description, puis configurez-la en fonction de vos besoins.

   Pour ce faire, le **créateur de segments** de Adobe Experience Platform est disponible pour vous aider à créer les conditions de la règle. Pour plus d&#39;informations sur la façon de l&#39;utiliser, consultez la [documentation consacrée](https://docs.adobe.com/content/help/en/experience-platform/segmentation/ui/segment-builder.html).

   Dans cet exemple, la règle cible les clients qui ont le niveau de fidélité &quot;Or&quot;.

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >Le créateur de segments fourni pour créer des règles de décision présente certaines spécificités par rapport à celui utilisé avec le service **[!UICONTROL Audiences Destinations]**. Par exemple, l&#39;onglet **[!UICONTROL Segments]** n&#39;est pas disponible pour utilisation. Cependant, le processus global décrit dans la documentation du créateur de segments est toujours valide pour créer des règles de prise de décision pour les offres.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer.

1. Une fois la règle créée, elle s’affiche dans la liste de règles. Vous pouvez la sélectionner pour afficher ses propriétés et la modifier ou la supprimer.

   ![](../assets/rule_created.png)

## Vidéo didactique {#video}

>[!NOTE]
>
>Cette vidéo s’applique au service d’applications d’Offer decisioning créé sur Adobe Experience Platform. Toutefois, il fournit des orientations générales pour l&#39;utilisation de l&#39;Offre dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
