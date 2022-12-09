---
solution: Journey Optimizer
product: journey optimizer
title: Prise en charge de l’archivage dans Journey Optimizer
description: Découvrez comment archiver des messages
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 186a5044-80d5-4633-a7a7-133e155c5e9f
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 0%

---

# Prise en charge de l’archivage {#archiving-support}

## Comment archiver des messages {#about-archiving}

Des réglementations telles que la loi HIPAA exigent que : [!DNL Journey Optimizer] doit fournir un moyen d’archiver les messages envoyés aux individus. En effet, si vos clients soumettent une réclamation, ils devraient avoir la possibilité d&#39;obtenir une copie du message envoyé à des fins de vérification.

* Pour le canal email, [!DNL Journey Optimizer] fournit une fonctionnalité de messagerie en Cci intégrée. [En savoir plus](#bcc-email)

* De plus, pour tous les canaux, vous pouvez utiliser le champ &quot;Modèle&quot; dans la variable **Jeu de données d’entité**, qui contient les détails des modèles de messages non personnalisés. Exportez le jeu de données avec ce champ pour enregistrer des métadonnées telles que : qui a envoyé le message, à qui et quand. Notez que les données personnalisées ne sont pas exportées : seul le modèle (format et structure du message) est pris en compte. [En savoir plus](../data/datasets-query-examples.md#entity-dataset)

>[!NOTE]
>
>[!DNL Journey Optimizer] ne possède pas la prise en charge des exigences d’archivage des SMS. Pour une prise en charge dédiée de l’archivage, travaillez avec votre fournisseur SMS (Synch ou Twilio).

## Utilisation de la fonctionnalité Cci pour les emails {#bcc-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_bcc"
>title="Définition d’une adresse email en Cci"
>abstract="Vous pouvez conserver une copie des emails envoyés en les envoyant à une boîte de réception en Cci. Saisissez l&#39;adresse email de votre choix afin que chaque email envoyé soit copié en aveugle vers cette adresse Cci. Notez que le domaine de l’adresse en Cci ne doit pas être le même que tout sous-domaine délégué à Adobe. Cette fonction est facultative."

Vous pouvez envoyer une copie identique (ou une copie en carbone invisible) d’un email envoyé par [!DNL Journey Optimizer] dans une boîte de réception Cci. Cette fonctionnalité facultative vous permet de conserver des copies des communications par e-mail que vous envoyez à vos utilisateurs à des fins de conformité et/ou d’archivage. Cela sera invisible pour les destinataires de la diffusion.

### Activer les emails en Cci {#enable-bcc}

Pour activer la variable **[!UICONTROL BCC email]** , saisissez l&#39;adresse email de votre choix dans le champ dédié du champ [surface du canal](channel-surfaces.md) (c’est-à-dire le paramètre prédéfini du message). Vous pouvez spécifier n’importe quelle adresse externe au format correct, à l’exception d’une adresse électronique définie sur un sous-domaine délégué à Adobe. Par exemple, si vous avez délégué la variable *marketing.luma.com* sous-domaine à Adobe, toute adresse telle que *abc@marketing.luma.com* est interdit.

>[!CAUTION]
>
>Vous ne pouvez définir qu&#39;une seule adresse email en Cci. Assurez-vous que l&#39;adresse en Cci dispose d&#39;une capacité de réception suffisante pour stocker tous les emails envoyés à l&#39;aide de la surface actuelle du canal.
>
>D’autres recommandations sont répertoriées dans la section [cette section](#bcc-recommendations-limitations).

>[!NOTE]
>
>Si vous avez acheté l’offre de module complémentaire Healthcare Shield, vous devez vous assurer que le FAI de votre adresse en Cci prend en charge le protocole TLS 1.2.

![](assets/preset-bcc.png)

Tous les emails utilisant cette surface seront copiés en aveugle vers l&#39;adresse email en Cci que vous avez saisie. De là, ils peuvent être traités et archivés à l’aide d’un système externe.

>[!CAUTION]
>
>Votre utilisation de la fonctionnalité en Cci sera prise en compte par rapport au nombre de messages pour lesquels vous disposez d’une licence. Par conséquent, activez-la uniquement sur les surfaces utilisées pour les communications critiques que vous souhaitez archiver. Vérifiez votre contrat pour les volumes sous licence.

Le paramètre d’adresse email en Cci est immédiatement enregistré et traité au niveau de la surface. Lorsque vous créez un message à partir de cette surface, l&#39;adresse email en Cci s&#39;affiche automatiquement.

![](assets/preset-bcc-in-msg.png)

Cependant, l’adresse en Cci est sélectionnée pour envoyer des communications selon la logique décrite. [here](../email/email-settings.md).

### Recommandations et limitations {#bcc-recommendations-limitations}

* Pour garantir la conformité de vos informations personnelles, les emails en Cci doivent être traités par un système d’archivage capable de stocker en toute sécurité des informations d’identification personnelles (PII).

* Comme les messages peuvent contenir des données sensibles ou privées, telles que des informations d’identification personnelle (PII), vérifiez que l’adresse en Cci est correcte et sécurisez l’accès aux messages.

* Votre boîte de réception utilisée pour la fonctionnalité Cci doit être correctement gérée pour l’espace et la diffusion. Si la boîte de réception renvoie des rebonds, certains emails peuvent ne pas être reçus et ne seront donc pas archivés.

* Les messages peuvent être envoyés à l&#39;adresse email en Cci avant les destinataires cibles. Les messages en Cci peuvent également être envoyés même si les messages originaux peuvent avoir [bounce](../reports/suppression-list.md#delivery-failures).

   <!--OR: Only successfully sent emails are taken in account. [Bounces](../reports/suppression-list.md#delivery-failures) are not. TO CHECK -->

* Ne pas ouvrir ni cliquer sur les emails envoyés à l&#39;adresse en Cci, car cela est pris en compte dans le nombre total d&#39;ouvertures et de clics de l&#39;analyse d&#39;envoi, ce qui peut entraîner des erreurs de calcul dans [rapports](../reports/global-report.md).

* Ne marquez pas les messages comme spam dans la boîte de réception en Cci, car cela aura un impact sur tous les autres emails envoyés à cette adresse.


>[!CAUTION]
>
>Ne cliquez pas sur le lien de désabonnement dans les emails envoyés à l&#39;adresse en Cci, car vous désabonnerez immédiatement les destinataires correspondants.

### Conformité au RGPD {#gdpr-compliance}

Les réglementations telles que le RGPD stipulent que les titulaires de données doivent pouvoir modifier leur consentement à tout moment. Puisque les emails en Cci que vous envoyez avec Journey Optimizer incluent des informations d’identification personnelle (PII) en toute sécurité, vous devez modifier la variable **[!UICONTROL CJM Email BCC Feedback Event Schema]** être en mesure de gérer ces informations d’identification personnelle conformément au RGPD et aux règlements similaires.

Pour ce faire, procédez comme suit.

1. Accédez à **[!UICONTROL Data management]** > **[!UICONTROL Schemas]** > **[!UICONTROL Browse]** et sélectionnez **[!UICONTROL CJM Email BCC Feedback Event Schema]**.

   ![](assets/preset-bcc-schema.png)

1. Cliquez pour développer **[!UICONTROL _experience]**, **[!UICONTROL customerJourneyManagment]** then **[!UICONTROL secondaryRecipientDetail]**.

1. Sélectionner **[!UICONTROL originalRecipientAddress]**.

1. Dans le **[!UICONTROL Field properties]** à droite, faites défiler l’écran jusqu’à la **[!UICONTROL Identity]** .

1. Sélectionnez-le et sélectionnez également **[!UICONTROL Primary identity]**.

1. Sélectionnez un espace de noms dans la liste déroulante.

   ![](assets/preset-bcc-schema-identity.png)

1. Cliquez sur **[!UICONTROL Apply]**.

>[!NOTE]
>
>En savoir plus sur la gestion de la confidentialité et les réglementations applicables dans [Documentation d’Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html){target=&quot;_blank&quot;}.

### Données de reporting en Cci {#bcc-reporting}

La création de rapports en tant que tels en Cci n’est pas disponible dans les rapports sur les parcours et les messages. Toutefois, les informations sont stockées dans un jeu de données système appelé **[!UICONTROL AJO BCC Feedback Event Dataset]**. Vous pouvez exécuter des requêtes sur ce jeu de données pour trouver des informations utiles à des fins de débogage, par exemple.

Vous pouvez accéder à ce jeu de données par le biais de l’interface utilisateur. Sélectionner **[!UICONTROL Data management]** > **[!UICONTROL Datasets]** > **[!UICONTROL Browse]** et activez la variable **[!UICONTROL Show system datasets]** basculez à partir du filtre pour afficher les jeux de données générés par le système. En savoir plus sur l’accès aux jeux de données dans [cette section](../data/get-started-datasets.md#access-datasets).

![](assets/preset-bcc-dataset.png)

Pour exécuter des requêtes sur ce jeu de données, vous pouvez utiliser l’éditeur de requêtes fourni par la variable [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}. Pour y accéder, sélectionnez **[!UICONTROL Data management]** > **[!UICONTROL Queries]** et cliquez sur **[!UICONTROL Create query]**. [En savoir plus](../data/get-started-queries.md)

![](assets/preset-bcc-queries.png)

Selon les informations que vous recherchez, vous pouvez exécuter les requêtes suivantes.

1. Pour toutes les autres requêtes ci-dessous, vous aurez besoin de l’identifiant d’action de parcours. Exécutez cette requête pour récupérer tous les identifiants d’action associés à un ID de version de parcours particulier au cours des 2 derniers jours :

       &quot;
       SELECT
       DISTINCT
       CAST(TIMESTAMP EN TANT QUE DATE) COMME EventTime,
       _experience.journeyOrchestration.stepEvents.journeyVersionID,
       _experience.journeyOrchestration.stepEvents.actionName,
       _experience.journeyOrchestration.stepEvents.actionID
       FROM journey_step_events
       WHERE
       _experience.journeyOrchestration.stepEvents.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39; AND
       _experience.journeyOrchestration.stepEvents.actionID n’est pas NULL AND
       HORODATAGE > NOW() - INTERVALLE &quot;2&quot; JOUR
       ORDER PAR EventTime DESC ;
       &quot;
   
   >[!NOTE]
   >
   >Pour obtenir le `<journey version id>`, sélectionnez le paramètre correspondant. [version du parcours](../building-journeys/journey.md#journey-versions) de la **[!UICONTROL Journey management]** > **[!UICONTROL Journeys]** . L’ID de version du parcours s’affiche à la fin de l’URL affichée dans votre navigateur web.
   >
   >![](assets/preset-bcc-action-id.png)

1. Exécutez cette requête pour récupérer tous les événements de retour de message (en particulier l’état des retours) générés pour un message spécifique ciblé sur un utilisateur spécifique au cours des 2 derniers jours :

       &quot;
       SELECT
       _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID,
       _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID,
       timestamp AS EventTime,
       _experience.customerJourneyManagement.emailChannelContext.address AS RecipientAddress,
       _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
       CASE_experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
       LORSQUE &quot;envoyé&quot; PUIS &quot;Envoyé&quot;
       LORSQUE &quot;delay&quot; PUIS &quot;Retry&quot;
       QUAND &#39;out_of_band&#39; PUIS &#39;Bounce&#39;
       LORSQUE &quot;rebond&quot; PUIS &quot;rebond&quot;
       END AS FeedbackStatusCategory
       FROM cjm_message_feedback_event_dataset
       WHERE
       timestamp > now() - INTERVALLE &quot;2&quot; day AND
       _experience.customerJourneyManagement.messageExecution.journeyVersionID = &#39;&lt;journey version=&quot;&quot; id=&quot;&quot;>&#39; AND
       _experience.customerJourneyManagement.messageExecution.journeyActionID = &#39;&lt;journey action=&quot;&quot; id=&quot;&quot;>&#39; AND
       _experience.customerJourneyManagement.emailChannelContext.address = &#39;&lt;recipient email=&quot;&quot; address=&quot;&quot;>&#39;
       ORDER PAR EventTime DESC ;
       &quot;
   
   >[!NOTE]
   >
   >Pour obtenir le `<journey action id>` , exécutez la première requête décrite ci-dessus à l’aide de l’identifiant de version du parcours. Le `<recipient email address>` est l’adresse électronique du destinataire ciblé ou réel.

1. Exécutez cette requête pour récupérer tous les événements de retour de message en Cci générés pour un message spécifique ciblé sur un utilisateur spécifique au cours des deux derniers jours :

   ```
   SELECT   
   _experience.customerJourneyManagement.messageExecution.journeyVersionID AS JourneyVersionID, 
   _experience.customerJourneyManagement.messageExecution.journeyActionID AS JourneyActionID, 
   _experience.customerJourneyManagement.emailChannelContext.address AS BccEmailAddress,
   timestamp AS EventTime, 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddress, 
   _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus AS FeedbackStatus,
   CASE _experience.customerjourneymanagement.messagedeliveryfeedback.feedbackStatus
               WHEN 'sent' THEN 'Sent'
               WHEN 'delay' THEN 'Retry'
               WHEN 'out_of_band' THEN 'Bounce' 
               WHEN 'bounce' THEN 'Bounce'
           END AS FeedbackStatusCategory 
   FROM ajo_bcc_feedback_event_dataset  
   WHERE  
   timestamp > now() - INTERVAL '2' day  AND
   _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   _experience.customerJourneyManagement.messageExecution.journeyActionID = '<journeyaction id>' AND 
   _experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = '<recipient email address>'
   ORDER BY EventTime DESC;
   ```

1. Exécutez cette requête pour récupérer toutes les adresses des destinataires qui n&#39;ont pas reçu le message alors que son entrée en Cci existe au cours des 30 derniers jours :

   ```
    SELECT
        DISTINCT 
    bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress AS RecipientAddressesNotRecievedMessage
    FROM ajo_bcc_feedback_event_dataset bcc
    LEFT JOIN cjm_message_feedback_event_dataset mfe
    ON 
   bcc._experience.customerJourneyManagement.messageExecution.journeyVersionID =
            mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID AND    bcc._experience.customerJourneyManagement.messageExecution.journeyActionID = mfe._experience.customerJourneyManagement.messageExecution.journeyActionID AND 
   bcc._experience.customerJourneyManagement.secondaryRecipientDetail.originalRecipientAddress = mfe._experience.customerJourneyManagement.emailChannelContext.address AND
   mfe._experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journey version id>' AND 
   mfe._experience.customerJourneyManagement.messageExecution.journeyActionID = '<journey action id>' AND
   mfe.timestamp > now() - INTERVAL '30' DAY AND
   mfe._experience.customerjourneymanagement.messagedeliveryfeedback.feedbackstatus IN ('bounce', 'out_of_band') 
    WHERE bcc.timestamp > now() - INTERVAL '30' DAY;
   ```
