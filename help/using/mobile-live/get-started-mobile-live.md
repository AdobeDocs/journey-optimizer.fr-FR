---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des activités en direct
description: Découvrez comment créer des activités en direct dans Journey Optimizer.
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
TQID: https://experienceleague.adobe.com/IB00r0QSfCthvgvyqubGwsaUoiJKBL-E96duLn4R5i0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: ed2fba79-65cb-4680-96d2-2ad5d851714d
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 421
ht-degree: 100%

---

# Prise en main des activités en direct {#get-started-mobile-live}


Les activités en direct sont des éléments d’interface d’utilisation persistants et modifiables qui s’affichent sur l’écran de verrouillage de l’appareil. Elles permettent à votre application d’afficher des informations actualisées en temps réel pour les utilisateurs et utilisatrices tout au long d’un événement. Ils restent donc informés sans avoir à ouvrir l’application et sans recevoir des notifications push intempestives.

>[!AVAILABILITY]
>
>Les activités en direct dans Journey Optimizer sont uniquement compatibles avec Apple iOS.

Contrairement aux notifications push traditionnelles, les activités en direct représentent l’**engagement basé sur l’état** : au lieu d’envoyer des alertes ponctuelles, elles maintiennent une présence contextuelle et continue, qui se met à jour dynamiquement à mesure que les événements évoluent.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="Activités en direct iOS sur l’écran verrouillé et la Dynamic Island" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>Avantages clés</strong></p>
<p>Avec les activités en direct, l’engagement mobile basé sur les notifications devient basé sur l’état, ce qui permet aux marques d’effectuer les opérations suivantes :</p>
<ul>
<li>Maintenir une <strong>présence continue</strong> sur l’écran verrouillé tout au long des événements à forte valeur ajoutée</li>
<li><strong>Mettre à jour les informations de manière dynamique</strong> sans surcharger les utilisateurs et utilisatrices avec des notifications intempestives</li>
<li>Proposer des expériences mobiles <strong>plus riches et plus contextuelles</strong> liées à des événements réels</li>
<li><strong>Augmenter l’engagement et la rétention</strong> lors des transactions actives ou des expériences en direct</li>
</ul>
</td>
</tr>
</table>

Avec Adobe Journey Optimizer, vous pouvez **démarrer**, **mettre à jour** et **terminer** des activités en direct à distance par programmation via des campagnes déclenchées par API, en prenant en charge aussi bien des cas d’utilisation particuliers que basés sur une audience à grande échelle.

Les activités en direct peuvent **uniquement** être lancées par le biais de campagnes **déclenchées par API**, ce qui vous permet de fournir des payloads personnalisées et d’effectuer toute la personnalisation par le biais de votre propre payload.
Sélectionnez le type de campagne **Déclenchée par API** en fonction du cas d’utilisation prévu de l’activité en direct :

* Sélectionnez **Déclenchée par API (marketing)** pour les cas d’utilisation de diffusion, avec des mises à jour basées sur l’audience envoyées à grande échelle :

   * Scores sportifs et comptes à rebours d’événements en direct
   * Mises à jour du statut du vol pour tous les passagers d’un même trajet
   * Expériences partagées sur un segment d’utilisateurs

* Sélectionnez **Déclenchée par API (transactionnelle)** pour les cas d’utilisation particuliers - 1:1 mises à jour en temps réel par utilisateur :

   * Suivi des commandes et progression de la diffusion
   * Mises à jour du statut de la course ou du service
   * Confirmations de réservation et de rendez-vous en temps réel

## Guide de démarrage rapide

Suivez les étapes ci-dessous pour configurer et implémenter des activités en direct dans votre application :

1. **[Configurer Adobe Journey Optimizer](mobile-live-configuration.md)**

   Configurez votre environnement en créant une configuration mobile.

1. **[Intégrer le SDK mobile d’Adobe Experience Platform](mobile-live-configuration-sdk.md)**

   Intégrez le SDK mobile Adobe Experience Platform pour activer les mises à jour dynamiques en temps réel sur l’écran de verrouillage et Dynamic Island.

1. **[Créer une activité en direct dans Journey Optimizer](create-mobile-live.md)**

   Utilisez des campagnes déclenchées par API dans Journey Optimizer pour démarrer votre activité en direct.

1. **[Surveiller vos campagnes](../reports/campaign-global-report-cja-activity.md)**

   Commencez à mesurer l’impact de votre activité en direct à l’aide de rapports intégrés.

## Vidéo pratique

Découvrez comment configurer les activités en direct iOS avec Adobe Journey Optimizer pour afficher des mises à jour détaillées et en temps réel sur l’écran verrouillé et la Dynamic Island d’un iPhone.

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
