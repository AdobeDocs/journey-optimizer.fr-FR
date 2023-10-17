---
solution: Journey Optimizer
product: journey optimizer
title: Créer un plan de préchauffage d’adresses IP
description: Découvrez comment créer un plan de préchauffage d’adresses IP dans Journey Optimizer.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: IP, groupe, sous-domaines, délivrabilité
hide: true
hidefromtoc: true
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: 82c189545ab4f37a2e4b1044c0b8cfeb539aed13
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 97%

---

# Créer un plan de préchauffage d’adresses IP {#ip-warmup}

>[!BEGINSHADEBOX]

Ce guide couvre les sujets suivants :

* [Commencer avec le préchauffage d’adresses IP](ip-warmup-gs.md)
* [Créer des campagnes de préchauffage d’adresses IP](ip-warmup-campaign.md)
* **[Créer un plan de préchauffage d’adresses IP](ip-warmup-plan.md)**
* [Exécuter le plan de préchauffage d’adresses IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Une fois que vous avez créé une ou plusieurs [campagnes de préchauffage d’adresses IP](ip-warmup-campaign.md) avec une surface dédiée et l’option correspondante activée, vous pouvez commencer à créer votre plan de préchauffage d’adresses IP.

## Préparer un fichier de plan de préchauffage d’adresses IP {#prepare-file}

Le préchauffage d’adresses IP est une activité qui consiste à augmenter progressivement le volume d’e-mails qui sortent de vos adresses IP et domaine vers les principaux fournisseurs d’accès à Internet (FAI), afin d’établir votre réputation d’expéditeur légitime.

Cette activité est réalisée en temps opportun avec l’aide d’un spécialiste en délivrabilité qui contribue à la préparation d’un plan bien conçu basé sur les domaines du secteur, les cas d’utilisation, les régions, les FAI et d’autres facteurs.

Lorsque vous utilisez la fonctionnalité de préchauffage d’adresses IP [!DNL Journey Optimizer], ce plan prend la forme d&#39;un fichier Excel qui doit contenir un certain nombre de colonnes prédéfinies. Avant de pouvoir créer un plan de préchauffage d’adresses IP dans l’interface [!DNL Journey Optimizer], vous devez renseigner ce modèle avec toutes les données qui alimenteront votre plan.

>[!CAUTION]
>
>Collaborez avec votre consultant ou consultante en délivrabilité pour vous assurer que votre fichier de plan de préchauffage d’adresses IP est correctement configuré.

Vous trouverez ci-dessous un exemple de fichier contenant un plan de préchauffage d’adresses IP.

![](assets/ip-warmup-sample-file.png)

### Onglet Plan de préchauffage d’adresses IP

* Dans cet exemple, un plan a été préparé sur 17 jours (appelé « **exécutions** ») pour atteindre un volume cible de plus d’un million de profils.

* Ce plan est exécuté en 6 **phases**, chacune d’elles contenant au moins une exécution.

* Vous pouvez avoir autant de colonnes que vous le souhaitez pour les domaines sur lesquels vous souhaitez envoyer des messages. Dans cet exemple, le plan est divisé en 6 colonnes : 5 correspondent aux **groupes de domaines principaux** à utiliser dans votre plan (Gmail, Microsoft, Yahoo, Orange et Apple) et la sixième colonne, **Autres**, contient toutes les adresses restantes d’autres domaines.
* La colonne **Jours d’engagement** indique que seuls les profils impliqués dans votre marque au cours des 30 derniers jours sont ciblés.

L’idée est d’augmenter progressivement le nombre d’adresses ciblées au cours de chaque exécution, tout en réduisant le nombre d’exécutions pour chaque phase.

Les groupes de domaines principaux prêts à l’emploi que vous pouvez ajouter à votre plan sont répertoriés ci-dessous :

* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigpond
* Orange
* Softbank
* Docomo
* United Internet
* Microsoft
* KDDI
* Italia Online
* La Poste
* Apple

### Onglet Groupe de domaines personnalisés

Vous pouvez également ajouter d’autres colonnes à votre plan en incluant des groupes de domaines personnalisés.

Utilisez l’onglet **[!UICONTROL Groupe de domaines personnalisés]** pour définir un nouveau groupe de domaines. Pour chaque domaine, vous pouvez ajouter tous les sous-domaines qu’il couvre.<!--TBC-->

Par exemple, si vous ajoutez le domaine personnalisé Luma, vous souhaitez inclure les sous-domaines suivants : luma.com, luma.co.uk, luma.it, luma.fr, luma.de, etc.

![](assets/ip-warmup-sample-file-custom.png)

## Accéder à des plans de préchauffage d’adresses IP et les gérer {#manage-ip-warmup-plans}

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Plans de préchauffage d’adresses IP]**. Tous les plans de préchauffage d’adresses IP créés jusqu’à présent s’affichent.

   ![](assets/ip-warmup-filter-list.png)

1. Vous pouvez filtrer par statut. Les différents statuts sont les suivants :

   * **Pas démarré** : aucune exécution n’a été activée pour le moment. [En savoir plus](ip-warmup-execution.md#define-runs)
   * **Actif** : le plan passe à ce statut dès que la première exécution de la première phase a été activée avec succès. [En savoir plus](ip-warmup-execution.md#define-runs)
   * **Terminé** : le plan a été marqué comme terminé. Cette option n’est disponible que si toutes les exécutions du plan sont incluses dans **[!UICONTROL Terminé]** ou **[!UICONTROL Version préliminaire]** status (aucune exécution ne peut être exécutée. **[!UICONTROL En direct]**). [En savoir plus](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. Pour supprimer un plan de préchauffage d’adresses IP, sélectionnez l’icône **[!UICONTROL Supprimer]** en regard du nom d’un plan et confirmez la suppression.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >Le plan de préchauffage d’adresses IP sélectionné sera définitivement supprimé.

## Créer un plan de préchauffage d’adresses IP {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Définir votre plan de préchauffage d’adresses IP"
>abstract="Téléchargez le modèle CSV et renseignez-le avec des données pour les phases de préchauffage d’adresses IP et le nombre cible de profils."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Sélectionner une surface marketing"
>abstract="Vous devez sélectionner la même surface que celle sélectionnée dans la campagne que vous souhaitez associer à votre plan de préchauffage d’adresses IP."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=fr" text="Configurer des surfaces de canal"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=fr" text="Créer des campagnes de préchauffage d’adresses IP"

Lorsqu’une ou plusieurs campagnes actives avec l’option **[!UICONTROL Activation du plan de préchauffage d’adresses IP]** sont activées, vous pouvez les associer à un plan de préchauffage d’adresses IP.

>[!CAUTION]
>
>Pour créer, modifier et supprimer des plans de préchauffage d’adresses IP, vous devez disposer de l’autorisation **[!UICONTROL Consultant ou consultante en délivrabilité]**. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Plans de préchauffage d’adresses IP]**, puis cliquez sur **[!UICONTROL Créer un plan de préchauffage d’adresses IP]**.

   ![](assets/ip-warmup-create-plan.png)

1. Renseignez les détails du plan de préchauffage d’adresses IP : attribuez-lui un nom et une description.

   ![](assets/ip-warmup-plan-details.png)

1. Sélectionnez une [surface](channel-surfaces.md). Seules les surfaces marketing peuvent être sélectionnées. [En savoir plus sur le type d’e-mail](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >Vous devez sélectionner la même surface que celle sélectionnée dans la campagne que vous souhaitez associer à votre plan de préchauffage d’adresses IP. [Découvrez comment créer une campagne de préchauffage d’adresses IP](ip-warmup-campaign.md).

1. Chargez le fichier Excel contenant votre plan de préchauffage d’adresses IP. [En savoir plus](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. Cliquez sur **[!UICONTROL Créer]**. Toutes les phases, les exécutions, les colonnes et leur contenu définis dans le fichier que vous avez chargé sont automatiquement affichés dans l’interface de [!DNL Journey Optimizer]. [En savoir plus](ip-warmup-execution.md)

   ![](assets/ip-warmup-plan-uploaded.png)
