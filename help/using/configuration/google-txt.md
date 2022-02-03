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
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: bbc2adabac63ffb813ea2630f29aec552fc3f4df
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 100%

---

# Ajout d&#39;un enregistrement TXT Google à un sous-domaine {#google-txt-record}

Les enregistrements TXT font partie des enregistrements DNS. Ils servent à donner des informations textuelles à propos d&#39;un domaine, que des sources externes pourront lire par la suite.

Pour garantir une bonne délivrabilité et une diffusion réussie des e-mails vers les adresses Gmail, [!DNL Journey Optimizer] permet dʼajouter des enregistrements TXT de vérification de site Google spéciaux à vos sous-domaines afin de sʼassurer qu’ils soient vérifiés.

>[!CAUTION]
>
> Cette opération ne peut être effectuée que lorsqu&#39;un sous-domaine a le statut **[!UICONTROL Succès]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](access-subdomains.md).

Pour ajouter un enregistrement TXT Google à votre sous-domaine, procédez comme suit :

1. Ouvrez le sous-domaine à partir du menu **[!UICONTROL Canaux]**/**[!UICONTROL Sous-domaines]**.

1. Dans la section **[!UICONTROL Enregistrement TXT de Google]**, saisissez le code de vérification généré depuis [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, puis cliquez sur **[!UICONTROL Enregistrer]**.

   ![](../assets/subdomain-google-txt.png)

1. Une fois l’enregistrement TXT ajouté, vous devez le faire vérifier par Google. Pour ce faire, accédez à [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, puis entamez lʼétape de vérification.
