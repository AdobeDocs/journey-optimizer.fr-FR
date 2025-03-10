---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Changement de dimension
description: Découvrir comment utiliser l’activité « Changement de dimension »
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 67%

---

# Changement de dimension {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Générer un complément"
>abstract="Vous pouvez générer une transition sortante supplémentaire avec la population restante, qui a été exclue en tant que doublon. Pour ce faire, activez l’option **Générer un complément**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Activité Changement de dimension"
>abstract="Cette activité vous permet de modifier la dimension de ciblage à mesure que vous créez une audience. Elle déplace l’axe en fonction du modèle de données et de la dimension d’entrée. Par exemple, vous pouvez passer de la dimension « contrats » à la dimension « clientèle »."

L’activité **Changement de dimension** est une activité de **ciblage**. Cette activité permet de modifier la dimension de ciblage au fur et à mesure que vous créez votre campagne à plusieurs étapes. Il déplace l’axe en fonction du modèle de données et de la dimension d’entrée.

Par exemple, vous pouvez basculer la dimension de ciblage d’une campagne à plusieurs étapes de « Destinataires » vers « Application des abonnés » afin d’envoyer des notifications push aux destinataires ciblés.

>[!IMPORTANT]
>
>Notez que les activités **[!UICONTROL Changer la dimension]** et **[!UICONTROL Modifier la source de données]** ne doivent pas être ajoutées sur une même ligne. Si vous devez utiliser les deux activités consécutivement, veillez à inclure une activité **[!UICONTROL Enrichissement]** entre les deux. Cela garantit une bonne exécution et évite les erreurs et conflits potentiels.

## Configurer l’activité Changement de dimension {#configure}

Pour configurer l’activité **Changement de dimension**, procédez comme suit :

1. Ajoutez une activité **Modifier la dimension** à votre campagne à plusieurs étapes.

   ![](../assets/workflow-change-dimension.png)

1. Définissez la **Nouvelle dimension cible**. Lors du changement de dimension, tous les enregistrements sont conservés. D’autres options ne sont pas encore disponibles.

1. Exécutez la campagne à plusieurs étapes pour afficher le résultat. Comparez les données dans les tables avant et après l’activité de changement de dimension, et comparez la structure des tables de campagne à plusieurs étapes.

## Exemple {#example}

Dans cet exemple, nous souhaitons envoyer une diffusion SMS à tous les profils ayant effectué un achat. Pour ce faire, nous utilisons d’abord une activité **[!UICONTROL Créer une audience]** liée à une dimension de ciblage « Achat » personnalisée pour cibler tous les achats qui se sont produits.

Nous utilisons ensuite une activité **[!UICONTROL Modifier la dimension]** pour basculer la dimension de ciblage de campagne à plusieurs étapes vers « Destinataires ». Cela nous permet de cibler les personnes destinataires qui correspondent à la requête.

![](../assets/workflow-change-dimension-example.png)
