---
title: Configuration d’un canal personnalisé - Aperçu
description: Découvrez les étapes qu’un administrateur doit suivre pour configurer un canal personnalisé dans Adobe Journey Optimizer, de la création du canal à la configuration d’un canal.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 4556e8b50fe71cf9d703d034a3c5772b8fea9d33
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 9%

---


# Configuration d’un canal personnalisé {#custom-channel-configuration}

>[!AVAILABILITY]
>
>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en bénéficier.

La configuration d’un canal personnalisé est une tâche d’administration qui se produit une fois par canal. Une fois le canal configuré, les marketeurs peuvent le sélectionner immédiatement dans les campagnes, les parcours et les campagnes orchestrées, comme pour n’importe quel canal [!DNL Journey Optimizer] natif.

Le processus de configuration comprend quatre étapes : définition du canal lui-même (point d’entrée, authentification, payload), gestion des informations d’identification d’API utilisées pour authentifier les requêtes, délégation facultative d’un sous-domaine pour le suivi des liens et enfin création d’une configuration de canal que les spécialistes marketing sélectionneront au moment de la création.

>[!NOTE]
>
>Avant de commencer, passez en revue les conditions préalables et les mécanismes de sécurisation pour les canaux personnalisés, y compris les autorisations requises et les méthodes d’authentification prises en charge.

## Étapes de configuration {#steps}

Le processus de configuration d’un canal personnalisé se compose de quatre étapes. Chaque étape est décrite en détail dans les articles liés ci-dessous.

| Étape | Ce que vous faites | Importance de ces éléments | Lien |
| --- | --- | --- | --- |
| **1. Créez le canal personnalisé** | Définissez l’URL du point d’entrée, les en-têtes, la politique de limitation, le type d’authentification et la structure de la payload du message dans le créateur de canaux. | Il s’agit de la définition principale de votre canal . Il [!DNL Journey Optimizer] indique comment envoyer un message et à quoi il ressemble. | [En savoir plus](create-custom-channel.md) |
| **2. Gérez les informations d’identification d’API** | Créez et gérez les ensembles d’informations d’identification utilisés pour authentifier les requêtes sur votre point d’entrée. | Plusieurs jeux d’informations d’identification vous permettent de réutiliser la même définition de canal sur différentes marques ou environnements sans dupliquer le canal. | [En savoir plus](custom-channel-api-credentials.md) |
| **3. Déléguer un sous-domaine** *(facultatif)* | Déléguer un sous-domaine spécifique à votre canal personnalisé. | Obligatoire uniquement si la payload du message contient des liens pouvant faire l’objet d’un suivi. Sans sous-domaine délégué, le suivi des liens n’est pas disponible pour ce canal. | [En savoir plus](custom-channel-subdomains.md) |
| **4. Créez une configuration de canal** | Créez un préréglage nommé qui lie le canal personnalisé à un ensemble spécifique d’informations d’identification, à un sous-domaine et à des valeurs par défaut facultatives de payload. | Lors de la création de campagnes ou de parcours, les marketeurs sélectionnent un canal personnalisé et une configuration de canal associée. Vous pouvez créer plusieurs configurations pour le même canal (par exemple, une par marque ou région). | [En savoir plus](custom-channel-configuration.md) |

<!--
## Get started {#get-started}

1. [Create the custom channel](create-custom-channel.md) by defining its endpoint, authentication method, and message payload structure in the Channel Builder.
1. [Set up API credentials](custom-channel-api-credentials.md) to authenticate requests sent to your endpoint — required for all authentication types other than **None**.
1. [Delegate a subdomain](custom-channel-subdomains.md) if your message payload includes trackable links and you want them served from a branded domain.
1. [Create a channel configuration](custom-channel-configuration.md) to produce the named preset that marketers will select when building campaigns and journeys.


-->