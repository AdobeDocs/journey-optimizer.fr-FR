---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des opt-out des emails
description: Découvrez comment gérer l’exclusion avec les emails
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# Gestion des opt-out des emails {#email-opt-out}

Afin de permettre aux destinataires de se désabonner de la réception des communications par e-mail, vous devez toujours inclure une **lien de désabonnement** dans chaque email envoyé aux destinataires. [En savoir plus sur la gestion de la confidentialité et de l’exclusion](../privacy/opt-out.md)

Pour cela, vous pouvez :

* Insérer une **lien vers une landing page externe** dans un email afin de permettre aux utilisateurs de se désabonner de la réception des communications de votre marque. [Découvrez comment ajouter un lien d’exclusion externe](#opt-out-external-lp)

* Ajouter un **lien d’exclusion en un clic** dans le contenu de votre email. Ce lien permettra à vos destinataires de se désabonner rapidement de vos communications, sans être redirigés vers une landing page dans laquelle ils devront confirmer leur choix, ce qui accélère le processus de désabonnement. [Découvrez comment ajouter un lien d’exclusion en un clic](#one-click-opt-out)

En outre, si la variable **[!UICONTROL List-Unsubscribe]** est activée au niveau de la surface du canal, les courriers électroniques correspondants envoyés avec Journey Optimizer incluront un lien de désabonnement dans l’en-tête de l’email. [En savoir plus sur l’exclusion dans l’en-tête de l’email](#unsubscribe-header)

>[!NOTE]
>
>Les messages électroniques de type marketing doivent inclure un lien d’exclusion, qui n’est pas obligatoire pour les messages transactionnels. La catégorie du message (**[!UICONTROL Marketing]** ou **[!UICONTROL Transactional]**) est défini au niveau de la variable [surface du canal](../configuration/channel-surfaces.md#email-type) niveau (c’est-à-dire le paramètre prédéfini du message) et lors de la création du message.

## Désinscription externe {#opt-out-external-lp}

### Ajout d’un lien de désabonnement {#add-unsubscribe-link}

Vous devez d’abord ajouter un lien de désabonnement dans un message. Pour ce faire, procédez comme suit :

1. Créez votre propre landing page de désinscription.

1. Hébergez-le sur le système tiers de votre choix.

1. Créez un message dans un parcours.

1. Sélectionnez du texte dans votre contenu et [insérer un lien](../email/message-tracking.md#insert-links) à l’aide de la barre d’outils contextuelle.

   ![](assets/opt-out-insert-link.png)

1. Sélectionner **[!UICONTROL External Opt-out/Unsubscription]** de la **[!UICONTROL Link type]** liste déroulante.

   ![](assets/opt-out-link-type.png)

1. Dans le **[!UICONTROL Link]** collez le lien vers votre page d’entrée tierce.

   ![](assets/opt-out-link-url.png)

1. Cliquez sur **[!UICONTROL Save]**.

### Mise en oeuvre d’un appel API pour l’exclusion {#opt-out-api}

Pour que vos destinataires soient désinscrits lorsqu’ils envoient leur choix à partir de la page d’entrée, vous devez mettre en oeuvre une **Appel de l’API d’abonnement** through [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;} pour mettre à jour les préférences des profils correspondants.

Cet appel POST est le suivant :

Point d’entrée : platform.adobe.io/journey/imp/consent/preferences

Paramètres de requête :

* **params**: contient la charge utile chiffrée ;
* **sig**: signature
* **pid**: identifiant de profil crypté

Ces trois paramètres seront inclus dans l’URL de page d’entrée tierce envoyée à votre destinataire :

![](assets/opt-out-parameters.png)

Exigences d’en-tête :

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* autorisation (jeton utilisateur de votre compte technique)

Corps de la requête :

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

[!DNL Journey Optimizer] utilisera ces paramètres pour mettre à jour le choix du profil correspondant via l’ [Adobe Developer](https://developer.adobe.com)Appel de l’API {target=&quot;_blank&quot;}.

### Envoyer le message avec le lien de désabonnement {#send-message-unsubscribe-link}

Une fois que vous avez configuré le lien de désabonnement sur votre page d’entrée et mis en oeuvre l’appel API , votre message est prêt à être envoyé.

1. Envoyer le message, y compris le lien par le biais d&#39;une [parcours](../building-journeys/journey.md).

1. Une fois le message reçu, si le destinataire clique sur le lien de désabonnement, votre landing page s&#39;affiche.

   ![](assets/opt-out-lp-example.png)

1. Si le destinataire envoie le formulaire (ici, en appuyant sur la fonction **Désabonner** dans votre landing page), les données de profil sont mises à jour via la fonction [appel API](#opt-out-api).

1. Le destinataire qui s&#39;est désinscrit est alors redirigé vers un écran de message de confirmation indiquant que l&#39;opt-out a réussi.

   ![](assets/opt-out-confirmation-example.png)

   Par conséquent, cet utilisateur ne recevra pas de communication de votre marque, sauf s’il s’est de nouveau abonné.

1. Pour vérifier que le choix du profil correspondant a été mis à jour, accédez à Experience Platform et au profil en sélectionnant un espace de noms d’identité et une valeur d’identité correspondante. En savoir plus dans la section [Documentation d’Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

   ![](assets/opt-out-profile-choice.png)

   Dans le **[!UICONTROL Attributes]** vous pouvez voir la valeur de **[!UICONTROL choice]** a été remplacé par **[!UICONTROL no]**.

## Exclusion en un clic {#one-click-opt-out}

Pour ajouter un lien d’exclusion dans votre email, procédez comme suit.

1. [Insérer un lien](../email/message-tracking.md#insert-links) et sélectionnez **[!UICONTROL One click Opt-out]** comme type de lien.

   ![](assets/message-tracking-opt-out.png)

1. Sélectionnez le mode d’application du droit d’opposition : au niveau du canal, de l’identité ou de l’abonnement.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**: L’opt-out s’applique aux prochains messages envoyés à la cible du profil (c’est-à-dire son adresse email) pour le canal actuel. Si plusieurs cibles sont associées à un profil, l&#39;opt-out s&#39;applique à toutes les cibles (adresses email, par exemple) du profil pour ce canal.
   * **[!UICONTROL Identity]**: L’opt-out s’applique aux prochains messages envoyés à la cible spécifique (c’est-à-dire l’adresse email) utilisée pour le message en cours.
   * **[!UICONTROL Subscription]**: L&#39;opt-out s&#39;applique aux futurs messages associés à une liste d&#39;abonnements spécifique. Cette option ne peut être sélectionnée que si le message actif est associé à une liste d&#39;abonnements.

1. Saisissez l&#39;URL de la landing page vers laquelle l&#39;utilisateur sera redirigé une fois désabonné. Cette page n’est disponible que pour confirmer que l’exclusion a réussi.

   >[!NOTE]
   >
   >Si vous avez activé la variable **List-Unsubscribe** au niveau de la surface du canal, cette URL sera également utilisée lorsque les utilisateurs cliqueront sur le lien de désabonnement dans l’en-tête de l’email. [En savoir plus](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Vous pouvez personnaliser vos liens. En savoir plus sur les URL personnalisées dans [cette section](../personalization/personalization-syntax.md).

1. Enregistrez vos modifications.

Une fois que votre message est envoyé via une [parcours](../building-journeys/journey.md), si un destinataire clique sur le lien d’exclusion, son profil est immédiatement désinscrit.

## Lien de désabonnement dans l’en-tête de l’email {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Ajout d’un lien de désabonnement à l’en-tête de courrier électronique"
>abstract="Activez List-Unsubscribe pour ajouter un lien de désabonnement à l’en-tête de l’email. Pour définir une URL de désabonnement, insérez un lien d’exclusion en un clic dans le contenu de l’email."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#one-click-opt-out" text="Exclusion en un clic"

Si la variable [Option List-Unsubscribe](../configuration/channel-surfaces.md#list-unsubscribe) est activé au niveau de la surface du canal, les emails correspondants envoyés avec [!DNL Journey Optimizer] inclut un lien de désabonnement dans l’en-tête de l’email.

Par exemple, le lien de désabonnement s’affiche comme suit dans Gmail :

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>Pour afficher le lien de désabonnement dans l’en-tête de l’email, le client de messagerie du destinataire doit prendre en charge cette fonctionnalité.

L’adresse de désabonnement est la valeur par défaut. **[!UICONTROL Mailto (unsubscribe)]** adresse affichée à la surface du canal correspondant. [En savoir plus](../configuration/channel-surfaces.md#list-unsubscribe).

Pour définir une URL de désabonnement personnalisée, insérez un lien d&#39;opt-out en un clic dans le contenu de l&#39;email et saisissez l&#39;URL de votre choix. [En savoir plus](#one-click-opt-out)

Selon le client de messagerie, cliquer sur le lien de désabonnement de l’en-tête peut avoir les effets suivants :

* La demande de désabonnement est envoyée à l’adresse de désabonnement par défaut.

* Le destinataire est dirigé vers l&#39;URL de la landing page que vous avez spécifiée lors de l&#39;ajout du lien de désinscription à votre message.

   >[!NOTE]
   >
   >Si vous n&#39;ajoutez pas de lien d&#39;opt-out en un clic dans le contenu de votre message, aucune landing page ne s&#39;affichera.

* Le profil correspondant est immédiatement exclu et ce choix est mis à jour dans Experience Platform. En savoir plus dans la section [Documentation d’Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.
