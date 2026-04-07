---
title: Créer une boîte de réception
description: Découvrez comment créer et configurer une boîte de réception dans Adobe Journey Optimizer pour diffuser des messages persistants et non intrusifs à vos utilisateurs.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
source-git-commit: d84cc0f4d9226876e55e37409a685550fe0c9050
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 44%

---

# Création d’une boîte de réception {#inbox-create}

Avant de créer une boîte de réception, suivez les étapes décrites dans la section [Configuration de la boîte de réception](inbox-configuration.md). La configuration de canal identifie l’application ou le site web cible, la page ou la règle et l’emplacement où la boîte de réception est générée.

Pour créer une boîte de réception de messages par le biais d&#39;une campagne, procédez comme suit :

1. Création d’une campagne. [En savoir plus](../campaigns/create-campaign.md)

1. Sélectionnez le type de campagne que vous souhaitez exécuter :

   * **[!UICONTROL Scheduled - Marketing]** : permet d’exécuter la campagne immédiatement ou à une date spécifiée. Les campagnes planifiées visent à envoyer des messages de **marketing**. Elles sont configurées et exécutées à partir de l’interface d’utilisation.

   * **[!UICONTROL Déclenchée par API - Marketing/Transactionnelle]** : permet d’exécuter la campagne à l’aide d’un appel API. Les campagnes déclenchées par API sont destinées à envoyer des messages **marketing**, ou **transactionnels**, c’est-à-dire des messages envoyés suite à une action effectuée par une personne : réinitialisation du mot de passe, abandon de panier, etc. [Découvrir comment déclencher une campagne à l’aide d’API](../campaigns/api-triggered-campaigns.md)

1. Dans l’onglet **[!UICONTROL Propriétés]**, spécifiez un nom et une description pour la campagne.

1. Dans l’onglet **[!UICONTROL Action]**, sélectionnez l’action **[!UICONTROL Boîte de réception]**.

   ![](assets/inbox-create-1.png)

1. Sélectionnez ou créez une [configuration de boîte de réception](inbox-configuration.md).

   ![](assets/inbox-create-2.png)

1. Accédez à l’onglet Contenu pour concevoir votre message à l’aide du concepteur de contenu. [En savoir plus](inbox-design.md)

1. Dans l’onglet **[!UICONTROL Audience]**, cliquez sur le bouton **[!UICONTROL Sélectionner une audience]** pour afficher la liste des audiences Adobe Experience Platform disponibles. [En savoir plus sur les audiences](../audience/about-audiences.md).

1. Dans le champ **[!UICONTROL Espace de noms d’identité]**, choisissez l’espace de noms à utiliser pour identifier les personnes à partir du segment sélectionné. [En savoir plus sur les espaces de noms](../event/about-creating.md#select-the-namespace)

1. Vous pouvez planifier vos campagnes à une date spécifique ou à intervalles réguliers. [En savoir plus](../campaigns/create-campaign.md#schedule)

1. Vérifiez et activez votre campagne pour envoyer des messages à la boîte de réception.

Vous pouvez désormais choisir cette boîte de réception lors de la création de votre [campagne de carte de contenu](../content-card/create-content-card.md).
