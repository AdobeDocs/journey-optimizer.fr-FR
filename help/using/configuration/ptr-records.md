---
title: Enregistrements PTR
description: '"Découvrir comment gérér les enregistrements ptr"'
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
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: ht
source-wordcount: '169'
ht-degree: 100%

---


# Enregistrements PTR

## À propos des enregistrements PTR

Un enregistrement pointeur (PTR) est un type d&#39;enregistrement DNS (Domain Name System) qui fournit le nom de domaine associé à une adresse IP.

Avec les enregistrements PTR, les serveurs de messagerie de réception peuvent vérifier l&#39;authenticité des serveurs de messagerie d&#39;envoi en identifiant si leurs adresses IP correspondent aux noms avec lesquels les serveurs se connectent.

## Accès aux enregistrements PTR de vos sous-domaines

Une fois qu&#39;un sous-domaine est délégué dans Customer Journey Management, un enregistrement PTR est automatiquement créé et associé à ce sous-domaine. Vous pouvez y accéder à partir du menu **[!UICONTROL Canaux]** `>` **[!UICONTROL Enregistrements PTR]**.

![](../assets/ptr-records.png)

La liste affiche les enregistrements PTR générés pour chaque sous-domaine délégué, en utilisant la syntaxe ci-dessous :

* &quot;r&quot; pour l&#39;enregistrement,
* &quot;xx&quot; pour les deux derniers chiffres de l&#39;adresse IP,
* nom du sous-domaine.

Vous pouvez ouvrir un enregistrement PTR de la liste pour afficher le nom de sous-domaine et l&#39;adresse IP associés.

>[!NOTE]
>
>Veuillez noter que les enregistrements PTR sont en lecture seule et que vous ne pouvez pas modifier le sous-domaine associé à une adresse IP.
