---
solution: Journey Optimizer
product: journey optimizer
title: Cycle de publication de Adobe Journey Optimizer
feature: Release Notes
description: Présentation du cycle de publication de Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 920c9080768e1972b487b3a258281914a4b7d8de
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 1%

---

# Cycle de publication de Journey Optimizer {#releases}

[!DNL Adobe Journey Optimizer] est mis à jour régulièrement pour fournir de nouvelles fonctionnalités, des améliorations et des correctifs. Cette page explique le fonctionnement du cycle de publication et la signification de chaque phase de publication, afin que vous puissiez facilement comprendre quand les fonctionnalités sont disponibles pour votre organisation.

## Modèle de diffusion au fil de l’eau {#continuous-delivery-model}

[!DNL Adobe Journey Optimizer] fonctionne sur un modèle de diffusion continu, ce qui permet une approche évolutive et progressive du déploiement des fonctionnalités. Ce modèle permet à Adobe de proposer de l’innovation plus rapidement et d’assurer une stabilité et des performances continues lors du déploiement.

>[!NOTE]
>
> Étant donné que [!DNL Adobe Journey Optimizer] utilise la diffusion au fil de l’eau, de nouvelles fonctionnalités peuvent apparaître progressivement dans toutes les organisations ou régions.

Dans le cadre de ce modèle :

* Les nouvelles fonctionnalités et améliorations sont déployées en production dès qu’elles sont prêtes.

* Les [**notes de mise à jour**](release-notes.md) sont mises à jour entre les versions mensuelles avec une section _Dernières mises à jour_ qui annonce les nouvelles fonctionnalités et améliorations au fur et à mesure de leur déploiement, afin que vous soyez informé en temps réel.

## Calendrier et cadence des versions {#release-timing}

[!DNL Adobe Journey Optimizer] suit généralement une cadence de publication mensuelle, les déploiements ayant généralement lieu au cours de la dernière semaine de chaque mois. Les notes de mise à jour mensuelles et la documentation associée sont publiées le mardi de la semaine de publication. Les notes de version préliminaire sont publiées le vendredi précédant la semaine de publication.

>[!TIP]
>
> À la fin de chaque trimestre, les versions peuvent être anticipées et déployées jusqu’à deux semaines avant la fin du mois afin de s’aligner sur les calendriers trimestriels ou les versions de produits dépendantes.

Bien que la version mensuelle introduise l’ensemble principal des nouvelles fonctionnalités et des correctifs, l’approche de diffusion continue permet de déployer des mises à jour supplémentaires entre les cycles lorsqu’elles sont prêtes. Les notes de mise à jour sont ensuite mises à jour en conséquence dans la section _Dernières mises à jour_ et la date de disponibilité est mentionnée. Toutes les modifications publiées au cours du mois sont consolidées dans les notes de mise à jour mensuelles à la date de publication.


## Chemins de version {#release-paths}

Les fonctionnalités de Journey Optimizer suivent différents chemins de mise à jour en fonction de leur complexité, de leurs dépendances et de leur portée. La plateforme utilise plusieurs libellés de disponibilité (Beta, Disponibilité limitée, Disponibilité générale), mais toutes les fonctionnalités ne sont pas reprises en entier.

Les chemins de publication courants sont les suivants :

* **Direct to GA** — Certaines nouvelles fonctionnalités et améliorations vont directement vers la disponibilité générale (GA).
* **LA → GA** — Certaines fonctionnalités sont d’abord disponibles pour une audience limitée (disponibilité limitée) avant le déploiement général.
* **Beta → LA → GA** — Des fonctionnalités plus importantes ou expérimentales passent par toutes les phases de test et de validation.
* **Beta → GA** — Certaines fonctionnalités Beta stables peuvent passer directement à GA, sans phase LA intermédiaire.

>[!TIP]
>
> Si vous souhaitez bénéficier d’un accès anticipé aux fonctionnalités de Beta ou à disponibilité limitée, contactez votre représentant Adobe pour discuter des options de participation.


## Libellés de disponibilité {#availability-labels}

| **Libellé** | **Rôle** | **Disponibilité** | **Remarques clés** |
|------------|-------------|------------------|----------------|
| **Beta** | Des tests précoces et la collecte de commentaires. | Restrictions aux clients ou organisations sélectionnés participant au programme Adobe Beta. | - Non destinés à la production.<br>- La fonctionnalité ou la conception peuvent changer avant la disponibilité générale.<br>- Les commentaires permettent d’affiner l’implémentation finale. |
| **Disponibilité limitée (LA)** | Déploiement contrôlé pour la validation et la surveillance. | Activé uniquement pour les clients ou environnements sélectionnés (par exemple, les sandbox de développement). | - Prêt pour la production et entièrement pris en charge.<br>- Utilisé pour valider les performances et l’évolutivité avant la publication générale.<br>- L’accès nécessite l’approbation d’Adobe. |
| **Disponibilité générale (GA)** | Version étendue de fonctionnalités entièrement prises en charge. | Activé par défaut pour toutes les organisations éligibles. | - Prêt pour la production et entièrement pris en charge.<br> - Une licence ou des droits peuvent s&#39;appliquer.<br> - Peut être déployé progressivement entre les régions. |


## Déploiement et disponibilité {#rollout}

Même après une annonce de disponibilité générale, le déploiement peut se faire progressivement dans toutes les organisations ou régions. Si une nouvelle fonctionnalité n’apparaît pas immédiatement dans votre environnement, elle est généralement disponible dans les jours qui suivent sa publication.

Ce déploiement progressif permet à Adobe de surveiller la stabilité, les performances et l’expérience utilisateur avant d’effectuer le déploiement.


## Rester informé {#staying-informed}

Pour rester à jour :

* Consultez les [**notes de mise à jour les plus récentes**](release-notes.md) pour découvrir les fonctionnalités nouvelles et mises à jour.
* Consultez la section **_Dernières mises à jour_** entre les versions mensuelles pour les déploiements en temps réel.
* Surveillez **les notes de mise à jour préliminaires** (le cas échéant) pour obtenir un aperçu des fonctionnalités à venir.
* Contactez votre représentant Adobe pour obtenir des informations sur l’accès ou les droits de Beta ou de disponibilité limitée.

Vous pouvez vous abonner à des **e-mails et alertes sur les produits** pour les mises à jour de produits Journey Optimizer. Pour vous abonner :

1. Accédez aux **préférences d’Adobe Experience Cloud**.
1. Sous **Notifications**, recherchez **Journey Optimizer**
1. Activer les **nouvelles versions** notifications in-app et par e-mail

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}

## Questions fréquentes {#faq}

+++ Quand les versions de Adobe Journey Optimizer sont-elles planifiées ?

[!DNL Adobe Journey Optimizer] publie généralement des mises à jour au cours de la dernière semaine de chaque mois. À la fin de chaque trimestre, la version peut être avancée de deux semaines au maximum pour s’aligner sur les mises à jour inter-solutions ou à l’échelle de la plateforme.

+++

+++ Pourquoi est-ce que je ne vois pas une nouvelle fonctionnalité immédiatement après son annonce ?

Certaines fonctionnalités de disponibilité générale sont déployées progressivement pour garantir la stabilité et les performances de la plateforme. Si vous ne voyez pas immédiatement une fonctionnalité, elle apparaîtra une fois le déploiement terminé pour votre région ou organisation.

+++

+++ Quelle est la différence entre Beta, la disponibilité limitée et la disponibilité générale ?

* **Beta** : phase de test précoce, accès limité, basée sur les commentaires.
* **Disponibilité limitée (LA)** : déploiement contrôlé pour la validation finale.
* **Disponibilité générale (GA, General Availability)** : version complète pour tous les clients et clientes autorisés.

+++

+++ Toutes les fonctionnalités passent-elles par Beta et la disponibilité limitée ?

Non. Certaines fonctionnalités sont publiées directement en disponibilité générale ou uniquement à Los Angeles, selon leur nature et leur état de préparation. Le chemin de publication est adapté à chaque fonctionnalité pour équilibrer l’agilité, la qualité et la stabilité.

+++

+++ Comment puis-je participer à des programmes Beta ou à disponibilité limitée ?

L’accès s’effectue sur invitation ou sur demande auprès de votre représentant Adobe. La participation permet de concevoir les fonctionnalités et de s’assurer que vos cas d’utilisation sont pris en compte dans la version finale.

+++

+++ À quelle fréquence les notes de mise à jour sont-elles mises à jour ?

Les notes de mise à jour sont mises à jour en permanence. Au-delà des versions mensuelles, la section _Dernières mises à jour_ est actualisée chaque fois que de nouvelles fonctionnalités ou améliorations sont mises en production.

+++
