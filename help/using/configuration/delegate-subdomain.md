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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: a174944bb8efcb67d758d4fe215674c1b8bbee13
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 97%

---

# Délégation d&#39;un sous-domaine

La délégation de noms de domaine est une méthode qui permet au propriétaire d&#39;un nom de domaine (techniquement : une zone DNS) de déléguer une sous-division (techniquement : une zone DNS située au-dessous, qui peut être appelée sous-zone) à une autre entité. En tant que client, si vous gérez la zone &quot;example.com&quot;, vous pouvez déléguer la sous-zone &quot;marketing.example.com&quot; à l’Adobe.

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

   >[!CAUTION]
   >
   >La délégation d’un sous-domaine non valide à Adobe n’est pas autorisée. Veillez à saisir un sous-domaine valide détenu par votre entreprise, tel que marketing.votre_entreprise.com.
   >
   >Veuillez noter que les sous-domaines à plusieurs niveaux tels que email.marketing.votre_entreprise.com ne sont actuellement pas pris en charge.

1. La liste des enregistrements à placer dans les serveurs DNS s&#39;affiche. Copiez ces enregistrements un par un ou en téléchargeant un fichier CSV, puis accédez à votre solution d&#39;hébergement de domaine pour générer les enregistrements DNS correspondants.

1. Assurez-vous que tous les enregistrements DNS ont été générés dans votre solution d&#39;hébergement de domaine. Si tout est correctement configuré, cochez la case &quot;Je confirme...&quot;, puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Vous pouvez créer les enregistrements et soumettre ultérieurement la configuration du sous-domaine à l&#39;aide du bouton **[!UICONTROL Enregistrer en tant que version préliminaire]**. Vous pourrez ensuite reprendre la délégation de sous-domaine en l&#39;ouvrant à partir de la liste de sous-domaines.

1. Une fois la délégation de sous-domaine envoyée, le sous-domaine s&#39;affiche dans la liste avec le statut **[!UICONTROL Traitement]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](access-subdomains.md).

   ![](../assets/subdomain-processing.png)

   Avant de pouvoir utiliser ce sous-domaine pour envoyer des messages, vous devez attendre qu’Adobe effectue les vérifications nécessaires, ce qui peut prendre jusqu’à 3 heures. En savoir plus dans [cette section](#subdomain-validation).

1. Une fois les vérifications effectuées, le sous-domaine obtient le statut **[!UICONTROL Succès]**. Il est prêt à être utilisé pour diffuser des messages.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)

## Validation de sous-domaine {#subdomain-validation}

Les vérifications et actions ci-dessous seront effectuées jusqu&#39;à ce que le sous-domaine soit vérifié et puisse être utilisé pour envoyer des messages.

>[!NOTE]
>
>Ces étapes sont effectuées par Adobe et peuvent prendre jusqu&#39;à 3 heures.

1. **Pré-validation** : Adobe vérifie si le sous-domaine a été délégué au DNS Adobe (enregistrement NS, enregistrement SOA, configuration de zone, enregistrement propriétaire). Si l’étape de pré-validation échoue, une erreur est renvoyée avec la raison correspondante, sinon Adobe passe à l’étape suivante.

1. **Configuration du DNS pour le domaine**:

   * **Enregistrement MX** (enregistrement Mail eXchange) : enregistrement du serveur de messagerie qui traite les e-mails entrants envoyés au sous-domaine.
   * **Enregistrement SPF** (enregistrement Sender Policy Framework) : répertorie les adresses IP des serveurs de messagerie qui peuvent envoyer des e-mails à partir du sous-domaine.
   * **Enregistrement DKIM** (enregistrement standard DomainKeys Identified Mail) : utilise le chiffrement de la clé publique-privée pour authentifier le message afin d’éviter les usurpations.
   * **A** : mappage IP par défaut.

1. **Création des URL de tracking et miroir** : si le domaine est email.example.com, le domaine tracking/mirror sera data.email.example.com. La sécurité est assurée par l’installation du certificat SSL.

1. **Approvisionnement de CDN CloudFront** : si le réseau CDN n’est pas déjà configuré, Adobe l’approvisionne pour l’imsorg.

1. **Création d’un domaine CDN** : si le domaine est email.example.com, le domaine CDN sera cdn.email.example.com.

1. **Création et association d’un certificat SSL CDN** : Adobe crée le certificat CDN pour le domaine CDN et associe le certificat au domaine CDN.

1. **Création d’un DNS forward** : s’il s’agit du premier sous-domaine que vous déléguez, Adobe crée le DNS forward qui est requis pour créer des enregistrements PTR, un pour chacune de vos adresses IP.

1. **Création d’un enregistrement PTR** : l’enregistrement PTR, également appelé enregistrement DNS inversé, est requis par les FAI pour qu’ils ne marquent pas les e-mails comme spam. Gmail recommande également d’avoir des enregistrements PTR pour chaque adresse IP. Adobe crée des enregistrements PTR uniquement lorsque vous déléguez le premier sous-domaine, un pour chaque adresse IP, toutes les adresses IP pointant vers le premier sous-domaine. Par exemple, si l’adresse IP est *192.1.2.1* et que le sous-domaine est *email.example.com*, l’enregistrement PTR est : *192.1.2.1 PTR r1.email.example.com*. Vous pouvez mettre à jour l’enregistrement PTR par la suite pour pointer vers le nouveau domaine délégué.
