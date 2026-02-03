---
solution: Journey Optimizer
product: journey optimizer
title: Envoyer des mises à jour d’éléments de liste de souhaits
description: Envoyer des mises à jour d’éléments de liste de souhaits
feature: Use Cases
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 98%

---

# Envoyer des mises à jour d’éléments de liste de souhaits {#wishist-uc}

>[!BEGINSHADEBOX]

Bien que cet exemple utilise un schéma **Wishlist**, la même méthode s’applique à toute entité ayant une relation un-à-multiple avec **Recipients**, comme **Purchases**, **Subscriptions**, ou tout schéma personnalisé dans lequel chaque destinataire peut avoir plusieurs enregistrements associés.

**Schémas requis pour ce cas d’utilisation :**

* **Recipients** : utilisé comme dimension de ciblage
* **WishlistItems** : avec les champs `creationDate`, `product` et `Wishlistid`
* **Product** : avec les champs `description`, `priceref` et `imageurl`
* **AbandonedCarts** (facultatif) : avec le champ `lastmodified`

➡️ [Découvrez comment configurer des schémas relationnels](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-reengagement-11.png){zoomable="yes"}

Cette campagne orchestrée a pour objectif le réengagement des visiteurs en leur rappelant les produits qu’ils ont enregistrés dans leur liste de souhaits. À l’aide de l’orchestration de campagne, définissez l’audience avec des conditions basées sur l’activité Liste de souhaits afin d’inciter les visiteurs à revenir pour conversion.

1. Commencez par créer une nouvelle campagne destinée au réengagement des listes de souhaits. Cela permet d’adapter les messages aux clients et clientes qui ont montré une intention d’achat en enregistrant des articles.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Définissez les **paramètres de campagne**.

1. Ajoutez une activité **[!UICONTROL Créer une audience]** pour identifier le groupe de personnes à cibler en fonction du comportement de la liste de souhaits.

   ![](assets/uc-reengagement-2.png){zoomable="yes"}

1. Définissez un **[!UICONTROL libellé]** descriptif pour cette audience et choisissez **[!UICONTROL Destinataires]** comme **[!UICONTROL Dimension de ciblage]**. Cliquez ensuite sur **[!UICONTROL Continuer]** pour configurer l’audience.

1. Cliquez sur **[!UICONTROL Ajouter une condition]** pour affiner votre audience en créant la condition suivante :

   `WishlistItems Exist such as (creationDate greater than or equal to 36 months ago) AND (product is not empty`
OR
   `AbandonedCarts Exist such as lastmodified greater than or equal to 36 months ago`

   Cette audience est basée sur les destinataires qui disposent d’une liste de souhaits contenant des articles avec des images de produit ou qui ont un panier abandonné au cours de la période définie.

   ![](assets/uc-reengagement-3.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Calculer]** pour voir le nombre de profils concernés par ces conditions, puis sur **[!UICONTROL Afficher les résultats]** pour examiner les détails de chaque condition et confirmer que l’audience correspond à votre segment cible.

   ![](assets/uc-reengagement-4.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Confirmer]**.

1. Ajoutez une activité **[!UICONTROL Enrichissement]** pour personnaliser la campagne avec **Liste de souhaits** et **Informations sur les produits**.

   ![](assets/uc-reengagement-5.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Ajouter des données d’enrichissement]**.

1. Accédez à `Targeting dimension > Wishlistitems > Wishlistid`.

   ![](assets/uc-reengagement-6.png){zoomable="yes"}

1. Sélectionnez le mode de collecte des données, dans ce cas, **[!UICONTROL Collecter des données]** pour obtenir les détails sur les listes de souhaits de votre audience.

1. Choisissez le nombre de lignes à récupérer. Par défaut, trois articles par liste de souhaits sont récupérés, mais vous pouvez ajuster ce nombre en fonction des besoins de la campagne pour mettre en évidence plus ou moins de produits.

1. Cliquez sur **[!UICONTROL Ajouter un attribut]** pour créer les trois attributs suivants :

   * `Product > description`
   * `Product > priceref`
   * `Product > imageurl`

   Le message est ainsi enrichi d’informations détaillées sur les produits afin de générer des conversions.

   ![](assets/uc-reengagement-7.png){zoomable="yes"}

1. Ajoutez une activité d’e-mail pour créer un message de réengagement personnalisé pour chaque personne. Cliquez sur **[!UICONTROL Modifier le contenu]** pour commencer à créer votre contenu.

   ➡️ [En savoir plus sur la personnalisation des e-mails](../email/content-from-scratch.md)

   ![](assets/uc-reengagement-8.png){zoomable="yes"}

1. Une fois l’e-mail terminé, enregistrez et exécutez la campagne en mode brouillon en cliquant sur **[!UICONTROL Démarrer]** à partir de la campagne orchestrée.

1. Après avoir démarré le mode brouillon, prévisualisez l’audience avec les détails des listes de souhaits.

   Pour obtenir des informations plus détaillées, cliquez sur un résultat de sortie et sélectionnez **[!UICONTROL Prévisualiser les résultats]**.

   ![](assets/uc-reengagement-10.png){zoomable="yes"}

Une fois la campagne lancée, vous pouvez examiner les rapports et analyser les performances de la campagne grâce aux nombreuses données et KPI.

➡️ [En savoir plus sur la création de rapports](../reports/campaign-global-report-cja.md)
