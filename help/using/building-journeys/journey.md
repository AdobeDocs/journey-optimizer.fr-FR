---
solution: Journey Optimizer
product: journey optimizer
title: Principe général
description: Principe général
feature: Journeys
topic: Content Management
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: ab2956ab1dc3dfdf2ff67c3b6bcb1e3090d34ee3
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 63%

---


# Principe général{#jo-general-principle}

Utilisation [!DNL Journey Optimizer] pour créer des cas d’utilisation d’orchestration en temps réel à l’aide de données contextuelles stockées dans des événements ou des sources de données.

Concevez des scénarios avancés à plusieurs étapes avec les fonctionnalités suivantes :

* Envoyez des **diffusions unitaires** en temps réel déclenchées lorsqu’un événement est reçu ou **par lots** à l’aide de segments Adobe Experience Platform.

* Tirez parti des **données contextuelles** issues des événements, des informations d’Adobe Experience Platform ou des données provenant de services d’API tiers.

* Utilisez les **actions intégrées** pour envoyer des messages conçus dans [!DNL Journey Optimizer] ou créez des **actions personnalisées** si vous utilisez un système tiers pour envoyer vos messages.

* Avec le **concepteur de parcours**, créez vos cas d’utilisation à plusieurs étapes : en toute facilité, faites glisser et déposez un événement d’entrée ou une activité de lecture de segment, ajoutez des conditions et envoyez des messages personnalisés.

## Procédure de création d’un parcours{#steps-journey}

Utilisez Adobe Journey Optimizer pour concevoir et orchestrer des parcours personnalisés à partir d’une seule zone de travail.

Adobe Journey Optimizer comprend un canevas d’orchestration omnicanal qui permet aux marketeurs d’harmoniser la portée marketing avec l’engagement client individuel. L’interface utilisateur vous permet de faire glisser facilement des activités de la palette vers la zone de travail pour créer votre parcours.

![](assets/interface-journeys.png)

Découvrez comment démarrer et créer votre premier parcours dans [cette page](journey-gs.md).

Le concepteur de parcours omnicanal vous aide à créer des parcours à plusieurs étapes avec des audiences ciblées, des mises à jour basées sur les interactions client ou commerciale en temps réel et des messages omnicanaux à l’aide d’une interface intuitive de glisser-déposer.

![](assets/journey38.png)

En savoir plus dans [cette section](using-the-journey-designer.md).

En tant qu’ingénieur en données, les étapes de configuration de vos parcours, y compris les sources de données, les événements et les actions, sont détaillées dans la section [cette section](../configuration/about-data-sources-events-actions.md).


## Cas d’utilisation{#uc-journey}

Découvrez comment créer des parcours dans les cas d’utilisation de bout en bout suivants.

Cas pratiques professionnels :

* [Envoi de messages multi-canal](journeys-uc.md)
* [Envoi de messages à l’aide de Campaign v7/v8](campaign-classic-use-case.md)
* [Envoyer un message aux abonnés](message-to-subscribers-uc.md)

Cas pratiques techniques :

* [Transmission dynamique des collections à l’aide d’actions personnalisées](collections.md)
* [Accélération des diffusions](ramp-up-deliveries-uc.md)
* [Limitation du débit avec les sources de données externes et les actions personnalisées](limit-throughput.md)

## Versions de parcours{#journey-versions}

Dans la liste des parcours, toutes les versions de parcours sont accompagnées d&#39;un numéro. Voir [cette page](../building-journeys/using-the-journey-designer.md).

Lorsque vous recherchez un parcours, les versions les plus récentes apparaissent en haut de la liste la première fois que vous ouvrez l&#39;application. Vous pouvez ensuite définir l&#39;ordre de tri souhaité ; l&#39;application le conservera en tant que préférence utilisateur. La version du parcours est également affichée en haut de l&#39;interface d&#39;édition des parcours, au-dessus de la zone de travail.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Dans la plupart des cas, un profil ne peut pas être présent plusieurs fois dans le même parcours, en même temps. Si la reprise est activée, un profil peut rejoindre à nouveau un parcours, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours. [En savoir plus](end-journey.md).

Si vous devez modifier un parcours actif, créez une nouvelle version de votre parcours.

1. Ouvrez la dernière version de votre parcours actif, cliquez sur **[!UICONTROL Créer une version]**, puis confirmez.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Vous ne pouvez créer une version qu&#39;à partir de la dernière version d&#39;un parcours.

1. Effectuez vos modifications, cliquez sur **[!UICONTROL Publier]**, puis confirmez.

   ![](assets/journeyversions3.png)

Aussitôt le parcours publié, les individus commencent à accéder à la dernière version. Les clients qui ont déjà accédé à une version antérieure y restent jusqu&#39;à la fin du parcours. En cas de rentrée ultérieure dans le même parcours, les clients accéderont à la version la plus récente.

Les versions de parcours peuvent être arrêtées individuellement. Toutes les versions des parcours portent le même nom.

Lorsque vous publiez une nouvelle version d&#39;un parcours, la version précédente se termine automatiquement et passe au statut **Fermé**. Aucune entrée dans le parcours ne peut se produire. Même si vous arrêtez la dernière version, la version précédente reste fermée.

>[!NOTE]
>
>Pour en savoir plus sur les versions de parcours, consultez [cette page](../start/guardrails.md#journey-versions-limitations)