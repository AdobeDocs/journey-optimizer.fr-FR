---
solution: Journey Optimizer
product: journey optimizer
title: Ajout d’un enregistrement TXT Google à un sous-domaine
description: Découvrez comment ajouter un enregistrement TXT Google à un sous-domaine.
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: sous-domaine, google, txt, enregistrement, gmail, délivrabilité
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
TQID: https://experienceleague.adobe.com/FCUB2NeETecjNGYnVhkpkYtEZqgX6y-czXinn2t3J84
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 324
ht-degree: 91%

---

# Ajout d’un enregistrement TXT Google à un sous-domaine {#google-txt-record}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment ajouter et mettre à jour un enregistrement TXT de vérification de site Google sur votre sous-domaine pour réussir la diffusion des e-mails aux adresses Gmail.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Enregistrements TXT Google"
>abstract="Pour garantir la réussite de l’envoi d’e-mails aux adresses Gmail, vous pouvez ajouter des enregistrements TXT de vérification de site Google spéciaux à votre sous-domaine pour vous assurer qu’il est vérifié."

Les enregistrements TXT font partie des enregistrements DNS. Ils servent à donner des informations textuelles à propos d’un domaine, que des sources externes pourront lire par la suite.

Pour garantir une délivrabilité optimale et une diffusion réussie des e-mails vers les adresses Gmail, [!DNL Journey Optimizer] permet dʼajouter des enregistrements TXT de vérification de site Google spéciaux à vos sous-domaines afin dʼassurer qu’ils soient vérifiés.

>[!CAUTION]
>
> Cette opération ne peut être effectuée que lorsqu&#39;un sous-domaine a le statut **[!UICONTROL Succès]**. Pour en savoir plus sur les statuts des sous-domaines, consultez [cette section](delegate-subdomain.md#access-delegated-subdomains).

## Ajouter un enregistrement TXT Google {#add-google-txt-record}

Pour ajouter un enregistrement TXT Google à votre sous-domaine, procédez comme suit :

1. Ouvrez le sous-domaine à partir du menu **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres des e-mails]** > **[!UICONTROL Sous-domaines]**.

1. Dans la section **[!UICONTROL Enregistrement TXT Google]**, saisissez le code de vérification généré depuis [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->, puis cliquez sur **[!UICONTROL Enregistrer]**.

   ![](assets/subdomain-google-txt.png)

1. Une fois l’enregistrement TXT ajouté, vous devez le faire vérifier par Google. Pour ce faire, accédez à [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->, puis lancez lʼétape de vérification.

## Mettre à jour un enregistrement TXT Google {#update-google-txt-record}

Pour mettre à jour un enregistrement TXT Google existant, procédez comme suit :

1. Ouvrez le sous-domaine à partir du menu **[!UICONTROL Sous-domaines]**.

1. Effacez la valeur existante dans le champ **[!UICONTROL Enregistrement TXT Google]** et cliquez sur **[!UICONTROL Enregistrer]**. Cette étape remplace la valeur d’enregistrement TXT Google précédente par une chaîne vide.

1. Rouvrez maintenant le même sous-domaine et saisissez le nouveau code de vérification.

1. Cliquez de nouveau sur **[!UICONTROL Enregistrer]**.

1. Vérifiez l’enregistrement mis à jour via [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}.
