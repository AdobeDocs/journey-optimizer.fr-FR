---
title: Surveiller vos expériences web
description: Découvrir comment surveiller vos expériences web dans Journey Optimizer
feature: Web Channel, Reporting, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: d89795bb-c51d-4d1f-b7ed-2b2c5d278922
TQID: https://experienceleague.adobe.com/CEjKwnKx1ixUKA-mO7FfWGXaW9FyO-I-ZYyYm0scs88
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c618a0dc-1818-4c6d-9916-0d92e6796f24id: d056adbe-402d-4f42-9746-f3d424e598b1
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: f8905d41c1ec293d453f3f3992c4f91b94c3357f
workflow-type: tm+mt
source-wordcount: 366
ht-degree: 79%

---

# Surveiller vos expériences web {#monitor-web-experiences}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment surveiller vos expériences web actives dans Adobe Journey Optimizer en vérifiant les rapports web et en configurant le suivi des clics sur des éléments de page spécifiques.

>[!ENDSHADEBOX]

## Vérifier les rapports web {#check-web-reports}

Une fois votre expérience web activée, vous pouvez vérifier l’onglet **[!UICONTROL Web]** du [rapport de parcours](../reports/journey-global-report-cja-web.md) et du [rapport de campagne](../reports/campaign-global-report-cja-web.md) pour comparer des éléments tels que le nombre d’impressions, le taux de clics et le nombre d’engagements de votre page web.

<!--You can check the **[!UICONTROL Web]** tab of the campaign reports. Learn more about the campaign web [live report](../reports/campaign-live-report.md#web-tab) and [global report](../reports/campaign-global-report-cja.md#web).-->

Pour améliorer davantage la surveillance de l’expérience web, vous pouvez également effectuer le suivi des clics sur n’importe quel élément spécifique de votre site web. Vous pouvez ainsi afficher le nombre de clics sur cet élément dans les rapports web. [Voici comment procéder.](#use-click-tracing)

## Utiliser le suivi des clics {#use-click-tracking}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_click_tracking"
>title="Utiliser le suivi des clics"
>abstract="Effectuez le suivi des clics sur n’importe quel élément de votre page web pour surveiller les interactions utilisateur. Sélectionnez un élément, choisissez **Cliquer sur l’élément de suivi** dans le menu contextuel, puis ajoutez un libellé significatif. Les données suivies apparaissent dans vos rapports web, ce qui vous aide à comprendre comment les utilisateurs interagissent avec votre contenu."

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
