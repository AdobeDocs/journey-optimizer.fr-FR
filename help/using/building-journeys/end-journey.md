---
solution: Journey Optimizer
product: journey optimizer
title: Fin de parcours
description: Découvrez comment un parcours se termine dans Journey Optimizer.
feature: Journeys
role: User
level: Intermediate
keywords: rentrée, parcours, fin, dynamique, arrêt
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-mknoNfkNCnfnLD1UCiA6C88NjookKqGr5tQdJ-f3T4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: d7dd6f7f-9e2a-47ee-a2bc-b7b9caaefc1d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1779
ht-degree: 50%

---

# Terminer un parcours {#journey-ending}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment les parcours se terminent à la fois pour les profils individuels et globalement, et comment fermer ou arrêter un parcours dynamique lorsque vous devez arrêter de nouvelles entrées ou tout traitement.

>[!ENDSHADEBOX]

>[!TIP]
>
>Vous recherchez des conseils pratiques sur quand et comment les profils doivent quitter les parcours ? Consultez notre [guide complet des critères d’entrée et de sortie de parcours](entry-exit-criteria-guide.md), qui comprend des scénarios de sortie réels, des bonnes pratiques et des conseils de configuration.

## Fin d’un parcours dynamique

Les parcours sont fermés lorsque la temporisation globale du parcours est atteinte ou après la dernière occurrence d’un parcours récurrent basé sur l’audience. [Découvrir comment les parcours sont fermés](#close-journey).

Pour terminer un parcours dynamique, nous vous recommandons de [le clôturer](#close-to-new-entrances) manuellement. L’arrivée de nouvelles personnes dans le parcours sera alors bloquée. Les profils qui ont déjà rejoint le parcours peuvent l’expérimenter jusqu’à la fin.

Vous pouvez également [arrêter un parcours](#stop-journey), uniquement en cas d’urgence et si tout le traitement du parcours doit être arrêté immédiatement. Les personnes qui l’ont déjà rejoint sont toutes arrêtées dans leur progression.

>[!IMPORTANT]
>
>* Vous ne pouvez pas redémarrer ou supprimer un parcours [fermé](#close-journey) ou [arrêté](#stop-journey). Vous pouvez [le dupliquer](journey-ui.md#duplicate-a-journey) ou en [créer une nouvelle version](publish-journey.md#journey-versions).
>
>* Seuls les parcours terminés peuvent être supprimés.

## Terminaison d’un parcours par les profils

Un parcours peut se terminer pour une personne dans deux contextes spécifiques :

* L’individu atteint la dernière activité d’un chemin, puis passe à la [balise de fin](#end-tag).
* L’individu arrive à une activité **Condition** (ou à une activité **Attente** avec une condition) et ne répond à aucune des conditions.

L’individu peut alors rejoindre à nouveau le parcours si une nouvelle entrée est autorisée. [En savoir plus sur la gestion des entrées/rentrées](../building-journeys/journey-properties.md#entrance)

## Balise de fin de parcours {#end-tag}

Lors de la création d’un parcours, une « balise de fin » s’affiche à la fin de chaque chemin. Ce nœud ne peut pas être ajouté par un utilisateur ou une utilisatrice, ne peut pas être supprimé et seul son libellé peut être modifié. Il marque la fin de chaque chemin du parcours.

Si le parcours comporte plusieurs chemins, il est conseillé d’ajouter un libellé à chaque fin pour faciliter la lecture des rapports. En savoir plus sur les [rapports de parcours](../reports/live-report.md).

![Bouton d’action Terminer le parcours dans la barre d’outils du parcours](assets/journey-end.png)

## Fermeture d’un parcours {#close-journey}

Les raisons suivantes peuvent entraîner la fermeture d&#39;un parcours :

* Un parcours Lecture d’audience non récurrent **s’arrête automatiquement** une fois que le dernier profil quitte le parcours. [En savoir plus](#auto-stop-non-recurring)
* Après la dernière occurrence d’un parcours récurrent basé sur une audience.
* Le parcours est fermé manuellement par le biais du bouton [**[!UICONTROL Fermer aux nouvelles entrées]**](#close-to-new-entrances).
* Le délai d’expiration global du parcours de 91 jours est atteint.

Après la **temporisation globale de 91 jours**, le statut d’un parcours de lecture d’audience passe à **Terminé**. Ce comportement est défini uniquement sur 91 jours, car toutes les informations relatives aux profils qui ont rejoint le parcours sont supprimées 91 jours après leur entrée. Les personnes toujours présentes dans le parcours sont automatiquement affectées. Elles quittent le parcours après la temporisation de 91 jours.  En savoir plus sur [la temporisation globale d’un parcours](../building-journeys/journey-properties.md#global_timeout).

### Arrêt automatique des parcours pour les audiences non récurrentes {#auto-stop-non-recurring}

Un parcours **Lecture d’audience non récurrent** passe automatiquement au statut **[!UICONTROL Arrêté]** une fois que le dernier profil quitte le parcours. Cela élimine le comportement précédent où les parcours Lecture d’audience non récurrents conservaient le statut **Actif** jusqu’à l’expiration du délai d’expiration global de 91 jours, même si aucun profil ne les traversait activement.

**Fonctionnement :**

1. Le parcours s’exécute et tous les profils de l’audience sont traités.
1. Lorsque chaque profil atteint la fin du parcours, il se ferme normalement.
1. Lorsque le **dernier profil actif se ferme**, le parcours passe automatiquement au statut **[!UICONTROL Arrêté]**.

Ce comportement s’applique uniquement aux parcours Lecture d’audience non récurrents **.** Les parcours récurrents ne sont pas affectés.

>[!NOTE]
>
>* Ce comportement d’arrêt automatique ne s’applique **pas** aux parcours non récurrents qui incluent des nœuds provoquant des périodes d’attente, tels que les nœuds **Wait** (basés sur le minuteur), **Reaction** (qui attendent des événements tels que l’ouverture ou le clic d’un e-mail) ou les transitions déclenchées par un événement. Ces parcours restent soumis à la temporisation globale standard [91 jours](../building-journeys/journey-properties.md#global_timeout).
>
>* Vous pouvez toujours fermer manuellement à tout moment un parcours Lecture d’audience non récurrent à l’aide de l’option [**[!UICONTROL Fermer aux nouvelles entrées]**](#close-to-new-entrances). Le comportement d’arrêt automatique permet simplement de s’assurer que le parcours s’arrête automatiquement lorsqu’il n’est plus nécessaire, sans nécessiter d’intervention manuelle.

### Quand un parcours est-il considéré comme « terminé » ? {#journey-finished-definition}

La définition de « terminé » varie en fonction du type de parcours :

| Type de parcours | Récurrent ? | A une date de fin ? | Définition de « terminé » |
|--------------|------------|---------------|--------------------------|
| Lecture d’audience | Non | S.O. | Lorsque le dernier profil se ferme (arrêt automatique) |
| Lecture d’audience | Oui | Non | 91 jours après le début de la dernière occurrence |
| Lecture d’audience | Oui | Oui | Lorsque la date de fin est atteinte |
| Parcours déclenché par un événement | S.O. | Oui | Lorsque la date de fin est atteinte |
| Parcours déclenché par un événement | S.O. | Non | Si fermeture dans l’interface d’utilisation ou via l’API |

### Fermer aux nouvelles entrées {#close-to-new-entrances}

Le fait de fermer un parcours manuellement assure que les clients qui l’ont déjà rejoint puissent terminer leur chemin, mais que les nouveaux utilisateurs ne puissent pas le rejoindre. Lorsqu&#39;un parcours est fermé (pour l&#39;une des raisons ci-dessus), le statut **[!UICONTROL Fermé]** lui est attribué. Il n’est alors plus accessible aux nouvelles personnes. Les profils déjà présents dans le parcours peuvent terminer le parcours normalement. Au-delà de la temporisation globale par défaut de 91 jours, le statut du parcours passe à **Terminé**.

Vous pouvez arrêter un parcours dont l’état est **En ligne** ou **En pause**. Lorsque le parcours est **En pause**, vous n’avez pas besoin de le reprendre au préalable au statut **En ligne**. [En savoir plus sur l’arrêt d’un parcours en pause](journey-pause.md#stop-close-paused).

Pour fermer un parcours dans la liste des parcours, cliquez sur le bouton **[!UICONTROL Points de suspension]** situé à droite du nom du parcours et sélectionnez **[!UICONTROL Fermer aux nouvelles entrées]**.

![Liste déroulante Terminer l’action dans le menu des actions rapides pour terminer le parcours](assets/journey-finish-quick-action.png)

Vous pouvez également réaliser les opérations suivantes :

1. Dans la liste **[!UICONTROL Parcours]**, cliquez sur le parcours que vous souhaitez fermer.
1. En haut à droite, cliquez sur la flèche vers le bas.

   ![Menu des options de fin affichant terminer le parcours et les actions alternatives](assets/finish_drop_down_list.png){width="50%" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Fermer aux nouvelles entrées]** et confirmez dans la boîte de dialogue.


## Arrêt d’un parcours {#stop-journey}

Si nécessaire, il est possible d’arrêter la progression de toutes les personnes dans le parcours. L’arrêt du parcours entraîne une temporisation pour toutes les personnes présentes dans le parcours. Cependant, l’arrêt d’un parcours entraîne l’arrêt de la progression de toutes les personnes qui y participent. Le parcours est simplement mis à l&#39;arrêt. Si vous souhaitez mettre fin à un parcours, la bonne pratique consiste [à le fermer](#close-journey).

Vous pouvez également arrêter directement un parcours **En pause**, sans le reprendre en **En ligne** au préalable. [En savoir plus](journey-pause.md#stop-close-paused).

Vous pouvez arrêter un parcours, par exemple, si un spécialiste marketing se rend compte que le parcours cible une audience incorrecte ou si une action personnalisée censée diffuser des messages ne fonctionne pas correctement. Pour arrêter un parcours dans la liste des parcours, cliquez sur le bouton **[!UICONTROL Points de suspension]** situé à droite du nom du parcours et sélectionnez **[!UICONTROL Arrêter]**.

![Liste déroulante Terminer l’action dans le menu des actions rapides pour terminer le parcours](assets/journey-finish-quick-action.png)

Vous pouvez également réaliser les opérations suivantes :

1. Dans la liste **[!UICONTROL Parcours]**, cliquez sur le parcours que vous souhaitez arrêter.
1. En haut à droite, cliquez sur la flèche vers le bas.

   ![Options de fin supplémentaires, notamment fermeture du parcours et nettoyage](assets/finish_drop_down_list2.png){width="50%" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Arrêter]** et confirmez dans la boîte de dialogue.

À l’arrêt, le statut du parcours est défini sur **[!UICONTROL Arrêté]**.

>[!CAUTION]
>
>L’arrêt d’un parcours nécessite l’autorisation **[!DNL Manage journeys]** . Si le parcours comprend des campagnes intégrées ou des nœuds de messagerie, les utilisateurs doivent également disposer des autorisations **Campagnes > Publier les campagnes**. Si le parcours utilise des ressources (par exemple, dans des e-mails), les utilisateurs doivent avoir accès à ces dossiers de ressources. Pour en savoir plus sur la gestion des droits d’accès des utilisateurs et des utilisatrices [!DNL Journey Optimizer], consultez [cette section](../administration/permissions-overview.md).

## Rubriques connexes

* [Guide des critères d’entrée et de sortie de parcours](entry-exit-criteria-guide.md) : guide complet avec des exemples réels et des bonnes pratiques.
* [Gestion des entrées de profil](entry-management.md) : configurez la manière dont les profils rejoignent les parcours.
* [Configurer les critères de sortie](journey-properties.md#exit-criteria) : configurez la suppression automatique des profils des parcours.
* [Mettre en pause un parcours ](journey-pause.md) : arrêtez temporairement l’exécution du parcours.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page explique les différentes manières dont un parcours en ligne peut se terminer (y compris le délai d’expiration global de 91 jours, la fermeture manuelle des nouvelles entrées et l’arrêt d’urgence), ainsi que leurs effets sur les profils en cours.

**Intentions:**

* Fermer un parcours dynamique à de nouvelles entrées tout en permettant aux profils actuels de le terminer
* Arrêter immédiatement un parcours pour arrêter tous les profils en cours
* Comprendre la différence entre les statuts de parcours Fermé, Arrêté et Terminé
* Déterminer quand un parcours est considéré comme « terminé » en fonction de son type et de sa configuration
* Supprimer un parcours une fois qu’il a atteint le statut Terminé

**Glossaire:**

* **Balise de fin** : nœud non amovible généré automatiquement et affiché à la fin de chaque chemin de parcours lors de la création ; son libellé peut être modifié *(spécifique au produit)*
* **Fermer aux nouvelles entrées** : action manuelle qui empêche les nouveaux profils d’entrer dans un parcours tout en permettant aux profils existants de terminer leur chemin d’accès *(spécifique au produit)*
* **Délai d’expiration global du parcours** : délai maximal de 91 jours après lequel un parcours passe automatiquement au statut Terminé et toutes les données de profil sont supprimées *(spécifique au produit)*
* **Statut Arrêté** : statut de parcours dans lequel tous les profils en cours sont immédiatement arrêtés ; utilisé uniquement pour les urgences *(spécifique au produit)*

**Mécanismes de sécurisation :**

* Les parcours fermés et arrêtés ne peuvent pas être redémarrés ni supprimés ; seule une nouvelle version ou un doublon peut être créé.
* Seuls les parcours dont le statut est Terminé peuvent être supprimés.
* L’arrêt d’un parcours nécessite l’autorisation Gestion des parcours ; les parcours avec des campagnes intégrées ou des nœuds de messagerie nécessitent également l’autorisation Campagnes > Publier les campagnes .
* Au-delà de la temporisation globale de 91 jours, toutes les données de parcours de profil sont supprimées et les profils restants sont automatiquement fermés.
* Un parcours Lecture d’audience unique reste à l’état Actif après son exécution. Il doit être fermé manuellement ou se fermera après 91 jours.

**Terminologie:**

* Nom canonique : Fermer aux nouvelles entrées — Acronyme : s.o. — variantes : fermer le parcours, fermer manuellement
* Synonymes : parcours « Arrêté » ≠ parcours « Fermé » : arrêté interrompt immédiatement tous les profils ; fermé ne bloque que les nouvelles entrées
* Ne pas confondre : « Balise de fin » ≠ « Activité de fin » — La balise de fin est générée automatiquement et ne peut pas être supprimée ; l&#39;activité de fin est un nœud de zone de travail positionnable

**FAQ:**

* **Q : Quelle est la différence entre fermer et arrêter un parcours ?** : la fermeture bloque les nouvelles entrées tout en laissant les profils existants se terminer ; l&#39;arrêt interrompt immédiatement tous les profils dans leur trajectoire.
* **Q : Quand un parcours Lecture d’audience atteint-il le statut Terminé ?** — 91 jours après le début de l&#39;exécution (non récurrent), lorsque la date de fin est atteinte (récurrent avec date de fin), ou 91 jours après le début (récurrent sans date de fin).
* **Q : Puis-je supprimer un parcours fermé ?** — Non, seuls les parcours terminés peuvent être supprimés.
* **Q : Qu’advient-il des profils toujours dans un parcours lorsque le délai d’expiration de 91 jours atteint ?** — Ils sont automatiquement sortis du parcours à ce stade.
* **Q : Ai-je besoin d’autorisations spéciales pour arrêter un parcours ?** — Oui, l’autorisation Gérer les parcours est requise, plus Campagnes > Publier les campagnes si le parcours contient des campagnes intégrées ou des nœuds de messagerie.

+++
