---
solution: Journey Optimizer
product: journey optimizer
title: Expérience de création de rapports mise à jour
description: Prise en main du rapport complet
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: bfd88d2a-e7b8-4e3b-85a1-4a14b0ba56dc
source-git-commit: a9349cedc4da2a8e76e53f9e2b5185270cda2558
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 66%

---

# Prise en main du rapport complet {#channel-report-gs-cja}

>[!CONTEXTUALHELP]
>id="cja_connections_enable_cja"
>title="Activer Customer Journey Analytics"
>abstract="Pour analyser ce rapport dans Customer Journey Analytics, contactez votre administration pour vous assurer que votre organisation a acheté Customer Journey Analytics et que l’intégration est correctement configurée."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/channels/email/design-email/add-content/content-components#add-content-components" text="Customer Journey Analytics"

La création de rapports Journey Optimizer est fournie avec une interopérabilité améliorée avec les fonctionnalités de Customer Journey Analytics, ce qui permet de normaliser la création de rapports sur les deux plateformes et d’améliorer la cohérence et la fiabilité des données. L’intégration transparente entre Journey Optimizer et Customer Journey Analytics fournit une meilleure visibilité des mesures de performance, ce qui aide les utilisateurs et les utilisatrices à prendre des décisions plus éclairées.

L’accès à ces fonctionnalités de création de rapports dépend du contexte et des domaines de produits :

* **Parcours** - Si vous souhaitez cibler un parcours ou des diffusions dans le cadre d’un parcours, dans le menu **[!UICONTROL Parcours]**, accédez à votre parcours et cliquez sur le bouton **[!UICONTROL Afficher le rapport]**.

  Dans la liste des parcours existants, vous pouvez également sélectionner **[!UICONTROL Rapport]** dans le menu avancé du parcours que vous avez sélectionné. [En savoir plus sur le rapport de parcours](journey-global-report-cja.md)

  ![](assets/gs-cja-report-3.png)

* **Campagnes** - Si vous souhaitez cibler une campagne, dans le menu **[!UICONTROL Campagnes]**, accédez à votre campagne et cliquez sur le bouton **[!UICONTROL Rapports]** puis **[!UICONTROL Afficher le rapport à toute heure]**.

  Dans la liste des campagnes existantes, vous pouvez également sélectionner **[!UICONTROL Rapport]** dans le menu avancé de la campagne que vous avez sélectionnée. [En savoir plus sur le rapport de campagne](campaign-global-report-cja.md)

  ![](assets/gs-cja-report-2.png)

* **Global** - Si vous souhaitez cibler des mesures pour toutes les campagnes et tous les parcours de votre environnement, accédez au rapport **Aperçu** en accédant au menu **[!UICONTROL Rapports]** dans la section **[!UICONTROL Gestion des Parcours]**. [En savoir plus sur le rapport de vue d’ensemble](channel-report-cja.md)

  ![](assets/gs-cja-report-1.png)

>[!IMPORTANT]
>
>Le fuseau UTC est actuellement la norme pour les rapports dans Adobe Journey Optimizer. La possibilité de personnaliser le fuseau horaire des rapports sera disponible dans une prochaine version.

## Prérequis {#prerequisites}

* Si vous ne disposez **pas** de Customer Journey Analytics, ou si vous en disposez mais que vous n’avez **pas** accès à un profil de produit de Customer Journey Analytics, les autorisations sont gérées dans Journey Optimizer. Dans ce cas, vous avez besoin de l’autorisation **[!UICONTROL Afficher les rapports de canal]** ou des rôles associés. [En savoir plus](../administration/permissions.md)

* Si vous **possédez** Customer Journey Analytics et avez accès à un profil de produit Customer Journey Analytics, vous avez besoin des éléments suivants :

   * Autorisations de **[!UICONTROL création d’audience]** et d’**[!UICONTROL affichage d’audience]** pour Customer Journey Analytics. [En savoir plus](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/technotes/access-control){target="_blank"}

   * Autorisation de **[!UICONTROL gestion des profils]** pour Adobe Journey Optimizer. [En savoir plus](../administration/permissions.md)

* Vos vues de données Customer Journey Analytics doivent être configurées avec le paramètre suivant : **Définir comme vue de données par défaut dans Adobe Journey Optimizer**. [En savoir plus sur les vues de données](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}


## Rapports à toute heure par canal

Des rapports globaux à tout moment sont disponibles pour tous vos canaux. Sélectionnez le rapport pour le canal dont vous avez besoin pour obtenir plus de détails.

### Canaux sortants

Sélectionnez un canal sortant pour découvrir les **rapports globaux en tout temps** associés.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="E-mail" src="../channels/assets/do-not-localize/email.png">
<div align="center"><p><strong>Canal e-mail</strong></p><p><a href="campaign-global-report-cja-email.md"><strong>Rapport de campagne</strong></a></p><p><a href="journey-global-report-cja-email.md"><strong>Rapport de parcours</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-sms.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><p><strong>Canal SMS</strong></p><p><a href="campaign-global-report-cja-sms.md"><strong>Rapport de campagne</strong></a></p><p><a href="journey-global-report-cja-sms.md"><strong>Rapport de parcours</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-push.md"><img alt="Notification push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><p><strong>Canal de notification push</strong></p><p><a href="campaign-global-report-cja-push.md"><strong>Rapport de campagne</strong></a></p><p><a href="journey-global-report-cja-push.md"><strong>Rapport de parcours</strong></a></p></div></td>
<td><a href="campaign-global-report-cja-direct.md"><img alt="Courrier" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><p><strong>Canal courrier</strong></p><p><a href="campaign-global-report-cja-direct.md"><strong>Rapport de campagne</strong></a></p><p><a href="journey-global-report-cja-direct.md"><strong>Rapport de parcours</strong></a></p></div></td>
</tr></table>

### Expériences entrantes

Sélectionnez une expérience entrante pour découvrir les **rapports globaux à tout moment** associés.

<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="In-app" src="../channels/assets/do-not-localize/inapp.jpg">
<div align="center"><p><strong>Canal in-app</strong></p><p><a href="campaign-global-report-cja-inapp.md"><strong>Rapport de campagne</strong></a></p><p><a href="journey-global-report-cja-inapp.md"><strong>Rapport de parcours</strong></a></p></div></td>
<td><p><img alt="Web" src="../channels/assets/do-not-localize/web.jpg"></p>
<div align="center"><p><strong>Canal web</strong></p><p><a href="campaign-global-report-cja-web.md"><strong>Rapport de campagne</strong></a></p><p><a href="journey-global-report-cja-web.md"><strong>Rapport de parcours</strong></a></p></div></td>
<td><img alt="Expérience basée sur du code" src="../channels/assets/do-not-localize/code.png">
<div align="center"><p><strong>Expériences basées sur du code</strong></p><p><a href="campaign-global-report-cja-code.md"><strong>Rapport de campagne</strong></a></p><p><a href="campaign-global-report-cja-code.md"><strong>Rapport de parcours</strong></a></p></div></td>
<td><img alt="Cartes de contenu" src="../channels/assets/do-not-localize/cards.png">
<div align="center"><p><strong>Cartes de contenu</strong></p><p><a href="campaign-global-report-cja-content.md"><strong>Rapport de campagne</strong></a></p><p><a href="journey-global-report-cja-content.md"><strong>Rapport de parcours</strong></a></p></div></td>
</tr></table>

## Vidéo pratique{#video}

La vidéo ci-dessous montre comment utiliser le reporting Journey Optimizer amélioré avec Customer Journey Analytics.

>[!VIDEO](https://video.tv.adobe.com/v/3443153?captions=fre_fr)