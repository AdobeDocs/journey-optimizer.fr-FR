---
title: Paramètres techniques
description: Découvrez les instructions relatives à l'administration et aux paramètres
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 31%

---

# Paramètres techniques

![](assets/do-not-localize/badge.png)

## Configuration des paramètres de marque{#cjm-branding}

Chaque entreprise dispose de directives visuelles et techniques en ce qui concerne la marque. Vous pouvez définir un ensemble de spécifications pour présenter une marque cohérente à vos clients, des logos aux aspects techniques, tels que l&#39;expéditeur de courrier électronique, le domaine de l&#39;URL des pages miroir ou les paramètres de suivi des messages.
Les marques ne peuvent pas être créées ou modifiées par les utilisateurs finaux : cette configuration est gérée par Adobe.

Pour configurer les paramètres de marque de votre instance [!DNL Journey Optimizer], vous devez contacter l&#39;Adobe et partager les informations suivantes :

* Nom de la société

* Adresse électronique de l’expéditeur (de)

* Nom de l&#39;expéditeur (de)

* Adresse de réponse

Une fois les paramètres de marque configurés, vous pourrez les sélectionner lors de la création de messages.

Une fois les paramètres de marque configurés, vous pouvez les sélectionner lors de la création de messages à partir de la liste **[!UICONTROL Paramètres prédéfinis]**. [En savoir plus sur la création](create-message.md) de contenu.

## Configuration du canal de notification Push

Découvrez comment configurer le canal Push dans cette [section](configure-push.md).

## Délégation de sous-domaine

Pour tout nouveau sous-domaine à utiliser dans [!DNL Journey Optimizer], la première étape consiste à le déléguer. Vous devez contacter votre contact technique Adobe.

Lors de la mise en oeuvre d’une solution, les composants externes sont requis : il s&#39;agit notamment de la configuration des liens et des pages Web à suivre, de l&#39;affichage des pages miroir, etc.

Bien que ces exigences soient gérées au moyen de composants hébergés à la fois par Adobe et le client, elles incluent des URL visibles par les destinataires des emails.  Afin d&#39;éviter que des URL indiquant la solution technique sous-jacente ou le fournisseur d&#39;hébergement ne soient installées, il est possible de configurer des sous-domaines pour rendre cette opération transparente pour les destinataires des emails.

À la suite de ces délégations, l&#39;infrastructure mise en place par Adobe garantit que les services suivants sont mis en œuvre pour chaque domaine d&#39;envoi délégué ou en alias CNAME :

* Création de boîtes de réception &quot;maître de poste&quot; et &quot;abus&quot;

* Configuration de boucles de commentaires pour le domaine délégué

* Configuration d’enregistrement DMARC de base

Les paramètres établis par Adobe ne sont valables qu&#39;à partir du moment où la délégation a été effectuée puis vérifiée par Adobe, et restent fonctionnels.

[En savoir plus sur la délégation](https://helpx.adobe.com/fr/campaign/kb/domain-name-delegation.html) de domaine.


## Création de sources de données, de Événements et d’actions

Utilisez la section **[!UICONTROL Admin]** pour gérer les **[!UICONTROL sources de données]**, **[!UICONTROL Événements]** et **[!UICONTROL actions]**.

![](assets/admin-menu.png)

### Sources de données

La configuration de la source de données vous permet de définir une connexion à un système pour récupérer des informations supplémentaires qui seront utilisées dans vos parcours.

En savoir plus sur les sources de données dans cette [section](../using/datasource/about-data-sources.md)

### Événements

Les événements vous permettent de déclencher vos parcours à l&#39;unité pour envoyer des messages, en temps réel, à la personne qui arrive sur le parcours.

Dans la configuration du événement, vous configurez les événements attendus dans les parcours. Les données des événements entrants sont normalisées à la suite du modèle de données d’expérience Adobe (XDM). Les événements authentifiés et non authentifiés proviennent des API d’ingestion en flux continu (notamment ceux issus du kit de développement Adobe Mobile SDK).

En savoir plus sur les événements dans cette [section](../using/event/about-events.md)

### Actions

[!DNL Journey Optimizer] les fonctionnalités de message sont intégrées : il vous suffit de concevoir votre contenu et de publier votre message. Si vous utilisez un système tiers pour envoyer vos messages, vous pouvez créer une action personnalisée.

En savoir plus sur les actions de cette [section](../using/action/action.md)
