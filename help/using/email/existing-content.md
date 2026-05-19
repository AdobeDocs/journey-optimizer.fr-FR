---
solution: Journey Optimizer
product: journey optimizer
title: Importer le contenu de vos e-mails
description: Découvrez comment importer du contenu d'e-mail
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: e-mail, importation, contenu, html, zip, css
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
TQID: https://experienceleague.adobe.com/R0Csd9gbvY-iyW81G-clHoXozEBYWBfjb0y9PWq4zZA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 100%

---

# Importer le contenu de vos e-mails {#existing-content}

[!DNL Journey Optimizer] vous permet d&#39;importer du contenu HTML existant pour concevoir vos e-mails. Ce contenu peut être :

* Un **fichier HTML** avec une feuille de style incorporée ;
* Un **dossier .zip** avec le fichier HTML, la feuille de style (.css) et les images.

  >[!NOTE]
  >
  >Il n’existe aucune contrainte sur la structure des fichiers .zip. Cependant, les références doivent être relatives et s’ajuster à l’arborescence du dossier .zip.


>[!TIP]
>
>Si vous disposez d’images (JPEG ou PNG) au lieu de fichiers HTML, vous pouvez utiliser le [convertisseur d’images en HTML](../content-management/image-to-html.md) pour les convertir automatiquement en modèles d’e-mail HTML modifiables à l’aide de l’IA.

Pour importer un fichier avec du contenu HTML, procédez comme suit :

1. Dans la page d’accueil du concepteur d’e-mail, sélectionnez **[!UICONTROL Importer du contenu HTML]**.

   ![](assets/import-html_2.png)

1. Faites glisser et déposez le fichier HTML ou .zip contenant le contenu HTML, puis cliquez sur **[!UICONTROL Importer]**.

   ![](assets/html-imported_2.png)

1. Une fois le contenu HTML chargé, votre contenu sera en **[!UICONTROL Mode de compatibilité]**.

   Dans ce mode, vous pouvez uniquement personnaliser votre texte, ajouter des liens ou inclure des ressources à votre contenu.

1. Pour pouvoir utiliser les composants de contenu du concepteur d’e-mail, accédez à l’onglet **[!UICONTROL Convertisseur HTML]** et cliquez sur **[!UICONTROL Convertir]**.

   ![](assets/html-imported.png)

   >[!NOTE]
   >
   > L’utilisation d’une balise `<table>` comme première couche d’un fichier HTML peut entraîner une perte de style, y compris les paramètres d’arrière-plan et de largeur dans la balise de couche supérieure.

1. Vous pouvez désormais personnaliser votre fichier importé selon vos besoins à l’aide des fonctionnalités du Concepteur d’e-mail. [En savoir plus](content-from-scratch.md)

## Vidéo pratique {#video}

Découvrez comment importer du contenu HTML existant, améliorer la conception et ajouter une page miroir et des liens de désabonnement. Apprenez également comment coder le contenu.

>[!VIDEO](https://video.tv.adobe.com/v/334102?quality=12)
