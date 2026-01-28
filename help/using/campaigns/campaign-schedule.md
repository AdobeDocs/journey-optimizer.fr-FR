---
solution: Journey Optimizer
product: journey optimizer
title: Planifier la campagne d’action
description: Découvrez comment planifier la campagne d’action.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: créer, optimizer, campagne, surface, messages
exl-id: b183eeb8-606f-444d-9302-274f159c3847
source-git-commit: e6aa361229f068c475732c715160b7c644189e51
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 59%

---

# Planifier la campagne d’action {#action-campaign-schedule}

Utilisez l’onglet **[!UICONTROL Planifier]** pour définir le planning de la campagne.

## Définir une date de début de campagne

Par défaut, les campagnes d’action démarrent après avoir été activées manuellement et se terminent dès que le message a été envoyé une fois. Si vous ne souhaitez pas exécuter votre campagne juste après son activation, vous pouvez spécifier la date et l’heure auxquelles le message doit être envoyé dans la section **[!UICONTROL Début de campagne]**.

Lors de la planification de campagnes dans [!DNL Adobe Journey Optimizer], assurez-vous que la date/l’heure de début correspond à la première diffusion souhaitée. Pour les campagnes récurrentes, si l’heure planifiée initiale est déjà dépassée, les campagnes sont reportées au prochain créneau horaire disponible en fonction de leurs règles de périodicité.

![](assets/campaign-start.png)

## Envoyer à l’heure locale du destinataire {#profile-timezone}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_profile_timezone"
>title="Utiliser le fuseau horaire du profil"
>abstract="Envoyer des messages en fonction du fuseau horaire du profil de chaque destinataire. Tous les destinataires recevront le message au même moment local, quelle que soit leur localisation géographique. Le système utilise le champ « timeZone » des profils Adobe Experience Platform, avec le fuseau horaire du créateur de la campagne comme fuseau horaire de secours."

Lors de la planification d’une campagne à une date et une heure spécifiques, vous pouvez choisir d’envoyer des messages en fonction du fuseau horaire du profil de chaque destinataire. Cela permet de s’assurer que tous les destinataires reçoivent le message au même moment local, quel que soit leur emplacement géographique.

Par exemple, si vous planifiez une campagne pour l’envoyer à 9 h du matin en utilisant le fuseau horaire du profil, les destinataires à New York (ET) la recevront à 9 h du matin (ET), tandis que les destinataires à Los Angeles (PT) la recevront à 9 h (PT).

>[!AVAILABILITY]
>
>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.
>
>La planification à l’aide des fuseaux horaires de profil est disponible uniquement pour ces canaux sortants : e-mail, notification push, SMS, WhatsApp et LINE.

Pour activer la planification du fuseau horaire de profil :

1. Dans la section **[!UICONTROL Début de campagne]** , indiquez la date et l’heure auxquelles le message doit être envoyé.

1. Activez l’option **[!UICONTROL Utiliser le fuseau horaire du profil]**.

   ![](assets/campaign-profile-timezone.png)

**Fonctionnement :**

Le système utilise le champ `profile.timeZone` du profil Adobe Experience Platform de chaque destinataire pour déterminer son fuseau horaire local. Si un profil ne dispose pas d’une valeur de fuseau horaire, le système utilise le fuseau horaire dans lequel la campagne a été créée comme solution de secours.

La campagne conserve le statut **Actif** pendant la diffusion des messages dans tous les fuseaux horaires. Une fois tous les fuseaux horaires traités, le statut de la campagne passe à **Terminé**.

**Identifiants de fuseau horaire pris en charge :**

Journey Optimizer valide la valeur `profile.timeZone` par rapport aux identifiants de fuseau horaire IANA standard. Les identifiants sont sensibles à la casse et doivent correspondre aux noms IANA officiels. Les décalages peuvent changer au fil du temps en raison de règles d&#39;enregistrement de la lumière du jour et de mises à jour historiques. Reportez-vous à la [Base de données des fuseaux horaires IANA](https://www.iana.org/time-zones){_blank} pour obtenir la liste officielle des identifiants.

## Définir une fréquence d’exécution

Pour les actions **E-mail**, **SMS** et **notification push**, vous pouvez définir la fréquence d’envoi du message de la campagne. Pour ce faire, utilisez l’option **[!UICONTROL Déclencheurs d’action]** dans l’écran de création de la campagne pour indiquer si la campagne doit être exécutée tous les jours, toutes les semaines ou tous les mois.

![](assets/campaign-frequency.png)

>[!NOTE]
>
>Pour les actions **E-mail**, vous pouvez créer des campagnes spécifiques d’activation de plans de préchauffage d’adresses IP. Le planning de la campagne sera piloté par le plan de préchauffage d’adresses IP auquel il sera associé, ce qui signifie que le planning ne sera plus défini dans la campagne elle-même. [Découvrez comment créer des campagnes de préchauffage d’adresses IP](../configuration/ip-warmup-campaign.md).

## Définir une date de fin

La section **[!UICONTROL Fin de la campagne]** vous permet de spécifier le moment où une campagne doit cesser d’être exécutée. En dehors des dates spécifiées, la campagne ne sera pas exécutée.

![](assets/campaign-end.png)

## Définir le contrôle du débit

[!DNL Journey Optimizer] vous permet d’activer le contrôle du débit pour les actions sortantes (e-mails, SMS, notifications push).

Cette fonctionnalité est particulièrement utile pour éviter la surcharge sur les systèmes en aval, tels que les pages de destination ou les plateformes d’assistance clientèle. Par exemple, vous pouvez définir une limite de débit de 165 messages par seconde pour garantir une diffusion régulière sans surcharger les systèmes en aval.

Pour définir le contrôle du débit, activez l’option **[!UICONTROL Limiter la diffusion]** dans la section **[!UICONTROL Paramètres de diffusion]** et indiquez le **[!UICONTROL Taux de diffusion]** par seconde souhaité.

* Taux de diffusion minimum pris en charge : 1 par seconde.
* Taux de diffusion maximal pris en charge : 2 000 par seconde lorsque l’option « Limiter la diffusion » est activée.

![](assets/throttling-rate-control.png)

>[!IMPORTANT]
>
>Lors de la définition d’un taux de diffusion, le délai maximal d’exécution de l’audience de la campagne est de 12 heures. Si le taux de diffusion est défini sur une valeur qui ne permet pas d’envoyer le message à l’ensemble de l’audience dans un délai de 12 heures, les profils restants seront exclus de la campagne. Le nombre de ces profils exclus apparaît dans le rapport de campagne.

## Étapes suivantes {#next}

Une fois votre planning de campagne prêt, vous pouvez vérifier et activer la campagne. [En savoir plus](review-activate-campaign.md)
