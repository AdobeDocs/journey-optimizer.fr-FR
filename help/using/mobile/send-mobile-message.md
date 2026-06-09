---
solution: Journey Optimizer
product: journey optimizer
title: Vérifier et tester vos messages mobiles
description: Découvrez comment vérifier et envoyer vos messages mobiles dans Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
TQID: https://experienceleague.adobe.com/JPjBxyZzo13tgSLo0dqd5bFOwn9C6MHkA-DjLzlAdEI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: c41e8697-e629-4c38-96b3-564faaa17acfid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 534
ht-degree: 54%

---

# Vérifier et envoyer votre message mobile {#send-sms}

## Prévisualiser votre message mobile {#preview-sms}

Une fois le contenu de votre message défini, vous pouvez prévisualiser son contenu à l’aide de l’une des méthodes de simulation suivantes :

* Cliquez sur **[!UICONTROL Simuler du contenu]** pour tester les variations de contenu avec des exemples de données d’entrée ou la génération automatique d’IA. [Découvrez comment simuler des variations de contenu.](../test-approve/simulate-sample-input.md)
* Cliquez sur **[!UICONTROL Simuler du contenu]** puis sélectionnez **[!UICONTROL Simuler du contenu (profils AEP)]** dans la liste déroulante pour afficher un aperçu avec des profils de test.

![](assets/sms_preview_2.png)

Vous trouverez des informations détaillées sur comment prévisualiser et tester votre contenu dans la section [Gestion de contenu](../content-management/preview-test.md).

### Codage des caractères et limites {#sms-character-limits}

Un nombre de caractères s’affiche lors de l’accès à l’une des méthodes de simulation à partir de **[!UICONTROL Simuler du contenu]** pour vous aider à planifier et à gérer vos messages mobiles.

![](assets/sms_preview_3.png)

Journey Optimizer utilise le codage UTF-8 dans son éditeur de SMS, ce qui vous permet de saisir ou de coller des caractères codés sur deux octets ou Unicode. Ces caractères sont ensuite transmis au fournisseur de services pour diffusion. La plupart des fournisseurs SMS utilisent le codage GSM 7 bits pour les messages standard avec une limite de 160 caractères et passent à UTF-16 (UCS-2) lorsque des caractères non-GSM sont détectés, ce qui réduit la limite à 70 caractères.

Notez que le nombre de caractères ne reflète pas les variations liées à la personnalisation dynamique ou les caractères spéciaux 7 bits non-GSM.

>[!IMPORTANT]
>
>Le reporting de diffusion de SMS Journey Optimizer ne prend pas en compte les messages concaténés et la personnalisation dynamique, et peuvent donc ne pas refléter le nombre réel de messages envoyés par le fournisseur. Pour plus d’informations sur l’utilisation et la facturation, contactez votre représentant ou représentante Adobe.
>
>Pour connaître les bonnes pratiques visant à réduire les dépassements de facturation des SMS, reportez-vous à [Bonnes pratiques relatives aux SMS pour l’optimisation des caractères](mobile-cost-optimization.md).

## Valider votre contenu {#sms-validate}

>[!NOTE]
>
> Pour améliorer votre délivrabilité, utilisez les numéros de téléphone dans les formats pris en charge par le fournisseur. Par exemple, Twilio et Sinch ne prennent en charge que les numéros de téléphone au format E.164.

Vous devez vérifier les alertes dans la section supérieure de l’éditeur. Certaines d’entre elles sont de simples avertissements, mais d’autres peuvent vous empêcher d’envoyer le message. Deux types d’alertes peuvent se produire : avertissements et erreurs.

![](assets/sms-alert-button.png)

* Les **avertissements** se rapportent aux recommandations et aux bonnes pratiques. Par exemple, un message d&#39;avertissement s&#39;affiche si votre Message mobile est vide ou si les limites de caractères peuvent être dépassées avec du contenu dynamique.

  **Limites de caractères :** 160 caractères par segment (GSM 7 bits), 70 caractères pour Unicode/émojis, jusqu’à 1 500 caractères au total.

* Les **erreurs** vous empêchent de tester ou d’activer le parcours ou de publier la campagne tant que celles-ci ne sont pas corrigées. Par exemple, un message d’erreur vous avertit lorsque l’objet est manquant.

L’**d’alerte « La limite de caractères du texte du SMS a été dépassée »** peut apparaître même lorsque le message simulé est plus court, car la validation calcule la **longueur maximale possible** en évaluant toutes les branches conditionnelles, les champs de personnalisation et le contenu dynamique à leur plus longue longueur.

La validation calcule la longueur maximale de toutes les données de profil possibles, tandis que la simulation affiche la sortie réelle d’un profil de test.

## Envoyer vos messages mobiles {#sms-send}

>[!IMPORTANT]
>
> Si votre campagne est soumise à une politique de validation, vous devrez demander une validation afin de pouvoir envoyer vos messages mobiles. [En savoir plus](../test-approve/gs-approval.md)

Lorsque votre message mobile est prêt, effectuez la configuration de votre [parcours ](../building-journeys/journey-gs.md) ou [campagne](../campaigns/create-campaign.md) pour l&#39;envoyer.

**Rubriques connexes**

* [Configurer le canal SMS](mobile-configuration.md)
* [Rapports SMS/RCS/MMS](../reports/journey-global-report-cja-sms.md)
* [Créer un message mobile](create-mobile-message.md)
* [Ajouter un message dans un parcours](../building-journeys/journey-action.md)
