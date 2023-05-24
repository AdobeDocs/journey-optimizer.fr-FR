---
product: Journey Optimizer
audience: end-user
user-guide-title: Guide de Journey Optimizer
user-guide-description: Utilisez Journey Optimizer pour créer et proposer aux clients des expériences connectées, contextuelles et personnalisées
type: Documentation
solution: Journey Optimizer
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: ht
source-wordcount: '1370'
ht-degree: 100%

---

# Aide d’Adobe Journey Optimizer {#using}

+ [Documentation Journey Optimizer](ajo-home.md)
+ Nouveautés {#whats-new}
   + [Dernières notes de mise à jour de](using/rn/release-notes.md)
   + Notes de mise à jour précédentes {#previous-rn-new}
      + [Notes de mise à jour 2022](using/rn/release-notes-2022.md)
      + [Notes de mise à jour 2021](using/rn/release-notes-2021.md)
   + [Mises à jour de la documentation](using/rn/documentation-updates.md)
+ Prise en main{#get-started}
   + [Qu’est-ce que Journey Optimizer ?](using/start/get-started.md)
   + Guides de démarrage rapide{#quick-start}
      + [Présentation](using/start/quick-start.md)
      + [Prise en main en tant que marketeur](using/start/path/marketer.md)
      + [Prise en main en tant qu’ingénieur de données](using/start/path/data-engineer.md)
      + [Prise en main en tant qu’administrateur](using/start/path/administrator.md)
      + [Prise en main en tant que développeur](using/start/path/developer.md)
   + [Interface utilisateur](using/start/user-interface.md)
   + [Recherche, filtrage, catégorisation](using/start/search-filter-categorize.md)
   + [Accessibilité](using/start/accessibility.md)
   + [Intégrations](using/start/ajo-integrations.md)
   + [Mécanismes de sécurisation](using/start/guardrails.md)
+ Parcours {#orchestrate-journeys}
   + [Prise en main des parcours](using/building-journeys/journey.md)
   + Création d’un parcours{#create-journey}
      + [Créer votre premier parcours](using/building-journeys/journey-gs.md)
      + [Concevoir le parcours](using/building-journeys/using-the-journey-designer.md)
      + [Tester votre parcours](using/building-journeys/testing-the-journey.md)
      + [Publier votre parcours](using/building-journeys/publishing-the-journey.md)
   + Gestion des parcours{#manage-journey}
      + [Fin de votre parcours](using/building-journeys/end-journey.md)
      + [Gestion des fuseaux horaires](using/building-journeys/timezone-management.md)
      + [Gestion des entrées de profil](using/building-journeys/entry-management.md)
      + [Copier un parcours dans un autre sandbox](using/building-journeys/copy-to-sandbox.md)
      + [Dépannage de votre parcours](using/building-journeys/troubleshooting.md)
      + [Intégration avec les services intelligents](using/building-journeys/ai-services-overview.md)
   + Activités {#about-journey-building}
      + [Prise en main des activités de parcours](using/building-journeys/about-journey-activities.md)
      + [Événements généraux](using/building-journeys/general-events.md)
      + [Réaction](using/building-journeys/reaction-events.md)
      + [Qualification du segment](using/building-journeys/segment-qualification-events.md)
      + [Condition](using/building-journeys/condition-activity.md)
      + [Attente](using/building-journeys/wait-activity.md)
      + [Lecture de segment](using/building-journeys/read-segment.md)
      + [E-mail, in-app, push, SMS](using/building-journeys/journeys-message.md)
      + [Actions personnalisées](using/building-journeys/using-custom-actions.md)
      + [Actions d&#39;Adobe Campaign Standard](using/building-journeys/using-adobe-campaign-standard.md)
      + [Actions d’Adobe Campaign v7/v8](using/building-journeys/using-adobe-campaign-classic.md)
      + [Saut](using/building-journeys/jump.md)
      + [Mise à jour du profil](using/building-journeys/update-profiles.md)
   + Création d’expressions {#building-advanced-conditions-journeys}
      + [Présentation](using/building-journeys/expression/expressionadvanced.md)
      + Syntaxe {#syntax}
         + [Généralités](using/building-journeys/expression/generalities.md)
         + [Instruction conditionnelle](using/building-journeys/expression/conditional-instruction.md)
         + [Types de données](using/building-journeys/expression/data-types.md)
         + [Références de champ](using/building-journeys/expression/field-references.md)
         + [Fonctions de gestion des collections](using/building-journeys/expression/collection-management-functions.md)
         + [Opérateurs](using/building-journeys/expression/operators.md)
         + [Propriétés du parcours](using/building-journeys/expression/journey-properties.md)
         + [Exemples](using/building-journeys/expression/advanced-editor-use-cases.md)
      + Fonctions {#main-functions-journey}
         + [Fonctions principales](using/building-journeys/expression/functions.md)
         + Adobe Experience Platform {#adobe-experience-platform}
            + [inSegment](using/building-journeys/functions/functioninsegment.md)
         + Agrégation {#aggregation}
            + [avg](using/building-journeys/functions/functionavg.md)
            + [count](using/building-journeys/functions/functioncount.md)
            + [countOnlyNull](using/building-journeys/functions/functioncountonlynull.md)
            + [countWithNull](using/building-journeys/functions/functioncountwithnull.md)
            + [distinctCount](using/building-journeys/functions/functiondistinctcount.md)
            + [distinctCountWithNull](using/building-journeys/functions/functiondistinctcountwithnull.md)
            + [max](using/building-journeys/functions/functionmax.md)
            + [min](using/building-journeys/functions/functionmin.md)
            + [sum](using/building-journeys/functions/functionsum.md)
         + Conversion {#conversion}
            + [toBool](using/building-journeys/functions/functiontobool.md)
            + [toDateOnly](using/building-journeys/functions/functiontodateonly.md)
            + [toDateTime](using/building-journeys/functions/functiontodatetime.md)
            + [toDateTimeOnly](using/building-journeys/functions/functiontodatetimeonly.md)
            + [toDecimal](using/building-journeys/functions/functiontodecimal.md)
            + [toDuration](using/building-journeys/functions/functiontoduration.md)
            + [toInteger](using/building-journeys/functions/functiontointeger.md)
            + [toString](using/building-journeys/functions/functiontostring.md)
         + Date {#date}
            + [currentTime&#x200B;InMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
            + [inLastDays](using/building-journeys/functions/functioninlastdays.md)
            + [inLastHours](using/building-journeys/functions/functioninlasthours.md)
            + [inLastMonths](using/building-journeys/functions/functioninlastmonths.md)
            + [inLastYears](using/building-journeys/functions/functioninlastyears.md)
            + [inNextDays](using/building-journeys/functions/functioninnextdays.md)
            + [inNextHours](using/building-journeys/functions/functioninnexthours.md)
            + [inNextMonths](using/building-journeys/functions/functioninnextmonths.md)
            + [inNextYears](using/building-journeys/functions/functioninnextyears.md)
            + [now](using/building-journeys/functions/functionnow.md)
            + [nowWithDelta](using/building-journeys/functions/functionnowwithdelta.md)
            + [setHours](using/building-journeys/functions/functionsethours.md)
            + [setDays](using/building-journeys/functions/functionsetdays.md)
            + [updateTimeZone](using/building-journeys/functions/functionupdatetimezone.md)
         + Liste {#list}
            + [distinct](using/building-journeys/functions/functiondistinct.md)
            + [distinctWithNull](using/building-journeys/functions/functiondistinctwithnull.md)
            + [filter](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [in](using/building-journeys/functions/functionin.md)
            + [intersect](using/building-journeys/functions/functionintersect.md)
            + [limite](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [sort](using/building-journeys/functions/functionsort.md)
         + Math {#math}
            + [random](using/building-journeys/functions/functionrandom.md)
            + [round](using/building-journeys/functions/functionround.md)
         + Chaîne {#string}
            + [concat](using/building-journeys/functions/functionconcat.md)
            + [contain](using/building-journeys/functions/functioncontain.md)
            + [containIgnoreCase](using/building-journeys/functions/functioncontainwithignorecase.md)
            + [endWith](using/building-journeys/functions/functionendwith.md)
            + [endWithIgnorecase](using/building-journeys/functions/functionendwithignorecase.md)
            + [equalIgnoreCase](using/building-journeys/functions/functionequalignorecase.md)
            + [indexOf](using/building-journeys/functions/functionindexof.md)
            + [isEmpty](using/building-journeys/functions/functionisempty.md)
            + [isNotEmpty](using/building-journeys/functions/functionisnotempty.md)
            + [lastIndexOf](using/building-journeys/functions/functionlastindexof.md)
            + [length](using/building-journeys/functions/functionlength.md)
            + [lower](using/building-journeys/functions/functionlower.md)
            + [matchRegExp](using/building-journeys/functions/functionmatchregexp.md)
            + [notequalIgnoreCase](using/building-journeys/functions/functionnotequalignorecase.md)
            + [replace](using/building-journeys/functions/functionreplace.md)
            + [replaceAll](using/building-journeys/functions/functionreplaceall.md)
            + [split](using/building-journeys/functions/functionsplit.md)
            + [startWith](using/building-journeys/functions/functionstartwith.md)
            + [startWithIgnoreCase](using/building-journeys/functions/functionstartwithignorecase.md)
            + [substr](using/building-journeys/functions/functionsubstr.md)
            + [trim](using/building-journeys/functions/functiontrim.md)
            + [upper](using/building-journeys/functions/functionupper.md)
            + [uuid](using/building-journeys/functions/functionuuid.md)
   + Cas pratiques {#journey-use-cases}
      + Cas d’utilisation commerciale {#business-use-cases}
         + [Envoi de messages multi-canal](using/building-journeys/journeys-uc.md)
         + [Envoi de messages à l’aide de Campaign v7/v8](using/building-journeys/ajo-ac.md)
         + [Envoyer un message aux abonnés](using/building-journeys/message-to-subscribers-uc.md)
      + Cas d’utilisation technique {#technical-use-cases}
         + [Transmettre des collections de manière dynamique à l’aide d’actions personnalisées](using/building-journeys/collections.md)
         + [Accélérer les diffusions](using/building-journeys/ramp-up-deliveries-uc.md)
         + [Limiter le débit avec les sources de données externes et les actions personnalisées](using/building-journeys/limit-throughput.md)
+ Campagnes{#campaigns}
   + [Prise en main des campagnes](using/campaigns/get-started-with-campaigns.md)
   + [Création d’une campagne](using/campaigns/create-campaign.md)
   + [Vérification et activation d’une campagne](using/campaigns/review-activate-campaign.md)
   + [Gérer les campagnes](using/campaigns/modify-stop-campaign.md)
   + Expérience de contenu {#content-experiment}
      + [Prise en main de l’expérience de contenu](using/campaigns/get-started-experiment.md)
      + [Créer une expérience de contenu](using/campaigns/content-experiment.md)
      + [Présentation des calculs statistiques](using/campaigns/experiment-calculations.md)
      + [Configurer des rapports d’expérience](using/campaigns/reporting-configuration.md)
      + [Calculs statistiques dans le rapport d’expérience](using/campaigns/experiment-report-calculations.md)
   + [Déclenchement de campagnes à l’aide d’API](using/campaigns/api-triggered-campaigns.md)
+ Canal e-mail {#email}
   + [Prise en main des e-mails](using/email/get-started-email.md)
   + [Créer un e-mail](using/email/create-email.md)
   + Concevoir le contenu de vos e-mails {#design-email}
      + [Prise en main de la conception d’e-mails](using/email/get-started-email-design.md)
      + Commencer à créer du contenu {#start-creating-content}
         + [Concevoir du contenu en partant de zéro](using/email/content-from-scratch.md)
         + [Importer votre contenu](using/email/existing-content.md)
         + [Coder votre propre contenu](using/email/code-content.md)
         + [Utiliser des modèles](using/email/email-templates.md)
      + Concevoir votre contenu {#add-content}
         + [Utiliser des composants de contenu](using/email/content-components.md)
         + [Ajouter des liens et suivre les messages](using/email/message-tracking.md)
         + Gérer les ressources {#manage-asset}
            + [Utiliser Assets Essentials](using/email/assets-essentials.md)
            + [Utilisation d’Adobe Stock](using/email/stock.md)
         + [Insérer des offres personnalisées](using/email/add-offers-email.md)
         + [Génération de la version texte](using/email/text-version-email.md)
         + [Ajout d’un pré-titre](using/email/preheader.md)
      + Modifier le style {#edit-style}
         + [Prise en main du style des e-mails](using/email/get-started-email-style.md)
         + [Modifier les paramètres d’arrière-plan](using/email/backgrounds.md)
         + [Ajustement de l&#39;alignement vertical et la marge intérieure](using/email/alignment-and-padding.md)
         + [Définir un style pour les liens](using/email/styling-links.md)
         + [Ajout d’attributs de style intégrés](using/email/inline-styling.md)
   + [Prévisualiser et tester votre e-mail](using/email/preview.md)
   + [Créer des modèles de contenu](using/email/content-templates.md)
   + [Utiliser les modèles Experience Manager](using/email/aem-templates.md)
   + [Gérer les désinscriptions aux e-mails](using/email/email-opt-out.md)
   + Configurer le canal e-mail {#configure-email}
      + [Prise en main de la configuration du canal e-mail](using/email/get-started-email-config.md)
      + [Configurer les paramètres de la surface d’e-mails](using/email/email-settings.md)
+ Canal in-app{#in-app}
   + [Prise en main du canal in-app](using/in-app/get-started-in-app.md)
   + [Créer un message in-app](using/in-app/create-in-app.md)
   + [Créer un message in-app dans un parcours](using/in-app/create-in-app-journey.md)
   + [Concevoir votre contenu in-app](using/in-app/design-in-app.md)
   + [Tester et envoyer une notification in-app](using/in-app/send-in-app.md)
   + [Configurer le canal in-app](using/in-app/inapp-configuration.md)
+ Canal de notification push{#push}
   + [Prise en main des notifications push](using/push/get-started-push.md)
   + [Créer une notification push](using/push/create-push.md)
   + [Concevoir votre notification push](using/push/design-push.md)
   + [Envoyer votre notification push](using/push/send-push.md)
   + Configurer des notifications push{#push-config}
      + [Flux de notification push](using/push/push-gs.md)
      + [Configurer le canal de notification push](using/push/push-configuration.md)
      + [Workflow de démarrage rapide de l’intégration mobile](using/push/mobile-onboarding-wf.md)
+ Canal SMS{#sms}
   + [Prise en main des SMS](using/sms/get-started-sms.md)
   + [Création d’un SMS](using/sms/create-sms.md)
   + [Prévisualiser et tester votre SMS](using/sms/send-sms.md)
   + [Gérer les désinscriptions aux SMS](using/sms/sms-opt-out.md)
   + [Configurer le canal SMS](using/sms/sms-configuration.md)
   + [Configurer des sous-domaines SMS](using/sms/sms-subdomains.md)
+ Publipostage direct {#direct-mail}
   + [Créer un publipostage direct](using/direct-mail/create-direct-mail.md)
   + [Configurer le publipostage direct](using/direct-mail/direct-mail-configuration.md)
+ Canal web{#web}
   + [Prise en main du canal web](using/web/get-started-web.md)
   + [Conditions préalables requises pour les canaux web](using/web/web-prerequisites.md)
   + [Créer des expériences web](using/web/create-web.md)
   + [Créer des pages web](using/web/author-web.md)
   + [Configurer des sous-domaines web](using/web/web-delegated-subdomains.md)
+  Pages de destination {#landing-pages}
   + [Prise en main des pages de destination](using/landing-pages/get-started-lp.md)
   + [Création d’une page de destination](using/landing-pages/create-lp.md)
   + Conception du contenu {#landing-pages-design}
      + [À propos de la conception d&#39;une page de destination](using/landing-pages/design-lp.md)
      + [Création du contenu de la page de destination](using/landing-pages/lp-content.md)
      + [Création de modèles](using/landing-pages/lp-templates.md)
      + [Ajout d’un code JavaScript personnalisé](using/landing-pages/lp-custom-js.md)
   + [Créer une liste dʼabonnements](using/landing-pages/subscription-list.md)
   + [Apprendre avec des cas d’utilisation](using/landing-pages/lp-use-cases.md)
   + Configuration des pages de destination   {#lp-configuration}
      + [Configurer les sous-domaines des pages de destination](using/landing-pages/lp-subdomains.md)
      + [Définir les préréglages de page de destination](using/landing-pages/lp-presets.md)
+ Personnalisation et contenu dynamique {#personalized-dynamic-content}
   + Personnalisation {#personalization}
      + [Prise en main de la personnalisation](using/personalization/personalize.md)
      + [Contextes de personnalisation](using/personalization/personalization-contexts.md)
      + Création d’expressions {#build-expressions}
         + [Syntaxe de personnalisation](using/personalization/personalization-syntax.md)
         + Utilisation de l’éditeur d’expression {#expression-editor}
            + [À propos de l’éditeur d’expression](using/personalization/personalization-build-expressions.md)
            + [Ajouter des attributs aux favoris](using/personalization/personalization-favorites.md)
            + [Utilisation d’expressions enregistrées](using/personalization/personalization-library.md)
            + [Validation de la personnalisation](using/personalization/personalization-validation.md)
         + Fonctions helper{#functions}
            + [Prise en main des fonctions d’assistance](using/personalization/functions/functions.md)
            + [Fonctions d’agrégation](using/personalization/functions/aggregation.md)
            + [Fonctions arithmétiques](using/personalization/functions/arithmetic-functions.md)
            + [Tableaux et fonctions de liste](using/personalization/functions/arrays-list.md)
            + [Fonctions de date](using/personalization/functions/dates.md)
            + [Fonctions booléennes et de comparaison](using/personalization/functions/operators.md)
            + [Assistants](using/personalization/functions/helpers.md)
            + [Fonctions de mappage](using/personalization/functions/maps.md)
            + [Fonctions mathématiques](using/personalization/functions/math.md)
            + [Fonctions d’objet](using/personalization/functions/objects.md)
            + [Fonctions de chaîne](using/personalization/functions/string.md)
      + Cas pratiques{#personalization-use-cases}
         + [Notification de statut de la commande](using/personalization/personalization-use-case.md)
         + [E-mail d’abandon de panier](using/personalization/personalization-use-case-helper-functions.md)
   + Contenu dynamique {#dynamic}
      + [Prise en main du contenu dynamique](using/personalization/get-started-dynamic-content.md)
      + [Créer des règles conditionnelles](using/personalization/create-conditions.md)
      + [Créer du contenu dynamique](using/personalization/dynamic-content.md)
+ Segments, profils et identité{#segment}
   + Segments {#segments}
      + [Prise en main des segments](using/segment/about-segments.md)
      + [Création de segments](using/segment/creating-a-segment.md)
   + Profils{#profiles}
      + [Prise en main des profils](using/segment/get-started-profiles.md)
      + [Créer des profils de test](using/segment/creating-test-profiles.md)
   + [Identités](using/segment/get-started-identity.md)
   + Composer des audiences {#audience-orchestration}
      + [Prise en main de la composition des audiences](using/segment/get-started-audience-orchestration.md)
      + [Créer des workflows de composition](using/segment/create-compositions.md)
      + [Utiliser la zone de travail de composition](using/segment/composition-canvas.md)
      + [Accéder aux audiences et les gérer](using/segment/access-audiences.md)
   + [Utilisation des licences](using/segment/license-usage.md)
+ Suivre et surveiller {#reporting}
   + Rapport dynamique {#live-report}
      + [Prise en main du rapport dynamique](using/reports/live-report.md)
      + [Liste des composants](using/reports/live-report-components.md)
      + [Rapport dynamique sur les parcours](using/reports/journey-live-report.md)
      + [Rapport dynamique de campagne](using/reports/campaign-live-report.md)
      + [Rapport dynamique sur les pages de destination](using/reports/lp-report-live.md)
      + [Rapport dynamique sur les listes d’abonnements](using/reports/subscription-report-live.md)
   + Rapport global {#global-report}
      + [Prise en main du rapport global](using/reports/global-report.md)
      + [Liste des composants](using/reports/global-report-components.md)
      + [Rapport global sur les parcours](using/reports/journey-global-report.md)
      + [Rapport global de campagne](using/reports/campaign-global-report.md)
      + [Rapport global sur les pages de destination](using/reports/lp-report-global.md)
      + [Rapport global sur les listes d’abonnements](using/reports/subscription-report-global.md)
   + Rapports de parcours {#reports}
      + [Création de rapports de parcours](using/reports/sharing-overview.md)
      + [Liste des champs d’événement d’étape](using/reports/sharing-field-list.md)
      + Champs d’événement d’étape anciens {#legacy-step-event-fields}
         + [À propos des champs anciens](using/reports/sharing-legacy-fields.md)
         + [Champs du parcours](using/reports/sharing-journey-fields.md)
         + [Champs communs](using/reports/sharing-common-fields.md)
         + [Champs d’exécution d’action](using/reports/sharing-execution-fields.md)
         + [Champs de récupération de données](using/reports/sharing-fetch-fields.md)
         + [Champs d’identité](using/reports/sharing-identity-fields.md)
      + [Exemples de requêtes](using/reports/query-examples.md)
   + Délivrabilité {#deliverability}
      + [Prise en main de la délivrabilité](using/reports/deliverability.md)
      + [Présentation de la liste de suppression](using/reports/suppression-list.md)
   + [Alertes](using/reports/alerts.md)
   + [Utiliser Customer Journey Analytics](using/reports/cja-ajo.md)
+ Gestion des décisions {#offer-decisioning}
   + Prise en main de la gestion des décisions {#get-started-decision}
      + [À propos de la gestion des décisions](using/offers/get-started/starting-offer-decisioning.md)
      + [Interface utilisateur](using/offers/get-started/user-interface.md)
      + [Étapes clés de création et de gestion des offres](using/offers/offer-library/key-steps.md)
      + [Cas pratique : insertion d’offres dans un e-mail](using/offers/offers-e2e.md)
   + Création de composants {#create-components}
      + [Créer des emplacements](using/offers/offer-library/creating-placements.md)
      + [Création de règles de décision](using/offers/offer-library/creating-decision-rules.md)
      + [Créer des qualificateurs de collection](using/offers/offer-library/creating-tags.md)
   + Créer des classements {#rankings}
      + [Prise en main des classements](using/offers/ranking/get-started-rankings.md)
      + [Formules de classement](using/offers/ranking/create-ranking-formulas.md)
      + Modèles d’IA {#ai-models}
         + [À propos des modèles d’IA](using/offers/ranking/ai-models.md)
         + Types de modèles d’IA {#ai-model-types}
            + [Modèle dʼoptimisation automatique](using/offers/ranking/auto-optimization-model.md)
            + [Modèle d’optimisation personnalisé](using/offers/ranking/personalized-optimization-model.md)
         + [Créer des modèles d’IA](using/offers/ranking/create-ranking-strategies.md)
   + Création et gestion des offres {#managing-offers-in-the-offer-library}
      + Configuration des offres {#configure-offers}
         + [Créer des offres personnalisées](using/offers/offer-library/creating-personalized-offers.md)
         + [Ajouter des représentations](using/offers/offer-library/add-representations.md)
         + [Ajouter des contraintes](using/offers/offer-library/add-constraints.md)
      + [Créer des offres de secours](using/offers/offer-library/creating-fallback-offers.md)
      + [Créer des collections](using/offers/offer-library/creating-collections.md)
   + Création et gestion des décisions {#create-manage-activities}
      + [Création de décisions](using/offers/offer-activities/create-offer-activities.md)
      + [Configurer la sélection des offres dans les décisions](using/offers/offer-activities/configure-offer-selection.md)
      + [Création de simulations](using/offers/offer-activities/simulation.md)
   + [Utiliser la prise de décision par lots](using/offers/batch-delivery.md)
   + Collecter les données d’événement {#collect-event-data}
      + [Prise en main de la collecte de données](using/offers/data-collection/data-collection.md)
      + [Créer un jeu de données pour collecter des événements](using/offers/data-collection/create-dataset.md)
      + [Configurer la capture d’événements](using/offers/data-collection/schema-requirement.md)
   + Créer des rapports de gestion des décisions {#create-reports}
      + [Utiliser les événements de gestion des décisions](using/offers/reports/get-started-events.md)
      + [Accès aux champs XDM des événements](using/offers/reports/xdm-fields.md)
   + Export de votre catalogue d’offres {#export-catalog}
      + [Commencer à exporter des catalogues d’offres ](using/offers/export-catalog/get-started-export.md)
      + [Accès au catalogue d’offres exporté](using/offers/export-catalog/access-dataset.md)
      + [Jeu de données d’offres personnalisées](using/offers/export-catalog/export-offers.md)
      + [Jeu de données de décisions](using/offers/export-catalog/export-decisions.md)
      + [Jeu de données d’emplacements](using/offers/export-catalog/export-placements.md)
      + [Jeu de données de secours](using/offers/export-catalog/export-fallback.md)
   + Référence d’API {#api-reference}
      + [Prise en main](using/offers/api-reference/getting-started.md)
      + Création et gestion des offres à l’aide d’API {#offers-api}
         + Emplacements {#placements}
            + [Liste des emplacements](using/offers/api-reference/offers-api/placements/placements-list.md)
            + [Recherche d’un emplacement](using/offers/api-reference/offers-api/placements/lookup.md)
            + [Création d’un emplacement](using/offers/api-reference/offers-api/placements/create.md)
            + [Mise à jour d’un emplacement](using/offers/api-reference/offers-api/placements/update.md)
            + [Suppression d’un emplacement](using/offers/api-reference/offers-api/placements/delete.md)
         + Règles de décision {#decision-rules}
            + [Liste des règles de décision](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
            + [Recherche d’une règle de décision](using/offers/api-reference/offers-api/decision-rules/lookup.md)
            + [Création d’une règle de décision](using/offers/api-reference/offers-api/decision-rules/create.md)
            + [Mise à jour d’une règle de décision](using/offers/api-reference/offers-api/decision-rules/update.md)
            + [Suppression d’une règle de décision](using/offers/api-reference/offers-api/decision-rules/delete.md)
         + Qualificateurs de collection {#tags}
            + [Répertorier les qualificateurs de collection](using/offers/api-reference/offers-api/tags/tags-list.md)
            + [Rechercher un qualificateur de collection](using/offers/api-reference/offers-api/tags/lookup.md)
            + [Créer un qualificateur de collection](using/offers/api-reference/offers-api/tags/create.md)
            + [Mettre à jour un qualificateur de collection](using/offers/api-reference/offers-api/tags/update.md)
            + [Supprimer un qualificateur de collection](using/offers/api-reference/offers-api/tags/delete.md)
         + Offres personnalisées {#personalized-offers}
            + [Liste des offres personnalisées](using/offers/api-reference/offers-api/personalized-offers/offers-list.md)
            + [Recherche d’une offre personnalisée](using/offers/api-reference/offers-api/personalized-offers/lookup.md)
            + [Création d’une offre personnalisée](using/offers/api-reference/offers-api/personalized-offers/create.md)
            + [Mise à jour d’une offre personnalisée](using/offers/api-reference/offers-api/personalized-offers/update.md)
            + [Suppression d’une offre personnalisée](using/offers/api-reference/offers-api/personalized-offers/delete.md)
         + Collections {#collections}
            + [Liste des collections](using/offers/api-reference/offers-api/collections/collections-list.md)
            + [Recherche d’une collection](using/offers/api-reference/offers-api/collections/lookup.md)
            + [Création d’une collection](using/offers/api-reference/offers-api/collections/create.md)
            + [Mise à jour d’une collection](using/offers/api-reference/offers-api/collections/update.md)
            + [Suppression d’une collection](using/offers/api-reference/offers-api/collections/delete.md)
         + Offres de secours {#fallback-offers}
            + [Liste des offres de secours](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
            + [Recherche d’une offre de secours](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
            + [Création d’une offre de secours](using/offers/api-reference/offers-api/fallback-offers/create.md)
            + [Mise à jour d’une offre de secours](using/offers/api-reference/offers-api/fallback-offers/update.md)
            + [Suppression d’une offre de secours](using/offers/api-reference/offers-api/fallback-offers/delete.md)
      + Création et gestion des décisions à l’aide d’API {#activities-api}
         + [Liste des décisions](using/offers/api-reference/activities-api/activities/activities-list.md)
         + [Recherche d’une décision](using/offers/api-reference/activities-api/activities/lookup.md)
         + [Création d’une décision](using/offers/api-reference/activities-api/activities/create.md)
         + [Mise à jour d’une décision](using/offers/api-reference/activities-api/activities/update.md)
         + [Suppression d’une décision](using/offers/api-reference/activities-api/activities/delete.md)
      + Diffuser des offres à l’aide d’API {#offer-delivery-api}
         + [Prise en main des API de diffusion d’offres](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
         + [API Decisioning](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
         + [API Edge Decisioning](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
         + [API Batch Decisioning](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Gestion des données {#data-management}
   + [Prise en main de la gestion des données](using/data/gs-data.md)
   + [Utilisation des schémas](using/data/get-started-schemas.md)
   + Jeux de données Journey Optimizer {#datasets}
      + [Prise en main des jeux de données](using/data/get-started-datasets.md)
      + [Exporter des jeux de données Journey Optimizer](using/data/export-datasets.md)
      + [Exemples de requêtes](using/data/datasets-query-examples.md)
      + [Schémas intégrés > ](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=fr)
   + [Requêtes](using/data/get-started-queries.md)
+ Configuration {#configuration}
   + [Prise en main de la configuration de Journey Optimizer](using/configuration/get-started-configuration.md)
   + Déléguer les sous-domaines d’e-mail {#delegate-subdomains}
      + [Prise en main de la délégation de sous-domaines](using/configuration/about-subdomain-delegation.md)
      + [Délégation d’un sous-domaine](using/configuration/delegate-subdomain.md)
      + [Ajout d’un enregistrement TXT Google](using/configuration/google-txt.md)
      + [Accès aux enregistrements PTR et modification](using/configuration/ptr-records.md)
      + [Création de groupes d’adresses IP](using/configuration/ip-pools.md)
   + [Configurer des surfaces de canal](using/configuration/channel-surfaces.md)
   + Surveiller des adresses e-mail {#monitor-reputation}
      + [Liste de suppression](using/configuration/manage-suppression-list.md)
      + [Reprises](using/configuration/retries.md)
      + [Liste autorisée](using/configuration/allow-list.md)
   + [Prise en charge de l’archivage](using/configuration/archiving-support.md)
   + [Configurer des règles de fréquence](using/configuration/frequency-rules.md)
   + [Gérer les adresses d’exécution](using/configuration/primary-email-addresses.md)
   + Configuration des parcours {#configure-journeys}
      + [À propos des sources de données, des événements et des actions](using/configuration/about-data-sources-events-actions.md)
      + Intégration aux systèmes externes {#external-systems}
         + [Intégration des parcours à des systèmes externes](using/configuration/external-systems.md)
         + [API de plafonnement](using/configuration/capping.md)
         + [API de limitation](using/configuration/throttling.md)
      + Configuration des événements {#events-journeys}
         + [Principe général](using/event/about-events.md)
         + Configuration d’un événement unitaire {#unitary-events}
            + [Prise en main des événements unitaires](using/event/about-creating.md)
            + [À propos des schémas ExperienceEvent](using/event/experience-event-schema.md)
            + [Utiliser Adobe Analytics](using/event/about-analytics.md)
         + [Configuration d’un événement métier](using/event/about-creating-business.md)
         + [Étapes supplémentaires pour l’envoi d’événements](using/event/additional-steps-to-send-events-to-journey.md)
      + Configuration des sources de données{#data-source-journeys}
         + [À propos des sources de données](using/datasource/about-data-sources.md)
         + [Configurer une source de données](using/datasource/configure-data-sources.md)
         + [Source de données Adobe Experience Platform](using/datasource/adobe-experience-platform-data-source.md)
         + [Sources de données externes](using/datasource/external-data-sources.md)
      + Configuration des actions {#action-journeys}
         + [À propos des actions](using/action/action.md)
         + [Configuration d’une action](using/action/about-custom-action-configuration.md)
         + [Intégration à Adobe Campaign Standard](using/action/acs-action.md)
         + [Intégration à Adobe Campaign v7/v8](using/action/acc-action.md)
   + [Sources](using/start/get-started-sources.md)
+ Contrôle d’accès {#access-control}
   + [Présentation du contrôle d’accès](using/administration/permissions-overview.md)
   + [Profils de produit intégrés](using/administration/ootb-product-profiles.md)
   + [Gestion des utilisateurs et des profils de produits](using/administration/permissions.md)
   + [Niveaux d’autorisation](using/administration/high-low-permissions.md)
   + [Gestion des sandbox](using/administration/sandboxes.md)
   + [Contrôle d’accès basé sur attribut](using/administration/attribute-based-access.md)
   + [Contrôle d’accès au niveau de l’objet](using/administration/object-based-access.md)
+ Confidentialité {#privacy}
   + [Prise en main de la confidentialité](using/privacy/get-started-privacy.md)
   + [Demandes d’accès à des informations personnelles](using/privacy/requests.md)
   + [Actions d’audit sur les ressources ](using/privacy/audit-logs.md)
   + [Effectuer des opérations d’hygiène des données](using/privacy/data-hygiene.md)
   + Gérer le consentement {#consent}
      + [Gérer le processus d’opt-out](using/privacy/opt-out.md)
      + [Utiliser les politiques de consentement](using/action/consent.md)
   + [Gouvernance des données](using/action/action-privacy.md)
