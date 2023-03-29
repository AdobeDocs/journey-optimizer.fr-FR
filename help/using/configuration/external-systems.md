---
solution: Journey Optimizer
product: journey optimizer
title: Intégration de Journey Optimizer à des systèmes externes
description: Découvrez les bonnes pratiques à appliquer lors de l’intégration de Journey Optimizer à des systèmes externes
role: User
level: Beginner
keywords: externe, API, optimizer, limitation
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 62%

---

# Intégration avec des systèmes externes {#external-systems}

Cette page présente les différents mécanismes de sécurisation fournis par Journey Optimizer lors de l&#39;intégration d&#39;un système externe, ainsi que les bonnes pratiques : comment optimiser la protection de votre système externe à l&#39;aide de l&#39;API de limitation, comment configurer le délai d&#39;expiration du parcours et comment les reprises fonctionnent.

Journey Optimizer vous permet de configurer des connexions à des systèmes externes par le biais de sources de données et d&#39;actions personnalisées. Vous pouvez ainsi, par exemple, enrichir vos parcours de données provenant d&#39;un système de réservation externe ou envoyer des messages à l&#39;aide d&#39;un système tiers tel qu&#39;Epsilon ou Facebook.

Lors de l&#39;intégration d&#39;un système externe, vous pouvez rencontrer plusieurs problèmes : le système peut être lent, il peut arrêter de répondre ou ne pas être en mesure de gérer un volume important. Journey Optimizer propose plusieurs mécanismes de sécurisation pour protéger votre système contre la surcharge.

Tous les systèmes externes sont différents en termes de performances. Vous devez adapter la configuration à vos cas d&#39;utilisation.

Lorsque Journey Optimizer exécute un appel à une API externe, les mécanismes de sécurisation techniques sont exécutés comme suit :

1. Les règles de limitation ou de ralentissement sont appliquées : si le taux maximal est atteint, les appels restants sont ignorés ou placés en file d’attente.

2. Temporisation et reprise : si la règle de limitation est remplie, Journey Optimizer tente d&#39;effectuer l&#39;appel jusqu&#39;à la fin de la temporisation.

## Limitation API de limitation et de ralentissement {#capping}

### À propos des API de limitation et de limitation

Lors de la configuration d’une source de données ou d’une action, vous établissez une connexion à un système afin de récupérer des informations supplémentaires à utiliser dans vos parcours ou d’envoyer des messages ou des appels d’API.

Les API Parcours prennent en charge jusqu’à 5 000 événements par seconde, mais certains systèmes ou API externes peuvent ne pas avoir un débit équivalent. Pour éviter de surcharger ces systèmes, vous pouvez utiliser la variable **Limitation** et **Ralentissement** API pour limiter le nombre d’événements envoyés par seconde.

Chaque fois qu’un appel API est effectué par parcours, il passe par le moteur d’API. Si la limite définie dans l’API est atteinte, l’appel est rejeté si vous utilisez l’API de limitation, ou mis en file d’attente et traité le plus tôt possible dans l’ordre dans lequel ils ont été reçus si vous utilisez l’API de limitation.

Supposons, par exemple, que vous ayez défini une règle de limitation ou de limitation de 100 appels par seconde pour votre système externe. Votre système est appelé par une action personnalisée dans 10 parcours différents. Si un parcours reçoit 200 appels par seconde, il utilise les 100 emplacements disponibles et ignore ou met en file d’attente les 100 emplacements restants. Comme le taux maximum a été dépassé, il ne restera plus aucun emplacement pour les 9 autres parcours. Cette granularité permet de protéger le système externe contre la surcharge et la panne.

>[!IMPORTANT]
>
>**Règles de limitation** sont configurés au niveau de l’environnement de test, pour un point de terminaison spécifique (l’URL appelée), mais globaux pour tous les parcours de cet environnement de test.
>
>**Règles de limitation** sont configurés uniquement sur les environnements de test de production, pour un point de terminaison spécifique, mais globaux pour tous les parcours de tous les environnements de test. Vous ne pouvez avoir qu’une seule configuration de limitation par organisation.

Pour plus d’informations sur l’utilisation des API, reportez-vous aux sections suivantes :

* [API de limitation](capping.md)
* [API de limitation](throttling.md)

### Sources de données et capacité des actions personnalisées {#capacity}

Pour **sources de données externes**, le nombre maximal d’appels par seconde est limité à 15. Si cette limite est dépassée, tout appel supplémentaire est ignoré ou mis en file d’attente selon l’API utilisée. Il est possible d’augmenter cette limite pour les sources de données externes privées en contactant Adobe pour inclure le point de terminaison dans la liste autorisée de données, mais il ne s’agit pas d’une option pour les sources de données externes publiques. * [Découvrez comment configurer des sources de données](../datasource/about-data-sources.md).

>[!NOTE]
>
>Si une source de données utilise une authentification personnalisée avec un point d’entrée différent de celui utilisé pour la source de données, vous devez contacter Adobe pour inclure également ce point d’entrée dans la liste autorisée.

Pour **actions personnalisées**, vous devez évaluer la capacité de votre API externe. Par exemple, si Journey Optimizer envoie 1 000 appels par seconde et que votre système ne peut prendre en charge que 100 appels par seconde, vous devez définir une configuration de limitation ou de ralentissement afin que votre système ne se satue pas. [Découvrez comment configurer des actions](../action/action.md)

## Temporisation et reprises{#timeout}

Si la règle de limitation ou de ralentissement est remplie, la règle de dépassement de délai est appliquée.

Dans chaque parcours, vous pouvez définir un délai de temporisation. Vous pouvez ainsi définir une durée maximale lors de l&#39;appel d&#39;un système externe. Le délai de temporisation est configuré dans les propriétés d&#39;un parcours. Voir [cette page](../building-journeys/journey-gs.md#timeout_and_error).

Cette temporisation est commune à tous les appels externes (appels API externes dans les actions personnalisées et les sources de données personnalisées). Par défaut, elle est définie sur 30 secondes.

Pendant le délai de temporisation défini, Journey Optimizer tente d&#39;appeler le système externe. Après le premier appel, trois reprises au maximum peuvent être effectuées jusqu&#39;à la fin du délai de temporisation. Le nombre de reprises ne peut pas être modifié.

Chaque nouvelle reprise utilise un emplacement. Si vous avez une limitation de 100 appels par seconde et que chacun de vos appels nécessite deux reprises, le taux chute à 30 appels par seconde (chaque appel utilise 3 emplacements : le premier appel et deux reprises).

La valeur du délai de temporisation dépend du cas d&#39;utilisation. Si vous souhaitez envoyer votre message rapidement, par exemple lorsque le client entre dans le magasin, le délai de temporisation ne doit pas être long. En outre, plus le délai de temporisation est long, plus les éléments sont placés en file d&#39;attente. Cela peut avoir un impact considérable sur les performances. Si Journey Optimizer effectue 1 000 appels par seconde, conserver 5 ou 15 secondes de données peut rapidement entraîner une surcharge du système.

Prenons un exemple pour une temporisation de 5 secondes.

* Le premier appel dure moins de 5 secondes : l&#39;appel a réussi, aucune nouvelle reprise n&#39;a été effectuée.
* Le premier appel dure plus de 5 secondes : l&#39;appel est annulé et il n&#39;y a aucune reprise. Il est compté comme une erreur de temporisation dans les rapports.
* Le premier appel échoue après 2 secondes (le système externe renvoie une erreur) : 3 secondes restent pour les reprises, si des emplacements de limitation sont disponibles.
   * Si l&#39;une des trois reprises réussit avant la fin des 5 secondes, l&#39;appel est effectué et aucune erreur ne se produit.
   * Si la fin du délai de temporisation est atteinte lors des nouvelles reprises, l&#39;appel est annulé et compté comme une erreur de temporisation dans les rapports.

## Questions fréquentes{#faq}

**Comment configurer une règle de limitation ou de ralentissement ? Existe-t-il une règle par défaut ?**

Par défaut, il n’existe aucune règle de limitation ou de ralentissement. Les règles sont définies au niveau de l’environnement de test pour un point de terminaison spécifique (l’URL appelée), à l’aide de l’API Limitation ou Limitation. Reportez-vous à [cette section](../configuration/external-systems.md#capping).

**Combien de reprises sont effectuées ? Puis-je modifier le nombre de reprises ou définir une période d&#39;attente minimale entre deux reprises ?**

Pour un appel donné, trois reprises au maximum peuvent être effectuées jusqu&#39;à la fin du délai de temporisation. Le nombre de reprises et la durée entre chaque reprise ne peuvent pas être modifiés. Reportez-vous à [cette section](../configuration/external-systems.md#timeout).

**Où puis-je configurer la temporisation ? Existe-t-il une valeur maximale ?**

Dans chaque parcours, vous pouvez définir un délai de temporisation. Le délai de temporisation est configuré dans les propriétés d&#39;un parcours. Le délai de temporisation doit être compris entre 1 et 30 secondes. Consultez [cette section](../configuration/external-systems.md#timeout) et [cette page](../building-journeys/journey-gs.md#timeout_and_error).