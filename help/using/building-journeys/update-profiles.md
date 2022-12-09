---
solution: Journey Optimizer
product: journey optimizer
title: Mettre à jour le profil
description: Découvrez comment utiliser l’activité Mise à jour de profil dans un parcours
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Mettre à jour le profil {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Activité Mise à jour de profil"
>abstract="L’activité d’action Mettre à jour le profil permet de mettre à jour un profil Adobe Experience Platform existant avec des informations provenant de l’événement, d’une source de données ou à l’aide d’une valeur spécifique."

Utilisez la variable **[!UICONTROL Update Profile]** activité d’action pour mettre à jour un profil Adobe Experience Platform existant avec des informations provenant d’un événement, d’une source de données ou d’une valeur spécifique.

## Recommandations

* Le **Mettre à jour le profil** ne peut être utilisée que dans les parcours commençant par un événement ayant un espace de noms .
* L&#39;action ne met à jour que les champs existants, elle ne crée pas de nouveaux champs de profil.
* Vous ne pouvez pas utiliser la variable **Mettre à jour le profil** pour générer des événements d’expérience, par exemple un achat.
* Comme toute autre action, vous pouvez définir un autre chemin en cas d’erreur ou de dépassement de délai, et vous ne pouvez pas placer deux actions en parallèle.
* La demande de mise à jour envoyée à Adobe Experience Platform est immédiate/inférieure à une seconde. Cela prendra normalement quelques secondes mais parfois plus sans aucune garantie. Par conséquent, par exemple, si une action utilise &quot;champ 1&quot; mis à jour par une **Mettre à jour le profil** action positionnée juste avant, vous ne devez pas vous attendre à ce que &quot;champ 1&quot; soit mis à jour dans l’action.
* Le **Mettre à jour le profil** L’activité ne prend pas en charge les champs XDM définis comme une énumération.

## Utilisation de la mise à jour du profil

1. Concevez votre parcours en commençant par un événement. Voir [section](../building-journeys/journey.md).

1. Dans le **Action** de la palette, déposez le **Mettre à jour le profil** dans la zone de travail.

   ![](assets/profileupdate0.png)

1. Sélectionnez un schéma dans la liste.

1. Cliquez sur **Champ** pour sélectionner le champ à mettre à jour. Un seul champ peut être sélectionné.

   ![](assets/profileupdate2.png)

1. Sélectionnez un jeu de données dans la liste.

   >[!NOTE]
   >
   >Le **Mettre à jour le profil** l’action met à jour les données de profil en temps réel, mais elle ne met pas à jour les jeux de données. La sélection du jeu de données est nécessaire, car le profil est un enregistrement associé à un jeu de données.

1. Cliquez sur le bouton **Valeur** pour définir la valeur à utiliser :

   * L’éditeur d’expression simple vous permet de sélectionner un champ à partir d’une source de données ou de l’événement entrant.

      ![](assets/profileupdate4.png)

   * Si vous souhaitez définir une valeur spécifique ou utiliser des fonctions avancées, cliquez sur **Mode avancé**.

      ![](assets/profileupdate3.png)

Le **Mettre à jour le profil** est maintenant configuré.

![](assets/profileupdate1.png)


## Utiliser le mode test {#using-the-test-mode}

En mode test, la mise à jour du profil ne sera pas simulée. La mise à jour sera effectuée sur le profil de test.

Seuls les profils de test peuvent entrer dans un parcours en mode test. Vous pouvez créer un profil de test ou transformer un profil existant en profil de test. Dans Adobe Experience Platform, vous pouvez mettre à jour les attributs de profil par le biais d’un import de fichier CSV ou d’appels d’API. Une méthode simple consiste à utiliser une **Mettre à jour le profil** activité d’action et modifiez le champ booléen du profil de test de false à true.

Pour plus d&#39;informations sur la façon de transformer un profil existant en profil de test, reportez-vous à cette section [section](../segment/creating-test-profiles.md#create-test-profiles-csv).
