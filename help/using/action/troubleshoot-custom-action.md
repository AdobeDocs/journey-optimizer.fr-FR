---
solution: Journey Optimizer
product: journey optimizer
title: Résolution des problèmes liés aux actions personnalisées
description: Découvrez comment résoudre les problèmes liés à une action personnalisée
badge: label="Disponibilité limitée"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: action, tiers, personnalisé, parcours, API
source-git-commit: 51882b5f664e335c472afd790494f86b300e0e56
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 3%

---


# Résolution des problèmes liés aux actions personnalisées {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>Cette fonctionnalité est réservée à un nombre restreint d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.
>

Vous pouvez tester vos actions personnalisées en envoyant des appels d’API à partir de la section administration de l’interface utilisateur de Journey Optimizer. Cette fonctionnalité vous permet de résoudre les problèmes liés à vos actions personnalisées avant ou après leur utilisation dans un parcours.

En tant qu’administrateur, utilisez la fonctionnalité **[!UICONTROL Envoyer une requête de test]** pour valider vos configurations d’action personnalisée en effectuant des appels API réels directement depuis Adobe Journey Optimizer. Cette fonctionnalité permet de s’assurer que la structure de la requête, les en-têtes, l’authentification et la payload sont correctement formatés avant d’être utilisés dans un parcours.

![](assets/send-test-request.png){width="70%" align="left"}

L’utilisation de cette fonctionnalité simplifie le processus de test et de validation, en veillant à ce que les actions personnalisées fonctionnent correctement dans les parcours en direct.

## Conditions préalables {#troubleshoot-custom-action-prereq}

Pour utiliser la fonctionnalité **[!UICONTROL Envoyer une requête de test]**, une **Action personnalisée** doit être préconfigurée avec une URL, des en-têtes et des paramètres d’authentification.

Pour que les administrateurs puissent utiliser cette fonctionnalité, les autorisations suivantes sont requises :

* Les utilisateurs doivent disposer de l’autorisation **[!DNL Manage journeys events, data sources and actions]**.
* Cette autorisation est incluse dans le rôle *Administrateurs de Parcours*.
* L’autorisation **[!DNL View journeys events]** seule n’est pas suffisante.

En savoir plus sur les autorisations de parcours dans [cette section](../administration/high-low-permissions.md#journey-capability).

## Utilisation de la fonctionnalité Envoyer une requête de test {#troubleshoot-custom-action-use}

Pour tester une action personnalisée, procédez comme suit :

1. Accédez à l’écran de configuration **Actions personnalisées** et sélectionnez une action personnalisée.
1. Cliquez sur le bouton **[!UICONTROL Envoyer la requête de test]** en bas de l’écran de configuration de l’action.
   ![Bouton Envoyer la demande de test dans le panneau Configuration de l’action](assets/test-request.png){width="70%" align="left"}
1. Dans la fenêtre pop-up, vous pouvez spécifier les paramètres de la demande :

   * Si la méthode d’action personnalisée **est GET**, aucune payload n’est requise.
   * Si la méthode d’action personnalisée **est POST**, vous devez fournir une payload JSON.

     >[!NOTE]
     >
     >Adobe Journey Optimizer génère une erreur si la structure de ce fichier JSON est incorrecte, mais ne la génère pas en cas d’incohérence avec un type de données. Par exemple, il n’y aura aucune erreur si un paramètre entier est utilisé pour ce qui doit être une chaîne.

   * Si l’authentification est définie, vous serez invité à saisir les détails d’authentification.

1. Cliquez sur **Envoyer** pour exécuter la requête.
1. La réponse de l’API, y compris les en-têtes et les codes d’état, s’affiche dans l’interface.

## Gestion de l’authentification {#troubleshoot-custom-action-auth}

Lorsqu’une action personnalisée inclut une authentification, Adobe Journey Optimizer exige que l’utilisateur saisisse les détails d’authentification pour chaque requête de test :

* **Authentification de base :** l’utilisateur doit fournir le *mot de passe*.
* **Authentification de la clé API :** l’utilisateur doit saisir la clé API *valeur*.
* **Authentification personnalisée :** l’utilisateur doit fournir les paramètres d’authentification dans la requête *bodyParam*. Deux sections à compléter sont ajoutées dans ce cas : **Requête d’authentification** et **Réponse d’authentification**.

## Avantages clés {#troubleshoot-custom-action-benefits}

En tant qu’administrateur ou administratrice Journey Optimizer, vous pouvez également utiliser des outils externes (par exemple, Postman) pour tester vos actions personnalisées. Les principaux avantages de la fonctionnalité de dépannage intégrée au produit par rapport à un test externe sont répertoriés ci-dessous :

* La demande de test est exécutée par le Parcours **AJO**, ce qui signifie :

   * La structure exacte de la requête (y compris les en-têtes spécifiques à Adobe Journey Optimizer) est utilisée.
   * L’adresse IP source et les en-têtes correspondent à ceux utilisés dans les parcours en direct.

* La fonctionnalité **[!UICONTROL Envoyer une requête de test]** peut être utilisée pour résoudre les problèmes **Live parcours**, car l’action personnalisée est déjà déployée.

* Cette fonctionnalité de test intégrée au produit élimine la nécessité de copier manuellement les informations de configuration entre les outils, ce qui réduit le risque d’erreurs.

## Dépannage {#troubleshoot-custom-action-check}

Si la requête échoue, vous pouvez vérifier les éléments suivants :

* Informations d’authentification saisies dans le test.
* La méthode de requête (GET ou POST) et la payload correspondante.
* Point d’entrée de l’API et en-têtes définis dans l’action personnalisée.
* Utilisez les données de réponse pour identifier les erreurs de configuration potentielles.

