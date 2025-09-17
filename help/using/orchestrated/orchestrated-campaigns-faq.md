---
solution: Journey Optimizer
product: journey optimizer
title: Questions fréquentes sur les campagnes orchestrées
description: Questions fréquentes sur les campagnes orchestrées Journey Optimizer
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: f82e725b58dbb2fdea70455a203d83b13b0e4a2b
workflow-type: tm+mt
source-wordcount: '1419'
ht-degree: 14%

---

# Questions fréquentes {#faq-oc}

Vous trouverez ci-dessous les questions fréquentes sur les campagnes orchestrées Adobe Journey Optimizer.

Vous avez besoin de plus d’informations ? Utilisez les options de commentaires au bas de cette page pour poser votre question ou contacter la communauté [Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=en){target="_blank"}.

+++ Qu’est-ce que l’orchestration des campagnes ?

L’orchestration des campagnes est une fonctionnalité de Journey Optimizer qui prend en charge les workflows en une ou plusieurs étapes qui utilisent le magasin de données relationnelles pour créer et segmenter les audiences dans le but d’un engagement par lots.

Journey Optimizer intègre un nouveau type de campagnes : **Campagnes orchestrées**. Les campagnes orchestrées aident les marques à exécuter des campagnes marketing complexes de type « un à plusieurs » à grande échelle. Elles sont conçues pour l’engagement initié par la marque, tel que les promotions, les campagnes saisonnières ou les communications basées sur un compte.

Par rapport aux campagnes à envoi unique/action, elles apportent l’**orchestration et le séquencement** au marketing sortant : les audiences passent par un workflow à plusieurs étapes ensemble, plutôt que de recevoir une seule opération.

+++

+++ Que puis-je faire avec une campagne orchestrée ?

Les fonctionnalités principales sont les suivantes :

* **Audiences à la demande** : créez et affinez instantanément des groupes cibles à l’aide de requêtes relationnelles.
* **Segmentation d’entités multiples** : créez des audiences précises en connectant les données client à des entités associées (par exemple, comptes, achats, réservations).
* **Visibilité avant l’envoi** : obtenez une évaluation précise de la taille des audiences avant le lancement pour optimiser le ciblage.
* **Workflows à plusieurs étapes** : exécutez des campagnes séquencées telles que des promotions saisonnières, des lancements de produits ou des offres de fidélité.

**Bonnes pratiques**

* Définissez un **objectif de campagne clair** avant de concevoir des workflows.
* Commencez avec une **audience pilote** pour valider les nombres et la logique avant la mise à l’échelle.
* Conservez des règles de segmentation **aussi simples que possible** pour optimiser les performances et la transparence.
* Utilisez des **conventions de nommage cohérentes** pour les audiences et les campagnes afin de faciliter la gestion.

+++

+++ Comment accéder à l&#39;orchestration des campagnes ?

Pour accéder à l’orchestration de campagne, votre licence doit inclure le package **Journey Optimizer - Campagnes et parcours** ou **Journey Optimizer - Campagnes**. Contactez votre représentant ou représentante Adobe pour confirmer votre licence et effectuer une mise à jour si nécessaire.

En savoir plus sur le modèle de licence d&#39;orchestration de Campaign dans la description du produit [Adobe Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

+++

+++ En quoi les campagnes orchestrées sont-elles différentes des Parcours ?

* **Campagnes orchestrées** : idéal pour les campagnes **par lots, de type « un à plusieurs »**. Les audiences progressent en bloc, selon un planning.
* **Parcours** : parfaits pour l’engagement **en temps réel, de type « un-à-plusieurs »**. Chaque client ou cliente suit le parcours à son propre rythme, déclenché par un comportement ou des événements.

**Bonne pratique** : utilisez-les ensemble : Parcours pour les expériences déclenchées et réactives, et campagnes orchestrées pour les initiatives planifiées basées sur un calendrier.


+++

+++ Qu’est-ce que la segmentation d’entités multiples ?

Dans Adobe Journey Optimizer, l’orchestration de Campaign utilise une base de données relationnelle. Ce type de modèle de données comporte des schémas de données distincts connectés par le biais de relations 1:1 ou 1:many. Cela permet aux utilisateurs et utilisatrices de démarrer une requête sur n’importe quel schéma, pas seulement au niveau du destinataire, puis de basculer entre les schémas associés, tels que les achats, les produits, les réservations ou les détails du destinataire, offrant ainsi une grande flexibilité dans la manière dont les segments et les audiences peuvent être créés et
raffiné.


**Exemple** - Ciblez tous les destinataires dont les abonnements expirent au cours des 30 prochains jours. Dans Campaign Orchestration, la requête peut commencer par le schéma Abonnements , rechercher uniquement la colonne Date d’expiration de ce schéma et renvoyer tous les abonnements dont l’expiration est prévue, puis cumuler les données des destinataires liées à ces identifiants d’abonnements spécifiques et renvoyer les résultats plus rapidement et plus efficacement que les modèles de données qui lancent chaque requête au niveau du destinataire.

+++

+++ Comment fonctionne le modèle de données ?

Les campagnes utilisent une **base de données relationnelle**. Vous pouvez ainsi interroger différents jeux de données (par exemple, clients, produits, abonnements) et les connecter de manière flexible pour une segmentation avancée.

**Bonnes pratiques**

* Organisez les jeux de données de sorte que les **relations (jointures)** reflètent la logique commerciale.
* Évitez les jointures inutiles pour maintenir les performances des requêtes.
* Validez les exemples de résultats avant d’exécuter des extractions à grande échelle.


+++

+++ Puis-je personnaliser les messages avec des données relationnelles ?

Oui. Dans Campaign Orchestration, un profil de destinataire appelé « Entité de personnes » peut être mis à jour et ces données sont utilisées pour la personnalisation. En outre, les données enrichies des entités liées dans la base de données relationnelle peuvent également être utilisées pour la personnalisation. Vous pouvez utiliser les profils client ainsi que les données liées (comme les achats ou les abonnements) pour personnaliser le contenu sur tous les canaux pris en charge.


**Recommandations**

* Utilisez des **données transactionnelles et comportementales** pour rendre les offres pertinentes.
* Combinez les **attributs statiques** (par exemple, le niveau de fidélité) avec les **attributs dynamiques** (par exemple, la date de dernier achat).
* Personnalisation concise : surcharger les messages avec des données peut nuire à la lisibilité.


+++

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  -->

+++ Quels canaux sont pris en charge ?

Vous pouvez créer des campagnes orchestrées pour envoyer des **e-mails**, **SMS** et **notifications push**.

+++

+++ Est-il possible de lancer plusieurs communications et différents canaux au sein d’une même campagne orchestrée ?

Oui, les campagnes orchestrées prennent en charge l’orchestration cross-canal.

+++

+++ Les modèles de campagne orchestrée sont-ils disponibles ?

Non, vous ne pouvez pas définir ni utiliser de modèles de campagne, mais vous pouvez utiliser des modèles de contenu pour vos communications.

+++

+++ Le concepteur de contenu pour les messages est-il spécifique aux campagnes orchestrées ?

Non, le concepteur de contenu, y compris le Designer Email, est commun à toutes les fonctionnalités de Journey Optimizer.

+++

+++ Comment les différents canaux sont-ils connectés dans les campagnes orchestrées ?

Le composant de canal et l’exécution sont communs à toutes les campagnes Journey Optimizer, mais les canaux pris en charge diffèrent.

+++


+++ Les campagnes orchestrées peuvent-elles se connecter aux canaux sortants (web, inApp) ?

Non, les canaux sortants ne sont pas pris en charge dans les campagnes orchestrées.

+++

+++ Qu’en est-il des autorisations et du consentement ?

Les autorisations et le consentement pour les campagnes et les parcours orchestrés sont gérés de manière centralisée dans Adobe Experience Platform. Ces paramètres sont appliqués aux deux solutions pour chaque destinataire avant l’envoi.


**Bonnes pratiques**

* Appliquez la **gouvernance centralisée** évitez de gérer le consentement séparément au niveau de la campagne.
* Contrôlez régulièrement les données de consentement pour détecter les incohérences.
* Respectez les **désinscriptions spécifiques à un canal** — ne supposez pas que le consentement global couvre tous les canaux.

+++


+++ Puis-je effectuer une segmentation ad hoc dans les campagnes orchestrées ?

Dans l’orchestration de Campaign, nous appelons la segmentation ad hoc « segmentation en direct », où vous pouvez accéder à toutes les données disponibles dans la boutique relationnelle en temps réel, créer une requête complexe par-dessus et obtenir le résultat pour une activation instantanée via les canaux sortants (par exemple : e-mail + SMS).


**Conseils**

* Utilisez la segmentation ad hoc pour les **besoins urgents** (par exemple, les promotions Flash).
* Enregistrez et documentez les requêtes utiles afin qu’elles puissent être réutilisées dans les prochaines campagnes.
* Validez le nombre d’audiences avant l’activation pour éviter un envoi insuffisant ou excessif.

+++


+++ L’orchestration de Campaign accède-t-elle uniquement aux données chargées par lots ou peut-elle également interroger des tables mises à jour en temps réel (telles que les données Analytics) ?

L’orchestration de Journey Optimizer Campaign peut d’abord créer des requêtes ad hoc sur des schémas relationnels. Pour l’instant, les schémas relationnels ne prennent en charge que les sources par lots. En outre, il prend en charge la lecture d’audience à partir de n’importe quel type d’audience Adobe Experience Platform.

+++

+++ Les campagnes orchestrées prennent-elles en charge la prise de décision ?

Oui. Decisioning peut utiliser des données relationnelles provenant de campagnes orchestrées. Une fois le schéma relationnel connecté aux schémas XDM, les données XDM peuvent être utilisées dans la prise de décision.

+++


+++ Comment fonctionne le déploiement dans les environnements ?

Les objets créés dans des campagnes orchestrées (audiences, workflows, etc.) sont liés au sandbox dans lequel ils sont créés. Les workflows de package et de déploiement standard dans les environnements (de développement, d’évaluation et de production) ne sont actuellement pas disponibles pour les campagnes orchestrées.

**Bonnes pratiques**

* Conservez les **sandbox distincts** pour l’expérimentation, l’assurance qualité et la production.
* Documentez minutieusement les configurations pour activer la réplication manuelle si nécessaire.
* Alignez-vous sur les équipes de gouvernance pour réduire la dérive de configuration entre les environnements.

+++

<!--
## Are there recommended practices for running campaigns at scale? {#scale}

Yes, follow the best practices below:  

* **Plan campaigns around business calendars** (product launches, seasonal peaks) to align volume and resources.  
* Use **audience pre-views** before sending to confirm the expected size and avoid surprises.  
* Where possible, **stagger send times** to avoid overwhelming downstream systems (e.g., call centers, websites).  
* Establish a **monitoring routine**—track delivery logs, error rates, and opt-outs after each send.  
* Run **post-campaign analysis** in Customer Journey Analytics to refine targeting and orchestration for the next cycle.  
-->

+++ Quelle est la relation entre les entités destinataire et profil ?

La segmentation est effectuée sur les destinataires lors de l’envoi de messages par rapport au profil Adobe Experience Platform. La dimension cible du destinataire étend le profil unifié avec des données supplémentaires utilisées pour la segmentation dans les campagnes orchestrées, tandis que le destinataire est réconcilié avec le profil à l’exécution pour l’envoi des messages et la vérification de la politique de consentement et des règles métier. Cette réconciliation est utile pour unifier les règles métier et l’application du consentement au niveau du profil

![](assets/recipients-and-profiles.png)

+++

+++ Dans quels cas est-il recommandé d’utiliser Destinataire ou Entités de profil ?

Répondre « Oui » suggère la meilleure banque de données. Cependant, confirmez toujours la meilleure approche en fonction de votre cas d’utilisation et des contraintes avec votre représentant Adobe.

| Magasin relationnel | Profil client en temps réel |
|---------|----------|
| La source est-elle déjà relationnelle ? | La source de la diffusion des données en continu est-elle ? |
| Prévoyez-vous d’ingérer les données en l’état pour les cas d’utilisation marketing ? | La fraîcheur des données est-elle une exigence majeure ? |
| Un grand volume de données historiques (`>` 2 mois) est-il nécessaire pour les cas d’utilisation de l’activation marketing ? | Existe-t-il des scénarios dans lesquels une action ou une décision à un moment donné nécessite des données ? |
| Existe-t-il des besoins ad hoc pour la création, l’évaluation et l’activation d’audiences ? | Les données comportementales peuvent-elles être limitées à `<` 90 jours à l’aide d’agrégats précalculés ? |
|  | Les données sont-elles nécessaires pour personnaliser les messages en temps réel ? |

+++

+++ Quel est le nombre maximal d’activités par campagne orchestrée ?

Le nombre d’activités d’une campagne orchestrée est limité à 500.

+++

+++ Est-il possible d’effectuer des enrichissements pour ajouter des données supplémentaires ?

Oui, vous pouvez enrichir les données du magasin relationnel et des audiences Adobe Experience Platform.

+++

+++ Tous les filtres doivent-ils être définis via les audiences ou un type de filtre particulier peut-il être configuré ?

Les campagnes orchestrées prennent en charge les filtres prédéfinis : vous pouvez définir et enregistrer une requête en tant que filtre, puis l’ajouter à vos favoris pour la réutiliser dans d’autres tâches de segmentation.

+++




>[!MORELIKETHIS]
>
>* [Mécanismes de sécurisation et limitations des campagnes orchestrées](../orchestrated/guardrails.md)
>* [Prise en main des schémas et des jeux de données dans les campagnes orchestrées](../orchestrated/gs-schemas.md)
>* [Créer votre première campagne orchestrée](../orchestrated/gs-campaign-creation.md)
>* Description du produit [Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
