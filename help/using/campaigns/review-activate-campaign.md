---
solution: Journey Optimizer
product: journey optimizer
title: Vérifier et activer une campagne d’action
description: Découvrez comment vérifier et activer des campagnes d’action dans [!DNL Journey Optimizer].
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campagne, vérification, validation, activation, activer, optimizer
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
TQID: https://experienceleague.adobe.com/BKGXccq-kwZJA-cZ4SAyf3zJBIvyJnr5V01xmbQgwmo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 087a4bd254486a4962d8338d1d35ffb5345341af
workflow-type: tm+mt
source-wordcount: 310
ht-degree: 92%

---

# Vérifier et activer la campagne d’action {#action-campaign-review}

Une fois votre campagne configurée, vous devez vérifier ses paramètres et son contenu avant de l’activer. Pour ce faire, suivez les étapes ci-après.

>[!IMPORTANT]
>
> Si votre campagne est soumise à une politique d’approbation, vous devrez effectuer une demande d’approbation pour pouvoir l’envoyer. [En savoir plus](../test-approve/gs-approval.md)

1. Dans l’écran de configuration de la campagne, cliquez sur **[!UICONTROL Vérifier pour activer]** pour afficher un résumé de la campagne.

   ![](assets/campaign-review.png)

1. Un récapitulatif de la configuration de la campagne s’affiche, vous permettant de vérifier si un paramètre est incorrect ou manquant et de modifier votre campagne si nécessaire.

   En cas d’erreur, vous ne pouvez pas activer la campagne. Résolvez les erreurs avant de continuer.

   ![](assets/create-campaign-alerts.png)

1. Lorsqu’une campagne utilise des [politiques de décision](../experience-decisioning/create-decision.md) dans son contenu, vous pouvez examiner la structure de chaque politique et copier les détails techniques directement à partir du résumé de la campagne. [Voici comment procéder](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

1. Vérifiez que votre campagne est correctement configurée, puis cliquez sur **[!UICONTROL Activer]**.

1. La campagne est activée. Son statut est soit **[!UICONTROL Actif]**, soit **[!UICONTROL Planifié]** si vous avez saisi une date de début. Le message configuré dans la campagne est envoyé immédiatement ou à la date indiquée.

   Le statut **[!UICONTROL Terminé]** est automatiquement affecté à une campagne 3 jours après son activation ou à la date de fin de la campagne si son exécution est récurrente. [Découvrez les statuts des campagnes](manage-campaigns.md#statuses).

   Si aucune date de fin n’a été spécifiée, la campagne conserve le statut **[!UICONTROL Actif]**. Pour le modifier, vous devez arrêter manuellement la campagne. [Découvrez comment arrêter une campagne](manage-campaigns.md)

1. Une fois qu’une campagne a été activée, vous pouvez vérifier à tout moment ses informations en l’ouvrant. Le résumé vous permet d’obtenir des statistiques sur le nombre de profils ciblés et les actions diffusées et en échec.

   Vous pouvez également obtenir des statistiques supplémentaires dans les rapports dédiés en cliquant sur le bouton **[!UICONTROL Rapports]**. [En savoir plus](../reports/campaign-global-report-cja.md)

   ![](assets/create-campaign-summary.png)
