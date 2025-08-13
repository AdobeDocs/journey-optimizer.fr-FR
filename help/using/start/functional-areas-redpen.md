---
solution: Journey Optimizer
product: journey optimizer
title: Domaines fonctionnels
description: Domaines fonctionnels dans AJO
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: c9b02ae2-e07b-41f4-90cc-b2c0966f1ed1
hide: true
source-git-commit: 72ff06a7d87d6d9e5bfc0c6462ea4d60a98fc940
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Concepts de base

Adobe Journey Optimizer (AJO) comprend plusieurs domaines fonctionnels clés qui fonctionnent ensemble en toute transparence. Ce guide explique chaque zone et décrit comment ces zones se combinent pour créer des expériences client percutantes. La connaissance de ces domaines fonctionnels vous permet de tirer parti d’AJO pour offrir efficacement des expériences personnalisées et omnicanales.

## Présentation des domaines fonctionnels

| Domaine Fonctionnel | Bénéfice du Principal | Analogie |
|-------------------------|--------------------------------------------------|------------------------|
| Data Management | Organiser les données client appropriées | La Fondation |
| Gestion des clientes et clients | Identifiez vos clients | Connaître Votre Audience |
| Gestion de contenu | Créer et gérer des messages personnalisés et cohérents | Concevoir Votre Message |
| Gestion des décisions | Sélectionner le meilleur message/offre en temps réel | Le cerveau |
| Gestion des parcours | Concevoir et automatiser des expériences client transparentes | Chef D&#39;Orchestre |
| Connexions | Connecter les sources de données et effectuer la diffusion via les canaux client | Les tuyaux |
| Administration et confidentialité | Contrôler la configuration, l’accès et assurer la conformité des données | Le règlement |

## Domaines fonctionnels détaillés

### Gestion des données : The Foundation

**Objectif** : ingérer, structurer et gérer les données qui alimentent la personnalisation. Ce processus comprend la définition de structures de données (schémas), la création de conteneurs de stockage (jeux de données) et l’importation de données provenant de divers systèmes.

Considérez la gestion des données comme la base de l’engagement de tous les clients. Une base de données bien structurée garantit que chaque décision, message et parcours utilise des informations précises et organisées.

**Composants clés** :
- **Création et gestion des schémas** : définissez la structure des données client.
   - Exemple : créez un schéma décrivant des champs tels que « Prénom », « Adresse électronique » et « Historique des achats ».
- **Configuration du jeu de données** : organisez les données en conteneurs logiques.
   - Exemple : regroupez les données de transaction dans un jeu de données « Transactions de vente » pour une analyse plus facile.
- **Workflows d’ingestion de données** : importez efficacement des données dans la plateforme.
   - Exemple : utilisez des connecteurs Source préconfigurés pour importer les données client d’un système de gestion de la relation client (GRC).
- **Outils de qualité des données** : veillez à la précision et à l’exhaustivité des données.

**Avantage** : garantit que les données client sont fiables, organisées et accessibles, formant la base de toutes les activités AJO. Les connecteurs Source préconfigurés rationalisent l’ingestion des données à partir de plateformes courantes.



### Gestion des clients : connaître votre audience

**Objectif** : acquérir et maintenir une compréhension approfondie de chaque client. Cela implique l’utilisation du profil client en temps réel de Adobe Experience Platform (AEP) pour fusionner les données de tous les points de contact en une vue unifiée. Il gère également les identités entre les appareils et les canaux, ce qui permet le regroupement des individus en audiences cibles en fonction d’attributs ou de comportements partagés.

Les outils de gestion des clients connectent des points de données disparates afin de fournir une image cohérente de chaque client. Cette compréhension garantit que vous pouvez offrir des expériences pertinentes et personnalisées.

**Composants clés** :
- **Real-time Customer Profile** : vue unifiée de chaque client.
   - Exemple : combiner l’historique de navigation web, les interactions d’application et les achats hors ligne dans un seul profil.
- **Résolution d’identité** : liaison des données client entre les appareils et les canaux.
   - Exemple : faites correspondre l’adresse e-mail d’un client avec ses données d’utilisation de l’application à l’aide du graphique d’identités.
- **Création et gestion d’audiences** : définissez des groupes en fonction des attributs et des comportements.
   - Exemple : créez une audience pour les « clients fidèles » qui ont effectué plus de cinq achats au cours de l’année dernière.
- **Segmentation** : appliquez des règles pour l’appartenance dynamique à une audience.
   - Exemple : configurez un segment pour les « Acheteurs à forte valeur ajoutée » qui se met automatiquement à jour lorsque les clients dépensent plus de 500 $.

**Avantage** : permet un ciblage et une personnalisation précis grâce à une compréhension dynamique des préférences individuelles, de l’historique et des appartenances aux segments.



### Gestion De Contenu : Concevoir Votre Message

**Objectif** : créer, gérer, personnaliser et réutiliser du contenu marketing sur plusieurs canaux. Cela inclut la gestion des ressources numériques, la création de messages à l’aide d’éditeurs ou de code visuels, l’utilisation de modèles et de fragments de contenu réutilisables, la création de pages de destination et l’utilisation de l’intelligence artificielle (IA) pour la génération de contenu.

Les outils de gestion de contenu garantissent que les équipes créent et diffusent efficacement des messages personnalisés, en maintenant la cohérence et la pertinence à chaque point de contact.

**Composants clés** :
- **Éditeurs de contenu** : créez et formatez des messages visuellement ou à l’aide de code.
   - Exemple : utilisez l’éditeur visuel pour concevoir une campagne par e-mail visant à promouvoir les ventes de vacances.
- **Gestion des ressources numériques** : organisez et utilisez des images et d’autres médias.
   - Exemple : stockez les images du produit dans une bibliothèque centralisée pour une réutilisation facile dans les campagnes.
- **Modèles et fragments** : créez des composants de contenu réutilisables.
   - Exemple : créez un modèle « Message de bienvenue » qui insère dynamiquement les noms des clients.
- **Outils Personalization** : personnalisez dynamiquement le contenu pour les individus.
   - Exemple : afficher des recommandations de produits personnalisées en fonction de l&#39;historique de navigation.
- **Créateur de pages de destination** : créez des destinations web pour les campagnes.

**Avantage** : simplifie la création de contenu, assure la cohérence de la marque et facilite la diffusion efficace de messages hautement personnalisés.



### Gestion des décisions : le cerveau de Personalization

**Objectif** : sélectionnez le meilleur message ou la meilleure offre pour chaque client au bon moment, en fonction de son profil en temps réel, de son contexte et des règles commerciales ou modèles d’IA prédéfinis. La gestion des décisions implique la gestion d’une bibliothèque centrale d’offres, la définition de règles d’éligibilité, l’application de contraintes (comme le capping de la fréquence) et l’établissement d’une logique de classement.

La gestion des décisions garantit que la personnalisation fonctionne à grande échelle en offrant une valeur maximale grâce à l’automatisation intelligente.

**Composants clés** :
- **Bibliothèque des offres** : référentiel central des offres marketing.
   - Exemple : stockez des offres telles que « 20 % de réduction sur le coupon » ou « Livraison gratuite » dans une bibliothèque partagée.
- **Règles de décision** : logique de sélection d’un contenu optimal.
   - Exemple : afficher une « remise fidélité » uniquement pour les clients du segment « Clients fidèles ».
- **Contraintes et éligibilité** : contrôlez qui reçoit quoi et quand.
   - Exemple : appliquez un capping de la fréquence pour empêcher un client de recevoir la même offre deux fois en une semaine.
- **Stratégies de classement** : hiérarchisez les offres en fonction des objectifs commerciaux ou de l’IA.
   - Exemple : classer les offres par rentabilité, en commençant par les produits à marge élevée.
- **Outils de simulation** : tester et valider des stratégies de décision.

**Avantage** : automatise et optimise la personnalisation, en veillant à ce que des expériences pertinentes et percutantes soient fournies à chaque point de contact.



### Gestion du parcours : Le chef d&#39;orchestre

**Objectif** : concevoir, orchestrer et automatiser des expériences client sur plusieurs étapes et canaux. Les parcours réagissent aux comportements et aux événements des clients en temps réel, en guidant les individus à travers des chemins personnalisés. AJO prend également en charge les campagnes pour la diffusion de messages ponctuels planifiés à des audiences spécifiques.

La gestion des parcours permet de s’assurer que les expériences sont adaptatives et transparentes, en guidant les individus en fonction de leurs préférences et de leurs actions.

**Composants clés** :
- **Concepteur de Parcours** : zone de travail visuelle pour la création de chemins d’accès client.
   - Exemple : concevez un parcours qui envoie un e-mail de bienvenue lorsqu’un client s’inscrit.
- **Déclencheurs de Parcours** : événements qui déclenchent ou avancent des parcours.
   - Exemple : déclenchement d’un SMS de relance après l’abandon du panier par un client.
- **Étapes de condition** : utilisez l’embranchement logique.
   - Exemple : envoyez un message différent selon qu’un client ouvre ou non un e-mail.
- **Activités d’attente** : contrôle de la progression avec des retards.
   - Exemple : patientez trois jours avant d’envoyer un e-mail de rappel.
- **Gestion de campagne** : outils de messagerie planifiée unique.

**Avantage** : crée des expériences connectées et transparentes qui s’adaptent aux interactions individuelles, tout en nourrissant les relations et en produisant les résultats souhaités.



### Connexions : les tuyaux

**Objectif** : gérer le flux de données dans AJO (sources) et la diffusion de messages ou de données à partir d’AJO (canaux et destinations). Les sources apportent des données dans Adobe Experience Platform (AEP). Les canaux diffusent les messages (par e-mail, SMS, notification push, web, etc.). Les destinations permettent aux informations d’audience ou de jeu de données de se diriger vers des plateformes externes.

Les connexions permettent de s’assurer que les données entrent efficacement dans AJO et atteignent les clients de manière fiable via les bons points de contact.

**Composants clés** :
- **Connecteurs Source** : importez les données dans la plateforme.
   - Exemple : utilisez un connecteur pour importer les données d’achat d’une plateforme d’e-commerce.
- **Configuration des canaux** : configurez et gérez les mécanismes de diffusion.
   - Exemple : configurer la diffusion par SMS pour les messages promotionnels.
- **Configuration de la destination** : connexion à des systèmes d’activation externes.
   - Exemple : partagez des données d’audience avec une plateforme publicitaire de médias sociaux.
- **Gestion des flux de données** : contrôle du mouvement des informations.

**Avantage** : garantit une ingestion de données efficace et une diffusion fiable des messages sur plusieurs canaux, tout en activant l’activation dans des systèmes externes.



### Administration et confidentialité : le règlement

**Objectif** : configurer les paramètres du système, gérer l’accès et les autorisations des utilisateurs et utilisatrices, configurer des canaux de communication, définir des paramètres de parcours et assurer la conformité aux politiques de confidentialité et de gouvernance des données. Cela inclut la gestion du consentement, l’application des règles d’utilisation des données et le traitement des demandes d’accès ou de suppression des données.

Les outils d’administration et de confidentialité garantissent la protection de l’intégrité des données et le respect de toutes les politiques juridiques et organisationnelles.

**Composants clés** :
- **Gestion des utilisateurs et des accès** : contrôlez l’accès et les autorisations.
   - Exemple : attribuez des autorisations spécifiques aux équipes marketing et informatiques.
- **Configuration de sandbox** : environnements distincts pour le développement et les tests.
   - Exemple : utilisez un sandbox pour tester de nouvelles conceptions de parcours avant de les déployer en direct.
- **Configuration du canal** : configurez les paramètres techniques de la diffusion.
   - Exemple : configurer les détails du serveur de messagerie pour la messagerie de campagne.
- **Outils de confidentialité** : gérez les préférences de consentement et de confidentialité.
   - Exemple : gérez efficacement les demandes de suppression de données dans le cadre du RGPD (Règlement général sur la protection des données).
- **Contrôles de gouvernance** : application des politiques d’utilisation des données.

**Avantage** : garantit le fonctionnement sécurisé de la plateforme, la conformité aux réglementations et l’alignement sur les politiques organisationnelles.



## Connecter les points : comment tout cela fonctionne ensemble

Ces domaines fonctionnels fonctionnent dans un cycle continu pour offrir et optimiser des expériences client personnalisées :

1. **Ingestion des données** : flux de données dans AEP, structuré par la gestion des données.
2. **Compréhension du client** : les profils clients en temps réel unifient ces données, tandis que la gestion de la clientèle affine les informations par le biais des profils et des audiences.
3. **Stratégie de contenu et d’offre** : la gestion de contenu crée des messages et des ressources. La gestion des décisions définit les offres et la logique de sélection de la meilleure.
4. **Orchestration** : la gestion des Parcours cartographie les interactions entre les canaux, en tirant parti de la compréhension, du contenu et des décisions des clients.
5. **Diffusion** : les connexions facilitent la diffusion des messages par le biais de canaux choisis ou le partage de données avec des systèmes externes.
6. **Mesure et optimisation** : les données de performances et les interactions des clients alimentent les informations sur le système pour affiner les audiences, le contenu, les décisions et les parcours.
7. **Gouvernance** : les contrôles d’administration et de confidentialité garantissent la conformité et une configuration système appropriée.

Ce processus itératif permet aux entreprises d’apprendre et d’améliorer en permanence leurs stratégies d’engagement client.
