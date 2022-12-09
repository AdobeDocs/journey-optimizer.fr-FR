---
title: Ajouter des représentations à une offre
description: Découvrez comment ajouter des représentations à vos offres
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 718af505-7b7c-495e-8974-bd9c35d796bb
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 0%

---

# Ajouter des représentations à une offre {#add-representations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_representation"
>title="Représentations"
>abstract="Ajoutez des représentations pour définir l’emplacement d’affichage de votre offre dans le message. Plus une offre a de représentations, plus il y a d’opportunités d’utiliser l’offre dans différents contextes d’emplacement."

Une offre peut être affichée à différents endroits dans un message : dans une bannière supérieure avec une image, comme texte dans un paragraphe, comme bloc HTML, etc. Plus une offre a de représentations, plus il y a d’opportunités d’utiliser l’offre dans différents contextes d’emplacement.

## Configurer les représentations de l’offre {#representations}

Pour ajouter une ou plusieurs représentations à votre offre et les configurer, procédez comme suit.

1. Pour la première représentation, commencez par sélectionner la variable **[!UICONTROL Channel]** qui sera utilisé.

   ![](../assets/channel-placement.png)

   >[!NOTE]
   >
   >Seuls les emplacements disponibles pour le canal sélectionné s’affichent dans la variable **[!UICONTROL Placement]** liste déroulante.

1. Sélectionnez un emplacement dans la liste.

   Vous pouvez également utiliser le bouton en regard de la fonction **[!UICONTROL Placement]** liste déroulante pour parcourir tous les emplacements.

   ![](../assets/browse-button-placements.png)

   Vous pouvez toujours filtrer les emplacements selon leur canal et/ou type de contenu. Sélectionnez un emplacement et cliquez sur **[!UICONTROL Select]**.

   ![](../assets/browse-placements.png)

1. Ajoutez du contenu à votre représentation. Découvrez comment [cette section](#content).

1. Lorsque vous ajoutez du contenu, tel qu’une image ou une URL, vous pouvez définir une **[!UICONTROL Destination link]**: les utilisateurs qui cliquent sur l’offre sont redirigés vers la page correspondante.

   ![](../assets/offer-destination-link.png)

1. Enfin, sélectionnez la langue de votre choix pour vous aider à identifier et gérer les éléments à afficher pour les utilisateurs.

1. Pour ajouter une autre représentation, utilisez le **[!UICONTROL Add representation]** et ajoutez autant de représentations que nécessaire.

   ![](../assets/offer-add-representation.png)

1. Une fois que vous avez ajouté toutes vos représentations, sélectionnez **[!UICONTROL Next]**.

## Définition du contenu de vos représentations {#content}

Vous pouvez ajouter différents types de contenu à une représentation.

>[!NOTE]
>
>Seul le contenu correspondant au type de contenu de l’emplacement peut être utilisé.

### Ajout d’images {#images}

Si l’emplacement sélectionné est de type image, vous pouvez ajouter du contenu provenant de la variable **Adobe Experience Cloud Asset** Bibliothèque, un référentiel centralisé des ressources fournies par [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> Pour utiliser [Principes fondamentaux d’Adobe Experience Manager Assets](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}, vous devez déployer [!DNL Assets Essentials] pour votre entreprise et assurez-vous que les utilisateurs font partie de la variable **Utilisateurs clients Assets Essentials** ou/et **Utilisateurs d’Assets Essentials** Profils de produit. En savoir plus sur [cette page](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html){target=&quot;_blank&quot;}.

1. Choisissez la **[!UICONTROL Asset library]** .

1. Sélectionner **[!UICONTROL Browse]**.

   ![](../assets/offer-browse-asset-library.png)

1. Parcourir les ressources pour sélectionner l’image de votre choix

1. Cliquez sur **[!UICONTROL Select]**.

   ![](../assets/offer-select-asset.png)

### Ajout de fichiers HTML ou JSON {#html-json}

Si l’emplacement sélectionné est de type HTML, vous pouvez également ajouter du contenu HTML ou JSON provenant de la variable [Bibliothèque de ressources Adobe Experience Cloud](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}).

Par exemple, vous avez créé un modèle de courrier électronique HTML dans [Adobe Experience Manager](https://experienceleague.adobe.com/docs/experience-manager.html){target=&quot;_blank&quot;} et vous souhaitez utiliser ce fichier pour le contenu de votre offre. Au lieu de créer un nouveau fichier, vous pouvez simplement charger le modèle dans le **Bibliothèque de ressources** pour pouvoir la réutiliser dans les représentations de votre offre.

Pour réutiliser votre contenu dans une représentation, accédez au **Bibliothèque de ressources** comme décrit dans [cette section](#images) et sélectionnez le fichier HTML ou JSON de votre choix.

![](../assets/offer-browse-asset-library-json.png)

### Ajout d’URL {#urls}

Pour ajouter du contenu depuis un emplacement public externe, sélectionnez **[!UICONTROL URL]**, puis saisissez l’adresse URL du contenu à ajouter.

![](../assets/offer-content-url.png)

### Ajouter du texte personnalisé {#custom-text}

Vous pouvez également insérer du contenu de type texte lors de la sélection d’un emplacement compatible.

1. Sélectionnez la **[!UICONTROL Custom]** et cliquez sur **[!UICONTROL Add content]**.

   ![](../assets/offer-add-content.png)

   >[!NOTE]
   >
   >Cette option n’est pas disponible pour les emplacements de type image.

1. Saisissez le texte qui s’affichera dans l’offre.

   ![](../assets/offer-text-content.png)

   Vous pouvez personnaliser votre contenu à l&#39;aide de l&#39;éditeur d&#39;expression. En savoir plus sur [personnalisation](../../personalization/personalize.md#use-expression-editor).

   ![](../assets/offer-personalization.png)

   >[!NOTE]
   >
   >Seule la variable **[!UICONTROL Profile attributes]**, **[!UICONTROL Segment memberships]** et **[!UICONTROL Helper functions]** Les sources sont disponibles pour la gestion de la décision.

