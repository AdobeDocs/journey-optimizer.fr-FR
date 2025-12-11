---
solution: Journey Optimizer
product: journey optimizer
title: Critères d’entrée et de sortie de parcours
description: Découvrez comment gérer efficacement le moment où les profils entrent sur les parcours et en sortent à l’aide d’exemples réels et de bonnes pratiques
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: entrée, sortie, critères, parcours, profil, reprise, bonnes pratiques
version: Journey Orchestration
source-git-commit: a60ea57ffed3fa9e11dc202f26889d05862604d9
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 0%

---


# Utiliser les critères d’entrée et de sortie de parcours {#entry-exit-criteria-guide}

Dans l’orchestration de l’expérience client, diffuser le bon message au bon moment nécessite un contrôle précis des moments où les clients entrent et sortent de vos parcours. Comprendre et configurer correctement les critères d’entrée et de sortie peut faire la différence entre une campagne réussie et attrayante et les opportunités manquées ou la fatigue des messages.

Ce guide fournit des conseils pratiques, des exemples réels et des bonnes pratiques pour gérer les critères d’entrée et de sortie de parcours dans Adobe Journey Optimizer.

## Quels sont les critères d’entrée et de sortie ? {#what-are-criteria}

**Critères d’entrée** déterminent les conditions dans lesquelles un [profil client](../audience/get-started-profiles.md) peut rejoindre un parcours spécifique. Les profils peuvent entrer en fonction des éléments suivants :

* **[Comportement du client](../event/about-events.md)** - Les actions entreprises par les clients déclenchent une entrée de parcours en temps réel, comme effectuer un achat, abandonner un panier ou ouvrir votre application mobile.

* **[Attributs de profil](../audience/get-started-profiles.md)** - Les caractéristiques du client déterminent l’éligibilité en fonction des données stockées dans leur profil, telles que le niveau de fidélité, l’emplacement, l’âge ou les préférences de communication.

* **[Événements externes](../event/about-creating-business.md)** - Déclencheurs commerciaux ou environnementaux qui affectent plusieurs clients simultanément, tels que des alertes de faible niveau d’inventaire, des conditions météorologiques ou des changements de prix.

* **[Appartenance à une audience](../audience/about-audiences.md)** - L’appartenance à un segment d’audience spécifique active des parcours ciblés pour des groupes tels que les clients à forte valeur ajoutée, les utilisateurs inactifs ou les nouveaux abonnés.

**Critères de sortie** définissez quand et comment un profil quitte ou est supprimé d’un parcours :

* **Achèvement du Parcours** - Les profils se ferment automatiquement lorsqu’ils atteignent la [fin de tous les chemins de parcours &#x200B;](end-journey.md), achevant ainsi l’expérience conçue.

* **Réalisation des mesures de succès** - Les profils se ferment lorsqu’ils atteignent l’objectif du parcours [&#128279;](success-metrics.md), par exemple lors d’un achat ou du téléchargement d’une application, ce qui élimine les communications de suivi inutiles.

* **Basé sur des conditions** - Les profils se ferment lorsque des [conditions spécifiques](condition-activity.md) sont remplies, comme l’inactivité sur une période définie ou des modifications dans les attributs de profil.

* **Basé sur un événement** - Les profils se ferment lorsque des événements [&#x200B; spécifiques se produisent](../event/about-events.md) tels que l’annulation d’un abonnement ou le retour d’un produit.

* **Disqualification de l’audience** - Les profils disparaissent lorsqu’ils ne répondent plus aux [critères de l’audience cible](../audience/about-audiences.md), en s’assurant que les messages restent pertinents.

## Importance des critères d’entrée et de sortie {#why-they-matter}

Bien définir les critères d’entrée et de sortie offre une valeur commerciale significative :

* **Pertinence** : seuls les bons clients entrent sur le parcours, ce qui augmente les taux d’engagement et de conversion en ciblant l’audience la plus appropriée au moment optimal.

* **Efficacité** : empêche les clients de rester sur des parcours non pertinents, ce qui réduit les communications inutiles, les coûts d’exploitation et la gêne des clients.

* **Personalization** : permet la personnalisation dynamique des expériences en fonction des données et du comportement en temps réel, créant ainsi des interactions client plus significatives.

* **Conformité** : permet de gérer le capping de la fréquence et d’éviter la surcommunication, en respectant les préférences des clients et les exigences réglementaires tout en préservant la réputation de la marque.

## Exemples concrets d’entrées et de sorties de parcours {#real-world-examples}

Voici des scénarios courants qui montrent comment fonctionnent en pratique les critères d’entrée et de sortie :

**Campagne de bienvenue pour les nouveaux abonnés**

Créez une première impression personnalisée en guidant automatiquement les nouveaux abonnés à travers une introduction à votre marque, vos produits et vos services.

* **Entrée** : les profils rejoignent le parcours lorsqu&#39;ils s&#39;abonnent à une newsletter
* **Quitter** : les profils se ferment une fois qu’ils ont terminé une série d’e-mails de bienvenue ou après une période définie s’ils n’interagissent pas
* **Avantage** : garantit que les nouveaux abonnés reçoivent une intégration en temps opportun tout en évitant les messages répétitifs

**Récupération de panier abandonné**

Récupérez les revenus perdus en rappelant aux clients les articles qu&#39;ils ont laissés et en les incitant à terminer leur achat.

* **Entrée** : les clients rejoignent le parcours s’ils ajoutent des articles à un panier mais ne terminent pas le passage en caisse dans les 24 heures
* **Quitter** : les profils se ferment lorsqu’ils effectuent l’achat ou après 7 jours si aucun achat n’est effectué
* **Avantage** : génère des conversions par des rappels opportuns sans spammer les clients qui ne sont pas intéressés

**Engagement du programme de fidélité**

Récompensez vos clients les plus précieux avec des avantages exclusifs et des communications personnalisées qui renforcent la fidélité à la marque et augmentent la valeur de toute une vie.

* **Entrée** : les clients rejoignent le parcours après avoir atteint un certain seuil de points de fidélité
* **Quitter** : les profils se ferment après l’échange de récompenses ou s’ils sont inactifs pendant 60 jours
* **Avantage** : fidélise les clients à forte valeur ajoutée grâce à des offres personnalisées et évite la fatigue de la communication

**Collecte de commentaires sur les produits**

Collectez des informations sur la satisfaction client et les performances des produits en demandant des commentaires au moment optimal après la diffusion.

* **Entrée** : les clients rejoignent le parcours après réception d’un événement de confirmation de diffusion du produit
* **Quitter** : les profils se ferment une fois les commentaires envoyés ou après 10 jours en l’absence de réponse
* **Avantage** : capture rapidement des commentaires utiles sans ennuyer les clients avec des demandes persistantes

## Configuration des critères d’entrée de parcours {#configure-entry}

>[!BEGINSHADEBOX]

**Découvrez tout ce que vous devez savoir sur les critères d’entrée ici :**

* **[Déclencheurs basés sur un événement](../event/about-events.md)** : utilisez des événements tels que « création de profil », « transaction terminée » ou des événements personnalisés pour lancer un parcours. [Configurer les événements](../event/about-creating.md) dans **[!UICONTROL Administration]** > **[!UICONTROL Événements]**, définissez [le schéma et les champs d’événement](../event/experience-event-schema.md), puis ajoutez l’événement à partir de la palette **[!UICONTROL Événements]** dans le [Concepteur de parcours &#x200B;](using-the-journey-designer.md).

* **[Entrée basée sur l’audience](read-audience.md)** : les parcours cibles sont destinés aux profils qui appartiennent à des audiences spécifiques, sous la forme d’un lot unique ou selon un planning récurrent. [Créez des audiences](../audience/creating-a-segment-definition.md) dans le menu **[!UICONTROL Audiences]**, puis ajoutez une activité **[!UICONTROL Lecture d’audience]** et [configurez le planning](journey-properties.md#schedule).

* **[Entrée de la qualification de l’audience](audience-qualification-events.md)** : déclenche des parcours lorsque les profils répondent aux critères d’audiences spécifiques ou en sortent en temps réel. Définissez [audiences en flux continu](../audience/about-audiences.md), ajoutez un événement **[!UICONTROL Qualification d’audience]** à partir de la palette **[!UICONTROL Événements]** et choisissez le type de déclencheur.

* **[Filtres d’attributs](condition-activity.md)** : affinez les critères d’entrée en combinant des événements ou des audiences avec des attributs de profil et du contexte à l’aide de la logique AND/OR. Utilisez [conditions](conditions.md) pour référencer [attributs de profil](../audience/get-started-profiles.md), événements ou [données externes](../datasource/about-data-sources.md).

* **[Fenêtres de temps et planification](journey-properties.md#schedule)** : définissez des contraintes temporelles pour que les parcours restent opportuns et pertinents. Configurez des [plannings sur les activités Lecture d’audience](read-audience.md), utilisez des [activités Attente](wait-activity.md) et ajoutez des [conditions basées sur le temps](conditions.md) pour contrôler la durée.

>[!ENDSHADEBOX]

## Configuration des critères de sortie de parcours {#configure-exit}

>[!BEGINSHADEBOX]

**Découvrez tout ce que vous devez savoir sur les critères de sortie ici :**

* **[Achèvement de Parcours](end-journey.md)** : les profils se ferment automatiquement lorsqu’ils atteignent l’étape de parcours finale. Concevez des chemins de parcours pour terminer les activités **[!UICONTROL de fin]**.

* **[Réalisation de la mesure de succès](journey-properties.md#exit-criteria)** : définissez des mesures de succès (comme les achats ou les abonnements) et quittez les profils à la fin de l’opération. Cliquez sur l’icône **[!UICONTROL Afficher les critères de sortie]**, sélectionnez **[!UICONTROL Ajouter des critères de sortie]**, puis choisissez un [Événement](../event/about-events.md) ou [Audience](../audience/about-audiences.md) comme déclencheur de sortie.

* **[Délais d’inactivité](wait-activity.md)** : quittez les profils si aucun engagement ne se produit au cours d’une période définie. Utilisez les [Critères de sortie](journey-properties.md#exit-criteria) avec les audiences qui vérifient la date du dernier engagement, définissent les [activités d’attente](wait-activity.md) avec des durées définies et utilisent les [conditions](condition-activity.md) pour vérifier l’activité.

* **[Règles de rentrée](entry-management.md)** : déterminez si les profils peuvent entrer à nouveau dans le parcours plusieurs fois ou une seule fois, selon votre stratégie de campagne. Configurez les paramètres **[!UICONTROL Rentrée]** dans le parcours **[!UICONTROL Propriétés]** pour définir des périodes d’attente, activer une reprise forcée ou utiliser [des identifiants supplémentaires](supplemental-identifier.md) pour une reprise spécifique au contexte.

>[!ENDSHADEBOX]

## Exemples de parcours détaillés {#journey-examples}

Pour obtenir des conseils de mise en œuvre détaillés avec des détails techniques complets, explorez ces cas d’utilisation documentés :

* **[parcours d’intégration des clients](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)** - Créez des expériences de bienvenue personnalisées avec qualification d’audience, temporisation de l’événement et sorties basées sur des objectifs

* **[Récupération du panier abandonné](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)** - Récupérez les ventes perdues avec des parcours, des playbooks et un routage de canal déclenchés par un événement

* **[Campagnes de réengagement](https://experienceleague.adobe.com/fr/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)** - Récupérez les clients inactifs à l’aide du ciblage comportemental et de l’activation de médias achetés

* **[Envoyer des messages aux abonnés](message-to-subscribers-uc.md)** - Ciblez les listes d’abonnements avec lecture d’audience et contenu personnalisé

* **[Envoi de messages multicanaux](journeys-uc.md)** - Combinez l’e-mail et la notification push avec des événements de réaction et une logique à chemins multiples

* **[Envoyer des e-mails uniquement les jours de la semaine](weekday-email-uc.md)** - Planifier des communications à l’aide de conditions temporelles et de formules d’attente

>[!TIP]
>
>Parcourez tous les cas d’utilisation disponibles dans la bibliothèque de cas d’utilisation de Parcours [&#128279;](jo-use-cases.md) pour découvrir d’autres modèles et implémentations, notamment [augmenter les diffusions](ramp-up-deliveries-uc.md), [modèles d’événement d’expérience](exp-event-lookup.md) et [supprimer des profils des parcours en direct](journey-pause.md#apply-an-exit-criteria-in-a-paused-journey).

## Bonnes pratiques de gestion des entrées et des sorties {#best-practices}

**Effacer la définition**

* Documentez votre logique d’entrée et de sortie avant de créer des parcours pour aligner les équipes marketing et analytics
* Créer des diagrammes de flux présentant les points d’entrée, les chemins de parcours et les conditions de sortie
* Définissez clairement les règles métier : « Les profils se ferment lorsque X se produit OU après Y jours »
* Utilisez des libellés descriptifs : « Sortie - Achat terminé » et non « Sortie 1 ».
* [parcours de balises](../start/search-filter-categorize.md#tags) de manière cohérente pour les rapports et le filtrage

**Éviter les parcours qui se chevauchent**

* [Contrôlez les parcours actifs](journey-ui.md) avant de lancer des programmes similaires pour éviter les conflits
* Tirez parti de la [gestion des conflits](../conflict-prioritization/conflicts.md) et [scores de priorité](../conflict-prioritization/priority-scores.md) pour résoudre les chevauchements et hiérarchiser les parcours
* Concevoir des parcours qui se complètent plutôt que de se concurrencer

>[!NOTE]
>
>Pour les scénarios avancés tels que la suppression automatique des profils lorsqu’ils remplissent les critères pour les parcours de priorité supérieure, utilisez la limitation et l’arbitrage des parcours [&#128279;](../conflict-prioritization/journey-capping.md) au lieu des critères de sortie.

**Surveiller et optimiser**

* Suivez le taux d’entrée, le taux de sortie et le taux d’achèvement pour chaque parcours à l’aide de [rapports de parcours &#x200B;](../reports/journey-global-report-cja.md)
* Surveiller [mesures de succès](success-metrics.md) : pourcentage de sortie via l’achèvement des mesures de succès par rapport au délai d’expiration
* [Test des critères d’entrée et de sortie](testing-the-journey.md) avec divers scénarios de profil avant le lancement
* Ajuster en fonction des données : si le taux de sortie précoce est élevé, examiner la pertinence des critères d’entrée ; si la mesure de succès est faible, analyser le contenu et le timing.
* Consulter tous les parcours actifs chaque trimestre

**Respectez les limites de fréquence**

* Définir des [périodes d’attente de rentrée](entry-management.md) ou désactiver la rentrée pour les parcours uniques
* Utilisez des [règles de limitation de la fréquence](../conflict-prioritization/rule-sets.md) pour éviter la surcommunication
* Surveiller les mesures de fréquence dans les rapports pour garantir la conformité

>[!NOTE]
>
>Pour gérer les limites de fréquence et les limites d’entrée de parcours sur plusieurs parcours, utilisez [le capping et l’arbitrage des parcours &#x200B;](../conflict-prioritization/journey-capping.md) et [capping de la fréquence par canal](../conflict-prioritization/channel-capping.md).

## Conclusion {#conclusion}

Les critères d’entrée et de sortie de parcours sont fondamentaux pour offrir des expériences client personnalisées, opportunes et efficaces avec Adobe Journey Optimizer. En concevant soigneusement ces conditions, les professionnels du marketing peuvent stimuler l’engagement, réduire les frictions et créer des relations client plus solides.

Commencez par mapper clairement les déclencheurs et les points de sortie de vos clients, effectuez des tests approfondis et surveillez les résultats pour affiner en permanence votre orchestration de parcours.

## Ressources connexes {#related-resources}

**Documentation technique**

[&#x200B; Gestion des entrées de profil &#x200B;](entry-management.md) | [Propriétés du Parcours et critères de sortie](journey-properties.md) | [Fin des parcours &#x200B;](end-journey.md) | [&#x200B; Identifiants supplémentaires &#x200B;](supplemental-identifier.md) | [Concepteur de Parcours &#x200B;](using-the-journey-designer.md)

**Tutoriels et exemples**

[Cas d’utilisation de Parcours &#x200B;](jo-use-cases.md) | [Vidéo d’intégration des clients](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding) | [Vidéo de panier abandonné](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart) | [Blog communautaire : critères d&#39;entrée et de sortie](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/mastering-journey-entry-and-exit-criteria-in-adobe-journey/ba-p/760958?profile.language=fr)

**Fonctionnalités associées**

[&#x200B; Événements de qualification d’audience &#x200B;](audience-qualification-events.md) | [Mesures de succès et objectifs](success-metrics.md) | [&#x200B; Gestion des conflits &#x200B;](../conflict-prioritization/conflicts.md) | [Capping de la fréquence](../conflict-prioritization/rule-sets.md) | [Test des parcours &#x200B;](testing-the-journey.md) | [Activité de condition](condition-activity.md) | [Événements de réaction](reaction-events.md) | [Activité d’attente](wait-activity.md)
