---
solution: Journey Optimizer
product: journey optimizer
title: Dynamic Media
description: Utiliser Dynamic Media avec Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: 3e777cc5-a935-4e68-9de7-60b241e78f63
source-git-commit: 714d3dc6f0c8351e95ce4a2df2ad251c1491904b
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 97%

---

# Utiliser Dynamic Media {#aem-dynamic}

## Commencer avec Dynamic Media {#gs-aem-dynamic}

Le sélecteur de ressources prend désormais en charge Dynamic Media, ce qui vous permet de sélectionner et d’utiliser facilement des rendus de médias dynamiques approuvés dans Journey Optimizer. Les modifications apportées aux ressources dans Adobe Experience Manager sont immédiatement répercutées dans votre contenu Journey Optimizer. Ainsi, les versions les plus récentes sont toujours utilisées sans nécessiter de mises à jour manuelles.

Notez que cette intégration n’est disponible que pour les clients et clientes qui utilisent Dynamic Media Manager as a Cloud Service.

Pour en savoir plus sur Dynamic Media dans Adobe Experience Manager as a Cloud Service, consultez la [documentation d’Experience Manager](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media){target="_blank"}.

>[!AVAILABILITY]
>
>Pour les clients du secteur de la santé, l’intégration n’est activée que sous licence pour les offres complémentaires Journey Optimizer Healthcare Shield et Adobe Experience Manager Extended Security for Healthcare.


## Ajouter et gérer des médias dynamiques {#dynamic-media}


Améliorez et optimisez votre contenu pour n’importe quel écran ou navigateur en insérant des médias dynamiques depuis Adobe Experience Manager as a Cloud Service directement dans votre contenu Journey Optimizer.  Vous pouvez ensuite redimensionner, recadrer, améliorer et effectuer d’autres réglages si nécessaire.


>[!IMPORTANT]
>
>Vérifiez que Dynamic Media avec OpenAPI est activé dans Adobe Experience Manager as a Cloud Service. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview#enable-dynamic-media-open-apis){target="_blank"}.

L’intégration de Dynamic Media à Adobe Journey Optimizer est disponible à la fois pour Dynamic Media en [mode Scene7](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/assets/dynamic/config-dms7){target="_blank"} et Dynamic Media [avec OpenAPI](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview){target="_blank"}.

<!--
>[!AVAILABILITY]
>
>Older versions of Outlook (including 2016) do not support rendering of content with Dynamic Media.  We are actively working on a permanent fix to enhance compatibility. In the meantime, apply the following guidelines:
>
>* For Dynamic Media Scene7 URLs: Append `?bfc=on` to the image URL. This enables automatic format negotiation, ensuring the most compatible image format is delivered based on the client's capabilities.
>
>* For Dynamic Media with Open API: Use the `.avif` format. This format includes built-in fallback mechanisms to deliver a compatible format when necessary.
>
-->

Pour ajouter une ressource Adobe Experience Manager à votre contenu HTML, procédez comme suit :

1. Faites glisser et déposez un **[!UICONTROL composant HTML]** dans votre contenu.

1. Sélectionnez **[!UICONTROL Afficher le code source]**.

   ![](assets/dynamic-media-1.png)

1. Dans le menu **[!UICONTROL Modifier le code HTML]**, accédez à **[!UICONTROL Ressources]**, puis cliquez sur **[!UICONTROL Ouvrir le sélecteur de ressources]**.

   Vous pouvez également copier et coller l’URL de la ressource.

   ![](assets/dynamic-media-2.png)

1. Parcourez vos ressources AEM et sélectionnez celle que vous souhaitez ajouter à votre contenu.

1. Ajustez les paramètres de l’image (par exemple, la hauteur, la largeur, la rotation, le basculement, la luminosité, la teinte, etc.) selon les exigences de vos ressources.

   Pour obtenir la liste complète des paramètres d’image qui peuvent être ajoutés à l’URL, consultez la [documentation d’Experience Manager](https://experienceleague.adobe.com/fr/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/c-command-reference){target="_blank"}.

   ![](assets/dynamic-media-3.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Votre contenu comprend désormais un média dynamique. Toutes les mises à jour effectuées dans Experience Manager apparaîtront automatiquement dans Journey Optimizer.

## Personnaliser la superposition de texte {#text-overlay}

Personnalisez facilement n’importe quel média dynamique en remplaçant la superposition de texte existante par un texte de votre choix, pour simplifier les mises à jour et la personnalisation.

Par exemple, à l’aide de la fonctionnalité d’expérimentation, vous pouvez mettre à jour la superposition de texte existante en la remplaçant par un texte différent pour chaque traitement. Ainsi, chaque ouverture de message est personnalisée pour chaque profil.

![](assets/dynamic-media-layout-1.png)

>[!AVAILABILITY]
>
>La **personnalisation de la superposition de texte** est uniquement disponible dans Dynamic Media en [mode Scene7](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/assets/dynamic/config-dms7){target="_blank"}. Comme le mode Scene7 n’est pas accessible pour les clientes et clients du secteur de la santé, le contenu est rendu à l’aide d’une copie binaire de l’image Journey Optimizer. Pour toute exception, veuillez contacter votre représentant ou représentante Adobe.

Pour personnaliser votre superposition de texte, procédez comme suit :

1. Faites glisser et déposez un **[!UICONTROL composant HTML]** dans votre contenu.

1. Sélectionnez **[!UICONTROL Afficher le code source]**.

1. Dans le menu **[!UICONTROL Modifier le code HTML]**, accédez à **[!UICONTROL Ressources]**, puis **[!UICONTROL Ouvrir le sélecteur de ressources]**.

   Vous pouvez également simplement copier et coller l’URL de vos ressources.

1. Parcourez vos ressources AEM et sélectionnez celle que vous souhaitez ajouter à votre contenu.

1. Remplacez la superposition par le texte souhaité.

   ![](assets/do-not-localize/dynamic_media_layout.gif)

1. Mettez à jour les paramètres d’image suivants :

   * **Layer** : saisissez l’élément de base où est placé le texte.
   * **Taille** : mettez à jour la taille de votre bloc de texte.
   * **TextAttr** : ajustez la taille de la police du texte.
   * **Pos** : définissez la position du texte sur l’image.

   >[!WARNING]
   >
   >Le paramètre Layer est requis pour mettre à jour le média dynamique.

   ![](assets/dynamic-media-layout-2.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Votre contenu inclut désormais la superposition de texte mise à jour.

![](assets/dynamic-media-layout-3.png)

## Ajouter et gérer votre modèle Dynamic Media {#dynamic-media-template}

Ajoutez facilement votre modèle Dynamic Media dans Journey Optimizer et mettez à jour votre contenu multimédia chaque fois que nécessaire. Vous pouvez désormais incorporer des champs de personnalisation dans vos médias, ce qui vous permet de créer du contenu plus personnalisé et plus attrayant dans Journey Optimizer.

En savoir plus sur le [modèle Dynamic Media](https://experienceleague.adobe.com/fr/docs/dynamic-media-classic/using/template-basics/quick-start-template-basics){target="_blank"}


>[!AVAILABILITY]
>
>Le **modèle Dynamic Media** est disponible exclusivement dans Dynamic Media en [mode Scene7](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/assets/dynamic/config-dms7). Comme le mode Scene7 n’est pas accessible pour les clientes et clients du secteur de la santé, le contenu ne sera pas rendu. Pour toute exception, contactez l’assistance Experience Manager.


### Avec le composant Image {#image-component}

Vous pouvez insérer votre modèle dynamique directement dans votre contenu à l’aide du composant Image :

1. Ouvrez votre campagne ou votre parcours et accédez à votre contenu.

1. Faites glisser et déposez un **composant Image** dans votre disposition.

   Pour plus d’informations sur le composant Image, consultez [cette page](../email/content-components.md).

   ![](assets/dynamic-media-template-1.png)

1. Parcourez vos ressources AEM et sélectionnez le modèle Dynamic Media que vous souhaitez ajouter à votre contenu.

   ![](assets/dynamic-media-template-2.png)

1. Dans les **paramètres d’image**, accédez aux paramètres de votre modèle Dynamic Media.

   Les champs disponibles dépendent des paramètres ajoutés lors de la [création du modèle](https://experienceleague.adobe.com/fr/docs/dynamic-media-classic/using/template-basics/creating-template-parameters#creating_template_parameters){target="_blank"} dans Adobe Experience Manager.

   ![](assets/dynamic-media-template-3.png)

1. Renseignez les différents champs et utilisez l’éditeur de personnalisation pour ajouter du contenu personnalisé. Vous pouvez utiliser n’importe quel attribut, tel que le nom du profil, la ville ou d’autres détails pertinents, pour créer une expérience plus personnalisée.

   Pour en savoir plus sur la personnalisation, consultez [cette page](../personalization/personalize.md).

   ![](assets/do-not-localize/dynamic_media_template.gif)

1. Le contenu conditionnel peut être appliqué au composant Dynamic Media pour générer différentes variantes de contenu. [En savoir plus](../personalization/dynamic-content.md)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Une fois que vous avez effectué vos tests et validé le contenu, vous pouvez envoyer votre message à votre audience.

### Avec le composant HTML {#html-component}

Vous pouvez insérer votre modèle dynamique directement dans votre contenu à l’aide du composant HTML :

1. Ouvrez votre campagne ou votre parcours et accédez à votre contenu.

1. Faites glisser et déposez un **composant HTML** dans votre disposition.

   ![](assets/dynamic-media-template-4.png)

1. Sélectionnez **[!UICONTROL Afficher le code source]**.

   ![](assets/dynamic-media-template-5.png)

1. Dans le menu **[!UICONTROL Modifier le code HTML]**, accédez à **[!UICONTROL Ressources]**, puis **[!UICONTROL Ouvrir le sélecteur de ressources]**.

   Vous pouvez également simplement copier et coller l’URL de vos ressources.

1. Ajustez les paramètres de texte de l’image selon vos besoins pour répondre aux exigences des ressources.

   ![](assets/do-not-localize/dynamic_media_template_html.gif)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Une fois que vous avez effectué vos tests et validé le contenu, vous pouvez envoyer votre message à votre audience.

<!--
## Personalization with Text Overlay

Easily customize any dynamic media by replacing the existing text overlay with new text of your choice, allowing for seamless updates and personalization.

In this example, our goal is to update the existing text overlay by replacing it with a new validity date and adding a personalization block, ensuring it is customized for each profile when they open their messages.

1. Drag and drop an **[!UICONTROL HTML component]** into your content.

1. Select **[!UICONTROL Show the source code]**.

1. From the **[!UICONTROL Edit HTML]** menu, access **[!UICONTROL Assets]** then **[!UICONTROL Open asset selector]**.

    You can also simply copy and paste your assets URL.

1. Browse through your AEM assets and select the one you want to add to your content.

1. Replace the overlay with the desired text.

    Here we change the validity date from 31st December 2024 to the 1st July 2025.

1. Add the required personalization fields to your image.

1. Click **[!UICONTROL Save]**.

Your content now includes your updated text overlay and personalization.

## Add Dynamic media conditional content

Enable conditional content in your dynamic media to better target your audience and deliver a more personalized experience.

1. Drag and drop an **[!UICONTROL HTML component]** into your content.

1. Select **[!UICONTROL Show the source code]**.

1. From the **[!UICONTROL Edit HTML]** menu, access **[!UICONTROL Assets]** then **[!UICONTROL Open asset selector]**.

    You can also simply copy and paste your assets URL.

1. Browse through your AEM assets and select the one you want to add to your content.

1. Once your dynamic media is inserted to your content, select **[!UICONTROL Enable conditional]** content from your HTML component toolbar to create your different user experiences. 

1. From the Variant - 1, click **[!UICONTROL Select condition]** to fine tune your audience.

1. Choose your condition or create a new one if needed and click **[!UICONTROL Select]**.

    [Learn more about conditions](../personalization/create-conditions.md)

1. Select your **[!UICONTROL Component]** and access the **[!UICONTROL Settings]** menu.

1. In the **[!UICONTROL Custom Attributes]** menu, populate the Dynamic Media text and personalization fields to customize the content for your audience.

-->

## Vidéo pratique {#video}

Découvrez comment intégrer Adobe Experience Manager Dynamic Media à Adobe Journey Optimizer pour activer la mise à jour de contenu en temps réel et la personnalisation.

Ce tutoriel explique comment modifier des images directement dans AJO, ajouter des superpositions de texte à l’aide du mode HTML, créer des modèles Dynamic Media dans AEM à des fins d’hyper-personnalisation et personnaliser des campagnes en adaptant le contenu à différents segments d’audience. Cette intégration permet aux spécialistes du marketing de créer efficacement des campagnes attrayantes et personnalisées sans passer d’une application à l’autre.

>[!VIDEO](https://video.tv.adobe.com/v/3463784/?captions=fre_fr&learn=on&enablevpops=&autoplay=true)

