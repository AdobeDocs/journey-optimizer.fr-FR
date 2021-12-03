---
title: Cas pratiques de landing page
description: Découvrez les cas d’utilisation les plus courants avec les landing pages dans Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 27%

---

# Cas pratiques de landing page

Vous trouverez ci-dessous des exemples d’utilisation de [!DNL Journey Optimizer] landing pages pour que vos clients s’abonnent/se désabonnent de la réception de certaines ou de toutes vos communications.

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## Abonnement à un service {#subscription-to-a-service}

Les principales étapes pour que vos destinataires s&#39;abonnent à un service sont présentées ci-dessous.

![](../assets/lp_subscription-uc.png)

Supposons, par exemple, que vous organisiez un événement le mois prochain et que vous souhaitiez lancer une campagne d’enregistrement d’événement afin que vos clients intéressés soient mis à jour sur cet événement.

1. Créez la liste d’abonnements de l’enregistrement d’événement. En savoir plus sur [listes d’abonnements](subscription-list.md)

1. [Créer une landing page](create-lp.md), qui permettra à vos destinataires de s&#39;inscrire à votre événement.

1. Configurez et concevez la landing page d&#39;inscription, y compris le lien vers la liste d&#39;inscription. En savoir plus sur la création de la variable [Principale landing page](create-lp.md#configure-primary-page)

1. Créez une page de remerciement qui s&#39;affichera à vos destinataires une fois le formulaire d&#39;inscription envoyé. En savoir plus sur [landing sous-pages](create-lp.md#configure-subpages)

1. Créer un message e-mail. En savoir plus sur [création de messages](../create-message.md)

1. [Insérer un lien](../message-tracking.md#insert-links) dans votre message. Sélectionner **[!UICONTROL Landing page]** comme la propriété **[!UICONTROL Type de lien]** et sélectionnez la variable [landing page](create-lp.md#configure-primary-page) que vous avez créé pour enregistrement.

   ![](../assets/lp_subscription-uc-link.png)

1. Enregistrez votre contenu et [publiez votre message](../publish-manage-message.md).

1. Envoyer votre message par le biais d’un [parcours](../building-journeys/journey.md) pour annoncer que l’enregistrement est maintenant ouvert pour votre événement et pour diriger le trafic vers la page d’entrée de l’enregistrement.

   Une fois qu&#39;ils auront reçu l&#39;email, si vos destinataires cliquent sur le lien vers la landing page, ils seront redirigés vers la page de remerciement et ils seront ajoutés à la liste d&#39;inscription.

1. Vous pouvez envoyer un email de confirmation aux destinataires qui se sont inscrits à votre événement. Pour ce faire, envoyez-le via un autre parcours à l’aide de la fonction **[!UICONTROL Qualification du segment]** et sélectionnez la liste d’abonnements que vous avez créée comme segment.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Exclusion {#opt-out}

Pour permettre aux destinataires de se désabonner de vos communications, vous pouvez inclure dans vos emails un lien vers une landing page d&#39;opt-out.

En savoir plus sur la gestion du consentement de vos destinataires et pourquoi cela est important dans [cette section](../consent.md).

### Gestion du droit d&#39;opposition {#opt-out-management}

La possibilité pour les destinataires de se désabonner de la réception des communications d&#39;une marque est une exigence légale. Pour en savoir plus sur la législation applicable, consultez la [documentation d’Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=fr#regulations){target=&quot;_blank&quot;}.

Par conséquent, vous devez toujours inclure un **lien de désabonnement** dans chaque e-mail envoyé aux destinataires :

* Lorsqu&#39;ils cliquent sur ce lien, les destinataires sont dirigés vers une page de destination contenant un bouton pour confirmer leur désinscription.
* Lorsque vous cliquez sur le bouton d’exclusion, les données de profil sont mises à jour avec ces informations.

### Configuration du droit d’opposition {#configure-opt-out}

Pour permettre aux destinataires d&#39;un message de se désabonner de vos communications par le biais d&#39;une landing page, procédez comme suit.

1. Créez votre [landing page](create-lp.md). Utilisation spécifique à la landing page **[!UICONTROL Formulaire]** composant, définir une **[!UICONTROL Exclusion]** et choisissez de mettre à jour **[!UICONTROL Canal (email)]**: le profil qui coche la zone d’exclusion sur votre page d’entrée sera exclu de toutes vos communications. [En savoir plus](design-lp.md)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. [Créez un message](../create-message.md) dans [!DNL Journey Optimizer].

1. Sélectionnez du texte dans votre contenu et [insérer un lien](../message-tracking.md#insert-links) à l’aide de la barre d’outils contextuelle. Vous pouvez également utiliser un lien sur un bouton.

   ![](../assets/lp_opt-out-insert-link.png)

1. Sélectionner **[!UICONTROL Landing page]** de la **[!UICONTROL Type de lien]** liste déroulante.

1. Sélectionnez la [landing page](create-lp.md#configure-primary-page) que vous avez créé pour vous exclure.

   ![](../assets/lp_opt-out-landing-page.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

1. Enregistrez votre contenu et [publiez votre message](../publish-manage-message.md).

1. Envoyer votre message par le biais d’un [parcours](../building-journeys/journey.md).

1. Une fois le message reçu, si le destinataire clique sur le lien de désabonnement, votre page de destination s’affiche.

   <!--![](../assets/lp_opt-out-lp-example.png)-->

1. Si le destinataire clique sur le lien de désinscription dans la landing page, les données de profil sont mises à jour et ne recevront pas les communications de votre marque, sauf si vous vous êtes de nouveau abonné.

   <!--The opted-out recipient is then redirected to a confirmation message screen indicating that opting out was successful.-->

   <!--![](../assets/lp_opt-out-confirmation-example.png)-->

Pour vérifier que le choix du profil correspondant a été mis à jour, accédez à Experience Platform et accédez au profil en sélectionnant un espace de noms d&#39;identité et une valeur d&#39;identité correspondante. Pour en savoir plus, consultez la [documentation d’Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=fr#getting-started){target=&quot;_blank&quot;}.

![](../assets/lp_opt-out-profile-choice.png)

Dans l&#39;onglet **[!UICONTROL Attributs]**, vous pouvez voir la valeur de **[!UICONTROL choice]** remplacée par **[!UICONTROL no]**.

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../message-tracking.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../consent.md#unsubscribe-email)
-->