---
solution: Journey Optimizer
product: journey optimizer
title: Mécanismes de sécurisation et limitations de Journey Optimizer
description: En savoir plus sur les mécanismes de sécurisation de Journey Optimizer.
feature: Guardrails
role: User
level: Intermediate
mini-toc-levels: 2
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
TQID: https://experienceleague.adobe.com/k4DqGogrTZ9QrnqyFGwdgDeUI9ivpOd1iSI0c5comuU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
subfeature_v2:
  - id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 9fc2a1d79d334001cee4c60b86e7f7912754eb94
workflow-type: tm+mt
source-wordcount: 4689
ht-degree: 64%

---


# Mécanismes de sécurisation et limitations {#limitations}

Vous trouverez ci-dessous des mécanismes de sécurisation et des limitations lors de l’utilisation d’[!DNL Adobe Journey Optimizer].

Les droits, les limitations de produit et les mécanismes de sécurisation des performances sont répertoriés dans la [page de description du produit Adobe Journey Optimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

>[!CAUTION]
>
>* [Les mécanismes de sécurisation pour les données et la segmentation du profil client en temps réel](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/guardrails){target="_blank"} s’appliquent également à Adobe Journey Optimizer.
>
>* Consultez également la section [Mécanismes de sécurisation pour l’ingestion de données dans le profil client en temps réel](https://experienceleague.adobe.com/fr/docs/experience-platform/ingestion/guardrails){target="_blank"}.

## Principales limites en un coup d’œil {#quick-reference}

Utilisez ce tableau pour rechercher les limites numériques les plus critiques avant de créer ou de publier. Vous trouverez des détails complets et un contexte dans les sections ci-dessous.

| Zone | Limite | Valeur | Type |
|---|---|---|---|
| **Parcours** | Activités max. par parcours | **50** | Limite Hard |
| **Parcours** | Parcours max. en ligne / en pause / d’essai | **100** | Limite soft (extensible) |
| **Parcours** | Taille de l’instance de parcours | **1 MO** | Limite Hard |
| **Parcours** | Taille de la payload du parcours (publication) | **2 Mo** (avertir à 90 %) | Limite Hard |
| **Parcours** | Temporisation de parcours globale | **91 jours** | Limite Hard |
| **Parcours** | File d’attente des événements en attente par profil | **10 événements** | Limite Hard |
| **Parcours** | Instances d’audience en lecture simultanée | **5** dans tous les sandbox | Limite Hard |
| **Parcours** | Débit de lecture du sandbox d’audience | **20 000 profils/s** (partagé) | Limite Hard |
| **Parcours** | Délai d’expiration de la tâche de lecture d’audience | **12 heures** | Limite Hard |
| **Canaux** | Requêtes entrantes par seconde | 5 000 **/S** | Limite Hard |
| **Canaux** | Actions entrantes actives max. | **500** | Limite Hard |
| **Canaux** | Messages transactionnels/s (campagnes) | **500** | Limite Hard |
| **Canaux** | Événements de parcours entrants par seconde | **5,000** | Limite Hard |
| **Actions personnalisées** | Appels par minute (réponse &lt; 0,75 s) | 300 000 **/min** par hôte/sandbox | Limite Hard (configurable) |
| **Actions personnalisées** | Appels par 30 s (réponse > 0,75 s) | 150 000 **/30 s** par hôte/sandbox | Limite Hard (configurable) |
| **Contenu** | Contenu de l’e-mail au moment de la publication | **2 Mo** (auteur de moins de 1 Mo) | Limite Hard |
| **Contenu** | Contenu du message in-app | **2 MO** | Limite Hard |
| **Contenu** | Taille visuelle du fragment | **100 KO** | Limite Hard |
| **Contenu** | Taille du fragment d’expression | **200 KO** | Limite Hard |
| **Contenu** | nœuds de fragment de parcours | **20 nœuds/fragment**, 200 actifs/sandbox | Limite Hard |
| **Audiences** | Compositions d’audience par sandbox | **10** | Limite Hard |
| **Jeux de données** | TTL de magasin de profils (nouvelles organisations/sandbox) | **90 jours** | Limite Hard |
| **Jeux de données** | TTL du lac de données (nouvelles organisations/nouveaux sandbox) | **13 mois** | Limite Hard |

>[!NOTE]
>
>Les limites marquées **Limite Hard (configurable)** peuvent être augmentées en contactant votre représentant Adobe ou l’assistance clientèle d’Adobe.


## Système et plateforme {#system-platform}

### Navigateurs pris en charge {#browsers}

L&#39;interface d&#39;Adobe [!DNL Journey Optimizer] est conçue pour fonctionner de manière optimale avec la dernière version de Google Chrome. Vous pouvez rencontrer des problèmes lors de l&#39;utilisation de certaines fonctions sur des versions plus anciennes ou d&#39;autres navigateurs.

### Mécanismes de sécurisation des jeux de données {#datasets-guardrails}

À compter de février 2025, un mécanisme de sécurisation de la durée de vie (TTL) sera déployé dans les jeux de données générés par le système Journey Optimizer dans **les nouveaux sandbox et les nouvelles organisations** comme suit :

* **90 jours** pour les données du magasin de profils
* **13 mois** pour les données du lac de données

Cette modification sera déployée sur les **sandbox client existants** dans une phase ultérieure. [En savoir plus sur les mécanismes de sécurisation de durée de vie (TTL) des jeux de données](../data/datasets-ttl.md)

## Canaux et messages {#channel-guardrails}

Cette section couvre les mécanismes de sécurisation pour tous les canaux de communication, y compris les e-mails, SMS, canaux entrants (web, in-app, basés sur du code, cartes de contenu) et messages transactionnels.

>[!NOTE]
>
>Dans de rares cas, des pannes temporaires dans une zone géographique spécifique peuvent entraîner l’exclusion de profils valides des parcours ou l’indication erronée des e-mails comme rebonds. Une fois les services restaurés, vérifiez à nouveau les journaux du parcours, les champs du profil de consentement et republiez le parcours si nécessaire. En cas de panne du FAI, découvrez comment supprimer des profils de la liste de suppression dans [cette section](../configuration/manage-suppression-list.md#remove-from-suppression-list).

### Mécanismes de sécurisation des e-mails {#message-guardrails}

Les mécanismes de sécurisation suivants s’appliquent au [canal e-mail](../email/get-started-email.md) :

* Vous ne pouvez pas utiliser le même domaine d’envoi pour envoyer des e-mails depuis [!DNL Adobe Journey Optimizer] et depuis un autre produit, tel que [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage], par exemple.

Lors de la conception des e-mails, le système vérifie les paramètres essentiels et affiche des alertes pour les avertissements (recommandations et bonnes pratiques) ainsi que pour les erreurs (problèmes bloquants empêchant les tests ou l’activation). Pour en savoir plus sur les alertes d’e-mail et les exigences de validation, consultez [cette section](../email/create-email.md#check-email-alerts).

#### Taille du contenu des messages pour la publication de parcours {#message-content-size}

Lors de la publication de parcours contenant des e-mails, la taille totale du contenu du message ne doit pas dépasser **2 Mo** après le traitement du serveur principal. Lors de la publication, le système traite automatiquement le contenu des messages en corrigeant les liens et les images, ainsi qu’en appliquant des transformations, ce qui augmente la taille de la payload au-delà de la taille du contenu créé.

>[!CAUTION]
>
>Si le contenu final du message traité dépasse **2 Mo**, la publication par parcours échoue. Conservez le contenu de votre message créé bien en dessous de 2 Mo, idéalement en dessous de **1 Mo**, pour permettre une mémoire tampon de 300 à 400 Ko pour la surcharge de traitement du serveur principal.

**Bonnes pratiques pour éviter les échecs de publication :**

* Conserver le contenu d’e-mail créé sous **1 Mo**
* Réduire le nombre de variantes de contenu
* Optimiser et compresser les images avant de les ajouter aux messages
* Supprimer les ressources inutilisées et les éléments HTML inutiles
* Tester la taille des messages avant la publication des parcours en production

Si la publication du parcours échoue en raison de la taille du contenu, réduisez le contenu des messages et republiez le parcours.

### Mécanismes de sécurisation des SMS {#sms-guardrails}

Les mécanismes de sécurisation suivants s’appliquent au [canal SMS](../mobile/get-started-mobile.md) :

* Les fichiers multimédias pour MMS peuvent être inclus via une URL prise en charge. Assurez-vous que le fichier multimédia est chargé séparément.
* La synchronisation des commentaires des messages n’est actuellement pas disponible pour les MMS.
* La gestion du consentement fonctionne au niveau du canal SMS pour les MMS.

### Mécanismes de sécurisation pour le canal entrant {#inbound-guardrails}

* Pour utiliser des actions d’[expérience basée sur du code](../code-based/get-started-code-based.md) dans [!DNL Journey Optimizer] et fournir la payload de contenu de code qui peut être utilisée par vos applications, respectez les conditions préalables requises présentées dans [cette page](../code-based/code-based-prerequisites.md).

* Pour créer et accéder à des [pages web](../web/get-started-web.md) dans l’interface d’utilisation de [!DNL Journey Optimizer], suivez les conditions préalables répertoriées sur [cette page](../web/web-prerequisites.md).

* Pour envoyer des messages in-app dans vos parcours et campagnes avec [!DNL Journey Optimizer], suivez les conditions préalables à la diffusion répertoriées sur [cette page](../in-app/inapp-configuration.md).

* Pour qu’Adobe Journey Optimizer affiche correctement les cartes de contenu, vous devez configurer les paramètres Adobe Experience Platform répertoriés sur [cette page](../content-card/content-card-configuration-prereq.md).

* Journey Optimizer prend en charge un volume maximal de 5 000 requêtes entrantes **par seconde**. Ce mécanisme de sécurisation s’applique à toutes les requêtes entrantes, qui peuvent provenir de n’importe quel canal entrant pris en charge par Journey Optimizer ([web](../web/get-started-web.md), [in-app](../in-app/get-started-in-app.md), [expériences basées sur du code](../code-based/get-started-code-based.md), [cartes de contenu](../../rp_landing_pages/content-card-landing-page.md)).

* Journey Optimizer prend en charge un maximum de **500 actions entrantes actives** à tout moment. Ces actions entrantes sont comptabilisées si elles font partie d’une campagne active ou si elles sont un nœud utilisé dans un parcours actif. Une fois ce nombre atteint, vous devez désactiver les anciennes campagnes ou les anciens parcours qui utilisent des actions entrantes avant de pouvoir en lancer de nouvelles.

#### Gestion des profils avec canaux entrants {#profile-management-inbound}

Les canaux entrants [!DNL Journey Optimizer] peuvent cibler des profils pseudonymes, c’est-à-dire des profils qui ne sont pas authentifiés ou qui ne sont pas encore connus, car ils n’ont encore jamais été engagés sur d’autres canaux. C’est notamment le cas lors du ciblage de tous les visiteurs ou audiences en fonction d’ID temporaires tels que les ECID.

Cela augmente le nombre total de profils engageables, ce qui peut avoir des implications de coût si le nombre contractuel de profils engageables que vous avez achetés est dépassé. Les mesures de licence de chaque package sont répertoriées dans la page [Description de produit Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Vous pouvez vérifier le nombre de profils engageables dans le [tableau de bord de l’utilisation des licences](../audience/license-usage.md).

Pour que le nombre de profils engageables reste raisonnable, Adobe recommande de définir une durée de vie (TTL) pour supprimer automatiquement les profils pseudonymes du profil client en temps réel s’ils n’ont pas été vus ou engagés dans une période spécifique. Adobe recommande de définir la valeur de durée de vie sur **14 jours** pour correspondre à la durée de vie actuelle du profil Edge.

>[!NOTE]
>
>Découvrez comment configurer l’expiration des données pour les profils pseudonymes dans la [documentation d’Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

### Mécanismes de sécurisation des messages transactionnels {#transactional-message-guardrails}

Journey Optimizer prend en charge un volume maximal de 500 messages transactionnels **par seconde** dans les campagnes.

## Contenu et ressources {#content-assets}

Cette section présente les mécanismes de sécurisation pour la création et la gestion de contenu, y compris les pages de destination, les sous-domaines et les fragments.

### Mécanismes de sécurisation de l’assistant AI {#ai-assistant-g}

Les mécanismes de sécurisation et les limitations de la **génération de contenu de l’assistant AI**, y compris les canaux pris en charge (e-mail, push, web, SMS) et les limitations de l’éditeur de personnalisation, sont répertoriés sur [cette page](../content-management/gs-generative.md#generative-guardrails).

### Mécanismes de sécurisation des pages de destination {#lp-guardrails}

Les mécanismes de sécurisation suivants s’appliquent aux [pages de destination](../landing-pages/get-started-lp.md) :

* Un seul composant de **Formulaire** peut être utilisé dans une page principale unique.
* Le composant de **Formulaire** ne peut pas être utilisé dans les sous-pages.
* Vous ne pouvez pas ajouter de pré-en-tête à une page de destination.
* Vous ne pouvez pas sélectionner l’option **Coder le vôtre** lors de la conception d’une page de destination principale.

### Mécanismes de sécurisation des sous-domaines {#subdomain-guardrails}

Les mécanismes de sécurisation et les limitations qui s’appliquent à la délégation de sous-domaines dans Journey Optimizer sont décrits dans [cette page](../configuration/delegate-subdomain.md#guardrails).

### Mécanismes de sécurisation des fragments {#fragments-guardrails}

Les mécanismes de sécurisation suivants s’appliquent aux [fragments](../content-management/fragments.md) :

* Pour créer, modifier, archiver et publier des fragments, vous avez besoin des autorisations **[!DNL Manage library items]** et **[Publier le fragment]** incluses dans le profil de produit **[!DNL Content Library Manager]**. [En savoir plus](../administration/ootb-product-profiles.md#content-library-manager)
* Les fragments visuels ne sont disponibles que pour le canal E-mail.
* Les fragments d’expression ne sont pas disponibles pour les canaux In-app.
* Les fragments visuels ne peuvent pas dépasser **100 Ko**. Les fragments d’expression ne peuvent pas dépasser **200 Ko**.
* Pour utiliser un fragment dans un parcours ou une campagne, son statut doit être **Actif**.
* Les [attributs contextuels](../personalization/personalization-build-expressions.md) ne sont pas pris en charge dans les fragments.
* Les fragments visuels ne sont pas compatibles entre les modes Utiliser des thèmes et Style manuel. Pour pouvoir utiliser un fragment dans un contenu auquel vous souhaitez appliquer un thème, ce fragment doit être créé en mode Utiliser des thèmes. [En savoir plus sur les thèmes](../email/apply-email-themes.md)
* Lorsque le suivi est activé dans un parcours ou une campagne, si vous ajoutez des liens à un fragment et que ce fragment est utilisé dans un message, ces liens font l’objet d’un suivi comme tous les autres liens inclus dans le message. [En savoir plus sur les liens et le suivi](../email/message-tracking.md)

## Audiences et profils {#audiences-profiles}

Cette section présente les mécanismes de sécurisation pour la gestion des audiences, la gestion des profils et les considérations sur les profils engageables.

### Mécanismes de sécurisation des audiences et des profils {#audience}

* Vous pouvez publier jusqu’à **10 compositions d’audience** dans un sandbox donné. Si vous avez atteint ce seuil, vous devez supprimer une composition pour libérer de l’espace et en publier une nouvelle.

  En savoir plus sur les compositions d’audiences sur [cette page](../audience/get-started-audience-orchestration.md).

* Lors de l’ingestion de données, les e-mails sont sensibles à la casse. Cela signifie que des profils peuvent être créés en double (par exemple, un profil pour John.Greene@luma.com, un autre pour john.greene@luma.com) et utilisés lors du ciblage du destinataire correspondant dans vos parcours et campagnes [!DNL Journey Optimizer].

* Lors du ciblage de profils pseudonymes (visiteurs non authentifiés) avec des canaux entrants, pensez à définir une durée de vie (TTL) pour la suppression automatique des profils afin de maîtriser le nombre de profils engageables et les coûts associés. [En savoir plus](#profile-management-inbound)

## Gestion des décisions {#decision-management}

### Mécanismes de sécurisation des décisions et de la gestion des décisions {#decisioning-guardrails}

Les mécanismes de sécurisation et les limitations à garder à l’esprit lorsque vous utilisez la prise de décision ou la gestion des décisions sont détaillés dans les sections Prise de décision et gestion des décisions présentées ci-après :

* [Mécanismes de sécurisation et limitations des prises de décision](../experience-decisioning/decisioning-guardrails.md)
* [Mécanismes de sécurisation et limitations de la gestion des décisions](../offers/decision-management-guardrails.md)

## Parcours {#journeys-guardrails}

Cette section présente les mécanismes de sécurisation et les limitations des parcours, y compris les limitations générales des parcours, les composants de parcours (actions, événements, sources de données), les activités de parcours et les fonctionnalités spécifiques telles que les actions personnalisées et l’éditeur d’expression.

### Mécanismes de sécurisation généraux des parcours {#journeys-guardrails-journeys}

* Le nombre d&#39;activités dans un parcours est limité à 50 **de**. Le nombre d’activités s’affiche dans la section supérieure gauche de la zone de travail du parcours.

  Lorsque les parcours se rapprochent de cette limite, les performances de modification et de publication peuvent se dégrader et des échecs d’enregistrement ou de validation peuvent se produire. Si cela se produit, divisez votre parcours en sous-parcours plus petits à l’aide d’[activités de saut](../building-journeys/jump.md) ou recréez-le dans une nouvelle version. La limite d’activité ne peut pas être augmentée.

* Par défaut, le nombre de parcours d’exécution actifs, en pause ou secs à la fois est limité à 100 **&#x200B;**. Le nombre actuel de parcours s’affiche au-dessus de la zone de travail du parcours.

  Lorsque vous publiez des parcours, nous les mettons automatiquement à l’échelle et les ajustons pour garantir une stabilité et un débit maximaux. Lorsque vous approchez du jalon de 100 parcours actifs à la fois, une notification s’affiche dans l’interface utilisateur pour cette réalisation. Si cette notification s’affiche et que vous devez étendre vos parcours au-delà de 100 parcours actifs à la fois, créez un ticket pour l’assistance clientèle et nous vous aiderons à atteindre vos objectifs.

* Lors de l’utilisation d’une qualification d’audience dans un parcours, cette activité de qualification d’audience peut prendre jusqu’à **10 minutes** pour être active et écouter les profils qui rejoignent l’audience ou en sortent.

* La taille maximale d’une instance de parcours pour un profil est de **1 Mo**. Toutes les données collectées dans le cadre de l’exécution du parcours sont stockées dans cette instance de parcours. Par conséquent, les données d’un événement entrant, les informations de profil récupérées sur Adobe Experience Platform, les réponses d’action personnalisée, etc. sont stockées dans cette instance de parcours et ont des conséquence sur la taille du parcours. Il est conseillé, lorsqu&#39;un parcours commence par un événement, de limiter la taille maximale de la payload de cet événement (par exemple, inférieure à 800 **Ko**) afin d&#39;éviter d&#39;atteindre cette limite après quelques activités, lors de l&#39;exécution du parcours. Lorsque cette limite est atteinte, le profil est au statut d’erreur et est exclu du parcours.

* Pour chaque profil et version de parcours, l’exécution du parcours conserve une file d’attente interne allant jusqu’à 10 événements en attente **&#x200B;**&#x200B;pendant le traitement d’un événement. Si cette limite est atteinte, les événements supplémentaires sont ignorés pour la raison `maxInstanceStackEventsReached` jusqu’à ce que la pile se vide. Voir [Événements ignorés en raison d’une instance de parcours bloquée](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached).

* Outre la temporisation utilisée dans les activités de parcours, il existe une temporisation globale qui n’est pas affichée dans l’interface et qui ne peut pas être modifiée. Cette temporisation globale arrête la progression des personnes dans le parcours **91 jours** après leur entrée. [En savoir plus](../building-journeys/journey-properties.md#global_timeout)

>[!TIP]
>
>**Ce que cela signifie pour vous :** la limite de **50 activités** et la limite de **100 parcours en direct** sont les deux mécanismes de sécurisation que la plupart des équipes rencontrent en premier lors de la mise à l’échelle. Planifiez le fractionnement précoce des parcours et étendez les heures de début de la lecture d’audience à au moins 5 à 10 minutes d’intervalle afin d’éviter les conflits de débit dans le sandbox.

#### Validation de la taille de la payload du parcours {#journey-payload-size}

Lorsque vous enregistrez ou publiez un parcours, Journey Optimizer valide la taille totale de la payload du parcours afin de préserver la stabilité et les performances.

| Scénario | Seuil | Comportement |
|---|---|---|
| Payload &lt; 90 % de la limite | En dessous de l’avertissement | Le parcours enregistre et publie. Aucun avertissement ou erreur affiché. |
| Payload 90 à 99 % de la limite | Avertissement (soft) | Le parcours enregistre et publie avec un avertissement : **Avertissement** : la taille de la payload du Parcours est proche de la limite. Nœud le plus grand : « [nom du nœud] » (type : « [type de nœud] », taille : [N] octets). |
| Payload ≥ 100 % de la limite | **Erreur (hard)** | L’enregistrement ou la publication est bloqué. Renvoie **Une entité de requête HTTP 413 trop grande**. Erreur : la taille de la payload du Parcours dépasse la limite. Nœud le plus grand : « [nom du nœud] » (type : « [type de nœud] », taille : [N] octets). |

**Configuration par défaut**

* **Taille maximale de requête par défaut** : **2 Mo** (2 000 000 octets). Certaines organisations peuvent avoir des limites personnalisées configurées par Adobe.
* **Seuil d’avertissement** : 90 % de la limite maximale.
* **Seuil d’erreur** : 100 % de la limite maximale.

**Résolution des problèmes et recommandations**

* Examinez le nœud le plus grand mis en surbrillance dans l’avertissement ou l’erreur.
* Simplifiez les conditions, réduisez les mappages de données et supprimez les étapes ou paramètres inutiles.
* Envisagez de diviser le parcours en parcours plus petits si nécessaire.
* Si vous pensez que votre organisation a besoin d’une limite supérieure, contactez votre représentant ou représentante Adobe.

Pour surveiller la taille actuelle de la payload de votre parcours avant la publication, utilisez l’indicateur **[!UICONTROL Taille actuelle de la payload du parcours]** dans le panneau des propriétés du parcours. [Découvrez comment vérifier la taille de la payload du parcours &#x200B;](../building-journeys/journey-properties.md#journey-payload-size)

### Comparaison des packages de licence {#select-package-limitations}

>[!NOTE]
>
>Les limitations du package Select ci-dessous ne s’appliquent pas aux parcours Lecture d’audience ou Événement métier. Si vous avez besoin d’une logique de parcours plus complexe avec plusieurs actions, conditions ou activités d’attente, envisagez de mettre à niveau votre package de licence ou d’utiliser des parcours Lecture d’audience, le cas échéant.

Pour les clients qui utilisent le package de licence **Select**, les restrictions supplémentaires suivantes s’appliquent spécifiquement aux parcours unitaires (parcours commençant par un événement ou une qualification d’audience) :

| Limite | Code d’erreur | Description |
|---|---|---|
| Une seule action autorisée | `ERR_PKG_SELECT_8` | Les parcours unitaires ne peuvent contenir qu&#39;une seule activité d **action**. Plusieurs activités d’action, telles que les e-mails, les notifications push et les SMS ne sont pas autorisées dans le même parcours. |
| Aucune condition autorisée | `ERR_PKG_SELECT_7` | Les activités de condition ne peuvent pas être utilisées dans des parcours unitaires. Le parcours doit suivre un unique chemin linéaire sans logique de branche. |
| Aucune activité d’attente | `ERR_PKG_SELECT_6` | Les activités d’attente ne peuvent pas être ajoutées aux parcours unitaires. Les actions doivent s’exécuter immédiatement, sans délai. |
| Les transitions temporisation/erreur doivent aller au nœud de fin | `ERR_PKG_SELECT_2` | Si vous configurez des transitions de temporisation ou d’erreur pour une action (une action d’e-mail, par exemple), ces chemins doivent pointer directement vers un nœud de fin. Elles ne peuvent pas se connecter à d’autres activités ou actions dans le parcours. |

>[!TIP]
>
>**Signification pour vous :** si vous êtes sur le package Select et que vous avez besoin d’une logique d’embranchement, d’activités d’attente ou de plusieurs actions, vous devez utiliser un parcours Lecture d’audience à la place, ou contacter votre représentant Adobe pour mettre à niveau votre package.

### Actions générales {#general-actions-g}

Les mécanismes de sécurisation suivants s’appliquent aux [actions](../building-journeys/about-journey-activities.md) dans vos parcours :

* En cas d’erreur, trois reprises sont systématiquement effectuées. Vous ne pouvez pas adapter le nombre de reprises en fonction du message d&#39;erreur renvoyé. Les reprises sont effectuées pour toutes les erreurs HTTP, à l’exception des erreurs HTTP 401, 403 et 404.
* L’événement **Réaction** intégré vous permet de réagir aux actions d’usine. En savoir plus sur [cette page](../building-journeys/reaction-events.md). Si vous souhaitez réagir à un message envoyé par le biais d’une action personnalisée, vous devez configurer un événement dédié.
* Vous ne pouvez pas placer deux actions en parallèle ; vous devez les ajouter l’une après l’autre.
* Un profil ne peut pas être présent plusieurs fois dans le même parcours, en même temps, pour toutes les [versions actives du parcours &#x200B;](../building-journeys/publish-journey.md#journey-create-new-version). Si la rentrée est activée, un profil peut rejoindre à nouveau un parcours, à condition d’avoir complètement quitté cette instance précédente du parcours. [En savoir plus](../building-journeys/end-journey.md)

### Versions de parcours {#journey-versions-g}

Les mécanismes de sécurisation suivants s’appliquent aux [versions de parcours](../start/user-interface.md) :

* Un parcours commençant par une activité d’événement dans la version_v1 ne peut pas débuter avec un autre élément qu’un événement dans d’autres versions. Vous ne pouvez pas débuter un parcours avec un événement **Qualification d’audience**.
* Un parcours commençant par une activité **Qualification d’audience** dans la version v1 doit toujours débuter avec une **qualification d’audience** dans d’autres versions.
* L’audience et l’espace de noms sélectionnés dans **Qualification d’audience** (premier nœud) ne peuvent pas être modifiés dans les nouvelles versions.
* La règle de rentrée doit être la même dans toutes les versions du parcours.
* Un parcours commençant par une **lecture d’audience** ne peut pas commencer par un autre événement dans les versions suivantes.
* Vous ne pouvez pas créer de nouvelle version d’un parcours de lecture d’audience avec lecture incrémentielle. Vous devez dupliquer le parcours.

### Actions personnalisées {#custom-actions-g}

Les mécanismes de sécurisation suivants s’appliquent aux [actions personnalisées](../action/action.md) dans vos parcours :

| Mécanisme de sécurisation | Valeur | Remarques |
|---|---|---|
| Limite de limitation — réponse &lt; 0,75 s | 300 000 appels **/min** par hôte et par sandbox | Fenêtre coulissante. Appliqué par sandbox et par point d’entrée. |
| Limite de limitation — réponse > 0,75 s | **150 000 appels/30 s** par hôte et par sandbox | Fenêtre coulissante. Limite distincte appliquée lorsque la latence du point d’entrée dépasse 0,75 s. |
| Type d’URL | Statique uniquement | Les paramètres dynamiques dans l’URL de l’action personnalisée ne sont pas pris en charge. |
| Méthodes HTTP prises en charge | POST, PUT, GET | Les autres méthodes ne sont pas prises en charge. |
| Paramètre de requête / format du nom de l’en-tête | Ne doit pas commencer par `.` ou `$` | Les noms commençant par ces caractères sont rejetés. |
| Adresses IP dans l’URL | Non autorisé | Utilisez des noms d’hôtes plutôt que des adresses IP. |
| Adresses Adobe internes | Non autorisé | Les adresses `.adobe.*` ne sont pas autorisées dans les URL et les API. |
| Actions personnalisées intégrées | Impossible de supprimer | Les actions personnalisées intégrées sont permanentes. |
| Format de la payload | JSON uniquement | Le format JSON est requis pour les payloads de la requête et de la réponse. Voir [cette page](../action/about-custom-action-configuration.md#custom-actions-limitations). |
| Débit minimal du point d’entrée | 200 TPS | Tout point d’entrée ciblé par une action personnalisée doit prendre en charge au moins 200 TPS. |

>[!TIP]
>
>**Ce que cela signifie pour vous :** la limite de 300 000 appels/min par défaut protège vos points d’entrée externes contre le dépassement par le débit du parcours. Si votre point d’entrée peut gérer une charge plus importante, vous pouvez augmenter cette limite à l’aide de l’API [de plafonnement](../configuration/capping.md) ou [de limitation](../configuration/throttling.md). Contactez votre représentant Adobe si vous avez besoin d’une limite organisationnelle plus élevée.

Cette limite a été définie en fonction de l’utilisation de la clientèle, afin de protéger les points d’entrée externes ciblés par des actions personnalisées. Si nécessaire, vous pouvez remplacer ce paramètre en définissant une limitation ou un ralentissement plus élevé via nos API de limitation/ralentissement. Consultez [cette page](../configuration/external-systems.md).

### Événements {#events-g}

Les mécanismes de sécurisation suivants s’appliquent aux [événements](../event/about-events.md) dans vos parcours :

* Journey Optimizer prend en charge un volume maximal de 5 000 événements de parcours entrant **par seconde** dans tous les sandbox. Pour en savoir plus sur cette limitation, consultez [cette page](../event/about-events.md#event-thoughput).
* Les parcours déclenchés par un événement peuvent prendre jusqu’à **5 minutes** pour traiter la première action du parcours.
* En ce qui concerne les événements générés par le système, les données de diffusion en continu utilisées pour initier un parcours client doivent d’abord être configurées dans Journey Optimizer pour obtenir un identifiant d’orchestration unique. Cet identifiant d’orchestration doit être ajouté à la payload de diffusion en continu entrant dans Adobe Experience Platform. Cette limitation ne s’applique pas aux événements basés sur une règle.
* Les événements métier ne peuvent pas être utilisés conjointement avec des événements unitaires ou des activités de qualification d’audience.
* Les parcours unitaires (qui commencent par un événement ou une qualification d’audience) incluent un mécanisme de sécurisation qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La rentrée du profil est temporairement bloquée par défaut pendant **5 minutes**. Par exemple, si un événement déclenche un parcours à 12:01 pour un profil spécifique et qu’un autre événement se produit à 12:03 (qu’il s’agisse du même événement ou d’un autre déclenchant le même parcours), ce parcours ne reprendra pas pour ce profil.
* Journey Optimizer exige que les événements soient diffusés en continu vers Data Collection Core Service (DCCS) pour pouvoir déclencher un parcours. Les événements ingérés par lot, les événements insérés via **Query Service**, ou les événements provenant de jeux de données Journey Optimizer internes (commentaires des messages, tracking e-mail, etc.) ne peuvent pas être utilisés pour déclencher un parcours. Pour les cas d’utilisation où vous ne pouvez pas obtenir d’événements en flux continu, vous devez créer une audience basée sur ces événements et utiliser l’activité **Lecture d’audience** à la place. La qualification d’audience peut techniquement être utilisée. Cette méthode n’est toutefois pas recommandée, car elle peut entraîner des défis en aval en fonction des actions utilisées.

### Sources de données {#data-sources-g}

Les mécanismes de sécurisation suivants s’appliquent aux [sources de données](../datasource/about-data-sources.md) dans vos parcours :

* Les sources de données externes peuvent être exploitées au cours d’un parcours client pour consulter des données externes en temps réel. Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.
* Les adresses d’Adobe internes (`.adobe.*`) ne sont pas autorisées dans les URL et les API.

>[!NOTE]
>
>Les réponses étant désormais prises en charge, vous devez utiliser des actions personnalisées au lieu de sources de données pour les cas d’utilisation de sources de données externes.

### Création de parcours et de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/la mise à jour de profils basés sur l’API dans Adobe Experience Platform. La cible de niveau de service (TSL) en termes de latence est d’atteindre moins de 1 minute entre l’ingestion et le profil unifié pour le 95e centile des requêtes, avec un volume de **20 000 requêtes par seconde (DPS)**.

Si un parcours est déclenché simultanément à la création d’un profil et qu’il vérifie/récupère immédiatement des informations auprès du service de profil, il est possible qu&#39;il ne fonctionne pas correctement.

Vous pouvez choisir l’une des deux solutions suivantes :

* Ajouter une activité d’attente après le premier événement pour donner à Adobe Experience Platform le temps nécessaire pour exécuter l’ingestion sur le service de profil.

* Configurer un parcours qui n’utilise pas immédiatement le profil. Par exemple, si le parcours est conçu pour confirmer la création d’un compte, l’événement d’expérience peut contenir les informations nécessaires à l’envoi du premier message de confirmation (prénom, nom, adresse e-mail, etc.).

### Identifiants supplémentaires {#supplemental}

Des mécanismes de sécurisation spécifiques s’appliquent à l’utilisation d’identifiants supplémentaires dans les parcours. Ils sont répertoriés dans [cette page](../building-journeys/supplemental-identifier.md#guardrails).

### Éditeur d’expression {#expression-editor}

Le mécanisme de sécurisation suivant s’applique à l’[éditeur d’expression de parcours](../building-journeys/expression/expressionadvanced.md) :

* Les groupes de champs d’événement d’expérience ne peuvent pas être utilisés dans les parcours commençant par une activité Lecture d’audience, Qualification d’audience ou événement métier. Vous devez créer une audience et utiliser une condition `inaudience` dans le parcours.
* Les attributs `timeSeriesEvents` ne peuvent pas être utilisés dans l’éditeur d’expression. Pour accéder aux événements d’expérience au niveau du profil, créez un groupe de champs basé sur un schéma `XDM ExperienceEvent`.

### Activités de parcours {#activities}

#### Activité Qualification de l’audience {#audience-qualif-g}

Le mécanisme de sécurisation suivant s’applique à l’activité de parcours [Qualification d’audience](../building-journeys/audience-qualification-events.md) :

* L’activité Qualification de l’audience ne peut pas être utilisée avec les activités Adobe Campaign.
* Les identifiants supplémentaires ne sont pas pris en charge pour les parcours de qualification d’audience.

Pour en savoir plus sur les taux de traitement de parcours et les limites de débit, consultez [cette section](../building-journeys/entry-management.md#journey-processing-rate).

D’autres mécanismes de sécurisation, notamment des recommandations sur les audiences en flux continu par rapport aux audiences par lots et les limites d’audience de composition, sont répertoriés sur [cette page](../building-journeys/audience-qualification-events.md#audience-qualification-guardrails).

#### Activités de campagne {#ac-g}

Les mécanismes de sécurisation suivants s’appliquent aux activités **[!UICONTROL Campaign v7/v8]** et **[!UICONTROL Campaign Standard]** :

* Les activités Adobe Campaign ne peuvent pas être utilisées avec une activité Lecture d’audience ou Qualification d’audience.
* Les activités **[!UICONTROL Campaign Standard]** ne peuvent pas être utilisées avec les activités des autres canaux : Carte, Expérience basée sur du code, E-mail, Notification push, SMS, Messages in-app, Web.
* Les activités **[!UICONTROL Campaign v7/v8]** peuvent être utilisées conjointement avec les activités de canal natives dans le même parcours.

#### Événements de réaction {#reaction-events-g}

Des mécanismes de sécurisation spécifiques s’appliquent aux événements **[!UICONTROL Reaction]**, notamment l’exigence de placer l’activité immédiatement après une action de canal et l’impossibilité de suivre les messages envoyés dans un autre parcours. Ils sont répertoriés sur [cette page](../building-journeys/reaction-events.md#guardrails-limitations).

#### Activité in-app {#in-app-activity-limitations}

Les mécanismes de sécurisation suivants s’appliquent à l’action **[!UICONTROL Message in-app]**. En savoir plus sur les messages in-app sur [cette page](../in-app/create-in-app.md).

* Cette fonctionnalité n’est actuellement pas disponible pour les clientes et clients du secteur de la santé.

* La personnalisation ne peut contenir que des attributs de profil.

* L’activité in-app ne peut pas être utilisée avec les activités **[!UICONTROL Campaign Standard]**.

* L’affichage in-app est lié à la durée de parcours, ce qui signifie que lorsque le parcours se termine pour un profil, tous les messages in-app de ce parcours ne s’affichent plus pour ce profil. Par conséquent, il n’est pas possible d’arrêter un message in-app directement à partir d’une activité de parcours. Vous devez plutôt terminer le parcours entier pour que les messages in-app ne s’affichent pas sur le profil.

* En mode test, l’affichage in-app dépend de la durée de vie du parcours. Pour éviter que le parcours ne se termine trop tôt au cours du test, ajustez la valeur **[!UICONTROL Temps d’attente]** de vos activités **[!UICONTROL Attente]**.

* Les activités **[!UICONTROL Réaction]** ne peuvent pas être utilisées pour réagir à une ouverture ou un clic in-app.

* Un délai d’activation peut se produire entre le moment où le profil d’une personne atteint une activité in-app dans la zone de travail et le moment où ladite personne commence à voir ce message in-app.

* La taille du contenu du message in-app est limitée à **2 Mo**. L’inclusion d’images de grande taille peut entraver le processus de publication.

#### Activité de décision de contenu {#content-decision-g}

Des mécanismes de sécurisation spécifiques s’appliquent à l’activité **[!UICONTROL Décision de contenu]**, notamment un délai de 48 heures avant que les politiques de consentement mises à jour ne prennent effet dans les politiques de décision. Ils sont répertoriés sur [cette page](../building-journeys/content-decision.md#guardrails).

#### Activité Saut {#jump-g}

Des mécanismes de sécurisation spécifiques s’appliquent à l’activité **[!UICONTROL Saut]**. Ils sont répertoriés sur [cette page](../building-journeys/jump.md#jump-limitations).

#### Activité Lecture d’audience {#read-segment-g}

Les mécanismes de sécurisation suivants s’appliquent à l’activité de parcours [Lecture d’audience](../building-journeys/read-audience.md) :

| Mécanisme de sécurisation | Valeur | Remarques |
|---|---|---|
| Instances simultanées (tous les sandbox + parcours) | **5** | Évitez de planifier plus de 5 parcours avec Lecture d’audience commençant en même temps ; étendez-les à 5-10 minutes d’intervalle. |
| Débit des sandbox | **20 000 profils/s** (partagé) | Partagé dans toutes les activités Lecture d’audience du sandbox. Si les limites sont atteintes, les tâches peuvent être mises en file d’attente. |
| Débit configurable par activité | **500 à 20 000 profils/s** | Configurez par activité dans la limite partagée du sandbox. |
| Délai d’expiration du traitement des tâches | **12 heures** | Les tâches qui ne peuvent pas être traitées dans les 12 heures sont automatiquement nettoyées et ne s’exécutent pas. |
| Fenêtre Réessayer | Jusqu’à **1 heure** (intervalles de 10 minutes) | Les reprises sont appliquées lors de la récupération de la tâche d’exportation. Les parcours peuvent s’exécuter jusqu’à 1 heure après l’heure planifiée. |
| Taux de lecture des ID supplémentaires | **500 profils/s** par instance de parcours | S’applique lorsque des ID supplémentaires sont en cours d’utilisation. |
| Lecture d’instances d’audience par parcours | **1** | Un parcours ne peut avoir qu’une seule activité Lecture d’audience. |
| Types d’audience | Les audiences diffusées en continu sont toujours à jour | Les audiences par lots ne sont évaluées qu’une seule fois par jour au moment de l’évaluation quotidienne des lots. |
| Actualisation des attributs de profil | Actualisation des activités **Attente** | À l’entrée du parcours, les profils utilisent des valeurs d’instantané par lots. Les attributs s’actualisent lorsqu’un profil atteint une activité Attente . |
| Positionnement dans le parcours | Première activité ou après un événement métier | L&#39;activité Lecture d&#39;audience ne peut être utilisée que comme première activité d&#39;un parcours ou après un événement métier. |
| Utiliser avec Adobe Campaign | Non pris en charge | L’activité Lecture d’audience ne peut pas être utilisée avec les activités Adobe Campaign. |
| Audiences multiples | Pas de prise en charge directe | L’activité Lecture d’audience ne peut cibler qu’une seule audience par parcours. Pour utiliser plusieurs audiences, fusionnez-les d’abord. [Voici comment procéder](../audience/get-started-audience-orchestration.md) |

>[!TIP]
>
>**Ce que cela signifie pour vous :** la limite de 5 instances simultanées est un plafond strict pour l’ensemble de votre organisation. Si plusieurs équipes planifient des parcours de lecture d’audience, coordonnez soigneusement les heures de début. Les tâches qui ne respectent pas l’intervalle de traitement de 12 heures sont ignorées silencieusement. Confirmez toujours la réussite de l’exécution dans les journaux de parcours.

Voir aussi [recommandations et configuration](../building-journeys/read-audience.md#must-read) pour l’activité Lecture d’audience.

#### Activité Mettre à jour un profil {#update-profile-g}

Des mécanismes de sécurisation spécifiques s’appliquent à l’activité **[!UICONTROL Mettre à jour un profil]**. Ils sont répertoriés sur [cette page](../building-journeys/update-profiles.md).

#### Parcours Pause {#pause-g}

Des mécanismes de sécurisation spécifiques s’appliquent à la **suspension des parcours**, notamment une durée de pause maximale de **14 jours** et une limite de **10 millions de profils** sur tous les parcours en pause de votre organisation. Ils sont répertoriés sur [cette page](../building-journeys/journey-pause.md#journey-pause-guardrails).

#### Test à blanc du parcours {#dry-run-g}

Des mécanismes de sécurisation spécifiques s’appliquent à l’exécution d’essai de Parcours **&#x200B;**, y compris le comptage en fonction des quotas de profil engageable et de parcours réel. Ils sont répertoriés sur [cette page](../building-journeys/journey-dry-run.md#journey-dry-run-limitations).

#### Fragments de parcours {#fragments-journey-g}

Des mécanismes de sécurisation spécifiques s’appliquent à **fragments de Parcours**, y compris un maximum de **20 nœuds par fragment** et **200 fragments actifs par sandbox**. Ils sont répertoriés sur [cette page](../building-journeys/journey-fragments.md#guardrails).

#### Envoyer par vagues {#waves-g}

Des mécanismes de sécurisation spécifiques s’appliquent à **l’envoi de vagues dans les parcours**, notamment une plage de vagues de 2 à 10 et un intervalle minimum de **30 minutes** entre les vagues. Ils sont répertoriés sur [cette page](../building-journeys/send-using-waves.md#limitations-guardrails).

#### Simulation de parcours {#simulation-g}

Des mécanismes de sécurisation spécifiques s’appliquent à la simulation de parcours **&#x200B;**. Ils sont répertoriés sur [cette page](../building-journeys/simulate-journey.md#limitations).

## Orchestration de campagne {#campaign-orchestration}

### Mécanismes de sécurisation de l’orchestration de campagne {#orchestration-guardrails}

Les mécanismes de sécurisation et les limitations à prendre en compte lorsque vous utilisez l’orchestration de campagne sont décrits dans cette section : [Mécanismes de sécurisation et limitations](../orchestrated/guardrails.md).
