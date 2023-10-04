---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation de fragments d’expression
description: Découvrez comment utiliser des fragments d’expression dans le [!DNL Journey Optimizer] Éditeur d’expression.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, éditeur, bibliothèque, personnalisation
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: 623aa2ee317553eaebfb16c350a69672de2866a1
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 10%

---

# Utilisation des fragments d’expression {#use-expression-fragments}

Lorsque vous utilisez l’éditeur d’expression, vous pouvez exploiter tous les fragments d’expression qui ont été créés ou enregistrés dans l’environnement de test actuel.

Découvrez comment créer et gérer des fragments dans [cette section](../content-management/fragments.md).

➡️ [Découvrez comment gérer, créer et utiliser des fragments dans cette vidéo](../content-management/fragments.md#video-fragments)

## Utilisation d’un fragment d’expression {#use-expression-fragment}

Pour ajouter des fragments d’expression à votre contenu, procédez comme suit.

1. Ouvrez le [Editeur d&#39;expression](personalization-build-expressions.md) et sélectionnez la variable **[!UICONTROL Fragments]** dans le volet de gauche.

   ![](assets/expression-fragments-pane.png)

   La liste affiche tous les fragments d’expression qui ont été créés ou enregistrés en tant que fragments sur l’environnement de test actuel. [En savoir plus](../content-management/fragments.md#create-expression-fragment)

   >[!NOTE]
   >
   >Les fragments sont triés par date de création : les fragments d’expression récemment ajoutés sont affichés en premier dans la liste.

1. Vous pouvez également actualiser la liste.

   >[!NOTE]
   >
   >Si certains fragments ont été modifiés ou ajoutés pendant que vous modifiez votre contenu, la liste est mise à jour avec les dernières modifications.

1. Cliquez sur l’icône + en regard d’un fragment d’expression pour insérer l’ID de fragment correspondant dans l’éditeur.

   ![](assets/expression-fragment-add.png)

   Une fois l’identifiant du fragment ajouté, si vous ouvrez le fragment d’expression correspondant et [modifier](../content-management/fragments.md#edit-fragments) depuis l’interface , les modifications sont synchronisées. Ils sont automatiquement propagés à tous **[!UICONTROL Version préliminaire]** parcours/campagnes contenant cet identifiant de fragment.

   >[!NOTE]
   >
   >Les modifications ne sont pas propagées au contenu utilisé dans **[!UICONTROL En direct]** parcours ou campagnes.

1. Cliquez sur le bouton **[!UICONTROL Autres actions]** en regard d’un fragment.

1. Dans le menu contextuel qui s’ouvre, sélectionnez **[!UICONTROL Afficher le fragment]** pour obtenir plus d’informations sur ce fragment. La variable **[!UICONTROL Identifiant du fragment]** s’affiche également et peut être copié à partir de cet emplacement.

   ![](assets/expression-fragment-view.png)

1. Vous pouvez ouvrir le fragment d’expression dans une autre fenêtre pour modifier son contenu et ses propriétés, à l’aide de la fonction **[!UICONTROL Ouvrir le fragment]** dans le menu contextuel ou à partir de l’ **[!UICONTROL Informations sur le fragment]** volet. [Découvrez comment modifier un fragment](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. Vous pouvez ensuite personnaliser et valider votre contenu comme vous le faites habituellement à l’aide de toutes les fonctionnalités de personnalisation et de création de [Editeur d&#39;expression](personalization-build-expressions.md).

>[!NOTE]
>
>Si vous créez un fragment d’expression qui contient plusieurs sauts de ligne et l’utilisez dans [SMS](../sms/create-sms.md#sms-content) ou [push](../push/design-push.md) , les sauts de ligne sont conservés. Veillez donc à tester vos [SMS](../sms/send-sms.md) ou [push](../push/send-push.md) avant de l’envoyer.

## Rompre l’héritage {#break-inheritance}

Lors de l’ajout d’un ID de fragment à l’éditeur d’expression, les modifications apportées au fragment d’expression d’origine sont synchronisées.

Cependant, vous pouvez également coller le contenu d’un fragment d’expression dans l’éditeur. Dans le menu contextuel, sélectionnez **[!UICONTROL Coller le fragment]** pour insérer ce contenu.

![](assets/expression-fragment-paste.png)

Dans ce cas, l’héritage du fragment d’origine est rompu. Le contenu du fragment est copié dans l’éditeur et les modifications ne sont plus synchronisées.

Il devient un élément autonome qui n’est plus lié au fragment d’origine. Vous pouvez le modifier comme tout autre élément de votre code.

