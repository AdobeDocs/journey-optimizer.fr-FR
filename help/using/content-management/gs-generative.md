---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec l’assistant IA
description: Découvrez comment accéder à l’Assistant IA de Journey Optimizer et l’utiliser.
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Version bêta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 100%

---

# Commencer avec l’assistant IA {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Assistant IA"
>abstract="Une fois que vous avez conçu et personnalisé votre diffusion, vous pouvez utiliser l’assistant IA pour améliorer votre contenu. Cette fonctionnalité simplifie le processus de personnalisation et d’amélioration du contenu en vous permettant d’affiner le contenu en décrivant ce que vous souhaitez générer."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Définir le contexte avec l’assistant IA"
>abstract="Pour utiliser le contenu sélectionné comme entrée pour la génération du contenu, activez le bouton (bascule) **Utiliser le contenu original**. Vous pouvez également charger vos ressources de marque pour les utiliser comme source. Si vous n’utilisez pas le contenu sélectionné, le chargement et la sélection de ressources de marque sont obligatoires."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Conditions d’IA générative Adobe"
>abstract="L’accès à cette fonctionnalité est soumis à votre accord des directives d’utilisation de l’IA générative d’Adobe Experience Cloud. Les invites, les informations contextuelles ou supplémentaires, ou toute autre information que vous fournissez à cette fonctionnalité, doivent être liées à un contexte spécifique, qui peut inclure vos documents d’image de marque, le contenu du site web, les données, les schémas de ces données, modèles ou autres documents approuvés, et ne doit pas contenir d’informations personnelles (les informations personnelles incluent tout ce qui peut être lié à une personne spécifique). Vous devez vérifier l’exactitude des résultats de cette fonctionnalité et vous assurer qu’ils sont appropriés à votre cas d’utilisation."
>additional-url="https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Directives d’utilisation de l’IA générative d’Adobe"

>[!BEGINSHADEBOX]

**Table des matières**

* Commencer avec l’assistant IA
* [Génération d’e-mails avec l’assistant IA](generative-email.md)
* [Génération de SMS avec l’assistant IA](generative-sms.md)
* [Génération de notifications push avec l’assistant IA](generative-push.md)
* [Expérience de contenu avec l’assistant IA](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>L’assistant IA dans Adobe Journey Optimizer est actuellement disponible en version bêta pour certains utilisateurs et utilisatrices uniquement.

L’assistant IA dans Adobe Journey Optimizer offre des suggestions proactives de variations de contenu pour le texte et les images. Il est disponible pour les canaux e-mail, notification push et SMS. Cette nouvelle fonctionnalité permet de générer rapidement du texte et des images. La génération d’images est gérée avec Adobe Firefly.

Utilisez l’Assistant IA dans Journey Optimizer pour optimiser l’impact de votre message en testant plusieurs images et titres principaux. Générez plusieurs variantes et créez une expérience pour les comparer. L’expérience de contenu Journey Optimizer vous permet de définir plusieurs traitements de message afin de mesurer celui qui fonctionne le mieux pour votre audience cible. Vous pouvez choisir de varier le contenu ou l’objet de la diffusion. L’audience du message est attribuée de manière aléatoire à chaque traitement afin de déterminer laquelle fonctionne le mieux avec la mesure spécifiée. En savoir plus sur l’expérience de contenu dans [cette section](../content-management/content-experiment.md).

## Mécanismes de sécurisation et limitations {#generative-guardrails}

Vous trouverez ci-dessous des instructions générales concernant l’utilisation de l’assistant IA dans Journey Optimizer pour la génération d’e-mails :

* La qualité du contenu généré est fortement influencée par l’objectif/l’invite marketing que vous définissez. Utilisez une invite bien définie pour que le modèle GenAI soit correctement interprété. 
* Chargez les ressources de marque pour disposer de contenu exact sur la marque. Sinon, le contenu est basé sur des informations disponibles publiquement. Le contenu chargé peut se présenter sous les formats suivants : fichiers PDF, JPEG, PNG ou ZIP (avec les formats de fichiers pris en charge).
* La taille maximale des ressources de marque chargées est de 50 Mo. Des fichiers plus volumineux ou un grand nombre d’images peuvent être utilisés, mais le temps de traitement est plus long.
* Utilisez des modèles d’e-mail créés par Adobe Campaign, de préférence des [modèles d’e-mail intégrés](../email/use-email-templates.md), un modèle spécifique à la marque ou un modèle personnalisé, pour créer le contenu de votre e-mail. Il est recommandé d’utiliser un modèle d’e-mail contenant jusqu’à 8 à 10 images.
* Veillez à signaler tout résultat problématique à l’aide des icônes de pouce vers le haut, de pouce vers le bas ou de drapeau lors de la sélection de variantes.
* Votre utilisation de l’assistant IA est soumise aux directives d’utilisation de l’IA générative d’Adobe Experience Cloud. [En savoir plus](https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

Les restrictions suivantes s’appliquent à l’assistant IA dans Journey Optimizer :

* La seule langue prise en charge est l’anglais.
* Uniquement disponible pour les canaux e-mail, notification push et SMS.
* Le contenu GenAI n’est peut-être pas toujours précis : partagez vos commentaires pour que nos ingénieures et ingénieurs puissent affiner les modèles.
* Vous pouvez charger plusieurs ressources de marque, mais vous ne pouvez en utiliser qu’une seule pour une génération spécifique.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="Génération d’e-mails" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong>Génération d’e-mails</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="Génération de SMS" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong>Génération de SMS</strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="Génération de notifications push" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>Génération de notifications push</strong></a>
</div>
<p></td>
</tr></table>
