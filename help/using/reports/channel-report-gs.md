---
solution: Journey Optimizer
product: journey optimizer
title: Rapports sur les canaux
description: Prise en main des rapports Canal
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: e812621c0b365e07432f6b517a012cf59c37f01f
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 15%

---

# Prise en main des rapports Canal {#channel-report-gs}

Les rapports Canal constituent un puissant outil qui fournit un aperçu complet des mesures de trafic et d’engagement dans un rapport unifié pour chaque canal, englobant toutes les actions de tous les Parcours et campagnes. Il est divisé en différents widgets, chacun d’eux fournissant une vue spécifique des performances de votre campagne ou de votre parcours.

Les rapports Canal sont entièrement personnalisables. Vous pouvez donc redimensionner ou supprimer des widgets pour créer un tableau de bord qui répond à vos besoins. Vous pouvez également exporter les données du rapport vers un PDF ou un fichier CSV pour une analyse plus approfondie.

En savoir plus sur les différents widgets et mesures disponibles pour les rapports Canal dans cette [page](channel-report.md).

## Avant de commencer {#manage-reports-prereq}

Avant de commencer, vérifiez que vous avez accès au **[!UICONTROL Rapports]** .

Si vous ne pouvez pas voir la variable **[!UICONTROL Rapports]** , vos droits d’accès doivent être étendus pour inclure la variable **[!UICONTROL Affichage des rapports Canal]** autorisation. Vous pouvez étendre vos propres autorisations si vous avez accès à Adobe Experience Platform. [Autorisations](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=fr){target="_blank"} pour votre organisation. Si ce n’est pas le cas, contactez votre administrateur Adobe Journey Optimizer.

+++Découvrez comment attribuer une autorisation de rapport

Notez que cette autorisation est incluse dans la version intégrée suivante : **[!UICONTROL Rôles]**: gestionnaire de campagnes, approbateur de campagnes, visionneuse de campagnes et administrateur de campagnes.

Pour attribuer l’autorisation correspondante à votre **[!UICONTROL Rôle]**:

1. Dans la [!DNL Permissions] produit, accédez à la **[!UICONTROL Rôles]** et sélectionnez le rôle que vous souhaitez mettre à jour avec la nouvelle **[!UICONTROL Affichage des rapports Canal]** autorisation.

1. À partir du tableau de bord **[!UICONTROL Rôle]**, cliquez sur **[!UICONTROL Modifier]**.

   ![](assets/channel_permission_1.png)

1. Faites glisser et déposez le **[!UICONTROL Rapport]** ressource pour attribuer une autorisation.

   Dans la **[!UICONTROL Rapport]** menu déroulant des ressources, sélectionnez l’option **[!UICONTROL Affichage des rapports Canal]** autorisation.

   ![](assets/channel_permission_2.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Utilisateurs affectés à cette tâche **[!UICONTROL Rôle]** peuvent désormais accéder à la variable **[!UICONTROL Rapports]** .

+++

## Gérer le tableau de bord des rapports {#manage-reports}

Pour accéder aux rapports Canal et les gérer, procédez comme suit :

1. Accédez au **[!UICONTROL Rapports]** dans le **[!UICONTROL Gestion des parcours]** .

   ![](assets/channel_report_1.png)

1. Dans votre tableau de bord, choisissez une **Début** et **[!UICONTROL Heure de fin]** pour cibler des données spécifiques.

1. Dans la **[!UICONTROL Action de]** , choisissez si vous souhaitez cibler les campagnes, les Parcours ou les deux.

   ![](assets/channel_report_2.png)

1. Cliquez sur **[!UICONTROL Modifier]** pour redimensionner ou supprimer des widgets afin de créer un tableau de bord qui répond à vos besoins spécifiques.

   ![](assets/channel_report_3.png)

1. Une fois satisfait de l&#39;ordre d&#39;affichage et de la taille de vos widgets, cliquez sur **[!UICONTROL Enregistrer]**.

1. Selon le widget, vous pouvez choisir de basculer d’un tableau, d’un graphique à barres ou d’un anneau à l’autre.

1. Cliquez sur l’icône de pourcentage pour afficher vos données sous forme de taux.

   ![](assets/channel_report_4.png)

## Exporter vos rapports {#export-reports}

Vous pouvez facilement exporter vos différents rapports au format PDF ou CSV, ce qui vous permet de les partager, de les manipuler ou de les imprimer. Les onglets suivants décrivent les étapes détaillées pour exporter les rapports Canal :

>[!BEGINTABS]

>[!TAB Exporter votre rapport sous la forme d’un fichier PDF]

1. Dans votre rapport, cliquez sur **[!UICONTROL Exporter]** et sélectionnez **[!UICONTROL Fichier PDF]**.

1. Dans la fenêtre Imprimer, configurez votre document selon vos besoins. Notez que les options peuvent varier en fonction de votre navigateur.

1. Choisissez d’imprimer ou d’enregistrer votre rapport en tant que PDF.

1. Localisez le dossier dans lequel vous souhaitez enregistrer votre fichier, renommez-le si nécessaire, puis cliquez sur Enregistrer.

Votre rapport peut maintenant être affiché ou partagé dans un fichier PDF.

>[!TAB Exportation de votre rapport au format CSV]

1. Dans votre rapport, cliquez sur **[!UICONTROL Exporter]** et sélectionnez **[!UICONTROL fichier CSV]** pour générer un fichier CSV au niveau du rapport global.

1. Vous pouvez également choisir d’exporter des données à partir d’un widget spécifique. Cliquez sur **[!UICONTROL Exportation des données de widget au format CSV]** en regard du widget sélectionné.

1. Votre fichier est automatiquement téléchargé et peut se trouver dans vos fichiers locaux.

   Si vous avez généré le fichier au niveau du rapport, il contient des informations détaillées pour chaque widget, notamment son titre et ses données.

   Si vous avez généré le fichier au niveau du widget, il fournit spécifiquement des données pour le widget sélectionné.

>[!ENDTABS]
