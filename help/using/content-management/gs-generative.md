---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec l’Assistant IA
description: Découvrez comment accéder à l’Assistant IA de Journey Optimizer et l’utiliser.
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Version Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 644e0959ee0d0ec8ee0c4ec54c3bcd1cc3c4dda9
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 85%

---

# Commencer avec l’Assistant IA {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Assistant IA"
>abstract="Une fois que vous avez conçu et personnalisé votre diffusion, vous pouvez utiliser l’assistant IA pour améliorer votre contenu. Cette fonctionnalité simplifie le processus de personnalisation et d’amélioration du contenu en vous permettant d’affiner le contenu en décrivant ce que vous souhaitez générer."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Définition du contexte avec l’assistant d’IA"
>abstract="Pour utiliser le contenu sélectionné comme entrée pour la génération du contenu, activez la variable **Utiliser le contenu d’origine** bascule. Vous pouvez également charger vos ressources de marque pour les utiliser comme source. Si vous n’utilisez pas le contenu sélectionné, le chargement et la sélection de ressources de marque sont obligatoires."


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Termes de l’IA générative d’Adobe"
>abstract="L’accès à cette fonctionnalité est soumis à votre acceptation des directives d’utilisation de l’IA générative d’Adobe Experience Cloud. Les prompts, les informations contextuelles ou supplémentaires, ou toute autre information que vous saisissez dans cette fonctionnalité, doivent être liées à un contexte spécifique, ce qui peut inclure vos éléments de marque, le contenu de votre site web, vos données, les schémas de ces données, vos modèles ou autres documents approuvés, et ne doit pas contenir d’informations personnelles (les informations personnelles incluent tout ce qui peut être associé à une personne spécifique). Vous devez vérifier la conformité des résultats produits par cette fonctionnalité et vous assurer qu’ils sont adaptés à votre cas d’utilisation."
>additional-url="https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Directives à l’intention des utilisateurs de l’IA générative Adobe"

>[!BEGINSHADEBOX]

**Table des matières**

* Commencer avec l’Assistant IA
* [Génération d’e-mails avec l’assistant IA](generative-email.md)
* [Génération de SMS avec l’assistant IA](generative-sms.md)
* [Génération des notifications push à l’aide de l’assistant d’IA](generative-push.md)
* [Expérience de contenu avec l’assistant d’IA](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>L’assistant d’IA dans Adobe Journey Optimizer est actuellement disponible en version bêta pour sélectionner uniquement les utilisateurs.

L’assistant IA d’Adobe Journey Optimizer offre des suggestions proactives de variations de contenu pour le texte et les images. Il est disponible pour les canaux email, push et SMS. Cette nouvelle fonctionnalité permet de générer rapidement du texte et des images. La génération d’images est gérée avec Adobe Firefly.

Utilisez l’Assistant IA dans Journey Optimizer pour optimiser l’impact de votre message en testant plusieurs images et titres principaux. Générez plusieurs variantes et créez une expérience pour les comparer. L’expérience de contenu Journey Optimizer vous permet de définir plusieurs traitements de message afin de mesurer celui qui fonctionne le mieux pour votre audience cible. Vous pouvez choisir de varier le contenu ou l’objet de la diffusion. L’audience du message est attribuée de manière aléatoire à chaque traitement afin de déterminer laquelle fonctionne le mieux avec la mesure spécifiée. En savoir plus sur l’expérience de contenu dans [cette section](../campaigns/content-experiment.md).

## Mécanismes de sécurisation et limitations {#generative-guardrails}

Les instructions générales pour l’utilisation de l’assistant d’IA dans Journey Optimizer pour la génération d’emails sont répertoriées ci-dessous :

* La qualité du contenu généré est fortement influencée par l’invite/l’objectif marketing que vous définissez. Utilisez une invite bien définie pour que le modèle GenAI soit interprété avec précision. 
* Chargez les ressources de marque pour qu’elles soient précises sur le contenu de la marque. Autrement, le contenu est basé sur des informations disponibles au public. Le contenu chargé peut se présenter dans les formats suivants : fichiers PDF, JPEG, PNG ou ZIP (avec les formats de fichiers pris en charge).
* La taille maximale pour la ressource de marque chargée est de 50 Mo.Des fichiers plus volumineux ou de nombreuses images peuvent faire l’objet d’un traitement, mais le temps de traitement sera plus long.
* Utilisez des modèles d’e-mails créés par Adobe Campaign, ou de préférence des [modèles d’e-mails intégrés](../email/use-email-templates.md), un modèle de marque spécifique ou un modèle personnalisé pour créer le contenu de votre e-mail. Il est recommandé d’utiliser un modèle d’e-mail contenant jusqu’à 8-10 images.
* Veillez à signaler les sorties problématiques à l’aide des icônes de pouce vers le haut, de pouce vers le bas ou d’indicateur lors de la sélection de variantes.
* Votre utilisation de l’assistant IA est soumise aux directives d’utilisation de l’IA générative d’Adobe Experience Cloud. [En savoir plus](https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

Les restrictions suivantes s’appliquent à l’assistant d’IA dans Journey Optimizer :

* La seule langue prise en charge est l’anglais.
* Uniquement disponible pour les canaux e-mail, push et SMS.
* Il est possible que le contenu de GenAI ne soit pas toujours précis : envoyez-nous vos commentaires pour que nos ingénieures et ingénieurs puissent affiner les modèles.
* Vous pouvez charger plusieurs ressources de marque, mais vous ne pouvez en utiliser qu’une seule pour une génération spécifique.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="Génération d’e-mails" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong>Génération d'emails</strong></a>
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
<a href="generative-push.md"><strong>Génération des notifications push</strong></a>
</div>
<p></td>
</tr></table>
