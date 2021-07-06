---
title: Utiliser des offres personnalisées dans un email
description: Découvrez un exemple de bout en bout montrant toutes les étapes nécessaires pour configurer des offres et les utiliser dans un email.
feature: Offres
topic: Intégrations
role: User
level: Intermediate
source-git-commit: a25264cb43f77671c29f18522110fd85d0155697
workflow-type: tm+mt
source-wordcount: '1340'
ht-degree: 4%

---

# Cas pratique : Configurer des offres personnalisées pour les utiliser dans un email {#configure-add-personalized-offers-email}

Cette section présente un exemple de bout en bout de la configuration des offres et de leur utilisation dans un email, en fonction d’une décision que vous avez précédemment créée.

## Principales étapes

Les étapes clés de configuration des offres, de leur inclusion dans une décision et de l’utilisation de cette décision dans un email sont répertoriées ci-dessous :

1. Avant de créer des offres, [définissez vos composants](#define-components)

   * Création d&#39;emplacements
   * Création de règles de décision
   * Création de balises
   * Créer des classements (facultatif)

1. [Configurer les offres](#configure-offers)

   * Créer des offres
   * Pour chaque offre :

      * Créer des représentations et sélectionner un emplacement et une ressource pour chaque représentation
      * Ajouter une règle pour chaque offre
      * Définition d’une priorité pour chaque offre

1. [Création d&#39;une offre de secours](#create-fallback)

1. [Créer une ](#create-collection) collection pour inclure les offres personnalisées que vous avez créées

1. [Configurer la décision](#configure-decision)

   * Création d&#39;une décision
   * Sélectionner les emplacements que vous avez créés
   * Pour chaque emplacement, sélectionnez la collection .
   * Pour chaque emplacement, sélectionnez un classement (facultatif).
   * Sélectionner la version de secours

1. [Insérer la décision dans un email](#insert-decision-in-email)

   * Sélectionner un emplacement correspondant aux offres que vous souhaitez afficher
   * Sélectionnez la décision parmi les éléments compatibles avec l’emplacement sélectionné.
   * Prévisualiser vos offres

Le processus global de gestion des décisions pour utiliser les offres dans un email peut être décrit comme suit :

![](../assets/offers-e2e-process.png)

## Définition des composants {#define-components}

Avant de commencer à créer des offres, vous devez définir plusieurs composants que vous utiliserez dans vos offres.

Vous les trouverez sous le **[!UICONTROL menu Gestion de la décision]** > **[!UICONTROL Composants]**.

1. Commencez par créer **emplacements** pour vos offres.

   Vous utiliserez ces emplacements pour définir où l’offre résultante apparaîtra lors de la définition de votre décision d’offre.

   Dans cet exemple, créez trois emplacements avec le canal et les types de contenu suivants :

   * *Web - Image*
   * *Email - Image*
   * *Non numérique - Texte*

   ![](../assets/offers-e2e-placements.png)

   Les étapes détaillées pour créer des emplacements sont décrites dans [cette section](../../using/offers/offer-library/creating-placements.md).

1. Créez des **règles de décision**.

   Les règles de décision offrent la meilleure offre à un profil dans Adobe Experience Platform.

   Configurez deux règles simples en utilisant l’attribut **[!UICONTROL XDM Individual Profile > Person > Gender]** :

   * *Clients féminins*
   * *Clients masculins*

   ![](../assets/offers-e2e-rules.png)

   Les étapes détaillées pour créer des règles sont décrites dans [cette section](../../using/offers/offer-library/creating-decision-rules.md).

1. Vous pouvez également créer une balise ****.

   Vous pourrez ensuite l’associer à vos offres et utiliser cette balise pour regrouper vos offres dans une collection.

   Dans cet exemple, créez la balise *Yoga* .

   ![](../assets/offers-e2e-tag.png)

   Les étapes détaillées pour créer des balises sont décrites dans [cette section](../../using/offers/offer-library/creating-tags.md).

1. Si vous souhaitez définir des règles qui déterminent quelle offre doit être présentée en premier pour un emplacement donné (plutôt que de prendre en compte les scores de priorité des offres), vous pouvez créer une **formule de classement**.

   Les étapes détaillées pour créer des formules de classement sont décrites dans [cette section](../../using/offers/offer-library/create-ranking-formulas.md#create-ranking-formula).

   >[!NOTE]
   >
   >Dans cet exemple, nous n’utiliserons que les scores de priorité. En savoir plus sur les [règles d’éligibilité et les contraintes](../../using/offers/offer-library/creating-personalized-offers.md#eligibility).

## Configurer des offres {#configure-offers}

Vous pouvez maintenant créer et configurer vos offres. Dans cet exemple, vous allez créer quatre offres que vous souhaitez afficher en fonction de chaque profil spécifique.

1. Création d’une offre. En savoir plus dans [cette section](../../using/offers/offer-library/creating-personalized-offers.md#create-offer).

1. Dans cette offre, créez trois représentations. Chaque représentation doit être une combinaison d’un emplacement que vous avez créé précédemment et d’une ressource :

   * Un correspondant à l’emplacement *Web - Image*
   * Un correspondant à l’emplacement *Email - Image*
   * Un correspondant à l’emplacement *Non numérique - Texte*

   >[!NOTE]
   >
   >Une offre peut être affichée à différents endroits dans un message afin de créer plus d’opportunités d’utilisation de l’offre dans différents contextes d’emplacement.

   En savoir plus sur les représentations dans [cette section](../../using/offers/offer-library/creating-personalized-offers.md#representations).

1. Sélectionnez une image appropriée pour les deux premiers emplacements. Saisissez du texte personnalisé pour l’emplacement *Non numérique - Texte*.

   ![](../assets/offers-e2e-representations.png)

1. Dans la section **[!UICONTROL Eligibilité de l&#39;offre]** , sélectionnez **[!UICONTROL Par règle de décision définie]** et effectuez un glisser-déposer de la règle de votre choix.

   ![](../assets/offers-e2e-eligibility.png)

1. Remplissez la **[!UICONTROL Priorité]**. Dans cet exemple, ajoutez *25*.

1. Vérifiez votre offre, puis cliquez sur **[!UICONTROL Enregistrer et approuver]**.

   ![](../assets/offers-e2e-review.png)

1. Dans cet exemple, créez trois offres supplémentaires avec les mêmes représentations, mais des ressources différentes. Attribuez-les à des règles et priorités différentes, telles que :

   * Première offre - Règle de décision : *Clients féminins*, Priorité : *25*
   * Deuxième offre - Règle de décision : *Clients féminins*, Priorité : *15*
   * Troisième offre - Règle de décision : *Clients masculins*, Priorité : *25*
   * Quatrième offre - Règle de décision : *Clients masculins*, Priorité : *15*

   ![](../assets/offers-e2e-offers-created.png)

Les étapes détaillées pour créer et configurer des offres sont décrites dans [cette section](../../using/offers/offer-library/creating-personalized-offers.md).

## Création d&#39;une offre de secours {#create-fallback}

1. Création d&#39;une offre de secours.

1. Définissez les mêmes représentations que pour les offres, avec les ressources appropriées (elles doivent être différentes de celles utilisées dans vos offres).

   Chaque représentation doit être une combinaison d’un emplacement que vous avez créé précédemment et d’une ressource :

   * Un correspondant à l’emplacement *Web - Image*
   * Un correspondant à l’emplacement *Email - Image*
   * Un correspondant à l’emplacement *Non numérique - Texte*

   ![](../assets/offers-e2e-fallback-representations.png)

1. Vérifiez votre offre de secours, puis cliquez sur **[!UICONTROL Enregistrer et approuver]**.

![](../assets/offers-e2e-fallback.png)

Votre offre de secours est maintenant prête à être utilisée dans une décision.

Les étapes détaillées pour créer et configurer une offre de secours sont décrites dans [cette section](../../using/offers/offer-library/creating-fallback-offers.md).

## Création d&#39;une collection {#create-collection}

Lors de la configuration de la décision, vous devez ajouter vos offres personnalisées dans le cadre d’une collection.

1. Pour accélérer le processus de décision, créez une collection dynamique.

1. Utilisez la balise *Yoga* pour sélectionner les quatre offres personnalisées que vous avez créées précédemment.

   ![](../assets/offers-e2e-collection-using-tag.png)

Les étapes détaillées pour créer une collection sont décrites dans [cette section](../../using/offers/offer-library/creating-collections.md).

## Configurer la décision {#configure-decision}

Vous devez maintenant créer une décision qui combinera des emplacements avec les offres personnalisées et l’offre de secours que vous venez de créer.

Cette combinaison sera utilisée par le moteur d’Offer decisioning pour trouver la meilleure offre pour un profil spécifique : dans cet exemple, il sera basé sur la priorité et la règle de décision que vous avez assignées à chaque offre.

Pour créer et configurer une décision d’offre, procédez comme suit :

1. Création d&#39;une décision. En savoir plus dans [cette section](../../using/offers/offer-activities/create-offer-activities.md#create-activity).

1. Sélectionnez les emplacements *Web - Image*, *Email - Image* et *Non numérique - Texte*.

   ![](../assets/offers-e2e-decision-placements.png)

1. Pour chaque emplacement, ajoutez la collection que vous avez créée.

   ![](../assets/offers-e2e-decision-collection.png)

1. Si vous avez défini un classement lors de la [création de vos composants](#define-components), vous pouvez l’affecter à un emplacement dans la décision. Si plusieurs offres peuvent être présentées à cet emplacement, la décision utilisera cette formule pour calculer la première offre à diffuser.

   Les étapes détaillées pour attribuer une formule de classement à un emplacement sont décrites dans [cette section](../../using/offers/offer-activities/configure-offer-selection.md#assign-ranking-formula).

1. Sélectionnez l’offre de secours que vous avez créée. Il s’affichera comme une offre de secours disponible pour les trois emplacements sélectionnés.

   ![](../assets/offers-e2e-decision-fallback.png)

1. Vérifiez votre décision, puis cliquez sur **[!UICONTROL Enregistrer et approuver]**.

   ![](../assets/offers-e2e-review-decision.png)

Votre décision est maintenant prête à être utilisée pour diffuser des offres optimisées et personnalisées.

Les étapes détaillées pour créer et configurer une décision sont décrites dans [cette section](../../using/offers/offer-activities/create-offer-activities.md).

## Insérer la décision dans un email {#insert-decision-in-email}

Maintenant que votre décision est en ligne, vous pouvez l’insérer dans un email. Procédez comme suit :

1. Créez votre email, puis ouvrez le [Concepteur d&#39;email](../../using/design-emails.md) pour configurer son contenu.

1. Ajoutez un composant de structure à partir de la palette gauche.

1. Ajoutez un composant de contenu **[!UICONTROL Décision d’offre]** . Découvrez comment utiliser les composants de contenu dans [cette section](../../using/content-components.md).

   ![](../assets/offers-e2e-decision-component.png)

1. sélectionnez-le. Dans la palette de droite, cliquez sur **[!UICONTROL Sélectionner la décision de l’offre]** pour ajouter une décision.

   ![](../assets/offers-e2e-select-offer-decision.png)

1. Sélectionnez l’emplacement correspondant aux offres que vous souhaitez afficher dans la liste déroulante **[!UICONTROL Emplacements]** .

   Dans ce cas, à partir des emplacements que vous avez créés précédemment dans le cadre de cet exemple, seul l’emplacement **Email - Image** est disponible car vous souhaitez utiliser la décision dans un email. En savoir plus sur la [création d’emplacements](../../using/offers/offer-library/creating-placements.md).

   ![](../assets/offers-e2e-select-placement-in-decision.png)

1. Les décisions correspondant à l’emplacement **Email - Image** s’affichent. Sélectionnez la décision à utiliser dans le composant de contenu, puis cliquez sur **[!UICONTROL Ajouter]**.

   ![](../assets/offers-e2e-matching-placement-in-decision.png)

   >[!NOTE]
   >
   >Seules les décisions compatibles avec l’emplacement sélectionné s’affichent dans la liste.

Vous pouvez désormais visualiser toutes les offres personnalisées et l’offre de secours dans le Concepteur d’email.

![](../assets/offers-e2e-offers-displayed.png)

Utilisez la section **[!UICONTROL Offres]** ou les flèches des composants de contenu (flèches droite et gauche) pour parcourir les données. Vous pouvez également afficher les différentes offres qui font partie de la décision avec un profil client. En savoir plus dans [cette section](../../using/deliver-personalized-offers.md#preview-offers-in-email).

Une fois vos modifications enregistrées et le message publié, vos offres sont prêtes à être affichées pour les profils pertinents lors de l’envoi du message dans le cadre d’un parcours.

**Rubriques connexes :**

* Découvrez comment vérifier l’aperçu du message dans [cette section](../../using/preview.md#preview-your-messages).

* Découvrez comment publier des messages dans [cette section](../../using/publish-manage-message.md).

* Découvrez comment les messages sont déclenchés par un ou plusieurs parcours dans [cette section](../building-journeys/journey.md).

