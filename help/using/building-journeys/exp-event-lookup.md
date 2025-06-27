---
solution: Journey Optimizer
product: journey optimizer
title: Recherche d’événements d’expérience dans les parcours
description: Découvrez comment utiliser la recherche d’événements d’expérience dans parcours
source-git-commit: 190d7d5fd5cb93a6ddf3757e00f42a9714a1f722
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 6%

---


# Recherche d’événement d’expérience dans parcours {#ee-journeys}

>[!CAUTION]
>
>À compter du 8 juillet, dans les nouvelles organisations clientes, la création d’expressions à l’aide d’événements d’expérience ne sera plus prise en charge dans l’éditeur d’expression utilisé dans les conditions de parcours. Par conséquent, les événements d’expérience dans la source de données [Experience Platform](../datasource/adobe-experience-platform-data-source.md) ne peuvent pas être utilisés pour créer des expressions. Les autres approches et bonnes pratiques pour créer des expressions/logiques avec des événements d’expérience sont référencées ci-dessous.
>
>Besoin de plus de détails ? [Lire la FAQ](#faq-ee).

Cette page décrit les modèles courants et les approches évolutives pour vous aider à tirer le meilleur parti des événements d’expérience dans Adobe Journey Optimizer. Ces cas d’utilisation sont conçus pour vous aider à résoudre des défis fréquents tels que la gestion des désinscriptions, le contrôle de la fréquence des messages, la personnalisation du contenu en fonction du comportement de l’utilisateur et la réaction aux signaux en temps réel.

En utilisant ces stratégies, vous pouvez transformer les données comportementales en actions significatives, à savoir la suppression, la qualification ou l’exclusion de profils en fonction des événements qu’ils déclenchent ou des attributs qu’ils transportent. Que vous élaboriez une logique pour les seuils d’achat, les déclencheurs d’abandon ou la gestion des bounces, ces exemples offrent des conseils pratiques que vous pouvez adapter à vos besoins.

Lorsque vous évaluez l’approche la plus adaptée, tenez compte des exigences de latence de votre cas d’utilisation pour vous assurer que vos parcours restent réactifs et efficaces.

## Suppression de l’opt-out

Pour supprimer des profils qui se sont désinscrits des communications marketing, utilisez la gestion intégrée du consentement. Les préférences de désinscription sont automatiquement capturées dans les champs de consentement du profil ; elles peuvent être référencées directement dans des conditions de parcours et sont automatiquement appliquées par Journey Optimizer lors de la diffusion du message.

En savoir plus :

* [Gérer le consentement](../privacy/opt-out.md)
* [Gestion du processus de désinscription aux e-mails](../email/email-opt-out.md)
* [Gestion d’opt-out pour les SMS](../sms/sms-opt-out.md)


## Suppression basée sur les rebonds

Pour exclure les profils qui ont subi des rebonds d’e-mails, utilisez la liste de suppression automatique de Adobe Journey Optimizer pour les adresses qui ont fait l’objet de rebonds. Ce mécanisme intégré garantit que les e-mails non valides ou inatteignables sont exclus des envois futurs sans nécessiter de logique personnalisée.

En savoir plus :

* [Gérer la liste de suppression](../configuration/manage-suppression-list.md)


## Suppression générique

Pour supprimer des profils qui ont démontré certains comportements, utilisez des audiences par lots avec une logique basée sur les événements afin de capturer les profils qui répondent aux critères de suppression. Référencez cette audience dans des conditions de parcours.

En savoir plus :

* Adobe Experience Platform [Créateur de segments - Événements](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Créateur de segments - Contraintes de temps](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()](../building-journeys/functions/functioninaudience.md)


## Exclusion des communications reçues

Pour empêcher l’envoi de messages aux profils qui ont reçu des communications au cours d’une période récente :

* Utilisez des audiences par lot avec des critères temporels et référencez-les dans des conditions de parcours.
* Appliquez les règles métier de limitation de la fréquence pour appliquer des limites de messages quotidiennes ou hebdomadaires.


En savoir plus sur l’utilisation des audiences :

* Adobe Experience Platform [Créateur de segments - Événements](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Créateur de segments - Contraintes de temps](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()](../building-journeys/functions/functioninaudience.md)


Voir également :

* [Capping de la fréquence par canal et type de communication](../conflict-prioritization/channel-capping.md)



## Inclusion/exclusion spécifique au message

Pour inclure ou exclure des profils en fonction du message reçu, créez des audiences par lots qui encapsulent cette logique et les référencent dans des conditions de parcours.


En savoir plus :

* Adobe Experience Platform [Créateur de segments - Événements](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [Créateur de segments - Contraintes de temps](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [Utiliser des audiences dans des conditions](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()](../building-journeys/functions/functioninaudience.md)

## Personnalisation de l’abandon du panier ou de la navigation

Pour personnaliser les communications en fonction du dernier panier ou parcourir les événements sur plusieurs types de panier ou consultations de produits :

* Si vous avez accès à [Adobe Experience Platform Data Distiller](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/overview){target="_blank"}, configurez des requêtes automatisées pour extraire les données requises de l&#39;événement, les manipuler pour les adapter au cas d&#39;utilisation et les réécrire dans un jeu de données activé pour un profil pour activation.
* Si les données d’abandon peuvent être modélisées sur le profil avec des attributs scalaires, pensez à utiliser les attributs calculés pour capturer les dernières informations, puis à référencer ces attributs dans le parcours pour créer la communication. [En savoir plus dans la documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}


## Sortie de parcours basée sur le comportement

Pour supprimer des profils du parcours lorsqu’ils présentent un comportement particulier, utilisez les critères de sortie afin de quitter le profil du parcours lorsqu’un événement particulier est reçu ou que le profil se qualifie pour une audience spécifique.

En savoir plus :

* [Définir vos propriétés de parcours - Critères de sortie](journey-properties.md#exit-criteria)

## Qualification basée sur l’achat avec seuils de valeur

Pour déclencher des parcours en fonction des achats et supprimer si la valeur est supérieure ou inférieure à un seuil, définissez des attributs calculés pour additionner les achats sur une période spécifique. Créez une audience qui comprend des profils dont le montant des dépenses répond à certains critères.

En savoir plus :

* Adobe Experience Platform [Présentation des attributs calculés](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## Questions fréquentes {#faq-ee}

L’utilisation d’événements d’expérience dans des expressions/conditions de parcours n’est plus prise en charge. Les impacts sont répertoriés dans les questions fréquentes ci-dessous :

+++Quelles fonctionnalités spécifiques sont affectées ?

Seule la recherche d’événements d’expérience dans l’éditeur d’expression est affectée. Les fonctionnalités suivantes ne sont **pas** affectées et restent les mêmes :

* Observer les événements d’expérience associés à un profil spécifique dans l’interface utilisateur du profil

* Utilisation d’événements d’expérience dans des règles d’attributs calculés et accès aux attributs calculés dans un parcours

* Déclenchement d’un parcours avec un événement unitaire ou métier

* Utilisation des données contextuelles du parcours issues des événements qui déclenchent le parcours dans les éditeurs d’expression et de personnalisation

* Écoute d’un événement dans un parcours

* Configuration des événements pour déclencher un parcours

* Détection des événements de réaction de l’utilisateur final aux communications marketing (par exemple, ouverture d’e-mail)

+++

+++Mon organisation Adobe existante sera-t-elle affectée par cette mise à jour ?

Votre organisation Adobe ne serait affectée que si vous n’utilisiez pas déjà la recherche d’événement d’expérience. Si vous utilisez déjà des événements d’expérience dans la source de données [Experience Platform](../datasource/adobe-experience-platform-data-source.md), votre organisation Adobe continuera à prendre en charge la recherche d’événements d’expérience.

+++

+++J’ai une nouvelle organisation Adobe. Comment résoudre mon cas d’utilisation nécessitant des données d’événement d’expérience ?

D’autres approches et bonnes pratiques impliquant des événements d’expérience sont disponibles ci-dessus pour atteindre les cas d’utilisation souhaités.

+++

+++ Que faire si d’autres approches ne fonctionnent pas pour mon cas d’utilisation ?

Si votre cas d’utilisation ne peut pas être résolu à l’aide de l’une des autres approches répertoriées ci-dessus, contactez votre représentant ou représentante Adobe.

+++
