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
source-wordcount: '169'
ht-degree: 24%

---


# Ajout d’un enregistrement TXT Google à un sous-domaine

Les enregistrements TXT font partie des enregistrements DNS. Ils servent à donner des informations textuelles à propos d’un domaine, que des sources externes pourront lire par la suite.

Afin d’assurer une bonne délivrabilité et une diffusion réussie des emails aux adresses Gmail, la gestion des Parcours clients vous permet d’ajouter des enregistrements TXT de vérification de site Google spéciaux à vos sous-domaines pour vous assurer qu’ils sont vérifiés.

>[!NOTE]
>
> Cette opération ne peut être effectuée que lorsqu’un sous-domaine a le statut **[!UICONTROL Succès]**. Pour plus d’informations sur les états des sous-domaines, reportez-vous à [cette section](access-subdomains.md).

Pour ajouter un enregistrement TXT Google à votre sous-domaine, procédez comme suit :

1. Ouvrez le sous-domaine à partir du menu **[!UICONTROL Canaux]** / **[!UICONTROL Sous-domaines]** .

1. Dans la section Enregistrement de texte Google, saisissez le code de vérification généré dans [Outils d’administration de la suite G](https://support.google.com/a/answer/183895), puis cliquez sur **[!UICONTROL Enregistrer]**.

   ![](../assets/subdomain-google-txt.png)

1. Une fois l’enregistrement TXT ajouté, vous devez le faire vérifier par Google. Pour ce faire, accédez aux outils G Suite Admin, puis lancez l’étape de vérification.
