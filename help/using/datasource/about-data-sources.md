---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les sources de données
description: Découvrez comment commencer avec les sources de données.
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: données, source, parcours, plateforme
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
TQID: https://experienceleague.adobe.com/eG1QcfpHtxpabUt5e7RZiMIpSAJD6Z6bjO-4wtZEUOg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: dd51b532-b93f-4bcf-8dbf-0d007f593aca
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 917
ht-degree: 43%

---

# Commencer avec les sources de données {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="À propos des sources de données"
>abstract="La configuration d’une source de données est toujours effectuée par un utilisateur technique. Elle vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours. Par exemple : définition de conditions, données de paramètres et de personnalisation dans les actions, définition d’attente personnalisée, définition de fuseau horaire."

>[!TIP]
>Vous découvrez la gestion des données dans Journey Optimizer ? Commencez par la présentation de la [Prise en main de la gestion des données](../data/gs-data.md) pour comprendre les schémas, les jeux de données, les identités et le flux de données avant de configurer des sources de données.

Elle vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours. Par exemple :

* [Définition d’une condition](../building-journeys/conditions.md)
* Données de paramètre et de personnalisation dans les [actions](../action/action.md)
* [Définition d’une attente personnalisée](../building-journeys/wait-activity.md#custom)
* [Définition d’un fuseau horaire](../building-journeys/timezone-management.md)

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

Cette configuration n’est pas requise si vos parcours utilisent uniquement les données locales provenant d’une payload d’événement. Par exemple, si votre parcours comprend un événement suivi d’une activité d’action de canal qui utilise uniquement les données de l’événement, il n’est pas nécessaire de configurer une source de données.

Il existe deux types de sources de données :

* La source de données Adobe Experience Platform **préconfigurée** qui définit la connexion au service de profil client en temps réel. Il s’agit d’une source de données intégrée. Consultez [cette page](../datasource/adobe-experience-platform-data-source.md).
* Les sources de données **externes** qui vous permettent de définir une connexion à des systèmes externes. Il s’agit des sources de données que vous pouvez créer. Consultez [cette page](../datasource/external-data-sources.md).

>[!NOTE]
>
>Les réponses étant désormais prises en charge, vous devez utiliser des actions personnalisées au lieu de sources de données pour les cas d’utilisation de sources de données externes. Pour plus d’informations sur les réponses, voir [cette section](../action/action-response.md)

Pour chaque source de données, vous définissez les informations à récupérer à l’aide de groupes de champs. Les groupes de champs sont des ensembles de champs qui peuvent être récupérés à partir d’une source de données. Consultez [cette page](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Les relations de schémas ne sont pas prises en charge pour les sources de données.

## Choisir votre stratégie d’accès aux données {#data-access-strategy}

Avant de configurer une source de données, réfléchissez à l’approche la mieux adaptée à votre cas d’utilisation. Trois options sont disponibles, chacune avec différents compromis en termes de persistance, d’enrichissement du profil et de réutilisation. Pour obtenir des informations détaillées sur ces options, consultez [Bonnes pratiques relatives aux parcours avancés dans Journey Optimizer](https://experienceleague.adobe.com/en/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.

**Option 1 — Accès aux données externes par le biais d’actions personnalisées (pas de lac de données)**

Se connecter directement à une API externe au moment de l’exécution du parcours sans conserver les données dans le lac de données Experience Platform. Idéal lorsque :

* Les données ne sont utiles que dans le cadre du parcours et ne sont pas nécessaires ailleurs.
* Le système externe est accessible par le biais d’un point d’entrée de l’API qui renvoie les attributs nécessaires.

En savoir plus sur les [actions personnalisées](../action/action.md) et [réponses d’action personnalisée](../action/action-response.md).

>[!TIP]
>
>Cette option est adaptée si vous répondez **oui** aux deux questions :
>* Les données sont-elles uniquement utiles dans le contexte du parcours et non nécessaires ailleurs ? Si les données sont également nécessaires pour les audiences ou d’autres canaux, considérez les options 2 ou 3.
>* Le système externe est-il accessible par le biais d’un point d’entrée de l’API qui renvoie les attributs requis ? Dans le cas contraire, vous devrez d’abord ingérer les données dans le lac de données.

**Option 2 — Jeu de données dans le lac de données, non activé pour le profil**

Ingérez des données dans un jeu de données pour déclencher et personnaliser des parcours en fonction des données d’événement contextuelles, sans contribuer au profil client en temps réel. Idéal lorsque :

* Les enregistrements contiennent un champ d’identité utilisable pour accéder aux profils déjà stockés dans Experience Platform.
* Les données ne sont pas nécessaires pour la création d’audiences ou l’assemblage d’identités en dehors de Journey Optimizer.

>[!TIP]
>
>Cette option est adaptée si vous répondez **oui** aux deux questions :
>* Les enregistrements contiennent-ils un champ d’identité pouvant être utilisé pour accéder aux profils déjà stockés dans Experience Platform ? Dans le cas contraire, les parcours ne pourront pas accéder aux profils et les diffuser.
>* Les données NE sont-elles PAS nécessaires pour la création d’[audience](../audience/about-audiences.md) ou l’assemblage d’identités en dehors de Journey Optimizer ? Si c’est le cas, utilisez plutôt l’option 3.

**Option 3 — Jeu de données activé pour Profile dans le lac de données**

Ingérez des données dans un [jeu de données activé pour les profils](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} afin de créer des audiences, d’enrichir les graphiques d’identités et d’exploiter les données sur plusieurs parcours et destinations RT-CDP. Idéal lorsque :

* Les données sont utiles pour les définitions d’audience utilisées dans des canaux au-delà de Journey Optimizer.
* Les données contiennent plusieurs identités qui contribuent à des fragments de profil assemblés plus riches.

>[!CAUTION]
>
>**Avant d’activer un jeu de données pour Profile**, évaluez les domaines suivants :
>* **Synchronisation des données** — Les bases de données externes doivent être synchronisées, avec des alertes en place pour identifier les échecs d&#39;ingestion.
>* **[Mécanismes de sécurisation de profil](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/guardrails){target="_blank"}** — Les mécanismes de sécurisation spécifiques aux profils s’appliquent en plus des [mécanismes de sécurisation généraux de l’ingestion des données](https://experienceleague.adobe.com/fr/docs/experience-platform/ingestion/guardrails){target="_blank"} pour Experience Platform.
>* **Intégrité des identités** — Les données d’identité de vos systèmes sources doivent être soigneusement planifiées pour conserver des graphiques d’identités sains.
>* **Utilisation du lac de données** — La consommation globale de stockage, les relations entre les tables et les profils adressables doivent être évaluées avant l’ingestion.

| | Données conservées dans le lac de données | Jeu de données activé pour le profil |
| --- | --- | --- |
| **Option 1** — Données externes via des actions personnalisées | Non | Non |
| **Option 2** — Jeu de données non activé pour le profil | Oui | Non |
| **Option 3** — Jeu de données activé pour Profil | Oui | Oui |

Pour plus d’informations sur la configuration d’une source de données Adobe Experience Platform et d’une source de données externe, ainsi que sur la recherche et l’utilisation des données dans un parcours, regardez ce [tutoriel vidéo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html?lang=fr){target="_blank"}.

## Vidéo pratique {#video}

Comprenez ce quʼest une source de données. Découvrez également comment configurer des sources de données Experience Platform et externes.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

