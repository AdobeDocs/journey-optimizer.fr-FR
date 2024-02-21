---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour anticipées de Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 1c65043965d1335297127f6cc6c23ec9a7893463
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 16%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans les [notes de mise à jour](release-notes.md).

Les notes de mise à jour ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md), à la date de publication.

## Notes de mise à jour initiales de février 2024 {#e-2024}

**Date de publication**: 21-22 février 2024

### Nouvelles fonctionnalités{#e-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.


<table>
<thead>
<tr>
<th><strong>Messagerie in-app web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser la nouvelle fonctionnalité de messagerie in-app web pour afficher du contenu personnalisé directement sur les sites web, par le biais de messages de superposition modale. Cette fonctionnalité vous permet d’interagir efficacement avec les visiteurs web, ce qui améliore l’interaction utilisateur, la rétention et les taux de conversion.<br/><br/></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Règles de fréquence pour les SMS et le courrier</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant créer des règles de fréquence pour les canaux SMS et courrier. Les règles de fréquence excluent automatiquement les profils sur-sollicités des messages et actions lorsque le plafond de fréquence est atteint. <br/><br/></p>
<img src="assets/do-not-localize/sms-dm-rules.gif">
</tr>
</tbody>
</table>

### Améliorations {#e-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Audiences**

* **Listes de contrôle** - Les variantes sont désormais prises en charge lors de l’utilisation de **listes de contrôle**. Comme chaque profil de l&#39;audience ciblée, les adresses de contrôle reçoivent une copie de toutes les variantes du même message (comme les différents traitements d&#39;une expérience de contenu).

Antérieurement disponibles en version bêta, les améliorations suivantes sont désormais disponibles pour tous les utilisateurs :

* Vous pouvez désormais cibler **audiences créées via la composition de l’audience** et exploiter les attributs d’enrichissement dans Parcours. [En savoir plus](../building-journeys/read-audience.md)

* Vous pouvez désormais cibler **audiences chargées à partir d’un fichier CSV** dans les parcours et les campagnes. [En savoir plus](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* L’utilisation d’audiences et d’attributs provenant de la composition de l’audience et du téléchargement personnalisé (fichier CSV) n’est actuellement pas disponible avec Healthcare Shield ou Privacy and Security Shield.
  >* Veuillez noter que le téléchargement de l’audience à partir d’une amélioration de fichier CSV sera graduellement déployé dans les jours qui suivront la version initiale. Certains utilisateurs auront un accès immédiat, mais d’autres peuvent rencontrer un retard avant qu’il ne soit disponible dans leurs comptes.

**Parcours**

* **Filtrage des parcours** - Vous pouvez désormais utiliser **dates personnalisées pour filtrer les parcours** inventory, en plus des filtres de dates prédéfinis existants. Vous pouvez ainsi affiner la liste en affichant les parcours publiés à une date spécifique, au cours d’un mois donné, sur une année entière ou dans des périodes spécifiées.
* **Actions personnalisées** - Vous pouvez désormais mettre à jour l’en-tête &quot;content-type&quot; dans **actions personnalisées**.
* **Configuration** - L’attribut identityMap dans stepEvents est maintenant prérenseigné. L’identité principale est définie comme &quot;primary = true&quot;.
* **Interface utilisateur** - La barre supérieure, dans les écrans de parcours, a été réorganisée pour une expérience améliorée. Parmi les différentes mises à jour, l’icône &quot;crayon&quot; permettant d’accéder aux propriétés du parcours s’affiche désormais sur la gauche de la barre supérieure, en regard du nom du parcours.

**Canal SMS**

* **Mots-clés d’inclusion/exclusion** - Lors de la configuration de votre canal SMS, vous pouvez désormais personnaliser le **Mots-clés d’inclusion et d’exclusion** selon vos préférences. Journey Optimizer déclenche la réponse en fonction de ces mots-clés spécifiés.

**Campagnes**

* **Campagnes déclenchées par l’API** - Le code cURL généré après l’activation d’une campagne déclenchée par une API a été amélioré. Elle inclut désormais toutes les variables de personnalisation (profil et contexte) utilisées dans le message.

**Gestion des décisions**

* **Règles de limitation** - Vous pouvez maintenant ajouter **plusieurs règles de limitation** pour une offre. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées.

**Modèles de contenu**

* **Miniature** - A **vue miniature** est désormais disponible pour les modèles de contenu et les fragments afin d’améliorer l’accès visuel.

  >[!AVAILABILITY]
  >
  >Cette fonctionnalité est progressivement déployée dans les environnements clients à partir de cette version.

* **Modèles multicanaux** - Des modèles de contenu sont désormais disponibles pour **tous les canaux**, à l’exception du Web. Pour Email, vous pouvez maintenant sélectionner le type (HTML ou Contenu).
