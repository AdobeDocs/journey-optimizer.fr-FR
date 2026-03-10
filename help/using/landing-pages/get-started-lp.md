---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des pages de destination
description: En savoir plus sur les pages de destination dans Journey Optimizer
feature: Landing Pages, Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: destination, page de destination, commencer, prise en main
exl-id: 0da96e32-52ad-4cc3-bac4-844b1f39ed16
source-git-commit: 2240a4bf85d3f5f41a12d128afdc15431dbab75b
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 23%

---

# Prise en main des pages de destination {#get-started-lp}

Une page de destination est une page web autonome sur laquelle l’utilisateur arrive après avoir cliqué sur un lien présent dans un e-mail, un site Web, une publicité ou tout autre emplacement numérique.

[!DNL Journey Optimizer] vous permet de créer et de concevoir des pages de destination pour diriger vos utilisateurs vers des formulaires en ligne où ils peuvent s’inscrire ou se désinscrire de la réception de vos communications ou d’un service spécifique tel qu’une newsletter.

➡️ [Découvrez la configuration des abonnements et la création de pages de destination dans cette vidéo.](#video)

## Quand utiliser les pages de destination {#when-to-use}

Utilisez les pages de destination lorsque vous souhaitez :

* Autoriser les clients **opt-in ou opt-out** à utiliser des communications marketing ou un service ou une newsletter spécifique à partir d’un lien dans un e-mail ou une campagne, y compris des listes d’abonnement pour les services ciblés. [En savoir plus](lp-use-cases.md#subscription-to-a-service)
* **Collectez le consentement** avant d’envoyer des communications et envoyez un **e-mail de confirmation** lors de l’opt-in ou de l’opt-out. [En savoir plus](lp-use-cases.md#send-confirmation-email)
* Rediriger les utilisateurs vers un **formulaire web dédié** sans créer de page externe en dehors de [!DNL Journey Optimizer]
* Créer des **pages de destination réactives** à l’aide des fonctionnalités de conception de contenu d’[!DNL Journey Optimizer]

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-lp.md">
<img alt="Lead" src="../assets/do-not-localize/lp-subscription.jpeg">
</a>
<div><a href="create-lp.md"><strong>Créer des pages de destination</strong>
</div>
<p>
</td>
<td>
<a href="subscription-list.md">
<img alt="Peu fréquent" src="../assets/do-not-localize/lp-list.jpg">
</a>
<div>
<a href="subscription-list.md"><strong>Créer des listes d’abonnements</strong></a>
</div>
<p></td>
<td>
<a href="design-lp.md">
<img alt="Validation" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="design-lp.md"><strong>Concevoir des pages de destination</strong></a>
</div>
<p>
</td>
<td>
<a href="../reports/lp-report-live.md">
<img alt="Validation" src="../assets/do-not-localize/lp-reporting.jpg">
</a>
<div>
<a href="../reports/lp-report-live.md"><strong>Créer des rapports</strong></a>
</div>
<p>
</td>
</tr></table>

## Avant de commencer {#prerequisites}

Avant de créer une page de destination, procédez comme suit :

1. [**Configurer un sous-domaine**](lp-subdomains.md) — Configurez un sous-domaine dédié à l&#39;hébergement de vos pages de destination.
1. [**Créer un préréglage de page de destination**](lp-presets.md#lp-create-preset) — Un préréglage définit le sous-domaine et les autres paramètres appliqués à vos pages de destination.
1. [**Créer une liste d’abonnements**](subscription-list.md) (pour les cas d’utilisation d’abonnement) : cette option est obligatoire si vous souhaitez que les clients s’abonnent ou se désabonnent d’un service spécifique.

## Fonctionnement {#how-it-works}

La création et le déploiement d’une landing page s’effectuent comme suit :

1. [**Créer et configurer votre page de destination**](create-lp.md) — Sélectionnez un préréglage, configurez la page principale et ajoutez toutes les sous-pages requises.
1. [**Concevoir la page**](design-lp.md) — Créez le contenu et le formulaire de la page à l’aide de l’éditeur glisser-déposer de [!DNL Journey Optimizer].
1. [**Tester**](create-lp.md#test-landing-page) et [**publier**](create-lp.md#publish-landing-page) votre page de destination : prévisualisez la page, testez le comportement du formulaire, puis publiez pour la rendre active.
1. [**Lien dans un message ou un parcours**](../email/message-tracking.md#insert-links) — Ajoutez l’URL de la page de destination à un e-mail, une campagne ou une action de parcours pour que les clients puissent l’atteindre.

## Vidéo pratique{#video}

La vidéo ci-dessous montre comment créer une liste d’abonnements, configurer des pages de destination pour l’opt-in ou l’opt-out à un service, intégrer l’option d’opt-in/opt-out à un message et configurer des parcours pertinents.

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)
