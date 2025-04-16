---
solution: Journey Optimizer
product: journey optimizer
title: Création de campagnes orchestrées avec Journey Optimizer
description: Découvrez comment créer une campagne orchestrée avec Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 13%

---

# Créer une campagne orchestrée {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Liste des campagnes orchestrées"
>abstract="L’onglet **à plusieurs étapes** répertorie toutes les campagnes orchestrées. Cliquez sur le nom d’une campagne orchestrée pour la modifier. Utilisez le bouton **Créer une campagne orchestrée** pour ajouter une nouvelle campagne orchestrée."

## Conditions préalables

### Autorisations

### Paramètres

Présentation des nouveaux paramètres d’administration > schémas, champs d’exécution, politique de fusion. [En savoir plus](ms-schemas.md)


## Étapes de création

Pour créer une campagne orchestrée, procédez comme suit :

1. Pour créer une **campagne orchestrée**, accédez au menu **Campagnes**.

1. Cliquez sur le bouton **[!UICONTROL Créer une campagne orchestrée]** dans le coin supérieur droit de l’écran.

1. Dans la boîte de dialogue Campagne orchestrée **Propriétés**, sélectionnez le modèle à utiliser pour créer la campagne orchestrée (vous pouvez également utiliser le modèle intégré par défaut). [En savoir plus sur les modèles de campagne orchestrés](#campaign-templates).

1. Saisissez un libellé pour la campagne orchestrée. En outre, nous vous recommandons vivement d’ajouter une description à votre campagne orchestrée, dans le champ dédié de la section **[!UICONTROL Options supplémentaires]** de l’écran.

1. Développez la section **[!UICONTROL Options supplémentaires]** pour configurer d’autres paramètres pour la campagne orchestrée.

1. Cliquez sur le bouton **[!UICONTROL Créer une campagne orchestrée]** pour confirmer la création de votre campagne orchestrée.

Votre campagne orchestrée est maintenant créée et disponible dans la liste des workflows. Vous pouvez maintenant accéder à sa zone de travail visuelle et commencer à ajouter, configurer et orchestrer les tâches qu’il exécutera. [Découvrez comment orchestrer des activités de campagne orchestrées](orchestrate-activities.md).

## Utiliser des modèles de campagne orchestrés {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Modèles de campagne orchestrés"
>abstract="Les modèles de campagne orchestrée contiennent des paramètres préconfigurés et des activités qui peuvent être réutilisés pour créer une campagne orchestrée."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Propriétés de campagne orchestrées"
>abstract="Les modèles de campagne orchestrée contiennent des paramètres préconfigurés et des activités qui peuvent être réutilisés pour créer de nouvelles campagnes orchestrées. Dans cet écran, saisissez le libellé du modèle de campagne orchestré et configurez ses paramètres tels que son nom interne, ses dossiers et d&#39;exécution, son fuseau horaire et son groupe de superviseurs."

Les modèles de campagne orchestrée contiennent des paramètres préconfigurés et des activités qui peuvent être réutilisés pour créer de nouvelles campagnes orchestrées. Vous pouvez sélectionner le modèle de votre campagne orchestrée dans les propriétés de la campagne orchestrée lors de la création d’une campagne orchestrée. Un modèle vide est fourni par défaut.

Vous pouvez créer un modèle à partir d’une campagne orchestrée existante, ou créer un nouveau modèle à partir de zéro. Les deux méthodes sont présentées ci-dessous.

>[!BEGINTABS]

>[!TAB Créer un modèle à partir d’une campagne orchestrée existante]

Pour créer un modèle de campagne orchestrée à partir d’une campagne orchestrée existante, procédez comme suit :

1. Ouvrez le menu **Campagne** et accédez à la campagne orchestrée pour l’enregistrer en tant que modèle.
1. Cliquez sur les trois points situés à droite du nom de la campagne orchestrée, puis sélectionnez **Copier comme modèle**.
1. Dans la fenêtre contextuelle, confirmez la création du modèle.
1. Dans la zone de travail du modèle de campagne orchestrée, cochez, ajoutez et configurez les activités selon vos besoins.
1. Accédez aux paramètres à partir du bouton **Paramètres** pour modifier le nom du modèle de campagne orchestré, puis saisissez une description.
1. Sélectionnez le **dossier** et le **dossier d’exécution** du modèle. Le dossier correspond à l’emplacement d’enregistrement du modèle de campagne orchestré. Le dossier d’exécution est le dossier dans lequel les campagnes orchestrées créées à partir de ce modèle sont enregistrées.
1. Enregistrez vos modifications.

Le modèle de campagne orchestrée est désormais disponible dans la liste des modèles. Vous pouvez créer une campagne orchestrée basée sur ce modèle. Cette campagne orchestrée sera préconfigurée avec les paramètres et activités définis dans le modèle.


>[!TAB Créer un modèle à partir de zéro]


Pour créer entièrement un modèle de campagne orchestrée, procédez comme suit :

1. Ouvrez le menu **Campagne** et accédez à l’onglet **Modèles**. La liste des modèles de campagnes orchestrées disponibles s’affiche.
1. Cliquez sur le bouton **[!UICONTROL Créer un modèle]** dans le coin supérieur droit de l’écran.
1. Saisissez le libellé et ouvrez les options supplémentaires pour saisir une description du modèle de campagne orchestré.
1. Sélectionnez le dossier et le dossier d’exécution du modèle. Le dossier correspond à l’emplacement d’enregistrement du modèle de campagne orchestré. Le dossier d’exécution est le dossier dans lequel les campagnes orchestrées créées à partir de ce modèle sont enregistrées.
1. Cliquez sur le bouton **Créer** pour confirmer vos paramètres.
1. Dans la zone de travail du modèle de campagne orchestrée, ajoutez et configurez les activités selon vos besoins.

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. Enregistrez vos modifications.

Le modèle de campagne orchestrée est désormais disponible dans la liste des modèles. Vous pouvez créer une campagne orchestrée basée sur ce modèle. Cette campagne orchestrée sera préconfigurée avec les paramètres et activités définis dans le modèle.

>[!ENDTABS]
