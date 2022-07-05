---
title: Création dʼun SMS
description: Découvrez comment créer un message SMS dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 630b8ef5a140709161b24256083b2104be5b6121
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 38%

---

# Création dʼun SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Création d&#39;un SMS"
>abstract="Ajoutez votre message texte et commencez à le personnaliser à l&#39;aide de l&#39;éditeur d&#39;expression."

Une fois que [création d’un message](get-started-content.md), utilisez le **[!UICONTROL SMS]** pour définir les paramètres et le contenu du SMS.


>[!AVAILABILITY]
>
>Le canal SMS est actuellement disponible uniquement pour un ensemble d’organisations (disponibilité limitée). Pour en savoir plus, contactez votre représentant Adobe.

![](assets/sms_1.png)

Si c&#39;est la première fois que vous créez un SMS, vérifiez que le canal SMS a été configuré. [En savoir plus](../configuration/sms-configuration.md).

## Définir le contenu du SMS{#sms-content}

Pour personnaliser votre message SMS, procédez comme suit :

1. Cliquez sur le champ **[!UICONTROL Ajouter un message texte]** pour afficher lʼéditeur dʼexpression.

   ![](assets/sms_3.png)

1. Utilisez l’éditeur d’expression pour définir le contenu. Vous pouvez utiliser n’importe quel attribut pour personnaliser le contenu, tel que le nom du profil ou la ville. Consultez [cette section](../personalization/personalize.md) pour en savoir plus sur la personnalisation dans l&#39;éditeur d&#39;expression.

   >[!NOTE]
   >
   > Un SMS peut contenir jusqu’à 160 caractères, espaces et sauts de ligne inclus.

   ![](assets/sms_2.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** lorsque votre message est prêt.

## Valider votre SMS{#sms-preview}

Une fois le contenu de votre message défini, vous pouvez utiliser des profils de test pour le prévisualiser et le tester. Si vous avez inséré [contenu personnalisé](../personalization/personalize.md), vous pouvez vérifier l’affichage de ce contenu dans le message en exploitant les données de profil de test.

Pour visualiser l’affichage de votre SMS sur les appareils mobiles, accédez à la page **[!UICONTROL Aperçu]** .

Voir à ce propos [cette section](../design/preview.md).

## Publier votre SMS {#sms-publish}

Une fois que votre message est prêt, vous pouvez le publier afin de permettre son exécution à lʼaide du bouton **[!UICONTROL Publier]**. Cette action publie la nouvelle version du message qui sera utilisée pour les prochaines exécutions dans vos parcours.

Votre message SMS peut maintenant être utilisé dans un parcours. [Découvrez comment créer des parcours](../building-journeys/journey-gs.md).

## Inclusion et exclusion{#sms-opt-in-out}

Pour tous les messages marketing, le SMS doit contenir un moyen pour que les destinataires puissent facilement se désabonner. Une fois désabonnés, les profils sont automatiquement supprimés de l’audience des futurs messages marketing. L&#39;ajout d&#39;un lien de désinscription n&#39;est pas obligatoire pour les messages transactionnels.

Les destinataires des SMS peuvent répondre avec des mots-clés d&#39;opt-in et d&#39;opt-out. Conformément aux normes et réglementations du secteur, Adobe Journey Optimizer traite automatiquement les mots-clés suivants dans les messages entrants : DÉMARRER, ARRÊTER et DÉMARRER. Ces mots-clés déclenchent des réponses standard automatiques de la part du fournisseur SMS.

Pour en savoir plus sur le fonctionnement de la prise en charge native des mots-clés entrants (démarrage, arrêt et arrêt) pour les SMS, reportez-vous à la vidéo suivante.

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

## Vidéo pratique

Découvrez comment configurer, créer et inclure des messages SMS dans vos parcours clients.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)

**Rubriques connexes**

* [Configuration du canal SMS](../configuration/sms-configuration.md)
* [Rapport SMS](../reports/journey-global-report.md#sms-global)
* [Création d&#39;un nouveau message](get-started-content.md)
* [Ajout d&#39;un message dans un parcours](../building-journeys/journeys-message.md)
