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
TQID: https://experienceleague.adobe.com/wr4XGNostKoN8jZ50VRAQPoGg9tsNhMOyJGEt1mASso
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b19d9237-76be-466d-a869-aacf2d72205f
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 712
ht-degree: 100%

---

# Prise en main des pages de destination {#get-started-lp}

Une page de destination est une page web autonome sur laquelle l’utilisateur arrive après avoir cliqué sur un lien présent dans un e-mail, un site Web, une publicité ou tout autre emplacement numérique.

[!DNL Journey Optimizer] vous permet de créer et de concevoir des pages de destination afin d’orienter vos utilisateurs et vos utilisatrices vers des formulaires en ligne qui permettent de s’abonner à vos communications ou à un service spécifique tel qu’une newsletter, ou de s’en désabonner.

➡️ [Découvrez la configuration des abonnements et la création de pages de destination dans cette vidéo.](#video)

## Quand utiliser les pages de destination {#when-to-use}

Utilisez les pages de destination dans les cas suivants :

* Autoriser les clientes et clients **à s’abonner ou à se désabonner** des communications marketing, d’un service spécifique ou d’une newsletter via un lien dans un e-mail ou une campagne, y compris des listes d’abonnement pour les services ciblés. [En savoir plus](lp-use-cases.md#subscription-to-a-service)
* **Obtenir le consentement** avant d’envoyer les communications et envoyer un **e-mail de confirmation** lors de l’abonnement ou du désabonnement. [En savoir plus](lp-use-cases.md#send-confirmation-email)
* **Capturer ou mettre à jour les données de profil** à l’aide de formulaires sur les pages de destination **[!UICONTROL Capture de données]** pour la création de profils utilisateur progressive, les préférences, les enregistrements et des scénarios similaires. [En savoir plus](#data-capture-lp)
* Rediriger les utilisateurs et utilisatrices vers un **formulaire web dédié** sans créer de page externe en dehors de [!DNL Journey Optimizer]
* Créer des **pages de destination réactives** à l’aide des fonctionnalités de conception de contenu de [!DNL Journey Optimizer]

### Capture de données via des pages de destination {#data-capture-lp}

Les pages de destination **[!UICONTROL Capture de données]** vous permettent d’incorporer des formulaires publiés afin que les visiteurs et visiteuses puissent envoyer des attributs enregistrés dans votre jeu de données [!DNL Adobe Experience Platform] par le biais de la connexion en streaming configurée dans votre préréglage de formulaire. [Découvrir comment créer et incorporer des formulaires dans une page de destination](lp-forms.md)

>[!NOTE]
>
>La capture de données par le biais de formulaires de page de destination est prise en charge pour les **profils connus** (profils existants identifiés dans [!DNL Adobe Experience Platform]). La page de destination doit être ouverte à partir d’un **lien personnalisé** (provenant par exemple d’une campagne par e-mail) afin que l’identité du profil puisse être reconnue lors du chargement de la page.

Voici des exemples de cas d’utilisation :

1. **Enrichissement progressif des profils** : collectez des attributs supplémentaires auprès de clientes et clients connus, tels que le numéro de téléphone, la date de naissance ou l’emplacement, au moyen d’une page de destination personnalisée afin d’enrichir leur profil [!DNL Experience Platform] existant à des fins de segmentation et de personnalisation.

2. **Mise à jour du centre de préférences** : permettez aux personnes abonnées connues de gérer leurs préférences de communication (canal, centres d’intérêt) via une page de destination. Les modifications sont généralement prises en compte sur leur profil [!DNL Experience Platform] dans un délai de 15 minutes environ.

3. **Inscription à un événement ou à un webinaire** : capturez des données spécifiques à un événement à partir de profils connus sur une page d’inscription, mettez à jour le profil avec des attributs d’inscription et déclenchez un parcours de confirmation.

4. **Inscription à des offres de fidélité ou à différents programmes** : autorisez les clientes et clients existants à s’inscrire à des programmes de fidélité ou d’adhésion en envoyant des informations supplémentaires via une page de destination, ce qui enrichit le profil pour le ciblage en aval.

5. **Participation à un concours ou à un tirage au sort** : laissez les clientes et clients connus participer à des concours ou à des tirages au sort via un formulaire de page de destination, capturez les détails spécifiques à leur participation (réponses, préférences ou déclarations) et enregistrez-les dans le profil pour faciliter l’éligibilité, la sélection des gagnantes et gagnants et les parcours de suivi.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-lp.md">
<img alt="Lead" src="../assets/do-not-localize/lp-subscription.jpeg">
</a>
<div><a href="create-lp.md"><strong>Créer des landing pages</strong>
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
<img alt="Liste de formulaires pour les pages de destination dans Journey Optimizer" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>Utiliser des formulaires dans vos pages de destination</strong></a>
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

Avant de créer une page de destination, procédez comme suit :

1. **Configurer un sous-domaine** : configurez un sous-domaine dédié à l’hébergement de vos pages de destination. [En savoir plus](lp-subdomains.md)
1. **Créer un préréglage de page de destination** : un préréglage définit le sous-domaine et les autres paramètres appliqués à vos pages de destination. [En savoir plus](lp-presets.md#lp-create-preset)
1. **Créer une liste d’abonnements** (pour les cas d’utilisation d’abonnement) : cette option est obligatoire si vous souhaitez que les clientes et clients s’abonnent ou se désabonnent d’un service spécifique. [En savoir plus](subscription-list.md)
1. **Créer un formulaire** (pour les cas d’utilisation de capture de données) : obligatoire lorsque vous souhaitez incorporer un formulaire sur une page de destination **[!UICONTROL Capture de données]** et transmettre les envois à [!DNL Experience Platform]. [En savoir plus](lp-forms.md)

## Fonctionnement {#how-it-works}

La création et le déploiement d’une page de destination s’effectuent comme suit :

1. **Créer et configurer votre page de destination** : sélectionnez un préréglage, configurez la page principale et ajoutez toutes les sous-pages requises. [En savoir plus](create-lp.md#create-landing-page)
1. **Concevoir la page** : créez le contenu de la page et le formulaire à l’aide de l’éditeur glisser-déposer de [!DNL Journey Optimizer]. [En savoir plus](design-lp.md)
1. **Tester et publier votre page de destination** : prévisualisez la page, testez le comportement du formulaire, puis publiez-la pour la mettre en ligne. [En savoir plus](create-lp.md#test-landing-page)
1. **Ajouter un lien dans un message ou un parcours** : ajoutez l’URL de la page de destination à un e-mail, à une campagne ou à une action de parcours pour que les clientes et clients puissent y accéder. [En savoir plus](../email/message-tracking.md#insert-links)

## Vidéo pratique{#video}

La vidéo ci-dessous montre comment créer une liste d’abonnements, configurer des pages de destination permettant de s’abonner à un service ou de s’en désabonner, intégrer l’option d’abonnement ou de désabonnement à un message et configurer les parcours pertinents.

>[!VIDEO](https://video.tv.adobe.com/v/344398?captions=fre_fr&quality=12&learn=on)
