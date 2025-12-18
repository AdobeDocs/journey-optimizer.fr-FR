---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Utilisation d’offres personnalisées dans un e-mail
description: Découvrez un exemple complet montrant toutes les étapes nécessaires pour configurer des offres et les utiliser dans un e-mail.
badge: label="Hérité" type="Informative"
feature: Decision Management, Email
topic: Integrations
role: User
level: Intermediate
exl-id: 851d988a-2582-4c30-80f3-b881d90771be
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 100%

---

# Cas d&#39;utilisation : configuration des offres personnalisées pour les utiliser dans un e-mail {#configure-add-personalized-offers-email}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../experience-decisioning/gs-experience-decisioning.md)

Cette section présente un exemple complet de la configuration des offres et de leur utilisation dans un e-mail, en fonction d&#39;une décision que vous avez précédemment créée.

## Principales étapes {#main-steps}

Les étapes clés de configuration des offres, de leur inclusion dans une décision et de l&#39;utilisation de cette décision dans un e-mail sont répertoriées ci-dessous :

1. Avant de créer des offres, [définissez vos composants](#define-components)

   * Créer des emplacements
   * Créer des règles de décision
   * Créer des qualificateurs de collection (précédemment appelés « balises »)
   * Création de classements (facultatif)

1. [Configuration des offres](#configure-offers)

   * Création d’offres
   * Pour chaque offre :

      * Création de représentations et sélection d’un emplacement et d’une ressource pour chaque représentation
      * Ajout d&#39;une règle pour chaque offre
      * Définition d&#39;une priorité pour chaque offre

1. [Création d&#39;une offre de secours](#create-fallback)

1. [Création d’une collection](#create-collection) incluant les offres personnalisées que vous avez créées

1. [Configuration de la décision](#configure-decision)

   * Création d&#39;une décision
   * Sélection des emplacements que vous avez créés
   * Pour chaque emplacement, sélection la collection
   * Pour chaque emplacement, sélection d’un classement (facultatif)
   * Sélection d&#39;une version de secours

1. [Insertion d&#39;une décision dans un e-mail](#insert-decision-in-email)

   * Sélection d’un emplacement correspondant aux offres que vous souhaitez afficher
   * Sélection de la décision parmi les éléments compatibles avec l&#39;emplacement sélectionné
   * Prévisualisation de vos offres

Le processus global de gestion des décisions pour utiliser les offres dans un e-mail peut être décrit comme suit :

![](assets/offers-e2e-process.png)

## Définition des composants {#define-components}

Avant de commencer à créer des offres, vous devez définir plusieurs composants que vous utiliserez dans vos offres.

Vous les trouverez sous le menu **[!UICONTROL Gestion des décisions]** > **[!UICONTROL Composants]**.

1. Commencez par créer des **emplacements** pour vos offres.

   Vous utilisez ces emplacements pour définir où l&#39;offre générée apparaîtra lors de la définition de votre décision d&#39;offre.

   Dans cet exemple, créez trois emplacements avec le canal et les types de contenu suivants :

   * *Web - Image*
   * *E-mail - Image*
   * *Non numérique - Texte*

   ![](assets/offers-e2e-placements.png)

   Les étapes détaillées pour créer des emplacements sont présentées dans [cette section](../../using/offers/offer-library/creating-placements.md).

1. Créez des **règles de décision**.

   Les règles de décision offrent la meilleure offre à un profil dans Adobe Experience Platform.

   Configurez deux règles simples en utilisant l&#39;attribut **[!UICONTROL XDM Individual Profile > Person > Gender]** :

   * *Clientes*
   * *Clients*

   ![](assets/offers-e2e-rules.png)

   Les étapes détaillées pour créer des règles sont présentées dans [cette section](../../using/offers/offer-library/creating-decision-rules.md).

1. Vous pouvez également créer un **qualificateur de collection**.

   Vous pourrez ensuite l’associer à vos offres et l’utiliser pour regrouper vos offres dans une collection.

   Dans cet exemple, créez le qualificateur de collection *Yoga*.

   ![](assets/offers-e2e-tag.png)

   Pour créer des qualificateurs de collection, suivez les étapes détaillées présentées dans [cette section](../../using/offers/offer-library/creating-tags.md).

1. Si vous souhaitez définir des règles qui déterminent quelle offre doit être présentée en premier pour un emplacement donné (plutôt que de prendre en compte les scores de priorité des offres), vous pouvez créer une **formule de classement**.

   Les étapes détaillées pour créer des formules de classement sont présentées dans [cette section](../../using/offers/ranking/create-ranking-formulas.md#create-ranking-formula).

   >[!NOTE]
   >
   >Dans cet exemple, nous n&#39;utiliserons que les scores de priorité. En savoir plus sur les [règles d’éligibilité et les contraintes](../../using/offers/offer-library/add-constraints.md#eligibility).

## Configuration des offres {#configure-offers}

Vous pouvez maintenant créer et configurer vos offres. Dans cet exemple, vous allez créer quatre offres à afficher en fonction de chaque profil spécifique.

1. Créez une offre. En savoir plus dans [cette section](../../using/offers/offer-library/creating-personalized-offers.md#create-offer).

1. Dans cette offre, créez trois représentations. Chaque représentation doit être une combinaison d&#39;un emplacement que vous avez créé précédemment et d&#39;une ressource :

   * Une correspondant à l&#39;emplacement *Web - Image*
   * Une correspondant à l&#39;emplacement *E-mail - Image*
   * Une correspondant à l&#39;emplacement *Non numérique - Texte*

   >[!NOTE]
   >
   >Une offre peut être affichée à différents endroits dans un message afin de créer davantage de possibilités d&#39;utiliser l&#39;offre dans différents contextes d&#39;emplacement.

   En savoir plus sur les représentations dans [cette section](../../using/offers/offer-library/add-representations.md#representations).

1. Sélectionnez une image appropriée pour les deux premiers emplacements. Saisissez du texte personnalisé pour l&#39;emplacement *Non numérique - Texte*.

   ![](assets/offers-e2e-representations.png)

1. Dans la section **[!UICONTROL Éligibilité de l&#39;offre]**, sélectionnez **[!UICONTROL Par règle de décision définie]** et effectuez un glisser-déposer de la règle de votre choix.

   ![](assets/offers-e2e-eligibility.png)

1. Remplissez la **[!UICONTROL Priorité]**. Dans cet exemple, ajoutez *25*.

1. Vérifiez votre offre, puis cliquez sur **[!UICONTROL Enregistrer et approuver]**.

   ![](assets/offers-e2e-review.png)

1. Dans cet exemple, créez trois offres supplémentaires avec les mêmes représentations, mais des ressources différentes. Attribuez-les à des règles et priorités différentes, par exemple :

   * Première offre - Règle de décision : *Clientes*, Priorité : *25*
   * Deuxième offre - Règle de décision : *Clientes*, Priorité : *15*
   * Troisième offre - Règle de décision : *Clients*, Priorité : *25*
   * Quatrième offre - Règle de décision : *Clients*, Priorité : *15*

   ![](assets/offers-e2e-offers-created.png)

Les étapes détaillées pour créer et configurer des offres sont présentées dans [cette section](../../using/offers/offer-library/creating-personalized-offers.md).

## Création d&#39;une offre de secours {#create-fallback}

1. Créez une offre de secours.

1. Définissez les mêmes représentations que pour les offres, avec les ressources appropriées (elles doivent être différentes de celles utilisées dans vos offres).

   Chaque représentation doit être une combinaison d&#39;un emplacement que vous avez créé précédemment et d&#39;une ressource :

   * Une correspondant à l&#39;emplacement *Web - Image*
   * Une correspondant à l&#39;emplacement *E-mail - Image*
   * Une correspondant à l&#39;emplacement *Non numérique - Texte*

   ![](assets/offers-e2e-fallback-representations.png)

1. Vérifiez votre offre de secours, puis cliquez sur **[!UICONTROL Enregistrer et approuver]**.

![](assets/offers-e2e-fallback.png)

Votre offre de secours est maintenant prête à être utilisée dans une décision.

Les étapes détaillées pour créer et configurer une offre de secours sont présentées dans [cette section](../../using/offers/offer-library/creating-fallback-offers.md).

## Création d&#39;une collection {#create-collection}

Lors de la configuration de la décision, vous devez ajouter vos offres personnalisées dans le cadre d&#39;une collection.

1. Pour accélérer le processus de décision, créez une collection dynamique.

1. Utilisez le qualificateur de collection *Yoga* pour sélectionner les quatre offres personnalisées que vous avez créées précédemment.

   ![](assets/offers-e2e-collection-using-tag.png)

Les étapes détaillées pour créer une collection sont présentées dans [cette section](../../using/offers/offer-library/creating-collections.md).

## Configuration de la décision {#configure-decision}

Vous devez maintenant créer une décision qui combinera des emplacements avec les offres personnalisées et l&#39;offre de secours que vous venez de créer.

Cette combinaison sera utilisée par le moteur de décision afin de trouver la meilleure offre pour un profil spécifique : dans cet exemple, elle sera basée sur la priorité et la règle de décision que vous avez attribuées à chaque offre.

Pour créer et configurer une décision d&#39;offre, procédez comme suit :

1. Créez une décision. En savoir plus dans [cette section](../../using/offers/offer-activities/create-offer-activities.md#create-activity).

1. Sélectionnez les emplacements *Web - Image*, *E-mail - Image* et *Non numérique - Texte*.

   ![](assets/offers-e2e-decision-placements.png)

1. Pour chaque emplacement, ajoutez la collection que vous avez créée.

   ![](assets/offers-e2e-decision-collection.png)

1. Si vous avez défini un classement lors de la [création de vos composants](#define-components), vous pouvez l&#39;affecter à un emplacement dans la décision. Si plusieurs offres sont éligibles à la présentation dans cet emplacement, la décision utilisera cette formule pour calculer l&#39;offre à diffuser en premier.

   Les étapes détaillées pour attribuer une formule de classement à un emplacement sont présentées dans [cette section](../../using/offers/offer-activities/configure-offer-selection.md#assign-ranking-formula).

1. Sélectionnez l&#39;offre de secours que vous avez créée. Elle s&#39;affichera comme une offre de secours disponible pour les trois emplacements sélectionnés.

   ![](assets/offers-e2e-decision-fallback.png)

1. Vérifiez votre décision, puis cliquez sur **[!UICONTROL Enregistrer et approuver]**.

   ![](assets/offers-e2e-review-decision.png)

Votre décision est maintenant prête à être utilisée pour diffuser des offres optimisées et personnalisées.

Les étapes détaillées pour créer et configurer une décision sont présentées dans [cette section](../../using/offers/offer-activities/create-offer-activities.md).

## Insertion d&#39;une décision dans un e-mail {#insert-decision-in-email}

Maintenant que votre décision est active, vous pouvez l&#39;insérer dans un e-mail. Pour ce faire, suivez les étapes présentées sur [cette page](../../using/email/add-offers-email.md).

![](assets/offers-e2e-offers-displayed.png)
