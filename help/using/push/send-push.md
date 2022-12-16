---
solution: Journey Optimizer
product: journey optimizer
title: Envoyer votre notification push
description: Découvrez comment prévisualiser et tester votre notification push dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 63%

---

# Envoyer votre notification push {#send-push}

## Prévisualiser votre notification push {#preview-push}

Une fois le contenu de votre message défini, vous pouvez utiliser des profils de test pour le prévisualiser et le tester. Si vous avez inséré du contenu personnalisé, vous pourrez vérifier comment ce contenu s’affiche dans le message en exploitant les données du profil de test.

1. Cliquez sur **[!UICONTROL Simulation du contenu]**.

1. Cliquez sur **[!UICONTROL Gestion des profils de test]** pour ajouter un profil de test.

1. Recherchez votre profil de test avec la méthode **[!UICONTROL Espace de noms d’identité]** et **[!UICONTROL Valeur d’identité]** champs. Cliquez ensuite sur **[!UICONTROL Ajouter un profil]**.

   ![](assets/push_preview_1.png)

1. appliquer les mêmes étapes que celles décrites ci-dessus pour sélectionner un profil de test ;

   ![](assets/push_preview_2.png)

1. Dans la prévisualisation push, les données du profil de test sont exploitées dans le contenu du message.

   Sélectionnez le type de périphérique sur lequel prévisualiser le contenu : **[!UICONTROL iOS]** ou **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## Validation de la notification push {#push-validate}

>[!NOTE]
>
> Pour une meilleure délivrabilité, vous devez toujours utiliser les numéros de téléphone dans les formats pris en charge par le fournisseur. Par exemple, Twilio et Sinch ne prennent en charge que les numéros de téléphone au format E.164.

Vous devez également vérifier les alertes dans la section supérieure de l’éditeur.  Certaines d’entre elles sont de simples avertissements, mais d’autres peuvent vous empêcher d’utiliser le message. Deux types d’alertes peuvent avoir lieu :

* Les **avertissements** se rapportent aux recommandations et aux bonnes pratiques.

* **Erreurs** vous empêche de tester ou d’activer le parcours tant qu’il n’est pas résolu, par exemple :

   * **[!UICONTROL La version push du message est vide]** : cette erreur s’affiche lorsque le titre ou le corps de la notification push est manquant. Découvrez comment définir le contenu des notifications push dans [cette section](create-push.md).

   * **[!UICONTROL La surface n&#39;existe pas]**: vous ne pouvez pas utiliser votre message si la surface que vous avez sélectionnée est supprimée après la création du message. Si cette erreur se produit, sélectionnez une autre surface dans les **[!UICONTROL Propriétés]** du message. Pour en savoir plus sur les surfaces de canal, consultez [cette section](../configuration/channel-surfaces.md).

   * **[!UICONTROL La payload iOS/Android push dépasse la limite de 4 Ko]** : la taille de la notification push ne peut pas dépasser 4 Ko. Pour respecter cette limite, essayez de réduire l’utilisation des images ou des émoticônes. Découvrez comment gérer le contenu de vos notifications push dans [cette section](../push/create-push.md).

![](assets/push_alert.png)

Une fois votre notification push prête, effectuez la configuration de votre [parcours](../building-journeys/journey-gs.md) ou [campaign](../campaigns/create-campaign.md) pour l’envoyer.
