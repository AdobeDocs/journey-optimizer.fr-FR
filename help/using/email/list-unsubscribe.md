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
source-git-commit: b3655506dff97756a59a63d5b8f0c358dc7c7510
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 100%

---

# Désabonnement de la liste{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->

Lors de la configuration d’une nouvelle configuration de canal e-mail, au moment de la [sélection d’un sous-domaine](email-settings.md#subdomains-and-ip-pools) dans la liste, l’option **[!UICONTROL Activer List-Unsubscribe]** s’affiche.

![](assets/preset-list-unsubscribe.png)

## Activer le désabonnement de la liste {#enable-list-unsubscribe}

Cette option est activée par défaut pour inclure une URL de désabonnement en un clic dans l’en-tête de l’e-mail, par exemple :

![](assets/preset-list-unsubscribe-header.png)

>[!NOTE]
>
>Si vous désactivez cette option, aucune URL de désabonnement en un clic ne s’affiche dans l’en-tête de l’e-mail.

L’en-tête Désabonnement de la liste propose deux fonctionnalités qui sont activées par défaut, sauf si vous désélectionnez l’une des fonctionnalités ou les deux :

![](assets/surface-list-unsubscribe.png){width="80%"}

* Une adresse **[!UICONTROL Mailto (annuler l’abonnement)]**, qui est l’adresse de destination vers laquelle les demandes de désabonnement sont acheminées pour le traitement automatique.

  Dans [!DNL Journey Optimizer], l’adresse e-mail de désabonnement est l’adresse par défaut **[!UICONTROL Mailto (annuler l’abonnement)]** affichée dans la configuration des canaux, en fonction du [sous-domaine sélectionné](#subdomains-and-ip-pools).<!--With this method, clicking the Unsubscribe link sends a pre-filled email to the unsubscribe address specified in the email header.-->

* L’**[!UICONTROL URL de désabonnement en un clic]**, qui est par défaut l’URL d’opt-out en un clic générée par l’en-tête de désabonnement de la liste en fonction du sous-domaine que vous avez défini et dont la configuration est effectuée dans les paramètres de configuration des canaux.<!--With this method, clicking the Unsubscribe link directly unsubscribes the user, requiring only a single action to unsubscribe.-->

Vous pouvez sélectionner le **[!UICONTROL niveau de consentement]** dans la liste déroulante correspondante. Il peut être spécifique au canal ou à l’identité du profil. En fonction de ce paramètre, lorsqu’un utilisateur ou une utilisatrice se désabonne à l’aide de l’URL de désabonnement de la liste dans l’en-tête d’un e-mail, le consentement est mis à jour dans [!DNL Adobe Journey Optimizer] au niveau du canal ou de l’ID.

Les fonctionnalités **[!UICONTROL Mailto (se désabonner)]** et **[!UICONTROL URL de désabonnement en un clic]** sont facultatives.

Si vous ne souhaitez pas utiliser l’URL de désabonnement en un clic générée par défaut, vous pouvez décocher la fonction. Dans le scénario dans lequel l’option **[!UICONTROL Activer le désabonnement de la liste]** est activée et où la fonctionnalité **[!UICONTROL URL de désabonnement en un clic]** n’est pas cochée, si vous ajoutez un [lien d’exclusion en un clic](../email/email-opt-out.md#one-click-opt-out) dans un message créé à l’aide de cette configuration, l’en-tête de désabonnement de la liste récupère le lien d’exclusion en un clic que vous avez inséré dans le corps de l’e-mail et l’utilise comme valeur de l’URL de désabonnement en un clic.

![](assets/preset-list-unsubscribe-opt-out-url.png)

>[!NOTE]
>
>Si vous n’ajoutez pas de lien d’exclusion en un clic au contenu de votre message et que l’**[!UICONTROL URL de désabonnement en un clic]** par défaut est décochée dans les paramètres de configuration des canaux, aucune URL n’est transmise à l’en-tête de l’e-mail dans le cadre de l’en-tête de désabonnement de la liste.

Pour plus d’informations sur la gestion des fonctionnalités de désabonnement dans vos messages, consultez [cette section](../email/email-opt-out.md#unsubscribe-header).

## Gérer les données de désabonnement en externe {#custom-managed}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="Définir la manière de gérer les données de désabonnement"
>abstract="**Géré par Adobe** : les données de consentement sont gérées par vous dans le système Adobe.<br>**Géré par le client ou la cliente** : les données de consentement sont gérées par vous dans un système externe et aucune synchronisation des données de consentement n’est mise à jour dans le système Adobe, sauf si vous en êtes à l’origine."

Si vous gérez le consentement en dehors d’Adobe, sélectionnez l’option **[!UICONTROL Géré par le client ou la cliente]** pour saisir une adresse e-mail de désabonnement personnalisée et votre propre URL de désabonnement en un clic.

![](assets/surface-list-unsubscribe-custom.png){width="80%"}

>[!WARNING]
>
>Si vous utilisez l’option **[!UICONTROL Géré par le client ou la cliente]**, Adobe ne stocke aucune donnée de désabonnement ou de consentement. Avec l’option **[!UICONTROL Géré par le client ou la cliente]**, les organisations choisissent d’utiliser un système externe et seront chargées de gérer leurs données de consentement dans celui-ci. Il n’existe pas de synchronisation automatique des données de consentement entre le système externe et [!DNL Journey Optimizer]. Toute synchronisation des données de consentement, qui provient du système externe pour mettre à jour les données de consentement d’utilisation dans [!DNL Journey Optimizer], doit être lancée par l’organisation sous la forme d’un transfert de données pour renvoyer les données de consentement vers [!DNL Journey Optimizer].

### Configurer l’API de déchiffrement {#configure-decrypt-api}

Lorsque l’option **[!UICONTROL Géré par le client ou la cliente]** est sélectionnée, si vous saisissez des points d’entrée personnalisés et les utilisez dans une campagne ou un parcours, [!DNL Journey Optimizer] ajoute certains paramètres spécifiques au profil par défaut à l’événement de mise à jour du consentement <!--sent to the custom endpoint -->lorsque vos destinataires cliquent sur le lien de désabonnement.

Ces paramètres sont envoyés au point d’entrée de manière chiffrée. Par conséquent, le système de consentement externe doit mettre en œuvre une API spécifique via [Adobe Developer](https://developer.adobe.com){target="_blank"} pour déchiffrer les paramètres envoyés par Adobe.

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

+++
