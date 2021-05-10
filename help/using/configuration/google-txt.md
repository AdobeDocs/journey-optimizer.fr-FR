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
source-git-commit: 6988a6ab9412e5d27f1ba9d1145cc11c7c06e7b7
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 24%

---


# Ajouter un enregistrement Google TXT à un sous-domaine

Les enregistrements TXT font partie des enregistrements DNS. Ils servent à donner des informations textuelles à propos d’un domaine, que des sources externes pourront lire par la suite.

Afin d’assurer une bonne délivrabilité et une diffusion réussie des courriers électroniques aux adresses Gmail, la Gestion des Parcours clients vous permet d’ajouter des enregistrements TXT spéciaux de vérification de site Google à vos sous-domaines pour vous assurer qu’ils sont vérifiés.

>[!NOTE]
>
> Cette opération ne peut être effectuée qu&#39;une fois qu&#39;un sous-domaine a l&#39;état **[!UICONTROL Success]**. Pour plus d&#39;informations sur les états des sous-domaines, consultez [cette section](access-subdomains.md).

Pour ajouter un enregistrement Google TXT à votre sous-domaine, procédez comme suit :

1. Ouvrez le sous-domaine à partir du menu **[!UICONTROL Canaux]** / **[!UICONTROL Sous-domaines]**.

1. Dans la section des enregistrements de texte de Google, saisissez le code de vérification généré dans [Outils d’administration de la suite ](https://support.google.com/a/answer/183895), puis cliquez sur **[!UICONTROL Enregistrer]**.

![](../assets/subdomain-google-txt.png)

1. Une fois l’enregistrement TXT ajouté, vous devez le faire vérifier par Google. Pour ce faire, accédez aux outils d’administration de la Suite G, puis lancez l’étape de vérification.
