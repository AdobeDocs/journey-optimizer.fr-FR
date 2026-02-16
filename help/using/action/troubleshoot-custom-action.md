---
solution: Journey Optimizer
product: journey optimizer
title: Résoudre les problèmes liés aux actions personnalisées
description: Découvrez comment résoudre les problèmes liés aux actions personnalisées.
feature: Journeys, Actions, Custom Actions, Monitoring
topic: Administration
role: Developer, Admin
level: Experienced
keywords: action, tiers, personnalisé, parcours, API
exl-id: c0bb473a-82dc-4604-bd8a-020447ac0c93
source-git-commit: bae446ea38a0cb97487201f7dcf4df751578ad0a
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 61%

---

# Résoudre les problèmes liés aux actions personnalisées {#troubleshoot-a-custom-action}

Vous pouvez tester vos actions personnalisées en envoyant des appels API à partir de la section administration de l’interface d’utilisation de Journey Optimizer. Cette fonctionnalité vous permet de résoudre les problèmes liés à vos actions personnalisées avant ou après leur utilisation dans un parcours.

En tant qu’administrateur ou administratrice, utilisez la fonctionnalité **[!UICONTROL Envoyer une demande de test]** pour valider vos configurations d’actions personnalisées en effectuant des appels API réels directement depuis Adobe Journey Optimizer. Cette fonctionnalité permet de s’assurer que la structure de la demande, les en-têtes, l’authentification et la payload sont correctement formatés avant leur utilisation dans un parcours.

![](assets/send-test-request.png){width="70%" align="left"}

L’utilisation de cette fonctionnalité simplifie le processus de test et de validation, en veillant au bon déroulement des actions personnalisées dans les parcours actifs.

>[!NOTE]
>
>Si le proxy IP (sortie) est activé pour votre organisation, l’appel **[!UICONTROL Envoyer la requête de test]** le contourne. Pour confirmer le routage du proxy, exécutez un test ou un parcours en direct. En savoir plus sur le proxy IP (sortie) et son activation dans [Intégration à des systèmes externes](../configuration/external-systems.md#faq).


## Conditions préalables {#troubleshoot-custom-action-prereq}

Pour utiliser la fonctionnalité **[!UICONTROL Envoyer une demande de test]**, une **action personnalisée** doit être préconfigurée avec une URL, des en-têtes et des paramètres d’authentification.

Pour que l’administration puisse utiliser cette fonctionnalité, les autorisations suivantes sont requises :

* Les utilisateurs et utilisatrices doivent disposer de l’autorisation **[!DNL Manage journeys events, data sources and actions]**.
* Cette autorisation est incluse dans le rôle *Administrateurs et administratrices de parcours*.
* L’autorisation **[!DNL View journeys events]** seule n’est pas suffisante.

En savoir plus sur les autorisations de parcours dans [cette section](../administration/high-low-permissions.md#journey-capability).

## Utiliser la fonctionnalité Envoyer une demande de test {#troubleshoot-custom-action-use}

Pour tester une action personnalisée, procédez comme suit :

1. Accédez à l’écran de configuration **Actions** et sélectionnez une action personnalisée.
1. Cliquez sur le bouton **[!UICONTROL Envoyer une demande de test]** en bas de l’écran de configuration de l’action.
   ![Bouton Envoyer une demande de test du panneau Configuration de l’action](assets/test-request.png){width="70%" align="left"}
1. Dans la fenêtre contextuelle qui s’affiche, spécifiez les paramètres de la demande :

   * Si la **méthode d’action personnalisée est GET**, aucune payload n’est requise.
   * Si la **méthode d’action personnalisée est POST**, vous devez fournir une payload JSON.

     >[!NOTE]
     >
     >Adobe Journey Optimizer génère une erreur si la structure de ce fichier JSON est incorrecte, mais pas en cas d’incohérence avec un type de données. Par exemple, il n’y aura aucune erreur si un paramètre entier est utilisé au lieu d’une chaîne.

   * Si l’authentification est définie, il vous est demandé de saisir les détails de l’authentification.

1. Cliquez sur **Envoyer** pour exécuter la demande.
1. La réponse de l’API, y compris les en-têtes et les codes d’état, s’affiche dans l’interface.

## Gestion de l’authentification {#troubleshoot-custom-action-auth}

Lorsqu’une action personnalisée comprend une authentification, Adobe Journey Optimizer exige que la personne saisisse les détails d’authentification pour chaque demande de test :

* **Authentification de base :** la personne doit fournir le *mot de passe*.
* **Authentification par clé API :** la personne doit saisir la *valeur* de la clé API.
* **Authentification personnalisée :** la personne doit fournir les paramètres d’authentification dans la demande *bodyParam*. Deux sections sont ajoutées dans ce cas : **Demande d’authentification** et **Réponse d’authentification**.

## Avantages clés {#troubleshoot-custom-action-benefits}

En tant qu’administrateur ou administratrice de Journey Optimizer, vous pouvez également utiliser des outils externes (par exemple, Postman) pour tester vos actions personnalisées. Les principaux avantages de la fonctionnalité de dépannage intégrée au produit par rapport à un test externe sont répertoriés ci-dessous :

* La demande de test est exécutée par le **Parcours AJO**, ce qui offre les avantages suivants :

   * La structure exacte de la requête (y compris les en-têtes spécifiques à Adobe Journey Optimizer) est utilisée.
   * L’adresse IP source et les en-têtes correspondent à ceux utilisés dans les parcours actifs.

* La fonctionnalité **[!UICONTROL Envoyer une demande de test]** permet de résoudre les problèmes liés aux **parcours actifs**, car l’action personnalisée est déjà déployée.

* Cette fonctionnalité de test intégrée au produit élimine la nécessité de copier manuellement les informations de configuration entre les outils, ce qui réduit le risque d’erreurs.

## Résolution des problèmes {#troubleshoot-custom-action-check}

Si la demande échoue, vous pouvez vérifier les éléments suivants :

* Les informations d’authentification saisies dans le test.
* La méthode de la demande (GET ou POST) et la payload correspondante.
* Le point d’entrée de l’API et les en-têtes définis dans l’action personnalisée.
* Utilisez les données de réponse pour identifier les erreurs de configuration potentielles.

## Gestion des événements d’ignorance et des délais d’inactivité {#handling-discard-events-and-idle-timeouts}

Lorsqu’une action personnalisée dans un parcours déclenche un événement destiné à démarrer un **second parcours**, assurez-vous que le second parcours est dans un état valide et que l’événement est reconnu. Si l’événement ne remplit pas les conditions d’entrée du second parcours, il peut être **ignoré** et apparaître dans les journaux avec des codes tels que `notSuitableInitialEvent`. Les délais d’inactivité peuvent survenir si le deuxième parcours n’est pas prêt, ce qui entraîne l’abandon des événements dans les journaux.

**Causes fréquentes :**

* **Qualification d’événement non remplie** - Le deuxième parcours utilise un événement basé sur des règles avec une condition de qualification (par exemple, un champ obligatoire doit être non vide, comme une `isNotEmpty` sur un champ spécifique). Si la payload de l&#39;événement ne répond pas à cette condition (par exemple, le champ est vide ou manquant), l&#39;événement est **reçu mais ignoré** et le deuxième parcours n&#39;est pas déclenché. Ce comportement est attendu. La documentation et les journaux confirment que si la condition de qualification n’est pas remplie, l’événement sera ignoré et le parcours ne sera pas déclenché pour ce profil. Vérifiez que la payload envoyée par l’action personnalisée inclut tous les champs et valeurs requis par la configuration d’événement du second parcours. Découvrez comment [configurer des événements basés sur des règles](../event/about-creating.md) et [résoudre les problèmes de réception d’événements](../building-journeys/troubleshooting-execution.md#checking-if-people-enter-the-journey) dans l’exécution de parcours.

* **Second parcours non prêt** - Des délais d’inactivité peuvent se produire si le second parcours n’est pas encore actif (par exemple, pas en mode test ou actif) ou s’il existe un intervalle de temps entre le déclenchement de l’action personnalisée et la réception du second parcours. Assurez-vous que le parcours cible est publié ou en mode test avant le déclenchement de l’action personnalisée.

* **Diagnostic des événements ignorés** - Si vous voyez des événements ignorés dans les journaux, vérifiez les journaux de parcours et les traces Splunk pour confirmer si l’événement a été reçu mais ignoré en raison de la qualification (la payload ne respectait pas la règle) ou de la synchronisation. Assurez-vous que la date de début et la configuration du deuxième parcours sont correctes et que le parcours se trouve dans sa fenêtre de date active.

Pour éviter de ignorer des événements lors de l’association de parcours par le biais d’actions personnalisées, validez la payload de l’événement par rapport à la règle d’événement du deuxième parcours et confirmez que le parcours cible est actif ou en test et dans sa fenêtre de date active.

## Ressources supplémentaires

Parcourez les sections ci-dessous pour en savoir plus sur la configuration et l’utilisation de vos actions personnalisées :

* [Commencer avec les actions personnalisées](../action/action.md) : découvrez en quoi consiste une action personnalisée et comment elle vous permet de vous connecter à vos systèmes tiers.
* [Configurer vos actions personnalisées](../action/about-custom-action-configuration.md) : découvrez comment créer et configurer une action personnalisée.
* [Utiliser des actions personnalisées](../building-journeys/using-custom-actions.md) : découvrez comment utiliser des actions personnalisées dans vos parcours.
* [Transmettre des collections dans des paramètres d’action personnalisés](../building-journeys/collections.md) : découvrez comment transmettre une collection dans des paramètres d’action personnalisés qui est renseignée dynamiquement au moment de l’exécution.

