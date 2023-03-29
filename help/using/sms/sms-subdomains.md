---
solution: Journey Optimizer
product: journey optimizer
title: Configuration des sous-domaines SMS
description: Découvrez comment configurer des sous-domaines SMS avec Journey Optimizer
role: Admin
level: Intermediate
keywords: SMS, sous-domaines, configuration
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 48%

---

# Configuration des sous-domaines SMS {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms_header"
>title="Déléguer un sous-domaine SMS"
>abstract="Vous allez configurer votre sous-domaine pour l’utilisation des SMS. Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou en configurer un autre."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_sms"
>title="Déléguer un sous-domaine SMS"
>abstract="Vous devez configurer un sous-domaine à utiliser pour vos SMS, car vous aurez besoin de ce sous-domaine pour créer une surface SMS. Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou configurer un nouveau sous-domaine."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="Créer des surfaces SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_sms_subdomain"
>title="Sélectionner un sous-domaine SMS"
>abstract="Pour pouvoir créer une surface SMS, vérifiez que vous avez déjà configuré au moins un sous-domaine SMS à sélectionner dans la liste Nom de sous-domaine."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="Créer des surfaces SMS"

Pour pouvoir raccourcir les URL ajoutées à vos SMS, vous devez configurer le sous-domaine que vous allez sélectionner lors de la [création d&#39;une surface SMS](sms-configuration.md#message-preset-sms).

Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou en configurer un autre. En savoir plus sur la délégation de sous-domaines à Adobe dans [cette section](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>La configuration du sous-domaine SMS est commune à tous les environnements. Par conséquent :
>
>* Pour accéder aux sous-domaines SMS et les modifier, vous devez disposer de la variable **[!UICONTROL Gestion des sous-domaines SMS]** autorisation sur l’environnement de test de production.
>
> * Toute modification apportée à un sous-domaine SMS aura également un impact sur les environnements de test de production.


## Utiliser un sous-domaine existant {#sms-use-existing-subdomain}

Pour utiliser un sous-domaine déjà délégué à Adobe, procédez comme suit.

1. Accédez au **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** , puis sélectionnez **[!UICONTROL Configuration des SMS]** > **[!UICONTROL Sous-domaines SMS]**.

   ![](assets/sms_access-subdomains.png)

1. Cliquez sur **[!UICONTROL Configurer le sous-domaine]**.

   ![](assets/sms_set-up-subdomain.png)

1. Sélectionner **[!UICONTROL Utiliser un sous-domaine délégué]** de la **[!UICONTROL Type de configuration]** .

   ![](assets/sms_use-delegated-subdomain.png)

1. Saisissez le préfixe qui s&#39;affichera dans votre URL SMS.

   >[!NOTE]
   >
   >Seuls les caractères alphanumériques et les tirets sont autorisés.

1. Sélectionnez un sous-domaine délégué dans la liste.

   >[!NOTE]
   >
   >Vous ne pouvez pas sélectionner un sous-domaine déjà utilisé comme sous-domaine SMS.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/sms_prefix-and-subdomain.png)

   <!--Note that you cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your SMS messages, you will not be able to use 'marketing2.yourcompany.com'. However, multi-level subdomains being supported for SMS, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.-->

   >[!CAUTION]
   >
   >Si vous sélectionnez un domaine qui a été délégué à Adobe à l’aide de la [méthode CNAME](../configuration/delegate-subdomain.md#cname-subdomain-delegation), vous devez créer l’enregistrement DNS sur votre plateforme d’hébergement. Pour générer l’enregistrement DNS, le processus est le même que lorsque vous configurez un nouveau sous-domaine SMS. Découvrez comment dans [cette section](#sms-configure-new-subdomain).

1. Cliquez sur **[!UICONTROL Envoyer]**.

1. Une fois envoyé, le sous-domaine s’affiche dans la liste avec le statut du **[!UICONTROL Traitement]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >Avant de pouvoir utiliser ce sous-domaine pour envoyer des messages, vous devez attendre qu’Adobe effectue les vérifications nécessaires, ce qui peut prendre jusqu’à 4 heures.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Une fois les vérifications effectuées, le sous-domaine obtient le statut **[!UICONTROL Succès]**. Il est prêt à être utilisé pour créer des surfaces de canal SMS.

## Configurer un nouveau sous-domaine {#sms-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_subdomain_dns"
>title="Générer l’enregistrement DNS correspondant"
>abstract="Pour configurer un nouveau sous-domaine SMS, vous devez copier les informations du serveur de noms d’Adobe affichées dans l’interface de Journey Optimizer et les coller dans votre solution d’hébergement de domaine pour générer l’enregistrement DNS correspondant. Une fois les vérifications effectuées, le sous-domaine est prêt à être utilisé pour créer des surfaces SMS."

Pour configurer un nouveau sous-domaine, procédez comme suit :

1. Accédez au **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** , puis sélectionnez **[!UICONTROL Configuration des SMS]** > **[!UICONTROL Sous-domaines SMS]**.

1. Cliquez sur **[!UICONTROL Configurer un sous-domaine]**.

1. Sélectionnez **[!UICONTROL Ajouter votre propre domaine]** de la section **[!UICONTROL Type de configuration]**.

   ![](assets/sms_add-your-own-subdomain.png)

1. Spécifiez le sous-domaine à déléguer.

   >[!CAUTION]
   >
   >Vous ne pouvez pas utiliser un sous-domaine SMS existant.
   >
   >Les majuscules ne sont pas autorisées dans les sous-domaines.

   La délégation d’un sous-domaine non valide à Adobe n’est pas autorisée. Veillez à saisir un sous-domaine valide détenu par votre entreprise, tel que marketing.votre_entreprise.com.

   >[!NOTE]
   >
   >Les sous-domaines de plusieurs niveaux (du même domaine parent) sont pris en charge. Par exemple, vous pouvez utiliser &quot;sms.marketing.votreentreprise.com&quot;.

1. L’enregistrement à placer dans les serveurs DNS s’affiche. Copiez cet enregistrement ou téléchargez un fichier CSV, puis accédez à votre solution d’hébergement de domaine pour générer l’enregistrement DNS correspondant.

1. Assurez-vous que l’enregistrement DNS a été généré dans votre solution d’hébergement de domaine. Si tout est correctement configuré, cochez la case « Je confirme... », puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](assets/sms_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Lorsque vous configurez un nouveau sous-domaine SMS, il pointe toujours vers un enregistrement CNAME.

1. Une fois la délégation de sous-domaine envoyée, le sous-domaine s&#39;affiche dans la liste avec le statut **[!UICONTROL Traitement]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >Avant de pouvoir utiliser ce sous-domaine pour envoyer des SMS, vous devez attendre que l’Adobe effectue les vérifications requises, qui peuvent prendre jusqu’à 4 heures.<!--Learn more in [this section](#subdomain-validation).-->

1. Une fois les vérifications effectuées, le sous-domaine obtient le statut **[!UICONTROL Succès]**. Il est prêt à être utilisé pour créer des surfaces de canal SMS.

   Le statut du sous-domaine sera marqué comme en **[!UICONTROL Échec]** si la création de lʼenregistrement de validation sur votre solution dʼhébergement nʼa pas réussi.
