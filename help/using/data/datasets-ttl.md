---
solution: Journey Optimizer
product: journey optimizer
title: À propos des mécanismes de sécurisation de la durée de vie (TTL) des jeux de données
description: Mécanismes de sécurisation de la durée de vie des jeux de données dans  [!DNL Adobe Journey Optimizer]
feature: Data Model, Datasets, Data Management
role: Developer, Admin
level: Experienced
keywords: platform, lac de données, créer, lac, jeux de données, profil
exl-id: 08633a79-5601-4e36-b8cf-080234956d99
source-git-commit: 6233fcb466e741fd7eb912e6c59c8daf030f71a0
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 67%

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
| Jeu de données d’événement d’entité | 13 mois | S.O. |
| Parcours | 13 mois | S.O. |
| Événements d’étape de parcours | 13 mois | S.O. |
| Référentiel d’objets de décision - Offres personnalisées | 13 mois | S.O. |
| Référentiel d’objets de décision - Offres de secours | 13 mois | S.O. |
| Référentiel d’objets de décision - Emplacements | 13 mois | S.O. |
| Référentiel d’objets de décision - Activités | 13 mois | S.O. |
| Référentiel d’objets de décisions pour les expériences - Éléments d’offres personnalisées | 13 mois | S.O. |
| ODE DecisionEvents - Décisions de production | 13 mois | S.O. |

## Questions fréquentes {#faq}

Vous trouverez ci-dessous les questions fréquentes sur la durée de vie (TTL) de jeux de données.

Vous avez besoin de plus d’informations ? Utilisez les options de commentaires au bas de cette page pour poser votre question ou contacter la [communauté Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=fr){target="_blank"}.

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
>Les données stockées dans le profil sont soumises aux droits relatifs au volume total de données. Par conséquent, toute augmentation du stockage de données sur le profil suite à une extension de la durée de vie est comptabilisée dans les droits relatifs au volume total de données. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/landing/license/total-data-volume.html?lang=fr){target=_blank}

+++

+++La clientèle peut-elle augmenter la durée de vie des données du jeu de données système de [!DNL Journey Optimizer] dans le lac de données ? 

Les extensions de la durée de vie ne sont actuellement pas prises en charge. Les clientes et clients peuvent exporter des données via les destinations pour conserver les données plus longtemps. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=fr){target=_blank} En outre, les clientes et clients disposant de droits **[!DNL Data Distiller]** peuvent créer des jeux de données dérivés pour stocker les données dans le lac de données sans TTL. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/query/data-distiller/derived-datasets/overview){target=_blank}

+++

+++Les durées de vie auront-elles une incidence sur les fonctionnalités suivantes ? 

* **Recherche dans une banque** : non
* **Limitation de parcours** : non
* **Limitation d’offre** : non
* **Optimisation de l’heure d’envoi (STO)** : non
* **Capping de la fréquence des messages** (règles métier) : non
* **Reporting** : non

  >[!NOTE]
  >
  >Une durée de vie est déjà implémentée sur la connexion [!DNL Customer Journey Analytics] (CJA), ce qui réduit à 13 mois la période de recherche en amont maximale effective des données du jeu de données concerné.

* **Source de données Experience Platform** : sans objet - La récupération des événements d’expérience n’est pas prise en charge via les sources de données.
* **Attributs calculés** : oui - le calcul du renvoi initial sera limité aux 90 derniers jours de données ; l’attribut calculé sera mis à jour en fonction des événements incrémentiels pour les mises à jour ultérieures. Dès que les mises à jour suivantes atteignent la période de recherche en amont (6 mois max.), la durée de vie n’affecte pratiquement plus l’attribut calculé. En savoir plus.
* **Segmentation et reciblage** : oui - la segmentation dépend des données de la banque de profils. Par conséquent, la recherche en amont a été limitée à 90 jours sur les données des jeux de données affectés.
* **Suivi** : oui - réduit à 90 jours la période de recherche en amont maximale effective des données du jeu de données concerné. Les données des jeux de données affectés résident pendant 13 mois dans le lac de données.

+++

+++Quelles dates est heures sont utilisées pour l’application de la durée de vie (par exemple, pour les cas d’utilisation de renvoi) ? 

La date et l’heure de l’événement sont utilisées (et non la date d’ingestion).

+++

+++Comment la nouvelle durée de vie affecte-t-elle les cas d’utilisation qui nécessitent une conservation des données plus longue (par exemple, en excluant les profils qui ont reçu un e-mail au cours des 120 derniers jours ou en limitant les e-mails sur un an) ?

La nouvelle politique de durée de vie limite la période de recherche en amont des données de jeux de données générés par le système dans la banque de profils à 90 jours et dans le lac de données à 13 mois. Les cas d’utilisation qui nécessitent l’accès aux données au-delà de ces périodes seront affectés. Par exemple, la segmentation de l’audience ou le capping de la fréquence en fonction des événements de plus de 90 jours dans la banque de profils ne sera plus possible à l’aide des jeux de données système.

+++

+++Quelles sont les alternatives disponibles pour conserver les données plus longtemps que la durée de vie ?

Les clients qui nécessitent une rétention plus longue doivent envisager d’exporter les données pertinentes des jeux de données AJO vers un stockage externe avant l’expiration de la durée de vie. Adobe Journey Optimizer prend en charge l’exportation de jeux de données vers diverses destinations d’espace de stockage (Amazon S3, Azure Blob, Google Cloud Storage, etc.). [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=fr){target=_blank}

+++

+++Que doivent faire les clients pour se préparer au changement de durée de vie ?

* Passez en revue vos cas d’utilisation et identifiez ceux qui nécessitent une conservation des données au-delà des nouvelles TTL.
* Configurez des requêtes automatisées pour copier des données critiques vers des jeux de données dérivés avant que les données ne soient supprimées.
* Contactez votre représentant Adobe pour discuter des besoins supplémentaires ou des extensions de durée de vie potentielles (prévues pour les prochaines versions).

+++

+++Les clients seront-ils avertis avant l’application de la TTL sur les sandbox existants ?

Oui, les clients concernés seront avertis à l’avance et l’équipe produit travaillera avec eux pour assurer une transition fluide.

+++Puis-je supprimer des jeux de données générés par le système Journey Optimizer ?

Les jeux de données générés par le système Journey Optimizer sont protégés et ne peuvent pas être supprimés via l’interface utilisateur Adobe Experience Platform standard. Ces jeux de données sont essentiels aux fonctionnalités de Journey Optimizer et sont gérés par le système.

Si vous devez supprimer définitivement un jeu de données système Journey Optimizer (par exemple, pour les environnements d’assurance qualité, le nettoyage des sandbox ou des exigences spécifiques en matière d’hygiène des données), contactez l’ingénierie Adobe ou l’assistance clientèle Adobe. Ces jeux de données nécessitent des procédures d’arrière-plan spécialisées pour garantir une suppression complète et sécurisée.

>[!NOTE]
>
>Pour le nettoyage de routine des données de ces jeux de données système, utilisez les opérations **[!UICONTROL Cycle de vie des données]** disponibles via Privacy Service pour supprimer des enregistrements ou des identités spécifiques. [En savoir plus](../privacy/data-hygiene.md)


+++
