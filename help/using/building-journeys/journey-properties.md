---
solution: Journey Optimizer
product: journey optimizer
title: Définir les propriétés de votre parcours
description: Découvrir comment définir les propriétés de votre parcours avec Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: parcours, configuration, propriétés
exl-id: 6c21371c-6cbc-4d39-8fe6-39f1b8b13280
source-git-commit: 43cf43c6ba92d64836222ce872054b5dec6d11fe
workflow-type: tm+mt
source-wordcount: '2259'
ht-degree: 96%

---

# Définir les propriétés de votre parcours {#jo-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Propriétés du parcours"
>abstract="Cette section présente les propriétés du parcours. Par défaut, les paramètres en lecture seule sont masqués. Les paramètres disponibles dépendent du statut du parcours, de vos autorisations et de la configuration de votre produit."

## Accéder aux propriétés d’un parcours {#access-properties}

Les propriétés d’un parcours sont centralisées dans le rail de droite. Cette section est affichée par défaut lors de la création d’un parcours. Pour les parcours existants, cliquez sur l’icône en forme de crayon à côté du nom du parcours pour l’ouvrir.

Depuis cette section, vous pouvez définir le nom du parcours, ajouter une description et :

* gérer [l’entrée et la rentrée](#entrance),
* choisir les [dates](#dates) de début et de fin,
* gérer [l’accès aux données](#manage-access),
* définir une [durée de temporisation](#timeout) dans les activités de parcours (pour les personnes chargées de l’administration uniquement),
* sélectionner les [fuseaux horaires](#timezone) des parcours et des profils,
* attribuer des balises unifiées Adobe Experience Platform à votre parcours afin de les classer facilement et d’améliorer la recherche dans la liste des campagnes. [Découvrir comment utiliser les balises](../start/search-filter-categorize.md#tags)
* Surveillez les conflits et gérez la priorité de vos parcours à l’aide des [outils de gestion des conflits](#conflict).

![](assets/journey32.png)

>[!NOTE]
>
>Pour les parcours actifs, cet écran affiche la date de publication et le nom de l’utilisateur ou de l’utilisatrice qui a publié le parcours.

La fonction **Copier les détails techniques** permet de copier les informations techniques relatives au parcours qui seront utiles à l’équipe d’assistance technique pour résoudre les problèmes. Les informations suivantes sont copiées : `JourneyVersion UID`, `OrgID`, `orgName`, `sandboxName`, `lastDeployedBy`, `lastDeployedAt`.

Pour plus d’informations sur les champs techniques liés à un parcours pour un profil donné et comment les utiliser, consultez [cette page](expression/journey-properties.md).

## Entrée et rentrée {#entrance}

Le mode d’entrée des profils est défini au niveau du parcours, dans le volet de configuration de droite. Les paramètres sont décrits ci-dessous.

La gestion des entrées de profil dépend du type de parcours. Pour plus d’informations sur la gestion des entrées et des rentrées de profils, consultez [cette page](entry-management.md).

### Autoriser une nouvelle rentrée  {#allow-reentrance}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_entrance"
>title="Autoriser une nouvelle rentrée"
>abstract="Par défaut, les nouveaux parcours autorisent la rentrée. Vous pouvez décocher l&#39;option **Autoriser une rentrée** si vous souhaitez par exemple offrir un cadeau unique à un utilisateur ou une utilisatrice qui effectue sa première visite dans la boutique."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="Gestion des entrées de profil"

Par défaut, les nouveaux parcours autorisent la rentrée. Vous pouvez désélectionner l’option **Autoriser la rentrée** pour les parcours « uniques », par exemple, si vous souhaitez offrir un cadeau unique à un utilisateur ou une utilisatrice qui effectue sa première visite dans la boutique.

### Période d’attente de nouvelle entrée  {#reentrance-wait}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_re-entrance_wait"
>title="Période d’attente de nouvelle entrée"
>abstract="Définissez le temps d’attente avant de permettre à un profil de reprendre le parcours dans les parcours unitaires. Cela empêche les utilisateurs et utilisatrices d’entrer de nouveau dans le parcours pendant une durée donnée. Durée maximale : 90 jours."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="Gestion des entrées de profil"

Lorsque l’option **Autoriser une rentrée** est activée, le champ **Période d’attente de rentrée** s’affiche. Ce champ vous permet de définir le temps d’attente avant d’autoriser un profil à entrer à nouveau dans un parcours pour les parcours unitaires (en commençant par un événement ou une qualification d’audience). Cela empêche les parcours d’être déclenchés plusieurs fois par erreur pour le même événement. Par défaut, le champ est défini sur 5 minutes. La durée maximale est de 90 jours.


## Gérer l’accès {#manage-access}

Pour attribuer des libellés d’utilisation des données personnalisés ou de base au parcours, cliquez sur le bouton **[!UICONTROL Gérer l’accès]**. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

## Fuseaux horaires des parcours et des profils {#timezone}

Le fuseau horaire est défini au niveau du parcours. Vous pouvez entrer un fuseau horaire fixe ou utiliser les profils Adobe Experience Platform pour définir le fuseau horaire du parcours. Si un fuseau horaire est défini dans le profil Adobe Experience Platform, il peut être récupéré dans le parcours.

Pour plus d&#39;informations sur la gestion des fuseaux horaires, voir [cette page](../building-journeys/timezone-management.md).

## Dates de début et de fin {#dates}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_start_date"
>title="Date de début"
>abstract="Sélectionnez la date à laquelle l’entrée dans le parcours peut commencer. Si aucune date de début n’est spécifiée, elle est automatiquement définie au moment de la publication."


>[!CONTEXTUALHELP]
>id="ajo_journey_properties_end_date"
>title="Date de fin"
>abstract="Sélectionnez la date de fin de votre parcours. Une fois cette date atteinte, les profils de ce parcours le quittent automatiquement et les nouveaux ne peuvent plus y entrer."

Vous pouvez définir une **date de début**. Si vous n’en avez pas spécifié une, elle sera automatiquement définie au moment de la publication.

Vous pouvez également ajouter une **date de fin**. Cela permet aux profils de se fermer automatiquement lorsque la date est atteinte. Si aucune date de fin n’est spécifiée, les profils peuvent rester jusqu’à la [temporisation globale du parcours](#global_timeout) (ce qui correspond généralement à 91 jours). La seule exception concerne les parcours de lecture d’audience récurrents avec l’option **Forcer une rentrée sur la périodicité** activée, qui se termine à la date de début de l’occurrence suivante.

## Temporisation {#timeout}

### Temporisation ou erreur dans les activités du parcours {#timeout_and_error}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_timeout"
>title="Temporisation"
>abstract="Définissez la durée pendant laquelle le parcours tentera d’exécuter une action ou de vérifier une condition avant de considérer que le délai a expiré."


Lorsque vous modifiez une action ou une activité de condition, vous pouvez définir un autre chemin en cas d’erreur ou de temporisation. Si la durée de traitement de l’activité qui interroge un système tiers dépasse la durée de temporisation définie dans le champ **[!UICONTROL Temporisation ou erreur]** des propriétés du parcours, le deuxième chemin d’accès est choisi pour effectuer une éventuelle action de remplacement.

Les valeurs autorisées sont comprises entre 1 et 30 secondes.

Nous vous recommandons de définir une valeur très basse pour **[!UICONTROL Temporisation ou erreur]** si votre parcours est sensible au temps (c’est le cas, par exemple, lorsqu’il convient de réagir à l’emplacement d’une personne en temps réel), car l’action ne peut pas être différée de plus de quelques secondes. Si le facteur temps revêt une importance moindre, vous pouvez définir un délai plus long afin d’accorder davantage de temps au système appelé pour envoyer une réponse valide.

Les parcours utilisent également une temporisation globale comme décrit ci-dessous.

### Temporisation de parcours globale {#global_timeout}

En plus de la [temporisation](#timeout_and_error) utilisée dans les activités de parcours, une temporisation globale de parcours est appliquée. Elle ne s’affiche pas dans l’interface et ne peut pas être modifiée.

Cette temporisation globale met fin à la progression des personnes dans le parcours **91 jours** après leur entrée. En d’autres termes, la durée du parcours d’une personne ne peut pas excéder 91 jours. Après cette période de temporisation, les données de cette personne sont supprimées. Les personnes qui sont encore actives dans le parcours au terme de cette période de temporisation seront arrêtées et ne seront pas prises en compte dans le cadre du reporting. Vous pouvez donc voir plus de personnes rejoindre le parcours que le quitter.

Compte tenu de la temporisation de 91 jours du parcours, lorsque la rentrée de celui-ci n’est pas autorisée, nous sommes dans l’impossibilité de garantir que le blocage de la rentrée fonctionnera plus de 91 jours. En effet, étant donné que nous supprimons toutes les informations sur les personnes qui ont rejoint le parcours 91 jours après leur entrée, rien ne nous permet de savoir qu’une personne l’a déjà rejoint il y a plus de 91 jours.

Une personne ne peut entrer dans une activité d’attente que si elle dispose de suffisamment de temps dans le parcours pour terminer la durée d’attente avant la temporisation de 91 jours du parcours. Consultez [cette page](../building-journeys/wait-activity.md).


#### Questions fréquentes sur la durée de vie (TTL) et la rétention des données {#timeout-faq}

À compter de la version de juin 2024 d’Adobe Journey Optimizer, la temporisation globale du parcours est passée de 30 à 91 jours. Les impacts sont répertoriés dans les questions fréquentes ci-dessous :

**Pour les parcours unitaires**
<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Qu’advient-il du parcours publié après le déploiement de l’extension de la durée de vie ?</p>
    </td>
    <td>
      <p>Les profils entrant dans le nouveau parcours auront automatiquement une durée de vie (TTL) de 91 jours.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Qu’advient-il d’un profil entrant dans un parcours publié avant le lancement de l’extension de la durée de vie ?</p>
    </td>
    <td>
      <p>Le profil conserve une durée de vie de 30 jours (7 jours pour HIPAA), en fonction de l’heure à laquelle le parcours a été publié à l’origine.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Que se passe-t-il pour un profil qui a déjà accédé à un parcours au lancement de l’extension de la durée de vie ?</p>
    </td>
    <td>
      <p>Le profil conserve une durée de vie de 30 jours (7 jours pour HIPAA), selon l’heure de publication originale du parcours.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Qu’advient-il d’un profil dans une version de parcours précédente qui est republiée après le lancement de l’extension de la durée de vie ?</p>
    </td>
    <td>
      <p>Le profil conserve une durée de vie de 30 jours (7 jours pour HIPAA), alignée sur l’heure de publication originale du parcours.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Qu’advient-il d’un nouveau profil entrant dans une version de parcours republiée après le lancement de l’extension de la durée de vie ?</p>
    </td>
    <td>
      <p>Le profil conserve une durée de vie de 91 jours, correspondant à la durée de vie de la nouvelle version de parcours republiée.</p>
    </td>
  </tr>
</table>

**Pour les parcours de déclenchement de segment**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>Qu’advient-il des nouveaux parcours uniques publiés après l’extension de la durée de vie ?</p>
    </td>
    <td>
      <p>Les profils entrant dans le nouveau parcours auront une durée de vie de 91 jours automatiquement.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Qu’advient-il des nouveaux parcours récurrents sans nouvelle reprise forcée publiée après l’extension de la durée de vie ?</p>
    </td>
    <td>
      <p>Les profils entrant dans le nouveau parcours auront une durée de vie de 91 jours automatiquement.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Qu’advient-il des nouveaux parcours récurrents avec une reprise forcée publiée après l’extension de la durée de vie ?</p>
    </td>
    <td>
      <p>Les profils entrant dans le nouveau parcours auront une durée de vie égale à la période de périodicité. Par exemple, si le parcours s’exécute tous les jours, la durée de vie est d’1 jour.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Qu’advient-il d’un profil entrant dans un parcours publié avant le lancement de l’extension de la durée de vie ?</p>
    </td>
    <td>
      <p>Le profil conserve une durée de vie de 30 jours (7 jours pour HIPAA), cohérente avec l’heure de publication originale du parcours. Pour les parcours récurrents avec une reprise forcée, la durée de vie correspond à la période de périodicité.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Qu’advient-il d’un profil s’exécutant par le biais d’un parcours lorsque l’extension de la durée de vie est lancée ?</p>
    </td>
    <td>
      <p>Le profil conserve une durée de vie de 30 jours (7 jours pour HIPAA), selon l’heure de publication originale du parcours. Pour les parcours récurrents avec une reprise forcée, la durée de vie correspond à la période de périodicité.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Qu’advient-il d’un profil en cours d’exécution dans une version de parcours précédente qui est republiée après le lancement de l’extension de la durée de vie ?</p>
    </td>
    <td>
      <p>Le profil conserve une durée de vie de 30 jours (7 jours pour HIPAA), alignée sur l’heure de publication originale du parcours. Pour les parcours récurrents avec une reprise forcée, la durée de vie correspond à la période de périodicité.</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>Qu’advient-il d’un nouveau profil entrant dans une version de parcours republiée après le lancement de l’extension de la durée de vie ?</p>
    </td>
    <td>
      <p>Le profil conserve une durée de vie de 91 jours, correspondant à la durée de vie de la nouvelle version de parcours republiée. Pour les parcours récurrents avec une reprise forcée, la durée de vie correspond à la période de périodicité.</p>
    </td>
  </tr>
</table>

## Politiques de fusion {#merge-policies}

Le parcours utilise des politiques de fusion lors de la récupération des données de profil d’Adobe Experience Platform. Selon le type de parcours, différentes politiques de fusion sont utilisées :

* Dans les parcours Lecture d’audience ou Qualification d’audience : la politique de fusion de l’audience est utilisée
* Dans les parcours d’événements unitaires : la politique de fusion par défaut est utilisée.
* Dans les parcours d’événements métier : la politique de fusion de l’audience ciblée dans l’activité Lecture d’audience suivante est utilisée.

Le parcours respecte la politique de fusion utilisée tout au long du parcours. Par conséquent, si de multiples audiences sont utilisées dans un parcours (par exemple dans les fonctions « inAudience »), créant des incohérences avec la politique de fusion utilisée par le parcours, une erreur se produit et la publication est bloquée. Cependant, si une audience incohérente est utilisée dans la personnalisation des messages, une alerte n’est pas déclenchée, malgré l’incohérence. C’est pourquoi il est vivement recommandé de vérifier la politique de fusion associée à votre audience lorsque cette audience est utilisée dans la personnalisation des messages.

Pour en savoir plus sur les politiques de fusion, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.


## Critères de sortie {#exit-criteria}

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="Critères de sortie de parcours"
>abstract="Cette section présente les options des critères de sortie. Vous pouvez créer une ou plusieurs règles de critères de sortie pour votre parcours."

### Description {#exit-criteria-desc}

En ajoutant des critères de sortie, vous faites quitter le parcours aux profils dès qu’un événement se produit (un achat, par exemple) ou qu’ils répondent aux critères d’une audience. Cela évite à l’utilisateur ou à l’utilisatrice de recevoir d’autres communications du parcours.

Vous pouvez supprimer des profils d’un parcours lorsqu’ils ne remplissent plus l’objectif du parcours. Pour ce faire, utilisez les **critères de sortie globale**, qui sont étroitement associés à la gestion des objectifs.

**Exemple de cas d’utilisation**

Une personne spécialiste du marketing dispose d’un parcours promotionnel avec une série de communications. Chacune de ces communications a pour but d’inciter le client ou la cliente à effectuer un achat. Dès que l’achat est effectué, le client ou la cliente ne doit pas recevoir le reste des messages de la série. En définissant un critère de sortie, tous les profils ayant effectué un achat sont supprimés du parcours.

### Configuration et utilisation {#exit-criteria-config}

Les critères de sortie sont définis au niveau du parcours. Un parcours peut comporter plusieurs critères de sortie. Lorsque plusieurs critères de sortie sont définis, l’évaluation se fait de haut en bas avec une logique `OR`. Ainsi, si vous disposez des critères de sortie A et B, ils seront évalués en tant que A **OU** B. Les critères sont évalués à chaque étape du parcours.

Pour **créer** un critère de sortie, procédez comme suit :

1. Ouvrez votre parcours.

1. Cliquez sur l’icône ![](assets/do-not-localize/Smock_UserCheckedOut_18_N.svg) **[!UICONTROL Afficher les critères de sortie]** située dans la section supérieure droite de la zone de travail du parcours.

1. Sélectionnez **[!UICONTROL Ajouter un critère de sortie]**.

1. Saisissez un **libellé** et sélectionnez si votre critère de sortie est basé sur un **événement** ou une **audience**.

   * Pour les critères de sortie basés sur un événement, comme le téléchargement d’une application ou l’ajout d’un produit à un panier, sélectionnez uniquement un événement unitaire.
   * Pour Quitter les critères en fonction d’une audience, par exemple une audience qui vérifie si un client a effectué un achat au cours des dernières 24 heures, sélectionnez une audience. Note : pour être efficaces, les critères de sortie utilisant une audience peuvent prendre jusqu’à 10 minutes.

Vous pouvez ajouter plusieurs critères de sortie.

![](assets/exitcriteria-sample.png){width="40%" align="left"}

### Mécanismes de sécurisation et limitations {#exit-criteria-guardrails}

Les mécanismes de sécurisation et limitations suivants s’appliquent à la fonctionnalité de critère de sortie de parcours :

* Les critères de sortie sont définis en état de brouillon uniquement.
* Cohérence de l’espace de noms de parcours entre les événements et les critères de sortie basés sur un événement

## Gestion des conflits {#conflict}

La section **[!UICONTROL Gestion des conflits]** dans les propriétés du parcours vous permet de surveiller les conflits et de gérer la priorité de vos parcours. Vous pouvez effectuer les actions suivantes :

* Appliquez un **jeu de règles** pour exclure ce parcours pour une partie de votre audience en fonction de règles de capping de fréquence. [Découvrir comment utiliser les jeux de règles](../configuration/rule-sets.md)

* Attribuez un **score de priorité** au parcours, allant de 0 à 100. Un nombre plus élevé indique une priorité plus élevée. La valeur de priorité insérée ici est héritée par toute action entrante (in-app, par exemple) contenue dans ce parcours. [Découvrir comment utiliser les scores de priorité](../conflict-prioritization/priority-scores.md)

  Dans les cas où cette même configuration de canal entrant est utilisée dans d’autres campagnes ou parcours, l’action entrante ayant le score de priorité le plus élevé est présentée aux destinataires. Si plusieurs parcours ou campagnes ont le même score, l’élément qui a été modifié le plus récemment est sélectionné.

* **Affichez les conflits** avec d’autres configuration de parcours, de campagnes, ou de canaux. Si vous souhaitez identifier un chevauchement concernant l’audience, la date de début et de fin, la configuration des canaux, le canal ou le jeu de règles, vous pouvez afficher les conflits potentiels ici. [Découvrir comment identifier les conflits potentiels dans un parcours](../conflict-prioritization/conflicts.md)
