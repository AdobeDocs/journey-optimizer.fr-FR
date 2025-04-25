---
solution: Journey Optimizer
product: journey optimizer
title: Configurer des sous-domaines pour les messages texte (SMS/MMS)
description: Découvrez comment configurer des sous-domaines SMS avec Journey Optimizer
role: Admin
feature: SMS, Channel Configuration
level: Intermediate
keywords: SMS, sous-domaines, configuration
exl-id: 08a546d1-060c-43e8-9eac-4c38945cc3e1
source-git-commit: 19f127c2abc81239abda8ebd38bdcacee796a1b0
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 70%

---

# Configurer des sous-domaines SMS {#sms-mms-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms_header"
>title="Déléguer un sous-domaine SMS/MMS"
>abstract="Configurez votre sous-domaine pour les messages texte (SMS/MMS). Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou en configurer un nouveau."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms"
>title="Déléguer un sous-domaine SMS/MMS"
>abstract="Vous devez configurer un sous-domaine dédié aux messages texte, car vous en aurez besoin pour créer une configuration des SMS. Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou en configurer un nouveau."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Créer une configuration des SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_sms_subdomain"
>title="Sélectionner un sous-domaine SMS/MMS"
>abstract="Avant de créer une configuration des SMS, vous devez déjà avoir configuré au moins un sous-domaine SMS, que vous pouvez sélectionner dans la liste des noms de sous-domaines."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Créer une configuration des SMS"

## Prise en main des sous-domaines SMS {#gs-sms-mms-subdomains}

Pour pouvoir raccourcir les URL ajoutées à vos SMS/MMS, vous devez configurer le sous-domaine qui sera utilisé lors de la [création d&#39;une configuration SMS](sms-configuration.md#message-preset-sms).

Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou en configurer un autre. En savoir plus sur la délégation de sous-domaines à Adobe dans [cette section](../configuration/delegate-subdomain.md).

La configuration du sous-domaine SMS est **partagée entre tous les environnements**. Par conséquent, toute modification apportée à un sous-domaine aura également un impact sur les sandbox de production.

Pour accéder aux sous-domaines SMS et les modifier, vous devez disposer de l’autorisation **[!UICONTROL Gestion des sous-domaines SMS]** dans le sandbox de production. Pour en savoir plus sur les autorisations, consultez [cette section](../administration/high-low-permissions.md).

## Utiliser un sous-domaine existant {#sms-use-existing-subdomain}

Pour utiliser un sous-domaine déjà délégué à Adobe, procédez comme suit.

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**, puis sélectionnez **[!UICONTROL Paramètres des SMS]** > **[!UICONTROL Sous-domaines SMS]**.

1. Cliquez sur **[!UICONTROL Configurer le sous-domaine]**.

   ![](assets/sms_set-up-subdomain.png)

1. Sélectionnez **[!UICONTROL Utiliser le sous-domaine délégué]** dans la section **[!UICONTROL Type de configuration]**.

   ![](assets/sms_use-delegated-subdomain.png)

1. Saisissez le préfixe qui sʼaffichera dans lʼURL de votre SMS.

   Seuls les caractères alphanumériques et les tirets sont autorisés.

1. Sélectionnez un sous-domaine délégué dans la liste.

   Vous ne pouvez pas sélectionner un sous-domaine déjà utilisé comme sous-domaine SMS.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >Si vous sélectionnez un domaine qui a été délégué à Adobe à l’aide de la [méthode CNAME](../configuration/delegate-subdomain.md#cname-subdomain-delegation), vous devez créer l’enregistrement DNS sur votre plateforme d’hébergement. Pour générer l’enregistrement DNS, le processus est le même que lorsque vous configurez un nouveau sous-domaine SMS. Découvrez comment dans [cette section](#sms-configure-new-subdomain).

1. Cliquez sur **[!UICONTROL Envoyer]**.

1. Une fois envoyé, le sous-domaine s’affiche dans la liste avec le statut du **[!UICONTROL Traitement]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   Avant de pouvoir utiliser ce sous-domaine pour envoyer des messages, vous devez attendre qu’Adobe effectue les vérifications nécessaires, ce qui peut prendre **jusqu’à 4 heures**.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Une fois les vérifications effectuées, le sous-domaine obtient le statut **[!UICONTROL Succès]**. Vous pouvez à présent l’utiliser pour créer des configurations de canal SMS.

## Configurer un nouveau sous-domaine {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="Générer l’enregistrement DNS correspondant"
>abstract="Pour configurer un nouveau sous-domaine SMS, vous devez copier les informations du serveur de noms Adobe affichées dans l’interface de Journey Optimizer et les coller dans votre solution d’hébergement de domaine pour générer l’enregistrement DNS correspondant. Une fois les contrôles effectués, le sous-domaine est prêt à être utilisé pour créer des configurations SMS."

Pour configurer un nouveau sous-domaine, procédez comme suit.

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**, puis sélectionnez **[!UICONTROL Paramètres des SMS]** > **[!UICONTROL Sous-domaines SMS]**.

1. Cliquez sur **[!UICONTROL Configurer un sous-domaine]**.

   ![](assets/sms_set-up-subdomain.png)

1. Sélectionnez **[!UICONTROL Ajouter votre propre domaine]** de la section **[!UICONTROL Type de configuration]**.

   ![](assets/sms_add-your-own-subdomain.png)

1. Spécifiez le sous-domaine à déléguer.

   >[!CAUTION]
   >
   >* Vous ne pouvez pas utiliser un sous-domaine SMS existant.
   >
   >* Les majuscules ne sont pas autorisées dans les sous-domaines.

   La délégation d’un sous-domaine non valide à Adobe n’est pas autorisée. Veillez à saisir un sous-domaine valide détenu par votre entreprise, tel que marketing.votre_entreprise.com.

   Les sous-domaines à plusieurs niveaux (du même domaine parent) sont pris en charge. Par exemple, vous pouvez utiliser « sms.marketing.yourcompany.com ».

1. L’enregistrement à placer dans les serveurs DNS s’affiche. Copiez cet enregistrement ou téléchargez un fichier CSV, puis accédez à votre solution d’hébergement de domaine pour générer l’enregistrement DNS correspondant.

1. Assurez-vous que l’enregistrement DNS a été généré dans votre solution d’hébergement de domaine. Si tout est correctement configuré, cochez la case « Je confirme... », puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   Lorsque vous configurez un nouveau sous-domaine SMS, il pointe toujours vers un enregistrement CNAME.

1. Une fois la délégation de sous-domaine envoyée, le sous-domaine s&#39;affiche dans la liste avec le statut **[!UICONTROL Traitement]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

Avant de pouvoir utiliser un sous-domaine pour envoyer des messages SMS, vous devez attendre qu’Adobe effectue les vérifications nécessaires, ce qui peut prendre jusqu’à 4 heures.<!--Learn more in [this section](#subdomain-validation).-->Une fois les vérifications effectuées, le sous-domaine obtient le statut **[!UICONTROL Succès]**. Vous pouvez à présent l’utiliser pour créer des configurations de canal SMS.

Le statut du sous-domaine sera marqué comme en **[!UICONTROL Échec]** si la création de lʼenregistrement de validation sur votre solution dʼhébergement nʼa pas réussi.

## Annulation de la délégation d’un sous-domaine {#undelegate-subdomain}

Si vous souhaitez annuler la délégation d’un sous-domaine SMS, contactez votre représentant Adobe.

Cependant, vous devez effectuer plusieurs étapes dans l’interface utilisateur avant de contacter Adobe.

>[!NOTE]
>
>Vous pouvez uniquement annuler la délégation de sous-domaines avec le statut **[!UICONTROL Succès]**. Les sous-domaines avec les statuts **[!UICONTROL Brouillon]** et **[!UICONTROL Échec]** peuvent simplement être supprimés de l’interface utilisateur.

Tout d’abord, effectuez les étapes suivantes dans [!DNL Journey Optimizer] :

1. Désactivez toutes les configurations de canal associées au sous-domaine. [Voici comment procéder](../configuration/channel-surfaces.md#deactivate-a-surface)

<!--
1. If the SMS subdomain is using an email subdomain that was [already delegated](#lp-use-existing-subdomain) to Adobe, undelegate the email subdomain. [Learn how](../configuration/delegate-subdomain.md#undelegate-subdomain)-->

1. Arrêtez les campagnes actives associées aux sous-domaines. [Voici comment procéder](../campaigns/modify-stop-campaign.md#stop)

1. Arrêtez les parcours actifs associés aux sous-domaines. [Voici comment procéder](../building-journeys/end-journey.md#stop-journey)

1. Si le sous-domaine SMS était un [nouveau sous-domaine délégué](#sms-configure-new-subdomain), supprimez les entrées DNS associées à ce sous-domaine.

Une fois cette opération terminée, contactez votre représentant Adobe avec le sous-domaine dont vous souhaitez annuler la délégation.

Une fois que votre demande est gérée par Adobe, le domaine non délégué ne s’affiche plus sur la page d’inventaire des sous-domaines.

>[!CAUTION]
>
>Après la suppression de la délégation d’un sous-domaine :
>
>   * Vous ne pouvez pas réactiver les configurations de canal qui utilisaient ce sous-domaine.
>   * Vous ne pouvez pas déléguer à nouveau le sous-domaine exact via l’interface utilisateur. Si vous souhaitez le faire, contactez votre représentant ou représentante Adobe.
