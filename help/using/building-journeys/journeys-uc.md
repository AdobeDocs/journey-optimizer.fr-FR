---
solution: Journey Optimizer
product: journey optimizer
title: Cas d'utilisation de parcours
description: Cas d'utilisation de parcours
feature: Journeys, Use Cases, Email, Push
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: cas d’utilisation, multicanal, messages, parcours, canal, événements, notification push
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/o4-7bKdQzB3Yyz22khT4RHNpNvKL0sCg8YPPnaeav9I
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: e57d1da4-32c2-4cc6-945c-9feb219156ff
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 1060
ht-degree: 73%

---

# Envoyer des messages multicanaux {#send-multi-channel-messages}

Cette section présente un cas d’utilisation qui combine une lecture d’audience, un événement, des événements de réaction et des e-mails/messages push.

![Flux de parcours simple avec les activités Lecture d’audience, Attente et E-mail](assets/jo-uc1.png)

## Description du cas d’utilisation

Dans ce cas d’utilisation, l’objectif est d’envoyer un premier e-mail à l’ensemble des clientes et clients appartenant à une audience spécifique.

En fonction de leur réaction au premier message, des messages spécifiques de suivi sont envoyés.

Si le client ou la cliente ouvre l’e-mail, le système attend un achat et envoie une notification push pour le ou la remercier.

En l’absence de réaction, un e-mail de relance est envoyé.

## Conditions préalables

Pour que ce cas d’utilisation fonctionne, vous devez configurer les éléments suivants :

* Une audience pour la clientèle qui réside à Atlanta, à San Francisco ou à Seattle et qui est née après 1980.
* Un événement d’achat.

### Créer l’audience

Dans ce parcours, une audience spécifique de clientes et de clients est utilisée. Toutes les personnes appartenant à l’audience rejoignent le parcours et suivent les différentes étapes. Dans cet exemple, l’audience cible la clientèle qui réside à Atlanta, à San Francisco ou à Seattle et qui est née après 1980.

Pour plus d’informations sur les audiences, [consultez cette page](../audience/about-audiences.md).

1. Dans la section du menu CLIENT OU CLIENTE, sélectionnez **[!UICONTROL Audiences]**.
1. Cliquez sur le bouton **[!UICONTROL Créer une audience]** situé en haut à droite de la liste des audiences.
1. Dans le volet **[!UICONTROL Propriétés de l’audience]**, saisissez le nom de l’audience.
1. Effectuez un glisser-déposer des champs de votre choix à partir du volet de gauche vers l’espace de travail central, puis configurez-les en fonction de vos besoins. Dans cet exemple, utilisez les champs d’attributs **Ville** et **Année de naissance**.
1. Cliquez sur **[!UICONTROL Enregistrer]**.

   ![Panneau Attributs supplémentaires pour la sélection des données d’enrichissement](assets/add-attributes.png)

L’audience est maintenant créée et prête à être utilisée dans votre parcours. Avec l’activité **Lecture d’audience**, toutes les personnes appartenant à l’audience peuvent rejoindre le parcours.

### Configurer l’événement

Configurez un événement qui est envoyé au parcours lorsqu’un client ou une cliente effectue un achat. Lorsque le parcours reçoit l’événement, il déclenche le message de remerciement.

Pour cela, utilisez un [événement basé sur des règles](../event/about-events.md).

1. Dans la section du menu ADMINISTRATION, sélectionnez **[!UICONTROL Configurations]**, puis cliquez sur **[!UICONTROL Événements]**. Cliquez sur **[!UICONTROL Créer un événement]** pour créer un événement.

1. Saisissez le nom de l’événement.

1. Dans le champ **[!UICONTROL Type d&#39;identifiant d&#39;événement]**, sélectionnez **[!UICONTROL Basé sur des règles]**.

1. Définissez les champs **[!UICONTROL Schéma]** et **[!UICONTROL Payload]**. Utilisez plusieurs champs, par exemple, le produit acheté, la date d’achat et l’identifiant d’achat.

1. Dans le champ **[!UICONTROL Condition d’identifiant d’événement]**, définissez la condition utilisée par le système pour identifier les événements qui déclenchent le parcours. Par exemple, ajoutez un champ `purchaseMessage` et définissez la règle suivante : `purchaseMessage="thank you"`

1. Définissez l&#39;**[!UICONTROL espace de noms]** et l&#39;**[!UICONTROL identifiant du profil]**.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

   ![Parcours avec activité Condition ramifiée entre Membres Gold et les autres chemins](assets/jo-uc2.png)

L’événement est maintenant configuré et prêt à être utilisé dans votre parcours. À l’aide de l’activité d’événement correspondante, une action peut être déclenchée à chaque fois qu’un client ou une cliente effectue un achat.

## Concevoir le parcours

1. Débutez le parcours avec une activité **Lecture d’audience**. Sélectionnez l’audience que vous venez de créer. Toutes les personnes appartenant à l’audience rejoignent le parcours.

   ![Vérification des conditions météorologiques pour savoir si la température est inférieure à 50 degrés](assets/jo-uc4.png)

1. Déposez une activité d’action **E-mail** et définissez le contenu du « premier message ». Ce message est envoyé à tous individus dans le parcours. Consultez cette [section](../email/create-email.md) pour savoir comment configurer et concevoir un e-mail.

   ![Parcours complet basé sur les conditions météorologiques avec conditions de température et actions par e-mail](assets/jo-uc5.png)

1. Ajoutez un événement **Réaction** et sélectionnez **E-mail ouvert**. L’événement est déclenché lorsqu’une personne appartenant à l’audience ouvre l’e-mail.

1. Cochez la case **Définir la temporisation de l’événement**, définissez une durée (1 jour dans notre exemple) et cochez **Définir un chemin de temporisation**. Cela crée un autre chemin pour les personnes qui n’ouvrent pas le premier message par notification push ou par e-mail.

1. Dans le chemin de temporisation, déposez une activité d’action **E-mail** et définissez le contenu du message de « relance ». Ce message est envoyé aux personnes qui n’ouvrent pas le premier e-mail ou la première notification push dans les 24 heures. [Découvrez comment configurer et concevoir un e-mail](../email/create-email.md).

1. Dans le premier chemin, ajoutez l’événement d’achat créé précédemment. L&#39;événement est déclenché lorsqu&#39;un individu effectue un achat.

1. Après l’événement, déposez une activité d’action **Push** et définissez le contenu du message « merci ». Consultez cette section [section](../push/create-push.md) pour savoir comment configurer et concevoir une notification push.

## Tester et publier le parcours

1. Avant de tester votre parcours, vérifiez qu’il est valide et qu’il ne comporte aucune erreur.

1. Cliquez sur le bouton **Test** situé dans le coin supérieur droit pour activer le mode test. Reportez-vous à cette [section](testing-the-journey.md) pour savoir comment utiliser le mode test.

1. Lorsque le parcours est prêt, publiez-le à l&#39;aide du bouton **Publier** situé dans le coin supérieur droit.

## Parcours de fidélité multiphase {#multi-phase-loyalty}

Cet exemple illustre un modèle d’architecture de parcours clé : décomposition d’un parcours complexe et multiphase en sous-parcours plus petits et ciblés liés à l’activité [**[!UICONTROL Saut]**](jump.md). Un programme de fidélité fait office de scénario, mais ce modèle s’applique à tout parcours qui s’étend sur plusieurs jalons ou phases d’entreprise.

Les parcours multiphases complexes génèrent rapidement un grand nombre de chemins d’accès clients uniques. En les décomposant en un sous-parcours par phase, chaque parcours reste gérable, testable et gérable indépendamment.

### Scénario

Prenons l’exemple d’un programme de fidélité qui guide les clients à travers trois jalons à l’aide de deux canaux marketing ([e-mail](../email/create-email.md) et [push](../push/create-push.md)) :

1. **Phase 1 — Télécharger l’application mobile :** les communications initiales encouragent les nouveaux membres du programme de fidélité à télécharger l’application. Un rappel est envoyé si le client n&#39;a pas agi dans un délai défini.
1. **Phase 2 — Effectuer une première transaction :** une fois l’application téléchargée, les messages ciblés guident les clients vers la réalisation de leur première transaction de fidélité.
1. **Phase 3 - Effectuer une seconde transaction :** après la première transaction, un ensemble final de communications entraîne une seconde transaction pour approfondir l’engagement de fidélité.

Même avec cette stratégie simple, ce parcours expose plus de 20 chemins uniques qu’un client peut emprunter. La complexité augmente de manière exponentielle avec chaque point de contact ou canal supplémentaire.

### Décomposition du sous-parcours

Divisez le parcours de bout en bout en trois sous-parcours plus petits et connectés :

| Sous-parcours | Condition d’entrée | Objectif professionnel |
|---|---|---|
| Phase 1 - Téléchargement de l’application | Le client rejoint le programme de fidélité | Lancer le téléchargement des applications mobiles |
| Phase 2 — Première transaction | Le client télécharge l’application | Lancer la première transaction de fidélité |
| Phase 3 — Deuxième opération | Le client effectue la première transaction | Lancer la deuxième transaction de fidélité |

Connectez les sous-parcours à l’aide de l’activité [**[!UICONTROL Saut]**](jump.md) afin que les profils passent facilement d’une phase à l’autre. Chaque sous-parcours reste simple, lisible et gérable indépendamment.

<!--
>[!NOTE]
>
>If your goal is to build a gamified loyalty program with challenges, tasks, and built-in reward tracking, Journey Optimizer also offers a dedicated **Loyalty Challenges** capability.
-->

