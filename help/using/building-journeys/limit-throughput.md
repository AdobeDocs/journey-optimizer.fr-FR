---
solution: Journey Optimizer
title: Limitation du débit avec les sources de données externes et les actions personnalisées
description: Limitation du débit avec les sources de données externes et les actions personnalisées
source-git-commit: 8e3753927e16cc0c4bebf83be2fded6f19d9487e
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 1%

---


# Cas pratique : Débit limite avec les sources de données externes et les actions personnalisées{#limit-throughput}

## Description du cas d&#39;utilisation

Adobe Journey Optimizer permet aux utilisateurs d’envoyer des appels d’API aux systèmes externes par le biais d’actions personnalisées et de sources de données.

Pour ce faire, procédez comme suit :

* **Sources de données**: pour collecter des informations à partir de systèmes externes et les utiliser dans le contexte du parcours, par exemple pour obtenir des informations météorologiques sur la ville du profil et avoir un flux de parcours dédié basé sur cela.

* **Actions personnalisées**: pour envoyer des informations à des systèmes externes, par exemple pour envoyer des emails via une solution externe à l’aide des fonctionnalités d’orchestration de Journey Optimizer avec des informations de profil, des données d’audience et un contexte de parcours.

Si vous utilisez des sources de données externes ou des actions personnalisées, vous pouvez vouloir protéger vos systèmes externes en limitant le débit des parcours : jusqu’à 5 000 instances/seconde pour les parcours unitaires et jusqu’à 2 000 instances/seconde pour les instances déclenchées par un segment. Vous pouvez définir des limites de limitation au niveau du point d’entrée afin d’éviter de surcharger ces systèmes externes par le biais des API de limitation de Journey Optimizer. Cependant, toutes les requêtes restantes après l’atteinte de la limite seront ignorées.

Dans cette section, vous trouverez des solutions de contournement que vous pouvez utiliser pour optimiser votre débit. Pour plus d&#39;informations sur l&#39;intégration aux systèmes externes, reportez-vous à cette section [page](../configuration/external-systems.md).

## Mise en œuvre

Pour **parcours déclenchés par un segment**, vous pouvez définir le taux de ralentissement de votre activité Lecture de segment qui aura une incidence sur le débit des parcours.  [En savoir plus](../building-journeys/read-segment.md)

![](assets/limit-throughput-1.png)

Vous pouvez modifier cette valeur de 500 à 20 000 instances par seconde. Si vous devez descendre en dessous de 500/s, vous pouvez également ajouter des conditions de &quot;partage en pourcentage&quot; avec des activités d’attente pour fractionner votre parcours en plusieurs branches et les faire s’exécuter à un moment spécifique.

![](assets/limit-throughput-2.png)

Prenons un exemple de **parcours déclenchés par un segment** travailler avec une population de **10 000 profils** et envoyer des données à un système externe prenant en charge **100 requêtes/seconde**.

1. Vous pouvez définir votre segment de lecture pour lire les profils avec un débit de 500 profils par seconde, ce qui signifie que la lecture de tous vos profils prendra 20 secondes. Sur le deuxième 1, vous lirez 500 d&#39;entre eux, sur le second 2 500 de plus, etc.

1. Vous pouvez ensuite ajouter une activité Condition de &quot;partage en pourcentage&quot; avec un partage de 20 % afin d’avoir à chaque seconde 100 profils dans chaque branche.

1. Ensuite, ajoutez les activités Attente avec un minuteur spécifique dans chaque branche. Nous avons configuré une attente de 30 secondes pour chacune d&#39;elles. À chaque seconde, 100 profils s’enchaînent dans chaque branche.

   * Sur la branche 1, ils attendront 30 secondes, ce qui signifie que :
      * au second 1, 100 profils attendront au second 31
      * le deuxième 2, 100 profils attendront le deuxième 32, etc.
   * Sur la branche 2, ils attendront 60 secondes, ce qui signifie que :
      * Au second 1, 100 profils attendront le second 61 (1&#39;01&#39;)
      * Sur le second 2, 100 profils attendront le second 62 (1&#39;02&#39;), etc.
   * Sachant que nous prévoyons 20 secondes au maximum pour lire tous les profils, il n’y aura pas de chevauchement entre chaque branche, la seconde étant la dernière où les profils entreront dans la condition. Entre les secondes 31 et 51, tous les profils de la branche 1 seront traités. Entre le second 61 (1&#39;01&#39;) et le second 81 (1&#39;21&#39;), tous les profils de la branche 2 seront traités, etc.

   * En tant que garde-fous, vous pouvez également ajouter une sixième branche pour avoir moins de 100 profils par branche, en particulier si votre système externe ne prend en charge que 100 requêtes/seconde.



>[!IMPORTANT]
>
>Comme pour toute solution de contournement, testez minutieusement cette solution avant de passer en production pour vous assurer qu’elle fait ce que vous voulez.

En tant que garde-fous supplémentaire, vous pouvez également utiliser les fonctionnalités de limitation.

>[!NOTE]
>
>Contrairement aux fonctionnalités de limitation, qui protègent un point de terminaison en étant global sur tous les parcours d’un environnement de test, cette solution fonctionne uniquement au niveau du parcours. Cela signifie que si plusieurs parcours s’exécutent en parallèle et ciblent le même point de terminaison, vous devez en tenir compte lors de la conception de votre parcours. Cette solution ne convient donc pas à tous les cas d’utilisation.

