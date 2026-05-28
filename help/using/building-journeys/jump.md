---
solution: Journey Optimizer
product: journey optimizer
title: Passage d’un parcours à un autre
description: Passage d’un parcours à un autre
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: saut, activité, parcours, partage, partager
exl-id: 46d8950b-8b02-4160-89b4-1c492533c0e2
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/qCnWzqjO5YRbKO-WHUo950uoHS0skcZT6sdYyNJ4esE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1405
ht-degree: 60%

---

# Sauter d’un parcours à un autre {#jump}

>[!CONTEXTUALHELP]
>id="ajo_journey_jump"
>title="Activité Saut"
>abstract="L’activité d’action Saut permet d’inviter des individus à passer d’un parcours à un autre. Cette fonctionnalité vous permet de simplifier la conception de parcours très complexes et de créer des parcours basés sur des modèles de parcours communs et réutilisables."

L’activité d’action **[!UICONTROL Saut]** permet d’inviter des individus à passer d’un parcours à un autre. Cette fonctionnalité permet d’effectuer les opérations suivantes :

* simplifier la conception de parcours très complexes en les divisant en plusieurs autres ;
* créer des parcours basés sur des schémas de parcours communs et réutilisables.

Dans le parcours d’origine, ajoutez une activité **[!UICONTROL Saut]** et sélectionnez un parcours cible. Lorsque la personne parvient à l’étape de **[!UICONTROL saut]**, un événement interne est envoyé au premier événement du parcours cible. Si l’action **[!UICONTROL Saut]** réussit, la personne continue à progresser dans le parcours. Le comportement est similaire aux autres actions.

Dans le parcours cible, le premier événement déclenché en interne par l’activité **[!UICONTROL Saut]** permet à la personne de s’insérer dans le parcours.

## Cycle de vie {#jump-lifecycle}

Supposons que vous ayez ajouté une activité **[!UICONTROL Saut]** d’un parcours A à un parcours B. Le parcours A est le **parcours d’origine** et le parcours B, le **parcours cible**.

Voici les différentes étapes du processus d’exécution :

Le **parcours A** est déclenché par un événement externe :

1. Le parcours A reçoit un événement externe lié à un individu.
1. L’individu atteint l’étape du **[!UICONTROL saut]**.
1. La personne est amenée au parcours B et passe aux étapes suivantes du parcours A, situées après l’étape **[!UICONTROL Saut]**.

Dans le parcours B, le premier événement est déclenché en interne via l’activité **[!UICONTROL Saut]** à partir du parcours A :

1. Le parcours B reçoit un événement interne du parcours A.
1. La personne commence à effectuer le parcours B.

>[!NOTE]
>
>Le parcours B peut également être déclenché par un événement externe.

### Comportement du profil lors d’un saut {#jump-profile-behavior}

Lorsqu’un profil atteint l’étape **[!UICONTROL Saut]**, il continue à progresser dans le parcours d’origine (Parcours A) tout en accédant simultanément au parcours cible (Parcours B). Le profil est donc actif dans les deux parcours en même temps.

Autrement dit :

* Le profil effectue toutes les étapes restantes dans le Parcours A après l’activité Saut (par exemple, une action d’attente ou de fermeture de relance).
* Le profil commence également à circuler dans le Parcours B à partir de son premier événement, indépendamment du Parcours A.
* Si le profil est **déjà actif** dans le Parcours B lors de l’exécution du Saut, il **ne reviendra pas** dans le Parcours B. Le parcours A continue normalement ; aucune erreur n&#39;est signalée.

>[!NOTE]
>
>Le cas ci-dessus — profil déjà actif dans le Parcours B — se traduit par un **saut silencieux** : aucune erreur n&#39;est générée et le Parcours A se poursuit normalement. Dans d’autres situations, le Saut peut **échouer** et le Parcours A applique sa gestion standard des actions et des erreurs. Voir [Échecs d’exécution](#jump-troubleshoot) pour obtenir la liste complète des cas.

## Bonnes pratiques et limites {#jump-limitations}

Suivez ces instructions pour que le comportement de l’activité Saut reste prévisible et sûr.

### Création {#jump-limitations-authoring}

* L’activité **[!UICONTROL Saut]** n’est disponible que dans les parcours utilisant un espace de noms.
* Vous ne pouvez accéder qu’à un parcours qui utilise le même espace de noms que le parcours d’origine.
* Vous ne pouvez pas accéder à un parcours commençant par un événement **Qualification d’audience** ou **Lecture d’audience**.
* Un même parcours ne peut pas contenir une activité **[!UICONTROL Saut]** et un événement **Qualification d’audience** ou **Lecture d’audience**.
* Vous pouvez inclure autant d’activités **[!UICONTROL Saut]** que nécessaire dans un parcours. Après un **[!UICONTROL saut]**, vous pouvez ajouter toutes les activités nécessaires.
* Vous pouvez avoir autant de niveaux de saut que nécessaire. Par exemple, un saut du parcours A vers le parcours B, puis un saut du parcours B vers le parcours C, etc.
* Le parcours cible peut également comporter autant d’activités **[!UICONTROL Saut]** que nécessaire.
* Les schémas de boucle ne sont pas pris en charge. Il n’est pas possible de relier deux parcours ou plus entre eux, car cela entraînerait une boucle infinie. L’écran de configuration de l’activité **[!UICONTROL Saut]** vous empêche de le faire.

### Exécution {#jump-limitations-exec}

* Lorsque l’activité **[!UICONTROL Saut]** est exécutée, la dernière version du parcours cible est déclenchée.
* Une personne unique ne peut être présente qu’une seule fois dans un même parcours. Ainsi, si une personne provenant d’un parcours d’origine se trouve déjà dans le parcours cible, elle ne rejoindra pas le parcours cible. Aucune erreur ne sera signalée lors de l’activité **[!UICONTROL Saut]**, car il s’agit d’un comportement normal.

## Stratégie de conception : sous-parcours de petite taille {#jump-strategy}

Les parcours clients complexes peuvent rapidement devenir difficiles à créer et à gérer, en particulier lorsque des canaux ou points de contact supplémentaires sont introduits. Même un parcours comportant quelques jalons peut exposer 20 chemins uniques ou plus qu’un client peut emprunter, et cette complexité augmente de manière exponentielle à chaque ajout.

Une approche pratique pour gérer cela consiste à diviser les grands parcours en sous-parcours plus petits et ciblés (un par phase d’entreprise ou jalon) et à les connecter à l’aide de l’activité **[!UICONTROL Saut]**. Cela permet à chaque parcours d’être lisible, testable et gérable indépendamment.

**Étape 1 — Visualiser le parcours de bout en bout**

Cartographiez l’ensemble du parcours client et identifiez ses phases de haut niveau. Par exemple, un parcours d’intégration de la fidélité peut inclure trois phases distinctes : télécharger l’application mobile, effectuer une première transaction, effectuer une seconde transaction.

**Étape 2 — Annoter les phases et définir les sous-parcours**

Délimitez chaque phase et définissez son objectif commercial. Chaque phase devient un sous-parcours candidat avec une condition d&#39;entrée et un objectif clairs.

**Étape 3 — Créer et connecter des sous-parcours**

Créez chaque phase sous la forme d’un parcours distinct dans Journey Optimizer, puis utilisez les activités **[!UICONTROL Saut]** pour transmettre les profils d’un sous-parcours à l’autre. Le résultat est un ensemble de parcours plus simples et réutilisables qui se combinent pour produire une expérience complète de bout en bout, avec moins de risque d’introduire des erreurs.

>[!TIP]
>
>Pour obtenir un exemple pratique d’utilisation d’un programme de fidélité multiphase, consultez parcours de fidélité multiphase[&#128279;](journeys-uc.md#multi-phase-loyalty).

## Configuration de l’activité Saut {#jump-configure}

1. Concevez votre **parcours d’origine**.

   ![Activité Saut dans la palette de parcours pour la transition entre les parcours &#x200B;](assets/jump1.png)

1. À chaque étape du parcours, ajoutez une activité **[!UICONTROL Saut]**, depuis la catégorie **[!UICONTROL ACTIONS]**. Ajoutez un libellé et une description.

   ![Liste déroulante de sélection du parcours cible dans la configuration de l’activité Saut](assets/jump2.png)

1. Cliquez dans le champ **Parcours cible**.
La liste contient toutes les versions de parcours en version brouillon, version active ou en mode test. Les parcours qui utilisent un autre espace de noms ou commençant par un événement **Qualification d’audience** ne sont pas disponibles. Les parcours cible qui créeraient un schéma de boucle sont également filtrés.

   ![Activité Saut présentant le parcours cible et les paramètres d’action](assets/jump3.png)

   >[!NOTE]
   >
   >Vous pouvez cliquer sur l’icône **Ouvrir le parcours cible**, sur le côté droit, pour ouvrir le parcours cible dans un nouvel onglet.

1. Sélectionnez le parcours cible auquel vous souhaitez accéder.
Le champ **Premier événement** est prérenseigné avec le nom du premier événement du parcours cible. Si votre parcours cible comporte plusieurs événements, le **[!UICONTROL saut]** n’est autorisé que pour le premier.

   ![Configuration du mapping des paramètres pour l’activité Saut avec l’éditeur d’expression](assets/jump4.png)

1. La section **Paramètres d’action** affiche tous les champs de l’événement cible. Mappez chaque champ aux champs de l’événement d’origine ou de la source de données, comme pour les autres types d’actions. Ces informations seront transmises au parcours cible au moment de l’exécution.
1. Ajoutez les activités suivantes pour terminer le parcours d’origine.

   ![Interface du mode Test pour tester l’activité Saut entre les parcours &#x200B;](assets/jump5.png)


   >[!NOTE]
   >
   >L’identité de l’individu est automatiquement mappée. Ces informations ne sont pas visibles dans l’interface.

Votre activité **[!UICONTROL Saut]** est configurée. Dès que votre parcours est actif ou en mode de test, les personnes qui atteignent l’étape **[!UICONTROL Saut]** sont amenées au parcours cible.

Lorsqu’une activité **[!UICONTROL Saut]** est configurée dans un parcours, une icône d’entrée **[!UICONTROL Saut]** est automatiquement ajoutée au début du parcours cible. Vous pouvez ainsi identifier que le parcours peut être déclenché depuis l’extérieur mais aussi en interne par le biais d’une activité **[!UICONTROL Saut]**.

![Flux du parcours affichant le saut du parcours source vers le parcours cible](assets/jump7.png)

## Dépannage {#jump-troubleshoot}

### Erreurs de configuration

Les problèmes suivants empêchent le fonctionnement correct du Saut et apparaissent comme des erreurs sur la zone de travail du parcours :

* Le parcours cible n’existe plus.
* Le parcours cible est en version brouillon, fermé ou arrêté.
* Le premier événement du parcours cible a changé et le mapping est rompu.

![Journey Analytics affichant les mesures d’exécution de l’activité Saut](assets/jump6.png)

### Échecs d’exécution

Dans les cas ci-dessous, l’étape Saut est traitée comme une **action en échec** dans le Parcours A. Le Parcours A applique la gestion standard action-erreur et continue :

* L’instance de parcours cible existante a été arrêtée et le parcours cible n’est pas rentrant.
* Une période de reprise est configurée sur le parcours cible. Même lorsque la rentrée est autorisée en principe, le profil ne peut pas rentrer à nouveau avant l’expiration de la période (le Saut échoue avec un statut « non rentrant pour la période »).
* La version du parcours cible est introuvable, a été supprimée, est terminée ou a été arrêtée.
