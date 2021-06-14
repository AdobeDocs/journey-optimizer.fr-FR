---
title: Enregistrements PTR
description: '"Découvrez comment gérer les ptr-records"'
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
source-wordcount: '169'
ht-degree: 1%

---


# Enregistrements PTR

## À propos des enregistrements PTR

Un enregistrement pointeur (PTR) est un type d’enregistrement DNS (Domain Name System) qui fournit le nom de domaine associé à une adresse IP.

Avec les enregistrements PTR, les serveurs de messagerie de réception peuvent vérifier l’authenticité des serveurs de messagerie d’envoi en identifiant si leurs adresses IP correspondent aux noms avec lesquels les serveurs se connectent.

## Accès aux enregistrements PTR de vos sous-domaines

Une fois qu’un sous-domaine est délégué dans Customer Journey Management, un enregistrement PTR est automatiquement créé et associé à ce sous-domaine. Vous pouvez y accéder à partir du menu **[!UICONTROL Canaux]** / **[!UICONTROL Enregistrements PTR]** .

![](../assets/ptr-records.png)

La liste affiche les enregistrements PTR générés pour chaque sous-domaine délégué, en utilisant la syntaxe ci-dessous :

* &quot;r&quot; pour l’enregistrement,
* &quot;xx&quot; pour les deux derniers chiffres de l&#39;adresse IP,
* nom du sous-domaine.

Vous pouvez ouvrir un enregistrement PTR de la liste pour afficher le nom de sous-domaine et l’adresse IP associés.

>[!NOTE]
>
>Notez que les enregistrements PTR sont en lecture seule et que vous ne pouvez pas modifier le sous-domaine associé à une adresse IP.
