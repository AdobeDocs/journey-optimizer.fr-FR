---
title: Limite de profil
description: Limite de profil
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
hide: true
hidefromtoc: true
source-git-commit: b5ce2ea81d4091b4fa9c09e83573f9043c5e55a8
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 5%

---


# Établir votre réputation en tant qu’expéditeur

Si vous avez récemment migré vers un autre fournisseur de services de messagerie, une adresse IP, un domaine de messagerie ou un sous-domaine, vous devez établir votre réputation en tant qu’expéditeur. Sinon, vos diffusions peuvent être bloquées ou déplacées dans le dossier spam de la boîte aux lettres des destinataires.

Pour réchauffer votre adresse IP, vous pouvez augmenter progressivement le nombre de vos diffusions. Voir [cas d’utilisation](../building-journeys/ramp-up-deliveries-uc.md). 

## Type de condition de limite de profil {#profile_cap}

Les autres types de condition sont présentés dans cette section [section](../building-journeys/condition-activity.md).

Utilisez ce type de condition pour définir un nombre maximal de profils pour un chemin d’accès au parcours. Lorsque cette limite est atteinte, les profils entrant prennent un autre chemin.

Vous pouvez utiliser ce type de condition pour augmenter le volume de vos diffusions. Voir [cas d’utilisation](../building-journeys/ramp-up-deliveries-uc.md). 

La limite par défaut est 1 000. Vous pouvez définir une valeur entière comprise entre 1 et 20 000.

Le compteur s’applique uniquement à la version de parcours sélectionnée. Le compteur est réinitialisé à zéro au bout d’un mois. Après une réinitialisation, les profils entrant reprennent le chemin nominal jusqu’à ce que la limite de compteur soit atteinte.

Le chemin nominal a toujours la priorité sur le chemin alternatif, même si vous déplacez le chemin alternatif au-dessus du chemin nominal sur le canevas de parcours.

![](../assets/profile-cap-condition.png)

## Cas pratique : augmenter vos diffusions ;

Si vous avez récemment migré vers un autre fournisseur de services de messagerie, une adresse IP, un domaine de messagerie ou un sous-domaine, vous devez établir votre réputation en tant qu’expéditeur. Sinon, vos diffusions peuvent être bloquées ou déplacées dans le dossier spam de la boîte aux lettres des destinataires. Découvrez comment améliorer la réputation de vos emails grâce au réchauffement des adresses IP dans la section [Guide des bonnes pratiques de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}.

Pour réchauffer votre adresse IP, vous pouvez augmenter progressivement le nombre de vos diffusions. En savoir plus sur [optimisation de la délivrabilité dans Journey Optimizer](../deliverability.md).

Ce cas pratique a pour but de créer un parcours pour accélérer vos diffusions email. Pour configurer ce parcours, procédez comme suit:

1. Création d’un parcours. [En savoir plus](../building-journeys/journey-gs.md).

1. Ajouter un **[!UICONTROL Condition]** à l’parcours. [En savoir plus](../building-journeys/condition-activity.md).

1. Dans le **[!UICONTROL Condition]** paramètres d&#39;activité, définissez le nombre maximum de destinataires pour votre diffusion :

   1. Dans le **[!UICONTROL Condition]** paramètres d’activité, définissez **[!UICONTROL Type]** champ à **[!UICONTROL Limite de profil]**. [En savoir plus](profile-cap.md#profile_cap).

   1. Définissez la variable **[!UICONTROL Limite]** au nombre maximum de destinataires pour cette diffusion.

   ![](../assets/profile-cap-condition.png)

   Vous pouvez augmenter progressivement cette limite jusqu’au nombre total d’abonnés.

1. Ajouter un **[!UICONTROL Message]** l’activité vers le chemin d’accès nominal après la **[!UICONTROL Condition]** activité.

   ![](../assets/ramp-up-deliveries-message.png)

   Lorsque le parcours s’exécute, le message est envoyé aux profils de saisie, jusqu’au nombre maximum de profils que vous avez spécifiés. Lorsque cette limite est atteinte, les profils entrant prennent le chemin alternatif.

1. Complétez le parcours avec les activités de votre choix.

Une fois votre adresse IP réchauffée, vous pouvez supprimer cette condition.

