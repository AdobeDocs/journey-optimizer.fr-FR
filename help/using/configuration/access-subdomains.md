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
source-git-commit: 2d8b7bbaee7509d4cc33445c64b2382ed14a9678
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---


# Accès aux sous-domaines délégués

Tous les sous-domaines délégués s’affichent dans le menu **[!UICONTROL Canaux]** / **[!UICONTROL Sous-domaines]** . Des filtres sont disponibles pour vous aider à affiner la liste (date de délégation, utilisateur ou statut).

![](../assets/subdomain-list.png)

La colonne **[!UICONTROL Status]** fournit des informations sur le processus de délégation de sous-domaine :

* **[!UICONTROL Version préliminaire]** : La délégation de sous-domaine a été enregistrée en tant que brouillon. Cliquez sur le nom du sous-domaine pour reprendre le processus de délégation,
* **[!UICONTROL Traitement]** : Le sous-domaine fait l&#39;objet de plusieurs contrôles de configuration avant de pouvoir être utilisé,
* **[!UICONTROL Succès]** : Le sous-domaine a passé les contrôles avec succès et peut être utilisé pour diffuser des messages,
* **[!UICONTROL Échec]** : Une ou plusieurs vérifications ont échoué après l’envoi de la délégation de sous-domaine.

Pour accéder à des informations détaillées sur un sous-domaine, ouvrez-le dans la liste. Vous pouvez :

* Récupérez le nom du sous-domaine (lecture seule) configuré pendant le processus de délégation, ainsi que les URL générées (ressources, page miroir, URL de tracking),

* Ajoutez un enregistrement TXT de vérification de site Google à votre sous-domaine pour vous assurer qu’il est vérifié (voir [Ajout d’un enregistrement TXT Google à un sous-domaine](google-txt.md)).

![](../assets/subdomain-delegated.png)
