---
solution: Journey Optimizer
product: journey optimizer
title: Corrections de marque basées sur l’IA
description: Découvrez comment configurer et utiliser les corrections de marque basées sur l’IA dans Adobe Journey Optimizer.
feature: Brand Validation
topic: Content Management
role: User
level: Intermediate
exl-id: dd4fde0e-86c8-4a57-86ba-202e3be2c41f
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: 993
ht-degree: 1%

---


# Corrections de marque basées sur l’IA {#brand-corrections}

>[!AVAILABILITY]
>
>Cette fonctionnalité est disponible pour Adobe Journey Optimizer et s’applique aux canaux de contenu push, SMS et Web.

## Vue d’ensemble {#overview}

Lorsque le contenu est marqué pendant le contrôle qualité de la marque, Adobe Journey Optimizer peut automatiquement générer des équivalents textuels corrigés ou améliorés à l’aide de l’IA générative. Au lieu de réécrire manuellement les copies marquées, vous recevez des suggestions intégrées conformes aux directives de votre marque, que vous pouvez examiner, prévisualiser et appliquer en un seul clic.

Cela transforme l’étape du contrôle qualité de la marque, qui est passée d’un point de contrôle bloquant à une **expérience à corriger au fur et à mesure**, ce qui réduit le temps consacré aux corrections manuelles et accélère la production de contenu sur l’ensemble des canaux.

Cette fonctionnalité est conçue pour les spécialistes du marketing de contenu, les rédacteurs et les opérateurs de campagnes qui ont besoin de maintenir la conformité de la marque sur les campagnes multicanaux à volume élevé, sans ralentir les workflows de production.

## Fonctionnement {#how-it-works}

Le contrôle qualité de la marque dans Adobe Journey Optimizer évalue le contenu en fonction des directives de votre entreprise en matière de marque, notamment le ton de la voix, la terminologie, les normes de messagerie et les règles éditoriales. Lorsqu’une violation ou un problème de qualité est détecté, le système signale l’élément de contenu affecté et, lorsqu’il est pris en charge, génère automatiquement un remplacement recommandé à l’aide du moteur d’IA générative d’Adobe.

Le flux de bout en bout est le suivant :

1. **Analyse QA de marque** — Lorsque vous exécutez une vérification de marque sur votre contenu (corps de la notification push, texte du message SMS ou bloc de contenu Web), le système évalue chaque élément par rapport aux règles de marque actives.
2. **Détection des violations** — Les éléments qui ne répondent pas à un ou plusieurs critères de marque sont marqués avec un indicateur de gravité (par exemple, critique, avertissement ou suggestion).
3. **Génération de suggestions AI** — Pour chaque élément marqué, le système génère automatiquement un ou plusieurs équivalents textuels corrigés. Les suggestions sont générées par le moteur d’IA générative d’Adobe, qui connaît à la fois le motif de la violation et le contexte des directives de votre marque.
4. **Aperçu en ligne** : le texte de remplacement suggéré apparaît en ligne, directement à côté de l’original avec indicateur. Vous pouvez comparer les versions d’origine et suggérées côte à côte avant d’apporter des modifications.
5. **Appliquer en un clic** — Si la suggestion répond à vos besoins, sélectionnez **Appliquer** pour remplacer le texte avec indicateur par la version générée par l’IA. L’éditeur de contenu est immédiatement mis à jour et l’indicateur de marque est effacé.
6. **Remplacement manuel** — Vous n’êtes jamais verrouillé par la suggestion de l’IA. Vous pouvez modifier la suggestion avant de l’appliquer, la rejeter et écrire votre propre correction, ou ignorer entièrement l’indicateur si le contexte justifie une exception.

>[!NOTE]
>
>Les suggestions générées par l’IA ne sont que des recommandations. Votre équipe conserve un contrôle éditorial complet. Examinez toujours les suggestions dans le contexte de votre campagne avant de les appliquer.

## Conditions préalables {#prerequisites}

Avant d’utiliser les corrections de marque basées sur l’IA, assurez-vous que les conditions suivantes sont remplies :

- **Recommandations relatives à la marque configurées** — Votre organisation doit avoir au moins un profil de marque actif configuré dans Adobe Journey Optimizer. Les profils de marque définissent les règles selon lesquelles le contenu est évalué. Contactez votre administrateur Adobe ou votre responsable de marque pour vérifier que les profils de marque sont publiés et associés à vos sandbox.
- **Fonctionnalités d’IA dédiée au contenu activées** — L’assistance au contenu optimisée par l’IA doit être activée pour votre entreprise et votre sandbox. La gestion s’effectue au niveau du profil de produit dans Adobe Admin Console. Si les suggestions de l’IA n’apparaissent pas après une analyse de la marque, vérifiez auprès de l’administrateur que les droits de génération du contenu de l’IA sont actifs.
- **Type de contenu pris en charge** — Les corrections de marque avec des suggestions d’IA sont prises en charge pour les types de contenu suivants : titre et corps de la notification push, texte du message SMS et blocs de contenu Web modifiés via Journey Optimizer Web Designer. Les ressources multimédias enrichies (images, vidéos) sont évaluées séparément en termes de conformité de la marque et ne sont pas concernées par les corrections de l’IA au niveau du texte.
- **Autorisations de modification** — Vous devez disposer d&#39;un accès en modification au parcours, à la campagne ou au modèle de contenu dans lequel réside le contenu marqué.

## Configuration {#configure}

Aucune configuration supplémentaire n’est requise pour activer les corrections de marque basées sur l’IA si votre entreprise utilise déjà l’assurance qualité de la marque. Le calque de suggestions de l’IA s’active automatiquement lorsque des violations de marque sont détectées dans les types de contenu pris en charge.

Pour exécuter une vérification de marque et accéder aux suggestions de l’IA :

1. Ouvrez votre campagne ou votre parcours dans Adobe Journey Optimizer.
2. Accédez à l’étape du contenu pour le canal approprié (push, SMS ou web).
3. Sélectionnez **Vérifier l’alignement de la marque** (ou ouvrez le panneau **AQ de marque** dans la barre d’outils de l’éditeur de contenu).
4. Attendez la fin de l’analyse. Les éléments marqués sont mis en surbrillance dans la zone de travail et répertoriés dans le panneau **Problèmes de marque** à droite.
5. Pour chaque élément marqué, développez la ligne de l’événement pour afficher le motif de la violation et la suggestion générée par l’IA.
6. Utilisez **Aperçu** pour afficher le texte suggéré rendu dans la zone de travail du contenu.
7. Sélectionnez **Appliquer la suggestion** pour remplacer le texte avec indicateur, ou sélectionnez **Modifier** pour modifier la suggestion avant l’application.
8. Une fois tous les problèmes résolus ou confirmés, relancez la vérification de marque pour confirmer la conformité.

>[!NOTE]
>
>L’application d’une suggestion met à jour le contenu en direct dans l’éditeur, mais ne publie pas ou n’active pas automatiquement la campagne. Vous devez terminer les étapes restantes de configuration et d’activation de la campagne normalement.

### Utilisation de plusieurs suggestions {#multiple-suggestions}

Pour certaines violations, le moteur d’IA peut générer plusieurs alternatives. Dans ce cas, le panneau **Problèmes de marque** affiche une liste numérotée d’options. Utilisez les flèches avant et arrière pour passer en revue les alternatives avant de sélectionner celle qui correspond le mieux à votre intention. Chaque alternative est générée avec une approche stylistique différente - par exemple, l’une peut donner la priorité à la concision tandis qu’une autre souligne l’alignement des tons.

### Corrections en bloc {#bulk-corrections}

Si plusieurs éléments du même élément de contenu sont marqués, vous pouvez appliquer des suggestions individuellement ou utiliser l’action **Appliquer toutes les suggestions** en haut du panneau **Problèmes de marque** pour accepter tous les remplacements générés par l’IA en une seule étape. Examinez attentivement la liste avant d’utiliser l’application en bloc, car cette action remplace simultanément tout le texte marqué.

>[!NOTE]
>
>L’application en bloc est disponible uniquement lorsque tous les éléments marqués d’un indicateur sont associés à une suggestion d’IA. Les éléments sans suggestion disponible (par exemple, les indicateurs de conformité d’image) sont ignorés et restent marqués pour une révision manuelle.

## Rubriques connexes {#related-topics}

- [Présentation des directives relatives à la marque](../content-management/brands.md)
- [Effectuer une vérification de la marque de votre contenu](../content-management/brand-score.md)
- [Assistant IA pour la génération de contenu](../content-management/gs-generative.md)
- [Créer une notification push](create-push.md)
- [Créer un SMS](../sms/create-sms.md)
- [Modification du contenu web avec Journey Optimizer](../web/edit-web-content.md)
