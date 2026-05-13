---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les schémas
description: Découvrez comment utiliser les schémas Adobe Experience Platform dans Adobe Journey Optimizer.
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: schémas, platform, données, structure
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
TQID: https://experienceleague.adobe.com/fWsW9Rvyd8L4nphczzc7GF1rbO7HuYsjqDBBpy3uoGU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b23e006f-0a29-4f1d-8fd0-77aa56f3d12b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 100%

---

# Commencer avec les schémas {#schemas-gs}

[!DNL Adobe Journey Optimizer] s’appuie sur les schémas **Adobe Experience Platform** pour décrire la structure des données de manière cohérente et réutilisable. Un schéma fournit une définition abstraite d’un objet du monde réel (une personne, par exemple) et décri les données à inclure dans chaque instance de cet objet (comme le nom, la date de naissance, etc.). Lorsque des données sont ingérées dans Experience Platform, elles sont toujours structurées en fonction d’un **schéma XDM**.

## Schémas standard et relationnels

Adobe Experience Platform comporte deux types de schémas :

* Les **schémas standard** sont des schémas hiérarchiques qui utilisent des classes et des groupes de champs pour capturer des données d’enregistrement ou de série temporelle.

  Un schéma standard est composé des éléments suivants :

   * Une **classe** (qui définit le comportement des données : enregistrement ou série temporelle).
   * Un ou plusieurs **groupes de champs** (qui ajoutent des champs spécifiques au schéma).

  Dans Journey Optimizer, les schémas standard sont généralement utilisés pour représenter des **personnes individuelles et leurs attributs**, capturer des **interactions de série temporelle** telles que des clics, des achats ou des connexions, et alimenter le **profil client en temps réel** en termes de segmentation et de personnalisation.

  ➡️ [Découvrir comment créer et configurer un schéma standard dans cette vidéo](#video-schema) (vidéo)

* Les **schémas relationnels** sont des schémas plats, non hiérarchiques, qui n’utilisent ni classes ni groupes de champs. Ils sont utilisés pour capturer des données d’enregistrement pour des entités relationnelles et servent principalement dans des **campagnes orchestrées** [!DNL Journey Optimizer].

  Voici quelques exemples d’entités relationnelles :
   * Réservations, contrats ou abonnements
   * Produits ou catalogues
   * Magasins, emplacements ou partenaires

  Avec les schémas relationnels, vous pouvez envoyer un message par entité (par réservation ou par abonnement, par exemple), créer des segments en fonction des attributs d’entité (par exemple, catégorie de produits, emplacement de la boutique) et améliorer l’adressabilité en contactant toutes les personnes liées à une entité.

  Fonctionnement des schémas relationnels :

   1. **Créer manuellement des schémas ou effectuer un import via un fichier DDL**
   1. **Liez des schémas** pour définir les relations entre les entités et les personnes (par exemple, les transactions de fidélité liées à des personnes membres, les récompenses liées à des marques).
   1. **Ingérez des données** dans votre jeu de données à partir de sources prises en charge.

  ➡️ [Découvrez comment gérer des jeux de données et des schémas relationnels.](../orchestrated/gs-schemas.md)
➡️ [Commencer à utiliser les campagnes orchestrées](../orchestrated/gs-schemas.md)

## Vidéo pratique{#video-schema}

Découvrez comment créer un schéma standard, ajouter des groupes de champs, et créer et configurer des groupes de champs personnalisés.

>[!VIDEO](https://video.tv.adobe.com/v/334461?quality=12)

>[!MORELIKETHIS]
>
>* [Commencer avec la gestion des données dans Journey Optimizer](gs-data.md)
>* [Créer un schéma et un jeu de données et ingérer des données pour ajouter des profils de test dans Journey Optimizer](../audience/creating-test-profiles.md)
>* [Vue d’ensemble du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"}
>* [Bonnes pratiques de modélisation des données](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=fr){target="_blank"}
>* [Créer un schéma à l’aide de l’API Schema Registry](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=fr){target="_blank"}
>* [Définir une relation entre deux schémas à l’aide de l’éditeur de schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=fr){target="_blank"}
