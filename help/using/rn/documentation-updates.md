---
solution: Journey Optimizer
product: journey optimizer
title: Mises à jour de la documentation
description: En savoir plus sur les dernières mises à jour de la documentation
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 83c8f206-bce3-4cc8-94a3-575ec1d999bc
source-git-commit: 5bc467f7fd25dd4218470c0e73bc0dc87938e218
workflow-type: tm+mt
source-wordcount: '1658'
ht-degree: 88%

---

# Mises à jour de la documentation {#latest-updates}

Cette page répertorie toutes les mises à jour récentes de la documentation de [!DNL Journey Optimizer].

## Juin 2025 {#june-2025}

* Ajout d’une nouvelle section sur l’ajout et l’utilisation de texte enrichi tel que des sauts de ligne, du gras, de l’italique, etc., à des fragments personnalisables à l’aide de composants HTML. [En savoir plus](../content-management/customizable-fragments.md#rich-text)

* La partie Prise de décision a été mise à jour avec une section spécifique dédiée à la création de modèles d’IA. [En savoir plus](../experience-decisioning/ranking/ai-models.md)

* Ajout d’une recommandation sur l’utilisation du champ `actionExecutionTime` dans l’action d’événements journeyStep. [En savoir plus](../reports/sharing-execution-fields.md#actionexecutiontime-actionexecutiontime-field)

* Ajout d’une note sur les `messageID` qui peuvent ne pas être uniques pour chaque diffusion individuelle. [En savoir plus](../data/datasets-query-examples.md)

* Ajout d’une recommandation sur la gestion des événements historiques dans les opérations d’hygiène des données. [En savoir plus](../privacy/data-hygiene.md#recommendations-data-hygiene-recommendations)

* Ajout d’un mécanisme de sécurisation concernant les pages de destination non prises en charge pour la migration entre les sandbox. [En savoir plus](../configuration/copy-objects-to-sandbox.md#general-best-practices-global)

* Ajout d’une note d’avertissement concernant les objets JSON imbriqués non pris en charge dans l’authentification personnalisée pour les actions personnalisées. [En savoir plus](../datasource/external-data-sources.md)

* Ajout d’une note d’avertissement sur les variantes de contenu conditionnel dans le Concepteur d’e-mail. [En savoir plus](../personalization/create-conditions.md)

* Mise à jour de la section « Annuler la délégation d’un sous-domaine de page de destination ». [En savoir plus](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* Clarification des règles de reprise des parcours lors de l’utilisation d’identifiants supplémentaires. [En savoir plus](../building-journeys/supplemental-identifier.md#guardrails--limitations)

* Ajout d’une nouvelle note pour indiquer clairement que vous devez utiliser l’éditeur d’expression en mode avancé lors de la sélection de l’attribut d’identifiant supplémentaire lors de la configuration de l’événement. [En savoir plus](../building-journeys/supplemental-identifier.md#add)

* Ajout d’une clarification sur le fonctionnement de la reprise des parcours avec des identifiants supplémentaires. [En savoir plus](../building-journeys/supplemental-identifier.md#guardrails)

## Mai 2025 {#may-2025}

* Les intégrations Adobe disponibles avec Journey Optimizer sont désormais répertoriées dans la section « Connecter vos systèmes et environnements ». [En savoir plus](../integrations/ajo-integrations.md)

* Les intégrations de contenu sont désormais regroupées dans la section Gestion de contenu. [En savoir plus](../integrations/content-integrations.md)

* Mise à jour des diagrammes d’architecture pour Adobe Experience Platform et Journey Optimizer. [En savoir plus](../start/get-started.md#architecture-architecture)

* Ajout d’une vidéo sur le terrain de jeu de l’éditeur de personnalisation pour vous aider à apprendre à écrire et à tester le code de personnalisation à l’aide de données d’exemple. [En savoir plus](../personalization/personalize.md#how-to-videosvideo-perso)

* Le nombre maximal d’adresses dans une liste de contrôle a été augmenté de 50 à 300. [En savoir plus](../configuration/seed-lists.md#create-seed-list)

* Une nouvelle étape détaillant la manière d’encapsuler le code lors de l’utilisation de politiques de décision dans l’éditeur d’expérience basée sur le code a été ajoutée à la page Créer des politiques de décision. [En savoir plus](../experience-decisioning/create-decision.md#use-decision-policy)

* Une note a été ajoutée à la documentation relative aux expériences basées sur du code pour indiquer que, lorsque plusieurs actions d’expériences basées sur du code sont exécutées sur la même surface, le score de priorité de la campagne ou du parcours détermine ce qui est diffusé à l’utilisateur final ou l’utilisatrice finale si la personne remplit les critères de plusieurs actions. [En savoir plus](../code-based/code-based-surface.md#surface-definition)

* Une nouvelle page sur la résolution des problèmes liés aux actions entrantes dans un parcours fournit un guide détaillé pour identifier et résoudre les problèmes de manière indépendante avant de contacter l’assistance. [En savoir plus](../building-journeys/troubleshooting-inbound.md)

* Une nouvelle [page](../code-based/code-based-decisioning-implementations.md) a été ajoutée pour décrire la manière d’ajouter les indicateurs suivants à votre implémentation cliente lors de l’utilisation de la prise de décision dans des expériences basées sur du code :

   * Ajout de l’indicateur `dryRun` pour tester la prise de décision dans les expériences basées sur du code. [En savoir plus](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

   * Appliquez la déduplication aux requêtes de prise de décision dans les expériences basées sur du code. [En savoir plus](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## Avril 2025 {#apr-2025}

* Le chapitre Configuration est désormais divisé en trois chapitres : [Configuration des canaux](../configuration/get-started-configuration.md), [Configuration de parcours ](../configuration/about-data-sources-events-actions.md) et [Connexion des systèmes](../configuration/ajo-apis.md).
* Ajout d’une note d’avertissement concernant l’utilisation d’événements d’expérience dans des expressions et conditions de parcours. [En savoir plus](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* Ajout d’une note sur la page Configuration du courrier concernant le stockage temporaire du fichier de sortie. [En savoir plus](../direct-mail/direct-mail-configuration.md)
* Ajout d’une astuce dans la section Éditeur d’expression avancé du parcours à propos des instructions de format de condition. [En savoir plus](../building-journeys/expression/expressionadvanced.md)
* Ajout d’une note d’avertissement dans la section Fonction `inAudience` concernant les impacts et les bonnes pratiques lors du changement de nom d’une audience. [En savoir plus](../building-journeys/functions/functioninaudience.md)
* Ajout d’une recommandation sur l’utilisation des mots-clés natifs avec les SMS bidirectionnels. [En savoir plus](../sms/sms-opt-out.md)
* Mise à jour de la page de test du parcours avec une note sur la nécessité d’inclure un espace de noms d’identité dans l’événement utilisé. [En savoir plus](../building-journeys/testing-the-journey.md)
* Il est actuellement impossible d’annuler la délégation des sous-domaines depuis l’interface d’utilisation [!UICONTROL Journey Optimizer]. Vous devez contacter votre représentant ou représentante Adobe. Les étapes d’annulation de la délégation d’un sous-domaine sont désormais détaillées pour les [e-mails](../configuration/delegate-subdomain.md#undelegate-subdomain), les [SMS](../sms/sms-subdomains.md#undelegate-a-subdomain-undelegate-subdomain), les [expériences web](../web/web-delegated-subdomains.md#undelegate-a-subdomain-undelegate-subdomain) et les [pages de destination](../landing-pages/lp-subdomains.md#undelegate-subdomain).<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
* Ajout d’une clarification sur le paramètre `maxHttpConnections` facultatif dans l’API de limitation des parcours, y compris des conseils sur la manière de l’utiliser avec des configurations de limitation pour le même point d’entrée. [En savoir plus](../configuration/throttling.md)
* Ajout de conseils dans la section Décisions pour les expériences expliquant que les éléments d’offre approuvés ne peuvent pas être supprimés s’ils sont utilisés dans une collection ou une décision. Les étapes pour faire passer le statut sur « Brouillon » à l’aide de l’option **[!UICONTROL Annuler l’approbation]** sont incluses. [En savoir plus](../experience-decisioning/items.md#manage)
* Les informations sur les sandbox ont été regroupées dans une nouvelle section nommées « Gestion des sandbox ». Cette nouvelle section fournit des informations sur l’utilisation et l’attribution de sandbox, ainsi que sur l’utilisation des fonctionnalités d’export et d’import de packages pour copier des objets tels que des parcours, des modèles ou des fragments de contenu sur plusieurs sandbox. [En savoir plus](../administration/sandboxes.md)

## Mars 2025 {#mar-2025}

* La page sur les événements de qualification d’audience a été mise à jour avec de nouvelles recommandations. [En savoir plus](../building-journeys/audience-qualification-events.md)
* La fonctionnalité de dépannage d’action personnalisée est désormais disponible pour tous les clients et clientes (GA). [En savoir plus](../action/troubleshoot-custom-action.md)
* L’hygiène des données correspond désormais au cycle de vie des données dans l’interface d’utilisation du produit. La documentation a été mise à jour pour prendre en compte cette modification. [En savoir plus](../privacy/data-hygiene.md)
* Les autorisations intégrées manquantes de la page de destination ont été ajoutées à la documentation. [En savoir plus](../administration/ootb-permissions.md)
* Une note a été ajoutée concernant la planification des campagnes récurrentes. [En savoir plus](../campaigns/create-campaign.md)
* La section concernant l’insertion de liens et l’activation du suivi dans un e-mail a été mise à jour et réorganisée. [En savoir plus](../email/message-tracking.md)
* La section sur les capacités de personnalisation dans Adobe Journey Optimizer a été réorganisée et améliorée. [En savoir plus](../personalization/personalize.md)
* L’API de gestion des décisions pour répertorier les offres personnalisées a été mise à jour avec un exemple pour effectuer la pagination si plusieurs offres personnalisées sont manquantes dans la réponse. [En savoir plus](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* Nous avons créé une page qui regroupe toutes les informations relatives à la fonctionnalité de désabonnement de la liste pour plus de clarté. [En savoir plus](../email/list-unsubscribe.md)
* Nous avons ajouté à la section Capping de la fréquence des informations sur la mise à jour du compteur de capping de la fréquence pour les API Decisioning et Batch Decisioning, en plus de l’API Edge Decisioning. [En savoir plus](../offers/offer-library/add-constraints.md#frequency-capping)

## Février 2025 {#feb-2025}

* Les mécanismes de sécurisation de l’activité « Lecture d’audience » ont été mis à jour afin d’indiquer qu’une seule activité peut être utilisée dans un parcours et qu’elle ne peut cibler qu’une seule audience. [En savoir plus](../building-journeys/read-audience.md)
* Les mécanismes de sécurisation de parcours lors de l’utilisation d’activités Adobe Campaign ont été mis à jour. [En savoir plus](../start/guardrails.md#ac-g)
* Les étapes de création de vos premiers parcours ont été détaillées et des liens vers la section de documentation ont été ajoutés. [En savoir plus](../building-journeys/journey-gs.md)
* Une nouvelle page est désormais disponible pour présenter le tableau de bord du parcours et l’interface d’utilisation de filtrage. [En savoir plus](../building-journeys/journey-ui.md)
* La documentation relative à l’**[!UICONTROL optimisation de l’heure d’envoi]** et ses questions fréquentes associées ont été mises à jour, enrichies et déplacées vers une nouvelle page dédiée. [En savoir plus](../building-journeys/send-time-optimization.md)
* De nouveaux mécanismes de sécurisation ont été ajoutés pour les événements de parcours. [En savoir plus](../start/guardrails.md#events-g)
* La page des actions de canal intégrée a été réorganisée. [En savoir plus](../building-journeys/journeys-message.md)
* Des mécanismes de sécurisation et des limitations ont été ajoutés dans les sections Prise de décision et Gestion des décisions.
   * [Mécanismes de sécurisation et limitations des prises de décision](../experience-decisioning/decisioning-guardrails.md)
   * [Mécanismes de sécurisation et limitations de la gestion des décisions](../offers/decision-management-guardrails.md)
* Une nouvelle section sur les données contextuelles a été ajoutée à la documentation Gestion des décisions. Elle fournit des informations sur la manière d’exploiter les données contextuelles dans le moteur de décision, par exemple pour concevoir une règle de décision qui nécessite que la météo actuelle soit de ≥27 degrés au moment où la demande de décision est effectuée. [En savoir plus](../offers/context-data.md)

## Janvier 2025 {#jan-2025}

* Une section sur l’option **[!UICONTROL Adresse d’exécution]** dans la configuration du canal e-mail a été ajoutée. L’adresse principale est définie au niveau du sandbox, mais le paramètre par défaut peut être remplacé pour une configuration du canal e-mail spécifique. [En savoir plus](../email/email-settings.md#execution-address)

* La page **Commencer avec la délivrabilité** a été mise à jour, avec la possibilité de créer des workflows de préchauffage d’adresses IP directement depuis l’interface d’utilisation. [En savoir plus](../reports/deliverability.md#reputation)

* La section **Paramètres d’en-tête** a été mise à jour pour prendre en compte les nouveaux libellés et leurs modifications dans l’interface d’utilisation. [En savoir plus](../email/email-settings.md#email-header)

* La section **Transférer l’e-mail** a été mise à jour afin d’indiquer que tous les e-mails envoyés à l’**e-mail d’expédition** sont transférés à l’adresse e-mail de transfert. Si aucun e-mail de transfert n’est spécifié, ces e-mails sont ignorés. [En savoir plus](../email/email-settings.md#forward-email)

* La taille maximale des attributs contextuels transmis dans une requête de campagne déclenchée par API a été mise à jour à 200 Ko. [En savoir plus](../campaigns/api-triggered-campaigns.md#contextual)

* Une nouvelle section a été ajoutée à la page **Gérer les fragments** pour décrire comment ajouter de nouveaux attributs à un fragment actif. La page entière a également été enrichie. [En savoir plus](../content-management/manage-fragments.md#adding-new-attributes)

* Une section « Mécanismes de sécurisation et limitations » a été ajoutée à la documentation sur les outils de gestion des conflits et de hiérarchisation. [En savoir plus](../conflict-prioritization/gs-conflict-prioritization.md)

* Un nouveau cas d’utilisation de bout en bout a été ajouté pour présenter toutes les étapes nécessaires à l’utilisation de la prise de décision dans les expériences de contenu avec le canal d’expérience basé sur le code [!DNL Journey Optimizer]. [En savoir plus](../experience-decisioning/experience-decisioning-uc.md)

* La page **Configurer les paramètres d’e-mail** a été divisée en plusieurs sous-pages pour une meilleure lisibilité, y compris les nouvelles pages autonomes dédiées au [Désabonnement de la liste](../email/list-unsubscribe.md), aux [Paramètres d’en-tête](../email/header-parameters.md) et au [Tracking d’URL](../email/url-tracking.md).

## Décembre 2024 {#nov-2024}

* Une note a été ajoutée pour aider à résoudre un message d’erreur potentiel lors d’un appel API pour activer les jeux de données pour la personnalisation à l’aide de données Adobe Experience Platform. [En savoir plus](../personalization/aep-data-perso.md)

## Octobre 2024 {#oct-2024}

* Toutes les nouvelles fonctionnalités et améliorations de la version d’octobre 2024 de [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Tous les canaux de communication disponibles dans [!DNL Journey Optimizer] sont désormais regroupés dans une section dédiée de la documentation. [En savoir plus](../channels/gs-channels.md)
* La page **Configurer votre expérience basée sur le code** a été améliorée afin de rendre le processus plus clair, y compris la section expliquant ce qu’est un URI de surface. [En savoir plus](../code-based/code-based-configuration.md)
* La page **Créer une configuration de canal web** a été mise à jour afin de clarifier les étapes de création d’une règle de correspondance de pages, qui s’applique également à la configuration d’expérience basée sur le code. [En savoir plus](../web/web-configuration.md#web-page-matching-rule)
* Une note concernant le prochain mécanisme de sécurisation sur la durée de vie (TTL) pour les jeux de données générés par le système a été ajoutée. [En savoir plus](../data/get-started-datasets.md)
* Une nouvelle section a été ajoutée pour décrire comment prévisualiser vos expériences personnalisées basées sur du code directement sur votre navigateur ou vos appareils mobiles, à l’aide de l’option **Prévisualiser sur l’appareil** lors de la simulation de contenu dans un parcours ou une campagne. [En savoir plus](../code-based/test-code-based.md#preview-on-device)
* Une nouvelle page a été ajoutée sur la manière d’exploiter les audiences de chargement personnalisées pour la prise de décision. [En savoir plus](../offers/custom-upload-decisioning.md)
* Une nouvelle page a été ajoutée pour présenter les fonctionnalités de décision disponibles dans Journey Optimizer. [En savoir plus](../experience-decisioning/gs-decision.md)
* Les mécanismes de sécurisation et les limites ont été ajoutés à la documentation de la prise de décision. [En savoir plus](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## Septembre 2024 {#sept-2024}

* Toutes les nouvelles fonctionnalités et améliorations de la version de février 2024 de [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Ajout d’une section sur la gestion des reprises de parcours. [En savoir plus](../building-journeys/read-audience.md#read-audience-retry)
* Mise à jour des questions fréquentes sur la règle de capping et de limitation pour les actions personnalisées afin de mentionner la règle de capping par défaut. [En savoir plus](../configuration/external-systems.md#faq)
* Mise à jour de la section Contrôler l’accès afin d’inclure les autorisations liées au générateur de contenu de l’assistant IA. [En savoir plus](../administration/high-low-permissions.md#ai-permission)
* Ajout d’une vidéo sur l’utilisation du générateur de contenu de l’assistant IA pour la génération d’e-mails. [En savoir plus](../content-management/generative-email.md#video)

<!--

## August 2024 {#aug-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] August '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Performance guardrails for Decision Management have been updated to mention Decisioning APIs delivery throughputs with/without Edge Segmentation. [Read more](../start/guardrails.md#decision-management)
* Journey guardrails have been updated. [Read more](../start/guardrails.md#journeys-guardrails-journeys)


## July 2024 {#july-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] July '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A personalization use case has been added on how to personalize an email with information related health plans and prescriptions. [Read more](../personalization/perso-uc-plan-prescriptions.md)

## June 2024 {#june-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] June '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A note about the usage of merge policies in journeys has been added on [this page](../building-journeys/journey-properties.md#merge-policies).
* The page about how to configure a **Wait** activity in a journey has been reorganized and improved. [Read more](../building-journeys/wait-activity.md)
* A new page has been created to detail journey's properties. [Read more](../building-journeys/journey-properties.md)

## May 2024 {#may-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] May '24 release have been detailed in the documentation. [Read more](release-notes.md)
* The section on seed lists has been updated regarding recurring journeys. [Read more](../configuration/seed-lists.md#use-seed-list)
* The setion on external data sources has been updated. [Read more](../datasource/external-data-sources.md#custom-authentication-access-token)
* The global journey timeout of 30 days has been added to the Guardrail and limitation page. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* The section on the Adobe Campaign v7/v8 integration has been updated with information on provisionning. [Read more](../action/acc-action.md#access)
* The expression editor used to personalize content has been renamed in the documentation to "personalization editor" to clearly differenciate it from the [Journey expression editor](../building-journeys/expression/expressionadvanced.md). [Read more](../personalization/personalization-build-expressions.md)

## April 2024 {#april-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] April '24 release have been detailed in the documentation. [Read more](release-notes.md#apr-2024)
* Configuration steps for In-app messaging have been detailed. [Read more](../in-app/inapp-configuration.md)
* Documentation for [Offer decisioning APIs](../offers/api-reference/offer-delivery-api/decisioning-api.md) and [Batch decisioning APIs](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md) have been updated.
* Information has been added in the Decision Management documentation regarding edge and hub regions management when using frequency capping with the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)
* Information has been added on identity creation with custom namespaces when working with API-triggered campaigns. [Read more](../campaigns/api-triggered-campaigns.md)
* Screeshots have been updated to reflect the improved Journey canvas.
* Naming constraints has been updated in the following page: [Configure a unitary event](../event/about-creating.md), [Configure a business event](../event/about-creating-business.md#gs-business-events), [Configure a custom action](../action/about-custom-action-configuration.md#configuration-steps), [External data sources](../datasource/external-data-sources.md)
* A note has been added on Send Time Optimization availability. [Read more](../building-journeys/send-time-optimization.md)
* A new technical use case has been added on how to create a custom action to send data to Experience Platform. [Read more](../building-journeys/custom-action-aep.md)

## March 2024 {#march-2024}
 
* A Frequently Asked Questions section has been added to address common questions regarding the use of audience composition and custom upload audiences in Journey Optimizer. [Read more](../audience/about-audiences.md#faq)
* All new features and improvements coming with [!DNL Journey Optimizer] March '24 release have been detailed in the documentation. [Read more](release-notes.md#mar-2024)
* The page on profile entrance management has been improved. [Read more](../building-journeys/entry-management.md)
* Troubleshooting information has been added to the Alerts page. [Read more](../reports/alerts.md#alert-troubleshooting)
* Information on the Wait activity has been added to the page on journey reports. [Read more](../reports/sharing-overview.md)
* For Journeys in test mode, following shortcuts have been disabled:
    * T: Shortcut to toggle the test mode on or off.
    * E: Shortcut used to trigger an event in an event-based journey.
    * P: Shortcut to trigger an event in an audience-based journey for which the Single profile at a time option is turned on.
    * L: Shortcut designated to display the test logs.
* The Message frequency rules page has been updated with a new subsection on daily frequency cap, which is available on demand in addition to weekly or monthly capping.
* The Work with consent policies page has been improved and updated with useful links to the Experience Platform documentation. [Read more](../action/consent.md)
* A new section has been added to reflect the fact that you can display HTML email content templates as thumbnails with the Grid view mode (Limited Availability). [Read more](../content-management/content-templates.md#template-thumbnails)
* A new section has been added to the Deliverability page to explain what feedback loops are and how to leverage them. [Read more](../reports/deliverability.md#feedback-loops)
* A note has been added to the Create personalized offers section to specify that the size of an offer including all its representations cannot exceed 300KB. [Read more](../offers/offer-library/creating-personalized-offers.md#create-offer)

## February 2024 {#feb-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] February '24 release have been detailed in the documentation. [Read more](release-notes.md#feb-2024)
* The Journey Optimizer + Workfront integration has been added to the integrations page. [Read more](../integrations/ajo-integrations.md)
* Information has been added on how to personalize offers' representations based on context data. [Read more](../offers/offer-library/add-representations.md#context-data)
* The guardrails page has ben updated with a note on custom actions which support JSON format only when using request or response payloads. [Read more](../start/guardrails.md#custom-actions-g)
* Additional information has been added about the basic authentication type in external datasources. [Read more](../datasource/external-data-sources.md)
* A note has been added to clearly differenciate the [Journey expression editor](../building-journeys/expression/expressionadvanced.md) from the [personalization editor](../personalization/functions/functions.md).
* The list of functions available in the advanced expression editor has been updated. [Read more](../building-journeys/expression/functions.md)
* The page on the Split function has been updated. [Read more](../building-journeys/functions/functioninaudience.md)
* Information has been added regarding the impact of the opt-in or opt-out of push notifications on In-app messages. [Read more](../in-app/create-in-app.md)
* The Message frequency rules page has been updated to reflect the Duration options available in the user interface (weekly or monthly).
* The Edit a PTR record section has been updated to clarify the fact that PTR records cannot be created manually and that you need to edit PTR records to assign them new subdomains. [Read more](../configuration/ptr-records.md#edit-ptr-record)

## January 2024 {#jan-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] January '24 release have been detailed in the documentation. [Read more](release-notes.md)
* A guardrail about the journey size has been added. [Read more](../start/guardrails.md#journeys-guardrails-journeys)
* Journey timeout management has been detailed [in the following section](../building-journeys/journey-properties.md#global_timeout).
* Journey Optimizer [documentation home](../../ajo-home.md) page has been redesigned.
* Recommendations about the Update Profiles activity have been added. [Read more](../building-journeys/update-profiles.md) 
* Information has been added regarding the behaviour of timeouts on event activities in journeys. When no event is received during the specified timeout period, individuals will continue the journey if no timeout path is defined. [Read more](../building-journeys/general-events.md#events-specific-time)
* In-app channel configuration prerequisites have been updated with a note about the usage of a custom Dataset preference merge policy. [Read more](../in-app/inapp-configuration.md)
* More details have been added about how to manipulate collections in a custom action response. [Read more](../action/action-response.md#exp-syntax).
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=fr) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important-notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `<listObject>` has been modified in multiple functions.
* Update the **duration** parameter in the `toString` function. [Read more](../building-journeys/functions/functiontostring.md)
* For some external data sources use-cases, usage of custom actions is recommended.
* Event field syntax has been updated. The following syntax is deprecated `@(my_event.myfield}` and replaced by `@event{my_event.myfield}`. [Read more](../building-journeys/expression/field-references.md)

+++ 2023

## November 2023 {#nov-2023}

* The guardrail that limits all custom actions has been changed from 150,000 calls over 30 seconds to 300,000 calls over one minute. In addition, the default capping no longer applies to each endpoint. It is now performed per host and per sandbox. For example, on a sandbox, if you have two endpoints with the same host (eg: `https://www.adobe.com/endpoint1` and `https://www.adobe.com/endpoint2`), the capping will apply for all endpoints under the adobe.com host. "endpoint1" and "endpoint2" will share the same capping configuration and having one endpoint reach the limit will have an impact on the other endpoint. [Read more](../action/about-custom-action-configuration.md)
* A new status for email campaigns has been added to the list of campaigns' statuses. [Read more](../campaigns/modify-stop-campaign.md#campaign-statuses-and-alerts-statuses)
* The Get started with Adobe Experience Platform audiences section has been updated to reflect the audience evaluation methods available and how to select them. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* A new subsection has been added to specify which events should be avoided when building your audience if you are using the streaming segmentation evaluation method. [Read more](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## October 2023 {#oct-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] October '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added GIFs to illustrate some key capabilities, such as: [Content templates](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Computed attributes](../audience/computed-attributes.md), [Direct mail](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Decision management optimization models](../offers/ranking/personalized-optimization-model.md), [API-triggered campaigns](../campaigns/api-triggered-campaigns.md), and [Content experiment](../content-management/content-experiment.md).
* The Schema creation process has been updated to reflect latest updates in the user interface, coming with Adobe Experience Platform changes. [Read more](../audience/creating-test-profiles.md) 
* Decision Management guardrails have been added to the Guardrails and limitations page. [Read more](../start/guardrails.md#decision-management)
* The Header parameters section has been updated to reflect how out-of-office notifications and challenge responses are handled (they are received on the **[!UICONTROL Error email]**). [Read more](../email/email-settings.md#email-header)
* A new section on how to preview and test your content has been created. [Read more](../content-management/preview-test.md)
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=fr){target="_blank"}
* The Capping section has been updated to reflect the label changes relating to offer capping in the decision management interface. [Read more](../offers/offer-library/add-constraints.md#capping)
* The Add dynamic content into emails has been updated with details on how to delete a variant. [Read more](../personalization/dynamic-content.md#emails)
* The example for capping & throttling configurations has been updated. [Read more](../configuration/external-systems.md)
* The limitation regarding scalar arrays has been removed from the external data source section. [Read more](../datasource/external-data-sources.md)
* The multi-channel journey use case has been updated. [Read more](../building-journeys/journeys-uc.md)
* The Journey Optimizer documentation set has been updated to reflect the new Experience Platform schema creation process. 

## September 2023 {#september-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] September '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added with scaling best practices and real-time stitching guidance. [Read more](../start/best-practices.md)
* A Frequently-Asked-Questions section has been added for Send-Time Optimization. [Read more](../building-journeys/journeys-message.md#faq-send-time)
* A note has been added for the audience qualification activity. It may take up to 10 minutes to be active and listen to profiles entering or exiting the audience. [Read more](../building-journeys/audience-qualification-events.md#important-notes-segment-qualification)
* A list of limitations to be aware of when creating decision rules has been added to the decision management documentation. [Read more](../offers/offer-library/creating-decision-rules.md)
* Links to access control documentation have been updated. [Read more](../administration/permissions.md)
* In-app channel prerequisites have been updated with Adobe Experience Platform Data Collection details. [Read more](../in-app/inapp-configuration.md)
* Some expressions presented in ranking formula examples have been updated to avoid validation errors. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* A warning has been added to the Define decision scopes section to specify that if AI model is used in an evaluation criteria group, all the evaluation criteria in that group must use the AI ranking method, with the same specific AI model. Moreover, only one evaluation criteria group can use AI model. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] August '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The note about **authentication cache management** in journey has been updated to detail that the token is not shared between different journeys. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* The page about journey **entry management** has been updated to clarify behaviour. [Read more](../building-journeys/entry-management.md)
* Offer decisioning **export datasets** are now enabled by default. The note about the previous behavior has been removed.  [Read more](../offers/export-catalog/get-started-export.md)
* Various **campaign report metrics** have been renamed, in both Live and Global reports. [Read more](../reports/campaign-live-report.md)
* A new section has been added on content experiment prerequisites for the web channel. [Read more](../web/web-prerequisites.md#experiment-prerequisites)
* A warning has been added on the **Work with content templates** page to indicate that currently tracking is not supported when testing email content templates. To test tracking, you must use the content template in an email and send a proof. [Read more](../content-management/content-templates.md#test-template)
* Several warnings have been added in the **Create and publish landing pages** section to specify that you cannot access your landing page by simply copy-pasting into a web browser the URL defined when creating the page, even if published. Instead you can test it using the preview function. [Read more](../landing-pages/create-lp.md)
* A new section has been added on how to **manage consent** for the direct mail channel. [Read more](../direct-mail/test-send-direct-mail.md)

## July 2023 {#july-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] July '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The wait activity documentation page has been improved with additional information and best practices related to the global timeout and reentrance usage. [Read more](../building-journeys/wait-activity.md)
* The page on entry management has been improved. [Read more](../building-journeys/entry-management.md)
* Additional information has been added about the throttling rate in the Read audience activity documentation. [Read more](../building-journeys/read-audience.md)
* Additional information has been added about retries. [Read more](../start/guardrails.md#general-actions-g)
* The **Implement personalization consent** section has been updated to describe how to manually enforce personalization consent in campaigns: you can use the segment rule builder to create an audience containing opt-out profiles or add a split activity to a composition workflow. [Read more](../privacy/opt-out.md#opt-out-expression-editor)

## June 2023 {#june-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] June '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the discard rate ratio in the Journeys overview screen. [Read more](../building-journeys/journey-gs.md#journey-access)
* A note has been added with the steps to follow if you modify your schema with new enumeration values after creating an event [Read more](../event/about-creating.md)
* A recommendation has been added to use journeyVersionID instead of journeyVersionName when querying journeys. [Read more](../reports/sharing-common-fields.md#journeyversionid-field)
* Additional examples on the evaluation criteria order have been added to the **Create decisions** section to illustrate cases where multiple criteria and multiple decision scopes are used. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* Decision Management documentation has been clarified with a note specifying that the use of Object Level Access Control is not available for dynamic collections. [Read more](../offers/offer-library/creating-collections.md)

## May 2023 {#may-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] May '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added to describe how to set up the subdomain that will be used to publish content coming from the Adobe Experience Manager Assets Essentials in your web experiences. [Read more](../web/web-delegated-subdomains.md)
* A new subsection has been added to explain how to add personalized tracking parameters to URLs in the Email Designer. [Read more](../email/message-tracking.md#url-tracking)
* A new section has been added to describe how to ensure that the choice of your customers who opt out from having their profile data used for personalization is honored. [Read more](../privacy/opt-out.md#opt-out-personalization)
* A note has been added about using special international characters in URLs included in email contents. [Read more](../email/message-tracking.md#insert-links)
* The permission needed to test and publish landing pages has been added. [Read more](../landing-pages/create-lp.md)
* A note has been added about the Adobe Experience Platform endpoints needed to have your custom events accounted for in Decision Management frequency capping. [Read more](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] April '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A note has been added to specify that built-in actions cannot be removed. [Read more](../start/guardrails.md#custom-actions-g)
* Information has been added on serviceEvents as well as a query example to check the details of a serviceEvent. [Read more](../reports/query-examples.md#common-queries) 
* A note has been added to specify that you cannot perform queries on time series. [Read more](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials and Adobe Stock have been added to the multi-solution integration page. [Read more](../integrations/ajo-integrations.md)
* The warning on multi-level email subdomains not being allowed has been removed as they are now supported. [Read more](../configuration/delegate-subdomain.md)
* A note has been added to specify that, if changes are made to an offer decision which is being used in a journey's message, you need to unpublish the journey and republish it. [Read more](../building-journeys/publishing-the-journey.md)
* Explanation on how to make sure events are correctly accounted for in the capping counter has been clarified in the decision management **Capping event** section. [Read more](../offers/offer-library/add-constraints.md#capping-event)
* A new section has been added to the **Change execution addresses** page. It specifies that it is possible to override the execution field set globally in the journey advanced parameters, but the email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. [Read more](../configuration/primary-email-addresses.md#journey-parameters)
* The **URL tracking** section now provides the list and description of all contextual attributes that can be set for URL tracking in an email channel configuration. [Read more](../email/email-settings.md#url-tracking)

## March 2023 {#march-2023}

* The Journey Optimizer schema dictionary is now available. You will find the complete list of fields and attributes for each schema.  [Read more](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=fr)
* All new features and improvements coming with [!DNL Journey Optimizer] March '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a step to enable Adobe Analytics events in your journeys. [Read more](../event/about-analytics.md)
* A new section has been created in the Decision management guide on how to collect offer decisioning feedback in Adobe Experience Platform, including which offers are displayed and how users interact with them. [Read more](../offers/data-collection/data-collection.md)
* A new subsection has been added to the **Create decision** section to explain the difference between evaluating criteria in a sequential order or at the same time. [Read more](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order)
* A guardrail has been added for read audience journeys with incremental read. You cannot create a new version, you need to duplicate the journey. [Read more](../start/guardrails.md#journey-versions-g)
* The use case on how to limit throughput put has been updated with information on throttling capabilities. [Read more](../building-journeys/limit-throughput.md)
* A note has been added to specify that scalar arrays are not supported in response payload definition. [Read more](../datasource/external-data-sources.md)
* The section on profile cap conditions has been updated. [Read more](../building-journeys/condition-activity.md#profile_cap)

## February 2023 {#feb-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added about the canvas toolbar. [Read more](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Information has been added to state that internal Adobe addresses are not allowed in URLs and APIs. [Read more](../start/guardrails.md)
* A note has been added in the API-triggered campaigns documentation to specify that contextual attributes passed into the request cannot exceed 50kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)
* Information was added on how opt-out information is stored in the **Consent Service Dataset** after recipients are unsubscribed through a landing page. [Read more](../landing-pages/lp-use-cases.md#configure-opt-out)

## January 2023 {#jan-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Information has been added on custom authentication endpoints in the capping documentation. [Read more](../configuration/external-systems.md)
* A new custom authentication example has been added in the external datasources section. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* A note has been added about Data Collection Core Service (DCCS) for event-triggered journeys. [Read more](../start/guardrails.md#events-g)
* A note on identity namespace retrieval has been added in the [Read audience](../building-journeys/read-audience.md), [Audience qualification](../building-journeys/audience-qualification-events.md) and [Event creation](../event/about-creating.md) sections.
* Accessibility features in [!DNL Journey Optimizer] are now grouped in a dedicated page. [Read more](../start/accessibility.md)
* The examples have been updated in the Operators section of the advanced expression editor documentation. [Read more](../building-journeys/expression/operators.md)
* A note has been added about the limitation on lookup with array of objects. [Read more](../event/experience-event-schema.md#relationships_limitations)
* Added a new page about data management in [!DNL Journey Optimizer]. [Read more](../data/gs-data.md)
* Added a table listing all codes that can be returned in the response when delivering offers using the Decisioning API. [Read more](../offers/api-reference/offer-delivery-api/decisioning-api.md)

+++

+++ 2022

## December 2022 {#december-2022}

* The Messages guide has been reorganized and split into dedicated guides for each channel:

    * [Email channel](../email/get-started-email.md)
    * [Push notification channel](../push/get-started-push.md)
    * [SMS channel](../sms/get-started-sms.md)

* The Configuration guide has been reorganized for improved readability. [Read more](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Added a new page about Journey Optimizer integrations. [Read more](../integrations/ajo-integrations.md)
* Added a recommendation about the length of mirror pages URLs. [Read more](../email/message-tracking.md)
* A new subsection in the email settings configuration has been added on the reply to email address, including recommendations to ensure proper reply management. [Read more](../email/email-settings.md#reply-to-email)
* Added a section on how to modify the content of a message in a live journey. [Read more](../building-journeys/journeys-message.md#update-live-content)

## October 2022 {#october-2022}

* Added a journey use case on how to limit throughput using External Data Sources and Custom Actions. [Read more](../building-journeys/limit-throughput.md)
* The journey use case section has been reorganized into two categories: [Business use cases](../building-journeys/journeys-uc.md) and [Technical use cases](../building-journeys/collections.md).
* The **Entity Dataset** section has been updated with more details. [Read more](../data/datasets-query-examples.md#entity-dataset)
* The opt-out management and consent policies sections have been reorganized. [Read more](../privacy/opt-out.md)
* The section on advanced parameters in journey messages has been clarified and now specifies that email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. 
* Added a note to the **Configure landing page subdomains** section to specify that capital letters are not allowed in landing page subdomains. [Read more](../landing-pages/lp-subdomains.md)

## September 2022 {#september-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] September '22 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a best practice related to the use of wait activities in recurring read audience journeys. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added new step event query examples as well as information on the difference between id, instanceid and profileid. [Read more](../reports/query-examples.md).
* Updated the pages related to the [toDateOnly](../building-journeys/functions/functiontodateonly.md) and [toString](../building-journeys/functions/functiontostring.md) functions.
* Added details on the time condition parameters. [Read more](../building-journeys/condition-activity.md#time_condition)
* Added information on built-in datasets. [Read more](../data/get-started-datasets.md#access-datasets)
* The Global report and Live report sections have been improved and reorganized. [Read more](../reports/report-gs-cja.md)
* A list of every reporting metric available in Adobe Journey Optimizer has been added.
[Read more](../reports/report-gs-cja.md#email-and-sms-metrics)
* The BCC email section has been moved to the new Support for archiving page. [Read more](../configuration/archiving-support.md)

## August 2022 {#august-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] August '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The Frequency rules section has been updated to reflect the new in-line messaging flow.
* A video showing how to configure subscriptions and create landing pages is now referenced in the Get started with landing pages section. [Read more](../landing-pages/get-started-lp.md#video)
* A limitation has been added for journeys using Read Audience activities. [Read more](../building-journeys/read-audience.md)
* The expression editor operators page has been improved. [Read more](../building-journeys/expression/operators.md)
* A section on how to schedule a campaign has been added. [Read more](../campaigns/create-campaign.md)
* General syntax rules section for expression editor has been updated to take into account the new rule regarding the backslash symbol escaping in literal functions. The existing published messages are not impacted by this change. Only the new or draft messages must be updated. [Read more](../personalization/personalization-syntax.md#general-rules)

## July 2022 {#july-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] July '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Set up channel configurations** section has been clarified and updated with links to the page describing how to configure the SMS channel. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* In the journey properties, the **Profile Time zone** option is now disabled by default. [Read more](../building-journeys/timezone-management.md#timezone-from-profiles)
* In the **Wait** activity, the **Fixed date** option is no longer available. [Read more](../building-journeys/wait-activity.md)
* Added more information on the **Incremental read** option in the **Read audience** activity. [Read more](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Added recommendations on the **Profile cap** condition type. [Read more](../building-journeys/condition-activity.md#profile_cap)
* Added a limitation on business events. [Read more](../start/guardrails.md#events-g)

## June 2022 {#june-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] June '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new section about Privacy requests has been added to the documentation. [Read more](../privacy/requests.md)
* A new section about Audit logs on resources has been added to the documentation. [Read more](../privacy/audit-logs.md)
* A new section about how to add HTML or JSON content coming from Adobe Experience Cloud Asset library to an offer representation has been added to the documentation. [Read more](../offers/offer-library/add-representations.md#html-json)
* Added a new page on journey lifecyle. [Read more](../building-journeys/journey.md#journey-versions)
* Updated the Wait activity page. [Read more](../building-journeys/wait-activity.md)
* Added the list of Adobe Journey Optimizer datasets with query examples. [Read more](../data/datasets-query-examples.md)
* The Allowed list page has been moved to the Configuration section. [Read more](../configuration/allow-list.md)
* The Suppression list page has been updated to clarify some information, including the fact that all ASCII characters comprised between 32 and 126 are allowed in the reason for suppression field. [Read more](../configuration/manage-suppression-list.md)
* The link to guardrails and static limits for Decision management has been added. [Read more](../start/guardrails.md)
* Send-Time Optimization is now available for all customers. The beta mention has been removed. [Read more](../building-journeys/send-time-optimization.md)
* The Batch Decisioning API has been added to the list of available APIs to delivery personalized offers. [Read more](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## May 2022 {#may-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] May '22 release have been detailed in the documentation. [Read more](release-notes.md)
* New query examples related to [audience qualification](../reports/query-examples.md#segment-qualification-queries) and [events](../reports/query-examples.md#event-based-queries) have been added.
* The email design section now mentions new built-in templates available to start content with. Related screenshots have been updated. [Read more](../email/get-started-email-design.md)
* Links to key resources have been updated in Journey Optimizer documentation home page.
* Screenshots for landing page and subscription reporting have been updated. [Read more](../reports/live-report.md)
* A note has been added stating that the Delete method is not supported in custom actions. [Read more](../action/about-custom-action-configuration.md)
* Links to how-to videos have been updated.
* The [Email configuration](../configuration/about-subdomain-delegation.md), [Message presets](../configuration/channel-surfaces.md) and [Configure landing pages](../landing-pages/lp-subdomains.md) sections have been reorganized for improved readability.
* The URL tracking section has been updated and improved with examples. [Read more](../email/email-settings.md#url-tracking)
* A new subsection on setting up a forward email address has been added. Note that you cannot do it through the user interface. [Read more](../email/email-settings.md#forward-email)

## April 2022 {#april-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] April '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **reactions** event documentation page has been updated. [Read more](../building-journeys/reaction-events.md)
* Videos for Decision Management capabilities have been updated to reflect Journey Optimizer user interface. [Read more](../offers/get-started/starting-offer-decisioning.md)
* The **Get Started with Datasets** section has been improved to detail how to access and create datasets. [Read more](../data/get-started-datasets.md)
* Links to help guides and product release notes have been added to the **Adobe Journey Optimizer Documentation** home page. [Read more](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=fr)
* The **Create message presets** section now specifies that you cannot proceed with preset creation while the selected IP pool is under edition (**[!UICONTROL Processing]** status) and has never been associated with the selected subdomain. [Read more](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* The message presets **URL tracking** section has been updated to reflect minor changes in the user interface. [Read more](../configuration/channel-surfaces.md#url-tracking)

## March 2022 {#march-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] March '22 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page on getting started with AI models has been added to the **Offer decisioning** section, including a thorough description of the [auto-optimization model](../offers/ranking/auto-optimization-model.md), the algorithm it uses and more technical details. [Read more](../offers/ranking/ai-models.md)
* The test profile creation page has been moved to the  **Audience, profiles and identity** section. [Read more](../audience/creating-test-profiles.md)
* Added an example on how to add an expression as a default value in the expression editor. [Read more](../building-journeys/expression/field-references.md#default-value)
* The **Create personalized offers** section has been reorganized for improved readability. [Read more](../offers/offer-library/creating-personalized-offers.md)
* A new section has been added to describe the impacts that changing an offer's start and/or end dates may have on this offer's frequency capping. [Read more](../offers/offer-library/add-constraints.md#capping-change-date)
* The **Change the primary email addresses** section has been updated to reflect the user interface changes. [Read more](../configuration/primary-email-addresses.md)

## February 2022 {#feb-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Feb '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The [replace](../building-journeys/functions/functionreplace.md#example_2) and [replaceAll](../building-journeys/functions/functionreplaceall.md#example) function documentation pages have been updated with additional information and examples regarding the target parameter.
* Best practices have been added to the [Operators](../building-journeys/expression/operators.md#important-notes) page.

## January 2022 {#january-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Offer decisioning AI rankings** section has been updated with a more detailed description of the auto-optimization model. [Read more](../offers/ranking/auto-optimization-model.md)
* A new section on the schema requirements needed to be able to send in event types when using an AI model has been added. [Read more](../offers/data-collection/schema-requirement.md)
* The section related to [!DNL Journey Optimizer] personalization capabilities has been reorganized for better readability. [Read more](../personalization/personalize.md)
* The **Create message presets** section has been divided into several sections for improved clarity. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* The **Opt-out management** section has been clarified and slightly reorganized. [Read more](../privacy/opt-out.md#opt-out-management)
* The **Insert links** section has been updated to reflect the recent user interface changes. [Read more](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* A full description of the **advanced expression editor** used in journeys is now available. [Read more](../building-journeys/expression/expressionadvanced.md)
* A new section about **CNAME subdomain delegation method** has been added. [Read more](../configuration/delegate-subdomain.md#cname-subdomain-delegation)

## October 2021 {#october-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] Oct '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added **Date time function** list. [Read more](../personalization/functions/dates.md)
* New **Get Started sections per user persona**. Take your own path to get to your goals faster! [Read more](../start/quick-start.md)
* New **Edit a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New **Edit a PTR record** section. [Read more](../configuration/ptr-records.md#edit-ptr-record)
* New **Deactivate a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface#deactivate-a-surface)
* New limitations added to the **Decision Management API developer guide** on offer constraints not supported with the mobile [!DNL Experience Edge] workflows. [Read more](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* New **Create simulations** section. [Read more](../offers/offer-activities/simulation.md)
* Updated **Add decision scopes** section. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Updated **Define content for your representations** section, including a new [subsection](../offers/offer-library/creating-personalized-offers.md#custom-text) on how to define and personalize custom text. [Read more](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* The following function pages have been updated: [sethours](../building-journeys/functions/functionsethours.md), [getListItem](../building-journeys/functions/functiongetlistitem.md), [inSegment](../building-journeys/functions/functioninaudience.md)

* The following functions have been added: [filter](../building-journeys/functions/functionfilter.md), [intersect](../building-journeys/functions/functionintersect.md), [toDateOnly](../building-journeys/functions/functiontodateonly.md)

* The dateOnly date type has been added in the expression editor documentation. [Read more](../building-journeys/expression/data-types.md)

* Added details on custom action cache duration. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)

* Added information on custom action default ports. [Read more](../action/about-custom-action-configuration.md#url-configuration)

* Added information on multiple business event use cases. [Read more](../event/about-creating-business.md#multiple-business-events)

* Added commonly used examples to query Journey Step Events in Data Lake. [Read more](../reports/query-examples.md)

* Added a new **Limitations** page. [Read more](../start/guardrails.md)

* Improved the **Quick start** page with steps for different personas. [Read more](../start/quick-start.md)

* Now all the Decision Management features described in the dedicated section also apply to the Adobe Experience Platform users leveraging the Offer Decisioning application. [Read more](../offers/get-started/starting-offer-decisioning.md)

* Added a subsection to clarify the differences between using audiences versus decision rules when applying a constraint to restrict the selection of offers for a given placement. [Read more](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* Added specific ranking formula examples to illustrate some real-life use cases. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Added a subsection on how to edit IP pools. [Read more](../configuration/ip-pools.md#edit-ip-pool)

## August 2021 {#august-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] August '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Updated Decision management permissions. [Read more](../administration/ootb-product-profiles.md)
* Updated Email Designer screenshots with latest UI.
* Updated the configuration procedure for custom actions with dynamic URL paths and dynamic headers. [Read more](../action/about-custom-action-configuration.md#url-configuration)
* Added a section about accessibility features and shortcuts. [Read more](../start/user-interface.md#accessibility)
* Added a section about audience evaluation methods. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Added notes to the Suppression list, Allowed list and Email global/live report sections to specify that profiles with Suppressed and Not allowed statuses are excluded from the Email report Sent metrics. [Read more](../reports/report-gs-cja.md)
* Added a new section to describe how to retrieve email addresses or domains that were excluded from a sending because they were not on the allowed list. [Read more](../configuration/allow-list.md#reporting)
* Updated the Enable the allow list section. [Learn more](../configuration/allow-list.md#enable-allow-list)
* Updated the Monitor message presets section with the possible preset creation failure reasons and details on such errors. [Read more](../configuration/channel-surfaces.md#monitor-channel-surfaces)
* Updated and renamed the Retry time period section to reflect the fact that you can now adjust the email retry setting in the message presets. [Read more](../configuration/retries.md#retry-duration)
* Updated the Delegate a subdomain section with more detailed information on the validation process performed by Adobe. [Read more](../configuration/delegate-subdomain.md#subdomain-validation)
* Added a section to describe how to manually add email addresses and domains to the suppression list. [Read more](../configuration/manage-suppression-list.md#add-addresses-and-domains)
* Updated the [Access the suppression list](../configuration/manage-suppression-list.md#access-suppression-list) section and [Retries](../configuration/retries.md) sections to reflect the new user interface.
* The new flow to add and configure representations when creating an offer has been documented. [Read more](../offers/offer-library/creating-personalized-offers.md#representations)

## July 2021 {#july-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] July '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added direct links to Experience Platform services documentation in [!DNL Journey Optimizer] home page and table of contents
* New landing pages for Experience Platform services available in [!DNL Journey Optimizer] 
* Added links to [!DNL Journey Optimizer] product description in the home page
* Added tutorial videos in multiple pages
* Optimized home page imagery
* Moved, improved and renamed 'Message tracking' section to 'Add links and track messages'. [Read more](../email/message-tracking.md)
* Added a subsection on mirror pages. [Read more](../email/message-tracking.md#mirror-page)
* Renamed 'offer activities' as 'decisions' and 'decisions' as 'decision scopes' in documentation and screens. [Read more](../offers/get-started/starting-offer-decisioning.md)
* New use case: [personalize a message with helper functions](../personalization/personalization-use-case-helper-functions.md)
* Updated the Read audience documentation to reflect materialized segment impacts. [Read more](../building-journeys/read-audience.md)
* Updated the Journey limitations. [Read more](../start/guardrails.md)
* Updated the Configure offers selection in decisions section. [Read more](../offers/offer-activities/configure-offer-selection.md)
* Added a warning to mention that event-based offers are not currently supported. [Read more](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documented the Decision Management new **[!UICONTROL Overview]** tab. [Read more](../offers/get-started/user-interface.md#overview)
* Added new sections to describe the actions available from the offer and decision lists: [Offer list](../offers/offer-library/creating-personalized-offers.md#offer-list) and [Decision list](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
-->
