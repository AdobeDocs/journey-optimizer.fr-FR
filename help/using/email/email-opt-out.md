---
solution: Journey Optimizer
product: journey optimizer
title: Gérer le processus d’opt-out aux e-mails
description: Découvrez comment gérer l’exclusion avec les emails
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 87%

---

# Gérer le processus d’opt-out aux e-mails {#email-opt-out}

Afin de permettre aux destinataires de se désabonner de la réception des communications par e-mail, vous devez toujours inclure une **lien de désabonnement** dans chaque email envoyé aux destinataires. [En savoir plus sur la gestion de la confidentialité et de l’exclusion](../privacy/opt-out.md)

Pour cela, vous pouvez :

* Insérer une **lien vers une landing page externe** dans un email afin de permettre aux utilisateurs de se désabonner de la réception des communications de votre marque. [Découvrez comment ajouter un lien d’exclusion externe](#opt-out-external-lp)

* Ajouter un **lien d’exclusion en un clic** dans le contenu de votre email. Ce lien permettra à vos destinataires de se désinscrire rapidement de vos communications, sans être redirigés vers une page de destination dans laquelle ils doivent confirmer leur désinscription. Cela permet d’accélérer le processus de désinscription. [Découvrez comment ajouter un lien d’exclusion en un clic](#one-click-opt-out)

En outre, si la variable **[!UICONTROL List-Unsubscribe]** est activée au niveau de la surface du canal, les emails correspondants envoyés avec Journey Optimizer incluront un lien de désabonnement dans l’en-tête de l’email. [En savoir plus sur l’exclusion dans l’en-tête de l’email](#unsubscribe-header)

>[!NOTE]
>
>Les e-mails de type marketing doivent inclure un lien d’opt-out, qui n’est pas obligatoire pour les messages transactionnels. La catégorie du message (**[!UICONTROL Marketing]** ou **[!UICONTROL Transactionnel]**) est définie au niveau de la [surface de canal](../configuration/channel-surfaces.md#email-type) (c’est-à-dire au niveau du préréglage de message) et lors de la création du message).

## Opt-out externe {#opt-out-external-lp}

### Ajouter un lien de désabonnement {#add-unsubscribe-link}

Vous devez d’abord ajouter un lien de désabonnement dans un message. Pour ce faire, procédez comme suit :

1. Construisez votre page de destination de désinscription.

1. Hébergez-la sur le système tiers de votre choix.

1. Créez un message dans un parcours.

1. Sélectionnez du texte dans votre contenu et [insérez un lien](../email/message-tracking.md#insert-links) à l’aide de la barre d’outils contextuelle.

   ![](assets/opt-out-insert-link.png)

1. Sélectionnez **[!UICONTROL Désinscription/opt-out externe]** à partir de la liste déroulante **[!UICONTROL Type de lien]**.

   ![](assets/opt-out-link-type.png)

1. Dans le champ **[!UICONTROL Lien]**, collez le lien vers votre page de destination tierce.

   ![](assets/opt-out-link-url.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

### Implémenter un appel API pour le processus d’opt-out {#opt-out-api}

Pour que vos destinataires soient désinscrits lorsqu’ils envoient leur choix à partir de la page de destination, vous devez implémenter un **appel API d’abonnement** via [Adobe Developer](https://developer.adobe.com/){target=&quot;_blank&quot;} pour mettre à jour les préférences des profils correspondants.

Cet appel POST est le suivant :

Point dʼentrée : platform.adobe.io/journey/imp/consent/preferences

Paramètres de requête:

* **params** : contient la payload chiffrée
* **sig** : signature
* **pid** : identifiant de profil chiffré

Ces trois paramètres seront inclus dans l’URL de page de destination tierce envoyée à votre destinataire :

![](assets/opt-out-parameters.png)

Exigences d’en-tête :

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* autorisation (jeton utilisateur de votre compte technique)

Contenu de la requête :

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

[!DNL Journey Optimizer] utilisera ces paramètres pour mettre à jour le choix du profil correspondant par le biais de l’appel API [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;}.

### Envoyer le message avec le lien de désinscription {#send-message-unsubscribe-link}

Une fois que vous avez configuré le lien de désinscription sur votre page de destination et implémenté l’appel API, votre message est prêt à être envoyé.

1. Envoyer le message incluant le lien par le biais d’un [parcours](../building-journeys/journey.md).

1. Une fois le message reçu, si le destinataire clique sur le lien de désinscription, votre page de destination s’affiche.

   ![](assets/opt-out-lp-example.png)

1. Si le destinataire envoie le formulaire (ici, en appuyant sur le bouton **Se désinscrire** dans votre page de destination), les données de profil sont mises à jour via l’[appel API](#opt-out-api).

1. Le destinataire désabonné est ensuite redirigé vers un écran de message de confirmation indiquant que la désinscription a réussi.

   ![](assets/opt-out-confirmation-example.png)

   Par conséquent, cet utilisateur ne recevra aucune communication de votre marque à moins d&#39;être de nouveau abonné.

1. Pour vérifier que le choix du profil correspondant a été mis à jour, accédez à Experience Platform puis au profil en sélectionnant un espace de noms d’identité et une valeur d’identité correspondante. Pour en savoir plus, consultez la [documentation d’Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=fr#getting-started){target=&quot;_blank&quot;}.

   ![](assets/opt-out-profile-choice.png)

   Dans l&#39;onglet **[!UICONTROL Attributs]**, vous pouvez voir la valeur de **[!UICONTROL choice]** remplacée par **[!UICONTROL no]**.

## Opt-out en un clic {#one-click-opt-out}

Pour ajouter un lien d&#39;opt-out dans votre e-mail, procédez comme suit.

1. [Insérez un lien](../email/message-tracking.md#insert-links) et sélectionnez **[!UICONTROL Opt-out en un clic]** comme type de lien.

   ![](assets/message-tracking-opt-out.png)

1. Sélectionnez le mode d’application de la désinscription : au niveau du canal, de l’identité ou de l’abonnement.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Canal]** : le processus d’opt-out s’applique aux futurs messages envoyés à la cible du profil (c’est-à-dire son adresse e-mail) pour le canal actuel. Si plusieurs cibles sont associées à un profil, le processus d’opt-out s’applique à toutes les cibles (adresses e-mail, par exemple) du profil pour ce canal.
   * **[!UICONTROL Identité]** : le processus d’opt-out s’applique aux futurs messages envoyés à la cible spécifique (c’est-à-dire l’adresse e-mail) utilisée pour le message en cours.
   * **[!UICONTROL Abonnement]** : le processus d’opt-out s’applique aux futurs messages associés à une liste d’abonnement spécifique. Cette option ne peut être sélectionnée que si le message actif est associé à une liste d’abonnement.

1. Saisissez l’URL de la page de destination vers laquelle l’utilisateur sera redirigé une fois désabonné. Cette page n’est disponible que pour confirmer que la désinscription a réussi.

   >[!NOTE]
   >
   >Si vous avez activé l’option **List-Unsubscribe** au niveau des paramètres des surfaces du canal, cette URL sera également utilisée lorsque les utilisateurs cliqueront sur le lien de désabonnement dans l’en-tête de l’e-mail. [En savoir plus](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Vous pouvez personnaliser vos liens. Pour en savoir plus sur les URL personnalisées, consultez [cette section](../personalization/personalization-syntax.md).

1. Enregistrez vos modifications.

Une fois votre message envoyé via un [parcours](../building-journeys/journey.md), si un destinataire clique sur le lien d&#39;opt-out, il est immédiatement désinscrit.

## Lien de désabonnement dans l’en-tête de l’e-mail {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Ajout d’un lien de désabonnement à l’en-tête d’un e-mail"
>abstract="Activez List-Unsubscribe pour ajouter un lien de désabonnement à l’en-tête de l’e-mail. Pour définir une URL de désabonnement, insérez un lien d’opt-out en un clic dans le contenu de l’e-mail."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=fr#one-click-opt-out" text="Opt-out en un clic"

Si l’[option List-Unsubscribe](../configuration/channel-surfaces.md#list-unsubscribe) est activée au niveau des surfaces du canal, les e-mails correspondants envoyés avec [!DNL Journey Optimizer] incluent un lien de désabonnement dans l’en-tête de l’e-mail.

Par exemple, le lien de désabonnement s&#39;affiche comme suit dans Gmail :

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>Pour afficher le lien de désabonnement dans l’en-tête de l’e-mail, le client de messagerie du destinataire doit prendre en charge cette fonctionnalité.

L’adresse de désabonnement est l’adresse **[!UICONTROL Mailto (unsubscribe)]** par défaut affichée dans la surface de canal correspondante. [En savoir plus](../configuration/channel-surfaces.md#list-unsubscribe).

Pour définir une URL de désabonnement personnalisée, insérez un lien d&#39;opt-out en un clic dans le contenu de l&#39;e-mail et saisissez l&#39;URL de votre choix. [En savoir plus](#one-click-opt-out)

En fonction du client de messagerie, cliquer sur le lien de désabonnement de l&#39;en-tête peut avoie l&#39;un des impacts suivants :

* La demande de désabonnement est envoyée à l’adresse de désabonnement par défaut.

* Le destinataire est dirigé vers l&#39;URL de la page de destination que vous avez spécifiée lors de l&#39;ajout du lien d&#39;opt-out à votre message.

   >[!NOTE]
   >
   >Si vous n&#39;ajoutez pas de lien d&#39;opt-out en un clic dans le contenu de votre message, aucune page de destination ne s&#39;affichera.

* Le profil correspondant est immédiatement exclu et ce choix est mis à jour dans Experience Platform. Pour en savoir plus, consultez la [documentation d’Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.
