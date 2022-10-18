---
solution: Journey Optimizer
product: journey optimizer
title: Déclencher des campagnes à l’aide d’API
description: Découvrez comment déclencher des campagnes à l’aide d’ [!DNL Journey Optimizer] API
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '800'
ht-degree: 92%

---

# Déclencher des campagnes à l’aide d’API {#trigger-campaigns}

## À propos des campagnes déclenchées par API {#about}

Avec [!DNL Journey Optimizer], vous pouvez créer des campagnes, puis les appeler à partir d’un système externe en fonction du déclencheur utilisateur à l’aide de la fonction [API REST d’exécution de message interactif](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). Vous pouvez ainsi couvrir divers besoins de messagerie opérationnelle et transactionnelle tels que les réinitialisations de mot de passe, le jeton OTP, etc.

Pour cela, vous devez d’abord créer une campagne déclenchée par une API dans Journey Optimizer, puis lancer son exécution via un appel API.

Les canaux disponibles pour les campagnes déclenchées par API sont E-mail, SMS et les messages push.

## Créer une campagne déclenchée par une API {#create}

Le processus de création de campagnes déclenchées par API reste identique aux campagnes planifiées, à l’exception de la sélection d’audiences qui est effectuée dans la payload de l’API. Vous trouverez des informations détaillées sur la création d’une campagne dans [cette section](create-campaign.md).

Pour créer une campagne déclenchée par API, procédez comme suit :

1. Créez une campagne avec le type **[!UICONTROL déclenché par API]**.

1. Sélectionnez le canal et la surface du canal à utiliser pour envoyer votre message, puis cliquez sur **[!UICONTROL Créer]**.

   ![](assets/api-triggered-type.png)

1. Indiquez un titre et une description pour la campagne, puis configurez le message à envoyer.

   ![](assets/api-triggered-properties.png)

   >[!NOTE]
   >
   >Vous pouvez transmettre des données supplémentaires dans la payload de l’API que vous pouvez utiliser pour personnaliser votre message. [En savoir plus](#contextual)
   >
   >L’utilisation d’un grand nombre de données contextuelles importantes dans votre contenu peut avoir un impact sur les performances.

1. Dans la section **[!UICONTROL Audience]**, spécifiez l’espace de nommage à utiliser pour identifier les individus du segment.

   L’option **[!UICONTROL Créer de nouveaux profils]** permet de créer automatiquement des profils qui n’existent pas dans la base de données. [En savoir plus sur la création de profils lors de l’exécution de la campagne](#profile-creation)

1. Configurez les dates de début et de fin de la campagne.

   Si vous configurez une date de début et/ou de fin spécifique pour une campagne, elle ne sera pas exécutée en dehors de ces dates et les appels d’API échoueront si la campagne est déclenchée par des API.

1. Dans la section **[!UICONTROL requête cURL]**, récupérez la variable **[!UICONTROL Identifiant de campagne]** à utiliser dans la payload de l’API.

   ![](assets/api-triggered-curl.png)

1. Cliquez sur **[!UICONTROL Examiner pour activer]** pour vérifier que votre campagne est correctement paramétrée, puis activez-la.

## Utiliser des attributs contextuels dans des campagnes déclenchées par API {#contextual}

Avec les campagnes déclenchées par API, vous pouvez transmettre des données supplémentaires dans la payload de l’API et les utiliser dans la campagne pour personnaliser votre message.

Prenons un exemple où les clients souhaitent réinitialiser leur mot de passe et où vous souhaitez leur envoyer une URL de réinitialisation de mot de passe générée dans un outil tiers. Avec les campagnes déclenchées par API, vous pouvez transmettre cette URL générée dans la payload de l’API et l’utiliser dans la campagne pour l’ajouter au message.

>[!NOTE]
>
>Contrairement aux événements activés pour le profil, les données contextuelles transmises dans l’API REST sont utilisées pour une communication ponctuelle et ne sont pas stockées par rapport au profil. Au maximum, le profil est créé avec les détails de l’espace de noms, s’il a été détecté comme manquant.

Pour utiliser ces données dans vos campagnes, vous devez les transmettre dans la payload de l’API et les ajouter dans votre message à l’aide de l’éditeur d’expression. Pour ce faire, utilisez la syntaxe `{{context.<contextualAttribute>}}`, où `<contextualAttribute>` doit correspondre au nom de la variable dans votre payload de l’API contenant les données que vous souhaitez transmettre.

La syntaxe `{{context.<contextualAttribute>}}` est mappée à un type de données String uniquement.

![](assets/api-triggered-context.png)

>[!IMPORTANT]
>
>La syntaxe `context.system` est limitée à l’utilisation interne d’Adobe uniquement et ne doit pas être utilisée pour transmettre des attributs contextuels.
Notez que, pour l’instant, aucun attribut contextuel n’est disponible dans le menu du rail de gauche. Les attributs doivent être saisis directement dans votre expression de personnalisation, sans vérification effectuée par [!DNL Journey Optimizer].

## Exécuter la campagne {#execute}

Pour exécuter une campagne déclenchée par une API, vous devez d’abord récupérer son identifiant et le transmettre à la payload de l’API. Pour ce faire, ouvrez la campagne, puis copiez-collez l’identifiant à partir de la section **[!UICONTROL requête cURL]**.

![](assets/api-triggered-id.png)

Vous pouvez ensuite utiliser cet identifiant dans la payload de votre API pour déclencher la campagne. Reportez-vous à la section [Documentation de l’API d’exécution de message interactif](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution) pour plus d’informations.

Notez que si vous avez configuré une date de début et/ou de fin spécifique lors de la création de la campagne, elle ne sera pas exécutée en dehors de ces dates et les appels API échoueront.

## Création de profils lors de l’exécution de la campagne {#profile-creation}

Dans certains cas, vous devrez peut-être envoyer des messages transactionnels à des profils qui n’existent pas dans le système, Par exemple, si un utilisateur inconnu tente de réinitialiser le mot de passe sur votre site web.

Lorsqu’un profil n’existe pas dans la base de données, Journey Optimizer vous permet de le créer automatiquement lors de l’exécution de la campagne afin de permettre l’envoi du message à ce profil.

>[!IMPORTANT]
>
>Cette fonctionnalité est fournie pour **création de profil à très petit volume** dans un cas pratique d’envoi transactionnel à volume élevé, avec la majorité des profils déjà existants dans platform.

Pour activer la création de profil à l’exécution de la campagne, faites basculer le **[!UICONTROL Créer de nouveaux profils]** activée dans la variable **[!UICONTROL Audience]** .

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>Les profils inconnus sont créés dans le jeu de données **Jeu de données de profil de messagerie interactive AJO**, dans trois espaces de nommage par défaut (e-mail, téléphone et ECID), respectivement pour chaque canal sortant (e-mail, SMS et notification push).
