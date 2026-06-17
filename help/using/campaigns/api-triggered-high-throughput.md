---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 61%

---
Le fichier n’existe pas dans le référentiel de pipeline ; il s’agit d’un fichier de documentation fourni comme contexte. Je vais écrire le markdown complet mis à jour directement comme indiqué (sortie uniquement du fichier, aucune explication).

---

solution : Journey Optimizer
produit : parcours optimizer
titre : activation du mode débit élevé pour les campagnes déclenchées par API
Description : découvrez comment activer le mode Débit élevé pour les campagnes déclenchées par l’API.
fonctionnalité : campagnes, API
rubrique : Gestion de contenu
Rôle : développeur
niveau : Expérimenté
mots-clés : campagnes, déclenchées par API, REST, optimizer, messages
exl-id : 2b3e87dc-097a-4d05-873c-f421d11338c3
TQID : https://experienceleague.adobe.com/SwmK1epuhZUf4EWnaLRHTBH-eE1hEV02Z8nqXGtMb6U
product_v2 :
- id : cb954087-f4fc-4456-afb9-e939cabcdc79
internal-label : Journey Optimizer
feature_v2 :
- id : d556b755-390a-43f0-be32-a08cf6236126
internal-label : Configuration
- id : a653cc2e-bc85-4353-a306-399e5b247978
libellé interne : campagnes Journey Optimizer
subfeature_v2 :
- id : f7479fa1-474b-479d-8c98-f6cee5865a38
internal-label : campagnes déclenchées par API
- id : ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
internal-label : Gestion de campagne
role_v2 :
- id : ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label : développeur
topic_v2 :
- id : e0eb8757-182f-49f3-94a4-1587d16f5094
internal-label : Personalization
---
# Activer le mode de débit élevé pour les campagnes déclenchées par API {#high-throughput}

>[!BEGINSHADEBOX]

**Sur cette page :** Activez le mode à débit élevé pour les campagnes déclenchées par l’API afin de pouvoir envoyer des messages transactionnels en temps réel à très grande échelle jusqu’à 5 000 transactions par seconde (e-mail) ou jusqu’à 1 500 transactions par seconde (push) sans dépendre des profils.

>[!ENDSHADEBOX]

Le mode haut débit est conçu pour les organisations qui ont besoin de **messages transactionnels en temps réel à très grande échelle**. Contrairement aux campagnes standard déclenchées par API, les campagnes à débit élevé fonctionnent indépendamment des profils Adobe et nécessitent un modèle de configuration différent.

Cette page explique en quoi les campagnes à débit élevé diffèrent des campagnes standard déclenchées par API, les exigences de configuration et quand choisir chaque mode.

## Mécanismes de sécurisation et limitations

* **Accès** : disponible uniquement aux États-Unis pour les organisations disposant d’une licence avec le module complémentaire High Throughput transactional messaging.

* **Canaux** : disponible pour les e-mails et les notifications push.

* **Débit** :

   * **E-mail** - Jusqu’à 5 000 transactions par seconde.
   * **Push** - Jusqu&#39;à 1 500 transactions par seconde. Les niveaux de débit hiérarchique suivants sont disponibles : 500 TPS (de base), 1 000 TPS et 1 500 TPS. Les niveaux supérieurs nécessitent les droits de module complémentaire appropriés.

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
| **Débit** | Jusqu’à 500 transactions par seconde | Jusqu&#39;à 5 000 TPS (e-mail) ; jusqu&#39;à 1 500 TPS (push) |
| **Canaux** | E-mail, SMS, Push | E-mail, notification push |
| **Personnalisation** | Profil + contextuel dans la payload de l’API | Contextuel dans la payload de l’API uniquement |
| **Profil et rattachement** | Existe ou est créé avec des événements rattaché à un profil. | Aucun profil |
| **Volume des messages** | Droits standard et packs de messages | Volumes de messages hiérarchisés distincts |
| **Infrastructure** | Standard | Amélioré |
| **Temps de disponibilité** | 99,9 % | 99,99 % |
| **API Health check** | Oui | Oui |

En d’autres termes :

* Choisissez les campagnes **standard déclenchées par API** si :
   * Vous n’avez pas de contrat avec débit élevé.
   * Vos besoins de débit sont de ≤500 TPS.
   * Vous avez besoin d’une personnalisation basée sur les profils Adobe.
   * Vous souhaitez que les données de campagne soient rattachées aux profils pour un ciblage futur.
   * Vous avez besoin de SMS.

* Choisissez les campagnes à **débit élevé** si :
   * Vous avez besoin d’un débit > 500 TPS.
   * Vous n’avez pas besoin de rattacher les données aux profils.
   * Vous pouvez transmettre toute la personnalisation dans la payload de l’API.
   * Vous souhaitez utiliser le canal E-mail ou Push.

## Instructions relatives à la configuration

Pour configurer correctement des campagnes à débit élevé, suivez ces instructions :

1. **Pour les e-mails à débit élevé uniquement** - Créez un groupe d’adresses IP. [Découvrir comment créer des groupes d’adresses IP](../configuration/ip-pools.md)
1. Créez une configuration de canal. [Découvrir comment configurer les canaux](../configuration/channel-surfaces.md)
1. Contactez l’assistance clientèle d’Adobe pour demander que la surface activée soit mappée à la fonctionnalité de débit élevé. Fournissez la configuration du canal et les détails du pool d’adresses IP (pour les e-mails) ainsi que l’identifiant de votre organisation.

>[!IMPORTANT]
>
>Les configurations de canal désignées pour les messages transactionnels à débit élevé doivent être utilisées exclusivement à cette fin et ne doivent pas être utilisées avec des messages transactionnels standard à l’aide de campagnes ou de parcours déclenchés par l’API. Pour un débit élevé des e-mails, le groupe d’adresses IP désigné à cet effet doit également être utilisé exclusivement pour l’envoi à débit élevé.