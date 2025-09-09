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
source-git-commit: 13623d28ba7b852f7267b5f800f2c9a3afda4a62
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 80%

---

# Accéder et s’abonner aux alertes système {#alerts}

Lors de la création de vos parcours et campagnes, utilisez le bouton **Alertes** pour les vérifier et résoudre les erreurs avant de les exécuter ou de les publier :

* Découvrez comment résoudre les problèmes de vos parcours sur [cette page](../building-journeys/troubleshooting.md).
* Découvrez comment vérifier vos campagnes sur [cette page](../campaigns/review-activate-campaign.md).

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

* Alertes spécifiques à la configuration des canaux :

   * Alerte [Enregistrement DNS du domaine AJO manquant](#alert-dns-record-missing)
  <!--* the [AJO channel configuration failure](#alert-channel-config-failure) alert
   * the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## S’abonner aux alertes {#subscribe-alerts}

1. Vous pouvez vous abonner individuellement à chaque alerte depuis l’interface d’utilisation en sélectionnant l’option **[!UICONTROL S’abonner]**.

   ![](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >L’abonnement s’applique uniquement à un sandbox spécifique. Vous devez vous abonner à des alertes pour chaque sandbox.

1. Utilisez la même méthode pour vous **[!UICONTROL désabonner]**.

1. Vous pouvez également vous abonner aux alertes par le biais des [notifications d’événements d’entrée/sortie](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=fr){target="_blank"}. Les règles d’alerte sont organisées en différents packages d’abonnement. Les abonnements aux événements correspondant aux alertes Journey Optimizer spécifiques sont présentés [ci-dessous](#journey-alerts).

1. Si un comportement inattendu se produit, et/ou qu’un certain ensemble de conditions de vos opérations est atteint (par exemple, un problème potentiel lorsque le système dépasse un certain seuil), des notifications d’alerte sont envoyées à l’ensemble des personnes de votre organisation qui s’y sont abonnées.

En fonction des préférences des personnes abonnées, les alertes sont envoyées par e-mail ou directement dans le centre de notification de Journey Optimizer, dans le coin supérieur droit de l’interface d’utilisation (notifications in-app). Sélectionnez le mode de réception de ces alertes dans les **[!UICONTROL Préférences]** [!DNL Adobe Experience Cloud]. [En savoir plus](../start/user-interface.md#in-product-alerts)

>[!NOTE]
>
>Par défaut, seules les alertes in-app sont activées.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=fr#enable-email-alerts){target="_blank"}.-->

Lorsqu’une alerte est résolue, les personnes abonnées reçoivent une notification « Résolue ».

## Gérer les alertes {#manage-alerts}

Pour gérer les alertes, sélectionnez un élément et utilisez le bouton **[!UICONTROL Plus d’actions]**.

![](assets/alert-more-actions.png){width=80%}

Par défaut, toutes les alertes sont activées. Pour désactiver une alerte, sélectionnez l’option **[!UICONTROL Désactiver l’alerte]** dans le menu **[!UICONTROL Plus d’actions]**. Toutes les personnes abonnées à cette alerte ne recevront plus les notifications associées.

Sélectionnez **[!UICONTROL Gérer les personnes abonnées aux alertes]** pour afficher la liste des personnes qui se sont abonnées à l’alerte. Utilisez le champ vide pour ajouter d’autres personnes abonnées.

![](assets/alert-subscribers.png){width=80%}

Les statuts d’alerte possibles sont énumérés ci-dessous :

* **[!UICONTROL Activé]** : l’alerte est activée et contrôle la condition de déclenchement.
* **[!UICONTROL Désactivé]** : l’alerte est désactivée et ne contrôle pas la condition de déclenchement. Vous ne recevrez aucune notification pour cette alerte.
* **[!UICONTROL Déclenché]** : la condition de déclenchement de l’alerte est respectée.

## Alertes de parcours {#journey-alerts}

>[!CAUTION]
>
>Les alertes spécifiques à Adobe Journey Optimizer s’appliquent uniquement aux parcours **dynamiques**. Les alertes ne seront pas déclenchées pour les parcours en mode test.

### Échec de l’action personnalisée du parcours {#alert-custom-actions}

Cette alerte vous avertit si une action personnalisée échoue. Nous considérons qu’il existe un échec quand plus de 1 % d’erreurs sont commises sur une action personnalisée spécifique au cours des 5 dernières minutes. Ces données sont évaluées toutes les 30 secondes.

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





