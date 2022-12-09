---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation des stratégies de consentement
description: Découvrez comment utiliser les stratégies de consentement d’Adobe Experience Platform
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Utilisation des stratégies de consentement {#consent-management}

Adobe Experience Platform vous permet d’adopter et d’appliquer facilement des stratégies marketing afin de respecter les préférences de consentement de vos clients. Les stratégies de consentement sont définies dans Adobe Experience Platform. Voir [cette documentation](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=en#consent-policy).

Dans Journey Optimizer, vous pouvez appliquer ces stratégies de consentement à vos actions personnalisées. Par exemple, vous pouvez définir des stratégies de consentement pour exclure les clients qui n’ont pas consenti à recevoir des communications par courrier électronique, push ou SMS.

>[!NOTE]
>
>Actuellement, les politiques de consentement ne sont disponibles que pour les organisations qui ont acheté l’offre complémentaire du Bouclier de santé.

Dans Journey Optimizer, le consentement est défini à plusieurs niveaux :

* when **configuration d’une action personnalisée**, vous pouvez définir un canal et une action marketing. Voir [section](../action/consent.md#consent-custom-action).
* lors de l’ajout de la variable **action personnalisée dans un parcours**, vous pouvez définir une action marketing supplémentaire. Voir [section](../action/consent.md#consent-journey).

## Remarques importantes {#important-notes}

Dans Journey Optimizer, le consentement peut être utilisé dans des actions personnalisées. Si vous souhaitez l’utiliser avec les fonctionnalités de message intégré, vous devez utiliser une activité de condition pour filtrer les clients dans votre parcours.

Avec la gestion du consentement, deux activités de parcours sont analysées :

* Lecture de segment : le segment récupéré est pris en compte.
* Action personnalisée : la gestion du consentement prend en compte les attributs utilisés ([paramètres d’action](../action/about-custom-action-configuration.md#define-the-message-parameters)) ainsi que la ou les actions marketing définies (action marketing requise et action marketing supplémentaire).
* Les attributs qui font partie d’un groupe de champs à l’aide du schéma d’union d’usine ne sont pas pris en charge. Ces attributs seront masqués dans l’interface. Vous devez créer un autre groupe de champs à l’aide d’un autre schéma.
* Les stratégies de consentement s’appliquent uniquement lorsqu’une action marketing (requise ou supplémentaire) est définie au niveau de l’action personnalisée.

Toutes les autres activités utilisées dans un parcours ne sont pas prises en compte. Si vous commencez votre parcours avec une qualification de segment , le segment n’est pas pris en compte.

Dans un parcours, si un profil est exclu par une stratégie de consentement dans une action personnalisée, le message ne lui est pas envoyé, mais il poursuit le parcours. Le profil n’atteint pas le délai d’expiration et le chemin d’erreur lors de l’utilisation d’une condition.

Avant d’actualiser les stratégies dans une action personnalisée placée dans un parcours, assurez-vous que ce dernier ne comporte aucune erreur.

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

## Configuration de l’action personnalisée {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_admin"
>title="Définition d’une action marketing requise"
>abstract="L’action marketing requise vous permet de définir l’action marketing associée à votre action personnalisée. Par exemple, si vous utilisez cette action personnalisée pour envoyer des emails, vous pouvez sélectionner Ciblage des emails. Lorsqu’elles sont utilisées dans un parcours, toutes les stratégies de consentement associées à cette action marketing sont récupérées et exploitées. Il ne peut pas être modifié dans la zone de travail."

Lors de la configuration d’une action personnalisée, deux champs peuvent être utilisés pour la gestion du consentement.

Le **Canal** vous permet de sélectionner le canal associé à cette action personnalisée : **Email**, **SMS** ou **Notification push**. Elle préremplit la variable **Action marketing requise** avec l’action marketing par défaut pour le canal sélectionné. Si vous sélectionnez **other**, aucune action marketing ne sera définie par défaut.

![](assets/consent1.png)

Le **Action marketing requise** vous permet de définir l’action marketing associée à votre action personnalisée. Par exemple, si vous utilisez cette action personnalisée pour envoyer des emails, vous pouvez sélectionner **Ciblage des emails**. Lorsqu’elles sont utilisées dans un parcours, toutes les stratégies de consentement associées à cette action marketing sont récupérées et exploitées. Une action marketing par défaut est sélectionnée, mais vous pouvez cliquer sur la flèche vers le bas pour sélectionner n’importe quelle action marketing disponible dans la liste.

![](assets/consent2.png)

Pour certains types de communications importantes, par exemple un message transactionnel envoyé pour réinitialiser le mot de passe du client, vous pouvez ne pas appliquer de stratégie de consentement. Vous pouvez ensuite sélectionner **Aucun** dans le **Action marketing requise** champ .

Les autres étapes de configuration d’une action personnalisée sont présentées dans la section [cette section](../action/about-custom-action-configuration.md#consent-management).

### Création du parcours {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_canvas"
>title="Action marketing requise"
>abstract="Une action marketing requise est définie lors de la création d’une action personnalisée. Cette action marketing requise ne peut pas être supprimée de l’action ou modifiée."

>[!CONTEXTUALHELP]
>id="ajo_consent_additional_marketing_action_canvas"
>title="Action marketing supplémentaire"
>abstract="Ajoutez une autre action marketing en plus de celle requise. Les stratégies de consentement liées aux deux actions marketing seront appliquées."

>[!CONTEXTUALHELP]
>id="ajo_consent_refresh_policies_canvas"
>title="Visualiser les stratégies de consentement qui s’appliqueront au moment de l’exécution"
>abstract="Les actions marketing apportent des stratégies de consentement qui combinent des paramètres d’action et des valeurs de consentement de profil individuel pour filtrer les utilisateurs. Obtenez la dernière définition de ces stratégies en cliquant sur le bouton pour l’actualiser."

Lors de l’ajout de l’action personnalisée dans un parcours, plusieurs options vous permettent de gérer le consentement. Cliquez sur le bouton **Afficher les champs en lecture seule** pour afficher tous les paramètres.

Le **Canal** et **Action marketing requise**, définies lors de la configuration de l’action personnalisée, s’affichent en haut de l’écran. Vous ne pouvez pas modifier ces champs.

![](assets/consent4.png)

Vous pouvez définir une **Action marketing supplémentaire** pour définir le type d’action personnalisée. Cela vous permet de définir l’objectif de l’action personnalisée dans ce parcours. Outre l’action marketing requise, généralement spécifique à un canal, vous pouvez définir une action marketing supplémentaire qui sera spécifique à l’action personnalisée de ce parcours spécifique. Par exemple : une communication avec les musiciens, une newsletter, une communication sur la condition physique, etc. L’action marketing requise et l’action marketing supplémentaire s’appliqueront toutes deux.

![](assets/consent3.png)

Cliquez sur le bouton **Actualiser les stratégies** , en bas de l’écran, pour mettre à jour et vérifier la liste des stratégies prises en compte pour cette action personnalisée. Il est fourni à titre d’information uniquement lors de la création d’un parcours. Avec les parcours actifs, les stratégies de consentement sont récupérées et mises à jour automatiquement toutes les 6 heures.

![](assets/consent5.png)

<!--
The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* action parameters defined in the custom action, see this [section](../action/about-custom-action-configuration.md#define-the-message-parameters) 
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-segment.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

Les autres étapes de configuration d’une action personnalisée dans un parcours sont présentées dans la section [cette section](../building-journeys/using-custom-actions.md).
