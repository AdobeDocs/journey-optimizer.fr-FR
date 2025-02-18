---
solution: Journey Optimizer
product: journey optimizer
title: Test d’une action personnalisée
description: Découvrez comment résoudre les problèmes liés à une action personnalisée
badge: label="Disponibilité limitée"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: action, tiers, personnalisé, parcours, API
source-git-commit: 5ce76bd61a61e1ed5e896f8da224fc20fba74b53
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 3%

---


# Résolution des problèmes liés aux actions personnalisées {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>Cette fonctionnalité est réservée à un nombre restreint d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.
>

## Vue d’ensemble

La fonctionnalité **Envoyer la requête de test** permet aux administrateurs de valider leurs configurations d’actions personnalisées en effectuant des appels API réels directement depuis Adobe Journey Optimizer (AJO). Cette fonctionnalité permet de s’assurer que la structure de la requête, les en-têtes, l’authentification et la payload sont correctement formatés avant d’être utilisés dans un parcours.

![](assets/send-test-request.png){width="70%" align="left"}

## Conditions préalables

- **Accès administrateur requis :**
   - Les utilisateurs doivent disposer de l’autorisation **Gérer les événements parcours, les sources de données et les actions »**
   - Cette autorisation est incluse dans le rôle *Administrateurs de Parcours*.
   - L’autorisation **Afficher les événements parcours... »** seule, n’est pas suffisante.
- Une **action personnalisée** doit être préconfigurée avec une URL, des en-têtes et des paramètres d’authentification.

## Utilisation de la fonction Envoyer une requête de test

1. Accédez à l’écran de configuration **Actions personnalisées**.
1. Cliquez sur le bouton **Envoyer la demande de test**.
1. Une fenêtre pop-up s’affiche, vous permettant de définir les paramètres de la requête :
   - Si la méthode d’action personnalisée **est GET**, aucune payload n’est requise.
   - Si la méthode d’action personnalisée **est POST**, vous devez fournir une payload JSON.

     >[!NOTE]
     >
     >AJO génère une erreur si la structure de ce fichier JSON est incorrecte, mais ne la génère pas en cas d’incohérence avec un type de données. Par exemple, il n’y aura aucune erreur si un paramètre entier est utilisé pour ce qui doit être une chaîne.

   - Si l’authentification est définie, vous serez invité à saisir les détails d’authentification.

1. Cliquez sur **Envoyer** pour exécuter la requête.
1. La réponse de l’API, y compris les en-têtes et les codes d’état, s’affiche dans l’interface.

## Gestion de l’authentification

Lorsqu’une action personnalisée inclut une authentification, AJO demande à l’utilisateur de saisir les détails d’authentification pour chaque requête de test :

- **Authentification de base :** l’utilisateur doit fournir le *mot de passe*.
- **Authentification de la clé API :** l’utilisateur doit saisir la clé API *valeur*.
- **Authentification personnalisée :** l’utilisateur doit fournir les paramètres d’authentification dans la requête *bodyParam*. Deux sections à compléter sont ajoutées dans ce cas : **Requête d’authentification** et **Réponse d’authentification**.

## Principales différences par rapport aux outils de test externes (par exemple, Postman)

- La demande de test est exécutée par le Parcours **AJO**, ce qui signifie :
   - La structure exacte de la requête (y compris les en-têtes spécifiques à AJO) est utilisée.
   - L’adresse IP source et les en-têtes correspondent à ceux utilisés dans les parcours en direct.
- Peut être utilisé pour résoudre les problèmes **Live parcours** lorsque l’action personnalisée est déjà déployée.
- Il n’est plus nécessaire de copier manuellement les informations de configuration entre les outils, ce qui réduit le risque d’erreurs.

## Dépannage

- Si la requête échoue, vérifiez les éléments suivants :
   - Informations d’authentification saisies dans le test.
   - La méthode de requête (GET ou POST) et la payload correspondante.
   - Point d’entrée de l’API et en-têtes définis dans l’action personnalisée.
- Utilisez les données de réponse pour identifier les erreurs de configuration potentielles.

Cette fonctionnalité simplifie le processus de test et de validation, en veillant à ce que les actions personnalisées fonctionnent correctement dans les parcours AJO actifs.

