---
solution: Journey Optimizer
product: journey optimizer
title: Gérer le processus d’opt-out
description: Découvrez comment gérer le processus d’opt-out et la confidentialité
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 8b459f71852d031dc650b77725bdc693325cdb1d
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 45%

---

# Gérer le processus d’opt-out {#consent}

Fournir aux destinataires la possibilité de se désabonner de la réception des communications d’une marque est une obligation légale, et s’assurer que ce choix est respecté. Pour en savoir plus sur la législation applicable, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=fr#regulations){target="_blank"}.

**Pourquoi est-ce important ?**

* Le fait de ne pas se conformer à ces règlements introduit des risques juridiques réglementaires pour votre marque.
* Cela vous aide à éviter d&#39;envoyer des communications non sollicitées à vos destinataires, ce qui pourrait les faire marquer vos messages comme des courriers indésirables et nuire à votre réputation.

## Gestion des désabonnements dans les parcours et les campagnes {#opt-out-ajo}

Lors de l’envoi de messages à partir des parcours ou des campagnes, vous devez toujours vous assurer que les client(e)s peuvent annuler l’abonnement à de futures communications. Une fois désinscrits, les profils sont automatiquement supprimés de l’audience des futurs messages marketing.

Alors que **[!DNL Journey Optimizer]** offre des moyens permettant de gérer les désinscriptions des e-mails et des SMS, les notifications push ne nécessitent aucune action de votre part, car les destinataires peuvent annuler leur abonnement depuis leurs appareils. Par exemple, lors du téléchargement ou de l’utilisation de votre application, ils peuvent choisir d’arrêter les notifications. De même, ils peuvent modifier les paramètres de notification par le biais du système d’exploitation mobile.

Découvrez comment gérer les désinscriptions des e-mails et des SMS de Journey Optimizer dans les sections suivantes :

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Prospect" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%">
</a>
<div><a href="../email/email-opt-out.md"><strong>Gestion du processus de désinscription aux e-mails</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Peu fréquent" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%">
</a>
<div>
<a href="../sms/sms-opt-out.md"><strong>Gestion du processus de désinscription aux SMS</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>Dans [!DNL Journey Optimizer], le consentement est géré par le [Schéma de consentement](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=fr){target="_blank"}. By default, the value for the consent field is empty and treated as consent to receive your communications. You can modify this default value while onboarding to one of the possible values listed [here](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=fr#choice-values){target="_blank"} d’Experience Platform.

## Mise en oeuvre du consentement de personnalisation {#opt-out-personalization}

Vos clients peuvent également refuser la présentation de contenus personnalisés. Une fois qu’un profil s’est désinscrit de la personnalisation, vous devez vous assurer que ses données ne sont pas utilisées pour la personnalisation et que vous devez remplacer tout contenu personnalisé par une variante de secours.

### Dans la gestion des décisions

Lors de l’utilisation des offres, les préférences de personnalisation ne sont pas automatiquement implémentées dans [portées de décision](../offers/offer-activities/create-offer-activities.md#add-decision-scopes) utilisé à partir d’un [prise de décision](../offers/api-reference/offer-delivery-api/decisioning-api.md) demande d’API ou [prise de décision Edge](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md) requête API. Dans ce cas, vous devez appliquer manuellement le consentement de personnalisation. Pour ce faire, procédez comme suit.

>[!NOTE]
>
>Portées de décision utilisées dans [!DNL Journey Optimizer] les canaux créés répondent à cette exigence du parcours ou de la campagne auquel ils appartiennent.



1. Créez un [Segment Adobe Experience Platform](../segment/about-segments.md) en utilisant un attribut de profil tel que : *&quot;Concède à la personnalisation = Vrai&quot;* pour cibler les utilisateurs qui ont consenti à la personnalisation.

1. Lors de la création d’un [décision](../offers/offer-activities/create-offer-activities.md), ajoutez une portée de décision et définissez une contrainte d’éligibilité basée sur ce segment pour chaque collection de critères d’évaluation contenant des offres personnalisées.

1. Créez un [offre de secours](../offers/offer-library/creating-fallback-offers.md) qui n’inclut pas de contenu personnalisé.

1. [Attribuer](../offers/offer-activities/create-offer-activities.md#add-fallback) offre de secours non personnalisée à la décision.

1. [Examiner et enregistrer la décision.](../offers/offer-activities/create-offer-activities.md#review)

Si un utilisateur possède :

* consentement pour la personnalisation, la portée de la décision détermine la meilleure offre pour ce profil.

* n’étant pas accepté pour la personnalisation, le profil correspondant ne sera éligible à aucune des offres qui se trouvent dans les critères d’évaluation et recevra donc l’offre de secours non personnalisée.

>[!NOTE]
>
>Consentement pour utiliser les données de profil dans [modélisation des données](../offers/ranking/ai-models.md) n’est pas encore pris en charge dans [!DNL Journey Optimizer].

