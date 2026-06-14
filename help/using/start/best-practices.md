---
solution: Journey Optimizer
product: journey optimizer
title: Bonnes pratiques relatives à Journey Optimizer
description: En savoir plus sur les bonnes pratiques de Journey Optimizer
feature: Get Started
role: User
level: Intermediate
hide: true
exl-id: 271fb85d-5621-4a12-b3d1-65cf6021b174
TQID: https://experienceleague.adobe.com/Se4lHbRPMhMXUr8yWmtAYi3BSaacSBZzmUNeig1QpUI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: c4147b6e-073b-4d3c-9ab1-d60f2f4434efid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
source-git-commit: 46a5a6dc0a3486633a1a71f8bba8a3cd53aaa618
workflow-type: tm+mt
source-wordcount: 1026
ht-degree: 96%

---

# Bonnes pratiques {#best-practices}

>[!BEGINSHADEBOX]

**Sur cette page :** appliquez les bonnes pratiques de Journey Optimizer en matière de combinaison d’identités, de personnalisation omnicanal et de mécanismes de sécurisation de parcours, afin de pouvoir créer des cas d’utilisation fiables et les mettre à l’échelle efficacement dans les limites du système.

>[!ENDSHADEBOX]

## Conseils pour la personnalisation des cas d’utilisation en temps réel et des omnicanaux {#real-time-guidance}

Suite à la mise à jour du Service d’identités 2.0, la connexité d’identités en temps réel a évolué.

Adobe Journey Optimizer exploite le Service d’identités pour fusionner des profils et personnaliser les expériences de l’utilisateur ou de l’utilisatrice. Par conséquent, le service doit tenir compte de certains aspects importants lors de la création de vos cas d’utilisation. En tant que marque, vous cherchez à offrir une expérience personnalisée. Le graphique d’identité permet aux spécialistes du marketing de comprendre les appareils auxquels une personne est associée sur différents canaux. Le graphique peut contenir des identités qui représentent une personne (CRMID) ou un navigateur web (ECID). Le Service d’identités rassemble ces informations, ce qui permet la création d’une « vision à 360 degrés » de la personne ou du profil fusionné. En d’autres termes, lorsqu’une personne navigue sur votre site, puis se connecte, toutes les données antérieures de cette session peuvent être associées à l’utilisateur ou l’utilisatrice de la connexion. Cette action se produit en plusieurs étapes :

1. Connexité initiale des identités : lorsqu’une personne se connecte, l’identifiant de connexion (CRMID) est associé à l’identifiant du navigateur web (session web ou application mobile).

   * Cela peut prendre entre 30 minutes et 4 heures.
   * En règle générale, cet événement de connexion génère un graphique d’identité qui lie les CRMID aux ECID.

1. Après la connexité initiale, toutes les données envoyées avec l’une des deux identités seront associées au profil fusionné et disponibles pour personnalisation dans Journey Optimizer en temps réel. La mise à jour du profil avec les dernières données comportementales peut prendre jusqu’à 1 minute. Voir cette [page](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=fr).

Lors de la création de cas d’utilisation, tenez compte des points suivants :

1. La marque souhaite réengager un visiteur ou une visiteuse du site 30 minutes après l’abandon (par exemple, e-mail d’abandon de panier) :

   Utilisez l’identité avec les données : ECID. Si vous souhaitez capturer 100 % des visiteurs et visiteuses ayant fourni leur adresse e-mail ou installation d’application au cours des 30 dernières minutes, vous devez utiliser l’identité basée sur les cookies pour lancer ce parcours (ECID). Cela suppose que votre adresse e-mail, votre jeton push ou toute autre adresse de l’expérience soient associés à l’ECID.

1. Engagement omnicanal sur le web, les e-mails, les notifications push, etc. :

   * Les adresses de communication doivent être disponibles sur le profil au moment de l’engagement. Pour que cela se produise de manière cohérente et opportune, assurez-vous que vos données sont associées à l’identité que vous souhaitez utiliser.
   * Si vous devez utiliser des informations provenant d’une nouvelle application ou session de navigateur installée, combinées à des informations connues ou connectées, cette communication doit être envoyée après la connexité de ces identités. Cela peut varier d’un client ou d’une cliente à l’autre, nous vous invitons donc à attendre au moins 30 minutes pour obtenir le volume de profils le plus élevé.

## Mettre à l’échelle avec les mécanismes de sécurisation des parcours {#scale}

Cette section vous guide sur la mise à l’échelle avec les deux limites suivantes :

* Journey Optimizer dispose d’un mécanisme de sécurisation de 50 activités dans la zone de travail du parcours. Ce mécanisme de sécurisation permet de faciliter la lisibilité, l’assurance qualité et la résolution des problèmes. Le nombre d’activités d’un parcours apparaît dans la section supérieure gauche de sa zone de travail lorsque vous approchez de la limite (10 activités).

* Lorsque vous publiez des parcours, Journey Optimizer les met automatiquement à l’échelle et les ajuste pour garantir une stabilité et un débit maximaux. Lorsque vous approchez du jalon de 100 parcours actifs à la fois dans une sandbox, un recouvrement orange et un signe d’avertissement s’affichent dans l’interface pour cette réalisation. Si cette notification s’affiche et que vous devez étendre vos parcours au-delà de 100 parcours actifs à la fois, créez un ticket pour l’assistance clientèle et nous vous aiderons à atteindre vos objectifs.

<!--
DOCAC-10977

* As you publish journeys, Journey Optimizer automatically scales and adjusts to ensure maximum throughput and stability. As you near the milestone of 500 live journeys at one time in a sandbox, you will see an orange overlay and warning sign appear in the interface on this achievement. If you see this notification and have a need to extend your journeys beyond 500 live journeys at a time, please create a ticket for customer care and we will help you reach your goals.
-->


Il existe un certain nombre de bonnes pratiques que vous pouvez adopter, qui vous aideront à respecter les mécanismes de sécurisation et à utiliser le système efficacement.

* Si vous approchez de votre limite de parcours actifs, la première chose que vous pouvez faire est d’accéder à l’onglet **Vue d’ensemble** dans **Parcours** pour voir le nombre de parcours actifs au cours des dernières 24 heures qui comprennent des profils actifs. Vous pouvez vérifier le nombre de profils entrant et sortant du parcours dans cette section.

  ![](assets/journey-guardrails2.png)

* Ensuite, dans la section Inventaire des parcours, vous pouvez filtrer tous les parcours par Statut = « Actif » et Type = « Lecture d’audience ». Triez ensuite par date de publication (du plus ancien au plus récent). Cliquez sur le parcours et accédez au planning. Arrêtez tous les parcours actifs dont l’exécution était planifiée **Une fois** ou **Dès que possible** qui ont plus d’une journée et n’ont qu’une seule action.

  ![](assets/journey-guardrails1.png)

* Si votre parcours **Lecture d’audience** ne comporte qu’une seule action, aucune attente/décision ou optimisation de l’heure d’envoi, envisagez de le déplacer vers les campagnes Journey Optimizer. Les campagnes sont mieux adaptées à un engagement à une seule étape. L’une des principales différences entre une campagne et un parcours est de savoir s’il est important d’écouter activement l’engagement client afin de déterminer l’étape suivante et de lancer une autre action.
* Pour réduire le nombre d’activités au sein d’un parcours, vérifiez les étapes des conditions. Il y aura de nombreux cas où vous pourrez déplacer les conditions dans la définition de segment ou la composition d’audiences.
* Si les mêmes conditions sont répétées sur plusieurs parcours (contrôles du consentement, suppressions), envisagez de les déplacer dans le cadre de la définition de segment. Par exemple, si vous avez une condition pour vérifier que « l’adresse e-mail n’est pas vide » sur plusieurs parcours, cette condition est incluse dans la définition de segment.
* Si votre parcours comporte plusieurs conditions pour diviser l’audience afin d’afficher les nombres à chaque étape, pensez à utiliser Customer Journey Analytics ou d’autres solutions de création de rapports mieux adaptées à l’analyse.
* Si vous approchez de la limite des nœuds sur la zone de travail, envisagez de consolider les actions avec des paramètres ou du contenu dynamiques pour servir le contenu approprié plutôt que des nœuds explicites.

* Si vous avez un parcours **Lecture d’audience** avec le segment par lots (A) et si vous utilisez dans le parcours le segment de streaming inAudience (B) pour exclure (c’est-à-dire exécuter A-B), envisagez de déplacer cette logique vers la logique de segmentation et d’utiliser l’exclusion dans le cadre de la logique de segmentation elle-même.