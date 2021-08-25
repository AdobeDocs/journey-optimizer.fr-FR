---
title: Rapport dynamique sur les emails
description: Découvrez comment utiliser les données du rapport dynamique sur les emails
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 79%

---

# Rapport dynamique sur les emails {#email-live-report}

Le **[!UICONTROL Rapport dynamique]** sur les emails ne cible qu’une diffusion email spécifique.

Dans l’onglet **[!UICONTROL Exécutions]** du menu **[!UICONTROL Messages]**, sélectionnez **[!UICONTROL Affichage dynamique]**, puis, dans le menu avancé de la diffusion sélectionnée, sélectionnez **[!UICONTROL Rapport dynamique]**.

![](../assets/live_report.png)

Le **[!UICONTROL Rapport dynamique]** sur les emails est divisé en différents widgets indiquant le succès et les erreurs de votre diffusion. Chaque widget peut être redimensionné et supprimé en cas de besoin. Pour plus d’informations à ce sujet, consultez cette [section](live-report.md#modify-dashboard).

![](../assets/live_report_5.png)

Les widgets **[!UICONTROL Performances des emails]** et **[!UICONTROL Résumé des emails]** présentent les principales informations relatives à votre message avec un graphique et des KPI :

* **[!UICONTROL Envoyés]** : nombre total d’envois pour la diffusion.

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs qui se sont produites au cours d’une diffusion, l’empêchant d’être envoyée aux profils.

* **[!UICONTROL Ouvertures]** : nombre d’ouvertures d’un message dans une diffusion.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans une diffusion.

Le graphique **[!UICONTROL Statistiques d’envoi]** présente le succès de votre diffusion :

* **[!UICONTROL Délivrés]** : nombre de messages envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Bounces]** : nombre total d&#39;erreurs cumulées lors des diffusions et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs]** : nombre total d’erreurs survenues au cours d’une diffusion, empêchant l’erreur d’être envoyée aux profils.

![](../assets/live_report_6.png)

Le graphique et le tableau **[!UICONTROL Causes des erreurs]** vous permettent de voir quelle erreur s’est produite au cours de votre diffusion.

Les widgets **[!UICONTROL Causes des bounces]** et **[!UICONTROL Catégories de bounces]** contiennent les données disponibles relatives aux messages ayant fait l’objet d’un rebond, notamment :

* **[!UICONTROL Hard bounce]** : nombre total d&#39;erreurs permanentes, telles qu&#39;une adresse email incorrecte. Un message d&#39;erreur indique explicitement que l&#39;adresse n&#39;est pas valide, comme Utilisateur inconnu.

* **[!UICONTROL Soft bounces]** : nombre total d&#39;erreurs temporaires, telles qu&#39;une boîte de réception pleine.

* **[!UICONTROL Ignorées]** : nombre total d&#39;erreurs temporaires (par exemple, Absent(e) du bureau) ou techniques (par exemple, si le type d&#39;expéditeur est administrateur).

>[!NOTE]
>
>Les profils avec le statut **[!UICONTROL Supprimés]** ou **[!UICONTROL Non autorisés]** sont exclus pendant le processus d’envoi du message. Par conséquent, bien que les **rapports de Parcours** indiquent que ces profils ont traversé le parcours ([Lecture de segment](../building-journeys/read-segment.md) et [Message](../building-journeys/journeys-message.md)), les **Rapports par e-mail** ne les incluront pas dans les mesures **[!UICONTROL Envoyés]** telles qu’elles sont filtrées avant l’envoi par e-mail .
>
>Pour en savoir plus, consultez [Liste de suppression](../suppression-list.md) et [Liste autorisée](../allow-list.md). Pour connaître la raison de tous les cas d’exclusion, vous pouvez utiliser le [service de requête Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.
