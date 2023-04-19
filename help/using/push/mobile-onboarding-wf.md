---
solution: Journey Optimizer
product: journey optimizer
title: Workflow de démarrage rapide de l’intégration mobile
description: Découvrez comment utiliser le workflow de démarrage rapide de l’intégration mobile
topic: Mobile
feature: Push
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: 82477d40-cfea-456b-a7b1-9cfebd76db35
source-git-commit: 1332bc6caf18eaa735d1c99b8e5f70f8a4eaaf2b
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 8%

---

# Workflow de démarrage rapide de l’intégration mobile {#mobile-wf}

La nouvelle **processus de démarrage rapide de l’intégration mobile** est une nouvelle fonctionnalité de produit qui permet de configurer rapidement le SDK Mobile, de commencer à collecter et valider les données d’événement mobile et d’envoyer des notifications push avec . [!DNL Journey Optimizer].

Cette fonctionnalité est accessible à partir de la fonction **[!DNL Adobe Experience Platform Data Collection]** page d’accueil à tous les clients en tant que version bêta publique.

## Prise en main   {#gs-mobile-wf}

Ce nouveau workflow automatise la configuration de la collecte de données en réduisant le nombre total de clics et en accélérant la configuration mobile pour Journey Optimizer. Ce workflow de démarrage rapide vous permet de suivre quatre étapes simples pour [configurer](##setup-mobile-wf), [implémenter](#implement-mobile-wf), [valider](#valid-mobile-wf), et [review](#review-mobile-wf) votre configuration mobile.

Pour accéder au nouveau workflow de démarrage rapide de l’intégration mobile, accédez à **[!DNL Data Collection]** à partir du sélecteur de solution. Sélectionnez ensuite le **[!DNL Start Collecting Mobile Data]** sur la page d’accueil.

![](assets/mobile-wf-home.png)

Voici quelques autres fonctionnalités :

* Processus simple en quatre étapes et interface utilisateur.
* Fournit une configuration de base pour commencer à collecter des données d’événement mobile via le SDK Mobile en quelques minutes.
* Possibilité de tester et de valider un événement push mobile de base à l’aide de l’assurance.
* Crée et configure automatiquement toutes les ressources Journey Optimizer et la collecte de données nécessaires.
* Dans des conseils sur les produits et des info-bulles.
* Fournit une transition naturelle pour une mise en oeuvre plus avancée si nécessaire.

## Configurer {#setup-mobile-wf}

La première étape de ce workflow crée et configure automatiquement toutes les collections de données et ressources Journey Optimizer nécessaires, telles que les propriétés mobiles, les extensions mobiles, l’extension Journey Optimizer, les règles, les éléments de données, etc.

Après avoir accepté les conditions générales de la version bêta, saisissez le nom de votre application mobile, puis cliquez sur **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

Fournissez des informations pour les plateformes iOS et Android, y compris votre ID d’application et vos clés d’authentification ou fichier de clé.

## Mise en œuvre{#implement-mobile-wf}

L’étape suivante fournit des conseils détaillés pour l’installation du code sur votre application mobile.

![](assets/mobile-wf-add-code.png)


## Validation{#valid-mobile-wf}

Vérifiez et vérifiez l’implémentation pour la valider. Vous pouvez envoyer une notification push de test.

![](assets/mobile-wf-valid.png)


## Révision {#review-mobile-wf}

La configuration automatisée est terminée. Vous pouvez désormais accéder à la propriété mobile de votre balise et configurer vos règles ou élément de données, puis commencer à envoyer des notifications push avec Adobe Journey Optimizer.

![](assets/mobile-wf-done.png)


**Rubriques connexes**

* [Prise en main des notifications push](get-started-push.md)
* [Flux de données et composants des notifications push](push-gs.md)
* [Configuration du canal de push](push-configuration.md)
* [Rapport des notifications push](../reports/journey-global-report.md#push-global)
* [Créer une notification push](create-push.md)
