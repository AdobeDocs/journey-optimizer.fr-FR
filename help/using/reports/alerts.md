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
source-git-commit: 074390ccd77d3753d9b347a67dcbad0611cb3e49
workflow-type: tm+mt
source-wordcount: '1865'
ht-degree: 68%

---

# Accéder et s’abonner aux alertes système {#alerts}

Lors de la création de vos parcours et campagnes, utilisez le bouton **Alertes** pour vérifier et résoudre les erreurs avant de les exécuter ou les publier.

* Découvrez comment résoudre les problèmes liés à vos parcours sur [cette page](../building-journeys/troubleshooting.md)

* Découvrez comment vérifier vos campagnes sur [cette page](../campaigns/review-activate-campaign.md)


En outre, lorsqu’un certain ensemble de conditions est atteint, des messages d’alerte peuvent être envoyés à tous les utilisateurs de votre organisation qui se sont abonnés à ces messages. Ces alertes sont disponibles à partir du menu dédié **[!UICONTROL Alertes]**. Adobe Experience Platform fournit plusieurs règles d’alerte prédéfinies que vous pouvez activer pour votre organisation. En outre, vous pouvez vous abonner à des alertes système spécifiques à [!DNL Adobe Journey Optimizer], comme indiqué sur cette page.

>[!NOTE]
>
>En savoir plus sur les alertes dans Adobe Experience Platform dans la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=fr){target="_blank"}.

Dans le menu de gauche, sous **[!UICONTROL Administration]**, cliquez sur **[!UICONTROL Alertes]**. Plusieurs alertes préconfigurées pour Journey Optimizer sont disponibles dans l’onglet **Parcourir**.


* Alertes spécifiques aux parcours :

   * Alerte [Échec de l’action personnalisée de parcours](#alert-custom-actions)
   * Alerte [Échec du déclenchement de la lecture d’audience](#alert-read-audiences)
   * l’alerte [Taux de rejet du profil dépassé](#alert-discard-rate)
   * l’alerte [&#x200B; Taux d’erreur d’action personnalisée dépassé &#x200B;](#alert-custom-action-error-rate)
   * l’alerte [Taux d’erreur de profil dépassé](#alert-profile-error-rate)

* Alertes spécifiques à la configuration des canaux :

   * Alerte [Enregistrement DNS du domaine AJO manquant](#alert-dns-record-missing)
   * Alerte [Échec de configuration du canal AJO](#alert-channel-config-failure)
     <!--* the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## S’abonner aux alertes {#subscribe-alerts}

Si un comportement inattendu se produit, et/ou qu’un certain ensemble de conditions de vos opérations est atteint (par exemple, un problème potentiel lorsque le système dépasse un certain seuil), des notifications d’alerte sont envoyées à l’ensemble des personnes de votre organisation qui s’y sont abonnées.

Vous pouvez vous abonner à chaque alerte individuellement à partir de l’interface utilisateur, soit globalement à partir du menu **[!UICONTROL Alertes]** (voir [Abonnement global](#global-subscription)), soit unitairement pour un parcours spécifique (voir [Abonnement unitaire](#unitary-subscription)).

En fonction des préférences des personnes abonnées, les alertes sont envoyées par e-mail ou directement dans le centre de notification de Journey Optimizer, dans le coin supérieur droit de l’interface d’utilisation (notifications in-app). Sélectionnez le mode de réception de ces alertes dans les **[!UICONTROL Préférences]** [!DNL Adobe Experience Cloud]. [En savoir plus](../start/user-interface.md#in-product-alerts)

Lorsqu’une alerte est résolue, les personnes abonnées reçoivent une notification « Résolue ».


### Abonnement global {#global-subscription}

Pour vous abonner ou vous désabonner d’une alerte pour tous les parcours et campagnes, procédez comme suit :

1. Accédez au tableau de bord **[!UICONTROL Alertes]** dans le menu de gauche, puis sélectionnez l’option **[!UICONTROL S’abonner]** correspondant à l’alerte à laquelle vous souhaitez vous abonner.

   ![Abonnement à une alerte](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >L’abonnement s’applique uniquement à un sandbox spécifique. Vous devez vous abonner à des alertes pour chaque sandbox.

1. Utilisez la même méthode pour vous **[!UICONTROL désabonner]**.

Vous pouvez également vous abonner par le biais des [notifications d’événements d’E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=fr){target="_blank"}. Les règles d’alerte sont organisées en différents packages d’abonnement. Les abonnements aux événements correspondant aux alertes Journey Optimizer spécifiques sont présentés [ci-dessous](#journey-alerts).

### Abonnement unitaire {#unitary-subscription}

Pour vous abonner/désabonner à une alerte pour un parcours spécifique, procédez comme suit :

1. Accédez à l’inventaire des parcours et sélectionnez l’option **[!UICONTROL S’abonner aux alertes]** pour un parcours spécifique.

   ![Abonnement à une alerte concernant un parcours spécifique](assets/subscribe-journey-alert.png){width=80%}

1. Choisissez la ou les alertes. Les alertes suivantes sont disponibles : [Taux de rejet du profil dépassé](#alert-discard-rate), [Taux d’erreur de l’action personnalisée dépassé](#alert-custom-action-error-rate) et [Taux d’erreur du profil dépassé](#alert-profile-error-rate).

1. Pour vous désabonner d’une alerte, désélectionnez-la dans le même écran.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=fr#enable-email-alerts){target="_blank"}.-->

## Alertes de parcours {#journey-alerts}

>[!CAUTION]
>
>Les alertes spécifiques à Adobe Journey Optimizer s’appliquent uniquement aux parcours **dynamiques**. Les alertes ne seront pas déclenchées pour les parcours en mode test.


### Échec de l’action personnalisée du parcours {#alert-custom-actions}

Cette alerte vous avertit si une action personnalisée échoue. Nous considérons qu’il existe un échec quand plus de 1 % d’erreurs sont commises sur une action personnalisée spécifique au cours des 5 dernières minutes. Ces données sont évaluées toutes les 30 secondes.

Cliquez sur le nom de l’alerte pour vérifier ses détails et sa configuration.

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

### Taux de rejet de profil dépassé {#alert-discard-rate}

Cette alerte vous avertit si le ratio des abandons de profil par rapport aux profils entrés au cours des 5 dernières minutes a dépassé le seuil. Le seuil par défaut est défini sur 20 %, mais vous pouvez [définir un seuil personnalisé](#custom-threshold).

Cliquez sur le nom de l’alerte pour vérifier ses détails et sa configuration.

Il existe plusieurs raisons pour lesquelles un profil peut être ignoré, ce qui éclairera la méthode de dépannage. Voici quelques raisons courantes :

* Profil ignoré à l’entrée car il est déjà en ligne dans ce parcours unitaire. Pour résoudre ce problème, assurez-vous que le profil a suffisamment de temps pour quitter le parcours avant l’arrivée de l’événement suivant pour ce profil.
* L’identité n’est pas définie pour le profil ou l’espace de noms utilisé par le parcours Lecture d’audience n’est pas utilisé dans ce profil. Pour résoudre ce problème, assurez-vous que l’espace de noms du parcours correspond à l’espace de noms d’identité utilisé par les profils.
* Le taux de débit de l’événement est dépassé. Pour résoudre ce problème, assurez-vous que les événements qui entrent dans le système ne dépassent pas ces limites.


### Taux d’erreurs des actions personnalisées dépassé {#alert-custom-action-error-rate}

Cette alerte vous avertit si le taux d’erreurs d’action personnalisée par rapport aux appels HTTP réussis au cours des 5 dernières minutes a dépassé le seuil. Le seuil par défaut est défini sur 20 %, mais vous pouvez [définir un seuil personnalisé](#custom-threshold).

Les erreurs d’actions personnalisées peuvent se produire pour diverses raisons. Vous pouvez effectuer les actions suivantes :

* Vérifiez que l’action personnalisée est correctement configurée.
* Vérifiez que le point d’entrée est accessible et que l’action personnalisée peut y accéder via le vérificateur de connectivité de l’action personnalisée
* Vérifiez les informations d’authentification, vérifiez la connectivité Internet, etc.

### Taux d’erreurs de profil dépassé {#alert-profile-error-rate}

Cette alerte vous avertit si le taux d’erreurs d’action personnalisée par rapport aux appels HTTP réussis au cours des 5 dernières minutes a dépassé le seuil. Le seuil par défaut est défini sur 20 %, mais vous pouvez [définir un seuil personnalisé](#custom-threshold).

Cliquez sur le nom de l’alerte pour vérifier ses détails et sa configuration.

Pour éviter cela, vous pouvez interroger les données des événements d’étape pour comprendre où et pourquoi le profil a échoué dans le parcours.

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

### Échec de configuration des canaux AJO {#alert-channel-config-failure}

>[!IMPORTANT]
>
>Cette alerte s’applique uniquement aux configurations du canal **E-mail** utilisant le type de délégation [sous-domaine personnalisé](../configuration/delegate-custom-subdomain.md). <!--Other channel types (such as SMS, push, or in-app) are not covered by this alert.-->

Cette alerte est déclenchée lorsque l’audit système détecte des problèmes de configuration du canal E-mail. Ces problèmes peuvent comprendre des paramètres de canal mal configurés, une configuration DNS non valide, un problème de liste de suppression, une incohérence d’adresses IP ou toute autre erreur pouvant avoir un impact sur la diffusion des e-mails.

Si vous recevez une alerte de ce type, les étapes de résolution sont répertoriées ci-dessous :

1. Cliquez sur l’alerte pour accéder à la [configuration du canal e-mail](../email/get-started-email-config.md) concernée dans l’interface [!DNL Journey Optimizer].

   Pour obtenir des instructions afin de modifier des configurations de canal, voir [cette section](../configuration/channel-surfaces.md#edit-channel-surface).

1. Vérifiez les détails de configuration et les messages d’erreur fournis. Les causes courantes d’échec sont les suivantes :

   * Échec de la validation SPF
   * Échec de la validation DKIM
   * Échec de la validation des enregistrements MX
   * Enregistrements DNS non valides

   >[!NOTE]
   >
   >Les raisons possibles de l’échec de configuration sont répertoriées dans [cette section](../configuration/channel-surfaces.md).

1. Résolvez le problème :

   * Mettez à jour la configuration du canal si nécessaire.
   * Vous devrez peut-être résoudre des problèmes DNS spécifiques mentionnés dans l’alerte.

   >[!NOTE]
   >
   >Comme un seul domaine peut être associé à plusieurs configurations de canal, la résolution des problèmes DNS pour une configuration de canal peut permettre de corriger automatiquement les problèmes liés à plusieurs configurations.

Si les modifications ne permettent pas de résoudre le problème, la même alerte sera déclenchée à nouveau le lendemain.

Lors de la résolution des problèmes de configuration du canal e-mail, gardez à l’esprit les bonnes pratiques répertoriées ci-dessous :

* Agissez rapidement : corrigez les erreurs de configuration dès qu’elles sont détectéss afin d’éviter toute interruption de la diffusion des e-mails.
* Vérifiez toutes les configurations : si l’alerte indique plusieurs configurations d’e-mail affectées, examinez et corrigez chacune d’elles.

<!--### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->

## Gérer les alertes {#manage-alerts}

### Modifier une alerte

Vous pouvez vérifier les détails d’une alerte en cliquant sur sa ligne. Le nom, le statut et les canaux de notification s’affichent dans le panneau de gauche.
Pour les alertes de Parcours, utilisez le bouton **[!UICONTROL Autres actions]** pour les modifier. Vous pouvez ensuite définir un [seuil personnalisé](#custom-threshold) pour ces alertes.

![](assets/alert-more-actions.png){width=60%}

#### Définir un seuil personnalisé {#custom-threshold}

Vous pouvez définir des seuils pour les [alertes de Parcours &#x200B;](#journey-alerts). Le seuil d’alerte ci-dessus est défini par défaut sur 20 %.

Pour modifier le seuil :

1. Accédez à l’écran **Alertes**
1. Cliquez sur le bouton **[!UICONTROL Autres actions]** de l’alerte à mettre à jour
1. Saisissez le nouveau seuil et confirmez. Le nouveau seuil s’applique à **tous** parcours


![](assets/alert-threshold.png){width=60%}

>[!CAUTION]
>
>Les niveaux de seuil sont globaux pour tous les parcours et ne peuvent pas être modifiés individuellement par parcours.

### Désactiver une alerte

Par défaut, toutes les alertes sont activées. Pour désactiver une alerte, sélectionnez l’option **[!UICONTROL Désactiver l’alerte]** : les personnes abonnées à cette alerte ne recevront plus les notifications associées.


### Statuts d’alerte

Les statuts d’alerte possibles sont énumérés ci-dessous :

* **[!UICONTROL Activé]** : l’alerte est activée et contrôle la condition de déclenchement.
* **[!UICONTROL Désactivé]** : l’alerte est désactivée et ne contrôle pas la condition de déclenchement. Vous ne recevrez aucune notification pour cette alerte.
* **[!UICONTROL Déclenché]** : la condition de déclenchement de l’alerte est respectée.


### Afficher et mettre à jour les personnes abonnées {#manage-subscribers}

Sélectionnez **[!UICONTROL Gérer les personnes abonnées aux alertes]** pour afficher la liste des personnes qui se sont abonnées à l’alerte.

![](assets/alert-subscribers.png){width=80%}

Pour ajouter d’autres personnes abonnées, saisissez les adresses e-mails séparées par des virgules, puis sélectionnez **[!UICONTROL Mettre à jour]**.

Pour supprimer des personnes abonnées, supprimez leurs adresses e-mail de la liste des personnes actuellement abonnées, puis sélectionnez **[!UICONTROL Mettre à jour]**.

## Ressources supplémentaires {#additional-resources-alerts}

* Découvrez comment résoudre les problèmes de vos parcours sur [cette page](../building-journeys/troubleshooting.md).
* Découvrez comment vérifier vos campagnes sur [cette page](../campaigns/review-activate-campaign.md).