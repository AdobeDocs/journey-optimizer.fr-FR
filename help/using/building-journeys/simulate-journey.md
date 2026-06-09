---
solution: Journey Optimizer
product: journey optimizer
title: Simuler votre parcours
description: Découvrez comment simuler votre parcours
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: test, parcours, vérification, erreur, dépannage
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: e2e8634a0c897b0b0339b410b3fef0e358095a1e
workflow-type: tm+mt
source-wordcount: 1891
ht-degree: 1%

---

# Simuler votre parcours {#simulate-journey}

>[!IMPORTANT]
>
>Vous avez besoin d’au moins de l’une des autorisations suivantes pour accéder à la fonction **[!UICONTROL Simulation]** : **Simuler des parcours**, **Publier des parcours** ou **Approuver et publier des parcours**. [En savoir plus](../administration/permissions.md)
>
>Pour utiliser l’IA dans **[!UICONTROL Simulation]** (**[!UICONTROL Simulation rapide]**, génération d’utilisateurs simulés avec l’IA **[!UICONTROL Générer des valeurs d’événement]**), les utilisateurs doivent disposer de l’autorisation **[!UICONTROL Générer le contenu]** de la fonctionnalité **[!UICONTROL Assistant IA]**.

Utilisez **[!UICONTROL Simulation]** pour valider votre parcours avec des **utilisateurs simulés** avant de procéder à la publication. Cette page vous guide tout au long des étapes **[!UICONTROL Simulation rapide]** et **[!UICONTROL Simulation manuelle]**, de la création et de l’envoi d’utilisateurs simulés, du déclenchement d’événements unitaires lorsque votre parcours en a besoin, ainsi que de la révision du journal **[!UICONTROL Résultats]**.

Pour obtenir un aperçu par type de parcours, voir [Prise en main de la simulation de Parcours ](simulate-journey-gs.md).

## Types de simulation {#simulation-types}

Après l’activation, les parcours par lots avec entrée d’audience lue offrent deux manières d’exécuter une simulation :

* La **[!UICONTROL simulation rapide]** s’exécute de bout en bout avec les utilisateurs et utilisatrices générés, les valeurs d’événement générées et les paramètres de test par défaut, optimisés par Journey Agent. Il s’agit d’une méthode rapide pour simuler un parcours bout en bout avec une intervention minimale. La simulation rapide démarre dès que vous sélectionnez cette option.

* **[!UICONTROL Simulation manuelle]** permet d’exécuter une simulation pas à pas, manuellement. Créez des utilisateurs simulés (manuellement ou avec le Journey Agent), déclenchez-les dans le parcours, définissez des payloads d’événement (manuellement ou avec le Journey Agent) et remplacez les attentes.

![Panneau Paramètres de simulation avec les options Simulation rapide et Simulation manuelle en regard de la zone de travail du parcours ](assets/quick-simulation-1.png)

### Simulation rapide {#quick-simulation}

Sur n’importe quel parcours de **[!UICONTROL Simulation]**, **[!UICONTROL Simulation rapide]** exécute le parcours avec les utilisateurs et utilisatrices générés, les valeurs d’événement et les paramètres préremplis.

1. Sélectionnez **[!UICONTROL Simulation rapide]**.

1. Examinez les champs que Adobe Journey Optimizer a collectés pour l’exécution. Cliquez sur **[!UICONTROL Mettre à jour les valeurs]** pour modifier les paramètres de test et les adresses d’exécution, ou continuez sans apporter de modifications.

   Cette étape n’apparaît que si le parcours utilise des attentes ou des canaux. Vous pouvez ajuster toutes les durées d’attente et les adresses d’exécution pour les utilisateurs simulés, par exemple utiliser votre propre e-mail afin que les messages de l’exécution soient envoyés à votre boîte de réception.

   ![Boîte de dialogue Simulation rapide à l’étape Collecte d’informations avec Mettre à jour les valeurs et Passer à l’étape suivante](assets/quick-simulation-2.png)

1. Si vous avez ouvert **[!UICONTROL Mettre à jour les valeurs]**, modifiez les paramètres, par exemple l’adresse utilisée pour les BAT des messages, puis confirmez pour démarrer la simulation.

   ![Étape de mise à jour de la simulation rapide des valeurs avec remplacement du temps d’attente et champs d’e-mail et de téléphone du BAT](assets/quick-simulation-3.png)

1. Le Journey Agent génère un ensemble d’utilisateurs simulés à partir de la définition du parcours.

   Pour les parcours dotés d’un nœud E-mail, SMS ou Push, l’agent vous invite à confirmer l’adresse e-mail, le numéro de téléphone ou le jeton push à utiliser. Les utilisateurs simulés sont générés à l’aide de ces valeurs. Une fois que vous avez terminé, cliquez sur **[!UICONTROL Générer]**.

1. Une fois l’exécution terminée, cliquez sur **[!UICONTROL Afficher les résultats]** pour consulter les chemins d’accès, les erreurs et les branches découvertes. Voir [Afficher les résultats](#viewing-results).

   ![La simulation rapide s’est terminée avec toutes les étapes réussies et Afficher les résultats disponibles](assets/quick-simulation-4.png)

La simulation rapide prend également en charge les parcours déclenchés par un événement et les parcours qui incluent des activités d’événement. Les valeurs d’événement sont définies et déclenchées automatiquement pour chaque utilisateur simulé généré. Une fois qu’un utilisateur entre dans le parcours, chaque événement est déclenché dès qu’il atteint l’Attente correspondante.

### Simulation manuelle {#manual-simulation}

Choisissez **[!UICONTROL Simulation manuelle]** lorsque vous devez sélectionner chaque utilisateur simulé, contrôler l’ordre d’envoi, configurer les payloads de l’événement et remplacer les durées **[!UICONTROL d’attente]** de l’exécution.

Continuez avec [Créer et gérer des utilisateurs simulés](#test-users), [Déclencher vos événements](#firing-events) et [Afficher les résultats](#viewing-results).

## Création et gestion d’utilisateurs simulés {#test-users}

>[!IMPORTANT]
>
>Vous avez besoin d’au moins de l’une des autorisations suivantes pour accéder à la fonction **[!UICONTROL Simulation]** : **Simuler des parcours**, **Publier des parcours** ou **Approuver et publier des parcours**. [En savoir plus](../administration/permissions.md)
>
>Pour utiliser l’IA dans **[!UICONTROL Simulation]** (**[!UICONTROL Simulation rapide]**, génération d’utilisateurs simulés avec l’IA **[!UICONTROL Générer des valeurs d’événement]**), les utilisateurs doivent disposer de l’autorisation **[!UICONTROL Générer le contenu]** de la fonctionnalité **[!UICONTROL Assistant IA]**.

Les utilisateurs simulés sont des entités temporaires de type profil que vous définissez dans **[!UICONTROL Paramètres de simulation]**. Cette section explique comment les créer, les enregistrer pour les réutiliser, les ajuster ou les supprimer de la liste et les envoyer dans le parcours.

1. Commencez par remplir la liste **[!UICONTROL Tester les utilisateurs]** :

   +++ Générer des utilisateurs à l’aide de l’IA

   Adobe Journey Optimizer génère un ensemble d’utilisateurs simulés à partir de la définition du parcours.

   Pour les parcours disposant d’un nœud E-mail, Push ou SMS, l’IA vous invite à confirmer l’adresse e-mail ou le numéro de téléphone à utiliser. Les utilisateurs simulés seront générés à l’aide de ces valeurs définies. Une fois que vous avez terminé, cliquez sur **[!UICONTROL Générer]**.

   ![ Boîte de dialogue Générer des utilisateurs simulés avec les champs d’e-mail et de téléphone d’exécution et bouton Générer ](assets/simulate-generate.png)

   +++

   +++ Parcourir l’inventaire

   Choisissez **[!UICONTROL Parcourir l’inventaire]** pour ajouter des utilisateurs simulés que vous avez déjà enregistrés, par exemple, les utilisateurs que vous avez créés à partir d’un formulaire ou d’un fichier JSON, ou les utilisateurs que vous avez conservés après une exécution de génération d’IA.

   ![ Boîte de dialogue d’inventaire des utilisateurs simulés avec recherche, tableau des utilisateurs et bouton Sélectionner ](assets/simulate-inventory.png)

   +++

   +++ Créer à partir d’un formulaire

   1. Saisissez un **[!UICONTROL Nom d’affichage]**, **[!UICONTROL Espace de noms d’identité]** et **[!UICONTROL Description]** pour identifier cet utilisateur simulé.

      ![Créez un formulaire Utilisateurs simulés avec le nom d’affichage, l’espace de noms d’identité, la description et les attributs de schéma d’union](assets/simulate-form.png)

   1. Sélectionnez ensuite les attributs du schéma d’union à renseigner pour cet utilisateur.

   1. Cliquez sur **[!UICONTROL Ajouter une appartenance à une audience]** pour simuler les appartenances à un segment.

   1. Dans la fenêtre **[!UICONTROL Créer des utilisateurs simulés]**, cliquez sur **[!UICONTROL Ajouter un utilisateur simulé]** pour définir plusieurs utilisateurs simulés dans une seule session.

      Vous pouvez modifier le mode d’affichage des utilisateurs dans la liste, réduire chaque carte en mode empilé ou ouvrir les métadonnées d’attribut d’un utilisateur.

      ![Créer un pied de page Utilisateurs simulés avec les contrôles d’affichage Ajouter un utilisateur simulé, Tout réduire et Disposition](assets/simulate-form-3.png)

   1. Dans le menu Utilisateur simulé, utilisez **[!UICONTROL Dupliquer]** pour copier un utilisateur, **[!UICONTROL Appliquer tous les attributs aux autres utilisateurs]** pour copier les attributs d’un utilisateur vers tous les autres utilisateurs de la session ou **[!UICONTROL Supprimer]** pour supprimer un utilisateur.

      ![Création de cartes Utilisateurs simulés avec doublon, Application de tous les attributs aux autres utilisateurs et Suppression sur chaque utilisateur](assets/simulate-form-2.png)

   1. Cliquez sur **[!UICONTROL Enregistrer]** lorsque vous avez terminé de configurer les utilisateurs de cette session.

   +++

   +++ Créer à partir de JSON

   Définissez de nouveaux utilisateurs simulés en mettant à jour les champs correspondants avec vos données utilisateur simulées.

   ![Créer un éditeur JSON d’utilisateurs simulés avec le modèle d’utilisateurs et le contrôle JSON de format](assets/simulate-json.png)

   +++

1. Les utilisateurs simulés que vous avez créés apparaissent dans la liste **[!UICONTROL Tester les utilisateurs]**. Pour chaque entrée, sélectionnez l’une des options suivantes :

   * ![Icône Modifier](assets/do-not-localize/Smock_Edit_18_N.svg) : mettez à jour les détails de l’utilisateur simulé.
   * ![Icône Envoyer](assets/do-not-localize/Smock_Send_18_N.svg) : exécutez la simulation pour cet utilisateur simulé uniquement.

     Cette option n’est pas disponible pour les parcours commençant par un événement , car l’entrée utilisateur simulée est déclenchée par l’événement envoyé. [En savoir plus](#firing-events)

   * ![Icône Effacer](assets/do-not-localize/Smock_Close_18_N.svg) : supprimez l’utilisateur de cette liste. L’utilisateur simulé n’est pas supprimé et reste disponible dans la sélection Utilisateurs simulés .

   ![Tester la liste des utilisateurs avec les actions de modification, d’envoi et de suppression et le chemin simulé mis en surbrillance sur la zone de travail](assets/simulate-4-2.png)

1. Pour modifier la liste après votre sélection, cliquez sur **[!UICONTROL Gérer les utilisateurs]** pour ajouter d’autres utilisateurs simulés, à partir de l’inventaire ou en créant de nouveaux. Pour supprimer chaque utilisateur de la liste **[!UICONTROL Tester les utilisateurs]** pour cette exécution, choisissez **[!UICONTROL Effacer tous les utilisateurs]**.

   ![Le menu Gérer les utilisateurs s’ouvre avec les options d’ajout d’utilisateurs et Effacer tous les utilisateurs](assets/simulate-manage.png)

1. Si votre parcours comprend une activité **[!UICONTROL Attente]**, ouvrez l’onglet **[!UICONTROL Paramètres de test]** pour définir précisément la durée de cette attente pendant la simulation. Par exemple, si l’activité active **[!UICONTROL Attente]** est configurée pendant plusieurs jours, vous pouvez la remplacer par 10 secondes afin que l’utilisateur simulé ne passe que cette durée sur le nœud avant de passer à l’activité suivante.

1. Cliquez sur **[!UICONTROL Envoyer tout]** pour envoyer chaque utilisateur simulé dans la liste du parcours, ou cliquez sur ![Icône Envoyer](assets/do-not-localize/Smock_Send_18_N.svg) sur une ligne pour envoyer uniquement cet utilisateur. Un message de confirmation `Simulated users have entered the journey successfully.` s’affiche lorsque les utilisateurs simulés rejoignent le parcours avec succès.

   ![Onglet Tester les utilisateurs une fois qu’ils ont accédé au parcours avec le message de réussite et le chemin sur la zone de travail](assets/simulate-5-2.png)

1. Si le parcours comprend des événements unitaires, vous devez sélectionner l’événement à déclencher. Voir [ Déclencher vos événements](#firing-events).

1. Accédez à l’onglet **[!UICONTROL Résultats]** pour ouvrir le journal d’exécution et consulter l’exécution de chaque étape. Pour plus d’informations, voir [Affichage des résultats](#viewing-results).

1. Une fois les tests terminés, ouvrez le menu **[!UICONTROL Gérer la simulation]** :

   * **[!UICONTROL Fermez la simulation]** pour quitter la session de simulation en cours.
   * **[!UICONTROL Réinitialiser la simulation]** pour effacer toutes les données de l’exécution en cours, les utilisateurs simulés sélectionnés, les valeurs d’événement définies et d’autres paramètres de test, afin que vous puissiez démarrer une nouvelle simulation à partir de zéro.

     ![Le menu Gérer la simulation s’ouvre avec les options Réinitialiser la simulation et Fermer la simulation](assets/simulate-15.png)

Après avoir validé le parcours dans **[!UICONTROL Simulation]**, consultez le journal **[!UICONTROL Résultats]**. Si des erreurs s’affichent, laissez **[!UICONTROL Simulation]**, apportez les modifications requises au parcours et exécutez à nouveau **[!UICONTROL Simulation]** jusqu’à ce que l’exécution semble correcte. Vous pouvez ensuite publier le parcours. Voir [Publier votre parcours ](../building-journeys/publish-journey.md).

## Déclencher vos événements {#firing-events}

Si votre parcours comprend un ou plusieurs événements unitaires, vous pouvez les déclencher lorsque la Simulation est active. Pour les parcours ne commençant pas par un événement mais en contenant un, cette section ne sera pas visible tant qu’un utilisateur simulé n’aura pas accédé au parcours.

1. Dans **[!UICONTROL Sélectionner le type d’événement]**, sélectionnez l’événement à déclencher pour cette simulation.

   ![Le menu déroulant Sélectionner le type d’événement s’ouvre dans la section Tester les événements des paramètres Simulation](assets/simulate-10-2.png)

1. Pour appliquer la même modification à chaque utilisateur de la liste, utilisez l’option **[!UICONTROL Gérer les événements]** pour :

   * **[!UICONTROL Générer des valeurs d’événement]** pour permettre au Journey Agent de générer toutes les payloads à l’aide de l’IA. Lorsque des valeurs sont générées, l’utilisateur est marqué **[!UICONTROL Prêt à envoyer]**.
   * **[!UICONTROL Modifier les données d’événement]** pour modifier la payload de chaque utilisateur simulé dans la liste.

   ![Menu Gérer les événements dans Événements de test avec les options Générer avec l’IA et Modifier toutes les options](assets/simulate-9-2.png)

1. Configurez la payload d’événement pour chaque utilisateur en cliquant sur l’![Modifier l’événement](assets/do-not-localize/Smock_Edit_18_N.svg) en regard d’un utilisateur pour :

   * **[!UICONTROL Générez des valeurs d’événement]** pour permettre au Journey Agent de générer la payload à l’aide de l’IA. Lorsque des valeurs sont générées, l’utilisateur est marqué **[!UICONTROL Prêt à envoyer]**.
   * **[!UICONTROL Modifiez les données d’événement]** afin de modifier la payload pour cet utilisateur simulé uniquement.

   ![Menu par utilisateur dans Événements de test avec les options Générer des valeurs d’événement et Modifier les données d’événement ](assets/simulate-8-2.png)

1. Dans **[!UICONTROL Événements de test]**, sélectionnez **[!UICONTROL Envoyer tout]** pour envoyer cet événement à tous les utilisateurs simulés répertoriés sous **[!UICONTROL Utilisateurs de test]** ou sélectionnez ![Icône Envoyer](assets/do-not-localize/Smock_Send_18_N.svg) pour qu’un seul événement soit déclenché pour cet utilisateur uniquement.

   ![Section des événements de test avec les commandes Envoyer tout et Envoyer par utilisateur pour les utilisateurs marqués comme Prêt](assets/simulate-11-2.png)

1. Une fois les événements déclenchés, la zone de travail se met à jour pour refléter la progression de chaque utilisateur.

1. Accédez à l’onglet **[!UICONTROL Résultats]** pour ouvrir le journal d’exécution et consulter l’exécution de chaque étape. Pour plus d’informations, voir [Affichage des résultats](#viewing-results).

1. Une fois les tests terminés, ouvrez le menu **[!UICONTROL Gérer la simulation]** :

   * **[!UICONTROL Fermez la simulation]** pour quitter la session de simulation en cours.
   * **[!UICONTROL Réinitialiser la simulation]** pour effacer toutes les données de l’exécution en cours, les utilisateurs simulés sélectionnés, les valeurs d’événement définies et d’autres paramètres de test, afin que vous puissiez démarrer une nouvelle simulation à partir de zéro.

     ![Le menu Gérer la simulation s’ouvre avec les options Réinitialiser la simulation et Fermer la simulation](assets/simulate-15.png)

## Affichage des résultats {#viewing-results}

L’onglet **[!UICONTROL Résultats]** vous permet d’afficher les résultats du test. Dans le menu déroulant **[!UICONTROL Tester l’utilisateur]**, sélectionnez l’utilisateur simulé dont vous souhaitez contrôler l’exécution.

Sélectionnez **[!UICONTROL Tous]** pour afficher les résultats agrégés pour chaque utilisateur simulé dans l’exécution. Cette vue vous permet d’analyser la simulation complète en un coup d’œil, y compris les activités, les résultats et les erreurs, sans devoir sélectionner un seul utilisateur simulé au préalable.

![Onglet Résultats avec résumé de la simulation, filtre de l’utilisateur du test et couverture du chemin d’accès sur la zone de travail du parcours ](assets/simulate-6-2.png)

Pour chaque activité, le journal peut indiquer si l’utilisateur simulé est entré ou sorti de l’étape, ainsi que les erreurs survenues pendant la simulation.

Pour les activités **Attente**, le journal comprend deux valeurs liées à la durée :

* **Durée définie** : durée spécifiée sur l&#39;activité **Attente** pour le parcours publié et appliquée une fois le parcours actif. Le journal enregistre si la simulation applique un remplacement à partir des paramètres de test, par exemple 10 secondes, plutôt que de se fier uniquement à la valeur définie sur le parcours.
* **Durée réelle** : temps écoulé pendant lequel l’utilisateur simulé est resté sur l’activité **Attente**. Cette valeur est définie à partir de l’onglet **[!UICONTROL Paramètres de test]**.

Lorsque des erreurs apparaissent dans le journal, laissez **Simulation**, apportez les modifications requises au parcours et exécutez à nouveau **Simulation**. Une fois la validation réussie, publiez le parcours. Voir [Publier votre parcours ](../building-journeys/publish-journey.md).
