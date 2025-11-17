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
source-git-commit: 7eaca4faf61431fa438afc7550ff4b89f95fa192
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 64%

---

# Vérifier et envoyer votre message texte (SMS/MMS){#send-sms}

## Prévisualiser votre message texte {#preview-sms}

Une fois le contenu de votre message défini, vous pouvez utiliser des profils de test ou des exemples de données d’entrée (chargés à partir d’un fichier CSV/JSON ou ajoutés manuellement) pour le prévisualiser. Si vous avez inséré du contenu personnalisé, vous pouvez vérifier la façon dont celui-ci s’affiche dans le message.

Pour ce faire, cliquez sur **[!UICONTROL Simuler du contenu]**, puis vérifiez votre message à l’aide des données de profil de test.

![](assets/sms_preview_2.png)

Vous trouverez des informations détaillées sur comment prévisualiser et tester votre contenu dans la section [Gestion de contenu](../content-management/preview-test.md).

### Encodage et limites des caractères {#sms-character-limits}

Un nombre de caractères s’affiche lors de l’accès au menu **[!UICONTROL Simuler du contenu]** pour vous aider à planifier et à gérer vos SMS.

![](assets/sms_preview_3.png)

Journey Optimizer utilise le codage UTF-8 dans son éditeur de SMS, ce qui vous permet de saisir ou de coller des caractères codés sur deux octets ou Unicode. Ces caractères sont ensuite transmis au fournisseur de services pour diffusion. La plupart des fournisseurs SMS utilisent le codage GSM 7 bits pour les messages standard avec une limite de 160 caractères et passent à UTF-16 (UCS-2) lorsque des caractères non-GSM sont détectés avec une limite de 70 caractères.

Notez que le nombre de caractères ne reflète pas les variations introduites par la personnalisation dynamique ou les caractères spéciaux 7 bits non-GSM.

>[!IMPORTANT]
>
>Les rapports de diffusion SMS Journey Optimizer ne prennent pas en compte les messages concaténés et la personnalisation dynamique, et peuvent donc ne pas refléter le nombre réel de messages envoyés depuis le fournisseur. Pour plus d’informations sur l’utilisation et la facturation, contactez votre représentant Adobe.
>
>Pour connaître les bonnes pratiques relatives à la minimisation des dépassements de facturation par SMS, reportez-vous à [Bonnes pratiques relatives aux SMS pour l’optimisation des caractères](sms-cost-optimization.md).

## Valider votre contenu {#sms-validate}

Vous devez vérifier les alertes dans la section supérieure de l’éditeur. Certaines d’entre elles sont de simples avertissements, mais d’autres peuvent vous empêcher d’envoyer le message. Deux types d’alertes peuvent se produire : avertissements et erreurs.

![](assets/sms-alert-button.png)

* Les **avertissements** se rapportent aux recommandations et aux bonnes pratiques. Par exemple, un message d’avertissement s’affiche si votre message texte est vide.

* Les **erreurs** vous empêchent de tester ou d’activer le parcours ou de publier la campagne tant que celles-ci ne sont pas corrigées. Par exemple, un message d’erreur vous avertit lorsque l’objet est manquant.


>[!NOTE]
>
> Pour améliorer votre délivrabilité, utilisez les numéros de téléphone dans les formats pris en charge par le fournisseur. Par exemple, Twilio et Sinch ne prennent en charge que les numéros de téléphone au format E.164.

## Envoyer vos messages texte {#sms-send}

>[!IMPORTANT]
>
> Si votre campagne est soumise à une politique de validation, vous devrez effectuer une demande d’approbation afin de pouvoir envoyer vos SMS. [En savoir plus](../test-approve/gs-approval.md)

Une fois votre message texte prêt, effectuez la configuration de votre [parcours](../building-journeys/journey-gs.md) ou [campagne](../campaigns/create-campaign.md) pour l’envoyer.

**Rubriques connexes**

* [Configurer le canal SMS](sms-configuration.md)
* [Rapports SMS/MMS](../reports/journey-global-report-cja-sms.md)
* [Créer un message texte](create-sms.md)
* [Ajouter un message dans un parcours](../building-journeys/journeys-message.md)
