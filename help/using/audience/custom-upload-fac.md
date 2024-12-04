---
solution: Journey Optimizer
product: journey optimizer
title: Chargement personnalisé (CSV) et composition d’audiences fédérées
description: Découvrez les informations clés et les bonnes pratiques lorsque vous utilisez des audiences de chargement personnalisé (CSV) et de composition d’audiences fédérées.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
exl-id: d2365e3f-fbef-43c2-bf2a-0a868cb93015
source-git-commit: a98312d9ac5a457bfd6789bf79ad80a24d894a0b
workflow-type: ht
source-wordcount: '394'
ht-degree: 100%

---

# Chargement personnalisé (CSV) et composition d’audiences fédérées {#csv-fac}

## À propos du chargement personnalisé et de la composition d’audiences fédérées {#about}

En plus des définitions de segment et de la composition d&#39;audiences, [!DNL Journey Optimizer]vous permet de générer et de cibler des audiences en les important à partir d’un fichier CSV ou en exploitant les données de votre entrepôt de données.

* **Chargement personnalisé** : importez une audience à l’aide d’un fichier CSV. Découvrez comment importer des audiences dans la [documentation du service de segmentation](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"} d’Adobe Experience Platform.

* **Composition d’audiences fédérées** : fédérez directement les jeux de données de votre entrepôt de données existant pour créer et enrichir les audiences et les attributs Adobe Experience Platform dans un seul système. Veuillez lire le guide sur la [Composition d’audiences fédérées](https://experienceleague.adobe.com/fr/docs/federated-audience-composition/using/home).

Vous pouvez cibler ces audiences dans Journey Optimizer ou les activer vers n’importe quelle destination prise en charge par Adobe Experience Platform.

➡️ [Découvrir ces fonctionnalités en vidéo](#video)

## À lire absolument {#must-read}

Cette section fournit des informations clés à garder à l’esprit lorsque vous utilisez des audiences de chargement personnalisé (fichiers CSV) et de composition d’audiences fédérées.

* **Prise en charge de la prévisualisation et du BAT :** actuellement, la prévisualisation et le BAT ne sont pas pris en charge pour les audiences créées à l’aide du chargement CSV ou de la composition d’audiences fédérées. Gardez cela à l’esprit lors de la planification de vos campagnes.

* **Délai d’activation :** les audiences sont prêtes à être utilisées dans Journey Optimizer dès que l’ingestion est terminée. Ce délai est généralement de moins d’une heure, mais il peut varier.

* **Enregistrements activés et combinaison d’identités :** chaque enregistrement de l’audience est activé, y compris les doublons. Lors du prochain export de profils UPS, ces enregistrements feront l’objet d’un assemblage d’identités. En conséquence, le nombre d’enregistrements activés peut être différent du nombre de profils après l’assemblage d’identités.

* **Ciblage de nouveaux profils :** lorsqu’une correspondance est introuvable entre un enregistrement et un profil UPS, un nouveau profil vide est créé. Ce profil est lié aux attributs d’enrichissement stockés dans le lac de données. Ce nouveau profil étant vide, les champs de ciblage généralement utilisés dans Journey Optimizer (par exemple, personalEmail.address, mobilePhone.number) sont vides et ne peuvent donc pas être utilisés pour le ciblage.

  Pour résoudre ce problème, vous pouvez spécifier le « champ d’exécution » (ou « adresse d’exécution » selon le canal) dans la configuration des canaux en tant que « identityMap ». Ainsi, l’attribut choisi comme identité lors de la création de l’audience sera celui utilisé pour le ciblage dans Journey Optimizer.

## Tutoriels vidéo {#video}

Découvrez comment charger des audiences au format CSV dans Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)

En savoir plus sur la composition d’audiences fédérées.

>[!VIDEO](https://video.tv.adobe.com/v/3432261?quality=12)
