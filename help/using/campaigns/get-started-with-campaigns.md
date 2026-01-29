---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les campagnes
description: Apprenez en plus sur les campagnes dans Journey Optimizer.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: campagne, guide, commencer, optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: a7d2557790054e7c6e28ca3ffa937f454c4b004c
workflow-type: tm+mt
source-wordcount: '1510'
ht-degree: 97%

---

# Commencer avec les campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Planning de la campagne"
>abstract="Par défaut, les campagnes démarrent via une activation manuelle et se terminent immédiatement après un seul envoi du message. Vous avez la possibilité de définir une date et une heure spécifiques pour l’envoi du message. De plus, vous pouvez spécifier une date de fin pour les campagnes d’action récurrentes. Dans les déclencheurs d’action, vous pouvez également configurer la fréquence d’envoi des messages en fonction de vos préférences."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Début de campagne"
>abstract="Indiquez la date et l’heure auxquelles le message doit être envoyé."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fin de campagne"
>abstract="Indiquez à quel moment une campagne récurrente doit cesser d’être exécutée."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Déclencheurs d’action de campagne"
>abstract="Vous pouvez définir la fréquence d’envoi du message de la campagne."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="Contrôle des taux"
>abstract="Définissez le contrôle des taux pour votre campagne en spécifiant les limites de taux souhaitées. Cette fonctionnalité est particulièrement utile pour éviter la surcharge sur les systèmes en aval, tels que les pages de destination ou les plateformes d’assistance clientèle."

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="Créer des campagnes"
>abstract="Utilisez **Adobe Journey Optimizer** pour diffuser du contenu ponctuel sur une audience spécifique à l’aide de divers canaux. Lors de l’utilisation de parcours, les actions sont exécutées à la suite. Avec les campagnes, les actions sont exécutées simultanément, immédiatement ou selon un planning spécifié."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Créez des campagnes pour diffuser du contenu ponctuel à une audience spécifique sur différents canaux. Avant de créer votre campagne, assurez-vous de disposer d’une configuration de canal et d’une audience Adobe Experience Platform prête à l’emploi."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Type de campagne"
>abstract="Sélectionnez le type de la campagne. Les canaux disponibles varient en fonction du type sélectionné. <br>**Campagnes planifiées** (campagnes d’action) : idéales pour les communications par lots, simples et ponctuelles, que vous pouvez planifier pour qu’elles s’exécutent à une heure spécifique.<br>**Campagnes déclenchées par API** : activées par le biais d’un appel API, elles permettent d’envoyer des messages automatisés et basés sur un événement, directement depuis des systèmes externes.<br>**Campagnes orchestrées** : fournissent une zone de travail visuelle par glisser-déposer pour concevoir et automatiser des workflows marketing complexes et à plusieurs étapes, depuis la segmentation d’audience jusqu’à la diffusion de messages personnalisés sur plusieurs canaux."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="Campagnes"
>abstract="Créez votre flux de segmentation, concevez vos messages cross-canal et planifiez vos campagnes. Canaux pris en charge : e-mail, SMS, notification push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="Campagnes"
>abstract="Effectuez des diffusions sortantes uniques ou récurrentes ou des actions entrantes continues."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="Campagnes"
>abstract="Envoyez des actions transactionnelles sortantes uniques ou récurrentes."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="Campagnes"
>abstract="Diffusez des communications marketing personnalisées aux audiences ciblées. Canaux pris en charge : e-mail, SMS, notifications push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="Campagnes"
>abstract="Diffusez des communications transactionnelles à des profils individuels ou à des ensembles de profils. Canaux pris en charge : e-mail, SMS, notifications push."

Adobe Journey Optimizer vous permet de diffuser du contenu ciblé et unique à des audiences spécifiques sur plusieurs canaux. Grâce aux campagnes, vous pouvez exécuter simultanément des actions marketing coordonnées afin d’atteindre votre audience avec le bon message au bon moment.

Ce guide fournit une feuille de route claire pour vous permettre de comprendre les principes de base des campagnes, de choisir le type de campagne approprié à votre cas d’utilisation et de concevoir en toute confiance des campagnes qui offrent des expériences clients percutantes.

## Que sont les campagnes ?

Les **campagnes** sont des actions marketing coordonnées qui diffusent du contenu à une audience spécifique sur un ou plusieurs canaux. Contrairement aux parcours où les actions s’exécutent de manière séquentielle, les campagnes exécutent des actions simultanément, immédiatement ou selon un planning défini.

Utilisez les campagnes [!DNL Journey Optimizer] pour :

* diffuser du **contenu unique ou récurrent** aux segments d’audience ciblés ;
* exécuter des **communications multicanaux coordonnées** par e-mail, notification push, SMS, in-app, web, etc. ;
* déclencher des **réponses automatisées** via des appels API pour des messages en temps réel pilotés par les événements ;
* concevoir des **workflows marketing complexes** avec des outils d’orchestration visuels.

![](assets/gs-campaigns.png)

➡️ **Vous souhaitez commencer à créer ?** [Créez votre première campagne](create-campaign.md) en quelques minutes.

## Choisir votre type de campagne {#campaign-types}

**Avant de commencer la création**, il est important de comprendre quel type de campagne correspond à votre cas d’utilisation. Adobe Journey Optimizer prend en charge trois types de campagnes, chacun conçu pour différents scénarios et mécanismes d’activation :

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB Campagnes orchestrées]

**Utilisation :** workflows marketing complexes et à plusieurs étapes

Les **campagnes orchestrées** fournissent une zone de travail visuelle par glisser-déposer pour concevoir et automatiser des workflows marketing sophistiqués. Depuis la segmentation d’audience jusqu’à la diffusion personnalisée des messages sur plusieurs canaux, tout se passe dans un environnement intuitif conçu pour la vitesse et le contrôle.

**Idéales pour :** des programmes d’engagement client à plusieurs étapes, des stratégies de ciblage et de segmentation complexes, l’orchestration de campagnes cross-canal, le marketing à grande échelle initié par la marque et l’automatisation avancée des workflows avec plusieurs points de décision

➡️ [Découvrir les campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md)

>[!TAB Campagnes d’action (planifiées)]

**Utilisation :** communications par lots simples et planifiées

Les **campagnes d’action** (également appelées campagnes planifiées) sont idéales pour les communications par lots simples, ponctuelles ou récurrentes qui s’exécutent à un moment spécifique.

**Deux catégories :**

* **Marketing** : offres promotionnelles, campagnes d’engagement, annonces, informations juridiques ou mises à jour de politiques. Les destinataires doivent être inscrits.
* **Transactionnelle** : perturbations, urgences, annulations. Ne nécessite pas d’opt-in.

**Idéales pour :** des newsletters mensuelles destinées aux segments client, des annonces promotionnelles à durée limitée, des campagnes marketing saisonnières, des communications de lancement de produit et des notifications d’interruption de service.

➡️ [Découvrir les campagnes d’action](create-campaign.md)

>[!TAB Campagnes déclenchées par API]

**Utilisation :** messages en temps réel pilotés par les événements avec les systèmes externes

**Campagnes déclenchées par API** : activez-les par le biais d’un appel API, ce qui permet d’envoyer des messages automatisés directement depuis des systèmes externes. Ces campagnes prennent en charge la personnalisation à l’aide des attributs de profil et des données contextuelles en temps réel de la payload de l’API.

**Deux catégories :**

* **Marketing** : communications marketing personnalisées aux audiences ciblées
* **Transactionnelle** : messages suivant des actions individuelles (réinitialisations de mot de passe, achats de panier, etc.)

**Idéales pour :** des confirmations de réinitialisation de mot de passe, une récupération d’abandon de panier, des confirmations de commande et mises à jour d’expédition, des notifications d’activité de compte et des recommandations personnalisées en temps réel

➡️ [Découvrir les campagnes déclenchées par API](api-triggered-campaigns.md)

>[!ENDTABS]

>[!NOTE]
>
>Vous ne savez pas quel type choisir ? Commencez par les **campagnes d’action** pour les communications par lots planifiées ou par les **campagnes déclenchées par API** pour des messages en temps réel : celles-ci couvrent la plupart des cas d’utilisation courants.

## Conditions préalables {#prerequisites}

Avant d’utiliser des campagnes, vérifiez que vous disposez des éléments suivants :

* **Audiences** : des audiences doivent être disponibles dans Adobe Experience Platform avant de créer des campagnes. [Commencer à utiliser des audiences →](../audience/about-audiences.md)

* **Configurations de canal** : les configurations de canal (paramètres prédéfinis) doivent être créées et disponibles pour les canaux que vous souhaitez utiliser. [Paramétrer des configurations de canal →](../configuration/channel-surfaces.md)

* **Autorisations** : vous avez besoin d’autorisations appropriées en fonction du type de campagne. Contactez votre administrateur ou votre administratrice si vous ne pouvez pas accéder aux fonctionnalités de campagne. [En savoir plus sur les rôles intégrés →](../administration/ootb-product-profiles.md)

  +++Liste des autorisations relatives aux campagnes

  | Type de campagne | Autorisations |
  |-------------|---------------|
  | **Campagnes d’action** et **campagnes déclenchées par l’API** | Administrateur ou administratrice de campagne<br>Approbateur ou approbatrice de campagne<br>Responsable de campagne<br>Observateur ou observatrice de campagne |
  | **Campagnes orchestrées** | Administrateur ou administratrice de campagne orchestrée<br>Approbateur ou approbatrice de campagne orchestrée<br>Responsable de campagne orchestrée<br>Observateur ou observatrice de campagne orchestrée |

  +++

  +++Attribution des autorisations de campagne

   1. Accédez à l’onglet **[!UICONTROL Rôles]** dans le produit [!DNL Permissions] et sélectionnez l’un des **[!UICONTROL Rôles]** intégrés relatifs à la campagne.

   1. Dans l’onglet **[!UICONTROL Utilisateurs et utilisatrices]**, cliquez sur **[!UICONTROL Ajouter un utilisateur ou une utilisatrice]**.

   1. Saisissez le nom ou l’adresse e-mail de votre utilisateur ou utilisatrice, ou sélectionnez cette personne dans la liste, puis cliquez sur **[!UICONTROL Enregistrer]**.

  Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez la [documentation relative à l’ajout d’utilisateurs et d’utilisatrices](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/ui/users){target="_blank"}.

  La personne doit alors recevoir un e-mail la redirigeant vers votre instance.

  +++

## Workflow de création de votre campagne {#workflow}

La création de campagnes réussies suit un processus clair et reproductible. Voici votre workflow détaillé :

+++&#x200B;1. Planifier votre campagne

Avant de commencer, clarifiez vos objectifs :

* **Quel est l’objectif ?** (par exemple, stimuler les conversions, augmenter l’engagement, avertir les clientes et clients)
* **Qui est l’audience ?** (par exemple, créée ou sélectionnée à partir d’Adobe Experience Platform)
* **Quel type de campagne est approprié ?** (voir les [types de campagne](#campaign-types) ci-dessus)
* **Quels canaux allez-vous utiliser ?** (e-mail, notification push, SMS, in-app, web, etc.) → [Voir les canaux pris en charge par type de campagne](../channels/gs-channels.md#channels)
* **Quand doit-elle s’exécuter ?** (immédiate, planifiée ou déclenchée par API)

+++

+++&#x200B;2. Configurer les propriétés de la campagne

Configurez les bases de votre campagne :

1. **Nommez et décrivez** votre campagne pour une identification facile.
2. **Sélectionnez le type de campagne** (action, déclenchée par API ou orchestrée).
3. **Choisissez votre audience.**
4. **Définissez sa priorité** si vous utilisez la gestion des conflits.
5. **Configurez le planning** (pour les campagnes d’action) ou les détails de l’API (pour les campagnes déclenchées par API).

**Guides spécifiques aux types :** [Propriétés des campagnes d’action](campaign-properties.md) | [Propriétés des campagnes déclenchées par API](api-triggered-campaign-properties.md) | [Configurer une campagne orchestrée](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;3. Concevoir votre contenu

Créez des messages attrayants pour votre audience :

* Utilisez le **Concepteur d’e-mail** pour des expériences d’e-mail riches.
* Configurez des **notifications push** avec des images et des liens profonds.
* Concevez des **SMS/MMS** avec de la personnalisation.
* Créez des expériences **in-app** et **web**.
* Ajoutez de la **personnalisation** à l’aide des attributs de profil et des données contextuelles.

**Guides spécifiques aux types :** [Contenu de campagne d’action](campaign-content.md) | [Contenu de campagne déclenchée par API](api-triggered-campaign-content.md) | [Contenu de campagne orchestrée](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;4. Vérification et test

Vérifiez toujours votre campagne avant son activation :

* **Prévisualisez le contenu** avec des profils de test.
* **Vérifiez le ciblage** pour vous assurer qu’il s’agit de la bonne audience.
* **Vérifiez le planning** et les paramètres d’activation.
* **Demandez une approbation** si vous utilisez le workflow d’approbation.
* **Testez la délivrabilité** avec des listes de contrôle.

**Guides spécifiques aux types :** [Vérifier les campagnes d’action](review-activate-campaign.md) | [Vérifier les campagnes déclenchées par API](review-activate-api-triggered-campaign.md) | [Vérifier les campagnes orchestrées](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;5. Activer votre campagne

Une fois la vérification terminée, activez votre campagne :

* **Activation manuelle** : activez-la immédiatement ou à un horaire défini.
* **Activation par API** : pour les campagnes déclenchées par API, utilisez le point d’entrée d’activation.
* **Processus d’approbation** : si nécessaire, attendez l’approbation des parties prenantes.

Remarque : les campagnes actives ne peuvent pas être modifiées (vous devez les dupliquer pour apporter des modifications).

**Guides spécifiques aux types :** [Activer des campagnes d’action](review-activate-campaign.md) | [Activer des campagnes déclenchées par API](review-activate-api-triggered-campaign.md) | [Activer des campagnes orchestrées](../orchestrated/create-orchestrated-campaign.md)

+++

+++&#x200B;6. Surveiller et analyser

Suivez les performances de votre campagne :

* Consultez les rapports et les analyses de campagne.
* Surveillez les taux de diffusion des messages et les mesures d’engagement.
* Effectuez un suivi des erreurs et des rebonds.
* Analysez la conversion et le retour sur investissement.
* Utilisez des informations pour l’optimisation.

**Guides spécifiques aux types :** [Rapports de campagnes d’action](../reports/campaign-global-report-cja.md) | [Surveillance des campagnes déclenchées par API](api-triggered-campaigns.md#monitor) | [Analyses de campagnes orchestrées](../orchestrated/create-orchestrated-campaign.md)

+++

## Explorons plus en détail. {#get-started-types}

Maintenant que vous comprenez comment fonctionnent les campagnes dans [!DNL Journey Optimizer], choisissez votre type de campagne pour commencer :

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campagnes d’action" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campagnes d’action</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campagnes déclenchées par API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="notification push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campagnes orchestrées</a></td>
</tr></table>

À mesure que vous vous familiarisez avec les campagnes, explorez ces puissantes fonctionnalités :

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**Planification et timing**

Planifiez des campagnes à des dates/heures spécifiques, paramétrez des diffusions récurrentes et optimisez les heures d’envoi pour obtenir un impact maximal. (Campagnes d’action et déclenchées par API)

[En savoir plus sur la planification](campaign-schedule.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**Contrôle du débit**

Limitez le débit des messages pour éviter la surcharge sur les systèmes en aval tels que les pages de destination ou les plateformes d’assistance clientèle.

[Contrôler les limites de débit](create-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**Ciblage des audiences**

Ciblez des audiences Adobe Experience Platform spécifiques avec précision et gérez les qualifications d’audience de manière dynamique.

[Sélectionner l’audience de la campagne](campaign-audience.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**Workflows d’approbation**

Mettez en œuvre des processus de vérification et d’approbation avant la mise en ligne des campagnes afin de garantir la qualité et la conformité. (Campagnes d’action et déclenchées par API)

[Vérifier et activer](review-activate-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=fr)

**Heures creuses**

Respectez les préférences des clientes et des clients en évitant de diffuser des messages durant les fenêtres temporelles spécifiées. (Campagnes d’action et déclenchées par API)

[Configurer les heures creuses](../conflict-prioritization/quiet-hours.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**Optimisation** :

Utilisez les règles de ciblage et les expériences de contenu pour diffuser du contenu personnalisé et maximiser l’engagement.

[Optimiser les campagnes](../content-management/gs-message-optimization.md)
:::

::::
