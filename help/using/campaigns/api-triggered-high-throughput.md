---
solution: Journey Optimizer
product: journey optimizer
title: Activer le mode Débit élevé pour les campagnes déclenchées par l’API
description: Découvrez comment activer le mode Débit élevé pour les campagnes déclenchées par l’API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, déclenchement par API, REST, optimizer, messages
source-git-commit: 5a6abcd48495a66496495e62c6027c2fd0fdd4c4
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 5%

---


# Activer le mode Débit élevé pour les campagnes déclenchées par l’API {#high-throughput}

Le mode à haut débit est conçu pour les organisations qui ont besoin de **messages transactionnels en temps réel à très grande échelle** (jusqu’à 5 000 transactions par seconde). Contrairement aux campagnes standard déclenchées par API, les campagnes à débit élevé fonctionnent indépendamment des profils Adobe et nécessitent un modèle de configuration différent.

Cette page explique en quoi les campagnes à débit élevé diffèrent des campagnes standard déclenchées par l’API, les exigences de configuration et le moment où choisir chaque mode.

## Mécanismes de sécurisation et limitations

* **Accès** - Disponible uniquement aux États-Unis pour les organisations disposant d’une licence avec le module complémentaire de messagerie transactionnelle à haut débit.

* **Canaux** : actuellement disponible uniquement pour les e-mails.

* **Personalization**:

   * Toutes les personnalisations doivent être incluses dans la payload de l’API en tant que **données contextuelles**. [Découvrez comment personnaliser du contenu à l’aide de données contextuelles](../campaigns/api-triggered-campaign-action.md#contextual)
   * La personnalisation basée sur un profil n’est pas prise en charge. Si des variables de profil sont utilisées, des erreurs de validation se produisent.

* **Configurations de canal personnalisées** - Les configurations de canal qui utilisent [la personnalisation basée sur les profils](../email/surface-personalization.md) ne peuvent pas être utilisées avec des campagnes à débit élevé. Seules les surfaces sans personnalisation de profil peuvent être utilisées.

* **Point d’entrée de l’API** - Les campagnes à haut débit utilisent un point d’entrée différent des campagnes déclenchées par l’API standard. Pour plus d’informations, voir [Exécution d’une campagne déclenchée par une API](../campaigns/trigger-campaigns.md#trigger).

* **Exclusivité de la campagne** - Les campagnes à débit élevé n’utilisent pas les profils Adobe. Les messages sont diffusés qu’il existe un profil ou non.

  De plus, une campagne ne peut pas être utilisée à la fois pour les cas d’utilisation activés et non activés pour le profil. Si vous avez besoin des deux, créez deux campagnes distinctes et assurez-vous que le système d’appel décide laquelle déclencher en fonction du contexte.

## Choix entre des campagnes standard ou à débit élevé

Utilisez ce tableau pour décider quel type de campagne déclenché par l’API correspond à votre cas d’utilisation :

| Fonctionnalité/exigence | Campagne déclenchée par l’API standard | Campagne à haut débit |
|------------------------|---------------------------------|---------------------------|
| **Disponibilité** | Inclus dans l’offre de base | Nécessite un module complémentaire de messagerie transactionnelle à débit élevé. |
| **Débit** | Jusqu’à 500 transactions par seconde | Jusqu’à 5 000 transactions par seconde |
| **Canaux** | E-mail, SMS, Push | E-mail |
| **Personnalisation** | Profil + contextuel dans la payload de l’API | Contextuel dans la payload de l’API uniquement |
| **Profil et groupement** | Existe ou est créé avec des événements assemblés à un profil | Aucun profil |
| **Volume des messages** | Droits standard et packs de messages | Volumes de messages hiérarchisés distincts |
| **Infrastructure** | Standard | Amélioré |
| **Temps de disponibilité** | 99,9 % | 99,99 % |
| **API de vérification d’intégrité** | Oui | Oui |

En d’autres termes :

* Choisissez les campagnes **standard déclenchées par l’API** si :
   * Vous n’avez pas de contrat de débit élevé.
   * Vos besoins de débit sont &lt;500 TPS.
   * Vous avez besoin d’une personnalisation basée sur les profils Adobe.
   * Vous souhaitez que les données de campagne soient regroupées en profils pour un ciblage futur.
   * Vous souhaitez utiliser un autre canal que E-mail.

* Choisissez les campagnes **débit élevé** si :
   * Vous avez besoin d’un débit > 500 TPS.
   * Vous n’avez pas besoin d’assembler les profils.
   * Vous pouvez transmettre toute la personnalisation dans la payload de l’API.
   * Vous souhaitez utiliser le canal E-mail .

## Instructions de configuration

Pour configurer correctement des campagnes à haut débit, suivez ces instructions :

1. Créez un groupe d’adresses IP. [Découvrez comment créer des groupes d’adresses IP](../configuration/ip-pools.md)
1. Créez une configuration de canal. [Découvrir comment configurer les canaux](../configuration/channel-surfaces.md)
1. Contactez l’assistance clientèle d’Adobe pour demander que la surface activée soit mappée à la fonctionnalité de débit élevé. Fournissez la configuration du canal et les détails du pool d’adresses IP avec votre identifiant d’organisation.

>[!IMPORTANT]
>
>Les configurations du groupe d’adresses IP et du canal désignées pour les messages transactionnels à débit élevé doivent être utilisées exclusivement à cette fin et ne doivent pas être utilisées avec des messages transactionnels standard à l’aide de campagnes ou de parcours déclenchés par l’API.
