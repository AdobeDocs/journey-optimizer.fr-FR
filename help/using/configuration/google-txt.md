---
solution: Journey Optimizer
product: journey optimizer
title: Ajout d’un enregistrement TXT Google à un sous-domaine
description: Découvrez comment ajouter un enregistrement TXT Google à un sous-domaine.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: sous-domaine, google, txt, enregistrement, gmail, délivrabilité
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 72%

---

# Ajout d’un enregistrement TXT Google à un sous-domaine {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Enregistrements TXT Google"
>abstract="Pour garantir la réussite de l’envoi d’e-mails aux adresses Gmail, vous pouvez ajouter des enregistrements TXT de vérification de site Google spéciaux à votre sous-domaine pour vous assurer qu’il est vérifié."

Les enregistrements TXT sont un type d’enregistrement DNS utilisé pour fournir des informations textuelles sur un domaine, qui peuvent être lues par des sources externes.

Pour garantir une délivrabilité optimale et une diffusion réussie des e-mails vers les adresses Gmail, [!DNL Journey Optimizer] permet dʼajouter des enregistrements TXT de vérification de site Google spéciaux à vos sous-domaines afin dʼassurer qu’ils soient vérifiés.

>[!CAUTION]
>
> Cette opération ne peut être effectuée que lorsqu&#39;un sous-domaine a le statut **[!UICONTROL Succès]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](about-subdomain-delegation.md#access-delegated-subdomains).

Pour ajouter un enregistrement TXT Google à votre sous-domaine, procédez comme suit :

1. Ouvrez le sous-domaine à partir du menu **[!UICONTROL Canaux]**/**[!UICONTROL Sous-domaines]**.

1. Dans le **[!UICONTROL Enregistrement de texte Google]** , saisissez le code de vérification généré à partir de [Espace de travail Google](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->, puis cliquez sur **[!UICONTROL Enregistrer]**.

   ![](assets/subdomain-google-txt.png)

1. Une fois l’enregistrement TXT ajouté, vous devez le faire vérifier par Google. Pour ce faire, accédez à [Espace de travail Google](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->, puis lancez l’étape de vérification.
