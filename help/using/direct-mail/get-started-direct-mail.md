---
title: Prise en main du courrier
description: Découvrez comment créer un message et un courrier dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: courrier, message, campagne
source-git-commit: 40cd058475b37b8fa7d5c0286ad230422e027cf8
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 49%

---

# Créer un message de publipostage direct {#create-direct}

>[!AVAILABILITY]
>
>Pour l’instant, le canal Courrier n’est pas disponible pour les organisations qui ont acheté l’offre complémentaire Bouclier de santé Adobe.

Le publipostage direct est un canal hors ligne qui vous permet de personnaliser et de générer les fichiers d’extraction requis par les fournisseurs de publipostage direct pour envoyer du courrier à votre clientèle.

Lors de la création d’une campagne courrier, Journey Optimizer génère automatiquement un fichier contenant tous les profils ciblés et les données sélectionnées, telles que les adresses postales et les attributs de profil. Ce fichier est envoyé au serveur de votre choix afin qu’il soit accessible par le prestataire de services postaux de votre choix, qui gérera le processus de diffusion réel pour vous.

Les principales étapes pour envoyer des messages postaux sont les suivantes :

![](assets/dm-creation-process.png)

Les messages de publipostage direct ne peuvent être créés que dans le cadre de campagnes planifiées. Ils ne sont pas disponibles pour une utilisation dans des campagnes déclenchées par l’API ou dans des parcours.

>[!IMPORTANT]
>
>Avant d’envoyer un message de publipostage direct, assurez-vous d’avoir configuré les éléments suivants :
>
>1. Une [configuration du routage des fichiers](../direct-mail/direct-mail-configuration.md#file-routing-configuration) qui spécifie le serveur sur lequel le fichier d’extraction doit être téléchargé et stocké,
>1. Une [surface de message de publipostage direct](../direct-mail/direct-mail-configuration.md#direct-mail-surface) qui fera référence à la configuration du routage des fichiers.
