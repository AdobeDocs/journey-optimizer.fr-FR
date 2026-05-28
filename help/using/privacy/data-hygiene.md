---
solution: Journey Optimizer
product: journey optimizer
title: Effectuer des opérations de cycle de vie des données
description: Découvrez comment effectuer des opérations de cycle de vie des données.
feature: Privacy, Monitoring
role: User
level: Intermediate
exl-id: 8045b559-bf5e-4b5f-9da4-accd44641a68
TQID: https://experienceleague.adobe.com/-zue9aNrWtfL3MGs7OjH-1CF436mzPh50fsru8OSEq8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 100%

---

# Effectuer des opérations de cycle de vie des données {#data-hygiene}

>[!AVAILABILITY]
>
>Les fonctionnalités de cycle de vie des données ne sont actuellement disponibles que pour les organisations qui ont acheté les offres complémentaires **Healthcare Shield** et **Privacy and Security Shield**.

Comme les données sont ingérées en permanence dans Adobe Experience Platform, il devient essentiel de s’assurer que vos données sont utilisées comme prévu, mises à jour si nécessaire et supprimées selon les politiques de l’entreprise.

Ces tâches peuvent être effectuées à l’aide du menu **[!UICONTROL Cycle de vie des données]** qui vous permet de configurer et de planifier les opérations d’hygiène des données, en veillant à ce que vos enregistrements soient correctement conservés.

![](assets/data-hygiene.png)


## Recommandations {#data-hygiene-recommendations}

Lors de l’exécution d’opérations de nettoyage des données (telles que la suppression d’identités ou de jeux de données), n’oubliez pas que les événements de diffusion historiques associés aux identités supprimées n’apparaîtront plus dans les rapports standard ou les requêtes de lac de données. Cela peut entraîner des incohérences entre le nombre d’e-mails **Diffusés** et le nombre d’e-mails **Reçus** dans les boîtes de réception des destinataires, en particulier pour les parcours plus anciens.

Avant d’exécuter des suppressions à grande échelle, validez et exportez toutes les données de diffusion ou de création de rapports requises. Si une réconciliation s’avère nécessaire après le nettoyage des données, contactez l’assistance Adobe pour accéder aux journaux archivés ou utilisez des requêtes de jeu de données d’événement de feedback sur les messages pour obtenir des données récentes.

## En savoir plus {#data-hygiene-learn-more}

Pour plus d’informations sur Privacy Service et sur la réalisation des opérations de cycle de vie des données, consultez la documentation d’Adobe Experience Platform :

* [Présentation de Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=fr)
* [Cycle de vie des données dans Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/home.html?lang=fr)
