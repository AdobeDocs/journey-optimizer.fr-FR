---
solution: Journey Optimizer
product: journey optimizer
title: Modifier le contenu de la campagne déclenchée par l’API
description: Découvrez comment modifier le contenu de la campagne déclenchée par l’API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, déclenchées par l’API, REST, optimizer, messages
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 62%

---


# Modifier le contenu de la campagne déclenchée par l’API {#api-content}

Pour configurer le contenu du message, accédez à l’onglet **[!UICONTROL Contenu]** ou cliquez sur le bouton **[!UICONTROL Modifier le contenu]**.

![](assets/campaign-content.png)

## Concevoir le contenu {#design}

Le processus de création de contenu dépend du canal que vous avez sélectionné. Découvrez les étapes détaillées pour créer le contenu de votre message dans les pages suivantes :

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/create-email.md"><img alt="E-mail" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/create-email.md"><strong>E-mail</strong></a></div></td>
<td><a href="../sms/create-sms.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="Notification push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/create-push.md"><strong>Notification push</strong></a></div></td>
</tr></table>

## Personnaliser du contenu à l’aide de données contextuelles {#contextual}

Vous pouvez transmettre des données supplémentaires dans la payload de l’API que vous pouvez exploiter pour personnaliser votre message.

Prenons un exemple où les clients souhaitent réinitialiser leur mot de passe et où vous souhaitez leur envoyer une URL de réinitialisation de mot de passe générée dans un outil tiers. Avec les campagnes déclenchées par API, vous pouvez transmettre cette URL générée dans la payload de l’API et l’utiliser dans la campagne pour l’ajouter au message.

Pour ce faire, vous devez les transmettre dans la payload de l’API et les ajouter dans votre message à l’aide de l’éditeur de personnalisation. Utilisez la syntaxe `{{context.<contextualAttribute>}}`, où `<contextualAttribute>` doit correspondre au nom de la variable dans la payload de l’API contenant les données que vous souhaitez transmettre.

Notez que, pour l’instant, aucun attribut contextuel n’est disponible dans le menu du rail de gauche. Les attributs doivent être saisis directement dans votre expression de personnalisation, sans vérification effectuée par [!DNL Journey Optimizer].

![](assets/api-triggered-context.png)

**À lire absolument**

* Les attributs contextuels transmis dans la requête ne peuvent pas dépasser 200 Ko et sont toujours considérés de type chaîne.
* La syntaxe `context.system` est limitée à l’utilisation interne d’Adobe uniquement et ne doit pas être utilisée pour transmettre des attributs contextuels.
* Contrairement aux événements activés pour le profil, les données contextuelles transmises dans l’API REST sont utilisées pour une communication ponctuelle et ne sont pas stockées par rapport au profil. Au maximum, le profil est créé avec les détails de l’espace de noms, s’il a été détecté comme manquant.
* L’utilisation d’un grand nombre de données contextuelles importantes dans votre contenu peut avoir un impact sur les performances.

## Test et vérification du contenu

Une fois votre contenu défini, utilisez le bouton **[!UICONTROL Simuler le contenu]** pour prévisualiser et tester votre contenu avec des profils de test ou des exemples de données d’entrée chargés à partir d’un fichier CSV/JSON ou ajoutés manuellement. [Découvrez comment prévisualiser et tester du contenu](../content-management/preview-test.md). Pour revenir à l’écran de création de campagne, cliquez sur la flèche vers la gauche.

![](assets/create-campaign-design.png)

## Étapes suivantes {#next}

Une fois que la configuration et le contenu de votre campagne sont prêts, vous pouvez définir l’audience de la campagne. [En savoir plus](api-triggered-campaign-audience.md)
