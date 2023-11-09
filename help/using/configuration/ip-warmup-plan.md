---
solution: Journey Optimizer
product: journey optimizer
title: Créer un plan de préchauffage d’adresses IP
description: Découvrez comment créer un plan de préchauffage d’adresses IP dans Journey Optimizer.
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, groupe, sous-domaines, délivrabilité
hide: true
hidefromtoc: true
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: eb4a4929de17f0b57216f69e00da6314f7b59b07
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 100%

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

>[!CAUTION]
>
>Pour créer, modifier supprimer des plans de préchauffage d’adresses IP, et y accéder, vous devez disposer de l’autorisation **[!UICONTROL Consultant ou consultante en délivrabilité]**. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

## Préparer un fichier de plan de préchauffage d’adresses IP {#prepare-file}

Le préchauffage d’adresses IP est une activité qui consiste à augmenter progressivement le volume d’e-mails qui sortent de vos adresses IP et domaine vers les principaux fournisseurs d’accès à Internet (FAI), afin d’établir votre réputation d’expéditeur légitime.

Cette activité est réalisée en temps opportun avec l’aide d’un spécialiste en délivrabilité qui contribue à la préparation d’un plan bien conçu basé sur les domaines du secteur, les cas d’utilisation, les régions, les FAI et d’autres facteurs.

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

Avant de pouvoir créer un plan de préchauffage d’adresses IP dans l’interface [!DNL Journey Optimizer], vous devez renseigner un modèle Excel avec toutes les données qui alimenteront votre plan.

>[!CAUTION]
>
>Collaborez avec votre consultant ou consultante en délivrabilité pour vous assurer que votre fichier de plan de préchauffage d’adresses IP est correctement configuré.
>
>Veillez à utiliser le format fourni dans le modèle.

Vous trouverez ci-dessous un exemple de fichier contenant un plan de préchauffage d’adresses IP.

![](assets/ip-warmup-sample-file.png)

>[!NOTE]
>
>Pour l’instant, vous ne devez pas toucher aux cellules **Propriétés** et **Valeur**.

### Onglet Plan de préchauffage d’adresses IP {#ip-warmup-plan-tab}

* Dans cet exemple, un plan a été préparé sur 17 jours (appelé « **exécutions** ») pour atteindre un volume cible de plus d’un million de profils.

* Ce plan est exécuté en six **phases**, chacune d’elles contenant au moins une exécution.

* Vous pouvez avoir autant de colonnes que vous le souhaitez pour les domaines sur lesquels vous souhaitez envoyer des messages. Dans cet exemple, le plan est divisé en six colonnes :

   * Quatre d’entre elles correspondent aux **groupes de domaines prêts à l’emploi** à utiliser dans votre plan (Gmail, Microsoft, Yahoo et Orange).
   * L’une correspond à un groupe de domaines personnalisé (que vous devez ajouter à l’aide de l’onglet [Groupe de domaines personnalisé](#custom-domain-group-tab)).
   * La sixième colonne, **Autres**, contient toutes les adresses restantes d’autres domaines qui ne sont pas explicitement couverts dans le plan. Cette colonne est facultative : si elle est omise, les e-mails seront envoyés uniquement aux domaines spécifiés.
* La colonne **Jours d’engagement** indique que seuls les profils impliqués dans votre marque au cours de la dernière période sont ciblés.

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

<!--
+++ Gmail
gmail.com;gmail.fr;gmail.de;gmail.co.uk;gmail.it
+++

+++ Adobe
adobe.com;adobe.fr;adobe.es
+++

+++WP
+++

+++Comcast
+++

+++Yahoo
+++

+++Bigpond
+++

+++Orange
+++

+++Softbank
+++

+++Docomo
+++

+++United Internet
+++

+++Microsoft
+++

+++KDDI
+++

+++Italia Online
+++

+++La Poste
+++
-->

### Onglet Groupe de domaines personnalisés {#custom-domain-group-tab}

Vous pouvez également ajouter d’autres colonnes à votre plan en incluant des groupes de domaines personnalisés.

Utilisez l’onglet **[!UICONTROL Groupe de domaines personnalisés]** pour définir un nouveau groupe de domaines. Pour chaque domaine, vous pouvez ajouter tous les sous-domaines qu’il couvre.<!--TBC-->

Par exemple, si vous ajoutez le domaine personnalisé Luma, vous souhaitez inclure les sous-domaines suivants : luma.com, luma.co.uk, luma.it, luma.fr, luma.de, etc.

![](assets/ip-warmup-sample-file-custom.png)

### Exemple {#example}

Supposons que vous souhaitiez avoir deux groupes de domaines personnalisés :

* Un pour les domaines Hotmail uniquement.
* Un pour tous les autres domaines du groupe de domaines Microsoft (excluant ainsi tous les domaines Hotmail).

Notez que tous les autres domaines seront rassemblés dans la colonne **[!UICONTROL Autres]**.

1. Dans l’onglet **[!UICONTROL Groupe de domaines personnalisé]**, créez le groupe de domaines **Hotmail**.

1. Ajoutez tous les domaines Hotmail sur la même ligne.

   Vous pouvez [copier et coller](#copy-paste) tous les domaines Hotmail répertoriés dans la section de l’[onglet Plan de préchauffage d’adresses IP](#ip-warmup-plan-tab).

1. Ajoutez une autre ligne.

1. Créez le groupe de domaines **Microsoft_X**.

1. Ajoutez tous les domaines Microsoft qui ne sont pas Hotmail sur la même ligne. De même, vous pouvez les copier et les coller à partir de la liste ci-dessus. [En savoir plus](#copy-paste)

1. Revenez à l’onglet **[!UICONTROL Plan de préchauffage d’adresses IP]**.

1. Créez trois colonnes : une pour **Hotmail**, une pour **Microsoft_X** et une pour **Autres**.

1. Renseignez les colonnes selon vos besoins.

>[!NOTE]
>
>Une fois le plan de préchauffage d’adresses IP chargé dans [!DNL Journey Optimizer], il n’est pas nécessaire d’exclure les groupes de domaines Microsoft.

<!--Only the domain groups listed in the **[!UICONTROL IP Warmup Plan]** tab will be taken into account.-->

### Copier et coller les domaines par défaut {#copy-paste}

Si vous souhaitez créer un groupe de domaines personnalisé contenant par exemple tous les domaines Hotmail, vous pouvez copier et coller les domaines à partir de la liste par défaut fournie [ci-dessus](#ip-warmup-plan-tab).

Utilisez ensuite l’outil de conversion Excel pour convertir le texte en colonnes :

1. Sélectionnez **[!UICONTROL Données]** > **[!UICONTROL Texte en colonnes…]**, choisissez **[!UICONTROL Délimité]** et sélectionnez **[!UICONTROL Suivant]**.

1. Sélectionnez **[!UICONTROL Point-virgule]**, cliquez sur **[!UICONTROL Suivant]** et **[!UICONTROL Terminer]**.

Chaque domaine s’affiche désormais dans une colonne différente sur la même ligne.

## Accéder à des plans de préchauffage d’adresses IP et les gérer {#manage-ip-warmup-plans}

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Plans de préchauffage d’adresses IP]**. Tous les plans de préchauffage d’adresses IP créés jusqu’à présent s’affichent.

   ![](assets/ip-warmup-filter-list.png)

1. Vous pouvez filtrer par statut. Les différents statuts sont les suivants :

   * **Pas démarré** : aucune exécution n’a été activée pour le moment. [En savoir plus](ip-warmup-execution.md#define-runs)
   * **Actif** : le plan passe à ce statut dès que la première exécution de la première phase a été activée avec succès. [En savoir plus](ip-warmup-execution.md#define-runs)
   * **Terminé** : le plan a été marqué comme terminé. <!--This option is only available if all the runs in the plan are in **[!UICONTROL Completed]** or **[!UICONTROL Draft]** status (no run can be **[!UICONTROL Live]**).--> [En savoir plus](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. Pour supprimer un plan de préchauffage d’adresses IP, sélectionnez l’icône **[!UICONTROL Supprimer]** en regard du nom d’un plan et confirmez la suppression.

   >[!NOTE]
   >
   >Seuls les plans ayant le statut **Non démarré** peuvent être supprimés.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >Le plan de préchauffage d’adresses IP sélectionné sera définitivement supprimé.

## Créer un plan de préchauffage d’adresses IP {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Définition de votre plan de préchauffage d’adresses IP"
>abstract="Téléchargez le modèle CSV et remplissez-le de données pour les phases de préchauffage d’adresses IP et le nombre cible de profils."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Sélectionner une surface marketing"
>abstract="Vous devez sélectionner la même surface que celle sélectionnée dans la campagne que vous souhaitez associer à votre plan de préchauffage d’adresses IP."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=fr" text="Configurer des surfaces de canal"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=fr" text="Créer des campagnes de préchauffage d’adresses IP"

Pour créer une campagne de préchauffage d’adresses IP, suivez les étapes ci-dessous.

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Plans de préchauffage d’adresses IP]**, puis cliquez sur **[!UICONTROL Créer un plan de préchauffage d’adresses IP]**.

   ![](assets/ip-warmup-create-plan.png)

1. Renseignez les détails du plan de préchauffage d’adresses IP : attribuez-lui un nom et une description.

   ![](assets/ip-warmup-plan-details.png)

1. Sélectionnez la [surface](channel-surfaces.md) que vous voulez vous préchauffer. Seules les surfaces marketing peuvent être sélectionnées. [En savoir plus sur le type d’e-mail](../email/email-settings.md#email-type)

   >[!NOTE]
   >
   >Les campagnes que vous souhaitez associer à votre plan de préchauffage d’adresses IP doivent utiliser la même surface. [Découvrez comment créer une campagne de préchauffage d’adresses IP](ip-warmup-campaign.md).

1. Chargez le fichier Excel contenant votre plan de préchauffage d’adresses IP. [En savoir plus](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

   >[!NOTE]
   >
   >En cas d’échec du chargement, assurez-vous d’utiliser le formatage et le format de fichier corrects (.xls ou .xlsx). Utilisez l’exemple fourni par Adobe.

1. Cliquez sur **[!UICONTROL Créer]**. Toutes les phases, les exécutions, les colonnes et leur contenu définis dans le fichier que vous avez chargé sont automatiquement affichés dans l’interface de [!DNL Journey Optimizer].

   ![](assets/ip-warmup-plan-uploaded.png)

Vous pouvez maintenant exécuter votre plan de préchauffage d’adresses IP. [En savoir plus](ip-warmup-execution.md)
