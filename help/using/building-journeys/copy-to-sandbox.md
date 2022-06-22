---
title: Copier un parcours dans un autre sanddox
description: Découvrez comment copier un parcours dans un autre sanddox
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 4d211b9a0087526fe81d7b989195f21ceab42865
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Copier un parcours dans un autre environnement de test {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copier un parcours dans un autre environnement de test"
>abstract="Journey Optimizer vous permet de copier un parcours entier d’un environnement de test à un autre. Par exemple, vous pouvez copier un parcours de l’environnement de test intermédiaire vers votre environnement de test de production. Outre le Parcours lui-même, Journey Optimizer copie également la plupart des objets dont dépend le parcours."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Détails des environnements de test"
>abstract="Sélectionnez l’environnement de test de destination vers lequel vous souhaitez copier le parcours. Seuls les environnements de test de votre organisation IMS sont disponibles."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Détails de l’objet"
>abstract="C&#39;est le parcours que vous allez copier."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Objets dépendants"
>abstract="Il s’agit de la liste des objets associés utilisés dans le parcours. Cette liste affiche le nom, le type d’objet et l’Journey Optimizer ID interne."

Journey Optimizer vous permet de copier un parcours entier d’un environnement de test à un autre. Par exemple, vous pouvez copier un parcours de votre environnement de test dans votre environnement de test de production. Outre le parcours lui-même, Journey Optimizer copie également la plupart des objets dont dépend le parcours : messages, segments, paramètres prédéfinis, schémas, événements et actions. Reportez-vous à la section [limitations](../event/about-events.md)

>[!CAUTION]
>
>Nous ne garantissons pas que tous les éléments liés seront copiés dans l’environnement de test de destination. Nous vous recommandons vivement d’effectuer une vérification approfondie avant de publier le parcours. Vous pourrez ainsi identifier tout objet manquant potentiel.

Les objets copiés dans l’environnement de test cible sont uniques et il n’y a aucun risque de remplacer des éléments existants. Le parcours et tous les messages à l’intérieur du parcours sont transmis en mode préliminaire. Cela vous permet d’effectuer une validation approfondie avant la publication sur l’environnement de test cible. Le processus de copie ne copie que les métadonnées du parcours et des objets de ce Parcours. Aucune donnée de profil ou de jeu de données n’est copiée dans le cadre de ce processus.

Pour copier un parcours dans un autre environnement de test, procédez comme suit :

1. Dans la section du menu GESTION DES PARCOURS, cliquez sur **[!UICONTROL Parcours]**. La liste des parcours s&#39;affiche.

2. Recherchez le parcours à copier, puis cliquez sur le bouton **Autres actions** (les trois points en regard du nom du parcours) et cliquez sur **Copier vers l’environnement de test**.

   ![](assets/copy-sandbox1.png)

   Le **Copier vers l’environnement de test** s’affiche.

   ![](assets/copy-sandbox2.png)

3. Sélectionnez la **Environnement de test Target** dans le champ déroulant. Seuls les environnements de test de votre organisation IMS sont disponibles.

4. Consultez la section **Objets dépendants** . Il s’agit de la liste des objets associés utilisés dans le parcours. Cette liste affiche le nom, le type d’objet et l’Journey Optimizer ID interne.

5. Cliquez sur le bouton **Copier** , dans le coin supérieur droit, pour commencer à copier le parcours dans l’environnement de test cible.

   ![](assets/copy-sandbox3.png)

   Le processus de copie commence et la progression de chaque objet est affichée. Le processus de copie varie en fonction de la complexité du parcours et du nombre d’objets à copier. Si une erreur se produit, un message s’affiche pour l’objet associé.

   ![](assets/copy-sandbox4.png)

6. Une fois la copie terminée, cliquez sur **Fermer**.

7. Accédez à votre environnement de test cible et vérifiez minutieusement tous les objets copiés.

## Copie du processus et des limitations {#limitations}

Nous ne garantissons pas que tous les éléments liés seront copiés dans l’environnement de test de destination. Nous vous recommandons vivement d’effectuer une vérification approfondie. Identifiez tout objet potentiel manquant et créez-le manuellement avant de publier le parcours.

Les objets suivants sont copiés :

* Segment

   Un segment ne peut être copié qu’une seule fois d’un environnement de test à un autre. Les requêtes suivantes pour copier le segment échoueront. Une fois qu’un segment est copié, il n’est pas modifiable sur l’environnement de test de destination.

* Schéma

   Les schémas utilisés dans ce parcours sont copiés.

* Message

   Le ou les messages physiques utilisés dans le parcours (email ou push). Les champs utilisés pour la personnalisation dans le message ne sont pas vérifiés pour être complets. Les blocs de contenu ne sont pas copiés.

* Parcours - détails du canevas

   Représentation du parcours sur la zone de travail, y compris les objets du parcours tels que les conditions, les actions, les événements, les segments de lecture, etc. L’activité Saut est exclue de la copie.

* Événement

   Les événements et les détails de l’événement utilisés dans le parcours sont copiés.

* Action

   Les actions et les détails de l’action utilisés dans le parcours sont copiés.

Les paramètres prédéfinis ne sont pas copiés. Le système sélectionne automatiquement la correspondance la plus proche possible sur l’environnement de test de destination, en fonction du type de message et du nom du paramètre prédéfini. Si aucun paramètre prédéfini n’est trouvé sur l’environnement de test cible, la copie du paramètre prédéfini échoue. Cela signifie que la copie du message échouera également, car un message nécessite qu’un paramètre prédéfini soit disponible pour la configuration. Dans ce cas, au moins un paramètre prédéfini doit être créé, pour le canal approprié du message, afin que la copie fonctionne.

