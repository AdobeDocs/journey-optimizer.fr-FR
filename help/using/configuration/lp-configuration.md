---
title: Configuration des pages de destination
description: Découvrez comment configurer votre environnement pour créer et utiliser des pages de destination avec Journey Optimizer.
role: Admin
level: Intermediate
exl-id: 7cf1f083-bef0-40b5-8ddd-920a9d108eca
source-git-commit: e9878246c2af5c7ee0f961aaaad64e186431d96e
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 96%

---

# Configurer des pages de destination {#lp-configuration}

## Configurer les sous-domaines des pages de destination {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="Créer un préréglage de page de destination"
>abstract="Pour pouvoir créer un paramètre prédéfini de page d’entrée, vérifiez que vous avez déjà configuré au moins un sous-domaine de page d’entrée à sélectionner dans la liste Nom de sous-domaine."

Avant de pouvoir [créer des préréglages de page de destination](#lp-create-preset), vous devez avoir configuré les sous-domaines que vous utiliserez pour vos pages de destination.

Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou en configurer un autre. En savoir plus sur la délégation de sous-domaines à Adobe dans [cette section](delegate-subdomain.md).

### Utiliser un sous-domaine existant {#lp-use-existing-subdomain}

Pour utiliser un sous-domaine déjà délégué à Adobe, procédez comme suit.

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**, puis sélectionnez **[!UICONTROL Configuration du canal e-mail]** > **[!UICONTROL Sous-domaines de la page de destination]**.

   ![](assets/lp_access-subdomains.png)

1. Cliquez sur **[!UICONTROL Configurer le sous-domaine]**.

   ![](assets/lp_set-up-subdomain.png)

1. Sélectionnez **[!UICONTROL Utiliser le domaine délégué]** dans la section **[!UICONTROL Type de configuration]**.

   ![](assets/lp_use-delegated-subdomain.png)

1. Saisissez le préfixe qui sʼaffichera dans lʼURL de votre page de destination.

   >[!NOTE]
   >
   >Seuls les caractères alphanumériques et les tirets sont autorisés.

1. Sélectionnez un sous-domaine délégué dans la liste.

   >[!NOTE]
   >
   >Vous ne pouvez pas sélectionner un sous-domaine déjà utilisé comme sous-domaine de page de destination.

   ![](assets/lp_prefix-and-subdomain.png)

   >[!CAUTION]
   >
   >Si vous sélectionnez un domaine qui a été délégué à Adobe à l’aide de la [méthode CNAME](delegate-subdomain.md#cname-subdomain-delegation), vous devez créer l’enregistrement DNS sur votre plateforme d’hébergement. Pour générer l’enregistrement DNS, le processus est le même que lorsque vous configurez un nouveau sous-domaine de page de destination. Découvrez comment dans [cette section](#lp-configure-new-subdomain).

1. Cliquez sur **[!UICONTROL Envoyer]**.

1. Une fois envoyé, le sous-domaine s’affiche dans la liste avec le statut du **[!UICONTROL Traitement]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](access-subdomains.md).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >Avant de pouvoir utiliser ce sous-domaine pour envoyer des messages, vous devez attendre qu’Adobe effectue les vérifications nécessaires, ce qui peut prendre jusqu’à 4 heures.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Une fois les vérifications effectuées, le sous-domaine obtient le statut **[!UICONTROL Succès]**. Il est prêt à être utilisé pour créer des préréglages de page de destination.

### Configurer un nouveau sous-domaine           {#lp-configure-new-subdomain}

Pour configurer un nouveau sous-domaine, procédez comme suit :

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**, puis sélectionnez **[!UICONTROL Configuration du canal e-mail]** > **[!UICONTROL Sous-domaines des pages de destination]**.

1. Cliquez sur **[!UICONTROL Configurer un sous-domaine]**.

1. Sélectionnez **[!UICONTROL Ajouter votre propre domaine]** de la section **[!UICONTROL Type de configuration]**.

   ![](assets/lp_add-your-own-subdomain.png)

1. Spécifiez le sous-domaine à déléguer.

   >[!CAUTION]
   >
   >Vous ne pouvez pas utiliser un sous-domaine de page de destination existant.

   La délégation d’un sous-domaine non valide à Adobe n’est pas autorisée. Veillez à saisir un sous-domaine valide détenu par votre entreprise, tel que marketing.votre_entreprise.com.

   Veuillez noter que les sous-domaines à plusieurs niveaux tels qu’email.marketing.votre_entreprise.com ne sont actuellement pas pris en charge.

1. L’enregistrement à placer dans les serveurs DNS s’affiche. Copiez cet enregistrement ou téléchargez un fichier CSV, puis accédez à votre solution d’hébergement de domaine pour générer l’enregistrement DNS correspondant.

1. Assurez-vous que l’enregistrement DNS a été généré dans votre solution d’hébergement de domaine. Si tout est correctement configuré, cochez la case « Je confirme... », puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Lorsque vous configurez un nouveau sous-domaine de page de destination, il pointe toujours vers un enregistrement CNAME.

1. Une fois la délégation de sous-domaine envoyée, le sous-domaine s&#39;affiche dans la liste avec le statut **[!UICONTROL Traitement]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](access-subdomains.md).<!--Same statuses?-->

   >[!NOTE]
   >
   >Avant de pouvoir utiliser ce sous-domaine pour envoyer des messages, vous devez attendre qu’Adobe effectue les vérifications nécessaires, ce qui peut prendre jusqu’à 4 heures.<!--Learn more in [this section](#subdomain-validation).-->

1. Une fois les vérifications effectuées, le sous-domaine obtient le statut **[!UICONTROL Succès]**. Il est prêt à être utilisé pour créer des préréglages de page de destination.

   Le statut du sous-domaine sera marqué comme en **[!UICONTROL Échec]** si la création de lʼenregistrement de validation sur votre solution dʼhébergement nʼa pas réussi.

## Définir les préréglages de page de destination {#lp-define-preset}

Lors de la [conception dʼune page de destination](../landing-pages/create-lp.md#create-a-lp), vous devez sélectionner un préréglage de page de destination pour pouvoir créer la page de destination et lʼutiliser avec **[!DNL Journey Optimizer]**.

### Accéder aux préréglages de la page de destination {#lp-presets}

Pour accéder aux préréglages de la page de destination, procédez comme suit.

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**.

1. Sélectionnez **[!UICONTROL Marques]** > **[!UICONTROL Préréglages de page de destination]**.

   ![](assets/lp_presets-access.png)

1. Cliquez sur un libellé de préréglage de page de destination pour consulter ses détails.

   ![](assets/lp_preset-details.png)

### Créer un préréglage de page de destination {#lp-create-preset}

Pour créer un préréglage de page de destination, procédez comme suit.

>[!NOTE]
>
>Avant de pouvoir créer un préréglage, vous devez avoir configuré au moins un sous-domaine de la page de destination. [Voici comment procéder](#lp-subdomains)

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**, puis sélectionnez **[!UICONTROL Branding]** > **[!UICONTROL Préréglages de page de destination]**.

1. Sélectionnez **[!UICONTROL Créer un préréglage de page de destination]**.

   ![](assets/lp_create-preset-temp.png)

1. Saisissez un nom et une description pour le préréglage.

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Sélectionnez un sous-domaine de page de destination dans la liste déroulante.

   ![](assets/lp_preset-subdomain.png)

   >[!NOTE]
   >
   >Avant de pouvoir sélectionner un sous-domaine, vous devez avoir configuré au moins un sous-domaine de page de destination. [Voici comment procéder](#lp-subdomains)

   Les paramètres correspondant au sous-domaine sélectionné s’affichent.

1. Si vous souhaitez sélectionner le sous-domaine de page de destination comme URL de tracking, cochez lʼoption **[!UICONTROL Identique au sous-domaine de la page de destination]**. [En savoir plus sur le tracking.](../messages/message-tracking.md)

   ![](assets/lp_preset-subdomain-settings-same.png)

   Par exemple, si l’URL de la page de destination est « pages.mail.luma.com » et que lʼURL de tracking est « data.mail.luma.com », vous pouvez choisir « pages.mail.luma.com » comme sous-domaine de tracking.

1. Cliquez sur **[!UICONTROL Envoyer]** pour confirmer la création du préréglage de page de destination. Vous pouvez également enregistrer le préréglage en tant que brouillon et reprendre sa configuration ultérieurement.

   ![](assets/lp_preset-subdomain-settings-submit.png)

1. Une fois le préréglage de page de destination créé, il sʼaffiche dans la liste avec le statut **[!UICONTROL Actif]**. Il est prêt à être utilisé avec vos pages de destination.

   ![](assets/lp-preset-active-temp.png)

Vous êtes maintenant prêt à [créer des pages de destination](../landing-pages/create-lp.md) dans [!DNL Journey Optimizer].

>[!NOTE]
>
>Découvrez comment créer des préréglages de message pour les notifications push et les e-mails dans [cette section](message-presets.md).

**Rubriques connexes** :

* [Prise en main des pages de destination](../landing-pages/get-started-lp.md)
* [Création d’une page de destination](../landing-pages/create-lp.md#create-a-lp)
