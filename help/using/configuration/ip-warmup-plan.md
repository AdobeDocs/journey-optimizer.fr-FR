---
solution: Journey Optimizer
product: journey optimizer
title: Créer une formule de chauffage des adresses IP
description: Découvrez comment créer un plan de chauffage par IP dans Journey Optimizer
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, groupe, sous-domaines, délivrabilité
hide: true
hidefromtoc: true
source-git-commit: b3e5a825b881736516b3bcd1d368843c3a601100
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 5%

---

# Créer une formule de chauffage des adresses IP {#ip-warmup}

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* [Prise en main du réchauffement des adresses IP](ip-warmup-gs.md)
* [Créer des campagnes de réchauffement des adresses IP](ip-warmup-campaign.md)
* **[Créer une formule de chauffage des adresses IP](ip-warmup-plan.md)**
* [Exécution de la formule de chauffage par IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Une fois que vous avez créé une ou plusieurs [Campagnes de chaleur des adresses IP](ip-warmup-campaign.md) avec une surface dédiée et l’option correspondante activée, vous pouvez commencer à créer votre plan de chauffage par IP.

## Préparer le fichier du plan de chauffage par IP {#prepare-file}

Le réchauffement des adresses IP est une activité qui consiste à augmenter progressivement le volume d’emails qui sortent de vos adresses IP et domaine vers les principaux fournisseurs d’accès à Internet (FAI) - afin d’établir votre réputation d’expéditeur légitime.

Cette activité est réalisée en temps opportun avec l’aide d’un expert en délivrabilité qui contribue à la préparation d’un plan bien conçu basé sur les domaines du secteur, les cas d’utilisation, les régions, les FAI et d’autres facteurs.

Lorsque vous utilisez l’objet [!DNL Journey Optimizer] Fonctionnalité de réchauffement des adresses IP, ce plan prend la forme d&#39;un fichier Excel qui doit contenir un certain nombre de colonnes prédéfinies. Avant de pouvoir créer un plan de chauffage par IP dans la variable [!DNL Journey Optimizer] , vous devez renseigner ce modèle avec toutes les données qui alimenteront votre plan.

>[!CAUTION]
>
>Contactez votre conseiller en délivrabilité pour vous assurer que votre fichier de plan de chauffage par IP est correctement configuré.

Vous trouverez ci-dessous un exemple de fichier contenant un plan de chauffage par IP.

![](assets/ip-warmup-sample-file.png)

### Onglet Plan de stockage d’adresses IP

* Dans cet exemple, un plan a été préparé sur 17 jours (appelé &quot;**exécutions**&quot;) pour atteindre un volume cible de plus d’un million de profils.

* Ce planifié est exécuté via la version 6 **phases**, chacune d’elles contenant au moins une exécution.

* Vous pouvez avoir autant de colonnes que vous le souhaitez pour les domaines sur lesquels vous souhaitez envoyer des messages. Dans cet exemple, le plan est divisé en 6 colonnes : 5 correspondent à la variable **groupes de domaines principaux** à utiliser dans votre plan (Gmail, Microsoft, Yahoo, Orange et Apple) et dans la sixième colonne, **Autres**, contient toutes les adresses restantes d’autres domaines.
* La variable **Jours d’engagement** indique que seuls les profils impliqués dans votre marque au cours des 30 derniers jours sont ciblés.

L’idée est d’augmenter progressivement le nombre d’adresses ciblées au cours de chaque exécution, tout en réduisant le nombre d’exécutions pour chaque phase.

Les groupes de domaines principaux d’usine que vous pouvez ajouter à votre plan sont répertoriés ci-dessous :

* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigpond
* Orange
* Softbank
* Docomo
* Internet unifié
* Microsoft
* KDDI
* Italia Online
* La Poste
* Apple

### Onglet Groupe de domaines personnalisé

Vous pouvez également ajouter d’autres colonnes à votre plan en incluant des groupes de domaines personnalisés.

Utilisez la variable **[!UICONTROL Groupe de domaines personnalisé]** pour définir un nouveau groupe de domaines. Pour chaque domaine, vous pouvez ajouter tous les sous-domaines qu’il couvre.<!--TBC-->

Par exemple, si vous ajoutez le domaine personnalisé Luma, vous souhaitez inclure les sous-domaines suivants : luma.com, luma.co.uk, luma.it, luma.fr, luma.de, etc.

## Accès et gestion des plans de chauffage des adresses IP {#manage-ip-warmup-plans}

1. Accédez au **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Plans de chauffage des adresses IP]** . Tous les plans de chauffage des adresses IP créés jusqu’à présent s’affichent.

   ![](assets/ip-warmup-filter-list.png)

1. Vous pouvez filtrer par Etat de la . Les différents statuts sont les suivants :

   * **Pas démarré**: aucune exécution n’a encore été activée. [En savoir plus](ip-warmup-execution.md#define-runs)
   * **En direct**: le plan passe à ce statut dès que la première exécution de la première phase a été activée avec succès. [En savoir plus](ip-warmup-execution.md#define-runs)
   * **Terminé**: le plan a été marqué comme terminé. Cette option n’est disponible que si toutes les exécutions du plan sont incluses dans **[!UICONTROL Succès]** ou **[!UICONTROL Version préliminaire]** status (aucune exécution ne peut être exécutée. **[!UICONTROL En direct]**). [En savoir plus](ip-warmup-execution.md#define-runs#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. Pour supprimer un plan de chauffage par IP, sélectionnez le **[!UICONTROL Supprimer]** en regard du nom d’un plan et confirmez la suppression.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >Le plan de chauffage d’une adresse IP sélectionné sera définitivement supprimé.

## Créer une formule de chauffage des adresses IP {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Définition de votre formule de chauffage des adresses IP"
>abstract="Téléchargez le modèle CSV et remplissez-le de données pour les phases de réchauffement des adresses IP et le nombre cible de profils."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Sélectionner une surface marketing"
>abstract="Vous devez sélectionner la même surface que celle sélectionnée dans l&#39;opération que vous souhaitez associer à votre plan de chaleur IP."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=fr" text="Configurer des surfaces de canal"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=fr" text="Créer des campagnes de réchauffement des adresses IP"

Lorsqu’une ou plusieurs campagnes en direct avec la variable **[!UICONTROL Activation du plan de chauffage par IP]** Les options activées sont activées. Vous pouvez les associer à un plan de réchauffement des adresses IP.

>[!CAUTION]
>
>Pour créer, modifier et supprimer des plans de réchauffement des adresses IP, vous devez disposer de la variable **[!UICONTROL Consultant en matière de délivrabilité]** autorisation. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

1. Accédez au **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Plans de chauffage des adresses IP]** , puis cliquez sur **[!UICONTROL Créer un plan de chauffage par IP]**.

   ![](assets/ip-warmup-create-plan.png)

1. Renseignez les détails du plan de chaleur IP : donnez-lui un nom et une description.

   ![](assets/ip-warmup-plan-details.png)

1. Sélectionnez une [surface](channel-surfaces.md). Seules les surfaces marketing peuvent être sélectionnées. [En savoir plus sur le type d&#39;email](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >Vous devez sélectionner la même surface que celle sélectionnée dans l&#39;opération que vous souhaitez associer à votre plan de chaleur IP. [Découvrez comment créer une campagne de réchauffement des adresses IP](ip-warmup-campaign.md)

1. Téléchargez le fichier Excel contenant votre plan de chauffage par IP. [En savoir plus](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. Cliquez sur **[!UICONTROL Créer]**. Toutes les phases, les exécutions, les colonnes et leur contenu définis dans le fichier que vous avez téléchargé sont automatiquement affichés dans le [!DNL Journey Optimizer] . [En savoir plus](ip-warmup-execution.md)

   ![](assets/ip-warmup-plan-uploaded.png)
