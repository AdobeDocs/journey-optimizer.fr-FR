---
title: Enregistrements PTR
description: Découvrez comment xxxx
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
translation-type: tm+mt
source-git-commit: a65cefd0bbd15ffa389bac910eaceb40181cb38d
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# Enregistrements PTR

## A propos des enregistrements PTR

Un enregistrement pointeur (PTR) est un type d&#39;enregistrement DNS (Domain Name System) qui fournit le nom de domaine lié à une adresse IP.

Avec les enregistrements PTR, les serveurs de messagerie de réception peuvent vérifier l&#39;authenticité des serveurs de messagerie d&#39;envoi en identifiant si leurs adresses IP correspondent aux noms avec lesquels les serveurs se connectent.

## Accéder aux enregistrements PTR de vos sous-domaines

Une fois qu’un sous-domaine est délégué dans la gestion du parcours du client, un enregistrement PTR est automatiquement créé et associé à ce sous-domaine. Vous pouvez y accéder à partir du menu **[!UICONTROL Configuration du message]** / **[!UICONTROL Enregistrements PTR]**.

    -SCREENSHOT-

La liste affiche les enregistrements PTR générés pour chaque sous-domaine délégué, en utilisant la syntaxe ci-dessous :

Les enregistrements PTR respectent une syntaxe de dénomination spécifique :
* &quot;r&quot; pour le compte rendu,
* &quot;xx&quot; pour 2 derniers chiffres de l’adresse IP,
* nom du sous-domaine.

Vous pouvez ouvrir un enregistrement PTR à partir de la liste pour afficher le nom de sous-domaine et l’adresse IP associés.

>[!NOTE]
>
>Notez que les enregistrements PTR sont en lecture seule et que vous ne pouvez pas modifier le sous-domaine associé à une adresse IP.
