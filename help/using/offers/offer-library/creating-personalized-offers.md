---
title: Création d’offres personnalisées
description: Découvrez comment créer des offres personnalisées dans Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 90%

---

# Création d’offres personnalisées {#creating-personalized-offers}

Avant de créer une offre, assurez-vous que vous avez créé les éléments suivants :

* Un **emplacement** dans lequel l’offre sera affichée. Voir [Création de placements](../offer-library/creating-placements.md)
* Une **règle de décision** qui définit la condition dans laquelle l’offre sera présentée. Voir [Création de règles de décision](../offer-library/creating-decision-rules.md).
* Une ou plusieurs **balises** que vous souhaitez associer à l’offre. Voir [Création de balises](../offer-library/creating-tags.md).

![](../../assets/do-not-localize/how-to-video.png) [Découvrez cette fonctionnalité en vidéo](#video)

La liste des offres personnalisées est accessible dans le menu **[!UICONTROL Offres]**.

![](../../assets/offers_list.png)

## Création de l’offre {#create-offer}

Pour créer une **offre**, procédez comme suit :

1. Cliquez sur **[!UICONTROL Créer une offre]**, puis sélectionnez **[!UICONTROL offre personnalisée]**.

   ![](../../assets/create_offer.png)

1. Indiquez le nom de l’offre, ainsi que sa date et son heure de début et de fin. Vous pouvez également associer une ou plusieurs balise(s) existante(s) à l’offre, ce qui vous permet de rechercher et d’organiser plus facilement la bibliothèque des offres.

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >La section **[!UICONTROL Attributs de l’offre]** vous permet d’associer des paires clé-valeur à l’offre à des fins de rapports et d’analyse.

## Configuration des représentations de l’offre {#representations}

1. Ajoutez une ou plusieurs représentations pour votre offre à l’aide du bouton **[!UICONTROL Ajouter une représentation]**.

   >[!NOTE]
   >
   >Une offre peut être affichée à différents endroits dans un message : dans une bannière supérieure avec une image, sous forme de texte dans un paragraphe, sous forme de bloc html, etc. Plus une offre a de représentations, plus il y a d’occasions d’utiliser l’offre dans différents contextes d’emplacement.

1. Pour chaque représentation, spécifiez le **[!UICONTROL Canal]** et l’**[!UICONTROL Emplacement]** où l’offre sera affichée.

   ![](../../assets/channel-placement.png)

   Le bouton **[!UICONTROL Parcourir]** permet de filtrer les emplacements disponibles, en fonction de leur canal et/ou de leur type de contenu.

   ![](../../assets/browse-placements.png)

1. Ajoutez le contenu à chaque représentation provenant de la bibliothèque de ressources Adobe Experience Cloud ou d’un emplacement public externe.

   * Pour ajouter du contenu issu de la bibliothèque de ressources Adobe Experience Cloud, faites-le glisser du volet de gauche vers la zone de représentation, puis spécifiez l’URL à associer au contenu dans le champ **[!UICONTROL Lien de destination]**.

      >[!NOTE]
      >
      >Il n’est possible d’effectuer un glisser-déposer du contenu qu’à partir du Sélecteur de ressources dans le volet de gauche. Notez que seul le contenu correspondant au type de contenu de l’emplacement peut être utilisé.

      ![](../../assets/offer_drag_content.png)

   * Pour ajouter du contenu à partir d’un emplacement public externe, cliquez sur le bouton **[!UICONTROL Ajouter du contenu]**, puis spécifiez le nom, l’URL et le lien de destination du contenu à ajouter.

      Assurez-vous que le contenu que vous ajoutez correspond au type de contenu de l’emplacement sélectionné.

      ![](../../assets/offer_add_content.png)

   * Vous pouvez également insérer du contenu de type texte. Pour ce faire, cliquez sur le bouton **[!UICONTROL Ajouter du contenu]**, puis sélectionnez l’option **[!UICONTROL Texte personnalisé]**. Dans le champ **[!UICONTROL Texte]**, saisissez le texte qui s’affichera dans l’offre.

      >[!NOTE]
      >
      >Cette option n’est pas disponible pour les emplacements de type image.

      ![](../../assets/offer_text_content.png)

## Ajout de règles d’éligibilité et de contraintes {#eligibility}

Les règles d’éligibilité et les contraintes permettent de définir les conditions d’affichage d’une offre.

1. Configurez l’**[!UICONTROL éligibilité des offres]**. Par défaut, l’option de règle de décision **[!UICONTROL Tous les visiteurs]** est sélectionnée, ce qui signifie que tout profil peut se voir présenter l’offre.

   Vous pouvez limiter la présentation de l’offre aux membres d’un ou de plusieurs segments d’Adobe Experience Platform. Pour cela, activez l’option **[!UICONTROL Visiteurs appartenant à un ou plusieurs segments]**, puis ajoutez un ou plusieurs segments dans le volet de gauche et combinez-les à l’aide des opérateurs logiques **[!UICONTROL Et]** / **[!UICONTROL Ou]**.

   Pour plus d’informations sur l’utilisation d’un segment, consultez la [documentation du service de segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr).

   ![](../../assets/offer-eligibility-segment.png)

   Si vous souhaitez associer une règle de décision spécifique à l’offre, sélectionnez **[!UICONTROL Par une règle de décision définie]**, puis faites glisser la règle de décision de votre choix depuis le volet de gauche vers la zone **[!UICONTROL Règle de décision]**. Pour plus d’informations sur la façon de créer une règle de décision, reportez-vous à [cette section](../offer-library/creating-decision-rules.md).

   ![](../../assets/offer_rule.png)

1. Définissez la **[!UICONTROL Priorité]** de l’offre par rapport à d’autres si l’utilisateur est éligible à plusieurs offres. Plus la priorité d’une offre est élevée, plus elle sera comparée à celle d’autres offres

1. Spécifiez la **[!UICONTROL Limitation]** de l’offre, soit le nombre total de fois où l’offre sera présentée au total à tous les utilisateurs. Si le nombre de fois où l’offre a été diffusée à tous les utilisateurs correspond à celui que vous avez indiqué dans ce champ, la diffusion de l’offre s’arrête.

   >[!NOTE]
   >
   >Le nombre de fois où une offre est proposée est calculé au moment de la préparation de l’email. Par exemple, si vous préparez un email contenant un certain nombre d’offres, ces chiffres sont pris en compte dans votre limitation maximale, et ce que l’email soit envoyé ou non.
   >
   >Si une diffusion email est supprimée ou si la préparation est effectuée à nouveau avant d’être envoyée, la valeur de limitation de l’offre est automatiquement mise à jour.

   ![](../../assets/offer_capping.png)

   Dans l’exemple ci-dessus :

   * La priorité de l’offre est définie sur « 50 », ce qui signifie que l’offre sera présentée avant les offres dont la priorité est comprise entre 1 et 49, et après celles dont la priorité est d’au moins 51.
   * L’offre sera prise en compte uniquement pour les utilisateurs qui correspondent à la règle de décision « Clients fidèles Gold ».
   * L’offre ne sera présentée qu’une seule fois par utilisateur.

## Examen de l’offre {#review}

Une fois les règles d’éligibilité et les contraintes définies, un résumé des propriétés de l’offre s’affiche. Si tout est configuré correctement et que votre offre est prête à être présentée aux utilisateurs, cliquez sur **[!UICONTROL Terminer]**, puis sélectionnez **[!UICONTROL Enregistrer et valider]**.

Vous pouvez également enregistrer l’offre en tant que version préliminaire pour la modifier et l’approuver ultérieurement.

![](../../assets/offer_review.png)

L’offre s’affiche dans la liste avec le statut **[!UICONTROL En ligne]** ou **[!UICONTROL Version préliminaire]**, selon que vous l’avez approuvée ou non à l’étape précédente.

Elle est maintenant prête à être diffusée aux utilisateurs. Vous pouvez la sélectionner pour afficher ses propriétés et la modifier ou la supprimer.

![](../../assets/offer_created.png)

Une fois une offre créée, vous pouvez cliquer sur son nom dans la liste pour accéder à des informations détaillées, ainsi que surveiller toutes les modifications qui y ont été apportées à l&#39;aide de l&#39;onglet **[!UICONTROL Journal des modifications]** (voir [Surveillance des modifications apportées aux offres et décisions](../get-started/user-interface.md#monitoring-changes)).

## Tutoriel vidéo {#video}

>[!NOTE]
>
>Cette vidéo s’applique au service d’applications d’Offer decisioning créé sur Adobe Experience Platform. Toutefois, il fournit des orientations générales pour l&#39;utilisation de l&#39;Offre dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
