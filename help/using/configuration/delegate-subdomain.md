---
title: Délégation de sous-domaines
description: Découvrez comment déléguer vos sous-domaines
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: 068ee9c8966e5968a488c12b2a48fa2ba2ab5245
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 11%

---


# Délégation d’un sous-domaine

Journey Optimizer vous permet de déléguer entièrement vos sous-domaines à l’Adobe. Ce faisant, Adobe pourra diffuser des messages en tant que service géré en contrôlant et en gérant tous les aspects du DNS nécessaires à la diffusion, au rendu et au suivi des campagnes email.

>[!NOTE]
>
>Par défaut, le contrat de licence [!DNL Journey Optimizer] vous permet de déléguer jusqu’à 10 sous-domaines. Contactez votre Adobe si vous souhaitez augmenter cette limite.
>
>L’utilisation de CNAME pour la délégation de sous-domaine n’est actuellement pas prise en charge par Journey Optimizer.

Pour déléguer un nouveau sous-domaine, procédez comme suit :

1. Accédez au menu **[!UICONTROL Canaux]** / **[!UICONTROL Sous-domaines]**, puis cliquez sur **[!UICONTROL Déléguer le sous-domaine]**.

   ![](../assets/subdomain-delegate.png)

1. Indiquez le nom du sous-domaine à déléguer.

   ![](../assets/subdomain-name.png)

1. La liste des enregistrements à placer dans les serveurs DNS s’affiche. Copiez ces enregistrements un par un ou en téléchargeant un fichier CSV, puis accédez à votre solution d’hébergement de domaine pour générer les enregistrements DNS correspondants.

   Assurez-vous que tous les enregistrements DNS ont été générés dans votre solution d’hébergement de domaine. Si tout est correctement configuré, cochez la case &quot;Je confirme...&quot;, puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Vous pouvez créer les enregistrements et soumettre ultérieurement la configuration du sous-domaine à l’aide du bouton **[!UICONTROL Enregistrer en tant que brouillon]**. Vous pourrez ensuite reprendre la délégation de sous-domaine en l’ouvrant à partir de la liste de sous-domaines.

1. Une fois la délégation de sous-domaine envoyée, le sous-domaine s’affiche dans la liste avec le statut **[!UICONTROL Traitement]** . Pour plus d’informations sur les états des sous-domaines, reportez-vous à [cette section](access-subdomains.md).

   Les vérifications et actions ci-dessous seront effectuées jusqu’à ce que le sous-domaine soit vérifié et puisse être utilisé pour envoyer des messages.

   Cette étape est effectuée par Adobe et peut prendre jusqu’à 3 heures.

   1. Vérifiez si le sous-domaine a été délégué au DNS de l’Adobe (enregistrement NS, enregistrement SOA, configuration de zone, enregistrement propriétaire),
   1. Configuration du DNS pour le domaine,
   1. Créer des URL de tracking et miroir,
   1. Configuration de CDN Cloud Front,
   1. Créer, valider et joindre un certificat SSL CDN,
   1. Créer un DNS de transfert,
   1. Créez un enregistrement PTR.

   ![](../assets/subdomain-processing.png)

1. Une fois les vérifications effectuées, le sous-domaine obtient l’état **[!UICONTROL Succès]**. Il est prêt à être utilisé pour diffuser des messages.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)


