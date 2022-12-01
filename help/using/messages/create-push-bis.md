---
solution: Journey Optimizer
product: journey optimizer
title: Configurer une notification push
description: Découvrez comment créer une notification push dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 5e5b078fa61e2c615a2242f50439c2f20ea5216a
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 50%

---

# Créer une notification push {#create-push-notification-bis}

## Créer la notification push dans un parcours ou une campagne

Pour créer une notification push, procédez comme suit :

>[!BEGINTABS]

>[!TAB Ajout d’une notification push à un Parcours]

1. Ouvrez votre parcours, puis faites glisser et déposez une activité Push depuis la section Actions de la palette.

1. Fournissez des informations de base sur votre message (libellé, description, catégorie), puis choisissez la surface du message à utiliser.

   Pour plus d’informations sur la configuration d’un parcours, reportez-vous à la section

1. Dans l’écran de configuration du parcours, cliquez sur le bouton **[!UICONTROL Modifier le contenu]** pour configurer le contenu push.

1. Une fois le contenu de votre message défini, vous pouvez utiliser des profils de test pour le prévisualiser et le tester.

1. Lorsque votre notification push est prête, effectuez la configuration de votre pour l’envoyer.

   Pour suivre le comportement de vos destinataires par le biais des ouvertures et/ou interactions push, assurez-vous que les options dédiées dans la section tracking sont activées dans .

>[!TAB Ajout d’une notification push à une campagne]

1. Créez une campagne planifiée ou déclenchée par une API, sélectionnez **[!UICONTROL Notification push]** comme action et choisissez la variable **[!UICONTROL Surface de l’application]** à utiliser.

1. Cliquez sur **[!UICONTROL Créer]**.

1. Dans la section **[!UICONTROL Propriétés]**, modifiez le **[!UICONTROL Titre]** et la **[!UICONTROL Description]** de votre campagne.

1. Cliquez sur le bouton **[!UICONTROL Sélectionner une audience]** pour définir l’audience à cibler à partir de la liste des segments Adobe Experience Platform disponibles.

1. Dans le champ **[!UICONTROL Espace de noms d’identité]**, choisissez l’espace de noms à utiliser pour identifier les personnes à partir du segment sélectionné.

1. Les campagnes sont conçues pour être exécutées à une date spécifique ou à une fréquence récurrente. Découvrez comment configurer le **[!UICONTROL Planification]** de votre campagne dans .

1. Dans la **[!UICONTROL Déclencheurs d’action]** , choisissez la variable **[!UICONTROL Fréquence]** de votre notification push :

   * Une fois
   * Quotidien
   * Hebdomadaire
   * Mensuel

1. Dans l&#39;écran de configuration de l&#39;opération, cliquez sur le bouton **[!UICONTROL Modifier le contenu]** pour configurer le contenu push.

1. Une fois le contenu de votre message défini, vous pouvez utiliser des profils de test pour le prévisualiser et le tester.

1. Lorsque votre notification push est prête, effectuez la configuration de votre pour l’envoyer.

   Pour suivre le comportement de vos destinataires par le biais des ouvertures et/ou interactions push, assurez-vous que les options dédiées dans la section de tracking sont activées dans la section ).

>[!ENDTABS]

## Mode de diffusion rapide

Mode de diffusion rapide, précédemment connu sous le nom de mode d’éclatement dans parcours, est un [!DNL Journey Optimizer] module complémentaire permettant d’envoyer très rapidement des messages push dans de grands volumes par le biais de campagnes.

Le mode de diffusion rapide est utilisé lorsque le retard dans la diffusion des messages est critique pour l’entreprise, quand vous souhaitez envoyer une alerte push urgente sur les téléphones mobiles, par exemple des nouvelles importantes destinées aux utilisateurs qui ont installé votre application de canal d’actualités.

Pour plus d&#39;informations sur les performances lors de l&#39;utilisation du mode de diffusion Rapid, reportez-vous à la section .

### Conditions préalables

La messagerie en diffusion rapide est fournie avec les conditions suivantes :

* La diffusion rapide est disponible pour les campagnes **[!UICONTROL planifiées]** uniquement et n’est pas disponible pour les campagnes déclenchées par l’API.
* Aucune personnalisation n’est autorisée dans le message push.
* L’audience cible doit contenir moins de 30 millions de profils.
* Vous pouvez exécuter simultanément jusqu’à 5 campagnes à l’aide du mode de diffusion Rapid .

### Activer le mode de diffusion rapide

1. Créez une campagne de notification push et activez/désactivez l’option **[!UICONTROL Diffusion rapide]**.

1. Configurez le contenu du message et sélectionnez l’audience à cibler.

   >[!IMPORTANT]
   >
   >Assurez-vous que le contenu du message ne contient aucune personnalisation et que l’audience contient moins de 30 millions de profils.

1. Vérifiez et activez votre campagne comme vous le faites habituellement. Notez que, en mode test, les messages ne sont pas envoyés via le mode de diffusion rapide.