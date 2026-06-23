---
solution: Journey Optimizer
title: Limiter le débit avec des sources de données externes et des actions personnalisées
description: Limiter le débit avec des sources de données externes et des actions personnalisées
feature: Journeys, Use Cases, Custom Actions, Data Sources
topic: Content Management
role: Developer
level: Experienced
keywords: parcours, sources de données, limite, débit, personnalisé, actions
exl-id: 45d6bb82-88ea-4510-a023-a75a82cc6f7b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/r96xAEjUJDufjpxGMrxoYS0VthagaSyYdS9NQttT9x0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1454
ht-degree: 51%

---

# Cas d’utilisation : limiter le débit avec les sources de données externes et les actions personnalisées{#limit-throughput}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment ralentir le traitement des parcours avec des actions personnalisées et des sources de données externes afin que les systèmes externes ne soient pas submergés par un nombre de requêtes par seconde supérieur à celui pris en charge.

>[!ENDSHADEBOX]

Utilisez ce cas d’utilisation pour ralentir le traitement du parcours lorsque des systèmes externes doivent gérer un nombre limité de requêtes par seconde.

## Description du cas d’utilisation

[!DNL Adobe Journey Optimizer] permet aux utilisateurs d’envoyer des appels d’API à des systèmes externes par le biais d’actions personnalisées et de sources de données.

Cela est possible grâce aux éléments suivants :

* **Sources de données** : pour collecter des informations à partir de systèmes externes et les utiliser dans le contexte du parcours, par exemple pour obtenir des informations météorologiques sur la ville du profil et avoir un flux du parcours dédié basé sur ces informations.

* **Actions personnalisées** : pour envoyer des informations à des systèmes externes, par exemple pour envoyer des e-mails par le biais d’une solution externe à l’aide des fonctionnalités d’orchestration de Journey Optimizer avec des informations de profil, des données d’audience et un contexte de parcours.

>[!NOTE]
>
>Les réponses étant désormais prises en charge, vous devez utiliser des actions personnalisées au lieu de sources de données pour les cas d’utilisation de sources de données externes. Pour plus d’informations sur les réponses, voir [cette section](../action/action-response.md)

Si vous utilisez des sources de données externes ou des actions personnalisées, il peut être judicieux de protéger vos systèmes externes en limitant le débit des parcours : jusqu’à 5 000 instances/seconde pour les parcours unitaires et jusqu’à 20 000 instances/seconde pour les parcours déclenchés par une audience. Pour en savoir plus sur les débits et les taux de traitement des parcours, consultez [cette section](entry-management.md#journey-processing-rate).

Pour les actions personnalisées, les fonctionnalités de ralentissement existent au niveau du produit. Voir cette [page](../configuration/external-systems.md#capping).

Pour les sources de données externes, vous pouvez définir des limites maximum au niveau du point d’entrée afin d’éviter de surcharger ces systèmes externes par le biais des API de plafonnement de Journey Optimizer. Toutefois, toutes les requêtes restantes une fois la limite atteinte seront ignorées. Dans cette section, vous trouverez des solutions de contournement que vous pouvez utiliser pour optimiser votre débit.

Pour plus d’informations sur l’intégration aux systèmes externes, référez-vous à cette [page](../configuration/external-systems.md).

## Mise en œuvre

Pour les **parcours déclenchés par une audience**, vous pouvez définir le taux de lecture de votre activité Lecture d’audience qui aura une incidence sur le débit des parcours. [En savoir plus](../building-journeys/read-audience.md)

>[!NOTE]
>
> Il s’agit du nombre maximum de profils pouvant entrer dans le parcours par seconde. Ce taux s’applique uniquement à cette activité et non aux autres activités du parcours. [En savoir plus](../building-journeys/read-audience.md)


![Panneau de configuration de limitation de débit avec les paramètres de limitation de débit](assets/limit-throughput-1.png)

Vous pouvez modifier cette valeur de 500 à 20 000 instances par seconde. Si vous devez descendre en dessous de 500/s, vous pouvez également ajouter des conditions de « partage en pourcentage » avec des activités d’attente pour fractionner votre parcours en plusieurs branches et les faire s’exécuter à un moment spécifique.

![Parcours avec une activité de limitation de débit contrôlant le taux de diffusion des messages](assets/limit-throughput-2.png)

Prenons l’exemple d’un **parcours déclenché par une audience** s’exécutant avec une population de **10 000 profils** et envoyant des données à un système externe prenant en charge **100 requêtes/seconde**.

1. Vous pouvez définir votre Lecture d’audience pour lire les profils avec un débit de 500 profils/seconde, ce qui signifie que la lecture de tous vos profils prendra 20 secondes. Lors de la seconde 1, vous lirez 500 d’entre eux, lors de la seconde 2, 500 de plus, etc.

1. Vous pouvez ensuite ajouter une activité de condition de « partage en pourcentage » avec un partage de 20 % afin d’avoir à chaque seconde 100 profils dans chaque branche.

1. Ensuite, ajoutez les activités d’attente avec un retardateur spécifique dans chaque branche. Nous avons configuré ici une attente de 30 secondes pour chacune d’elles. À chaque seconde, un flux de 100 profils ira dans chaque branche.

   * Sur la branche 1, ils attendront 30 secondes, ce qui signifie que :
      * lors de la seconde 1, 100 profils attendront la seconde 31
      * lors de la seconde 2, 100 profils attendront la seconde 32, etc.

   * Sur la branche 2, ils attendront 60 secondes, ce qui signifie que :
      * Lors de la seconde 1, 100 profils attendront la seconde 61 (1 min 01 s)
      * Lors de la seconde 2, 100 profils attendront la seconde 62 (1 min 02 s), etc.

   * Sachant que nous prévoyons 20 secondes au maximum pour lire tous les profils, il n’y aura pas de chevauchement entre chaque branche, la seconde 20 étant la dernière durant laquelle les profils entreront dans la condition. Entre les secondes 31 et 51, tous les profils de la branche 1 seront traités. Entre la seconde 61 (1 min 01 s) et la seconde 81 (1 min 21 s), tous les profils de la branche 2 seront traités, etc.

   * Comme mécanisme de sécurisation, vous pouvez également ajouter une sixième branche pour avoir moins de 100 profils par branche, en particulier si votre système externe ne prend en charge que 100 requêtes/seconde.

>[!IMPORTANT]
>
>Comme pour toute solution de contournement, testez minutieusement cette solution avant de passer en production pour vous assurer qu’elle fonctionne comme vous le voulez.

Comme autre mécanisme de sécurisation, vous pouvez également utiliser les fonctionnalités de limitation.

>[!NOTE]
>
>Contrairement aux fonctionnalités de limitation, qui protègent un point d’entrée en étant global sur tous les parcours d’un sandbox, cette solution de contournement fonctionne uniquement au niveau du parcours. Cela signifie que si plusieurs parcours s’exécutent en parallèle et ciblent le même point d’entrée, vous devrez en tenir compte lors de la conception de votre parcours. Cette solution de contournement ne convient donc pas à tous les cas d’utilisation.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page explique comment limiter le débit du parcours lorsque des sources de données externes ou des actions personnalisées ont un nombre limité de requêtes par seconde, à l’aide de la configuration du taux de lecture d’audience, des fractionnements de pourcentage et des activités d’attente.

**Intentions:**

* Limitez le débit d’un parcours déclenché par une audience pour éviter qu’un système externe ne soit submergé
* Configurez le taux de lecture d’une activité Lecture d’audience pour contrôler le nombre de profils entrés par seconde
* Combinez des conditions de partage en pourcentage et des activités d’attente pour répartir le traitement des profils dans le temps
* Comprenez la différence entre les solutions de contournement du débit au niveau du parcours et les fonctionnalités de limitation au niveau du sandbox
* Application des fonctionnalités de limitation aux actions personnalisées au niveau du produit

**Glossaire:**

* **Limitation/limitation du débit** : contrôle du débit auquel les profils traversent un parcours afin d’éviter de dépasser la capacité de requête d’un système externe. *(spécifique au produit)*
* **Taux de lecture d’audience** : paramètre configurable sur l’activité Lecture d’audience qui définit le nombre maximal de profils entrant dans le parcours par seconde (plage : 500 à 20 000 instances/seconde). *(spécifique au produit)*
* **API de limitation** : API Journey Optimizer qui définit une limite maximale de requêtes par point d’entrée pour les sources de données externes ; les requêtes au-delà de la limite sont ignorées. *(spécifique au produit)*
* **Condition de partage en pourcentage** : une activité de condition qui divise le flux de profils en branches par pourcentage, utilisée ici pour distribuer les profils sur les chemins d’attente échelonnés dans le temps. *(spécifique au produit)*

**Mécanismes de sécurisation :**

* Le taux de lecture d’audience peut être défini entre 500 et 20 000 instances par seconde ; les valeurs inférieures à 500/s nécessitent une solution de contournement à l’aide de divisions en pourcentage et d’activités d’attente
* Les parcours unitaires prennent en charge jusqu’à 5 000 instances/seconde ; les parcours déclenchés par une audience prennent en charge jusqu’à 20 000 instances/seconde.
* La solution de contournement de division en pourcentage + attente fonctionne uniquement au niveau du parcours, et non sur tous les parcours du sandbox
* Lorsque plusieurs parcours ciblent en parallèle le même point d’entrée externe, cette solution de contournement ne prend pas en compte la charge combinée. Utilisez plutôt les fonctionnalités de limitation .
* Les requêtes restantes qui dépassent la limite de limitation sur les sources de données externes sont ignorées et non mises en file d’attente
* La solution doit être minutieusement testée avant le passage en production

**Terminologie:**

* Nom canonique : Limitation du débit — Acronyme : aucun — variantes : limitation, limitation de débit, contrôle du débit du parcours
* Synonymes : « Limitation » = « limitation » dans le contexte de la protection des points d’entrée externes
* Ne les confondez pas : « API de limitation (niveau de point d’entrée) » ≠ « taux de lecture (niveau de parcours) » - L’API de limitation s’applique globalement à tous les parcours d’un sandbox ciblant un point d’entrée ; le taux de lecture et la solution de fractionnement/d’attente s’appliquent uniquement à chaque parcours

**FAQ:**

* **Q : Quel est le taux de lecture maximal que je peux définir sur une activité Lecture d’audience ?** — Entre 500 et 20 000 profils par seconde ; pour descendre en dessous de 500/s, utilisez un partage en pourcentage avec les activités d’attente.
* **Q : Comment les fractionnements en pourcentage et les activités d’attente permettent-ils de limiter le débit ?** : en divisant les profils en branches (par exemple, 20 % chacune) et en ajoutant des temporisateurs d’attente décalés par branche, vous vous assurez que seul un nombre contrôlé de profils atteignent le système externe par seconde.
* **Q : La solution de contournement de partage en pourcentage protège-t-elle tous les parcours ciblant le même point d’entrée ?** — Non ; cela ne fonctionne qu&#39;au niveau des parcours individuels. Si plusieurs parcours s’exécutent en parallèle sur le même point d’entrée, utilisez plutôt les fonctionnalités de limitation au niveau du sandbox .
* **Q : Qu’advient-il des requêtes qui dépassent la limite de limitation sur une source de données externe ?** — Elles sont ignorées ; l’API de limitation ne met pas en file d’attente les requêtes en trop.
* **Q : Dois-je utiliser des actions personnalisées ou des sources de données pour les cas d’utilisation de données externes ?** — Les actions personnalisées sont recommandées, car elles prennent en charge le traitement des réponses ; les sources de données ne doivent être utilisées que lorsque le cas d’utilisation les requiert spécifiquement.

+++
