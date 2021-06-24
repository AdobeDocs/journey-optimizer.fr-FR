---
title: Création d'offres personnalisées
description: Découvrez comment créer des offres personnalisées dans Adobe Experience Platform.
feature: Offres
topic: Intégrations
role: User
level: Intermediate
source-git-commit: 8ffafb76b15ea7dfabd52c278833fc607f3338a5
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 95%

---

# Création d&#39;offres personnalisées {#creating-personalized-offers}

Avant de créer une offre, assurez-vous que vous avez créé les éléments suivants :

* Un **emplacement** dans lequel l&#39;offre sera affichée. Voir [Créer des emplacements](../offer-library/creating-placements.md)
* Une **règle de décision** qui définit la condition dans laquelle l&#39;offre sera présentée. Voir [Création de règles de décision](../offer-library/creating-decision-rules.md).
* Une ou plusieurs **balises** que vous souhaitez associer à l&#39;offre. Voir [Création de balises](../offer-library/creating-tags.md).

![](../../assets/do-not-localize/how-to-video.png) [Découvrez cette fonctionnalité en vidéo](#video)

La liste des offres personnalisées est accessible dans le menu **[!UICONTROL Offres]**.

![](../../assets/offers_list.png)

## Création de l&#39;offre {#create-offer}

Pour créer une **offre**, procédez comme suit :

1. Cliquez sur **[!UICONTROL Créer une offre]**, puis sélectionnez **[!UICONTROL Offre personnalisée]**.

   ![](../../assets/create_offer.png)

1. Indiquez le nom de l&#39;offre, ainsi que sa date et son heure de début et de fin. Vous pouvez également associer une ou plusieurs balise(s) existante(s) à l&#39;offre, ce qui vous permet de rechercher et d&#39;organiser plus facilement la bibliothèque des offres.

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >La section **[!UICONTROL Attributs de l&#39;offre]** vous permet d&#39;associer des paires clé-valeur à l&#39;offre à des fins de rapports et d&#39;analyse.

## Configuration des représentations de l&#39;offre {#representations}

1. Ajoutez une ou plusieurs représentations pour votre offre à l&#39;aide du bouton **[!UICONTROL Ajouter une représentation]**.

   >[!NOTE]
   >
   >Une offre peut être affichée à différents endroits dans un message : dans une bannière supérieure avec une image, sous forme de texte dans un paragraphe, sous forme de bloc html, etc. Plus une offre a de représentations, plus il y a d&#39;occasions d&#39;utiliser l&#39;offre dans différents contextes d&#39;emplacement.

1. Pour chaque représentation, spécifiez le **[!UICONTROL Canal]** et l&#39;**[!UICONTROL Emplacement]** où l&#39;offre sera affichée.

   ![](../../assets/channel-placement.png)

   Le bouton **[!UICONTROL Parcourir]** permet de filtrer les emplacements disponibles, en fonction de leur canal et/ou de leur type de contenu.

   ![](../../assets/browse-placements.png)

1. Ajoutez le contenu à chaque représentation provenant de la bibliothèque de ressources Adobe Experience Cloud ou d&#39;un emplacement public externe.

   * Pour ajouter du contenu issu de la bibliothèque de ressources Adobe Experience Cloud, faites-le glisser du volet de gauche vers la zone de représentation, puis spécifiez l&#39;URL à associer au contenu dans le champ **[!UICONTROL Lien de destination]**.

      >[!NOTE]
      >
      >Il n&#39;est possible d&#39;effectuer un glisser-déposer du contenu qu&#39;à partir du Sélecteur de ressources dans le volet de gauche. Notez que seul le contenu correspondant au type de contenu de l&#39;emplacement peut être utilisé.

      ![](../../assets/offer_drag_content.png)

   * Pour ajouter du contenu à partir d&#39;un emplacement public externe, cliquez sur le bouton **[!UICONTROL Ajouter du contenu]**, puis spécifiez le nom, l&#39;URL et le lien de destination du contenu à ajouter.

      Assurez-vous que le contenu que vous ajoutez correspond au type de contenu de l&#39;emplacement sélectionné.

      ![](../../assets/offer_add_content.png)

   * Vous pouvez également insérer du contenu de type texte. Pour ce faire, cliquez sur le bouton **[!UICONTROL Ajouter du contenu]**, puis sélectionnez l&#39;option **[!UICONTROL Texte personnalisé]**. Dans le champ **[!UICONTROL Texte]**, saisissez le texte qui s&#39;affichera dans l&#39;offre.

      >[!NOTE]
      >
      >Cette option n&#39;est pas disponible pour les emplacements de type image.

      ![](../../assets/offer_text_content.png)

## Ajout de règles d’éligibilité et de contraintes {#eligibility}

Les règles d&#39;éligibilité et les contraintes permettent de définir les conditions d&#39;affichage d&#39;une offre.

1. Configurez l&#39;**[!UICONTROL éligibilité des offres]**. Par défaut, l&#39;option de règle de décision **[!UICONTROL Tous les visiteurs]** est sélectionnée, ce qui signifie que tout profil peut se voir présenter l&#39;offre.

   Vous pouvez limiter la présentation de l&#39;offre aux membres d&#39;un ou de plusieurs segments d&#39;Adobe Experience Platform. Pour cela, activez l&#39;option **[!UICONTROL Visiteurs appartenant à un ou plusieurs segments]**, puis ajoutez un ou plusieurs segments dans le volet de gauche et combinez-les à l&#39;aide des opérateurs logiques **[!UICONTROL Et]** / **[!UICONTROL Ou]**.

   Pour plus d&#39;informations sur l&#39;utilisation d&#39;un segment, consultez la [documentation du service de segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr).

   ![](../../assets/offer-eligibility-segment.png)

   Si vous souhaitez associer une règle de décision spécifique à l&#39;offre, sélectionnez **[!UICONTROL Par une règle de décision définie]**, puis faites glisser la règle de décision de votre choix depuis le volet de gauche vers la zone **[!UICONTROL Règle de décision]**. Pour plus d&#39;informations sur la façon de créer une règle de décision, reportez-vous à [cette section](../offer-library/creating-decision-rules.md).

   ![](../../assets/offer_rule.png)

1. Définissez la **[!UICONTROL Priorité]** de l&#39;offre par rapport à d&#39;autres si l&#39;utilisateur est éligible à plusieurs offres. Plus la priorité d’une offre est élevée, plus sa priorité est comparée à d’autres offres.

1. Spécifiez la **[!UICONTROL Limitation]** de l&#39;offre, soit le nombre total de fois où l&#39;offre sera présentée au total à tous les utilisateurs. Si le nombre de fois où l&#39;offre a été diffusée à tous les utilisateurs correspond à celui que vous avez indiqué dans ce champ, la diffusion de l&#39;offre s&#39;arrête.

   >[!NOTE]
   >
   >Le nombre de fois où une offre est proposée est calculé au moment de la préparation de l&#39;email. Par exemple, si vous préparez un email contenant un certain nombre d&#39;offres, ces chiffres sont pris en compte dans votre limitation maximale, et ce que l&#39;email soit envoyé ou non.
   >
   >Si une diffusion email est supprimée ou si la préparation est effectuée à nouveau avant d&#39;être envoyée, la valeur de limitation de l&#39;offre est automatiquement mise à jour.

   ![](../../assets/offer_capping.png)

   Dans l&#39;exemple ci-dessus :

   * La priorité de l&#39;offre est définie sur « 50 », ce qui signifie que l&#39;offre sera présentée avant les offres dont la priorité est comprise entre 1 et 49, et après celles dont la priorité est d&#39;au moins 51.
   * L&#39;offre sera prise en compte uniquement pour les utilisateurs qui correspondent à la règle de décision « Clients fidèles Gold ».
   * L&#39;offre ne sera présentée qu&#39;une seule fois par utilisateur.

## Examen de l&#39;offre {#review}

Une fois les règles d&#39;éligibilité et les contraintes définies, un résumé des propriétés de l&#39;offre s&#39;affiche. Si tout est configuré correctement et que votre offre est prête à être présentée aux utilisateurs, cliquez sur **[!UICONTROL Terminer]**, puis sélectionnez **[!UICONTROL Enregistrer et valider]**.

Vous pouvez également enregistrer l&#39;offre en tant que version préliminaire pour la modifier et l&#39;approuver ultérieurement.

![](../../assets/offer_review.png)

L’offre s’affiche dans la liste avec le statut **[!UICONTROL En ligne]** ou **[!UICONTROL En création]**, selon que vous l’avez approuvée ou non à l’étape précédente.

Elle est maintenant prête à être diffusée aux utilisateurs. Vous pouvez la sélectionner pour afficher ses propriétés et la modifier ou la supprimer.

![](../../assets/offer_created.png)

Une fois l&#39;offre créée, vous pouvez cliquer sur son nom dans la liste pour accéder à des informations détaillées et surveiller toutes les modifications qui y ont été apportées dans l&#39;onglet **[!UICONTROL Log des modifications]** (voir [Surveillance des modifications apportées aux offres et aux décisions](../get-started/user-interface.md#monitoring-changes)).

## Tutoriel vidéo {#video}

>[!NOTE]
>
>Cette vidéo s’applique au service applicatif d’Offer decisioning créé sur Adobe Experience Platform. Elle fournit toutefois des orientations générales pour l&#39;utilisation d’Offer dans le contexte de Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
