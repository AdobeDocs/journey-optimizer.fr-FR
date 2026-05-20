---
solution: Journey Optimizer
product: journey optimizer
title: Configurer le canal SMS
description: Découvrez comment configurer votre environnement pour envoyer des messages texte avec Journey Optimizer.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
TQID: https://experienceleague.adobe.com/dO8HoRdGLuYVFN2YVjRCiFJQHmWHApROU8qz2-hKmTs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a4c92daab69394e6a736517f2e23a941135f7eb4
workflow-type: tm+mt
source-wordcount: 429
ht-degree: 85%

---

# Prise en main de la configuration mobile {#sms-configuration}

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
   * [Infobip](mobile-configuration-infobip.md)
   * [Sinch](mobile-configuration-sinch.md)
   * [Twilio](mobile-configuration-twilio.md)
   * [Fournisseur personnalisé](mobile-configuration-custom.md)
1. [Créer un webhook](mobile-webhook.md)
1. [Création d’une configuration mobile](mobile-configuration-surface.md)

Ces étapes doivent être exécutées par un [Administrateur ou une Administratrice système](../start/path/administrator.md) Adobe Journey Optimizer.

## Conditions préalables{#sms-prerequisites}

Adobe Journey Optimizer s’intègre actuellement à des fournisseurs tiers qui proposent des services de messages texte indépendants d’Adobe Journey Optimizer. Les fournisseurs pris en charge pour les SMS et les MMS sont les suivants : **Sinch**, **Twilio** et **Infobip**. Notez que vous pouvez configurer des fournisseurs de messagerie supplémentaires à l’aide de la [configuration de fournisseur personnalisé](mobile-configuration-custom.md).

Avant la configuration du canal mobile, vous devez créer un compte auprès de l’un de ces fournisseurs pour obtenir votre **Jeton API** et **Identifiant de service**, dont vous avez besoin pour configurer la connexion entre Adobe Journey Optimizer et le fournisseur approprié.

Votre utilisation des services de messages SMS et MMS sera soumise aux conditions générales supplémentaires de la part du fournisseur concerné. En tant que solutions tierces, Sinch, Twilio et Infobip sont disponibles pour les utilisateurs et utilisatrices d’Adobe Journey Optimizer via une intégration. Adobe ne contrôle pas et n’est pas responsable des produits tiers. Pour tout problème ou toute demande d’assistance liés aux services de messagerie mobile, contactez votre fournisseur.

>[!CAUTION]
>
>Pour accéder aux sous-domaines SMS et les modifier, vous devez disposer de l’autorisation **[!UICONTROL Gestion des sous-domaines SMS]** dans le sandbox de production. En savoir plus sur les autorisations sur [cette page](../administration/high-low-permissions.md#administration-permissions).
>

