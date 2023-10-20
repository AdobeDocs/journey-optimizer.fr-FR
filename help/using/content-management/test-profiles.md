---
title: Sélectionner des profils de test
description: Découvrez comment sélectionner des profils de test pour prévisualiser et tester le contenu.
feature: Preview, Proofs
role: User
level: Beginner
source-git-commit: 6da7f4c8caa5a0a6cfda1e90d0c6cd4787c6afca
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 42%

---

# Sélectionner des profils de test {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="Utiliser des profils de test pour vérifier votre contenu"
>abstract="Utilisez des profils de test pour prévisualiser et tester votre contenu. Si vous avez ajouté des champs personnalisés, vous pouvez vérifier leur affichage à l&#39;aide des données de profil de test."

Avant de prévisualiser ou de tester votre contenu, vous devez d&#39;abord sélectionner des profils de test, c&#39;est-à-dire des destinataires supplémentaires qui ne correspondent pas aux critères de ciblage définis. [Découvrez comment créer des profils de test](../audience/creating-test-profiles.md)

Pour sélectionner des profils de test, procédez comme suit :

1. Dans l&#39;écran d&#39;édition du contenu de votre message ou dans le Concepteur d&#39;email, cliquez sur le bouton **[!UICONTROL Simulation du contenu]** bouton .

1. Cliquez sur le bouton **[!UICONTROL Gestion des profils de test]** puis sélectionnez l’espace de noms à utiliser pour identifier les profils de test en cliquant sur le bouton **[!UICONTROL Espace de noms d’identité]** icône de sélection. [En savoir plus sur les espaces de noms d’identité Adobe Experience Platform](../audience/get-started-identity.md).

   Dans l’exemple ci-dessous, nous utilisons la méthode **Email** espace de noms.

   ![](../email/assets/previewselect-namespace.png)

1. Utilisez le champ de recherche pour trouver l&#39;espace de noms, sélectionnez-le et cliquez sur **[!UICONTROL Sélectionner]**.

   ![](../email/assets/preview-email-namespace.png)

1. Dans le champ **[!UICONTROL Valeur d’identité]**, saisissez la valeur (l’adresse e-mail ici) permettant d’identifier le profil de test et cliquez sur **[!UICONTROL Ajouter un profil]**.

   <!--![](assets/preview-identity-value.png)-->

1. Si vous avez ajouté une personnalisation à votre message, ajoutez d’autres profils afin de pouvoir tester différentes variantes du message en fonction des données du profil. Une fois ajoutés, les profils sont répertoriés sous les champs sélectionnés.

   ![](../email/assets/preview-profile-list.png)

   En fonction des éléments de personnalisation du message, cette liste affiche les données de chaque profil de test dans les colonnes associées.
