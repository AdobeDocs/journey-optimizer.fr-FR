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
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
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

>[!VIDEO](https://video.tv.adobe.com/v/3423356?captions=fre_fr&quality=12)
