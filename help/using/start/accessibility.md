---
solution: Journey Optimizer
product: journey optimizer
title: Fonctionnalités d’accessibilité dans Journey Optimizer
description: En savoir plus sur l’accessibilité dans l’interface utilisateur de Journey Optimizer
feature: Accessibility
role: User
level: Beginner
source-git-commit: 9555c37f8bac295a668f64990e229c6e0e5ceb8d
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 81%

---

# Accessibilité dans Journey Optimizer{#accessibility}

L’accessibilité fait référence à une série de fonctionnalités qui rendent un produit logiciel utilisable, avec le moins d’effort possible, par des utilisateurs présentant un handicap visuel, auditif, cognitif, moteur ou autre. Leader du secteur en matière d’accessibilité, Adobe soutient la création d’expériences web exceptionnelles en encourageant les développeurs à produire du contenu riche et attrayant accessible à tous les utilisateurs. En savoir plus sur l’engagement de l’Adobe envers l’accessibilité dans le [Page Accessibilité des Adobes](https://www.adobe.com/accessibility.html){target="_blank"}.

Pour aider à atteindre l’objectif de conformité à l’accessibilité, [!DNL Journey Optimizer] suit les bonnes pratiques reconnues internationalement dans les directives WCAG 2.1 sur l’accessibilité des contenus web (niveau A et niveau AA). En savoir plus dans la dernière version [Rapport de conformité à l’accessibilité de Adobe Journey Optimizer](https://www.adobe.com/accessibility/compliance/adobe-journey-optimizer-2022.html){target="_blank"}.


Les fonctionnalités d’accessibilité de [!DNL Adobe Journey Optimizer] sont héritées d’Adobe Experience Platform :

* Accessibilité à l’aide du clavier
* Contraste des couleurs
* Validation des champs obligatoires

Les fonctions d’accessibilité de Adobe Experience Platform sont détaillées. [dans cette documentation](https://experienceleague.adobe.com/docs/experience-platform/accessibility/features.html?lang=fr){target="_blank"}.

Les raccourcis clavier courants suivants sont disponibles dans la section [!DNL Journey Optimizer]:

| Action | Raccourci |
| --- | --- |
| Déplacement entre les éléments, sections et groupes de menus de l’interface utilisateur | Tabulation |
| Retour en arrière entre les éléments, sections et groupes de menus de l’interface utilisateur | Maj+Tabulation |
| Déplacement dans des sections pour définir la cible d’action sur des éléments individuels | Flèche |
| Sélection ou suppression d’un élément ciblé | Entrée ou Barre d’espace |
| Annuler une sélection, réduire un panneau ou fermer une boîte de dialogue | Échap |

Vous pouvez utiliser ces raccourcis dans des zones spécifiques de [!DNL Journey Optimizer] interface utilisateur :

<table>
  <thead>
    <tr>
      <th>Élément d’interface</th>
      <th>Action</th>
      <th>Raccourci</th>
    </tr>
  </thead>
  <tr>
    <td>Liste de parcours, d’actions, de sources de données ou d’événements</td>
    <td>Création d’un parcours, d’une action, d’une source de données ou d’un événement</td>
    <td>C</td>
  </tr>
  <tr>
    <td rowspan="3">Zone de travail de parcours à l'état de brouillon</td>
    <td>Ajoutez une activité à partir de la palette gauche à la première position disponible, du haut vers le bas.</td>
    <td>Effectuez un double clic sur l’activité.</td>
  </tr>
  <tr>
    <td>Sélection de toutes les activités</td>
    <td>Ctrl + A (Windows)<br/>Commande + A (Mac)</td>
  </tr>
  <tr>
    <td>Suppression des activités sélectionnées</td>
    <td>Suppr ou Retour arrière, puis Entrée pour confirmer la suppression</td>
  </tr>
  <tr>
    <td>Zoom avant et arrière (sélection sur la zone de travail ou l’un de ses éléments enfants)</td>
    <td>Ctrl +/- (Windows) ou Commande +/- (Mac)</td>
  </tr>  
  <tr>
    <td>Navigation entre chaque activité et chemin (sélection sur la zone de travail) ou entre les boutons de la barre d’outils (sélection sur la barre d’outils)</td>
    <td>Touches fléchées</td>
  </tr>   
  <tr>
    <td>Déplacement de la sélection vers l’élément exploitable suivant sur la zone de travail, la barre d’outils étant la première</td>
    <td>Tabulation</td>
  </tr>  
  <tr>
    <td>Ouverture du volet de configuration de droite (sélection sur une activité)</td>
    <td>Entrée</td>
  </tr>   
  <tr>
    <td>Déplacement d’une activité dans la zone de travail (sélection sur une activité)</td>
    <td>Maj + touches fléchées</td>
  </tr>  
  <tr>
  <td rowspan="3">

Volet de configuration de ces éléments :

<ul>
  <li>Activité dans un parcours</li>
  <li>Événement</li>
  <li>Source de données</li>
  <li>Action</li>
</ul>

</td>
    <td>Accès au champ suivant à configurer</td>
    <td>Tabulation</td>
  </tr>
  <tr>
    <td>Enregistrement des modifications et fermeture du volet de configuration</td>
    <td>Enter</td>
  </tr>
  <tr>
    <td>Rejet des modifications et fermeture du volet de configuration</td>
    <td>Échap</td>
  </tr>
  <tr>
    <td rowspan="4">Parcours en mode test</td>
    <td>Activation ou désactivation du mode test</td>
    <td>T</td>
  </tr>
  <tr>
    <td>Déclenchement d’un événement dans un parcours basé sur un événement</td>
    <td>E</td>
  </tr>
  <tr>
    <td>

Déclenchez un événement dans un parcours basé sur des segments pour lequel l’option **[!UICONTROL Un profil unique à la fois]** est activée.

</td>
    <td>P</td>
  </tr>
  <tr>
    <td>Affichage des journaux de test</td>
    <td>L</td>
  </tr>
<!-- //Ajouter ce raccourci quand il marchera (actuellement, le raccourci Ctrl/Cmd+F du navigateur a priorité sur celui de AJO).//
  <tr>
    <td>Page with a search bar</td>
    <td>Select the search bar</td>
    <td>Ctrl/Command + F</td>
  </tr>
-->
  <tr>
    <td>Champ de texte</td>
    <td>Sélection de tout le texte dans le champ sélectionné</td>
    <td>Ctrl + A (Windows)<br/>Commande + A (Mac)</td>
  </tr>
  <tr>
    <td rowspan="2">Fenêtre contextuelle</td>
    <td>Enregistrement des modifications ou confirmation de l’action</td>
    <td>Enter</td>
  </tr>
  <tr>
    <td>Fermeture de la fenêtre</td>
    <td>Échap</td>
  </tr>
  <tr>
    <td>Éditeur d’expression simple</td>
    <td>Sélection et ajout d’un champ</td>
    <td>Double-clic sur un champ</td>
  </tr>
  <tr>
    <td>Navigation à travers les champs XDM</td>
    <td>Sélection de tous les champs d’un nœud</td>
    <td>Sélection du nœud parent</td>
  </tr>
  <tr>
    <td>Aperçu de la payload</td>
    <td>Sélection de la payload</td>
    <td>Ctrl + A (Windows)<br/>Commande + A (Mac)</td>
  </tr>
</table>
