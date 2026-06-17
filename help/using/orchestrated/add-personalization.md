---
solution: Journey Optimizer
product: journey optimizer
title: Ajouter de la personnalisation dans des campagnes orchestrées
description: Découvrez comment personnaliser des messages de campagne orchestrés à l’aide d’attributs de profil, d’attributs de cible de la table de travail et de tableaux de collecte d’enrichissement.
exl-id: c4a91e2b-6f08-4d1a-9e3b-2f8f5a0d1c62
version: Campaign Orchestration
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: e0a12bd7971c778378f9905cf93653792f38509d
workflow-type: tm+mt
source-wordcount: 477
ht-degree: 0%

---

# Ajouter de la personnalisation dans des campagnes orchestrées {#add-personalization}

Après avoir [orchestré les activités](orchestrate-activities.md) sur la zone de travail et ajouté une activité de canal, vous personnalisez le contenu du message dans l’éditeur d’e-mail, de SMS ou d’un autre canal.

Le fonctionnement de Personalization dans les campagnes orchestrées est similaire à celui d’autres campagnes ou parcours [!DNL Journey Optimizer], avec des différences liées à la **table de travail** : attributs calculés par les activités de ciblage et d’enrichissement sur la zone de travail, et pas seulement les données de la banque de profils.

## Accès à l’éditeur de personnalisation {#access}

1. Ouvrez votre campagne orchestrée et ajoutez une activité de canal. [Découvrez comment ajouter une activité de canal](activities/channels.md#add)

1. Configurez l’activité de canal, puis ouvrez l’onglet **[!UICONTROL Contenu]** et modifiez le message.

1. Dans l’éditeur de messages, utilisez l’éditeur de personnalisation pour insérer des attributs dans le contenu.

Pour prévisualiser et tester le contenu personnalisé à partir de l’activité de canal, consultez [Vérifier et tester votre contenu](activities/channels.md#simulate-content-test-profiles).

## Attributs de profil et de cible {#attributes}

Lorsque vous ouvrez l’éditeur de personnalisation, deux dossiers principaux contiennent des attributs disponibles pour la personnalisation :

* **[!UICONTROL Attributs de profil]**

  Données liées au profil provenant de l’[!DNL Adobe Experience Platform] : nom, adresse e-mail, emplacement et autres caractéristiques capturées dans le profil utilisateur.

* **[!UICONTROL Attributs de cible]** (campagnes orchestrées uniquement)

  Attributs calculés sur la zone de travail de la campagne à partir de la table de travail. Ce dossier comporte deux sous-dossiers :

   * **`<Targeting dimension>`** (par exemple, Destinataires ou Achats) : attributs liés à la dimension ciblée dans la campagne.

   * **`Enrichment`** — Données ajoutées par des activités **[!UICONTROL Enrichissement]** (liens relationnels, lignes collectées, agrégats). Après un enrichissement 1:N **[!UICONTROL Collecter des données]**, vous obtenez à la fois des lignes numérotées et un tableau de collection. [Découvrez comment utiliser les données de la collecte d’enrichissement](#enrichment-collections)

Pour une présentation détaillée de l’éditeur de personnalisation dans [!DNL Journey Optimizer], voir [Prise en main de la personnalisation](../personalization/personalize.md).

## Utiliser des données de collecte d’enrichissement {#enrichment-collections}

Lorsque vous configurez une activité **[!UICONTROL Enrichissement]** avec un lien 1:N et **[!UICONTROL Collecter des données]**, les attributs d’enrichissement sont disponibles sous **[!UICONTROL Attributs de la cible] > [!UICONTROL Enrichissement]** sous deux formes :

* **Lignes aplaties** — Un champ par ligne récupérée (par exemple, **Achat 1**, **Achat 2**, **Achat 3**), chacun avec les attributs que vous avez sélectionnés sur le lien (tels que le prix ou le produit). Utilisez-les lorsque vous avez besoin d&#39;emplacements fixes distincts, par exemple des emplacements `target.enrichment.purchase1.price`.

* **Tableau de collection** — Un tableau pour toutes les lignes collectées, nommé à partir du libellé du lien (par exemple, **purchases**). Utilisez cette option lorsque vous devez travailler sur l’ensemble complet des enregistrements, avec des [fonctions de tableau](#array-functions).

![](assets/enrichment-target-attributes-picker.png)

Pour identifier les lignes aplaties du tableau de collection, insérez l’attribut dans l’éditeur d’expression et lisez le chemin d’accès généré. Le tableau de collection est l’entrée dont le chemin d’accès est **plural** (par exemple `purchases`) et n’a **aucun numéro de ligne** (`purchase1`, `purchase2`, etc.).

| Ce dont vous avez besoin | Chemin dans l’éditeur d’expression |
| --- | --- |
| **Une ligne collectée** | **Numérotée** — par exemple `target.enrichment.purchase1.price` |
| **Collection complète** | **Pluriel et non numéroté** — par exemple `target.enrichment.purchases.price` |

Vous pouvez appliquer les mêmes fonctions [tableau et liste](../personalization/functions/arrays-list.md) que celles utilisées ailleurs dans [!DNL Journey Optimizer] à une collection d’enrichissement, en référençant `target.enrichment.<label>`.

Par exemple, dans une ligne d&#39;objet, vous pouvez afficher le nombre d&#39;achats collectés et le prix du premier article :

```sql
Hello number of Items: {%= count(target.enrichment.purchases.price) %} , Name of first item: {%= head(target.enrichment.purchases.product) %}
```

➡️ [Découvrez comment configurer l’enrichissement de la collection sur la zone de travail](activities/enrichment.md#collection-personalization)
