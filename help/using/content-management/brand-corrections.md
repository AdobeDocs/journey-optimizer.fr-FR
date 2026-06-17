---
solution: Journey Optimizer
product: journey optimizer
title: Corrections de marque basées sur l’IA
description: Découvrez comment configurer et utiliser les corrections de marque basées sur l’IA dans Adobe Journey Optimizer.
feature: Brand Guidelines
topic: Content Management
role: User
level: Intermediate
exl-id: a872a3a4-f05b-439d-923e-5191b6e06d34
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: 1000
ht-degree: 3%

---


# Corrections de marque et suggestions éditoriales optimisées par l’IA {#brand-corrections-ai}

>[!AVAILABILITY]
>
>Cette fonctionnalité est disponible pour les utilisateurs de Adobe Journey Optimizer qui disposent de consignes de marque actives et de droits d’assistant AI. Contactez votre représentant Adobe pour obtenir les détails d’accès.

## Vue d’ensemble {#overview}

Adobe Journey Optimizer étend ses outils de conformité de marque optimisés par GenAI à tous les canaux de contenu pris en charge (SMS, notifications push, contenu web et e-mail). Lorsque le moteur AQ de marque détecte un contenu qui enfreint les directives de la marque ou qui ne répond pas aux critères de qualité éditoriale, le système génère automatiquement des alternatives corrigées que vous pouvez examiner et appliquer directement dans le workflow de création.

Cela transforme la validation de la marque d’une liste de contrôle passive en une expérience active, corrigée au fur et à mesure. Au lieu d’identifier les violations et de revenir à l’éditeur pour résoudre chaque problème manuellement, les auteurs de contenu reçoivent des suggestions ciblées générées par l’IA qui s’alignent sur les directives établies en matière de voix, de ton et de style de la marque de l’entreprise, le tout sans quitter l’éditeur de contenu.

Cette fonctionnalité est conçue pour les spécialistes du marketing de contenu, les rédacteurs et les opérateurs de campagnes qui doivent déplacer rapidement le contenu du brouillon vers l’activation, tout en maintenant la conformité de la marque à grande échelle.

## Conditions préalables {#prerequisites}

Avant d’utiliser les corrections de marque optimisées par l’IA, confirmez les points suivants :

- Les **directives relatives aux marques** sont configurées dans Adobe Journey Optimizer. Sans profil de marque actif, le système ne peut pas générer de suggestions de correction alignées sur la marque.
- La fonctionnalité **Assistant IA** est activée pour votre organisation Adobe Experience Cloud.
- Vous disposez des autorisations appropriées pour créer et modifier du contenu pour le canal approprié (SMS, notification push, web ou e-mail).
- Au moins un élément de contenu est disponible à la révision dans l’éditeur de contenu de Journey Optimizer.

>[!NOTE]
>
>Les suggestions de correction de marque sont générées à l’aide de l’infrastructure d’IA générative d’Adobe et sont soumises aux politiques d’utilisation de l’assistant AI applicables à votre entreprise. Consultez toujours les suggestions acceptées avant de les publier.

## Fonctionnement {#how-it-works}

Les corrections de marque s’intègrent directement au flux de validation de l’AQ de marque dans l’éditeur de contenu de Journey Optimizer. Le processus de bout en bout fonctionne comme suit.

**Étape 1 - Analyse de l’assurance qualité de la marque** : lorsque vous exécutez un contrôle de validation de marque sur votre contenu, manuellement à partir du panneau de révision ou déclenché par une règle de workflow, le système évalue chaque bloc de contenu en fonction des directives de votre marque configurée. Les contrôles portent sur le ton de la voix, la terminologie, le langage interdit, les normes éditoriales et les exigences réglementaires.

**Étape 2 — Détection des violations et marquage** : tout segment de contenu qui ne répond pas aux critères de marque ou de qualité éditoriale est marqué d’un indicateur de violation. Le type de violation (par exemple, incohérence de la tonalité, utilisation interdite des termes ou non-conformité aux directives) s’affiche à côté du segment marqué afin que les auteurs comprennent exactement ce qui doit être modifié.

**Étape 3 — Génération de suggestions par l’IA** : pour chaque segment marqué, Journey Optimizer génère automatiquement une ou plusieurs alternatives corrigées à l’aide de l’assistant AI. Les suggestions sont basées sur vos directives de marque actives, ce qui garantit que le texte recommandé reflète la voix, la terminologie et le style éditorial corrects spécifiques à votre organisation.

**Étape 4 - Aperçu et révision sur la ligne** : les corrections suggérées apparaissent sur la ligne, directement à côté du contenu marqué dans le panneau latéral AQ de la marque. Vous pouvez comparer le texte d’origine avec l’alternative générée par l’IA sans quitter l’éditeur.

**Étape 5 — Accepter ou ignorer** : acceptez une suggestion en un seul clic pour remplacer le contenu marqué par la version corrigée. Vous pouvez également ignorer la suggestion et modifier le contenu manuellement. Accepter une suggestion met immédiatement à jour le bloc de contenu et marque la violation comme résolue dans le panneau d’assurance qualité.

**Étape 6 — Revalidation** : après avoir appliqué les corrections, relancez l’analyse du contrôle qualité de la marque pour confirmer que toutes les violations sont résolues avant de publier ou d’activer le contenu dans un parcours ou une campagne.

## Configuration {#configure}

Aucune configuration supplémentaire n’est requise au-delà des conditions préalables standard. La fonctionnalité s’active automatiquement dans le panneau AQ de marque lorsqu’un profil de marque est associé à votre contenu et que l’assistant d’IA est activé pour votre organisation.

Pour commencer à utiliser les corrections de marque optimisées par l’IA :

1. Ouvrez l’éditeur de contenu pour le canal approprié (SMS, notification push, web ou e-mail).
2. Dans la barre d’outils de l’éditeur, sélectionnez **Brand Guidelines** et choisissez le profil de marque applicable dans le menu déroulant.
3. Créez un brouillon ou ouvrez votre contenu, puis sélectionnez **AQ de marque** dans le panneau de révision pour lancer une analyse.
4. Examinez les violations signalées dans le panneau latéral **AQ de marque**. Pour chaque élément marqué, une suggestion générée par l’IA s’affiche automatiquement.
5. Cliquez sur **Appliquer** pour accepter une suggestion, ou sur **Ignorer** pour gérer la correction manuellement.
6. Exécutez à nouveau **AQ de marque** pour vérifier que toutes les violations sont résolues, puis poursuivez votre processus d’approbation ou d’activation standard.

### Canaux pris en charge {#supported-channels}

Les corrections de marque optimisées par l’IA sont disponibles pour les types de contenu suivants dans Adobe Journey Optimizer :

| Canal | Éléments de contenu pris en charge |
|---|---|
| **E-mail** | Ligne d’objet, pré-titre, corps de texte, libellés CTA |
| **SMS** | Corps du message |
| **Notifications push** | Titre, corps de texte |
| **Web** | Titre, corps du texte, libellés de bouton |

>[!NOTE]
>
>Les éléments de contenu pris en charge peuvent varier en fonction de la configuration de votre canal et des directives de marque définies dans votre profil de marque. La validation des images et des ressources visuelles n’est pas prise en compte pour les corrections de texte générées par l’IA.

## Avantages clés {#key-benefits}

**Réduction des efforts de modification manuelle** : les auteurs de contenu n’ont plus besoin de référencer les directives de la marque manuellement pour chaque problème signalé. Les suggestions de l’IA font apparaître des alternatives prêtes à l’emploi, ce qui réduit considérablement le temps passé dans le cycle de correction.

**Conformité cohérente de la marque** : les corrections sont fondées sur les mêmes directives de marque utilisées pour la validation. Les suggestions acceptées sont cohérentes avec les normes approuvées de voix de marque et de rédaction sur tous les canaux, ce qui réduit le risque d’incohérence des messages dans les campagnes multicanaux.

**Production de contenu plus rapide** : en transformant le contrôle qualité de la marque en un workflow de correction au fur et à mesure rationalisé, les équipes déplacent le contenu plus rapidement tout au long du cycle de révision, ce qui réduit le délai entre le brouillon et l’activation. Les opérateurs Campaign peuvent résoudre un ensemble complet de violations en une seule passe sans devoir passer d’un outil à l’autre.

**Couverture cross-canal** : qu’il s’agisse de la production d’une campagne SMS, d’une séquence de notification push mobile ou d’un message web in-app, des suggestions de correction de marque sont disponibles de manière cohérente sur toutes les surfaces de contenu prises en charge, en veillant à ce que les normes de marque soient respectées partout où votre marque communique.

## Rubriques connexes {#related-topics}

- [Prise en main des directives relatives aux marques](../content-management/brands.md)
- [Utiliser l’assistant d’IA pour la génération de contenu](../content-management/ai-assistant.md)
- [Créer un SMS](../sms/create-sms.md)
- [Créer une notification push](../push/create-push.md)
- [Commencer avec le canal web](../web/get-started-web.md)
- [Prévisualiser et tester le contenu](../content-management/preview-test.md)
