---
solution: Journey Optimizer
product: journey optimizer
title: Ajout d’offres personnalisées
description: Découvrez comment ajouter des offres personnalisées à vos messages
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 100%

---

# Ajout d&#39;offres personnalisées {#deliver-personalized-offers}

Dans les e-mails [!DNL Journey Optimizer], vous pouvez insérer des décisions qui utiliseront le moteur de décision d’offre afin de sélectionner la meilleure offre à proposer à vos clients.

Par exemple, vous pouvez ajouter une décision qui affichera dans votre email une offre de remise spéciale qui variera en fonction du niveau de fidélité du destinataire.

Pour plus d’informations sur la façon de créer et gérer des offres, reportez-vous à [cette section](../offers/get-started/starting-offer-decisioning.md).

Pour obtenir un **exemple complet** montrant comment configurer des offres, les utiliser dans une décision et exploiter cette décision dans un e-mail, consultez [cette section](../offers/offers-e2e.md#insert-decision-in-email).

➡️ [Découvrez comment ajouter des offres en tant que personnalisation dans cette vidéo](#video-offers)

## Insertion d’une décision dans un e-mail {#insert-offers}

>[!CAUTION]
>
>Avant de commencer, vous devez [définir une décision d&#39;offre](../offers/offer-activities/create-offer-activities.md).

Pour insérer une décision dans un email, procédez comme suit :

1. Créez votre email, puis ouvrez le Concepteur d&#39;email pour configurer son contenu.

1. Ajoutez un composant de contenu **[!UICONTROL Décision d&#39;offre]**.

   ![](assets/deliver-offer-component.png)

   Découvrez comment utiliser les composants de contenu dans [cette section](content-components.md).

1. L&#39;onglet **[!UICONTROL Décision d&#39;offre]** s&#39;affiche dans la palette de droite. Cliquez sur **[!UICONTROL Sélectionner une décision d&#39;offre]**.

   ![](assets/deliver-offer-tab.png)

1. Dans la fenêtre qui s&#39;affiche, sélectionnez l&#39;emplacement correspondant aux offres que vous souhaitez afficher.

   Les [emplacements](../offers/offer-library/creating-placements.md) sont des conteneurs utilisés pour présenter vos offres. Dans cet exemple, nous utiliserons l’emplacement « image en haut de l&#39;e-mail ». Cet emplacement a été créé dans la bibliothèque des offres pour afficher les offres de type image situées en haut des messages.

1. Les décisions correspondant à l’emplacement sélectionné s’affichent. Sélectionnez la décision à utiliser dans le composant de contenu, puis cliquez sur **[!UICONTROL Ajouter]**.

   >[!NOTE]
   >
   >Seules les décisions compatibles avec l&#39;emplacement sélectionné s&#39;affichent dans la liste. Dans cet exemple, une seule activité d&#39;offre correspond à l&#39;emplacement « image en haut de l&#39;e-mail ».

   ![](assets/deliver-offer-placement.png)

L&#39;activité d&#39;offre est alors ajoutée au composant.

Une fois vos modifications enregistrées, vos offres sont prêtes à être affichées pour les profils pertinents lors de l’envoi du message dans le cadre d’un parcours.

>[!NOTE]
>
>Lors de la mise à jour dʼune offre, dʼune offre de secours, dʼune collection d’offres ou dʼune décision d’offre, directement ou indirectement référencée dans un message, les mises à jour sont automatiquement répercutées dans le message correspondant.

## Prévisualisation des offres dans un e-mail {#preview-offers-in-email}

Vous pouvez prévisualiser les différentes offres qui font partie de la décision ajoutée à l&#39;e-mail en utilisant la section **[!UICONTROL Offres]** ou les flèches des composants de contenu.

![](assets/deliver-offer-preview.png)

Pour afficher les différentes offres qui font partie de la décision avec un profil client, procédez comme suit.

1. Cliquez sur **[!UICONTROL Aperçu]**.

   ![](assets/deliver-offer-preview-button.png)

   >[!NOTE]
   >
   >Vous devez disposer de profils de test pour pouvoir prévisualiser vos messages. Découvrez comment [créer un profil de test](../segment/creating-test-profiles.md).

1. Pour choisir l&#39;espace de noms à utiliser pour identifier les profils de test, sélectionnez **[!UICONTROL E-mail]** dans le champ **[!UICONTROL Espace de noms d&#39;identité]**.

   >[!NOTE]
   >
   >Dans cet exemple, nous utiliserons l&#39;espace de noms **E-mail**. Apprenez-en davantage sur les espaces de noms d&#39;identité d&#39;Adobe Experience Platform [dans cette section](../segment/get-started-identity.md).

1. Dans la liste des espaces de noms d&#39;identité, sélectionnez **[!UICONTROL E-mail]** et cliquez sur **[!UICONTROL Sélectionner]**.

1. Dans le champ **[!UICONTROL Valeur d&#39;identité]**, saisissez la valeur pour identifier le profil de test. Dans cet exemple, saisissez l&#39;adresse e-mail d&#39;un profil de test.

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

1. Ajoutez d&#39;autres profils afin de pouvoir tester différentes variantes du message en fonction des données de profil.

   ![](assets/deliver-offer-test-profiles.png)

1. Cliquez sur l&#39;onglet **[!UICONTROL Prévisualisation]** pour tester votre message.

1. Sélectionnez un profil de test. L&#39;offre correspondant au profil sélectionné (une femme) s&#39;affiche.

   ![](assets/deliver-offer-test-profile-female-preview.png)

1. Sélectionnez d&#39;autres profils de test pour prévisualiser le contenu des e-mails pour chaque variante de votre message. Dans le contenu du message, l&#39;offre correspondant au profil de test sélectionné (désormais un homme) s&#39;affiche maintenant.

   ![](assets/deliver-offer-test-profile-male-preview.png)

Pour en savoir plus sur les étapes détaillées afin de vérifier la prévisualisation du message, consultez [cette section](#preview-your-messages).

## Vidéo pratique{#video-offers}

Découvrez comment ajouter un composant de gestion des décisions aux messages dans [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)

