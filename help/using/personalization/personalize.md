---
solution: Journey Optimizer
product: journey optimizer
title: Personnalisation du contenu dans Journey Optimizer
description: Commencez avec la personnalisation.
feature: Personalization
topic: Personalization
role: Developer
level: Beginner
keywords: expression, éditeur, commencer, personnalisation
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1403
ht-degree: 40%

---

# Prise en main de la personnalisation{#add-personalization}

>[!BEGINSHADEBOX]

**Sur cette page :** Prise en main de la personnalisation dans Adobe Journey Optimizer, y compris le fonctionnement de l’éditeur de personnalisation, les données de profil que vous pouvez utiliser, le terrain de jeu d’apprentissage et la modification en ligne.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="Personnaliser des expériences"
>abstract="Utilisez **Adobe Journey Optimizer** pour adapter vos messages à chaque personne destinataire spécifique en exploitant les données et informations que vous possédez à son sujet. Il peut s’agir de son prénom, de ses centres d’intérêt, de son lieu de résidence, de ses achats, etc."

Les fonctionnalités de personnalisation d’[!DNL Adobe Journey Optimizer] vous permettent d’adapter vos messages à chaque destinataire en exploitant les données et informations que vous possédez à son sujet. Il peut s’agir de son prénom, de ses centres d’intérêt, de son lieu de résidence, de ses achats, etc.

## Fonctionnement de la personnalisation

Grâce à l’**éditeur de personnalisation**, vous pouvez sélectionner, organiser, personnaliser et valider toutes les données afin de personnaliser le contenu et utiliser divers outils tels que des fonctions d’assistance ou des expressions prédéfinies pour personnaliser efficacement les messages.

Journey Optimizer utilise une syntaxe de personnalisation intégrée basée sur Handlebars, qui vous permet de créer des expressions avec du contenu encadré par des accolades doubles **`{{}}`**.

Lors du traitement du message, Journey Optimizer remplace l’expression par les données contenues dans le jeu de données Experience Platform. Par exemple, `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` devient `Hello John Doe` de manière dynamique. Cette syntaxe vous permet de personnaliser des messages dans plusieurs champs, notamment l’objet des e-mails, le corps des messages, les notifications push ou les URL.

## Données utilisées pour la personnalisation

La personnalisation est basée sur les données de profil gérées par le schéma **Profil individuel XDM** défini dans Adobe Experience Platform. Le schéma **Profil individuel XDM** est le seul que vous pouvez utiliser pour personnaliser le contenu dans [!DNL Journey Optimizer]. Pour en savoir plus, consultez la [documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"}.

Vous pouvez également utiliser les **attributs calculés** pour personnaliser le contenu. Les attributs calculés vous permettent de résumer des événements comportementaux individuels en attributs de profil calculés disponibles sur Adobe Experience Platform. [Découvrir comment utiliser les attributs calculés](../audience/computed-attributes.md)

En outre, [!DNL Journey Optimizer] vous permet d’utiliser les données d’Adobe Experience Platform dans l’éditeur de personnalisation pour personnaliser le contenu. Pour ce faire, les jeux de données nécessaires à la personnalisation de la recherche doivent d’abord être activés par le biais d’un appel API. Après cela, vous pouvez utiliser les données pour personnaliser le contenu dans Journey Optimizer. Cette fonctionnalité est actuellement disponible en version Beta. [En savoir plus](../personalization/aep-data-perso.md)

## Découvrez et testez la personnalisation. {#playground}

**[!DNL Adobe Journey Optimizer]** comprend un outil interactif conçu pour vous aider à apprendre et à tester les fonctionnalités de personnalisation.

Ce terrain de jeu fournit un environnement simulé pour écrire et tester du code de personnalisation à l’aide de données d’exemple sans nécessiter de jeux de données actifs. Vous pouvez tirer parti des exemples de code prédéfinis, modifier les payloads de profil factices et prévisualiser la sortie de votre code de personnalisation en temps réel.

![terrain de jeu de personnalisation](assets/playground.png)

➡️ [Accédez au terrain de jeu de la personnalisation.](https://experienceleague.adobe.com/fr/apps/journey-optimizer/ajo-personalization){target="_blank"}

## Assistant IA pour les expressions de personnalisation {#ai-personalization-expressions}

Dans l’**[!UICONTROL Éditeur]** ou dans la barre d’outils Designer d’e-mail (**[!UICONTROL Ajouter une expression]**), l’**[!UICONTROL Assistant AI]** vous aide à générer de nouvelles expressions à partir du langage naturel, à expliquer la fonction du code existant et à résoudre les problèmes d’une sélection, puis à appliquer la sortie lorsqu’elle correspond à votre intention.

![](../content-management/assets/ai-perso-generate.png)

➡️ [Découvrez comment utiliser l’assistant AI pour les expressions Personalization](../content-management/generative-personalization-expressions.md)

## Modification en ligne des attributs de profil {#inline-personalization}

Vous pouvez insérer des expressions d’attribut de profil directement lors de la modification du contenu dans l’éditeur **Email Designer** ou **Canal push**, sans ouvrir l’éditeur de personnalisation complet.

Pour ce faire, procédez comme suit :

1. Saisissez `{{` dans un champ de texte. Une liste déroulante de saisie automatique intégrée s’ouvre à l’emplacement du curseur.
1. Commencez la saisie pour filtrer les attributs de profil disponibles.
1. Sélectionnez l’attribut dont vous avez besoin : il est inséré en tant que jeton de personnalisation à la position du curseur.

![](assets/inline-profile-attributes.png)

## Explorons plus en détail.

Maintenant que vous savez comment effectuer des personnalisations dans **[!DNL Journey Optimizer]**, il est temps d’examiner plus en détail ces sections de documentation pour commencer à utiliser cette fonctionnalité.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="personalization-build-expressions.md">
<img alt="Ajouter une personnalisation" src="assets/do-not-localize/add.png">
</a>
<div>
<a href="personalization-build-expressions.md"><strong>Ajouter une personnalisation</strong></a>
</div>
<p>
</td>
<td>
<a href="../personalization/personalization-syntax.md">
<img alt="Lead" src="assets/do-not-localize/syntax.png">
</a>
<div><a href="../personalization/personalization-syntax.md"><strong>Syntaxe de personnalisation</strong>
</div>
<p>
</td>
<td>
<a href="../personalization/functions/functions.md">
<img alt="Peu fréquent" src="assets/do-not-localize/functions.png">
</a>
<div>
<a href="../personalization/functions/functions.md"><strong>Liste des fonctions d’assistance</strong></a>
</div>
<p></td>
<td>
<a href="../personalization/personalization-recipes.md">
<img alt="Peu fréquent" src="assets/do-not-localize/uc.png">
</a>
<div>
<a href="../personalization/personalization-recipes.md"><strong>recettes </strong></a>
</div>
<p></td>
<td>
<a href="../personalization/personalization-use-case.md">
<img alt="Peu fréquent" src="assets/do-not-localize/uc.png">
</a>
<div>
<a href="../personalization/personalization-use-case.md"><strong>Cas d’utilisation de la personnalisation</strong></a>
</div>
<p></td>
</tr></table>

## Vidéos pratiques{#video-perso}

Découvrez comment utiliser les informations d’événement contextuelles d’un parcours pour personnaliser un message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Découvrez comment ajouter une personnalisation basée sur un profil à un message et comment utiliser l’appartenance à une audience comme condition préalable à un bloc de personnalisation.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

Découvrez comment tirer parti du terrain de jeu de l’éditeur de personnalisation pour écrire et tester du code de personnalisation à l’aide de données d’exemple.

>[!VIDEO](https://video.tv.adobe.com/v/3457868?quality=12)

Découvrez d’autres tutoriels vidéo sur les fonctionnalités de personnalisation et les bonnes pratiques dans les [tutoriels sur la personnalisation](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/personalize-content/personalization-editor-overview){target="_blank"}.

## Référence rapide {#quick-reference}

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

>[!BEGINTABS]

>[!TAB Vue d’ensemble]

**TL;DR**

Cette page présente la personnalisation dans Journey Optimizer : le fonctionnement de l’éditeur de personnalisation basé sur Handlebars, les données qu’il utilise, le terrain de jeu interactif, l’assistant AI pour les expressions et la modification des attributs intégrés dans l’éditeur de Designer d’e-mail et de notification push.

**Intentions**

* Comprendre le fonctionnement de la personnalisation Journey Optimizer (syntaxe Handlebars avec des accolades doubles)
* Identifier les sources de données disponibles pour la personnalisation (schéma de profil individuel XDM, attributs calculés, recherche de jeu de données AEP en version bêta)
* Testez la personnalisation à l’aide du terrain de jeu interactif sans sandbox en direct
* Utilisez l’assistant AI pour générer, expliquer ou corriger des expressions de personnalisation à partir du langage naturel
* Insérez des attributs de profil intégrés dans le Designer d’e-mail ou l’éditeur push en saisissant `{{`

>[!TAB Glossaire]

* **Éditeur Personalization** : outil complet permettant de créer, de personnaliser et de valider des expressions de personnalisation ; disponible dans n’importe quel champ Journey Optimizer prenant en charge la personnalisation. *(spécifique au produit)*
* **Schéma de profil individuel XDM** : le seul schéma qui peut être utilisé pour personnaliser le contenu dans Journey Optimizer ; définit tous les attributs de profil disponibles pour la personnalisation. *(spécifique au produit)*
* **Attributs calculés** : attributs de profil précalculés résumant les événements comportementaux individuels en valeurs au niveau du profil ; disponibles en tant que données de personnalisation avec les champs de profil XDM standard. *(spécifique au produit)*
* **Personalization playground** : environnement interactif et simulé sur Experience League pour écrire et tester du code de personnalisation avec des exemples de données. Aucun jeu de données actif ou sandbox n’est requis. *(spécifique au produit)*
* **Modification en ligne** : possibilité de saisir du `{{` dans n’importe quel champ de texte de l’éditeur de canal Email Designer ou Push pour déclencher une liste déroulante de saisie automatique et insérer des attributs de profil sans ouvrir l’éditeur de personnalisation complet. *(spécifique au produit)*
* **Assistant AI (expressions de personnalisation)** : outil d’IA dans l’éditeur de personnalisation et le Designer d’e-mail qui génère des expressions de personnalisation à partir du langage naturel, explique le code existant et corrige les problèmes d’une sélection. *(spécifique au produit)*

>[!TAB  Terminologie ]

* **Nom canonique : personnalisation** — variantes : personnalisation de contenu, personnalisation de message, personnalisation d’expression
* **Nom canonique :** éditeur de personnalisation — variantes : fonctionnalités de personnalisation
* **Ne pas confondre :** l’éditeur Personalization (utilisé pour créer des expressions de contenu dans les messages et les offres, prend en charge à la fois Handlebars et PQL) ≠ l’éditeur d’expression avancé (utilisé dans le parcours pour les conditions sur les sources de données et les informations d’événement, les activités d’attente personnalisées et le mappage des paramètres d’action) fournit des fonctions et des opérateurs intégrés qui diffèrent de ceux de l’éditeur de personnalisation
* **Ne pas confondre :** modification en ligne (saisissez `{{` dans Email Designer ou Push pour l’insertion rapide d’attributs sans ouvrir l’éditeur complet) ≠ éditeur de personnalisation (outil complet pour les expressions complexes, les fonctions d’assistance, les règles conditionnelles et les fragments)
* **Ne les confondez pas :** schéma Profil individuel XDM (le seul utilisable pour la personnalisation dans Journey Optimizer) ≠ d’autres schémas AEP (non utilisables pour la personnalisation, sauf s’ils sont exposés via la recherche de jeu de données)

>[!TAB Mécanismes de sécurisation et limitations]

* Le schéma Profil individuel XDM est le seul qui peut être utilisé pour personnaliser le contenu dans Journey Optimizer.
* La recherche de jeux de données AEP pour la personnalisation nécessite que les jeux de données soient activés par le biais d’un appel API avant utilisation. Cette fonctionnalité est actuellement en version bêta.
* La modification en ligne (saisie de `{{` dans Email Designer ou l’éditeur push) prend uniquement en charge les attributs de profil.

>[!TAB FAQ]

**Q : Quelles données peuvent être utilisées pour la personnalisation dans Journey Optimizer ?**

Les données de profil du schéma Profil individuel XDM, les attributs calculés (événements comportementaux résumés au niveau du profil) et la recherche de jeu de données d’enregistrement AEP (actuellement en version bêta : les jeux de données doivent être activés via l’API).

**Q : Quel est le terrain de jeu de la personnalisation ?**

Un environnement interactif et simulé sur Experience League où vous pouvez écrire et tester du code de personnalisation à l’aide de données d’exemple, sans avoir besoin d’un sandbox Journey Optimizer actif ou de jeux de données réels.

**Q : Comment fonctionne la modification d’attributs intégrée ?**

Saisissez `{{` dans un champ de texte de l’éditeur de canal Email Designer ou Push pour ouvrir une liste déroulante de saisie automatique à l’emplacement du curseur. Commencez à saisir pour filtrer les attributs de profil, puis sélectionnez-en un pour l’insérer en tant que jeton de personnalisation. Seuls les attributs de profil sont disponibles en ligne.

**Q : Que peut faire l’assistant AI dans l’éditeur de personnalisation ?**

Il peut générer de nouvelles expressions de personnalisation à partir de descriptions en langage naturel, expliquer ce que fait le code existant et résoudre des problèmes dans une expression sélectionnée, puis appliquer la sortie lorsqu’elle correspond à votre intention.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 248b894f -->
