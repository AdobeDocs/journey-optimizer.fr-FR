---
solution: Journey Optimizer
product: journey optimizer
title: Informer les utilisateurs et les utilisatrices de la disponibilité d’un produit
description: Informer les utilisateurs et les utilisatrices de la disponibilité d’un produit
feature: Use Cases
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: ht
source-wordcount: '383'
ht-degree: 100%

---

# Informer les utilisateurs et les utilisatrices de la disponibilité d’un produit {#product-availability-uc}

>[!BEGINSHADEBOX]

Ce cas pratique illustre l’envoi à plusieurs niveaux : générer un e-mail distinct pour chaque élément de la liste de souhaits en utilisant l’adresse e-mail associée à chaque élément plutôt qu’au dossier du destinataire. Cela permet à la clientèle de recevoir des notifications distinctes pour chaque produit de sa liste de souhaits, même si elle utilise des adresses e-mail différentes pour différents éléments.

>[!ENDSHADEBOX]

![](assets/notify-6.png){zoomable="yes"}

Concevez une notification de retour en stock pour informer la clientèle lorsque des articles de sa liste de souhaits sont à nouveau disponibles. Ce message permet d’interagir de nouveau avec la clientèle intéressée et l’encourage à terminer ses achats alors que le stock est réapprovisionné.

1. Commencez par mettre en place une nouvelle campagne visant spécifiquement le réengagement de la liste de souhaits. Vous garantissez ainsi que vos messages se concentrent sur la clientèle qui a déjà affiché ses intentions d’achat en enregistrant les produits sur sa liste de souhaits.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Renseignez vos **[!UICONTROL paramètres de campagne]** tels que le nom, la description, les dates de début et de fin de la campagne et les balises pertinentes.

1. Ajoutez une activité **[!UICONTROL Créer une audience]** avec une liste de souhaits comme **[!UICONTROL Dimension de ciblage]**.

   ![](assets/notify-1.png){zoomable="yes"}

1. Ajoutez votre condition pour n’inclure que les listes de souhaits créées au cours des 36 derniers mois.

   ![](assets/notify-2.png){zoomable="yes"}

1. Ajoutez une activité **[!UICONTROL Changement de dimension]** pour passer des listes de souhaits au jeu de clientèle correspondant pour le ciblage.

   ![](assets/notify-3.png){zoomable="yes"}

1. Après avoir démarré le mode brouillon, prévisualisez l’audience avec les détails de la liste de souhaits. Pour obtenir des informations plus détaillées, cliquez sur un résultat de sortie et sélectionnez **[!UICONTROL Prévisualiser les résultats]**.

   Ici, les données affichent à la fois les destinataires et leurs articles de liste de souhaits. Certaines personnes ont plusieurs articles dans leur liste de souhaits et, par le biais d’un envoi à plusieurs niveaux, reçoivent un e-mail distinct pour chaque article. Dans certains cas, les personnes utilisent des adresses e-mail différentes pour des demandes de réapprovisionnement distinctes.

   ![](assets/notify-4.png){zoomable="yes"}

1. Pour pouvoir envoyer un e-mail distinct pour chaque article, assurez-vous que [votre configuration du canal e-mail](../orchestrated/target-dimension.md) est définie avec `Recipients - email` comme **[!UICONTROL dimension cible du profil]** et `Wishlistitems` comme dimension **[!UICONTROL secondaire]**.

   Ensuite, dans le menu **[!UICONTROL Adresse d’exécution]**, sélectionnez `wishlist.email` comme **[!UICONTROL dimension secondaire]**. Chaque article de liste de souhaits déclenche un e-mail distinct, en utilisant l’adresse e-mail stockée dans les données de liste de souhaits comme dimension secondaire.

   ![](assets/notify-5.png){zoomable="yes"}

1. Ajoutez une activité **[!UICONTROL E-mail]** pour créer un message de disponibilité du produit. Cliquez sur **[!UICONTROL Modifier le contenu]** pour commencer à concevoir votre contenu.

   ➡️ [En savoir plus sur la personnalisation d’e-mail](../email/content-from-scratch.md)

   ![](assets/notify-7.png){zoomable="yes"}

1. Une fois votre campagne testée et prête, cliquez sur **[!UICONTROL Publier]** pour la mettre en ligne.

Avec cette campagne orchestrée, la clientèle reçoit un e-mail distinct pour chacun des articles de sa liste de souhaits. Chaque message est envoyé à l’adresse e-mail spécifique associée à cette liste de souhaits, avec un contenu personnalisé provenant des détails de l’article de cette liste.

