---
solution: Journey Optimizer
product: journey optimizer
title: Envoyer par vagues
description: Planifiez la diffusion des messages de campagne sortants par lots contrôlés dans le temps. L’envoi de vagues prend en charge la délivrabilité et permet de maintenir la réputation de l’expéditeur.
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: vagues, lots, planning, campagne, parcours, délivrabilité
source-git-commit: 7df05e41b086c60724576328c5bcfee47cab65ca
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 1%

---

# Envoi par vagues dans les campagnes {#send-using-waves}

Vous pouvez diviser la diffusion des messages de campagne sortants en plusieurs lots (vagues) et les planifier au fil du temps. L’envoi de vagues permet d’équilibrer la charge, d’éviter de surcharger les systèmes en aval (tels que les centres d’appels ou les landing pages) et de prendre en charge la délivrabilité et la réputation des expéditeurs, en particulier pour les envois de gros volumes.

<!--
>[!CAUTION]
>
>Wave sending applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

Journey Optimizer vous permet de définir le nombre de vagues, leur taille (en pourcentage de l’audience ou en nombres absolus) et le moment où chaque vague s’exécute.

## Limites et mécanismes de sécurisation {#limitations-guardrails}

* L’envoi de vagues s’applique uniquement aux actions **sortantes** (e-mail, SMS, notification push, courrier).
* Vous devez définir au moins 2 vagues de **2** et vous pouvez ajouter jusqu’à 10 vagues de ****.
* L’intervalle minimum entre le début de deux vagues est de **30 minutes**.
* Un début de vague ne peut pas être antérieur au début de la campagne ou antérieur.

## Configurer l’envoi de vagues {#configure-wave-sending}

Pour configurer comment et à quel moment envoyer des vagues dans une campagne, procédez comme suit.

1. Créez ou ouvrez une [Campagne d’action](create-campaign.md) qui contient une action sortante (par exemple, e-mail, SMS, notification push).

1. Dans l’onglet **[!UICONTROL Planifier]** de votre campagne, sélectionnez **[!UICONTROL Diffuser les actions de campagne par vagues]**.

   ![](assets/campaign-wave-option.png){width="100%"}

   >[!NOTE]
   >
   >L’option **[!UICONTROL Diffuser les actions de campagne par vagues]** ne s’affiche que lorsqu’une action sortante est sélectionnée dans l’onglet **[!UICONTROL Actions]** de la campagne. [En savoir plus](campaign-action.md)

1. Définissez le nombre de vagues à envoyer (par exemple, 4).

   >[!NOTE]
   >
   >Vous devez définir au moins 2 vagues et pouvez ajouter jusqu’à 10 vagues.

1. Choisissez comment définir la taille et la durée des vagues comme décrit ci-dessous.

### Ondes égales {#equal-waves}

Par défaut, l’audience est divisée en vagues de taille égale. Planifiez l’heure de la première vague et définissez un intervalle fixe entre le début de chaque vague (par exemple, 2 heures).

![](assets/campaign-equal-waves.png){width="80%"}

>[!NOTE]
>
>L’intervalle minimum entre le début de deux vagues est de **30 minutes**.

Le système planifie ensuite automatiquement les vagues suivantes (par exemple, la première vague à 9 :00, la deuxième à 11 :00, la troisième à 13 :00, la quatrième à 15 :00).

### Distribution personnalisée {#custom-distribution}

Sélectionnez l’option **[!UICONTROL Distribution personnalisée]** pour définir la taille de chaque vague en pourcentage de l’audience totale (par exemple, 15 %, 20 %, 25 %, 40 %).

![](assets/campaign-wave-percentage.png){width="80%"}

>[!NOTE]
>
>Le total sur toutes les vagues doit être égal à 100 %. Si ce n&#39;est pas le cas, un message d&#39;avertissement s&#39;affiche.<!--are the waves actually sent or does the system prevent user from saving the campaign?-->

Sélectionnez **[!UICONTROL Nombres]** pour définir la taille de chaque vague en tant que nombre absolu de profils (par exemple, 10 000 ; 50 000).

![](assets/campaign-wave-numbers.png){width="80%"}

>[!NOTE]
>
>Lorsque vous utilisez des nombres, le système ne vérifie pas si la somme couvre toute l’audience. Vous devez vous assurer que la taille des vagues couvre l’audience à laquelle vous avez l’intention d’envoyer. Pour en savoir plus, consultez le [Forum aux questions](#faq).

### Planning personnalisé {#custom-schedule}

Sélectionnez **[!UICONTROL Planifier chaque vague]** pour définir une date et une heure de début spécifiques pour chaque vague. Les vagues n’ont pas besoin d’être régulièrement espacées (par exemple, 9 :00, 11:00, 17:00, 20 :30).

![](assets/campaign-wave-custom-schedule.png){width="80%"}

>[!NOTE]
>
>L’intervalle minimum entre le début de deux vagues est de **30 minutes**.

## Cas d’utilisation {#use-cases}

L’envoi de vagues vous permet de contrôler le moment et le nombre de messages envoyés, ce qui peut améliorer la délivrabilité, protéger la réputation de l’expéditeur et aligner les envois sur votre capacité opérationnelle. Envisagez d’utiliser des vagues dans les scénarios suivants :

* **Gestion du centre d’appel ou de la réaction :** limitez le nombre de messages envoyés par jour ou par heure afin que les équipes en aval (par exemple l’assistance clientèle) puissent gérer les réponses. Par exemple, envoyez 20 messages par jour pour correspondre à la capacité du centre d’appels.

  ![](assets/campaign-waves-ex-call-center.png){width="75%"}

* **Volume et délivrabilité élevés :** évitez d’envoyer une campagne très volumineuse en une seule fois. Diffusez la diffusion au fil du temps pour aider à maintenir la réputation de l&#39;expéditeur et réduire le risque d&#39;être marqué comme indésirable.

  ![](assets/campaign-waves-ex-high-volume.png){width="75%"}

* **Ramp-up :** lors de l’utilisation d’une nouvelle plateforme ou d’une nouvelle adresse IP, augmentez progressivement le volume (par exemple, 10 % lors de la première vague, puis 15 %, 20 %, etc.) pour établir progressivement la réputation.

  ![](assets/campaign-waves-ex-ramp-up.png){width="75%"}

## Questions fréquentes {#faq}

+++ Que se passe-t-il si la somme des tailles des vagues n’est pas égale à votre audience totale ?

* Si la somme de vos tailles de vagues **dépasse** l’audience (par exemple, vous planifiez 100 000 dans la première vague pour une audience de 100 000), la première vague sera envoyée à l’audience complète et les vagues restantes n’auront plus personne à qui envoyer ; elles ne s’exécuteront pas.
* Si la somme **est inférieure** à l’audience (par exemple, si vous définissez quatre vagues totalisant 40 000 profils pour une audience de 100 000), seuls les profils inclus dans ces vagues recevront le message. Le reste de l’audience ne recevra pas la communication et ne fera pas l’objet de nouvelles tentatives par vagues ultérieures.

+++

+++ Puis-je attribuer différents segments ou critères à des vagues individuelles ?

Vous pouvez uniquement définir la taille et la durée des vagues. La sélection des destinataires est la même pour l’ensemble de la campagne ; vous ne pouvez pas affecter différents segments ou critères à des vagues individuelles.

+++

## Étapes suivantes {#next}

* [Planifier la campagne Action](campaign-schedule.md) : définissez la date de début, la date de fin, la fréquence et le contrôle des taux.
* [Vérifier et activer la campagne](review-activate-campaign.md)—vérifier la campagne et la mettre en ligne.
