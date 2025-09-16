---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les schémas
description: Découvrez comment utiliser les schémas Adobe Experience Platform dans Adobe Journey Optimizer.
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: schémas, platform, données, structure
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
source-git-commit: 70f647cf4e95c1152a5c16395b88b11a6b72865c
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 20%

---

# Commencer avec les schémas {#schemas-gs}

[!DNL Adobe Journey Optimizer] repose sur **les schémas Adobe Experience Platform** pour décrire la structure des données de manière cohérente et réutilisable. Un schéma fournit une définition abstraite d’un objet du monde réel (une personne, par exemple) et décrit les données à inclure dans chaque instance de cet objet (comme le nom, l’anniversaire, etc.). Lorsque des données sont ingérées dans Experience Platform, elles sont toujours structurées selon un **schéma XDM**.

## Schémas standard et relationnels

Adobe Experience Platform comporte deux types de schémas :

* **Schémas standard** sont des schémas hiérarchiques qui utilisent des classes et des groupes de champs pour capturer des données d’enregistrement ou de série temporelle.

  Un schéma standard est composé des éléments suivants :

   * Une **classe** (qui définit le comportement des données : enregistrement ou série temporelle).
   * Un ou plusieurs **groupes de champs** (qui ajoutent des champs spécifiques au schéma).

  Dans Journey Optimizer, les schémas standard sont généralement utilisés pour représenter **des personnes individuelles et leurs attributs**, capturer **des interactions de série temporelle** telles que des clics, des achats ou des connexions, et alimenter **Profil client en temps réel** la segmentation et la personnalisation.

  ➡️ [Découvrez comment créer et configurer un schéma standard dans cette vidéo](#video-schema) (vidéo)

* Les **schémas relationnels** sont des schémas aplatis non hiérarchiques qui n’utilisent pas de classes ni de groupes de champs. Ils sont utilisés pour capturer des données d’enregistrement pour des entités relationnelles et sont principalement utilisés dans des [!DNL Journey Optimizer] **campagnes orchestrées**.

  Voici quelques exemples d’entités relationnelles :
   * Réservations, contrats ou abonnements
   * Produits ou catalogues
   * Magasins, emplacements ou partenaires

  Avec les schémas relationnels, vous pouvez envoyer un seul message par entité (par exemple, par réservation, par abonnement), créer des segments en fonction des attributs d’entité (par exemple, catégorie de produits, emplacement de la boutique) et améliorer l’adressabilité en atteignant tous les contacts liés à une entité.

  Fonctionnement des schémas relationnels :

   1. **Création manuelle de schémas ou importation via DDL**
   1. **Schémas de lien** pour définir les relations entre les entités et les personnes (par exemple, les transactions de fidélité liées à des membres, les récompenses liées à des marques).
   1. **Ingérez des données** dans votre jeu de données à partir de sources prises en charge.

  ➡️ [Découvrez comment gérer les schémas relationnels et les jeux de données](../orchestrated/gs-schemas.md)
➡️ [Prise en main des campagnes orchestrées](../orchestrated/gs-schemas.md)

## Vidéo pratique{#video-schema}

Découvrez comment créer un schéma standard, ajouter des groupes de champs, créer et configurer des groupes de champs personnalisés.

>[!VIDEO](https://video.tv.adobe.com/v/3416870?quality=12&captions=fre_fr)

>[!MORELIKETHIS]
>
>* [Créer un schéma e t un jeu de données et ingérer des données pour ajouter des profils de test dans Journey Optimizer](../audience/creating-test-profiles.md)
>* [Vue d’ensemble du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"}
>* [Bonnes pratiques de modélisation des données](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=fr){target="_blank"}
>* [Créer un schéma à l’aide de l’API Schema Registry](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=fr){target="_blank"}
>* [Définir une relation entre deux schémas à l’aide de l’éditeur de schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=fr){target="_blank"}
