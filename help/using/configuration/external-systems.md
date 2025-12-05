---
solution: Journey Optimizer
product: journey optimizer
title: Intégrer Journey Optimizer à des systèmes externes
description: Découvrez les bonnes pratiques à appliquer lors de l’intégration de Journey Optimizer à des systèmes externes
feature: Integrations
role: User
level: Beginner
keywords: externe, API, optimizer, limitation
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: bc614a78229771e826edea581aefb97b0e3f4159
workflow-type: ht
source-wordcount: '1805'
ht-degree: 100%

---

# Intégration avec des systèmes externes {#external-systems}

Cette page présente les différents mécanismes de sécurisation fournis par Journey Optimizer lors de l&#39;intégration d&#39;un système externe, ainsi que les bonnes pratiques : comment optimiser la protection de votre système externe à l&#39;aide de l&#39;API de limitation, comment configurer le délai d&#39;expiration du parcours et comment les reprises fonctionnent.

Journey Optimizer vous permet de configurer des connexions à des systèmes externes par le biais de sources de données et d&#39;actions personnalisées. Vous pouvez ainsi, par exemple, enrichir vos parcours de données provenant d&#39;un système de réservation externe ou envoyer des messages à l&#39;aide d&#39;un système tiers tel qu&#39;Epsilon ou Facebook.

Lors de l&#39;intégration d&#39;un système externe, vous pouvez rencontrer plusieurs problèmes : le système peut être lent, il peut arrêter de répondre ou ne pas être en mesure de gérer un volume important. Journey Optimizer propose plusieurs mécanismes de sécurisation pour protéger votre système contre la surcharge.

Tous les systèmes externes sont différents en termes de performances. Vous devez adapter la configuration à vos cas d&#39;utilisation.

Lorsque Journey Optimizer exécute un appel à une API externe, les mécanismes de sécurisation techniques sont exécutés comme suit :

1. Les règles de plafonnnement et de limitation sont appliquées : si le taux maximum est atteint, les appels restants sont ignorés ou mis en file d’attente.

1. Temporisation et reprise : si la règle de limitation ou de plafonnement est remplie, Journey Optimizer tente d’effectuer l’appel jusqu’à la fin de la temporisation.

>[!TIP]
>
>Nous vous recommandons de laisser au moins une minute de buffer entre la période d’expiration du jeton de l’API externe et votre paramètre [`cacheDuration` de Journey Optimizer](../datasource/external-data-sources.md#custom-authentication-access-token), en particulier en cas de lourdes charges de travail, afin d’éviter les décalages d’expiration et les erreurs 401.

## API de plafonnement et de limitation {#capping}

### À propos des API de plafonnement et de limitation

En configurant une source de données ou une action, vous établissez une connexion à un système afin de récupérer des informations supplémentaires pour enrichir vos parcours, les messages que vous envoyez ou les appels API.

Les API de Journeys prennent en charge jusqu’à 5 000 événements par seconde, mais certains systèmes externes ou API peuvent ne pas avoir un débit équivalent. Pour éviter de surcharger ces systèmes, utilisez les API de **plafonnement** et de **limitation** pour limiter le nombre d’événements envoyés par seconde.

Chaque fois qu’un appel API est réalisé par les parcours, le moteur d’API est sollicité. Si la limite définie dans l’API est atteinte, deux scénarios peuvent se présenter selon l’API utilisée : avec l’API de plafonnement, l’appel est rejeté. Si vous utilisez l’API de limitation, l’appel est mis en file d’attente pendant 6 heures au maximum et traité dès que possible, dans l’ordre où il a été reçu.

Supposons, par exemple, que vous ayez défini une règle de plafonnement ou de limitation de 200 appels par seconde pour votre système externe. Votre système est appelé par une action personnalisée dans 10 parcours différents. Si un parcours reçoit 300 appels par seconde, il utilise les 200 emplacements disponibles et rejette ou met en file d’attente les 100 emplacements restants. Comme le taux maximum a été dépassé, il ne restera plus aucun emplacement pour les 9 autres parcours. Cette granularité permet de protéger le système externe contre la surcharge et la panne.

>[!IMPORTANT]
>
>Les **Règles de limitation** sont configurées au niveau du sandbox, pour un point d’entrée spécifique (l’URL appelée), mais elles s’appliquent à tous les parcours de ce sandbox. La limitation est disponible à la fois sur les sources de données et les actions personnalisées.
>
>Les **Règles de limitation** sont configurées dans les sandbox de production uniquement, pour un point d’entrée spécifique, mais elles s’appliquent à tous les parcours sur l’ensemble des sandbox. Une seule configuration de limitation est autorisée par organisation. La limitation n’est disponible que pour les actions personnalisées.
>
>La valeur **maxCallsCount** doit être supérieure à 1.

Pour plus d’informations sur l’utilisation des API, reportez-vous aux sections suivantes :

* [API Capping](capping.md)
* [API de limitation](throttling.md)

Consultez la description détaillée des API dans la [Documentation des API Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/journeys/).

### Sources de données et capacité des actions personnalisées {#capacity}

Pour les **sources de données externes**, le nombre maximal d’appels par seconde est limité à 15. Si cette limite est dépassée, les appels suivants sont rejetés ou mis en file d’attente, selon l’API utilisée. Contactez Adobe si vous souhaitez augmenter cette limite pour les sources de données externes privées. Le point d’entrée sera alors placé dans la liste autorisée. Cette opération n’est pas possible pour les sources de données externes publiques. * [Découvrez comment configurer des sources de données](../datasource/about-data-sources.md).

>[!NOTE]
>
>Si une source de données utilise une authentification personnalisée avec un point d’entrée différent de celui utilisé pour la source de données, vous devez contacter Adobe pour inclure également ce point d’entrée dans la liste autorisée.

Pour les **actions personnalisées**, vous devez évaluer la capacité de votre API externe. Par exemple, si Journey Optimizer envoie 1 000 appels par seconde et que votre système ne peut prendre en charge que 200 appels par seconde, vous devez définir une configuration de plafonnement ou de limitation afin que votre système ne sature pas. [Découvrir comment configurer des actions](../action/action.md)

>[!NOTE]
>
>Les réponses étant désormais prises en charge, vous devez utiliser des actions personnalisées au lieu de sources de données pour les cas d’utilisation de sources de données externes. Pour plus d’informations sur les réponses, voir [cette section](../action/action-response.md)

## Points d’entrée avec un temps de réponse allongé {#response-time}

Lorsqu’un point d’entrée a un temps de réponse supérieur à 0,75 seconde, ses appels d’action personnalisée sont acheminés via un **service d’action personnalisée lent** dédié au lieu du service par défaut.

Ce service d’action personnalisée lent applique une limite de capping de 150 000 appels toutes les 30 secondes. La limite est appliquée à l’aide d’une fenêtre glissante, qui peut commencer à n’importe quelle milliseconde au cours de cette période de 30 secondes. Une fois la fenêtre pleine, les appels supplémentaires sont refusés, au moyen d’erreurs de capping. Le système n’attend pas l’intervalle fixe suivant, mais commence le capping juste après avoir atteint le seuil de 30 secondes.

Comme les points d’entrée lents peuvent entraîner des retards pour toutes les actions en file d’attente du pipeline, il est recommandé de ne pas configurer d’actions personnalisées avec des points d’entrée dont les temps de réponse sont lents. Le routage de ces actions vers le service lent permet de protéger les performances globales du système et d’éviter une latence supplémentaire pour d’autres actions personnalisées.

## Temporisation et reprises {#timeout}

Si la règle de plafonnement ou de limitation est remplie, la règle de temporisation est appliquée.

Dans chaque parcours, vous pouvez définir un délai de temporisation. Vous pouvez ainsi définir une durée maximale lors de l&#39;appel d&#39;un système externe. Le délai de temporisation est configuré dans les propriétés d&#39;un parcours. Voir [cette page](../building-journeys/journey-properties.md#timeout_and_error).

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

## Questions fréquentes {#faq}

Vous trouverez ci-dessous les questions fréquentes sur l’intégration de Journey Optimizer aux systèmes externes.

Vous avez besoin de plus d’informations ? Utilisez les options de commentaires au bas de cette page pour poser votre question ou contacter la [communauté Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=fr){target="_blank"}.

+++ Comment configurer une règle de limitation ? Existe-t-il une règle par défaut ?

Pour créer des règles de limitation ou de ralentissement, reportez-vous à [cette section](../configuration/external-systems.md#capping). Par défaut, il n’y a aucune règle de ralentissement mais une limitation de 300 000 appels de plus d’une minute est définie pour toutes les actions personnalisées, par hôte et par sandbox. La limite « par hôte » s’applique au niveau du domaine (par exemple, example.com). Cette limite a été définie en fonction de l’utilisation de la clientèle, afin de protéger les points d’entrée externes ciblés par des actions personnalisées. Si nécessaire, vous pouvez remplacer ce paramètre en définissant une limitation ou un ralentissement plus élevé via nos API de limitation/ralentissement. Consultez [cette page](../action/about-custom-action-configuration.md) pour plus d’informations sur la manière de demander des augmentations de limitation.

+++

+++ Combien de reprises sont effectuées ? Puis-je modifier le nombre de reprises ou définir une période d’attente minimale entre deux reprises ?

Pour un appel donné, trois reprises au maximum peuvent être effectuées jusqu&#39;à la fin du délai de temporisation. Le nombre de reprises et la durée entre chaque reprise ne peuvent pas être modifiés. Reportez-vous à [cette section](../configuration/external-systems.md#timeout).

+++

+++ Où configurer la temporisation ? Existe-t-il une valeur maximale ?

Dans chaque parcours, vous pouvez définir un délai de temporisation. Le délai de temporisation est configuré dans les propriétés d&#39;un parcours. Le délai de temporisation doit être compris entre 1 et 30 secondes. Consultez [cette section](../configuration/external-systems.md#timeout) et [cette page](../building-journeys/journey-properties.md#timeout_and_error).

+++

+++ Qu’est-ce que le proxy de sortie et quand dois-je l’utiliser ?

Le proxy de sortie fournit une **adresse IP statique** pour les appels sortants de Journey Optimizer vers vos systèmes externes. Utilisez-le lorsque vos points d’entrée tiers nécessitent une liste autorisée d’adresses IP.

**Important :** le proxy de sortie NE contrôle PAS le débit, les limites de débit ni le nombre de connexions simultanées. Pour gérer le volume d’appels et les limites de connexion, utilisez l’[API de limitation](capping.md) ou l’[API d’étranglement](throttling.md).

**Utiliser le proxy de sortie pour :**
* Placer sur la liste autorisée une adresse IP statique sur votre pare-feu ou point d’entrée tiers

**Utiliser les API de limitation ou d’étranglement pour :**
* Limiter le nombre d’appels API par seconde
* Contrôler les connexions simultanées à votre point d’entrée
* Protéger votre système externe contre les surcharges

Contactez Adobe pour activer le proxy sortant pour votre organisation si vous avez besoin d’une adresse IP statique à des fins d’ajout à une liste autorisée.

+++

+++ Quel est le nombre maximal de connexions ouvertes par Journey Optimizer lorsque des actions personnalisées sont utilisées ?

Lorsque le proxy IP est activé et qu’une configuration de limitation est définie sur le point d’entrée ciblé, le nombre de connexions est basé sur le taux (il s’agit d’estimations, et non de nombres garantis) :

* entre 200 c/s et 2 000 c/s : 50 connexions
* entre 2 000 et 3 000 : 75 connexions
* entre 3 000 et 4 000 : 100 connexions
* entre 4 000 et 5 000 : 125 connexions

Si aucune configuration de limitation n’est définie sur un point d’entrée, le moteur de Journey Optimizer est conçu pour être augmenté et peut atteindre un grand nombre de connexions (plus de 2 000). Pour obtenir un nombre limité de connexions, les clientes et clients doivent utiliser une configuration de limitation.

+++
