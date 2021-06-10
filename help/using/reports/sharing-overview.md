---
title: Présentation du partage des étapes du parcours
description: Présentation du partage des étapes du parcours
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: ht
source-wordcount: '424'
ht-degree: 100%

---

# Créer des rapports de parcours{#design-jo-reports}

![](../assets/do-not-localize/badge.png)

Outre les [rapports en temps réel](live-report.md) et les [fonctionnalités de reporting global](global-report.md) intégrées, [!DNL Journey Optimizer] peut automatiquement envoyer des données de performances de parcours à Adobe Experience Platform afin qu’elles soient combinées à d’autres données à des fins d’analyse.

>[!NOTE]
>
>Cette fonction n’est pas activée par défaut sur toutes les instances nouvellement déployées. L’activation est effectuée sur demande.

Par exemple, vous avez configuré un parcours qui envoie plusieurs e-mails. Cette fonctionnalité permet de combiner les données de [!DNL Journey Optimizer] avec des données d’événements situés en aval, comme le nombre de conversions réalisées, le nombre d’engagements survenus sur le site web ou le nombre de transactions effectuées dans le magasin. Les informations de parcours sont combinées avec les données d’Adobe Experience Platform, à partir d’autres propriétés numériques ou de propriétés hors ligne, pour offrir une vue plus complète des performances.

[!DNL Journey Optimizer] crée automatiquement les schémas et les flux nécessaires dans les jeux de données d’Adobe Experience Platform pour chaque étape d’un parcours individuel. Un événement d’étape correspond à un individu qui se déplace d’un nœud à un autre d’un parcours. Par exemple, dans le cadre d’un parcours comportant un événement, une condition et une action, trois événements d’étape sont envoyés à Adobe Experience Platform.

La liste des champs XDM transmis est complète. Certains contiennent des codes générés par le système et d’autres portent des noms conçus pour être lisibles. Il peut s’agir, par exemple, du libellé de l’activité de parcours ou du statut de l’étape : nombre de fois où une action a expiré ou s’est terminée par une erreur.

>[!CAUTION]
>
>Les jeux de données ne peuvent pas être activés pour le service de profil en temps réel. Assurez-vous que le bouton bascule **[!UICONTROL Profil]** est désactivé..

Les parcours envoient les données au fur et à mesure, en flux continu. Vous pouvez appliquer des requêtes à ces données à l’aide du service Requêtes. Vous pouvez vous connecter à Customer Journey Analytics ou à d’autres outils de BI pour visualiser les données concernant ces étapes.

Les schémas suivants sont créés :

* Schéma d’événement de profil d’étape du parcours pour [!DNL Journey Orchestration] - Événements d’expérience pour les étapes d’un parcours avec un mappage d’identité à utiliser pour le mappage avec un participant individuel au parcours.
* Schéma d’événement d’étape du parcours pour [!DNL Journey Orchestration] - Événement d’étape du parcours lié à des métadonnées de parcours.
* Schéma du parcours avec champs de parcours pour [!DNL Journey Orchestration] - Métadonnées servant à décrire les parcours.

![](../assets/sharing1.png)

![](../assets/sharing2.png)

Les jeux de données suivants sont transmis :

* Schéma d’événement de profil d’étape du parcours pour [!DNL Journey Orchestration]
* Événements d’étape du parcours
* Parcours

![](../assets/sharing3.png)

Les listes des champs XDM transmis à Adobe Experience Platform sont détaillées ici :

* [Champs communs des événements journeySteps](../reports/sharing-common-fields.md)
* [Champs d’exécution d’action des événements journeyStep](../reports/sharing-execution-fields.md)
* [Champs de récupération des données des événements journeyStep](../reports/sharing-fetch-fields.md)
* [Champs d’identité des événements journeyStep](../reports/sharing-identity-fields.md)
* [Champs du parcours](../reports/sharing-journey-fields.md)

Pour plus d’informations sur le reporting des événements d’étape à Adobe Experience Platform, regardez ce [tutoriel vidéo](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/reporting-step-events-to-adobe-experience-platform.html?lang=fr).
