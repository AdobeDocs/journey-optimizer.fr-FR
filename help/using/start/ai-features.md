---
solution: Journey Optimizer
product: journey optimizer
title: Fonctionnalités intelligentes et IA
description: Découvrez en quoi l’IA et le machine learning améliorent les fonctionnalités d’Adobe Journey Optimizer.
feature: Overview
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
source-git-commit: 7ec41e5b1aa51991847ef8cf9dad428b06dfcaef
workflow-type: tm+mt
source-wordcount: '1676'
ht-degree: 87%

---

# Fonctionnalités intelligentes et IA {#ai-features}

Adobe Journey Optimizer exploite la puissance de l’intelligence artificielle et du machine learning pour transformer la manière dont vous créez, optimisez et diffusez des expériences clients exceptionnelles. Depuis la génération de contenu personnalisé jusqu’à la prévision d’heures d’envoi optimales, les fonctionnalités d’IA rationalisent votre workflow et maximisent l’impact. Les playbooks de cas d’utilisation fournissent des modèles préconfigurés pour rapidement mettre en œuvre des scénarios marketing courants.

## Assistant IA {#ai-assistant}

L’assistant IA est votre guide conversationnel pour Adobe Journey Optimizer. Utilisez-le pour obtenir des réponses instantanées sur les fonctionnalités des produits, des informations opérationnelles sur vos parcours et une aide à la navigation sur la plateforme.

### Accéder à l’assistant IA

Cliquez sur l’icône de l’assistant AI dans la barre supérieure pour ouvrir le panneau de l’assistant sur le côté droit de l’écran.

![](assets/do-not-localize/ai-assistant-open.png)

>[!IMPORTANT]
>
>Avant de pouvoir utiliser l’assistant IA, vous devez accepter les [directives d’utilisation de l’IA générative d’Adobe Experience Cloud](https://experienceleague.adobe.com/fr/docs/experience-platform/ai-assistant/home){target="_blank"}.

### Capacités de l’assistant IA

**Connaissance du produit** : posez des questions sur les fonctionnalités et les concepts d’Adobe Journey Optimizer :

* « Comment configurer une campagne dans Adobe Journey Optimizer ? »
* « Comment créer une action personnalisée qui puisse être utilisée dans des parcours ? »
* « Combien d’activités actives est-il possible d’avoir dans un seul sandbox ? »

**Informations opérationnelles (Beta)** : obtenez des informations en temps réel sur vos parcours :

* « Combien de parcours actifs ai-je ? » 
* « Écris-moi une liste de tous les parcours planifiés. »
* « Combien de parcours ont été créés au cours des 7 derniers jours ? »

>[!NOTE]
>
>Actuellement, les informations opérationnelles ne sont disponibles que pour les **parcours** et reflètent les données de votre sandbox actuel.

### Utilisation de l’assistant IA

1. Saisissez votre question dans le champ de texte en bas du panneau.
2. Appuyez sur Entrée pour envoyer votre requête.
3. Examinez la réponse générée par l’IA.
4. Cliquez sur **Afficher les sources** pour accéder à la documentation associée.
5. Utilisez les pouces vers le haut/bas pour évaluer la qualité de la réponse.

![](assets/do-not-localize/ai-assistant-answer.png){width="40%" align="left"}

[En savoir plus sur l’assistant IA d’Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/ai-assistant/home){target="_blank"}

## Agents IA avancés pour l’optimisation des parcours {#ai-agents}

En s’appuyant sur les capacités de conversation de l’assistant IA, Adobe Journey Optimizer propose des agents IA spécialisés qui fournissent une analyse approfondie et des recommandations exploitables pour l’optimisation et l’expérimentation des parcours.

### Journey Agent {#journey-agent}

Journey Agent comprend deux compétences dans l’assistant AI : Analyser et Créer. Utilisez-les pour optimiser les parcours existants ou en créer de nouveaux à partir d’invites en langage naturel.

+++**Autorisations requises**

* **Afficher les parcours** : affichez des informations sur les parcours directement dans l’assistant IA.
* **Gérer les parcours** : créez des parcours directement dans l’assistant IA.
* **Affichage des segments** - Obtenez des informations sur les audiences et recherchez des audiences existantes
* **Gérer les segments** : créez des audiences directement dans l’assistant IA.
* **Afficher les événements de Parcours, les sources de données et les actions** - Requis pour que la compétence Créer puisse rechercher des événements de parcours et des actions personnalisées

+++

#### Compétence en analyse de parcours {#journey-analyze-skill}

L’[agent d&#39;analyse de parcours](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide){target="_blank"} vous aide à optimiser les performances du parcours grâce à l’analyse du langage naturel :

+++**Fonctionnalités principales**

* **Analyse des abandons dans les parcours** : identifiez où et pourquoi la clientèle abandonne les parcours et détectez les schémas de désengagement.
* **Détection des chevauchements d’audiences** : analysez le chevauchement des audiences sur plusieurs parcours pour éviter la lassitude due à un ciblage excessif.
* **Identification des conflits de planification** : détectez les conflits de calendrier entre des parcours planifiés ciblant la même audience.
* **Informations opérationnelles** obtenez des informations basées sur des prompts tels que « affiche tous les parcours actifs » ou « quelles audiences sont utilisées dans plus de X parcours ».

+++

+++**Exemples de prompts**

* « Effectuer une analyse des abandons pour le parcours \[Journey Name\] »
* « Existe-t-il des conflits de plannings pour le parcours \[Journey Name\] ? »
* « Montre-moi les conflits de chevauchement d’audiences pour le parcours \[Journey Name\]. »
* « Quelles audiences sont utilisées dans plus de 5 parcours ? »

+++


#### Parcours Create Skill {#journey-create-skill}

L’agent de création de Parcours [&#128279;](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-analyze-agent-skill-overview-and-user-guide){target="_blank"} vous aide à créer des parcours à partir d’invites de langage naturel, en traduisant vos objectifs en configurations de parcours structurées :

+++**Fonctions principales**

* **Création d’un Parcours en langage naturel** - Décrivez le parcours souhaité et faites-le créer automatiquement
* **Démarrages basés sur un événement et une audience** - Créez des parcours de qualification d’audience, d’événement métier ou déclenchés par un événement
* **Logique conditionnelle** - Créez des chemins de division en fonction des attributs ou du comportement du client
* **Messagerie multicanal** - Ajoutez des actions e-mail, push et SMS.
* **Planification** - Configurez les dates et heures de début entre les étapes.

+++

+++**Exemples de prompts**

* « Créez un parcours qui démarre lorsqu’un client effectue un achat en ligne et envoie une notification push de remerciement. »
* « Créez un parcours ciblant mon audience de randonneurs d’une journée avec trois e-mails sur deux semaines, à partir du 20/12. »
* « Créez un parcours qui démarre lorsqu’un utilisateur ou une utilisatrice saisit l’emplacement de ma boutique et effectue un suivi selon qu’il ou elle dispose d’une adresse e-mail valide. »

+++

### Agent Experimentation {#experimentation-agent}

L’[agent Experimentation](https://experienceleague.adobe.com/fr/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment){target="_blank"} modernise la manière dont vous exécutez et gérez des expériences numériques sur des sites web, des e-mails, des messages push et des applications :

+++**Fonctions principales**

* **Analyse des performances** : vue claire de ce qui s’est passé dans les expériences
* **Génération d’informations** : explication des raisons des résultats
* **Découverte d’opportunités** : conseils sur les prochaines actions à entreprendre
* **Analyse de contenu** : examen des éléments de message pour comprendre pourquoi certains traitements ont mieux fonctionné que d’autres
* **Génération de recommandations** : suggestion de nouveaux traitements ou d’ajustements en fonction des informations

+++

+++**Exemples de prompt**

* « Quelles expériences sont en cours pour \[Campaign Name\] ? »
* « Pour \[Experiment Name\], quel traitement fonctionne le mieux ? »
* « Qu’avons-nous appris de \[Experiment Name\] ? »
* « Que me recommandes-tu de faire après cette expérience ? »
* « Quels schémas ressortent le plus des tests récents ? »

+++

+++**Autorisations requises**

* **Afficher les expériences** : affichez des informations sur les expériences dans l’assistant IA.
* **Gérer les métadonnées d’expérience** : créez des expériences dans l’assistant IA.

**Remarque :** disponible avec la licence Journey Optimizer Experimentation Accelerator.

+++

### Agents IA supplémentaires

**Agent Audience** : pour l’exploration et la gestion des audiences conversationnelles dans Adobe Experience Platform, y compris la détection des doublons et le suivi de la taille. [En savoir plus sur l’agent Audience](https://experienceleague.adobe.com/fr/docs/experience-cloud-ai/experience-cloud-ai/agents/audience){target="_blank"}

**Agent Orchestrator** : il coordonne plusieurs agents spécialisés afin de résoudre des défis marketing complexes en plusieurs étapes. L’orchestrateur détermine automatiquement quels agents impliquer et planifie leurs actions de manière optimale. [En savoir plus sur l’agent Orchestrator](https://experienceleague.adobe.com/fr/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator){target="_blank"}

## Génération de contenu optimisé par l’IA {#content-generation}

Utilisez l’IA générative pour créer et personnaliser du contenu sur plusieurs canaux, et ainsi accélérer votre processus de création de contenu tout en préservant la cohérence de la marque. L’assistant IA pour la génération de contenu est disponible pour les expériences [e-mail](../email/get-started-email.md), [notifications push](../push/get-started-push.md), [SMS](../sms/get-started-sms.md) et [web](../web/get-started-web.md). Il vous permet de générer des objets, le corps des messages, des images et des variantes complètes des messages.

### Fonctionnalités clés

* **Génération de texte** : créez des contenus attrayants en accord avec le ton et les objectifs de votre marque. [Génération de texte avec l’IA](../content-management/generative-text.md)
* **Génération d’images** : générez des images personnalisées à l’aide d’Adobe Firefly. [Génération d’images avec l’IA](../content-management/generative-image.md)
* **Variantes de contenu** : produisez plusieurs variantes pour les tests A/B. [Expérience de contenu avec l’IA](../content-management/generative-experimentation.md)
* **Alignement sur la marque** : assurez-vous que le contenu généré correspond aux consignes de votre marque. [Évaluation de l’alignement sur la marque](../content-management/brands-score.md)
* **Prise en charge des modèles** : utilisez vos modèles d’e-mail existants. [Utiliser des modèles de contenu](../content-management/content-templates.md)

### Bonnes pratiques

* **Faire preuve de précision** : rédigez des prompts clairs et détaillés pour de meilleurs résultats.
* **Charger des ressources de la marque** : utilisez des fichiers PDF, des images ou des fichiers ZIP (50 Mo max.) pour assurer la cohérence de la marque.
* **Utiliser des modèles personnalisés** : utilisez des modèles spécifiques à la marque contenant jusqu’à 8 à 10 images.
* **Fournir des commentaires** : évaluez les sorties pour améliorer les modèles d’IA.
* **Vérifier l’ensemble du contenu** : vérifiez toujours l’exactitude du contenu généré par l’IA avant de le publier.

[En savoir plus sur la génération de contenu par l’IA](../content-management/gs-generative.md)

## Optimisation de l’heure d’envoi {#send-time-optimization}

Utilisez l’IA pour prédire l’heure optimale d’envoi de chaque message en fonction des modèles de comportement individuels des clients et clientes, et ainsi optimiser l’engagement.

### Fonctionnement

L’optimisation de l’heure d’envoi analyse les données d’engagement historiques (ouvertures et clics) afin de prédire à quel moment chaque client ou cliente est le plus susceptible d’interagir avec vos messages. Le système planifie automatiquement la diffusion dans la fenêtre temporelle spécifiée.

### Meilleurs moments d’utilisation

| Idéal pour | Déconseillé pour |
|----------|---------------------|
| Campagnes marketing et newsletters | Messages opérationnels urgents (confirmations de commande, réinitialisations de mot de passe) |
| Messages promotionnels | Notifications urgentes (retards de vol, alertes d&#39;urgence) |
| Contenu éducatif | Messages basés sur un événement aux exigences temporelles spécifiques |
| Campagnes d’engagement | |

[En savoir plus sur l’optimisation de l’heure d’envoi](../building-journeys/send-time-optimization.md)

## Modèles d’IA pour la prise de décision {#ai-decisioning}

Créez des modèles de classement intelligents qui optimisent automatiquement les offres à présenter à chaque client et cliente, maximisant ainsi les objectifs commerciaux.

### Types de modèles

**Optimisation automatique** : tirez les leçons des interactions client pour améliorer automatiquement les performances des offres au fil du temps.

**Optimisation personnalisée** : utilisez les attributs de profil client et le comportement pour prédire la meilleure offre pour chaque individu.

### Conditions requises

* Au moins 2 offres avec des données d’interaction suffisantes :
   * Plus de 100 événements d’affichage
   * Plus de 5 clics sur les événements
   * Au cours des 14 derniers jours
* Maximum de 5 modèles de classement IA par organisation

[En savoir plus sur les modèles d’IA pour la prise de décision](../experience-decisioning/ranking/ai-models.md) | [Créer des modèles de classement IA](../experience-decisioning/ranking/create-ai-models.md)

## Contenu : expérimentation avec l’IA {#experimentation}

L’**accélérateur d’expériences** vous permet d’exécuter des expériences plus rapidement avec des informations et des recommandations pilotées par l’IA, en identifiant plus rapidement les variations de contenu gagnantes.

Fonctionnalités principales :

* Génération automatique de plusieurs variations de contenu
* Réception des recommandations de l’IA pour la conception d’expériences
* Obtention des premiers indicateurs des tendances de performances
* Accélération du délai d’obtention de la signification statistique

[En savoir plus sur l’accélérateur d’expériences](../content-management/experiment-accelerator-gs.md)

## Playbooks de cas d’utilisation {#playbooks}

Les playbooks de cas d’utilisation sont des workflows préconfigurés qui vous permettent d’implémenter rapidement des scénarios marketing courants. Chaque playbook comprend des parcours, des messages, des schémas et des segments prêts à l’emploi.

![Interface des playbooks de cas d’utilisation](assets/playbooks-filter.png)

### Fonctionnement des playbooks

1. **Parcourir** la bibliothèque de playbooks pour trouver des cas d’utilisation correspondant à vos objectifs
2. **Activer** un playbook pour générer automatiquement toutes les ressources requises
3. **Personnaliser** les ressources générées pour répondre à votre marque et à vos besoins
4. **Déployer** en production ou tester dans un sandbox de développement

### Playbooks disponibles

Parcourez les playbooks Journey Optimizer pour obtenir des scénarios courants tels que :

* Récupération de panier abandonné
* Série de bienvenue pour les nouveaux clients et nouvelles clientes
* Engagement après achat
* Messages d’anniversaire
* Campagnes de réengagement

+++**Conditions préalables**

* Sandbox avec les autorisations appropriées
* Configurations de canal pour les e-mails, les notifications push et/ou les SMS
* Autorisations utilisateur pour la création de parcours et de messages

+++

[Afficher tous les playbooks disponibles](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/playbooks-list.html?lang=fr){target="_blank"} | [En savoir plus dans la documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/use-case-playbooks/playbooks/overview.html){target="_blank"}

## Fonctionnalités d’IA supplémentaires {#additional-capabilities}

### Convertisseur d’images en HTML

Transformez des images statiques (JPEG, PNG) en modèles d’e-mail HTML modifiables à l’aide de la technologie de conversion optimisée par l’IA.

[En savoir plus sur la conversion d’images en HTML](../email/image-to-html.md)

### Marque : évaluation de l’alignement

Évaluez l’alignement de votre contenu sur les consignes de votre marque à l’aide d’un système de notation optimisé par l’IA qui mesure la cohérence du ton, du style et des messages.

[En savoir plus sur l’alignement sur la marque](../content-management/brands-score.md)

## Questions fréquentes {#faq}

+++**De quelles autorisations ai-je besoin pour utiliser les fonctionnalités d’IA ?**

* **[Assistant IA pour la génération de contenu](#content-generation)** : nécessite l’autorisation Générer du contenu.
* **[Assistant IA](#ai-assistant)** pour la connaissance du produit : nécessite l’acceptation des règles d’utilisation de l’IA générative Adobe.
* **[Agent d’analyse des parcours](#journey-agent)** : nécessite les autorisations Afficher/Gérer les parcours et Afficher/Gérer des segments.
* **[Agent de création de Parcours](#journey-create-agent)** - Nécessite des autorisations de niveau Gérer les Parcours, Afficher les événements de Parcours/les sources de données/les actions, Afficher les segments et Gérer les segments
* **[Agent Experimentation](#experimentation-agent)** : nécessite les autorisations Afficher les expériences et Gérer les métadonnées d’expérience.

Tous les agents IA doivent avoir accès à l’assistant IA et accepter les règles d’utilisation de l’IA générative d’Adobe Experience Cloud.

[En savoir plus sur les autorisations](../administration/ootb-permissions.md)

+++

+++**Le contenu généré par l’IA est-il toujours exact ?**

Non. Passez toujours en revue le [contenu généré par l’IA](#content-generation) pour en vérifier l’exactitude et l’alignement sur la marque. Utilisez les outils de commentaires (pouces vers le haut/vers le bas) pour améliorer les modèles.

+++

+++**Quelles sont les principales limites ?**

* **[Optimisation de l’heure d’envoi](#send-time-optimization)** : disponible uniquement pour les e-mails et les notifications push dans les parcours ; nécessite une période d’entraînement de 30 jours
* **[Génération de contenu avec l’IA](#content-generation)** : non disponible pour le courrier, les cartes de contenu, LINE ni WhatsApp
* **[Modèles de classement IA](#ai-decisioning)** : maximum 5 modèles par organisation ; nécessite un minimum de données d’interaction

+++

+++**Comment puis-je accéder à ces fonctionnalités ?**

La plupart des fonctionnalités d’IA sont incluses dans Adobe Journey Optimizer. Certaines fonctionnalités telles que l’[optimisation de l’heure d’envoi](#send-time-optimization) et les [agents d’IA](#ai-agents) doivent être activées par Adobe. Contactez votre représentant ou représentante Adobe pour plus d’informations sur les fonctionnalités disponibles avec votre licence.

+++
