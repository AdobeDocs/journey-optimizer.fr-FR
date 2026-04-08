---
title: Boîte de réception de conception
description: Concevez une liste de boîte de réception et des vues développées, des modèles et un comportement d’interaction pour les messages de boîte de réception dans Adobe Journey Optimizer.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 0ab71b21-0085-4a93-b319-3c960bd8f7dd
source-git-commit: 2eb2e99e654516fc13a7f98125f48e7e8f672ee3
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Concevoir une boîte de réception {#inbox-design}

La conception de boîte de réception régit la manière dont chaque message est rendu aux profils ciblés dans la surface de boîte de réception. La configuration englobe le modèle de boîte de réception, les présentations de liste et développées, ainsi que les indicateurs de lecture qui distinguent les nouveaux messages de ceux déjà consultés.

Pour connaître la procédure complète de création d’une campagne de boîte de réception, reportez-vous à la section [Création d’une boîte de réception](inbox-create.md).

1. Ouvrez l’onglet **[!UICONTROL Contenu]** de la campagne [Boîte de réception](inbox-create.md) que vous avez créée.

1. Définissez le **[!UICONTROL titre du conteneur]**.

1. Sélectionnez une disposition de boîte de réception :

   * **[!UICONTROL Disposition Liste]** : affiche chaque carte de contenu dans une liste verticale afin que les profils puissent faire défiler les messages et les ouvrir une par une.

   * **[!UICONTROL Disposition carrousel]** : affiche les cartes dans un carrousel horizontal afin que les profils puissent faire défiler ou se déplacer latéralement à travers les surbrillances sans quitter la surface de la boîte de réception.

   ![](assets/inbox-design-1.png)

1. Spécifiez la boîte de réception **capacité**, le nombre maximal de cartes de contenu que la boîte de réception est configurée pour contenir.

1. Activez le bouton **[!UICONTROL Paramètres non lus]** et configurez la manière dont les messages non lus sont indiqués :

   * **[!UICONTROL URL de l’image de l’icône Non lu]** : fournissez l’image affichée à côté ou sur les éléments non lus ; ajoutez une URL en mode sombre afin que l’icône reste visible et sur la marque lorsque l’application ou le site utilise un thème sombre.

   * **[!UICONTROL Couleurs d’arrière-plan]** : définissez les couleurs pour le mode clair et, si nécessaire, sombre afin que le traitement non lu corresponde à votre marque et reste lisible sur l’arrière-plan de la boîte de réception.

   * **[!UICONTROL Emplacement]** : utilisez la liste déroulante pour choisir l’emplacement où l’icône Non lu s’affichera pour s’aligner sur votre disposition.

   ![](assets/inbox-design-2.png)

1. Sous **[!UICONTROL État vide]**, configurez les profils qui s’affichent lorsqu’il n’y a aucun message à afficher :

   * **[!UICONTROL Texte du message]** : texte court expliquant que la boîte de réception est vide ou suggérant une étape suivante.

   * **[!UICONTROL URL de l’image]** : illustration ou graphique facultatif pour le mode clair qui renforce l’état vide au lieu d’afficher une zone vide.

   * **[!UICONTROL URL de l’image sombre]** : image facultative optimisée pour le mode sombre afin que l’état vide semble correct sans contraste faible ou bords durs.

   ![](assets/inbox-design-3.png)

1. Cliquez sur l’icône ![rail](assets/do-not-localize/Smock_Rail_18_N.svg) pour ouvrir le panneau d’aperçu et vérifier comment la boîte de réception vide s’affiche.

   ![](assets/inbox-design-3.png)

1. Dans la section **[!UICONTROL Données]**, cliquez sur **[!UICONTROL Ajouter un méta]** pour ajouter des paires clé/valeur personnalisées à la payload.

1. Cliquez sur l’icône ![](assets/do-not-localize/Smock_StarOutline_18_N.svg) pour ouvrir un aperçu en mode sombre de la boîte de réception et confirmer les couleurs et images de votre thème sombre.

   ![](assets/inbox-design-4.png)

Lorsque vous êtes prêt, vérifiez vos paramètres et activez la boîte de réception. Après l’activation, vous pouvez l’utiliser avec des [cartes de contenu](../content-card/create-content-card.md).

