---
solution: Journey Optimizer
product: journey optimizer
title: Exécution de la formule de chauffage des adresses IP
description: Découvrez comment exécuter et surveiller un plan de réchauffement des adresses IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, groupes, sous-domaines, délivrabilité
hide: true
hidefromtoc: true
source-git-commit: 11bdb3ddc666d2025133f70ab522c4ce2d676aa6
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 1%

---

# Exécution de la formule de chauffage des adresses IP {#ip-warmup-running}

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* [Prise en main du réchauffement des adresses IP](ip-warmup-gs.md)
* [Créer des campagnes de réchauffement des adresses IP](ip-warmup-campaign.md)
* [Créer une formule de chauffage des adresses IP](ip-warmup-plan.md)
* **[Exécution de la formule de chauffage des adresses IP](ip-warmup-running.md)**

>[!ENDSHADEBOX]

## Définition des phases {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Sélectionner les audiences de campagnes à exclure"
>abstract="Sélectionnez les audiences d’autres campagnes que vous souhaitez exclure de la phase en cours."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Sélectionner les groupes de domaines à exclure"
>abstract="Sélectionnez les domaines que vous souhaitez exclure de la phase actuelle."

Vous devez associer la campagne et l’audience au niveau de la phase et activer certains paramètres si nécessaire pour toutes les exécutions associées à une seule création/campagne.

Au niveau de la phase, le système s’assure que les profils précédemment ciblés + nouveaux sont sélectionnés ET au niveau de l’itération, le système s’assure que chaque exécution comporte des profils uniques et que le nombre correspond à ce qui est indiqué dans le plan.

1. Pour chaque phase, sélectionnez la campagne que vous souhaitez associer à cette phase du plan de réchauffement des adresses IP.

   ![](assets/ip-warmup-plan-select-campaign.png)

   Prenez note des points suivants :

   * Seules les campagnes avec la variable **[!UICONTROL Activation du plan de chauffage par IP]** option activée <!--and live?--> sont disponibles pour sélection. [En savoir plus](#create-ip-warmup-campaign)

   * Vous devez sélectionner une opération qui utilise la même surface que celle sélectionnée pour le plan de chaleur IP en cours.

   * Vous ne pouvez pas sélectionner une campagne qui est déjà utilisée dans une autre campagne de chaleur IP.

1. Dans le **[!UICONTROL Exclusion de profil]** , vous pouvez constater que les profils des exécutions précédentes de cette phase sont toujours exclus. Par exemple, si dans Exécuter #1 un profil est couvert dans les 4800 premières personnes ciblées, le système s’assure automatiquement que le même profil ne reçoit pas l’email dans Exécuter #2.

1. Dans la **[!UICONTROL Audiences de campagne exclues]** , sélectionnez les audiences d’autres <!--executed/live?-->campagnes que vous souhaitez exclure de la phase actuelle.

   ![](assets/ip-warmup-plan-exclude-campaigns.png)

   Par exemple, lors de l’exécution de la phase 1, vous deviez [fractionner](#split-phase) pour une raison quelconque. Par conséquent, vous pouvez exclure la campagne utilisée dans la phase 1 afin que les profils précédemment contactés de la phase 1 ne soient pas inclus dans la phase 2. Vous pouvez également exclure les campagnes des autres plans de chauffage par IP.

1. Dans la **[!UICONTROL Groupes de domaines exclus]** , sélectionnez les domaines à exclure de cette phase.

   ![](assets/ip-warmup-plan-exclude-domains.png)

   Par exemple, après avoir exécuté le réchauffement des adresses IP pendant quelques jours, vous réalisez que la réputation du FAI avec un domaine (c’est-à-dire un Adobe) n’est pas bonne et que vous souhaitez la résoudre sans arrêter votre plan de réchauffement des adresses IP. Dans ce cas, vous pouvez exclure le groupe de domaines Adobe.

   >[!NOTE]
   >
   >L’exclusion de domaine requiert une phase non exécutée, vous devrez peut-être donc diviser une phase d’exécution pour ajouter des exclusions. De même, si le groupe de domaines n’est pas un groupe de domaines prêt à l’emploi, vous devez l’ajouter au fichier Excel, le télécharger, puis exclure le domaine.

   ![](assets/ip-warmup-plan-phase-1.png)

1. Vous pouvez ajouter une phase, si nécessaire. Il sera ajouté après la dernière phase actuelle.

1. Utilisez la variable **[!UICONTROL Phase de suppression]** pour supprimer toute phase indésirable.

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >Vous ne pouvez pas annuler la **[!UICONTROL Supprimer]** action.
   >
   >Si vous supprimez toutes les phases du plan de chauffage par IP, nous vous recommandons de télécharger à nouveau un plan.

## Définition des exécutions {#define-runs}

1. Sélectionnez un planning pour chaque exécution. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. Sélectionnez une heure de fin, qui définit la fenêtre dans laquelle la campagne de chaleur IP peut être exécutée en cas de retard dans l’exécution des tâches de segmentation d’audience. Si aucune heure de fin n’est spécifiée, l’exécution est tentée au début et échoue si la segmentation n’est pas terminée.

1. Activez chaque exécution. Veillez à planifier une heure suffisamment tôt pour permettre l’exécution de la tâche de segmentation. <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >Chaque exécution doit être activée au moins 12 heures avant l’heure d’envoi réelle. Sinon, la segmentation risque de ne pas être terminée. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

   <!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. Si l&#39;exécution de la campagne n&#39;a pas démarré, vous pouvez arrêter une exécution.<!--why?-->

   >[!NOTE]
   >
   >Une fois l&#39;exécution de l&#39;opération démarrée, la variable **[!UICONTROL Arrêter]** n’est plus disponible. <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. Pour ajouter une exécution, sélectionnez **[!UICONTROL Ajoutez une exécution ci-dessous.]** à partir de l’icône de trois points.

   ![](assets/ip-warmup-plan-run-more-actions.png)

## Fractionner une phase {#split-phase}

À tout moment, si vous souhaitez utiliser une autre campagne à partir d’une exécution spécifique, sélectionnez la variable **[!UICONTROL Option Partager sur une nouvelle phase]** à partir de l’icône de trois points.

Une nouvelle phase est créée pour les exécutions restantes de la phase en cours. Suivez les étapes [above](#define-phases) pour définir la nouvelle phase.

Par exemple, si vous sélectionnez cette option pour Exécuter #4, Exécuter #4 sur #8 sera déplacé vers une nouvelle phase.

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

## Surveiller le plan

Une exécution peut avoir les états suivants :<!--TBC with Medha-->:

* **[!UICONTROL Terminé]**:
* **[!UICONTROL Échec]**:
* **[!UICONTROL Annulé]**: vous avez arrêté l&#39;exécution avant le démarrage de l&#39;exécution de la campagne.

Avantages :

* Les rapports continueront à s’afficher au niveau de la campagne avec des fonctionnalités similaires à celles d’aujourd’hui. Mais le plan de réchauffement des adresses IP sert également de rapport consolidé à un seul endroit du nombre d’exécutions effectuées, etc.

* Emplacement unique pour gérer et afficher l’avancement du réchauffement des adresses IP.

* Rapport consolidé au niveau de la création/de la campagne, car tous s’exécutent pour une phase