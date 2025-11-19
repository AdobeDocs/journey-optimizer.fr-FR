---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Créer des règles de décision
description: Découvrez comment créer des règles de décision pour définir pour qui les offres peuvent être affichées.
badge: label="Hérité" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: ht
source-wordcount: '408'
ht-degree: 100%

---

# Créer des règles de décision {#create-decision-rules}

## À propos des règles de décision {#about}

Vous pouvez créer des règles de décision d&#39;offre basées sur les données disponibles dans Adobe Experience Platform. Les règles de décision déterminent pour qui une offre peut être affichée.

Par exemple, vous pouvez indiquer que vous souhaitez qu&#39;une « offre vêtements d&#39;hiver pour femmes » s&#39;affiche lorsque (genre = « femme ») et (région = « nord-est »).

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

Voici une liste des limites à connaître lors de l’utilisation de règles de décision :

* La prise de décision Edge utilise le profil Edge qui ne stocke pas d’événements. Par conséquent, toute règle utilisée dans une décision Edge sera non valide.
* Lors de la création d’une règle de décision, la recherche dans une période précédente n’est pas prise en charge. Par exemple, si vous spécifiez un événement d’expérience qui s’est produit au cours du dernier mois en tant que composant de la règle. Toute tentative d’inclusion d’une période de recherche arrière lors de la création d’une règle déclenche une erreur lors de son enregistrement.
  <!--* Decision requests that use the hub profile will look at the last 100 experience events on the profile to evaluate rules that reference historical experience events.-->

## Créer une règle de décision {#create}

La liste des règles de décision créées est accessible dans le menu **[!UICONTROL Composants]**.

![](../assets/decision_rules_list.png)

Pour créer cette règle de décision, procédez comme suit :

1. Accédez à l&#39;onglet **[!UICONTROL Règles]**, puis cliquez sur **[!UICONTROL Créer une règle]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Nommez votre règle et fournissez une description, puis configurez-la en fonction de vos besoins.

   Pour ce faire, le **Créateur de segments** d’Adobe Experience Platform est disponible pour vous aider à créer les conditions de la règle. [Découvrez comment créer des définitions de segment](../../audience/creating-a-segment-definition.md).

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >Le Créateur de segments fourni pour créer des règles de décision présente certaines spécificités par rapport à celui utilisé avec le service **[!UICONTROL Segmentation]**. Cependant, le processus global décrit dans la documentation du [Créateur de segments](../../audience/creating-a-segment-definition.md) est toujours valide pour créer des règles de décision d’offre. Pour en savoir plus, consultez la [documentation du service de segmentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=fr).

1. À mesure que vous ajoutez et configurez de nouveaux champs dans l’espace de travail, le volet **[!UICONTROL Propriétés de l’audience]** affiche des informations sur l’estimation des profils appartenant à l’audience. Cliquez sur **[!UICONTROL Actualiser l’estimation]** pour mettre à jour les données.

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >Les estimations de profil ne sont pas disponibles lorsque les paramètres de règle incluent des données qui ne figurent pas dans le profil, telles que des données contextuelles. Par exemple, une règle d’éligibilité qui exige que la météo actuelle soit de ≥80 degrés.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer.

1. Une fois la règle créée, elle s’affiche dans la liste des **[!UICONTROL règles]**. Vous pouvez la sélectionner pour afficher ses propriétés et la modifier ou la supprimer.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>Les offres basées sur un événement ne sont actuellement pas prises en charge dans [!DNL Journey Optimizer]. Si vous créez une règle de décision basée sur un [événement](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=fr#events){target="_blank"}, vous ne pourrez pas l’exploiter dans une offre.

## Tutoriel vidéo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
