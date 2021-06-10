---
title: Ajout d’offres personnalisées
description: Découvrez comment ajouter des offres personnalisées à vos messages
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: ht
source-wordcount: '272'
ht-degree: 100%

---

# Ajout d’offres personnalisées {#deliver-personalized-offers}

![](assets/do-not-localize/badge.png)

## À propos de la gestion des décisions {#about-offer-decisioning}

Avec [!DNL Journey Optimizer], vous pouvez insérer dans vos emails des décisions (précédemment connues sous le nom d&#39;activités d&#39;offre) qui utiliseront le moteur de décision d’offre afin de sélectionner la meilleure offre à proposer à vos clients.

Par exemple, vous pouvez ajouter une décision qui affichera dans votre email une offre de remise spéciale qui variera en fonction du niveau de fidélité du destinataire.

Pour plus d’informations sur la façon de créer et gérer des offres, reportez-vous à [cette section](offers/get-started/starting-offer-decisioning.md).

## Insérer une décision dans un email {#insert-offers}

Pour insérer une décision dans un email, procédez comme suit :

1. Créez votre email, puis ouvrez le Concepteur d&#39;email pour configurer son contenu.

1. Ajoutez un composant de contenu **[!UICONTROL Décision d&#39;offre]** (voir [Utiliser les composants de contenu](content-components.md)).

   ![](assets/deliver-offer-component.png)

1. Un onglet **[!UICONTROL Décision d&#39;offre]** est ajouté au composant. Cliquez sur **[!UICONTROL Ajouter une personnalisation - Décision d&#39;offre]** pour ajouter une activité d&#39;offre.

   ![](assets/deliver-offer-tab.png)

1. Sélectionnez l&#39;emplacement correspondant aux offres que vous souhaitez afficher.

   Les placements sont des conteneurs utilisés pour présenter vos offres. Dans cet exemple, nous utiliserons l’emplacement « image en haut de l&#39;email ». Cet emplacement a été créé dans la bibliothèque des offres pour afficher les offres de type image situées en haut des messages.

1. Sélectionnez l’activité d’offre à utiliser dans le composant de contenu, puis cliquez sur **[!UICONTROL Ajouter]**.

   >[!NOTE]
   >
   >Notez que seules les décisions compatibles avec l&#39;emplacement sélectionné s&#39;affichent dans la liste. Dans cet exemple, une seule activité d’offre correspond à l’emplacement « image en haut de l&#39;email ».

   ![](assets/deliver-offer-placement.png)

1. L’activité d’offre est alors ajoutée au composant. Vous pouvez prévisualiser les différentes offres qui font partie de la décision en utilisant la section **[!UICONTROL Offres]** ou les flèches des composants de contenu.

   ![](assets/deliver-offer-preview.png)
