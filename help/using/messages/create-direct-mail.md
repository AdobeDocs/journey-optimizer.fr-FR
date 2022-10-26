---
title: Créer un message de courrier
description: Découvrez comment créer un courrier dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: fe6fedfd3fb0a8b083f7b047e2879ef6510b041b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Créer un message de courrier {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Création de publipostage direct"
>abstract="Créez des messages de courrier dans des campagnes planifiées et concevez les fichiers d&#39;extraction requis par les opérateurs de services postaux pour envoyer du courrier à vos clients."

Le canal Courrier est un canal off-line qui vous permet de personnaliser et de générer les fichiers d’extraction requis par les opérateurs de services postaux pour envoyer du courrier à vos clients.

Lorsque vous créez un courrier, Journey Optimizer génère un fichier contenant tous les profils ciblés et les données sélectionnées (adresse postale, attributs de profil, par exemple). Vous pourrez alors envoyer ce fichier à votre opérateur de services postaux qui prendra en charge l&#39;envoi réel.

Les messages directs ne peuvent être créés que dans le cadre de campagnes planifiées. Elles ne sont pas disponibles pour une utilisation dans des campagnes déclenchées par l’API ou dans des parcours.

>[!IMPORTANT]
>
>Avant d&#39;envoyer un courrier, vérifiez que vous avez configuré :
>* A [configuration du routage des fichiers](../configuration/direct-mail-configuration.md#file-routing-configuration) qui spécifie le serveur sur lequel le fichier d&#39;extraction doit être téléchargé et stocké,
>* A [surface du message courrier](../configuration/direct-mail-configuration.md#direct-mail-surface) qui fera référence à la configuration de routage des fichiers.


## Créer un message de courrier {#create}

Les étapes de création et d&#39;envoi d&#39;un Courrier sont les suivantes :

1. Créez une opération planifiée, puis sélectionnez **[!UICONTROL Canal Courrier]** comme action et choisissez la surface du message à utiliser.

   ![](assets/direct-mail-campaign.png)

1. Cliquez sur **[!UICONTROL Créer]** définissez ensuite des informations de base sur votre campagne (nom, description). [Découvrez comment configurer une campagne](../campaigns/create-campaign.md)

   ![](assets/direct-mail-edit.png)

1. Cliquez sur le bouton **[!UICONTROL Modifier le contenu]** pour configurer le fichier d&#39;extraction à envoyer à votre opérateur de services postaux.

1. Définissez le nom du fichier d’extraction dans la variable **[!UICONTROL Nom du fichier]** champ .

   Vous pouvez parfois avoir besoin d&#39;ajouter des informations au début ou à la fin du fichier d&#39;extraction. Pour ce faire, utilisez la méthode **[!UICONTROL Remarques]** puis indiquez si vous souhaitez inclure la note en tant qu’en-tête ou pied de page.

   <!--Click on the button to the right of the Output file field and enter the desired label. You can use personalization fields, content blocks and dynamic text (see Defining content). For example, you can complete the label with the delivery ID or the extraction date.-->

   ![](assets/direct-mail-properties.png)

1. Utilisez la zone de gauche pour définir les informations à afficher en colonnes dans le fichier d&#39;extraction :

   1. Cliquez sur le bouton **[!UICONTROL Ajouter]** pour ajouter une nouvelle colonne, puis sélectionnez-la dans la liste.

   1. Dans le **[!UICONTROL Formatage]** , indiquez un libellé pour la colonne, puis définissez les attributs de profil à afficher à l’aide de la fonction [Éditeur d’expression](../personalization/personalization-build-expressions.md).

      ![](assets/direct-mail-content.png)

   1. Pour trier le fichier d’extraction à l’aide de la colonne sélectionnée, faites basculer le **[!UICONTROL Tri par]** sur . Le **[!UICONTROL Trier par]** s’affiche alors en regard du libellé de la colonne dans la structure du fichier.

1. Répétez ces étapes pour ajouter autant de colonnes que nécessaire pour créer votre fichier d&#39;extraction. Vous pouvez ajouter jusqu’à 50 colonnes.

   ![](assets/direct-mail-complete.png)

   Vous pouvez supprimer une colonne à tout moment en la sélectionnant et en cliquant sur le bouton **[!UICONTROL Supprimer]** à partir du bouton **[!UICONTROL Formatage]** .

1. Une fois le contenu du courrier défini, effectuez le paramétrage de votre opération.

   Lorsque la campagne démarrera, le fichier d&#39;extraction sera automatiquement généré et téléchargé sur le serveur spécifié dans votre [configuration du routage des fichiers](../configuration/direct-mail-configuration.md).
