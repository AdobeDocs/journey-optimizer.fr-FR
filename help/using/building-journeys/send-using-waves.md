---
solution: Journey Optimizer
product: journey optimizer
title: Envoi par vagues dans les parcours
description: Planifiez la diffusion des messages de parcours sortants par lots contrôlés (vagues) dans le temps. L’envoi de vagues dans des parcours en lecture d’audience permet d’équilibrer la charge et de prendre en charge la délivrabilité.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
mini-toc-levels: 1
keywords: vagues, lots, planning, parcours, lecture d’audience, délivrabilité
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 1%

---

# Envoi par vagues dans les parcours {#send-using-waves-journeys}

>[!AVAILABILITY]
>
>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

Vous pouvez diffuser des messages sortants à partir d’un parcours par lots (vagues) au fil du temps, au lieu de les diffuser tous en même temps. L’envoi de vagues permet d’équilibrer la charge, d’éviter de surcharger les systèmes en aval (tels que les centres d’appels ou les landing pages) et de prendre en charge la délivrabilité et la réputation de l’expéditeur, en particulier pour les parcours de lecture d’audience à volume élevé.

<!--
>[!CAUTION]
>
>Wave sending is available for read audience journeys only and applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

Vous le configurez au niveau du parcours lorsque vous définissez la manière dont l’audience entre et comment les actions sont planifiées. Vous définissez le nombre de vagues, leur taille (en pourcentage de l’audience ou en nombres absolus) et le moment où chaque vague s’exécute.

## Limites et mécanismes de sécurisation {#limitations-guardrails}

* L’envoi de vagues est uniquement disponible pour les parcours d’audience lue avec les types de planificateur **[!DNL As soon as possible]** et **[!UICONTROL Une fois]**. En savoir plus sur le planning de parcours [&#128279;](read-audience.md#schedule).
* L’envoi de vagues n’est pas disponible pour les parcours récurrents, déclenchés par un événement, d’événement métier, de mode test ou d’exécution d’essai.
* Vous devez définir au moins 2 vagues de **2** et vous pouvez ajouter jusqu’à 10 vagues de **&#x200B;**.
* L’intervalle minimum entre le début de deux vagues est de **30 minutes**.
* Un début de vague ne peut pas être antérieur au début du parcours ou antérieur.
* La division de l’audience en vagues peut prendre jusqu’à 1 heure. Les profils ne peuvent pas entrer dans le parcours avant cette date.
* Dans une seule version de parcours, deux vagues ne s’exécutent jamais en même temps. La prochaine vague ne commence qu&#39;une fois la précédente terminée. Par exemple, si des vagues sont planifiées à 1 heure d’intervalle, mais que la première vague dure 2 heures, la seconde vague commence à la fin de la première vague, et non à l’heure planifiée.
* Les démarrages de vagues peuvent être retardés lorsque la plateforme applique des limites de quota ou lorsque la capacité du système est soumise à une charge importante.

## Configurer l’envoi de vagues dans un parcours {#configure-wave-sending}

1. Commencez votre parcours par une activité [&#x200B; Lecture d’audience &#x200B;](read-audience.md).

1. Double-cliquez sur l’activité **[!UICONTROL Lecture d’audience]** pour afficher ses propriétés et sélectionnez l’option **[!UICONTROL Diffuser l’action de parcours par vagues]**.

   ![](assets/journey-wave-option.png){width="100%"}

1. Définissez le **nombre de vagues** (par exemple, 4).

   ![](assets/journey-wave-number.png){width="80%"}

   >[!NOTE]
   >
   >Vous devez définir au moins 2 vagues et pouvez ajouter jusqu’à 10 vagues.

1. Choisissez comment définir la taille et la durée des vagues comme décrit ci-dessous.

### Ondes égales {#equal-waves}

Par défaut, l’audience est divisée en vagues de taille égale. Définissez un intervalle fixe entre le début de chaque vague (par exemple, 2 heures).

![](assets/journey-equal-waves.png){width="70%"}

>[!NOTE]
>
>L’intervalle minimum entre le début de deux vagues est de **30 minutes**.

Le système planifie ensuite automatiquement les vagues suivantes (par exemple, la première vague à 9 :00, la deuxième à 11 :00, la troisième à 13 :00, la quatrième à 15 :00).

### Distribution personnalisée {#custom-distribution}

Sélectionnez l’option **[!UICONTROL Distribution personnalisée]** pour définir la taille de chaque vague en pourcentage de l’audience totale (par exemple, 15 %, 20 %, 25 %, 40 %).

![](assets/journey-wave-percentage.png){width="70%"}

>[!NOTE]
>
>Le total sur toutes les vagues doit être égal à 100 %. Si ce n&#39;est pas le cas, un message d&#39;avertissement s&#39;affiche.<!--are the waves actually sent or does the system prevent user from saving the journey?-->

Sélectionnez **[!UICONTROL Nombres]** pour définir la taille de chaque vague en tant que nombre absolu de profils (par exemple, 10 000 ; 50 000).

![](assets/journey-wave-numbers.png){width="70%"}

>[!NOTE]
>
>Lorsque vous utilisez des nombres, le système ne vérifie pas si la somme couvre toute l’audience. Vous devez vous assurer que la taille des vagues couvre l’audience à laquelle vous avez l’intention d’envoyer. Pour en savoir plus, consultez le [Forum aux questions](#faq).

### Planning personnalisé {#custom-schedule}

Sélectionnez **[!UICONTROL Planifier chaque vague]** pour définir une date et une heure de début spécifiques pour chaque vague. Les vagues n’ont pas besoin d’être régulièrement espacées (par exemple, 9 :00, 11:00, 17:00, 20 :30).

![](assets/journey-wave-custom-schedule.png){width="70%"}

>[!NOTE]
>
>L’intervalle minimum entre le début de deux vagues est de **30 minutes**.

## Cas d’utilisation {#use-cases}

L’envoi de vagues vous permet de contrôler le moment et le nombre de messages envoyés, ce qui peut améliorer la délivrabilité, protéger la réputation de l’expéditeur et aligner les envois sur votre capacité opérationnelle. Envisagez d’utiliser des vagues dans les scénarios suivants :

* **Gestion du centre d’appel ou de la réaction :** limitez le nombre de messages envoyés par jour ou par heure afin que les équipes en aval (par exemple l’assistance clientèle) puissent gérer les réponses. Par exemple, envoyez 20 messages par jour pour correspondre à la capacité du centre d’appels.

  ![](assets/journey-waves-ex-call-center.png){width="55%"}

* **Volume et délivrabilité élevés :** évitez d’envoyer un parcours très volumineux en une seule fois. Diffusez la diffusion au fil du temps pour aider à maintenir la réputation de l&#39;expéditeur et réduire le risque d&#39;être marqué comme indésirable.

  ![](assets/journey-waves-ex-high-volume.png){width="55%"}

* **Ramp-up :** lors de l’utilisation d’une nouvelle plateforme ou d’une nouvelle adresse IP, augmentez progressivement le volume (par exemple, 10 % lors de la première vague, puis 15 %, 20 %, etc.) pour établir progressivement la réputation.

  ![](assets/journey-waves-ex-ramp-up.png){width="55%"}

## Questions fréquentes {#faq}

+++ Que se passe-t-il si la somme des tailles des vagues n’est pas égale à votre audience totale ?

* Si la somme de vos tailles de vagues **dépasse** l’audience (par exemple, vous planifiez 100 000 dans la première vague pour une audience de 100 000), la première vague sera envoyée à l’audience complète et les vagues restantes n’auront plus personne à qui envoyer ; elles ne s’exécuteront pas.
* Si la somme **est inférieure** à l’audience (par exemple, si vous définissez quatre vagues totalisant 40 000 profils pour une audience de 100 000), seuls les profils inclus dans ces vagues recevront le message. Le reste de l’audience ne recevra pas la communication et ne fera pas l’objet de nouvelles tentatives par vagues ultérieures.

+++

+++ Puis-je attribuer différents segments ou critères à des vagues individuelles ?

Vous pouvez uniquement définir la taille et la durée des vagues. La même audience traverse le parcours. Vous ne pouvez pas attribuer différents segments ou critères à des vagues individuelles.

+++

## Voir également {#see-also}

* [Utiliser une audience dans un parcours &#x200B;](read-audience.md) : configurez l&#39;activité Lecture d&#39;audience.
