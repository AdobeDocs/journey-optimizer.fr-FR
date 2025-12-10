---
solution: Journey Optimizer
product: journey optimizer
title: Envoyer des mises à jour d’éléments de liste de souhaits
description: Envoyer des mises à jour d’éléments de liste de souhaits
feature: Use Cases
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---

# Envoyer des mises à jour d’éléments de liste de souhaits {#wishist-uc}

>[!BEGINSHADEBOX]

Bien que cet exemple utilise un schéma **Wishlist**, la même méthode s’applique à toute entité ayant une relation un-à-plusieurs avec **Destinataires** tel que **Achats**, **Abonnements**, ou tout schéma personnalisé dans lequel chaque destinataire peut avoir plusieurs enregistrements associés.

**Schémas nécessaires pour ce cas d’utilisation :**

* **Destinataires** : utilisé comme dimension de ciblage
* **WishlistItems** : avec champs : `creationDate`, `product`, `Wishlistid`
* **Produit** : avec champs : `description`, `priceref`, `imageurl`
* **AbandonedCarts** (facultatif) : avec le champ : `lastmodified`

➡️ [Découvrez comment configurer des schémas basés sur des modèles](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-reengagement-11.png){zoomable="yes"}

Cette campagne orchestrée se concentre sur le réengagement des visiteurs en leur rappelant les produits enregistrés dans leur liste de souhaits. À l’aide de l’orchestration de Campaign, définissez l’audience avec des conditions basées sur l’activité Liste de souhaits, afin de repousser les visiteurs à la conversion.

1. Commencez par créer une nouvelle campagne spécifiquement destinée au réengagement des listes de souhaits. Cela permet de cibler la messagerie sur les clients qui ont affiché leur intention d’achat en enregistrant des articles.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Renseignez vos **paramètres de Campaign**.

1. Ajoutez une activité **[!UICONTROL Créer une audience]** pour identifier le groupe de clients à cibler en fonction du comportement de la liste de souhaits.

   ![](assets/uc-reengagement-2.png){zoomable="yes"}

1. Définissez un **[!UICONTROL Libellé]** descriptif pour cette audience et choisissez **[!UICONTROL Destinataires]** comme **[!UICONTROL Dimension de ciblage]**. Cliquez ensuite sur **[!UICONTROL Continuer]** pour configurer l’audience.

1. Cliquez sur **[!UICONTROL Ajouter une condition]** pour affiner votre audience en créant la condition suivante :

   `WishlistItems Exist such as (creationDate greater than or equal to 36 months ago) AND (product is not empty`
SOIT
   `AbandonedCarts Exist such as lastmodified greater than or equal to 36 months ago`

   Cette audience est basée sur les destinataires qui ont une liste de souhaits, qui contiennent des éléments avec des images de produit ou qui ont un panier abandonné au cours de la période définie.

   ![](assets/uc-reengagement-3.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Calculer]** pour voir le nombre de profils affectés par ces conditions et **[!UICONTROL Afficher les résultats]** pour examiner les détails de chaque condition et confirmer que l’audience correspond à votre segment cible.

   ![](assets/uc-reengagement-4.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Confirmer]**.

1. Ajoutez une activité **[!UICONTROL Enrichissement]** pour personnaliser la campagne avec **Liste de souhaits** et **informations sur les produits**.

   ![](assets/uc-reengagement-5.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Ajouter des données d’enrichissement]**.

1. Accédez à `Targeting dimension > Wishlistitems > Wishlistid`.

   ![](assets/uc-reengagement-6.png){zoomable="yes"}

1. Sélectionnez le mode de collecte des données, dans ce cas, **[!UICONTROL Collecter des données]** pour rassembler les détails de la liste de souhaits de votre audience.

1. Choisissez le nombre de lignes à récupérer. Par défaut, trois éléments par liste de souhaits sont récupérés, mais cela peut être ajusté en fonction des besoins de la campagne pour mettre en évidence plus ou moins de produits.

1. Cliquez sur **[!UICONTROL Ajouter un attribut]** pour créer les trois attributs suivants :

   * `Product > description`
   * `Product > priceref`
   * `Product > imageurl`

   Le message est ainsi enrichi d’informations détaillées sur les produits afin de générer des conversions.

   ![](assets/uc-reengagement-7.png){zoomable="yes"}

1. Ajoutez une activité d’e-mail pour créer un message de réengagement personnalisé pour chaque client. Cliquez sur **[!UICONTROL Modifier le contenu]** pour commencer à concevoir votre contenu.

   ➡️ [En savoir plus sur la personnalisation des emails](../email/content-from-scratch.md)

   ![](assets/uc-reengagement-8.png){zoomable="yes"}

1. Une fois l’e-mail finalisé, enregistrez et exécutez la campagne en mode brouillon en cliquant sur **[!UICONTROL Démarrer]** à partir de la campagne orchestrée.

1. Après avoir démarré le mode brouillon, prévisualisez l’audience avec les détails de la liste de souhaits.

   Pour obtenir des informations plus détaillées, cliquez sur un résultat de sortie et sélectionnez **[!UICONTROL Prévisualiser les résultats]**.

   ![](assets/uc-reengagement-10.png){zoomable="yes"}

Une fois la campagne terminée, nous pouvons explorer nos rapports, ce qui nous donne un ensemble robuste de données et d’indicateurs clés de performance sur les performances de notre campagne.

➡️ [En savoir plus sur le reporting](../reports/campaign-global-report-cja.md)
