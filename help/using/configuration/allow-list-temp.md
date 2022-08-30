---
title: Liste autorisée
description: Découvrez comment utiliser la liste autorisée.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 634e46c70aa272785950d669938f3b35ec07ab1e
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 96%

---

# Liste autorisée {#allow-list}

Il est possible de définir une liste d’envoi sécurisé spécifique au niveau du [sandbox](../administration/sandboxes.md), afin d’avoir un environnement sécurisé à des fins de test.

Par exemple, sur une instance hors production, où des erreurs peuvent se produire, la liste autorisée garantit que vous n’avez aucun risque d&#39;envoyer des messages indésirables à vos clients.

>[!NOTE]
>
>Cette fonctionnalité est disponible sur les sandbox de production et hors production.

La liste autorisée vous permet de spécifier des adresses e-mail ou des domaines individuels qui seront les seuls destinataires ou domaines autorisés à recevoir les e-mails que vous envoyez à partir d&#39;un environnement Sandbox spécifique. Cela peut vous empêcher d&#39;envoyer accidentellement des e-mails à des adresses client réelles lorsque vous vous trouvez dans un environnement de test.

>[!CAUTION]
>
>Cette fonctionnalité s&#39;applique uniquement au canal e-mail.

## Accès à la liste autorisée {#access-allowed-list}

Pour accéder à la liste détaillée des adresses e-mail et domaines autorisés, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Configuration du canal e-mail]**, puis sélectionnez **[!UICONTROL Liste autorisée]**.

>[!CAUTION]
>
>Les autorisations d’affichage, d’export et de gestion de la liste autorisée sont limitées aux [Administrateurs de Journey](../administration/ootb-product-profiles.md#journey-administrator). Pour en savoir plus sur la gestion des droits d’accès des utilisateurs [!DNL Journey Optimizer], consultez [cette section](../administration/permissions-overview.md).

## Activation de la liste autorisée {#enable-allow-list}

Pour activer la liste autorisée, procédez comme suit.

1. Accédez au menu **[!UICONTROL Canaux]** > **[!UICONTROL Configuration des e-mails]** > **[!UICONTROL Liste autorisée]**.

1. Cliquez sur **[!UICONTROL Modifier]**.

1. Sélectionnez **[!UICONTROL Activer la liste autorisée]**.

1. Cliquez sur **[!UICONTROL Enregistrer]**. La liste autorisée est activée.

La logique de liste autorisée s’applique lorsque la fonctionnalité est activée. En savoir plus dans [cette section](#logic).

>[!NOTE]
>
>Lorsqu&#39;elle est activée, la fonctionnalité de liste autorisée est respectée lors de l&#39;exécution des parcours, mais également lors du test des messages avec des [bons à tirer](../design/preview.md#send-proofs) et du test des parcours à l&#39;aide du [mode test](../building-journeys/testing-the-journey.md).

## Ajout d&#39;entités à la liste autorisée {#add-entities}

Pour ajouter de nouvelles adresses électroniques ou de nouveaux domaines à la liste autorisée pour un environnement de test spécifique, vous pouvez utiliser une [appel API](#api-call-allowed-list).

>[!NOTE]
>
>La liste autorisée peut contenir jusqu&#39;à 1 000 entrées.

### Ajout d’entités à l’aide d’un appel API {#api-call-allowed-list}

Pour renseigner la liste autorisée, vous pouvez également appeler l’API de suppression avec la valeur `ALLOWED` pour l’attribut `listType`. Par exemple :

![](assets/allow-list-api.png)

Vous pouvez effectuer les opérations **Ajouter**, **Supprimer** et **Obtenir**.

Pour en savoir plus sur l’émission d’appels d’API, consultez la documentation de référence [API Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=fr){target=&quot;_blank&quot;}.

## Logique de liste autorisée {#logic}

Lorsque la liste autorisée est [activée](#enable-allow-list), la logique suivante s’applique :

* Si la liste autorisée est **vide**, aucun e-mail ne sera envoyé.

* Si une entité est **sur la liste autorisée** et pas sur la liste de suppression, l’e-mail peut être envoyé au(x) destinataire(s) correspondant(s). Cependant, si l&#39;entité figure également sur la [liste de suppression](../reports/suppression-list.md), le destinataire correspondant ne recevra pas l’e-mail, la raison étant **[!UICONTROL Supprimé]**.

* Si une entité **n’est pas sur la liste autorisée** (et pas sur la liste de suppression), le destinataire correspondant ne recevra pas l’e-mail, la raison étant **[!UICONTROL Non autorisé]**.

>[!NOTE]
>
>Les profils avec le statut **[!UICONTROL Non autorisé]** sont exclus pendant le processus d’envoi du message. Par conséquent, bien que les **rapports sur les parcours** indiquent que ces profils ont traversé le parcours ([Lecture de segment](../building-journeys/read-segment.md) et [Message](../building-journeys/journeys-message.md)), les **Rapports sur les e-mails** ne les incluront pas dans les mesures **[!UICONTROL Envoyés]** étant donné qu’ils sont filtrés avant l’envoi des e-mails.
>
>En savoir plus sur le [Rapport dynamique](../reports/live-report.md) et le [Rapport global](../reports/global-report.md).

## Rapport d’exclusion {#reporting}

Lorsque cette fonction est activée sur un environnement Sandbox hors production, vous pouvez récupérer les adresses électroniques ou les domaines qui ont été exclus d’un envoi car ils ne se trouvaient pas sur la liste autorisée. Pour ce faire, vous pouvez utiliser le [service de requête d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=fr){target=&quot;_blank&quot;} pour effectuer les appels API ci-dessous.

Pour obtenir le **nombre d’e-mails** qui n’ont pas été envoyés car les destinataires n’étaient pas sur la liste autorisée, utilisez la requête suivante :

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

Pour obtenir la **liste des adresses e-mail** qui n’ont pas été envoyées car les destinataires n’étaient pas sur la liste autorisée, utilisez la requête suivante :

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
