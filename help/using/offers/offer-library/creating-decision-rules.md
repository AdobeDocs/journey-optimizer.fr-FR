---
title: Création de règles de décision
description: Découvrez comment créer des règles de décision dans Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 85%

---

# Création de règles de décision {#creating-decision-rules}

Vous pouvez créer des règles de décision d’offre basées sur les données disponibles dans Adobe Experience Platform. Les règles de décision déterminent pour qui une offre peut être affichée.

Par exemple, vous pouvez indiquer que vous souhaitez qu’une « offre vêtements d’hiver pour femmes » s’affiche lorsque (genre = « femme ») et (région = « nord-est »).

![](../../assets/do-not-localize/how-to-video.png) [Découvrez cette fonctionnalité en vidéo](#video)

La liste des règles de décision créées est accessible dans le menu **[!UICONTROL Composants]**.

![](../../assets/decision_rules_list.png)

Pour créer cette règle de décision, procédez comme suit :

1. Accédez à l’onglet **[!UICONTROL Règles]**, puis cliquez sur **[!UICONTROL Créer une règle]**.

   ![](../../assets/offers_decision_rule_creation.png)

1. Nommez votre règle et fournissez une description, puis configurez-la en fonction de vos besoins.

   Pour ce faire, le **Créateur de segments** d’Adobe Experience Platform est disponible pour vous aider à créer les conditions de la règle. Pour plus d’informations sur son utilisation, reportez-vous à la [documentation dédiée](https://docs.adobe.com/content/help/fr-FR/experience-platform/segmentation/ui/segment-builder.html).

   Dans cet exemple, la règle cible les clients qui ont le niveau de fidélité « Or ».

   ![](../../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >Le Créateur de segments fourni pour créer des règles de décision présente certaines spécificités par rapport à celui utilisé avec le service **[!UICONTROL Destinations d’audience]**. Par exemple, l’onglet **[!UICONTROL Segments]** n’est pas disponible. Cependant, le processus global décrit dans la documentation du Créateur de segments est toujours valide pour créer des règles de prise de décision pour les offres.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour valider.

1. Une fois la règle créée, elle s’affiche dans la liste des règles. Vous pouvez la sélectionner pour afficher ses propriétés et la modifier ou la supprimer.

   ![](../../assets/rule_created.png)

## Tutoriel vidéo {#video}

>[!NOTE]
>
>Cette vidéo s’applique au service d’applications d’Offer decisioning créé sur Adobe Experience Platform. Toutefois, il fournit des orientations générales pour l&#39;utilisation de l&#39;Offre dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
