---
solution: Journey Optimizer
product: journey optimizer
title: Vérifier et tester vos messages texte
description: Découvrez comment vérifier et tester vos messages texte dans Journey Optimizer.
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: f275820c3f79bb4c9aca8593c2c761ccd4283795
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 96%

---

# Vérifier et envoyer votre message texte {#send-sms}

## Prévisualiser votre message texte {#preview-sms}

Une fois le contenu de votre message défini, vous pouvez utiliser les profils de test pour prévisualiser son contenu. Si vous avez inséré du contenu personnalisé, vous pouvez vérifier l’affichage de celui-ci dans le message à l’aide des données de profil de test.

Pour ce faire, cliquez sur **[!UICONTROL Simuler du contenu]**, puis ajoutez un profil de test pour vérifier votre message à l’aide des données de profil de test.

![](assets/sms_preview_2.png)

Vous trouverez des informations détaillées sur la sélection des profils de test et la prévisualisation de votre contenu dans la section [Gestion de contenu](../content-management/preview-test.md).

## Valider votre contenu {#sms-validate}

Vous devez vérifier les alertes dans la section supérieure de l’éditeur. Certaines d’entre elles sont de simples avertissements, mais d’autres peuvent vous empêcher d’envoyer le message. Deux types d’alertes peuvent se produire : avertissements et erreurs.

![](assets/sms-alert-button.png)

* Les **avertissements** se rapportent aux recommandations et aux bonnes pratiques. Par exemple, un message d’avertissement s’affiche si votre message texte est vide.

* Les **erreurs** vous empêchent de tester ou d’activer le parcours ou de publier la campagne tant que celles-ci ne sont pas corrigées. Par exemple, un message d’erreur vous avertit lorsque l’objet est manquant.


>[!NOTE]
>
> Pour améliorer votre délivrabilité, utilisez les numéros de téléphone dans les formats pris en charge par le fournisseur. Par exemple, Twilio et Sinch ne prennent en charge que les numéros de téléphone au format E.164.

## Envoyer vos messages texte {#sms-send}

Une fois votre message texte prêt, effectuez la configuration de votre [parcours](../building-journeys/journey-gs.md) ou [campagne](../campaigns/create-campaign.md) pour l’envoyer.

**Rubriques connexes**

* [Configurer le canal SMS](sms-configuration.md)
* [Rapports SMSS](../reports/journey-global-report.md#sms-global)
* [Créer un message texte](create-sms.md)
* [Ajouter un message dans un parcours](../building-journeys/journeys-message.md)
