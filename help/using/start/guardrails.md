---
solution: Journey Optimizer
product: journey optimizer
title: Mécanismes de sécurisation et limitations de Journey Optimizer
description: En savoir plus sur les mécanismes de sécurisation de Journey Optimizer.
feature: Guardrails
role: User
level: Intermediate
mini-toc-levels: 1
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 8d8f47cafb05cacbda19930a4ca741e05f1e4d1d
workflow-type: tm+mt
source-wordcount: '3574'
ht-degree: 99%

---

# Mécanismes de sécurisation et limitations {#limitations}

Vous trouverez ci-dessous des mécanismes de sécurisation et des limitations lors de l’utilisation de [!DNL Adobe Journey Optimizer].

Les droits, les limitations de produit et les mécanismes de sécurisation des performances sont répertoriés dans la [page de description du produit Adobe Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.


>[!CAUTION]
>
>* [Les mécanismes de sécurisation pour les données et la segmentation du profil client en temps réel](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/guardrails){target="_blank"} s’appliquent également à Adobe Journey Optimizer.
>
>* Consultez également la section [Mécanismes de sécurisation pour l’ingestion de données dans le profil client en temps réel](https://experienceleague.adobe.com/fr/docs/experience-platform/ingestion/guardrails){target="_blank"}.


## Navigateurs pris en charge {#browsers}

L&#39;interface d&#39;Adobe [!DNL Journey Optimizer] est conçue pour fonctionner de manière optimale avec la dernière version de Google Chrome. Vous pouvez rencontrer des problèmes lors de l&#39;utilisation de certaines fonctions sur des versions plus anciennes ou d&#39;autres navigateurs.

## Mécanismes de sécurisation des jeux de données {#datasets-guardrails}

À compter de février 2025, un mécanisme de sécurisation de la durée de vie (TTL) sera déployé dans les jeux de données générés par le système Journey Optimizer dans **les nouveaux sandbox et les nouvelles organisations** comme suit :

* 90 jours pour les données dans la banque de profils
* 13 mois pour les données du lac de données

Cette modification sera déployée sur les **sandbox client existants** dans une phase ultérieure. [En savoir plus sur les mécanismes de sécurisation de durée de vie (TTL) des jeux de données](../data/datasets-ttl.md)

## Mécanismes de sécurisation des canaux {#channel-guardrails}

>[!NOTE]
>
>Dans de rares cas, des pannes temporaires dans une zone géographique spécifique peuvent entraîner l’exclusion de profils valides des parcours ou l’indication erronée des e-mails comme rebonds. Une fois les services restaurés, vérifiez à nouveau les journaux du parcours, les champs du profil de consentement et republiez le parcours si nécessaire. En cas de panne du FAI, découvrez comment supprimer des profils de la liste de suppression dans [cette section](../configuration/manage-suppression-list.md#remove-from-suppression-list).
>

### Mécanismes de sécurisation des e-mails {#message-guardrails}

<!--The following guardrails apply to the [email channel](../../rp_landing_pages/email-landing-page.md):-->

Les mécanismes de sécurisation suivants s’appliquent au [canal e-mail](../email/get-started-email.md) :

* Vous ne pouvez pas utiliser le même domaine d’envoi pour envoyer des e-mails depuis [!DNL Adobe Journey Optimizer] et depuis un autre produit, tel que [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage], par exemple.

Lors de la conception des e-mails, le système vérifie les paramètres essentiels et affiche des alertes pour les avertissements (recommandations et bonnes pratiques) ainsi que pour les erreurs (problèmes bloquants empêchant les tests ou l’activation). Pour en savoir plus sur les alertes d’e-mail et les exigences de validation, consultez [cette section](../email/create-email.md#check-email-alerts).

#### Taille du contenu des messages pour la publication de parcours {#message-content-size}

Lors de la publication de parcours contenant des e-mails, la taille totale du contenu des messages ne doit pas dépasser **2 Mo** après le traitement back-end. Lors de la publication, le système traite automatiquement le contenu des messages en corrigeant les liens et les images, ainsi qu’en appliquant des transformations, ce qui augmente la taille de la payload au-delà de la taille du contenu créé.

>[!CAUTION]
>
>Si le contenu final des messages traité dépasse 2 Mo, la publication de parcours échoue. Pour éviter les échecs de publication, gardez le contenu des messages créés bien en dessous de 2 Mo (idéalement sous **1 Mo**), afin de conserver un buffer de 300 à 400 Ko pour la surcharge liée au traitement back-end.

**Bonnes pratiques pour éviter les échecs de publication :**

* Conserver le contenu des e-mails créés sous 1 Mo
* Réduire le nombre de variantes de contenu
* Optimiser et compresser les images avant de les ajouter aux messages
* Supprimer les ressources inutilisées et les éléments HTML inutiles
* Tester la taille des messages avant la publication des parcours en production

Si la publication du parcours échoue en raison de la taille du contenu, réduisez le contenu des messages et republiez le parcours.

### Mécanismes de sécurisation des SMS {#sms-guardrails}

Les mécanismes de sécurisation suivants s’appliquent au [canal SMS](../sms/get-started-sms.md) :

* Les fichiers multimédias pour MMS peuvent être inclus via une URL prise en charge. Assurez-vous que le fichier multimédia est chargé séparément.
* La synchronisation des commentaires des messages n’est actuellement pas disponible pour les MMS.
* La gestion du consentement fonctionne au niveau du canal SMS pour les MMS.

### Mécanismes de sécurisation pour le canal entrant {#inbound-guardrails}

* Pour utiliser des actions d’[expérience basée sur du code](../code-based/get-started-code-based.md) dans [!DNL Journey Optimizer] et fournir la payload de contenu de code qui peut être utilisée par vos applications, respectez les conditions préalables requises présentées dans [cette page](../code-based/code-based-prerequisites.md).

* Pour créer et accéder à des [pages web](../web/get-started-web.md) dans l’interface d’utilisation de [!DNL Journey Optimizer], suivez les conditions préalables répertoriées sur [cette page](../web/web-prerequisites.md).

* Pour envoyer des messages in-app dans vos parcours et campagnes avec [!DNL Journey Optimizer], suivez les conditions préalables à la diffusion répertoriées sur [cette page](../in-app/inapp-configuration.md).

* Pour qu’Adobe Journey Optimizer affiche correctement les cartes de contenu, vous devez configurer les paramètres Adobe Experience Platform répertoriés sur [cette page](../content-card/content-card-configuration-prereq.md).

* Journey Optimizer prend en charge un volume maximal de 5 000 requêtes entrantes par seconde. Ce mécanisme de sécurisation s’applique à toutes les requêtes entrantes, qui peuvent provenir de n’importe quel canal entrant pris en charge par Journey Optimizer ([web](../web/get-started-web.md), [in-app](../in-app/get-started-in-app.md), [expériences basées sur du code](../code-based/get-started-code-based.md), [cartes de contenu](../../rp_landing_pages/content-card-landing-page.md)).

* Journey Optimizer prend en charge un maximum de 500 actions entrantes actives, quel que soit le moment. Ces actions entrantes sont comptabilisées si elles font partie d’une campagne active ou si elles sont un nœud utilisé dans un parcours actif. Une fois ce nombre atteint, vous devez désactiver les anciennes campagnes ou les anciens parcours qui utilisent des actions entrantes avant de pouvoir en lancer de nouvelles.

#### Gestion des profils avec canaux entrants {#profile-management-inbound}

Les canaux entrants [!DNL Journey Optimizer] peuvent cibler des profils pseudonymes, c’est-à-dire des profils qui ne sont pas authentifiés ou qui ne sont pas encore connus, car ils n’ont encore jamais été engagés sur d’autres canaux. C’est notamment le cas lors du ciblage de tous les visiteurs ou audiences en fonction d’ID temporaires tels que les ECID.

Cela augmente le nombre total de profils engageables, ce qui peut avoir des implications de coût si le nombre contractuel de profils engageables que vous avez achetés est dépassé. Les mesures de licence de chaque package sont répertoriées dans la page [Description de produit Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Vous pouvez vérifier le nombre de profils engageables dans le [tableau de bord de l’utilisation des licences](../audience/license-usage.md).

Pour que le nombre de profils engageables reste raisonnable, Adobe recommande de définir une durée de vie (TTL) pour supprimer automatiquement les profils pseudonymes du profil client en temps réel s’ils n’ont pas été vus ou engagés dans une période spécifique.

>[!NOTE]
>
>Découvrez comment configurer l’expiration des données pour les profils pseudonymes dans la [documentation d’Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

Adobe recommande de définir la valeur de durée de vie (TTL) sur 14 jours pour correspondre à la durée de vie actuelle du profil Edge.

### Mécanismes de sécurisation des messages transactionnels {#transactional-message-guardrails}

Journey Optimizer prend en charge un volume maximal de 500 messages transactionnels par seconde dans les campagnes.

## Mécanismes de sécurisation des pages de destination {#lp-guardrails}

Les mécanismes de sécurisation suivants s’appliquent aux [pages de destination](../landing-pages/get-started-lp.md) :

* Un seul composant de **Formulaire** peut être utilisé dans une page principale unique.
* Le composant de **Formulaire** ne peut pas être utilisé dans les sous-pages.
* Vous ne pouvez pas ajouter de pré-en-tête à une page de destination.
* Vous ne pouvez pas sélectionner l’option **Coder le vôtre** lors de la conception d’une page de destination principale.

## Mécanismes de sécurisation des sous-domaines {#subdomain-guardrails}

Les mécanismes de sécurisation et les limitations qui s’appliquent à la délégation de sous-domaines dans Journey Optimizer sont décrits dans [cette page](../configuration/delegate-subdomain.md#guardrails).

## Mécanismes de sécurisation des fragments {#fragments-guardrails}

Les mécanismes de sécurisation suivants s’appliquent aux [fragments](../content-management/fragments.md) :

* Pour créer, modifier, archiver et publier des fragments, vous avez besoin des autorisations **[!DNL Manage library items]** et **[Publier le fragment]** incluses dans le profil de produit **[!DNL Content Library Manager]**. [En savoir plus](../administration/ootb-product-profiles.md#content-library-manager)
* Les fragments visuels ne sont disponibles que pour le canal E-mail.
* Les fragments d’expression ne sont pas disponibles pour les canaux In-app.
* Les fragments visuels ne doivent pas dépasser 100 Ko. Les fragments d’expression ne doivent pas dépasser 200 Ko.
* Pour utiliser un fragment dans un parcours ou une campagne, son statut doit être **Actif**.
* Les [attributs contextuels](../personalization/personalization-build-expressions.md) ne sont pas pris en charge dans les fragments.
* Les fragments visuels ne sont pas compatibles entre les modes Utiliser des thèmes et Style manuel. Pour pouvoir utiliser un fragment dans un contenu auquel vous souhaitez appliquer un thème, ce fragment doit être créé en mode Utiliser des thèmes. [En savoir plus sur les thèmes](../email/apply-email-themes.md)
* Lorsque le suivi est activé dans un parcours ou une campagne, si vous ajoutez des liens à un fragment et que ce fragment est utilisé dans un message, ces liens font l’objet d’un suivi comme tous les autres liens inclus dans le message. [En savoir plus sur les liens et le suivi](../email/message-tracking.md)

## Mécanismes de sécurisation des audiences et des profils {#audience}

* Vous pouvez publier jusqu’à 10 compositions d’audiences dans un sandbox donné. Si vous avez atteint ce seuil, vous devez supprimer une composition pour libérer de l’espace et en publier une nouvelle.

  En savoir plus sur les compositions d’audiences sur [cette page](../audience/get-started-audience-orchestration.md).

* Lors de l’ingestion de données, les e-mails sont sensibles à la casse. Cela signifie que des profils peuvent être créés en double (par exemple, un profil pour John.Greene@luma.com, un autre pour john.greene@luma.com) et utilisés lors du ciblage du destinataire correspondant dans vos parcours et campagnes [!DNL Journey Optimizer].

* Lors du ciblage de profils pseudonymes (visiteurs non authentifiés) avec des canaux entrants, pensez à définir une durée de vie (TTL) pour la suppression automatique des profils afin de maîtriser le nombre de profils engageables et les coûts associés. [En savoir plus](#profile-management-inbound)

## Mécanismes de sécurisation des décisions et de la gestion des décisions {#decisioning-guardrails}

Les mécanismes de sécurisation et les limitations à garder à l’esprit lorsque vous utilisez la prise de décision ou la gestion des décisions sont détaillés dans ces sections Prise de décision et gestion des décisions :

* [Mécanismes de sécurisation et limitations de la prise de décisions](../experience-decisioning/decisioning-guardrails.md)
* [Mécanismes de sécurisation et limitations de la gestion des décisions](../offers/decision-management-guardrails.md)

## Mécanismes de sécurisation des parcours {#journeys-guardrails}

### Mécanismes de sécurisation généraux des parcours {#journeys-guardrails-journeys}

* Le nombre d’activités d’un parcours est désormais limité à 50. Le nombre d’activités s’affiche dans la section supérieure gauche de la zone de travail du parcours. Cela permet de faciliter la lisibilité, l’assurance qualité et la résolution des problèmes.
* Par défaut, le nombre de parcours actifs, en pause ou testés à blanc à la fois est limité à 100.  Le nombre actuel de parcours s’affiche au-dessus de la zone de travail du parcours.
* Lorsque vous publiez des parcours, nous les mettons automatiquement à l’échelle et les ajustons pour garantir une stabilité et un débit maximaux. Lorsque vous approchez du jalon de 100 parcours actifs à la fois, une notification s’affiche dans l’interface utilisateur pour cette réalisation. Si cette notification s’affiche et que vous devez étendre vos parcours au-delà de 100 parcours actifs à la fois, créez un ticket pour l’assistance clientèle et nous vous aiderons à atteindre vos objectifs.
* Lorsque vous utilisez une qualification d’audience dans un parcours, cette activité de qualification d’audience peut demander jusqu’à 10 minutes avant d’être active et d’écouter les profils entrant ou sortant de l’audience.
* La taille maximale d’une instance de parcours pour un profil est de 1 Mo. Toutes les données collectées dans le cadre de l’exécution du parcours sont stockées dans cette instance de parcours. Par conséquent, les données d’un événement entrant, les informations de profil extraites d’Adobe Experience Platform, les réponses d’action personnalisée, etc. sont stockées dans cette instance de parcours et affectent la taille du parcours. Il est conseillé, lorsqu’un parcours commence par un événement, de limiter la taille maximale de cette payload d’événement (par exemple, à moins de 800 Ko), afin d’éviter d’atteindre cette limite après quelques activités, dans l’exécution du parcours. Lorsque cette limite est atteinte, le profil est au statut d’erreur et est exclu du parcours.
* Outre la temporisation utilisée dans les activités de parcours, il existe une temporisation globale qui n’est pas affichée dans l’interface et qui ne peut pas être modifiée. Cette temporisation globale arrête la progression des personnes dans le parcours 91 jours après leur entrée. [En savoir plus](../building-journeys/journey-properties.md#global_timeout)

### Restrictions du package Select pour les parcours unitaires {#select-package-limitations}

>[!NOTE]
>
>Ces restrictions ne s’appliquent pas aux parcours Lecture d’audience ou Événement métier avec le package **Select**. Si vous avez besoin d’une logique de parcours plus complexe avec plusieurs actions, conditions ou activités d’attente, envisagez de mettre à niveau votre package de licence ou d’utiliser des parcours Lecture d’audience, le cas échéant.

Pour les clientes et les clients qui utilisent le package de licence **Select**, les restrictions supplémentaires suivantes s’appliquent spécifiquement aux parcours unitaires, aux parcours commençant par un événement, ou à une qualification d’audience :

* **Package SELECT : une seule action autorisée dans un parcours unitaire (ERR_PKG_SELECT_8)** - Les parcours unitaires ne peuvent contenir qu’une seule activité d’action. Vous ne pouvez pas ajouter plusieurs activités d’action e-mail, notification push, SMS, ou autres, dans le même parcours.

* **Package SELECT : aucune condition autorisée dans les parcours unitaires (ERR_PKG_SELECT_7)** - Les activités de condition ne peuvent pas être utilisées dans les parcours unitaires. Le parcours doit suivre un unique chemin linéaire sans logique de branche.

* **Package SELECT : aucune attente autorisée dans les parcours unitaires (ERR_PKG_SELECT_6)** - Les activités d’attente ne peuvent pas être ajoutées aux parcours unitaires. Les actions doivent s’exécuter immédiatement, sans délai.

* **Package SELECT : la transition de délai d’expiration/d’erreur à partir du nœud doit pointer uniquement vers le nœud de fin (ERR_PKG_SELECT_2)** - Si vous configurez des transitions de délai d’expiration ou d’erreur pour une action, telle qu’une action d’e-mail, ces chemins doivent pointer directement vers un nœud de fin. Elles ne peuvent pas se connecter à d’autres activités ou actions dans le parcours.


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

* Une limitation de 300 000 appels de plus d’une minute est définie pour toutes les actions personnalisées, par hôte et par sandbox. La limite « par hôte » s’applique au niveau du domaine (par exemple, exemple.com). Cette limite est appliquée en tant que fenêtre glissante par sandbox et par point d’entrée, pour les points d’entrée dont le temps de réponse est inférieur à 0,75 seconde. Pour les points d’entrée dont le temps de réponse est supérieur à 0,75 seconde, une limite distincte de 150 000 appels par 30 secondes (également une fenêtre glissante) s’applique. Consultez [cette page](../action/about-custom-action-configuration.md). Cette limite a été définie en fonction de l’utilisation de la clientèle, afin de protéger les points d’entrée externes ciblés par des actions personnalisées. Si nécessaire, vous pouvez remplacer ce paramètre en définissant une limitation ou un ralentissement plus élevé via nos API de limitation/ralentissement. Consultez [cette page](../configuration/external-systems.md).
* L’URL de l’action personnalisée ne prend pas en charge les paramètres dynamiques.
* Les méthodes d’appel POST, PUT et GET sont prises en charge.
* Le nom du paramètre de la requête ou de l’en-tête ne doit pas commencer par « . » ou « $ »
* Les adresses IP ne sont pas autorisées.
* Les adresses d’Adobe internes (`.adobe.*`) ne sont pas autorisées dans les URL et les API.
* Les actions personnalisées intégrées ne peuvent pas être supprimées.
* Les actions personnalisées ne prennent en charge le format JSON que lors de l’utilisation de payloads de requêtes ou de réponses. Consultez [cette page](../action/about-custom-action-configuration.md#custom-actions-limitations).
* Lorsque vous choisissez un point d’entrée à cibler à l’aide d’une action personnalisée, assurez-vous de ce qui suit :

   * Ce point d’entrée peut prendre en charge le débit des parcours à l’aide de configurations de l’[API de limitation](../configuration/throttling.md) ou de l’[API de plafonnement](../configuration/capping.md) pour le limiter. Faites preuve de prudence si une configuration de limitation ne peut pas descendre sous 200 TPS. Tout point d’entrée ciblé doit prendre en charge au moins 200 TPS.
   * Ce point d’entrée doit avoir un temps de réponse aussi bas que possible. En fonction de votre débit prévu, un temps de réponse élevé peut avoir un impact sur le débit réel.

### Événements {#events-g}

Les mécanismes de sécurisation suivants s’appliquent aux [événements](../event/about-events.md) dans vos parcours :

* Journey Optimizer prend en charge un volume maximal de 5 000 événements de parcours entrants par seconde, sur tous les sandbox. Pour en savoir plus sur cette limitation, consultez [cette page](../event/about-events.md#event-thoughput).
* Les parcours déclenchés par un événement peuvent prendre jusqu’à 5 minutes pour traiter la première action du parcours.
* En ce qui concerne les événements générés par le système, les données de diffusion en continu utilisées pour initier un parcours client doivent d’abord être configurées dans Journey Optimizer pour obtenir un identifiant d’orchestration unique. Cet identifiant d’orchestration doit être ajouté à la payload de diffusion en continu entrant dans Adobe Experience Platform. Cette limitation ne s’applique pas aux événements basés sur une règle.
* Les événements métier ne peuvent pas être utilisés conjointement avec des événements unitaires ou des activités de qualification d’audience.
* Les parcours unitaires (qui commencent par un événement ou une qualification d’audience) incluent un mécanisme de sécurisation qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La rentrée du profil est temporairement bloquée par défaut pendant 5 minutes. Par exemple, si un événement déclenche un parcours à 12:01 pour un profil spécifique et qu’un autre événement se produit à 12:03 (qu’il s’agisse du même événement ou d’un autre déclenchant le même parcours), ce parcours ne reprendra pas pour ce profil.
* Journey Optimizer exige que les événements soient diffusés en continu vers Data Collection Core Service (DCCS) pour pouvoir déclencher un parcours. Les événements ingérés par lot ou les événements provenant de jeux de données Journey Optimizer internes (commentaires des messages, tracking e-mail, etc.) ne peuvent pas être utilisés pour déclencher un parcours. Pour les cas d’utilisation où vous ne pouvez pas obtenir d’événements en flux continu, vous devez créer une audience basée sur ces événements et utiliser l’activité **Lecture d’audience** à la place. La qualification d’audience peut techniquement être utilisée. Cette méthode n’est toutefois pas recommandée, car elle peut entraîner des difficultés en aval en fonction des actions utilisées.

### Sources de données {#data-sources-g}

Les mécanismes de sécurisation suivants s’appliquent aux [sources de données](../datasource/about-data-sources.md) dans vos parcours :

* Les sources de données externes peuvent être exploitées au cours d’un parcours client pour consulter des données externes en temps réel. Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.
* Les adresses d’Adobe internes (`.adobe.*`) ne sont pas autorisées dans les URL et les API.

>[!NOTE]
>
>Les réponses étant désormais prises en charge, vous devez utiliser des actions personnalisées au lieu de sources de données pour les cas d’utilisation de sources de données externes.

### Création de parcours et de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/la mise à jour de profils basés sur l’API dans Adobe Experience Platform. La cible de niveau de service (TSL) en termes de latence est d’atteindre moins de 1 minute entre l’ingestion et le profil unifié pour le 95e percentile des demandes, avec un volume de 20K demandes par seconde (DPS).

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

#### Activités de campagne {#ac-g}

Les mécanismes de sécurisation suivants s’appliquent aux activités **[!UICONTROL Campaign v7/v8]** et **[!UICONTROL Campaign Standard]** :

* Les activités Adobe Campaign ne peuvent pas être utilisées avec une activité Lecture d’audience ou Qualification d’audience.
* Les activités de campagne ne peuvent pas être utilisées avec les activités des autres canaux : Carte, Expérience basée sur du code, E-mail, Notification push, SMS, Messages in-app, Web.

#### Activité in-app {#in-app-activity-limitations}

Les mécanismes de sécurisation suivants s’appliquent à l’action **[!UICONTROL Message in-app]**. En savoir plus sur les messages in-app sur [cette page](../in-app/create-in-app.md).

* Cette fonctionnalité n’est actuellement pas disponible pour les clientes et clients du secteur de la santé.

* La personnalisation ne peut contenir que des attributs de profil.

* L’activité in-app ne peut pas être utilisée avec les activités Adobe Campaign.

* L’affichage in-app est lié à la durée de parcours, ce qui signifie que lorsque le parcours se termine pour un profil, tous les messages in-app de ce parcours ne s’affichent plus pour ce profil.  Par conséquent, il n’est pas possible d’arrêter un message in-app directement à partir d’une activité de parcours. Vous devez plutôt terminer le parcours entier pour que les messages in-app ne s’affichent pas sur le profil.

* En mode test, l’affichage in-app dépend de la durée de vie du parcours. Pour éviter que le parcours ne se termine trop tôt au cours du test, ajustez la valeur **[!UICONTROL Temps d’attente]** de vos activités **[!UICONTROL Attente]**.

* Les activités **[!UICONTROL Réaction]** ne peuvent pas être utilisées pour réagir à une ouverture ou un clic in-app.

* Un délai d’activation peut se produire entre le moment où le profil d’une personne atteint une activité in-app dans la zone de travail et le moment où ladite personne commence à voir ce message in-app.

* La taille du contenu du message in-app est limitée à 2 Mo. L’inclusion d’images de grande taille peut entraver le processus de publication.

#### Activité Saut {#jump-g}

Des mécanismes de sécurisation spécifiques s’appliquent à l’activité **[!UICONTROL Saut]**. Ils sont répertoriés sur [cette page](../building-journeys/jump.md#jump-limitations).

#### Activité Lecture d’audience {#read-segment-g}

Les mécanismes de sécurisation suivants s’appliquent à l’activité de parcours [Lecture d’audience](../building-journeys/read-audience.md) :

* Les audiences en flux continu sont toujours à jour, mais les audiences par lots ne sont pas calculées au moment de la récupération. Elles ne sont évaluées que tous les jours au moment de l’évaluation quotidienne des lots.
* Lors de leur entrée dans le parcours, les profils utilisent les valeurs d’attributs issues de l’instantané d’audience par lots. Cependant, lorsqu’un profil atteint une activité **Attente**, le parcours actualise automatiquement les attributs de profils en récupérant les dernières données à partir du service de profil unifié (UPS). Cela signifie que les attributs de profils peuvent changer au cours de l’exécution du parcours.
* Pour les parcours qui utilisent une activité **Lecture d’audience**, il y a un nombre maximal de parcours pouvant commencer exactement au même moment. Les nouvelles tentatives sont effectuées par le système, mais il est recommandé d’éviter de lancer plus de cinq parcours (avec **Lecture d’audience**, planifiés ou démarrant « dès que possible ») exactement au même moment, en les espaçant dans le temps, par exemple de 5 à 10 minutes. Pour en savoir plus sur les autorisations de parcours, consultez [cette section](../building-journeys/entry-management.md#journey-processing-rate).
* L’activité **Lecture d’audience** ne peut pas être utilisée avec les activités Adobe Campaign.
* L’activité **Lecture d’audience** ne peut être utilisée que comme première activité dans un parcours ou après une activité d’événement métier.
* Un parcours ne peut avoir qu’une seule activité **Lecture d’audience**.
* Consultez également les recommandations sur l’utilisation de l’activité **Lecture d’audience** sur [cette page](../building-journeys/read-audience.md).
* Les reprises sont appliquées par défaut sur les parcours déclenchés par l’audience (commençant par une **lecture d’audience** ou un **événement métier**) lors de la récupération du traitement d’export. Si une erreur se produit lors de la création du traitement d’export, des reprises sont effectuées toutes les 10 minutes, pendant 1 heure au maximum. Après cela, nous considérerons cela comme un échec. Ces types de parcours peuvent donc être exécutés jusqu’à 1 heure après l’heure planifiée.
* Pour les parcours qui utilisent des ID supplémentaires, le taux de lecture de l’activité Lecture d’audience pour chaque instance de parcours est limité à un maximum de 500 profils par seconde.

Consultez également [cette page](../building-journeys/read-audience.md#must-read).

#### Activité Mettre à jour un profil {#update-profile-g}

Des mécanismes de sécurisation spécifiques s’appliquent à l’activité **[!UICONTROL Mettre à jour un profil]**. Ils sont répertoriés sur [cette page](../building-journeys/update-profiles.md).

## Mécanismes de sécurisation de l’orchestration de campagne {#orchestration-guardrails}

Les mécanismes de sécurisation et les limitations à prendre en compte lorsque vous utilisez l’orchestration de campagne sont décrits dans cette section : [Mécanismes de sécurisation et limitations](../orchestrated/guardrails.md).
