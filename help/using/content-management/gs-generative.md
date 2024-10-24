---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec l’assistant IA dans l’accélérateur de contenu Journey Optimizer
description: Découvrir comment accéder à l’assistant IA et l’utiliser dans l’accélérateur de contenu Journey Optimizer
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: f316ec79958ac23e0e416f0cafd49c017f2b6d4c
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 72%

---

# Commencer avec l’accélérateur de contenu de l’assistant IA {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Accélérateur de contenu de l’assistant AI dans Journey Optimizer"
>abstract="Une fois que vous avez conçu et personnalisé votre diffusion, vous pouvez utiliser l’accélérateur de contenu de l’assistant d’IA dans Journey Optimizer pour améliorer votre contenu. Cette fonctionnalité simplifie le processus de personnalisation et d’amélioration du contenu en vous permettant d’affiner le contenu à travers la description de ce que vous souhaitez générer."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Charger une ressource de marque"
>abstract="Le menu Charger des ressources de marque permet d’ajouter toute ressource de marque contenant du contenu pouvant fournir un contexte supplémentaire à l’accélérateur de contenu de l’assistant d’IA dans Journey Optimizer ou de sélectionner une ressource précédemment chargée. Cette option permet de s’assurer que l’Assistant IA a accès à tous les supports nécessaires pour améliorer ses fonctionnalités et sa pertinence."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Conditions de l’IA Generative d’Adobe"
>abstract="L’accès à cette fonctionnalité est soumis à votre accord des directives d’utilisation de l’IA générative d’Adobe Experience Cloud. Vous devez vérifier la précision des résultats produits par cette fonctionnalité et vous assurer qu’ils sont adaptés à votre cas d’utilisation."
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Directives d’utilisation de l’IA générative d’Adobe"

>[!INFO]
>
>Découvrez une expérience pratique avec [notre aperçu des fonctionnalités en direct](https://experienceleague.adobe.com/fr/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"}, conçu pour vous permettre d’explorer directement ses fonctionnalités et de les comprendre pleinement.


L’accélérateur de contenu de l’assistant d’IA dans Adobe Journey Optimizer, optimisé par Microsoft Azure OpenAI et Adobe Firefly, offre des suggestions proactives de variations de contenu pour le texte et les images. Il est disponible pour les canaux e-mail, notification push et SMS. Cette nouvelle fonctionnalité permet de générer rapidement du texte et des images. La génération d’images est gérée avec Adobe Firefly.

Utilisez l’accélérateur de contenu de l’assistant d’IA dans Adobe Journey Optimizer pour optimiser l’impact de votre message en testant différents titres et images principaux. Générez plusieurs variantes et créez une expérience pour les comparer. L’expérience de contenu Journey Optimizer vous permet de définir plusieurs traitements de message afin de mesurer celui qui fonctionne le mieux pour votre audience cible. Vous pouvez choisir de varier le contenu ou l’objet de la diffusion. L’audience du message est attribuée de manière aléatoire à chaque traitement afin de déterminer laquelle fonctionne le mieux avec la mesure spécifiée. En savoir plus sur l’expérience de contenu dans [cette section](../content-management/content-experiment.md).

>[!IMPORTANT]
>
>* Avant de commencer à utiliser cette fonctionnalité, lisez la section connexe [Mécanismes de sécurisation et limitations](#generative-guardrails).
>
>
>* Vous devez accepter un [ accord utilisateur](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} avant de pouvoir utiliser l’accélérateur de contenu de l’assistant d’IA dans Adobe Journey Optimizer. Pour en savoir plus, contactez votre représentant ou représentante Adobe.

## Accéder à l’accélérateur de contenu de l’assistant IA {#generative-access}

Pour accéder à la fonctionnalité Accélérateur de contenu de l’assistant d’IA dans Adobe Journey Optimizer, les utilisateurs doivent se voir accorder l’autorisation **Générer le contenu**. [En savoir plus](../administration/permissions.md)

+++  Découvrir comment attribuer des autorisations liées à la génération de contenu

1. Dans le produit **Autorisations**, accédez à l’onglet **Rôles** et sélectionnez le **Rôle** de votre choix.

1. Cliquez sur **Modifier** pour modifier les autorisations.

1. Ajoutez la ressource **Assistant IA**, puis sélectionnez **Générer le contenu** dans le menu déroulant.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. Cliquez sur **Enregistrer** pour appliquer vos modifications.

   Les autorisations des personnes déjà affectées à ce rôle seront automatiquement mises à jour.

1. Pour attribuer ce rôle à de nouvelles personnes, accédez à l’onglet **Utilisateurs et utilisatrices** du tableau de bord **Rôles** et cliquez sur **Ajouter un utilisateur ou une utilisatrice**.

1. Saisissez le nom de la personne, son adresse e-mail ou choisissez dans la liste, puis cliquez sur **Enregistrer**.

1. Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez cette [documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/abac/permissions-ui/users).

La personne recevra un e-mail avec des instructions pour accéder à votre instance.

+++

## Mécanismes de sécurisation et limitations {#generative-guardrails}

Les instructions générales pour l’utilisation de l’accélérateur de contenu de l’assistant d’IA dans Adobe Journey Optimizer pour la génération de courriers électroniques sont répertoriées ci-dessous :

* La qualité du contenu généré est fortement influencée par l’objectif/l’invite marketing que vous définissez. Utilisez une invite bien définie pour que le modèle GenAI soit correctement interprété. 
* Chargez les ressources de marque pour disposer de contenu exact sur la marque. Sinon, le contenu est basé sur des informations disponibles publiquement. Le contenu chargé peut se présenter sous les formats suivants : fichiers PDF, JPEG, PNG ou ZIP (avec les formats de fichiers pris en charge).
* La taille maximale des ressources de marque chargées est de 50 Mo. Des fichiers plus volumineux ou un grand nombre d’images peuvent être utilisés, mais le temps de traitement est plus long.
* Utilisez un modèle personnalisé ou spécifique à la marque pour créer votre contenu d’email à l’aide de l’accélérateur de contenu de l’assistant d’IA dans Adobe Journey Optimizer. Il est recommandé d’utiliser un modèle d’e-mail contenant jusqu’à 8 à 10 images.
* Veillez à signaler tout résultat problématique à l’aide des icônes de pouce vers le haut, de pouce vers le bas ou de drapeau lors de la sélection de variantes.
* Votre utilisation de l’assistant d’IA est soumise aux directives utilisateur de Adobe Experience Cloud Generative AI. [En savoir plus](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Dans le cadre de l’engagement d’Adobe à promouvoir la transparence dans l’utilisation des outils d’IA générative dans la création de médias, Adobe appliquera Content Credentials lorsque le contenu ou un projet qui incluait une ressource générée par un Firefly est téléchargé ou exporté. [En savoir plus](https://helpx.adobe.com/fr/firefly/using/content-credentials.html)

Les restrictions suivantes s’appliquent à l’accélérateur de contenu de l’assistant d’IA dans Adobe Journey Optimizer :

* La langue prise en charge est uniquement l’anglais. Les entrées non anglaises peuvent produire des résultats incohérents ou erronés. Les questions découlant des réponses non anglaises ne seront pas traitées ni améliorées pour le moment.
* Uniquement disponible pour les canaux e-mail, notification push et SMS.
* Le contenu GenAI n’est peut-être pas toujours précis : partagez vos commentaires pour que nos ingénieures et ingénieurs puissent affiner les modèles.
* Vous pouvez charger plusieurs ressources de marque, mais vous ne pouvez en utiliser qu’une seule pour une génération spécifique.


## Fonctionnalités de génération de contenu de l’assistant IA {#generative-features}


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
<td>
<a href="generative-web.md">
<img alt="Génération web" src="assets/do-not-localize/web-genai.jpeg">
</a>
<div><a href="generative-web.md"><strong>Génération de pages web</strong>
</div>
<p>
</td>
</tr></table>
