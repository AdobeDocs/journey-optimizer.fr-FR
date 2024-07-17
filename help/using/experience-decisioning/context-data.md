---
title: Utiliser des données contextuelles dans la prise de décision basée sur l’expérience
description: Découvrir comment utiliser les données contextuelles dans la prise de décision basée sur l’expérience
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilité limitée"
exl-id: ddc4b681-020b-4433-b4b3-3791c41907c9
source-git-commit: 2349145fcf698769d16326a19a48a413a3c1dd95
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 100%

---

# Utiliser des données contextuelles dans la prise de décision basée sur l’expérience {#context}

Avec la prise de décision basée sur l’expérience, vous pouvez tirer profit de toutes les informations disponibles dans Adobe Experience Platform pour effectuer diverses actions, telles que la création de [règles de décision](rules.md) ou de [formules de classement](ranking.md). Par exemple, vous pouvez créer une règle de décision qui exige que la température actuelle soit de ≥ 80 degrés Fahrenheit au moment de la demande de décision.

>[!NOTE]
>
>Les données contextuelles sont définies dans Adobe Experience Platform et envoyées au moment d’une demande de décision. Elles n’incluent pas de données historiques.

Pour utiliser des données contextuelles, vous devez d’abord définir les données à rendre disponibles dans la prise de décision basée sur l’expérience. Une fois cette opération terminée, ces données s’intègrent de manière transparente à la prise de décision basée sur l’expérience sous l’onglet **[!UICONTROL Données contextuelles]** et sont disponibles lors de la création d’une règle de décision. Vous pouvez également utiliser les données lors de la modification d’une formule de classement.

![](assets/decision-rules-context.png)

Les étapes d’intégration des données Adobe Experience Platform dans Experience Decisioning sont les suivantes :

1. Créez un **schéma d’événement d’expérience** dans Adobe Experience Platform et son **jeu de données** associé.[Découvrir comment créer des schémas](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. Créez un train de données Adobe Experience Platform :

   1. Accédez au menu **[!UICONTROL Trains de données]** et sélectionnez **[!UICONTROL Nouveau train de données]**.

   1. Dans la liste déroulante **[!UICONTROL Schéma d’événement]**, sélectionnez le schéma d&#39;événement d’expérience créé précédemment, puis cliquez sur **[!UICONTROL Enregistrer]**.

      ![](assets/decision-rule-context-datastream.png)

   1. Cliquez sur **[!UICONTROL Ajouter un service]** et sélectionnez le service « Adobe Experience Platform ». Dans la liste déroulante **[!UICONTROL Jeu de données d’événement]**, sélectionnez le jeu de données d’événement créé précédemment et activez l’option **[!UICONTROL Adobe Journey Optimizer]**.

      ![](assets/decision-rules-context-datastream-service.png)

Une fois le train de données enregistré, les informations du jeu de données sélectionné sont automatiquement récupérées et intégrées dans Experience Decisioning et deviennent généralement disponibles dans les 24 heures.

Pour plus d’informations sur l’utilisation d’Adobe Experience Platform, consultez les ressources suivantes :

* [Schémas de modèle de données d’expérience (XDM)](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [Jeux de données](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [Trains de données](https://experienceleague.adobe.com/fr/docs/experience-platform/datastreams/overview){target="_blank"}
