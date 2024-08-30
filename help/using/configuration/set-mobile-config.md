---
solution: Journey Optimizer
product: journey optimizer
title: Configuration de mobile et web
description: Découvrez comment configurer et surveiller les canaux web et mobiles
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: canal, surface, technique, paramètres, optimizer
hide: true
hidefromtoc: true
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
source-git-commit: 06f79b7af3fe3c5ca556e2226d7e241a9c5b56d3
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 17%

---

# Prise en main de la configuration guidée du canal {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="Nom de la configuration mobile et web"
>abstract="Saisissez le nom de votre configuration mobile ou web. Ce nom sera utilisé pour chaque ressource automatiquement créée avec la configuration de canal guidée."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Valider avec Assurance"
>abstract="Adobe Experience Platform Assurance est incorporé à ce workflow pour vous aider à contrôler l’implémentation de votre SDK, ainsi qu’à simuler et valider des événements d’application."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home" text="Présentation de Adobe Experience Platform Assurance"

Cette opération facilite la configuration rapide des canaux marketing, en s’assurant que toutes les ressources requises sont facilement disponibles dans Experience Platform, Journey Optimizer et la collecte de données. Cela permet à votre équipe marketing de commencer à créer des campagnes et des parcours.

La configuration du canal guidée prend en charge les plateformes et canaux suivants.

* Plateformes et SDK :

   * Swift par Apple, iOS

   * Kotlin, Android

   * JavaScript, Web

* Canaux :

   * Mobile In-App

   * Message push mobile

   * Web de base

Notez que pour chaque plateforme que vous souhaitez configurer, il est nécessaire de créer une configuration distincte. Cela est dû au fait que chaque application nécessite une configuration de canal unique, ce qui offre la possibilité de déterminer les canaux que vous souhaitez pour chaque plateforme.

## Conditions préalables {#prereq}

* Pour implémenter efficacement cette fonction, il est essentiel qu’un membre de l’organisation disposant de l’autorité et de la capacité technique de modifier le code du site web ou du mobile supervise la configuration.

  Vous trouverez ci-dessous les autorisations requises pour exécuter la configuration de canal guidée.

+++ Autorisations nécessaires

  <table>
    <thead>
      <tr>
        <th><strong>Solution</strong></th>
        <th><strong>Autorisations</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          <p>Collecte de données</p>
        </td>
        <td>
          <ul>
            <li>Droits d’entreprise &gt; Propriétés</li>
            <li>Droits de propriété : développez, publiez, gérez des extensions et des environnements.</li>
            <li>Interface de l’application : gestion de la configuration de l’application</li>
         </ul>
        </td>
      </tr>
      <tr>
        <td>
          <p>Adobe Experience Platform</p>
        </td>
        <td>
        <ul>
            <li>Collecte de données : gestion des flux de données</li>
           <li>Environnement de test : accorder l’accès aux environnements de test</li>
            <li>Gestion des segments : lecture, création, modification et suppression de définitions de segment</li>
            <li>Gestion des profils : lecture, création, modification et suppression de profils</li>
            <li>Lecture de jeux de données : accès en lecture seule aux jeux de données</li>
            <li>Schémas en lecture seule : accès aux schémas</li>
            <li>Lecture de l’espace de noms d’identité : accès en lecture seule à l’espace de noms d’identité</li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>
         <p>Adobe Journey Optimizer</p>
        </td>
        <td>
          <p>Campagnes : gérez et publiez des campagnes.</p>
        </td>
      </tr>
    </tbody>
  </table>

+++

* Si vous utilisez l’option Configuration existante , veillez à utiliser les versions suivantes de l’extension SDK Mobile Adobe Experience Platform. Pour plus d’informations sur la configuration du SDK, y compris les dépendances requises et le code d’initialisation, reportez-vous à la [documentation suivante](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks?lang=en).

  Pour Android

   * Mobile Core v3.1.0 ou version ultérieure
   * Adobe Journey Optimizer v3.1.0 ou version ultérieure

  Pour iOS

   * Mobile Core v5.2.0 ou version ultérieure
   * Adobe Journey Optimizer v5.1.1 ou version ultérieure

## Ressources créées automatiquement {#auto-create-resources}

La configuration guidée des canaux simplifie la configuration rapide des canaux marketing, rendant ainsi toutes les ressources essentielles facilement disponibles dans les applications Experience Platform, Journey Optimizer et Data Collection. Cela permet à votre équipe marketing de commencer rapidement à créer des campagnes et des parcours. Vous trouverez ci-dessous une liste des ressources générées et configurées automatiquement dans le cadre de la configuration de canal guidée.

Accédez aux onglets ci-dessous pour accéder aux listes complètes de toutes les ressources générées automatiquement :

>[!BEGINTABS]

>[!TAB iOS]

Pour la **configuration initiale**, ci-dessous est une liste complète de toutes les ressources créées sur l’écran **Configuration Details** lorsque vous cliquez sur **Créer automatiquement des ressources**.

<table>
  <thead>
  <tr>
  <th><strong>Solution</strong></th>
  <th><strong>Ressources créées automatiquement</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Balises</p>
  </td>
  <td>
  <ul>
  <li>Propriété de balise mobile</li>
  <li>Règles</li>
  <li>Éléments de données</li>
  <li>Bibliothèque</li>
  <li>Environnements (évaluation, production, développement)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Extensions de balises</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>Assurance AEP</li>
  <li>Consentement (avec activation des stratégies de consentement par défaut)</li>
  <li>Identité (avec ECID par défaut, avec règles de groupement par défaut)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Session d’assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Trains de données</p>
  </td>
  <td>
  <p>Flux de données avec services</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Jeu de données</li>
  <li>Schéma</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Pour la **configuration de canal**, ci-dessous est une liste complète de toutes les ressources créées sur l’écran **Ajouter des canaux**.

<table>
  <thead>
  <tr>
  <th><strong>Solution</strong></th>
  <th><strong>Ressources créées automatiquement</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Configuration de canal</li>
  <li>Chargement des informations d’identification push (message push mobile uniquement)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Android]

Pour la **configuration initiale**, ci-dessous est une liste complète de toutes les ressources créées sur l’écran **Configuration Details** lorsque vous cliquez sur **Créer automatiquement des ressources**.

<table>
  <thead>
  <tr>
  <th><strong>Solution</strong></th>
  <th><strong>Ressources créées automatiquement</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Balises</p>
  </td>
  <td>
  <ul>
  <li>Propriété de balise mobile</li>
  <li>Règles</li>
  <li>Éléments de données</li>
  <li>Bibliothèque</li>
  <li>Environnements (évaluation, production, développement)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Extensions de balises</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>Assurance AEP</li>
  <li>Consentement (avec activation des stratégies de consentement par défaut)</li>
  <li>Identité (avec ECID par défaut, avec règles de groupement par défaut)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Session d’assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Trains de données</p>
  </td>
  <td>
  <p>Flux de données avec services</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Jeu de données</li>
  <li>Schéma</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Pour la **configuration de canal**, ci-dessous est une liste complète de toutes les ressources créées sur l’écran **Ajouter des canaux**.

<table>
  <thead>
  <tr>
  <th><strong>Solution</strong></th>
  <th><strong>Ressources créées automatiquement</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Configuration de canal</li>
  <li>Chargement des informations d’identification push (message push mobile uniquement)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Web]

Pour la **configuration initiale**, ci-dessous est une liste complète de toutes les ressources créées sur l’écran **Configuration Details** lorsque vous cliquez sur **Créer automatiquement des ressources**.

<table>
  <thead>
  <tr>
  <th><strong>Solution</strong></th>
  <th><strong>Ressources créées automatiquement</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Balises</p>
  </td>
  <td>
  <ul>
  <li>Propriété de balise mobile</li>
  <li>Règles</li>
  <li>Éléments de données</li>
  <li>Bibliothèque</li>
  <li>Environnements (évaluation, production, développement)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Extensions de balises</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>Assurance AEP</li>
  <li>Consentement (avec activation des stratégies de consentement par défaut)</li>
  <li>Identité (avec ECID par défaut, avec règles de groupement par défaut)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Session d’assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Trains de données</p>
  </td>
  <td>
  <p>Flux de données avec services</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Jeu de données</li>
  <li>Schéma</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!ENDTABS]
