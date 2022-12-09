---
solution: Journey Optimizer
product: journey optimizer
title: Modifier les adresses email principales
description: Découvrez comment déterminer l’adresse électronique à utiliser à partir du service de profil.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 0f69a47dccad20f3e978613b349a29f9daab94bd
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---

# Modifier les adresses primaires {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Définir l’adresse à utiliser"
>abstract="Lorsque plusieurs adresses email ou numéros de téléphone sont disponibles dans la base de données (personnelle, professionnelle, etc.), vous pouvez choisir celle dont l&#39;envoi doit être prioritaire."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="Définir l’adresse à utiliser"
>abstract="Editez les champs utilisés pour déterminer l&#39;adresse email ou le numéro de téléphone des profils à envoyer en priorité."

Lorsque vous ciblez un profil, plusieurs adresses email ou numéros de téléphone peuvent être disponibles dans la base de données (adresse email professionnelle, numéro de téléphone personnel, etc.).

Avec [!DNL Journey Optimizer], vous pouvez déterminer l’adresse électronique ou le numéro de téléphone à utiliser à partir du service de profil et définir la priorité lorsque plusieurs adresses sont disponibles. Pour ce faire, procédez comme suit.

1. Accédez au  **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]** .

   ![](assets/primary-address-execution-fields.png)

1. Les champs actuellement utilisés par défaut pour déterminer l’adresse email et le numéro de téléphone des profils s’affichent sur cet écran. Cliquez sur **[!UICONTROL Edit]** pour les modifier.

   ![](assets/primary-address.png)

1. Cliquez sur le champ actif de votre choix ou sur l’icône d’édition pour sélectionner un nouveau champ.

   ![](assets/primary-address-edit.png)

1. La liste des champs XDM de type courrier électronique disponibles s’affiche. Sélectionnez le champ à utiliser.

   ![](assets/primary-address-select-field.png)

1. Cliquez sur **[!UICONTROL Save]** pour confirmer votre choix.

Le champ d&#39;exécution est mis à jour et sera désormais utilisé comme adresse principale.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
