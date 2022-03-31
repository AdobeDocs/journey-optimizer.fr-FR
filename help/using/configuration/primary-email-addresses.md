---
title: 'Modification des adresses e-mails principales '
description: Découvrez comment déterminer l’adresse e-mail à utiliser à partir du service de profil.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 5071de634c9dbb13908d3190fe1157831c372c7d
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 42%

---

# Modification des adresses e-mail principales {#change-primary-email}

Lorsque vous ciblez un profil, plusieurs adresses e-mail peuvent être disponibles dans la base de données (adresse e-mail personnelle, professionnelle, etc.).

Avec [!DNL Journey Optimizer], vous pouvez déterminer l’adresse électronique à utiliser à partir du service de profil et définir la priorité lorsque plusieurs adresses sont disponibles. Pour ce faire, suivez les étapes ci-après.

1. Accédez au  **[!UICONTROL Canaux]** > **[!UICONTROL Général]** > **[!UICONTROL Champs d’exécution]** .

   ![](assets/primary-address-execution-fields.png)

1. Le champ actuellement utilisé par défaut pour déterminer les adresses email des profils s’affiche sur cet écran. Cliquez sur **[!UICONTROL Modifier]** pour le modifier.

   ![](assets/primary-address.png)

1. Cliquez sur le champ actif ou sur l’icône d’édition pour sélectionner un nouveau champ.

   ![](assets/primary-address-edit.png)

1. La liste des champs XDM de type e-mail disponibles s&#39;affiche. Sélectionnez le champ à utiliser.

   ![](assets/primary-address-field.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer votre choix.

   ![](assets/primary-address-save.png)

   Le champ d&#39;exécution est mis à jour et sera désormais utilisé comme adresse Principale.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
