---
solution: Journey Optimizer
product: journey optimizer
title: Zones fonctionnelles
description: Zones fonctionnelles dans AJO
feature: Get Started
role: Admin, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: c9b02ae2-e07b-41f4-90cc-b2c0966f1ed1
hide: true
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '1448'
ht-degree: 100%

---

# Concepts de base

Adobe Journey Optimizer (AJO) comprend plusieurs zones fonctionnelles clés qui opèrent de manière parfaitement intégrée. Ce guide présente chaque zone et décrit comment elles se combinent pour créer des expériences client à fort impact. Comprendre ces zones fonctionnelles permet d’exploiter AJO pour proposer efficacement des expériences personnalisées et omnicanales.

## Vue d’ensemble des zones fonctionnelles

| Zone fonctionnelle | Bénéfice principal | Analogie |
|-------------------------|--------------------------------------------------|------------------------|
| Gestion des données | Organiser des données client pertinentes | La base |
| Gestion des clientes et clients | Comprendre qui est la clientèle | Connaître l’audience |
| Gestion de contenu | Créer et gérer des messages cohérents et personnalisés | Concevoir le message |
| Gestion des décisions | Sélectionner en temps réel le message ou l’offre les plus adaptés | Le moteur |
| Gestion des parcours | Concevoir et automatiser des expériences client fluides | Chef d’orchestre |
| Connexions | Connecter les sources de données et effectuer la diffusion via les canaux client | Infrastructure technique |
| Administration et confidentialité | Contrôler la configuration, l’accès et garantir la conformité des données | Le règlement |

## Zones fonctionnelles détaillées

### Gestion des données : la base

**Objectif** : ingérer, structurer et gérer les données qui alimentent la personnalisation. Ce processus inclut la définition des structures de données (schémas), la création de conteneurs de stockage (jeux de données) et l’import de données depuis divers systèmes.

Considérez la gestion des données comme le socle de l’engagement client. Une base de données bien structurée garantit que chaque décision, message et parcours s’appuie sur des informations exactes et organisées.

**Composants clés** :

- **Création et gestion des schémas** : définissez la structure des données client.
   - Exemple : créez un schéma décrivant des champs tels que « Prénom », « Adresse électronique » et « Historique des achats ».
- **Configuration du jeu de données** : organisez les données en conteneurs logiques.
   - Exemple : regroupez les données de transaction dans un jeu de données « Transactions de vente » pour une analyse plus facile.
- **Workflows d’ingestion de données** : importez efficacement des données dans la plateforme.
   - Exemple : utilisez des connecteurs Source préconfigurés pour importer des données client depuis un système de gestion de la relation client (CRM).
- **Outils de qualité des données** : maintenez l’exactitude et l’exhaustivité des données.

**Bénéfice** : des données client fiables, organisées et accessibles, constituant la base de toutes les activités AJO. Les connecteurs Source préconfigurés simplifient l’ingestion de données depuis les plateformes courantes.



### Gestion des clients : connaître l’audience

**Objectif** : développer et maintenir une compréhension approfondie de chaque client ou cliente. Cela implique d’utiliser le profil client en temps réel d’Adobe Experience Platform (AEP) pour fusionner les données issues de tous les points de contact dans une vue unifiée. Elle gère également les identités sur les appareils et les canaux, ce qui permet de regrouper des individus en Audiences faciles à cibler selon des attributs ou des comportements communs.

Les outils de gestion de la clientèle relient des points de données disparates pour offrir une vue cohérente de chaque client ou cliente. Cette compréhension garantit la capacité de proposer des expériences pertinentes et personnalisées.

**Composants clés** :

- **Profil client en temps réel** : vue unifiée de chaque client ou cliente.
   - Exemple : combinez l’historique de navigation web, les interactions dans les applications et les achats hors ligne au sein d’un seul profil.
- **Résolution d’identité** : liez les données des clients ou des clientes sur différents appareils et canaux.
   - Exemple : faites correspondre l’adresse e-mail d’un client ou d’une cliente avec ses données d’usage d’application grâce à Identity Graph.
- **Création et gestion d’audiences** : définissez des groupes en fonction des attributs et des comportements.
   - Exemple : créez une audience « Clientèle fidèle » regroupant les personnes ayant effectué plus de cinq achats au cours de l’année écoulée.
- **Segmentation** : appliquez des règles d’appartenance dynamique à une audience.
   - Exemple : configurez un segment « Acheteurs à forte valeur » qui se met à jour automatiquement lorsque les clients ou clientes dépensent plus de 500 $.

**Bénéfice** : permet un ciblage et une personnalisation précis grâce à une compréhension dynamique des préférences individuelles, de l’historique et des appartenances à des segments.



### Gestion de contenu : concevoir le message

**Objectif** : créer, gérer, personnaliser et réutiliser du contenu marketing sur plusieurs canaux. Cela inclut la gestion des ressources numériques, la création de messages avec éditeurs visuels ou code, l’utilisation de modèles et de fragments réutilisables, la création de pages de destination et le recours à l’intelligence artificielle (IA) pour la génération de contenu.

Les outils de gestion de contenu permettent aux équipes de créer et de diffuser efficacement des messages adaptés, en maintenant cohérence et pertinence sur chaque point de contact.

**Composants clés** :

- **Éditeurs de contenu** : créez et formatez des messages visuellement ou à l’aide de code.
   - Exemple : utilisez l’éditeur visuel pour concevoir une campagne par e-mail promouvant les ventes de fin d’année.
- **Gestion des ressources numériques** : organisez et utilisez des images et d’autres médias.
   - Exemple : stockez les images produits dans une bibliothèque centralisée pour une réutilisation aisée dans les campagnes.
- **Modèles et fragments** : créez des composants de contenu réutilisables.
   - Exemple : créez un modèle « Message de bienvenue » qui insère dynamiquement les noms des clients ou clientes.
- **Outils de personnalisation** : personnalisez dynamiquement le contenu pour chaque individu.
   - Exemple : affichez des recommandations de produits personnalisées en fonction de l’historique de navigation.
- **Créateur de pages de destination** : créez des destinations web pour les campagnes.

**Bénéfice** : rationalise la création de contenu, garantit la cohérence de marque et facilite la diffusion efficace de messages hautement personnalisés.



### Gestion des décisions : le moteur de la personnalisation.

**Objectif** : sélectionner le meilleur message ou la meilleure offre pour chaque client ou cliente au moment opportun, selon le profil en temps réel, le contexte et des règles métier ou modèles d’IA prédéfinis. La gestion des décisions consiste à administrer une bibliothèque centrale d’offres, définir des règles d’éligibilité, appliquer des contraintes (comme le capping de la fréquence) et établir une logique de classement.

La gestion des décisions veille à ce que la personnalisation fonctionne à l’échelle en apportant une valeur maximale grâce à l’automatisation intelligente.

**Composants clés** :

- **Bibliothèque des offres** : référentiel central des offres marketing.
   - Exemple : stockez des offres telles que « coupon de 20 % de réduction » ou « Livraison gratuite » dans une bibliothèque partagée.
- **Règles de décision** :logique permettant de sélectionner le contenu optimal.
   - Exemple : affichez une « remise fidélité » uniquement aux clients ou aux clientes du segment « Clientèle fidèle ».
- **Contraintes et éligibilité** : contrôlez qui reçoit quoi et quand.
   - Exemple : appliquez un capping de la fréquence afin d’empêcher un client ou une cliente de recevoir deux fois la même offre en une semaine.
- **Stratégies de classement** : hiérarchisez les offres en fonction des objectifs commerciaux ou de l’IA.
   - Exemple : classez les offres par rentabilité, en commençant par les produits à marge élevée.
- **Outils de simulation** : testez et validez des stratégies de décision.

**Bénéfice** : automatise et optimise la personnalisation afin de garantir que des expériences pertinentes et percutantes soient proposées à chaque point de contact.



### Gestion des parcours : le chef d’orchestre

**Objectif** : concevoir, orchestrer et automatiser des expériences client sur plusieurs étapes et canaux. Les parcours réagissent en temps réel aux comportements et événements des clients ou des clientes, en orientant les individus tout au long de parcours personnalisés. AJO prend également en charge les campagnes permettant de diffuser des messages planifiés et ponctuels à des audiences spécifiques.

La gestion des parcours permet de s’assurer que les expériences sont adaptatives et transparentes, en guidant les individus en fonction de leurs préférences et de leurs actions.

**Composants clés** :

- **Concepteur de parcours** : zone de travail visuelle pour la création de chemins d’accès client.
   - Exemple : concevez un parcours qui envoie un e-mail de bienvenue lorsqu’un client ou une cliente s’inscrit.
- **Déclencheurs de parcours** : événements qui initient ou font progresser les parcours.
   - Exemple : déclenchez un SMS de relance après qu’un client ou une cliente ait abandonné son panier.
- **Étapes de condition** : utilisez un branchement basé sur la logique.
   - Exemple : envoyez un message différent selon qu’un client ou une cliente ouvre un e-mail.
- **Activités d’attente** : contrôlez la progression à l’aide de délais temporels.
   - Exemple : patientez trois jours avant d’envoyer un e-mail de rappel.
- **Gestion de campagnes** : outils pour la diffusion de messages planifiés et ponctuels.

**Bénéfice** : crée des expériences fluides et connectées qui s’adaptent aux interactions individuelles, renforcent les relations et favorisent les résultats attendus.



### Connexions : infrastructure technique

**Objectif** : gérer le flux de données entrant dans AJO (Sources) et la diffusion des messages ou des données sortant d’AJO (Canaux et destinations). Les sources introduisent des données dans Adobe Experience Platform (AEP). Les canaux diffusent les messages (par e-mail, SMS, notification push, web, etc.). Les destinations permettent aux informations d’audience ou de jeu de données de circuler vers des plateformes externes.

Les connexions garantissent que les données intègrent AJO de manière efficace et atteignent les clients ou les clientes de façon fiable aux bons points de contact.

**Composants clés** :

- **Connecteurs Source** : importez les données dans la plateforme.
   - Exemple : utilisez un connecteur pour importer les données d’achat d’une plateforme d’e-commerce.
- **Configuration des canaux** : configurez et gérez les mécanismes de diffusion.
   - Exemple : configurez la diffusion par SMS pour les messages promotionnels.
- **Configuration de la destination** : connectez-vous à des systèmes d’activation externes.
   - Exemple : partagez des données d’audience avec une plateforme publicitaire de médias sociaux.
- **Gestion des flux de données** : contrôlez le déplacement des informations.

**Bénéfice** : garantit une ingestion efficace des données et une diffusion fiable des messages sur l’ensemble des canaux, tout en permettant l’activation dans les systèmes externes.



### Administration et confidentialité : le règlement

**Objectif** : configurer les paramètres du système, gérer l’accès et les autorisations des utilisateurs ou des utilisatrices, mettre en place les canaux de communication, définir les paramètres de parcours et garantir la conformité avec les règles de confidentialité et de gouvernance des données. Cela inclut la gestion du consentement, l’application des règles d’utilisation des données et le traitement des demandes d’accès ou de suppression des données.

Les outils d’administration et de confidentialité garantissent la protection de l’intégrité des données et le respect de toutes les politiques juridiques et organisationnelles.

**Composants clés** :

- **Gestion des utilisateurs et des utilisatrices et des accès** : contrôlez l’accès et les autorisations.
   - Exemple : attribuez des autorisations spécifiques aux équipes marketing et informatiques.
- **Configuration des sandbox** : séparez les environnements de développement et de test.
   - Exemple : utilisez un sandbox pour tester de nouveaux parcours avant leur mise en production.
- **Configuration des canaux** : configurez les paramètres techniques pour la diffusion.
   - Exemple : configurez les paramètres du serveur de messagerie électronique pour les messages des campagnes.
- **Outils de confidentialité** : gérez le consentement et les préférences de confidentialité.
   - Exemple :traitez efficacement les demandes de suppression de données au titre du RGPD (Règlement général sur la protection des données).
- **Contrôles de la gouvernance** : appliquez les règles d’utilisation des données.

**Bénéfice** : garantit un fonctionnement sécurisé de la plateforme, la conformité avec les réglementations et l’alignement avec les politiques organisationnelles.



## Connecter les points : fonctionnement global

Ces domaines fonctionnels opèrent dans un cycle continu afin de proposer et d’optimiser des expériences personnalisées pour les clients ou les clientes.

1. **Ingestion de données** : les données circulent vers AEP et sont structurées par la gestion des données.
2. **Compréhension client** : les profils client en temps réel unifient ces données, tandis que la gestion client affine les informations via les profils et les audiences.
3. **Stratégie de contenu et d’offre** : la gestion de contenu crée des messages et des ressources. La gestion des décisions définit les offres et la logique de sélection de la meilleure d’entre elles.
4. **Orchestration** : la gestion des parcours cartographie les interactions sur l’ensemble des canaux, en s’appuyant sur la compréhension client, le contenu et les décisions.
5. **Diffusion** : les connexions facilitent la diffusion des messages via les canaux choisis ou le partage de données avec des systèmes externes.
6. **Mesures et optimisation** : les données de performance et les interactions des clients ou des clientes alimentent le système en données afin d’affiner les audiences, le contenu, les décisions et les parcours.
7. **Gouvernance** : les contrôles d’administration et de confidentialité garantissent la conformité et une configuration système appropriée.

Ce processus itératif permet aux entreprises d’apprendre et d’améliorer en permanence leurs stratégies d’engagement client.
