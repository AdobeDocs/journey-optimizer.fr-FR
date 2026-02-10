---
solution: Journey Optimizer
product: journey optimizer
title: Génération automatique de variantes de contenu (Beta)
description: Découvrez comment générer automatiquement des variantes de contenu à l’aide de la simulation basée sur l’IA.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="Private Beta" type="Informative"
hidefromtoc: true
hide: true
exl-id: 9b7fbd43-3d90-458b-8a2f-0bf0ac5437c3
source-git-commit: 692b539f2c7623a14192558c3eba55d90c54f22d
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 97%

---

# Génération automatique de variantes de contenu (Beta){#auto-generate-variants}

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

[!DNL Journey Optimizer] introduit une simulation basée sur l’IA qui peut générer automatiquement plusieurs variantes pour tester votre contenu. Cette fonctionnalité réduit la nécessité de créer manuellement des variantes, ce qui facilite la validation de la logique de personnalisation sur des modèles complexes.

Lors du rendu du contenu à des fins de simulation ou de relecture, le système analyse votre contenu et identifie tous les jetons de personnalisation et toutes les règles de branchement. Il remplace les jetons de personnalisation par des valeurs significatives qui offrent un aperçu quasi réaliste du contenu final.

Prenons un modèle d’e-mail pour les services financiers avec une logique de branchement basée sur **type d’investisseur**, **groupe d’âge**, **état civil**, **vérification de l’identifiant fiscal** et **lieu**. Sans génération de variantes, vous devrez créer manuellement des dizaines de variantes pour valider tous les chemins d’accès. Avec des variantes générées automatiquement, le système génère des variantes représentatives qui couvrent automatiquement ces conditions.  Chaque variante générée est rendue dans le volet d’aperçu, affichant exactement les blocs et conditions appliqués.

## Générer des variantes de contenu

Pour générer des variations pour votre contenu et les prévisualiser, procédez comme suit :

1. Ouvrez votre contenu et sélectionnez **[!UICONTROL Simuler du contenu]**/**[!UICONTROL Simuler des variations de contenu]**.

   ![Option Simuler des variations de contenu](assets/simulate-sample.png)

2. Cliquez sur le bouton **[!UICONTROL Générer]**.

   ![Bouton Générer les variantes](assets/simulate-generate-variant.png)

3. [!DNL Journey Optimizer] génère automatiquement des variantes en fonction des attributs détectés.

4. Passez en revue la liste des variantes générées dans le volet de gauche et sélectionnez une variante pour afficher son rendu personnalisé dans le volet d’aperçu.

>[!NOTE]
>
>Cette fonctionnalité est similaire à la fonctionnalité standard Simuler des variations de contenu. Pour plus d’informations sur les simulations de variations de contenu et sur les mécanismes de sécurisation et limitations associés, consultez cette section : [Simuler des variations de contenu](../test-approve/simulate-sample-input.md)
