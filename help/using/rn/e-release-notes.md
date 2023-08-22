---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour anticipées de Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: f528c2f11000d323370f06210c70a127a99f905d
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 42%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans les [notes de mise à jour](release-notes.md).

Les notes de mise à jour ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version. Les liens, les écrans et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md), à la date de publication.

## Notes de mise à jour initiales d’août 2023 {#aug-rn-2023}

**Date de publication**: 23-24 août 2023

### Nouvelles fonctionnalités{#aug-2023-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Envoyer des messages In-App dans vos parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais envoyer des messages In-App personnalisés aux utilisateurs de votre application dans un parcours. Utilisez Journey Optimizer pour concevoir des notifications et personnaliser la mise en page, l’affichage, le texte et les boutons des messages afin de créer une expérience optimale.</p>
<img src="assets/in_app_journey_1.png"/>
<p>Pour plus d’informations, consultez la <a href="../in-app/get-started-in-app.md">documentation détaillée</a>.</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Valider vos emails avec des listes de contrôle</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer et gérer des listes de contrôle dans Journey Optimizer. Une liste de contrôle consiste en des adresses de messagerie de test auxquelles vous envoyez un courrier électronique avant de l’envoyer à votre audience réelle. Utilisez cette fonctionnalité pour surveiller les copies d’emails envoyées et vous assurer que tous les formats d’affichage, URL, images et liens sont corrects.</p>
<img src="../configuration/assets/seed-list-details.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Générer du texte et des images avec l’assistant de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une fois que vous avez créé et personnalisé votre message, repositionnez votre contenu au niveau supérieur avec l'assistant Contenu. Vous pouvez désormais utiliser l’assistant de contenu pour optimiser l’impact de votre message en testant différents titres et images principaux. Chaque variante est gérée en tant que Traitement unique, afin de mesurer et de comparer quel titre génère plus de clics.</p>
<p>Cette fonctionnalité est actuellement disponible en version bêta privée.</p>
<img src="assets/gen-ai-image-2.png"/>
<!--p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>



### Améliorations {#aug-2023-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**API**

Une nouvelle API pour créer et gérer des fragments de contenu est désormais disponible. [En savoir plus](https://developer.adobe.com/journey-optimizer-apis/references/content-templates/#tag/Content-fragment-API){target="_blank"}.

**Canal e-mail**

* Une nouvelle option est disponible dans les paramètres de surface des emails pour inclure les adresses email supprimées en raison d’une plainte de spam dans vos audiences de messages transactionnels. Même s’ils ont marqué des messages marketing comme spam, ces profils peuvent alors recevoir des messages transactionnels, tels que la réinitialisation du mot de passe ou les instructions de compte. Par défaut, cette option est désactivée.

**Parcours**

* Vous pouvez désormais utiliser les réponses d’appel API dans des actions personnalisées et orchestrer votre parcours en fonction de ces réponses. Cette fonctionnalité est publiée sous forme de version Private Beta.
* Introduction d’un nouveau type d’alerte système. Vous pouvez désormais recevoir une notification en cas d’échec d’une action personnalisée.


**Courrier**

* Prise en charge d’Azure Blob en tant que destination de routage.
* Assistance `&` comme séparateur personnalisé.