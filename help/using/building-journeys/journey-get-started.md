---
solution: Journey Optimizer
product: journey optimizer
title: Guide complet - Journey Orchestration
description: Guide complet de prise en main de l’orchestration des parcours dans Adobe Journey Optimizer
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
keywords: parcours, orchestration, prise en main, intégration, fonctionnalités
source-git-commit: d1fd0b60ae60c2642108a1eb308564c9d04f5f9e
workflow-type: ht
source-wordcount: '851'
ht-degree: 100%

---


# Guide complet - Journey Orchestration{#journey-orchestration-guide}

Dans Adobe Journey Optimizer, les parcours vous permettent de créer des parcours clients personnalisés et à plusieurs étapes qui s’adaptent en temps réel au comportement et aux besoins de votre audience. Grâce à une zone de travail intuitive par glisser-déposer, vous pouvez orchestrer des messages et des actions sur plusieurs canaux, en exploitant les données contextuelles et le ciblage des audiences pour un impact maximal.

Que vous exploriez des déclencheurs en temps réel, gériez des propriétés de parcours ou utilisiez des outils avancés tels que des actions et des expressions personnalisées, ce guide fournit une feuille de route claire pour concevoir et affiner en toute confiance des parcours qui offrent des expériences clients significatives et opportunes.

## Que sont les parcours ?

Utilisez [!DNL Journey Optimizer] pour créer des cas d’utilisation d’orchestration en temps réel à l’aide de données contextuelles stockées dans des événements ou des sources de données. Concevez des scénarios avancés à plusieurs étapes qui répondent en temps réel au comportement des clients et clientes et aux événements métier.

Le concepteur de parcours Journey Optimizer fournit tout ce dont les spécialistes marketing et les responsables de parcours ont besoin pour orchestrer des parcours 1:1 à plusieurs étapes sur plusieurs canaux. Vous y trouverez une zone de travail intuitive par glisser-déposer pour orchestrer chaque étape du parcours, définir l’audience cible et inclure les messages, les offres et le contenu sur les canaux que les membres de l’audience cible verront en fonction du comportement, des données contextuelles et des événements métier.

![Interface du concepteur de parcours avec la palette, la zone de travail et le volet Propriétés](assets/journey38.png)

**Vous souhaitez commencer à créer ?** Découvrez comment concevoir et créer votre premier parcours dans [cette page](journey-gs.md).


## Fonctionnalités principales {#capabilities}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=fr)

**Diffusion en temps réel et par lots**

Envoyez des **diffusions unitaires** en temps réel déclenchées lors de la réception d’un événement ou **par lots** à l’aide d’audiences Adobe Experience Platform.

[En savoir plus sur les entrées de parcours](entry-management.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/database.svg?lang=fr)

**Données contextuelles**

Tirez parti des **données contextuelles** issues des événements, des informations d’Adobe Experience Platform ou des données provenant de services d’API tiers.

[Utiliser des sources de données](../datasource/about-data-sources.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=fr)

**Actions intégrées**

Utilisez des **actions de canal intégrées** pour envoyer des messages conçus dans [!DNL Journey Optimizer] par e-mail, notification push, SMS/MMS, etc.

[Envoyer des messages dans les parcours](journeys-message.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=fr)

**Actions personnalisées**

Créez des **actions personnalisées** si vous utilisez un système tiers pour envoyer vos messages ou vous connecter à des API externes.

[Configurer des actions personnalisées](../action/about-custom-action-configuration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=fr)

**Concepteur de parcours visuel**

Avec le **concepteur de parcours**, créez vos cas d’utilisation à plusieurs étapes : faites glisser et déposez facilement un événement d’entrée ou une activité de lecture d’audience, ajoutez des conditions et envoyez des messages personnalisés.

[Explorer le concepteur de parcours](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=fr)

**Tester et optimiser**

Testez vos parcours avant la publication, surveillez leurs performances et optimisez la diffusion à l’aide de fonctionnalités avancées telles que l’optimisation de l’heure d’envoi.

[Tester et publier des parcours](testing-the-journey.md)
:::

::::

## Cas d’utilisation et exemples {#use-cases}

À partir du concepteur de parcours, les spécialistes marketing peuvent envoyer des messages 1:1 déclenchés en temps réel via n’importe quel canal lorsqu’un événement se produit. Par exemple, lorsqu’une personne s’abonne à un service, cela peut [déclencher un e-mail de bienvenue](message-to-subscribers-uc.md) l’incitant à se connecter pour la première fois à l’application et à définir ses préférences. Des actions telles que terminer l’achat, ouvrir l’e-mail et se connecter à l’application peuvent être utilisées pour faire progresser les nouveaux clients et les nouvelles clientes dans leur parcours.

Le [concepteur de parcours](using-the-journey-designer.md) fournit des [actions de canal intégrées](journeys-message.md) qui prennent en charge les messages sortants, tels que les e-mails, les notifications push et les SMS/MMS, ainsi que les canaux entrants, notamment les applications mobiles, les sites web et les expériences basées sur du code créées directement dans Journey Optimizer. Vous pouvez également utiliser des systèmes tiers pour envoyer des messages. Journey Optimizer inclut des [actions personnalisées](using-custom-actions.md) pour permettre l’intégration de ces systèmes dans les parcours directement à partir du concepteur de parcours.


:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=fr)

**Apprendre à travers des cas d’utilisation**

Explorez des cas d’utilisation de parcours complets de bout en bout qui montrent les implémentations et les bonnes pratiques réelles.

[Découvrir tous les cas d’utilisation](jo-use-cases.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=fr)

**Bienvenue aux personnes nouvellement abonnées**

Envoyez un parcours de bienvenue personnalisé lorsque les personnes s’abonnent à votre service, en les guidant tout au long des étapes d’intégration.

[En savoir plus](message-to-subscribers-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg?lang=fr)

**Optimiser les heures d’envoi des e-mails**

Utilisez l’optimisation de l’heure d’envoi optimisée par l’IA pour diffuser des e-mails lorsque chaque personne est le plus susceptible d’interagir.

[En savoir plus](send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=fr)

**Accélérer les diffusions**

Augmentez progressivement le volume des messages pour consolider votre réputation en termes de communication et éviter les problèmes de délivrabilité.

[En savoir plus](ramp-up-deliveries-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=fr)

**Cible par jour de la semaine**

Envoyez un contenu différent en fonction du jour de la semaine où les personnes rejoignent votre parcours.

[En savoir plus](weekday-email-uc.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/question.svg?lang=fr)

**FAQ sur les parcours**

Trouvez des réponses aux questions fréquentes sur la création de parcours, le dépannage et les bonnes pratiques.

[Afficher les questions fréquentes](journey-faq.md)
:::

::::



## Ressources d’apprentissage {#learning-resources}

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=fr)

**Créer et gérer des parcours**

Cette section contient des conseils détaillés pour la conception, le test, la publication et le suivi des parcours clients afin de créer des campagnes omnicanales personnalisées.

[Explorer la création de parcours](/help/rp_landing_pages/create-journey-landing-page.md) | [Découvrir la gestion des parcours ](/help/rp_landing_pages/manage-journey-landing-page.md) | [Étapes de workflow des parcours](journey.md#workflow)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=fr)

**Activités de parcours**

Découvrez comment configurer et utiliser des activités telles que les déclencheurs, les étapes de décision, la gestion de l’audience et les messages personnalisés dans les parcours.

[Explorer les activités](/help/rp_landing_pages/about-journey-building-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=fr)

**Expressions et conditions**

Maîtrisez la création d’expressions pour les workflows dynamiques, la manipulation de données et l’orchestration de parcours avancée à l’aide d’outils et d’une syntaxe puissants.

[Découvrir les expressions](/help/rp_landing_pages/building-advanced-conditions-journeys-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bell.svg?lang=fr)

**Dépannage et surveillance**

Diagnostiquez et résolvez les problèmes d’exécution de parcours à l’aide d’outils, de codes d’erreur et des bonnes pratiques de débogage et d’optimisation.

[Guide de dépannage](/help/rp_landing_pages/troubleshoot-journey-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=fr)

**Vue d’ensemble du concepteur de parcours**

Découvrez la zone de travail des parcours et la palette ; découvrez comment concevoir vos parcours clientèle à l’aide de l’interface visuelle.

[Apprendre à utiliser le concepteur](using-the-journey-designer.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=fr)

**Tester et publier**

Testez minutieusement vos parcours avant de les publier afin de vous assurer qu’ils fonctionnent comme prévu et fournissent la bonne expérience.

[Guide de test](testing-the-journey.md)
:::

::::

### Tutoriel vidéo {#video}

Découvrez les composants d’un parcours et comprenez les principes de base de la création d’un parcours dans la zone de travail.

>[!VIDEO](https://video.tv.adobe.com/v/3424996?quality=12)

### Ressources supplémentaires

* **[Référence des codes d’erreur](error-codes-reference.md)** : codes d’erreur des parcours et étapes de dépannage.
* **[Alertes](../reports/alerts.md)** : configurez des alertes pour la surveillance des parcours.
* **[Dépannage](troubleshooting.md)** : problèmes courants des parcours et solutions.
* **[Tutoriels sur les parcours](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/journeys/journey-designer-overview){target="_blank"}** : découvrez la création de parcours au moyen de tutoriels vidéo pratiques.
* **[Mécanismes de sécurisation et limitations des parcours](../start/guardrails.md)** : vérifiez les mécanismes de sécurisation et les limitations lors de l’utilisation d’[!DNL Adobe Journey Optimizer].

