---
title: Prévisualiser et tester le contenu
description: Découvrez comment prévisualiser et tester votre contenu.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: 4847415fa33ebf1c21622ebf4faecafd4decc8d3
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 97%

---

# Prévisualiser et tester votre contenu {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Vérifier le rendu de votre contenu"
>abstract="Une fois votre contenu défini, vous pouvez utiliser des profils de test pour le prévisualiser et vérifier si le rendu est correct en fonction du canal que vous utilisez."

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="Vérifier le rendu de votre contenu"
>abstract="Une fois votre contenu défini, vous pouvez le prévisualiser et vérifier si le rendu est correct en fonction du canal que vous utilisez."

## À propos de la prévisualisation et du test {#about}

Une fois votre contenu défini, vous pouvez le prévisualiser avant d’envoyer le message. Il s’agit d’une étape cruciale pour vous assurer qu’il est exact, mais également exempt d’erreurs au niveau du contenu et des paramètres de personnalisation.

Vous pouvez également envoyer des diffusions de test de vos e-mails à des destinataires ou à des personnes abonnées spécifiques à des fins de test et de validation, et vérifier la façon dont ils s’affichent sur les clients populaires de bureau, mobiles et web.

>[!CAUTION]
>
>Lors de la prévisualisation d&#39;un message ou de l&#39;envoi de BAT, seules les données de personnalisation de profil s&#39;affichent. La personnalisation basée sur les données contextuelles, telles que les informations d&#39;événement, ne peut être testée que dans le contexte d&#39;un parcours. Découvrez comment tester la personnalisation dans [ce cas d&#39;utilisation](../personalization/personalization-use-case.md).

Toutes ces actions peuvent être effectuées à l’aide du bouton **[!UICONTROL Simuler du contenu]** accessible à partir de l’écran d’édition du contenu de votre message ou à partir des concepteurs d’e-mail et web pour les canaux e-mail et web.

![](../email/assets/email-preview-button.png)

Notez que vous devez disposer de l’autorisation **[!DNL Manage Simulate Content]** incluse dans le profil de produit **[!DNL Content Library Manager]**. [En savoir plus](../administration/ootb-product-profiles.md#content-library-manager).

## Test à l’aide de profils de test ou d’exemples de données d’entrée {#methods}

Vous pouvez prévisualiser et tester votre contenu à l’aide des éléments suivants :

* **Profils de test**

  Utilisez des profils de test pour prévisualiser votre contenu, envoyer des BAT d’e-mails et vérifier le rendu des e-mails. Si vous avez ajouté des champs personnalisés, vous pouvez vérifier la manière dont ils sont affichés à l’aide des données des profils de test. Pour plus d’informations, consultez les sections suivantes :

  ➡️ [Sélectionner des profils de test](test-profiles.md)

  ➡️ [Prévisualiser votre contenu à l’aide de profils de test](preview.md)

  ➡️ [Envoyer des BAT d’e-mails](proofs.md)

  ➡️ [Vérifier le rendu des e-mails](rendering.md)

  ➡️ [Prévisualiser et corriger votre e-mail (vidéo)](#video-preview)

* **Exemple de données d’entrée**

  [!DNL Journey optimizer] vous permet de tester différentes variantes de votre contenu en le prévisualisant et en envoyant des BAT à l’aide d’exemples de données d’entrée chargées à partir d’un fichier CSV/JSON ou ajoutées manuellement.

  Tous les attributs de profil utilisés dans votre contenu pour la personnalisation sont automatiquement détectés par le système et peuvent être utilisés pour vos tests afin de créer plusieurs variantes.

  ➡️ [Découvrir comment tester votre contenu à l’aide d’exemples de données d’entrée](../test-approve/simulate-sample-input.md)

  >[!NOTE]
  >
  >Cette fonctionnalité est actuellement disponible pour tous les clientes et clients en version bêta publique et uniquement pour les canaux E-mail, SMS et Notification push.

## Vidéo pratique {#video-preview}

Découvrez comment utiliser des profils de test pour tester le rendu d’e-mails dans différentes boîtes de réception, prévisualiser vos e-mails personnalisés avec des profils de test et envoyer des BAT.

>[!VIDEO](https://video.tv.adobe.com/v/3425026?quality=12)
