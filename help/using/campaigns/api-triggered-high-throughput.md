---
solution: Journey Optimizer
product: journey optimizer
title: Activer le mode de débit élevé pour les campagnes déclenchées par API
description: Découvrez comment activer le mode de débit élevé pour les campagnes déclenchées par API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, déclenchement par API, REST, optimizer, messages
exl-id: 2b3e87dc-097a-4d05-873c-f421d11338c3
TQID: https://experienceleague.adobe.com/SwmK1epuhZUf4EWnaLRHTBH-eE1hEV02Z8nqXGtMb6U
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: cf64c7f6-7428-4ae5-b158-8df9771f38f4id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721id: fa683eda-48de-4558-af32-2673edcd44feid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 100%

---

# Activer le mode de débit élevé pour les campagnes déclenchées par API {#high-throughput}

Le mode de débit élevé est conçu pour les organisations qui ont besoin de **messages transactionnels en temps réel à très grande échelle** (jusqu’à 5 000 transactions par seconde). Contrairement aux campagnes standard déclenchées par API, les campagnes à débit élevé fonctionnent indépendamment des profils Adobe et nécessitent un modèle de configuration différent.

Cette page explique en quoi les campagnes à débit élevé diffèrent des campagnes standard déclenchées par API, les exigences de configuration et quand choisir chaque mode.

## Mécanismes de sécurisation et limitations

* **Accès** : disponible uniquement aux États-Unis pour les organisations disposant d’une licence avec le module complémentaire High Throughput transactional messaging.

* **Canaux** : actuellement disponible uniquement pour les e-mails.

* **Personnalisation** :

   * Toutes les personnalisations doivent être incluses dans la payload de l’API en tant que **données contextuelles**. [Découvrez comment personnaliser du contenu à l’aide de données contextuelles](../campaigns/api-triggered-campaign-content.md#contextual).
   * La personnalisation basée sur un profil n’est pas prise en charge. Si des variables de profil sont utilisées, des erreurs de validation se produisent.

* **Configurations de canal personnalisées** - Les configurations de canal qui utilisent [la personnalisation basée sur les profils](../email/surface-personalization.md) ne peuvent pas être utilisées avec des campagnes à débit élevé. Seules les surfaces sans personnalisation de profil peuvent être utilisées.

* **Point d’entrée de l’API** : les campagnes à débit élevé utilisent un point d’entrée différent des campagnes standard déclenchées par API. Pour plus d’informations, voir [Exécuter une campagne déclenchée par API](../campaigns/trigger-campaigns.md#trigger).

* **Exclusivité de la campagne** - Les campagnes à débit élevé n’utilisent pas les profils Adobe. Les messages sont diffusés qu’il existe un profil ou non.

  De plus, une campagne ne peut pas être utilisée à la fois pour les cas d’utilisation avec ou sans profil. Si vous avez besoin des deux, créez deux campagnes distinctes et assurez-vous que le système d’appel décide laquelle déclencher en fonction du contexte.

* **Jeux de données pour le feedback et le suivi** - Les données de feedback et de suivi pour les campagnes à débit élevé sont stockées dans des jeux de données dédiés qui ne sont pas activés pour fonctionner avec les profils. Par conséquent, ces événements ne sont pas associés à des profils, même s’il existe un profil correspondant.

  Les jeux de données utilisés sont les suivants :

   * **Jeu de données d’événements de feedback de messages AJO - Pas activé pour les profils**
   * **Jeu de données d’événements d’expériences de suivi d’e-mails AJO - Pas activé pour les profils**

* **Attribution du débit** - Le débit fourni via le module complémentaire Débit élevé est exclusivement réservé aux campagnes à débit élevé. Le débit des campagnes déclenchées par API standard et à débit élevé n’est pas partagé.

## Choisir entre des campagnes standard ou à débit élevé

Utilisez ce tableau pour décider quel type de campagne déclenché par API correspond à votre cas d’utilisation :

| Fonctionnalité/exigence | Campagne standard déclenchée par API | Campagne à débit élevé |
|------------------------|---------------------------------|---------------------------|
| **Disponibilité** | Incluse dans l’offre de base | Nécessite le module complémentaire High Throughput transactional messaging. |
| **Débit** | Jusqu’à 500 transactions par seconde | Jusqu’à 5 000 transactions par seconde |
| **Canaux** | E-mail, SMS, Push | E-mail |
| **Personnalisation** | Profil + contextuel dans la payload de l’API | Contextuel dans la payload de l’API uniquement |
| **Profil et rattachement** | Existe ou est créé avec des événements rattaché à un profil. | Aucun profil |
| **Volume des messages** | Droits standard et packs de messages | Volumes de messages hiérarchisés distincts |
| **Infrastructure** | Standard | Amélioré |
| **Temps de disponibilité** | 99,9 % | 99,99 % |
| **API Health check** | Oui | Oui |

En d’autres termes :

* Choisissez les campagnes **standard déclenchées par API** si :
   * Vous n’avez pas de contrat avec débit élevé.
   * Le débit dont vous avez besoin est &lt; 500 TPS.
   * Vous avez besoin d’une personnalisation basée sur les profils Adobe.
   * Vous souhaitez que les données de campagne soient rattachées aux profils pour un ciblage futur.
   * Vous souhaitez utiliser un autre canal que E-mail.

* Choisissez les campagnes à **débit élevé** si :
   * Vous avez besoin d’un débit > 500 TPS.
   * Vous n’avez pas besoin de rattacher les données aux profils.
   * Vous pouvez transmettre toute la personnalisation dans la payload de l’API.
   * Vous souhaitez utiliser le canal E-mail.

## Instructions relatives à la configuration

Pour configurer correctement des campagnes à débit élevé, suivez ces instructions :

1. Créez un groupe d’adresses IP. [Découvrir comment créer des groupes d’adresses IP](../configuration/ip-pools.md)
1. Créez une configuration de canal. [Découvrir comment configurer les canaux](../configuration/channel-surfaces.md)
1. Contactez l’assistance clientèle d’Adobe pour demander que la surface activée soit mappée à la fonctionnalité de débit élevé. Fournissez la configuration du canal et les détails du groupe d’adresses IP avec votre ID d’organisation.

>[!IMPORTANT]
>
>Les configurations du groupe d’adresses IP et du canal désignées pour les messages transactionnels à débit élevé doivent être utilisées exclusivement à cette fin et non pas avec des messages transactionnels standard à l’aide de campagnes ou de parcours déclenchés par API.
