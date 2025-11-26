---
solution: Journey Optimizer
product: journey optimizer
title: Configurer des sous-domaines web
description: Découvrez comment configurer des sous-domaines web avec Journey Optimizer.
role: Admin
feature: Web Channel, Subdomains
level: Experienced
keywords: web, sous-domaines, configuration
exl-id: 6e00466d-4ce5-4d80-89ff-c7331a5ab158
source-git-commit: 311dbb72079b91d3faa1c60c38a66a806d80da42
workflow-type: ht
source-wordcount: '987'
ht-degree: 100%

---

# Configurer des sous-domaines web {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Déléguer un sous-domaine web"
>abstract="Votre tâche consiste à configurer votre sous-domaine pour le canal web. Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou en configurer un autre."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Déléguer un sous-domaine web"
>abstract="Si vous ajoutez du contenu provenant d’Adobe Experience Manager Assets à vos expériences web, vous devez configurer le sous-domaine qui sera utilisé pour publier ce contenu. Choisissez parmi les sous-domaines déjà délégués à Adobe ou configurez un nouveau sous-domaine."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Définir un sous-domaine web"
>abstract="Sélectionnez un sous-domaine dans la liste des sous-domaines délégués à Adobe. Vous pouvez définir ce sous-domaine web comme sous-domaine par défaut, mais un seul sous-domaine par défaut peut être utilisé à la fois."

## Commencer avec les sous-domaines web {#gs-web-subdomains}

Lors de la création d’expériences web, si vous ajoutez du contenu provenant de la bibliothèque [Adobe Experience Manager Assets](../integrations/assets.md), vous devez configurer le sous-domaine qui sera utilisé pour publier ce contenu.

Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou en configurer un autre. Pour en savoir plus sur la délégation de sous-domaines à Adobe, consultez [cette section](../configuration/delegate-subdomain.md).

La configuration de sous-domaines web est **commune à tous les environnements**. Par conséquent :

* Pour accéder aux sous-domaines web et les modifier, vous devez disposer de l’autorisation **[!UICONTROL Gérer les sous-domaines]** dans la sandbox de production.

* Toute modification apportée à un sous-domaine web aura également un impact sur les sandbox de production.

Vous pouvez créer plusieurs sous-domaines web, mais seul le sous-domaine **par défaut** sera utilisé. Vous pouvez modifier le sous-domaine web par défaut, mais un seul sous-domaine peut être utilisé à la fois.

## Accéder à des sous-domaines web et les gérer {#access-web-subdomains}

Pour accéder aux sous-domaines pour les expériences web, procédez comme suit :

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**, puis sélectionnez **[!UICONTROL Paramètres web]** > **[!UICONTROL Sous-domaines web]**. Tous les sous-domaines configurés avec la sandbox actuelle s’affichent.

   ![](assets/web-access-subdomains.png)

1. Vous pouvez filtrer selon l’utilisateur ou l’utilisatrice qui a délégué chaque sous-domaine ou selon le statut de délégation (**[!UICONTROL Brouillon]**, **[!UICONTROL En cours de traitement]**, **[!UICONTROL Succès]** ou **[!UICONTROL Échec]**).

   ![](assets/web-filter-subdomains.png)

1. Le badge **[!UICONTROL Par défaut]** s’affiche en regard du sous-domaine actuellement utilisé par défaut. Pour modifier le sous-domaine par défaut, sélectionnez **[!UICONTROL Définir comme valeur par défaut]** en cliquant sur le bouton **[!UICONTROL Plus d’actions]** en regard du sous-domaine souhaité.

   ![](assets/web-subdomain-default.png)

   Vous pouvez modifier le sous-domaine web par défaut, mais un seul sous-domaine peut être utilisé à la fois.

## Utiliser un sous-domaine existant {#web-use-existing-subdomain}

Pour utiliser un sous-domaine déjà délégué à Adobe, procédez comme suit :

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**, puis sélectionnez **[!UICONTROL Paramètres web]** > **[!UICONTROL Sous-domaines web]**.

1. Cliquez sur **[!UICONTROL Configurer le sous-domaine]**.

1. Sélectionnez l’option **[!UICONTROL Utiliser un sous-domaine délégué]** de la section **[!UICONTROL Type de configuration]** et sélectionnez un sous-domaine délégué dans la liste.

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >Vous ne pouvez pas sélectionner un sous-domaine déjà utilisé comme sous-domaine web.

1. Le préfixe qui s’affichera dans votre URL web est automatiquement ajouté. Vous ne pouvez pas le modifier.

1. Pour définir ce sous-domaine par défaut, sélectionnez l’option correspondante.

   ![](assets/web-subdomain-details-default.png)

   Seul le sous-domaine **par défaut** sera utilisé.

1. Cliquez sur **[!UICONTROL Envoyer]**. Le sous-domaine obtient le statut **[!UICONTROL Succès]**. Il est prêt à être utilisé avec vos expériences web.

   Dans de très rares occasions, une configuration de sous-domaine peut échouer. Dans ce cas, vous pouvez supprimer le sous-domaine en **[!UICONTROL échec]** pour nettoyer la liste à l’aide du bouton **[!UICONTROL Supprimer]** à partir de l’icône **[!UICONTROL Plus d’actions]**.

## Configurer un nouveau sous-domaine {#web-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_web_subdomain_dns"
>title="Générer l’enregistrement DNS correspondant"
>abstract="Pour configurer un nouveau sous-domaine web, vous devez copier les informations du serveur de noms Adobe affichées dans l’interface de Journey Optimizer et les coller dans votre solution d’hébergement de domaine pour générer l’enregistrement DNS correspondant. Une fois les vérifications effectuées, le sous-domaine est prêt à être utilisé pour publier du contenu provenant de la bibliothèque Adobe Experience Manager Assets."

Par défaut, [!DNL Journey Optimizer] vous permet de déléguer **jusqu’à 10 sous-domaines** (canaux e-mail et web inclus). Cependant, en fonction de votre contrat de licence, vous pouvez déléguer jusqu’à 100 sous-domaines. Contactez votre personne référente chez Adobe pour connaître le nombre de sous-domaines auxquels vous avez droit.

Pour configurer un nouveau sous-domaine, procédez comme suit :

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**, puis sélectionnez **[!UICONTROL Paramètres web]** > **[!UICONTROL Sous-domaines web]**.

1. Cliquez sur **[!UICONTROL Configurer le sous-domaine]**.

1. Sélectionnez **[!UICONTROL Ajouter votre propre domaine]** de la section **[!UICONTROL Type de configuration]**.

1. Spécifiez le sous-domaine à déléguer.

   >[!CAUTION]
   >
   >* Vous ne pouvez pas utiliser un sous-domaine web existant.
   >
   >* Les majuscules ne sont pas autorisées dans les sous-domaines.

   ![](assets/web-add-your-own-domain.png)

   La délégation d’un sous-domaine non valide à Adobe n’est pas autorisée. Veillez à saisir un sous-domaine valide détenu par votre entreprise, tel que marketing.votre_entreprise.com.

   Les sous-domaines à plusieurs niveaux (du même domaine parent) sont pris en charge. Par exemple, vous pouvez utiliser « web.marketing.yourcompany.com ».

1. Pour définir ce sous-domaine par défaut, sélectionnez l’option correspondante.

   >[!NOTE]
   >
   >Seul le sous-domaine **par défaut** sera utilisé.

1. L’enregistrement à placer dans les serveurs DNS s’affiche. Copiez cet enregistrement ou téléchargez un fichier CSV, puis accédez à votre solution d’hébergement de domaine pour générer l’enregistrement DNS correspondant.

1. Assurez-vous que l’enregistrement DNS a été généré dans votre solution d’hébergement de domaine. Si tout est correctement configuré, cochez la case « Je confirme... », puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](assets/web-add-your-own-domain-confirm.png)

   Lorsque vous configurez un nouveau sous-domaine web, il pointe toujours vers un enregistrement CNAME.

1. Une fois la délégation de sous-domaine envoyée, le sous-domaine s&#39;affiche dans la liste avec le statut **[!UICONTROL Traitement]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](../configuration/delegate-subdomain.md#access-delegated-subdomains).<!--Same statuses?-->

   Avant d’utiliser ce sous-domaine pour envoyer des messages web, vous devez attendre qu’Adobe effectue les vérifications nécessaires, ce qui peut prendre **jusqu’à 4 heures**.

1. Une fois les vérifications effectuées, le sous-domaine obtient le statut **[!UICONTROL Succès]**. Vous pouvez à présent l’utiliser pour créer des configurations de canal web.

   Le statut du sous-domaine sera marqué comme en **[!UICONTROL Échec]** si la création de lʼenregistrement de validation sur votre solution dʼhébergement nʼa pas réussi.

<!--
Only a subdomain with the **[!UICONTROL Success]** status can be set as default.
You cannot delete a subdomain with the **[!UICONTROL Processing]** status.
-->

## Annuler la délégation d’un sous-domaine {#undelegate-subdomain}

Si vous souhaitez annuler la délégation d’un sous-domaine web, contactez votre représentant ou représentante Adobe en indiquant le sous-domaine pour lequel vous souhaitez annuler la délégation.

<!--
1. Deactivate all the channel configurations associated with the subdomain. [Learn how](../configuration/channel-surfaces.md#deactivate-a-surface)

1. Stop the active campaigns associated with the subdomains. [Learn how](../campaigns/manage-campaigns.md#stop)

1. Stop the active journeys associated with the subdomains. [Learn how](../building-journeys/end-journey.md#stop-journey)-->

Si le sous-domaine web était un [nouveau sous-domaine délégué](#web-configure-new-subdomain), vous pouvez supprimer l’enregistrement DNS CNAME que vous avez créé pour le sous-domaine web de votre solution d’hébergement (mais ne supprimez pas le sous-domaine d’e-mail d’origine, le cas échéant).

Une fois votre demande traitée par Adobe, le domaine dont la délégation a été annulée ne s’affiche plus sur la page d’inventaire des sous-domaines.
