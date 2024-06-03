---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des fragments
description: Découvrez comment utiliser des fragments de contenu pour réutiliser du contenu dans des campagnes et des parcours Journey Optimizer
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: e7ff784d51da48c1970841e416c655c02cfafb7c
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 46%

---

# Prise en main des fragments {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Définir vos propres fragments"
>abstract="Créez et gérez des fragments autonomes pour rendre votre contenu réutilisable sur plusieurs parcours et campagnes."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="Créer des fragments"

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Campagnes de mise à jour des fragments"
>abstract="Campagnes de mise à jour des fragments"

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Parcours de mise à jour des fragments"
>abstract="Parcours de mise à jour des fragments"

Un fragment est un composant réutilisable pouvant être référencé dans un ou plusieurs emails au sein de [!DNL Journey Optimizer] campagnes et parcours. Cette fonctionnalité permet de précréer plusieurs blocs de contenu personnalisés qui peuvent être utilisés par des personnes chargées du marketing pour assembler rapidement les contenus d’e-mail dans un processus de conception amélioré.

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [Découvrez comment gérer, créer et utiliser des fragments dans ces vidéos.](#video-fragments)

Pour optimiser l’utilisation des fragments :

* **Créer vos propres fragments**: créez des fragments visuels ou d’expression, à partir de zéro ou en enregistrant le contenu en tant que fragment. [Découvrez comment créer un fragment](#create-fragments). En outre, vous pouvez tirer parti de l’**API REST de contenu** Journey Optimizer pour gérer les fragments de contenu. Pour plus d’informations à ce sujet, consultez la [documentation relative aux API Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.
* **Réutilisation des fragments :** Utilisez-les autant de fois que nécessaire dans votre contenu. Voir [Ajouter des fragments visuels](../email/use-visual-fragments.md) et [Utiliser des fragments d’expression](../personalization/use-expression-fragments.md)

## Avant de commencer {#fragment-prerequisites}

>[!NOTE]
>
>Pour créer, modifier et archiver des fragments, vous devez disposer de l’autorisation **[!DNL Manage library items]** incluse dans le profil de produit **[!DNL Content Library Manager]**. [En savoir plus](../administration/ootb-product-profiles.md#content-library-manager)

Dans cette version, les restrictions suivantes s’appliquent :

* **Fragments visuels** sont disponibles uniquement pour le canal Email .
* **Fragments d’expression** ne sont pas disponibles pour le canal In-App.

## Fragments d’expression visuelle {#visual-expression}

Deux types de fragments sont disponibles :

* **Fragments visuels** sont des blocs visuels prédéfinis que vous pouvez réutiliser dans plusieurs diffusions email à l’aide de la fonction [Concepteur d&#39;email](../email/get-started-email-design.md)ou dans [modèles de contenu](../email/use-email-templates.md).
* **Fragments d’expression** sont des expressions prédéfinies disponibles à partir d’une entrée dédiée dans la variable [éditeur de personnalisation](../personalization/personalization-build-expressions.md).


Tous les fragments sont accessibles à partir du **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Fragments]**  menu de gauche.

![](assets/fragment-list.png)

## Vidéo pratique {#video-fragments}

Découvrez comment gérer, créer et utiliser des fragments visuels dans [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

Découvrez comment gérer, créer et utiliser des fragments d’expression dans [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
