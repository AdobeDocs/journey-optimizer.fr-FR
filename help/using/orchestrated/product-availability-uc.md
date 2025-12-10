---
solution: Journey Optimizer
product: journey optimizer
title: Informer les utilisateurs de la disponibilité du produit
description: Informer les utilisateurs de la disponibilité du produit
feature: Use Cases
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 3%

---

# Informer les utilisateurs de la disponibilité du produit {#product-availability-uc}

>[!BEGINSHADEBOX]

Ce cas pratique illustre l’envoi à plusieurs niveaux : génération d’un e-mail distinct pour chaque élément de liste de souhaits à l’aide de l’adresse e-mail stockée avec l’élément individuel plutôt que de l’enregistrement du destinataire. Cela permet aux clients de recevoir des notifications distinctes pour chaque produit de leur liste de souhaits, même s’ils utilisent des adresses e-mail différentes pour différents éléments.

>[!ENDSHADEBOX]

![](assets/notify-6.png){zoomable="yes"}

Concevez une notification de retour en stock pour informer les clients lorsque des éléments de leur liste de souhaits sont à nouveau disponibles. Ce message permet de réengager les clients intéressés et les encourage à terminer leur achat pendant que le stock est réapprovisionné.

1. Commencez par mettre en place une nouvelle campagne visant spécifiquement le réengagement de la liste de souhaits. Cela garantit que votre messagerie se concentre sur les clients qui ont déjà affiché leur intention d’achat en enregistrant les produits sur leur liste de souhaits.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Renseignez vos **[!UICONTROL paramètres de campagne]** tels que le nom, la description, les dates de début et de fin de la campagne et les balises pertinentes.

1. Ajoutez une activité **[!UICONTROL Créer une audience]** avec une liste de souhaits comme **[!UICONTROL dimension de ciblage]**.

   ![](assets/notify-1.png){zoomable="yes"}

1. Ajoutez votre condition pour n’inclure que les listes de souhaits créées au cours des 36 derniers mois.

   ![](assets/notify-2.png){zoomable="yes"}

1. Ajoutez une activité **[!UICONTROL Modifier la dimension]** pour passer des listes de souhaits au jeu de clients correspondant pour le ciblage.

   ![](assets/notify-3.png){zoomable="yes"}

1. Après avoir démarré le mode brouillon, prévisualisez l’audience avec les détails de la liste de souhaits. Pour obtenir des informations plus détaillées, cliquez sur un résultat de sortie et sélectionnez **[!UICONTROL Prévisualiser les résultats]**.

   Ici, les données affichent à la fois les destinataires et leurs éléments de liste de souhaits. Certains clients disposent de plusieurs éléments de liste de souhaits et, par le biais d’un envoi à plusieurs niveaux, reçoivent un e-mail distinct pour chaque élément. Dans certains cas, les clients utilisent des adresses e-mail différentes pour des demandes de réapprovisionnement distinctes.

   ![](assets/notify-4.png){zoomable="yes"}

1. Pour pouvoir envoyer un e-mail distinct pour chaque élément, assurez-vous que [votre configuration d’e-mail](../orchestrated/target-dimension.md) est définie avec `Recipients - email` comme **[!UICONTROL Profile Target Dimension]** et `Wishlistitems` comme une dimension **[!UICONTROL Secondaire]**.

   Ensuite, dans le menu **[!UICONTROL Adresse d’exécution]**, sélectionnez `wishlist.email` comme **[!UICONTROL dimension Secondaire]**. Chaque élément de liste de souhaits déclenche un e-mail distinct, en utilisant l’adresse e-mail stockée dans les données de liste de souhaits comme dimension secondaire.

   ![](assets/notify-5.png){zoomable="yes"}

1. Ajoutez une activité **[!UICONTROL E-mail]** pour créer un message de disponibilité du produit. Cliquez sur **[!UICONTROL Modifier le contenu]** pour commencer à concevoir votre contenu.

   ➡️ [En savoir plus sur la personnalisation des emails](../email/content-from-scratch.md)

   ![](assets/notify-7.png){zoomable="yes"}

1. Une fois votre campagne testée et prête, cliquez sur **[!UICONTROL Publier]** pour la mettre en ligne.

Avec cette campagne orchestrée, le client reçoit un e-mail distinct pour chacun des éléments de sa liste de souhaits. Chaque message est envoyé à l’adresse e-mail spécifique associée à cette liste de souhaits, avec un contenu personnalisé tiré des détails de cet élément de liste de souhaits particulier.

