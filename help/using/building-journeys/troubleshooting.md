---
solution: Journey Optimizer
product: journey optimizer
title: Résoudre les erreurs avant de tester ou de publier votre parcours
description: Découvrez comment résoudre les erreurs avant de tester ou de publier votre parcours.
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: dépannage, résolution des problèmes, parcours, vérification, erreurs
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DorhpVm3trSxHG-l77-DpwbLTNQQxET1SIMYX-8ClQc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 548
ht-degree: 87%

---

# Résoudre les erreurs avant de tester votre parcours {#troubleshooting}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment rechercher et corriger les erreurs de configuration d’activité et de parcours avant de tester ou de publier, afin que votre parcours puisse s’exécuter sans problème.

>[!ENDSHADEBOX]

Cette section décrit comment résoudre les problèmes liés aux parcours avant de les tester ou de les publier. Il est possible d&#39;effectuer les vérifications répertoriées ci-dessous lorsque le parcours est en mode test ou actif. Il est recommandé de les réaliser en mode test, puis d&#39;effectuer la publication. En savoir plus sur le mode test sur [cette page](../building-journeys/testing-the-journey.md).

Découvrez sur [cette page](troubleshooting-execution.md) comment résoudre les problèmes liés aux événements de parcours. Apprenez également comment vérifier si des profils ont rejoint votre parcours et la façon dont ils progressent dans celui-ci, et si des messages sont envoyés. Si aucun profil n’entre dans votre parcours basé sur un événement malgré l’ingestion d’événements, assurez-vous que les types de données de condition d’événement [&#x200B; correspondent au schéma d’événement](troubleshooting-execution.md#verify-event-identity-and-rule-data-types).

Si vous utilisez des actions entrantes, découvrez comment résoudre les problèmes liés à ces dernières [dans cette page](troubleshooting-inbound.md).

## Erreurs dans les activités {#activity-errors}

Avant de tester et de publier votre parcours, vérifiez que toutes les activités sont correctement configurées. Vous ne pouvez pas effectuer de tests ou de publications si des erreurs sont détectées par le système.

Les erreurs sont représentées par un symbole d&#39;avertissement, affiché sur l&#39;activité elle-même, dans la zone de travail. Placez le curseur sur le point d&#39;exclamation pour afficher le message d&#39;erreur. Si vous sélectionnez l’activité, vous devez voir la ligne contenant l’erreur accompagnée d’un avertissement. Par exemple :

* si un champ obligatoire est vide, une erreur s’affiche ;

  ![Erreurs de validation de parcours affichées dans la zone de travail avec des indicateurs d’erreur](assets/journey63.png)

* dans la zone de travail, un avertissement s’affiche lorsque deux activités sont déconnectées.

  ![Icône d’avertissement affichant les activités déconnectées dans la zone de travail du parcours](assets/canvas-disconnected.png)

## Erreurs dans le parcours {#canvas-errors}

Les erreurs sont également visibles à partir du bouton **[!UICONTROL Alertes]**, au-dessus de la zone de travail. Il indique les erreurs détectées par le système et qui empêchent l’activation du mode test ou la publication du parcours.

Le système détecte deux types de problèmes : les **erreurs** et les **avertissements**. Les erreurs bloquent la publication et l&#39;activation des tests. Les avertissements indiquent des problèmes potentiels qui ne bloquent pas l&#39;activation ou la publication des tests. Vous verrez une description du problème et un identifiant de journal des problèmes du type ERR_XXX_XXX. Cela peut aider à identifier le problème.

![Indicateurs d’erreur et d’avertissement dans le parcours avec info-bulles de description](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

Les erreurs et les avertissements globaux du parcours apparaissent en tête de liste. Les erreurs et les avertissements liés à des activités spécifiques sont répertoriés ensuite, par ordre d’activité ou d’apparition dans le parcours, de gauche à droite. Au bas de la liste des alertes, le bouton **[!UICONTROL Copier les détails]** permet de copier des informations techniques sur le parcours, utiles pour résoudre les problèmes. Pour obtenir la liste des champs copiés (y compris les informations de pause et de reprise), voir [Copier les détails techniques](journey-properties.md#access-properties) dans les propriétés du parcours.

## Ajouter un chemin d’accès alternatif {#canvas-add-path}

Vous pouvez définir une action de remplacement en cas d’erreur pour les activités de parcours suivantes : **[!UICONTROL Optimiser]** et **[!UICONTROL Action]**.

Lorsqu’une erreur se produit dans une action ou une condition, le parcours d’une personne s’arrête. La seule façon pour qu’il continue consiste à résoudre le problème. Pour éviter d’interrompre le parcours, vous pouvez également cocher l’option **[!UICONTROL Ajouter un chemin alternatif en cas de temporisation ou d’erreur]** dans les propriétés de l’activité. En savoir plus dans [cette section](../building-journeys/using-the-journey-designer.md#paths).
