---
title: Prévisualiser et tester le contenu
description: Découvrez comment prévisualiser et tester votre contenu.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: a5eacd7a746b2f17804062b23aee3146db0434c9
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 50%

---

# Prévisualiser et tester le contenu {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Vérifier le rendu de votre contenu"
>abstract="Une fois votre contenu défini, vous pouvez utiliser des profils de test pour le prévisualiser et vérifier si le rendu est correct en fonction du canal que vous utilisez."

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="Vérifier le rendu de votre contenu"
>abstract="Une fois votre contenu défini, vous pouvez le prévisualiser et vérifier si le rendu est correct en fonction du canal que vous utilisez."

## A propos de l&#39;aperçu et du test {#about}

Une fois votre contenu défini, vous pouvez prévisualiser son contenu avant d&#39;envoyer le message. Il s’agit d’une étape cruciale pour vous assurer qu’il est exact, mais également exempt d’erreurs au niveau du contenu et des paramètres de personnalisation.

Vous pouvez également envoyer des diffusions test de vos emails à des destinataires ou des abonnés spécifiques à des fins de test et de validation, et vérifier leur rendu sur des clients populaires de bureau, mobiles et web.

>[!CAUTION]
>
>Lors de la prévisualisation d&#39;un message ou de l&#39;envoi de BAT, seules les données de personnalisation de profil s&#39;affichent. La personnalisation basée sur les données contextuelles, telles que les informations d&#39;événement, ne peut être testée que dans le contexte d&#39;un parcours. Découvrez comment tester la personnalisation dans [ce cas d&#39;utilisation](../personalization/personalization-use-case.md).

Toutes ces actions peuvent être effectuées à l’aide du bouton **[!UICONTROL Simuler du contenu]** accessible à partir de l’écran d’édition du contenu de votre message ou à partir des concepteurs d’e-mail et web pour les canaux e-mail et web.

![](../email/assets/email-preview-button.png)

Notez que l’autorisation **[!DNL Manage Simulate Content]** doit être incluse dans le profil de produit **[!DNL Content Library Manager]**. [En savoir plus](../administration/ootb-product-profiles.md#content-library-manager).

## Test à l’aide de profils de test ou d’exemples de données d’entrée {#methods}

Vous pouvez prévisualiser et tester votre contenu à l’aide des éléments suivants :

* **Profils de test**

  Utilisez des profils de test pour prévisualiser votre contenu, envoyer des BAT d’email et vérifier le rendu des emails. Si vous avez ajouté des champs personnalisés, vous pouvez vérifier leur affichage à l&#39;aide des données de profil de test. Pour plus d’informations, consultez les sections suivantes :

  ➡️ [Sélectionner des profils de test](test-profiles.md)

  ➡️ [Prévisualisez votre contenu à l’aide des profils de test](preview.md)

  ➡️ [Envoyer des BAT d&#39;email](proofs.md)

  ➡️ [Vérifier le rendu des emails](rendering.md)

  ➡️ [Prévisualisez et testez votre email (vidéo)](#video-preview)

* **Exemple de données d’entrée**

  [!DNL Journey optimizer] vous permet de tester différentes variantes de votre contenu en le prévisualisant et en envoyant des bons à tirer à l’aide d’exemples de données d’entrée téléchargées à partir d’un fichier CSV/JSON, ou ajoutées manuellement.

  Tous les attributs de profil utilisés dans votre contenu pour la personnalisation sont automatiquement détectés par le système et peuvent être utilisés pour vos tests afin de créer plusieurs variantes.

  ➡️ [Découvrez comment tester votre contenu à l’aide d’exemples de données d’entrée](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >Cette fonctionnalité est actuellement disponible pour tous les clients en version bêta publique uniquement pour les canaux Email, SMS et Notification push.

## Vidéo pratique {#video-preview}

Découvrez comment utiliser des profils de test pour tester le rendu des emails dans les boîtes de réception, prévisualiser vos emails personnalisés par rapport aux profils de test et envoyer des bons à tirer.

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
