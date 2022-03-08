---
title: Création de règles de décision
description: Découvrez comment créer des règles de décision pour définir pour qui les offres peuvent être affichées.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 100%

---

# Création de règles de décision {#create-decision-rules}

Vous pouvez créer des règles de décision d&#39;offre basées sur les données disponibles dans Adobe Experience Platform. Les règles de décision déterminent pour qui une offre peut être affichée.

Par exemple, vous pouvez indiquer que vous souhaitez qu&#39;une « offre vêtements d&#39;hiver pour femmes » s&#39;affiche lorsque (genre = « femme ») et (région = « nord-est »).

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

La liste des règles de décision créées est accessible dans le menu **[!UICONTROL Composants]**.

![](../assets/decision_rules_list.png)

Pour créer cette règle de décision, procédez comme suit :

1. Accédez à l&#39;onglet **[!UICONTROL Règles]**, puis cliquez sur **[!UICONTROL Créer une règle]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Nommez votre règle et fournissez une description, puis configurez-la en fonction de vos besoins.

   Pour ce faire, le **Créateur de segments** est disponible pour vous aider à créer les conditions de la règle. [En savoir plus](../../segment/about-segments.md)

   Dans cet exemple, la règle cible les clients qui ont le niveau de fidélité « Or ».

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >Le Créateur de segments fourni pour créer des règles de décision présente certaines spécificités par rapport à celui utilisé avec le service **[!UICONTROL Destinations d&#39;audience]**. Par exemple, l&#39;onglet **[!UICONTROL Segments]** n&#39;est pas disponible. Cependant, le processus global décrit dans la documentation du Créateur de segments est toujours valide pour créer des règles de décision d&#39;offre.


1. Cliquez sur **[!UICONTROL Enregistrer]** pour valider.

1. Une fois la règle créée, elle s&#39;affiche dans la liste des règles. Vous pouvez la sélectionner pour afficher ses propriétés et la modifier ou la supprimer.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>Les offres basées sur un événement ne sont actuellement pas prises en charge dans [!DNL Journey Optimizer]. Si vous créez une règle de décision basée sur un [événement](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=fr#events){target=&quot;_blank&quot;}, vous ne pourrez pas l&#39;exploiter dans une offre.

## Tutoriel vidéo {#video}

>[!NOTE]
>
>Cette vidéo s’applique au service applicatif Offer Decisioning intégré à Adobe Experience Platform. Toutefois, elle fournit des orientations générales pour l&#39;utilisation de l&#39;Offre dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
