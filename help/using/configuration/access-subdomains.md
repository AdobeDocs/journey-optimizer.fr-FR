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
exl-id: cb3248c5-f444-47aa-80b2-c1a9fbebfcc0
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: ht
source-wordcount: '167'
ht-degree: 100%

---

# Accès aux sous-domaines délégués

Tous les sous-domaines délégués s&#39;affichent dans le menu **[!UICONTROL Canaux]**/**[!UICONTROL Sous-domaines]**. Des filtres sont disponibles pour vous aider à affiner la liste (date de délégation, utilisateur ou statut).

![](../assets/subdomain-list.png)

La colonne **[!UICONTROL Statut]** fournit des informations sur le processus de délégation de sous-domaine :

* **[!UICONTROL Version préliminaire]** : la délégation de sous-domaine a été enregistrée en tant que version préliminaire. Cliquez sur le nom du sous-domaine pour reprendre le processus de délégation,
* **[!UICONTROL Traitement]** : le sous-domaine fait l&#39;objet de plusieurs contrôles de configuration avant de pouvoir être utilisé,
* **[!UICONTROL Succès]** : le sous-domaine a passé les contrôles avec succès et peut être utilisé pour diffuser des messages,
* **[!UICONTROL Échec]** : un ou plusieurs contrôles ont échoué après l&#39;envoi de la délégation de sous-domaine.

Pour accéder à des informations détaillées sur un sous-domaine, ouvrez-le dans la liste. Vous pouvez :

* Récupérer le nom du sous-domaine (lecture seule) configuré pendant le processus de délégation, ainsi que les URL générées (ressources, pages miroir, URL de tracking),

* Ajouter un enregistrement TXT de vérification de site Google à votre sous-domaine pour vous assurer qu&#39;il est vérifié (voir [Ajout d&#39;un enregistrement TXT Google à un sous-domaine](google-txt.md)).

![](../assets/subdomain-delegated.png)
