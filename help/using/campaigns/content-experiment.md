---
title: Création d’une expérience de contenu
description: Découvrez comment créer une expérience de contenu dans vos campagnes
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---

# Création d’une expérience de contenu {#content-experiment}

La fonctionnalité d’expérience de contenu vous permet de définir plusieurs traitements de diffusion. L’audience ciblée est attribuée de manière aléatoire à chaque traitement afin de déterminer lequel est le plus performant par rapport à la mesure d’intérêt. Vous pouvez choisir de varier le contenu, l’objet ou l’expéditeur de l’email.

Dans l&#39;exemple ci-dessous, la cible de la diffusion a été divisée en deux groupes, représentant chacun 45 % de la population ciblée, et un groupe d&#39;exclusion de 10 %, qui ne recevra pas la diffusion.

Chaque personne de l’audience ciblée recevra une version de l’email, avec un objet qui est l’un des deux suivants :

* une promotion directe d&#39;une offre de 10 % sur la nouvelle collection et une image.
* l’autre ne fait de la publicité que pour une offre spéciale sans spécifier les 10 % de réduction sans image.

L&#39;objectif ici est de voir si les destinataires interagissent avec l&#39;email en fonction de l&#39;expérience reçue. Nous choisirons donc **[!UICONTROL Ouvertures de courrier électronique]** comme mesure d’objectif Principal dans cette expérience de contenu.

![](assets/content_experiment.png)

## Créer votre campagne {#campaign-experiment}

1. Dans la **[!UICONTROL Campagnes]** page, cliquez sur **[!UICONTROL Créer une campagne]**.

   ![](assets/content_experiment_1.png)

1. Sélectionner **[!UICONTROL Email]** puis la fonction **[!UICONTROL Surface]** vous souhaitez utiliser pour cette diffusion. Voir à ce sujet la section [Surfaces des canaux](../configuration/channel-surfaces.md) page.

   ![](assets/content_experiment_2.png)

1. Cliquez sur **[!UICONTROL Créer]**.

1. Configurez les **[!UICONTROL Propriétés]** de votre diffusion :
   * **[!UICONTROL Titre]**
   * **[!UICONTROL Description]**
   * **[!UICONTROL Catégorie]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactionnel]**

1. Pour lancer votre expérience de contenu, activez la fonction **[!UICONTROL Expérience de contenu]** . Le **[!UICONTROL Expérience de contenu]** s’affiche.

   ![](assets/content_experiment_3.png)

1. Configurez les **[!UICONTROL Audience]** et **[!UICONTROL Planification]** des paramètres de vos diffusions. [En savoir plus](create-campaign.md)

1. Cliquez sur **[!UICONTROL Modifier le contenu]** pour commencer à personnaliser vos **[!UICONTROL Traitements]**.

   ![](assets/content_experiment_4.png)

## Créer vos traitements {#treatment-experiment}

1. Dans la **[!UICONTROL Modifier le contenu]** , ajoutez la fenêtre **[!UICONTROL Objet]** pour votre traitement Un e-mail et cliquez sur **[!UICONTROL Enregistrer]**.

   Pour ce traitement, nous spécifions l’offre directement dans la ligne d’objet.

   ![](assets/content_experiment_5.png)

1. Cliquez sur **[!UICONTROL Concepteur d&#39;email]** pour commencer à personnaliser vos diffusions.

   ![](assets/content_experiment_6.png)

1. Après avoir conçu votre email, cliquez sur **[!UICONTROL Enregistrer]** et revenez au **[!UICONTROL Modifier le contenu]** pour créer le traitement B.

1. Dans la **[!UICONTROL Autres actions]** bouton, cliquez **[!UICONTROL Dupliquer]**.

   Vous pouvez également choisir de commencer un nouveau traitement à partir de zéro en cliquant sur le bouton **[!UICONTROL Expérience de contenu]** pour accéder aux options avancées, puis **[!UICONTROL Ajouter un traitement]**.

   ![](assets/content_experiment_7.png)

1. Modifiez la variable **[!UICONTROL Titre]** de votre traitement pour mieux les différencier.

   ![](assets/content_experiment_8.png)

1. Sélectionnez la diffusion email associée à votre nouvellement créé. **[!UICONTROL Traitement]**.

1. Ajoutez la variable **[!UICONTROL Objet]** pour votre diffusion.

   Pour ce traitement, nous choisissons de ne pas spécifier l’offre dans la variable **[!UICONTROL Objet]**.

   ![](assets/content_experiment_9.png)

1. Cliquez sur **[!UICONTROL Concepteur d&#39;email]** pour personnaliser davantage la diffusion Traitement B si nécessaire.

Une fois vos traitements personnalisés, vous pouvez commencer à configurer votre expérience de contenu.

## Configuration de votre expérience de contenu {#configure-experiment}

1. Lorsque les deux diffusions sont personnalisées, à partir de la **[!UICONTROL Modifier le contenu]** fenêtre, sélectionnez **[!UICONTROL Configuration de l’expérience de contenu]**.

   ![](assets/content_experiment_10.png)

1. Sélectionnez les objectifs que vous souhaitez définir pour votre expérience.

   Pour notre expérience, nous sélectionnons **[!UICONTROL Ouverture d’email]** pour tester si les destinataires ouvriront leurs emails si le code promotion se trouve dans la ligne d’objet.

   ![](assets/content_experiment_11.png)

1. Choisissez d’ajouter une **[!UICONTROL Holdout]** à votre diffusion. Ce groupe ne recevra aucun contenu de cette campagne.

   Le fait de basculer sur la barre de bascule représentera automatiquement 10 % de votre population. Vous pouvez ajuster ce pourcentage si nécessaire.

   ![](assets/content_experiment_12.png)

1. Vous pouvez ensuite choisir d’attribuer un pourcentage précis à chaque **[!UICONTROL Traitement]** ou simplement activer la fonction **[!UICONTROL Répartir proportionnellement]** la barre de bascule.

   ![](assets/content_experiment_13.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** lorsque votre configuration est définie.

1. Lorsque votre expérience de contenu est prête, vous pouvez cliquer sur **[!UICONTROL Réviser pour activer]** pour afficher un résumé de l&#39;opération. Les alertes s’affichent si un paramètre est incorrect ou manquant.

   ![](assets/content_experiment_15.png)

1. Vérifiez que votre campagne est correctement configurée, puis cliquez sur **[!UICONTROL Activer]** pour le lancer.

   ![](assets/content_experiment_14.png)

