---
solution: Journey Optimizer
product: journey optimizer
title: Rapport de campagne
description: Découvrez comment utiliser les données de campagne du rapport de campagne.
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: b74d3137-2dd9-4302-a56e-73503d318d18
TQID: https://experienceleague.adobe.com/-1IfHcdK07JLG54DYR1GNNN-sU0VyHjfBjCLbNdKA-8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 647
ht-degree: 91%

---

# Rapport de campagne {#campaign-global-report-cja}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment lire le rapport de campagne dans Adobe Journey Optimizer pour consulter les KPI, la présentation et le funnel de la campagne, les liens suivis et les performances de ciblage sur tous les canaux utilisés dans votre campagne.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

Vous pouvez accéder au rapport de campagne en cliquant sur le bouton **[!UICONTROL Rapports]** de votre campagne, puis en sélectionnant **[!UICONTROL Afficher le rapport de toutes les périodes]**. [En savoir plus](report-gs-cja.md)

![](assets/report-access.png)

>[!ENDSHADEBOX]

## KPI de campagne {#campaign-kpis}

![](assets/cja-email-kpis.png)

Les indicateurs clés de performances (KPI) **[!UICONTROL Campagne]** fonctionnent comme un tableau de bord global, fournissant une analyse des mesures essentielles associées à votre campagne. Cela inclut des détails tels que le nombre de clics et le nombre de messages diffusés, ce qui vous offre des informations complètes sur l’efficacité et le niveau d’engagement de votre campagne.

Les KPI varient en fonction des canaux utilisés dans votre campagne.

+++ En savoir plus sur les mesures des KPI de campagne

* **[!UICONTROL Taux de clics]** : pourcentage d’utilisateurs et d’utilisatrices ayant interagi avec le message.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu de votre message.

* **[!UICONTROL Diffusés]** : nombre d’e-mails envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Affichages]** : nombre de fois que le message a été ouvert.

+++

>[!AVAILABILITY]
>Les campagnes orchestrées ne prennent en charge que les canaux SMS, E-mail et Notification push. Autres canaux (in-app, web, courrier, etc.) ne sont pas disponibles dans les campagnes orchestrées et n’apparaissent pas dans les rapports.

### Vue d’ensemble de la campagne {#delivery-global}

![](assets/cja-campaign-overview.png)

Le tableau **[!UICONTROL Vue d’ensemble de la campagne]** constitue un tableau de bord complet, qui propose une répartition détaillée des mesures clés liées à votre campagne. La section contient des informations essentielles telles que le nombre de profils et les actions diffusées, ce qui vous permet de bien comprendre les performances de votre campagne et l’engagement avec celle-ci.

Notez que les mesures varient en fonction des canaux utilisés dans votre campagne.

+++ En savoir plus sur les mesures de vue d’ensemble de campagne

* **[!UICONTROL Personnes]** : nombre de profils d’utilisateurs et d’utilisatrices identifiés comme cibles de vos messages.

* **[!UICONTROL Taux de clics]** : pourcentage d’utilisateurs et d’utilisatrices ayant interagi avec le message.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu de votre message.

* **[!UICONTROL Clics uniques]** : nombre de profils qui ont cliqué sur un contenu dans votre message.

* **[!UICONTROL Diffusés]** : nombre d’e-mails envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Rebonds pour les canaux sortants]** : nombre total d’erreurs cumulées lors de la procédure d’envoi et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs sortantes]** : nombre total d’erreurs survenues au cours de la procédure d’envoi, empêchant le message d’être envoyé à des profils.

* **[!UICONTROL Exclusions sortantes]** : nombre de profils qui ont été exclus par Adobe Journey Optimizer. [En savoir plus sur la comptabilisation des exclusions](exclusion-list.md#exclusion-list).

* **[!UICONTROL Affichages]** : nombre d’ouvertures du message.

* **[!UICONTROL Affichages uniques]** : nombre dʼouvertures du message, les multiples interactions dʼun même profil ne sont pas prises en compte.

+++

### Entonnoir de résultats de la campagne {#campaign-funnel}

![](assets/cja-campaign-funnel.png)

Le graphe **[!UICONTROL Entonnoir de résultats de la campagne]** présente une analyse détaillée de l’engagement de vos profils avec vos messages, fournissant des informations précieuses sur la manière dont différents profils ont interagi avec votre contenu.

+++ En savoir plus sur les mesures de l’entonnoir de résultats de la campagne

* **[!UICONTROL Diffusés]** : nombre d’e-mails envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu de votre message.
+++

### Libellé des liens de suivi {#campaign-track}

![](assets/cja-campaign-tracked-link.png)

Le tableau **[!UICONTROL Libellé des liens de suivi]** offre des informations essentielles sur l’engagement de vos visiteurs et visiteuses avec les URL incluses dans vos messages, fournissant des informations précieuses sur les liens qui attirent le plus d’interactions.

+++ En savoir plus sur les mesures de libellés des liens de suivi

* **[!UICONTROL Clics uniques]** : nombre de profils qui ont cliqué sur un contenu dans votre message.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu de votre message.

+++

## Vue d’ensemble du ciblage {#targeting}

![](assets/cja-journey-targeting-overview.png)

Si vous configurez des **[!UICONTROL règles de ciblage]** pour votre contenu, le tableau **[!UICONTROL Vue d’ensemble du ciblage]** fournit une vue détaillée des mesures d’engagement clés, montrant comment les profils ciblés de chaque règle ont interagi avec votre contenu.

➡️ [En savoir plus sur les règles de ciblage](../content-management/optimization-targeting.md)

+++ En savoir plus sur les mesures du tableau Vue d’ensemble du ciblage

* **[!UICONTROL Personnes]** : nombre de profils d’utilisateurs et d’utilisatrices identifiés comme cibles de vos événements.

* **[!UICONTROL Clics uniques]** : nombre de profils qui ont cliqué sur un contenu dans un e-mail.

* **[!UICONTROL Taux de clics uniques]** : pourcentage de profils ciblés ayant cliqué au moins une fois.

+++
