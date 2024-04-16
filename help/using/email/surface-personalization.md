---
solution: Journey Optimizer
product: journey optimizer
title: Configuration des sous-domaines dynamiques de messagerie
description: Découvrez comment configurer des sous-domaines dynamiques au niveau de la surface du canal email
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: paramètres, courrier électronique, configuration, sous-domaine
hide: true
hidefromtoc: true
badge: label="Version Beta"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: 94d39089d94b4fe42eb3fb95603426012b104517
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 14%

---

# Personnaliser les paramètres de surface des emails {#surface-personalization}

Pour une flexibilité et un contrôle accrus de vos paramètres d&#39;email, [!DNL Journey Optimizer] permet de définir des valeurs personnalisées pour les sous-domaines et les en-têtes.<!--and URL tracking parameters--> lors de la création de surfaces d&#39;email.

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement disponible en version bêta pour sélectionner uniquement les utilisateurs. <!--To join the beta program, contact Adobe Customer Care.-->

## Ajouter des sous-domaines dynamiques {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personnalisation non disponible"
>abstract="Cette surface a été créée sans aucun attribut de personnalisation. Reportez-vous à la documentation pour connaître les étapes à suivre pour résoudre les problèmes de personnalisation."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Activer les sous-domaines dynamiques"
>abstract="Lors de la création d’une surface d’e-mail, vous pouvez configurer des sous-domaines dynamiques en fonction des conditions définies à l’aide de l’éditeur d’expression. Vous pouvez ajouter jusqu’à 50 sous-domaines dynamiques."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Certains sous-domaines peuvent ne pas être disponibles."
>abstract="Certains sous-domaines ne peuvent actuellement pas être sélectionnés en raison de l’enregistrement en attente de la boucle de rétroaction. Ce processus peut prendre jusqu’à 10 jours ouvrables. Une fois l’opération terminée, vous pouvez choisir parmi tous les sous-domaines disponibles."

Lors de la création d’une surface d’email, vous pouvez configurer des sous-domaines dynamiques en fonction de conditions spécifiques.

Par exemple, si vous avez des contraintes juridiques pour envoyer des messages à partir d’une adresse email dédiée par pays, vous pouvez utiliser des sous-domaines dynamiques. Vous pouvez ainsi créer une surface unique avec plusieurs sous-domaines d’envoi correspondant à différents pays, au lieu de créer plusieurs surfaces pour chaque pays. Vous pouvez ensuite cibler des clients basés dans différents pays consolidés dans une seule campagne.

Pour définir des sous-domaines dynamiques sur une surface de canal email, procédez comme suit.

1. Avant de créer une surface, configurez les sous-domaines que vous souhaitez utiliser pour envoyer des emails en fonction de votre cas d’utilisation. [Voici comment procéder](../configuration/about-subdomain-delegation.md)

   Par exemple, supposons que vous souhaitiez utiliser différents sous-domaines pour différents pays : configurer un sous-domaine spécifique aux États-Unis, un autre spécifique au Royaume-Uni, etc.

1. Créer une surface de canal. [Voici comment procéder](../configuration/channel-surfaces.md)

1. Sélectionnez la variable **[!UICONTROL Email]** canal.

1. Dans le **Subdomain** , activez la fonction **[!UICONTROL Sous-domaine dynamique]** .

   ![](assets/surface-email-dynamic-subdomain.png)

1. Cliquez sur l’icône Modifier en regard de la première **[!UICONTROL Condition]** champ .

1. La variable [Éditeur d’expression](../personalization/personalization-build-expressions.md) s’ouvre. Dans cet exemple, définissez une condition telle que `Country` est égal à `US`.

   ![](assets/surface-email-edit-condition.png)

1. Sélectionnez le sous-domaine que vous souhaitez associer à cette condition. [En savoir plus sur les sous-domaines](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Certains sous-domaines ne peuvent actuellement pas être sélectionnés en raison de leur mise en attente. [feedback loop](../reports/deliverability.md#feedback-loops) enregistrement. Ce processus peut prendre jusqu’à 10 jours ouvrables. Une fois l’opération terminée, vous pouvez choisir parmi tous les sous-domaines disponibles. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Tous les destinataires basés aux Etats-Unis recevront les messages utilisant le sous-domaine sélectionné pour ce pays, ce qui signifie que toutes les URL impliquées (comme la page miroir, l’URL de tracking ou le lien de désabonnement) seront renseignées en fonction de ce sous-domaine.

1. Définissez d’autres sous-domaines dynamiques comme vous le souhaitez. Vous pouvez ajouter jusqu’à 50 éléments.

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the surface. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. Définir toutes les autres [paramètres de messagerie électronique](email-settings.md) et [submit](../configuration/channel-surfaces.md#create-channel-surface) votre surface.

Une fois que vous avez ajouté un ou plusieurs sous-domaines dynamiques à une surface, les éléments suivants sont renseignés en fonction du sous-domaine dynamique résolu pour cette surface :

* Toutes les URL (URL de ressource, URL de page miroir et URL de tracking)

* La variable [unsubscribe URL](email-settings.md#list-unsubscribe)

* La variable **Adresse électronique** et **Email d’erreur** suffixes

>[!NOTE]
>
>Si vous configurez des sous-domaines dynamiques, désactivez la variable **[!UICONTROL Sous-domaine dynamique]** , toutes les valeurs dynamiques sont supprimées. Sélectionnez un sous-domaine et envoyez la surface pour que les modifications soient prises en compte.

## Personnaliser votre en-tête {#personalize-header}

Vous pouvez également utiliser la personnalisation pour tous les paramètres d’en-tête définis dans une surface.

Par exemple, si vous disposez de plusieurs marques, vous pouvez créer une surface unique et utiliser des valeurs personnalisées pour vos en-têtes d’email. Vous pouvez ainsi vous assurer que tous les emails envoyés par vos différentes marques sont adressés à chacun de vos clients avec les **De** noms et courriers électroniques. De même, lorsque vos destinataires ont appuyé sur la variable **Répondre** dans leur logiciel de messagerie, vous souhaitez que la fonction **Répondre à** les noms et les emails correspondent à la marque correcte pour l’utilisateur approprié.

Pour utiliser des variables personnalisées pour vos paramètres d’en-tête de surface, procédez comme suit.

>[!NOTE]
>
>Vous pouvez personnaliser tous les **[!UICONTROL Paramètres d’en-tête]** , à l’exception des champs **[!UICONTROL Préfixe de courrier électronique d’erreur]** champ .


1. Définissez les paramètres d’en-tête comme vous le feriez habituellement. [Voici comment procéder](email-settings.md#email-header)

1. Pour chaque champ, sélectionnez l&#39;icône Modifier .

   ![](assets/surface-email-personalize-header.png)

1. La variable [Éditeur d’expression](../personalization/personalization-build-expressions.md) s’ouvre. Définissez votre condition comme vous le souhaitez et enregistrez vos modifications.

   Par exemple, définissez une condition telle que chaque destinataire reçoit un email de son propre représentant de marque.

   >[!NOTE]
   >
   >Vous pouvez uniquement sélectionner **[!UICONTROL Attributs de profil]** et **[!UICONTROL Fonctions d’assistance]**.

1. Répétez les étapes ci-dessus pour chaque paramètre auquel vous souhaitez ajouter une personnalisation.

>[!NOTE]
>
>Si vous avez ajouté un ou plusieurs sous-domaines dynamiques à votre surface, la variable **Adresse électronique** et **Email d’erreur** Les suffixes seront renseignés en fonction des [sous-domaine dynamique](#dynamic-subdomains).

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## Afficher les détails de la surface {#view-surface-details}

Lorsque vous utilisez une surface avec des paramètres personnalisés dans une opération ou une surface, vous pouvez afficher les détails de la surface directement dans la campagne ou la surface. Suivez les étapes ci-dessous.

1. Créer un email [campaign](../campaigns/create-campaign.md) ou [parcours](../building-journeys/journey-gs.md).

1. Sélectionnez la variable **[!UICONTROL Modifier le contenu]** bouton .

1. Cliquez sur le bouton **[!UICONTROL Afficher les détails de la surface]** bouton .

   ![](assets/campaign-view-surface-details.png)

1. La variable **[!UICONTROL Paramètres de diffusion]** s’affiche. Vous pouvez afficher tous les paramètres de surface, y compris les sous-domaines dynamiques et les paramètres d’en-tête personnalisés.

   >[!NOTE]
   >
   >Toutes les informations de cet écran sont en lecture seule.

1. Sélectionner **[!UICONTROL Développer]** pour afficher les détails des sous-domaines dynamiques.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
