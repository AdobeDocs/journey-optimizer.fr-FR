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
source-git-commit: 7cfeabc85b9645be9d61ed6458e57e42ea319619
workflow-type: tm+mt
source-wordcount: '3330'
ht-degree: 84%

---

# Mises à jour de la documentation {#latest-updates}

Cette page répertorie toutes les dernières modifications apportées à la documentation [!DNL Journey Optimizer], en plus des mises à jour liées aux fonctionnalités et améliorations de la version mensuelle.

## Février 2026 {#february-2026}

* Mise à jour de la page sur l’intégration des systèmes externes avec des liens vers des sources de données et des actions personnalisées, et clarifie que le proxy de sortie fournit une adresse IP statique pour les appels sortants depuis **Actions personnalisées** vers vos systèmes externes. [En savoir plus](../configuration/external-systems.md)

* La documentation sur l’exécution d’essai par Parcours a été clarifiée : les attributs d’événement d’étape `inDryRun` et `dryRunID` désormais documenter le fait qu’ils renvoient l’identifiant d’`true`/instance lorsqu’ils sont en mode Exécution d’essai et `null` pour les parcours de test ou en direct. Les conseils pour exclure les événements d’étape d’exécution d’essai dans les requêtes de rapport ont été mis à jour en conséquence. [En savoir plus](../building-journeys/journey-dry-run.md)

* **Web push** est désormais disponible. La documentation sur les notifications push a été restructurée et mise à jour en conséquence (prise en main, conception, envoi, création). [En savoir plus](../push/get-started-push.md)

* La page de configuration des notifications push web est désormais disponible dans la documentation. [En savoir plus](../push/push-configuration-web.md)

* Mise à jour de la documentation sur l&#39;utilisation de fragments dans la prise de décision : ajout de notes dans les sections Fragments et Prise de décision et mise à jour de la page Fragments dans les politiques de décision. [En savoir plus](../experience-decisioning/fragments-decision-policies.md)

* Mise à jour de la documentation du webhook SMS : suppression du contenu du webhook Twilio. [En savoir plus](../sms/sms-webhook.md)

* Mise à jour de la documentation sur l’API de migration Decisioning. [En savoir plus](../experience-decisioning/decisioning-migration-api.md)

* L’activité **Décision de contenu** est désormais disponible au public. La page d&#39;activité de décision de contenu a été mise à jour avec une section sur les données de prise de décision disponibles dans les événements d&#39;étape. [En savoir plus](../building-journeys/content-decision.md)

* Des liens vers la documentation de l’API de défi de fidélité ont été ajoutés à la section Défis de fidélité (prise en main, création de défis, création de tâches, accès aux défis de fidélité). [En savoir plus](../loyalty-challenges/get-started.md)

* Les informations sur les canaux pris en charge dans la documentation de l’assistant de création de campagne ont été corrigées. Les pages FAQ sur la Prise en main des canaux et des campagnes orchestrées ont été mises à jour en conséquence. [En savoir plus](../campaigns/get-started-with-campaigns.md)

* Correction de la documentation sur les autorisations concernant les autorisations de **Parcours Manager** et **Approve**. [En savoir plus](../administration/ootb-permissions.md)

* Mise à jour de la documentation sur les intégrations d&#39;AEM (Adobe Experience Manager) avec des noms révisés (contenu dynamique AEM et fragments AEM). [En savoir plus](../integrations/aem-fragments.md)

* Une nouvelle raison d’exclusion a été ajoutée à la liste d’exclusions : **UnsubscribeLinkNotValid** (code d’erreur 050081). Cette exclusion est générée lorsque la longueur de l&#39;objet List-Unsubscribe mailTo est supérieure à la limite RFC de 998 caractères. [En savoir plus](../reports/exclusion-list.md)

* La documentation de la fonction d&#39;assistance formatDate a été améliorée. Notez que la fonction nécessite un type de champ date-heure (et non une chaîne) et plusieurs exemples : formatage d&#39;un champ date-heure, conversion d&#39;une chaîne en date en premier, date complète avec nom du jour, date dynamique à partir de l&#39;heure système et format de jour de la semaine avec sortie en minuscules. [En savoir plus](../personalization/functions/dates.md#format-date)

* La documentation sur les e-mails de version texte a été améliorée avec des conseils d’utilisation complets, y compris des critères de décision pour l’utilisation de texte brut personnalisé par rapport à la synchronisation automatique, des exemples pratiques avec des scénarios réels et une section FAQ avec des questions courantes. [En savoir plus](../email/text-version-email.md#when-to-use)

* Une limitation a été ajoutée à la documentation de l’assistant Métadonnées d’exécution pour clarifier que les métadonnées ne sont pas capturées pour les profils exclus de l’action. [En savoir plus](../personalization/functions/helpers.md#execution-metadata)

* Mise à jour de la documentation sur les exemples d&#39;implémentation basés sur le code afin d&#39;inclure le champ de jetons dans la propositionAction pour un suivi et une attribution précis dans la prise de décision. [En savoir plus](../code-based/code-based-implementation-samples.md#client-side-how)

* Une note a été ajoutée à la documentation sur le tracking des URL et le désabonnement des listes pour clarifier que l’ordre des paramètres de tracking d’URL ajoutés aux URL est aléatoire et ne peut pas être contrôlé. [En savoir plus](../email/url-tracking.md)

* Mise à jour de la documentation sur les thèmes du Designer des e-mails avec des informations sur les polices web, les limitations de prise en charge et l’importance des polices de secours. [En savoir plus](../email/apply-email-themes.md#themes-guardrails)

## Janvier 2026 {#january-2026}

* Clarification de la documentation du tableau de bord d’utilisation des licences avec des conseils mis à jour sur les **profils engageables**, y compris des détails sur la définition et des conseils de dépannage. [En savoir plus](../audience/license-usage.md#what-is-engageable-profile)

* Une note a été ajoutée à la documentation sur les thèmes Designer d’e-mail pour clarifier les limites de prise en charge des polices web. [En savoir plus](../email/apply-email-themes.md#themes-guardrails)

* Une nouvelle section de mécanisme de sécurisation a été ajoutée pour documenter la validation de la taille de la payload du parcours, y compris les seuils d’avertissement et d’erreur, ainsi que des conseils sur la manière d’optimiser les parcours. [En savoir plus](../start/guardrails.md#journey-payload-size)

* La documentation sur les mécanismes de sécurisation de prise de décision a été mise à jour afin d’inclure des limitations de taille des éléments de décision (1 Ko pour les éléments comprenant des attributs avec un maximum de 30 attributs). [En savoir plus](../experience-decisioning/decisioning-guardrails.md)

* Une note a été ajoutée à la documentation sur la création de la politique de décision pour informer les utilisateurs et utilisatrices qu’une fois une politique de décision créée, toute modification peut prendre jusqu’à 15 minutes pour se propager dans toutes les régions de données, et jusqu’à 30 minutes pour le Canada. [En savoir plus](../experience-decisioning/create-decision-policy.md#review)

* Une note a été ajoutée à la documentation sur les fragments pour vous avertir que lorsque le libellé du bouton et l’URL sont rendus modifiables dans un fragment, le jeu de données de suivi consigne la valeur de l’URL au lieu de la valeur du libellé. [En savoir plus](../content-management/customizable-fragments.md#visual)

* Une nouvelle page décrivant les avantages de la migration de la gestion des décisions vers la prise de décision et comprenant des informations sur les API d’outils de migration à venir est désormais disponible. [En savoir plus](../experience-decisioning/migrate-to-decisioning.md)

* Ajout d’un mécanisme de sécurisation pour clarifier que les jeux de données de recherche sont disponibles pour l’activation entrante basée sur Edge uniquement dans la région où réside le sandbox du jeu de données. [En savoir plus](../data/lookup-aep-data.md#guidelines)

* Une nouvelle section a été ajoutée à la documentation relative à la configuration du canal des campagnes orchestrées. Elle explique comment utiliser les attributs contextuels (tels que l’identifiant de la campagne, le nom et les détails de l’action) dans les paramètres de tracking d’URL à des fins d’analyse et de création de rapports. [En savoir plus](../orchestrated/channel-config.md#url-tracking)

* La documentation sur l’optimisation du contenu a été restructurée pour plus de clarté. La page principale d’optimisation a été divisée en quatre sous-pages ciblées : une page de prise en main, une page dédiée au ciblage, une autre à l’expérimentation et une dernière combinant les deux approches. [En savoir plus](../content-management/gs-message-optimization.md)

* Les notes relatives à la disponibilité limitée ont été supprimées de trois alertes de parcours (parcours publié, parcours terminé et limitation d’action personnalisée déclenchée), car ces fonctionnalités sont désormais disponibles pour l’ensemble des utilisateurs et des utilisatrices. [En savoir plus](../reports/alerts.md)

* La page de destination Tester, valider et approuver a été enrichie de nouvelles sections, notamment une vue d’ensemble des fonctionnalités de test, des questions fréquentes, une arborescence de décision avec des liens de navigation et une terminologie améliorée avec des liens vers la documentation. [En savoir plus](../../rp_landing_pages/test-landing-page.md)

* Une nouvelle section a été ajoutée à la documentation sur la syntaxe de personnalisation pour clarifier comment utiliser les mots-clés réservés dans les expressions de personnalisation. Certains mots-clés PQL tels que `next`, `last` et `this` doivent être échappés avec des accents graves lorsque vous les utilisez comme noms de champ dans votre schéma XDM. [En savoir plus](../personalization/personalization-syntax.md#reserved-keywords)

* Les pages [Commencer avec les campagnes](../campaigns/get-started-with-campaigns.md) et [Gérer les campagnes](../campaigns/manage-campaigns.md) ont été restructurées avec une architecture des informations améliorée, comprenant un workflow complet avec des guides spécifiques aux types, des comparaisons de types de campagne améliorées et un tableau de statut consolidé.

* La page de destination Parcours a été repensée afin de faciliter l’intégration avec un nouveau workflow en 6 étapes, des comparaisons de types de parcours améliorées et une navigation améliorée dans toute la documentation. [En savoir plus](../building-journeys/journey.md)

* Une section détaillée a été ajoutée pour aider les utilisateurs et utilisatrices à générer des clés privées OpenSSH codées en Base64 pour l’authentification SFTP lors de la configuration du routage des fichiers pour le courrier afin d’éviter les erreurs de connexion. [En savoir plus](../direct-mail/direct-mail-configuration.md#ssh-key-generation)

* Une note a été ajoutée à la documentation sur la délégation de sous-domaine pour informer les utilisateurs et utilisatrices qu’un délai de 24 à 48 heures est nécessaire pour la propagation DNS avant de tenter une délégation à Adobe. [En savoir plus](../configuration/delegate-subdomain.md#set-up-subdomain)

## Décembre 2025 {#december-2025}

* La documentation sur le chargement d’audiences personnalisé pour la prise de décision a été mise à jour afin d’inclure un indicateur d’API requis pour récupérer les données d’enrichissement. Lors de l’utilisation d’audiences chargées au format CSV dans la prise de décisions sur les offres, vous devez inclure `"xdm:enrichedAudience": true` dans la payload de votre requête API pour récupérer les attributs d’enrichissement dans la réponse de décision d’offres. [En savoir plus](../offers/custom-upload-decisioning.md#must-read)

* Une note a été ajoutée dans la documentation sur l’envoi de BAT pour clarifier le fait que les règles de capping de la fréquence s’appliquent aux BAT. La page comprend désormais une section « À lire absolument » avec des considérations importantes sur le comportement de capping de la fréquence, les limitations de page miroir et les règles d’accessibilité des ressources. [En savoir plus](../content-management/proofs.md)

* Un nouveau tableau sur la disponibilité des canaux de communication a été ajouté à la page Commencer avec les canaux, qui indique les canaux pris en charge dans les parcours et les campagnes (campagnes d’action, campagnes déclenchées par API et campagnes orchestrées). [En savoir plus](../channels/gs-channels.md#channels)

* Une nouvelle page de destination de suivi complète a été créée pour permettre aux utilisateurs et utilisatrices de découvrir et d’accéder à toutes les fonctionnalités de suivi et de surveillance disponibles dans Journey Optimizer. [En savoir plus](../start/get-started-tracking.md)

* La page de gestion du processus de désabonnement aux e-mails a été améliorée avec des informations détaillées sur le processus de désabonnement, expliquant l’ordre attendu des événements pour le processus de désabonnement sur la page de destination. [En savoir plus](../email/email-opt-out.md#send-message-unsubscribe-link)

* Mise à jour de la documentation sur la liste d’abonnements afin d’inclure des informations sur les critères d’éligibilité des segments de streaming. [En savoir plus](../landing-pages/subscription-list.md#define-subscription-list)

* Un nouveau guide sur la délivrabilité du préchauffage des adresses IP est disponible, qui fournit des conseils complets sur les principes de base de la réputation, la préparation avant lancement, les mesures de surveillance et les bonnes pratiques pour passer d’une réputation inexistante à une arrivée réussie dans la boîte de réception. [En savoir plus](../configuration/ip-warmup-deliverability-guide.md)

* Un avertissement a été ajouté dans les sections Page de destination et Désabonnement aux e-mails pour clarifier le fait que cliquer sur un lien de désabonnement ouvre uniquement la page de destination, tandis que les utilisateurs et les utilisatrices doivent envoyer le formulaire pour terminer le processus de désabonnement. [En savoir plus](../landing-pages/lp-use-cases.md#configure-opt-out)

* Une nouvelle bibliothèque de cas d’utilisation de parcours est désormais disponible. Elle rassemble une collection de cas d’utilisation pratiques, y compris des modèles tactiques (logique de suppression, techniques de personnalisation, stratégies de sortie de parcours) et des scénarios complets couvrant les workflows marketing et techniques. [En savoir plus](../building-journeys/jo-use-cases.md)

* Un nouveau cas pratique est désormais disponible : il montre comment configurer un parcours pour envoyer des e-mails uniquement les jours de la semaine (du lundi au vendredi), avec la mise en file d’attente automatique des entrées du week-end pour qu’elles soient envoyées le lundi à une heure spécifiée. [En savoir plus](../building-journeys/weekday-email-uc.md)

* Une nouvelle page est désormais disponible pour expliquer les fonctionnalités de décision de Journey Optimizer, y compris les différences entre le framework de prise de décision de nouvelle génération et la solution de gestion des décisions existante, ainsi que leurs principaux avantages pour la diffusion d’offres personnalisées sur les différents canaux. [En savoir plus](../experience-decisioning/gs-decision.md)

* Une nouvelle section a été ajoutée à la documentation sur l’activation des audiences. Elle explique comment activer les types d’audience non pris en charge (tels que les audiences Customer Journey Analytics) dans [!DNL Journey Optimizer] en les enveloppant dans une nouvelle définition de segment dans le portail d’audience. [En savoir plus](../audience/target-audiences.md#activation-non-supported)

* Une nouvelle section a été ajoutée à la documentation sur l’activité d’attente pour expliquer comment les profils stationnés dans une activité d’attente dans les parcours de lecture d’audience actualisent automatiquement leurs attributs à partir du service de profil unifié (UPS). Cela permet de clarifier le fait que les données de profil peuvent changer au cours de l’exécution du parcours après un nœud d’attente, ce qui peut produire des résultats inattendus si vous vous attendez à des données d’instantanés constantes sur l’ensemble du parcours. [En savoir plus](../building-journeys/wait-activity.md#profile-refresh)

* Une note d’avertissement a été ajoutée dans la section Expérimentation de chemin pour avertir les utilisateurs et les utilisatrices de ne pas modifier les métadonnées d’une expérience de chemin une fois qu’elles ont été publiées, car cela perturberait le calcul et les rapports des résultats de l’expérience. [En savoir plus](../building-journeys/optimize.md#experimentation)

* Une note a été ajoutée à la section Créer un préréglage de formulaire pour spécifier les exigences relatives aux connexions en streaming à afficher dans la liste déroulante de sélection. [En savoir plus](../landing-pages/lp-forms.md#create-form-preset)

* Une nouvelle page est désormais disponible dans la section Prise de décision et concerne la configuration de la collecte de données pour le suivi des impressions, des clics et des événements personnalisés. [En savoir plus](../experience-decisioning/data-collection/schema-requirement.md)

* La documentation sur la génération de contenu avec l’assistant IA a été réorganisée pour en améliorer la clarté et la convivialité. Les cinq anciennes pages spécifiques aux canaux (e-mail, notification push, SMS, web et page de destination) ont été consolidées en trois pages de type génération : [Générer du contenu complet](../content-management/generative-full-content.md), [Générer du texte](../content-management/generative-text.md) et [Générer des images](../content-management/generative-image.md).

## Novembre 2025 {#november-2025}

* Une nouvelle page pour les Questions fréquentes relatives à la prise de décision est désormais disponible et traite de sujets tels que les règles de limitation, la configuration de modèles d’IA, les exigences en matière de trafic et les stratégies d’optimisation des offres. [En savoir plus](../experience-decisioning/decisioning-faq.md)

* Mise à jour de la page Commencer la conception d’e-mails afin de clarifier l’accès au Concepteur d’e-mail. [En savoir plus](../email/get-started-email-design.md)

* Ajout d’une section de dépannage à la page d’enregistrement DMARC pour résoudre les problèmes de latence de propagation DNS. [En savoir plus](../configuration/dmarc-record.md#troubleshooting)

* Amélioration de la page Utilisation de GenStudio for Performance Marketing en y ajoutant de nouvelles sections, notamment les fonctionnalités clés, les cas d’utilisation le plus courants, les conditions préalables et les questions fréquentes. [En savoir plus](../integrations/genstudio.md)

* Ajout à la page Mécanismes de sécurisation et limitations d’un mécanisme de sécurisation pour le ciblage des profils pseudonymes avec canaux entrants : le ciblage des visiteurs et visiteuses non authentifiés augmente le nombre total de profils engageables. Par conséquent, Adobe recommande de définir une durée de vie (TTL) pour la suppression automatique des profils afin de maîtriser les coûts associés. [En savoir plus](../start/guardrails.md#profile-management-inbound)

* Deux tutoriels sur la configuration du SDK Web pour les expériences de prise de décision et basées sur du code sont désormais référencés sur la page Exemples de méthodes d’implémentation basées sur du code . [En savoir plus](../code-based/code-based-decisioning-implementations.md#tutorials)

* Ajout d’une note pour indiquer que les ressources et les images restent accessibles pendant 2 ans (730 jours) à compter de la première publication et doivent être republiées après expiration. [En savoir plus](../content-management/proofs.md)

* Un guide complet sur la création de prompts de contenu avec l’assistant IA est à présent disponible. Ce guide vous explique comment créer des prompts efficaces, ainsi que des contenus marketing générant de fortes conversions et alignés sur la marque. Découvrez les bonnes pratiques relatives à la rédaction d’objectifs marketing, à l’utilisation de ressources de marque et à l’optimisation du contenu pour différents canaux. [En savoir plus](../content-management/ai-assistant-prompting-guide.md)

* Une note a été ajoutée à la documentation sur la définition de segment pour clarifier le fait que l’attribut `frequencyMap` ne soit pas pris en charge dans les définitions de segment et ne puisse pas être utilisé dans le cadre des critères de segmentation d’audience. Pour le ciblage basé sur la fréquence, pensez à utiliser des règles de capping de la fréquence sous les règles métier. [En savoir plus](../audience/creating-a-segment-definition.md)
* Un nouvel exemple montrant comment utiliser les réponses d’action personnalisée dans les canaux natifs a été ajouté à la documentation sur les réponses d’appel API. L’exemple montre comment effectuer une itération sur des tableaux imbriqués à partir de réponses d’action personnalisée à l’aide de la syntaxe Handlebars dans les e-mails, les notifications push et les SMS. [En savoir plus](../action/action-response.md#response-in-channels)

* Une nouvelle section a été ajoutée à la documentation sur l’intégration de Campaign v7/v8 pour expliquer comment mettre à jour les actions personnalisées existantes lorsque le point d’entrée en temps réel (RT) change. Cette section comprend des instructions détaillées pour mettre à jour l’URL du point d’entrée, tester la connexion et valider les modifications avant d’enregistrer. [En savoir plus](../action/acc-action.md#update-action)

* De nouvelles sections sur les limites et les bonnes pratiques ont été ajoutées à la documentation sur les fragments visuels pour indiquer toute imbrication non prise en charge de fragments contenant du contenu dynamique dans d’autres fragments déverrouillés avec du contenu dynamique. Ces conseils comprennent des étapes de dépannage pour les problèmes de mode de compatibilité et des recommandations pour une bonne conception de la structure des e-mails. [En savoir plus](../email/use-visual-fragments.md#fragment-dynamic-content)

* Une section de dépannage a été ajoutée à la documentation des rapports dynamiques de parcours pour permettre de résoudre les problèmes liés aux données de rapports manquantes. La section couvre la synchronisation des noms de parcours avec les jeux de données de rapports, le timing de l’actualisation des données, la vérification des autorisations d’accès et les exigences de statut de parcours. [En savoir plus](../building-journeys/report-journey.md#troubleshooting-missing-data)

* Trois nouveaux éléments de FAQ ont été ajoutés à la documentation des ressources pour expliquer l’expiration des ressources et la gestion du cycle de vie. Les sujets abordés incluent la politique de durée de vie (TTL) des ressources AEM (730 jours), la manière de résoudre les images endommagées en raison de l’expiration des ressources et des informations sur les améliorations à venir de la logique d’expiration des ressources. [En savoir plus](../integrations/assets.md#faq-assets)

* Une section de dépannage complète a été ajoutée à la documentation de l’activité Lecture d’audience pour résoudre les incohérences de tailles d’audiences entre les profils estimés et réels qui rejoignent les parcours. La section couvre les problèmes de synchronisation et de propagation des données, les techniques de validation et de surveillance des données, ainsi que les bonnes pratiques, y compris l’utilisation de l’option « Déclencher après l’évaluation de l’audience par lots ». [En savoir plus](../building-journeys/read-audience.md#audience-count-mismatch)

* Une note a été ajoutée à la documentation sur les événements de qualification d’audience pour clarifier la latence de la segmentation en streaming (jusqu’à 2 heures) et recommander l’ajout d’une activité Attente ou d’une durée de buffer pour les parcours sensibles au facteur temps. [En savoir plus](../building-journeys/audience-qualification-events.md#streamed-speed-segment-qualification)

* Une nouvelle section a été ajoutée aux mécanismes de sécurisation des e-mails. Elle documente la limite de taille du contenu des messages de 2 Mo pour la publication de parcours, y compris les bonnes pratiques pour conserver le contenu créé sous 1 Mo afin de tenir compte de la surcharge de traitement back-end. [En savoir plus](../start/guardrails.md#message-content-size)

* Amélioration de la documentation de l’option Lecture incrémentielle dans les activités Lecture d’audience afin de clarifier les dépendances temporelles des instantanés et la limitation de la fenêtre de recherche de 24 heures, y compris des recommandations pour éviter les profils manquants. [En savoir plus](../building-journeys/read-audience.md)

* Une note a été ajoutée aux mécanismes de sécurisation de la recherche de jeu de données pour indiquer que les recherches ne peuvent pas être liées. [En savoir plus](../data/lookup-aep-data.md#guidelines)

* Les canaux WhatsApp et LINE sont désormais disponibles pour les campagnes d’action. [En savoir plus](../campaigns/campaign-content.md)

* Une nouvelle section complète sur le taux de traitement des parcours a été ajoutée à la documentation de la gestion des entrées. Elle couvre les taux d’entrée des profils, les événements et les qualifications d’audience dans les parcours, l’impact des activités d’attente et l’impact des activités d’action. [En savoir plus](../building-journeys/entry-management.md#journey-processing-rate)

* Lors de la conception des e-mails, le système vérifie désormais les paramètres clés et affiche des alertes pour les avertissements et les erreurs. Des informations sur les alertes d’e-mail et les exigences de validation ont été ajoutées à la page Mécanismes de sécurisation. [En savoir plus](../email/create-email.md#check-email-alerts)

* La note d’avertissement indiquant que le capping de la fréquence ne peut pas être activée ou désactivée pour les offres créées précédemment a été supprimée de la page Ajouter des contraintes à une offre. [En savoir plus](../offers/offer-library/add-constraints.md#capping)

* La documentation sur l’utilisation des événements d’étape de parcours est désormais disponible. [En savoir plus](../reports/journey-step-events-overview.md)

* Un nouveau guide complet sur les critères d’entrée et de sortie de parcours est disponible et présente des bonnes pratiques, des exemples concrets et des conseils pratiques pour gérer les entrées et les sorties des profils dans des parcours dans Adobe Journey Optimizer. [En savoir plus](../building-journeys/entry-exit-criteria-guide.md)

* Une nouvelle page expliquant comment effectuer une itération sur les données contextuelles dans les messages est désormais disponible. Ce guide explique comment utiliser la syntaxe Handlebars pour afficher des listes dynamiques à partir d’événements, de réponses d’action personnalisée, de recherches dans des jeux de données et d’autres sources de contexte dans votre personnalisation. [En savoir plus](../personalization/iterate-contextual-data.md)

* La requête d’identification des événements ignorés dans les parcours a été corrigée afin d’inclure des filtres appropriés pour les erreurs de traitement d’export de segments, les abandons du Dispatcher et les abandons de machine d’état. [En savoir plus](../reports/query-examples.md#common-queries)

* Des phrases d’introduction ont été ajoutées aux 37 exemples de requête dans la documentation des exemples de requête afin de fournir un meilleur contexte et d’expliquer ce que chaque requête effectue avant de présenter le code SQL. Cela permet de mieux comprendre quand utiliser chaque requête et de fournir des conseils plus clairs. [En savoir plus](../reports/query-examples.md)

## Octobre 2025 {#october-2025}

* Vous pouvez désormais convertir des images en modèles HTML à l’aide du convertisseur d’images en HTML. [En savoir plus](../content-management/image-to-html.md)

* Des informations sur le cycle de publication d’Adobe Journey Optimizer sont désormais disponibles. [En savoir plus](releases.md)

* Une nouvelle page Questions fréquentes sur les parcours est désormais disponible. [En savoir plus](../building-journeys/journey-faq.md)

* La fonctionnalité Surveiller vos actions personnalisées est désormais disponible. [En savoir plus](../action/reporting.md)

* Le mode à débit élevé pour les campagnes déclenchées par API est désormais disponible. [En savoir plus](../campaigns/api-triggered-high-throughput.md)

* Une référence des codes d’erreur pour les parcours est désormais disponible. [En savoir plus](../building-journeys/error-codes-reference.md)

* La documentation de Journey Optimizer Experimentation Accelerator est désormais disponible. [En savoir plus](../content-management/experiment-accelerator-gs.md)

* Une nouvelle section a été ajoutée à la documentation de la fonction d’assistance **formatDate**. Cette section clarifie la signification des symboles clés tels que y, Y, M, d et D. [En savoir plus](../personalization/functions/dates.md#pattern-characters)

* Un exemple de PQL a été ajouté à la section sur la formule de classement de la prise de décision, illustrant la façon d’optimiser les offres en fonction du code postal et des revenus annuels du profil. [En savoir plus](../experience-decisioning/ranking/ranking-formulas.md#ranking-formula-examples)

* Une limitation a été ajoutée à la section Mode de test de parcours pour indiquer que le mode de test ne prend pas en charge l’enrichissement d’attributs d’audience de chargement personnalisé. [En savoir plus](../building-journeys/testing-the-journey.md#important_notes)

* Une nouvelle section a été ajoutée aux pages [Mécanismes de sécurisation et limitations de la gestion des décisions](../offers/decision-management-guardrails.md#configurations) et [Mécanismes de sécurisation et limitations de la prise de décisions](../experience-decisioning/decisioning-guardrails.md#configurations) pour spécifier le nombre maximal de configurations prises en charge (20 000), correspondant au nombre total de règles de limitation existant dans votre sandbox.

* Ajout d’une note à la section d’activité Condition du parcours pour documenter l’échec de l’évaluation de la condition pour les profils contenant plus de deux identités multi-appareils. [En savoir plus](../building-journeys/condition-activity.md)

* Une nouvelle page a été ajoutée pour décrire comment vous pouvez utiliser les politiques de consentement afin d’honorer les préférences de vos clientes et clients en fonction de leurs choix, tout en respectant leur consentement. [En savoir plus](../action/preference-center.md)

* Une note a été ajoutée aux pages Commencer avec les profils et Mécanismes de sécurisation pour indiquer que lors de l’ingestion de données, les e-mails sont sensibles à la casse, ce qui signifie que des profils en double peuvent être créés et utilisés lors du ciblage de la personne destinataire correspondante. [En savoir plus](../audience/get-started-profiles.md)

* Un nouvel attribut `render` a été introduit dans l’éditeur de personnalisation. Définissez-le sur `false` si vous souhaitez masquer le contenu d’un fragment d’expression. [En savoir plus](../personalization/use-expression-fragments.md#use-expression-fragment)

* Ajout à la section d’une liste de mécanismes de sécurisation, décrivant comment exploiter les fragments liés aux éléments de décision dans les politiques de décision. [En savoir plus](../experience-decisioning/use-decision-policy.md#fragments)

* Ajout de bonnes pratiques pour les recherches de jeux de données : maintenir les boutons (bascule) activés pour éviter les problèmes d’indexation et comprendre l’impact des suppressions par lots sur les données de recherche. [En savoir plus](../data/lookup-aep-data.md#guidelines)

* Ajout d’une limitation notant que seules les audiences du service de profil unifié sont prises en charge lors de l’utilisation de parcours Lecture d’audience avec des identifiants supplémentaires. [En savoir plus](../building-journeys/supplemental-identifier.md#guardrails)

* La documentation d’Experimentation Accelerator a été déplacée vers une collection distincte. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experimentation-accelerator/using/overview)

## Septembre 2025 {#september-2025}

* Une nouvelle section Canal entrant a été ajoutée à la page Mécanismes de sécurisation et limitations pour rassembler toutes les limitations s’appliquant aux expériences web, in-app, basées sur le code et aux canaux de cartes de contenu. Elle comprend la limite du volume maximal de 5 000 demandes entrantes par seconde pour toutes les requêtes entrantes, et le maximum de 500 actions entrantes actives. [En savoir plus](../start/guardrails.md#inbound-guardrails)

* Une page de questions fréquentes a été publiée pour les campagnes orchestrées. [En savoir plus](../orchestrated/orchestrated-campaigns-faq.md)

* Une section de dépannage a été ajoutée à la documentation sur les événements d’étape de parcours avec des définitions, des causes courantes et des étapes de dépannage pour les types d’événements de rejet les plus fréquents. [En savoir plus](../reports/sharing-field-list.md#discarded-events)

* La documentation relative à l’utilisation d’identifiants supplémentaires dans les parcours comprend désormais un tableau qui détaille le comportement des profils lorsque des critères de sortie sont appliqués dans les parcours à l’aide d’ID supplémentaires. [En savoir plus](../building-journeys/supplemental-identifier.md#exit-criteria)

* Une section de dépannage a été ajoutée pour comprendre les rejets de profil dans les parcours mis en pause. [En savoir plus](../building-journeys/journey-pause.md#discards-troubleshoot)

* Des informations ont été ajoutées dans la documentation de présentation des schémas pour différencier les schémas standard et relationnels utilisés pour les campagnes orchestrées. [En savoir plus](../data/gs-data.md)

* Des informations ont été ajoutées à la documentation sur la prise de décision et la gestion des décisions. Elles traitent des exigences requises pour entraîner les modèles d’[optimisation automatique](../experience-decisioning/ranking/auto-optimization-model.md) et d’[optimisation personnalisée](../experience-decisioning/ranking/personalized-optimization-model.md).

* Il est précisé que les appels de l’API REST Interactive Message Execution ont un délai d’expiration de 60 secondes, avec des reprises internes pour assurer la diffusion. [En savoir plus](../campaigns/trigger-campaigns.md)

* La page Collections d&#39;éléments de prise de décision a été mise à jour afin de clarifier le comportement de l’opérateur **CONTAINS** lors de la définition de règles. [En savoir plus](../experience-decisioning/collections.md)

* La page Attribuer des scores de priorité a été mise à jour avec les étapes spécifiques afin de définir un score de priorité pour les actions de canal entrant dans l’activité **Action**. [En savoir plus](../conflict-prioritization/priority-scores.md#priority-action)

<!--
## August 2025 {#august-2025}

* A new page listing the best practices for designing accessible email and landing page content with [!DNL Journey Optimizer] was added. [Read more](../email/accessible-content.md)

* The documentation for supplemental identifiers in journeys has been updated with the following clarifications:

    * After adding a supplemental identifier to a schema, a new event (for event-triggered journeys) or a new field group (for Read audience journeys) must be created. Existing entities do not refresh automatically and will not recognize the new identifier.

    * Supplemental identifiers are not validated against Data Usage Labeling & Enforcement (DULE) policies and are not considered during data governance checks in journeys.

        [Read more](../building-journeys/supplemental-identifier.md)

* The Optimization in campaigns page was updated to reflect the fact that optimization is now also available in journeys. [Read more](../content-management/gs-message-optimization.md)

* A link to the tutorial video describing how to leverage message optimization in a campaign was added. [Read more](../content-management/gs-message-optimization.md)

## July 2025 {#july-2025}

* The campaigns interface now features two separate tabs: **Action** and **API Triggered**. The documentation has been updated accordingly, with information for each campaign type organized into dedicated sections to improve clarity and usability. [Read more](../campaigns/get-started-with-campaigns.md)

* The [Get started with subdomain delegation](../configuration/about-subdomain-delegation.md) and [Delegate a subdomain](../configuration/delegate-subdomain.md) pages have been updated to better present the different delegation methods and the steps to set them up.

* A note has been added to the Fragments section, specifying that when tracking is enabled in a journey or a campaign, if links are present in a fragment and if this fragment is used in a message, these links are tracked such as all other links included in the message. [Learn more](../content-management/create-fragments.md#content)

* The guardrails and limitations applying to subdomain delegation in Journey Optimizer have been enriched and consolidated into one dedicated section. [Read more](../configuration/delegate-subdomain.md#guardrails)

* A note has been added to the Create fallback offers and Create decision pages to mention that fallback offers should contain all representations used within a decision. [Read more](../offers/offer-library/creating-fallback-offers.md)

* The guardrails applying to fragments have been enriched. [Read more](../start/guardrails.md#fragments-guardrails).

* A note has been added to specify that links added to messages expire after 25 months and links to mirror pages after 90 days. [Read more](../email/message-tracking.md)

<!--* The possible email error types that could happen upon sending email deliveries with are now listed in a dedicated section. [Read more](../configuration/email-error-types.md)-->

<!--
## June 2025 {#june-2025}

* Added a new section on how to add and use rich text such as line breaks, bold, italics etc., to customizable fragments by using HTML components. [Read more](../content-management/customizable-fragments.md#rich-text)

* The Decisioning part has been updated with a specific section dedicated to building AI models. [Read more](../experience-decisioning/ranking/ai-models.md)

* Added a recommendation about the usage of the `actionExecutionTime` field in the journeyStep events action. [Read more](../reports/sharing-execution-fields.md#actionexecutiontime-field)

* Added a note about the `messageID` which may not be unique for each individual delivery. [Read more](../data/datasets-query-examples.md)

* Added a recommendation about historical events management in data hygiene operations. [Read more](../privacy/data-hygiene.md#data-hygiene-recommendations)

* Added a guardrail about landing pages not being supported for migration between sandboxes. [Read more](../configuration/copy-objects-to-sandbox.md#global)

* Added a caution note about nested JSON objects not supported in custom authentication for custom actions. [Read more](../datasource/external-data-sources.md)

* Added a caution note about conditional content variant naming in the Email designer. [Read more](../personalization/create-conditions.md)

* Updated the "Undelegate a landing page subdomain" section. [Read more](../landing-pages/lp-subdomains.md#undelegate-subdomain)

* Clarified journey reentrance rules when using supplemental identifiers. [Read more](../building-journeys/supplemental-identifier.md#guardrails)

* Added a new note to clarify that you must use the expression editor in Advanced mode when selecting the supplemental identifier attribute during event configuration. [Learn more](../building-journeys/supplemental-identifier.md#add)

* Added clarification on how journey reentrance works with supplemental identifiers. [Learn more](../building-journeys/supplemental-identifier.md#guardrails)

## May 2025 {#may-2025}

* Adobe integrations available with Journey Optimizer are now listed in the "Connect your systems and environments" section. [Read more](../integrations/ajo-integrations.md)

* The content integrations are now grouped in the Content Management section. [Read more](../integrations/content-integrations.md)

* Architecture diagrams for Adobe Experience Platform and Journey Optimizer have been updated. [Read more](../start/get-started.md#architecture)

* Added a video about the personalization editor playground to help you learn how to write and test personalization code using sample data. [Read more](../personalization/personalize.md#video-perso)

* The maximum number of addresses in a seed list has been increased from 50 to 300. [Read more](../configuration/seed-lists.md#create-seed-list)

* A new step detailing how to wrap code when using decision policies in the code-based experience editor has been added to the Create decision policies page. [Read more](../experience-decisioning/create-decision.md#create-decision)

* A note has been added to the Code-based experiences documentation to specify that when you have multiple code-based experience actions running on the same surface, the campaign or journey's priority score determines what is delivered to the end-user if they qualify for more than one action. [Read more](../code-based/code-based-surface.md#surface-definition)

* A new page on troubleshooting inbound actions in journeys provides a step-by-step guide to identify and resolve issues independently before reaching out to support. [Read more](../building-journeys/troubleshooting-inbound.md)

* A new [page](../code-based/code-based-decisioning-implementations.md) has been added to describe how to add the following flags to your client implementation when using decisioning in code-based experiences:

    * Adding the `dryRun` flag to test decisioning in code-based experiences. [Read more](../code-based/code-based-decisioning-implementations.md#code-based-test-decisions)

    * Apply deduplication to decisioning requests in code-based experiences. [Read more](../code-based/code-based-decisioning-implementations.md#code-based-decisioning-deduplication)

## April 2025 {#apr-2025}

* The Configuration chapter is now split into three chapters: [Channel configuration](../configuration/get-started-configuration.md), [Journey configuration](../configuration/about-data-sources-events-actions.md), and [Connect your systems](../configuration/ajo-apis.md).
* Added a caution note about using experience events in journey expressions and conditions. [Read more](../building-journeys/expression/expressionadvanced.md#discovering-the-interface)
* Added a note on the Direct mail configuration page about temporary storage of the output file. [Read more](../direct-mail/direct-mail-configuration.md)
* Added a tip in the journey advanced expression editor section about the condition format guidelines. [Read more](../building-journeys/expression/expressionadvanced.md)
* Added a caution note in the `inAudience` function section about impacts and best practices when renaming an audience. [Read more](../building-journeys/functions/functioninaudience.md)
* Added a recommendation about the native keywords usage when using two-way SMS. [Read more](../sms/sms-opt-out.md)
* Updated the journey test page with a note about the need for including an identity namespace in the event used. [Read more](../building-journeys/testing-the-journey.md)
* Currently, you cannot undelegate subdomains through the [!UICONTROL Journey Optimizer] user interface - you must reach out to your Adobe representative. Steps to undelegate a subdomain are now detailed for [Emails](../configuration/delegate-subdomain.md#undelegate-subdomain), [SMS](../sms/sms-subdomains.md#undelegate-subdomain), [Web experiences](../web/web-delegated-subdomains.md#undelegate-subdomain), and [Landing pages](../landing-pages/lp-subdomains.md#undelegate-subdomain).<!--[Read more](../configuration/delegate-subdomain.md#undelegate-subdomain)-->
<!--
* Added clarification about the optional `maxHttpConnections` parameter in the journeys Capping API, including guidance on how to use it alongside throttling configurations for the same endpoint. [Read more](../configuration/throttling.md)
* In the Decisioning section, added guidance explaining that approved offer items cannot be deleted if they are used in a collection or a decision. Included steps to change their status to "Draft" using the **[!UICONTROL Undo approve]** option. [Read more](../experience-decisioning/items.md#manage)
* Information on sandboxes have been grouped together into a new "Sandboxes management" section. This new section provides information on how to use and assign sandboxes, and how to use package export and import capabilitie to copy objects such as journeys, content templates, or fragments, across multiple sandboxes. [Read more](../administration/sandboxes.md)

## March 2025 {#mar-2025}

* The page about Audience Qualification events has been updated with new recommendations. [Read more](../building-journeys/audience-qualification-events.md)
* Custom action troubleshooting capability is now available to all customers (GA). [Read more](../action/troubleshoot-custom-action.md)
* Data Hygiene is now Data Lifecycle in the product user interface. The documentation has been updated to reflect this change. [Read more](../privacy/data-hygiene.md)
* The missing Landing Page built-in permissions have been added to the documentation. [Read more](../administration/ootb-permissions.md)
* A note has been added about scheduling recurring campaigns. [Read more](../campaigns/create-campaign.md)
* The section about inserting links and enabling tracking in an email message has been updated and reorganized. [Read more](../email/message-tracking.md)
* The section about personalization capabilities into Adobe Journey Optimizer has been reorganized and improved. [Read more](../personalization/personalize.md)
* Decision management API to list personalized offers has been updated with a sample to perform pagination if multiple personalized offers are missing from the response. [Read more](../offers/api-reference/offers-api/personalized-offers/offers-list.md)
* A new page gathering all information regarding the List unsubscribe feature has been created for improved clarity. [Read more](../email/list-unsubscribe.md)
* The Frequency capping section has been updated with information on how the frequency capping counter is updated for the Decisioning and Batch Decisioning APIs, in addition to the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)

## February 2025 {#feb-2025}

* The Read Audience activity guardrails have been updated to specify that only one activity can be used in a journey and that it can target only one audience. [Read more](../building-journeys/read-audience.md)
* Journey guardrails when using Adobe Campaign activities have been updated. [Read more](../start/guardrails.md#ac-g)
* Steps to create your first journeys have been detailed, and links to documentation section have been added. [Read more](../building-journeys/journey-gs.md)
* A new page is now available to detail the journey dashboard and filtering user interface. [Read more](../building-journeys/journey-ui.md)
* Documentation for **[!UICONTROL Send-Time optimization]** and its related FAQ have been updated, improved and moved to a new dedicated page. [Read more](../building-journeys/send-time-optimization.md)
* New guardrails have been added for journey events. [Read more](../start/guardrails.md#events-g)
* The built-in channel actions page has been reorganized. [Read more](../building-journeys/journeys-message.md)
* Guardrails & limitations have been added in the Decisioning and Decision management sections.
    * [Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md)
    * [Decision management guardrails & limitations](../offers/decision-management-guardrails.md)
* A new section on context data has been added in the Decision management documentation. It provides information on how to leverage context data in the decisioning engine, for example to design a decision rule that requires the current weather to be ≥80 degrees at the time the decision request is made. [Read more](../offers/context-data.md)

## January 2025 {#jan-2025}

* A new section on the **[!UICONTROL Execution address]** option in the email configuration has been added. The primary address is defined at the sandbox level, but the default setting can be overidden for a specific email configuration. [Read more](../email/email-settings.md#execution-address)

* The **Get started with deliverability** page has been updated with the possibility to create IP warmup workflows directly from the user interface. [Read more](../reports/deliverability.md#reputation)

* The **Header parameters** section has been updated to reflect the new labels and changes in the user interface. [Read more](../email/email-settings.md#email-header)

* The **Forward email** section has been updated to specify that all emails sent to the **From email** address are forwarded to the forward email address. If no forward email is specified, these emails are discarded. [Read more](../email/email-settings.md#email-settings)

* The maximum size of contextual attributes passed into an API-triggered campaign request has been updated to 200kb. [Read more](../campaigns/api-triggered-campaigns.md#contextual)

* A new section has been added to the **Manage fragments** page to describe how to add new attributes to a live fragment. The whole page has also been improved. [Read more](../content-management/manage-fragments.md#adding-new-attributes)

* A "Guardrails & limitations" section has been added to the conflict management & prioritizations tools documentation. [Read more](../conflict-prioritization/gs-conflict-prioritization.md)

* A new end-to-end use case has been added to present all the steps needed to use Decisioning in content experiments with the [!DNL Journey Optimizer] code-based experience channel. [Read more](../experience-decisioning/experience-decisioning-uc.md)

* The **Configure email settings** page has been divided into several sub-pages for improved readability, including new standalone pages dedicated to [List unsubscribe](../email/list-unsubscribe.md), [Header parameters](../email/header-parameters.md) and [URL tracking](../email/url-tracking.md).

## December 2024 {#nov-2024}

* A note has been added to help troubleshoot a potential error message when making an API call to enable datasets for personalization using Adobe Experience Platform data. [Read more](../personalization/aep-data-perso.md)

## October 2024 {#oct-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] October '24 release have been detailed in the documentation. [Read more](release-notes.md)
* All communication channels available in [!DNL Journey Optimizer] are now grouped in a dedicated section of the documentation. [Read more](../channels/gs-channels.md)
* The **Configure your code-based experience** page has been improved to make the process clearer, including the section explaining what a surface URI is. [Read more](../code-based/code-based-configuration.md)
* The **Create web channel configuration** page has been updated to clarify the steps when creating a pages matching rule, which also apply to Code-based experience configuration. [Read more](../web/web-configuration.md#web-page-matching-rule)
* A note about the upcoming time-to-live (TTL) guardrail for system-generated datasets has been added. [Read more](../data/get-started-datasets.md)
* A new section has been added to describe how to preview your code-based personalized experiences right on your browser or on your mobile devices, using the **Preview on device** option when simulating content in a journey or a campaign. [Read more](../code-based/test-code-based.md#preview-on-device)
* A new page has been added on how to leverage Custom upload audiences for decisioning. [Read more](../offers/custom-upload-decisioning.md)
* A new page has been added to introduce the decision capabilities available in Journey Optimizer. [Read more](../experience-decisioning/gs-decision.md)
* Guardrails and limitations have been added to the Decisioning documentation. [Read more](../experience-decisioning/gs-experience-decisioning.md#guardrails)

## September 2024 {#sept-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] Sept '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Added a section about journey retry management. [Read more](../building-journeys/read-audience.md#read-audience-retry)
* The FAQ about Capping/throttling rule for custom actions has been updated to mention the default capping rule. [Read more](../configuration/external-systems.md#faq)
* The Control access section has been updated with permissions related to AI Assistant Content Generator. [Read more](../administration/high-low-permissions.md#ai-orchestrated-campaign)
* A video about AI Assistant Content Generator for email generation has been added. [Read more](../content-management/generative-full-content.md#video)

<!--

## August 2024 {#aug-2024}

* All new features and improvements coming with [!DNL Journey Optimizer] August '24 release have been detailed in the documentation. [Read more](release-notes.md)
* Performance guardrails for Decision management have been updated to mention Decisioning APIs delivery throughputs with/without Edge Segmentation. [Read more](../start/guardrails.md#decision-management)
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
* Information has been added in the Decision management documentation regarding edge and hub regions management when using frequency capping with the Edge Decisioning API. [Read more](../offers/offer-library/add-constraints.md#frequency-capping)
* Information has been added on identity creation with custom namespaces when working with API-triggered campaigns. [Read more](../campaigns/api-triggered-campaigns.md)
* Screeshots have been updated to reflect the improved Journey canvas.
* Naming constraints has been updated in the following page: [Configure a unitary event](../event/about-creating.md), [Configure a business event](../event/about-creating-business.md#gs-business-events), [Configure a custom action](../action/about-custom-action-configuration.md#configuration-steps), [External data sources](../datasource/external-data-sources.md)
* A note has been added on Send Time Optimization availability. [Read more](../building-journeys/send-time-optimization.md)
* A new technical use case has been added on how to create a custom action to send data to Experience Platform. [Read more](../building-journeys/custom-action-aep.md)

## March 2024 {#march-2024}
 
* A Frequently Asked Questions section has been added to address common questions regarding the use of audience composition and custom upload audiences in Journey Optimizer. [Read more](../audience/about-audiences.md#faq)
* All new features and improvements coming with [!DNL Journey Optimizer] March '24 release have been detailed in the documentation. [Read more](release-notes.md#mar-2024)
* The page on profile entrance management has been improved. [Read more](../building-journeys/entry-management.md)
* Troubleshooting information has been added to the Alerts page. [Read more](../reports/alerts.md#alert-profile-error-rate)
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
* Information has been added regarding the behavior of timeouts on event activities in journeys. When no event is received during the specified timeout period, individuals will continue the journey if no timeout path is defined. [Read more](../building-journeys/general-events.md#events-specific-time)
* In-app channel configuration prerequisites have been updated with a note about the usage of a custom Dataset preference merge policy. [Read more](../in-app/inapp-configuration.md)
* More details have been added about how to manipulate collections in a custom action response. [Read more](../action/action-response.md#exp-syntax).
* A link to the [Schema Dictionary for Adobe Journey Optimizer](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=fr) has been added to the home page.
* An outdated reference to the AJO Message resource has been removed from the list of resources available in the Audit Log. When an update is done on a message in a journey, a **Journey** log is created. [Read more](../privacy/audit-logs.md)
* Additional recommendations have been added about the usage of the **Read Audience** activity. [Read more](../building-journeys/read-audience.md#must-read)
* The Get started with Adobe Experience Platform audiences page has been improved with a list of audience generation methods. [Read more](../audience/about-audiences.md)
* Best practices have been added when choosing an endpoint to target using a custom action. [Read more](../action/about-custom-action-configuration.md)
* An note has been added to notify users that events cannot be fired from external systems using an API. [Read more](../building-journeys/testing-the-journey.md#important_notes)
* Information on the **currentActionField** function has been added to the list of [collection management functions](../building-journeys/expression/collection-management-functions.md). An expression sample leveraging the function has been added in the [Use API call reponses in custom actions](../action/action-response.md) page.
* Update custom authentication doc regarding cache duration. [Read more] (../datasource/external-data-sources.md)
* Support of `listObject` has been modified in multiple functions.
* Update the **duration** parameter in the `toString` function. [Read more](../building-journeys/functions/conversion-functions.md#toString)
* For some external data sources use-cases, usage of custom actions is recommended.
* Event field syntax has been updated. The following syntax is deprecated `@(my_event.myfield}` and replaced by `@event{my_event.myfield}`. [Read more](../building-journeys/expression/field-references.md)

+++ 2023

## November 2023 {#nov-2023}

* The guardrail that limits all custom actions has been changed from 150,000 calls over 30 seconds to 300,000 calls over one minute. In addition, the default capping no longer applies to each endpoint. It is now performed per host and per sandbox. For example, on a sandbox, if you have two endpoints with the same host (eg: `https://www.adobe.com/endpoint1` and `https://www.adobe.com/endpoint2`), the capping will apply for all endpoints under the adobe.com host. "endpoint1" and "endpoint2" will share the same capping configuration and having one endpoint reach the limit will have an impact on the other endpoint. [Read more](../action/about-custom-action-configuration.md)
* A new status for email campaigns has been added to the list of campaigns' statuses. [Read more](../campaigns/manage-campaigns.md#modify-an-action-campaign)
* The Get started with Adobe Experience Platform audiences section has been updated to reflect the audience evaluation methods available and how to select them. [Read more](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)
* A new subsection has been added to specify which events should be avoided when building your audience if you are using the streaming segmentation evaluation method. [Read more](../audience/about-audiences.md#streaming-segmentation-events-guardrails)

## October 2023 {#oct-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] October '23 release have been detailed in the documentation. [Read more](release-notes.md)
* Added GIFs to illustrate some key capabilities, such as: [Content templates](../content-management/content-templates.md), [Fragments](../content-management/fragments.md), [Computed attributes](../audience/computed-attributes.md), [Direct mail](../direct-mail/get-started-direct-mail.md), [Tags](../start/search-filter-categorize.md#tags), [Decision management optimization models](../offers/ranking/personalized-optimization-model.md), [API-triggered campaigns](../campaigns/api-triggered-campaigns.md), and [Content experiment](../content-management/content-experiment.md).
* The Schema creation process has been updated to reflect latest updates in the user interface, coming with Adobe Experience Platform changes. [Read more](../audience/creating-test-profiles.md) 
* Decision management guardrails have been added to the Guardrails and limitations page. [Read more](../start/guardrails.md#decision-management)
* The Header parameters section has been updated to reflect how out-of-office notifications and challenge responses are handled (they are received on the **[!UICONTROL Error email]**). [Read more](../email/email-settings.md#email-header)
* A new section on how to preview and test your content has been created. [Read more](../content-management/preview-test.md)
* The Implement single-page applications page has been moved to the Adobe Experience Paltform Web SDK documentation. [Read more](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-spa-implementation.html?lang=fr){target="_blank"}
* The Capping section has been updated to reflect the label changes relating to offer capping in the Decision management interface. [Read more](../offers/offer-library/add-constraints.md#capping)
* The Add dynamic content into emails has been updated with details on how to delete a variant. [Read more](../personalization/dynamic-content.md#emails)
* The example for capping & throttling configurations has been updated. [Read more](../configuration/external-systems.md)
* The limitation regarding scalar arrays has been removed from the external data source section. [Read more](../datasource/external-data-sources.md)
* The multi-channel journey use case has been updated. [Read more](../building-journeys/journeys-uc.md)
* The Journey Optimizer documentation set has been updated to reflect the new Experience Platform schema creation process. 

## September 2023 {#september-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] September '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added with scaling best practices and real-time stitching guidance. [Read more](../start/best-practices.md)
* A Frequently-Asked-Questions section has been added for Send-Time Optimization. [Read more](../building-journeys/journeys-message.md#faq-send-time)
* A note has been added for the audience qualification activity. It may take up to 10 minutes to be active and listen to profiles entering or exiting the audience. [Read more](../building-journeys/audience-qualification-events.md#batch-speed-segment-qualification)
* A list of limitations to be aware of when creating decision rules has been added to the Decision management documentation. [Read more](../offers/offer-library/creating-decision-rules.md)
* Links to access control documentation have been updated. [Read more](../administration/permissions.md)
* In-app channel prerequisites have been updated with Adobe Experience Platform Data Collection details. [Read more](../in-app/inapp-configuration.md)
* Some expressions presented in ranking formula examples have been updated to avoid validation errors. [Read more](../offers/ranking/create-ranking-formulas.md#ranking-formula-examples)
* A warning has been added to the Define decision scopes section to specify that if AI model is used in an evaluation criteria group, all the evaluation criteria in that group must use the AI ranking method, with the same specific AI model. Moreover, only one evaluation criteria group can use AI model. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

## August 2023 {#august-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] August '23 release have been detailed in the documentation. [Read more](release-notes.md)
* The note about **authentication cache management** in journey has been updated to detail that the token is not shared between different journeys. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)
* The page about journey **entry management** has been updated to clarify behavior. [Read more](../building-journeys/entry-management.md)
* Offer decisioning **export datasets** are now enabled by default. The note about the previous behavior has been removed.  [Read more](../offers/export-catalog/get-started-export.md)
* Various **campaign report metrics** have been renamed, in both Live and Global reports. [Read more](../reports/campaign-live-report.md)
* A new section has been added on content experiment prerequisites for the web channel. [Read more](../web/web-prerequisites.md#experiment-prerequisites)
* A warning has been added on the **Work with content templates** page to indicate that currently tracking is not supported when testing email content templates. To test tracking, you must use the content template in an email and send a proof. [Read more](../content-management/content-templates.md#content-templates)
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
* Decision management documentation has been clarified with a note specifying that the use of Object Level Access Control is not available for dynamic collections. [Read more](../offers/offer-library/creating-collections.md)

## May 2023 {#may-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] May '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A new page has been added to describe how to set up the subdomain that will be used to publish content coming from the Adobe Experience Manager Assets Essentials in your web experiences. [Read more](../web/web-delegated-subdomains.md)
* A new subsection has been added to explain how to add personalized tracking parameters to URLs in the Email Designer. [Read more](../email/message-tracking.md#url-tracking)
* A new section has been added to describe how to ensure that the choice of your customers who opt out from having their profile data used for personalization is honored. [Read more](../privacy/opt-out.md#opt-out-personalization)
* A note has been added about using special international characters in URLs included in email contents. [Read more](../email/message-tracking.md#insert-links)
* The permission needed to test and publish landing pages has been added. [Read more](../landing-pages/create-lp.md)
* A note has been added about the Adobe Experience Platform endpoints needed to have your custom events accounted for in Decision management frequency capping. [Read more](../offers/data-collection/schema-requirement.md#track-custom-events)

## April 2023 {#apr-2023}

* All new features and improvements coming with [!DNL Journey Optimizer] April '23 release have been detailed in the documentation. [Read more](release-notes.md)
* A note has been added to specify that built-in actions cannot be removed. [Read more](../start/guardrails.md#custom-actions-g)
* Information has been added on serviceEvents as well as a query example to check the details of a serviceEvent. [Read more](../reports/query-examples.md#common-queries) 
* A note has been added to specify that you cannot perform queries on time series. [Read more](../building-journeys/condition-activity.md)
* Adobe Experience Manager Assets Essentials and Adobe Stock have been added to the multi-solution integration page. [Read more](../integrations/ajo-integrations.md)
* The warning on multi-level email subdomains not being allowed has been removed as they are now supported. [Read more](../configuration/delegate-subdomain.md)
* A note has been added to specify that, if changes are made to an offer decision which is being used in a journey's message, you need to unpublish the journey and republish it. [Read more](../building-journeys/publish-journey.md)
* Explanation on how to make sure events are correctly accounted for in the capping counter has been clarified in the Decision management **Capping event** section. [Read more](../offers/offer-library/add-constraints.md#capping-event)
* A new section has been added to the **Change execution addresses** page. It specifies that it is possible to override the execution field set globally in the journey advanced parameters, but the email address override should only be used for specific use cases. Most of the time, the value defined as the primary address in the **Execution fields** is the one that should be used. [Read more](../configuration/primary-email-addresses.md#override-execution-address-journey)
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
    * [Push notification channel](../../rp_landing_pages/push-landing-page.md)
    * [SMS channel](../sms/get-started-sms.md)

* The Configuration guide has been reorganized for improved readability. [Read more](../configuration/get-started-configuration.md)

## November 2022 {#november-2022}

* Added a new page about Journey Optimizer integrations. [Read more](../integrations/ajo-integrations.md)
* Added a recommendation about the length of mirror pages URLs. [Read more](../email/message-tracking.md)
* A new subsection in the email settings configuration has been added on the reply to email address, including recommendations to ensure proper reply management. [Read more](../email/email-settings.md#send-to-suppressed-email-addresses)
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
* Updated the pages related to the [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly) and [toString](../building-journeys/functions/conversion-functions.md#toString) functions.
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
* Added a new page on journey lifecyle. [Read more](../building-journeys/journey.md)
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
* A new subsection on setting up a forward email address has been added. Note that you cannot do it through the user interface. [Read more](../email/email-settings.md#email-settings)

## April 2022 {#april-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] April '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **reactions** event documentation page has been updated. [Read more](../building-journeys/reaction-events.md)
* Videos for Decision management capabilities have been updated to reflect Journey Optimizer user interface. [Read more](../offers/get-started/starting-offer-decisioning.md)
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
* The [replace](../building-journeys/functions/string-functions.md#replace) and [replaceAll](../building-journeys/functions/string-functions.md#replaceAll) function documentation pages have been updated with additional information and examples regarding the target parameter.
* Best practices have been added to the [Operators](../building-journeys/expression/operators.md#important-notes) page.

## January 2022 {#january-2022}

* All new features and improvements coming with [!DNL Journey Optimizer] Jan '22 release have been detailed in the documentation. [Read more](release-notes.md)
* The **Offer decisioning AI rankings** section has been updated with a more detailed description of the auto-optimization model. [Read more](../offers/ranking/auto-optimization-model.md)
* A new section on the schema requirements needed to be able to send in event types when using an AI model has been added. [Read more](../offers/data-collection/schema-requirement.md)
* The section related to [!DNL Journey Optimizer] personalization capabilities has been reorganized for better readability. [Read more](../personalization/personalize.md)
* The **Create message presets** section has been divided into several sections for improved clarity. [Read more](../configuration/channel-surfaces.md#create-channel-surface)
* The **Opt-out management** section has been clarified and slightly reorganized. [Read more](../privacy/opt-out.md#opt-out-decision-management)
* The **Insert links** section has been updated to reflect the recent user interface changes. [Read more](../email/message-tracking.md#insert-links)

+++

+++ 2021

## November 2021 {#november-2021}

* A full description of the **advanced expression editor** used in journeys is now available. [Read more](../building-journeys/expression/expressionadvanced.md)
* A new section about **CNAME subdomain delegation method** has been added. [Read more](../configuration/delegate-subdomain.md#cname-subdomain-setup)

## October 2021 {#october-2021}

* All new features and improvements coming with [!DNL Journey Optimizer] Oct '21 release have been detailed in the documentation. [Read more](release-notes.md)
* Added **Date time function** list. [Read more](../personalization/functions/dates.md)
* New **Get Started sections per user persona**. Take your own path to get to your goals faster! [Read more](../start/quick-start.md)
* New **Edit a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New **Edit a PTR record** section. [Read more](../configuration/ptr-records.md#edit-ptr-record)
* New **Deactivate a message preset** section. [Read more](../configuration/channel-surfaces.md#edit-channel-surface)
* New limitations added to the **Decision Management API developer guide** on offer constraints not supported with the mobile [!DNL Experience Edge] workflows. [Read more](../offers/api-reference/offers-api/personalized-offers/create.md#limitations)
* New **Create simulations** section. [Read more](../offers/offer-activities/simulation.md)
* Updated **Add decision scopes** section. [Read more](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)
* Updated **Define content for your representations** section, including a new [subsection](../offers/offer-library/creating-personalized-offers.md#custom-text) on how to define and personalize custom text. [Read more](../offers/offer-library/creating-personalized-offers.md#content)

## September 2021 {#september-2021}

* The following function pages have been updated: [sethours](../building-journeys/functions/date-functions.md#setHours), [getListItem](../building-journeys/functions/list-functions.md#getListItem), [inSegment](../building-journeys/functions/functioninaudience.md)

* The following functions have been added: [filter](../building-journeys/functions/list-functions.md#filter), [intersect](../building-journeys/functions/list-functions.md#intersect), [toDateOnly](../building-journeys/functions/conversion-functions.md#toDateOnly)

* The dateOnly date type has been added in the expression editor documentation. [Read more](../building-journeys/expression/data-types.md)

* Added details on custom action cache duration. [Read more](../datasource/external-data-sources.md#custom-authentication-mode)

* Added information on custom action default ports. [Read more](../action/about-custom-action-configuration.md#url-configuration)

* Added information on multiple business event use cases. [Read more](../event/about-creating-business.md#multiple-business-events)

* Added commonly used examples to query Journey Step Events in Data Lake. [Read more](../reports/query-examples.md)

* Added a new **Limitations** page. [Read more](../start/guardrails.md)

* Improved the **Quick start** page with steps for different personas. [Read more](../start/quick-start.md)

* Now all the Decision management features described in the dedicated section also apply to the Adobe Experience Platform users leveraging the Offer Decisioning application. [Read more](../offers/get-started/starting-offer-decisioning.md)

* Added a subsection to clarify the differences between using audiences versus decision rules when applying a constraint to restrict the selection of offers for a given placement. [Read more](../offers/offer-activities/create-offer-activities.md#decision-list)

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
* Documented the Decision management new **[!UICONTROL Overview]** tab. [Read more](../offers/get-started/user-interface.md#overview)
* Added new sections to describe the actions available from the offer and decision lists: [Offer list](../offers/offer-library/creating-personalized-offers.md#offer-list) and [Decision list](../offers/offer-activities/create-offer-activities.md#decision-list).

+++
-->
