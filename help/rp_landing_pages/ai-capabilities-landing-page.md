---
solution: Journey Optimizer
product: Journey Optimizer
title: Fonctionnalités d’IA dans Adobe Journey Optimizer
description: Fonctionnalités d’IA dans Adobe Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: 2b377fea2f54c15d04fd0fc16633951c58598580
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 4%

---

# Fonctionnalités d’IA dans Adobe Journey Optimizer{#section-overview}

Adobe Journey Optimizer exploite la puissance de l’intelligence artificielle et du machine learning pour transformer la manière dont vous créez, optimisez et diffusez des expériences client. De la génération de contenu personnalisé sur plusieurs canaux à la prévision du moment optimal pour interagir avec les clients, les fonctionnalités d’IA rationalisent votre workflow et maximisent l’impact. Cette section explique comment les fonctionnalités optimisées par l’IA s’associent pour vous aider à prendre des décisions plus intelligentes, à automatiser des tâches complexes et à créer des expériences qui trouvent un véritable écho auprès de votre audience. Que vous tiriez parti de l’IA générative pour la création de contenu, que vous utilisiez des modèles prédictifs pour la prise de décision ou que vous optimisiez les heures d’envoi pour améliorer l’engagement, vous découvrirez des outils et des stratégies pratiques pour libérer le plein potentiel de l’IA dans votre orchestration de parcours clients.

## Fonctionnalités optimisées par l’IA

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=fr)

Assistant IA pour la génération de contenu

Utilisez l’IA générative pour créer et personnaliser du contenu dans les e-mails, SMS, notifications push, pages web et pages de destination.

[Explore AI Assistant](ai-assistant-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=fr)

Optimisation de l’heure d’envoi

Utilisez l’IA pour prévoir le moment optimal pour envoyer des messages et optimiser l’engagement des clients en fonction du comportement historique.

[En Savoir Plus Sur L’Optimisation De L’Heure D’Envoi](../using/building-journeys/send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=fr)

Modèles d’IA pour la prise de décision

Créez des modèles d’optimisation automatique et d’optimisation personnalisée pour classer et diffuser les meilleures offres à vos clients.

[Découvrir les modèles d’IA](ai-models-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=fr)

Connaissance des produits de l’assistant d’IA

Obtenez des réponses instantanées et des informations opérationnelles sur Adobe Journey Optimizer à l’aide de l’IA conversationnelle.

[Utiliser l’Assistant IA](../using/start/ai-assistant.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=fr)

Expérimentation de contenu avec l’IA

Générez plusieurs variations de contenu et exécutez des expériences pour identifier le contenu le plus performant pour votre audience.

[En savoir plus sur l’expérimentation d’IA](../using/content-management/generative-experimentation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=fr)

Intégration de Customer AI

Intégrez-la aux services intelligents d’Adobe afin de prédire le comportement des clients et d’utiliser les scores d’attrition et de conversion dans vos parcours.

[Explorer les services intelligents](../using/building-journeys/ai-services-overview.md)
:::

::::


## Ressources supplémentaires

- **[Score d’alignement des marques](../using/content-management/brands-score.md)** - Évaluez dans quelle mesure votre contenu généré par l’IA correspond aux directives de votre marque à l’aide du score optimisé par l’IA.
- **[Accélérateur d’expériences](../using/content-management/experiment-accelerator-gs.md)** - Accélérez votre processus d’expérimentation de contenu avec des informations et des recommandations pilotées par l’IA.
- **[API optimisées par l’IA](../using/configuration/ajo-apis.md)** - Accédez aux fonctionnalités d’IA et de machine learning de Journey Optimizer par programmation via les API.

## Questions fréquentes

+++**Quelles autorisations sont requises pour utiliser les fonctionnalités d’IA ?**

Pour utiliser l’assistant AI pour la génération de contenu, les utilisateurs doivent disposer de l’autorisation **Générer du contenu**. Cette autorisation est attribuée via la ressource Assistant AI dans le produit Autorisations . Pour utiliser AI Assistant avec des connaissances sur les produits et des informations opérationnelles, les utilisateurs doivent accepter les directives d’utilisation de Adobe Experience Cloud Generative AI.

[En savoir plus sur les autorisations](../using/administration/ootb-permissions.md)

+++

+++**Quels canaux prennent en charge la génération de contenu de l’assistant AI ?**

L’assistant AI pour la génération de contenu est disponible pour les canaux **E-mail**, **Push**, **SMS** et **Web**. Il n’est actuellement pas disponible pour les canaux Courrier, Cartes de contenu, LINE ou WhatsApp.

+++

+++**Quelles sont les bonnes pratiques relatives à l’utilisation de l’assistant AI ?**

- **Utiliser des invites bien définies** - La qualité du contenu généré est fortement affectée par votre objectif et votre invite marketing. Soyez précis et clair.
- **Chargement de ressources de marque** - Fournissez des ressources de marque au format PDF, JPEG, PNG ou ZIP (50 Mo max.) pour un contenu précis et intégré à la marque.
- **Utiliser des modèles personnalisés** - Utilisez des modèles d’e-mail spécifiques à la marque avec jusqu’à 8 à 10 images pour des résultats optimaux.
- **Fournir des commentaires** - Signalez les sorties problématiques à l’aide des icônes de pouce vers le haut, vers le bas ou d’indicateur pour aider à affiner les modèles.
- **N’utilisez qu’une ressource de marque par génération** - Bien que vous puissiez charger plusieurs ressources, n’en utilisez qu’une pour chaque génération spécifique.

[En savoir plus sur les mécanismes de sécurisation de l’assistant AI](../using/content-management/gs-generative.md#generative-guardrails)

+++

+++**Quelles sont les bonnes pratiques pour l’optimisation de l’heure d’envoi ?**

- **Patientez 30 jours** - Utilisez les actions E-mail et Push pendant au moins 30 jours avant d’activer l’optimisation de l’heure d’envoi pour garantir une collecte de données suffisante.
- **Choisir des temps d’attente optimaux** - Définissez le temps d’attente maximal entre 6 et 24 heures pour obtenir de meilleurs résultats. Des durées plus courtes limitent le potentiel d’optimisation ; des durées plus longues peuvent entraîner des messages obsolètes.
- **Optimiser pour la mesure appropriée** - Pour les e-mails, optimisez pour les clics lors de la conduite d’une action ou Ouvrez pour le contenu informatif. Les messages push sont toujours optimisés pour les ouvertures.
- **Éviter pour les messages sensibles à l’heure** - N’utilisez pas l’optimisation de l’heure d’envoi pour les messages opérationnels urgents tels que les confirmations de commande, les réinitialisations de mot de passe ou les notifications de vol. Idéal pour les communications marketing telles que les promotions et les newsletters.
- **Planifier les envois du matin pour les notifications push** - Pour éviter les notifications de nuit, planifiez les envois push par lots le matin avec des durées plus courtes (par exemple, envoi à 9 h avec un temps d&#39;attente de 8 heures).

[En savoir plus sur l’optimisation de l’heure d’envoi](../using/building-journeys/send-time-optimization.md)

+++

+++**Quelles sont les limites de l’optimisation de l’heure d’envoi ?**

- **Canaux** - Disponible uniquement pour les canaux E-mail et Notification push dans les Parcours. Non disponible dans les campagnes ou par le biais d’actions personnalisées.
- **Disponibilité** - Doit être activé par l’assistance clientèle d’Adobe ou votre représentant Adobe.
- **Période de formation** - Nécessite au moins 30 jours de données historiques d’e-mail ou de notification push avant utilisation.
- **Entraînement des modèles** - Les modèles sont d’abord entraînés une fois par semaine à l’aide des 16 dernières semaines de données, puis entraînés une fois par mois.
- **Exploration ou optimisation** - 5 % des messages reçoivent des heures d’envoi d’exploration aléatoire ; 95 % reçoivent des heures d’envoi optimisées.

+++

+++**Quelles sont les limites des modèles d’IA dans la prise de décision ?**

- **Modèles d’IA maximum** - Jusqu’à 5 modèles de classement par IA par organisation.
- **Exigences relatives aux jeux de données** - Au moins 2 offres doivent comporter plus de 100 événements d’affichage et plus de 5 événements de clic au cours des 14 derniers jours pour les modèles d’optimisation automatique.
- **Événements de retour** - Ils doivent être envoyés en tant qu’événements d’expérience et ne sont pas collectés automatiquement dans les canaux Journey Optimizer.
- **Limites de l’API** - Les modèles d’optimisation automatique ne fonctionnent pas avec l’API Batch Decisioning (gestion des décisions uniquement).

[Découvrir les modèles d’IA](../using/experience-decisioning/ranking/ai-models.md)

+++

+++**Quels mécanismes de sécurisation s’appliquent à la prise de décision optimisée par l’IA ?**

| Composant | Limite |
|-----------|-------|
| Modèles de classement AI | 5 par organisation |
| Demandes de décision (basées sur le code avec segmentation Edge) | 1 500 par seconde |
| Demandes de décision (basées sur le code sans segmentation Edge) | 5 000 par seconde |
| Collections d’éléments | 10 000 au total |
| Éléments d’offre par collection | 500 |
| Stratégies de sélection par politique de décision | 10 |
| Éléments d’offre renvoyés par politique de décision | 30 |
| Règles d&#39;éligibilité + formules de classement | 10 000 au total |
| Attributs de profil par règle | 25 |
| Attributs de données contextuelles par règle | 30 |

[En savoir plus sur les mécanismes de sécurisation de Decisioning](../using/experience-decisioning/decisioning-guardrails.md)

+++

+++**Dois-je accepter les conditions d’utilisation des fonctionnalités d’IA ?**

Oui, vous devez accepter les [instructions d’utilisation de l’IA générative de Adobe Experience Cloud](https://www.adobe.com/fr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) avant d’utiliser l’assistant d’IA dans Journey Optimizer. Pour plus d’informations, contactez votre représentant Adobe. En outre, Adobe applique Content Credentials aux ressources générées par Firefly dans le cadre de son engagement en faveur de la transparence dans l’utilisation générative de l’IA.

+++

+++**Le contenu généré par l’IA est-il toujours exact ?**

Non. Le contenu d’IA génératif peut ne pas toujours être précis. Vérifiez toujours la précision des sorties générées par l’IA et assurez-vous qu’elles sont appropriées à votre cas d’utilisation. Partagez vos commentaires à l’aide des outils d’évaluation fournis afin d’aider les ingénieurs à affiner les modèles.

+++

