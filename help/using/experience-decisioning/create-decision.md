---
title: Commencer avec les politiques de décision
description: Découvrez comment utiliser les politiques de décision pour diffuser des offres.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: c2388c84346ed9a0409270fd96f3a1458bf8ad88
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 98%

---

# Commencer avec les politiques de décision {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Qu’est-ce qu’une décision ?"
>abstract="Les politiques de décision contiennent toute la logique de sélection afin que le moteur de prise de décision choisisse le meilleur contenu. Les politiques de décision sont spécifiques aux campagnes. Leur objectif est de sélectionner les meilleures offres pour chaque profil, tandis que la création de campagne vous permet d’indiquer comment les éléments de décision sélectionnés doivent être présentés, y compris les attributs d’élément à inclure dans le message."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="À propos de la prise de décision"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="Définir une politique de décision"
>abstract="Une politique de décision vous permet de sélectionner les meilleurs éléments du moteur de prise de décision et de les diffuser à l’audience appropriée."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="À propos de la prise de décision"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="Politique de décision"
>abstract="Une politique de décision vous permet de sélectionner les meilleurs éléments du moteur de décision et de les diffuser à chaque audience."

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="Emplacement"
>abstract="Un emplacement détermine où les éléments renvoyés par le moteur de décision apparaissent dans un message. Vous pouvez suivre leurs performances sur les différents emplacements dans les rapports."

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="Sélectionner des attributs de décision dans un catalogue"
>abstract="Les attributs de décision sont stockés dans le schéma du catalogue. Sélectionnez un attribut que vous souhaitez utiliser ici dans le catalogue sélectionné."

Les politiques de décision sont des conteneurs pour vos offres qui tirent profit du moteur de prise de décision afin de renvoyer dynamiquement le meilleur contenu à diffuser pour chaque membre de l’audience. Leur objectif est de sélectionner les meilleures offres pour chaque profil, tandis que la création de campagne et de parcours vous permet d’indiquer comment les éléments de décision sélectionnés doivent être présentés, y compris les attributs d’élément à inclure dans le message.

>[!AVAILABILITY]
>
>Pour l’instant, les politiques de décision sont disponibles pour tous les clients et clientes pour le canal d’expérience basée sur du code. Elles sont en disponibilité limitée pour le canal e-mail. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

## Principales étapes {#key}

Les principales étapes pour utiliser les politiques de décision dans vos messages sont les suivantes :

1. [Créer une politique de décision](../experience-decisioning/create-decision-policy.md)

   Configurez une politique de décision dans votre message en choisissant le nombre d’éléments à renvoyer, en configurant des stratégies de sélection, des options de secours et l’ordre d’évaluation.

1. [Utiliser la politique de décision dans votre contenu](../experience-decisioning/use-decision-policy.md)

   Personnalisez votre contenu avec la sortie et les attributs de la politique de décision des éléments de décision que vous souhaitez afficher dans le message.

1. [Créer des tableaux de bord de reporting](cja-reporting.md)

   Créez des tableaux de bord Customer Journey Analytics personnalisés pour mesurer les performances et obtenir des informations sur la manière dont vos politiques de décision et vos offres sont diffusées et utilisées.

## Mécanismes de sécurisation et limitations

* **Pages miroir des e-mails** : pour l’instant, les éléments de décision ne s’affichent pas dans les pages miroir des e-mails.
* **Type de suivi et de liens** : pour suivre les liens générés par la prise de décision, définissez-les dans le schéma comme « Ressources de prise de décision ». Les liens basés sur les attributs ne pevent pas faire l’objet d’un suivi.
* **Imbrication de politiques de décision dans des e-mails** : vous ne pouvez pas imbriquer plusieurs politiques de décision dans un composant d’e-mail parent auquel est déjà associée une politique de décision.
* **Parcours ou campagnes dupliqués avec prise de décision** : si vous dupliquez un parcours ou une campagne qui inclut une politique de décision, la version dupliquée fait référence à l’e-mail ou à l’expérience basée sur du code d’origine, ce qui entraîne des erreurs. Reconfigurez toujours la politique de décision après la duplication.
* **Politiques de consentement** – les mises à jour des politiques de consentement prennent jusqu’à 48 heures. Si une politique de décision fait référence à un attribut lié à une politique de consentement récemment mise à jour, les modifications ne sont pas appliquées immédiatement.

  De même, si de nouveaux attributs de profil soumis à une politique de consentement sont ajoutés à une politique de décision, ils seront utilisables, mais la politique de consentement qui leur est associée ne sera pas appliquée tant que le délai ne sera pas écoulé.

  Les politiques de consentement ne sont actuellement disponibles que pour les organisations disposant des modules complémentaires Adobe Healthcare Shield et Privacy and Security Shield.

* **Classement AI** : pour l’instant, le classement AI n’est pas pris en charge pour le canal E-mail dans les parcours avec prise de décision.

## Étapes suivantes {#next-steps}

Maintenant que vous comprenez comment fonctionnent les politiques de décision et comment elles permettent de diffuser des offres personnalisées, vous êtes prêt à créer votre première politique de décision.

➡️ [Découvrez comment créer une politique de décision.](../experience-decisioning/create-decision-policy.md)

## Vidéo pratique {#video}

Découvrez comment utiliser Decisioning pour personnaliser les e-mails pour votre audience.

>[!VIDEO](https://video.tv.adobe.com/v/3479212?captions=fre_fr&quality=12)
