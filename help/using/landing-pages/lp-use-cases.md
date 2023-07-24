---
solution: Journey Optimizer
product: journey optimizer
title: Cas d’utilisation de pages de destination
description: Découvrez les cas d’utilisation les plus courants en rapport avec les pages de destination dans Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
keywords: destination, page de destination, cas d’utilisation
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: ht
source-wordcount: '968'
ht-degree: 100%

---

# Cas d’utilisation de pages de destination {#lp-use-cases}

Retrouvez ci-dessous quelques exemples sur la façon dont vous pouvez utiliser les pages de destination de [!DNL Journey Optimizer] afin que vos clients puissent sʼinscrire/se désinscrire de lʼenvoi de certaines ou de toutes vos communications.

## Abonnement à un service {#subscription-to-a-service}

L’un des cas d’utilisation les plus courants consiste à inviter vos clients à [sʼabonner à un service](subscription-list.md) (comme une newsletter ou un événement) par le biais dʼune page de destination. Retrouvez les étapes principales dans le graphique ci-dessous :

![](assets/lp_subscription-uc.png)

Supposons, par exemple, que vous organisiez un événement le mois prochain et que vous souhaitiez lancer une campagne d’inscription à cet événement<!--to keep your customers that are interested updated on that event-->. Pour ce faire, vous allez envoyer un e-mail qui contient un lien vers une page de destination sur laquelle vos destinataires pourront sʼinscrire à cet événement. Les utilisateurs qui s’inscrivent seront ajoutés à la liste d’abonnements que vous avez créée à cet effet.

### Configurer une page de destination {#set-up-lp}

1. Créez la liste d’abonnements relative aux inscriptions à l’événement, qui stockera les utilisateurs inscrits. Découvrez comment créer une liste d’abonnements [ici](subscription-list.md#define-subscription-list).

   ![](assets/lp_subscription-uc-list.png)

1. [Créez une page de destination](create-lp.md) pour permettre aux destinataires de sʼinscrire à votre événement.

   ![](assets/lp_create-lp-details.png)

1. Configurez la [page principale de la page de destination](create-lp.md#configure-primary-page).

1. Lors de la conception du [contenu de la page de destination](design-lp.md), sélectionnez la liste dʼabonnements créée pour la mettre à jour avec les profils ayant coché la case dʼinscription.

   ![](assets/lp_subscription-uc-lp-list.png)

1. Créez une page de remerciement qui sʼaffichera pour vos destinataires une fois le formulaire dʼinscription envoyé. Découvrez comment configurer des sous-pages de page de destination [ici](create-lp.md#configure-subpages).

   ![](assets/lp_subscription-uc-thanks.png)

1. [Publier](create-lp.md#publish) la page de destination.

1. Dans un [parcours](../building-journeys/journey.md), ajoutez une activité **E-mail** pour diriger le trafic vers la page de destination d’inscription.

   ![](assets/lp_subscription-uc-journey.png)

1. [Concevez un e-mail](../email/get-started-email-design.md) pour annoncer que l’inscription à lʼévénement a débuté.

1. [Insérez un lien](../email/message-tracking.md#insert-links) dans le contenu de votre message. Sélectionnez **[!UICONTROL Page de destination]** en tant que **[!UICONTROL Type de lien]** et sélectionnez la [Page de destination](create-lp.md#configure-primary-page) que vous avez créée pour lʼinscription.

   ![](assets/lp_subscription-uc-link.png)

   >[!NOTE]
   >
   >Pour pouvoir envoyer votre message, vérifiez que la page de destination sélectionnée n’a pas encore expiré. Découvrez comment mettre à jour la date d’expiration [dans cette section](create-lp.md#configure-primary-page).

   Une fois que vos destinataires ont reçu lʼe-mail, sʼils cliquent sur le lien vers la page de destination, ils seront redirigés vers la page de remerciement et seront ajoutés à la liste dʼabonnements.

### Envoi d’un e-mail de confirmation {#send-confirmation-email}

Vous pouvez également envoyer un e-mail de confirmation aux destinataires qui se sont inscrits à votre événement. Procédez comme suit.

1. Créez un autre [parcours](../building-journeys/journey.md). Vous pouvez le faire directement à partir de la page de destination en cliquant sur le bouton **[!UICONTROL Créer un parcours]**. [En savoir plus](create-lp.md#configure-primary-page).

   ![](assets/lp_subscription-uc-create-journey.png)

1. Développez la catégorie **[!UICONTROL Événements]** et déposez une activité de **[!UICONTROL qualification d’audience]** dans la zone de travail. [En savoir plus](../building-journeys/audience-qualification-events.md).

1. Cliquez dans le champ **[!UICONTROL Audience]** et sélectionnez la liste d’abonnements que vous avez créée.

   ![](assets/lp_subscription-uc-confirm-journey.png)

1. Ajoutez lʼe-mail de confirmation de votre choix et envoyez-le par le biais du parcours.

   ![](assets/lp_subscription-uc-confirm-email.png)

Tous les utilisateurs inscrits à votre événement recevront l’e-mail de confirmation.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Désinscription {#opt-out}

Pour permettre aux destinataires dʼannuler lʼabonnement à vos communications, vous pouvez inclure un lien vers une page de destination d&#39;opt-out dans vos e-mails.

En savoir plus sur la gestion du consentement de vos destinataires et son caractère important dans [cette section](../privacy/opt-out.md).

### Gestion du droit d&#39;opposition {#opt-out-management}

La possibilité pour les destinataires de se désabonner de la réception des communications d’une marque est une exigence légale. Pour en savoir plus sur la législation applicable, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=fr#regulations){target="_blank"}.

Par conséquent, vous devez toujours inclure un **lien de désabonnement** dans chaque e-mail envoyé aux destinataires :

* Lorsqu&#39;ils cliquent sur ce lien, les destinataires sont dirigés vers une page de destination contenant un bouton pour confirmer leur désinscription.
* Lorsque le destinataire clique sur le bouton d&#39;opt-out, les données de son profil sont mises à jour avec ces informations.

### Configuration du droit d&#39;opt-out {#configure-opt-out}

Pour permettre aux destinataires dʼun e-mail dʼannuler leur abonnement à vos communications par le biais dʼune page de destination, procédez comme suit.

1. Créez votre page de destination. [En savoir plus](create-lp.md)

1. Définissez la page principale. [En savoir plus](create-lp.md#configure-primary-page)

1. [Configurez](design-lp.md) le contenu de la page principale. Pour ce faire, utilisez le composant **[!UICONTROL Formulaire]**, spécialement conçu pour la page de destination, définissez une case à cocher **[!UICONTROL Opt-out]** et choisissez de mettre à jour le **[!UICONTROL Canal (e-mail)]** : le profil qui active la case d&#39;opt-out sur votre page de destination sera désinscrit de toutes vos communications.

   ![](assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice.-->

1. Ajoutez une [sous-page](create-lp.md#configure-subpages) de confirmation qui s’affichera pour les utilisateurs qui soumettent le formulaire.

   ![](assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >Veillez à référencer la sous-page dans la section **[!UICONTROL Appel à l’action]** de la page principale du composant **[!UICONTROL Formulaire]**. [En savoir plus](design-lp.md)

1. Une fois que vous avez configuré et défini le contenu de vos pages, [publiez](create-lp.md#publish) la page de destination.

1. [Créez un e-mail](../email/get-started-email-design.md) dans un parcours.

1. Sélectionnez du texte dans votre contenu et [insérez un lien](../email/message-tracking.md#insert-links) à l’aide de la barre d’outils contextuelle. Vous pouvez également employer un lien sur un bouton.

1. Sélectionnez **[!UICONTROL Page de destination]** dans la liste déroulante **[!UICONTROL Type de lien]**, puis sélectionnez la [page de destination](create-lp.md#configure-primary-page) que vous avez créée pour le désabonnement.

   ![](assets/lp_opt-out-landing-page.png)

   >[!NOTE]
   >
   >Pour pouvoir envoyer votre message, vérifiez que la page de destination sélectionnée n’a pas encore expiré. Découvrez comment mettre à jour la date d’expiration [dans cette section](create-lp.md#configure-primary-page).

1. Publiez et exécutez le parcours. [En savoir plus](../building-journeys/journey.md).

1. Une fois le message reçu, si le destinataire clique sur le lien de désabonnement présent dans lʼe-mail, votre page de destination s’affiche.

   ![](assets/lp_opt-out-submit-form.png)

   Si le destinataire coche la case et soumet le formulaire :

   * Le destinataire qui sʼest désabonné est redirigé vers lʼécran du message de confirmation.

   * Les données de son profil sont mises à jour et il ne recevra plus de communications de votre marque, sauf sʼil sʼabonne à nouveau.

Pour vérifier que le choix du profil correspondant a été mis à jour, accédez à Experience Platform puis au profil en sélectionnant un espace de noms d’identité et une valeur d’identité correspondante. Pour en savoir plus, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=fr#getting-started){target="_blank"}.

![](assets/lp_opt-out-profile-choice.png)

Dans l’onglet **[!UICONTROL Attributs]**, la valeur du **[!UICONTROL choix]** a été remplacée par **[!UICONTROL non]**.

Les informations concernant les désinscriptions sont stockées dans le **Jeu de données du service de consentement**. [En savoir plus sur les jeux de données](../data/get-started-datasets.md)

>[!NOTE]
>
>Si la méthode de fusion pour votre [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target="_blank"} **[!UICONTROL Profiles]** merge policy is **[!UICONTROL Dataset Precedence]**, make sure to enable the **[!UICONTROL AJO Consent Service Dataset]** and to prioritize it in the merge policy. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr#dataset-precedence-profile){target="_blank"} par défaut
>
>Même si aucun lot n’a été ajouté à ce jeu de données, il contiendra toujours les informations opt-in et opt-out.


<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../privacy/opt-out.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../privacy/opt-out.md#unsubscribe-header)

////////


## Leverage landing page submission event {#leverage-lp-event}

You can use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.

To do this, you need to create an event containing the landing page submission information and use it in a journey. Follow the steps below.

1. Go to **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**, and in the **[!UICONTROL Events]** section, select **[!UICONTROL Manage]**.

    ![](assets/lp_subscription-uc-configurations.png)

1. The list of events displays. Select **[!UICONTROL Create Event]**.

    ![](assets/lp_subscription-uc-create-event.png)

1. The event configuration pane opens on the right side of the screen. Configure a rule-based unitary event. [Learn more](../event/about-creating.md)

1. Define the schema: select **[!UICONTROL AJO Email Tracking Experience Event Schema v.1]** (available by default in [!DNL Journey Optimizer]).

    ![](assets/lp_subscription-uc-event-schema.png)

1. In the **[!UICONTROL Fields]** section, select the following elements:

    * **[!UICONTROL _experience]** > **[!UICONTROL customerJourneyManagement]** > **[!UICONTROL messageInteraction]** > **[!UICONTROL Interaction Type]**
    
    * **[!UICONTROL _experience]** > **[!UICONTROL customerJourneyManagement]** > **[!UICONTROL messageInteraction]** > **[!UICONTROL Landing Page Details]** > **[!UICONTROL Landing Page ID]**

    ![](assets/lp_subscription-uc-event-fields.png)

1. Click inside the **[!UICONTROL Event ID condition]** field. Using the simple expression editor, define the condition for the **[!UICONTROL Interaction Type]** and **[!UICONTROL Landing Page ID]** fields. This will be used by the system to identify the events that will trigger your journey.

    ![](assets/lp_subscription-uc-event-id-condition.png)

    >[!NOTE]
    >
    >To find the landing page ID, you can insert the landing page as a link into an email and select the source code from the contextual toolbar to display the landing page information.
    >
    >![](assets/lp_subscription-uc-lp-id.png)

1. Save your changes.

1. Create a [journey](../building-journeys/journey.md). You can do it directly from the landing page by clicking the **[!UICONTROL Create journey]** button. Learn more [here](create-lp.md#configure-primary-page)

    ![](assets/lp_subscription-uc-event-create-journey.png)

1. In the journey, unfold the **[!UICONTROL Events]** category and drop the event that you created into the canvas. Learn more [here](../building-journeys/audience-qualification-events.md)

    ![](assets/lp_subscription-uc-journey-event.png)

1. Unfold the **[!UICONTROL Actions]** category and drop an email action into the canvas.

    ![](assets/lp_subscription-uc-journey-email.png)

///How do you use the information from the event to send an email to the users? -->
