---
title: Gérer l’exclusion
description: Découvrez comment gérer l’exclusion et la confidentialité
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# Gérer l’exclusion {#consent}

![](assets/do-not-localize/badge.png)

Utilisez [!DNL Journey Optimizer] pour suivre le consentement de vos destinataires à la communication et comprendre comment ils veulent interagir avec votre marque en gérant leurs préférences et leurs abonnements. <!--Their preferences and subscriptions are handled through Consent management.-->

Des règlements tels que le RGPD stipulent que vous devez respecter des exigences spécifiques avant de pouvoir utiliser les informations provenant de sujets de données. En outre, les sujets de données devraient pouvoir modifier leur consentement à tout moment.

**Pourquoi est-ce important ?**

* Ne pas se conformer à ces règlements introduit des risques juridiques réglementaires pour votre marque.
* Il vous aide à éviter d&#39;envoyer des communications non sollicitées à vos destinataires, ce qui pourrait les faire marquer vos messages comme du spam et nuire à votre réputation.

Pour en savoir plus sur la gestion de la confidentialité et les réglementations applicables, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=en).

<!--* Recipients should be able to opt-in/opt-out from receiving electronic communication through one or more channel
* Recipients expect the brand to offer preference centre capability that controls how brand should engage with them (example: channel of communication, invasive and non-invasive tracking etc). This helps to fulfil regulatory obligations and also facilitates quality engagement with recipient. 
* The third category is the capability to offer subscription to recipients (newsletter, etc)-->

## Gestion des exclusions {#opt-out-management}

La possibilité pour les destinataires de se désabonner de la réception des communications d&#39;une marque est une exigence légale. Pour en savoir plus sur la législation applicable, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=en#regulations).

Par conséquent, vous devez toujours inclure un **lien de désabonnement** dans chaque courrier électronique envoyé aux destinataires :
* Lorsque vous cliquez sur ce lien, les destinataires sont dirigés vers un landing page contenant un bouton pour confirmer leur désinscription.
* Lorsque vous cliquez sur le bouton d’exclusion, un appel d’Adobe I/O est lancé pour mettre à jour les données du profil avec ces informations. [En savoir plus à ce sujet](#consent-service-api).

Pour ajouter un lien de désabonnement, procédez comme suit :

1. Construisez votre landing page de désinscription.
1. Hébergez votre landing page sur le système tiers de votre choix.
1. [Créez un ](../../help/using/create-message.md) message dans  [!DNL Journey Optimizer].

   <!--The link to your landing page should contain a static URL and the profile ID.-->

1. Sélectionnez du texte dans votre contenu et insérez un lien à l’aide de la barre d’outils contextuelle.

   ![](assets/opt-out-insert-link.png)

1. Sélectionnez **[!UICONTROL Lien de Désinscription]** dans la liste déroulante **[!UICONTROL Type de lien]**.

   ![](assets/opt-out-link-type.png)

1. Dans le cadre **[!UICONTROL URL de la page de Désinscription]**, copiez le lien vers votre landing page.

   ![](assets/opt-out-link-url.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

1. Enregistrez votre contenu et [publiez votre message](../../help/using/publish-manage-message.md).

   >[!NOTE]
   >
   >L&#39;URL de votre landing page tiers inclut trois paramètres qui seront utilisés pour mettre à jour les préférences des profils par le biais d&#39;un appel d&#39;Adobe I/O. &#x200B; [En savoir plus sur cette section](#consent-service-api).

1. Envoyez votre message avec le lien vers votre landing page via un [parcours](building-journeys/journey.md).

1. Une fois le message reçu, si le destinataire clique sur le lien de désabonnement, votre landing page s’affiche.

   ![](assets/opt-out-lp-example.png)

1. Si le destinataire clique sur le bouton d’exclusion dans le landing page (ici, le bouton **Se désabonner**), les données du profil sont mises à jour par le biais d’un appel d’Adobe I/O [](#opt-out-api).

   Le destinataire désabonné est ensuite redirigé vers un écran de message de confirmation indiquant que l’exclusion a réussi.

   ![](assets/opt-out-confirmation-example.png)

   Par conséquent, cet utilisateur ne recevra aucune communication de votre marque à moins d&#39;être de nouveau abonné.

Pour vérifier que le choix du profil correspondant a été mis à jour, accédez à l&#39;Experience Platform et accédez au profil en sélectionnant un espace de nommage d&#39;identité et une valeur d&#39;identité correspondante. Pour en savoir plus, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=en#getting-started).

![](assets/opt-out-profile-choice.png)

Dans l&#39;onglet **[!UICONTROL Attributes]**, vous pouvez voir la valeur de **[!UICONTROL choice]** remplacée par **[!UICONTROL no]**.

<!--The opt-out URL is resolved upon each recipient receiving the message. It is then personalized with the relevant encrypted parameters (profile ID, profile name, journey ID, sandbox ID, and message execution ID).-->

## Appel d&#39;API d&#39;exclusion {#opt-out-api}

Une fois que le destinataire s’est désabonné en cliquant sur le lien de désabonnement, une API d’Adobe I/O <!--Consent service API to capture the encrypted data and-->est appelée pour mettre à jour la préférence de profil correspondante.

Cet appel POST Adobe I/O est le suivant :

Point de terminaison : cjm.adobe.io/imp/consent/preferences

Paramètres de requête :
* **params** : contient la charge utile chiffrée
* **sig** : signature  <!--which signature?-->
* **pid** : ID de profil chiffré

Ces paramètres sont disponibles à partir du lien de désabonnement envoyé à votre destinataire, c’est-à-dire l’URL qui ouvrira votre landing page tiers pour un destinataire donné :

![](assets/opt-out-parameters.png)

<!--QUESTION: How do you get the URL built for each recipient? Do you have to wait until each targeted recipient receives the unsubscribe link or can you deduce it in advance? Is it done automatically upon the API call or do you have to do something manually for each profile? In other words will the LP automatically include the 3 parameters or do you have to insert something manually? Still not completely clear-->

Exigences d’en-tête :
* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* autorisation (jeton utilisateur de votre compte technique) <!--How do you find this information? And other header elements?-->

Corps de la demande :

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

<!--The Consent service /-->Adobe Customer Management will <!--decrypt and-->use these parameters to update the corresponding profile's choice. <!--and provide an answer back to the landing page.-->

## Gestion des exclusions push {#push-opt-out-management}

Les destinataires Push peuvent se désabonner eux-mêmes via leurs appareils.

Par exemple, lors du téléchargement ou de l’utilisation de votre application, ils peuvent choisir d’arrêter les notifications. De même, ils peuvent modifier les paramètres de notification par le biais du système d’exploitation mobile.
