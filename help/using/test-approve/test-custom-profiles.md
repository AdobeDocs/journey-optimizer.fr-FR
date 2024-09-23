---
solution: Journey Optimizer
product: journey optimizer
title: Test de votre contenu à l’aide de profils personnalisés
description: Découvrez comment prévisualiser votre contenu et envoyer des bons à tirer à l’aide de profils personnalisés.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Version bêta"
hide: true
hidefromtoc: true
source-git-commit: 6229f295b961b0535139b64928216e40c3759947
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 2%

---


# Test de votre contenu à l’aide de profils personnalisés {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simulation à l’aide de profils personnalisés"
>abstract="Dans cet écran, vous pouvez prévisualiser votre contenu et envoyer des bons à tirer tout en empruntant l’identité de profils personnalisés que vous pouvez charger à partir d’un fichier CSV ou ajouter manuellement depuis cet écran."

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement disponible en version bêta pour les utilisateurs sélectionnés uniquement.
>
>Les rapports d&#39;inbox rendering et de spam ne sont pas disponibles dans l&#39;expérience actuelle. Pour utiliser ces fonctionnalités, cliquez sur le bouton **[!UICONTROL Simuler le contenu]** de votre contenu pour accéder à l’interface utilisateur héritée.

L’outil d’optimisation des parcours vous permet de prévisualiser et de tester votre contenu à l’aide de profils personnalisés que vous pouvez charger à partir d’un fichier CSV ou ajouter manuellement lors de la simulation de votre contenu.

Pour accéder à cette expérience, cliquez sur le bouton **[!UICONTROL Simuler le contenu]** et sélectionnez **[!UICONTROL Simuler avec CSV(Beta)]**.

Cet écran vous permet de sélectionner les profils à utiliser pour prévisualiser votre contenu et envoyer des bons à tirer. Tous les attributs utilisés dans votre contenu pour la personnalisation sont automatiquement détectés par le système et peuvent être utilisés pour vos tests.

Les principales étapes pour tester votre contenu sont les suivantes :

1. Ajoutez des profils personnalisés, en chargeant un fichier CSV ou en les ajoutant un par un manuellement. [Découvrez comment ajouter des profils personnalisés](#profiles)
1. Vérifiez l&#39;aperçu de votre contenu à l&#39;aide des profils ajoutés. [Découvrez comment prévisualiser votre contenu](#preview)
1. Envoyez jusqu’à 10 bons à tirer aux adresses électroniques tout en empruntant les profils personnalisés de votre choix. [Découvrir comment envoyer des BAT](#proofs)


## Ajout de profils personnalisés {#profiles}

Vous pouvez ajouter des profils personnalisés pour tester votre contenu à l’aide d’un fichier CSV ou manuellement :

* Pour charger des profils à partir d’un fichier CSV, cliquez sur le lien **[!UICONTROL Télécharger le modèle]** pour récupérer un modèle de fichier CSV. Ces modèles incluent une colonne pour chaque attribut de personnalisation utilisé dans votre contenu.

  Renseignez le fichier CSV, puis cliquez sur le **[!UICONTROL Télécharger les exemples de profils]** pour le charger afin de tester votre contenu.

* Pour ajouter manuellement un profil, cliquez sur le bouton **[!UICONTROL Créer un exemple de profil]** et renseignez les informations du profil. Un champ s’affiche pour chaque attribut de personnalisation utilisé dans votre contenu.

  ![](assets/simulate-custom-add.png)

Une fois les profils sélectionnés, une zone s’affiche pour chaque profil sur le côté gauche de l’écran. Vous pouvez utiliser ces profils pour prévisualiser votre contenu et envoyer des bons à tirer.

## Prévisualiser votre contenu à l’aide de profils personnalisés {#preview}

Pour prévisualiser votre contenu à l&#39;aide de l&#39;un des profils, cochez la case correspondante afin de mettre à jour l&#39;aperçu du contenu dans la section droite avec les informations renseignées pour ce profil.

Vous pouvez supprimer une zone à tout moment à l’aide du bouton représentant des points de suspension dans le coin supérieur droit et en sélectionnant **[!UICONTROL Supprimer]**. Pour modifier les informations d’un profil, cliquez sur le bouton représentant des points de suspension et sélectionnez **[!UICONTROL Modifier]**.

![](assets/simulate-custom-boxes.png)

## Envoyer des BAT {#proofs}

Journey Optimizer permet d&#39;envoyer des BAT à des adresses email tout en empruntant l&#39;identité d&#39;un ou plusieurs profils personnalisés que vous avez ajoutés à l&#39;écran de la simulation. Les étapes sont les suivantes :

1. Vérifiez que des profils personnalisés ont été ajoutés pour tester votre contenu et cliquez sur le bouton **[!UICONTROL Envoyer le bon à tirer]** .

1. Dans le champ **[!UICONTROL Destinataires]**, saisissez l&#39;adresse email à laquelle vous souhaitez envoyer le BAT, puis cliquez sur **[!UICONTROL Ajouter]**. Répétez l’opération pour envoyer le BAT à des adresses email supplémentaires. Vous pouvez ajouter jusqu’à 10 destinataires de BAT.

1. Dans la section inférieure de l&#39;écran, sélectionnez les profils personnalisés que vous souhaitez incarner dans le BAT. Vous pouvez sélectionner plusieurs profils, auquel cas l&#39;email contiendra autant de BAT que les profils sélectionnés.

   ![](assets/simulate-custom-proofs.png)

1. Cliquez sur le bouton **[!UICONTROL Envoyer le bon à tirer]** pour commencer à envoyer le bon à tirer.

Vous pouvez suivre l’envoi à tout moment en cliquant sur le bouton **[!UICONTROL Afficher les bons à tirer]** dans l’écran de simulation de contenu.

![](assets/simulate-custom-sent-proofs.png)
