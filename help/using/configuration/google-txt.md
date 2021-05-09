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
translation-type: tm+mt
source-git-commit: 65e677860a6ba77532cc23b992d2671652548d0f
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# Ajouter un enregistrement Google TXT à un sous-domaine

Les enregistrements TXT sont un type d&#39;enregistrements DNS utilisés pour fournir des informations textuelles sur un domaine, qui peuvent être lues par des sources externes.

Afin d’assurer une bonne délivrabilité et une diffusion réussie des courriers électroniques aux adresses Gmail, la Gestion des Parcours clients vous permet d’ajouter des enregistrements TXT spéciaux de vérification de site Google à vos sous-domaines pour vous assurer qu’ils sont vérifiés.

>[!NOTE]
>
> Cette opération ne peut être exécutée qu&#39;une fois qu&#39;un sous-domaine a l&#39;état **[!UICONTROL Vérifié]**. Pour plus d&#39;informations sur les états des sous-domaines, consultez [cette section](access-subdomains.md).

Pour ajouter un enregistrement Google TXT à votre sous-domaine, procédez comme suit :

1. Ouvrez le sous-domaine à partir du menu **[!UICONTROL Configuration du message]** / **[!UICONTROL délégation du sous-domaine]**.

1. Dans la section des enregistrements de texte de Google, saisissez le code de vérification généré dans [Outils d’administration de la suite ](https://support.google.com/a/answer/183895), puis cliquez sur **[!UICONTROL Enregistrer]**.

![](../assets/subdomain-google-txt.png)

1. Une fois l’enregistrement TXT ajouté, vous devez le faire vérifier par Google. Pour ce faire, accédez aux outils d’administration de la Suite G, puis lancez l’étape de vérification.
