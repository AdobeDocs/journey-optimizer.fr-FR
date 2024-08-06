---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le canal SMS
description: Découvrez comment configurer votre environnement pour envoyer des messages texte avec Journey Optimizer.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: af03ad62c2c7b29d695670f083e0dfb6d0c71b93
workflow-type: ht
source-wordcount: '345'
ht-degree: 100%

---

# Commencer la configuration des SMS {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurer votre fournisseur de SMS avec Journey Optimizer"
>abstract="Adobe Journey Optimizer envoie des message SMS par le biais des fournisseurs de SMS. Sélectionnez votre fournisseur et renseignez vos informations d’identification de l’API."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Configurer votre fournisseur de SMS avec Journey Optimizer"
>abstract="Adobe Journey Optimizer envoie du contenu média par le biais de fournisseurs de services MMS. Sélectionnez votre fournisseur et renseignez vos informations d’identification de l’API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurer votre fournisseur de SMS/MMS avec Journey Optimizer"
>abstract="Avant d’envoyer des messages texte, vous devez intégrer les paramètres du fournisseur à Journey Optimizer. Une fois cette opération terminée, vous devrez créer une surface SMS/MMS. Ces étapes doivent être exécutées par un Administrateur ou une Administratrice système Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/sms/configure-sms/sms-configuration-surface" text="Création d’une surface de canal SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Sélectionnez la configuration du fournisseur de SMS."
>abstract="Sélectionnez les informations d’identification d’API configurées pour votre fournisseur SMS."

Avant d’envoyer des SMS ou des MMS, vous devez configurer votre environnement Adobe Journey Optimizer. Procédez comme suit :

1. Intégrez les paramètres du fournisseur à Journey Optimizer :
   * [Avec Sinch](sms-configuration-sinch.md)
   * [Avec Infobip](sms-configuration-infobip.md)
   * [Avec un fournisseur personnalisé](sms-configuration-custom.md)
1. [Créer une surface SMS](sms-configuration-surface.md)

Ces étapes doivent être exécutées par un [Administrateur ou une Administratrice système](../start/path/administrator.md) Adobe Journey Optimizer.

## Conditions préalables{#sms-prerequisites}

Adobe Journey Optimizer s’intègre actuellement à des fournisseurs tiers qui proposent des services de messages texte indépendants d’Adobe Journey Optimizer. Les fournisseurs pris en charge pour les SMS et les MMS sont les suivants : **Sinch**, **Twilio** et **Infobip**.

Avant la configuration du canal SMS, vous devez créer un compte auprès de l’un de ces fournisseurs afin de recevoir le **jeton API** et l’**ID de service** qui vous permettront d’établir la connexion entre Adobe Journey Optimizer et le fournisseur approprié.

Votre utilisation des services de messages SMS et MMS sera soumise aux conditions générales supplémentaires de la part du fournisseur concerné. En tant que solutions tierces, Sinch, Twilio et Infobip sont disponibles pour les utilisateurs et utilisatrices d’Adobe Journey Optimizer via une intégration. Adobe ne contrôle pas et n’est pas responsable des produits tiers. Pour tout problème ou toute demande d’assistance relative aux services de messages texte (SMS/MMS), contactez votre fournisseur.

>[!CAUTION]
>
>Pour accéder aux sous-domaines SMS et les modifier, vous devez disposer de l’autorisation **[!UICONTROL Gestion des sous-domaines SMS]** dans le sandbox de production. Pour en savoir plus sur les autorisations, consultez [cette page](../administration/high-low-permissions.md#administration-permissions).
>

