---
title: Liste autorisée
description: Découvrez comment utiliser la liste autorisée.
feature: Délivrabilité
topic: Gestion de contenu
role: User
level: Intermediate
source-git-commit: e2743c8fa624a7a95b12c3adb5dc17a1b632c25d
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---

# Liste autorisée {#allow-list}

Il est désormais possible de définir une liste de sécurité d’envoi spécifique au niveau [sandbox](administration/sandboxes.md), afin d’avoir un environnement sécurisé à des fins de test. Sur une instance hors production, où des erreurs peuvent se produire, la liste autorisée vous garantit que vous n’avez aucun risque d’envoyer des messages indésirables à vos clients.

La liste autorisée vous permet de spécifier des adresses électroniques ou des domaines individuels qui seront les seuls destinataires ou domaines autorisés à recevoir les courriers électroniques que vous envoyez à partir d’un environnement de test spécifique. Cela peut vous empêcher d’envoyer accidentellement des emails à de réelles adresses client lorsque vous vous trouvez dans un environnement de test.

>[!CAUTION]
>
>Cette fonctionnalité n’est **pas** disponible sur les environnements de test de production. Il s’applique uniquement au canal email.

## Activation de la liste autorisée {#enable-allow-list}

Pour activer cette fonction sur un environnement de test hors production, mettez à jour la liste autorisée afin qu’elle ne soit plus vide. Pour le désactiver, effacez la liste autorisée afin qu’elle soit à nouveau vide.

Pour en savoir plus sur la logique de liste autorisée, consultez [cette section](#logic).

<!--
To enable the allowed list on a non-production sandbox, you need to make an Adobe API call.

* Using this API, you can also disable the feature at any time.

* You can update the allowed list before or after enabling the feature.

* The allowed list logic applies when the feature is enabled and if the allowed list is not empty. Learn more in this section (logic).
-->

>[!NOTE]
>
>Lorsqu’elle est activée, la fonction de liste autorisée est respectée lors de l’exécution des parcours, mais également lors du test des messages avec [bons à tirer](preview.md#send-proofs) et du test des parcours à l’aide du [mode test](building-journeys/testing-the-journey.md).

## Ajouter des entités à la liste autorisée {#add-entities}

Pour ajouter de nouvelles adresses ou de nouveaux domaines de messagerie à la liste autorisée pour un environnement de test spécifique, vous devez appeler l’API de suppression avec la valeur `ALLOWED` pour l’attribut `listType` . Par exemple :

![](assets/allow-list-api.png)

Vous pouvez effectuer les opérations **Ajouter**, **Supprimer** et **Obtenir**.

>[!NOTE]
>
>La liste autorisée peut contenir jusqu’à 1 000 entrées.

<!--Learn more on making Adobe API calls in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## Logique de liste autorisée {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Lorsque la liste autorisée est **vide**, la logique de liste autorisée n’est pas appliquée. Cela signifie que vous pouvez envoyer des emails à n’importe quel profil, à condition qu’il ne figure pas dans la [liste de suppression](suppression-list.md).

Lorsque la liste autorisée est **non vide**, la logique de liste autorisée est appliquée :

* Si une entité n’est **pas sur la liste autorisée** et non sur la liste de suppression, le destinataire correspondant ne recevra pas l’email, la raison étant **[!UICONTROL Non autorisé]**.

* Si une entité est **sur la liste autorisée** et non sur la liste de suppression, l&#39;email peut être envoyé au destinataire correspondant. Cependant, si l’entité figure également dans la [liste de suppression](suppression-list.md), le destinataire correspondant ne recevra pas l’email, la raison étant **[!UICONTROL Supprimé]**.




