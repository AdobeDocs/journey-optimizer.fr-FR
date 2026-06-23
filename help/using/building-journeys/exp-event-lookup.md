---
solution: Journey Optimizer
product: journey optimizer
title: Recherche d’événements d’expérience dans les parcours
description: Découvrez comment utiliser la recherche d’événements d’expérience dans les parcours.
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/kVO36LmCfr9cYVq3EHRy8OpqPCZDq20mXTEA49TIRTI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: e23d48b5-7858-4d45-9c56-9e2b4be8500eid: fa683eda-48de-4558-af32-2673edcd44fe
topic_v2: id: c4147b6e-073b-4d3c-9ab1-d60f2f4434efid: e0eb8757-182f-49f3-94a4-1587d16f5094id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1717
ht-degree: 50%

---

# Recherche d’événements d’expérience dans les parcours {#ee-journeys}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez des modèles et des bonnes pratiques évolutifs pour l’utilisation d’événements d’expérience dans les parcours afin de supprimer, de qualifier ou de personnaliser les profils en fonction de leur comportement et de leurs attributs d’événement.

>[!ENDSHADEBOX]

>[!CAUTION]
>
>À compter du 8 juillet 2025, dans les nouvelles organisations clientes, la création d’expressions à l’aide d’événements d’expérience n’est plus prise en charge dans l’éditeur d’expression utilisé dans les conditions de parcours. Par conséquent, les événements d’expérience dans la [source de données Experience Platform](../datasource/adobe-experience-platform-data-source.md) ne peuvent pas être utilisés pour créer des expressions.
>
>À compter du 1er avril 2026, l’utilisation des attributs d’événement d’expérience dans les expressions de parcours ne sera plus prise en charge pour les organisations qui n’ont pas utilisé cette fonctionnalité au cours des 90 derniers jours. Les autres approches et bonnes pratiques pour créer des expressions/logiques avec des événements d’expérience sont référencées ci-dessous.
>
>Vous avez besoin de plus d’informations ? [Consultez les questions fréquentes](#faq-ee).

Cette page décrit les modèles courants et les approches évolutives pour vous aider à tirer le meilleur parti des événements d’expérience dans [!DNL Adobe Journey Optimizer]. Ces cas d’utilisation ont été conçus pour vous aider à résoudre les défis courants tels que la gestion des opt-outs, le contrôle de la fréquence des messages, la personnalisation du contenu en fonction du comportement des utilisateurs et des utilisatrices et la réaction aux signaux en temps réel.

En utilisant ces stratégies, vous pouvez transformer des données comportementales en actions significatives, à savoir la suppression, la qualification ou l’exclusion de profils en fonction des événements qu’ils déclenchent ou des attributs qu’ils possèdent. Que vous élaboriez une logique pour les seuils d’achat, les déclencheurs d’abandon ou la gestion des rebonds, ces exemples vous fournissent des conseils pratiques que vous pouvez adapter à vos besoins.

Lorsque vous évaluez quelle approche serait la plus adaptée, tenez compte des exigences de latence de votre cas d’utilisation pour vous assurer que vos parcours restent réactifs et efficaces.

## Suppression des opt-outs

Pour supprimer les profils qui se sont désinscrits des communications marketing, utilisez la gestion du consentement intégrée. Les préférences d’opt-out sont automatiquement capturées dans les champs de consentement du profil. Elles peuvent être référencées directement dans des conditions de parcours et sont automatiquement appliquées par Journey Optimizer lors de la diffusion des messages.

En savoir plus :

* [Gérer le consentement](../privacy/opt-out.md)
* [Gestion des opt-outs pour les e-mails](../email/email-opt-out.md)
* [Gestion du processus d’opt-out pour les messages mobiles](../mobile/mobile-opt-out.md)


## Suppression basée sur les rebonds

Pour exclure les profils qui ont subi des rebonds d’e-mails, utilisez la liste de suppression automatique de [!DNL Adobe Journey Optimizer] pour les adresses qui ont fait l’objet de rebonds. Ce mécanisme intégré garantit que les e-mails non valides ou inatteignables sont exclus des envois futurs sans nécessiter de logique personnalisée.

En savoir plus :

* [Gérer la liste de suppression](../configuration/manage-suppression-list.md)


## Suppression générique

Pour supprimer des profils qui ont manifesté des comportements spécifiques, utilisez des audiences par lots avec une logique basée sur les événements afin de capturer les profils qui correspondent aux critères de suppression. Référencez cette audience dans les conditions de parcours.

En savoir plus :

* [!DNL Adobe Experience Platform] [Créateur de segments - Événements](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Créateur de segments - Contraintes de temps](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utiliser des audiences dans des conditions](../building-journeys/conditions.md#using-a-segment)

* [Fonction inAudience()](../building-journeys/functions/functioninaudience.md)


## Exclusion basée sur des communications reçues

Pour empêcher l’envoi de messages aux profils qui ont reçu des communications au cours d’une période récente :

* Utilisez des audiences par lots avec des critères temporels et référencez ces audiences dans les conditions de parcours.
* Appliquez des règles métier de capping de la fréquence pour appliquer des limites de messages quotidiennes ou hebdomadaires.


En savoir plus sur l’utilisation des audiences :

* [!DNL Adobe Experience Platform] [Créateur de segments - Événements](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Créateur de segments - Contraintes de temps](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utiliser des audiences dans des conditions](../building-journeys/conditions.md#using-a-segment)

* [Fonction inAudience()](../building-journeys/functions/functioninaudience.md)


Voir également :

* [Capping de la fréquence par canal et type de communication](../conflict-prioritization/channel-capping.md)



## Inclusion/exclusion spécifique à un message

Pour inclure ou exclure des profils en fonction d’un message reçu spécifique, créez des audiences par lots qui encapsulent cette logique et référencez-les dans les conditions de parcours.


En savoir plus :

* [!DNL Adobe Experience Platform] [Créateur de segments - Événements](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Créateur de segments - Contraintes de temps](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utiliser des audiences dans des conditions](../building-journeys/conditions.md#using-a-segment)

* [Fonction inAudience()](../building-journeys/functions/functioninaudience.md)

## Personnalisation de l’abandon du panier ou de la navigation

Pour personnaliser les communications en fonction des derniers événements liés au panier ou à la navigation sur plusieurs types de panier ou consultations de produits :

* Si vous avez accès à [[!DNL Adobe Experience Platform] Data Distiller](https://experienceleague.adobe.com/fr/docs/experience-platform/query/data-distiller/overview){target="_blank"}, configurez des requêtes automatisées pour extraire les données requises de l’événement, les manipuler pour les adapter au cas d’utilisation et les réécrire dans un [jeu de données activé pour profile](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} pour activation.
* Si les données d’abandon peuvent être modélisées sur le profil avec des attributs scalaires, envisagez d’utiliser des attributs calculés pour capturer les dernières informations, puis de référencer ces attributs dans le parcours pour créer la communication. [En savoir plus dans  [!DNL Adobe Experience Platform]  documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}


## Sortie du parcours basée sur le comportement

Pour supprimer un profil du parcours lorsqu’il présente un comportement particulier, utilisez les critères de sortie afin de retirer le profil du parcours lorsqu’un événement particulier est reçu ou que le profil se qualifie pour une audience spécifique.

En savoir plus :

* [Définir vos propriétés de parcours - Critères de sortie](journey-properties.md#exit-criteria)

## Qualification basée sur l’achat avec seuils de valeur

Pour déclencher des parcours en fonction des achats et procéder à une suppression si la valeur est supérieure ou inférieure à un seuil, définissez des attributs calculés pour additionner les achats sur une période spécifique. Créez une audience qui comprend des profils dont le montant des dépenses répond à des critères spécifiques.

En savoir plus :

* [!DNL Adobe Experience Platform] [Présentation des attributs calculés](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## Questions fréquentes {#faq-ee}

Cette FAQ se concentre sur la chronologie du retrait de l’utilisation des événements d’expérience dans les expressions de parcours et sur les personnes affectées. Pour obtenir des conseils sur les autres approches, consultez les cas d’utilisation et les bonnes pratiques ci-dessus.

Vous avez besoin de plus d’informations ? Utilisez les options de commentaires au bas de cette page pour poser votre question ou contacter la [[!DNL Adobe Journey Optimizer] communauté](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=fr){target="_blank"}.

+++Quelles fonctionnalités spécifiques sont affectées ? 

Seule la recherche d’événements d’expérience dans l’éditeur d’expression est affectée. Les fonctionnalités suivantes **ne sont pas** affectées et restent les mêmes :

* Observation des événements d’expérience associés à un profil spécifique dans l’interface d’utilisation du profil

* Utilisation d’événements d’expérience dans des règles d’attributs calculés et accès aux attributs calculés dans un parcours

* Déclenchement d’un parcours via un événement unitaire ou un événement métier

* Utilisation des données contextuelles du parcours provenant des événements qui déclenchent le parcours dans les éditeurs d’expression et de personnalisation

* Écoute d’un événement dans un parcours

* Configuration des événements pour déclencher un parcours

* Détection des événements de réaction de l’utilisateur ou de l’utilisatrice aux communications marketing (par exemple, une ouverture d’e-mail)

+++

+++Mon organisation Adobe existante est-elle affectée par cette mise à jour ?

À compter du 8 juillet 2025, les nouvelles organisations clientes ne pourront plus créer d’expressions à l’aide d’attributs d’événement d’expérience. À compter du 1er avril 2026, les organisations qui n’ont pas accédé aux événements d’expérience par le biais d’expressions de parcours au cours des 90 derniers jours n’auront plus accès à cette fonctionnalité.

+++

+++J’ai une nouvelle organisation Adobe. Comment résoudre mon cas d’utilisation qui requiert des données d’événement d’expérience ? 

D’autres approches et bonnes pratiques concernant les événements d’expérience sont disponibles ci-dessus pour mener à bien les cas d’utilisation souhaités.

+++

+++ Que faire si les autres approches ne fonctionnent pas pour mon cas d’utilisation ?

Si votre cas d’utilisation ne peut pas être résolu à l’aide de l’une des autres approches répertoriées ci-dessus, contactez votre représentant ou représentante Adobe.

+++

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page présente d’autres modèles et bonnes pratiques pour l’utilisation des données d’événement d’expérience dans les parcours Adobe Journey Optimizer, dans le cadre de l’abandon de la recherche directe d’événement d’expérience dans l’éditeur d’expression de parcours.

**Intentions:**

* Supprimer les profils exclus à l’aide de la gestion de consentement intégrée au lieu des expressions d’événement d’expérience
* Exclure les adresses e-mail de rebond à l’aide de la liste de suppression automatique d’AJO
* Créer une logique de suppression générique à l’aide d’audiences par lots avec des critères basés sur un événement
* Prévenez la surcommunication en appliquant des règles de limitation de la fréquence ou des conditions d’audience basées sur le temps
* Personnaliser les communications abandonnées du panier ou parcourir à l’aide d’AEP Data Distiller ou d’attributs calculés

**Glossaire:**

* **Événement d’expérience** : enregistrement horodaté et non modifiable d’une action ou d’un comportement du client stocké dans Adobe Experience Platform *(spécifique au produit)*
* **Attribut calculé** : attribut au niveau du profil dérivé de l’agrégation ou de la synthèse des données d’événement d’expérience au fil du temps, disponible pour une utilisation dans des expressions de parcours *(spécifiques au produit)*
* **Liste de suppression** : liste intégrée d’AJO d’adresses e-mail automatiquement exclues des futurs envois en raison de hard bounces ou de plaintes contre le spam *(spécifiques au produit)*
* **Capping de la fréquence** : règle métier qui limite le nombre de messages qu’un profil peut recevoir au cours d’une période définie *(spécifique au produit)*
* Distiller de données **: fonctionnalité d’AEP qui permet aux requêtes par lots basées sur SQL d’extraire et de transformer des données d’événement en jeux de données activés pour le profil *(spécifiques au produit)***

**Mécanismes de sécurisation :**

* À compter du 8 juillet 2025, les nouvelles organisations clientes ne pourront plus créer d’expressions à l’aide d’attributs d’événement d’expérience dans l’éditeur d’expression de parcours.
* À compter du 1er avril 2026, les organisations qui n’ont pas utilisé d’attributs d’événement d’expérience dans les expressions de parcours au cours des 90 derniers jours perdront l’accès à cette fonctionnalité.
* La recherche directe d’événements d’expérience dans des conditions de parcours est en cours de suppression ; les alternatives incluent les audiences par lots, les attributs calculés et AEP Data Distiller.
* Les fonctionnalités NON affectées par la suppression sont les suivantes : déclenchement de parcours avec des événements, écoute des événements dans un parcours, utilisation des données contextuelles de parcours des événements de déclenchement, configuration des événements et détection des événements de réaction.

**Terminologie:**

* Nom canonique : recherche d’événement d’expérience — Acronyme : recherche EE — variantes : expressions d’événement d’expérience, recherche d’attribut d’événement
* Synonymes : « audience par lots avec logique basée sur un événement » = « segment basé sur un événement » comme mécanisme de suppression/d’inclusion
* Ne les confondez pas : « recherche d’événement d’expérience dans l’éditeur d’expression » ≠ « déclenchement d’un parcours avec un événement » - le déclenchement de parcours avec des événements n’est PAS retiré

**FAQ:**

* **Q : Puis-je toujours déclencher un parcours à l’aide d’un événement d’expérience ?** — Oui, le déclenchement de parcours avec des événements unitaires ou métier n’est pas affecté par cette modification.
* **Q : Quel est le remplacement recommandé pour la recherche d’événement d’expérience dans des conditions de parcours ?** utilisez des audiences par lots créées avec la logique d&#39;événement du créateur de segments d&#39;AEP, les attributs calculés ou AEP Data Distiller pour des transformations complexes.
* **Q : Mon organisation existante est-elle affectée en ce moment ?** — Les nouvelles organisations sont concernées à partir du 8 juillet 2025. Les organisations existantes ne sont affectées à compter du 1er avril 2026 que si elles n’ont pas utilisé la fonctionnalité au cours des 90 derniers jours.
* **Q : Comment gérer la personnalisation d’abandon de panier sans recherche directe d’événement ?** — Utilisez AEP Data Distiller pour extraire et écrire des données d&#39;événement dans un jeu de données activé pour un profil, ou utilisez les attributs calculés pour capturer le dernier état d&#39;abandon sur le profil.
* **Q : Quelles fonctionnalités ne sont PAS affectées par cette obsolescence ?** : le déclenchement de parcours avec événements, l&#39;écoute d&#39;événements dans les parcours, l&#39;utilisation de données contextuelles d&#39;événement dans les expressions, la configuration d&#39;événements et la détection d&#39;événements de réaction (par exemple, les ouvertures d&#39;e-mail) ne sont pas affectés.

+++
