---
solution: Journey Optimizer
product: journey optimizer
title: Recherche d’événements d’expérience dans les parcours
description: Découvrez comment utiliser la recherche d’événements d’expérience dans les parcours.
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 87%

---

# Recherche d’événements d’expérience dans les parcours {#ee-journeys}

>[!CAUTION]
>
>À compter du 8 juillet 2025, dans les nouvelles organisations clientes, la création d’expressions à l’aide d’événements d’expérience n’est plus prise en charge dans l’éditeur d’expression utilisé dans les conditions de parcours. Par conséquent, les événements d’expérience dans la [source de données Experience Platform](../datasource/adobe-experience-platform-data-source.md) ne peuvent pas être utilisés pour créer des expressions. Les autres approches et bonnes pratiques pour créer des expressions/logiques avec des événements d’expérience sont référencées ci-dessous.
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
* [Gestion des droits d’opposition pour les messages texte](../sms/sms-opt-out.md)


## Suppression basée sur les rebonds

Pour exclure les profils qui ont subi des rebonds d’e-mails, utilisez la liste de suppression automatique de [!DNL Adobe Journey Optimizer] pour les adresses qui ont fait l’objet de rebonds. Ce mécanisme intégré garantit que les e-mails non valides ou inatteignables sont exclus des envois futurs sans nécessiter de logique personnalisée.

En savoir plus :

* [Gérer la liste de suppression](../configuration/manage-suppression-list.md)


## Suppression générique

Pour supprimer des profils qui ont manifesté des comportements spécifiques, utilisez des audiences par lots avec une logique basée sur les événements afin de capturer les profils qui correspondent aux critères de suppression. Référencez cette audience dans les conditions de parcours.

En savoir plus :

* [!DNL Adobe Experience Platform] [Créateur de segments - Événements](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Créateur de segments - Contraintes de temps](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-a-segment)

* [Fonction inAudience()](../building-journeys/functions/functioninaudience.md)


## Exclusion basée sur des communications reçues

Pour empêcher l’envoi de messages aux profils qui ont reçu des communications au cours d’une période récente :

* Utilisez des audiences par lots avec des critères temporels et référencez ces audiences dans les conditions de parcours.
* Appliquez des règles métier de capping de la fréquence pour appliquer des limites de messages quotidiennes ou hebdomadaires.


En savoir plus sur l’utilisation des audiences :

* [!DNL Adobe Experience Platform] [Créateur de segments - Événements](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Créateur de segments - Contraintes de temps](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-a-segment)

* [Fonction inAudience()](../building-journeys/functions/functioninaudience.md)


Voir également :

* [Capping de la fréquence par canal et type de communication](../conflict-prioritization/channel-capping.md)



## Inclusion/exclusion spécifique à un message

Pour inclure ou exclure des profils en fonction d’un message reçu spécifique, créez des audiences par lots qui encapsulent cette logique et référencez-les dans les conditions de parcours.


En savoir plus :

* [!DNL Adobe Experience Platform] [Créateur de segments - Événements](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* [!DNL Adobe Experience Platform] [Créateur de segments - Contraintes de temps](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-a-segment)

* [Fonction inAudience()](../building-journeys/functions/functioninaudience.md)

## Personnalisation de l’abandon du panier ou de la navigation

Pour personnaliser les communications en fonction des derniers événements liés au panier ou à la navigation sur plusieurs types de panier ou consultations de produits :

* Si vous avez accès à [[!DNL Adobe Experience Platform] Data Distiller](https://experienceleague.adobe.com/fr/docs/experience-platform/query/data-distiller/overview){target="_blank"}, configurez des requêtes automatisées pour extraire les données requises de l’événement, les manipuler pour les adapter au cas d’utilisation et les réécrire dans un jeu de données activé pour un profil pour activation.
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

Vous trouverez ci-dessous les questions fréquentes sur la recherche d’événements d’expérience dans les parcours.

Vous avez besoin de plus d’informations ? Utilisez les options de commentaires au bas de cette page pour poser votre question ou communiquer avec [[!DNL Adobe Journey Optimizer] communauté](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=fr){target="_blank"}.

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

Votre organisation Adobe n’est affectée que si vous n’avez pas déjà utilisé la recherche d’événements d’expérience. Si vous utilisez déjà des événements d’expérience dans la [source de données Experience Platform](../datasource/adobe-experience-platform-data-source.md), votre organisation Adobe continue à prendre en charge la recherche d’événements d’expérience.

+++

+++J’ai une nouvelle organisation Adobe. Comment résoudre mon cas d’utilisation qui requiert des données d’événement d’expérience ? 

D’autres approches et bonnes pratiques concernant les événements d’expérience sont disponibles ci-dessus pour mener à bien les cas d’utilisation souhaités.

+++

+++ Que faire si les autres approches ne fonctionnent pas pour mon cas d’utilisation ?

Si votre cas d’utilisation ne peut pas être résolu à l’aide de l’une des autres approches répertoriées ci-dessus, contactez votre représentant ou représentante Adobe.

+++
