---
solution: Journey Optimizer
product: journey optimizer
title: Configurer les paramètres du référentiel AEM
description: Découvrez comment les administrateurs configurent les référentiels AEM, les domaines personnalisés, la publication authentifiée et l’accès aux fragments de contenu pour l’auteur uniquement dans Journey Optimizer.
feature: Integrations
topic: Administration
role: Admin
level: Experienced
hide: true
keywords: AEM, fragments de contenu, administration, référentiel, authentification, auteur, publication
source-git-commit: acbc63b37802bfe27a24246d4701efb00ac95940
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Configuration de l’accès au référentiel Adobe Experience Manager {#aem-admin-settings}

Adobe Journey Optimizer s’intègre à **[!DNL Adobe Experience Manager as a Cloud Service]** afin que vous puissiez utiliser **fragments de contenu** dans les Parcours et les campagnes. Par défaut, les **fragments de contenu** sont lus à partir du référentiel de publication Adobe Experience Manager. Les administrateurs peuvent passer en mode de création uniquement ou ajuster l’accès de publication dans le menu **[!UICONTROL Intégration d’AEM]**.

➡️ Lorsque le référentiel est configuré, continuez avec [Utiliser des fragments de contenu Experience Manager](../integrations/aem-fragments.md) pour les tâches de création et de sélection dans Journey Optimizer.

## Configuration des référentiels {#configure-ui}

>[!NOTE]
>
> **[!UICONTROL Intégration AEM]** enregistre les paramètres du référentiel **par sandbox**. Chaque sandbox conserve ses propres intégrations qui ne s’appliquent pas à tous les sandbox.

Journey Optimizer stocke une intégration par organisation, sandbox et référentiel Adobe Experience Manager. Si vous enregistrez une nouvelle intégration pour cette même combinaison, elle remplace les paramètres précédents. Seule la dernière configuration est conservée.

Pour configurer votre référentiel :

1. Accédez À **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Intégration AEM]**.

1. Cliquez sur **[!UICONTROL Créer une intégration]**.

   ![](assets/aem-admin-settings-1.png)

1. Choisissez le référentiel à configurer, puis cliquez sur **[!UICONTROL Suivant]**.

   De plus, vous pouvez cliquer sur **[!UICONTROL Afficher]** pour accéder à ce référentiel.

   >[!IMPORTANT]
   >
   >L’enregistrement d’une nouvelle configuration pour la même organisation, le même sandbox et le même référentiel **remplace** la configuration par défaut, c’est-à-dire le référentiel **publier**.

   ![](assets/aem-admin-settings-2.png)

1. Saisissez un **[!UICONTROL Nom]** et un **[!UICONTROL Description]**.

1. Choisissez votre configuration :

   +++ Configuration de l’auteur uniquement

   Sélectionnez **[!UICONTROL Configuration de l’auteur uniquement]** lorsque Journey Optimizer doit lire les fragments de contenu de l’environnement Adobe Experience Manager **auteur** uniquement. La réplication de l’auteur vers la publication et les mises à jour de publication actives ne sont pas prises en charge.

   ![](assets/aem-admin-settings-3.png)

   +++

   +++ Configuration de l’instance de publication

   1. Sélectionnez **[!UICONTROL Configuration de l’instance de publication]** pour activer les paramètres de l’instance de publication.

      ![](assets/aem-admin-settings-4.png)

   1. Vous pouvez éventuellement activer **[!UICONTROL Envoyer le jeton à l’instance de publication]** afin que les informations d’identification du service soient incluses avec les requêtes à l’instance de publication.

   1. Collez un **[!UICONTROL JSON d’informations d’identification de service]** valide pour l’authentification.

   1. Vous pouvez éventuellement fournir un domaine personnalisé si votre organisation ne parvient pas à atteindre l’hôte de publication AEM par défaut (`publish-XX-XX.adobeaemcloud.com`) pour récupérer du contenu.

      ![](assets/aem-admin-settings-5.png)

   +++

1. Cliquez sur **[!UICONTROL Enregistrer]**.

1. Pour modifier ou désactiver cette intégration de référentiel, accédez à la configuration précédemment créée à partir du menu **[!UICONTROL Intégration d’]**.

Lors de l’enregistrement, ce sandbox utilise le référentiel pour le sélecteur de fragment de contenu et le **gestionnaire d’accès de**.

