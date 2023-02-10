---
solution: Journey Optimizer
product: journey optimizer
title: Prévisualiser votre SMS
description: Découvrez comment prévisualiser et tester votre SMS dans Journey Optimizer.
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 100%

---

# Envoyer votre SMS {#send-sms}

## Prévisualiser votre SMS {#preview-sms}

Une fois le contenu de votre message défini, vous pouvez utiliser des profils de test pour le prévisualiser et le tester. Si vous avez inséré du contenu personnalisé, vous pourrez vérifier comment ce contenu s’affiche dans le message en exploitant les données du profil de test.

1. Cliquez sur **[!UICONTROL Simuler du contenu]**.

1. Cliquez sur **[!UICONTROL Gérer les profils de test]** pour ajouter un profil de test.

1. Recherchez votre profil de test avec les champs **[!UICONTROL Espace de noms d’identité]** et **[!UICONTROL Valeur d’identité]**. Cliquez ensuite sur **[!UICONTROL Ajouter un profil]**.

   ![](assets/sms_preview_3.png)

1. Une fois que vous avez sélectionné votre profil de test, vous pouvez fermer la fenêtre **[!UICONTROL Ajouter un profil de test]**.

   ![](assets/sms_preview_1.png)

1. Dans la fenêtre de prévisualisation et de test, les données du profil de test sont exploitées dans le contenu du message.

   Par exemple, pour ce SMS, le contenu du message est personnalisé :

   ![](assets/sms_preview_2.png)

## Valider votre SMS{#sms-preview}

>[!NOTE]
>
> Pour une meilleure délivrabilité, vous devez toujours utiliser les numéros de téléphone dans les formats pris en charge par le fournisseur. Par exemple, Twilio et Sinch ne prennent en charge que les numéros de téléphone au format E.164.

Vous devez également vérifier les alertes dans la section supérieure de l’éditeur.  Certaines d’entre elles sont de simples avertissements, mais d’autres peuvent vous empêcher d’utiliser le message. Deux types d’alertes peuvent avoir lieu :

* Les **avertissements** se rapportent aux recommandations et aux bonnes pratiques. Par exemple, un message s’affichera si votre SMS est vide.

* Les **erreurs** vous empêchent de tester ou d’activer le parcours tant qu’elles ne sont pas corrigées. Par exemple, un message vous avertit que l’objet est manquant.

![](assets/sms-alert-button.png)

Une fois votre SMS prêt, effectuez la configuration de votre [parcours](../building-journeys/journey-gs.md) ou [campagne](../campaigns/create-campaign.md) pour l’envoyer.

**Rubriques connexes**

* [Configurer le canal SMS](sms-configuration.md)
* [Rapport SMS](../reports/journey-global-report.md#sms-global)
* [Création d’un SMS](create-sms.md)
* [Ajout dʼun message dans un parcours](../building-journeys/journeys-message.md)
