---
solution: Journey Optimizer
product: journey optimizer
title: Experimentation Accelerator
description: Utilisation des données dans l’IA avec Experimentation Accelerator
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: contenu, expérience, multiple, audience, traitement
hide: true
hidefromtoc: true
source-git-commit: 50dcdd30e21fe1b12d502a2b9c478f4ceb546c49
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 1%

---

# Utilisation des données dans l’IA avec Experimentation Accelerator{#experiment-accelerator-security}

>[!BEGINSHADEBOX]

* [Prise en main d’Experimentation Accelerator](experiment-accelerator.md)
* [Utilisation des données dans l’IA avec Experimentation Accelerator](experiment-accelerator-security.md)
* [Bonnes pratiques relatives à Experimentation Accelerator](experiment-accelerator-best-practices.md)
* [Surveiller les expériences](experiment-accelerator-monitor.md)
* [Mesures d’expérimentation](experiment-accelerator-metrics.md)

>[!ENDSHADEBOX]

**Adobe Journey Optimizer Experimentation Accelerator** vous permet de découvrir automatiquement des informations et de recommander des opportunités pour améliorer vos expériences et votre programme d’expérimentation. La solution tire parti de l’IA et du machine learning pour fournir ces recommandations. Cette instruction explique comment les données de vos clients sont utilisées dans **Experimentation Accelerator**.

## Quelles données l’accélérateur d’expérimentation utilise-t-il ?

Actuellement, il existe trois types de données utilisées par **l’accélérateur d’expérimentation** :

* **Métadonnées de l’expérience** : nom de l’expérience, définition de l’audience utilisée dans l’expérience et traitements dans l’expérience, par exemple nom, pourcentages de division, emplacement ou surface sur lequel l’expérience est diffusée.

* **Performance des traitements** : nombre de personnes, moyenne de la mesure de succès et écart type pour chaque traitement.

* **Contenu du traitement** : l’HTML rendue et la capture d’écran du traitement telle qu’elle apparaîtrait à un utilisateur ou une utilisatrice sur votre site web.

## Que fait l’accélérateur d’expérimentation avec ces données ?

L’**accélérateur d’expérimentation** prend le contenu de chaque traitement et crée une incorporation, c’est-à-dire une représentation mathématique du contenu, puis met en corrélation ces incorporations avec la performance des traitements. Ce processus permet l’extraction des attributs de contenu qui se sont révélés les plus performants en vue d’une utilisation ultérieure. Ces attributs sont ensuite intégrés à un modèle de langage volumineux hébergé par Adobe, qui les convertit en instructions lisibles par l’utilisateur, utilisées pour générer des informations et suggérer des opportunités.

## Quelles restrictions Experimentation Accelerator a-t-il sur les données utilisées ?

Chaque client est affecté à une organisation et à un sandbox spécifiques. Un modèle dédié est entraîné pour chaque sandbox. Lorsqu’un sandbox est supprimé, toutes les données, tous les signaux et tous les modèles associés sont définitivement supprimés.

* Nous utilisons uniquement les données client pour entraîner ou affiner le modèle de ce client.

* Nous ne mélangeons jamais les clients pour former ou affiner un modèle.

## Les modèles ou l’IA d’Adobe modifieront-ils automatiquement l’expérience utilisateur d’une marque ?

Non. **Experimentation Accelerator** ne fait que des recommandations sur ce qui peut être modifié et sur la manière de le faire. Seuls les utilisateurs autorisés à modifier l’expérience à l’aide de Journey Optimizer ou de Target pourront appliquer ces recommandations. Toutes les recommandations peuvent être examinées et modifiées avant d’être publiées.

## Existe-t-il un risque pour les données ou la stabilité du système ?

**Experimentation Accelerator** ingère et analyse uniquement les données, produisant des informations et des recommandations pour les tests futurs. Il ne dispose pas de l’accès nécessaire pour modifier les paramètres de test. Toutes les suggestions générées dans l’outil sont envoyées à Target et à Journey Optimizer pour mise en œuvre, ce qui n’a aucun impact sur les activités actuelles d’un client.
