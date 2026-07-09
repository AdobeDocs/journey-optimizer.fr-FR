---
title: Prise en main de la messagerie in-app
description: Découvrez comment envoyer des notifications in-app avec Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: in-app, message, création, commencer
exl-id: 51562843-7b50-4eb5-bf79-5ce03f7549cb
TQID: https://experienceleague.adobe.com/b139LQsPe3HwKe1O5cyBx4Nj4jpW3GXCFIVIWTAIlbg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: cc5c44e2-54a1-4927-b794-442cd87d8f74id: c96d2aa5-76a2-443d-8d23-5de95577c909id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 601
ht-degree: 44%

---

# Prise en main du canal in-app {#gs-in-app}

>[!BEGINSHADEBOX]

**Sur cette page :** commencer à utiliser le canal de messagerie in-app d’Adobe Journey Optimizer pour envoyer aux utilisateurs et aux utilisatrices de l’application des notifications sur les fonctionnalités, les offres et l’intégration.

>[!ENDSHADEBOX]

Les messages in-app sont des notifications qui peuvent être envoyées aux utilisateurs et utilisatrices dans votre application, les guidant vers des points ciblés spécifiques. Ces notifications peuvent être utilisées à différentes fins, par exemple pour promouvoir de nouvelles fonctionnalités, présenter des offres spéciales ou faciliter l’intégration des utilisateurs et utilisatrices. En utilisant les messages in-app, vous pouvez interagir efficacement avec votre audience et l’orienter vers des aspects importants de votre application.

Utilisez Journey Optimizer pour créer des notifications in-app et configurer des options d’expérience, notamment la disposition et l’affichage du message, le texte et les options de bouton.

</br>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="inapp-configuration.md">
<img alt="Validation" src="../assets/do-not-localize/inapp-config.jpg">
</a>
<div>
<a href="inapp-configuration.md"><strong>Configurer le canal in-app</strong></a>
</div>
<p>
</td>
<td>
<a href="create-in-app.md">
<img alt="Lead" src="../assets/do-not-localize/inapp-create.jpeg">
</a>
<div><a href="create-in-app.md"><strong>Créer un message in-app</strong>
</div>
<p>
</td>
<td>
<a href="design-in-app.md">
<img alt="Peu fréquent" src="../assets/do-not-localize/inapp-design.jpg">
</a>
<div>
<a href="design-in-app.md"><strong>Concevoir votre contenu in-app</strong></a>
</div>
<p></td>
<td>
<a href="../reports/campaign-global-report-cja-inapp.md">
<img alt="Validation" src="../assets/do-not-localize/inapp-report.jpg">
</a>
<div>
<a href="../reports/campaign-global-report-cja-inapp.md"><strong>Accéder aux rapports in-app</strong></a>
</div>
<p>
</td>
</tr></table>

## Cas d’utilisation

Les messages in-app fonctionnent mieux lorsque vous souhaitez guider ou influencer les utilisateurs lorsqu’ils sont déjà engagés avec votre application, en profitant de ce moment d’attention active.

| Avantage | Pourquoi | Exemples de cas d’utilisation |
| --- | --- | --- |
| Interaction client importante | Atteint les utilisateurs lorsqu’ils sont actifs dans une session d’application | Annonces de fonctionnalités, conseils d’intégration |
| Déclencheurs pertinents du point de vue contextuel | Peut être déclenché en fonction du comportement ou de l’emplacement in-app | Mettre en surbrillance une fonctionnalité juste après qu’un utilisateur visite un écran associé |
| Diffusion en temps réel | Aucune dépendance aux jetons push ou aux services de diffusion externes | Invites sensibles à l’heure affichées pendant la session en cours |
| Aucune dépendance aux canaux externes | Fonctionne entièrement dans l’application, indépendamment du statut d’opt-in pour les autres canaux | Atteindre les utilisateurs qui se sont désinscrits des notifications push |
| Meilleur potentiel de conversion | Livré à un moment d&#39;attention active, augmentant les taux de réponse | Offres de montée en gamme ou de vente croisée, invites d&#39;enquête |
| Personnalisation et segmentation | La disposition, le texte et les boutons peuvent être adaptés à des audiences spécifiques | Flux d’intégration personnalisés pour différents segments d’utilisateurs |
| Conception non intrusive | conçus de manière à compléter l’expérience utilisateur plutôt qu’à l’interrompre. | Bannières ou modèles alignés sur l’interface utilisateur de l’application |

## Quand ne pas utiliser

Les messages in-app dépendent d’une session active, ils ne sont donc pas adaptés à chaque scénario. Prenons un autre canal dans les situations suivantes :

* L’utilisateur n’utilise pas activement l’application, car le message ne s’affichera jamais
* Le message est un problème critique ou urgent qui nécessite d’atteindre les utilisateurs en dehors de l’application, par exemple une panne ou une alerte de sécurité
* La communication est réglementaire ou légale et nécessite une confirmation de lecture que les messages in-app ne peuvent pas fournir
* L’objectif est la réactivation du compte ou une campagne de reconquête pour les utilisateurs inactifs qui ne vont probablement pas ouvrir l’application
* Le message correspond à une mise à jour transactionnelle à volume élevé, telle qu’une confirmation de commande, mieux adaptée aux e-mails ou aux SMS
* L’utilisation excessive peut entraîner la cécité des bannières, où les utilisateurs et utilisatrices commencent à ignorer les messages qui apparaissent trop souvent
* Les utilisateurs peuvent être hors ligne ou sans connectivité de l’application lorsque le message est destiné à être diffusé



## Ressources supplémentaires

* **[Créer des messages in-app](create-in-app.md)** : découvrez comment créer et configurer des messages in-app pour les applications mobiles.
* **[Configurer le canal in-app](inapp-configuration.md)** : configurez votre canal de messagerie in-app avec les configurations d’application mobile appropriées.
* **[Concevoir du contenu in-app](design-in-app.md)** : personnalisez les dispositions, les styles, les boutons et les éléments interactifs des messages in-app.
* **[In-app pour le web](create-in-app-web.md)** : découvrez comment créer et diffuser des messages in-app pour les applications web.
* **[Tutoriels sur le canal in-app](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/channels/in-app-channel/in-app-messages-overview){target="_blank"}** : découvrez des tutoriels vidéo détaillés sur les fonctionnalités de messagerie in-app et les bonnes pratiques.

