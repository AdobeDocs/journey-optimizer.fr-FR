---
title: Jeu de données Emplacements
description: Cette section liste tous les champs utilisés dans le jeu de données exporté pour les emplacements.
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 4%

---

# Jeu de données Emplacements {#placements-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les emplacements est mis à jour.

![](../../assets/dataset-placements.png)

Le lot le plus récent du jeu de données qui a réussi s&#39;affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d&#39;Offres dans [cette section](../export-catalog/access-dataset.md).

Voici la liste de tous les champs qui peuvent être utilisés dans le jeu de données **[!UICONTROL Decision Object Repository - Placements]**.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## Identifiant

**Champ:** _id 
**Titre:** Identifier 
**Description:** Identificateur unique de l’enregistrement.
**Type :** Chaîne

## _expérience

**Champ:** _experience 
**Type:** objet

### prise de décision

**Champ:** Type de 
**prise de décision:** objet

#### Identifiant de Canal du référencement

**Champ :** channelID 
**Titre :** Placement&#39;s Canal Identifier 
**Description :** canal dans lequel la proposition a été présentée. La valeur est un URI de Canal valide. Voir https://ns.adobe.com/xdm/channels/channel.
**Type :** Chaîne

#### Type de composant de contenu

**Champ:** componentType 
**Titre:** Content Component Type 
**Description:** Ensemble énuméré d’URI où chaque valeur correspond à un type donné au composant de contenu. Certains consommateurs des représentations de contenu s’attendent à ce que la valeur @type soit une référence au schéma qui décrit les propriétés supplémentaires du composant de contenu.
**Type :** Chaîne

#### contentTypes

**Champ:** contentTypes 
**Type:** tableau

* **Type de support MIME**

   **Titre:Type de support** MIME
   **Description :** contrainte pour le type de support des composants attendus dans cet emplacement. Il peut y avoir plusieurs types de supports possibles pour un composant, par exemple un format d’image différent.
   **Type :** Chaîne

#### Description du placement

**Champ:** description 
**Titre:** Placement Description 
**Description:** Il est utilisé pour transmettre des intentions lisibles sur la façon dont le contenu dynamique est utilisé dans la diffusion globale des messages. Le fait qu&#39;un certain espace soit une \&quot;bannière\&quot; dans une page Web est souvent transmis par la description et non par une méthode formelle.
**Type :** Chaîne

#### Nom du placement

**Champ:** nom 
**Titre:Nom du** placement 
**Description:** Nom attribué pour que le placement y fasse référence dans les interactions humaines.
**Type :** Chaîne

## _repo

**Champ:** _repo 
**Type:** objet

### Placement ETag

**Champ :** balise 
**Titre :** Placement ETag 
**Description :** révision à laquelle l&#39;objet de l&#39;option de décision se trouvait lors de la prise de l&#39;instantané.
**Type :** Chaîne
