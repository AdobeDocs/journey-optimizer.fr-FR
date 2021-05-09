---
solution: Journey Orchestration
title: A propos de la configuration des actions personnalisées
description: Découvrez comment configurer une action personnalisée
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# Configurer une action {#configure-an-action}

![](../assets/do-not-localize/badge.png)

Si vous utilisez un système tiers pour envoyer des messages ou si vous souhaitez que les parcours envoient des appels d&#39;API à un système tiers, vous devez configurer sa connexion aux parcours. L&#39;action personnalisée définie par les utilisateurs techniques sera alors disponible dans la palette de gauche de votre parcours, dans la catégorie **[!UICONTROL Action]** (voir [cette page](../building-journeys/about-journey-activities.md#action-activities). Voici quelques exemples de systèmes auxquels vous pouvez vous connecter avec des actions personnalisées : Epsilon, Facebook, Adobe.io, Firebase, etc.
Les limites sont répertoriées dans [cette page](../building-journeys/limitations.md).

Voici les étapes principales requises pour configurer une action personnalisée :

1. Dans la liste **[!UICONTROL Actions]**, cliquez sur **[!UICONTROL Ajouter]** pour créer une nouvelle action. Le volet de configuration de l&#39;action s&#39;ouvre sur le côté droit de l&#39;écran.

   ![](../assets/custom2.png)

1. Entrez le nom de votre action.

   >[!NOTE]
   >
   >N’utilisez pas d’espaces ni de caractères spéciaux. N’utilisez pas plus de 30 caractères.

1. Ajoutez une description de votre action. Cette étape est facultative.
1. Le nombre de parcours qui utilisent cette action est affiché dans le champ **[!UICONTROL Utilisé dans]**. Vous pouvez cliquer sur le bouton **[!UICONTROL parcours de Vue]** pour afficher la liste des parcours à l’aide de cette action.
1. Définissez les différents paramètres **[!UICONTROL Configuration de l&#39;URL]**. Voir [cette page](../action/about-custom-action-configuration.md#url-configuration).
1. Configurez la section **[!UICONTROL Authentification]**. Cette configuration est identique à celle des sources de données.  Voir [cette section](../datasource/external-data-sources.md#section_wjp_nl5_nhb).
1. Définissez les **[!UICONTROL paramètres de message]**. Voir [cette page](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Cliquez sur **[!UICONTROL Enregistrer]**.

   L’action personnalisée est maintenant configurée et prête à être utilisée dans vos parcours. Voir [cette page](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Lorsqu’une action personnalisée est utilisée dans un parcours, la plupart des paramètres sont en lecture seule. Vous pouvez uniquement modifier les champs **[!UICONTROL Nom]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** et la section **[!UICONTROL Authentification]**.

## Configuration de l&#39;URL {#url-configuration}

Lors de la configuration d’une action personnalisée, vous devez définir les paramètres **[!UICONTROL de configuration d’URL]** suivants :

![](../assets/journeyurlconfiguration.png)

1. Ajoutez l&#39;**[!UICONTROL URL]** du service externe.

   >[!NOTE]
   >
   >Pour des raisons de sécurité, nous vous recommandons vivement d’utiliser HTTPS. Nous n&#39;autorisons pas l&#39;utilisation d&#39;adresses d&#39;Adobe qui ne sont pas publiques et l&#39;utilisation d&#39;adresses IP.

1. Sélectionnez l&#39;appel **[!UICONTROL Méthode]** : il peut s’agir de **[!UICONTROL POST]** ou **[!UICONTROL PUT]**.
1. Dans la section **[!UICONTROL En-têtes]**, cliquez sur **[!UICONTROL Ajouter un champ d&#39;en-tête]** pour définir une nouvelle paire clé/valeur. Ils correspondent aux en-têtes HTTP de la demande envoyée au service externe. Pour supprimer des paires clé/valeur, placez le curseur sur le champ **[!UICONTROL En-têtes]** et cliquez sur l&#39;icône **[!UICONTROL Supprimer]**.

   **[!UICONTROL Par défaut, les paramètres]** Type de contenu et  **** Charsetare sont définis et ne peuvent pas être supprimés ou remplacés.

   >[!NOTE]
   >
   >Les en-têtes sont validés conformément aux [règles d’analyse](https://tools.ietf.org/html/rfc7230#section-3.2.4) suivantes.

## Définir les paramètres de message {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

Dans la section **[!UICONTROL Paramètres de message]**, collez un exemple de charge utile JSON à envoyer au service externe.

![](../assets/customactionpayloadmessage.png)

Vous pourrez définir le type de paramètre (par exemple : string, integer, etc.).

Vous aurez également le choix entre indiquer si un paramètre est une constante ou une variable :

* Constante signifie que la valeur du paramètre est définie dans le volet de configuration de l’action par une personne technique. La valeur sera toujours la même d’un parcours à l’autre. Il ne varie pas et le spécialiste du marketing ne le voit pas lors de l’utilisation de l’action personnalisée dans le parcours. Il peut s’agir, par exemple, d’un identifiant auquel le système tiers s’attend. Dans ce cas, le champ à droite de la constante/variable de basculement est la valeur transmise.
* Variable signifie que la valeur du paramètre varie. Le spécialiste du marketing qui utilise cette action personnalisée dans un parcours sera libre de transmettre la valeur qu’il souhaite ou de spécifier où récupérer la valeur de ce paramètre (par exemple, à partir du événement, du Adobe Experience Platform, etc.). Dans ce cas, le champ à droite de la constante/variable de basculement est l’étiquette que le spécialiste du marketing verra dans le parcours pour nommer ce paramètre.

![](../assets/customactionpayloadmessage2.png)
