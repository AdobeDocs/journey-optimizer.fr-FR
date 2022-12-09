---
title: Jeu de données de placements
description: Cette section répertorie tous les champs utilisés dans le jeu de données exporté pour les emplacements.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Jeu de données de placements {#placements-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les emplacements est mis à jour.

![](../assets/dataset-placements.png)

Le dernier lot réussi du jeu de données s’affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d’offres dans [cette section](../export-catalog/access-dataset.md).

Voici la liste de tous les champs pouvant être utilisés dans la variable **[!UICONTROL Decision Object Repository - Placements]** jeu de données.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

## Identifiant {#identifier}

**Champ :** _id
**Titre :** Identifiant
**Description :** Identifiant unique de l’enregistrement.
**Type :** string

## _experience {#experience}

**Champ :** _experience
**Type :** objet

### _experience > prise de décision

**Champ :** prise de décision
**Type :** objet

#### _experience > prise de décision > Identifiant de canal de référencement

**Champ :** channelID
**Titre :** Identifiant de canal de référencement
**Description :** Canal dans lequel la proposition a été faite. La valeur est un URI de canal valide. Voir https://ns.adobe.com/xdm/channels/channel.
**Type :** string

#### _experience > prise de décision > Type de composant de contenu

**Champ :** componentType
**Titre :** Type de composant de contenu
**Description :** Un ensemble énuméré d’URI où chaque valeur correspond à un type donné au composant de contenu. Certains consommateurs des représentations de contenu s’attendent à ce que la valeur @type soit une référence au schéma qui décrit les propriétés supplémentaires du composant de contenu.
**Type :** string

#### _experience > prise de décision > contentTypes

**Champ :** contentTypes
**Type :** tableau

**_experience > prise de décision > contentTypes > MIME Type de média**

**Titre :** Type de média MIME
**Description :** Contrainte pour le type de média des composants attendus à cet emplacement. Il peut y avoir plusieurs types de média possibles pour un composant, par exemple un format d’image différent.
**Type :** string

#### _experience > prise de décision > Description de l’emplacement

**Champ :** description
**Titre :** Description de l’emplacement
**Description :** Il est utilisé pour transmettre des intentions lisibles par l’utilisateur sur l’utilisation du contenu dynamique dans la diffusion globale du message. Le fait qu’un certain espace soit une \&quot;bannière\&quot; dans une page web est souvent transmis via la description et non par une méthode formelle.
**Type :** string

#### _experience > prise de décision > Nom de l’emplacement

**Champ :** name
**Titre :** Nom de l’emplacement
**Description :** Nom attribué à l’emplacement pour y faire référence dans les interactions humaines.
**Type :** string

## _repo {#repo}

**Champ :** _repo
**Type :** objet

### _repo > Placement ETag

**Champ :** etag
**Titre :** Placement ETag
**Description :** La révision à laquelle se trouvait l’objet d’option de décision lors de la prise de l’instantané.
**Type :** string
