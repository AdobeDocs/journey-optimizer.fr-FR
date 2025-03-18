---
solution: Journey Optimizer
product: journey optimizer
title: Création de campagnes à plusieurs étapes avec Journey Optimizer
description: Découvrez comment créer une campagne à plusieurs étapes avec Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 271c4739a5537a99da981913606bc9eb099b5139
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 31%

---

# Créer une campagne orchestrée {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Liste de campagnes à étapes multiples"
>abstract="L’onglet **étapes multiples** répertorie toutes les campagnes à étapes multiples. Cliquez sur le nom d’une campagne à étapes multiples pour la modifier. Cliquez sur le bouton **Créer une campagne à étapes multiples** pour ajouter une nouvelle campagne à étapes multiples."

## Conditions préalables

### Autorisations

### Paramètres

Présentation des nouveaux paramètres d’administration > schémas, champs d’exécution, politique de fusion. [En savoir plus](ms-schemas.md)


## Étapes de création

Pour créer une campagne à plusieurs étapes, procédez comme suit :

1. Pour créer une **campagne à plusieurs étapes**, accédez au menu **Campagnes**.

1. Cliquez sur le bouton **[!UICONTROL Créer une campagne à plusieurs étapes]** dans le coin supérieur droit de l’écran.

1. Dans la boîte de dialogue Campagne à plusieurs étapes **Propriétés**, sélectionnez le modèle à utiliser pour créer la campagne à plusieurs étapes (vous pouvez également utiliser le modèle intégré par défaut). [En savoir plus sur les modèles de campagne à plusieurs étapes](#campaign-templates).

1. Saisissez un libellé pour la campagne à plusieurs étapes. En outre, nous vous recommandons vivement d’ajouter une description à votre campagne à plusieurs étapes, dans le champ dédié de la section **[!UICONTROL Options supplémentaires]** de l’écran.

1. Développez la section **[!UICONTROL Options supplémentaires]** pour configurer d’autres paramètres pour la campagne à plusieurs étapes.

1. Cliquez sur le bouton **[!UICONTROL Créer une campagne à plusieurs étapes]** pour confirmer la création de votre campagne à plusieurs étapes.

Votre campagne à plusieurs étapes est maintenant créée et disponible dans la liste des workflows. Vous pouvez maintenant accéder à sa zone de travail visuelle et commencer à ajouter, configurer et orchestrer les tâches qu’il exécutera. [Découvrez comment orchestrer des activités de campagne à plusieurs étapes](orchestrate-activities.md).

## Utiliser des modèles de campagnes à étapes multiples {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Modèles de campagnes à étapes multiples"
>abstract="Les modèles de campagnes à étapes multiples contiennent des activités et des paramètres préconfigurés qui peuvent être réutilisés pour créer d’autres campagnes à étapes multiples."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Propriétés des campagnes à étapes multiples"
>abstract="Les modèles de campagnes à étapes multiples contiennent des activités et des paramètres préconfigurés qui peuvent être réutilisés pour créer d’autres campagnes à étapes multiples. Dans cet écran, saisissez le libellé du modèle de campagne à étapes multiples et paramétrez-la, notamment avec son nom interne, son dossier et ses dossiers d’exécution, son fuseau horaire et son groupe de supervision."

Les modèles de campagnes à étapes multiples contiennent des activités et des paramètres préconfigurés qui peuvent être réutilisés pour créer d’autres campagnes à étapes multiples. Vous pouvez sélectionner le modèle de votre campagne à plusieurs étapes dans les propriétés de la campagne à plusieurs étapes, lors de la création d’une campagne à plusieurs étapes. Un modèle vide est fourni par défaut.

Vous pouvez créer un modèle à partir d’une campagne à plusieurs étapes existante ou créer un modèle à partir de zéro. Les deux méthodes sont présentées ci-dessous.

>[!BEGINTABS]

>[!TAB Créer un modèle à partir d’une campagne existante à plusieurs étapes]

Pour créer un modèle de campagne à plusieurs étapes à partir d&#39;une campagne existante à plusieurs étapes, procédez comme suit :

1. Ouvrez le menu **Campagne** et accédez à la campagne à plusieurs étapes à enregistrer en tant que modèle.
1. Cliquez sur les trois points situés à droite du nom de la campagne à plusieurs étapes, puis choisissez **Copier comme modèle**.
1. Dans la fenêtre contextuelle, confirmez la création du modèle.
1. Dans la zone de travail du modèle de campagne à plusieurs étapes, cochez, ajoutez et configurez les activités selon vos besoins.
1. Accédez aux paramètres, à partir du bouton **Paramètres**, pour modifier le nom du modèle de campagne à plusieurs étapes, puis saisissez une description.
1. Sélectionnez le **dossier** et le **dossier d’exécution** du modèle. Le dossier correspond à l’emplacement d’enregistrement du modèle de campagne à plusieurs étapes. Le dossier d’exécution est le dossier dans lequel les campagnes à plusieurs étapes créées à partir de ce modèle sont enregistrées.
1. Enregistrez vos modifications.

Le modèle de campagne à plusieurs étapes est désormais disponible dans la liste des modèles. Vous pouvez créer une campagne à plusieurs étapes basée sur ce modèle. Cette campagne à plusieurs étapes sera préconfigurée avec les paramètres et activités définis dans le modèle.


>[!TAB Créer un modèle à partir de zéro]


Pour créer entièrement un modèle de campagne à plusieurs étapes, procédez comme suit :

1. Ouvrez le menu **Campagne** et accédez à l’onglet **Modèles**. La liste des modèles de campagne à plusieurs étapes disponibles s’affiche.
1. Cliquez sur le bouton **[!UICONTROL Créer un modèle]** dans le coin supérieur droit de l’écran.
1. Saisissez le libellé et ouvrez les options supplémentaires pour saisir une description de votre modèle de campagne à plusieurs étapes.
1. Sélectionnez le dossier et le dossier d’exécution du modèle. Le dossier correspond à l’emplacement d’enregistrement du modèle de campagne à plusieurs étapes. Le dossier d’exécution est le dossier dans lequel les campagnes à plusieurs étapes créées à partir de ce modèle sont enregistrées.
1. Cliquez sur le bouton **Créer** pour confirmer vos paramètres.
1. Dans la zone de travail du modèle de campagne à plusieurs étapes, ajoutez et configurez les activités selon vos besoins.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Enregistrez vos modifications.

Le modèle de campagne à plusieurs étapes est désormais disponible dans la liste des modèles. Vous pouvez créer une campagne à plusieurs étapes basée sur ce modèle. Cette campagne à plusieurs étapes sera préconfigurée avec les paramètres et activités définis dans le modèle.

>[!ENDTABS]
