---
solution: Journey Optimizer
product: journey optimizer
title: Ajout d’un enregistrement TXT Google à un sous-domaine
description: Découvrez comment ajouter un enregistrement TXT Google à un sous-domaine
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Ajout d’un enregistrement TXT Google à un sous-domaine {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Enregistrements TXT Google"
>abstract="Pour garantir le succès de la diffusion des emails vers les adresses Gmail, vous pouvez ajouter des enregistrements TXT de vérification de site Google spéciaux à votre sous-domaine pour vous assurer qu’il est vérifié."

Les enregistrements TXT sont un type d’enregistrements DNS utilisé pour fournir des informations textuelles sur un domaine, qui peuvent être lues par des sources externes.

Afin d&#39;assurer une délivrabilité optimale et une diffusion réussie des emails vers les adresses Gmail, [!DNL Journey Optimizer] vous permet d’ajouter des enregistrements TXT de vérification de site Google spéciaux à votre sous-domaine pour vous assurer qu’il est vérifié.

>[!CAUTION]
>
> Cette opération ne peut être effectuée qu’une fois qu’un sous-domaine possède la propriété **[!UICONTROL Success]** statut. Pour plus d’informations sur les statuts des sous-domaines, reportez-vous à la section [cette section](about-subdomain-delegation.md#access-delegated-subdomains).

Pour ajouter un enregistrement TXT Google à votre sous-domaine, procédez comme suit :

1. Ouvrez le sous-domaine à partir du **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** .

1. Dans le **[!UICONTROL Google txt record]** , saisissez le code de vérification généré à partir de [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, puis cliquez sur **[!UICONTROL Save]**.

   ![](assets/subdomain-google-txt.png)

1. Une fois l’enregistrement TXT ajouté, vous devez le faire vérifier par Google. Pour ce faire, accédez à [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->, puis lancez l’étape de vérification.
