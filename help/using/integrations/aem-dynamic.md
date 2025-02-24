---
solution: Journey Optimizer
product: journey optimizer
title: Dynamic Media
description: Utilisation de Dynamic Media avec Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
badge: label="Version bêta" type="Informative"
exl-id: 3e777cc5-a935-4e68-9de7-60b241e78f63
source-git-commit: 3a10f8440515bd569f9def6d15ac74d57427c1cf
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 2%

---

# Utiliser Dynamic Media {#aem-dynamic}

>[!AVAILABILITY]
>
>Cette intégration est disponible exclusivement pour les clients qui utilisent Dynamic Media Manager as a Cloud Service.

Le sélecteur de ressources prend désormais en charge Dynamic Media, ce qui vous permet de sélectionner et d’utiliser facilement des rendus Dynamic Media approuvés dans Journey Optimizer. Les modifications apportées aux ressources dans Adobe Experience Manager sont immédiatement répercutées dans votre contenu Journey Optimizer, ce qui garantit que les versions les plus récentes sont toujours utilisées sans nécessiter de mises à jour manuelles.

Pour en savoir plus sur Dynamic Media dans Adobe Experience Manager as a Cloud Service, consultez la [documentation Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media).

## Ajout et gestion de Dynamic Media

Améliorez et optimisez votre contenu pour n’importe quel écran ou navigateur en insérant Dynamic Media depuis Adobe Experience Manager as a Cloud Service directement dans votre contenu Journey Optimizer.  Vous pouvez ensuite redimensionner, recadrer, améliorer et effectuer d’autres réglages si nécessaire.

1. Effectuez un glisser-déposer d’un composant **[!UICONTROL HTML]** dans votre contenu.

1. Sélectionnez **[!UICONTROL Afficher le code source]**.

   ![](assets/dynamic-media-1.png)

1. Dans le menu **[!UICONTROL Modifier HTML]**, accédez à **[!UICONTROL Assets]** puis cliquez sur **[!UICONTROL Ouvrir le sélecteur de ressources]**.

   Vous pouvez également copier et coller l’URL de votre ressource.

   ![](assets/dynamic-media-2.png)

1. Parcourez vos ressources AEM et sélectionnez celle que vous souhaitez ajouter à votre contenu.

1. Ajustez les paramètres de l’image (par exemple, la hauteur, la largeur, la rotation, le basculement, la luminosité, la teinte, etc.) en fonction des besoins de votre ressource.

   Pour obtenir la liste complète des paramètres d’image pouvant être ajoutés à l’URL, consultez la [documentation Experience Manager](https://experienceleague.adobe.com/en/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/c-command-reference).

   ![](assets/dynamic-media-3.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Votre contenu comprend désormais Dynamic Media. Toutes les mises à jour effectuées dans Experience Manager apparaîtront automatiquement dans Journey Optimizer.

## Personnaliser la superposition de texte

Personnalisez facilement n’importe quel média dynamique en remplaçant la superposition de texte existante par un nouveau texte de votre choix, ce qui permet des mises à jour et une personnalisation transparentes.

Par exemple, à l’aide de la fonctionnalité d’expérimentation, vous pouvez mettre à jour la superposition de texte existante en la remplaçant par un texte différent pour chaque traitement, en vous assurant qu’elle est personnalisée pour chaque profil lorsqu’il ouvre ses messages.

![](assets/dynamic-media-layout-1.png)

1. Effectuez un glisser-déposer d’un composant **[!UICONTROL HTML]** dans votre contenu.

1. Sélectionnez **[!UICONTROL Afficher le code source]**.

1. Dans le menu **[!UICONTROL Modifier HTML]**, accédez à **[!UICONTROL Assets]** puis **[!UICONTROL Ouvrir le sélecteur de ressources]**.

   Vous pouvez également simplement copier et coller l’URL de vos ressources.

1. Parcourez vos ressources AEM et sélectionnez celle que vous souhaitez ajouter à votre contenu.

1. Remplacez le recouvrement par le texte souhaité.

   ![](assets/do-not-localize/dynamic_media_layout.gif)

1. Mettez à jour les paramètres des images :

   * **Calque** : saisissez l’élément de base où se trouve votre texte.
   * **Taille** : mettez à jour la taille de votre bloc de texte.
   * **TextAttr** : permet d’ajuster la taille de la police du texte.
   * **Pos** : permet de définir la position du texte dans l’image.

   >[!WARNING]
   >
   >Le paramètre Calque est requis pour mettre à jour Dynamic Media.

   ![](assets/dynamic-media-layout-2.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Votre contenu inclut désormais votre superposition de texte mise à jour.

![](assets/dynamic-media-layout-3.png)

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

    [Learn more on conditions](../personalization/create-conditions.md)

1. Select your **[!UICONTROL Component]** and access the **[!UICONTROL Settings]** menu.

1. In the **[!UICONTROL Custom Attributes]** menu, populate the Dynamic Media text and personalization fields to customize the content for your audience.

-->
