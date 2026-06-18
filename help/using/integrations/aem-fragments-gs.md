---
solution: Journey Optimizer
product: journey optimizer
title: Fragments de contenu AEM
description: Découvrir comment accéder aux fragments de contenu AEM et comment les gérer
topic: Content Management
role: User
level: Beginner
exl-id: c36a53a4-c324-4082-838e-ed27bd3b2e90
TQID: https://experienceleague.adobe.com/GRQ3Wz7Y4YJ3545mTtju0R8en9BYiejyo8UoMx558nM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 28395abcdcba6ed8fd02f252a57022aa473f3d3b
workflow-type: tm+mt
source-wordcount: 319
ht-degree: 22%

---

# Prise en main des fragments de contenu Adobe Experience Manager {#aem-fragments}

>[!BEGINSHADEBOX]

**Sur cette page :** Commencez avec les fragments de contenu Adobe Experience Manager et découvrez comment leur cycle de vie de création et de publication détermine les fragments disponibles dans Journey Optimizer.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Pour la clientèle du secteur de la santé, l’intégration n’est activée qu’après l’obtention d’une licence pour les offres complémentaires Journey Optimizer Healthcare Shield et Adobe Experience Manager Enhanced Security.

En intégrant **[!DNL Adobe Experience Manager as a Cloud Service]** et **[!DNL Adobe Experience Manager Managed Service]** à Adobe Journey Optimizer, vous pouvez utiliser les fragments de contenu d’AEM dans les parcours et les campagnes. Par **[!DNL Adobe Experience Manager Managed Service]**, l’intégration prend en charge les niveaux **Auteur** et **Publication** sur **le service SP2 de support à long terme (LTS) d’AEM** ; les mises à jour en temps réel de Adobe Experience Manager ne sont pas disponibles dans cette version. Contactez votre représentant Adobe Managed Services pour la configuration de l’instance, puis [configurez l’accès au référentiel Adobe Experience Manager](aem-admin-settings.md) pour ajouter votre référentiel Managed Services.

Pour en savoir plus sur les fragments de contenu AEM, voir [Utilisation des fragments de contenu](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} dans la documentation d’Experience Manager.

## Cycle de vie du fragment de contenu

![](assets/do-not-localize/AEM_CF.png)

Les fragments de contenu suivent différentes étapes du cycle de vie en fonction du niveau Adobe Experience Manager dans lequel ils existent. [En savoir plus dans la documentation de Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

Le contenu est créé et géré au **niveau Auteur**, où les fragments peuvent avoir des statuts tels que Nouveau, Brouillon, Publié, Modifié ou Dépublié. Ces statuts s’appliquent uniquement au **niveau Auteur** et prennent en charge la création et la révision de contenu.

Lorsqu’un fragment de contenu est publié, une copie est créée au **niveau Publication** et exposée via un point d’entrée public non authentifié. Par **[!DNL Adobe Experience Manager as a Cloud Service]**, Journey Optimizer prend en charge l’intégration avec les niveaux **Auteur** et **Publication**.

Par conséquent, Journey Optimizer n’affiche que les fragments de contenu publiés ou modifiés et utilise toujours la dernière version publiée. Les modifications apportées après la publication ne sont pas répercutées dans Journey Optimizer tant que le fragment de contenu n’a pas été republié.
