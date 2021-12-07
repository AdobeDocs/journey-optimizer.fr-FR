---
title: Concevoir une landing page
description: Découvrez comment concevoir le contenu d’une landing page dans Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: c61b8d80-17e1-4fdd-a739-efcee032dc23
source-git-commit: 88b037e079a46e10f7ee4715e78e5edc5a34a6ce
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 3%

---

# Concevoir le contenu de la landing page {#design-lp-content}

Pour commencer à créer du contenu pour votre landing page [Principale page](create-lp.md#configure-primary-page) ou [subpage](create-lp.md#configure-subpages), placez le pointeur de la souris sur le contenu de la Principale page, puis cliquez sur **[!UICONTROL Ouvrir Designer]**. Vous pouvez également cliquer sur le bouton correspondant dans la palette de droite.

![](../assets/lp_open-designer.png)

À partir de là, vous pouvez :

* **Concevoir entièrement votre landing page** par l’intermédiaire de l’interface du concepteur de contenu et utilisez des images à partir de [Adobe Experience Manager Assets Essentials](../assets-essentials.md). Découvrez comment concevoir votre contenu ou utiliser des modèles intégrés [dans cette section](../create-email-content.md).

* **Code ou coller un HTML brut** directement dans le concepteur de contenu. Découvrez comment coder votre propre contenu [dans cette section](../existing-content.md#import-raw-html-code).

* **Importez du contenu HTML existant** à partir d’un fichier ou d’un dossier .zip. Découvrez comment importer du contenu [dans cette section](../existing-content.md#import-html-content-from-file).

>[!NOTE]
>
>Le concepteur de contenu de page d’entrée est essentiellement similaire au concepteur d’email. En savoir plus sur [conception de contenu avec [!DNL Journey Optimizer]](../design-emails.md).

## Définition du contenu spécifique à une landing page {#define-lp-specific-content}

Pour définir un contenu spécifique qui permettra aux utilisateurs de sélectionner et d&#39;envoyer leurs choix depuis votre landing page, procédez comme suit.

1. Effectuez un glisser-déposer d&#39;une landing page spécifique **[!UICONTROL Formulaire]** de la palette gauche vers l’espace de travail principal.

   ![](../assets/lp_designer-form-component.png)

   >[!NOTE]
   >
   >Le **[!UICONTROL Formulaire]** ne peut être utilisé qu’une seule fois sur la même page.

1. Sélectionnez-le. Le **[!UICONTROL Contenu du formulaire]** s’affiche dans la palette de droite pour vous permettre de modifier les différents champs du formulaire.

   ![](../assets/lp_designer-form-content-options.png)

   >[!NOTE]
   >
   >Basculez vers le **[!UICONTROL Style de formulaire]** à tout moment pour modifier les styles du contenu de votre composant de formulaire. [En savoir plus](#define-lp-styles)

1. Dans la **[!UICONTROL Case à cocher 1]** , vous pouvez modifier le libellé correspondant à cette case à cocher.

1. Définissez si cette case à cocher permet d’exclure ou de désactiver les utilisateurs : acceptent-ils de recevoir des communications ou demandent-ils de ne plus être contactés ?

   ![](../assets/lp_designer-form-update.png)

1. Choisissez les options qui seront mises à jour parmi les trois options suivantes :

   ![](../assets/lp_designer-form-update-options.png)

   * **[!UICONTROL Liste d&#39;abonnements]**: Vous devez sélectionner la liste d&#39;abonnements qui sera mise à jour si le profil coche cette case. En savoir plus sur [listes d’abonnements](subscription-list.md).

      ![](../assets/lp_designer-form-subs-list.png)

   * **[!UICONTROL Canal (email)]**: L’opt-in ou l’opt-out s’applique à l’ensemble du canal. Par exemple, si un profil qui s’exclut possède deux adresses électroniques, les deux adresses seront exclues de toutes vos communications.

   * **[!UICONTROL Identité de courriel]**: L&#39;opt-in ou l&#39;opt-out ne s&#39;applique qu&#39;à l&#39;adresse email utilisée pour accéder à la landing page. Par exemple, si un profil comporte deux adresses électroniques, seule celle qui a été utilisée pour l’inclusion recevra les communications de votre marque.

1. Cliquez sur **[!UICONTROL Ajouter un champ]** > **[!UICONTROL Case à cocher]** pour ajouter une autre case à cocher. Répétez les étapes ci-dessus pour définir ses propriétés.

   ![](../assets/lp_designer-form-checkbox-2.png)

1. Une fois que vous avez ajouté toutes les cases à cocher de votre choix, cliquez sur **[!UICONTROL Appel à l’action]** pour développer la section correspondante. Il permet de définir le comportement du bouton dans la variable **[!UICONTROL Formulaire]** composant.

   ![](../assets/lp_designer-form-call-to-action.png)

1. Définissez ce qui se passe lorsque vous cliquez sur le bouton :

   * **[!UICONTROL URL de redirection]**: Saisissez l’URL de la page vers laquelle les utilisateurs seront redirigés.
   * **[!UICONTROL Texte de confirmation]**: Saisissez le texte de confirmation qui s’affichera.
   * **[!UICONTROL Lien vers une sous-page]**: Configurez une [subpage](create-lp.md#configure-subpages) et sélectionnez-le dans la liste déroulante qui s’affiche.

   ![](../assets/lp_designer-form-confirmation-action.png)

1. Définissez ce qui se passera lorsque vous cliquez sur le bouton en cas d’erreur :

   * **[!UICONTROL URL de redirection]**: Saisissez l’URL de la page vers laquelle les utilisateurs seront redirigés.
   * **[!UICONTROL Texte de l’erreur]**: Saisissez le texte de l’erreur qui s’affichera. Vous pouvez prévisualiser le texte de l’erreur lors de la définition de la variable [styles de formulaire](#define-lp-styles).

   * **[!UICONTROL Lien vers une sous-page]**: Configurez une [subpage](create-lp.md#configure-subpages) et sélectionnez-le dans la liste déroulante qui s’affiche.

   ![](../assets/lp_designer-form-error.png)

1. Si vous souhaitez effectuer des mises à jour supplémentaires lors de l’envoi du formulaire, sélectionnez **[!UICONTROL Inclusion]** ou **[!UICONTROL Exclusion]** et définissez si vous souhaitez mettre à jour une liste d’abonnements, le canal ou uniquement l’adresse électronique utilisée.

   ![](../assets/lp_designer-form-additionnal-update.png)

1. Enregistrez votre contenu et cliquez sur la flèche en regard du nom de la page pour revenir au [propriétés de page d’entrée](create-lp.md#configure-primary-page).

   ![](../assets/lp_designer-form-save.png)

<!--Will the name Email Designer be kept if you can also design LP with the same tool? > To modify in Messages section > content designer or Designer-->

## Définition des styles de formulaire de landing page {#define-lp-styles}

1. Pour modifier les styles du contenu de votre composant de formulaire, basculez à tout moment vers la fonction **[!UICONTROL Style de formulaire]** .

   ![](../assets/lp_designer-form-style.png)

1. Développez l’objet **[!UICONTROL Cases à cocher]** pour définir l’aspect des cases à cocher et du texte correspondant. Par exemple, vous pouvez ajuster la famille ou la taille de police, ainsi que la couleur de la bordure de la case à cocher.

   ![](../assets/lp_designer-form-style-checkboxes.png)

1. Développez l’objet **[!UICONTROL Boutons]** pour modifier l’aspect du bouton dans le formulaire du composant. Vous pouvez par exemple ajouter une bordure, éditer la couleur du libellé au survol ou ajuster l&#39;alignement du bouton.

   ![](../assets/lp_designer-form-style-buttons.png)

   Vous pouvez prévisualiser certains de vos paramètres, comme la couleur de l’étiquette du bouton lorsque vous survolez en utilisant la fonction **[!UICONTROL Aperçu]** bouton . En savoir plus sur le test des landing pages [here](create-lp.md#test).

   ![](../assets/lp_designer-form-style-buttons-preview.png)

1. Développez l’objet **[!UICONTROL Mettre en page le formulaire]** pour modifier les paramètres de mise en page, tels que la couleur d’arrière-plan, la marge intérieure ou la marge.

   ![](../assets/lp_designer-form-style-layout.png)

1. Développez l’objet **[!UICONTROL Erreur de formulaire]** pour ajuster l’affichage du message d’erreur qui s’affiche en cas de problème. Cochez l&#39;option correspondante pour prévisualiser le texte de l&#39;erreur sur le formulaire.

   ![](../assets/lp_designer-form-error-preview.png)

