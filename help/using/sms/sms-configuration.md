---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le canal SMS
description: Découvrez comment configurer votre environnement pour envoyer des messages texte avec Journey Optimizer.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 4278d8c8294b1413788402cd8eac5959996ad3f5
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 100%

---

# Commencer avec la configuration des SMS/MMS/RCS {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurer votre fournisseur de SMS avec Journey Optimizer"
>abstract="Adobe Journey Optimizer envoie des message SMS par le biais des fournisseurs de SMS. Sélectionnez votre fournisseur et renseignez vos informations d’identification d’API."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Configurer votre fournisseur de SMS avec Journey Optimizer"
>abstract="Adobe Journey Optimizer envoie du contenu média par le biais de fournisseurs de services MMS. Sélectionnez votre fournisseur et renseignez vos informations d’identification d’API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurer votre fournisseur de SMS/MMS avec Journey Optimizer"
>abstract="Avant d’envoyer des messages texte, vous devez intégrer les paramètres du fournisseur à Journey Optimizer. Une fois cette opération terminée, vous devrez créer une configuration SMS/MMS. Ces étapes doivent être exécutées par un administrateur ou une administratrice système Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Créer une configuration des canaux SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Sélectionnez la configuration du fournisseur de SMS."
>abstract="Sélectionnez les informations d’identification d’API configurées pour votre fournisseur SMS."

>[!CONTEXTUALHELP]
>id="ajo_admin_fuzzy_opt_out"
>title="Opt-out en logique floue"
>abstract="Lorsqu’elle est activée, l’option Opt-out en logique floue détecte les messages entrants qui ressemblent fortement aux mots-clés d’opt-out définis (par exemple, « CANCIL ») et envoie automatiquement une réponse de confirmation pour vérifier l’intention de désabonnement de l’utilisateur ou de l’utilisatrice. Si la personne confirme en utilisant le prompt défini, elle est désabonnée."

Avant d’envoyer des SMS, des MMS ou des RCS, vous devez configurer votre environnement Adobe Journey Optimizer. Pour ce faire, procédez comme suit :

1. Intégrez les paramètres du fournisseur à Journey Optimizer.
Les étapes dépendent de votre fournisseur SMS. Consultez les liens ci-dessous pour accéder à la documentation détaillée :
   * [Infobip](sms-configuration-infobip.md)
   * [Sinch](sms-configuration-sinch.md)
   * [Twilio](sms-configuration-twilio.md)
   * [Fournisseur personnalisé](sms-configuration-custom.md)
1. [Créer un webhook](sms-webhook.md)
1. [Créer une configuration des SMS](sms-configuration-surface.md)

Ces étapes doivent être exécutées par un [Administrateur ou une Administratrice système](../start/path/administrator.md) Adobe Journey Optimizer.

## Conditions préalables{#sms-prerequisites}

Adobe Journey Optimizer s’intègre actuellement à des fournisseurs tiers qui proposent des services de messages texte indépendants d’Adobe Journey Optimizer. Les fournisseurs pris en charge pour les SMS et les MMS sont les suivants : **Sinch**, **Twilio** et **Infobip**. Notez que vous pouvez configurer des fournisseurs de messagerie supplémentaires à l’aide de la [configuration de fournisseur personnalisé](sms-configuration-custom.md).

Avant la configuration du canal SMS, vous devez créer un compte auprès de l’un de ces fournisseurs afin de recevoir le **jeton API** et l’**ID de service** qui vous permettront d’établir la connexion entre Adobe Journey Optimizer et le fournisseur approprié.

Votre utilisation des services de messages SMS et MMS sera soumise aux conditions générales supplémentaires de la part du fournisseur concerné. En tant que solutions tierces, Sinch, Twilio et Infobip sont disponibles pour les utilisateurs et utilisatrices d’Adobe Journey Optimizer via une intégration. Adobe ne contrôle pas et n’est pas responsable des produits tiers. Pour tout problème ou toute demande d’assistance relative aux services de messages texte (SMS/MMS), contactez votre fournisseur.

>[!CAUTION]
>
>Pour accéder aux sous-domaines SMS et les modifier, vous devez disposer de l’autorisation **[!UICONTROL Gestion des sous-domaines SMS]** dans le sandbox de production. En savoir plus sur les autorisations sur [cette page](../administration/high-low-permissions.md#administration-permissions).
>

