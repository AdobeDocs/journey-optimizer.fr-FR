---
solution: Journey Optimizer
product: journey optimizer
title: Présentation du partage des étapes du parcours
description: Présentation du partage des étapes du parcours
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Création de rapports de parcours {#design-jo-reports}

En complément de [rapports en temps réel](live-report.md) et intégré [fonctionnalités de création de rapports globales](global-report.md), [!DNL Journey Optimizer] peut envoyer automatiquement des données de performances de parcours à Adobe Experience Platform afin qu’elles puissent être combinées à d’autres données à des fins d’analyse.

>[!NOTE]
>
>Cette fonction est activée par défaut sur toutes les instances pour les événements d’étapes du parcours. Vous ne pouvez pas modifier ni mettre à jour les schémas et les jeux de données créés lors de la mise en service des événements d’étape. Par défaut, ces schémas et jeux de données sont en lecture seule.

Par exemple, vous avez configuré un parcours qui envoie plusieurs emails. Cette fonctionnalité vous permet de combiner des [!DNL Journey Optimizer] des données avec des données d’événement en aval, telles que le nombre de conversions réalisées, le nombre d’engagements survenus sur le site web ou le nombre de transactions effectuées dans le magasin. Les informations de parcours peuvent être combinées avec les données d’Adobe Experience Platform, à partir d’autres propriétés numériques ou de propriétés hors ligne, afin d’offrir une vue plus complète des performances.

[!DNL Journey Optimizer] crée automatiquement les schémas et les flux nécessaires dans les jeux de données d’Adobe Experience Platform pour chaque étape d’un parcours individuel. Un événement d’étape correspond à un individu qui se déplace d’un noeud à un autre dans un parcours. Par exemple, dans un parcours comportant un événement, une condition et une action, trois événements d’étape sont envoyés à Adobe Experience Platform.

La liste des champs XDM transmis est complète. Certains contiennent des codes générés par le système et d’autres ont des noms conviviaux lisibles. Par exemple, le libellé de l’activité de parcours ou l’état de l’étape : nombre de fois où une action a expiré ou s’est terminée par une erreur.

>[!CAUTION]
>
>Les jeux de données ne peuvent pas être activés pour le service de profil en temps réel. Assurez-vous que la variable **[!UICONTROL Profile]** est désactivé.

[!DNL Journey Optimizer] envoie les données au fur et à mesure, en flux continu. Vous pouvez interroger ces données à l’aide de Query Service. Vous pouvez vous connecter à Customer Journey Analytics ou à d’autres outils de BI pour afficher les données liées à ces étapes.

Les schémas suivants sont créés :

* Schéma d’événement d’étape du parcours pour [!DNL Journey Orchestration] - Événement d’étape du parcours lié à des métadonnées de parcours.
* Schéma du parcours avec champs de parcours pour [!DNL Journey Orchestration] - Métadonnées de parcours pour décrire les parcours.

![](assets/sharing1.png)

![](assets/sharing2.png)

Les jeux de données suivants sont transmis :

* Événements d’étape du parcours
* Parcours

![](assets/sharing3.png)

Les listes des champs XDM transmis à Adobe Experience Platform sont détaillées ici :

* [Liste des champs d’événement d’étape](../reports/sharing-field-list.md)
* [Champs d’événement d’étape hérités](../reports/sharing-legacy-fields.md)

## Intégration à Customer Journey Analytics {#integration-cja}

[!DNL Journey Optimizer] Les événements d’étape peuvent être liés à d’autres jeux de données dans [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html){target=&quot;_blank&quot;}.

Le workflow général est le suivant :

* [!DNL Customer Journey Analytics] ingère le jeu de données &quot;Événement d’étape du parcours&quot;.
* Le **profileID** Le champ associé &quot;Schéma d’événement d’étape du parcours pour Journey Orchestration&quot; est défini comme un champ d’identité. Dans [!DNL Customer Journey Analytics], vous pouvez ensuite lier ce jeu de données à tout autre jeu de données ayant la même valeur que l’identifiant basé sur la personne.
* Pour utiliser ce jeu de données dans [!DNL Customer Journey Analytics], pour l’analyse des parcours cross-canal, reportez-vous à la section [Documentation de Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target=&quot;_blank&quot;}.

