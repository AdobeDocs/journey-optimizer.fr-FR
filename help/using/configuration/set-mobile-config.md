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
source-git-commit: 8fb87d2e2085d98dd8b014df6aa4d734bab4e997
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 10%

---

# Prise en main de la configuration guidée du canal {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="Nom de la configuration mobile et web"
>abstract="Saisissez le nom de votre configuration mobile ou web. Ce nom sera utilisé pour chaque ressource automatiquement créée avec la configuration de canal guidée."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Valider avec Assurance"
>abstract="Assurez-vous de la qualité de la collecte de données et de l’expérience utilisateur de votre application mobile avec Assurance. Cet outil offre une analyse, une validation et une optimisation approfondies. De plus, vous pouvez directement connecter votre application pour vérifier la précision de l’intégration du SDK."
>additional-url="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/assurance" text="Voir la documentation sur l’assurance"


Cette configuration facilite la configuration rapide des canaux marketing, en s’assurant que toutes les ressources requises sont facilement disponibles dans Experience Platform, Journey Optimizer et Data Collection. Cela permet à votre équipe marketing de commencer immédiatement la création de campagne et de parcours.

Pour implémenter efficacement cette fonction, il est essentiel qu’un membre de l’organisation disposant de l’autorité et de la capacité technique de modifier le code du site web ou du mobile supervise la configuration.

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

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="set-mobile-android.md">
<img alt="Lead" src="assets/do-not-localize/config-android.jpeg">
</a>
<div><a href="set-mobile-android.md"><strong>Configuration de la configuration mobile Android</strong>
</div>
<p>
</td>
<td>
<a href="set-mobile-ios.md">
<img alt="Peu fréquent" src="assets/do-not-localize/config-ios.jpeg">
</a>
<div>
<a href="set-mobile-ios.md"><strong>Configuration de la configuration mobile iOS</strong></a>
</div>
<p></td>
<td>
<a href="set-mobile-web.md">
<img alt="Validation" src="assets/do-not-localize/config-web.jpeg">
</a>
<div>
<a href="set-mobile-web.md"><strong> Configuration Web </strong></a>
</div>
<p>
</td>
</tr></table>
