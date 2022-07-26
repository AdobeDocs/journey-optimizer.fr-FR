---
title: Création dʼun SMS
description: Découvrez comment créer un message SMS dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 62%

---

# Création dʼun SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Création d&#39;un SMS"
>abstract="Ajoutez votre message texte et commencez à le personnaliser à l&#39;aide de l&#39;éditeur d&#39;expression."

Utilisation [!DNL Journey Optimizer] pour envoyer des SMS à vos clients sur leurs appareils mobiles. Vous pouvez créer, personnaliser et prévisualiser des messages au format texte à partir de l&#39;éditeur de SMS.

Une fois que [ajout d’un SMS](get-started-content.md) dans votre parcours, et définissez les paramètres de base, utilisez la variable **[!UICONTROL Actions : SMS]** volet de droite pour créer le contenu du SMS.

>[!AVAILABILITY]
>
>Le canal SMS est actuellement disponible uniquement pour un ensemble d’organisations (disponibilité limitée). Pour en savoir plus, contactez votre représentant Adobe.

![](assets/sms-edit-content.png)

Si c’est la première fois que vous créez un message SMS, vérifiez que le canal SMS a été configuré. [En savoir plus](../configuration/sms-configuration.md).

## Définir le contenu de votre SMS{#sms-content}

Pour personnaliser votre message SMS, procédez comme suit :

1. Cliquez sur le bouton **[!UICONTROL Message]** pour ouvrir l’éditeur d’expression.

   ![](assets/sms-content.png)

1. Utilisez l&#39;éditeur d&#39;expression pour définir le contenu. Vous pouvez utiliser n’importe quel attribut pour personnaliser le contenu, comme le nom du profil ou la ville. En savoir plus sur la personnalisation dans l’éditeur d’expression de la section [cette section](../personalization/personalize.md).

1. Cliquez sur **[!UICONTROL Enregistrer]** et vérifiez votre message dans l&#39;aperçu.

   ![](assets/sms-content-preview.png)


## Valider votre SMS{#sms-preview}

Une fois le contenu de votre message défini, vous pouvez utiliser des profils de test pour le prévisualiser et le tester. Si vous avez inséré du [contenu personnalisé](../personalization/personalize.md), vous pourrez vérifier comment ce contenu s’affiche dans le message en exploitant les données du profil de test.

Pour visualiser l’affichage de votre SMS sur les appareils mobiles, cliquez sur le bouton **[!UICONTROL Simulation du contenu]** . En savoir plus sur la simulation de contenu dans [cette section](../design/preview.md).

Vous devez également vérifier les alertes dans la section supérieure de l’éditeur.  Certains d’entre eux sont de simples avertissements, mais d’autres peuvent vous empêcher d’utiliser le message. En savoir plus dans [cette section](alerts.md).

![](assets/sms-alert-button.png)


## Opt-in et opt-out{#sms-opt-in-out}

Pour tous les messages marketing, les SMS doivent contenir une méthode de désinscription simple pour les utilisateurs. Une fois désinscrits, les profils sont automatiquement supprimés de l’audience des futurs messages marketing. L’ajout d’un lien de désinscription n’est pas obligatoire pour les messages transactionnels.

Les destinataires des SMS peuvent répondre avec des mots-clés pour indiquer l’opt-in et l’opt-out. Conformément aux normes et réglementations du secteur, Adobe Journey Optimizer traite automatiquement les mots-clés suivants dans les messages entrants : DÉMARRAGE, ARRÊT et REDÉMARRAGE. Ces mots-clés déclenchent des réponses standard automatiques de la part du fournisseur SMS.

Pour en savoir plus sur le fonctionnement de la prise en charge native des mots-clés entrants (démarrage, arrêt et redémarrage) pour les SMS, regardez la vidéo suivante.

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

<!--
## How-to video

Learn how to configure, author, and include SMS messaging into your customer journeys.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)
-->
**Rubriques connexes**

* [Configuration du canal SMS](../configuration/sms-configuration.md)
* [Rapport SMS](../reports/journey-global-report.md#sms-global)
* [Création d&#39;un nouveau message](get-started-content.md)
* [Ajout d&#39;un message dans un parcours](../building-journeys/journeys-message.md)
