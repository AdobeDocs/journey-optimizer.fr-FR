---
title: Demander l’approbation
description: Découvrez comment demander une approbation avant de publier vos parcours et campagnes.
role: User
level: Beginner
feature: Approval
source-git-commit: 509ebc377ac8c24db464728b7544eaa96e8e5da4
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 39%

---


# Demander l’approbation {#request-approval}

L&#39;accès au workflow de validation est déterminé par votre cas pratique spécifique :

* **Il n’existe aucune stratégie d’approbation active**

   * **Campagnes** : si aucune stratégie d’approbation n’est active pour l’objet de campagne dans un environnement de test, les campagnes affichent le bouton **[!UICONTROL Activer]**, ce qui vous permet de les activer sans avoir à les approuver.

   * **Parcours** : si aucune stratégie d’approbation n’est active pour l’objet de Parcours, les parcours affichent le bouton **[!UICONTROL Publish]**, ce qui vous permet de publier directement.

* **Il existe des stratégies d’approbation actives**

   * **Campagnes** : s’il existe une ou plusieurs stratégies d’approbation actives pour l’objet de campagne dans un environnement de test, toutes les campagnes de cet environnement de test afficheront le bouton **[!UICONTROL Demander l’approbation]** .
Si aucune stratégie d’approbation ne s’applique à l’objet sélectionné lorsque vous cliquez sur le bouton **[!UICONTROL Demander l’approbation]** , le processus de validation automatique est déclenché.

   * **Parcours** : s’il existe une ou plusieurs stratégies d’approbation actives pour l’objet de Parcours dans un environnement de test, tous les parcours afficheront le bouton **[!UICONTROL Demander l’approbation]** .
Si aucune stratégie d’approbation ne s’applique à l’objet sélectionné lorsque vous cliquez sur le bouton **[!UICONTROL Demander l’approbation]** , le processus de validation automatique est déclenché.

## Envoyer une demande d’approbation

Après avoir créé votre campagne ou votre parcours, cliquez sur le bouton **[!UICONTROL Demander l’approbation]** . Cela permet de vérifier si votre environnement de test contient une stratégie d’approbation active qui s’applique à la campagne ou au parcours.

* Si une stratégie d’approbation applicable est trouvée, votre campagne ou votre parcours sera envoyé pour révision.

* Si aucune stratégie d’approbation n’est applicable à la campagne ou au parcours après avoir cliqué sur le bouton **[!UICONTROL Demander l’approbation]** , la campagne ou le parcours sera automatiquement approuvé et activé ou publié.

Le volet **[!UICONTROL Demander l’approbation]** s’ouvre. Si nécessaire, envoyez un message aux approbateurs et approbatrices, puis cliquez sur **[!UICONTROL Envoyer]** pour envoyer votre demande.

![](assets/approval-request.png)

Bien que l’état de la campagne ou du parcours soit **[!UICONTROL En révision]**, vous avez la possibilité d’annuler la demande d’approbation. En cliquant sur le bouton **[!UICONTROL Annuler la demande]** , la campagne ou le parcours revient à l’étape de brouillon et une notification est envoyée aux réviseurs les informant que la demande a été annulée. Vous pouvez ensuite apporter les modifications nécessaires et demander à nouveau une approbation pour la campagne ou le parcours.

![](assets/approval-cancel.png)

## Gestion des demandes d’approbation

Une fois que la demande d’approbation a été envoyée aux personnes en charge de l’approbation, elles peuvent la vérifier et activer le parcours ou la campagne pour sa mise en ligne, ou demander des modifications si nécessaire. [Découvrir comment réviser et approuver une demande](review-approve-request.md)

Si les approbateurs et approbatrices demandent des modifications, vous recevez un e-mail et une alerte Journey Optimizer, accessible lorsque vous cliquez sur l’icône représentant une cloche en haut à droite de l’écran, dans l’onglet **[!UICONTROL Demandes]**.

![](assets/changes-requested.png)

Pour consulter la demande de modification, ouvrez-la à partir de l’e-mail ou de l’alerte pour accéder au parcours ou à la campagne et apporter les modifications demandées. Lorsque votre parcours ou votre campagne peut de nouveau faire l’objet d’une révision, envoyez une nouvelle demande d’approbation à l’aide du bouton **[!UICONTROL Demander l’approbation]**.



