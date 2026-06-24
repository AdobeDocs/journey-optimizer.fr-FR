---
solution: Journey Optimizer
product: journey optimizer
title: Fragments de contenu AEM
description: Découvrez comment gérer les fragments de contenu AEM
topic: Content Management
role: User
level: Beginner
source-git-commit: ce34eb885d85c6c0f81b477e155cb81547d53e03
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Gestion des fragments de contenu Adobe Experience Manager {#aem-fragments}

>[!BEGINSHADEBOX]

**Sur cette page :** Gérer les fragments de contenu AEM à partir de la liste Fragments de gestion de contenu pour surveiller le statut et les métadonnées, voir où les fragments sont utilisés dans les parcours et les campagnes, synchroniser les mises à jour publiées depuis Experience Manager et ouvrir les fragments pour modification sans quitter Journey Optimizer.

>[!ENDSHADEBOX]

En intégrant Adobe Experience Manager as a Cloud Service ou Managed Services à Adobe Journey Optimizer, vous pouvez utiliser les fragments de contenu d’AEM dans votre contenu et vérifier les statuts des fragments sans quitter Journey Optimizer.

Lorsque vous republiez un fragment déjà utilisé dans un Parcours ou une campagne, le minuteur de synchronisation démarre après la **publication du fragment** dans Adobe Experience Manager. Le contenu mis à jour est généralement disponible dans Journey Optimizer en environ **5 minutes** pour les parcours et campagnes unitaires, pour les diffusions par lots, la modification apparaît dans le **lot de traitement suivant**. Voir [&#x200B; Utilisation de fragments de contenu Adobe Experience Manager &#x200B;](aem-fragments.md). En cas de retard, vous pouvez synchroniser manuellement ce fragment depuis Journey Optimizer afin d’extraire la dernière version publiée.

## Accès aux fragments de contenu AEM {#access-aem-fragments}

1. Dans le menu **[!UICONTROL Gestion de contenu]**, sélectionnez **[!UICONTROL Fragments]**.

1. Ouvrez l’onglet **[!UICONTROL Fragments d’]** pour afficher les fragments de contenu disponibles à partir de Adobe Experience Manager.

1. Dans la liste Fragment , cliquez sur ![menu avancé](assets/do-not-localize/Smock_FolderSearch_18_N.svg) pour **[!UICONTROL Explorer les références]**.

   ![](assets/fragment-list-1.png)

1. Sélectionnez un fragment pour consulter son statut et les actions disponibles :

   * **[!UICONTROL Explorer les références]** : consultez les Parcours, les campagnes, les campagnes orchestrées et les modèles qui utilisent le fragment.
   * **[!UICONTROL Ouvrir dans AEM]** : ouvrez le fragment dans Adobe Experience Manager pour le modifier ou le republier.
   * **[!UICONTROL Synchronisation]** : extrayez la dernière version publiée de Adobe Experience Manager dans Journey Optimizer, par exemple lorsque le contenu republié ne s’est pas affiché après la fenêtre de synchronisation habituelle. Si le contrôle est désactivé, le fragment correspond déjà à la version publiée dans Experience Manager.

     ![](assets/fragment-list-2.png)

1. Le menu **[!UICONTROL Détails]** vous permet de passer en revue les métadonnées et de prévisualiser la payload synchronisée :

   * **[!UICONTROL Name]** : titre du fragment de contenu importé de Adobe Experience Manager.
   * **[!UICONTROL Description]** : description importée de Adobe Experience Manager.
   * **[!UICONTROL Variation]** : variation publiée actuellement représentée pour ce fragment.
   * **[!UICONTROL Repo Id]** : identifiant du référentiel pour le fragment dans Adobe Experience Manager.
   * **[!UICONTROL ID de fragment AEM]** : identifiant unique de fragment de contenu dans Adobe Experience Manager.
   * **[!UICONTROL Balises]** : balises affectées dans Adobe Experience Manager, y compris les balises d’activation de Journey Optimizer qui déterminent si le fragment apparaît dans les sélecteurs de votre organisation et de votre sandbox. [Découvrez comment créer et affecter des balises](aem-fragments.md#create-tag)
   * **[!UICONTROL Aperçu JSON]** : structure JSON en lecture seule du contenu de fragment utilisé par Journey Optimizer.

1. Dans **[!UICONTROL Explorer les références]**, utilisez les onglets pour afficher les parcours, les campagnes, les campagnes orchestrées et les modèles qui font référence au fragment.

   ![](assets/fragment-list-3.png)

➡️ [En savoir plus sur le fragment de contenu](aem-fragments.md)


