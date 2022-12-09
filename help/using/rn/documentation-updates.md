---
solution: Journey Optimizer
product: journey optimizer
title: Mises à jour de la documentation
description: En savoir plus sur les dernières mises à jour de la documentation
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '2235'
ht-degree: 0%

---

# Mises à jour de la documentation {#latest-updates}

Cette page répertorie toutes les mises à jour de la documentation pour [!DNL Journey Optimizer].

## Décembre 2022 {#december-2022}

* Le guide Messages a été réorganisé et divisé en guides dédiés pour chaque canal :

   * [Canal email](../email/get-started-email.md)
   * [Canal des notifications push](../push/get-started-push.md)
   * [Canal SMS](../sms/get-started-sms.md)

## Novembre 2022 {#november-2022}

* Ajout d’une nouvelle page sur les intégrations de Journey Optimizer. [En savoir plus](../start/ajo-integrations.md)
* Ajout d’une recommandation sur la longueur des URL de pages miroir. [En savoir plus](../email/message-tracking.md)
* Une nouvelle sous-section dans la configuration des paramètres de courrier électronique a été ajoutée à la réponse à l’adresse électronique, y compris des recommandations pour assurer une gestion adéquate des réponses. [En savoir plus](../email/email-settings.md#reply-to-email)
* Ajout d’une section sur la modification du contenu d’un message dans un parcours actif. [En savoir plus](../building-journeys/journeys-message.md#update-live-content)

## Octobre 2022 {#october-2022}

* Ajout d’un cas pratique de parcours sur la manière de limiter le débit à l’aide de sources de données externes et d’actions personnalisées. [En savoir plus](../building-journeys/limit-throughput.md)
* La section Cas pratique de parcours a été réorganisée en deux catégories : [Cas d’utilisation métier](../building-journeys/journeys-uc.md) et [Cas d’utilisation technique](../building-journeys/collections.md).
* Le **Jeu de données d’entité** a été mise à jour avec plus de détails. [En savoir plus](../data/datasets-query-examples.md#entity-dataset)
* Les sections Gestion des opt-out et Stratégies de consentement ont été réorganisées. [En savoir plus](../privacy/opt-out.md)
* La section sur les paramètres avancés des messages de parcours a été clarifiée et précise désormais que le remplacement de l’adresse électronique ne doit être utilisé que pour des cas d’utilisation spécifiques. La plupart du temps, la valeur définie comme adresse principale dans la variable **Champs d&#39;exécution** est celui qui doit être utilisé.
* Ajout d’une note au **Configuration des sous-domaines de landing page** pour indiquer que les majuscules ne sont pas autorisées dans les sous-domaines de la page d’entrée. [En savoir plus](../landing-pages/lp-subdomains.md)

## Septembre 2022 {#september-2022}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 22 septembre a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* Ajout d’une bonne pratique liée à l’utilisation des activités d’attente dans les parcours de segments de lecture récurrente. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Ajout d’exemples de requête d’événement d’étape, ainsi que d’informations sur la différence entre id, instanceid et profileid. [En savoir plus](../reports/query-examples.md).
* Mise à jour des pages relatives au [toDateOnly](../building-journeys/functions/functiontodateonly.md) et [toString](../building-journeys/functions/functiontostring.md) fonctions.
* Ajout de détails sur les paramètres de condition de temps. [En savoir plus](../building-journeys/condition-activity.md#time_condition)
* Ajout d’informations sur les jeux de données intégrés. [En savoir plus](../data/get-started-datasets.md#access-datasets)
* Les sections Rapport global et Rapport en direct ont été améliorées et réorganisées. [En savoir plus](../reports/global-report.md)
* Une liste de toutes les mesures de création de rapports disponibles dans Adobe Journey Optimizer a été ajoutée.
   [En savoir plus](../reports/global-report.md#email-and-sms-metrics)
* La section Email en Cci a été déplacée vers la nouvelle page Assistance pour l&#39;archivage. [En savoir plus](../configuration/archiving-support.md)

## Août 2022 {#august-2022}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 22 août a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* La section Règles de fréquence a été mise à jour pour prendre en compte le nouveau flux de messages en ligne. [En savoir plus](../configuration/frequency-rules.md#apply-frequency-rule)
* Une vidéo montrant comment configurer les abonnements et créer des landing pages est maintenant référencée dans la section Prise en main des landing pages . [En savoir plus](../landing-pages/get-started-lp.md#video)
* Une limitation a été ajoutée pour les parcours utilisant les activités Lecture de segment . [En savoir plus](../building-journeys/read-segment.md)
* La page des opérateurs de l&#39;éditeur d&#39;expression a été améliorée. [En savoir plus](../building-journeys/expression/operators.md)
* Ajout d’une section sur la planification d’une campagne - [En savoir plus](../campaigns/create-campaign.md)
* Mise à jour de la section sur les règles de syntaxe générales de l’éditeur d’expression afin de prendre en compte la nouvelle règle concernant l’échappement des symboles de barre oblique inverse dans les fonctions littérales - Les messages publiés existants ne sont pas affectés par cette modification. Seuls les nouveaux messages ou les brouillons doivent être mis à jour. [En savoir plus](../personalization/personalization-syntax.md#general-rules)

## Juillet 2022 {#july-2022}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 22 juillet a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* Le **Configuration des surfaces de canal** Clarification et mise à jour de la section avec des liens vers la page décrivant comment configurer le canal SMS - [En savoir plus](../configuration/channel-surfaces.md#create-channel-surface)
* Dans les propriétés du parcours, la variable **Fuseau horaire du profil** est désormais désactivée par défaut. [En savoir plus](../building-journeys/timezone-management.md#timezone-from-profiles)
* Dans le **Attente** l’activité **Date fixe** n’est plus disponible. [En savoir plus](../building-journeys/wait-activity.md)
* Ajout d’informations supplémentaires sur la variable **Lecture incrémentale** dans le **Lecture de segment** activité. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Ajout de recommandations sur la **Limite de profil** type de condition. [En savoir plus](../building-journeys/condition-activity.md#profile_cap)
* Ajout d’une limitation sur les événements professionnels. [En savoir plus](../start/guardrails.md#events-g)

## Juin 2022 {#june-2022}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 22 juin a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* Une nouvelle section sur les demandes d’accès à des informations personnelles a été ajoutée à la documentation. [En savoir plus](../privacy/requests.md)
* Une nouvelle section sur les journaux d’audit des ressources a été ajoutée à la documentation. [En savoir plus](../privacy/audit-logs.md)
* Une nouvelle section sur l’ajout à une représentation d’offre d’un contenu HTML ou JSON provenant de la bibliothèque de ressources Adobe Experience Cloud a été ajoutée à la documentation. [En savoir plus](../offers/offer-library/add-representations.md#html-json)
* Ajout d’une nouvelle page sur le cycle de vie du parcours. [En savoir plus](../building-journeys/journey.md#journey-versions)
* Mise à jour de la page Activité Attente . [En savoir plus](../building-journeys/wait-activity.md)
* Ajout de la liste des jeux de données Adobe Journey Optimizer avec des exemples de requête. [En savoir plus](../data/datasets-query-examples.md)
* La page Liste autorisée a été déplacée vers la section Configuration . [En savoir plus](../configuration/allow-list.md)
* La page Liste de suppression a été mise à jour afin de clarifier certaines informations, notamment le fait que tous les caractères ASCII compris entre 32 et 126 sont autorisés dans le champ de motif de suppression. [En savoir plus](../configuration/manage-suppression-list.md)
* Ajout du lien vers les barrières de sécurité et les limites statiques pour la gestion des décisions - [En savoir plus](../start/guardrails.md)
* L’optimisation du temps d’envoi est désormais disponible pour tous les clients. La mention bêta a été supprimée. [En savoir plus](../building-journeys/journeys-message.md#send-time-optimization)
* L’API Batch Decisioning a été ajoutée à la liste des API disponibles pour diffuser des offres personnalisées. [En savoir plus](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## Mai 2022 {#may-2022}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 22 mai a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* Nouveaux exemples de requête liés à [qualification de segment](../reports/query-examples.md#segment-qualification-queries) et [events](../reports/query-examples.md#event-based-queries) ont été ajoutés.
* La section Conception d’emails mentionne désormais les nouveaux modèles natifs disponibles pour commencer le contenu. Les captures d’écran connexes ont été mises à jour. [En savoir plus](../email/get-started-email-design.md)
* Des liens vers des ressources clés ont été mis à jour dans la page d’accueil de la documentation de Journey Optimizer.
* Mise à jour des captures d’écran pour les rapports de landing page et d’abonnement - [En savoir plus](../reports/live-report.md)
* Une note a été ajoutée indiquant que la méthode Delete n’est pas prise en charge dans les actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md)
* Des liens vers des vidéos pratiques ont été mis à jour.
* Le [Configuration des emails](../configuration/about-subdomain-delegation.md), [Paramètres prédéfinis de message](../configuration/channel-surfaces.md) et [Configuration des landing pages](../landing-pages/lp-subdomains.md) ont été réorganisées afin d’en améliorer la lisibilité.
* Mise à jour et amélioration de la section sur le suivi des URL avec des exemples - [En savoir plus](../email/email-settings.md#url-tracking)
* Ajout d’une nouvelle sous-section sur la configuration d’une adresse électronique de transfert - Notez que vous ne pouvez pas le faire via l’interface utilisateur. [En savoir plus](../email/email-settings.md#forward-email)

## Avril 2022 {#april-2022}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 22 avril a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* Le **réactions** mise à jour de la page de documentation sur les événements - [En savoir plus](../building-journeys/reaction-events.md)
* Mise à jour des vidéos relatives aux fonctionnalités de gestion de la décision pour prendre en compte l’interface utilisateur de Journey Optimizer - [En savoir plus](../offers/get-started/starting-offer-decisioning.md)
* Le **Prise en main des jeux de données** La section a été améliorée afin d’expliquer en détail comment accéder aux jeux de données et les créer. [En savoir plus](../data/get-started-datasets.md)
* Des liens vers des guides d’aide et des notes de mise à jour de produit ont été ajoutés au **Documentation d’Adobe Journey Optimizer** page d’accueil. [En savoir plus](https://experienceleague.adobe.com/docs/journey-optimizer.html)
* Le **Création de paramètres de message prédéfinis** indique désormais que vous ne pouvez pas procéder à la création de paramètres prédéfinis pendant que le pool d’adresses IP sélectionné est en cours d’édition (**[!UICONTROL Processing]** (status) et n’a jamais été associé au sous-domaine sélectionné. [En savoir plus](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* Paramètres prédéfinis du message **Suivi des URL** a été mise à jour pour prendre en compte des modifications mineures de l’interface utilisateur. [En savoir plus](../configuration/channel-surfaces.md#url-tracking)

## Mars 2022 {#march-2022}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 22 mars a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* Une nouvelle page sur la prise en main des modèles d’IA a été ajoutée au **Offer Decisioning** la section [modèle d’optimisation automatique](../offers/ranking/auto-optimization-model.md), l’algorithme qu’il utilise et des détails plus techniques. [En savoir plus](../offers/ranking/ai-models.md)
* La page de création du profil de test a été déplacée vers le  **Segment, profils et identité** . [En savoir plus](../segment/creating-test-profiles.md)
* Ajout d’un exemple sur l’ajout d’une expression en tant que valeur par défaut dans l’éditeur d’expression. [En savoir plus](../building-journeys/expression/field-references.md#default-value)
* Le **Créer des offres personnalisées** a été réorganisée pour en améliorer la lisibilité. [En savoir plus](../offers/offer-library/creating-personalized-offers.md)
* Une nouvelle section a été ajoutée pour décrire les impacts que la modification des dates de début et/ou de fin d’une offre peut avoir sur la limitation de fréquence de cette offre. [En savoir plus](../offers/offer-library/add-constraints.md#capping-change-date)
* Le **Modifier les adresses email principales** a été mise à jour pour prendre en compte les modifications apportées à l’interface utilisateur. [En savoir plus](../configuration/primary-email-addresses.md)

## Février 2022 {#feb-2022}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 22 février a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* Le [replace](../building-journeys/functions/functionreplace.md#example_2) et [replaceAll](../building-journeys/functions/functionreplaceall.md#example) les pages de documentation des fonctions ont été mises à jour avec des informations supplémentaires et des exemples concernant le paramètre target.
* Les bonnes pratiques ont été ajoutées à la variable [Opérateurs](../building-journeys/expression/operators.md#important-notes) page.

## Janvier 2022 {#january-2022}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 22 janvier a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* Le **Classement d’AI Offer Decisioning** Mise à jour de la section avec une description plus détaillée du modèle d’optimisation automatique - [En savoir plus](../offers/ranking/auto-optimization-model.md)
* Ajout d’une nouvelle section sur les exigences de schéma pour pouvoir envoyer des types d’événements lors de l’utilisation d’une stratégie de classement - [En savoir plus](../offers/ranking/schema-requirement.md)
* La section relative à [!DNL Journey Optimizer] les fonctionnalités de personnalisation ont été réorganisées pour une meilleure lisibilité. [En savoir plus](../personalization/personalize.md)
* Le **Création de paramètres de message prédéfinis** a été divisée en plusieurs sections afin d’en améliorer la clarté. [En savoir plus](../configuration/channel-surfaces.md#create-channel-surface)
* Le **Gestion des opt-out** a été clarifiée et légèrement réorganisée. [En savoir plus](../privacy/opt-out.md#opt-out-management)
* Le **Insérer des liens** a été mise à jour pour prendre en compte les modifications récentes de l’interface utilisateur d’ . [En savoir plus](../email/message-tracking.md#insert-links)

## Novembre 2021 {#november-2021}

* Une description complète de la variable **éditeur d’expression avancé** utilisé dans les parcours est désormais disponible. [En savoir plus](../building-journeys/expression/expressionadvanced.md)
* Nouvelle section à propos de **Méthode de délégation de sous-domaine CNAME** a été ajouté. [En savoir plus](../configuration/delegate-subdomain.md#cname-subdomain-delegation)


## Octobre 2021 {#october-2021}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 21 octobre a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* Ajout **Date et heure** liste. [En savoir plus](../personalization/functions/dates.md)
* Nouveau **Sections de prise en main par persona utilisateur**. Prenez votre propre chemin pour atteindre vos objectifs plus rapidement ! [En savoir plus](../start/quick-start.md)
* Nouveau **Modifier un paramètre prédéfini de message** . [En savoir plus](../configuration/channel-surfaces.md#edit-channel-surface)
* Nouveau **Modification d’un enregistrement PTR** . [En savoir plus](../configuration/ptr-records.md#edit-ptr-record)
* Nouveau **Désactivation d’un paramètre prédéfini de message** . [En savoir plus](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
* Nouvelles limites ajoutées à la variable **Guide de développement de l’API Decision Management** sur les contraintes d’offre non prises en charge avec le mobile [!DNL Experience Edge] workflows. [En savoir plus](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* Nouveau **Créer des simulations** . [En savoir plus](../offers/offer-activities/simulation.md)
* Mise à jour **Ajout de portées de décision** . [En savoir plus](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Mise à jour **Définition du contenu de vos représentations** , y compris une nouvelle section [sous-section](../offers/offer-library/creating-personalized-offers.md#custom-text) sur la définition et la personnalisation du texte personnalisé. [En savoir plus](../offers/offer-library/creating-personalized-offers.md#content)

## Septembre 2021 {#september-2021}

* Les pages de fonctions suivantes ont été mises à jour : [sethours](../building-journeys/functions/functionsethours.md), [getListItem](../building-journeys/functions/functiongetlistitem.md), [inSegment](../building-journeys/functions/functioninsegment.md)

* Les fonctions suivantes ont été ajoutées : [filter](../building-journeys/functions/functionfilter.md), [intersection](../building-journeys/functions/functionintersect.md), [toDateOnly](../building-journeys/functions/functiontodateonly.md)

* Le type de date date dateOnly a été ajouté à la documentation de l’éditeur d’expression. [En savoir plus](../building-journeys/expression/data-types.md)

* Ajout d’informations sur la durée du cache d’action personnalisée. [En savoir plus](../datasource/external-data-sources.md#custom-authentication-mode)

* Ajout d’informations sur les ports par défaut des actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration)

* Ajout d’informations sur plusieurs cas d’utilisation d’événements professionnels. [En savoir plus](../event/about-creating-business.md#multiple-business-events)

* Ajout d’exemples fréquemment utilisés pour interroger les événements d’étape du parcours dans le lac de données. [En savoir plus](../reports/query-examples.md)

* Ajout d’une nouvelle **Limites** page. [En savoir plus](../start/guardrails.md)

* Amélioration de la fonction **Démarrage rapide** avec des étapes pour différentes personnes. [En savoir plus](../start/quick-start.md)

* Désormais, toutes les fonctionnalités de gestion de la décision décrites dans la section dédiée s’appliquent également aux utilisateurs d’Adobe Experience Platform qui exploitent le service d’application Offer Decisioning. [En savoir plus](../offers/get-started/starting-offer-decisioning.md)

* Ajout d’une sous-section afin de clarifier les différences entre l’utilisation de segments et de règles de décision lors de l’application d’une contrainte afin de restreindre la sélection des offres pour un emplacement donné. [En savoir plus](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* Ajout d’exemples de formule de classement spécifiques pour illustrer certains cas d’utilisation réels. [En savoir plus](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Ajout d’une sous-section sur la modification des pools d’adresses IP. [En savoir plus](../configuration/ip-pools.md#edit-ip-pool)


## Août 2021 {#august-2021}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 21 août a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* Mise à jour des autorisations de la gestion des décisions. [En savoir plus](../administration/ootb-product-profiles.md)
* Mise à jour des captures d’écran du concepteur d’emails avec la dernière interface utilisateur.
* Mise à jour de la procédure de configuration pour les actions personnalisées avec les chemins d’URL dynamiques et les en-têtes dynamiques. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration)
* Ajout d’une section sur les fonctions d’accessibilité et les raccourcis. [En savoir plus](../start/user-interface.md#accessibility)
* Ajout d’une section sur les méthodes d’évaluation de segment. [En savoir plus](../segment/about-segments.md#evaluation-method-in-journey-optimizer)
* Ajout de notes aux sections Liste de suppression, Liste autorisée et Rapport global/en direct d’e-mail pour indiquer que les profils avec les états Supprimés et Non autorisés sont exclus des mesures Envoyer le rapport par e-mail. [En savoir plus](../reports/global-report.md)
* Ajout d’une nouvelle section pour décrire comment récupérer les adresses électroniques ou les domaines qui ont été exclus d’un envoi car ils ne figuraient pas dans la liste autorisée. [En savoir plus](../configuration/allow-list.md#reporting)
* Mise à jour de la section Activer la liste autorisée . [En savoir plus](../configuration/allow-list.md#enable-allow-list)
* Mise à jour de la section Surveillance des paramètres prédéfinis du message avec les raisons possibles d’échec de la création des paramètres prédéfinis et des détails sur ces erreurs. [En savoir plus](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Mise à jour et changement du nom de la section Période des reprises afin de tenir compte du fait que vous pouvez désormais ajuster le paramètre de nouvelle tentative d’email dans les paramètres prédéfinis du message. [En savoir plus](../configuration/retries.md#retry-duration)
* Ajout d’une nouvelle section décrivant comment insérer un lien d’exclusion d’un clic dans le contenu d’un email. [En savoir plus](../privacy/opt-out.md#one-click-opt-out-link)
* Mise à jour de la section Déléguer un sous-domaine avec des informations plus détaillées sur le processus de validation effectué par Adobe. [En savoir plus](../configuration/delegate-subdomain.md#subdomain-validation)
* Ajout d’une section décrivant comment ajouter manuellement des adresses et des domaines de courriel à la liste de suppression. [En savoir plus](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Mise à jour de la [Accès à la liste de suppression](../configuration/manage-suppression-list.md#access-suppression-list) et [Reprises](../configuration/retries.md) pour refléter la nouvelle interface utilisateur.
* Le nouveau flux pour ajouter et configurer des représentations lors de la création d’une offre a été documenté. [En savoir plus](../offers/offer-library/creating-personalized-offers.md#representations)


## Juillet 2021 {#july-2021}

* Toutes les nouvelles fonctionnalités et améliorations proposées [!DNL Journey Optimizer] La version du 21 juillet a été détaillée dans la documentation. [En savoir plus](release-notes.md)
* Ajout de liens directs vers la documentation des services Experience Platform dans [!DNL Journey Optimizer] page d’accueil et table des matières
* Nouvelles landing pages pour les services Experience Platform disponibles dans [!DNL Journey Optimizer]
* Ajout de liens vers [!DNL Journey Optimizer] description du produit dans la page d’accueil
* Ajout de tutoriels vidéo sur plusieurs pages
* Image optimisée de la page d’accueil
* Déplacement, amélioration et changement de nom de la section &#39;Suivi des messages&#39; en &#39;Ajouter des liens et tracker les messages&#39;. [En savoir plus](../email/message-tracking.md)
* Ajout d’une sous-section sur les pages miroir. [En savoir plus](../email/message-tracking.md#mirror-page)
* Les &quot;activités d’offre&quot; ont été renommées &quot;décisions&quot; et &quot;décisions&quot; &quot;portées de décision&quot; dans la documentation et les écrans. [En savoir plus](../offers/get-started/starting-offer-decisioning.md)
* Nouveau cas pratique : [personnaliser un message avec des fonctions d’assistance ;](../personalization/personalization-use-case-helper-functions.md)
* Mise à jour de la documentation Lecture de segment pour prendre en compte les impacts sur les segments matérialisés. [En savoir plus](../building-journeys/read-segment.md)
* Mise à jour des limites du parcours. [En savoir plus](../start/guardrails.md)
* Mise à jour de la section Configurer la sélection des offres dans les décisions . [En savoir plus](../offers/offer-activities/configure-offer-selection.md)
* Ajout d’un avertissement indiquant que les offres basées sur un événement ne sont actuellement pas prises en charge. [En savoir plus](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documentation de la nouvelle gestion des décisions **[!UICONTROL Overview]** . [En savoir plus](../offers/get-started/user-interface.md#overview)
* Ajout de nouvelles sections pour décrire les actions disponibles dans les listes d’offres et de décisions : [Liste des offres](../offers/offer-library/creating-personalized-offers.md#offer-list) et [Liste de décisions](../offers/offer-activities/create-offer-activities.md#decision-list).

