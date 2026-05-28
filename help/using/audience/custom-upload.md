---
solution: Journey Optimizer
product: journey optimizer
title: À propos des audiences Adobe Experience Platform
description: Découvrez comment utiliser les audiences Adobe Experience Platform.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 71c652ba-f38f-452c-9c1b-dcd728307baf
TQID: https://experienceleague.adobe.com/HkybhydJwQDHVEXCKM5o16ZNeiBk-n9mogm-2pwFKus
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 89%

---

# Chargement personnalisé {#custom-upload}

Le portail Audience d’Adobe Experience Platform permet d’importer une audience à l’aide d’un fichier CSV.

Pendant le processus de chargement personnalisé, spécifiez l’attribut CSV à utiliser comme identité et l’identité de profil à laquelle il correspond. Cela établit un lien entre les données de l’audience et le profil. Si le fichier CSV contient une valeur d’identité introuvable dans le profil, un nouveau profil est créé avec cette valeur d’identité.

>[!NOTE]
>
>Pour les audiences de chargement personnalisé, si l’option « Lecture incrémentielle » est activée dans un parcours récurrent, les profils ne sont récupérés que lors de la première périodicité, car ces audiences sont fixes.

![](assets/import-audience.png)

Vous trouverez des informations détaillées sur l’importation d’audiences dans Adobe Experience Platform [documentation du service de segmentation](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}.

Découvrez comment charger des audiences au format CSV dans cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)
