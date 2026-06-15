---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le canal LINE
description: Découvrez comment configurer votre environnement pour envoyer des messages LINE avec Journey Optimizer.
feature: Line, Channel Configuration
role: Admin
level: Intermediate
exl-id: 8ad0e57b-6bdc-43b0-9511-31e2ac1be1f9
TQID: https://experienceleague.adobe.com/yDRCVzfdPGXisgxJ59UT8HYsdXI82H07Ol--YP7wmE0
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: e09fc1e6-407c-418f-adc5-e2ffe8b8986eid: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 1356417d30312b74500dc930c92fe70e0d050a46
workflow-type: tm+mt
source-wordcount: 508
ht-degree: 71%

---

# Configurer le canal LINE dans Journey Optimizer {#line-configuration}

>[!BEGINSHADEBOX]

**Sur cette page :** configurez un canal LINE à partir de l&#39;interface ou de l&#39;API afin que Adobe Journey Optimizer puisse s&#39;authentifier auprès de l&#39;API de messagerie LINE et envoyer des messages à vos clients.

>[!ENDSHADEBOX]

1. Accédez au menu **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres généraux]** > **[!UICONTROL Configurations des canaux]**, puis cliquez sur **[!UICONTROL Créer une configuration des canaux]**.

   ![](assets/line-config-1.png)

1. Saisissez un nom et une description (facultatif) pour la configuration, puis sélectionnez le canal à configurer.

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à la configuration, vous pouvez sélectionner **[!UICONTROL Gérer l’accès]**. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../administration/object-based-access.md).

1. Sélectionnez le canal **LINE**.

   ![](assets/line-config-2.png)

1. Sélectionnez une **[!UICONTROL Action marketing]** ou plusieurs pour associer des politiques de consentement aux messages utilisant cette configuration. Toutes les politiques de consentement associées à cette action marketing sont utilisées afin de respecter les préférences de vos clientes et clients. [En savoir plus](../action/consent.md#surface-marketing-actions)

1. Sélectionnez le type de message pour la configuration :

   * **Marketing** : pour les messages promotionnels, tels que les promotions hebdomadaires d’un magasin de vente au détail. Ces messages nécessitent le consentement des destinataires et doivent être conformes à la politique de LINE concernant les opt-ins des utilisateurs et utilisatrices.
   * **Transactionnel** : pour les messages non commerciaux tels que la confirmation de commande, les notifications de réinitialisation de mot de passe ou les informations de diffusion, par exemple. Ces messages peuvent être envoyés même aux personnes qui se sont désabonnées des communications marketing, mais sont strictement limités à des contextes transactionnels spécifiques.

1. Sélectionnez les **[!UICONTROL paramètres du canal]**.

   Contactez votre représentant ou représentante Adobe pour configurer les **[!UICONTROL paramètres du canal]**.

   ![](assets/line-config-2.png)

1. Sélectionnez l’**[!UICONTROL ID de l’utilisateur ou l’utilisatrice LINE]** que vous souhaitez mapper. Il s’agit de l’identifiant utilisé pour lier les messages à chaque utilisateur et utilisatrice de votre canal LINE.

   >[!NOTE]
   >
   >L’identifiant utilisateur LINE que vous mappez ici doit déjà exister sur le [!DNL Real-Time Customer Profile] de vos clients. Capturez l’ID utilisateur LINE (par exemple, via la connexion LINE ou le SDK LIFF), ingérez-le dans Adobe Experience Platform et associez-le à un identifiant connu avec Identity Service afin que [!DNL Journey Optimizer] puissiez atteindre le profil unifié. [En savoir plus sur les identités dans Journey Optimizer](../audience/get-started-identity.md).
   >
   >Pour un exemple complet d’unification des ID utilisateur LINE avec des profils client à l’aide d’Identity Service, consultez l’article de la communauté [Unification des ID utilisateur LINE avec des profils client à l’aide de l’assemblage d’identités AEP](https://experienceleaguecommunities.adobe.com/adobe-journey-optimizer-15/unifying-line-user-ids-with-customer-profiles-in-adobe-journey-optimizer-using-aep-identity-stitching-248680){target="_blank"}.

1. Saisissez votre **[!UICONTROL nom d’expéditeur]**, tel que le nom de votre marque.

1. Soumettez vos modifications.

Vous pouvez maintenant sélectionner votre configuration lors de la création du message LINE.

## Configurer l’API des paramètres du canal LINE {#line-api}

Cette API configure les paramètres de canal qui stockent les détails d’autorisation et de configuration nécessaires pour la connexion à l’API LINE Messaging. Ces paramètres permettent à Adobe Journey Optimizer de s’authentifier et d’envoyer des messages via LINE à l’aide des informations d’identification fournies.

**Point d’entrée**

```
POST https://platform.adobe.io/journey/imp/config/channel-settings
```

| Nom de l’en-tête | Description |
|-|-|
| Autorisation | Jeton de l’utilisateur ou l’utilisatrice de votre compte technique |
| x-api-key | ID du client à partir d’Adobe Developer Console |
| x-gw-ims-org-id | Votre ID d’organisation IMS |
| x-sandbox-name | Nom du sandbox, par exemple prod |
| Content-Type | Doit être application/json. |


**Corps de la requête**

```json
{
    "name": "your_defined_name",
    "channelRegistryId": "line",
    "channel": "line",
    "channelSettings": {
        "channelId": "your_line_channel_id",
        "channelSecret": "your_line_channel_secret"
    }
}
```

**Réponse des paramètres de canal**

```json
{
"id": "3603ed66-ae86-42b8-8a90-d4b4e54e7c3b",
"name": "your_defined_name",
"channelRegistryId": "line",
"channel": "line",
"channelSettings": {
    "channelId": "your_line_channel_id",
    "channelSecret": "your_line_channel_secret"
    },
    "channelPublicationId": "v1_line",
    "createdAt": "2025-07-30T12:00:00.000Z",
    "modifiedAt": "2025-07-30T12:00:00.000Z",
    "isFromLatestVersion": true,
    "_etag": "\"eab98d24-18af-48ae-90f9-e59d4f8cfb2b\""
}
```
