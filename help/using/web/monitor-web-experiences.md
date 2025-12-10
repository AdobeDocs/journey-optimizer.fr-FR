---
title: Surveiller vos expériences web
description: Découvrir comment surveiller vos expériences web dans Journey Optimizer
feature: Web Channel, Reporting, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: d89795bb-c51d-4d1f-b7ed-2b2c5d278922
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 100%

---

# Surveiller vos expériences web {#monitor-web-experiences}

## Vérifier les rapports web {#check-web-reports}

Une fois votre expérience web activée, vous pouvez vérifier l’onglet **[!UICONTROL Web]** du [rapport de parcours](../reports/journey-global-report-cja-web.md) et du [rapport de campagne](../reports/campaign-global-report-cja-web.md) pour comparer des éléments tels que le nombre d’impressions, le taux de clics et le nombre d’engagements de votre page web.

<!--You can check the **[!UICONTROL Web]** tab of the campaign reports. Learn more about the campaign web [live report](../reports/campaign-live-report.md#web-tab) and [global report](../reports/campaign-global-report-cja.md#web).-->

Pour améliorer davantage la surveillance de l’expérience web, vous pouvez également effectuer le suivi des clics sur n’importe quel élément spécifique de votre site web. Vous pouvez ainsi afficher le nombre de clics sur cet élément dans les rapports web. [Voici comment procéder.](#use-click-tracing)

## Utiliser le suivi des clics {#use-click-tracking}

Le designer web vous permet de sélectionner n’importe quel élément de votre site web et d’effectuer le suivi des clics sur cet élément.

Ces informations peuvent se révéler utiles pour améliorer l’expérience des utilisateurs et utilisatrices de votre site web. Par exemple, si les [rapports web](../reports/campaign-global-report-cja-web.md) affichent que de nombreux utilisateurs et utilisatrices cliquent sur un élément qui n’est pas réellement cliquable, vous pouvez ajouter un lien à cet élément.

1. Sélectionnez un élément dans votre page et choisissez **[!UICONTROL Clic sur l’élément de suivi]** dans le menu contextuel.

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >Tout élément, cliquable ou non, peut être sélectionné.

1. L’action suivie correspondante s’affiche automatiquement dans le volet **[!UICONTROL Suivi des clics]** sur la gauche.

   ![](assets/web-designer-click-track-pane.png)

1. Ajoutez un libellé significatif pour gérer tous les éléments suivis et les retrouver facilement dans les rapports. Le **[!UICONTROL sélecteur CSS]** affiche des informations sur la localisation de l’élément sélectionné.

1. Répétez les étapes ci-dessus pour sélectionner autant d’autres éléments que nécessaire pour le suivi des clics. Les actions correspondantes sont toutes répertoriées dans le volet de gauche.

   ![](assets/web-designer-click-tracking-actions.png)

1. Pour supprimer le suivi des clics sur un élément, sélectionnez l’icône de suppression correspondante.

Une fois votre campagne activée, vous pouvez vérifier le nombre de clics sur chaque élément dans le [rapport dynamique](../reports/campaign-live-report.md#web-tab) et le [rapport Customer Journey Analytics](../reports/campaign-global-report-cja-web.md) de la campagne web.
