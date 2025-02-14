---
solution: Journey Optimizer
product: journey optimizer
title: À propos des mécanismes de sécurisation de la durée de vie (TTL) des jeux de données
description: Mécanismes de sécurisation de la durée de vie des jeux de données dans  [!DNL Adobe Journey Optimizer]
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: platform, lac de données, créer, lac, jeux de données, profil
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: 7aaaa566ec9e5a1cf50e067d7c3836bfc305b909
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 30%

---

# Mécanismes de sécurisation de la durée de vie (TTL) des jeux de données {#ttl-guardrail}

Depuis février 2025, un mécanisme de sécurisation de durée de vie (TTL) est déployé sur les jeux de données générés par le système Journey Optimizer dans **nouveaux sandbox et nouvelles organisations** comme suit :

* 90 jours pour les données dans la banque de profils,
* 13 mois pour les données du lac de données.

Cette modification sera déployée sur les **sandbox client existants** dans une phase ultérieure.

## Jeux de données affectés {#datasets}

Le tableau ci-dessous répertorie tous les jeux de données affectés et leur durée de vie respective dans le lac de données et le magasin de profils.

| Jeu de données | TTL du lac de données | TTL du magasin de profils |
|------|-----|-----|
| Jeu de données d’événement de feedback sur les messages AJO | 13 mois | 90 jours |
| Jeu de données d’événement d’expérience de tracking d’e-mail AJO | 13 mois | 90 jours |
| Jeu de données d’événement d’expérience de tracking de notifications push AJO | 13 mois | 90 jours |
| Jeu de données d’entité AJO | 13 mois | 90 jours |
| Jeu de données de surfaces AJO | 13 mois | S.O. |
| Jeu de données d’événement d’activité entrante AJO | 13 mois | 90 jours |
| Jeu de données de classification AJO | 13 mois | S.O. |
| Jeu De Données D’Événement De Retour En Cci D’E-Mail AJO | 13 mois | S.O. |
| Jeu de données d’événement acpEntity | 13 mois | S.O. |
| Parcours | 13 mois | S.O. |
| Événements d’étape de parcours | 13 mois | S.O. |
| Référentiel d’objets de décision - Offres personnalisées | 13 mois | S.O. |
| Référentiel d’objets de décision - Offres de secours | 13 mois | S.O. |
| Référentiel d’objets de décision - Emplacements | 13 mois | S.O. |
| Référentiel d’objets de décision - Activités | 13 mois | S.O. |
| ODE DecisionEvents - Décisions de production | 13 mois | S.O. |
| Jeu de données du service de consentement AJO | S.O. | 90 jours |
| Jeu de données de profil de messagerie interactive AJO | S.O. | 90 jours |
| Extension de compteurs de profils AJO | S.O. | 90 jours |
| Jeu de données de profil push AJO | S.O. | 90 jours |
| Jeu de données de profil AJO Engageable | S.O. | 90 jours |



## Questions fréquentes {#faq}

Vous trouverez ci-dessous une liste de réponses aux questions fréquentes sur la TLL des jeux de données.

+++Cette modification s’appliquera-t-elle uniquement aux sandbox de production ou s’appliquera-t-elle également aux sandbox de développement ?

Cette modification s’applique à tous les types de sandbox.

+++

+++Pour la durée de vie de 90 jours dans la banque de profils, les profils eux-mêmes sont-ils affectés ?

Les données du jeu de données généré par le système dans le profil sont ignorées au bout de 90 jours, et non pas les profils eux-mêmes.

+++

+++Si des données de jeu de données générées par le système sont transmises à [!DNL Customer Journey Analytics] (CJA), les données de CJA seront-elles également affectées par la TTL ?

Les données dans [!DNL Customer Journey Analytics] sont synchronisées avec Experience Platform. Par conséquent, une suppression de données en raison d’une durée de vie sur les données de jeu de données générées par le système aura également un impact sur les données en [!DNL Customer Journey Analytics].

+++

+++ Les clients peuvent-ils augmenter la durée de vie des données [!DNL Journey Optimizer] jeu de données système dans la banque de profils ?

Les extensions de TTL ne sont actuellement pas prises en charge. Cependant, des travaux sont prévus pour optimiser le processus de TTL afin de permettre ces demandes d’extension à partir de la fin du semestre 2025.

>[!NOTE]
>
>Les données stockées dans le profil sont soumises au droit Total du volume de données . Par conséquent, toute augmentation du stockage de données sur le profil suite à une extension de TTL est comptabilisée dans les droits relatifs au volume total de données. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html){target="_blank}

+++

+++Les clients peuvent-ils augmenter la durée de vie des données [!DNL Journey Optimizer] jeu de données système dans le lac de données ?

Les extensions de TTL ne sont actuellement pas prises en charge. Les clients disposant de droits Real-Time CDP peuvent exporter des données via Destinations pour conserver les données plus longtemps. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=fr){target="_blank}

+++

+++Les TTL auront-elles une incidence sur les fonctionnalités suivantes ?

* **Recherche de magasin** : non
* Limitation de Parcours **** : non
* **Limitation de l’offre** : non
* **Optimisation de l’heure d’envoi (STO)** : non
* **Capping de la fréquence des messages** (c’est-à-dire règles métier) : non
* **Reporting** : Non

  >[!NOTE]
  >
  >Une TTL est déjà implémentée sur la connexion [!DNL Customer Journey Analytics] (CJA), ce qui réduit la période de recherche en amont maximale effective des données du jeu de données concerné à 13 mois.

* **Source de données Experience Platform** : oui - la récupération de l’événement d’expérience est soumise à la durée de vie de 90 jours.
* **Attributs calculés** : oui - le calcul du renvoi initial sera limité aux 90 derniers jours de données ; l’attribut calculé sera mis à jour en fonction des événements incrémentiels pour les mises à jour ultérieures. Dès que les mises à jour suivantes atteignent la période d’analyse (6 mois max.), la TTL n’affecte pratiquement plus l’attribut calculé. En savoir plus.
* **Segmentation et reciblage** : Oui - la segmentation dépend des données de la banque de profils. Par conséquent, l’analyse a été limitée à 90 jours sur les données des jeux de données affectés.
* **Suivi** : oui - réduit la période de recherche en amont maximale effective des données du jeu de données concerné à 90 jours. Les données des jeux de données affectés résident pendant 13 mois dans le lac de données.

+++

+++Quel horodatage est utilisé pour l’application de la durée de vie (par exemple, pour les cas d’utilisation de renvoi) ?

La date et l’heure de l’événement sont utilisées (c’est-à-dire, pas la date d’ingestion).

+++
