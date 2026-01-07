---
solution: Journey Optimizer
product: Journey Optimizer
title: Prévisualiser et tester le contenu
description: Validez la précision du message avant le lancement. Prévisualisez du contenu personnalisé avec des profils de test, envoyez des BAT aux parties prenantes, vérifiez le rendu des e-mails sur les clients, évaluez les scores de spam et testez efficacement plusieurs variations de contenu.
redpen-status: CREATED_||_2025-08-11_20-30-05
exl-id: bd78e0af-573b-4880-a9f1-44467c9db159
source-git-commit: 6b83b015dfd74da9eb58bd06958d0963d81c6489
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 23%

---

# Prévisualiser et tester le contenu{#section-overview}

>[!BEGINSHADEBOX]

**Objectif :** outils de validation de prélancement pour les campagnes et les parcours\
**Utilisateurs du Principal :** responsables de campagne, spécialistes du marketing par e-mail, créateurs de contenu\
**Résultat clé :** détecter les erreurs avant la diffusion au client

>[!ENDSHADEBOX]

Garantissez une diffusion irréprochable des messages en détectant les erreurs avant qu’elles n’atteignent les clients. La prévisualisation du contenu valide la précision de la personnalisation sur différents profils clients, tandis que les outils de test révèlent des problèmes de rendu, des risques de spam et des variations de contenu susceptibles d’avoir un impact sur l’engagement. Accédez à des fonctionnalités complètes pour envoyer des BAT aux parties prenantes, simuler la personnalisation avec des exemples de données, vérifier le rendu des e-mails entre les clients et évaluer les mesures de délivrabilité, le tout avant activation. Principal de ces techniques de validation pour protéger la réputation de la marque, optimiser l’emplacement de la boîte de réception et offrir systématiquement d’excellentes expériences client.

## Prévisualiser et tester le contenu

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=fr)

Prévisualisation et test du contenu

Découvrez comment utiliser des profils de test et des exemples de données d’entrée pour prévisualiser et tester le contenu, envoyer des BAT et garantir la précision de la personnalisation.

[Commencer avec la prévisualisation et les tests](../using/content-management/preview-test.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=fr)

Comment sélectionner des profils de test

Découvrez comment sélectionner et gérer des profils de test pour prévisualiser et tester efficacement du contenu personnalisé.

[Découvrir comment sélectionner des profils de test](../using/content-management/test-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=fr)

Prévisualiser votre contenu à l’aide de profils de test

Guide détaillé pour la prévisualisation de contenu personnalisé à l’aide de profils de test et la simulation de variations de contenu.

[Prévisualiser du contenu avec des profils de test](../using/content-management/preview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=fr)

Envoyer des BAT à l’aide des données de profil de test

Testez et validez vos e-mails en envoyant des BAT à l’aide des données de profil de test afin de garantir la précision du contenu.

[Découvrir comment envoyer des BAT](../using/content-management/proofs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/eye.svg?lang=fr)

Comment tester le rendu des e-mails avec Litmus

Intégrez Litmus pour prévisualiser le rendu des e-mails sur les principaux clients de messagerie et garantir un affichage correct.

[Tester le rendu des e-mails avec Litmus](../using/content-management/rendering.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=fr)

Simulation et test de variations de contenu

Simulez des variations de contenu à l’aide d’exemples de données d’entrée pour tester le contenu personnalisé et garantir sa précision.

[Simuler des variations de contenu](../using/test-approve/simulate-sample-input.md)
:::

::::

## Guide de décision rapide

**Contexte :** ce tableau mappe les objectifs de test à des outils spécifiques dans Adobe Journey Optimizer.

Choisissez votre approche de test en fonction de votre objectif :

| **Si vous devez...** | **Utiliser cet outil** |
|----------------------|-------------------|
| Vérifier que la personnalisation s’affiche correctement | [Profils de test](../using/content-management/test-profiles.md) |
| Test rapide de plus de 10 variations de contenu | [Exemple de données d’entrée](../using/test-approve/simulate-sample-input.md) |
| Obtenir l’approbation des parties prenantes avant l’envoi | [Envoi de BAT](../using/content-management/proofs.md) |
| Vérifier l’affichage des e-mails dans Gmail, Outlook, Apple Mail | [Rendu Litmus](../using/content-management/rendering.md) |
| Amélioration de l’emplacement de la boîte de réception | [Rapport sur les spams](../using/content-management/spam-report.md) |
| Prévisualiser toutes les variations en une seule fois | [Mode Aperçu](../using/content-management/preview.md) |

## Test de la liste de contrôle du workflow

**Contexte :** séquence de test en 5 étapes recommandée applicable à tous les canaux (e-mail, SMS, notification push, web, in-app).

Suivez cette séquence pour une validation complète :

1. **Aperçu** - Utilisez des profils de test pour vérifier correctement les rendus de personnalisation
2. **Variations de test** - Chargez les données d’exemple au format CSV/JSON pour valider plusieurs scénarios.
3. **Vérifier la délivrabilité** (e-mail) - Exécutez le rapport de spam et les tests de rendu
4. **Envoyer des BAT** - Partagez avec les parties prenantes pour révision et approbation
5. **Vérification finale** - Vérifiez que tous les liens, images et CTA fonctionnent correctement.

Conseil **Pro :** testez avec au moins 3 profils représentant différents segments de clients (à forte valeur ajoutée, nouveaux, inactifs) pour détecter les cas particuliers.

## Scénarios courants

**Contexte :** exemples réels montrant comment appliquer des outils de test dans des cas d’utilisation standard.

**Scénario 1 : test des e-mails personnalisés pour une campagne multisegment**
→ Utilisez des [exemples de données d’entrée](../using/test-approve/simulate-sample-input.md) pour tester 20 à 30 variations sans créer de profils de test individuels. Chargez un fichier CSV avec différents attributs de client et prévisualisez-le en une seule fois.

**Scénario 2 : validation du rendu des e-mails avant un envoi majeur**
→ Exécuter [tests Litmus](../using/content-management/rendering.md) pour vérifier l&#39;affichage sur les principaux clients de messagerie, puis vérifiez le [rapport de spam](../using/content-management/spam-report.md) pour vérifier que la boîte de réception est bien placée.

**Scénario 3 : Obtention de l’approbation des parties prenantes**
→ [Envoyez des BAT](../using/content-management/proofs.md) aux réviseurs et réviseuses internes avec les données de profil de test afin qu’ils voient exactement ce que les clients et clientes recevront.

## Principaux points à retenir

- Les **profils de test** sont essentiels pour prévisualiser du contenu personnalisé ; utilisez des exemples de données d’entrée pour tester efficacement plus de 10 variations
- Les **outils spécifiques aux e-mails** incluent les tests de rendu (Litmus), les rapports de spam et les BAT
- **Séquence recommandée :** prévisualiser → tester les variations → vérifier la délivrabilité → envoyer des BAT → vérification finale.
- **Gain de temps :** chargez des fichiers CSV/JSON avec des attributs de client au lieu de créer des profils de test individuels

## Ressources supplémentaires

- **[Utilisation du rapport sur les courriers indésirables](../using/content-management/spam-report.md)** - Évaluez le score de spam du contenu des courriers électroniques à l&#39;aide de la fonctionnalité de rapport sur les courriers indésirables pour améliorer la délivrabilité.

**Rubriques connexes :** [Tester et approuver une page de destination](test-landing-page.md) | [Workflows d’approbation](approve-landing-page.md) | [Création de profils de test](../using/audience/creating-test-profiles.md)
