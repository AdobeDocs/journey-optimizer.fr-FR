---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec le suivi dans Journey Optimizer
description: Découvrez les fonctionnalités de suivi et de surveillance disponibles dans Journey Optimizer.
feature: Monitoring
topic: Administration
role: User
level: Beginner
keywords: suivi, surveillance, analyse, création de rapports, délivrabilité
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '1916'
ht-degree: 100%

---

# Commencer avec le suivi dans Journey Optimizer {#get-started-tracking}

Le suivi vous permet de mesurer l’efficacité de la campagne, d’optimiser les expériences client et de vous assurer que les messages atteignent leurs destinataires. Journey Optimizer offre un suivi complet des interactions client, des performances des diffusions et de l’intégrité du système, ce qui vous permet de prendre des décisions tout en respectant la confidentialité et la conformité.

La plupart des suivis sont automatiquement configurés lors de la création des messages et des parcours. Pour les scénarios avancés, vous pouvez configurer des mesures personnalisées, des paramètres d’URL et intégrer des plateformes d’analyse externes. Accédez à vos données de suivi par le biais de rapports intégrés ou exportez-les pour une analyse approfondie dans Customer Journey Analytics.

>[!BEGINSHADEBOX]

Ce que vous pouvez suivre dans Journey Optimizer :

📧 **Interactions avec les e-mails** : performances des ouvertures, des clics et des liens

🌐 **Comportement web** : pages vues, clics et modèles d’engagement

🛤️ **Performances du parcours** : mesures personnalisées, événements d’étape et chemins de conversion

📊 **Intégrité de la délivrabilité** : taux de rebond, plaintes pour spam et réputation comme expéditeur

⚙️ **Opérations système** : alertes, erreurs et performances des actions personnalisées

>[!ENDSHADEBOX]

Pour commencer, consultez ces rubriques essentielles sur le suivi et la surveillance :

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="../building-journeys/success-metrics.md">
    <img alt="Mesures" src="../assets/do-not-localize/success-metrics.jpeg">
    </a>
    <div>
    <a href="../building-journeys/success-metrics.md"><strong>Configuration des mesures de succès</strong></a>
    </div>
    <p>
    <em>Suivez des KPI personnalisés en fonction des objectifs de l’entreprise.</em>
    <p>
  </td>
  <td>
    <a href="../reports/deliverability.md">
    <img alt="Délivrabilité" src="../assets/do-not-localize/deliverability.jpeg">
    </a>
    <div>
    <a href="../reports/deliverability.md"><strong>Surveillance de la délivrabilité</strong></a>
    </div>
    <p>
    <em>Assurez-vous que vos messages parviennent jusqu’aux boîtes de réception des destinataires.</em>
    <p>
  </td>
  <td>
    <a href="../reports/gs-reports.md">
    <img alt="Création de rapports" src="../assets/do-not-localize/reporting.jpeg">
    </a>
    <div>
    <a href="../reports/gs-reports.md"><strong>Consultation des rapports</strong></a>
    </div>
    <p>
    <em>Accédez aux rapports dynamiques et historiques de vos parcours et campagnes.</em>
    <p>
  </td>
</tr>
</table>

## Suivre les interactions clients sur plusieurs canaux {#tracking-by-channel}

Journey Optimizer fournit des fonctionnalités de suivi pour chaque canal. Voici comment configurer et utiliser le suivi selon le canal.

+++Suivi des e-mails

Le suivi des e-mails est automatiquement activé lorsque vous créez un e-mail. Journey Optimizer suit les ouvertures, les clics et les désabonnements par défaut. Aucune configuration supplémentaire n’est nécessaire.

**Configurez les options de suivi :**

* **Activer/désactiver le suivi** : contrôlez le suivi au niveau des messages lors de la conception de l’e-mail. Vous pouvez choisir de suivre les ouvertures, les clics ou les deux. [En savoir plus](../email/message-tracking.md)

* **Configurer les paramètres de suivi d’URL** : configurez les paramètres de suivi au niveau de la surface pour ajouter automatiquement les identifiants de campagne (utm_campaign, utm_source, etc.) à tous les liens des e-mails. Cela permet de suivre l’attribution dans l’ensemble de votre environnement numérique. [En savoir plus](../email/url-tracking.md)

* **Suivre les liens dans les fragments enregistrés** : lorsque vous enregistrez un fragment à partir d’un contenu pour lequel le suivi est activé, le suivi des liens de ce fragment continue si vous le réutilisez dans d’autres parcours ou campagnes. [En savoir plus](../content-management/save-fragments.md)

* **Ajouter le suivi des pages miroir** : activez les pages miroir pour créer une version web de votre e-mail avec le suivi automatique de la personne qui la consulte. [En savoir plus](../email/message-tracking.md#mirror-page)

**Surveiller les performances :** affichez les mesures en temps réel dans les rapports de campagne et de parcours, y compris les ouvertures, les clics et les performances au niveau des liens. [Rapports de campagnes](../reports/campaign-global-report-cja-email.md) | [Rapports de parcours](../reports/journey-global-report-cja-email.md)

+++

+++Suivi web

Le suivi web nécessite une configuration explicite pour suivre les interactions des utilisateurs et utilisatrices avec vos modifications sur le site web.

**Configurez le suivi des clics :**

Lorsque vous créez une page web, vous pouvez sélectionner des éléments spécifiques (boutons, images, liens) dont vous souhaitez effectuer le suivi. Le suivi des clics s’active pour ces éléments sans code supplémentaire. [En savoir plus](../web/monitor-web-experiences.md)

* **Suivre tout élément interactif** : sélectionnez des boutons, des images, des liens ou tout élément interactif dans votre personnalisation web.
* **Collecte automatique de données** : une fois configuré, Journey Optimizer capture automatiquement les événements de clic et les associe à des profils.
* **Surveiller en temps réel** : suivez les interactions utilisateur au fur et à mesure qu’elles se produisent pour valider l’efficacité de la personnalisation.

**Afficher les données de suivi :** permet d’accéder aux mesures d’affichage, aux taux de clics publicitaires et aux performances au niveau des éléments dans les rapports. [Rapports de campagne](../reports/campaign-global-report-cja-web.md) | [Rapports de parcours](../reports/journey-global-report-cja-web.md)

+++

+++Suivi des notifications push

Le suivi des notifications push est automatiquement activé et capture les impressions (diffusées), les clics (activés) et les ouvertures (application lancée). Pour optimiser la valeur de suivi, configurez les éléments cliquables dans votre contenu push.

**Configurez les éléments suivis :**

* **Comportement en cas de clic dans le corps** : définissez ce qui se produit lorsqu’on appuie sur la notification : ouvrir l’application, accéder à un lien profond ou ouvrir une URL web. Chaque action est automatiquement suivie. [En savoir plus](../push/design-push.md#on-click-behavior)

* **Ajouter des boutons d’action** : incluez jusqu’à 3 boutons (Android) ou plusieurs boutons (iOS) avec un suivi indépendant pour chaque action de bouton (ouverture d’application, lien profond, URL web). [En savoir plus](../push/design-push.md#add-buttons-push)

* **Activer le suivi** : vérifiez que le suivi est activé dans votre activité de parcours push ou dans les paramètres de suivi de la campagne. [En savoir plus](../push/create-push.md#create)

>[!NOTE]
>
>Le suivi des notifications push nécessite une implémentation de SDK mobile. Vérifiez que le SDK mobile Adobe Experience Platform est correctement configuré pour votre application. [En savoir plus](../push/push-configuration.md#integrate-mobile-app)

**Analyser l’engagement :** affichez les taux de clics publicitaires, les performances des boutons et les détails des liens suivis dans les rapports. [Rapports de campagne](../reports/campaign-global-report-cja-push.md) | [Rapports de parcours](../reports/journey-global-report-cja-push.md)

+++

+++Suivi des messages in-app

Les messages in-app effectuent automatiquement le suivi des affichages et des interactions d’utilisation. Configurez les déclencheurs et le contenu pour optimiser l’efficacité du suivi.

**Configurez le suivi :**

* **Définir des règles d’affichage** : définissez quand et où les messages in-app apparaissent à l’aide de déclencheurs (lancement d’application, chargement d’écran), de règles de fréquence et de conditions d’audience. Une configuration appropriée garantit un suivi précis des messages déclenchés et affichés.

* **Ajouter des éléments suivis** : incluez des boutons, des liens et des éléments interactifs dans le contenu de votre message. Chaque interaction est automatiquement suivie avec des libellés détaillés.

* **Optimiser le timing de l’affichage** : configurez les règles relatives au jour de la semaine et à l’heure de la journée afin de maximiser la probabilité que les messages déclenchés s’affichent réellement pour les utilisateurs et les utilisatrices.

[Découvrez comment créer des messages in-app.](../in-app/create-in-app.md)

**Éléments suivis :** Journey Optimizer capture automatiquement les affichages, les clics sur les boutons, les rejets, les mesures déclenchées ou affichées et les performances des liens. [Rapports de campagne](../reports/campaign-global-report-cja-inapp.md) | [Rapports de parcours](../reports/journey-global-report-cja-inapp.md)

+++

+++Suivi des SMS et MMS

Le suivi des SMS nécessite une configuration minimale : Journey Optimizer raccourcit et suit automatiquement les liens que vous incluez dans les messages.

**Fonctionnement :**

* **Suivi automatique des liens** : ajoutez une URL à votre contenu SMS à l’aide de la fonction d’assistance d’URL. Journey Optimizer raccourcit automatiquement le lien et effectue le suivi des clics sans configuration supplémentaire. Pour utiliser le raccourcissement des URL, vous devez d’abord configurer un sous-domaine SMS. [En savoir plus](../sms/sms-subdomains.md)

* **Suivi des messages entrants** : les réponses des destinataires sont automatiquement capturées, ce qui vous permet de surveiller les conversations bidirectionnelles et les modèles de réponse. [En savoir plus](../sms/sms-opt-out.md#sms-native-keywords)

**Afficher les mesures :** accédez aux données de clic sur les liens, aux volumes de messages entrants et aux performances des types de messages dans les rapports. [Rapports de campagne](../reports/campaign-global-report-cja-sms.md) | [Rapports de parcours](../reports/journey-global-report-cja-sms.md)

+++

+++Suivi des expériences basées sur du code

Les expériences basées sur du code nécessitent une configuration d’implémentation pour envoyer des données de suivi à Adobe Experience Platform.

**Conditions préalables requises :**

Avant que le suivi ne fonctionne, vous devez configurer votre implémentation pour envoyer des événements d’interaction (affichages, clics) à Adobe Experience Platform. Cela nécessite les éléments suivants :

* Configuration d’un train de données configuré pour Adobe Experience Platform. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr)
* Mise en œuvre de la collecte d’événements dans votre code à l’aide du SDK web ou du SDK mobile.
* Envoi d’événements d’affichage et d’interaction lorsque le contenu est affiché ou qu’il fait l’objet d’un clic.

[En savoir plus sur les conditions préalables à l’implémentation](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**Éléments suivis :** une fois implémenté, suivez les affichages, les clics, les taux de clic publicitaire et les performances au niveau des éléments sur tous les points de contact numériques (sites web, applications mobiles, appareils IoT, etc.). [Rapports de campagne](../reports/campaign-global-report-cja-code.md) | [Rapports de parcours](../reports/journey-global-report-cja-code.md)

+++

+++Suivi des cartes de contenu

Les cartes de contenu effectuent automatiquement le suivi des interactions d’utilisation. Configurez le contenu et les règles d’affichage pour contrôler le comportement du suivi.

**Mise en œuvre :**

* **Conception du contenu suivi** : ajoutez des boutons et des liens à votre carte de contenu. Chaque élément interactif est automatiquement suivi avec des libellés et des URL.

* **Configurer la persistance** : les cartes de contenu persistent entre les sessions d’application, ce qui vous permet de suivre les modèles d’engagement à long terme. Définissez des règles d’expiration pour contrôler la durée pendant laquelle les cartes peuvent être suivies.

* **Configurer des règles d’affichage** : définissez quand et où les cartes doivent apparaître afin d’assurer le suivi précis des affichages par rapport aux interactions.

[Découvrez comment configurer des cartes de contenu.](../content-card/create-content-card.md)

**Surveiller l’engagement :** suivez les affichages, les clics, les taux de clics publicitaires et les schémas d’engagement sur plusieurs sessions. [Rapports de campagne](../reports/campaign-global-report-cja-content.md) | [Rapports de parcours](../reports/journey-global-report-cja-content.md)

+++

+++Suivi des pages de destination

Les pages de destination sont fournies avec un suivi intégré qui ne nécessite aucune configuration supplémentaire. Journey Optimizer capture automatiquement les visites, les conversions et les taux de rebond.

**Contenu suivi automatiquement :**

* **Visites** : nombre total de visites et de visites uniques pour mesurer la portée
* **Conversions** : envois de formulaires, confirmations d’abonnement ou autres actions définies
* **Taux de rebond** : pourcentage de personnes quittant la page sans interaction
* **Tendances des performances** : données de série temporelle montrant l’évolution des mesures

[Découvrez comment configurer des pages de destination.](../landing-pages/create-lp.md)

**Surveiller les performances :** suivez les modèles de visite, les taux de conversion et les taux de rebond au fil du temps pour comprendre comment les personnes interagissent avec vos formulaires ; identifiez les améliorations à apporter. [Rapports de campagne](../reports/lp-report-global-cja.md)

+++

## Suivre votre parcours et l’activité de la campagne {#journey-campaign-tracking}

Au-delà du suivi au niveau des canaux, configurez le suivi pour mesurer les performances globales et comprendre le comportement de la clientèle dans vos initiatives marketing.

* **Définir des mesures de succès personnalisées** : configurez des KPI spécifiques alignés sur les objectifs de votre entreprise (achats, inscriptions, renouvellements, etc.) au-delà des mesures d’engagement standard. [En savoir plus](../building-journeys/success-metrics.md)

* **Activer les événements d’étape de parcours** : activez le suivi détaillé de chaque action entreprise par la clientèle lorsqu’elle se déplace dans les parcours. Vous obtenez ainsi une visibilité granulaire sur les points d’entrée et de sortie, les choix de parcours et les points d’abandon. [En savoir plus](../reports/journey-step-events-overview.md)

* **Configurer la planification** : configurez l’optimisation de l’heure d’envoi pour suivre les performances sur différentes stratégies de timing et identifier les fenêtres d’envoi optimales. [En savoir plus](../building-journeys/send-time-optimization.md)

* **Configurer la surveillance des actions personnalisées** : configurez le suivi des intégrations à des systèmes externes pour surveiller les appels API, les temps de réponse et les modèles d’erreur. [En savoir plus](../action/reporting.md)

* **Créer des rapports personnalisés et exporter des données** : créez des rapports personnalisés et exportez les données de suivi vers des systèmes externes pour une analyse plus approfondie. [En savoir plus](../reports/sharing-overview.md)

* **Afficher des performances unifiées :** accédez à des rapports complets pour les campagnes et les parcours, afin de comparer les performances sur les e-mails, les notifications push, les SMS et d’autres canaux ; déterminez les combinaisons qui génèrent les meilleurs résultats. [Rapports de campagne](../reports/campaign-global-report-cja.md) | [Rapports de parcours](../reports/journey-global-report-cja.md)

## Suivre les performances d’optimisation et de prise de décision {#optimization-decisioning-tracking}

Journey Optimizer effectue automatiquement le suivi des expériences d’optimisation, des stratégies de ciblage et des performances de prise de décision. Configurez vos paramètres pour garantir une collecte de données appropriée.

### Configurer le suivi des optimisations {#optimization-tracking}

* **Optimisation de vos campagnes et parcours** :

   * Lorsque vous créez une expérience, sélectionnez les mesures à suivre (conversions, clics, événements personnalisés). Journey Optimizer collecte automatiquement les données de performance de chaque traitement. [En savoir plus](../content-management/optimization-experimentation.md)

   * Créez des règles de ciblage pour diffuser des contenus adaptés à chaque segment d’audience. Journey Optimizer effectue automatiquement le suivi des mesures d’engagement pour chaque groupe ciblé, ce qui vous permet de comparer les performances entre les segments. [En savoir plus](../content-management/optimization-targeting.md)

* **Optimisation des chemins de parcours** : ajoutez une activité **Optimiser** à votre parcours et configurez plusieurs chemins d’accès. Journey Optimizer suit automatiquement les chemins empruntés par les profils et mesure les performances. [En savoir plus](../building-journeys/optimize.md)

Pour analyser les résultats : affichez les taux de conversion, la signification statistique et l’effet élévateur entre les traitements dans les rapports d’expérimentation, ou comparez les mesures d’engagement des différents segments ciblés. [Rapport de campagne d’expérimentation](../reports/campaign-global-report-cja-experimentation.md) | [Rapport de parcours d’expérimentation](../reports/journey-global-report-cja-experimentation.md) | [Rapport de ciblage de parcours ](../reports/journey-global-report-cja.md#targeting)

### Suivre les performances de la prise de décision {#decisioning-tracking}

Lorsque vous utilisez la prise de décision pour personnaliser le contenu, Journey Optimizer effectue automatiquement le suivi des événements de décision, des impressions et des clics, sans configuration supplémentaire.

* **Capture automatique des événements** : Journey Optimizer capture automatiquement les événements de décision chaque fois qu’un élément de décision est sélectionné pour un profil.
* **Suivi des impressions** : pour les e-mails, les impressions sont automatiquement suivies. Pour les expériences basées sur du code, vous devez implémenter des événements d’affichage de proposition dans votre code. [En savoir plus](../code-based/code-based-implementation-samples.md#client-side-how)
* **Suivi des clics** : pour les e-mails, les clics sur les éléments de décision sont automatiquement suivis. Les expériences basées sur du code nécessitent l’implémentation d’événements de clic.

>[!NOTE]
>
>Pour suivre la prise de décision dans les **expériences basées sur du code**, assurez-vous que votre implémentation envoie des événements d’interaction des propositions (affichages et clics) à Adobe Experience Platform à l’aide du SDK web ou du SDK mobile. [En savoir plus](../experience-decisioning/data-collection/schema-requirement.md)

Pour surveiller les performances : affichez les KPI de prise de décision, comparez les éléments de décision, analysez les stratégies de sélection et surveillez les performances du modèle d’IA dans les rapports. [En savoir plus](../experience-decisioning/cja-reporting.md)

## Contrôle de l’utilisation des données de suivi {#data-governance}

Les politiques de gouvernance des données vous permettent de contrôler l’utilisation des données de suivi dans l’ensemble de votre organisation :

* **Étiqueter les données de suivi sensibles** : appliquez des étiquettes de gouvernance aux données comportementales suivies (par exemple, les clics sur du contenu de santé, les interactions avec des produits financiers) pour les marquer comme sensibles ou réglementées.

* **Limiter l’utilisation des données** : créez des politiques qui empêchent les données de suivi étiquetées d’être utilisées dans certains canaux, exportées vers des systèmes tiers ou utilisées pour certains cas de personnalisation.

* **Application automatique** : Journey Optimizer vérifie automatiquement les politiques de gouvernance lors de la création de parcours et de campagnes et bloque la publication si l’utilisation des données suivies va à l’encontre des politiques définies.

La gouvernance des données garantit la conformité aux réglementations telles que le RGPD et le CCPA tout en vous permettant de suivre et d’analyser le comportement de la clientèle dans les limites autorisées. [En savoir plus](../action/action-privacy.md)

## Surveiller la délivrabilité et l’intégrité du système {#monitoring-capabilities}

Au-delà du suivi de l’engagement, configurez la surveillance pour vous assurer que les messages parviennent correctement jusqu’aux boîtes de réception et que les systèmes fonctionnent de manière optimale.

La surveillance de la délivrabilité permet de s’assurer que vos messages atteignent les boîtes de réception des destinataires et préservent la bonne réputation de l’expéditeur en suivant les indicateurs clés :

* **Consultez régulièrement la liste de suppression** pour comprendre pourquoi les adresses sont bloquées et maintenir la liste à jour. [En savoir plus](../reports/suppression-list.md)

* **Analysez les erreurs de diffusion** pour diagnostiquer les échecs et prendre des mesures correctives. [En savoir plus](../configuration/email-error-types.md)

* **Suivez les bonnes pratiques** pour DMARC, SPF et DKIM afin d’optimiser le placement en boîte de réception. [En savoir plus](../reports/deliverability.md)

Configurez une surveillance proactive afin de recevoir des notifications en temps réel sur les événements critiques et les problèmes système, ce qui vous permet de répondre rapidement avant qu’ils n’affectent vos expériences client :

* **Configurer des alertes** : configurez des notifications en temps réel pour les erreurs de parcours, les échecs d’actions personnalisées et les problèmes critiques afin de répondre rapidement aux problèmes. [En savoir plus](../reports/alerts.md)

* **Activer les journaux d’audit** : activez la journalisation d’audit pour suivre toutes les actions sur les ressources à des fins de conformité et de résolution des problèmes. [En savoir plus](../privacy/audit-logs.md)

* **Surveiller les intégrations** : suivez les performances des actions personnalisées et la connectivité système externe pour identifier rapidement les problèmes d’intégration. [En savoir plus](../action/reporting.md)

