---
solution: Journey Optimizer
product: journey optimizer
title: Délégation de sous-domaine dans [!DNL Journey Optimizer]
description: Découvrez comment déléguer vos sous-domaines
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 0%

---

# Délégation de sous-domaine dans [!DNL Journey Optimizer] {#subdomain-delegation}

La création d’un sous-domaine pour les campagnes par e-mail permet aux marques d’isoler différents types de trafic (marketing ou entreprise, par exemple) dans des pools d’adresses IP spécifiques et avec des domaines spécifiques, ce qui accélère le processus de préparation des adresses IP et améliore globalement la délivrabilité. Si vous partagez un domaine et qu’il est bloqué ou ajouté à la liste refusée, cela peut avoir un impact sur la diffusion de votre courrier d’entreprise. Cependant, les problèmes de réputation ou les blocs sur un domaine spécifique à vos communications marketing par e-mail auront un impact sur ce flux d’e-mail. L’utilisation de votre domaine principal comme adresse d’expéditeur ou d’expéditeur pour plusieurs diffusions de courrier électronique peut également interrompre l’authentification des emails, ce qui peut entraîner le blocage ou la placement de vos messages dans le dossier spam.

>[!NOTE]
>
>Vous ne pouvez pas utiliser le même domaine d’envoi pour envoyer des messages depuis [!DNL Adobe Journey Optimizer] et provenant d’un autre produit, tel que [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage].

## Pourquoi configurer des sous-domaines ? {#why-setting-up-subdomains}

Un sous-domaine est une division de votre domaine qui peut être utilisée pour isoler vos marques ou divers types de trafic, par exemple les messages transactionnels et les communications marketing.

Prenons l&#39;exemple du domaine &quot;mybrand.com&quot;, qui est utilisé pour envoyer des communications transactionnelles et marketing. Dans ce cas, vous pouvez décider de configurer deux sous-domaines :

* sous-domaine &quot;info.mybrand.com&quot; pour vos communications transactionnelles (confirmation des achats, réinitialisation du mot de passe, etc.),
* Sous-domaine &quot;marketing.mybrand.com&quot; pour vos emails de prospection.

Ce faisant, vous contribuerez à préserver la réputation de votre domaine et des autres sous-domaines. Par exemple, si les sous-domaines &quot;marketing.mybrand.com&quot; se retrouvaient ajoutés à la liste bloquée par les fournisseurs de services Internet en raison d’une mauvaise délivrabilité, cela empêcherait l’ajout du domaine &quot;mybrand.com&quot; entier et du sous-domaine &quot;info.mybrand.com&quot; à la liste bloquée.

Lors de la mise en oeuvre d’une solution, les composants externes sont requis : il s’agit notamment de configurer des liens et des pages web qui feront l’objet d’un suivi, d’afficher des pages miroir, etc.

Bien que ces exigences soient gérées par le biais de composants hébergés à la fois par Adobe et par le client, elles incluent des URL que les destinataires des emails peuvent voir. Pour ne pas avoir d’URL indiquant la solution technique ou le fournisseur d’hébergement sous-jacent, il est possible de configurer des sous-domaines afin de les rendre transparentes aux destinataires des emails.

**En savoir plus**

* Découvrez comment [déléguer vos sous-domaines](delegate-subdomain.md) directement depuis l’interface
* Découvrez comment [Ajout d’enregistrements TXT Google](google-txt.md) à vos sous-domaines pour assurer la diffusion réussie des emails vers les adresses Gmail.
* Découvrez comment [Accéder aux enregistrements PTR](ptr-records.md) générés pour vos sous-domaines, ce qui permet de les vérifier en envoyant des serveurs de messagerie

## Méthodes de configuration de sous-domaine {#subdomain-delegation-methods}

La configuration de sous-domaine vous permet de configurer une sous-section de votre domaine (techniquement, une &quot;zone DNS&quot;) à utiliser avec Adobe Campaign. Les méthodes de configuration disponibles sont les suivantes :

* **Délégation complète de sous-domaine à Adobe** (recommandé) : Le sous-domaine est entièrement délégué à Adobe. Adobe peut contrôler et gérer tous les aspects du DNS nécessaires à la diffusion, au rendu et au suivi des messages. [En savoir plus sur la délégation complète de sous-domaine](delegate-subdomain.md#full-subdomain-delegation)

* **Utilisation de CNAME**: Créez un sous-domaine et utilisez des CNAME pour pointer vers des enregistrements spécifiques à Adobe. Grâce à cette configuration, vous partagez avec Adobe la responsabilité de la maintenance du DNS. [En savoir plus sur la délégation de sous-domaine CNAME](delegate-subdomain.md#cname-subdomain-delegation)

>[!CAUTION]
>
>* La délégation complète de sous-domaine est la méthode préconisée.
>
>* La méthode CNAME est recommandée si les stratégies de votre entreprise limitent la méthode de délégation de sous-domaine complète. Cette approche nécessite que vous gardiez et gériez vos enregistrements DNS vous-même. Adobe ne pourra pas vous aider à modifier, gérer ou gérer le DNS d’un sous-domaine configuré à l’aide de la méthode CNAME.


Le tableau ci-dessous résume le fonctionnement de ces méthodes, ainsi que le niveau d’effort implicite :

| Méthode de configuration | Fonctionnement | Niveau d&#39;effort |
|---|---|---|
| **Délégation complète** | Créez l’enregistrement du sous-domaine et de l’espace de noms. Adobe configurera alors tous les enregistrements DNS requis pour Adobe Campaign.<br/><br/>Dans cette configuration, Adobe est entièrement responsable de la gestion du sous-domaine et de tous les enregistrements DNS. | Faible |
| **CNAME, méthode personnalisée** | Créez l’enregistrement du sous-domaine et de l’espace de noms. Adobe fournira alors les enregistrements à placer dans vos serveurs DNS et configurera les valeurs correspondantes dans les serveurs DNS Adobe Campaign.<br/><br/>Dans cette configuration, vous partagez avec Adobe la responsabilité de la maintenance du DNS. | Élevée |

Des informations supplémentaires sur la configuration des domaines sont disponibles dans la section [cette documentation](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

Si vous avez des questions concernant les méthodes de configuration de sous-domaine, contactez Adobe ou l’assistance clientèle pour demander des conseils sur la délivrabilité.

## Accès aux sous-domaines délégués {#access-delegated-subdomains}

Tous vos sous-domaines délégués s’affichent dans la **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Subdomains]** . Des filtres sont disponibles pour vous aider à affiner la liste (date de délégation, utilisateur ou statut).

![](assets/subdomain-list.png)

Le **[!UICONTROL Status]** fournit des informations sur le processus de délégation de sous-domaine :

* **[!UICONTROL Draft]**: La délégation de sous-domaine a été enregistrée en tant que brouillon. Cliquez sur le nom du sous-domaine pour reprendre le processus de délégation,
* **[!UICONTROL Processing]**: Le sous-domaine fait l&#39;objet de plusieurs contrôles de configuration avant de pouvoir être utilisé,
* **[!UICONTROL Success]**: Le sous-domaine a passé les contrôles avec succès et peut être utilisé pour diffuser des messages,
* **[!UICONTROL Failed]**: Une ou plusieurs vérifications ont échoué après l’envoi de la délégation de sous-domaine.

Pour accéder à des informations détaillées sur un sous-domaine avec la variable **[!UICONTROL Success]** , ouvrez-le dans la liste.

![](assets/subdomain-delegated.png)

Vous pouvez :

* Récupérer le nom du sous-domaine (lecture seule) configuré pendant le processus de délégation, ainsi que les URL générées (ressources, pages miroir, URL de tracking),

* Ajoutez un enregistrement TXT de vérification de site Google à votre sous-domaine pour vous assurer qu’il est vérifié (voir [Ajout d’un enregistrement TXT Google à un sous-domaine](google-txt.md)).


>[!CAUTION]
>
>La configuration de sous-domaine est commune à tous les environnements. Par conséquent, toute modification apportée à un sous-domaine aura également un impact sur les environnements de test de production.
