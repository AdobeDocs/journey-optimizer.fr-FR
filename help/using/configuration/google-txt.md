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
source-git-commit: 1d7f661dc0a89e4754a76ecf2cdce1e43a5275ec
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 60%

---

# Ajout d&#39;un enregistrement TXT Google à un sous-domaine

Les enregistrements TXT font partie des enregistrements DNS. Ils servent à donner des informations textuelles à propos d&#39;un domaine, que des sources externes pourront lire par la suite.

Afin d&#39;assurer une bonne délivrabilité et une diffusion réussie des emails vers les adresses Gmail, [!DNL Journey Optimizer] vous permet d’ajouter des enregistrements TXT de vérification de site Google spéciaux à vos sous-domaines pour vous assurer qu’ils sont vérifiés.

>[!CAUTION]
>
> Cette opération ne peut être effectuée que lorsqu&#39;un sous-domaine a le statut **[!UICONTROL Succès]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](access-subdomains.md).

Pour ajouter un enregistrement TXT Google à votre sous-domaine, procédez comme suit :

1. Ouvrez le sous-domaine à partir du menu **[!UICONTROL Canaux]**/**[!UICONTROL Sous-domaines]**.

1. Dans le **[!UICONTROL Enregistrement de texte Google]** , saisissez le code de vérification généré à partir de [Espace de travail Google](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, puis cliquez sur **[!UICONTROL Enregistrer]**.

   ![](../assets/subdomain-google-txt.png)

1. Une fois l&#39;enregistrement TXT ajouté, vous devez le faire vérifier par Google. Pour ce faire, accédez à [Espace de travail Google](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, puis lancez l’étape de vérification.
