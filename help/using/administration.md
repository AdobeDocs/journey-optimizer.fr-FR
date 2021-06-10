---
title: Paramètres techniques
description: Découvrez les directives relatives à l’administration et aux paramètres.
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: ht
source-wordcount: '499'
ht-degree: 100%

---

# Paramètres techniques

![](assets/do-not-localize/badge.png)

## Configuration des paramètres de branding{#cjm-branding}

Chaque entreprise dispose de directives visuelles et techniques en ce qui concerne la marque. Vous pouvez définir un ensemble de spécifications pour présenter une marque cohérente à vos clients, depuis les logos jusqu’aux aspects techniques, tels que l’expéditeur de l’email, le domaine de l’URL des pages miroir ou les paramètres de suivi des messages.
Les marques ne peuvent pas être créées ou modifiées par les utilisateurs finaux : cette configuration est gérée par Adobe.

Pour configurer les paramètres de branding de votre instance [!DNL Journey Optimizer], vous devez contacter Adobe et communiquer les informations suivantes :

* Nom de la société

* Adresse email de l’expéditeur (De)

* Nom de l’expéditeur (De)

* Adresse de réponse

Une fois les paramètres de branding configurés, vous pourrez les sélectionner lors de la création de messages.

Une fois les paramètres de branding configurés, vous pourrez les sélectionner dans la liste **[!UICONTROL Préréglages]** lors de la création de messages. [En savoir plus sur la création de contenu](create-message.md).

## Configuration du canal de notification push

Découvrez comment configurer le canal push dans [cette section](configure-push.md).

## Délégation de sous-domaine

Pour un nouveau sous-domaine à utiliser dans [!DNL Journey Optimizer], la première étape consiste à le déléguer. Vous devez contacter votre contact technique Adobe.

Lors de la mise en œuvre d’une solution, des exigences doivent être satisfaites pour les composants orientés vers l’extérieur : par exemple, configurer les liens et les pages web à suivre, afficher les pages miroir, etc.

Bien que ces exigences soient gérées au moyen de composants hébergés à la fois par Adobe et le client, elles incluent des URL visibles par les destinataires des emails.  Afin d’éviter que des URL indiquant la solution technique sous-jacente ou le fournisseur d’hébergement ne soient installées, il est possible de configurer des sous-domaines pour rendre cette opération transparente pour les destinataires des emails.

À la suite de ces délégations, l&#39;infrastructure mise en place par Adobe garantit que les services suivants sont mis en œuvre pour chaque domaine d&#39;envoi délégué ou en alias CNAME :

* Création de boîtes de réception &quot;maître de poste&quot; et &quot;abus&quot;

* Configuration de boucles de commentaires pour le domaine délégué

* Configuration d’un enregistrement DMARC de base

Les paramètres établis par Adobe ne sont valables qu’à partir du moment où la délégation a été effectuée puis vérifiée par Adobe, et restent fonctionnels.

[En savoir plus sur la délégation de domaine](https://helpx.adobe.com/fr/campaign/kb/domain-name-delegation.html).


## Créer des sources de données, des événements et des actions

Utilisez la section **[!UICONTROL Administration]** pour gérer les **[!UICONTROL Sources de données]**, les **[!UICONTROL Événements]** et les **[!UICONTROL Actions]**.

![](assets/admin-menu.png)

### Sources de données

La configuration des sources de données vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours.

En savoir plus sur les sources de données dans [cette section](../using/datasource/about-data-sources.md).

### Événements

Les événements vous permettent de déclencher vos parcours de manière unitaire pour envoyer des messages, en temps réel, à l’individu progressant dans le parcours.

Dans la configuration des événements, vous configurez les événements attendus dans les parcours. Les données des événements entrants sont normalisées conformément au modèle de données Adobe Experience (XDM). Les événements authentifiés et non authentifiés proviennent des API d’ingestion en flux continu (notamment ceux issus du kit de développement Adobe Mobile SDK).

En savoir plus sur les événements dans [cette section](../using/event/about-events.md).

### Actions

Les fonctionnalités de message [!DNL Journey Optimizer] sont intégrées : il vous suffit de concevoir votre contenu et de publier votre message. Si vous utilisez un système tiers pour envoyer vos messages, vous pouvez créer une action personnalisée.

En savoir plus sur les actions dans [cette section](../using/action/action.md).
