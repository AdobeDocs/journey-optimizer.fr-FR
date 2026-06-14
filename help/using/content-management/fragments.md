---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les fragments
description: Découvrez comment utiliser des fragments de contenu afin de réutiliser du contenu dans des campagnes et des parcours Journey Optimizer.
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
TQID: https://experienceleague.adobe.com/2XVXr3MjYnD-7o0C2ARXQ8j3sJOFfJfvjfCEZdkV50I
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: dc3ac795cd3cbfbd3dd3adfe6f220641d331081f
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 82%

---

# Commencer avec les fragments {#fragments}

>[!BEGINSHADEBOX]

**Sur cette page :** Prise en main des fragments de contenu visuels et d’expression dans Adobe Journey Optimizer, composants réutilisables que vous pouvez créer une fois et référencer dans les e-mails de plusieurs campagnes et parcours.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Définir vos propres fragments"
>abstract="Créez et gérez des fragments autonomes pour rendre votre contenu réutilisable sur plusieurs parcours et campagnes."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="Créer des fragments"

Un fragment est un composant réutilisable pouvant être référencé dans un ou plusieurs e-mails dans des campagnes et des parcours [!DNL Journey Optimizer]. Cette fonctionnalité vous permet de créer en avance plusieurs blocs de contenu personnalisés qui peuvent être utilisés par des personnes chargées du marketing pour assembler rapidement des contenus d’e-mails avec un processus de conception amélioré.

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [Découvrez comment gérer, créer et utiliser des fragments dans ces vidéos.](#video-fragments)

Pour optimiser l’utilisation des fragments, procédez comme suit :

* **Créer vos propres fragments** : créez des fragments visuels ou des fragments d’expression, à partir de zéro ou en enregistrant du contenu en tant que fragment. [Découvrez comment créer un fragment](create-fragments.md). En outre, vous pouvez tirer parti de l’**API REST Content** Journey Optimizer pour gérer les fragments de contenu. Pour plus d’informations à ce sujet, consultez la [documentation relative aux API Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"}.
* **Réutilisez vos fragments :** utilisez-les autant de fois que nécessaire dans votre contenu. Voir [Ajouter des fragments visuels](../email/use-visual-fragments.md) et [Utiliser des fragments d’expression](../personalization/use-expression-fragments.md)


>[!NOTE]
>
>Les **[!UICONTROL fragments]** décrits sur cette page sont des composants **contenu** réutilisables. Elles sont différentes de :
>
>* **[Fragments de Parcours](../building-journeys/journey-fragments.md)** — ensembles réutilisables de nœuds de parcours insérés dans des parcours.
>* **[Fragments de contenu AEM](../integrations/aem-fragments.md)** — contenu créé dans Adobe Experience Manager et utilisé dans [!DNL Journey Optimizer].


## Avant de commencer {#fragment-prerequisites}

Pour créer, modifier, archiver et publier des fragments, vous avez besoin des autorisations **[!DNL Manage library items]** et **[Publier le fragment]** incluses dans le profil de produit **[!DNL Content Library Manager]**. [En savoir plus](../administration/ootb-product-profiles.md#content-library-manager)

Dans cette version, les restrictions suivantes s’appliquent :

* Les **fragments visuels** ne sont disponibles que pour le canal e-mail.
* Les **fragments d’expression** ne sont pas disponibles pour le canal in-app.

D’autres mécanismes de sécurisation s’appliquant aux fragments sont disponibles dans [cette section](../start/guardrails.md#fragments-guardrails).

## Fragments visuels et fragments d’expression {#visual-expression}

Deux types de fragments sont disponibles :

* Les **Fragments visuels** sont des blocs visuels prédéfinis que vous pouvez réutiliser dans plusieurs diffusions e-mail à l’aide du [Concepteur d’e-mail](../email/get-started-email-design.md)ou dans des [modèles de contenu](../email/use-email-templates.md).
* Les **Fragments d’expression** sont des expressions prédéfinies disponibles à partir d’une entrée dédiée dans l’[éditeur de personnalisation](../personalization/personalization-build-expressions.md).

Tous les fragments sont accessibles à partir du menu de gauche **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Fragments]**. [Découvrir comment gérer les fragments](../content-management/manage-fragments.md)

![](assets/fragment-list.png)

## Vidéo pratique {#video-fragments}

Découvrez comment gérer, créer et utiliser des **fragments visuels** dans [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3451184/?captions=fre_fr&quality=12)

Découvrez comment gérer, créer et utiliser des **fragments d’expression** dans [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3438919/?captions=fre_fr&quality=12)
