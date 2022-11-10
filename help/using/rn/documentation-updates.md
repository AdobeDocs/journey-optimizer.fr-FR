---
solution: Journey Optimizer
product: journey optimizer
title: Mises à jour de la documentation
description: En savoir plus sur les mises de la documentation la plus récente
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: ca423c25d39162838368b2242c1aff99388df768
workflow-type: tm+mt
source-wordcount: '2128'
ht-degree: 100%

---

# Mises à jour de la documentation {#latest-updates}

Cette page répertorie toutes les mises à jour de la documentation d&#39;[!DNL Journey Optimizer].

## Octobre 2022 {#october-2022}

* Ajout d’un cas d’utilisation de parcours sur la manière de limiter le débit à l’aide de sources de données externes et d’actions personnalisées. [En savoir plus](../building-journeys/limit-throughput.md)
* La section Cas d’utilisation de parcours a été réorganisée en deux catégories : [Cas d’utilisation commerciale](../building-journeys/journeys-uc.md) et [Cas d’utilisation technique](../building-journeys/collections.md).
* La section **Jeu de données d’entité** a été mise à jour avec plus de détails. [En savoir plus](../start/datasets-query-examples.md#entity-dataset)
* Les informations relatives à la gestion des désinscriptions et aux politiques de consentement ont été réorganisées en une nouvelle section. [En savoir plus](../privacy/opt-out.md)
* La section sur les paramètres avancés des messages de parcours a été clarifiée et précise désormais que le remplacement des adresses e-mail ne doit être utilisé que pour des cas d’utilisation spécifiques. La plupart du temps, la valeur définie comme adresse principale dans les **Champs d’exécution** est celle qui doit être utilisée. [En savoir plus](../messages/messages-in-journeys.md#adv-settings)
* Ajout d’une note à la section **Configuration des sous-domaines de page de destination** pour indiquer que les majuscules ne sont pas autorisées dans les sous-domaines de la page de destination. [En savoir plus](../configuration/lp-subdomains.md)

## Septembre 2022 {#september-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version de septembre 2022 de [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Ajout d’une bonne pratique liée à l’utilisation des activités d’attente dans les parcours de lecture de segment récurrents. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Ajout d’exemples de requête d’événement d’étape, ainsi que d’informations sur la différence entre id, instanceid et profileid. [En savoir plus](../reports/query-examples.md).
* Mise à jour des pages relatives aux fonctions [toDateOnly](../building-journeys/functions/functiontodateonly.md) et [toString](../building-journeys/functions/functiontostring.md).
* Ajout de détails sur les paramètres de condition de temps. [En savoir plus](../building-journeys/condition-activity.md#time_condition)
* Ajout d’informations sur les jeux de données intégrés. [En savoir plus](../start/get-started-datasets.md#access-datasets)
* Les sections Rapport global et Rapport dynamique ont été réorganisées pour une meilleure lisibilité. [En savoir plus](../reports/global-report.md)
* Une liste de toutes les mesures de création de rapports disponibles dans Adobe Journey Optimizer a été ajoutée.
   [En savoir plus](../reports/global-report.md#email-and-sms-metrics)
* La section Envoyer l’e-mail en copie (Cci) a été déplacée vers la nouvelle page Prise en charge de l’archivage. [En savoir plus](../configuration/archiving-support.md)

## Août 2022 {#august-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] d’août 2022 ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* La section Règles de fréquence a été mise à jour pour prendre en compte le nouveau flux de messages en ligne. [En savoir plus](../configuration/frequency-rules.md#apply-frequency-rule)
* Une vidéo montrant comment configurer les abonnements et créer des pages de destination est désormais référencée dans la section « Prise en main des pages de destination ». [En savoir plus](../landing-pages/get-started-lp.md#video)
* Ajout d’une limitation pour les parcours utilisant les activités Lecture de segment. [En savoir plus](../building-journeys/read-segment.md)
* La page des opérateurs de l’éditeur d’expression a été améliorée. [En savoir plus](../building-journeys/expression/operators.md)
* Ajout d’une section sur la planification d’une campagne. [En savoir plus](../campaigns/create-campaign.md)
* Mise à jour de la section sur les règles de syntaxe générales de l’éditeur d’expression afin de prendre en compte la nouvelle règle concernant l’échappement du symbole barre oblique inverse dans les fonctions littérales. Les messages publiés existants ne sont pas affectés par cette modification. Seuls les nouveaux messages ou les brouillons doivent être mis à jour. [En savoir plus](../personalization/personalization-syntax.md#general-rules)

## Juillet 2022 {#july-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version du 22 juillet de [!DNL Journey Optimizer] sont présentées dans la documentation. [En savoir plus](release-notes.md)
* La section **Configurer des surfaces de canal** a été simplifiée et contient des liens vers la page décrivant comment configurer le canal SMS. [En savoir plus](../configuration/channel-surfaces.md#create-channel-surface)
* Dans les propriétés du parcours, l’option **Fuseau horaire du profil** est désormais désactivée par défaut. [En savoir plus](../building-journeys/timezone-management.md#timezone-from-profiles)
* Dans l’activité **Attente**, l’option **Date fixe** n’est plus disponible. [En savoir plus](../building-journeys/wait-activity.md)
* Des informations supplémentaires ont été ajoutées sur l’option **Lecture incrémentale** dans l’activité **Lecture de segment**. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Des recommandations ont été ajoutées concernant le type de condition **Limite de profil**. [En savoir plus](../building-journeys/condition-activity.md#profile_cap)
* Une limitation sur les événements métier a été ajoutée. [En savoir plus](../start/guardrails.md#events-g)

## Juin 2022 {#june-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] du 22 juin ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Une nouvelle section sur les demandes d’accès à des informations personnelles a été ajoutée à la documentation. [En savoir plus](../privacy/requests.md)
* Une nouvelle section sur les journaux d’audit des ressources a été ajoutée à la documentation. [En savoir plus](../privacy/audit-logs.md)
* Une nouvelle section sur la façon d’ajouter du contenu HTML ou JSON, provenant de la bibliothèque de ressources Adobe Experience Cloud, à un rendu d’offre a été ajoutée à la documentation. [En savoir plus](../offers/offer-library/add-representations.md#html-json)
* Ajout d’une nouvelle page sur le cycle de vie des parcours. [En savoir plus](../building-journeys/journey.md#journey-versions)
* Mise à jour de la page Activité d’attente. [En savoir plus](../building-journeys/wait-activity.md)
* Ajout de la liste des jeux de données Adobe Journey Optimizer avec des exemples de requête. [En savoir plus](../start/datasets-query-examples.md)
* La page Liste autorisée a été déplacée vers la section Configuration. [En savoir plus](../configuration/allow-list.md)
* La page Liste de suppression a été mise à jour afin de clarifier certaines informations, notamment le fait que tous les caractères ASCII compris entre 32 et 126 sont autorisés dans le champ de motif de suppression. [En savoir plus](../configuration/manage-suppression-list.md)
* Ajout du lien vers les barrières de sécurité et les limites statiques pour la gestion des décisions. [En savoir plus](../start/guardrails.md)
* L’optimisation de l’heure d’envoi est désormais disponible pour tous les clients. La mention Beta a été supprimée. [En savoir plus](../messages/send-time-optimization.md)
* L’API Batch Decisioning a été ajoutée à la liste des API disponibles pour diffuser des offres personnalisées. [En savoir plus](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## Mai 2022 {#may-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] du 22 mai ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* De nouveaux exemples de requête liés à la [qualification de segment](../reports/query-examples.md#segment-qualification-queries) et aux [événements](../reports/query-examples.md#event-based-queries) ont été ajoutés.
* La section Conception d’e-mail mentionne désormais les nouveaux modèles intégrés disponibles pour commencer le contenu. Les captures d’écran connexes ont été mises à jour. [En savoir plus](../design/design-emails.md)
* Des liens vers des ressources clés ont été mis à jour dans la page d’accueil de la documentation Journey Optimizer.
* Les captures d’écran pour les rapports d’abonnement et de page de destination ont été mises à jour. [En savoir plus](../reports/live-report.md)
* Une note a été ajoutée indiquant que la méthode Delete n’est pas prise en charge dans les actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md)
* Des liens vers des vidéos pratiques ont été mis à jour.
* Les sections [Configuration du canal e-mail](../configuration/about-subdomain-delegation.md), [Préréglages de message](../configuration/channel-surfaces.md) et [Configuration des pages de destination](../configuration/lp-subdomains.md) ont été réorganisées afin d’en améliorer la lisibilité.
* La section Tracking des URL a été mise à jour et enrichie avec des exemples. [En savoir plus](../configuration/email-settings.md#url-tracking)
* Ajout d’une nouvelle sous-section sur la configuration d’une adresse e-mail de transfert. Notez que vous ne pouvez pas le faire via l’interface utilisateur. [En savoir plus](../configuration/email-settings.md#forward-email)

## Avril 2022 {#april-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version d’avril 2022 de [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* La page de documentation sur les événements de **réaction** a été mise à jour. [En savoir plus](../building-journeys/reaction-events.md)
* Les vidéos relatives aux fonctionnalités de gestion des décisions ont été mises à jour pour refléter l’interface utilisateur de Journey Optimizer. [En savoir plus](../offers/get-started/starting-offer-decisioning.md)
* La section **Prise en main des jeux de données** a été améliorée afin d’expliquer en détail comment accéder aux jeux de données et les créer. [En savoir plus](../start/get-started-datasets.md)
* Des liens vers les guides d’aide et les notes de mise à jour du produit ont été ajoutés à la page d’accueil de la **Documentation d’Adobe Journey Optimizer**. [En savoir plus](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=fr)
* La section **Créer des paramètres prédéfinis de messages** indique désormais que vous ne pouvez pas procéder à la création de paramètres prédéfinis tant que le groupe d’adresses IP sélectionné est en cours d’édition (statut de **[!UICONTROL traitement]**) et n’a jamais été associé au sous-domaine sélectionné. [En savoir plus](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* La section **Suivi des URL** des paramètres prédéfinis de messages a été mise à jour pour refléter des changements mineurs dans l’interface utilisateur. [En savoir plus](../configuration/channel-surfaces.md#url-tracking)

## Mars 2022 {#march-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] de mars 2022 ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Ajout dʼune nouvelle page sur la prise en main des modèles dʼIA dans la section **Offer Decisioning**, comprenant une description approfondie du [modèle d’optimisation automatique](../offers/ranking/auto-optimization-model.md), l’algorithme qu’il utilise et dʼautres détails techniques. [En savoir plus](../offers/ranking/ai-models.md)
* La page de création du profil de test a été déplacée vers la section **Segment, profils et identité**. [En savoir plus](../segment/creating-test-profiles.md)
* Ajout d’un exemple sur l’ajout d’une expression en tant que valeur par défaut dans l’éditeur d’expression. [En savoir plus](../building-journeys/expression/field-references.md#default-value)
* La section **Créer des offres personnalisées** a été réorganisée pour en améliorer la lisibilité. [En savoir plus](../offers/offer-library/creating-personalized-offers.md)
* Une nouvelle section a été ajoutée pour décrire les impacts que la modification des dates de début et/ou de fin d’une offre peut avoir sur le capping de la fréquence de cette offre. [En savoir plus](../offers/offer-library/add-constraints.md#capping-change-date)
* La section **Modifier les adresses e-mail principales** a été mise à jour pour prendre en compte les modifications apportées à l’interface utilisateur. [En savoir plus](../configuration/primary-email-addresses.md)

## Février 2022 {#feb-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] du 22 février ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Les pages de documentation des fonctions [replace](../building-journeys/functions/functionreplace.md#example_2) et [replaceAll](../building-journeys/functions/functionreplaceall.md#example) ont été mises à jour avec des informations supplémentaires et des exemples concernant le paramètre cible.
* Les bonnes pratiques ont été ajoutées à la page [Opérateurs](../building-journeys/expression/operators.md#important-notes).

## Janvier 2022 {#january-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version de janvier 2022 de [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Mise à jour de la section **Classements par l’IA dʼOffer Decisioning** afin de fournir une description plus détaillée du modèle d’optimisation automatique. [En savoir plus](../offers/ranking/auto-optimization-model.md)
* Ajout d’une nouvelle section sur les exigences relatives aux schémas requises pour pouvoir envoyer des types d’événement lors de l’utilisation d’une stratégie de classement. [En savoir plus](../offers/ranking/schema-requirement.md)
* La section relative aux capacités de personnalisation de [!DNL Journey Optimizer] a été réorganisée pour une meilleure lisibilité. [En savoir plus](../personalization/personalize.md)
* La section **Création de préréglages de message** a été divisée en plusieurs sections afin d’en améliorer la clarté. [En savoir plus](../configuration/channel-surfaces.md#create-channel-surface)
* La section **Gestion des processus d’opt-out** a été clarifiée et légèrement réorganisée. [En savoir plus](../privacy/opt-out.md#opt-out-management)
* La section **Insérer des liens** a été mise à jour pour prendre en compte les modifications récentes de l’interface utilisateur. [En savoir plus](../design/message-tracking.md#insert-links)

## Novembre 2021 {#november-2021}

* Une description complète de l’**éditeur d’expression avancé** utilisé dans les parcours est désormais disponible. [En savoir plus](../building-journeys/expression/expressionadvanced.md)
* Ajout d’une section sur la **méthode de délégation de sous-domaines CNAME**. [En savoir plus](../configuration/delegate-subdomain.md#cname-subdomain-delegation)


## Octobre 2021 {#october-2021}

* Toutes les nouvelles fonctionnalités et améliorations apportées à la version d’octobre 2021 de [!DNL Journey Optimizer] ont été détaillées dans la documentation. [En savoir plus](release-notes.md)
* Ajout de la liste des **fonctions Date/heure**. [En savoir plus](../personalization/functions/dates.md)
* Nouvelles **sections Prise en main par personnage utilisateur**. Tracez votre propre chemin pour atteindre plus rapidement vos objectifs ! [En savoir plus](../start/quick-start.md)
* Nouvelle section **Modification d’un préréglage de message**. [En savoir plus](../configuration/channel-surfaces.md#edit-channel-surface)
* Nouvelle section **Modification d’un enregistrement PTR**. [En savoir plus](../configuration/ptr-records.md#edit-ptr-record)
* Nouvelle section **Désactivation d’un préréglage de message**. [En savoir plus](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
* Nouvelles limitations ajoutées au **guide du développeur de l’API de gestion des décisions** sur les contraintes d’offre non prises en charge par les workflows mobiles d’[!DNL Experience Edge]. [En savoir plus](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* Nouvelle section **Créer des simulations**. [En savoir plus](../offers/offer-activities/simulation.md)
* Mise à jour de la section **Ajouter des portées de décision**. [En savoir plus](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Mise à jour de la section **Définir le contenu de vos représentations**, y compris une nouvelle [sous-section](../offers/offer-library/creating-personalized-offers.md#custom-text) sur la façon de définir et de personnaliser le texte personnalisé. [En savoir plus](../offers/offer-library/creating-personalized-offers.md#content)

## Septembre 2021 {#september-2021}

* Les pages de fonctions suivantes ont été mises à jour : [sethours](../building-journeys/functions/functionsethours.md), [getListItem](../building-journeys/functions/functiongetlistitem.md), [inSegment](../building-journeys/functions/functioninsegment.md)

* Les fonctions suivantes ont été ajoutées : [filter](../building-journeys/functions/functionfilter.md), [intersect](../building-journeys/functions/functionintersect.md), [toDateOnly](../building-journeys/functions/functiontodateonly.md)

* Le type de date dateOnly a été ajouté à la documentation de l’éditeur d’expression. [En savoir plus](../building-journeys/expression/data-types.md)

* Ajout d’informations sur la durée de mise en cache des actions personnalisées. [En savoir plus](../datasource/external-data-sources.md#custom-authentication-mode)

* Ajout d’informations sur les ports par défaut des actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration)

* Ajout d’informations sur plusieurs cas d’utilisation d’événements métier. [En savoir plus](../event/about-creating-business.md#multiple-business-events)

* Ajout d’exemples fréquemment utilisés pour interroger les événements d’étape de parcours dans le lac de données. [En savoir plus](../reports/query-examples.md)

* Ajout d’une nouvelle page **Limites**. [En savoir plus](../start/guardrails.md)

* Amélioration de la page **Démarrage rapide** avec des étapes pour différents rôles. [En savoir plus](../start/quick-start.md)

* Désormais, toutes les fonctionnalités de gestion des décisions décrites dans la section dédiée s’appliquent également aux utilisateurs d’Adobe Experience Platform qui tirent parti du service applicatif Offer Decisioning.
[En savoir plus](../offers/get-started/starting-offer-decisioning.md)

* Ajout d’une sous-section pour clarifier les différences entre l’utilisation des segments et celle des règles de décision lors de l’application d’une contrainte afin de restreindre la sélection des offres pour un emplacement donné. [En savoir plus](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* Ajout d’exemples de formule de classement spécifiques pour illustrer certains cas d’utilisation réels. [En savoir plus](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Ajout d’une sous-section sur la modification des groupes d’adresses IP. [En savoir plus](../configuration/ip-pools.md#edit-ip-pool)


## Août 2021 {#august-2021}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] du 21 août ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Mise à jour des autorisations de la gestion des décisions. [En savoir plus](../administration/ootb-product-profiles.md)
* Mise à jour des captures d’écran du concepteur d’e-mails avec la dernière interface utilisateur.
* Mise à jour de la procédure de configuration pour les actions personnalisées avec les chemins d’URL dynamiques et les en-têtes dynamiques. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration)
* Ajout d’une section sur les fonctions d’accessibilité et les raccourcis. [En savoir plus](../start/user-interface.md#accessibility)
* Ajout d’une section sur les méthodes d’évaluation de segment. [En savoir plus](../segment/about-segments.md#evaluation-method-in-journey-optimizer)
* Ajout de notes aux sections de rapport Liste de suppression, Liste autorisée et E-mail global/direct pour indiquer que les profils avec les statuts Supprimé et Non autorisé sont exclus des mesures Envoyer le rapport par e-mail. [En savoir plus](../reports/global-report.md)
* Ajout d’une nouvelle section pour décrire comment récupérer les adresses électroniques ou les domaines qui ont été exclus d’un envoi car ils ne se trouvaient pas sur la liste autorisée. [En savoir plus](../configuration/allow-list.md#reporting)
* Mise à jour de la section Activation de la liste autorisée. [En savoir plus](../configuration/allow-list.md#enable-allow-list)
* Mise à jour de la section Surveillance des préréglages du message avec les raisons possibles d’échec de la création des préréglages et des détails sur ces erreurs. [En savoir plus](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Mise à jour et changement du nom de la section Période de reprise afin de tenir compte du fait que vous pouvez désormais ajuster le paramètre de nouvelle tentative d’e-mail dans les préréglages du message. [En savoir plus](../configuration/retries.md#retry-duration)
* Ajout d’une nouvelle section décrivant comment insérer un lien d’opt-out en un clic dans le contenu d’un e-mail. [En savoir plus](../privacy/opt-out.md#one-click-opt-out-link)
* Mise à jour de la section Délégation d’un sous-domaine avec des informations plus détaillées sur le processus de validation effectué par Adobe. [En savoir plus](../configuration/delegate-subdomain.md#subdomain-validation)
* Ajout d’une section décrivant comment ajouter manuellement des adresses e-mail et des domaines à la liste de suppression. [En savoir plus](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Mise à jour des sections [Accéder à la liste de suppression](../configuration/manage-suppression-list.md#access-suppression-list) et [Reprises](../configuration/retries.md) pour refléter la nouvelle interface utilisateur.
* Le nouveau flux pour ajouter et configurer des représentations lors de la création d&#39;une offre a été documenté. [En savoir plus](../offers/offer-library/creating-personalized-offers.md#representations)


## Juillet 2021 {#july-2021}

* Toutes les nouvelles fonctionnalités et améliorations de la version du 21 juillet avec [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Ajout de liens directs vers la documentation des services Experience Platform dans la page d’accueil [!DNL Journey Optimizer] et la table des matières.
* Nouvelles pages de destination pour les services Experience Platform disponibles dans [!DNL Journey Optimizer]
* Ajout de liens vers la description du produit [!DNL Journey Optimizer] dans la page d’accueil.
* Ajout de tutoriels vidéo à plusieurs pages
* Image optimisée de la page d’accueil
* Déplacement, amélioration et changement du nom de la section « Suivi des messages » en « Ajout de liens et suivi des messages ». [En savoir plus](../design/message-tracking.md)
* Ajout d’une sous-section aux pages miroir. [En savoir plus](../design/message-tracking.md#mirror-page)
* Renommez « activités d’offre » en « décisions » et « décisions » en « portées de décision » dans la documentation et les écrans. [En savoir plus](../offers/get-started/starting-offer-decisioning.md)
* Nouveau cas d’utilisation : [personnaliser un message avec des fonctions helper](../personalization/personalization-use-case-helper-functions.md)
* Mise à jour de la documentation sur Lecture de segment pour prendre en compte les impacts sur les segments matérialisés. [En savoir plus](../building-journeys/read-segment.md)
* Mise à jour des limites de parcours. [En savoir plus](../start/guardrails.md)
* Mise à jour de la section Configurer la sélection des offres dans les décisions. [En savoir plus](../offers/offer-activities/configure-offer-selection.md)
* Ajout d&#39;un avertissement indiquant que les offres basées sur un événement ne sont actuellement pas prises en charge. [En savoir plus](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documentation du nouvel onglet **[!UICONTROL Aperçu]** de la gestion des décisions. [En savoir plus](../offers/get-started/user-interface.md#overview)
* Ajout de nouvelles sections pour décrire les actions disponibles dans les listes des offres et des décisions : [Liste des offres](../offers/offer-library/creating-personalized-offers.md#offer-list) et [Liste des décisions](../offers/offer-activities/create-offer-activities.md#decision-list).

