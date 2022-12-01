---
solution: Journey Optimizer
product: journey optimizer
title: Création dʼun SMS
description: Découvrez comment créer un message SMS dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: b7b333e96e0f4b32a0f94c3f1e67f0f3d3fc2816
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 55%

---

# Création dʼun SMS {#create-sms-bis}

>[!NOTE]
>
>Conformément aux normes et réglementations du secteur, tous les messages SMS de marketing doivent contenir un moyen permettant aux destinataires de se désabonner facilement. Pour ce faire, les destinataires de SMS peuvent répondre avec des mots-clés d’accord préalable et de droit d’opposition.

## Créer un SMS dans un parcours ou une campagne {#sms-content}

Pour personnaliser votre message SMS, procédez comme suit :

>[!BEGINTABS]

>[!TAB Ajouter un SMS à un Parcours]

1. Ouvrez votre parcours, puis faites glisser et déposez une activité SMS depuis la section Actions de la palette.

1. Fournissez des informations de base sur votre message (libellé, description, catégorie), puis choisissez la surface du message à utiliser.

   Pour plus d&#39;informations sur le paramétrage d&#39;un parcours, reportez-vous à la section .

Vous pouvez maintenant commencer à concevoir le contenu de votre SMS à partir du **[!UICONTROL Modifier le contenu]** bouton .

>[!TAB Ajout d’un SMS à une campagne]

1. Créez une campagne planifiée ou déclenchée par une API, sélectionnez **[!UICONTROL SMS]** comme action et choisissez la variable **[!UICONTROL Surface de l’application]** à utiliser.

1. Cliquez sur **[!UICONTROL Créer]**.

1. Dans la section **[!UICONTROL Propriétés]**, modifiez le **[!UICONTROL Titre]** et la **[!UICONTROL Description]** de votre campagne.

1. Dans le **[!UICONTROL Suivi des actions]** , indiquez si vous souhaitez effectuer le suivi des clics sur les liens de votre SMS.

1. Cliquez sur le bouton **[!UICONTROL Sélectionner une audience]** pour définir l’audience à cibler à partir de la liste des segments Adobe Experience Platform disponibles.

1. Dans le champ **[!UICONTROL Espace de noms d’identité]**, choisissez l’espace de noms à utiliser pour identifier les personnes à partir du segment sélectionné.

1. Les campagnes sont conçues pour être exécutées à une date spécifique ou à une fréquence récurrente. Découvrez comment configurer le **[!UICONTROL Planification]** de votre campagne dans .

1. Dans la **[!UICONTROL Déclencheurs d’action]** , choisissez la variable **[!UICONTROL Fréquence]** de votre SMS :

   * Une fois
   * Quotidien
   * Hebdomadaire
   * Mois

Vous pouvez maintenant commencer à concevoir le contenu de votre SMS à partir du **[!UICONTROL Modifier le contenu]** bouton .

>[!ENDTABS]

## Définir le contenu de votre SMS{#sms-content}

1. Dans l&#39;écran de configuration des parcours ou des campagnes, cliquez sur le bouton **[!UICONTROL Modifier le contenu]** pour configurer le contenu du SMS.

1. Cliquez sur le champ **[!UICONTROL Message]** pour ouvrir l’éditeur d&#39;expression.

1. Utilisez l’éditeur d’expression pour définir le contenu et ajouter du contenu dynamique. Vous pouvez utiliser n’importe quel attribut, comme le nom du profil ou la ville.

1. Cliquez sur **[!UICONTROL Enregistrer]** et vérifiez votre message dans l&#39;aperçu.

1. Une fois votre SMS prêt, effectuez la configuration de votre pour l’envoyer.

## Valider votre SMS{#sms-preview}

>[!NOTE]
>
> Pour une meilleure délivrabilité, vous devez toujours utiliser les numéros de téléphone dans les formats pris en charge par le fournisseur. Par exemple, Twilio et Sinch ne prennent en charge que les numéros de téléphone au format E.164.

Une fois le contenu de votre message défini, vous pouvez utiliser des profils de test pour le prévisualiser et le tester. Si vous avez inséré, vous pouvez vérifier l’affichage de ce contenu dans le message à l’aide des données de profil de test.

Pour visualiser l’affichage de votre message SMS sur les appareils mobiles, cliquez sur le bouton **[!UICONTROL Simuler du contenu]**. En savoir plus sur la simulation de contenu dans .

Vous devez également vérifier les alertes dans la section supérieure de l’éditeur.  Certaines d’entre elles sont de simples avertissements, mais d’autres peuvent vous empêcher d’utiliser le message. En savoir plus dans .
