---
title: Envoyer des BAT d’e-mail
description: Découvrez comment envoyer des BAT d’e-mail.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: f874456748a8bd7fce69c7ad2a7e69380d5336a6
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 48%

---

# Envoyer des BAT en utilisant des données de profil de test {#send-proofs}

Un BAT est un message spécifique qui permet de tester un message avant son envoi à l&#39;audience principale. Les destinataires du BAT sont chargés d&#39;approuver le message : rendu, contenu, paramètres de personnalisation, configuration.

>[!NOTE]
>
>[!DNL Journey Optimizer] vous permet également de tester différentes variantes de votre contenu en le prévisualisant et en envoyant des BAT à l’aide d’exemples de données d’entrée chargés à partir d’un fichier CSV/JSON ou ajoutés manuellement. [Découvrez comment simuler des variations de contenu.](../test-approve/simulate-sample-input.md)

## À lire impérativement {#must-read}

**Règles de limitation de la fréquence** - Toutes les règles de limitation de la fréquence existantes s’appliquent aux épreuves. Si vous avez défini des [règles de limitation de la fréquence](../conflict-prioritization/channel-capping.md) (par exemple, le nombre maximal d’envois par profil), ces limites s’appliquent également lors de l’envoi de BAT. Si un profil de test a déjà atteint la limite de fréquence, les BAT s&#39;affichent comme terminés, mais aucun e-mail ne sera diffusé. Pour des tests répétés, pensez à utiliser des profils de test uniques ou à ajuster les limites de fréquence pour les scénarios de relecture, si nécessaire.

**Page miroir** - Dans le BAT envoyé, le lien vers la page miroir n’est pas actif. Il n’est activé que dans les messages finaux.

**Assets** - Assets et les images ont des règles d’accessibilité spécifiques :

* Assets/Images sont accessibles dans le contenu diffusé ou le contenu du BAT pendant un maximum de 2 ans (730 jours) depuis leur première publication dans un fragment ou un message intégré.
* Une republication est nécessaire après cette période d’expiration (à tout moment après 730 jours) pour les conserver accessibles pendant 2 ans supplémentaires.
* Toute republication effectuée dans les 730 jours suivant la première publication n’étendra pas l’expiration des ressources/images aux 730 jours suivants.

## Envoyer des épreuves {#send-proofs-steps}

Pour envoyer des BAT d’e-mail en utilisant des données de profil de test, vous devez d’abord sélectionner des [profils de test](test-profiles.md). Suivez ensuite les étapes suivantes :

1. Dans l’écran **[!UICONTROL Simuler]**, cliquez sur le bouton **[!UICONTROL Envoyer le BAT]**.

   ![Bouton Envoyer un BAT dans l’écran Simuler](../email/assets/send-proof-button.png)

1. Dans la fenêtre **[!UICONTROL Envoyer le BAT]**, saisissez l’e-mail du destinataire et cliquez sur **[!UICONTROL Ajouter]** pour envoyer le BAT à vous-même ou aux membres de votre organisation.

   Vous pouvez ajouter jusqu’à dix destinataires pour la diffusion de votre BAT.

   ![Ajouter des destinataires à la diffusion du BAT](../email/assets/send-proof-add.png)

1. Sélectionnez les **profils de test** à utiliser pour personnaliser le contenu du message.

   Chaque destinataire du BAT recevra autant de messages que le nombre de profils de test sélectionnés. Par exemple, si vous avez ajouté cinq e-mails de destinataires et sélectionné dix profils de test, vous enverrez cinquante messages de BAT. Chaque destinataire en recevra dix.

1. Si nécessaire, vous pouvez ajouter un préfixe à l&#39;objet du BAT. Seuls les caractères alphanumériques et les caractères spéciaux, comme . - _ ( ) [ Les ] sont autorisées comme préfixe à l’objet.

1. Cliquez sur **[!UICONTROL Envoyer un BAT]**.

   ![Sélection des profils de test et envoi du BAT](../email/assets/send-proof-select.png)

1. De retour dans l’écran **[!UICONTROL Simuler]**, cliquez sur le bouton **[!UICONTROL Afficher les BAT]** pour vérifier le statut.

   ![Bouton Afficher les BAT pour vérifier le statut de la diffusion](../email/assets/send-proof-view.png)

Il est recommandé d’envoyer des BAT après chaque modification du contenu du message.
