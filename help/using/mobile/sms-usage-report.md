---
solution: Journey Optimizer
product: journey optimizer
title: Affichage des mesures d’utilisation des SMS
description: Découvrez comment générer des rapports d’utilisation des SMS pour réconcilier le volume des messages avec la facturation du fournisseur dans Journey Optimizer.
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: b519bcd5489c441e7f22cb47783d8b99a58c2442
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 1%

---

# Générer un rapport d’utilisation des SMS {#sms-usage-report}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_metrics"
>title="Mesures d’utilisation des SMS"
>abstract="Générer des rapports d&#39;utilisation des SMS pour réconcilier le volume des messages avec la facturation fournisseur. Les rapports répertorient les nombres de messages terminés par un téléphone mobile (MT) et de messages mobiles (MO) pour chaque numéro de téléphone ou code court, agrégés par jour."

>[!BEGINSHADEBOX]

**Sur cette page :** générez des rapports d’utilisation des SMS dans Adobe Journey Optimizer pour réconcilier le volume terminé par un téléphone mobile (MT) et provenant d’un téléphone mobile (MO) avec la facturation du fournisseur, à l’aide des informations d’identification de l’API Sinch MMS et d’une sortie CSV téléchargeable.

>[!ENDSHADEBOX]

Les mesures d’utilisation des SMS sont disponibles lorsque vous achetez des SMS via Adobe Journey Optimizer. Les rapports résument le trafic envoyé et reçu par numéro de téléphone ou code court, agrégé par jour, au cours des **90 derniers jours**.

Pour afficher les mesures d’utilisation, un administrateur doit :

1. [Créez des informations d’identification d’API MMS Sinch](mobile-configuration-sinch.md#sinch-mms) utilisées uniquement pour récupérer les données d’utilisation de Sinch.

   Les rapports d’utilisation nécessitent des informations d’identification d’API avec **[!UICONTROL Fournisseur SMS]** défini sur **Sinch MMS**. Ces informations d’identification connectent Journey Optimizer à Sinch afin que les données d’utilisation puissent être récupérées. Il est distinct des informations d’identification Sinch utilisées pour envoyer des SMS ou des MMS, bien que les valeurs de champ proviennent du même projet Sinch.

1. [Configurer et récupérer un rapport d’utilisation des SMS](#configure-sms-usage-report).

Ces étapes nécessitent l’autorisation **[!UICONTROL Gérer les paramètres SMS]**. [En savoir plus sur les autorisations](../administration/high-low-permissions.md#administration-permissions).

## Configuration et affichage des rapports d’utilisation des SMS {#configure-sms-usage-report}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_report_name"
>title="Nom du rapport"
>abstract="Saisissez un libellé qui vous aidera à reconnaître ce rapport dans la liste ultérieurement, par exemple la révision de facturation de mai 2026."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_credential"
>title="Informations d’identification SMS"
>abstract="Sélectionnez les informations d’identification de l’API Sinch dont le trafic d’envoi et de réception doit apparaître dans ce rapport. Pour ajouter ou mettre à jour des informations d’identification, accédez à **Administration** > **Canaux** > **Informations d’identification de l’API**, puis choisissez **Fournisseur SMS** > **Sinch MMS**."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_start_date"
>title="Date de début"
>abstract="Premier jour de la période à inclure dans le rapport. Les données d’utilisation ne sont disponibles que pour les 90 derniers jours."

Les rapports d’utilisation des SMS présentent le volume d’origine mobile (MO) et le volume d’extrémité mobile (MT) par numéro court afin de prendre en charge la réconciliation entre l’activité de facturation du fournisseur et l’activité de messagerie dans Journey Optimizer.

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres SMS]**.

1. Accédez au menu **[!UICONTROL Afficher les mesures d’utilisation des SMS]**, puis cliquez sur **[!UICONTROL Configurer un nouveau rapport]**.

   ![](assets/usage_report_1.png)

1. Configurez le rapport :

   * **[!UICONTROL Nom du rapport]** : saisissez un libellé qui vous aide à reconnaître votre rapport.
   * **[!UICONTROL Informations d’identification SMS]** : sélectionnez les informations d’identification de l’API **Sinch MMS** que vous avez précédemment créées pour les rapports d’utilisation des SMS.
   * **[!UICONTROL Date de début]** et **[!UICONTROL Date de fin]** : permet de définir la période du rapport. Les données d’utilisation ne sont disponibles que pour les 90 derniers jours.

     ![](assets/usage_report_2.png)

1. Cliquez sur **[!UICONTROL Configurer le rapport]** pour envoyer la requête.

1. Dans la liste **[!UICONTROL Rapports envoyés]**, recherchez le rapport que vous avez configuré, puis cliquez sur **[!UICONTROL Récupérer le rapport]**.

   Le statut passe à **En attente** lors de la génération du rapport.

1. Une fois que le statut de votre rapport est mis à jour sur **[!UICONTROL Prêt]**, cliquez sur **[!UICONTROL Afficher]** pour ouvrir le rapport. Le rapport comprend :

   * **Résumé d&#39;utilisation** : nombre total de messages MO (Mobile Origated) et MT (Mobile Terminated) pour les dates sélectionnées, répartis par numéro court.

   * **Volume quotidien des SMS** : volume quotidien des SMS, ventilé par numéro court.

     ![](assets/usage_report_3.png)

1. Pour exporter le rapport, cliquez sur **[!UICONTROL Télécharger CSV]**. Journey Optimizer télécharge un fichier CSV pour le rapport que vous consultez.
