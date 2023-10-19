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
source-git-commit: 37fda274025135f0577fd551971583e1b6d5c469
workflow-type: tm+mt
source-wordcount: '3845'
ht-degree: 96%

---

# Mises à jour de la documentation {#latest-updates}

Cette page répertorie toutes les mises à jour de la documentation d&#39;[!DNL Journey Optimizer].

## Octobre 2023 {#oct-2023}

* Ajout de GIFs pour illustrer certaines fonctionnalités clés, telles que : [Modèles de contenu](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Attributs calculés](../audience/computed-attributes.md), [Canal Courrier](../direct-mail/get-started-direct-mail.md), [Balises](../start/search-filter-categorize.md#tags), [Modèles d’optimisation de la gestion des décisions](../offers/ranking/personalized-optimization-model.md), [Campagnes déclenchées par l’API](../campaigns/api-triggered-campaigns.md), et [Expérience de contenu](../campaigns/content-experiment.md).
* Le processus de création de schémas a été mis à jour pour prendre en compte les dernières mises à jour apportées à l’interface utilisateur, avec des modifications apportées à Adobe Experience Platform. [En savoir plus](../audience/creating-test-profiles.md)
* Les barrières de sécurité de la gestion des décisions ont été ajoutées à la page Barrières de sécurité et limites . [En savoir plus](../start/guardrails.md#decision-management)
* Une nouvelle section sur la prévisualisation et le test de votre contenu a été créée. [En savoir plus](../content-management/preview-test.md)

## Septembre 2023 {#september-2023}

* Toutes les nouvelles fonctionnalités et améliorations de la version de septembre 2023 de [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Une nouvelle page contenant les bonnes pratiques de mise à l’échelle et des conseils de connexité en temps réel a été ajoutée. [En savoir plus](../start/best-practices.md)

  <!--  * The maximum wait duration has been changed from 30 to 29 days. [Read more](../building-journeys/wait-management.md) -->

* Une section Questions fréquentes a été ajoutée pour l’optimisation de l’heure d’envoi. [En savoir plus](../building-journeys/journeys-message.md#faq-send-time)
* Une note a été ajoutée pour l’activité de qualification de l’audience. L’activation et l’écoute des profils entrant ou sortant de l’audience peuvent prendre jusqu’à 10 minutes. [En savoir plus](../building-journeys/audience-qualification-events.md#important-notes-segment-qualification)
* Une liste des limites à connaître lors de la création de règles de décision a été ajoutée à la documentation de la gestion des décisions. [En savoir plus](../offers/offer-library/creating-decision-rules.md)
* Les liens vers la documentation sur le contrôle d’accès ont été mis à jour. [En savoir plus](../administration/permissions.md)
* Les conditions préalables du canal in-app ont été mises à jour avec les détails de la collecte de données Adobe Experience Platform. [En savoir plus](../in-app/inapp-configuration.md)
* Certaines expressions présentées dans des exemples de formule de classement ont été mises à jour afin d’éviter les erreurs de validation. [En savoir plus](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* Un avertissement a été ajouté à la variable **Définition des portées de décision** pour indiquer que si le modèle d’AI est utilisé dans un groupe de critères d’évaluation, tous les critères d’évaluation de ce groupe doivent utiliser la méthode de classement d’AI, avec le même modèle d’AI spécifique. En outre, un seul groupe de critères d’évaluation peut utiliser le modèle d’IA. [En savoir plus](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## Août 2023 {#august-2023}

* Toutes les nouvelles fonctionnalités et améliorations de la version du 23 août de [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* La note concernant la **gestion du cache d’authentification** dans le parcours a été mise à jour afin de préciser que le jeton n’est pas partagé entre différents parcours. [En savoir plus](../datasource/external-data-sources.md#custom-authentication-mode)
* La page sur la **Gestion des entrées** des parcours a été mise à jour afin de clarifier le comportement. [En savoir plus](../building-journeys/entry-management.md)
* L’option **Exporter des jeux de données** pour Offer Decisioning est désormais activée par défaut. La note sur le comportement précédent a été supprimée.  [En savoir plus](../offers/export-catalog/get-started-export.md)
* Diverses **mesures des rapports de campagne** ont été renommées dans les rapports dynamiques et globaux. [En savoir plus](../reports/campaign-global-report.md)
* Ajout d’une section sur les conditions préalables des expériences de contenu pour le canal web. [En savoir plus](../web/web-prerequisites.md#experiment-prerequisites)
* Ajout d’un avertissement sur la page **Utiliser les modèles de contenu** pour indiquer que le suivi actuel n’est pas pris en charge lors du test des modèles de contenu d’e-mail. Pour tester le suivi, vous devez utiliser le modèle de contenu d’un e-mail et envoyer un BAT. [En savoir plus](../content-management/content-templates.md#test-template)
* Ajout de plusieurs avertissements dans la section **Créer et publier des pages de destination** pour indiquer que vous ne pouvez pas accéder à votre page de destination en copiant-collant dans un navigateur web l’URL définie lors de la création de la page, même si elle est publiée. Testez-la plutôt à l’aide de la fonction de prévisualisation. [En savoir plus](../landing-pages/create-lp.md)
* Une section a été ajoutée sur la procédure à suivre pour **gérer le consentement** du canal courrier. [En savoir plus](../direct-mail/test-send-direct-mail.md)

## Juillet 2023 {#july-2023}

* Toutes les nouvelles fonctionnalités et améliorations de la version du 23 juillet de [!DNL Journey Optimizer] sont présentées dans la documentation. [En savoir plus](release-notes.md)
* La page de documentation sur l’activité d’attente a été enrichie avec des informations supplémentaires et des bonnes pratiques relatives à la temporisation globale et à l’utilisation de la reprise. [En savoir plus](../building-journeys/wait-activity.md)
* La page sur la gestion des entrées a été améliorée. [En savoir plus](../building-journeys/entry-management.md)
* Des informations supplémentaires sur le taux de limitation ont été ajoutées dans la documentation sur l’activité Lecture d’audience. [En savoir plus](../building-journeys/read-audience.md)
* Des informations supplémentaires sur les reprises ont été ajoutées. [En savoir plus](../start/guardrails.md#general-actions-g)
* La section **Implémenter le consentement de personnalisation** a été mise à jour de sorte à décrire comment appliquer manuellement le consentement à la personnalisation dans les campagnes : vous pouvez utiliser le créateur de règles de segmentation pour créer une audience contenant des profils d’exclusion ou ajouter une activité de partage à un workflow de composition. [En savoir plus](../privacy/opt-out.md#opt-out-expression-editor)

## Juin 2023 {#june-2023}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] du 23 juin ont été présentées dans la documentation. [En savoir plus](release-notes.md).
* Des informations ont été ajoutées sur le ratio de rejet dans l’écran de présentation des Parcours. [En savoir plus](../building-journeys/journey-gs.md#journey-access)
* Une note a été ajoutée avec les étapes à suivre si vous souhaitez modifier un schéma avec de nouvelles valeurs d’énumération après la création d’un événement. [En savoir plus](../event/about-creating.md)
* Une recommandation a été ajoutée pour utiliser journeyVersionID au lieu de journeyVersionName lors de l’interrogation d’un parcours. [En savoir plus](../reports/sharing-common-fields.md#journeyversionid-field).
* Des exemples supplémentaires sur l’ordre des critères d’évaluation ont été ajoutés à la section **Créer des décisions** pour illustrer les cas où plusieurs critères et portées de décision sont utilisés. [En savoir plus](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order).
* La documentation de la gestion des décisions a été clarifiée avec une note indiquant que l’utilisation du contrôle d’accès au niveau de l’objet n’est pas disponible pour les collections dynamiques. [En savoir plus](../offers/offer-library/creating-collections.md).

## Mai 2023 {#may-2023}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] du 23 mai ont été présentées dans la documentation. [En savoir plus](release-notes.md).
* Une nouvelle page a été ajoutée pour décrire comment configurer le sous-domaine qui sera utilisé pour publier du contenu provenant d’Adobe Experience Manager Assets Essentials dans vos expériences web. [En savoir plus](../web/web-delegated-subdomains.md).
* Une nouvelle sous-section a été ajoutée pour expliquer comment ajouter des paramètres de tracking personnalisés aux URL dans le concepteur d’e-mail. [En savoir plus](../email/message-tracking.md#url-tracking).
* Une nouvelle section a été ajoutée pour décrire comment garantir le respect du choix de vos clientes et clients qui refusent l’utilisation de leurs données de profil pour la personnalisation. [En savoir plus](../privacy/opt-out.md#opt-out-personalization).
* Un note a été ajoutée sur l’utilisation de caractères internationaux spéciaux dans les URL incluses dans les contenus d’e-mail. [En savoir plus](../email/message-tracking.md#insert-links).
* L’autorisation nécessaire pour tester et publier des pages de destination a été ajoutée. [En savoir plus](../landing-pages/create-lp.md).
* Une note a été ajoutée au sujet des points d’entrée Adobe Experience Platform nécessaires pour que vos événements personnalisés soient pris en compte dans le capping de la fréquence de la gestion des décisions. [En savoir plus](../offers/data-collection/schema-requirement.md#track-custom-events).

## Avril 2023 {#apr-2023}

* Toutes les nouvelles fonctionnalités et améliorations de la version d’avril 2023 de [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md).
* Une note a été ajoutée pour indiquer que les actions intégrées ne peuvent pas être supprimées. [En savoir plus](../start/guardrails.md#custom-actions-g)
* Des informations ont été ajoutées sur serviceEvents ainsi qu’un exemple de requête pour vérifier les détails d’un serviceEvent. [En savoir plus](../reports/query-examples.md#common-queries)
* Une note a été ajoutée pour indiquer que vous ne pouvez pas exécuter de requêtes sur des séries temporelles. [En savoir plus](../building-journeys/condition-activity.md).
* Adobe Experience Manager Assets Essentials et Adobe Stock ont été ajoutés à la page d’intégration multi-solution. [En savoir plus](../start/ajo-integrations.md).
* L’avertissement sur les sous-domaines de messagerie à plusieurs niveaux non autorisés a été supprimé, car ils sont désormais pris en charge. [En savoir plus](../configuration/delegate-subdomain.md).
* Une note a été ajoutée pour indiquer que, si des modifications sont apportées à une décision d’offres utilisée dans le message d’un parcours, vous devez dépublier le parcours puis le republier. [En savoir plus](../building-journeys/publishing-the-journey.md).
* La gestion des décisions a clarifié la manière de s’assurer que les événements sont correctement pris en compte dans la section **Événement de limitation**. [En savoir plus](../offers/offer-library/add-constraints.md#capping-event).
* Une nouvelle section a été ajoutée à la page **Modifier les adresses d’exécution**. Elle indique qu’il est possible de remplacer le champ d’exécution défini globalement dans les paramètres avancés du parcours, mais que le remplacement de l’adresse e-mail ne doit être utilisé que pour des cas d’utilisation spécifiques. La plupart du temps, la valeur définie comme adresse principale dans les **Champs d’exécution** est celle qui doit être utilisée. [En savoir plus](../configuration/primary-email-addresses.md#journey-parameters)
* La section **Suivi des URL** fournit désormais la liste et la description de tous les attributs contextuels pouvant être définis pour le suivi des URL dans une surface de canal d’e-mail. [En savoir plus](../email/email-settings.md#url-tracking).

## Mars 2023 {#march-2023}

* Le dictionnaire de schémas Journey Optimizer est maintenant disponible. Vous y trouverez la liste complète des champs et attributs de chaque schéma.  [En savoir plus](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=fr).
* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] de mars 2023 ont été présentées dans la documentation. [En savoir plus](release-notes.md).
* Ajout d’une étape pour activer les événements d’Adobe Analytics dans vos parcours. [En savoir plus](../event/about-analytics.md).
* Une nouvelle section a été créée dans le guide consacré à la gestion des décisions, sur la manière de collecter les commentaires relatifs à la prise de décisions sur les offres dans Adobe Experience Platform, y compris les offres affichées et la manière dont les utilisateurs et utilisatrices interagissent avec elles. [En savoir plus](../offers/data-collection/data-collection.md).
* Ajout d’une nouvelle sous-section à la section **Créer une décision**, qui informe sur la différence entre l’évaluation des critères dans un ordre séquentiel ou en même temps. [En savoir plus](../offers/offer-activities/create-offer-activities.md#evaluation-criteria-order).
* Ajout d’un mécanisme de sécurisation pour les parcours de lecture d’audience avec lecture incrémentielle. La création d’une nouvelle version n’est pas possible, vous devez dupliquer le parcours. [En savoir plus](../start/guardrails.md#journey-versions-g)
* Le cas d’utilisation sur la limitation du débit a été mis à jour avec des informations sur les fonctionnalités de limitation. [En savoir plus](../building-journeys/limit-throughput.md)
* Une note a été ajoutée pour indiquer que les tableaux scalaires ne sont pas pris en charge dans la définition de la payload de réponse. [En savoir plus](../datasource/external-data-sources.md)
* La section sur les conditions de limite des profils a été mise à jour. [En savoir plus](../building-journeys/condition-activity.md#profile_cap).

## Février 2023 {#feb-2023}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] de février 2023 ont été présentées dans la documentation. [En savoir plus](release-notes.md).
* Des informations sur la barre d’outils de la zone de travail ont été ajoutées. [En savoir plus](../building-journeys/using-the-journey-designer.md#gs-journey-design)
* Des informations ont été ajoutées pour indiquer que les adresses internes d’Adobe ne sont pas autorisées dans les URL et les API. [En savoir plus](../start/guardrails.md).
* Une note a été ajoutée dans la documentation des campagnes déclenchées par l’API pour indiquer que les attributs contextuels transmis dans la requête ne peuvent pas dépasser 50 Ko. [En savoir plus](../campaigns/api-triggered-campaigns.md#contextual).
* Des informations ont été ajoutées, décrivant la manière dont les informations de désinscription (opt-out) sont stockées dans le **jeu de données du service de consentement** une fois que les destinataires se sont désabonnés via une page de destination. [En savoir plus](../landing-pages/lp-use-cases.md#configure-opt-out).

## Janvier 2023 {#jan-2023}

* Toutes les nouvelles fonctionnalités et améliorations de la version de janvier 2023 de [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md).
* Des informations ont été ajoutées sur les points d’entrée d’authentification personnalisés dans la documentation sur les limites. [En savoir plus](../configuration/external-systems.md)
* Un nouvel exemple d’authentification personnalisée a été ajouté à la section Sources de données externes. [En savoir plus](../datasource/external-data-sources.md#custom-authentication-mode)
* Une note a été ajoutée concernant le Core Service de collecte de données (DCCS) pour les parcours déclenchés par un événement. [En savoir plus](../start/guardrails.md#events-g)
* Une note sur la récupération des espaces de noms d’identité a été ajoutée dans les sections [Lecture d’audience](../building-journeys/read-audience.md), [Qualification d’audience](../building-journeys/audience-qualification-events.md) et [Création d’événement](../event/about-creating.md).
* Les fonctionnalités d’accessibilité dans [!DNL Journey Optimizer] sont désormais regroupées dans une page dédiée. [En savoir plus](../start/accessibility.md).
* Les exemples ont été mis à jour dans la section Opérateurs de la documentation de l’éditeur d’expression avancé. [En savoir plus](../building-journeys/expression/operators.md)
* Une note a été ajoutée concernant la limitation de recherche avec un tableau d’objets. [En savoir plus](../event/experience-event-schema.md#relationships_limitations).
* Ajout d’une nouvelle page sur la gestion des données dans [!DNL Journey Optimizer]. [En savoir plus](../data/gs-data.md).
* Ajout d’un tableau répertoriant tous les codes qui peuvent être renvoyés dans la réponse lors de la diffusion d’offres à l’aide de l’API Decisioning. [En savoir plus](../offers/api-reference/offer-delivery-api/decisioning-api.md).

+++ 2022

## Décembre 2022 {#december-2022}

* Le guide Messages a été réorganisé et divisé en guides dédiés pour chaque canal :

   * [Canal e-mail](../email/get-started-email.md)
   * [Canal des notifications push](../push/get-started-push.md)
   * [Canal SMS](../sms/get-started-sms.md)

* Le guide de configuration a été réorganisé pour une meilleure lisibilité. [En savoir plus](../configuration/get-started-configuration.md).

## Novembre 2022 {#november-2022}

* Ajout d’une nouvelle page sur les intégrations de Journey Optimizer. [En savoir plus](../start/ajo-integrations.md)
* Ajout d’une recommandation sur la longueur des URL des pages miroir. [En savoir plus](../email/message-tracking.md)
* Ajout d’une nouvelle sous-section dans la configuration des paramètres d’e-mail concernant la réponse à l’adresse e-mail, y compris des recommandations pour assurer une gestion adéquate des réponses. [En savoir plus](../email/email-settings.md#reply-to-email)
* Ajout d’une section relative à la modification du contenu d’un message dans un parcours actif. [En savoir plus](../building-journeys/journeys-message.md#update-live-content)

## Octobre 2022 {#october-2022}

* Ajout d’un cas d’utilisation de parcours sur la manière de limiter le débit à l’aide de sources de données externes et d’actions personnalisées. [En savoir plus](../building-journeys/limit-throughput.md)
* La section Cas d’utilisation de parcours a été réorganisée en deux catégories : [Cas d’utilisation commerciale](../building-journeys/journeys-uc.md) et [Cas d’utilisation technique](../building-journeys/collections.md).
* La section **Jeu de données d’entité** a été mise à jour avec plus de détails. [En savoir plus](../data/datasets-query-examples.md#entity-dataset)
* Les sections Gestion de la désinscription et Politiques de consentement ont subi une refonte. [En savoir plus](../privacy/opt-out.md)
* La section sur les paramètres avancés des messages de parcours a été clarifiée et précise désormais que le remplacement des adresses e-mail ne doit être utilisé que pour des cas d’utilisation spécifiques. La plupart du temps, la valeur définie comme adresse principale dans les **Champs d’exécution** est celle qui doit être utilisée.
* Ajout d’une note à la section **Configuration des sous-domaines de page de destination** pour indiquer que les majuscules ne sont pas autorisées dans les sous-domaines de la page de destination. [En savoir plus](../landing-pages/lp-subdomains.md)

## Septembre 2022 {#september-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version de septembre 2022 de [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Ajout d’une bonne pratique liée à l’utilisation des activités d’attente dans les parcours de lecture d’audience récurrents. [En savoir plus](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Ajout d’exemples de requête d’événement d’étape, ainsi que d’informations sur la différence entre id, instanceid et profileid. [En savoir plus](../reports/query-examples.md).
* Mise à jour des pages relatives aux fonctions [toDateOnly](../building-journeys/functions/functiontodateonly.md) et [toString](../building-journeys/functions/functiontostring.md).
* Ajout de détails sur les paramètres de condition de temps. [En savoir plus](../building-journeys/condition-activity.md#time_condition)
* Ajout d’informations sur les jeux de données intégrés. [En savoir plus](../data/get-started-datasets.md#access-datasets)
* Amélioration et réorganisation des sections Rapport global et Rapport dynamique. [En savoir plus](../reports/global-report.md)
* Une liste de toutes les mesures de création de rapports disponibles dans Adobe Journey Optimizer a été ajoutée.
  [En savoir plus](../reports/global-report.md#email-and-sms-metrics)
* La section Envoyer l’e-mail en copie (Cci) a été déplacée vers la nouvelle page Prise en charge de l’archivage. [En savoir plus](../configuration/archiving-support.md)

## Août 2022 {#august-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] d’août 2022 ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* La section Règles de fréquence a été mise à jour pour prendre en compte le nouveau flux de messages en ligne. [En savoir plus](../configuration/frequency-rules.md#apply-frequency-rule)
* Une vidéo montrant comment configurer les abonnements et créer des pages de destination est désormais référencée dans la section « Prise en main des pages de destination ». [En savoir plus](../landing-pages/get-started-lp.md#video)
* Ajout d’une limitation pour les parcours utilisant les activités de lecture d’audience. [En savoir plus](../building-journeys/read-audience.md).
* La page des opérateurs de l’éditeur d’expression a été améliorée. [En savoir plus](../building-journeys/expression/operators.md)
* Ajout d’une section sur la planification d’une campagne. [En savoir plus](../campaigns/create-campaign.md)
* Mise à jour de la section sur les règles de syntaxe générales de l’éditeur d’expression afin de prendre en compte la nouvelle règle concernant l’échappement du symbole barre oblique inverse dans les fonctions littérales. Les messages publiés existants ne sont pas affectés par cette modification. Seuls les nouveaux messages ou les brouillons doivent être mis à jour. [En savoir plus](../personalization/personalization-syntax.md#general-rules)

## Juillet 2022 {#july-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version du 22 juillet de [!DNL Journey Optimizer] sont présentées dans la documentation. [En savoir plus](release-notes.md)
* La section **Configurer des surfaces de canal** a été simplifiée et contient des liens vers la page décrivant comment configurer le canal SMS. [En savoir plus](../configuration/channel-surfaces.md#create-channel-surface)
* Dans les propriétés du parcours, l’option **Fuseau horaire du profil** est désormais désactivée par défaut. [En savoir plus](../building-journeys/timezone-management.md#timezone-from-profiles)
* Dans l’activité **Attente**, l’option **Date fixe** n’est plus disponible. [En savoir plus](../building-journeys/wait-activity.md)
* Des informations supplémentaires ont été ajoutées sur l’option **Lecture incrémentielle** dans l’activité **Lecture d’audience**. [En savoir plus](../building-journeys/read-audience.md#configuring-segment-trigger-activity)
* Des recommandations ont été ajoutées concernant le type de condition **Limite de profil**. [En savoir plus](../building-journeys/condition-activity.md#profile_cap)
* Une limitation sur les événements métier a été ajoutée. [En savoir plus](../start/guardrails.md#events-g)

## Juin 2022 {#june-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] du 22 juin ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Une nouvelle section sur les demandes d’accès à des informations personnelles a été ajoutée à la documentation. [En savoir plus](../privacy/requests.md)
* Une nouvelle section sur les journaux d’audit des ressources a été ajoutée à la documentation. [En savoir plus](../privacy/audit-logs.md)
* Une nouvelle section sur la façon d’ajouter du contenu HTML ou JSON, provenant de la bibliothèque de ressources Adobe Experience Cloud, à un rendu d’offre a été ajoutée à la documentation. [En savoir plus](../offers/offer-library/add-representations.md#html-json)
* Ajout d’une nouvelle page sur le cycle de vie des parcours. [En savoir plus](../building-journeys/journey.md#journey-versions)
* Mise à jour de la page Activité d’attente. [En savoir plus](../building-journeys/wait-activity.md)
* Ajout de la liste des jeux de données Adobe Journey Optimizer avec des exemples de requête. [En savoir plus](../data/datasets-query-examples.md)
* La page Liste autorisée a été déplacée vers la section Configuration. [En savoir plus](../configuration/allow-list.md)
* La page Liste de suppression a été mise à jour afin de clarifier certaines informations, notamment le fait que tous les caractères ASCII compris entre 32 et 126 sont autorisés dans le champ de motif de suppression. [En savoir plus](../configuration/manage-suppression-list.md)
* Ajout du lien vers les mécanismes de sécurisation et les limites statiques pour la gestion des décisions. [En savoir plus](../start/guardrails.md)
* L’optimisation de l’heure d’envoi est désormais disponible pour tous les clients. La mention Beta a été supprimée. [En savoir plus](../building-journeys/journeys-message.md#send-time-optimization)
* L’API Batch Decisioning a été ajoutée à la liste des API disponibles pour diffuser des offres personnalisées. [En savoir plus](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)

## Mai 2022 {#may-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] du 22 mai ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* De nouveaux exemples de requête liés à la [qualification d’audience](../reports/query-examples.md#segment-qualification-queries) et aux [événements](../reports/query-examples.md#event-based-queries) ont été ajoutés.
* La section Conception d’e-mail mentionne désormais les nouveaux modèles intégrés disponibles pour commencer le contenu. Les captures d’écran connexes ont été mises à jour. [En savoir plus](../email/get-started-email-design.md)
* Des liens vers des ressources clés ont été mis à jour dans la page d’accueil de la documentation Journey Optimizer.
* Les captures d’écran pour les rapports d’abonnement et de page de destination ont été mises à jour. [En savoir plus](../reports/live-report.md)
* Une note a été ajoutée indiquant que la méthode Delete n’est pas prise en charge dans les actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md)
* Des liens vers des vidéos pratiques ont été mis à jour.
* Les sections [Configuration du canal e-mail](../configuration/about-subdomain-delegation.md), [Préréglages de message](../configuration/channel-surfaces.md) et [Configuration des pages de destination](../landing-pages/lp-subdomains.md) ont été réorganisées afin d’en améliorer la lisibilité.
* La section Tracking des URL a été mise à jour et enrichie avec des exemples. [En savoir plus](../email/email-settings.md#url-tracking)
* Ajout d’une nouvelle sous-section sur la configuration d’une adresse e-mail de transfert. Notez que vous ne pouvez pas le faire via l’interface utilisateur. [En savoir plus](../email/email-settings.md#forward-email)

## Avril 2022 {#april-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version d’avril 2022 de [!DNL Journey Optimizer] ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* La page de documentation sur les événements de **réaction** a été mise à jour. [En savoir plus](../building-journeys/reaction-events.md)
* Les vidéos relatives aux fonctionnalités de gestion des décisions ont été mises à jour pour refléter l’interface utilisateur de Journey Optimizer. [En savoir plus](../offers/get-started/starting-offer-decisioning.md)
* La section **Prise en main des jeux de données** a été améliorée afin d’expliquer en détail comment accéder aux jeux de données et les créer. [En savoir plus](../data/get-started-datasets.md)
* Des liens vers les guides d’aide et les notes de mise à jour du produit ont été ajoutés à la page d’accueil de la **Documentation d’Adobe Journey Optimizer**. [En savoir plus](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=fr)
* La section **Créer des préréglages de messages** indique désormais que vous ne pouvez pas procéder à la création de préréglages tant que le groupe d’adresses IP sélectionné est en cours d’édition (statut de **[!UICONTROL traitement]**) et n’a jamais été associé au sous-domaine sélectionné. [En savoir plus](../configuration/channel-surfaces.md#subdomains-and-ip-pools)
* La section **Suivi des URL** des préréglages de messages a été mise à jour pour refléter des changements mineurs dans l’interface utilisateur. [En savoir plus](../configuration/channel-surfaces.md#url-tracking)

## Mars 2022 {#march-2022}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] de mars 2022 ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Ajout dʼune nouvelle page sur la prise en main des modèles dʼIA dans la section **Offer Decisioning**, comprenant une description approfondie du [modèle d’optimisation automatique](../offers/ranking/auto-optimization-model.md), l’algorithme qu’il utilise et dʼautres détails techniques. [En savoir plus](../offers/ranking/ai-models.md)
* La page de création du profil de test a été déplacée vers la section **Audience, profils et identité**. [En savoir plus](../audience/creating-test-profiles.md)
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
* Mise à jour de la section **Classements par l’IA dʼOffer Decisioning** afin de fournir une description plus détaillée du modèle d’optimisation automatique. [En savoir plus](../offers/ranking/auto-optimization-model.md).
* Ajout d’une nouvelle section sur les exigences relatives aux schémas requises pour pouvoir envoyer des types d’événements lors de l’utilisation d’un modèle d’IA. [En savoir plus](../offers/data-collection/schema-requirement.md).
* La section relative aux capacités de personnalisation de [!DNL Journey Optimizer] a été réorganisée pour une meilleure lisibilité. [En savoir plus](../personalization/personalize.md)
* La section **Création de préréglages de message** a été divisée en plusieurs sections afin d’en améliorer la clarté. [En savoir plus](../configuration/channel-surfaces.md#create-channel-surface)
* La section **Gestion des processus d’opt-out** a été clarifiée et légèrement réorganisée. [En savoir plus](../privacy/opt-out.md#opt-out-management)
* La section **Insérer des liens** a été mise à jour pour prendre en compte les modifications récentes de l’interface utilisateur. [En savoir plus](../email/message-tracking.md#insert-links).

+++

+++ 2021

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

* Ajout d’une sous-section pour clarifier les différences entre l’utilisation des audiences et celle des règles de décision lors de l’application d’une contrainte afin de restreindre la sélection des offres pour un emplacement donné. [En savoir plus](../offers/offer-activities/create-offer-activities.md#segments-vs-decision-rules)

* Ajout d’exemples de formule de classement spécifiques pour illustrer certains cas d’utilisation réels. [En savoir plus](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)

* Ajout d’une sous-section sur la modification des groupes d’adresses IP. [En savoir plus](../configuration/ip-pools.md#edit-ip-pool)

## Août 2021 {#august-2021}

* Toutes les nouvelles fonctionnalités et améliorations de la version [!DNL Journey Optimizer] du 21 août ont été présentées dans la documentation. [En savoir plus](release-notes.md)
* Mise à jour des autorisations de la gestion des décisions. [En savoir plus](../administration/ootb-product-profiles.md)
* Mise à jour des captures d’écran du concepteur d’e-mails avec la dernière interface utilisateur.
* Mise à jour de la procédure de configuration pour les actions personnalisées avec les chemins d’URL dynamiques et les en-têtes dynamiques. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration)
* Ajout d’une section sur les fonctions d’accessibilité et les raccourcis. [En savoir plus](../start/user-interface.md#accessibility)
* Ajout d’une section sur les méthodes d’évaluation des audiences. [En savoir plus](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* Ajout de notes aux sections de rapport Liste de suppression, Liste autorisée et E-mail global/direct pour indiquer que les profils avec les statuts Supprimé et Non autorisé sont exclus des mesures Envoyer le rapport par e-mail. [En savoir plus](../reports/global-report.md)
* Ajout d’une nouvelle section pour décrire comment récupérer les adresses e-mail ou les domaines qui ont été exclus d’un envoi car ils ne se trouvaient pas sur la liste autorisée. [En savoir plus](../configuration/allow-list.md#reporting)
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
* Déplacement, amélioration et changement du nom de la section « Suivi des messages » en « Ajouter des liens et suivre les messages ». [En savoir plus](../email/message-tracking.md)
* Ajout d’une sous-section aux pages miroir. [En savoir plus](../email/message-tracking.md#mirror-page)
* Renommez « activités d’offre » en « décisions » et « décisions » en « portées de décision » dans la documentation et les écrans. [En savoir plus](../offers/get-started/starting-offer-decisioning.md)
* Nouveau cas d’utilisation : [personnaliser un message avec des fonctions helper](../personalization/personalization-use-case-helper-functions.md)
* Mise à jour de la documentation sur la lecture d’audience pour prendre en compte les effets sur les segments matérialisés. [En savoir plus](../building-journeys/read-audience.md)
* Mise à jour des limites de parcours. [En savoir plus](../start/guardrails.md)
* Mise à jour de la section Configurer la sélection des offres dans les décisions. [En savoir plus](../offers/offer-activities/configure-offer-selection.md)
* Ajout d&#39;un avertissement indiquant que les offres basées sur un événement ne sont actuellement pas prises en charge. [En savoir plus](../offers/offer-library/creating-personalized-offers.md#eligibility)
* Documentation du nouvel onglet **[!UICONTROL Aperçu]** de la gestion des décisions. [En savoir plus](../offers/get-started/user-interface.md#overview)
* Ajout de nouvelles sections pour décrire les actions disponibles dans les listes des offres et des décisions : [Liste des offres](../offers/offer-library/creating-personalized-offers.md#offer-list) et [Répertorier les décisions](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
