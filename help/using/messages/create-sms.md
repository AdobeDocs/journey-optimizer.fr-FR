---
title: Création dʼun SMS
description: Découvrez comment créer un message SMS dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 77%

---

# Création dʼun SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Création d&#39;un SMS"
>abstract="Ajoutez votre message texte et commencez à le personnaliser à l’aide de l’éditeur d’expression."

Utilisez [!DNL Journey Optimizer] pour envoyer des messages texte à vos clients sur leur appareil mobile. Vous pouvez créer, personnaliser et prévisualiser des messages au format texte à partir de l’éditeur de SMS.

Les diffusions SMS peuvent être créées :

* Dans un **Parcours**: Une fois que vous avez ajouté une activité SMS dans votre parcours et défini des paramètres de base, utilisez la variable **[!UICONTROL Actions : SMS]** volet de droite pour créer le contenu du SMS.

   Pour plus d&#39;informations sur le paramétrage de votre parcours, reportez-vous à cette section [page](../building-journeys/journey-gs.md).

* Dans un **Campagne**: Une fois une campagne créée, sélectionnez SMS comme action et définissez les paramètres de base.

   Pour plus d&#39;informations sur le paramétrage de votre opération, reportez-vous à cette section [page](../campaigns/create-campaign.md#configure).

Si c’est la première fois que vous créez un message SMS, vérifiez que le canal SMS a été configuré. [En savoir plus](../configuration/sms-configuration.md).

## Définir le contenu de votre SMS{#sms-content}

Pour personnaliser votre message SMS, procédez comme suit :

1. Cliquez sur le champ **[!UICONTROL Message]** pour ouvrir l’éditeur d&#39;expression.

   ![](assets/sms-content.png)

1. Utilisez l’éditeur d’expression pour définir le contenu. Vous pouvez utiliser n’importe quel attribut pour personnaliser le contenu, comme le nom du profil ou la ville. Consultez [cette section](../personalization/personalize.md) pour en savoir plus sur la personnalisation dans l’éditeur d’expression.

1. Cliquez sur **[!UICONTROL Enregistrer]** et vérifiez votre message dans l&#39;aperçu.

   ![](assets/sms-content-preview.png)

## Valider votre SMS{#sms-preview}

>[!NOTE]
>
> Pour une meilleure délivrabilité, vous devez toujours utiliser les numéros de téléphone dans les formats pris en charge par le fournisseur. Par exemple, Twilio et Sinch ne prennent en charge que les numéros de téléphone au format E.164.

Une fois le contenu de votre message défini, vous pouvez utiliser des profils de test pour le prévisualiser et le tester. Si vous avez inséré du [contenu personnalisé](../personalization/personalize.md), vous pourrez vérifier comment ce contenu s’affiche dans le message en exploitant les données du profil de test.

Pour visualiser l’affichage de votre message SMS sur les appareils mobiles, cliquez sur le bouton **[!UICONTROL Simuler du contenu]**. En savoir plus sur la simulation de contenu dans [cette section](../design/preview.md).

Vous devez également vérifier les alertes dans la section supérieure de l’éditeur.  Certaines d’entre elles sont de simples avertissements, mais d’autres peuvent vous empêcher d’utiliser le message. En savoir plus dans [cette section](alerts.md).

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
