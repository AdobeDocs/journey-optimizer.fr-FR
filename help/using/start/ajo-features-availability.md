---
solution: Journey Optimizer
product: journey optimizer
title: Disponibilité des fonctionnalités Journey Optimizer
description: Référence unique et consolidée permettant de déterminer les fonctionnalités Adobe Journey Optimizer disponibles, leur statut de cycle de vie (disponibilité générale, disponibilité limitée ou Beta), l’offre de base à laquelle elles s’appliquent et la date de livraison, sans référence croisée aux notes de mise à jour.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner, Intermediate
keywords: parcours optimizer, disponibilité des fonctionnalités, disponibilité générale, disponibilité limitée, version bêta, cycle de vie, date de publication, droits, offre de base, campagnes, parcours
hide: true
source-git-commit: f13e351c6c3851f9c031e7aa907ecc5924e0df4f
workflow-type: tm+mt
source-wordcount: '1880'
ht-degree: 13%

---


# Disponibilité des fonctionnalités Journey Optimizer {#ajo-features-availability}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez les fonctionnalités [!DNL Adobe Journey Optimizer] disponibles, à quelle étape du cycle de vie chacune d’elles se trouve (disponibilité générale, disponibilité limitée ou Beta), à quelle offre de base elles s’appliquent et quand elles ont été expédiées, afin que vous puissiez répondre *« puis-je utiliser ceci ? »* sans parcourir les notes de mise à jour.

>[!ENDSHADEBOX]

Cette page consolide la disponibilité des fonctionnalités dans [!DNL Adobe Journey Optimizer] afin que vous puissiez confirmer ce que vous pouvez utiliser pendant la définition de la portée préalable à l’implémentation. Les fonctionnalités sont regroupées par domaine de fonctionnalité. Dans chaque zone, chaque fonctionnalité répertorie son statut de cycle de vie actuel, l’offre de base à laquelle elle s’applique, la date à laquelle elle est devenue disponible et toute note sur la configuration ou les restrictions régionales.

Les lignes marquées **Fonctionnalité principale** dans la colonne *Disponible depuis* sont des fonctionnalités fondamentales de longue date qui sont généralement disponibles depuis avant 2026. Les lignes datées reflètent les modifications envoyées en 2026.

>[!IMPORTANT]
>
>**Pourquoi est-ce que je ne peux pas voir une fonctionnalité dans mon environnement ?** Les fonctionnalités de **Disponibilité limitée** ou **Beta** ne sont pas visibles par tout le monde ; elles sont d’abord déployées dans un ensemble restreint d’organisations. Si une fonctionnalité que vous avez lue n’apparaît pas dans votre environnement, vérifiez son statut ci-dessous : s’il s’agit de **LA** ou **Beta**, contactez votre représentant Adobe pour demander l’accès. Une fonctionnalité répertoriée ici ne signifie pas qu’elle est activée dans votre environnement.

>[!NOTE]
>
>**Disponibilité et droits.** Cette page effectue le suivi *cycle de vie et disponibilité des fonctionnalités* (si une fonctionnalité a été livrée et à quelle maturité). Le fait qu’une fonctionnalité soit *incluse dans votre licence* dépend de votre offre de base et de vos modules complémentaires. Voir [Packages et fonctionnalités](ajo-packages.md).

## Signification des statuts du cycle de vie {#status-definitions}

| État | Signification |
|--------|--------------|
| **GA** — Disponibilité générale | Distribué dans tous les environnements. Disponible pour toute organisation dont la licence inclut la fonctionnalité. |
| **LA** — Disponibilité limitée | Distribué à un ensemble restreint d’organisations. **Contactez votre représentant Adobe** pour demander l’accès. |
| **Beta** | Version à accès anticipé pour évaluation. Peut changer avant la disponibilité générale. Peut nécessiter un opt-in. |

## Mappage de l’expression « s’applique à » aux offres de base {#applies-to}

La colonne **S&#39;applique à** fait référence aux trois offres de base [!DNL Adobe Journey Optimizer] :

- **Journey Optimizer - Campagnes** — orchestration par lots basée sur les audiences
- **Journey Optimizer - Parcours** — orchestration en temps réel et basée sur les événements
- **Journey Optimizer - Campagnes et Parcours** - les deux

Les fonctionnalités de canal, de contenu et de plateforme marquées **Toutes les offres de base** sont disponibles quelle que soit l’offre de base, mais la plupart nécessitent toujours le canal approprié ou le module complémentaire de fonctionnalité avancé. Voir [Packages et fonctionnalités](ajo-packages.md) pour les détails des droits.

## Fonctionnalités par domaine de fonctionnalité {#features-by-area}

>[!BEGINTABS]

>[!TAB Canaux]

| Fonctionnalité | Statut | Application | Disponible depuis | Remarques |
|---------|--------|-----------|-----------------|-------|
| Nouveau canal de message mobile (SMS, MMS, RCS) | GA | Toutes les offres de base | 20 Mai 2026 | Unifie les SMS/MMS/RCS ; création RCS native (images, carrousels) |
| Liens profonds dans le Concepteur d’e-mail | GA | Toutes les offres de base | 12 Mai 2026 | Nécessite une configuration d’application mobile |
| Optimiser les e-mails pour les boîtes de réception d’IA | GA | Toutes les offres de base | 17 Avril 2026 | Intelligence Apple, Gmail Gemini |
| Paramètres expéditeur dans l’en-tête des e-mails | GA | Toutes les offres de base | Avril 2026 | « Expéditeur au nom de » / « via » |
| Champ Cc dans les paramètres du canal E-mail | GA | Toutes les offres de base | Avril 2026 | Prend en charge la personnalisation |
| Boîte de réception | GA | Toutes les offres de base | 7 Avril 2026 | — |
| Canal de notifications push web | GA | Toutes les offres de base | 13 Février 2026 | Anciennement Beta |
| Activité en direct pour iOS | GA | Toutes les offres de base | 3 mars 2026 | Verrouiller l’écran / île dynamique ; anciennement Beta |
| Canal Courrier dans les parcours | GA | Parcours ; Campagnes et Parcours | 29 janvier 2026 | Anciennement LA |
| Canal courrier dans les campagnes orchestrées | GA | Campagnes ; Campagnes et Parcours | 28 janvier 2026 | — |
| Canal LINE | GA | Toutes les offres de base | 2025 | — |
| Prise en charge et suivi des boutons WhatsApp | GA | Toutes les offres de base | Mai 2026 | Réponse rapide, URL/téléphone CTA |
| Email | GA | Toutes les offres de base | Fonctionnalité principale | Nécessite le module complémentaire Diffusion sortante |
| Notifications push | GA | Toutes les offres de base | Fonctionnalité principale | Nécessite une diffusion sortante ou un module complémentaire mobile |
| SMS/MMS | GA | Toutes les offres de base | Fonctionnalité principale | En fonction de la configuration sous licence |
| Canal Courrier | GA | Toutes les offres de base | Fonctionnalité principale | Nécessite le module complémentaire Diffusion sortante |
| Messagerie in-app | GA | Toutes les offres de base | Fonctionnalité principale | Nécessite un module complémentaire mobile |
| Cartes de contenu | GA | Toutes les offres de base | Fonctionnalité principale | Nécessite un module complémentaire mobile |
| Canal web | GA | Toutes les offres de base | Fonctionnalité principale | Nécessite un module complémentaire Web |
| Expériences basées sur du code | GA | Toutes les offres de base | Fonctionnalité principale | Nécessite un module complémentaire mobile ou web |
| Landing pages | GA | Toutes les offres de base | Fonctionnalité principale | — |
| WhatsApp | GA | Toutes les offres de base | Fonctionnalité principale | Nécessite un module complémentaire WhatsApp ; basé sur une configuration sous licence |

>[!TAB Parcours]

| Fonctionnalité | Statut | Application | Disponible depuis | Remarques |
|---------|--------|-----------|-----------------|-------|
| Fragments de parcours | GA | Parcours ; Campagnes et Parcours | 9 Juin 2026 | Nœuds de parcours réutilisables ; prise en charge des outils Sandbox |
| Simulation de parcours | GA | Parcours ; Campagnes et Parcours | 9 Juin 2026 | Validation de la logique avec des utilisateurs simulés |
| Optimisation du chemin de parcours - Ciblage | GA | Parcours ; Campagnes et Parcours | 8 Juin 2026 | Ciblage déterministe des chemins |
| Prise en charge des identifiants supplémentaires pour les audiences externes | GA | Parcours ; Campagnes et Parcours | 11 Juin 2026 | Composition du CSV et de l’audience fédérée |
| Expérimentation du chemin du parcours | GA | Parcours ; Campagnes et Parcours | 7 Avril 2026 | A/B et bandit manchot ; « Scale the winder » |
| Activité d’action dans les parcours | GA | Parcours ; Campagnes et Parcours | 20 Février 2026 | Remplace les activités de canal natives obsolètes |
| Activité de décision de contenu | GA | Parcours ; Campagnes et Parcours | 10 Février 2026 | Anciennement LA |
| Heures creuses (exclusions basées sur les heures) | GA | Parcours ; Campagnes et Parcours | 29 janvier 2026 | Anciennement LA |
| Assistant AI pour les expressions de parcours | Beta | Parcours ; Campagnes et Parcours | 3 Juin 2026 | Beta publique |
| Arbitrage des parcours | LA | Parcours ; Campagnes et Parcours | 24 Février 2026 | Contactez votre représentant Adobe |
| Arbitrage de parcours - Modèles d’IA | LA | Parcours ; Campagnes et Parcours | Avril 2026 | Contactez votre représentant Adobe |
| Prise en charge de la recherche de jeu de données dans les parcours | LA | Parcours ; Campagnes et Parcours | Mars 2026 | Pour les clients autorisés à rechercher un jeu de données |
| Envoi en vague des messages sortants (parcours) | LA | Parcours ; Campagnes et Parcours | 16 mars 2026 | GA dans les campagnes ; LA dans les parcours |
| Parcours automatisés (déclenchés par un événement) | GA | Parcours ; Campagnes et Parcours | Fonctionnalité principale | Orchestration 1:1 en temps réel |
| Déclencheurs d’événement en temps réel | GA | Parcours ; Campagnes et Parcours | Fonctionnalité principale | — |
| Lecture des parcours d’audience | GA | Parcours ; Campagnes et Parcours | Fonctionnalité principale | — |
| Rapports de parcours | GA | Parcours ; Campagnes et Parcours | Fonctionnalité principale | — |

>[!TAB Campagnes]

| Fonctionnalité | Statut | Application | Disponible depuis | Remarques |
|---------|--------|-----------|-----------------|-------|
| Campagnes orchestrées en chaîne | GA | Campagnes ; Campagnes et Parcours | 20 Mai 2026 | Déclencher une campagne à partir de l’activité Fin d’une autre campagne |
| Activité Requête incrémentale dans les campagnes orchestrées | GA | Campagnes ; Campagnes et Parcours | 30 Avril 2026 | Ne cible que les nouveaux profils/événements éligibles |
| Copier des campagnes orchestrées dans des sandbox | GA | Campagnes ; Campagnes et Parcours | Avril 2026 | Les campagnes importées atteignent le statut de brouillon |
| Activité de test dans les campagnes orchestrées | GA | Campagnes ; Campagnes et Parcours | Mars 2026 | — |
| Déclencher des campagnes orchestrées à l’aide d’un signal | GA | Campagnes ; Campagnes et Parcours | Mars 2026 | Reste une campagne par lots |
| Catégorie transactionnelle dans les campagnes orchestrées | GA | Campagnes ; Campagnes et Parcours | Mars 2026 | Déployé progressivement par région |
| Envoi d&#39;une vague de messages sortants (campagnes) | GA | Campagnes ; Campagnes et Parcours | 19 Février 2026 | LA dans les parcours |
| Campagnes par lots | GA | Campagnes ; Campagnes et Parcours | Fonctionnalité principale | Envois planifiés, basés sur l’audience |
| Campagnes orchestrées (workflows à plusieurs étapes) | GA | Campagnes ; Campagnes et Parcours | Fonctionnalité principale | e-mail, SMS, notification push, courrier uniquement |
| Messages transactionnels | GA | Toutes les offres de base | Fonctionnalité principale | e-mail, notification push, SMS ; inclus dans chaque offre de base |

>[!TAB Contenu et IA]

| Fonctionnalité | Statut | Application | Disponible depuis | Remarques |
|---------|--------|-----------|-----------------|-------|
| Sélecteur du conseilleur en contenu | GA | Toutes les offres de base | 19 Mai 2026 | Recherche sémantique de ressources et de fragments par l’IA |
| Intégrations (sources de données tierces) | GA | Toutes les offres de base | 4 Mai 2026 | Anciennement Beta |
| Limiter la rupture d’héritage dans les fragments | GA | Toutes les offres de base | 21 Mai 2026 | Verrouiller les fragments sur les modifications locales |
| Intégration d’Adobe Express | GA | Toutes les offres de base | 23 Avril 2026 | Anciennement LA |
| Assistant AI pour les expressions de personnalisation | GA | Toutes les offres de base | 13 Avril 2026 | Dans l’éditeur de personnalisation et le Designer d’e-mail |
| Convertir des images en modèles de contenu d’e-mail | GA | Toutes les offres de base | 31 mars 2026 | Anciennement LA |
| Formulaires personnalisés de la page de destination | GA | Toutes les offres de base | 26 mars 2026 | Anciennement LA (États-Unis et Australie) |
| Intégration de Firefly personnalisés et de modèles d’image tiers | GA | Toutes les offres de base | 2 mars 2026 | Adobe, Partenaires (Gemini) et modèles personnalisés |
| Éditeur HTML avancé pour les modèles d’e-mail | LA | Toutes les offres de base | 10 mars 2026 | Modèles de contenu d’e-mail uniquement ; contactez votre représentant |
| Mode expert en matière d’e-mail dans le contenu des e-mails | LA | Toutes les offres de base | 9 Avril 2026 | Contactez votre représentant Adobe |
| Thèmes du Concepteur d’e-mail | LA | Toutes les offres de base | 5 Novembre 2025 | Anciennement Beta ; contactez votre représentant |
| Designer des e-mails (glisser-déposer) | GA | Toutes les offres de base | Fonctionnalité principale | Création visuelle et HTML |
| Fragments de contenu | GA | Toutes les offres de base | Fonctionnalité principale | Blocs de contenu réutilisable |
| Modèles de contenu | GA | Toutes les offres de base | Fonctionnalité principale | — |
| Éditeur Personalization | GA | Toutes les offres de base | Fonctionnalité principale | Personnalisation basée sur les expressions |
| Assistant IA pour la génération de contenu | GA | Toutes les offres de base | Fonctionnalité principale | Conditions de licence de l’IA requises |

>[!TAB Prise de décision]

Toutes les fonctionnalités de prise de décision nécessitent le module complémentaire **Decisioning**. Voir [Packages et fonctionnalités](ajo-packages.md).

| Fonctionnalité | Statut | Application | Disponible depuis | Remarques |
|---------|--------|-----------|-----------------|-------|
| Prise en charge de la prise de décision dans le canal Courrier | GA | Toutes les offres de base | 3 Juin 2026 | Prise en charge de la diffusion de décisions par lots |
| Règles de prise de décision et optimisation de l’IA dédiée aux formules de classement | GA | Toutes les offres de base | 5 Mai 2026 | Simplifications suggérées par l’IA |
| Prise en charge de Prise de décision dans le canal E-mail | GA | Toutes les offres de base | 6 avril 2026 | Pages miroir prises en charge |
| Surveillance des modèles d’IA | GA | Toutes les offres de base | 9 mars 2026 | Modèles d’optimisation personnalisés uniquement |
| Prise en charge de la prise de décision dans le canal SMS | GA | Toutes les offres de base | 2 Février 2026 | — |
| Prise en charge de la prise de décision dans le canal Notification push | GA | Toutes les offres de base | 30 janvier 2026 | — |
| Fragments de contenu Adobe Experience Manager dans la prise de décision | LA | Toutes les offres de base | 20 Mai 2026 | Contactez votre représentant Adobe |
| Offer Decisioning (politiques de décision) | GA | Toutes les offres de base | Fonctionnalité principale | Sélection des meilleures offres en temps réel |
| Classement optimisé par l&#39;IA | GA | Toutes les offres de base | Fonctionnalité principale | Optimisation des offres de machine learning |

>[!TAB Agents AI]

| Fonctionnalité | Statut | Application | Disponible depuis | Remarques |
|---------|--------|-----------|-----------------|-------|
| Journey Agent : création d’un parcours | GA | Parcours ; Campagnes et Parcours | mardi 12 janvier 2026 | Création de parcours en langage naturel |
| Intégration de l’agent Journey Optimizer AI via MCP | Beta | Toutes les offres de base | Avril 2026 | Beta publique ; Claude Web et bureau |
| Journey Agent : création de contenu de canal | LA | Toutes les offres de base | 4 mars 2026 | Contactez votre représentant Adobe |

>[!TAB Administration et données]

| Fonctionnalité | Statut | Application | Disponible depuis | Remarques |
|---------|--------|-----------|-----------------|-------|
| Authentification personnalisée basée sur des certificats dans les actions personnalisées | GA | Toutes les offres de base | 4 Juin 2026 | Pour l’identité basée sur un certificat (par exemple, Microsoft Entra ID) |
| Alertes des clients pour les événements de cycle de vie des campagnes | GA | Toutes les offres de base | 1er juin 2026 | S’abonner au niveau du sandbox |
| Chiffrement des paramètres d’URL | GA | Toutes les offres de base | 1er juin 2026 | Anciennement LA ; nécessite des autorisations de registre de clé |
| API d’outils de migration en libre-service | GA | Toutes les offres de base | 3 Février 2026 | — |
| Surveillance des actions personnalisées | GA | Toutes les offres de base | 3 Février 2026 | Anciennement LA |
| Exporter des messages | GA | Toutes les offres de base | 28 janvier 2026 | Disponible en tant que module complémentaire |
| API de récupération de campagne d’action | GA | Toutes les offres de base | 24 Novembre 2025 | — |
| Migrer les sous-domaines vers la délégation personnalisée | LA | Toutes les offres de base | 19 Février 2026 | Contactez votre représentant Adobe |
| Sandbox | GA | Toutes les offres de base | Fonctionnalité principale | Jusqu’à 5 sandbox ; en plus disponible |
| Profils et audiences unifiés | GA | Toutes les offres de base | Fonctionnalité principale | Construit sur Adobe Experience Platform |
| Rapports et rapports dynamiques | GA | Toutes les offres de base | Fonctionnalité principale | — |
| Autorisations et contrôle d’accès | GA | Toutes les offres de base | Fonctionnalité principale | Accès en fonction du rôle |
| API REST | GA | Toutes les offres de base | Fonctionnalité principale | Framework API-First |

>[!ENDTABS]

>[!NOTE]
>
>Cette liste est compilée à partir des notes de mise à jour [2026](../rn/release-notes-2026.md) et des [notes de mise à jour actuelles](../rn/release-notes.md) et reflète le dernier état connu de chaque fonctionnalité. Il n&#39;est pas exhaustif. Pour obtenir l’historique complet et les ajouts les plus récents, consultez toujours les [notes de mise à jour](../rn/release-notes.md).

## Ressources connexes {#related}

- **Comprendre le contenu de votre package** — [Packages et fonctionnalités](ajo-packages.md)
- **Voir tout ce qui a été envoyé** — [Notes de mise à jour](../rn/release-notes.md) | Notes de mise à jour [2026](../rn/release-notes-2026.md)
- **Commencer** — [Commencer avec Journey Optimizer](get-started.md)
