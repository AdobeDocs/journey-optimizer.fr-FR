---
solution: Journey Optimizer
product: journey optimizer
title: Critères d’entrée et de sortie de parcours
description: Découvrez comment gérer efficacement le moment où les profils rejoignent les parcours et en sortent à l’aide d’exemples réels et de bonnes pratiques.
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: entrée, sortie, critères, parcours, profil, reprise, bonnes pratiques
version: Journey Orchestration
exl-id: e879a0f6-b969-4de0-a733-f2880d58d59b
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 94%

---

# Utiliser les critères d’entrée et de sortie d’un parcours {#entry-exit-criteria-guide}

Dans l’orchestration de l’expérience client, diffuser le bon message au bon moment nécessite un contrôle précis des moments où les personnes rejoignent vos parcours et en sortent. Comprendre et configurer correctement les critères d’entrée et de sortie peut faire la différence entre une campagne réussie et attrayante et les opportunités manquées ou la lassitude face aux messages.

Ce guide fournit des conseils pratiques, des exemples réels et des bonnes pratiques pour gérer les critères d’entrée et de sortie de parcours en [!DNL Adobe Journey Optimizer].

## Que sont les critères d’entrée et de sortie ? {#what-are-criteria}

Les **critères d’entrée** déterminent les conditions dans lesquelles un [profil client](../audience/get-started-profiles.md) peut rejoindre un parcours spécifique. Les profils peuvent rejoindre un parcours en fonction des éléments suivants :

* **[Comportement de la clientèle](../event/about-events.md)** : les actions entreprises par la clientèle déclenchent une entrée de parcours en temps réel, comme effectuer un achat, abandonner un panier ou ouvrir votre application mobile.

* **[Attributs de profil](../audience/get-started-profiles.md)** : les caractéristiques de la clientèle déterminent l’éligibilité en fonction des données stockées dans son profil, telles que le niveau de fidélité, l’emplacement, l’âge ou les préférences de communication.

* **[Événements externes](../event/about-creating-business.md)** : déclencheurs commerciaux ou environnementaux qui affectent plusieurs personnes simultanément, tels que des alertes de faible niveau de stock, des conditions météorologiques ou des changements de prix.

* **[Appartenance à une audience](../audience/about-audiences.md)** : l’appartenance à un segment d’audience spécifique active des parcours ciblés pour des groupes tels que la clientèle à forte valeur ajoutée, les personnes inactives ou les personnes nouvellement abonnées.

Les **critères de sortie** définissent quand et comment un profil quitte ou est supprimé d’un parcours :

* **Achèvement du parcours** : les profils sortent automatiquement lorsqu’ils atteignent la [fin de tous les chemins de parcours](end-journey.md), achevant ainsi l’expérience conçue.

* **Atteinte des mesures de succès** : les profils quittent le parcours lorsqu’ils atteignent l’[objectif du parcours](success-metrics.md), par exemple lors d’un achat ou du téléchargement d’une application, ce qui élimine les communications de suivi inutiles.

* **Basé sur des conditions** : les profils quittent le parcours lorsque des [conditions spécifiques](condition-activity.md) sont remplies, comme l’inactivité sur une période définie ou des modifications dans les attributs de profil.

* **Basé sur des événements** : les profils quittent le parcours lorsque des [événements spécifiques](../event/about-events.md) se produisent, tels que l’annulation d’un abonnement ou le retour d’un produit.

* **Disqualification de l’audience** : les profils quittent le parcours lorsqu’ils ne répondent plus aux [critères de l’audience cible](../audience/about-audiences.md), assurant ainsi que les messages restent pertinents.

## Importance des critères d’entrée et de sortie {#why-they-matter}

Bien définir les critères d’entrée et de sortie offre une valeur commerciale significative :

* **Pertinence** : seules les personnes pertinentes rejoignent le parcours, ce qui augmente les taux d’engagement et de conversion en ciblant l’audience la plus appropriée au moment optimal.

* **Efficacité** : évite que la clientèle reste dans des parcours non pertinents, ce qui réduit les communications inutiles, les coûts d’exploitation et la lassitude.

* **Personnalisation** : permet la personnalisation dynamique des expériences en fonction des données et du comportement en temps réel, créant ainsi des interactions clientèle plus significatives.

* **Conformité** : permet de gérer le capping de la fréquence et d’éviter la surcommunication, en respectant les préférences de la clientèle et les exigences réglementaires tout en préservant la réputation de la marque.

## Exemples concrets d’entrées et de sorties de parcours {#real-world-examples}

Voici des scénarios courants qui montrent comment fonctionnent en pratique les critères d’entrée et de sortie :

**Campagne de bienvenue pour les personnes nouvellement abonnées**

Créez une première impression personnalisée en orientant automatiquement les personnes nouvellement abonnées vers la présentation de votre marque, vos produits et vos services.

* **Entrée** : les profils rejoignent le parcours lorsqu’ils s’abonnent à une newsletter.
* **Sortie** : les profils quittent le parcours une fois qu’ils ont reçu une série d’e-mails de bienvenue ou après une période définie en cas d’absence d’interaction.
* **Avantage** : garantit que les personnes nouvellement abonnées soient intégrées au parcours en temps opportun tout en évitant les messages répétitifs.

**Récupération de panier abandonné**

Récupérez les revenus perdus en remémorant à la clientèle les articles qu’elle a laissés de côté et en l’incitant à terminer ses achats.

* **Entrée** : les personnes rejoignent le parcours si elles ajoutent des articles à un panier sans toutefois passer en caisse dans les 24 heures.
* **Sortie** : les profils quittent le parcours lorsqu’ils effectuent l’achat ou après 7 jours si aucun achat n’est effectué.
* **Avantage** : génère des conversions par des rappels opportuns sans spammer les personnes qui ne sont pas intéressées.

**Engagement au programme de fidélité**

Récompensez votre clientèle à forte valeur ajoutée avec des avantages exclusifs et des communications personnalisées qui renforcent la fidélité à la marque et augmentent la valeur de durée de vie.

* **Entrée** : les personnes rejoignent le parcours après avoir atteint un certain seuil de points de fidélité.
* **Sortie** : les profils quittent le parcours après l’échange de récompenses ou s’ils sont inactifs pendant 60 jours.
* **Avantage** : fidélise les personnes à forte valeur ajoutée grâce à des offres personnalisées et évite la lassitude liée aux nombreuses communications.

**Collecte des retours produit**

Collectez des informations sur la satisfaction client et les performances des produits en demandant un retour au meilleur moment après la diffusion.

* **Entrée** : les personnes rejoignent le parcours après réception d’un événement de confirmation de diffusion du produit.
* **Sortie** : les profils quittent le parcours une fois les commentaires envoyés ou après 10 jours en l’absence de réponse.
* **Avantage &#x200B;** : capture rapidement des commentaires utiles sans importuner la clientèle par des demandes persistantes.

## Configurer les critères d’entrée de parcours {#configure-entry}

>[!BEGINSHADEBOX]

**Découvrez ici tout ce que vous devez savoir sur les critères d’entrée :**

* **[Déclencheurs basés sur un événement](../event/about-events.md)** : utilisez des événements tels que « création de profil », « transaction terminée » ou des événements personnalisés pour lancer un parcours. [Configurez les événements](../event/about-creating.md) dans **[!UICONTROL Administration]** > **[!UICONTROL Événements]** et définissez [le schéma et les champs d’événement](../event/experience-event-schema.md). Ajoutez ensuite l’événement à partir de la palette **[!UICONTROL Événements]** dans le concepteur de parcours [&#128279;](using-the-journey-designer.md).

* **[Entrée basée sur l’audience](read-audience.md)** : les parcours cibles sont destinés aux profils qui appartiennent à des audiences spécifiques, sous la forme d’un lot unique ou selon un planning récurrent. [Créez des audiences](../audience/creating-a-segment-definition.md) dans le menu **[!UICONTROL Audiences]**, puis ajoutez une activité **[!UICONTROL Lecture d’audience]** et [configurez le planning](journey-properties.md#schedule).

* **[Entrée de la qualification de l’audience](audience-qualification-events.md)** : déclenchez des parcours lorsque les profils répondent aux critères d’audiences spécifiques ou en sortent en temps réel. Définissez des [audiences de streaming](../audience/about-audiences.md), ajoutez un événement **[!UICONTROL Qualification d’audience]** à partir de la palette **[!UICONTROL Événements]** et choisissez le type de déclencheur.

* **[Filtres d’attributs](condition-activity.md)** : affinez les critères d’entrée en combinant des événements ou des audiences avec des attributs de profil et du contexte à l’aide de la logique AND/OR. Utilisez des [conditions](conditions.md) pour référencer les [attributs de profil](../audience/get-started-profiles.md), événements ou [données externes](../datasource/about-data-sources.md).

* **[Fenêtres de temps et planification](journey-properties.md#schedule)** : définissez des contraintes temporelles pour que les parcours restent opportuns et pertinents. Configurez des [plannings sur les activités de lecture d’audience](read-audience.md), utilisez des [activités d’attente](wait-activity.md) et ajoutez des [conditions basées sur le temps](conditions.md) pour contrôler le timing.

>[!ENDSHADEBOX]

## Configurer les critères de sortie de parcours {#configure-exit}

>[!BEGINSHADEBOX]

**Découvrez ici tout ce que vous devez savoir sur les critères de sortie :**

* **[Achèvement du parcours](end-journey.md)** : les profils quittent le parcours automatiquement lorsqu’ils atteignent l’étape de parcours finale. Concevez des parcours se terminant par des activités de **[!UICONTROL fin]**.

* **[Atteinte des mesures de succès](journey-properties.md#exit-criteria)** : définissez des mesures de succès (comme les achats ou les abonnements) et faites sortir les profils une fois ces objectifs atteints. Cliquez sur l’icône **[!UICONTROL Afficher les critères de sortie]**, sélectionnez **[!UICONTROL Ajouter des critères de sortie]**, puis choisissez un [Événement](../event/about-events.md) ou une [Audience](../audience/about-audiences.md) comme déclencheur de sortie.

* **[Délais d’inactivité](wait-activity.md)** : faites sortir les profils si aucun engagement ne se produit au cours d’une période définie. Utilisez les [Critères de sortie](journey-properties.md#exit-criteria) avec les audiences qui vérifient la date du dernier engagement, définissent les [activités d’attente](wait-activity.md) avec des durées définies et utilisent les [conditions](condition-activity.md) pour vérifier l’activité.

* **[Règles de rentrée](entry-management.md)** : déterminez si les profils peuvent entrer à nouveau dans le parcours, plusieurs fois ou une seule fois, selon votre stratégie de campagne. Configurez les paramètres de **[!UICONTROL rentrée]** dans les **[!UICONTROL propriétés]** du parcours afin de définir des délais d’attente, d’activer la reprise forcée ou d’utiliser des [identifiants supplémentaires](supplemental-identifier.md) pour une reprise spécifique au contexte.

>[!ENDSHADEBOX]

## Exemples de parcours détaillés {#journey-examples}

Pour obtenir des conseils de mise en œuvre détaillés avec des détails techniques complets, explorez ces cas d’utilisation documentés :

* **[Parcours d’intégration de la clientèle](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)** : créez des expériences de bienvenue personnalisées avec qualification d’audience, temporisation des événements et sorties basées sur des objectifs.

* **[Récupération du panier abandonné](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)** : récupérez les ventes perdues avec des parcours, des playbooks et un routage de canal déclenchés par des événements.

* **[Campagnes de réengagement](https://experienceleague.adobe.com/fr/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)** : récupérez la clientèle inactive à l’aide du ciblage comportemental et de l’activation de médias achetés.

* **[Envoyez des messages aux personnes abonnées](message-to-subscribers-uc.md)** : ciblez les listes d’abonnements avec la lecture d’audience et du contenu personnalisé.

* **[Envoi de messages multicanaux](journeys-uc.md)** : Combinez les e-mails et les notifications push avec des événements de réaction et une logique à chemins multiples.

* **[Envoyer des e-mails uniquement les jours de la semaine](weekday-email-uc.md)** : planifiez des communications à l’aide de conditions temporelles et de formules d’attente.

>[!TIP]
>
>Parcourez tous les cas d’utilisation disponibles dans la bibliothèque de cas d’utilisation de Parcours [&#128279;](jo-use-cases.md) pour plus de modèles et d’implémentations. Par exemple, [améliorez les diffusions](ramp-up-deliveries-uc.md), [modèles d’événement d’expérience](exp-event-lookup.md) et [supprimez des profils des parcours en direct](journey-pause.md#apply-an-exit-criteria-in-a-paused-journey).

## Bonnes pratiques de gestion des entrées et des sorties {#best-practices}

**Une définition claire**

Établissez une documentation et des conventions de nommage claires pour vous assurer que votre équipe comprend comment les profils progressent dans vos parcours :

* Documentez votre logique d’entrée et de sortie avant de créer des parcours pour aligner les équipes marketing et d’analyse.
* Créez des diagrammes de flux présentant les points d’entrée, les chemins de parcours et les conditions de sortie.
* Définissez clairement les règles métier : « Les profils quittent le parcours lorsque X se produit OU après Y jours ».
* Utilisez des libellés descriptifs : « Sortie - Achat terminé » et non « Sortie 1 ».
* [Balisez les parcours](../start/search-filter-categorize.md#tags) de manière cohérente pour le reporting et le filtrage.

**Évitez les parcours qui se chevauchent**.

Évitez la confusion de la clientèle et les conflits de messages en coordonnant votre stratégie de parcours entre les campagnes :

* [Auditez les parcours actifs](journey-ui.md) avant de lancer des programmes similaires pour éviter les conflits.
* Tirez parti de la [gestion des conflits](../conflict-prioritization/conflicts.md) et des [scores de priorité](../conflict-prioritization/priority-scores.md) pour résoudre les chevauchements et hiérarchiser les parcours.
* Concevez des parcours qui se complètent plutôt que de se concurrencer.

>[!NOTE]
>
>Pour les scénarios avancés tels que la suppression automatique des profils lorsqu’ils remplissent les critères des parcours de priorité supérieure, utilisez le [capping et l’arbitrage des parcours](../conflict-prioritization/journey-capping.md) au lieu des critères de sortie.

**Surveiller et optimiser**

Évaluez en permanence les performances du parcours et ajustez vos critères d’entrée et de sortie en fonction du comportement réel des clients et des clientes :

* Suivez le taux d’entrée, le taux de sortie et le taux d’achèvement pour chaque parcours à l’aide des [rapports de parcours](../reports/journey-global-report-cja.md).
* Surveillez les [mesures de succès](success-metrics.md) : pourcentage de sorties dues à l’atteinte des mesures de succès par rapport celles dues à la temporisation.
* [Testez les critères d’entrée et de sortie](testing-the-journey.md) avec divers scénarios de profil avant le lancement.
* Effectuez des ajustements en vous basant sur les données : si le taux de sortie précoce est élevé, vérifiez que les critères d’entrée sont pertinents ; si le taux d’atteinte des mesures de succès est faible, analysez le contenu et le calendrier.
* Consultez tous les parcours actifs chaque trimestre.

**Respectez les cappings de la fréquence**.

Entretenez la confiance et l’engagement de la clientèle en contrôlant la fréquence des messages dans toutes les communications du parcours :

* Définissez des [périodes d’attente avant une reprise](entry-management.md) ou désactivez la possibilité d’effectuer une nouvelle entrée pour les parcours uniques.
* Utilisez des [règles de capping de la fréquence](../conflict-prioritization/rule-sets.md) pour éviter une communication excessive.
* Surveillez les mesures de fréquence dans les rapports pour garantir la conformité.

>[!NOTE]
>
>Pour gérer les limites de fréquence et les limites d’entrée de plusieurs parcours, utilisez [la limitation et l’arbitrage des parcours](../conflict-prioritization/journey-capping.md) ainsi que le [capping de la fréquence par canal](../conflict-prioritization/channel-capping.md).

## Conclusion {#conclusion}

Les critères d’entrée et de sortie de parcours sont fondamentaux pour offrir des expériences client personnalisées, opportunes et efficaces avec [!DNL Adobe Journey Optimizer]. Si vous remplissez ces conditions, vous pourrez stimuler l’engagement, réduire les frictions et renforcer la relation client.

Commencez par mapper clairement les déclencheurs et les points de sortie de vos clients et clientes, effectuez des tests approfondis et surveillez les résultats pour ajuster en permanence l’orchestration de votre parcours.

## Ressources connexes {#related-resources}

**Documentation technique**

[Gestion des entrées de profil](entry-management.md) | [Propriétés du parcours et critères de sortie](journey-properties.md) | [Fin des parcours](end-journey.md) | [Identifiants supplémentaires](supplemental-identifier.md) | [Concepteur de parcours](using-the-journey-designer.md)

**Tutoriels et exemples**

[Cas d’utilisation des parcours](jo-use-cases.md) | [Vidéo sur l’intégration des clients et des clientes](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding) | [Vidéo sur les paniers abandonnés](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart) | [Blog de la communauté : critères d’entrée et de sortie](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/mastering-journey-entry-and-exit-criteria-in-adobe-journey/ba-p/760958?profile.language=fr)

**Fonctionnalités associées**

[Événements de qualification d’audience](audience-qualification-events.md) | [Mesures de succès et objectifs](success-metrics.md) | [Gestion des conflits](../conflict-prioritization/conflicts.md) | [Capping de la fréquence](../conflict-prioritization/rule-sets.md) | [Test des parcours &#x200B;](testing-the-journey.md) | [Activité de condition](condition-activity.md) | [Événements de réaction](reaction-events.md) | [Activité d’attente](wait-activity.md)
