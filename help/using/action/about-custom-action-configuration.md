---
solution: Journey Orchestration
title: À propos de la configuration des actions personnalisées
description: Découvrez comment configurer une action personnalisée
feature: Actions
topic: Administration
role: Admin
level: Intermediate
source-git-commit: e6d8d8ee637008a886ca308b5b0d9d53d90b11ce
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 100%

---

# Configurer une action {#configure-an-action}

Si vous utilisez un système tiers pour envoyer des messages ou souhaitez que les parcours envoient des appels d&#39;API à un système tiers, c&#39;est à cet emplacement que vous configurez la connexion de ce système aux parcours. L&#39;action personnalisée définie par les utilisateurs techniques sera alors disponible dans la palette gauche du parcours, dans la catégorie **[!UICONTROL Action]** (voir [cette page](../building-journeys/about-journey-activities.md#action-activities). À titre d&#39;exemple, Epsilon, Facebook, Adobe.io, Firebase, etc. sont des systèmes auxquels vous pouvez vous connecter à l&#39;aide d&#39;actions personnalisées.
Les limites sont répertoriées dans [cette page](../building-journeys/limitations.md).

Les principales étapes nécessaires pour configurer une action personnalisée sont les suivantes :

1. Dans la section du menu ADMINISTRATION, sélectionnez **[!UICONTROL Configurations]**. Dans la section **[!UICONTROL Actions]**, cliquez sur **[!UICONTROL Gérer]**. Cliquez sur **[!UICONTROL Créer une action]** pour créer une nouvelle action. Le volet de configuration des actions s&#39;ouvre dans la droite de l&#39;écran.

   ![](../assets/custom2.png)

1. Saisissez le nom de l&#39;action.

   >[!NOTE]
   >
   >N&#39;utilisez ni espaces ni caractères spéciaux. Utilisez 30 caractères au maximum.

1. Ajoutez une description à l&#39;action. Cette étape est facultative.
1. Le nombre de parcours qui font appel à cette action apparaît dans le champ **[!UICONTROL Utilisé(e) dans]**. Vous pouvez cliquer sur le bouton **[!UICONTROL Afficher les parcours]** pour faire apparaître la liste des parcours utilisant cette action.
1. Définissez les différents paramètres de **[!UICONTROL Configuration d&#39;URL]**. Voir [cette page](../action/about-custom-action-configuration.md#url-configuration).
1. Configurez la section **[!UICONTROL Authentification]**. Cette configuration est la même que pour les sources de données.  Consultez [cette section](../datasource/external-data-sources.md#section_wjp_nl5_nhb).
1. Définissez les **[!UICONTROL paramètres d&#39;action]**. Voir [cette page](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Cliquez sur **[!UICONTROL Enregistrer]**.

   L&#39;action personnalisée est maintenant configurée et prête à être utilisée dans vos parcours. Voir [cette page](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Lorsqu&#39;une action personnalisée est utilisée dans un parcours, la plupart des paramètres sont en lecture seule. Vous ne pouvez modifier que les champs **[!UICONTROL Nom]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** et la section **[!UICONTROL Authentification.]**

## Configuration d&#39;URL {#url-configuration}

Lors de la configuration d&#39;une action personnalisée, vous devez définir les paramètres de **[!UICONTROL configuration d&#39;URL]** suivants :

![](../assets/journeyurlconfiguration.png)

1. Ajoutez l&#39;**[!UICONTROL URL]** du service externe.

   >[!NOTE]
   >
   >Nous vous recommandons vivement d&#39;utiliser le protocole HTTPS pour des raisons de sécurité. L&#39;utilisation des adresses Adobe qui ne sont pas publiques et des adresses IP n&#39;est pas autorisée.

1. Sélectionnez la **[!UICONTROL Méthode]** d&#39;appel : il peut s&#39;agir de **[!UICONTROL POST]** ou de **[!UICONTROL PUT]**.
1. Dans la section **[!UICONTROL En-têtes]**, cliquez sur **[!UICONTROL Ajouter un champ d&#39;en-tête]** pour définir une nouvelle paire clé/valeur. Ces en-têtes correspondent aux en-têtes HTTP de la requête adressée au service externe. Pour supprimer des paires clé/valeur, placez le curseur sur le champ En-tête, puis cliquez sur l&#39;icône **[!UICONTROL Supprimer]**.

   Les en-têtes **[!UICONTROL Content-Type]** et **[!UICONTROL Charset]** sont définis par défaut et ne peuvent pas être supprimés ni remplacés.

   >[!NOTE]
   >
   >Les en-têtes sont validés conformément à ces [règles d&#39;analyse](https://tools.ietf.org/html/rfc7230#section-3.2.4).

## Définition des paramètres d’action {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

Dans la section **[!UICONTROL Paramètres d&#39;action]**, collez un exemple de payload JSON à envoyer au service externe.

![](../assets/customactionpayloadmessage.png)

>[!NOTE]
>
>Les noms de champ de la payload ne peuvent pas contenir de caractère &quot;.&quot; . Ils ne peuvent pas commencer par le caractère &quot;$&quot;.

Vous aurez la possibilité de définir le type de paramètre (par exemple : string, integer, etc.).

Vous pourrez également préciser si le paramètre est une constante ou une variable :

* Le paramètre « Constante » signifie que la valeur du paramètre est définie dans le volet de configuration des actions par une personne ayant un rôle technique. La valeur reste identique dans tous les parcours et le marketeur ne la voit pas lors de l&#39;utilisation de l&#39;action personnalisée dans le parcours. Il peut s&#39;agir, par exemple, d&#39;un identifiant attendu par le système tiers. Dans ce cas, le champ situé à droite du bouton bascule Constante/Variable correspond à la valeur transmise.
* Le paramètre « Variable » signifie que la valeur du paramètre varie. Le marketeur qui utilise cette action personnalisée dans un parcours peut transmettre la valeur de son choix ou bien indiquer où récupérer la valeur de ce paramètre (à partir de l&#39;événement, d‘Adobe Experience Platform, etc.). Dans ce cas, le champ situé à droite du bouton bascule Constante/Variable correspond au libellé que le marketeur voit dans le parcours pour nommer ce paramètre.

![](../assets/customactionpayloadmessage2.png)
