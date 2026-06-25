---
solution: Journey Optimizer
product: journey optimizer
title: Terminologie clé
description: Termes et concepts essentiels dans Adobe Journey Optimizer
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 14e72376-87ad-4fae-bf8c-f347109d7903
TQID: https://experienceleague.adobe.com/-aDvt4RUXyf0EnPfFTJkG1CvWgte-1Fr6YaWvgcNNu4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e0eb8757-182f-49f3-94a4-1587d16f5094id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 9a0d5b396d569f7375a719229cf5a3779448567e
workflow-type: tm+mt
source-wordcount: 1617
ht-degree: 30%

---

# Terminologie clé {#key-terminology}

>[!BEGINSHADEBOX]

**Sur cette page :** recherchez les termes et concepts Adobe Journey Optimizer essentiels pour naviguer sur la plateforme en toute confiance et collaborer efficacement avec votre équipe.

>[!ENDSHADEBOX]

Ce guide de référence définit les termes essentiels que vous rencontrerez lorsque vous utiliserez Adobe Journey Optimizer. La compréhension de ces concepts vous permet de naviguer sur la plateforme en toute confiance et de collaborer efficacement avec votre équipe.

Pour obtenir des paires de termes à consonance similaire qui sont souvent confus, tels que **Prise de décision / Gestion des décisions** ou **Cartes de contenu / Messages In-App**, consultez [Lorsque les termes se ressemblent](#disambiguation) au bas de cette page.

>[!NOTE]
>
>Adobe Journey Optimizer est basé sur **Adobe Experience Platform**. De nombreux concepts fondamentaux que vous rencontrerez, tels que les profils clients en temps réel, les sandbox, les schémas et les jeux de données, sont des concepts Adobe Experience Platform et non spécifiques à Journey Optimizer. Pour connaître la définition de ces termes, consultez le glossaire [](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html?lang=fr){target="_blank"}.

## Termes du parcours et de la campagne {#journey-campaign-terms}

| Terme | Définition |
|------|------------|
| **Parcours** | Série d’étapes reliées entre elles qui guident les clientes et les clients à travers des expériences liées à votre marque au fil du temps. Chaque étape se produit en fonction des actions des clientes et clients ou des déclencheurs temporels, ce qui permet des interactions séquentielles et personnalisées. [En savoir plus](../building-journeys/journey.md) |
| **Campagne** | Action marketing coordonnée qui diffuse du contenu à une audience spécifique sur un ou plusieurs canaux. Contrairement aux parcours, les campagnes exécutent des actions simultanément. Journey Optimizer prend en charge trois types de campagnes : **Campagnes d’action** (envois par lots planifiés), **Campagnes déclenchées par l’API** (messagerie en temps réel pilotée par un événement via l’API) et **Campagnes orchestrées** (workflows complexes à plusieurs étapes avec une zone de travail visuelle). [En savoir plus](../campaigns/get-started-with-campaigns.md) |
| **Événement** | Action ou occurrence qui déclenchent ou font avancer un parcours. Les événements peuvent être des actions des clientes et clients (achat, abandon de panier) ou des événements système (date/heure, modification des données). [En savoir plus](../event/about-events.md) |
| **Canal** | Méthode utilisée pour communiquer avec les clientes et clients : e-mail, SMS, notifications push, messages in-app, web ou courrier. Chaque canal nécessite une configuration spécifique. [En savoir plus](../configuration/get-started-configuration.md) |

## Termes du client et de l’audience {#customer-audience-terms}

| Terme | Définition |
|------|------------|
| **Audience** | Groupe de clientes et clients qui partagent des caractéristiques ou des comportements communs, tels que « clientes et clients ayant effectué un achat au cours des 30 derniers jours » ou « membres du programme de fidélité ». Les audiences sont utilisées pour cibler des segments clients spécifiques. [En savoir plus](../audience/about-audiences.md) |
| **Qualification d’audience** | Processus qui se produit lorsqu’un client ou une cliente rejoint ou quitte une audience. Journey Optimizer peut déclencher des actions lorsqu’une personne rejoint ou quitte une audience, assurant ainsi des communications opportunes et pertinentes. [En savoir plus](../building-journeys/audience-qualification-events.md) |
| **Profils pouvant être engagés** | Les profils clients uniques engagés par le biais de parcours, de campagnes ou d’activités de prise de décision sur une période mobile de 12 mois. Il s’agit de la mesure de licence clé pour Journey Optimizer : chaque profil est comptabilisé une fois par sandbox, quel que soit le nombre de parcours ou de campagnes qu’il entre. Surveillez le nombre à **[!UICONTROL Administration]** > **[!UICONTROL Utilisation de la licence]**. [En savoir plus](../audience/license-usage.md) |
| **Profil de test** | Profils fictifs utilisés pour tester et prévisualiser des messages avant de les envoyer à des clientes et clients réels. Les profils de test permettent de vérifier la personnalisation, le contenu et la logique du parcours. [En savoir plus](../audience/creating-test-profiles.md) |

## Termes de contenu et de personnalisation {#content-terms}

| Terme | Définition |
|------|------------|
| **Personnalisation** | Processus de personnalisation du contenu en fonction des clientes et clients individuels à l’aide de leurs données de profil, de leurs préférences et de leurs comportements. Par exemple, l’insertion du nom d’un client ou d’une cliente, ou l’affichage de recommandations de produits en fonction de l’historique de navigation. [En savoir plus](../personalization/personalize.md) |
| **Modèle de contenu** | Conception de message réutilisable pouvant être utilisée dans plusieurs campagnes et parcours pour maintenir la cohérence de la marque et accélérer la création de contenu. [En savoir plus](../content-management/content-templates.md) |
| **Fragment** | Bloc de contenu réutilisable (par exemple, en-tête, pied de page ou bannière promotionnelle) pouvant être utilisé sur plusieurs messages pour garantir la cohérence et permettre des mises à jour centralisées. [En savoir plus](../content-management/fragments.md) |
| **Page de destination** | Page web autonome sur laquelle les clients et clients peuvent s’inscrire ou se désinscrire des communications, s’abonner à des services ou fournir des informations au moyen de formulaires en ligne. [En savoir plus](../landing-pages/get-started-lp.md) |
| **Expérience de contenu** | Un framework de test A/B qui divise une audience en groupes aléatoires et diffuse différentes variantes de message (contenu, objet ou offre) à chaque groupe, puis identifie la variante la plus performante en fonction d’une mesure de succès définie. [En savoir plus](../content-management/get-started-experiment.md) |
| **Expérimentation** | Fonctionnalité plus large de Journey Optimizer pour tester et optimiser les décisions : les expériences de contenu testent des variantes de message dans les campagnes et les parcours, tandis que les tests d’expérimentation de prise de décision offrent des stratégies de sélection. Toutes deux utilisent l’analyse statistique pour identifier les approches gagnantes. [En savoir plus](../content-management/get-started-experiment.md) |

## Conditions des décisions et des offres {#decision-terms}

| Terme | Définition |
|------|------------|
| **Prise de décision** | Le cadre de décision de génération actuelle dans Journey Optimizer, recommandé pour les nouvelles mises en œuvre. Offre une gestion de catalogue d’éléments basée sur des schémas, des règles de collection flexibles, des composants de décision réutilisables et des fonctionnalités d’expérimentation. Disponible pour les applications Code, Push, SMS et E-mail. [En savoir plus](../experience-decisioning/gs-experience-decisioning.md) |
| **Gestion des décisions** | L’ancienne fonctionnalité Offer Decisioning dans Journey Optimizer. Utilise une bibliothèque centrale d’offres marketing et un moteur de décision basé sur des règles qui applique des contraintes aux profils clients en temps réel. Toujours prise en charge pour les implémentations existantes, mais les nouvelles implémentations doivent utiliser Decisioning à la place. Prend en charge les e-mails, in-app, notifications push, SMS et publipostage direct. [En savoir plus](../offers/get-started/starting-offer-decisioning.md) |
| **Offre** | Message marketing, remise ou promotion pouvant être présentés aux clientes et clients. Les offres incluent des règles d’éligibilité qui déterminent les clientes et clients qui peuvent les recevoir. [En savoir plus](../offers/offer-library/creating-personalized-offers.md) |
| **Politique de décision** | Ensemble de règles et de stratégies qui déterminent l’offre à présenter à quelle personne et à quel moment, en fonction de contraintes telles que les règles d’éligibilité, de priorité et de limitation. [En savoir plus](../experience-decisioning/create-decision.md) |

## Termes relatifs aux données et à la configuration {#data-config-terms}

| Terme | Définition |
|------|------------|
| **Configuration du canal** | Les paramètres qui définissent la manière dont les messages sont diffusés pour un canal spécifique, y compris les détails de l’expéditeur, le sous-domaine, le groupe d’adresses IP et le type de message (marketing ou transactionnel). Précédemment appelé « surface » ou « paramètre prédéfini » dans l’ancienne documentation. [En savoir plus](../configuration/channel-surfaces.md) |
| **Liste de suppression** | Une liste d&#39;adresses e-mail et de domaines automatiquement exclus de la diffusion des messages en raison de hard bounces, de plaintes contre le spam ou d&#39;ajouts manuels. L&#39;envoi aux adresses supprimées est bloqué pour protéger la délivrabilité et la réputation de l&#39;expéditeur. [En savoir plus](../reports/suppression-list.md) |

## Termes de conflit et de hiérarchisation {#conflict-terms}

| Terme | Définition |
|------|------------|
| **Ensemble de règles** | Groupe nommé de règles métier appliquées aux parcours et aux campagnes pour régir le comportement des messages. Un ensemble de règles peut combiner le capping de la fréquence, les limites d’entrée du parcours et les heures creuses en une seule politique réutilisable. [En savoir plus](../conflict-prioritization/rule-sets.md) |
| **Capping de la fréquence** | Règle dans un ensemble de règles qui limite le nombre de messages qu’un profil peut recevoir au cours d’une période donnée, par canal ou type de communication (vente, promotion, etc.). Les profils qui dépassent la limite sont automatiquement exclus de la diffusion. [En savoir plus](../conflict-prioritization/channel-capping.md) |

## Lorsque les termes se ressemblent : guide de désambiguïsation {#disambiguation}

Adobe Journey Optimizer s’est développé au fil des ans, ce qui signifie que certaines zones de fonctionnalités partagent des noms similaires. Utilisez les tableaux ci-dessous pour identifier rapidement la fonctionnalité qui correspond à vos besoins.

### Prise de décision ou gestion de décision {#decisioning-vs-dm}

Ces deux fonctionnalités sélectionnent et diffusent les offres, mais elles interviennent à différentes étapes du cycle de vie du produit.

| | Prise de décision | Gestion des décisions |
|---|---|---|
| **Statut** | Actuel : recommandé pour toutes les nouvelles mises en œuvre | **Hérité** — toujours pris en charge, mais plus recommandé pour les nouvelles implémentations |
| **Catalogue d&#39;articles** | Métadonnées flexibles basées sur des schémas | Bibliothèque des offres centralisée |
| **Canaux pris en charge** | Expérience basée sur le code, notifications push, SMS, e-mail | E-mail, In-App, Push, SMS, Courrier |
| **Différenciateur clé** | Composants de décision réutilisables, expérimentation, feuille de route des canaux élargie | Moteur de contraintes éprouvé ; migration vers Decisioning pour les nouveaux projets |
| **Prise en main** | [Prise de décision](../experience-decisioning/gs-experience-decisioning.md) | [Gestion des décisions](../offers/get-started/starting-offer-decisioning.md) |

Si vous utilisez actuellement la gestion de décision et souhaitez changer, reportez-vous au [guide de migration](../experience-decisioning/migrate-to-decisioning.md).

### Types de campagne {#campaign-types-disambiguation}

Journey Optimizer propose trois types de campagnes qui sont activés différemment et qui servent des cas d’utilisation distincts.

| | Campagnes d’action (campagnes planifiées) | Campagnes déclenchées par API | Campagnes orchestrées |
|---|---|---|---|
| **Activation** | Manuelle ou planifiée | Appel API externe | Zone de travail visuelle du workflow |
| **Idéal pour** | Envois par lots ponctuels ou récurrents (newsletters, promotions) | Messages en temps réel pilotés par les événements (confirmations de commande, réinitialisations de mot de passe) | Programmes cross-canal complexes et à plusieurs étapes |
| **Source** | Attributs de profil | Attributs de profil + contexte de la payload de l’API | Attributs de profil + données relationnelles |
| **Prise en main** | [Campagnes d’action](../campaigns/create-campaign.md) | [Campagnes déclenchées par API](../campaigns/api-triggered-campaigns.md) | [Campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md) |

Pour une présentation complète de tous les types de campagne et des cas d’utilisation de chacun, reportez-vous à la section [Prise en main des campagnes](../campaigns/get-started-with-campaigns.md).

### Limitation de la fréquence par rapport à l’arbitrage du parcours {#capping-vs-arbitration}

Tous deux sont des mécanismes d’ensemble de règles sous l’ensemble d’outils Conflit et hiérarchisation , mais ils abordent différents problèmes.

| | Capping de la fréquence | Arbitrage des parcours |
|---|---|---|
| **Problème résolu** | Un profil reçoit trop de messages au fil du temps | Un profil se qualifie pour plusieurs parcours simultanément |
| **Périmètre** | Par canal et type de communication (vente, promotion, etc.) | Inscription au parcours : nombre de parcours simultanés ou parcours gagnant |
| **Mécanisme** | Limite le nombre de messages par période ; exclut automatiquement les profils sur-sollicités | Utilise les scores de priorité et les règles de limitation pour décider du parcours dans lequel un profil entre |
| **Configuré en** | Jeux de règles → Capping de la fréquence | Jeux de règles → limitation et arbitrage du Parcours |
| **En savoir plus** | [Définir le capping de la fréquence par canal](../conflict-prioritization/channel-capping.md) | [Gérer la limitation et l’arbitrage des parcours ](../conflict-prioritization/journey-capping.md) |

### Cartes de contenu par rapport aux messages in-app {#content-cards-vs-in-app}

Les deux canaux diffusent les messages dans une application mobile ou web, mais ils ont des modèles de rendu et des comportements de persistance différents.

| | Cartes de contenu | Messages In-App |
|---|---|---|
| **Modèle d’affichage** | Cartes persistantes intégrées à l’interface utilisateur de l’application (flux, boîte de réception ou surface personnalisée) | Superpositions transitoires, bannières ou modèles affichés sur le dessus de l’application |
| **Persistance** | Reste visible jusqu’à ce qu’il soit explicitement ignoré ou expiré | Disparaît lorsque l’utilisateur interagit ou le ferme |
| **Déclencheur** | Rendus SDK au chargement ; les règles contrôlent l’affichage et le rejet | Un événement temps réel dans le parcours ou la campagne déclenche la diffusion |
| **Idéal pour** | Promotions en cours, statut de fidélité, alertes persistantes | Conseils d’intégration, offres de durée limitée, notifications transitoires |
| **Prise en main** | [Cartes de contenu](../content-card/create-content-card.md) | [Messages In-App](../in-app/get-started-in-app.md) |

>[!NOTE]
>
>**Adobe Journey Optimizer ou Journey Optimizer B2B edition :** il s’agit de deux produits distincts appartenant à la même famille de marques. Adobe Journey Optimizer (cette documentation) cible les parcours clients B2C. Journey Optimizer B2B edition a été spécialement conçu pour le marketing basé sur les comptes, qui fonctionne avec des groupes d’achats et des audiences de compte. Si vous recherchez de la documentation sur B2B edition, consultez le [guide de Journey Optimizer B2B edition](https://experienceleague.adobe.com/fr/docs/journey-optimizer-b2b/user/guide-overview){target="_blank"}.

## Rubriques connexes {#related-topics}

* [Fonctionnement de Journey Optimizer ](understanding-ajo.md) — Découvrez comment les parcours, les campagnes, les profils et les canaux s’intègrent dans l’architecture du produit.
* [Prise en main des fonctionnalités de prise de décision](../experience-decisioning/gs-decision.md) — Comparez les outils de prise de décision et de gestion des décisions côte à côte et choisissez l’approche appropriée pour votre implémentation.
* [Prise en main des parcours ](../building-journeys/journey.md) — Découvrez comment créer étape par étape des expériences client séquentielles déclenchées par un événement.
* [Prise en main des campagnes](../campaigns/get-started-with-campaigns.md) — Découvrez les trois types de campagnes (Action, Déclenché par API, Orchestré) et quand les utiliser.
* [Gestion des conflits et hiérarchisation](../conflict-prioritization/gs-conflict-prioritization.md) — Découvrez comment utiliser des ensembles de règles, le capping de la fréquence, les scores de priorité et les heures creuses pour éviter les messages excessifs.
* [Prise en main des canaux de communication](../channels/gs-channels.md) — Parcourez tous les canaux disponibles, leurs conditions préalables et comment les configurer.
