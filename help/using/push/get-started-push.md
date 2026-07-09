---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des notifications push
description: Découvrez comment créer une notification push dans Journey Optimizer.
feature: Overview, Push
topic: Content Management
role: User
level: Beginner
exl-id: c1f16edd-efdf-41c2-a0ad-5f55009008f5
TQID: https://experienceleague.adobe.com/S-3ZtTNfgZGEFChfjaXPihxGWpdkWacrWF9AWc-AyZY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c96d2aa5-76a2-443d-8d23-5de95577c909id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 651
ht-degree: 57%

---

# Prise en main des notifications push {#gs-push-notification}

>[!BEGINSHADEBOX]

**Sur cette page :** commencez à utiliser les notifications push dans Adobe Journey Optimizer pour atteindre les utilisateurs et les utilisatrices de votre application mobile et vos visiteurs et visiteuses web par le biais de parcours et de campagnes.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Si c’est la première fois que vous créez une notification push, vérifiez que le canal push a été configuré. [En savoir plus](push-gs.md).

Les notifications push vous permettent d’atteindre les utilisateurs et utilisatrices de votre application mobile et les visiteurs et visiteuses de votre site web à tout moment, en particulier lorsque les personnes n’utilisent pas activement votre application ou ne naviguent pas sur votre site web. Elles sont utiles dans plusieurs cas d’utilisation, par exemple pour envoyer des mises à jour sur votre service, inciter un utilisateur ou une utilisatrice à agir, l’avertir d’une nouvelle offre, etc. Les plateformes d’appareil exigent un opt-in pour que les utilisateurs finaux puissent recevoir ou afficher vos notifications. Lʼaccord préalable de lʼutilisateur peut être reçu dès le lancement de lʼapplication pour la première fois après lʼinstallation, ou au cours dʼune session ou dʼun processus ultérieur, selon le cas.

[!DNL Journey Optimizer] prend en charge les notifications push et vous permet d&#39;envoyer des notifications extrêmement pertinentes à des taux de débit de pointe. Les notifications push peuvent inclure une personnalisation et un contexte basé sur les Parcours afin d&#39;exploiter les données de votre marque avec [!DNL Adobe CX Enterprise].

Les notifications push peuvent être créées :

* Dans un **parcours** : une fois que vous avez ajouté une activité push à votre parcours et défini des paramètres de base, utilisez le volet de droite **[!UICONTROL Actions : notification push]** pour créer le contenu des notifications push. [Découvrir comment créer un parcours](../building-journeys/journey-gs.md)

* Dans une **campagne** : une fois une campagne créée, sélectionnez Notification push comme action et définissez les paramètres de base. Découvrez comment créer une [campagne d’action](../campaigns/campaign-action.md#action-campaign-action), une [campagne déclenchée par API](../campaigns/api-triggered-campaigns.md) ou une [campagne orchestrée](../orchestrated/create-orchestrated-campaign.md#create).

Utilisez les onglets dédiés pour définir les paramètres de notification push pour les plateformes **iOS**, **Android** et **Web**.

>[!NOTE]
>
>Alors que **[!DNL Journey Optimizer]** offre des moyens permettant de gérer les désinscriptions des e-mails et des SMS, les notifications push ne nécessitent aucune action de votre part, car les destinataires peuvent annuler leur abonnement depuis leurs appareils. Par exemple, lors du téléchargement ou de l’utilisation de votre application, les destinataires peuvent choisir d’arrêter les notifications. De même, ces personnes peuvent modifier les paramètres de notification par le biais du système d’exploitation mobile ou des paramètres du navigateur web. Pour vérifier le statut de consentement push d’un profil dans la visionneuse de profils AEP, consultez [Vérification du statut d’opt-out push](../privacy/opt-out.md#push-opt-out-status).

</br>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-push.md">
<img alt="Lead" src="../assets/do-not-localize/push-create.jpg">
</a>
<div><a href="create-push.md"><strong>Créer une notification push</strong>
</div>
<p>
</td>
<td>
<a href="design-push.md">
<img alt="Peu fréquent" src="../assets/do-not-localize/push-design.jpg">
</a>
<div>
<a href="design-push.md"><strong>Créer votre notification push</strong></a>
</div>
<p></td>
<td>
<a href="send-push.md">
<img alt="Validation" src="../assets/do-not-localize/push-sending.jpg">
</a>
<div>
<a href="send-push.md"><strong>Envoyer votre notification push</strong></a>
</div>
<p>
</td>
<td>
<a href="push-gs.md">
<img alt="Validation" src="../assets/do-not-localize/push-config.jpg">
</a>
<div>
<a href="push-gs.md"><strong>Configurer les notifications push</strong></a>
</div>
<p>
</td>
</tr></table>

## Cas d’utilisation

Les notifications push fonctionnent mieux lorsque vous devez atteindre les utilisateurs rapidement et directement sur leur appareil, sans qu’ils soient obligés d’être dans votre application ou de vérifier leur boîte de réception.

| Avantage | Pourquoi | Exemples de cas d’utilisation |
| --- | --- | --- |
| Mises à jour sensibles à l’heure | Diffusé instantanément, même lorsque les utilisateurs n’utilisent pas activement votre application | Alertes de retard de vol, changements d&#39;état des commandes, dernières nouvelles |
| Réengagement | Invite les utilisateurs à revenir à votre application après une période d&#39;inactivité | Rappels d’abandon de panier, campagnes de reconquête |
| Réduction des coûts par rapport aux SMS | Pas de frais par opérateur de messagerie, contrairement aux SMS | Notifications promotionnelles ou transactionnelles à volume élevé |
| Contenu riche et interactif | Prend en charge les images, les boutons d’action et les liens profonds | Promotions de produits avec boutons de commande, aperçus de médias riches |
| Fonctionnalités natives de l’appareil | Exploite les fonctionnalités au niveau du système d’exploitation qui ne sont pas disponibles pour d’autres canaux. | Alertes de vibrations, badges d’icône d’application, déclencheurs d’emplacement géoréférencés |
| Probabilité d’opt-in élevée | Les utilisateurs sont invités à activer l’application dès son installation ou son premier lancement | Flux d’intégration, campagnes d’engagement du premier jour |

## Quand ne pas utiliser

Les notifications push ne conviennent pas à tous les messages. Prenons un autre canal dans les situations suivantes :

* Votre audience a un faible taux d’opt-in aux notifications push ou a montré une résistance aux notifications, car le message peut ne jamais leur atteindre
* Le message nécessite du contenu de forme longue, ce qui améliore le traitement des e-mails et permet une mise en forme plus détaillée
* Le contenu est sensible ou privé et ne doit pas être visible sur un écran de verrouillage, où toute personne proche de l’appareil pourrait le voir
* La plupart de vos utilisateurs accèdent à votre service à partir d’un bureau plutôt que d’une application mobile, où la portée des notifications push est limitée ou inexistante

