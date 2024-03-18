---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour anticipées de Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 2dfcbd1631c7fefccaf02782a3218c9a1c1dc7aa
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 29%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans la variable [notes de mise à jour](release-notes.md).

Les notes de mise à jour ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md), à la date de publication.

## Notes de mise à jour initiales de mars 2024 {#e-2024}

**Date de publication**: 19-20 mars 2024

### Nouvelle fonctionnalité {#e-features}

Cette version comprend la nouvelle fonctionnalité présentée ci-dessous.

<table>
<thead>
<tr>
<th><strong>Expériences basées sur le code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce au nouveau canal d’expérience basé sur le code, Adobe Journey Optimizer vous permet d’effectuer des tests et des personnalisations avancés pour l’une de vos propriétés entrantes, ce qui vous permet de diffuser facilement des expériences personnalisées sur différents points de contact tels que des applications web, des applications mobiles, des applications de bureau, des consoles vidéo, des périphériques connectés à la télévision, des téléviseurs intelligents, des kiosques, des distributeurs automatiques, des périphériques IoT, etc.</p>
<P>Les fonctionnalités principales sont les suivantes :</p>
<ul><li> Personnalisation universelle : étendez les expériences personnalisées sur tous les points de contact, en assurant un parcours utilisateur cohérent et personnalisé.</li>
<li>Précision granulaire de la modification : modifiez du contenu spécifique à des emplacements spécifiques dans vos applications ou pages web.</li>
<li>Mise en oeuvre polyvalente : prise en charge des méthodes de mise en oeuvre côté serveur, basées sur les API ou basées sur le SDK pour une intégration transparente à votre environnement de développement.</li></ul></p>
<p>Pour plus d’informations, consultez la <a href="../code-based/get-started-code-based.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/code-based.gif">
</tr>
</tbody>
</table>

### Améliorations {#e-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Modèles de contenu**

* **Miniatures** - A **Mode Grille** Le mode est désormais disponible pour les modèles de contenu, affichant des miniatures pour un accès visuel amélioré. Actuellement, seuls les modèles de HTML email sont pris en charge. [En savoir plus](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Cette fonctionnalité est publiée en disponibilité limitée pour un petit groupe de personnes.

**Parcours**

De nouveaux états intermédiaires ont été ajoutés au cycle de vie de création de parcours :

* **Publication** entre les **Version préliminaire** et la variable **En direct** status
* **Arrêt** entre les **En direct** et la variable **Stoppé** status
* **Activation du mode test** ou **Désactivation du mode test** les états entre les **Version préliminaire** et la variable **Version préliminaire (test)** status

Lorsqu’un parcours se trouve dans un état intermédiaire, il est en lecture seule.