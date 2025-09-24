---
solution: Journey Optimizer
product: journey optimizer
title: Accéder et s’abonner aux alertes système
description: Découvrez comment accéder et vous abonner aux alertes système.
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 34649ab411823f1aa09d390d23484697e80763c5
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 65%

---

# Accéder et s’abonner aux alertes système {#alerts}

Lors de la création de vos parcours et campagnes, utilisez le bouton **Alertes** pour vérifier et résoudre les erreurs avant de les exécuter ou de les publier.



Dans le menu dédié **[!UICONTROL Alertes]**, vous pouvez également vous abonner aux alertes système [!DNL Adobe Journey Optimizer], comme indiqué sur cette page.

## Accéder aux alertes {#access-alerts}

En cas d’échec, vous pouvez obtenir des alertes système dans le centre de notification de Journey Optimizer (alertes in-app) et/ou recevoir un e-mail. Pour accéder aux rapports, procédez comme suit.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

>[!NOTE]
>
>En savoir plus sur les alertes dans Adobe Experience Platform dans la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=fr){target="_blank"}.

Dans le menu de gauche, sous **[!UICONTROL Administration]**, cliquez sur **[!UICONTROL Alertes]**. Plusieurs alertes préconfigurées pour Journey Optimizer sont disponibles.

Elles sont répertoriées comme suit et chaque alerte est détaillée ci-dessous.

* Alertes spécifiques aux parcours :

   * Alerte [Échec de l’action personnalisée de parcours](#alert-custom-actions)
   * Alerte [Échec du déclenchement de la lecture d’audience](#alert-read-audiences)
<!--DOCAC-13465   * the [Profile Discard Rate Exceeded](#alert-discard-rate) alert
   * the [Custom Action Error Rate Exceeded](#alert-custom-action-error-rate) alert
   * the [Profile Error Rate Exceeded](#alert-profile-error-rate) alert-->

* Alertes spécifiques à la configuration des canaux :

   * Alerte [Enregistrement DNS du domaine AJO manquant](#alert-dns-record-missing)
   * l’alerte [échec de la configuration du canal AJO](#alert-channel-config-failure)
     <!--* the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## S’abonner aux alertes {#subscribe-alerts}

Si un comportement inattendu se produit, et/ou qu’un certain ensemble de conditions de vos opérations est atteint (par exemple, un problème potentiel lorsque le système dépasse un certain seuil), des notifications d’alerte sont envoyées à l’ensemble des personnes de votre organisation qui s’y sont abonnées.

Vous pouvez vous abonner à chaque alerte individuellement à partir de l’interface utilisateur, soit globalement à partir du menu **[!UICONTROL Alertes]** (voir [Abonnement global](#global-subscription))<!--DOCAC-13465, or unitary for a specific journey (see [Unitary subscription](#unitary-subscription))-->.

En fonction des préférences des personnes abonnées, les alertes sont envoyées par e-mail ou directement dans le centre de notification de Journey Optimizer, dans le coin supérieur droit de l’interface d’utilisation (notifications in-app). Sélectionnez le mode de réception de ces alertes dans les **[!UICONTROL Préférences]** [!DNL Adobe Experience Cloud]. [En savoir plus](../start/user-interface.md#in-product-alerts)

Lorsqu’une alerte est résolue, les personnes abonnées reçoivent une notification « Résolue ».


### Abonnement global {#global-subscription}

Pour vous abonner/désabonner à une alerte pour tous les parcours et campagnes, procédez comme suit :

1. Accédez au tableau de bord **[!UICONTROL Alertes]** dans le menu de gauche, sélectionnez l’option **[!UICONTROL S’abonner]** pour l’alerte à laquelle vous souhaitez vous abonner.

   ![Abonnement à une alerte](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >L’abonnement s’applique uniquement à un sandbox spécifique. Vous devez vous abonner à des alertes pour chaque sandbox.

1. Utilisez la même méthode pour vous **[!UICONTROL désabonner]**.

Vous pouvez également vous abonner par le biais des notifications d’événement [ I/O ](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=fr){target="_blank"}. Les règles d’alerte sont organisées en différents packages d’abonnement. Les abonnements aux événements correspondant aux alertes Journey Optimizer spécifiques sont présentés [ci-dessous](#journey-alerts).

<!--DOCAC-13465
### Unitary subscription {#unitary-subscription}

To subscribe/unsubscribe to an alert for a specific journey, follow these steps:

1. Browse to the journey inventory and select the **[!UICONTROL Subscribe to alerts]** option for a specific journey.

      ![Subscribing to an alert for a specific journey](assets/subscribe-journey-alert.png){width=80%}

1. Choose the alert(s). The following alerts are available: [Profile Discard Rate Exceeded](#alert-discard-rate), [Custom Action Error Rate Exceeded](#alert-custom-action-error-rate), and [Profile Error Rate Exceeded](#alert-profile-error-rate).
   
1. To unsubscribe to an alert, unselect it from the same screen.

1. Click **[!UICONTROL Save]** to confirm.
-->

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html#enable-email-alerts){target="_blank"}.-->




## Alertes de parcours {#journey-alerts}

>[!CAUTION]
>
>Les alertes spécifiques à Adobe Journey Optimizer s’appliquent uniquement aux parcours **dynamiques**. Les alertes ne seront pas déclenchées pour les parcours en mode test.


### Échec de l’action personnalisée du parcours {#alert-custom-actions}

Cette alerte vous avertit si une action personnalisée échoue. Nous considérons qu’il existe un échec quand plus de 1 % d’erreurs sont commises sur une action personnalisée spécifique au cours des 5 dernières minutes. Ces données sont évaluées toutes les 30 secondes.

Cliquez sur le nom de l’alerte pour vérifier les détails et la configuration de l’alerte.

![](assets/alerts-custom-action.png)

Les alertes relatives aux actions personnalisées sont résolues lorsque, au cours des 5 dernières minutes :

* il n’y a eu aucune erreur sur cette action personnalisée (ou les erreurs sont inférieures au seuil de 1 %) ;

* ou aucun profil n’a atteint cette action personnalisée.

Le nom d’abonnement à l’événement d’E/S correspondant à l’alerte d’action personnalisée est **Échec de l’action personnalisée du parcours**.

Pour résoudre les alertes **Action personnalisée** :

* Vérifiez votre action personnalisée à l’aide du mode test sur un autre parcours :

  ![](assets/alert-troubleshooting-2.png)

* Consultez le rapport de votre parcours pour afficher les motifs d’erreur lors de l’action.

  ![](assets/alert-troubleshooting-3.png)

* Vérifiez vos événements stepEvents de parcours pour obtenir plus d’informations sur « failureReason ».

* Vérifiez votre configuration d’action personnalisée et que l’authentification est toujours correcte. Effectuez un contrôle manuel avec Postman, par exemple.

### Échec du déclenchement de la lecture d’audience {#alert-read-audiences}

Cette alerte vous avertit si une activité **Lecture d’audience** n’a traité aucun profil 10 minutes après l’heure planifiée de l’exécution. Cet échec peut être dû à des problèmes techniques ou parce que l’audience est vide. Si cet échec est dû à des problèmes techniques, sachez que des reprises peuvent toujours se produire, selon le type de problème (par exemple : si la création du traitement d’export a échoué, nous allons réessayer toutes les 10 minutes pendant 1 h au maximum).

![](assets/alerts1.png)

Les alertes sur l’activité **Lecture d’audience** ne s’appliquent qu’aux parcours récurrents. Les activités **Lecture d’audience** dans des parcours dynamiques dont l’exécution est planifiée **Une fois** ou **Dès que possible** sont ignorées.

Les alertes sur **Lecture d’audience** sont résolues lorsqu’un profil entre dans le nœud **Lecture d’audience**.

Le nom d’abonnement à l’événement d’E/S correspondant à l’alerte **Échec du déclenchement de la lecture d’audience** est **Retards, échecs et erreurs dans la lecture d’audience du parcours**.

Pour résoudre les alertes **Lecture d’audience**, vérifiez la taille de l’audience dans l’interface d’Experience Platform.

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

<!--DOCAC-13465

### Profile Discard Rate Exceeded {#alert-discard-rate}

This alert warns you if the ratio of profile discards to entered profiles over the last 5 minutes exceeded threshold. The defaut threshold is set to 20% but you can [define a custom theshold](#custom-threshold).

Click the name of the alert to check the alert details and configuration.


### Custom Action Error Rate Exceeded {#alert-custom-action-error-rate}

This alert warns you if the ratio of custom action errors to successful HTTP calls over the last 5 minutes exceeded threshold. The defaut threshold is set to 20% but you can [define a custom theshold](#custom-threshold).

### Profile Error Rate Exceeded {#alert-profile-error-rate}

This alert warns you if the ratio of custom action errors to successful HTTP calls over the last 5 minutes exceeded threshold. The defaut threshold is set to 20% but you can [define a custom theshold](#custom-threshold).

Click the name of the alert to check the alert details and configuration.
-->

## Alertes de configuration {#configuration-alerts}

### Enregistrement DNS du domaine AJO manquant {#alert-dns-record-missing}

Cette alerte vous avertit lorsque des enregistrements DNS critiques (NS ou CNAME) requis pour une configuration de délivrabilité appropriée sont manquants ou mal configurés. Sans ces enregistrements, la délivrabilité des e-mails peut être compromise.

>[!NOTE]
>
>* Les enregistrements NS sont essentiels pour la délégation complète de sous-domaines à Adobe. [En savoir plus](../configuration/about-subdomain-delegation.md#full-subdomain-delegation)
>
>* Les enregistrements CNAME prennent en charge la configuration des sous-domaines CNAME. [En savoir plus](../configuration/about-subdomain-delegation.md#cname-subdomain-setup)

L’alerte **Enregistrement DNS du domaine AJO manquant** est déclenchée lorsque le système détecte que les enregistrements NS ou CNAME requis sont absents ou qu’ils ne correspondent pas aux normes de configuration.

1. Cliquez sur l’alerte pour accéder au [sous-domaine](../configuration/delegate-subdomain.md) concerné dans l’interface [!DNL Journey Optimizer].

   <!--For guidance on editing delegated subdomains, see [this section](../configuration/delegate-subdomain.md).-->

1. Corrigez la configuration DNS en définissant correctement les enregistrements et [soumettez à nouveau la délégation du sous-domaine](../configuration/delegate-subdomain.md#submit-subdomain).

   >[!NOTE]
   >
   >Assurez-vous que tous les enregistrements sont correctement créés sur votre solution d’hébergement de domaine avant de continuer.

1. Si vous ne connaissez pas les valeurs correctes, vous pouvez créer un nouveau sous-domaine dans [!DNL Journey Optimizer] avec le même nom que le sous-domaine concerné. [Découvrez comment configurer un nouveau sous-domaine](../configuration/delegate-subdomain.md#set-up-subdomain).

Si les modifications ne permettent pas de résoudre le problème, la même alerte sera déclenchée à nouveau le lendemain.

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?-->

### Échec de configuration du canal AJO {#alert-channel-config-failure}

>[!IMPORTANT]
>
>Cette alerte s’applique uniquement aux configurations de canal **e-mail** utilisant le type de délégation [sous-domaine personnalisé](../configuration/delegate-custom-subdomain.md). <!--Other channel types (such as SMS, push, or in-app) are not covered by this alert.-->

Cette alerte est déclenchée au cas où l’audit du système détecterait des problèmes de configuration du canal e-mail. Ces problèmes peuvent inclure des paramètres de canal mal configurés, une configuration DNS non valide, un problème de liste de suppression, une incohérence d’adresse IP ou toute autre erreur pouvant avoir un impact sur la diffusion des e-mails.

Si vous recevez une telle alerte, les étapes de résolution sont répertoriées ci-dessous :

1. Cliquez sur l’alerte pour être redirigé vers la [configuration du canal e-mail](../email/get-started-email-config.md) affectée dans l’interface [!DNL Journey Optimizer].

   Pour obtenir des conseils sur la modification des configurations de canal, voir [cette section](../configuration/channel-surfaces.md#edit-channel-surface).

1. Vérifiez les détails de configuration et les messages d’erreur fournis. Les raisons courantes d’échec sont les suivantes :

   * Échec de la validation SPF
   * Échec de la validation de DKIM
   * Échec de la validation de l’enregistrement MX
   * Enregistrements DNS non valides

   >[!NOTE]
   >
   >Les raisons possibles d’échec de la configuration sont répertoriées dans [cette section](../configuration/channel-surfaces.md).

1. Résolvez le problème :

   * Mettez à jour la configuration du canal si nécessaire.
   * Vous devrez peut-être résoudre des problèmes DNS spécifiques mentionnés dans l’alerte.

   >[!NOTE]
   >
   >Comme un seul domaine peut être associé à plusieurs configurations de canal, la résolution de problèmes DNS pour une configuration de canal peut résoudre automatiquement les problèmes liés à plusieurs configurations.

Si la modification ne résout pas le problème, la même alerte sera déclenchée à nouveau le lendemain.

Lors de la résolution des problèmes de configuration du canal e-mail, gardez à l&#39;esprit les bonnes pratiques répertoriées ci-dessous :

* Agissez rapidement - Corrigez les échecs de configuration dès qu’ils sont détectés afin d’éviter toute interruption de la diffusion des e-mails.
* Vérifier toutes les configurations - Si l’alerte indique plusieurs configurations d’e-mail affectées, examinez et corrigez chacune d’elles.

<!--### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->

## Gérer les alertes {#manage-alerts}

### Modification d’une alerte

Vous pouvez vérifier les détails d’une alerte en cliquant sur sa ligne. Le nom, le statut et les canaux de notification s’affichent dans le panneau de gauche.
<!--DOCAC-13465
For Journey alerts, use the **[!UICONTROL More actions]** button to edit them. You can then define a [custom theshold](#custom-threshold) for these alerts.-->

![](assets/alert-more-actions.png){width=60%}

<!--DOCAC-13465
#### Define a custom threshold {#custom-threshold}

You can set thresholds for the [Journey alerts](#journey-alerts). The threshold alerts above default to 20%. 

To change the threshold:

1. Browse to the **Alerts** screen
1. Click the **[!UICONTROL More actions]** button of the alert to update
1. Enter the new threshold and confirm. The new threshold applies to **all** journeys


![](assets/alert-threshold.png){width=60%}

>[!CAUTION]
>
>The threshold levels are global across all journeys and cannot be individually modified per journey.
-->

### Désactivation d’une alerte

Par défaut, toutes les alertes sont activées. Pour désactiver une alerte, sélectionnez l’option **[!UICONTROL Désactiver l’alerte]** : tous les abonnés à cette alerte ne recevront plus les notifications associées.


### Statuts des alertes

Les statuts d’alerte possibles sont énumérés ci-dessous :

* **[!UICONTROL Activé]** : l’alerte est activée et contrôle la condition de déclenchement.
* **[!UICONTROL Désactivé]** : l’alerte est désactivée et ne contrôle pas la condition de déclenchement. Vous ne recevrez aucune notification pour cette alerte.
* **[!UICONTROL Déclenché]** : la condition de déclenchement de l’alerte est respectée.


### Afficher et mettre à jour les abonnés {#manage-subscribers}

Sélectionnez **[!UICONTROL Gérer les abonnés aux alertes]** pour afficher la liste des utilisateurs et utilisatrices qui se sont abonnés à l’alerte.

![](assets/alert-subscribers.png){width=80%}

Pour ajouter d’autres abonnés et abonnées, saisissez leur adresse e-mail séparée par une virgule, puis sélectionnez **[!UICONTROL Mettre à jour]**.

Pour supprimer des abonnés, supprimez leur adresse e-mail des abonnés actuels, puis sélectionnez **[!UICONTROL Mettre à jour]**.

## Ressources supplémentaires {#additional-resources-alerts}


* Découvrez comment résoudre les problèmes de vos parcours sur [cette page](../building-journeys/troubleshooting.md).
* Découvrez comment vérifier vos campagnes sur [cette page](../campaigns/review-activate-campaign.md).