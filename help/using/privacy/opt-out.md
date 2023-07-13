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
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 43%

---

# Gérer le processus d’opt-out {#consent}

La possibilité pour les destinataires de se désabonner de la réception des communications d’une marque est une exigence légale, ainsi que de veiller au respect de leur choix. Pour en savoir plus sur la législation applicable, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=fr#regulations){target="_blank"}.

**Pourquoi est-ce important ?**

* Le fait de ne pas se conformer à ces règlements introduit des risques juridiques réglementaires pour votre marque.
* Cela vous aide à éviter d&#39;envoyer des communications non sollicitées à vos destinataires, ce qui pourrait les faire marquer vos messages comme des courriers indésirables et nuire à votre réputation.

## Gérer les désabonnements dans les parcours et les campagnes {#opt-out-ajo}

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

## Implémenter le consentement de personnalisation {#opt-out-personalization}

Vos clientes et clients peuvent également refuser la présentation de contenus personnalisés. Une fois qu’un profil a refusé la personnalisation, vous devez vous assurer que ses données ne sont pas utilisées pour celle-ci. Vous devez en outre remplacer tout contenu personnalisé par une variante de secours.

### Dans la gestion des décisions

Lors de l’utilisation des offres, les préférences de personnalisation ne sont pas automatiquement implémentées dans les [portées de décision](../offers/offer-activities/create-offer-activities.md#add-decision-scopes) utilisées à partir d’une requête d’API de [prise de décision](../offers/api-reference/offer-delivery-api/decisioning-api.md) ou de [prise de décision Edge](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md). Dans ce cas, vous devez appliquer manuellement le consentement de personnalisation. Pour ce faire, procédez comme suit.

>[!NOTE]
>
>Les portées de décision utilisées dans les canaux [!DNL Journey Optimizer] créés répondent à cette exigence de la campagne ou du parcours auxquels ils appartiennent.

1. Créez un [Audience Adobe Experience Platform](../audience/access-audiences.md) en utilisant la variable [Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=fr){target="_blank"} et utiliser un attribut de profil tel que **[!UICONTROL Personnaliser le contenu = Oui (opt-in)]** pour cibler les utilisateurs qui ont consenti à la personnalisation.

   ![](assets/perso-consent-od-audience.png)

1. Lors de la création d’un [décision](../offers/offer-activities/create-offer-activities.md), ajoutez une portée de décision et définissez une contrainte d’éligibilité basée sur cette audience pour chaque collection de critères d’évaluation contenant des offres personnalisées.

   ![](assets/perso-consent-od-audience-decision.png)

1. Créez une [offre de secours](../offers/offer-library/creating-fallback-offers.md) qui n’inclut pas de contenu personnalisé.

1. [Attribuez](../offers/offer-activities/create-offer-activities.md#add-fallback) l’offre de secours non personnalisée à la décision.

   ![](assets/perso-consent-od-audience-fallback.png)

1. [Examinez et enregistrez](../offers/offer-activities/create-offer-activities.md#review) la décision.

Si un utilisateur ou une utilisatrice :

* a consenti à la personnalisation, la portée de la décision détermine la meilleure offre pour ce profil ;

* n’a pas consenti à la personnalisation, le profil correspondant ne sera éligible à aucune des offres qui se trouvent dans les critères d’évaluation et recevra donc l’offre de secours non personnalisée.

>[!NOTE]
>
>Le consentement pour utiliser les données de profil dans la [modélisation des données](../offers/ranking/ai-models.md) n’est pas encore pris en charge dans [!DNL Journey Optimizer].

## Dans l&#39;éditeur d&#39;expression

<!--Expressions Editor while personalizing images, text, subject line  ( Segment in Campaigns) - UI and Headless -->

Le [Editeur d&#39;expression](../personalization/personalization-build-expressions.md) elle-même n’effectue aucune vérification ou application du consentement, car elle n’est pas impliquée dans la diffusion des messages.

Cependant, l’utilisation de libellés de contrôle d’accès basés sur le droit permet de restreindre les champs pouvant être utilisés pour la personnalisation. Le [aperçu du message](../email/preview.md#preview-email) et [service de rendu des emails](../email/preview.md#email-rendering) masquera les champs identifiés avec des informations sensibles.

>[!NOTE]
>
>En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC) dans [cette section](../administration/object-based-access.md).


Dans [!DNL Journey Optimizer] dans les campagnes, la stratégie de consentement est appliquée comme suit :

* Vous pouvez inclure des définitions de stratégie de consentement dans le cadre de la création de l’audience afin de vous assurer que l’audience sélectionnée pour la campagne a déjà été **profils filtrés qui ne correspondent pas aux critères de consentement**.

* [!DNL Journey Optimizer] effectue une vérification générale du consentement au niveau du canal pour **s’assurer que les profils ont donné leur accord** pour recevoir les communications marketing sur le canal correspondant.

  >[!NOTE]
  >
  >Le [!DNL Journey Optimizer] actuellement, l’objet campaign lui-même n’effectue aucune vérification supplémentaire de l’application de la stratégie de consentement.

Pour appliquer manuellement le consentement à la personnalisation dans les campagnes, suivez l’une des options ci-dessous.

### Utilisation du créateur de règles de segment

Vous pouvez utiliser le créateur de règles de segment pour créer une audience contenant des profils d’exclusion.

1. Créez un [Audience Adobe Experience Platform](../audience/access-audiences.md) en utilisant la variable [Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=fr){target="_blank"}.

   ![](assets/perso-consent-audience-build-rule.png)

1. Sélectionnez un attribut de profil tel que **[!UICONTROL Personnaliser le contenu = Non (opt-out)]** pour exclure les utilisateurs qui n’ont pas consenti à la personnalisation.

   ![](assets/perso-consent-audience-no.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Vous pouvez désormais utiliser cette audience pour filtrer les profils qui n’ont pas donné leur consentement à la personnalisation de vos campagnes.

### Utilisation d&#39;une activité de partage dans un workflow de composition

Vous pouvez également ajouter une vérification du consentement de personnalisation à une audience en ajoutant une activité de partage à un workflow de composition.

1. Créez une audience à l’aide du **[!UICONTROL Composer l’audience]** . [En savoir plus sur la création d’un workflow de composition](../audience/create-compositions.md)

   ![](assets/perso-consent-audience-compose.png)

1. Ajoutez l&#39;audience de départ à l&#39;aide du bouton dédié situé à droite.

1. Cliquez sur l’icône + et sélectionnez **[!UICONTROL Partage]** pour créer une audience partagée. [En savoir plus sur l&#39;activité Partage](../audience/composition-canvas.md#split)

   ![](assets/perso-consent-audience-split.png)

1. Sélectionner **[!UICONTROL Partage d’attributs]** comme type de division dans le volet de droite.

   ![](assets/perso-consent-audience-attribute-split.png)

1. Cliquez sur l’icône en forme de crayon en regard de la propriété **[!UICONTROL Attribut]** pour afficher le champ **[!UICONTROL Sélection d’un attribut de profil]** fenêtre.

1. Recherchez l’attribut de consentement de personnalisation (`profile.consents.personalize.content.val`) et sélectionnez-le.

   ![](assets/perso-consent-audience-consent-attribute.png)

1. **[!UICONTROL Chemin 1]** sera l’audience non personnalisée. Choisissez un libellé pertinent.

1. Sélectionnez la valeur appropriée parmi celles-ci [list](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=fr#choice-values){target="_blank"}.

   Dans ce cas, nous utiliserons `n` pour indiquer que les utilisateurs ne consentent pas à l’utilisation de leurs données à des fins de personnalisation.

   ![](assets/perso-consent-audience-path-1-n.png)

1. Vous pouvez créer un chemin d’accès distinct pour les autres valeurs de choix. Vous pouvez également choisir de supprimer les autres chemins et de les activer. **[!UICONTROL Autres profils]** pour inclure tous les autres profils qui n’avaient pas la valeur de choix de `n`.

1. Une fois que vous avez terminé, cliquez sur **[!UICONTROL Enregistrement de l’audience]** pour chaque chemin afin d&#39;enregistrer le résultat de votre workflow dans une nouvelle audience. Une audience sera enregistrée dans Adobe Experience Platform pour chaque chemin.

1. Une fois terminé, publiez le workflow de composition.

Vous pouvez désormais utiliser cette audience pour filtrer les profils qui n’ont pas donné leur consentement à la personnalisation de vos campagnes.

>[!NOTE]
>
>Si vous créez une audience qui n&#39;a pas donné son consentement pour la personnalisation et que vous sélectionnez ensuite cette audience dans une campagne, les outils de personnalisation restent disponibles. Il appartient à vos utilisateurs marketing de comprendre que s’ils travaillent avec une audience qui ne doit pas recevoir de personnalisation, ils ne doivent pas utiliser d’outils de personnalisation.
