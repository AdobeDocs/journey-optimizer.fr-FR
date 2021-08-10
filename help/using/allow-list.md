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
ht-degree: 86%

---

# Liste autorisée {#allow-list}

Il est maintenant possible de définir une liste d&#39;envoi sécurisé spécifique au niveau de l&#39;[environnement Sandbox](administration/sandboxes.md), afin d&#39;avoir un environnement sécurisé à des fins de test. Sur une instance hors production, où des erreurs peuvent se produire, la liste autorisée garantit que vous n&#39;avez aucun risque d&#39;envoyer des messages indésirables à vos clients.

La liste autorisée vous permet de spécifier des adresses e-mail ou des domaines individuels qui seront les seuls destinataires ou domaines autorisés à recevoir les e-mails que vous envoyez à partir d&#39;un environnement Sandbox spécifique. Cela peut vous empêcher d&#39;envoyer accidentellement des e-mails à des adresses client réelles lorsque vous vous trouvez dans un environnement de test.

>[!CAUTION]
>
>Cette fonctionnalité **n&#39;est pas** disponible sur les environnements Sandbox de production. Il s’applique uniquement au canal email.

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
>Lorsqu&#39;elle est activée, la fonctionnalité de liste autorisée est respectée lors de l&#39;exécution des parcours, mais également lors du test des messages avec des [bons à tirer](preview.md#send-proofs) et du test des parcours à l&#39;aide du [mode test](building-journeys/testing-the-journey.md).

## Ajout d&#39;entités à la liste autorisée {#add-entities}

Pour ajouter de nouvelles adresses e-mail ou de nouveaux domaines à la liste autorisée pour un environnement Sandbox spécifique, vous devez appeler l&#39;API de suppression avec la valeur `ALLOWED` pour l&#39;attribut `listType`. Par exemple :

![](assets/allow-list-api.png)

Vous pouvez effectuer les opérations **Ajouter**, **Supprimer** et **Obtenir**.

>[!NOTE]
>
>La liste autorisée peut contenir jusqu&#39;à 1 000 entrées.

<!--Learn more on making Adobe API calls in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## Logique de liste autorisée {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Lorsque la liste autorisée est **vide**, la logique de liste autorisée n&#39;est pas appliquée. Cela signifie que vous pouvez envoyer des e-mails à n&#39;importe quel profil, à condition qu&#39;il ne figure pas dans la [liste de suppression](suppression-list.md).

Lorsque la liste autorisée n&#39;est **pas vide**, la logique de liste autorisée est appliquée :

* Si une entité n&#39;est **pas sur la liste autorisée** et la liste de suppression, le destinataire correspondant ne recevra pas l&#39;e-mail, la raison étant **[!UICONTROL Non autorisé]**.

* Si une entité est **sur la liste autorisée** et pas sur la liste de suppression, l&#39;e-mail peut être envoyé au destinataire correspondant. Cependant, si l&#39;entité figure également dans la [liste de suppression](suppression-list.md), le destinataire correspondant ne recevra pas l&#39;e-mail, la raison étant **[!UICONTROL Supprimé]**.




