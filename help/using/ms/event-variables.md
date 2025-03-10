---
solution: Journey Optimizer
product: journey optimizer
title: Variables d’événement de campagne à plusieurs étapes
description: Découvrez comment exploiter les variables d’événement dans vos campagnes à plusieurs étapes
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 64%

---

# Variables d’événement de campagne à plusieurs étapes {#event-variables}

Certaines activités de campagne à plusieurs étapes vous permettent de modifier des scripts dans l’éditeur d’expression afin d’effectuer des actions spécifiques, telles que la récupération de données provenant d’activités précédentes, la création de conditions ou le calcul de noms de fichier en fonction de variables d’événement.

## Que sont les variables d’événement ? {#scripting}

Les scripts exécutés dans le cadre d’une campagne à plusieurs étapes accèdent à une série d’**objets** globaux supplémentaires, tels que la campagne à plusieurs étapes elle-même en cours d’exécution (`ìnstance`), ses différentes tâches (`task`) ou les événements qui ont activé une tâche donnée (`event`).

Pour chaque type d’**objet** est associé à une catégorie de **variables** qui peuvent être utilisées dans l’éditeur d’expression lors de la modification de scripts dans des activités telles que le **[!UICONTROL code JavaScript]** ou le **[!UICONTROL test]**.

* Les **variables d’instance** (`instance.vars.xxx`) sont comparables à des variables globales. Elles sont partagées par toutes les activités.
* Les **variables de tâche** (`task.vars.xxx`) sont comparables à des variables locales. Elles ne sont utilisées que par la tâche en cours. Ces variables sont utilisées par des activités persistantes pour conserver des données et sont parfois utilisées pour échanger des données entre les différents scripts d’une même activité.
* **Les variables d’événement** (`vars.xxx`) permettent l’échange de données entre les tâches élémentaires d’un processus de campagne à plusieurs étapes. Ces variables sont transmises par la tâche qui a activé la tâche en cours. Elles sont ensuite transmises aux activités suivantes. Les **variables d’événement** sont les variables les plus communément utilisées et doivent être préférées aux variables d’instance.

## Utiliser des variables d’événement dans l’éditeur d’expression {#expression-editor}

Les variables d’événement prédéfinies peuvent être utilisées dans le volet de gauche de l’éditeur d’expression. Vous pouvez également en créer de nouvelles en initialisant une nouvelle variable dans votre code.

![](assets/event-variables.png)

Outre ces variables d’événement, vous pouvez également utiliser le menu **[!UICONTROL Conditions]** dans le volet de gauche pour créer des conditions et le menu **[!UICONTROL Ajouter la date actuelle]** pour utiliser les fonctions liées au formatage des dates.
