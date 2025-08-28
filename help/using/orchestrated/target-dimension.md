---
solution: Journey Optimizer
product: journey optimizer
title: Création de votre dimension de ciblage
description: Découvrez comment mapper un schéma relationnel au profil client
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
source-git-commit: c1201025af216f8f3019e7696b6eb906962b681b
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 3%

---


# Configuration d’une dimension de ciblage {#configuration}

Grâce aux **[!UICONTROL Campagnes orchestrées]**, vous pouvez concevoir et diffuser des communications ciblées au niveau de l’entité, en exploitant les fonctionnalités du schéma relationnel de Adobe Experience Platform. Experience Platform utilise des schémas pour décrire la structure des données de manière cohérente et réutilisable. Lorsque des données sont ingérées dans Experience Platform, elles sont structurées selon un schéma XDM.

Bien que la segmentation des **[!UICONTROL Campagnes orchestrées]** fonctionne principalement sur des schémas relationnels, la diffusion réelle des messages se produit toujours au niveau du **Profil**.

Lors de la configuration du ciblage, vous devez définir deux aspects essentiels :

* **Schémas Cibles**

  Vous spécifiez les schémas relationnels éligibles au ciblage. Par défaut, le schéma nommé `Recipient` est utilisé, mais vous pouvez configurer d’autres schémas tels que `Visitors`, `Customers`, etc.

  >[!IMPORTANT]
  >
  > Le schéma cible doit avoir une relation 1:1 avec le schéma `Profile`. Par exemple, vous ne pouvez pas utiliser `Purchases` comme schéma cible, car il représente généralement une relation de type « un à plusieurs ».

* **Liaison de profil**

  Le système doit comprendre comment le schéma cible est mappé au schéma `Profile`. Pour ce faire, un champ d’identité partagé, qui existe à la fois dans le schéma cible et dans le schéma `Profile`, est configuré comme un espace de noms d’identité.

## Création de votre dimension de ciblage {#targeting-dimension}

Commencez par configurer l&#39;orchestration des campagnes en mappant un schéma relationnel au profil client.

1. Dans **[!UICONTROL Administration]**, accédez au menu **[!UICONTROL Configurations]** et sélectionnez **[!UICONTROL Dimension Campaign Target]**.

   ![](assets/target-dimension-1.png)

1. Cliquez sur **[!UICONTROL Créer]** pour commencer à créer votre **[!UICONTROL dimension de ciblage]**.

1. Sélectionnez le [Schéma précédemment configuré](gs-schemas.md) &#x200B; dans la liste déroulante.

   Bien que tous les schémas relationnels soient visibles, seuls les schémas ayant une relation d’identité directe avec le **Profil** peuvent être sélectionnés.

1. Sélectionnez la **[!UICONTROL valeur d’identité]** qui représente l’entité à cibler.

   Dans cet exemple, le profil client est lié à plusieurs abonnements, chacun étant représenté par un `crmID` unique dans le schéma `Recipient`. En définissant le **[!UICONTROL Dimension cible]** pour utiliser le schéma `Recipient` et son identité `crmID`, vous pouvez envoyer des messages au niveau de l’abonnement, plutôt qu’au niveau du profil client principal, en vous assurant que chaque contrat ou ligne reçoit son propre message personnalisé.

   [En savoir plus dans la documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/schema/composition#identity)

   ![](assets/target-dimension-2.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** pour terminer la configuration. Notez qu’une fois créée, une **[!UICONTROL dimension cible]** ne peut pas être supprimée ni modifiée.

Après avoir configuré le **[!UICONTROL Dimension cible]**, procédez à la création et à la configuration de votre **[!UICONTROL Configuration de canal]** et définissez les **[!UICONTROL Détails d’exécution]** correspondants.

## Configuration de votre configuration de canal {#channel-configuration}

Après avoir configuré votre **[!UICONTROL Dimension Target]**, vous devez configurer votre e-mail ou SMS **[!UICONTROL Configuration du canal]** et définir les **[!UICONTROL Détails d’exécution]** appropriés. Vous pouvez ainsi définir :

* **Niveau de diffusion des messages** : par exemple, l&#39;envoi d&#39;un message par destinataire, par exemple un seul e-mail par individu.

* **Adresse d’exécution** : champ de contact spécifique à utiliser pour l’envoi, tel qu’une adresse e-mail ou un numéro de téléphone.

Pour configurer la configuration de votre canal :

1. Commencez par créer et configurer votre **[!UICONTROL configuration de canal]**.

   Vous pouvez également mettre à jour une **[!UICONTROL configuration de canal]** existante.

   ➡️ [Suivez les étapes présentées sur cette page](../email/surface-personalization.md)

1. Dans la section **[!UICONTROL Détails d’exécution]** de votre **[!UICONTROL Configuration du canal]**, accédez à l’onglet **[!UICONTROL Campagnes orchestrées]**.

   ![](assets/target-dimension-3.png)

1. Cliquez sur **[!UICONTROL Activé]** pour le rendre compatible avec les campagnes orchestrées.

1. Choisissez votre méthode de diffusion :

   * **[!UICONTROL Dimension cible]** : envoyez-le à l’entité principale, par exemple au destinataire.

   * **[!UICONTROL Target + Dimension Secondaire]** : envoi à l’aide des entités principales et secondaires, par exemple destinataire + contrat.

1. Dans la liste déroulante, sélectionnez votre [Dimension Target précédemment créé](#targeting-dimension).

   ![](assets/target-dimension-4.png)

1. Si vous avez sélectionné **[!UICONTROL Target + Dimension Secondaire]** comme méthode de diffusion, choisissez une **[!UICONTROL Dimension Secondaire]** pour définir le contexte de diffusion des messages.

1. Dans la section **[!UICONTROL Adresse d’exécution]**, choisissez le **[!UICONTROL Source]** à utiliser pour récupérer l’adresse de diffusion, telle que l’adresse e-mail ou le numéro de téléphone :

   * **[!UICONTROL Profil]** : sélectionnez cette option si l’adresse de diffusion, par exemple l’adresse e-mail, est stockée directement dans le profil principal du client.

     Utile lors de l’envoi de messages au client principal, et non à une entité associée spécifique.

   * **[!UICONTROL Dimension cible]** : choisissez cette option si l’adresse de diffusion est stockée dans l’entité principale, par exemple un destinataire.

     Utile lorsque chaque destinataire possède sa propre adresse de diffusion, telle qu’un e-mail ou un numéro de téléphone différent.

   * **[!UICONTROL Dimension Secondaire]** : lorsque vous utilisez **[!UICONTROL Target + Dimension Secondaire]** comme méthode de diffusion, sélectionnez la **[!UICONTROL Dimension Secondaire appropriée]** que vous avez précédemment configurée.

     Par exemple, si la dimension secondaire représente une réservation ou un abonnement, l’adresse d’exécution, telle qu’un e-mail, peut être extraite de ce niveau. Cela s’avère utile lorsque les profils utilisent des coordonnées différentes lors de la réservation ou de l’abonnement à un service.

1. Dans le champ **[!UICONTROL Adresse de diffusion]**, cliquez sur ![icône de modification](assets/do-not-localize/edit.svg) pour choisir le champ spécifique à utiliser pour votre diffusion de messages.

   ![](assets/target-dimension-4.png)

1. Une fois la configuration effectuée, cliquez sur **[!UICONTROL Envoyer]**.

Votre canal est maintenant prêt à être utilisé avec les **Campagnes orchestrées** et les messages seront diffusés en fonction de la dimension cible sélectionnée.
