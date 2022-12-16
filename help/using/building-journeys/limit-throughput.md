---
solution: Journey Optimizer
title: Limiter le débit avec les sources de données externes et les actions personnalisées
description: Limiter le débit avec les sources de données externes et les actions personnalisées
exl-id: 45d6bb82-88ea-4510-a023-a75a82cc6f7b
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 100%

---

# Cas d’utilisation : limiter le débit avec les sources de données externes et les actions personnalisées{#limit-throughput}

## Description du cas d’utilisation

Adobe Journey Optimizer permet aux utilisateurs d’envoyer des appels API aux systèmes externes par le biais d’actions personnalisées et de sources de données.

Cela est possible grâce aux éléments suivants :

* **Sources de données** : pour collecter des informations à partir de systèmes externes et les utiliser dans le contexte du parcours, par exemple pour obtenir des informations météorologiques sur la ville du profil et avoir un flux du parcours dédié basé sur ces informations.

* **Actions personnalisées** : pour envoyer des informations à des systèmes externes, par exemple pour envoyer des e-mails par le biais d’une solution externe à l’aide des fonctionnalités d’orchestration de Journey Optimizer avec des informations de profil, des données d’audience et un contexte de parcours.

Si vous utilisez des sources de données externes ou des actions personnalisées, il peut être judicieux de protéger vos systèmes externes en limitant le débit des parcours : jusqu’à 5 000 instances/seconde pour les parcours unitaires et jusqu’à 2 000 instances/seconde pour les instances déclenchées par un segment. Vous pouvez définir des limites maximum au niveau du point d’entrée afin d’éviter de surcharger ces systèmes externes par le biais des API de limitation de Journey Optimizer. Toutefois, toutes les requêtes restantes une fois la limite atteinte seront ignorées.

Dans cette section, vous trouverez des solutions de contournement que vous pouvez utiliser pour optimiser votre débit. Pour plus d’informations sur l’intégration aux systèmes externes, référez-vous à cette [page](../configuration/external-systems.md).

## Mise en œuvre

Pour les **parcours déclenchés par un segment**, vous pouvez définir le taux de limitation de votre activité Lecture de segment qui aura une incidence sur le débit des parcours.  [En savoir plus](../building-journeys/read-segment.md)

![](assets/limit-throughput-1.png)

Vous pouvez modifier cette valeur de 500 à 20 000 instances par seconde. Si vous devez descendre en dessous de 500/s, vous pouvez également ajouter des conditions de « partage en pourcentage » avec des activités d’attente pour fractionner votre parcours en plusieurs branches et les faire s’exécuter à un moment spécifique.

![](assets/limit-throughput-2.png)

Prenons un exemple de **parcours déclenché par un segment** s’exécutant avec une population de **10 000 profils** et envoyant des données à un système externe prenant en charge **100 requêtes/seconde**.

1. Vous pouvez définir votre Lecture de segment pour lire les profils avec un débit de 500 profils/seconde, ce qui signifie que la lecture de tous vos profils prendra 20 secondes. Lors de la seconde 1, vous lirez 500 d’entre eux, lors de la seconde 2, 500 de plus, etc.

1. Vous pouvez ensuite ajouter une activité de condition de « partage en pourcentage » avec un partage de 20 % afin d’avoir à chaque seconde 100 profils dans chaque branche.

1. Ensuite, ajoutez les activités d’attente avec un retardateur spécifique dans chaque branche. Nous avons configuré ici une attente de 30 secondes pour chacune d’elles. À chaque seconde, un flux de 100 profils ira dans chaque branche.

   * Sur la branche 1, ils attendront 30 secondes, ce qui signifie que :
      * lors de la seconde 1, 100 profils attendront la seconde 31
      * lors de la seconde 2, 100 profils attendront la seconde 32, etc.
   * Sur la branche 2, ils attendront 60 secondes, ce qui signifie que :
      * Lors de la seconde 1, 100 profils attendront la seconde 61 (1 min 01 s)
      * Lors de la seconde 2, 100 profils attendront la seconde 62 (1 min 02 s), etc.
   * Sachant que nous prévoyons 20 secondes au maximum pour lire tous les profils, il n’y aura pas de chevauchement entre chaque branche, la seconde 20 étant la dernière durant laquelle les profils entreront dans la condition. Entre les secondes 31 et 51, tous les profils de la branche 1 seront traités. Entre la seconde 61 (1 min 01 s) et la seconde 81 (1 min 21 s), tous les profils de la branche 2 seront traités, etc.

   * Pour plus de sécurité, vous pouvez également ajouter une sixième branche pour avoir moins de 100 profils par branche, en particulier si votre système externe ne prend en charge que 100 requêtes/seconde.



>[!IMPORTANT]
>
>Comme pour toute solution de contournement, testez minutieusement cette solution avant de passer en production pour vous assurer qu’elle fonctionne comme vous le voulez.

Pour encore plus de sécurité, vous pouvez également utiliser les fonctionnalités de limitation.

>[!NOTE]
>
>Contrairement aux fonctionnalités de limitation, qui protègent un point d’entrée en étant global sur tous les parcours d’une sandbox, cette solution de contournement fonctionne uniquement au niveau du parcours. Cela signifie que si plusieurs parcours s’exécutent en parallèle et ciblent le même point d’entrée, vous devrez en tenir compte lors de la conception de votre parcours. Cette solution de contournement ne convient donc pas à tous les cas d’utilisation.
