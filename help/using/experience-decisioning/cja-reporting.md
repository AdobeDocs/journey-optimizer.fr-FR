---
title: Rapport sur la prise de décision
description: Découvrez comment créer des rapports sur la prise de décision.
feature: Experience Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="Disponibilité limitée"
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: 841a114610bfee743f5ebb349e3eef6312de0f7b
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 55%

---


# Rapport sur la prise de décision {#decisioning-report}

## Rapports de campagnes basés sur le code {#campaigns}

Une fois l’expérience basée sur le code activée, vous pouvez accéder à des rapports dédiés pour surveiller les indicateurs de performance clés (IPC) en tant que tableau de bord global, ce qui vous permet d’analyser les mesures essentielles associées à votre campagne.

Cela inclut les détails liés aux performances des éléments de décision et la manière dont les utilisateurs ont interagi avec eux. [Découvrez comment utiliser les rapports d’expérience basés sur le code](../reports/campaign-global-report-cja-code.md)

![](../reports/assets/cja-decisioning-item-performance.png)

## Rapports dans Customer Journey Analytics {#cja}

Si vous utilisez Customer Journey Analytics, vous pouvez créer des tableaux de bord de création de rapports personnalisés pour vos campagnes basées sur du code en exploitant la prise de décision.

Suivez les étapes principales ci-dessous : Vous trouverez des informations détaillées sur l’utilisation de Customer Journey Analytics dans la [documentation de Customer Journey Analytics](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-landing){target="_blank"}.

1. Créez et configurez une **connexion** dans Customer Journey Analytics. Vous pouvez ainsi vous connecter au jeu de données pour lequel vous souhaitez établir des rapports. [Découvrir comment créer une connexion](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. Créez une **vue des données** et associez-la à la connexion créée précédemment. Sous l’onglet **[!UICONTROL Composants]**, sélectionnez les champs de schéma appropriés que vous souhaitez afficher dans les rapports. Pour la prise de décision, veillez à inclure les champs **propositioninteraction** et **propositiondisplay** . [Découvrir comment créer et configurer des vues de données](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. Combinez des composants de données, des tableaux et des visualisations dans des **projets Workspace** pour créer et partager des rapports pour votre campagne basée sur du code.[Découvrir comment créer des projets Workspace](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
