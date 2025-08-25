---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour préliminaires pour Journey Optimizer
description: Notes de mise à jour préliminaires pour Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 75c3db704853b8d2d8920ddd0086681d1fb02a93
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 100%

---

# Notes de mise à jour préliminaires {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).


## Notes de version préliminaire d’août 2025 {#25-8-rn}

**Les notes de version préliminaire ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les notes de mise à jour, à la date de publication.

Voir également les [Notes de mise à jour préliminaires d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Date de publication** : 19 août 2025


### Nouvelles fonctionnalités {#Aug-25-8-features}

<table>
<thead>
<tr>
<th><strong>Suspendre et reprendre les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant suspendre et reprendre les parcours. Cette fonctionnalité offre aux concepteurs et conceptrices du parcours un meilleur contrôle et une plus grande flexibilité en leur permettant de suspendre temporairement les parcours actifs sans perturber l’expérience client. Lorsque le parcours est suspendu, aucune communication n’est envoyée et les profils restent suspendus jusqu’à la reprise du parcours.</p>
<p>Vous pouvez suspendre et reprendre un seul parcours ou un groupe de parcours par le biais d’opérations en bloc.</p>
<p>En outre, vous pouvez appliquer des filtres globaux aux parcours suspendus afin d’exclure les profils en fonction de leurs attributs.</p>
<p><!--img src="assets/do-not-localize/PauseResume.gif"/>--></p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-pause.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vue Calendrier</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une vue Calendrier est désormais disponible dans les listes des parcours et des campagnes. Elle vous permet de visualiser toutes les activations de parcours et de campagnes dans les listes respectives.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements. Avec cette version en disponibilité générale, la fonctionnalité inclut les points suivants :</p>
<ul>
<li>Améliorations de la conception pour la navigation dans les dates</li>
<li>Possibilité de voir les brouillons de campagne si vous avez défini une date de début et une date de fin</li>
<li>Nouveau paramètre permettant de masquer et d’afficher les éléments de calendrier s’exécutant sur une longue période</li>
</ul>
<p><!--img src="assets/do-not-localize/calendar.gif"/>--></p>
<p><!--For more information, refer to the <a href="../building-journeys/journey-ui.md#journeys-calendar">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Utiliser des données Adobe Experience Platform à des fins de personnalisation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Exploitez les données d’Adobe Experience Platform dans l’éditeur de personnalisation pour personnaliser votre contenu. Pour ce faire, les jeux de données nécessaires à la personnalisation de la recherche doivent d’abord être activés par le biais d’un appel API. Une fois que vous avez terminé, vous pouvez utiliser leurs données pour personnaliser votre contenu dans [!DNL Journey Optimizer].</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements. Les améliorations suivantes ont été apportées à cette version à disponibilité générale :</p>
<ul>
<li>Prise en charge des canaux entrants</li>
<li>La fonction d’assistance « datasetLookup » peut désormais être utilisée dans les fragments d’expression et fragments visuels pour personnaliser le contenu à l’aide de données des jeux de données Adobe Experience Platform.</li>
<li>Une option du jeu de données vous permet désormais d’activer les jeux de données pour la personnalisation de la recherche, sans avoir à effectuer d’appel API.</li>
</ul>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Optimisation des chemins de parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer vous fournit désormais les outils nécessaires pour optimiser vos parcours en utilisant l’IA et les frameworks d’expérimentation, tout en garantissant une facilité d’utilisation constante et une différenciation entre les fonctionnalités de condition et d’optimisation.</p>
<p>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour obtenir l’accès.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activité d’action dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer prend en charge une nouvelle activité d’action générique qui vous permet de configurer des actions uniques et des groupes d’actions entrantes multiples, ce qui simplifie la configuration des actions dans la zone de travail de parcours. Cette nouvelle fonctionnalité permet notamment les opérations suivantes :</p>
<ul>
<li>Configuration d’action native simplifiée dans la zone de travail de parcours</li>
<li>Capacité à créer des nœuds entrants à actions multiples</li>
<li>Possibilité d’ajouter une optimisation à toute action de canal intégrée</li>
<li>Possibilité d’ajouter des options d’expérimentation et multilingues à n’importe quelle action</li>
</ul>
<p>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour obtenir l’accès.</p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formulaires personnalisés de la page de destination</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer permet désormais de créer des formulaires personnalisés et de les utiliser dans les pages de destination pour capturer des attributs de profil dans le jeu de données défini pour chaque formulaire.</p>
<p>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour obtenir l’accès.</p>
<p><!--This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.--></p>
<p><!--img src="assets/do-not-localize/FILE.gif"/>--></p>
<p><!--For more information, refer to the <a href="../FILE.md">detailed documentation</a>--></p>
</td>
</tr>
</tbody>
</table>


### Améliorations {#Aug-25-8-improv}

Les améliorations de cette version sont présentées ci-dessous.

* **Administration**

   * **Alertes de surveillance de la configuration des canaux** : vous pouvez désormais vous abonner pour recevoir des alertes système, par e-mail ou dans le centre de notifications Journey Optimizer, au cas où un échec de configuration des canaux se produirait ou si un enregistrement DNS était manquant.

* **Campagnes**

   * **Contrôle des taux dans les campagnes sortantes** - Vous pouvez désormais activer la limitation pour le contrôle des taux des campagnes sortantes (e-mail, SMS, notifications push), ce qui vous permet d’éviter la surcharge sur les systèmes en aval, tels que les pages de destination ou les plateformes d’assistance clientèle.

   * **Planification des campagnes d’action** : les planificateurs de campagnes quotidiens, hebdomadaires et mensuels ont été mis à jour pour une meilleure granularité. Par exemple, vous pouvez désormais définir le nombre de semaines/mois entre les plannings, définir le jour de l’exécution et décider de l’arrêter après un nombre spécifique d’occurrences ou à une date spécifique.

   * **Campagnes d’action transactionnelles planifiées** : les campagnes d’action transactionnelles planifiées sont désormais disponibles pour l’envoi de communications transactionnelles par lots, basées sur l’audience, via les canaux e-mail, SMS et push.

* **Canal - Push**

   * **Date d’expiration des notifications push** : vous pouvez désormais spécifier une date d’expiration pour chaque notification push. Cela empêche l’envoi de messages urgents (comme les soldes du Black Friday) après une certaine date, évitant ainsi une mauvaise expérience pour vos clientes et clients.

* **Canal - E-mail**

   * **Pièces jointes PDF aux e-mails** : vous pouvez désormais joindre des fichiers PDF statiques aux e-mails envoyés avec Journey Optimizer.

* **Canal - SMS**

   * **Opt-out en logique floue** : lorsqu’elle est activée, l’option **Opt-out en logique floue** détecte les messages entrants qui ressemblent fortement aux mots-clés d’opt-out définis (par exemple, « CANCIL ») et envoie automatiquement une réponse de confirmation pour vérifier l’intention de désabonnement de l’utilisateur ou l’utilisatrice. Si la personne confirme en utilisant l’invite définie, elle est désabonnée.

     Notez que l’**Opt-out en logique floue** n’est disponible qu’avec Sinch et Infobip.

   * **Vérifier la connexion SMS** : vous pouvez désormais facilement tester et vérifier vos informations d’identification d’API SMS dans Adobe Journey Optimizer en envoyant un exemple de message à un appareil désigné.

* **Configuration**

   * **Prise en charge des domaines dynamiques** : Journey Optimizer prend désormais en charge la personnalisation du suivi des URL pour les domaines prédéfinis répertoriés au niveau de la configuration des canaux.

   * **Prise en charge des attributs personnalisés avec l’URL de désabonnement en un clic** : a-vec Journey Optimizer, si vous gérez le consentement en dehors d’Adobe, vous pouvez définir un point d’entrée personnalisé externe en définissant votre propre lien de désabonnement en un clic dans la configuration de l’e-mail. Lorsque les personnes destinataires cliquent sur le lien de désabonnement, Journey Optimizer ajoute certains paramètres par défaut, spécifiques au profil, à l’événement de mise à jour du consentement.

     Pour personnaliser davantage votre lien de désabonnement en un clic, vous pouvez maintenant définir des attributs personnalisés qui seront ajoutés à l’événement de consentement.

* **Prise de décision**

   * **Joindre des fragments aux éléments de décision** : Journey Optimizer permet désormais de joindre des fragments aux éléments de décision qui peuvent être utilisés dans les campagnes d’expérience basées sur du code par le biais de politiques de décision.

* **Parcours**

   * **Opérations de parcours en masse** : dans la liste de vos parcours, vous pouvez désormais sélectionner plusieurs éléments. Une fois la sélection réalisée, vous pouvez suspendre ou reprendre jusqu’à 10 parcours à la fois.
