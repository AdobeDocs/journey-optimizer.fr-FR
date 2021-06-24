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
feature: Paramétrage de l’application
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 100%

---


# Délégation d&#39;un sous-domaine

La délégation de noms de domaine est une méthode qui permet au propriétaire d&#39;un nom de domaine (techniquement : une zone DNS) de déléguer une sous-division (techniquement : une zone DNS située au-dessous, qui peut être appelée sous-zone) à une autre entité. En fait, si un client traite la zone &quot;exemple.com&#39;&#39;, il peut déléguer la sous-zone &quot;marketing.exemple.com&quot; à Adobe.

En déléguant un sous-domaine à utiliser avec [!DNL Journey Optimizer], les clients peuvent compter sur Adobe pour gérer l&#39;infrastructure DNS requise afin de répondre aux exigences de délivrabilité standard de leurs domaines de marketing par e-mail, tout en continuant à gérer et à contrôler le DNS de leurs domaines de messagerie internes.

[!DNL Journey Optimizer] vous permet de déléguer entièrement vos sous-domaines à Adobe directement à partir de l&#39;interface du produit. Ainsi, Adobe sera en mesure de diffuser des messages en tant que service géré en contrôlant et en gérant tous les aspects du DNS nécessaires à la diffusion, au rendu et au suivi des campagnes par e-mail.

>[!NOTE]
>
>Par défaut, le contrat de licence [!DNL Journey Optimizer] vous permet de déléguer jusqu&#39;à 10 sous-domaines. Contactez votre contact Adobe si vous souhaitez augmenter cette limite.
>
>L&#39;utilisation de CNAME pour la délégation de sous-domaine n&#39;est actuellement pas prise en charge par Journey Optimizer.

Pour déléguer un nouveau sous-domaine, procédez comme suit :

1. Accédez au menu **[!UICONTROL Canaux]**/**[!UICONTROL Sous-domaines]**, puis cliquez sur **[!UICONTROL Délégation de sous-domaine]**.

   ![](../assets/subdomain-delegate.png)

1. Indiquez le nom du sous-domaine à déléguer.

   ![](../assets/subdomain-name.png)

1. La liste des enregistrements à placer dans les serveurs DNS s&#39;affiche. Copiez ces enregistrements un par un ou en téléchargeant un fichier CSV, puis accédez à votre solution d&#39;hébergement de domaine pour générer les enregistrements DNS correspondants.

   Assurez-vous que tous les enregistrements DNS ont été générés dans votre solution d&#39;hébergement de domaine. Si tout est correctement configuré, cochez la case &quot;Je confirme...&quot;, puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Vous pouvez créer les enregistrements et soumettre ultérieurement la configuration du sous-domaine à l&#39;aide du bouton **[!UICONTROL Enregistrer en tant que version préliminaire]**. Vous pourrez ensuite reprendre la délégation de sous-domaine en l&#39;ouvrant à partir de la liste de sous-domaines.

1. Une fois la délégation de sous-domaine envoyée, le sous-domaine s&#39;affiche dans la liste avec le statut **[!UICONTROL Traitement]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](access-subdomains.md).

   Les vérifications et actions ci-dessous seront effectuées jusqu&#39;à ce que le sous-domaine soit vérifié et puisse être utilisé pour envoyer des messages.

   Cette étape est effectuée par Adobe et peut prendre jusqu&#39;à 3 heures.

   1. Vérifiez si le sous-domaine a été délégué au DNS Adobe (enregistrement NS, enregistrement SOA, configuration de zone, enregistrement propriétaire),
   1. Configuration du DNS pour le domaine,
   1. Création des URL de tracking et miroir,
   1. Configuration de CDN Cloud Front,
   1. Création, validation et association d&#39;un certificat SSL pour réseau CDN,
   1. Création d&#39;un DNS de transfert,
   1. Création d&#39;un enregistrement PTR.

   ![](../assets/subdomain-processing.png)

1. Une fois les vérifications effectuées, le sous-domaine obtient le statut **[!UICONTROL Succès]**. Il est prêt à être utilisé pour diffuser des messages.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)


