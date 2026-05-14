---
solution: Journey Optimizer
product: journey optimizer
title: Workflow de démarrage rapide de l’intégration mobile
description: Découvrez comment utiliser le workflow de démarrage rapide de l’intégration mobile.
topic: Mobile
feature: Push
role: Admin
level: Intermediate
badge: label="Beta" type="Informative"
exl-id: 364ef926-3f92-4297-acbd-a283668106ac
TQID: https://experienceleague.adobe.com/bqHcFNTpsuA6--8RiSjygD-8wsx4uwLeWqw9MBtby-4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 369
ht-degree: 98%

---

# Workflow de démarrage rapide de l’intégration mobile {#mobile-wf}

Le nouveau **workflow de démarrage rapide de l’intégration mobile** est une nouvelle fonctionnalité de produit qui permet de configurer rapidement le SDK mobile d’Adobe Experience Platform, de commencer à collecter et valider les données d’événement mobile et d’envoyer des notifications push avec [!DNL Journey Optimizer].

Cette fonctionnalité est accessible à partir de la page d’accueil d’**[!DNL Adobe Experience Platform Data Collection]** à l’ensemble des clientes et clients en tant que version Beta publique.

## Commencer{#gs-mobile-wf}

Ce nouveau workflow automatise la configuration de la collecte de données en réduisant le nombre total de clics et en accélérant la configuration mobile pour Journey Optimizer. Ce workflow de démarrage rapide vous permet de suivre quatre étapes simples pour [configurer](#gs-mobile-wf), [implémenter](#implement-mobile-wf), [valider](#valid-mobile-wf) et [réviser](#review-mobile-wf) votre configuration mobile.

Pour accéder au nouveau workflow de démarrage rapide de l’intégration mobile, accédez à **[!DNL Data Collection]** à partir du sélecteur de solution. Sélectionnez ensuite la vignette **[!DNL Start Collecting Mobile Data]** sur la page d’accueil.

![](assets/mobile-wf-home.png)

Voici quelques autres fonctionnalités :

* Workflow simple en quatre étapes et interface utilisateur.
* Fournit une configuration de base pour commencer à collecter en quelques minutes des données d’événement mobile via le [SDK mobile d’Adobe Experience Platform](https://developer.adobe.com/client-sdks/documentation){target="_blank"}.
* Permet de tester et de valider un événement push mobile de base à l’aide d’[Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html?lang=fr){target="_blank"}.
* Crée et configure automatiquement toutes les ressources de Journey Optimizer et de collecte de données nécessaires.
* Donne des conseils et affiche des info-bulles sur le produit.
* Fournit une transition naturelle pour une implémentation plus avancée, le cas échéant.

## Configurer {#setup-mobile-wf}

La première étape de ce workflow crée et configure automatiquement toutes les ressources Journey Optimizer et de collecte de données nécessaires, telles que les propriétés mobiles, les extensions mobiles, l’extension Journey Optimizer, les règles, les éléments de données, etc.

Après avoir accepté les conditions générales de la version Beta, saisissez le nom de votre application mobile, puis cliquez sur **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

Fournissez les informations pour les plateformes iOS et Android, y compris votre ID d’application et vos clés d’authentification ou votre fichier de clé.

## Implémenter{#implement-mobile-wf}

L’étape suivante fournit des conseils détaillés pour l’installation du code sur votre application mobile.

![](assets/mobile-wf-add-code.png)


## Valider{#valid-mobile-wf}

Vérifiez l’implémentation avant de la valider. Vous pouvez envoyer une notification push de test.

![](assets/mobile-wf-valid.png)


## Réviser {#review-mobile-wf}

La configuration automatisée est terminée. Vous pouvez désormais accéder à la propriété mobile de votre balise et configurer vos règles ou votre élément de données, puis commencer à envoyer des notifications push avec Adobe Journey Optimizer.

![](assets/mobile-wf-done.png)


**Rubriques connexes**

* [Prise en main des notifications push](../../rp_landing_pages/push-landing-page.md)
* [Flux de données et composants des notifications push](push-gs.md)
* [Configuration du canal push](push-configuration.md)
* [Rapport des notifications push](../reports/journey-global-report-cja-push.md#track-link-url-push)
* [Créer une notification push](create-push.md)
