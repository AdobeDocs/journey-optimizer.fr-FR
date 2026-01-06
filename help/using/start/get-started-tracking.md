---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main du tracking dans Journey Optimizer
description: Découvrez les fonctionnalités de suivi et de surveillance disponibles dans Journey Optimizer
feature: Monitoring
topic: Administration
role: User
level: Beginner
keywords: tracking, surveillance, analyse, reporting, délivrabilité
source-git-commit: 955dbbf944e40cd18530c9777c7f06ad39e45563
workflow-type: tm+mt
source-wordcount: '1916'
ht-degree: 3%

---

# Prise en main du tracking dans Journey Optimizer {#get-started-tracking}

Le tracking vous permet de mesurer l’efficacité de la campagne, d’optimiser les expériences client et de vous assurer que les messages atteignent leurs destinataires prévus. Journey Optimizer offre des fonctionnalités de suivi complètes qui capturent les interactions des clients, les performances des diffusions et l’intégrité du système, ce qui vous aide à prendre des décisions éclairées tout en respectant la confidentialité et en maintenant la conformité.

La plupart des suivis sont automatiquement configurés lors de la création des messages et des parcours. Pour les scénarios avancés, vous pouvez configurer des mesures personnalisées, des paramètres d’URL et intégrer des plateformes d’analyse externes. Accédez à vos données de tracking par le biais de rapports intégrés ou exportez-les pour une analyse plus approfondie dans Customer Journey Analytics.

>[!BEGINSHADEBOX]

Ce que vous pouvez suivre dans Journey Optimizer :

📧 **Interactions e-mail** - Performances des ouvertures, des clics et des liens

🌐 **Comportement web** - Pages vues, clics et modèles d’engagement

🛤️ **Performances du Parcours** - Mesures personnalisées, événements d’étape et chemins de conversion

📊 **Intégrité de la délivrabilité** - Taux de rebond, plaintes pour spam et réputation de l&#39;expéditeur

⚙️ **Opérations système** - Alertes, erreurs et performances des actions personnalisées

>[!ENDSHADEBOX]

Pour commencer, découvrez ces rubriques essentielles pour le suivi et la surveillance :

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="../building-journeys/success-metrics.md">
    <img alt="Mesures" src="../assets/do-not-localize/success-metrics.jpeg">
    </a>
    <div>
    <a href="../building-journeys/success-metrics.md"><strong>Configurer les mesures de succès</strong></a>
    </div>
    <p>
    <em>Suivre les KPI personnalisés en fonction des objectifs de votre entreprise</em>
    <p>
  </td>
  <td>
    <a href="../reports/deliverability.md">
    <img alt="Délivrabilité" src="../assets/do-not-localize/deliverability.jpeg">
    </a>
    <div>
    <a href="../reports/deliverability.md"><strong>Surveiller la délivrabilité</strong></a>
    </div>
    <p>
    <em>Assurez-vous que vos messages atteignent les boîtes de réception des clients</em>
    <p>
  </td>
  <td>
    <a href="../reports/gs-reports.md">
    <img alt="Création de rapports" src="../assets/do-not-localize/reporting.jpeg">
    </a>
    <div>
    <a href="../reports/gs-reports.md"><strong>Explorer le reporting</strong></a>
    </div>
    <p>
    <em>Accédez aux rapports dynamiques et historiques pour vos parcours et campagnes</em>
    <p>
  </td>
</tr>
</table>

## Suivi des interactions client sur plusieurs canaux {#tracking-by-channel}

Journey Optimizer fournit des fonctionnalités de suivi spécifiques au canal. Voici comment configurer et utiliser le suivi pour chaque canal.

+++Tracking d’e-mail

Le suivi des e-mails est automatiquement activé lorsque vous créez un e-mail. Journey Optimizer suit les ouvertures, les clics et les désabonnements par défaut. Aucune configuration supplémentaire n’est nécessaire.

**Configurer les options de tracking :**

* **Activer/désactiver le suivi** - Contrôlez le suivi au niveau des messages lors de la conception de votre e-mail. Vous pouvez choisir de suivre les ouvertures, les clics ou les deux. [En savoir plus](../email/message-tracking.md)

* **Configurer les paramètres de tracking d’URL** - Configurez les paramètres de tracking au niveau de la surface pour ajouter automatiquement des identifiants de campagne (utm_campaign, utm_source, etc.) à tous les liens d’e-mail. Cela permet le suivi de l’attribution dans l’ensemble de votre écosystème numérique. [En savoir plus](../email/url-tracking.md)

* **Suivi des liens dans les fragments enregistrés** - Lorsque vous enregistrez un fragment à partir d’un contenu pour lequel le suivi est activé, les liens de ce fragment restent suivis lorsque vous le réutilisez dans d’autres parcours ou campagnes. [En savoir plus](../content-management/save-fragments.md)

* **Ajouter le suivi des pages miroir** - Activez l’option de page miroir pour créer une version web de votre e-mail avec le suivi automatique de la personne qui la consulte. [En savoir plus](../email/message-tracking.md#mirror-page)

**Surveiller les performances :** affichez des mesures en temps réel dans les rapports de campagne et de parcours, y compris les ouvertures, les clics et les performances au niveau des liens. [&#x200B; Rapports de campagne &#x200B;](../reports/campaign-global-report-cja-email.md) | [Parcours de rapports](../reports/journey-global-report-cja-email.md)

+++

+++Tracking web

Le tracking web nécessite une configuration explicite pour suivre les interactions utilisateur avec vos modifications web.

**Configurer le suivi des clics :**

Lors de la création d’une page web, vous pouvez sélectionner des éléments spécifiques (boutons, images, liens) dont vous souhaitez effectuer le suivi. Cela permet le suivi des clics pour ces éléments sans avoir besoin de code supplémentaire. [En savoir plus](../web/monitor-web-experiences.md)

* **Suivre tout élément cliquable** - Sélectionnez des boutons, des images, des liens ou tout élément interactif dans votre personnalisation web.
* **Collecte automatique de données** - Une fois configuré, Journey Optimizer capture automatiquement les événements de clic et les associe à des profils.
* **Surveiller en temps réel** - Suivez les interactions utilisateur au fur et à mesure qu’elles se produisent pour valider l’efficacité de la personnalisation.

**Afficher les données de suivi :** permet d’accéder aux mesures d’affichage, aux taux de clics publicitaires et aux performances au niveau des éléments dans les rapports. [&#x200B; Rapports de campagne &#x200B;](../reports/campaign-global-report-cja-web.md) | [Parcours de rapports](../reports/journey-global-report-cja-web.md)

+++

+++Suivi des notifications push

Le suivi des notifications push est automatiquement activé et capture les impressions (diffusées), les clics (activés) et les ouvertures (application lancée). Pour optimiser la valeur de suivi, configurez les éléments cliquables dans votre contenu push.

**Configuration des éléments suivis :**

* **Comportement de clic du corps** - Définissez ce qui se produit lorsque les utilisateurs appuient sur la notification : ouvrez l’application, accédez à un lien profond ou ouvrez une URL web. Chaque action est automatiquement suivie. [En savoir plus](../push/design-push.md#on-click-behavior)

* **Ajouter des boutons d’action** - Incluez jusqu’à 3 boutons (Android) ou plusieurs boutons (iOS) avec un suivi indépendant pour chaque action de bouton (ouverture d’application, lien profond, URL web). [En savoir plus](../push/design-push.md#add-buttons-push)

* **Activer le suivi** - Vérifiez que le suivi est activé dans votre activité de parcours push ou dans les paramètres de suivi de la campagne. [En savoir plus](../push/create-push.md#create)

>[!NOTE]
>
>Le suivi des notifications push nécessite une implémentation de SDK mobile. Vérifiez que le SDK mobile Adobe Experience Platform est correctement configuré pour votre application. [En savoir plus](../push/push-configuration.md#integrate-mobile-app)

**Analyser l’engagement :** afficher les taux de clics publicitaires, les performances des boutons et les détails des liens suivis dans les rapports. [&#x200B; Rapports de campagne &#x200B;](../reports/campaign-global-report-cja-push.md) | [Parcours de rapports](../reports/journey-global-report-cja-push.md)

+++

+++Tracking des messages in-app

Les messages in-app effectuent automatiquement le suivi des affichages et des interactions utilisateur. Configurez les déclencheurs et le contenu pour optimiser l’efficacité du suivi.

**Configurer le suivi :**

* **Définir des règles d’affichage** - Définissez quand et où les messages in-app apparaissent à l’aide de déclencheurs (lancement d’application, chargement d’écran), de règles de fréquence et de conditions d’audience. Une configuration appropriée garantit un suivi précis des messages déclenchés et affichés.

* **Ajout d’éléments suivis** - Incluez des boutons, des liens et des éléments interactifs dans le contenu de votre message. Chaque interaction est automatiquement suivie avec des libellés détaillés.

* **Optimiser le timing de l’affichage** - Configurez les règles relatives au jour de la semaine et à l’heure de la journée afin de maximiser la probabilité que les messages déclenchés s’affichent réellement pour les utilisateurs et les utilisatrices.

[Découvrez comment configurer des messages in-app](../in-app/create-in-app.md)

**Ce qui est suivi :** Journey Optimizer capture automatiquement les affichages, les clics sur les boutons, les rejets, les mesures déclenchées ou affichées et les performances des liens. [&#x200B; Rapports de campagne &#x200B;](../reports/campaign-global-report-cja-inapp.md) | [Parcours de rapports](../reports/journey-global-report-cja-inapp.md)

+++

+++Tracking des SMS et MMS

Le suivi des SMS nécessite une configuration minimale : Journey Optimizer raccourcit et suit automatiquement les liens que vous incluez dans les messages.

**Fonctionnement :**

* **Suivi automatique des liens** - Ajoutez une URL à votre contenu SMS à l’aide de la fonction d’assistance d’URL. Journey Optimizer raccourcit automatiquement le lien et effectue le suivi des clics sans configuration supplémentaire. Pour utiliser le raccourcissement des URL, vous devez d’abord configurer un sous-domaine SMS. [En savoir plus](../sms/sms-subdomains.md)

* **Suivi des messages entrants** - Les réponses des destinataires sont automatiquement capturées, ce qui vous permet de surveiller les conversations bidirectionnelles et les modèles de réponse. [En savoir plus](../sms/sms-opt-out.md#sms-native-keywords)

**Afficher les mesures :** accédez aux données de clic sur les liens, aux volumes de messages entrants et aux performances des types de messages dans les rapports. [&#x200B; Rapports de campagne &#x200B;](../reports/campaign-global-report-cja-sms.md) | [Parcours de rapports](../reports/journey-global-report-cja-sms.md)

+++

+++Tracking de l’expérience basé sur le code

Les expériences basées sur du code nécessitent une configuration d’implémentation pour envoyer des données de suivi à Adobe Experience Platform.

**Conditions préalables requises :**

Avant que le suivi ne fonctionne, vous devez configurer votre implémentation pour envoyer des événements d’interaction (affichages, clics) à Adobe Experience Platform. Cela nécessite :

* Configurez un flux de données configuré pour Adobe Experience Platform. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr)
* Mise en œuvre de la collecte d’événements dans votre code à l’aide de Web SDK ou de Mobile SDK.
* Envoi d’événements d’affichage et d’interaction lorsque le contenu est affiché ou cliqué.

[En savoir plus sur les conditions préalables à l’implémentation](../code-based/code-based-prerequisites.md#reporting-prerequisites)

**Ce qui est suivi :** une fois implémenté, suivez les affichages, les clics, les taux de clic publicitaire et les performances au niveau des éléments sur tous les points de contact numériques (sites web, applications mobiles, appareils IoT, etc.). [&#x200B; Rapports de campagne &#x200B;](../reports/campaign-global-report-cja-code.md) | [Parcours de rapports](../reports/journey-global-report-cja-code.md)

+++

+++Suivi des cartes de contenu

Les cartes de contenu effectuent automatiquement le suivi des interactions utilisateur. Configurez le contenu et les règles d’affichage pour contrôler le comportement du suivi.

**Mise en œuvre :**

* **Conception de contenu suivi** - Ajoutez des boutons et des liens à votre carte de contenu. Chaque élément interactif est automatiquement suivi avec des libellés et des URL.

* **Configurer la persistance** - Les cartes de contenu persistent entre les sessions d’application, ce qui vous permet de suivre les modèles d’engagement à long terme. Définissez des règles d’expiration pour contrôler la durée pendant laquelle les cartes restent trackables.

* **Configurer des règles d’affichage** - Définissez quand et où les cartes doivent apparaître afin d’assurer le suivi précis des affichages par rapport aux interactions.

[Découvrez comment configurer des cartes de contenu](../content-card/create-content-card.md)

**Surveiller l’engagement :** suivez les affichages, les clics, les taux de clics publicitaires et les schémas d’engagement sur plusieurs sessions. [&#x200B; Rapports de campagne &#x200B;](../reports/campaign-global-report-cja-content.md) | [Parcours de rapports](../reports/journey-global-report-cja-content.md)

+++

+++Tracking des landing pages

Les landing pages sont fournies avec un suivi intégré qui ne nécessite aucune configuration supplémentaire. Journey Optimizer capture automatiquement les visites, les conversions et les taux de rebond.

**Contenu suivi automatiquement :**

* **Visites** - Nombre total de visites et de visites uniques pour mesurer la portée
* **Conversions** - Envois de formulaires, confirmations d’abonnement ou autres actions définies
* **Taux de rebond** - Pourcentage de visiteurs qui quittent sans interagir
* **Tendances des performances** - Données de série temporelle montrant l’évolution des mesures

[Découvrez comment configurer des pages de destination](../landing-pages/create-lp.md)

**Surveiller les performances :** suivez les modèles de visite, les taux de conversion et les taux de rebond au fil du temps pour comprendre comment les utilisateurs interagissent avec vos formulaires et identifier les améliorations à apporter. [Rapports de campagne](../reports/lp-report-global-cja.md)

+++

## Suivi du parcours et de l’activité de campagne {#journey-campaign-tracking}

Au-delà du suivi au niveau des canaux, configurez le suivi pour mesurer les performances globales et comprendre le comportement des clients dans vos initiatives marketing.

* **Définir des mesures de succès personnalisées** - Configurez des KPI spécifiques alignés sur les objectifs de votre entreprise (achats, inscriptions, renouvellements, etc.) au-delà des mesures d’engagement standard. [En savoir plus](../building-journeys/success-metrics.md)

* **Activer les événements d’étape de parcours** - Activez le suivi détaillé de chaque action entreprise par les clients et clientes lorsqu’ils se déplacent dans les parcours. Vous obtiendrez ainsi une visibilité granulaire sur les points d’entrée/de sortie, la sélection des chemins et les lieux de dépôt. [En savoir plus](../reports/journey-step-events-overview.md)

* **Configurer la planification** - Configurez l’optimisation de l’heure d’envoi pour suivre les performances sur différentes stratégies de minutage et identifier les fenêtres d’envoi optimales. [En savoir plus](../building-journeys/send-time-optimization.md)

* **Configurer la surveillance des actions personnalisées** - Configurez le suivi des intégrations à des systèmes externes pour surveiller les appels API, les temps de réponse et les modèles d’erreur. [En savoir plus](../action/reporting.md)

* **Créer des rapports personnalisés et exporter des données** - Créez des rapports personnalisés et exportez les données de suivi vers des systèmes externes pour une analyse plus approfondie. [En savoir plus](../reports/sharing-overview.md)

* **Afficher des performances unifiées :** accédez à des rapports complets pour les campagnes et les parcours afin de comparer les performances sur les e-mails, les notifications push, les SMS et d’autres canaux, et de déterminer les combinaisons qui génèrent les meilleurs résultats. [&#x200B; Rapports de campagne &#x200B;](../reports/campaign-global-report-cja.md) | [Parcours de rapports](../reports/journey-global-report-cja.md)

## Suivi des performances d’optimisation et de prise de décision {#optimization-decisioning-tracking}

Journey Optimizer effectue automatiquement le suivi des expériences d’optimisation, des stratégies de ciblage et des performances de prise de décision. Configurez vos paramètres pour garantir une collecte de données appropriée.

### Configurer le suivi de l’optimisation {#optimization-tracking}

* **Optimisation de vos campagnes et parcours** :

   * Lors de la création d’expériences, définissez les mesures à suivre (conversions, clics, événements personnalisés). Journey Optimizer collecte automatiquement les données de performance pour chaque traitement. [En savoir plus](../campaigns/campaigns-message-optimization.md#experimentation)

   * Créez des règles de ciblage pour diffuser un contenu différent à différents segments d’audience. Journey Optimizer effectue automatiquement le suivi des mesures d’engagement pour chaque groupe ciblé, ce qui vous permet de comparer les performances entre les segments. [En savoir plus](../campaigns/campaigns-message-optimization.md#targeting)

* **Optimisation des chemins de Parcours** : ajoutez une activité **Optimiser** à votre parcours et configurez plusieurs chemins d’accès. Journey Optimizer suit automatiquement les chemins empruntés par les profils et mesure les performances. [En savoir plus](../building-journeys/optimize.md)

Pour analyser les résultats : affichez les taux de conversion, la signification statistique et l’effet élévateur entre les traitements dans les rapports d’expérience, ou comparez les mesures d’engagement sur les segments ciblés. [&#x200B; Rapport de campagne d’expérimentation &#x200B;](../reports/campaign-global-report-cja-experimentation.md) | [Rapport parcours d’expérimentation](../reports/journey-global-report-cja-experimentation.md) | [rapport de ciblage de Parcours &#x200B;](../reports/journey-global-report-cja.md#targeting)

### Suivi des performances de prise de décision {#decisioning-tracking}

Lorsque vous utilisez Decisioning pour personnaliser le contenu, Journey Optimizer effectue automatiquement le suivi des événements, des impressions et des clics de décision, sans configuration supplémentaire requise.

* **Capture automatique d’événement** - Journey Optimizer capture automatiquement les événements de décision chaque fois qu’un élément de décision est sélectionné pour un profil.
* **Tracking des impressions** - Pour les e-mails, les impressions sont suivies automatiquement. Pour les expériences basées sur du code, vous devez implémenter des événements d’affichage de proposition dans votre code. [En savoir plus](../code-based/code-based-implementation-samples.md#client-side-how)
* **Suivi des clics** - Les clics sur les éléments de décision sont automatiquement suivis dans les e-mails. Les expériences basées sur le code nécessitent l’implémentation d’événements de clic.

>[!NOTE]
>
>Pour suivre la prise de décision dans les **expériences basées sur du code**, assurez-vous que votre implémentation envoie des événements d’interaction de proposition (affichages et clics) à Adobe Experience Platform à l’aide de Web SDK ou de Mobile SDK. [En savoir plus](../experience-decisioning/data-collection/schema-requirement.md)

Pour surveiller les performances : affichez les KPI de prise de décision, comparez les éléments de décision, analysez les stratégies de sélection et surveillez les performances du modèle d’IA dans les rapports. [En savoir plus](../experience-decisioning/cja-reporting.md)

## Contrôle de l’utilisation des données de tracking {#data-governance}

Les politiques de gouvernance des données vous permettent de contrôler comment les données de suivi peuvent être utilisées dans l’ensemble de votre organisation :

* **Étiqueter les données de tracking sensibles** - Appliquez des étiquettes de gouvernance aux données comportementales suivies (par exemple, les clics sur le contenu relatif à l&#39;intégrité, les interactions avec les produits financiers) pour les marquer comme sensibles ou réglementées.

* **Limiter l’utilisation des données** - Créez des politiques qui empêchent les données de suivi libellées d’être utilisées dans certains canaux, exportées vers des systèmes tiers ou utilisées pour des scénarios de personnalisation spécifiques.

* **Application automatique** - Journey Optimizer vérifie automatiquement les politiques de gouvernance lorsque vous créez des parcours et des campagnes, bloquant la publication si les données suivies sont utilisées en violation des politiques définies.

La gouvernance des données garantit la conformité aux réglementations telles que le RGPD et le CCPA tout en vous permettant de suivre et d’analyser le comportement des clients dans les limites approuvées. [En savoir plus](../action/action-privacy.md)

## Surveillance de la délivrabilité et de l’intégrité du système {#monitoring-capabilities}

Au-delà du suivi de l’engagement, configurez la surveillance pour vous assurer que les boîtes de réception et les systèmes atteignent les messages de manière optimale.

La surveillance de la délivrabilité permet de s’assurer que vos messages atteignent les boîtes de réception des destinataires et préservent la bonne réputation de l’expéditeur en suivant les indicateurs clés :

* **Consultez régulièrement la liste de suppression** pour comprendre pourquoi les adresses sont bloquées et conservez l’hygiène de la liste. [En savoir plus](../reports/suppression-list.md)

* **Analyser les erreurs de diffusion** diagnostiquer les échecs et prendre des mesures correctives. [En savoir plus](../configuration/email-error-types.md)

* **Suivez les bonnes pratiques** pour DMARC, SPF et DKIM afin d’optimiser l’emplacement des boîtes de réception. [En savoir plus](../reports/deliverability.md)

Configurez une surveillance proactive afin de recevoir des notifications en temps réel sur les événements critiques et les problèmes système, ce qui vous permet de répondre rapidement avant qu’ils n’affectent vos expériences client :

* **Configurer des alertes** - Configurez des notifications en temps réel pour les erreurs de parcours, les échecs d’action personnalisée et les problèmes critiques afin de répondre rapidement aux problèmes. [En savoir plus](../reports/alerts.md)

* **Activer les journaux d’audit** - Activez la journalisation d’audit pour suivre toutes les actions sur les ressources à des fins de conformité et de dépannage. [En savoir plus](../privacy/audit-logs.md)

* **Surveiller les intégrations** - Suivez les performances des actions personnalisées et la connectivité du système externe pour identifier rapidement les problèmes d’intégration. [En savoir plus](../action/reporting.md)

