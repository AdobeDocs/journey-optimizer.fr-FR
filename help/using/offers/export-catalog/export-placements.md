---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Jeu de données d’emplacements
description: Cette section répertorie tous les champs utilisés dans le jeu de données exporté pour les emplacements.
badge: label="Hérité" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 3e45f3cf-e17e-43a6-8424-98afef07aaa3
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/UFE7I-hQM4jKPpclDl3avrcE-q-vwRq-c91WOLdPBgo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 388
ht-degree: 71%

---

# Jeu de données d’emplacements {#placements-dataset}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)

Chaque fois qu&#39;une offre est modifiée, le jeu de données généré automatiquement pour les emplacements est mis à jour.

![](../assets/dataset-placements.png)

Le lot le plus récent dans le jeu de données s’affiche à droite. La vue hiérarchique du schéma du jeu de données s&#39;affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque des offres dans [cette section](../export-catalog/access-dataset.md).

Vous trouverez ci-dessous la liste de tous les champs qui peuvent être utilisés dans le jeu de données **[!UICONTROL Référentiel d&#39;objets de décision - Emplacements]**.

<!--A placement describes a location or place in a personalized message. It is used to set technical constraints for content that the personalization decision supplies. The placement also represents a request to produce certain types of metrics when an experience event is produced where this placement is involved. For instance, the placement facilitates a personalized clickable image inside an email shown to an end-user. The placement may for instance request from the assembled experience that the click on its image gets reported in an experience event with a metric https://ns.adobe.com/xdm/data/metrics/web/linkclicks and a reference to this placement.-->

+++ Identifiant

**Champ :** _id
**Titre :** identifiant
**Description :** identifiant unique de l’enregistrement.
**Type :** Chaîne

+++

+++ _experience

**Champ :** _experience
**Type :** objet

+++

+++ _experience > decisioning

**Champ : prise de décision**
**Type :** objet

+++

+++ _experience > decisioning > Placement&#39;s Channel Identifier

**Field:** channelID
**Titre : identifiant du canal de l&#39;emplacement**
**Description :** canal dans lequel la proposition a été effectuée. La valeur est une URI de canal valide. Voir https://ns.adobe.com/xdm/channels/channel.
**Type :** Chaîne

+++

+++ _experience > decisioning > Content Component Type

**Field:** componentType
**Titre :** type du composant du contenu
**Description** : ensemble énuméré d’URI où chaque valeur correspond à un type donné au composant de contenu. Certains consommateurs des représentations de contenu s&#39;attendent à ce que la valeur @type soit une référence au schéma qui décrit les propriétés supplémentaires du composant de contenu.
**Type :** Chaîne

+++

+++ _experience > decisioning > contentTypes

**Field:** contentTypes
**Type :** tableau

+++

+++_experience > decisioning > contentTypes > MIME Media Type

**Title :** type de média MIME
**Description :** contrainte pour le type de média des composants attendue à cet emplacement. Un composant peut avoir plusieurs types de média, par exemple différents formats d&#39;image.
**Type :** Chaîne

+++

+++ _experience > decisioning > Placement Description

**Champ :** description
**Titre :Description de l&#39;emplacement**
**Description :** permet de véhiculer les intentions lisibles par l’homme sur la manière dont le contenu dynamique est utilisé dans la diffusion globale des messages. Le fait qu&#39;un certain espace est une \&quot;bannière\&quot; sur une page web est souvent communiqué par la description et non par une méthode formelle.
**Type :** Chaîne

+++

+++ _experience > decisioning > Placement Name

**Champ :** nom
**Titre :** Nom De L’Emplacement
**Description :** nom attribué à l&#39;emplacement pour s&#39;y référer dans les interactions humaines.
**Type :** Chaîne

+++

+++ _repo

**Champ :** _repo
**Type :** objet

+++

+++ _repo > ETag d&#39;emplacement

**Champ :** etag
**Title:** ETag d’emplacement
**Description :** révision à laquelle l&#39;objet d&#39;option de décision se trouvait lors de la prise de l&#39;instantané.
**Type :** Chaîne

+++
