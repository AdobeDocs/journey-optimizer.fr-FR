---
title: Envoyer des BAT d’e-mail
description: Découvrez comment envoyer des BAT d’e-mail.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: 83da97926138c867ea2dacca6e5cf5e40c926eda
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 83%

---

# Envoyer des BAT d’e-mail {#send-proofs}

>[!PREREQUISITES]
>
>Pour envoyer des BAT, les utilisateurs doivent disposer des autorisations **Approuver et publier** pour la ressource, la campagne ou le parcours spécifique associé à l’e-mail. [En savoir plus sur les autorisations](../administration/ootb-permissions.md)

Un BAT est un message spécifique qui permet de tester un message avant son envoi à l&#39;audience principale. Les destinataires du BAT sont chargés d&#39;approuver le message : rendu, contenu, paramètres de personnalisation, configuration.

Notez que [!DNL Journey optimizer] vous permet également de tester différentes variantes de votre contenu en le prévisualisant et en envoyant des BAT à l’aide des exemples de données d’entrée téléchargées à partir d’un fichier CSV/JSON ou ajoutées manuellement. [Découvrir comment tester votre contenu à l’aide d’exemples de données d’entrée](../test-approve/simulate-sample-input.md)

Pour envoyer des BAT d’e-mails une fois des [profils de test](test-profiles.md) sélectionnés, procédez comme suit :

1. Dans l’écran **[!UICONTROL Simuler]**, cliquez sur le bouton **[!UICONTROL Envoyer le BAT]**.

   ![](../email/assets/send-proof-button.png)

1. Dans la fenêtre **[!UICONTROL Envoyer un BAT]**, saisissez l’e-mail du destinataire et cliquez sur **[!UICONTROL Ajouter]** pour envoyer le BAT à vous-même ou aux membres de votre organisation.

   Vous pouvez ajouter jusqu’à dix destinataires pour la diffusion de votre BAT.

   ![](../email/assets/send-proof-add.png)

1. Sélectionnez les **profils de test** à utiliser pour personnaliser le contenu du message.

   Chaque destinataire du BAT recevra autant de messages que le nombre de profils de test sélectionnés. Par exemple, si vous avez ajouté cinq e-mails de destinataires et sélectionné dix profils de test, vous enverrez alors cinquante messages de BAT et chaque destinataire en recevra dix.

1. Si nécessaire, vous pouvez ajouter un préfixe à l&#39;objet du BAT. Seuls les caractères alphanumériques et les caractères spéciaux, comme . - _ ( ) [ Les ] sont autorisées comme préfixe à l’objet.

1. Cliquez sur **[!UICONTROL Envoyer un BAT]**.

   ![](../email/assets/send-proof-select.png)

1. De retour dans l’écran **[!UICONTROL Simuler]**, cliquez sur le bouton **[!UICONTROL Afficher les BAT]** pour vérifier le statut.

   ![](../email/assets/send-proof-view.png)

Il est recommandé d’envoyer des BAT après chaque modification du contenu du message.

>[!NOTE]
>
>Dans le BAT envoyé, le lien vers la page miroir n’est pas actif. Il n’est activé que dans les messages finaux.
