---
solution: Journey Optimizer
product: journey optimizer
title: Chargement personnalisé (CSV) et composition d’audiences fédérées
description: Découvrez les informations clés et les bonnes pratiques lorsque vous utilisez le téléchargement personnalisé (CSV) et les audiences de composition d’audience fédérées.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
source-git-commit: 26d311802236a1f9e8f6273c1291bcb54138aad2
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 38%

---

# Chargement personnalisé (CSV) et composition d’audiences fédérées {#csv-fac}

## À propos du téléchargement personnalisé et de la composition d’audiences fédérées {#about}

Outre les définitions de segment et la composition de l’audience, [!DNL Journey Optimizer] vous permet de générer et de cibler des audiences en les important à partir d’un fichier CSV ou en exploitant les données de votre entrepôt de données.

* **Chargement personnalisé** : importez une audience à l’aide d’un fichier CSV. Découvrez comment importer des audiences dans la [documentation du service de segmentation](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"} d’Adobe Experience Platform.

* **Composition d’audiences fédérées** : fédérez directement les jeux de données de votre entrepôt de données existant pour créer et enrichir les audiences et les attributs Adobe Experience Platform dans un seul système. Veuillez lire le guide sur la [Composition d’audiences fédérées](https://experienceleague.adobe.com/fr/docs/federated-audience-composition/using/home).

  >[!AVAILABILITY]
  >
  >La composition d’audiences fédérées n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en savoir plus, contactez votre représentant ou représentante Adobe.

Vous pouvez cibler ces audiences dans Journey Optimizer ou les activer vers n’importe quelle destination prise en charge par Adobe Experience Platform.

➡️ [Découvrez ces fonctionnalités en vidéo](#video)

## À lire absolument {#must-read}

Cette section fournit des informations clés à garder à l’esprit lors de l’utilisation des téléchargements personnalisés (fichiers CSV) et des audiences de composition d’audience fédérée.

* **Prise en charge de l’aperçu et du BAT :** Actuellement, l’aperçu et le BAT ne sont pas pris en charge pour les audiences créées à l’aide du téléchargement CSV ou de la composition d’audiences fédérées. Gardez cela à l’esprit lors de la planification de vos campagnes.

* **Délai d’activation :** Les audiences sont prêtes à être utilisées dans Journey Optimizer juste après la fin de l’ingestion. Ce délai est généralement de moins d’une heure, mais il peut varier.

* **Enregistrement activé et combinaison d’identités :** Chaque enregistrement de l’audience est activé, y compris les doublons. Lors de la prochaine exportation de profils UPS, ces enregistrements passeront par le regroupement d’identités. Par conséquent, le nombre d’enregistrements activés peut différer du nombre de profils après combinaison d’identités.

* **Ciblage de nouveaux profils :** Lorsqu’une correspondance est introuvable entre un enregistrement et un profil UPS, un nouveau profil vide est créé. Ce profil est lié aux attributs d’enrichissement stockés dans le lac de données. Ce nouveau profil étant vide, les champs de ciblage généralement utilisés dans Journey Optimizer (par exemple, personalEmail.address, mobilePhone.number) sont vides et ne peuvent donc pas être utilisés pour le ciblage.

  Pour résoudre ce problème, vous pouvez spécifier le « champ d’exécution » (ou « adresse d’exécution » selon le canal) dans la configuration des canaux en tant que « identityMap ». Ainsi, l’attribut choisi comme identité lors de la création de l’audience sera celui utilisé pour le ciblage dans Journey Optimizer.

## Tutoriels vidéo {#video}

Découvrez comment charger des audiences au format CSV dans Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)

En savoir plus sur la composition des audiences fédérées.

>[!VIDEO](https://video.tv.adobe.com/v/3432261?quality=12)
