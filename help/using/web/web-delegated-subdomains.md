---
solution: Journey Optimizer
product: journey optimizer
title: Configurer des sous-domaines web
description: Découvrez comment configurer des sous-domaines web avec Journey Optimizer
role: Admin
level: Intermediate
keywords: web, sous-domaines, configuration
exl-id: 6503d9e6-6c6c-4a6d-ad3d-1d81eb3b4698
source-git-commit: 29070f0029c092782cf8a304f85e52869598a2fa
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 7%

---

# Configurer des sous-domaines web {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Délégation d’un sous-domaine web"
>abstract="Vous allez configurer votre sous-domaine pour une utilisation avec le canal web. Faites votre choix parmi les sous-domaines déjà délégués à Adobe."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Délégation d’un sous-domaine web"
>abstract="Si vous ajoutez du contenu provenant de Adobe Experience Manager Assets Essentials à vos expériences web, vous devez configurer le sous-domaine qui sera utilisé pour publier ce contenu. Sélectionnez parmi les sous-domaines déjà délégués à l’Adobe."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Définition d’un sous-domaine web"
>abstract="Sélectionnez un sous-domaine dans la liste des sous-domaines délégués à l’Adobe. Vous pouvez définir ce sous-domaine web comme sous-domaine par défaut, mais un seul sous-domaine par défaut peut être utilisé à la fois."

Lors de la création d’expériences web, si vous ajoutez du contenu provenant du [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) , vous devez configurer le sous-domaine qui sera utilisé pour publier ce contenu.

Pour ce faire, vous devez effectuer une sélection dans la liste des sous-domaines déjà délégués à Adobe. En savoir plus sur la délégation de sous-domaines à Adobe dans [cette section](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>La configuration des sous-domaines web est commune à tous les environnements. Par conséquent :
>
>* Pour accéder aux sous-domaines web et les modifier, vous devez disposer de la variable **[!UICONTROL Gestion des sous-domaines web]** autorisation sur l’environnement de test de production.
>
> * Toute modification apportée à un sous-domaine web aura également un impact sur les environnements de test de production.


Vous pouvez créer plusieurs sous-domaines web, mais uniquement le **default** Le sous-domaine sera utilisé. Vous pouvez modifier le sous-domaine web par défaut, mais un seul peut être utilisé à la fois.

1. Accédez au **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** , puis sélectionnez **[!UICONTROL Configuration web]** > **[!UICONTROL Sous-domaines web]**.

   ![](assets/web-access-subdomains.png)

1. Cliquez sur **[!UICONTROL Configurer le sous-domaine]**.

1. Sélectionnez un sous-domaine délégué dans la liste.

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >Vous ne pouvez pas sélectionner un sous-domaine déjà utilisé comme sous-domaine web.

1. Pour définir ce sous-domaine par défaut, sélectionnez l’option correspondante.

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >Seule la variable **default** Le sous-domaine sera utilisé.

1. Cliquez sur **[!UICONTROL Envoyer]**. Le sous-domaine récupère la variable **[!UICONTROL Succès]** statut. Il est prêt à être utilisé pour vos expériences web.

1. Le **[!UICONTROL Par défaut]** badge s’affiche en regard du sous-domaine actuellement utilisé par défaut. Pour modifier le sous-domaine par défaut, sélectionnez **[!UICONTROL Définir comme valeur par défaut]** de la **[!UICONTROL Autres actions]** en regard du sous-domaine souhaité.

   >[!NOTE]
   >
   >Vous pouvez modifier le sous-domaine web par défaut, mais un seul peut être utilisé à la fois.

   ![](assets/web-subdomain-default.png)

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.-->

1. Vous pouvez uniquement supprimer une **[!UICONTROL En échec]** sous-domaine pour nettoyer la liste. Pour ce faire, sélectionnez **[!UICONTROL Supprimer]** de la **[!UICONTROL Autres actions]** en regard du sous-domaine souhaité.

<!--You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->
