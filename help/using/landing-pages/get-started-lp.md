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
source-git-commit: d0dd382521aeb2c7e18dc547c2ec55fa1472ab8d
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 14%

---

# Prise en main des pages de destination {#get-started-lp}

Une page de destination est une page web autonome sur laquelle l’utilisateur arrive après avoir cliqué sur un lien présent dans un e-mail, un site Web, une publicité ou tout autre emplacement numérique.

[!DNL Journey Optimizer] vous permet de créer et de concevoir des pages de destination pour diriger vos utilisateurs vers des formulaires en ligne où ils peuvent s’inscrire ou se désinscrire de la réception de vos communications ou d’un service spécifique tel qu’une newsletter.

➡️ [Découvrez la configuration des abonnements et la création de pages de destination dans cette vidéo.](#video)

## Quand utiliser les pages de destination {#when-to-use}

Utilisez les pages de destination lorsque vous souhaitez :

* Autoriser les clients **opt-in ou opt-out** à utiliser des communications marketing ou un service ou une newsletter spécifique à partir d’un lien dans un e-mail ou une campagne, y compris des listes d’abonnement pour les services ciblés. [En savoir plus](lp-use-cases.md#subscription-to-a-service)
* **Collectez le consentement** avant d’envoyer des communications et envoyez un **e-mail de confirmation** lors de l’opt-in ou de l’opt-out. [En savoir plus](lp-use-cases.md#send-confirmation-email)
* **Capturez ou mettez à jour les données de profil** à l’aide de formulaires sur les pages de destination **[!UICONTROL Capture de données]** pour le profilage progressif, les préférences, les enregistrements et des scénarios similaires. [En savoir plus](#data-capture-lp)
* Rediriger les utilisateurs vers un **formulaire web dédié** sans créer de page externe en dehors de [!DNL Journey Optimizer]
* Créer des **pages de destination réactives** à l’aide des fonctionnalités de conception de contenu d’[!DNL Journey Optimizer]

### Capture de données avec pages de destination {#data-capture-lp}

Les pages de destination **[!UICONTROL capture de données]** vous permettent d’incorporer des formulaires publiés afin que les visiteurs puissent envoyer des attributs écrits dans votre jeu de données [!DNL Adobe Experience Platform] par le biais de la connexion en continu configurée dans votre paramètre prédéfini de formulaire. [Découvrez comment créer et incorporer des formulaires dans une page de destination](lp-forms.md)

>[!NOTE]
>
>La capture de données par le biais de formulaires de page de destination est prise en charge pour les **profils connus** (profils existants identifiés dans [!DNL Adobe Experience Platform]). La page de destination doit être ouverte à partir d’un **lien personnalisé** (provenant par exemple d’une campagne par e-mail) afin que l’identité du profil puisse être résolue au chargement de la page.

Voici des exemples de cas d’utilisation :

1. **Enrichissement progressif des profils** : collectez des attributs supplémentaires auprès de clients connus, tels que le numéro de téléphone, la date de naissance ou l’emplacement, au moyen d’une page de destination personnalisée afin d’enrichir leur profil de [!DNL Experience Platform] existant à des fins de segmentation et de personnalisation.

2. **Mise à jour du centre de préférences** - Permettre aux abonnés connus de gérer leurs préférences de communication (canal, centres d’intérêt) via une page de destination, les modifications étant généralement répercutées sur leur profil de [!DNL Experience Platform] en 15 minutes environ.

3. **Enregistrement d’événement ou de webinaire** — Capturez des données spécifiques à un événement à partir de profils connus sur une page d’enregistrement, mettez à jour le profil avec des attributs d’enregistrement et déclenchez un parcours de confirmation.

4. **Fidélité ou inscription au programme** — Autorisez les clients existants à s’inscrire à des programmes de fidélité ou à des niveaux d’abonnement en envoyant des détails supplémentaires par le biais d’une page de destination, ce qui enrichit le profil pour le ciblage en aval.

5. **Participation à un concours ou à un concours** — Laissez les clients connus participer à des concours ou à des tirages au sort au moyen d&#39;un formulaire de page de destination, capturez les détails spécifiques à l&#39;inscription (réponses, préférences ou déclarations) et écrivez-les dans le profil pour prendre en charge l&#39;éligibilité, la sélection des gagnants et les parcours de suivi.

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
<a href="lp-forms.md">
<img alt="Liste Forms des pages de destination dans Journey Optimizer" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>Utilisation de formulaires dans vos pages de destination</strong></a>
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

1. **Configurer un sous-domaine** — Configurez un sous-domaine dédié à l&#39;hébergement de vos pages de destination. [En savoir plus](lp-subdomains.md)
1. **Créer un préréglage de page de destination** — Un préréglage définit le sous-domaine et les autres paramètres appliqués à vos pages de destination. [En savoir plus](lp-presets.md#lp-create-preset)
1. **Créer une liste d’abonnements** (pour les cas d’utilisation d’abonnement) : cette option est obligatoire si vous souhaitez que les clients s’abonnent ou se désabonnent d’un service spécifique. [En savoir plus](subscription-list.md)
1. **Créer un formulaire** (pour les cas d’utilisation de capture de données) : cette option est obligatoire lorsque vous souhaitez incorporer un formulaire sur une page de destination **[!UICONTROL capture de données]** et envoyer des envois à [!DNL Experience Platform]. [En savoir plus](lp-forms.md)

## Fonctionnement {#how-it-works}

La création et le déploiement d’une landing page s’effectuent comme suit :

1. **Créer et configurer votre page de destination** — Sélectionnez un préréglage, configurez la page principale et ajoutez toutes les sous-pages requises. [En savoir plus](create-lp.md#create-landing-page)
1. **Concevoir la page** — Créez le contenu et le formulaire de la page à l’aide de l’éditeur glisser-déposer de [!DNL Journey Optimizer]. [En savoir plus](design-lp.md)
1. **Tester et publier votre page de destination** — Prévisualisez la page, testez le comportement du formulaire, puis publiez pour la rendre active. [En savoir plus](create-lp.md#test-landing-page)
1. **Lien dans un message ou un parcours** — Ajoutez l’URL de la page de destination à un e-mail, une campagne ou une action de parcours pour que les clients puissent l’atteindre. [En savoir plus](../email/message-tracking.md#insert-links)

## Vidéo pratique{#video}

La vidéo ci-dessous montre comment créer une liste d’abonnements, configurer des pages de destination pour l’opt-in ou l’opt-out à un service, intégrer l’option d’opt-in/opt-out à un message et configurer des parcours pertinents.

>[!VIDEO](https://video.tv.adobe.com/v/344398?captions=fre_fr&quality=12&learn=on)
