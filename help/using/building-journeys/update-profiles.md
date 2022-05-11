---
title: Mettre à jour le profil
description: Découvrez comment utiliser l'activité Mettre à jour le profil dans un parcours.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 80e0fea3be11dcd594b1de04a0a903b87b9c7b68
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 79%

---

# Mettre à jour le profil {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Mettre à jour l&#39;activité du profil"
>abstract="L&#39;activité d&#39;action Mettre à jour le profil vous permet de mettre à jour un profil Adobe Experience Platform existant avec des informations provenant de l&#39;événement, d&#39;une source de données ou à l&#39;aide d&#39;une valeur spécifique."

Utilisez la variable **[!UICONTROL Mettre à jour le profil]** activité d’action pour mettre à jour un profil Adobe Experience Platform existant avec des informations provenant d’un événement, d’une source de données ou d’une valeur spécifique.

## Recommandations

* L&#39;action **Mettre à jour le profil** ne peut être utilisée que dans les parcours commençant par un événement qui possède un espace de noms.
* L&#39;action ne met à jour que les champs existants, elle ne crée pas de nouveaux champs de profil.
* Vous ne pouvez pas utiliser l&#39;action **Mettre à jour le profil** pour générer des événements d&#39;expérience, par exemple un achat.
* Comme toute autre action, vous pouvez définir un autre chemin en cas d’erreur ou de dépassement de délai, et vous ne pouvez pas placer deux actions en parallèle.
* La requête de mise à jour envoyée à Adobe Experience Platform est immédiate/inférieure à une seconde. Cela prendra normalement quelques secondes, parfois plus, sans aucune garantie. Par conséquent, par exemple, si une action utilise &quot;champ 1&quot; mis à jour par une **Mettre à jour le profil** action positionnée juste avant, vous ne devez pas vous attendre à ce que &quot;champ 1&quot; soit mis à jour dans l’action.
* L’activité **Mettre à jour le profil** ne prend pas en charge les champs XDM définis comme une énumération.

## Utilisation de la mise à jour du profil

1. Concevez votre parcours en commençant par un événement. Consultez cette [section](../building-journeys/journey.md).

1. Dans la section **Action** de la palette, déposez l&#39;activité **Mettre à jour le profil** sur la zone de travail.

   ![](assets/profileupdate0.png)

1. Sélectionnez un schéma dans la liste.

1. Cliquez sur **Champ** pour sélectionner le champ à mettre à jour. Vous ne pouvez sélectionner qu&#39;un seul champ.

   ![](assets/profileupdate2.png)

1. Sélectionnez un jeu de données dans la liste.

   >[!NOTE]
   >
   >L&#39;action **Mettre à jour le profil** met à jour les données de profil en temps réel, mais elle ne met pas à jour les jeux de données. La sélection du jeu de données est nécessaire, car le profil est un enregistrement associé à un jeu de données.

1. Cliquez sur le champ **Valeur** pour définir la valeur à utiliser :

   * L&#39;éditeur d&#39;expression simple vous permet de sélectionner un champ à partir d&#39;une source de données ou de l&#39;événement entrant.

      ![](assets/profileupdate4.png)

   * Si vous souhaitez définir une valeur spécifique ou utiliser des fonctions avancées, cliquez sur **Mode avancé**.

      ![](assets/profileupdate3.png)

L&#39;action **Mettre à jour le profil** est maintenant configurée.

![](assets/profileupdate1.png)


## Utilisation du mode test {#using-the-test-mode}

En mode test, la mise à jour du profil ne sera pas simulée. La mise à jour sera effectuée sur le profil de test.

Seuls les profils de test peuvent rejoindre un parcours en mode test. Vous pouvez soit créer un profil de test, soit transformer un profil existant en profil de test. Dans Adobe Experience Platform, vous pouvez mettre à jour les attributs de profil par le biais d&#39;un import de fichier csv ou d&#39;appels d&#39;API. Une méthode plus simple consiste à utiliser une activité d&#39;action **Mettre à jour le profil** et à redéfinir le champ booléen du profil de test de false à true.

Pour plus d&#39;informations sur la façon de transformer un profil existant en profil de test, consultez [cette section](../segment/creating-test-profiles.md#create-test-profiles-csv).
