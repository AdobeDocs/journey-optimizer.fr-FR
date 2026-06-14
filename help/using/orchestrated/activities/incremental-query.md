---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité de requête incrémentale
description: Découvrez comment utiliser l’activité de Requête incrémentale dans Adobe Journey Optimizer pour cibler uniquement les nouveaux profils dans les campagnes orchestrées.
feature: Campaigns
topic: Building campaigns
role: User
level: Intermediate
version: Campaign Orchestration
feature_v2: 
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: cda41058be1eb26538f4b0ef8c7b6c3f1c01eccd
workflow-type: tm+mt
source-wordcount: 547
ht-degree: 22%

---


# Requête incrémentale {#incremental-query}

>[!BEGINSHADEBOX]

**Sur cette page :** Découvrez comment utiliser l&#39;activité de ciblage de requête incrémentale pour renvoyer uniquement les nouveaux enregistrements sur chaque exécution de campagne orchestrée, à l&#39;exclusion des profils déjà ciblés dans les exécutions précédentes.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery"
>title="Requête incrémentale"
>abstract="La requête incrémentale est une activité de ciblage qui exécute une requête de base de données à chaque exécution de la campagne orchestrée. Il renvoie uniquement les nouveaux enregistrements et exclut tous ceux déjà inclus dans une exécution précédente, afin d’éviter de recibler les mêmes personnes ou de réexporter les mêmes lignes."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery_processeddata"
>title="Données traitées"
>abstract="Sous Données traitées, choisissez comment exclure les enregistrements des exécutions précédentes. Avec l’option Utiliser un champ de date, l’activité utilise un champ de date sélectionné au lieu d’effectuer le suivi d’identifiants individuels et chaque exécution renvoie uniquement les lignes dont la date est postérieure à la dernière exécution."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_incrementalquery_history"
>title="Jours d’historique"
>abstract="Ce paramètre contrôle la durée de conservation de cette liste. Une valeur égale à 0 signifie une conservation indéfinie. Aucun enregistrement n’est supprimé."

L&#39;activité **[!UICONTROL Requête incrémentale]** est une activité **[!UICONTROL Ciblage]** qui exécute une requête de base de données à chaque exécution de la campagne orchestrée. L’important est qu’il ne génère que des **nouveaux** enregistrements. Toute personne déjà récupérée au cours d’une exécution précédente est exclue, ce qui vous évite de recibler les mêmes personnes ou de réexporter les mêmes lignes.

Utilisez-la lorsque la campagne peut s’exécuter plusieurs fois, par exemple lorsque vous planifiez la campagne, par exemple une fois par semaine ou lorsqu’elle est déclenchée par un signal externe ou une API. Chaque exécution cible uniquement les enregistrements qui n’ont pas été renvoyés lors d’une exécution précédente, afin d’éviter les doublons.

Utilisations standard :

* **Messages et audiences** : extrayez uniquement les nouvelles inscriptions, les nouveaux acheteurs ou d’autres segments « nouveau depuis la dernière exécution » dans l’étape suivante (par exemple, e-mail, SMS).
* **Exportations en cours** : envoyez uniquement des lignes nouvelles ou mises à jour aux fichiers pour les outils de création de rapports ou de BI, sans dupliquer ce que vous avez déjà exporté.

Lorsqu’une exécution ne renvoie aucune ligne, la campagne orchestrée s’arrête à la **requête incrémentale**. Les activités après la requête incrémentale ne sont pas exécutées tant qu’il n’y a pas de données, lorsque la campagne s’exécute à nouveau.

## Configurer l’activité Requête incrémentale {#incremental-query-configuration}

Définissez la dimension de ciblage, créez votre requête et choisissez comment l’activité décide des enregistrements à exclure des exécutions futures.

1. Déposez une activité **[!UICONTROL Requête incrémentale]** dans votre campagne orchestrée.

1. Dans **[!UICONTROL Audience]**, choisissez la **[!UICONTROL dimension de ciblage]** par exemple, destinataires, abonnés, puis cliquez sur **[!UICONTROL Continuer]**. En savoir plus sur [Dimensions de ciblage](../target-dimension.md).

   ![](../assets/incremental-query.png)

1. Cliquez sur **[!UICONTROL Ajouter une condition]** pour définir la requête. [Découvrez comment utiliser le créateur de règles](../orchestrated-rule-builder.md).

   ![](../assets/incremental-query-2.png)

1. Sous **[!UICONTROL Données traitées]**, choisissez votre **[!UICONTROL Chemin d’accès au champ de date]**. L’attribut doit utiliser le format **Date et heure**. Chaque exécution renvoie uniquement les lignes dont la date est postérieure à la dernière exécution.

   ![Configuration de l’activité de requête incrémentale dans la zone de travail de campagne orchestrée](../assets/incremental-query-3.png)

<!--
   * **[!UICONTROL Exclude results of previous execution]**: The activity maintains a list of records returned in prior runs. Each run excludes those records and returns only new ones. **[!UICONTROL History in days]** controls the retention period for that list. 0 indicates indefinite retention, no records are removed.

   >[!IMPORTANT]
   >
   >This mode stores the primary key of each processed record. Personally identifiable information (PII) must not be used as the primary key.

-->

## Exemple {#incremental-query-example}

L’exemple suivant envoie un e-mail de bienvenue aux profils qui viennent de devenir membres Gold. La campagne peut être planifiée pour s’exécuter toutes les semaines, tous les lundis. Chaque exécution cible uniquement les profils qualifiés pour l’adhésion Gold depuis l’exécution précédente. Chaque destinataire reçoit donc l’e-mail de bienvenue une fois.

* **[!UICONTROL Requête incrémentale]** : sélectionne des membres Gold. Première exécution : tous les membres Gold actuels. Exécutions ultérieures : uniquement les profils qui sont devenus membres Gold depuis l’exécution précédente.
* **[!UICONTROL Diffusion Email]** : envoie l&#39;email de bienvenue aux profils issus de la requête.

![Configuration de l’activité de requête incrémentale dans la zone de travail de campagne orchestrée](../assets/incremental-query-example.png)

