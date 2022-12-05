---
solution: Journey Optimizer
product: journey optimizer
title: Modification des adresses e-mails principales
description: Découvrez comment déterminer l’adresse e-mail à utiliser à partir du service de profil.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 0f69a47dccad20f3e978613b349a29f9daab94bd
workflow-type: ht
source-wordcount: '210'
ht-degree: 100%

---

# Modification des adresses principales {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Définir l’adresse à utiliser"
>abstract="Lorsque plusieurs adresses e-mail ou numéros de téléphone sont disponibles dans la base de données (personnel, professionnel, etc.), vous pouvez choisir l’adresse ou le numéro à envoyer en priorité."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="Définir l’adresse à utiliser"
>abstract="Modifiez les champs utilisés pour déterminer l’adresse e-mail ou le numéro de téléphone des profils à envoyer en priorité."

Lorsque vous ciblez un profil, plusieurs adresses e-mail ou numéros de téléphone peuvent être disponibles dans la base de données (adresse e-mail professionnelle, numéro de téléphone personnel, etc.).

Avec [!DNL Journey Optimizer], vous pouvez déterminer l’adresse e-mail ou le numéro de téléphone à utiliser à partir du service de profil et donner la priorité lorsque plusieurs adresses sont disponibles. Pour ce faire, suivez les étapes ci-après.

1. Accédez au menu **[!UICONTROL Canaux]** > **[!UICONTROL Général]** > **[!UICONTROL Champs d’exécution]**.

   ![](assets/primary-address-execution-fields.png)

1. Les champs actuellement utilisés par défaut pour déterminer l’adresse e-mail et le numéro de téléphone des profils s’affichent sur cet écran. Cliquez sur **[!UICONTROL Modifier]** pour les modifier.

   ![](assets/primary-address.png)

1. Cliquez sur le champ actif ou sur l’icône de modification pour sélectionner un nouveau champ.

   ![](assets/primary-address-edit.png)

1. La liste des champs XDM de type e-mail disponibles s&#39;affiche. Sélectionnez le champ à utiliser.

   ![](assets/primary-address-select-field.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer votre choix.

Le champ d&#39;exécution est mis à jour et sera désormais utilisé comme adresse principale.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
