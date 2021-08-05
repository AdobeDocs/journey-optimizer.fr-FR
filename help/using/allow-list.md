---
title: Liste autorisée
description: Découvrez comment utiliser la liste autorisée.
feature: Délivrabilité
topic: Gestion de contenu
role: User
level: Intermediate
source-git-commit: 288c27d4fc64a6d0a6f07b634ed044a6e858d0c1
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 2%

---

# Liste autorisée {#allow-list}

Il est désormais possible de définir une liste de sécurité d’envoi spécifique au niveau [sandbox](administration/sandboxes.md), afin d’avoir un environnement sécurisé à des fins de test. Sur une instance hors production, où des erreurs peuvent se produire, la liste autorisée vous garantit que vous n’avez aucun risque d’envoyer des messages indésirables à vos clients.

>[!CAUTION]
>
>Cette fonctionnalité n’est pas disponible sur les environnements de test de production.

La liste autorisée vous permet de spécifier des adresses électroniques ou des domaines individuels qui seront les seuls destinataires ou domaines autorisés à recevoir les courriers électroniques que vous envoyez à partir d’un environnement de test spécifique. Cela peut vous empêcher d’envoyer accidentellement des emails à de réelles adresses client lorsque vous vous trouvez dans un environnement de test.

>[!NOTE]
>
>Cette fonctionnalité s’applique uniquement au canal email.

## Activation de la liste autorisée {#enable-allow-list}

Pour activer la liste autorisée sur un environnement de test hors production, vous devez effectuer un appel API d’Adobe.

* Grâce à cette API, vous pouvez également désactiver la fonctionnalité à tout moment.

* Vous pouvez mettre à jour la liste autorisée avant ou après l’activation de la fonction.

* La logique de liste autorisée s’applique lorsque la fonction est activée et si la liste autorisée n’est pas vide. En savoir plus dans [cette section](#logic).

>[!NOTE]
>
>Lorsqu’elle est activée, la fonction de liste autorisée est respectée lors de l’exécution des parcours, mais également lors du test des messages avec [bons à tirer](preview.md#send-proofs) et du test des parcours à l’aide du [mode test](building-journeys/testing-the-journey.md).

## Ajouter des entités à la liste autorisée {#add-entities}

>[!CAUTION]
>
>Cette fonctionnalité n’est **pas** disponible sur les environnements de test de production. Il s’applique uniquement au canal email.

Pour ajouter de nouvelles adresses ou de nouveaux domaines de messagerie à la liste autorisée pour un environnement de test spécifique, vous devez appeler l’API de suppression avec la valeur `ALLOWED` pour l’attribut `listType` . Par exemple :

![](assets/allow-list-api.png)

Vous pouvez effectuer les opérations **Ajouter**, **Supprimer** et **Obtenir**.

>[!NOTE]
>
>La liste autorisée peut contenir jusqu’à 1 000 entrées.

Pour en savoir plus sur l’Adobe d’appels API, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).

## Logique de liste autorisée {#logic}

<!-- When the allowed list is \[enabled\]\(\add link here\) at the sandbox level using the API call above, the following applies.-->

1. Lorsque la liste autorisée est **vide**, la logique de liste autorisée n’est pas appliquée. Cela signifie que vous pouvez envoyer des emails à n’importe quel profil, à condition qu’il ne figure pas dans la [liste de suppression](suppression-list.md).

1. Lorsque la liste autorisée est **non vide**, la logique de liste autorisée est appliquée :

   * Si une entité n’est **pas sur la liste autorisée** et non sur la liste de suppression, le destinataire correspondant ne recevra pas l’email, la raison étant **[!UICONTROL Non autorisé]**.

   * Si une entité est **sur la liste autorisée** et non sur la liste de suppression, l&#39;email peut être envoyé au destinataire correspondant. Cependant, si l’entité figure également dans la [liste de suppression](suppression-list.md), le destinataire correspondant ne recevra pas l’email, la raison étant **[!UICONTROL Supprimé]**.




