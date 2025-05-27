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
source-git-commit: b27ddcc88ca4b4209c9d29974a0b0d0dbe98cc94
workflow-type: ht
source-wordcount: '678'
ht-degree: 100%

---

# Mécanismes de sécurisation de la durée de vie (TTL) des jeux de données {#ttl-guardrail}

Depuis février 2025, un mécanisme de sécurisation de la durée de vie (TTL) est déployé dans les jeux de données générés par le système Journey Optimizer dans **les nouveaux sandbox et les nouvelles organisations** comme suit :

* 90 jours pour les données dans la banque de profils
* 13 mois pour les données du lac de données

Cette modification sera déployée sur les **sandbox client existants** dans une phase ultérieure.

## Jeux de données affectés {#datasets}

Le tableau ci-dessous répertorie tous les jeux de données affectés et leur durée de vie respective dans le lac de données et la banque de profils.

| Jeu de données | Durée de vie du lac de données | Durée de vie de la banque de profils |
|------|-----|-----|
| Jeu de données d’événement de retour sur les messages AJO | 13 mois | 90 jours |
| Jeu de données d’événement d’expérience de tracking d’e-mail AJO | 13 mois | 90 jours |
| Jeu de données d’événement d’expérience de tracking de notifications push AJO | 13 mois | 90 jours |
| Jeu de données d’entité AJO | 13 mois | 90 jours |
| Jeu de données de surfaces AJO | 13 mois | S.O. |
| Jeu de données d’événement d’activité entrante AJO | 13 mois | 90 jours |
| Jeu de données de classification AJO | 13 mois | S.O. |
| Jeu de données d’événement de retour des e-mails en Cci AJO | 13 mois | S.O. |
| Jeu de données d’événement acpEntity | 13 mois | S.O. |
| Parcours | 13 mois | S.O. |
| Événements d’étape de parcours | 13 mois | S.O. |
| Référentiel d’objets de décision - Offres personnalisées | 13 mois | S.O. |
| Référentiel d’objets de décision - Offres de secours | 13 mois | S.O. |
| Référentiel d’objets de décision - Emplacements | 13 mois | S.O. |
| Référentiel d’objets de décision - Activités | 13 mois | S.O. |
| ODE DecisionEvents - Décisions de production | 13 mois | S.O. |

## Questions fréquentes {#faq}

Voici une liste de réponses aux questions fréquentes sur la durée de vie des jeux de données.

+++Cette modification s’appliquera-t-elle uniquement aux sandbox de production ou s’appliquera-t-elle également aux sandbox de développement ?

Cette modification s’applique à tous les types de sandbox.

+++

+++Pour la durée de vie de 90 jours dans la banque de profils, les profils eux-mêmes sont-ils affectés ?

Les données du jeu de données généré par le système dans le profil sont ignorées au bout de 90 jours, et non pas les profils eux-mêmes.

+++

+++Si les données d’un jeu de données généré par le système sont transmises à [!DNL Customer Journey Analytics] (CJA), les données de CJA seront-elles également affectées par la durée de vie ?

Les données de [!DNL Customer Journey Analytics] restent synchronisées avec Experience Platform. Par conséquent, la suppression de données en raison d’une durée de vie sur les données de jeu de données généré par le système aura également un impact sur les données dans [!DNL Customer Journey Analytics].

+++

+++ La clientèle peut-elle augmenter la durée de vie des données du jeu de données système de [!DNL Journey Optimizer] dans la banque de profils ?

Les extensions de la durée de vie ne sont actuellement pas prises en charge. Cependant, il est prévu d’optimiser le processus de durée de vie afin de permettre ces demandes d’extension à partir de la seconde moitié de 2025.

>[!NOTE]
>
>Les données stockées dans le profil sont soumises aux droits relatifs au volume total de données. Par conséquent, toute augmentation du stockage de données sur le profil suite à une extension de la durée de vie est comptabilisée dans les droits relatifs au volume total de données. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html?lang=fr){target=&quot;_blank}

+++

+++La clientèle peut-elle augmenter la durée de vie des données du jeu de données système de [!DNL Journey Optimizer] dans le lac de données ?

Les extensions de la durée de vie ne sont actuellement pas prises en charge. Les clientes et clients peuvent exporter des données via les destinations pour conserver les données plus longtemps. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=fr){target=&quot;_blank} En outre, les clientes et clients disposant de droits **[!DNL Data Distiller]** peuvent créer des jeux de données dérivés pour stocker les données dans le lac de données sans TTL. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=&quot;_blank}

+++

+++Les dures de vie auront-elles une incidence sur les fonctionnalités suivantes ?

* **Recherche dans une banque** : non
* **Limitation de parcours** : non
* **Limitation d’offre** : non
* **Optimisation de l’heure d’envoi (STO)** : non
* **Capping de la fréquence des messages** (règles métier) : non
* **Reporting** : non

  >[!NOTE]
  >
  >Une durée de vie est déjà implémentée sur la connexion [!DNL Customer Journey Analytics] (CJA), ce qui réduit à 13 mois la période de recherche en amont maximale effective des données du jeu de données concerné.

* **Source de données Experience Platform** : oui - la récupération de l’événement d’expérience est soumise à la durée de vie de 90 jours.
* **Attributs calculés** : oui - le calcul du renvoi initial sera limité aux 90 derniers jours de données ; l’attribut calculé sera mis à jour en fonction des événements incrémentiels pour les mises à jour ultérieures. Dès que les mises à jour suivantes atteignent la période de recherche en amont (6 mois max.), la durée de vie n’affecte pratiquement plus l’attribut calculé. En savoir plus.
* **Segmentation et reciblage** : oui - la segmentation dépend des données de la banque de profils. Par conséquent, la recherche en amont a été limitée à 90 jours sur les données des jeux de données affectés.
* **Suivi** : oui - réduit à 90 jours la période de recherche en amont maximale effective des données du jeu de données concerné. Les données des jeux de données affectés résident pendant 13 mois dans le lac de données.

+++

+++Quel horodatage est utilisé pour l’application de la durée de vie (par exemple, pour les cas d’utilisation de renvoi) ?

La date et l’heure de l’événement sont utilisées (et non la date d’ingestion).

+++
