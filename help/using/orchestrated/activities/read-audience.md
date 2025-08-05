---
solution: Journey Optimizer
product: journey optimizer
title: À propos de l’activité Lecture d’audience
description: Découvrez comment utiliser l’activité Lecture d’audience dans une campagne orchestrée
exl-id: ef8eba57-cd33-4746-8eb4-5214ef9cbe2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 16%

---


# Lecture d’audience {#read-audience}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_read_audience"
>title="Activité Créer une audience"
>abstract="L’activité **Lecture d’audience** permet de sélectionner l’audience qui va entrer dans la campagne orchestrée. Il peut s’agir d’une audience Adobe Experience Platform existante ou d’une audience extraite d’un fichier CSV. Lors de l’envoi de messages dans le cadre d’une campagne orchestrée, l’audience du message n’est pas définie dans l’activité de canal, mais dans une activité **Lecture d’audience** ou **Créer une audience**."

L&#39;activité **[!UICONTROL Lecture d&#39;audience]** vous permet de récupérer une audience existante, précédemment enregistrée ou importée, et de la réutiliser dans une campagne orchestrée. Cette activité est particulièrement utile pour cibler un ensemble prédéfini de profils sans avoir à exécuter un nouveau processus de segmentation.

Une fois l’audience chargée, vous pouvez éventuellement l’affiner en sélectionnant un champ d’identité unique et en enrichissant l’audience avec des attributs de profil supplémentaires à des fins de ciblage, de personnalisation ou de création de rapports.

## Configuration de l&#39;activité Lecture d&#39;audience {#read-audience-configuration}

Pour configurer l’activité **[!UICONTROL Lecture d’audience]**, procédez comme suit :

1. Avant d’ajouter votre activité **[!UICONTROL Lecture d’audience]**, veillez à sélectionner une **[!UICONTROL Politique de fusion]** dans vos paramètres Campaign.

   ![](../assets/read-audience-6.png)

1. Ajoutez une activité **[!UICONTROL Lecture d’audience]** à votre campagne orchestrée.

   ![](../assets/read-audience-1.png)

1. Saisissez un **[!UICONTROL libellé]** pour votre activité. Ce libellé servira de nom à votre audience.

1. Cliquez sur ![icône de recherche de dossier](../assets/do-not-localize/folder-search.svg) pour sélectionner l’audience que vous souhaitez cibler pour votre campagne orchestrée.

   ![](../assets/read-audience-2.png)

1. Choisissez une **[!UICONTROL Entité&#x200B;]** dans votre dimension de ciblage de campagne. Ce paramètre définit l’entité cible et l’attribut utilisé pour réconcilier l’audience avec la dimension cible.

   ➡️ [Suivez les étapes présentées sur cette page pour créer votre dimension de ciblage de campagne](../target-dimension.md)

   ![](../assets/read-audience-3.png)

1. Sélectionnez [!UICONTROL Ajouter un attribut] pour enrichir votre audience sélectionnée avec des données supplémentaires. Cette étape vous permet d’ajouter des attributs de profil à l’audience, ce qui entraîne une liste de destinataires enrichie de ces attributs.

1. Sélectionnez les **[!UICONTROL Attributs]** à ajouter à votre audience. Le sélecteur d’attributs affiche les champs du **Schéma de profil d’union** :

   * Pour les audiences CSV, cela inclut les attributs **Profil** et les attributs personnalisés au niveau de l’audience. Ces attributs se trouvent sous le chemin de schéma suivant :

     `<audienceid> > _ajobatchjourneystage > audienceEnrichment > CustomerAudienceUpload > <audienceid>`

   * Pour les audiences AEP standard, seuls les attributs **Profil** sont disponibles, car ils ne comportent pas de champs intégrés spécifiques à l’audience.

   >[!NOTE]
   >
   > Bien que certains attributs puissent apparaître dans le sélecteur, leur disponibilité au moment de l’exécution dépend de la réconciliation et de la fusion réussies des données d’audience avec le profil **Adobe Experience Platform**.

   ![](../assets/read-audience-4.png)

Une fois créée, l’audience est disponible en lecture seule et ne peut plus être modifiée. Il ne peut être utilisé qu’une fois le processus de création terminé.

## Exemple

Dans l’exemple ci-dessous, l’activité **[!UICONTROL Lecture d’audience]** permet de récupérer une audience créée et enregistrée précédemment pour les profils s’étant abonnés à la newsletter. L’audience est ensuite enrichie de l’attribut **Loyalty membership** pour permettre le ciblage des utilisateurs qui sont membres inscrits au programme de fidélité.

![](../assets/read-audience-5.png)
