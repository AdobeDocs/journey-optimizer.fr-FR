---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le désabonnement de la liste
description: Découvrez comment inclure une URL de désabonnement en un clic dans l’en-tête des e-mails lors de la configuration des canaux.
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: paramètres, e-mail, configuration
exl-id: c6c77975-ec9c-44c8-a8d8-50ca6231fea6
source-git-commit: d77c6376bee14d3d6f90be9be54ac01c740e754f
workflow-type: tm+mt
source-wordcount: '1704'
ht-degree: 98%

---

# Désabonnement de la liste{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->

Lorsque vous définissez une nouvelle configuration des canaux dans [!DNL Adobe Journey Optimizer], au moment de la [sélection d’un sous-domaine](email-settings.md#ip-pools) dans la liste, l’option **[!UICONTROL Activer le désabonnement de la liste]** s’affiche. Elle est activée par défaut.

![](assets/preset-list-unsubscribe.png)

Une URL de désabonnement de liste en un clic est un lien ou un bouton de désabonnement affiché à côté des informations sur l’expéditeur ou l’expéditrice de l’e-mail. Elle permet aux destinataires de se désinscrire instantanément de vos listes de publipostage en un seul clic.

Par exemple, l’URL de désabonnement en un clic affiche un lien de désabonnement comme celui-ci dans Gmail :

![](assets/preset-list-unsubscribe-header.png)

>[!IMPORTANT]
>
>Pour afficher l’URL de désabonnement en un clic dans l’en-tête de l’e-mail, le client de messagerie de la personne destinataire doit prendre en charge cette fonctionnalité.

Selon le client de messagerie e-mail et les paramètres de désabonnement de la configuration du canal e-mail, cliquer sur le lien de désabonnement dans l’en-tête de l’e-mail entraîne différents résultats :

* Lorsque la fonctionnalité **Mailto (se désabonner)** est activée, la demande de désabonnement est envoyée à l’adresse de désabonnement par défaut en fonction du sous-domaine que vous avez configuré.
* Lorsque la fonctionnalité **URL de désabonnement en un clic** est activée (ou si vous avez inséré une URL de désabonnement dans le contenu de votre corps d’e-mail), la personne destinataire est directement désinscrite, au niveau du canal ou au niveau de l’ID (selon la configuration du consentement), lorsqu’elle clique sur l’URL de désabonnement en un clic (selon le sous-domaine que vous avez configuré).

>[!NOTE]
>
>Découvrez comment gérer les paramètres de désabonnement dans [cette section](#enable-list-unsubscribe) ci-dessous.

Dans les deux cas, lorsqu’une personne destinataire clique sur le lien de désinscription, sa demande de désabonnement est traitée en conséquence. Le profil correspondant est immédiatement exclu et ce choix est mis à jour dans [Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=fr){target="_blank"}. En savoir plus sur le traitement du consentement dans la documentation d’[Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/consent/adobe/overview.html?lang=fr){target="_blank"}.

>[!NOTE]
>
>Parfois, la prise en compte des événements de désabonnement au niveau du profil peut prendre plus de temps en raison du traitement des données en aval. Attendez que le système procède à la mise à jour.

## Activer le désabonnement de la liste {#enable-list-unsubscribe}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Ajouter une URL de désabonnement à vos e-mails"
>abstract="Activez cette option pour ajouter automatiquement une URL de désabonnement dans l’en-tête de l’e-mail. Pour définir une URL de désabonnement dans un message, insérez un lien d’exclusion en un clic dans le contenu de l’e-mail."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/channels/email/email-opt-out#one-click-opt-out" text="Définir le désabonnement (opt-out) en un clic dans le contenu de l’e-mail"

Lorsque l’option **[!UICONTROL Activer le désabonnement de la liste]** est activée, si elle est prise en charge par le client de messagerie e-mail des destinataires, l’en-tête de l’e-mail comprend à la fois un lien mailto et/ou une URL par défaut que les destinataires peuvent utiliser pour se désabonner de votre liste de publipostage.

>[!NOTE]
>
>Si vous désactivez cette option, aucune URL de désabonnement en un clic ne s’affiche dans l’en-tête de l’e-mail.

L’en-tête Désabonnement de la liste propose deux fonctionnalités qui sont activées par défaut, sauf si vous désélectionnez l’une des fonctionnalités ou les deux :

![](assets/surface-list-unsubscribe.png){width="80%"}

* Un lien **[!UICONTROL Mailto (désabonnement)]**, qui correspond à l’adresse de destination où les demandes de désabonnement sont automatiquement traitées. Dans [!DNL Journey Optimizer], l’adresse e-mail de désabonnement est le lien **[!UICONTROL Mailto (désabonnement)]** par défaut affiché dans la configuration des canaux, en fonction du [sous-domaine sélectionné](email-settings.md#subdomains). <!--With this method, clicking the Unsubscribe link sends a pre-filled email to the unsubscribe address specified in the email header.-->

* L’**[!UICONTROL URL de désabonnement en un clic]**, qui est par défaut l’en-tête de désabonnement (opt-out) de la liste généré par l’URL de désinscription en un clic, en fonction du [sous-domaine sélectionné](email-settings.md#subdomains). <!--With this method, clicking the Unsubscribe link directly unsubscribes the user, requiring only a single action to unsubscribe.-->

Vous pouvez sélectionner le **[!UICONTROL niveau de consentement]** dans la liste déroulante correspondante. Il peut être spécifique au canal ou à l’identité du profil. En fonction de ce paramètre, lorsqu’un utilisateur ou une utilisatrice se désabonne à l’aide de l’URL de désabonnement de la liste dans l’en-tête d’un e-mail, le consentement est mis à jour dans [!DNL Adobe Journey Optimizer] au niveau du canal ou de l’ID.

## Mécanismes de sécurisation et recommandations {#list-unsubscribe-guardrails}

La fonctionnalité d’URL de désabonnement de liste en un clic permet à vos destinataires de se désinscrire facilement de vos communications. Cependant, comme tous les clients de messagerie e-mail ne prennent pas en charge ce lien dans l’en-tête de l’e-mail, Adobe vous recommande d’ajouter un [lien de désinscription (opt-out) en un clic](email-opt-out.md#one-click-opt-out) ou un [lien de désabonnement](email-opt-out.md#add-unsubscribe-link) dans le corps de l’e-mail.

Les fonctionnalités **[!UICONTROL Mailto (désabonnement)]** et **[!UICONTROL URL de désabonnement en un clic]** sont facultatives.

* Si vous avez activé l’option **[!UICONTROL Activer List-Unsubscribe]** dans les [paramètres de configuration du canal e-mail](email-settings.md), nous vous recommandons d’activer les deux méthodes : **Mailto (se désabonner)** et **URL de désabonnement en un clic**. Les clients de messagerie ne prennent pas tous en charge la méthode HTTP. La fonctionnalité de désabonnement de liste Mailto vous permet de sélectionner une alternative. Vous protégez ainsi mieux votre réputation d’expédition et l’ensemble de vos destinataires peuvent avoir accès à la fonctionnalité de désabonnement.

* Si vous ne souhaitez pas utiliser l’URL de désabonnement en un clic générée par défaut, vous pouvez décocher la fonctionnalité.

   * Dans le scénario dans lequel l’option **[!UICONTROL Activer le désabonnement de la liste]** est activée et où la fonctionnalité **[!UICONTROL URL de désabonnement en un clic]** n’est pas cochée, si vous ajoutez un [lien d’exclusion (opt-out) en un clic](../email/email-opt-out.md#one-click-opt-out) dans un message créé à l’aide de cette configuration, l’en-tête de désabonnement de la liste récupère le lien d’exclusion (opt-out) en un clic que vous avez inséré dans le corps de l’e-mail et l’utilise comme valeur de l’URL de désabonnement en un clic.

     ![](assets/preset-list-unsubscribe-opt-out-url.png)

   * Si vous n’ajoutez pas de lien d’exclusion en un clic au contenu de votre message et que l’**[!UICONTROL URL de désabonnement en un clic]** par défaut est décochée dans les paramètres de configuration des canaux, aucune URL n’est transmise à l’en-tête de l’e-mail dans le cadre de l’en-tête de désabonnement de la liste.

  >[!NOTE]
  >
  >Pour plus d’informations sur la gestion des fonctionnalités de désabonnement dans vos messages, consultez [cette section](../email/email-opt-out.md#unsubscribe-header).

Dans [!DNL Journey Optimizer], le consentement est géré par le [Schéma de consentement](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=fr){target="_blank"} d’Experience Platform. Par défaut, la valeur du champ de consentement est vide et traitée comme un consentement pour recevoir vos communications. Vous pouvez remplacer cette valeur par défaut lors de l’intégration par l’une des valeurs possibles répertoriées [ici](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=fr#choice-values){target="_blank"} ou utiliser des [politiques de consentement](../action/consent.md) pour remplacer la logique par défaut.

Actuellement, [!DNL Journey Optimizer] n’ajoute pas de balise spécifique aux événements de désabonnement déclenchés par la fonctionnalité Désabonnement des listes. Pour distinguer les clics de désabonnement de la liste des autres actions de désabonnement, vous devez implémenter le balisage personnalisé en externe ou utiliser une page de destination externe pour le suivi.

## Gérer les données de désabonnement en externe {#custom-managed}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="Définir la manière de gérer les données de désabonnement"
>abstract="**Géré par Adobe** : les données de consentement sont gérées par vous dans le système Adobe.<br>**Géré par le client ou la cliente** : les données de consentement sont gérées par vous dans un système externe et aucune synchronisation des données de consentement n’est mise à jour dans le système Adobe, sauf si vous en êtes à l’origine."

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom_url"
>title="Saisir votre propre URL de désabonnement en un clic"
>abstract="L’**URL de désabonnement en un clic** doit utiliser la méthode de requête POST."

Si vous gérez le consentement en dehors d’Adobe, sélectionnez l’option **[!UICONTROL Géré par le client ou la cliente]** pour saisir une adresse e-mail de désabonnement personnalisée et votre propre URL de désabonnement en un clic.

![](assets/surface-list-unsubscribe-custom.png){width="80%"}

L’**[!UICONTROL URL de désabonnement en un clic]** doit être une URL POST.

>[!WARNING]
>
>Si vous utilisez l’option **[!UICONTROL Géré par le client ou la cliente]**, Adobe ne stocke aucune donnée de désabonnement ou de consentement. Avec l’option **[!UICONTROL Géré par le client ou la cliente]**, les organisations choisissent d’utiliser un système externe et seront chargées de gérer leurs données de consentement dans celui-ci. Il n’existe pas de synchronisation automatique des données de consentement entre le système externe et [!DNL Journey Optimizer]. Toute synchronisation des données de consentement, qui provient du système externe pour mettre à jour les données de consentement d’utilisation dans [!DNL Journey Optimizer], doit être lancée par l’organisation sous la forme d’un transfert de données pour renvoyer les données de consentement vers [!DNL Journey Optimizer].

### Ajouter des attributs personnalisés à vos points d’entrée {#custom-attributes}

Lorsque l’option **[!UICONTROL Géré par le client ou la cliente]** est sélectionnée, si vous saisissez des points d’entrée personnalisés et que vous les utilisez dans une campagne ou un parcours, [!DNL Journey Optimizer] ajoute des paramètres spécifiques au profil par défaut à l’événement de mise à jour du consentement <!--sent to the custom endpoint -->lorsque vos destinataires cliquent sur le lien de désabonnement.

Pour personnaliser davantage vos points d’entrée <!-- (**[!UICONTROL Mailto (unsubscribe)]** and **[!UICONTROL One-click Unsubscribe URL]**)-->, vous pouvez désormais définir des attributs personnalisés qui seront également ajoutés à l’événement de consentement.

>[!AVAILABILITY]
>
>Pour l’option **[!UICONTROL Mailto (désabonnement)]**, cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès. Dans ce cas, vous devez utiliser les nouveaux paramètres de requête décrits dans la section **Mailto (désabonnement) avec des attributs personnalisés (disponibilité limitée)** [ci-dessous](#configure-decrypt-api).

Pour définir des attributs personnalisés pour vos points d’entrée, utilisez la section **[!UICONTROL Paramètres de suivi des URL]**. Tous les paramètres de suivi des URL que vous définissez dans la section correspondante seront ajoutés à la fin de vos points d’entrée personnalisés, en plus des paramètres par défaut. [Découvrez comment configurer le tracking personnalisé des URL](url-tracking.md).

### Configurer l’API de déchiffrement {#configure-decrypt-api}

Lorsque les personnes destinataires cliquent sur un lien de désabonnement personnalisé, les paramètres ajoutés à l’événement de mise à jour du consentement sont envoyés au point d’entrée de manière chiffrée. Par conséquent, le système de consentement externe doit mettre en œuvre une API spécifique via [Adobe Developer](https://developer.adobe.com){target="_blank"} pour déchiffrer les paramètres envoyés par Adobe.

L’appel GET pour récupérer ces paramètres dépend de l’option de désabonnement de la liste que vous utilisez : **[!UICONTROL URL de désabonnement en un clic]** ou **[!UICONTROL Mailto (annuler l’abonnement)]**.

<!--To configure the API to send back the information to [!DNL Adobe Journey Optimizer] when a recipient has unsubscribed using the List unsubscribe option with custom endpoints, follow the steps below.-->

+++ URL de désabonnement en un clic

Avec l’option **[!UICONTROL URL de désabonnement en un clic]**, cliquer sur le lien de désabonnement annule directement l’abonnement de l’utilisateur ou de l’utilisatrice.

L’appel GET se présente comme suit :

Point d’entrée : https://platform.adobe.io/journey/imp/consent/decrypt

Paramètres de requête :

* **params** : contient la payload chiffrée
* **pid** : identifiant de profil chiffré

Ces deux paramètres seront inclus dans l’événement de mise à jour du consentement envoyé aux points d’entrée personnalisés.

Exigences d’en-tête :

* x-api-key
* x-gw-ims-org-id
* autorisation (jeton utilisateur de votre compte technique)

Vous trouverez ci-dessous des exemples de paramètres et la réponse de consentement :

| Paramètre de requête | Exemple de payload |
|---------|----------|
| pid | {<br>&quot;pid&quot;  : &quot;5142733041546020095851529937068211571&quot;,<br>&quot;pns&quot;  : &quot;CRMID&quot;,<br>&quot;e&quot;    : &quot;john@google.com&quot;,<br>&quot;ens&quot;  : &quot;Email&quot;,<br>} |
| Paramètres | {<br>&quot;m&quot;  : &quot;messageExecutionId&quot;,<br>&quot;ci&quot;  : &quot;campaignId&quot;,<br>&quot;jv&quot; : &quot;journeyVersionId&quot;,<br>&quot;ja&quot; : &quot;journeyActionId&quot;,<br>&quot;s&quot;  : &quot;sandboxId&quot;,<br>&quot;us&quot; : &quot;unsubscribeScope&quot;<br>} |

Réponse de consentement :

```
{
    "profileNameSpace": " CRMID ",
    "profileId": "5142733041546020095851529937068211571",
    "emailAddress": "john@google.com",
    "emailNameSpace": "Email",
    "sandboxId": "sandboxId",
    "optOutLevel": "channel",
    "channelType": "email",
    "timestamp": "2024-11-26T14:25:09.316930Z"
    "utm": [
         {
            "utm_source": "AJO",
            "utm_medium": "Email"
        }
    ]
}
```

+++

+++ Mailto (se désabonner)

Avec l’option **[!UICONTROL Mailto (se désabonner)]**, cliquer sur le lien de désabonnement envoie un e-mail prérempli à l’adresse de désabonnement spécifiée.

L’appel GET se présente comme suit :

Point d’entrée : https://platform.adobe.io/journey/imp/consent/decrypt

Paramètres de requête :

* **emailParams** : chaîne contenant les paramètres **params** (payload chiffrée) et **pid** (identifiant de profil chiffré).

Les paramètres **params** et **pid** seront inclus dans l’événement de mise à jour du consentement envoyé aux points d’entrée personnalisés.

Exigences d’en-tête :

* x-api-key
* x-gw-ims-org-id
* autorisation (jeton utilisateur de votre compte technique)

Vous trouverez ci-dessous des exemples de paramètres et la réponse de consentement :

| Paramètre de requête | Exemple de payload |
|---------|----------|
| Paramètres d’e-mail | {<br>&quot;p&quot;  : &quot;profileId&quot;,<br>&quot;pn&quot;  : &quot;profileNamespace&quot;,<br>&quot;en&quot;  : &quot;emailNamespace&quot;,<br>&quot;ci&quot;  : &quot;campaignId&quot;,<br>&quot;jv&quot; : &quot;journeyVersionId&quot;,<br>&quot;ja&quot; : &quot;journeyActionId&quot;,<br>&quot;si&quot;  : &quot;sandboxId&quot;,<br>&quot;us&quot;: &quot;unsubscribeScope&quot;<br>} |

Réponse de consentement :

```
{
    "profileNameSpace": " CRMID ",
    "profileId": "5142733041546020095851529937068211571",
    "emailAddress": "john@google.com",
    "emailNameSpace": "Email",
    "sandboxId": "sandboxId",
    "optOutLevel": "channel",
    "channelType": "email",
    "timestamp": "2024-11-26T14:25:09.316930Z"
}
```

+++

+++ Mailto (désabonnement) avec des attributs personnalisés (disponibilité limitée)

Avec l’option **[!UICONTROL Mailto (désabonnement)]**, cliquer sur le lien de désabonnement envoie un e-mail prérempli à l’adresse de désabonnement spécifiée.

À partir d’octobre 2025, si vous utilisez l’option **[!UICONTROL Gestion par le client]** pour le point d’entrée **[!UICONTROL Mailto (désabonnement)]**, vous pouvez définir des attributs personnalisés qui seront ajoutés à l’événement de consentement. Dans ce cas, vous devez utiliser les paramètres de requête décrits ci-dessous.

>[!AVAILABILITY]
>
>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

L’appel GET se présente comme suit :

Point d’entrée : https://platform.adobe.io/journey/imp/consent/decrypt

Paramètres de requête :

* **emailParamsSub** : chaîne extraite de l’objet de l’e-mail reçu à l’adresse Mailto.

   * Exemple : *unsubscribev1.abc*

   * Valeur analysée : *v1.abc*

* **emailParamsBody** : chaîne extraite du corps de l’e-mail (le cas échéant) au format *unsubscribev1.xyz*.

   * Valeur analysée : *v1.xyz*

Exemple d’API : https://platform.adobe.io/journey/imp/consent/decrypt?emailParamsSub=v1.abc&emailParamsBody=v1.xyz

>[!CAUTION]
>
>Si vous utilisiez la mise en œuvre précédente (par exemple : https://platform.adobe.io/journey/imp/consent/decrypt?emailParams=&lt;v1.xxx>), vous devez utiliser les nouveaux paramètres **emailParamsSub** et **emailParamsBody** au lieu de **emailParams**. Contactez votre représentant ou représentante Adobe pour plus d’informations.

Les paramètres **emailParamsSub** et **emailParamsBody** seront inclus dans l’événement de mise à jour du consentement envoyé aux points d’entrée personnalisés.

Exigences d’en-tête :

* x-api-key
* x-gw-ims-org-id
* autorisation (jeton utilisateur de votre compte technique)

Réponse de consentement :

```
{
    "profileNameSpace": " CRMID ",
    "profileId": "5142733041546020095851529937068211571",
    "emailAddress": "john@google.com",
    "emailNameSpace": "Email",
    "sandboxId": "sandboxId",
    "optOutLevel": "channel",
    "channelType": "email",
    "timestamp": "2024-11-26T14:25:09.316930Z"
    "utm": [
        {
            "utm_source": "AJO",
            "utm_medium": "Email"
        }
    ]
}
```

+++
