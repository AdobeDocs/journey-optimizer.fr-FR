---
solution: Journey Optimizer
product: journey optimizer
title: Terminologie clé
description: Terminologie clé dans AJO
feature: Get Started
role: Admin, Data Engineer, Developer, User
level: Beginner
redpen-status: PASS_||_2025-04-28_15-13-07
exl-id: d4c968d2-5eae-4fff-9b67-427ac9d9d74c
hide: true
source-git-commit: f94067ffb421bfd095ed3fcb3001af0e5dc44ab3
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 3%

---

# Terminologie

Bienvenue dans le guide terminologique de Adobe Journey Optimizer. Cette ressource fournit des définitions claires et simples des termes clés que vous rencontrez lors de l’utilisation de la plateforme. La compréhension de ces termes vous permet de naviguer dans Adobe Journey Optimizer en toute confiance, d’implémenter des stratégies marketing efficacement et de collaborer efficacement avec les membres de l’équipe et l’assistance d’Adobe.

## Termes de la plateforme principale

| Terme | Définition |
|------|------------|
| **Adobe Journey Optimizer (AJO)** | Outil permettant de créer et d’envoyer des messages personnalisés à des clients sur plusieurs canaux, tels que des e-mails, des SMS et des notifications d’applications mobiles. Il vous permet de concevoir des parcours clients qui répondent aux actions des clients en temps réel. Par exemple, un e-mail de confirmation se déclenche immédiatement après qu’un client a effectué un achat sur votre site web. |
| **Adobe Experience Platform (AEP)** | Les bases de Adobe Journey Optimizer. Il collecte et organise toutes les données client à un seul endroit, créant ainsi des profils client complets que Adobe Journey Optimizer utilise pour envoyer des messages personnalisés. Considérez AEP comme le hub central qui génère les stratégies d’engagement des clients. |
| **Sandbox** | Un espace de travail distinct où vous testez et testez sans affecter les communications client en direct. Un sandbox fonctionne comme une zone d’exercices ou un environnement de test. Adobe Journey Optimizer fournit jusqu’à cinq sandbox, ce qui permet aux équipes de tester des scénarios tels que des parcours d’intégration ou des campagnes promotionnelles. |

## Conditions de parcours et de campagne

| Terme | Définition |
|------|------------|
| **Parcours** | Une série d&#39;étapes connectées qui guident les clients à travers les expériences avec votre marque. Par exemple, un parcours de bienvenue comprend un e-mail de bienvenue, un rappel de téléchargement d’application et des recommandations de produits personnalisées. Chaque étape se produit une fois la précédente terminée, ce qui permet des interactions séquentielles et personnalisées. |
| **Campaign** | Une communication unique ou un ensemble de communications identiques envoyées simultanément à un groupe spécifique de clients et clientes. Contrairement aux parcours, qui se déploient au fil du temps, les campagnes diffusent des messages simultanément, immédiatement ou à un moment planifié. Par exemple, vous pouvez planifier une campagne promotionnelle par e-mail pour une vente de week-end. |
| **Canal** | Méthode utilisée pour communiquer avec les clients et clientes, comme des e-mails, des SMS, des notifications push (alertes d’applications mobiles), des messages in-app ou des sites web. Chaque canal nécessite une configuration spécifique, telle que la vérification d’un domaine de messagerie ou la connexion d’un fournisseur SMS. |
| **Message** | Contenu envoyé aux clients et aux clientes, y compris du texte, des images et des éléments personnalisés. Vous créez des messages pour différents formats, tels que les e-mails, les SMS et les notifications push. Par exemple, un message peut être un e-mail de remerciement contenant des noms de client et des détails de commande insérés dynamiquement. |
| **Événement** | Une occurrence qui déclenche ou fait avancer un parcours. Les événements incluent les actions du client, telles qu’un achat, ou des événements système, tels qu’une nouvelle inscription du client. Les événements permettent aux parcours de répondre aux actions des clients en temps réel. Par exemple, l’anniversaire d’un client déclenche un e-mail de remise spéciale. |

## Termes du client et de l’audience

| Terme | Définition |
|------|------------|
| **Profile** | Une vue complète de chaque client qui combine des informations telles que les coordonnées, l’historique des achats, les préférences et les comportements. Un « profil engageable » fait référence à un client contacté à l’aide de Adobe Journey Optimizer au cours des 12 derniers mois. Les profils sont essentiels à la création d’expériences personnalisées basées sur les données. |
| **Audience** | Groupe de clients et clientes qui partagent des caractéristiques ou des comportements communs. Par exemple, « clients ayant acheté au cours des 30 derniers jours » ou « clients intéressés par des produits d’extérieur ». Les audiences sont créées dans Adobe Experience Platform et utilisées dans Adobe Journey Optimizer pour cibler des segments spécifiques. |
| **Qualification de l’audience** | Processus qui se produit lorsqu’un client rejoint ou quitte une audience. Adobe Journey Optimizer déclenche automatiquement des actions lorsqu’une personne entre ou quitte une audience. Par exemple, il envoie un message de bienvenue aux nouveaux membres du programme de fidélité, en assurant des communications opportunes et pertinentes. |
| **Audience adressable** | Nombre total de profils client que vous pouvez potentiellement atteindre. Votre compte permet d’atteindre une audience adressable 25 % plus importante que votre audience engageable sous contrat, offrant ainsi une flexibilité à mesure que votre base de clients se développe. |
| **Audience Modifiable** | Nombre de clients avec lesquels vous communiquez activement par le biais de Adobe Journey Optimizer en fonction de votre contrat. Cela vous permet de respecter les limites de licence tout en vous concentrant sur les interactions à forte valeur ajoutée. |
| **Définition de segment** | Les règles qui déterminent quels clients appartiennent à une audience. Ces règles sont basées sur des attributs, des comportements ou d’autres critères. Par exemple, une définition de segment peut inclure « clients ayant dépensé plus de 500 $ au cours des six derniers mois ». |

## Termes de gestion des décisions

| Terme | Définition |
|------|------------|
| **Gestion des décisions** | Une fonctionnalité qui sélectionne automatiquement le meilleur contenu ou la meilleure offre pour chaque client. Par exemple, il recommande une offre de livraison gratuite à un client qui abandonne fréquemment son panier. Cela garantit des interactions personnalisées et pertinentes. |
| **Offre** | Message ou promotion marketing spécifique présenté aux clients. Par exemple, une remise de 20 %, une offre de livraison gratuite ou une recommandation de produit. Adobe Journey Optimizer comprend jusqu’à 10 offres par e-mail, ce qui permet d’obtenir un contenu diversifié et personnalisé. |
| **API Decisioning** | Connexion technique qui permet à d’autres systèmes de demander à Adobe Journey Optimizer : « Quelle est la meilleure offre pour ce client en ce moment ? » L’offre sélectionnée s’affiche sur des sites web, des applications ou d’autres canaux. Cette intégration étend les fonctionnalités de Journey Optimizer au-delà des e-mails et des SMS. |
| **Bibliothèque des offres** | Une collection centralisée où toutes les offres marketing sont stockées et gérées. Cela garantit la cohérence entre les canaux et simplifie les mises à jour des stratégies promotionnelles. |
| **Règles d’éligibilité** | Conditions qui déterminent si un client peut recevoir une offre particulière. Par exemple, « Afficher cette remise uniquement aux clients qui n’ont pas effectué d’achats depuis 60 jours ». Ces règles permettent d’éviter les messages excessifs ou les offres non pertinentes. |

## Données et termes techniques

| Terme | Définition |
|------|------------|
| **Zone d’atterrissage des données** | Zone de stockage temporaire dans laquelle vous placez les fichiers de données avant de les déplacer dans Adobe Experience Platform. Considérez-la comme une zone de transit pour vos données. Par exemple, vous téléchargez ici un fichier CSV des transactions client avant de l’intégrer dans le système. |
| **Query Service** | Outil permettant d’exécuter des requêtes de style base de données pour valider les données importées dans Adobe Journey Optimizer. Par exemple, vous demandez « Combien de clients se sont inscrits la semaine dernière ? » pour garantir la précision de la segmentation de l’audience. |
| **Attribut calculé** | Une caractéristique client calculée à partir de son comportement. Par exemple, « valeur d’achat moyenne » ou « nombre total de visites sur le site web ce mois-ci ». Ces attributs vous permettent de personnaliser les messages en fonction des schémas des clients, par exemple en ciblant des clients à forte valeur ajoutée avec des offres exclusives. |
| **Champs de personnalisation** | Des espaces réservés dans les messages qui sont remplacés par des informations spécifiques au client, telles que le prénom, les achats récents ou le niveau d’abonnement. Adobe Journey Optimizer prend en charge jusqu’à cinq champs de personnalisation par message. Par exemple, « Bonjour [Prénom], votre récent achat de [Nom du produit] est en cours ! » |
| **Schéma** | Plan directeur définissant l’organisation des données client. Il mappe les types d&#39;informations stockées et leurs relations. Un schéma clair garantit une intégration transparente et une utilisation précise des données dans les workflows. |
| **Jeu de données** | Ensemble de données associées organisées selon un schéma. Par exemple, vous pouvez avoir des jeux de données distincts pour l’historique des achats, l’activité du site web et les interactions du service client. Ces jeux de données vous permettent d’analyser et d’agir sur différents aspects du comportement des clients et clientes. |

## Termes du contenu et des ressources

| Terme | Définition |
|------|------------|
| **Assistant IA** | Une fonctionnalité intégrée qui utilise l’intelligence artificielle pour créer du contenu. Il génère du texte, crée des e-mails ou crée des variations de message pour différents canaux. Par exemple, vous lui demandez de rédiger un e-mail promotionnel en fonction des préférences de l’audience. |
| **Assets Essentials** | Bibliothèque incluse avec Adobe Journey Optimizer pour stocker et gérer des fichiers numériques tels que des images, des logos et des documents. Il comprend un stockage pour les ressources marketing et prend en charge jusqu’à cinq utilisateurs avec des autorisations complètes et 100 utilisateurs avec un accès en affichage. Cela simplifie la collaboration et assure la cohérence de la marque. |
| **Fragment de contenu** | Un élément de contenu réutilisable utilisé dans plusieurs messages. Par exemple, un pied de page standard avec des informations de contact qui s’affiche dans tous les e-mails. Cela garantit la cohérence et réduit le temps passé à recréer les éléments partagés. |
| **Modèle** | Une disposition de message préconçue et personnalisée avec un contenu spécifique. Les modèles permettent de maintenir une apparence cohérente dans toutes les communications, telles que les conceptions d’e-mail de marque ou les formats de SMS. |

## Termes de Reporting &amp; Analysis

| Terme | Définition |
|------|------------|
| **Rapport global** | Présentation complète montrant les performances de tous les parcours et campagnes. Cela vous permet de comprendre les tendances des taux d’engagement sur l’ensemble des canaux et d’évaluer l’efficacité marketing globale. |
| **Rapport dynamique** | Données en temps réel sur les parcours et campagnes en cours d’exécution. Cela permet des ajustements immédiats si nécessaire. Par exemple, vous mettez en pause une campagne avec un faible engagement et révisez son message. |
| **Rapport de Parcours** | Informations détaillées sur les performances d’un parcours spécifique. Il montre comment les clients passent par chaque étape et identifie où ils peuvent abandonner. Cela permet d’optimiser les expériences client. |
| **Rapport des messages** | Statistiques sur un message spécifique, telles que le nombre de messages diffusés, ouverts et sur lesquels l’utilisateur a cliqué. Ces informations permettent d’affiner les futures communications en montrant comment les clients réagissent à votre contenu. |

## Documentation connexe

* [Prise en main de Adobe Journey Optimizer](get-started.md)
* [Architecture et concepts](architecture-concepts-redpen.md)
* [Guide des domaines fonctionnels](functional-areas-redpen.md)
