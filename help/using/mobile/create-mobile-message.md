---
solution: Journey Optimizer
product: journey optimizer
title: Créer un message mobile
description: Découvrez comment créer un message mobile dans Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
TQID: https://experienceleague.adobe.com/xgPlWorA3lsIF8ZBPHdg2UAK8cLKUsJO-2ONc7ZG8AU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e0eb8757-182f-49f3-94a4-1587d16f5094id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 748
ht-degree: 41%

---

# Créer un message mobile {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Créer un message mobile"
>abstract="Pour créer un message mobile, ajoutez une action SMS dans un parcours ou une campagne et commencez le personnaliser à l’aide de l’éditeur de personnalisation."

>[!AVAILABILITY]
>
>RCS n’est pas un service conforme à la loi HIPAA et ne doit pas être utilisé pour collecter, stocker ou traiter des données personnelles sensibles, y compris des données de santé autorisées, par exemple des informations de santé personnelles, que votre organisation pourrait par ailleurs être autorisée à traiter dans Journey Optimizer.

Vous pouvez concevoir et envoyer des messages texte (SMS), riches (RCS) et multimédia (MMS) avec Adobe Journey Optimizer. Vous devez d’abord ajouter une action Message mobile dans un parcours ou une campagne, puis définir le contenu du Message mobile, comme décrit ci-dessous. Adobe Journey Optimizer offre également des fonctionnalités permettant de tester vos messages mobiles avant l’envoi afin que vous puissiez vérifier le rendu, les attributs de personnalisation et tous les autres paramètres.

Conformément aux normes et réglementations du secteur, tous les messages marketing SMS/RCS/MMS doivent contenir un moyen permettant aux destinataires de se désabonner facilement. Pour ce faire, les destinataires de SMS peuvent répondre avec des mots-clés d’accord préalable et de droit d’opposition. [Découvrir comment gérer un droit d’opposition](../privacy/opt-out.md#opt-out-decision-management)

## Ajouter un message mobile {#create-sms-journey-campaign}

Parcourez les onglets ci-dessous pour savoir comment ajouter un Message mobile dans une campagne ou un parcours.

>[!BEGINTABS]

>[!TAB Ajouter un message mobile à un Parcours ]

1. Ouvrez votre parcours, puis effectuez un glisser-déposer d’une activité **[!UICONTROL Action]** depuis la section **[!UICONTROL Actions]** de la palette. En savoir plus sur l’activité [Action](../building-journeys/journey-action.md).

   >[!IMPORTANT]
   >
   >Les activités de canal natives héritées (e-mail, notification push, SMS, in-app, web, expérience basée sur le code et carte de contenu) sont obsolètes depuis la version de mars 2026. Les parcours existants qui utilisent ces activités continuent à fonctionner sans modification ; aucune migration n’est requise.

1. Sélectionnez **[!UICONTROL Message mobile]** comme type d’action, puis cliquez sur **[!UICONTROL Ajouter]**.

   ![](assets/sms_create_1.png)

1. Saisissez un **[!UICONTROL Libellé]** pour identifier votre action dans la zone de travail du parcours.

1. Cliquez sur le bouton **[!UICONTROL Configurer l’action]**.

1. Vous accédez à l’onglet **[!UICONTROL Actions]**. À partir de là, sélectionnez ou créez la configuration Message mobile à utiliser. [En savoir plus](mobile-configuration.md)

   ![](assets/sms_create_2.png)

1. De plus, vous pouvez appliquer des règles de limitation à votre action Message mobile en sélectionnant un jeu de règles dans la liste déroulante **[!UICONTROL Règles métier]**. [En savoir plus](../conflict-prioritization/channel-capping.md)

1. Sélectionnez le bouton **[!UICONTROL Modifier le contenu]** et créez votre contenu selon vos besoins. [En savoir plus](design-mobile.md)

1. Revenez à la zone de travail parcours. Si nécessaire, complétez votre flux de parcours en faisant glisser et en déposant des actions ou des événements supplémentaires. [En savoir plus](../building-journeys/about-journey-activities.md)

Pour plus d’informations sur la création, la configuration et la publication d’un parcours, consultez [cette page](../building-journeys/journey-gs.md).

>[!TAB Ajouter un message mobile à une campagne]

1. Accédez au menu **[!UICONTROL Campagnes]**, puis cliquez sur **[!UICONTROL Créer une campagne]**.

1. Sélectionner le type de campagne que vous souhaitez exécuter.

   * **Scheduled - Marketing** : permet d’exécuter la campagne immédiatement ou à une date spécifiée. Les campagnes planifiées visent à envoyer des messages marketing. Elles sont configurées et exécutées à partir de l’interface d’utilisation.

   * **Déclenchée par API - Marketing/Transactionnelle** : permet d’exécuter la campagne à l’aide d’un appel API. Les campagnes déclenchées par API sont destinées à envoyer des messages marketing, ou transactionnels, c’est-à-dire des messages envoyés suite à une action effectuée par un individu : réinitialisation du mot de passe, achat dans le panier, etc.

1. Dans la section **[!UICONTROL Propriétés]**, modifiez le **[!UICONTROL Titre]** et la **[!UICONTROL Description]** de votre campagne.

1. Dans l&#39;onglet **[!UICONTROL Action]**, cliquez sur **[!UICONTROL Ajouter une action]** et choisissez **[!UICONTROL Message mobile]**. Sélectionnez ou créez ensuite une configuration.

   En savoir plus sur la configuration des messages mobiles sur [cette page](mobile-configuration.md).

   ![](assets/sms_create_3.png)

1. Cliquez sur **[!UICONTROL Créer une expérience]** pour commencer à configurer votre expérience de contenu et créer des traitements afin de mesurer leurs performances et d’identifier la meilleure option pour votre audience cible. [En savoir plus](../content-management/content-experiment.md)

1. Dans la section **[!UICONTROL Tracking des actions]**, indiquez si vous souhaitez effectuer le tracking des clics sur les liens de votre message mobile.

1. Dans l’onglet **[!UICONTROL Audience]**, cliquez sur le bouton **[!UICONTROL Sélectionner une audience]** pour définir l’audience à cibler à partir de la liste des audiences Adobe Experience Platform disponibles. [En savoir plus](../audience/about-audiences.md).

1. Dans le champ **[!UICONTROL Espace de noms d’identité]**, choisissez l’espace de noms à utiliser pour identifier les personnes à partir de l’audience sélectionnée. [En savoir plus](../event/about-creating.md#select-the-namespace).

1. Dans l’onglet **[!UICONTROL Planifier]**, vous pouvez concevoir vos campagnes à exécuter à une date spécifique ou à une fréquence récurrente. Découvrez comment configurer le **[!UICONTROL Planning]** de votre campagne dans [cette section](../campaigns/campaign-schedule.md#action-campaign-schedule).

1. Dans le menu **[!UICONTROL Déclencheurs d’action]**, choisissez l’option **[!UICONTROL Fréquence]** de votre message mobile :

   * Une fois
   * Quotidien
   * Hebdomadaire
   * Mois

Vous pouvez maintenant commencer à concevoir le contenu de votre message mobile à partir du bouton **[!UICONTROL Modifier le contenu]**, comme décrit ci-dessous. [En savoir plus](design-mobile.md)

Pour plus d’informations sur la création, la configuration et l’activation d’une campagne, consultez [cette page](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

**Rubriques connexes**

* [Concevoir un message mobile](design-mobile.md)
* [Ajouter un message dans une campagne](../campaigns/create-campaign.md)
* [Prévisualiser, tester et envoyer votre message mobile](send-mobile-message.md)
* [Configurer le canal des messages mobiles](mobile-configuration.md)
* [Rapports de messages mobiles](../reports/journey-global-report-cja-sms.md)

