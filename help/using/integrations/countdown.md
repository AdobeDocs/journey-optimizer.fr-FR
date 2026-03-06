---
solution: Journey Optimizer
product: journey optimizer
title: Dynamic Media
description: Utiliser Dynamic Media avec Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4c1d39c4-3154-4bec-ac3c-c2ead7164d69
source-git-commit: f212a2178e83283d4755da5483d7c11ba4df183f
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 2%

---

# Insérer le compteur de décompte {#countdown}

Créez une urgence et optimisez les conversions avec les compteurs de compte à rebours Dynamic Media qui se mettent à jour en temps réel lorsque les destinataires ouvrent vos e-mails. Cette fonctionnalité est idéale pour les ventes flash, les offres à durée limitée et les promotions sensibles au facteur temps.

Par exemple, en tant que spécialiste marketing pour une marque de vente au détail, vous réalisez une vente flash de 48 heures. En utilisant le compte à rebours dans vos e-mails promotionnels :

* Les destinataires qui ouvrent immédiatement le dossier voient « 47 heures restantes »
* Les destinataires qui ouvrent 24 heures plus tard voient « 23 heures restantes »
* Les destinataires qui ouvrent après la fin de la vente voient « Time&#39;s up ! »

Pour plus d’informations sur l’ajout de minuteries de décompte à votre modèle Dynamic Media dans Adobe Experience Manager, reportez-vous [à ce document](assets/do-not-localize/countdown.pdf).


1. Dans **[!DNL Adobe Experience Manager]**, créez un modèle Dynamic Media et ajoutez-y un composant Compte à rebours .

   ![](assets/timer-1.png)

1. Dans **[!DNL Journey Optimizer]**, créez une campagne ou ouvrez une campagne existante, puis accédez au Designer Email.

1. Faites glisser et déposez un composant **HTML** ou **Asset** dans le contenu de votre e-mail.

1. Pointez sur le composant et cliquez sur **[!UICONTROL Afficher le code source]** (pour les composants HTML) ou **[!UICONTROL Parcourir]** (pour les composants Ressource).

   ![](assets/timer-2.png)

1. Dans le menu **[!UICONTROL Modifier HTML]**, accédez à **[!UICONTROL Assets]** et cliquez sur **[!UICONTROL Ouvrir le sélecteur de ressources]** pour parcourir et sélectionner votre modèle Dynamic Media publié.

   ![](assets/timer-3.png)

1. Activez l’expérience des pilules en activant Pilules . Cela améliore la lisibilité en masquant les chemins d’accès aux attributs longs.

   ![](assets/timer-6.png)

1. Dans le menu **[!UICONTROL Attributs personnalisés]**, configurez les paramètres d’URL personnalisables selon les besoins de votre modèle.

   Cliquez sur **[!UICONTROL Enregistrer]** lorsque vous avez terminé.

   ![](assets/timer-4.png)

1. Vous pouvez également accéder aux paramètres du modèle Dynamic Media en sélectionnant la ressource dans le Designer d’e-mail, puis en accédant au menu **[!UICONTROL Paramètres]**.

   Configurez les éléments suivants :

   * **Texte de bannière** : texte affiché avec votre minuteur
   * **Heure de fin** : date et heure d’expiration du décompte. Saisissez l’heure en GMT (heure de Greenwich) uniquement. Le système n&#39;accepte pas d&#39;autres fuseaux horaires.
   * **Texte de secours** : message affiché après la fin du minuteur

   ![](assets/timer-5.png)

1. Cliquez sur **[!UICONTROL Aperçu]** pour afficher le minuteur avec les mises à jour du compte à rebours en temps réel et vérifier votre configuration.

Lorsque les destinataires ouvrent l’e-mail, ils voient le temps précis restant pour votre vente flash. S’ils rouvrent l’e-mail ultérieurement, le compte à rebours est automatiquement mis à jour pour refléter le temps restant actuel. Après la date de fin, le message par défaut s’affiche automatiquement.
