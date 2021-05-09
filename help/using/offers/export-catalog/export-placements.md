---
title: Jeu de données Emplacements
description: Cette section liste tous les champs utilisés dans le jeu de données exporté pour les emplacements.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Jeu de données Emplacements {#placements-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les emplacements est mis à jour.

![](../assets/dataset-placements.png)

Le lot le plus récent du jeu de données qui a réussi s&#39;affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d&#39;Offres dans [cette section](../export-catalog/access-dataset.md).

Un emplacement décrit un emplacement ou un emplacement dans un message personnalisé. Il est utilisé pour définir des contraintes techniques pour le contenu fourni par la décision de personnalisation. L’emplacement représente également une demande de génération de certains types de mesures lorsqu’un événement d’expérience est généré en présence de cet emplacement. Par exemple, l’emplacement facilite l’affichage d’une image cliquable personnalisée à l’intérieur d’un courrier électronique envoyé à l’utilisateur final. L’emplacement peut, par exemple, demander à l’expérience assemblée que le clic sur son image soit signalé dans un événement d’expérience avec une mesure https://ns.adobe.com/xdm/data/metrics/web/linkclicks et une référence à cet emplacement.

Voici la liste de tous les champs qui peuvent être utilisés dans le jeu de données **[!UICONTROL Decision Object Repository - Placements]**.

## Identifiant

Identificateur unique de l&#39;enregistrement.

Type : chaîne

## _expérience

### prise de décision

#### Identifiant de Canal du référencement

Le canal dans lequel la proposition a été faite. La valeur est un URI de Canal valide. Voir https://ns.adobe.com/xdm/channels/channel.

Type : string

#### Type de composant de contenu

Ensemble énuméré d’URI où chaque valeur correspond à un type donné au composant de contenu. Certains consommateurs des représentations de contenu s’attendent à ce que la valeur @type soit une référence au schéma qui décrit les propriétés supplémentaires du composant de contenu.

Type : string

#### Type de support MIME

Contrainte pour le type de support des composants attendus dans ce placement. Il peut y avoir plusieurs types de supports possibles pour un composant, par exemple un format d’image différent.

Type : string

#### Description du placement

Il est utilisé pour transmettre des intentions lisibles sur la façon dont le contenu dynamique est utilisé dans la diffusion globale du message. Le fait qu&#39;un certain espace soit une \&quot;bannière\&quot; dans une page Web est souvent transmis par la description et non par une méthode formelle.

Type : string

#### Nom du placement

Nom attribué au placement pour qu’il y soit fait référence dans les interactions humaines.

Type : string

## _repo

### Placement ETag

Révision à laquelle l&#39;objet d&#39;option de décision se trouvait lors de la prise de l&#39;instantané.

Type : string
