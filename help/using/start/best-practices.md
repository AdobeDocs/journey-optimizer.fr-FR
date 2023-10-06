---
solution: Journey Optimizer
product: journey optimizer
title: Bonnes pratiques relatives à Journey Optimizer
description: En savoir plus sur les bonnes pratiques Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 271fb85d-5621-4a12-b3d1-65cf6021b174
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 5%

---

# Bonnes pratiques {#best-practices}

## Conseils sur la personnalisation des cas d’utilisation en temps réel et des omnicanaux {#real-time-guidance}

Suite à la mise à jour d’Identity Service 2.0, le regroupement d’identités en temps réel a évolué.

Adobe Journey Optimizer exploite le service Identity pour fusionner des profils et personnaliser les expériences de l’utilisateur. Par conséquent, le service doit tenir compte de certains aspects importants lors de la création de vos cas d’utilisation. En tant que marque, vous cherchez à offrir une expérience à une personne. Le graphique d’identités permet aux marketeurs de comprendre les périphériques auxquels une personne est associée sur différents canaux. Le graphique peut contenir des identités qui représentent une personne (CRMID) ou un navigateur web (ECID). Identity Service rassemble ces informations, ce qui permet la création d’une &quot;vue à 360 degrés&quot; d’une personne, ou d’un profil fusionné. En d’autres termes, lorsqu’une personne navigue sur votre site, puis se connecte, toutes les données antérieures de cette session peuvent être associées à l’utilisateur de connexion. Cette action se produit en plusieurs étapes :

1. Combinaison initiale des identités : lorsqu’une personne se connecte, l’identifiant de connexion (CRMID) est associé à l’identifiant du navigateur web (session web ou application mobile) :

   * Cela peut prendre entre 30 min et 4 heures.
   * En règle générale, cet événement de connexion génère un graphique d’identités qui lie CRMID à ECID.

1. Après l’assemblage initial, toutes les données envoyées avec l’une des deux identités seront associées au profil fusionné et disponibles pour personnalisation dans Journey Optimizer en temps réel. La mise à jour du profil avec les dernières données comportementales peut prendre jusqu’à 1 minute. Voir cette [page](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=fr).

Lors de la création de cas d’utilisation, tenez compte des points suivants :

1. La marque souhaite réengager un visiteur du site 30 minutes après l’abandon (par exemple, abandon de panier) :

   Utilisez l’identité avec les données - ECID. Si vous souhaitez capturer 100 % des visiteurs qui ont installé leur adresse électronique/application au cours des 30 dernières minutes, vous devez utiliser l’identité basée sur les cookies pour lancer ce parcours (ECID). Cela suppose que votre adresse électronique, votre jeton push ou toute autre adresse de l’expérience soient associés à l’ECID.

1. Engagement omnicanal sur le web, le courrier électronique, les notifications push, etc.:

   * Les adresses de communication doivent être disponibles sur le profil au moment de l’engagement. Pour que cela se produise de manière cohérente et opportune, assurez-vous que vos données sont associées à l’identité que vous souhaitez utiliser.
   * Si vous devez utiliser des informations provenant d’une nouvelle application ou session de navigateur installée, combinées à des informations connues ou connectées, cette communication doit être envoyée après l’assemblage de ces identités. Cela peut varier par client et nous vous invitons à attendre au moins 30 minutes pour obtenir le volume de profils le plus élevé.

## Échelle avec des barrières de sécurité de Parcours {#scale}

Cette section vous guide sur la mise à l’échelle avec les deux limites suivantes :

* Journey Optimizer dispose d’une barrière de sécurité de 50 activités dans une zone de travail de parcours. Cette barrière de sécurité est conçue pour faciliter la lisibilité, l’assurance qualité et la résolution des problèmes. Le nombre d’activités d’un parcours apparaît dans la section supérieure gauche du canevas de parcours lorsque vous vous trouvez dans les 10 activités de cette limite.

* Lorsque vous publiez des parcours, Journey Optimizer se met automatiquement à l’échelle et s’ajuste pour garantir un débit et une stabilité maximaux. Lorsque vous approchez du jalon de 100 parcours actifs à la fois dans un environnement de test, un recouvrement orange et un signe d’avertissement s’affichent dans l’interface pour cette réalisation. Si cette notification s’affiche et que vous devez étendre vos parcours au-delà de 100 parcours actifs à la fois, créez un ticket pour l’assistance clientèle et nous vous aiderons à atteindre vos objectifs.

Il existe un certain nombre de bonnes pratiques que vous pouvez adopter, qui vous aideront à rester dans les barrières de sécurité et à utiliser le système efficacement.

* Si vous approchez de votre limite de parcours en direct, la première étape que vous pouvez effectuer est d’accéder à la variable **Présentation** sous **Parcours** pour voir le nombre de parcours actifs au cours des dernières 24 heures (parcours disposant de profils actifs). Vous pouvez vérifier le nombre de profils entrant et sortant du parcours dans cette section pour le déterminer.

  ![](assets/journey-guardrails2.png)

* Ensuite, dans la section Inventaire des Parcours, vous pouvez filtrer tous les parcours par État = &quot;En direct&quot; et Type = &quot;Lecture d’audience&quot;. Triez ensuite par date de publication (du plus ancien au plus récent). Cliquez dans le parcours et accédez au planning. Arrêter tous les parcours actifs dont l’exécution était planifiée **Une fois** ou **Dès que possible** qui ont plus d’une journée et n’ont qu’une seule action.

  ![](assets/journey-guardrails1.png)

* Si votre **Lecture d’audience** parcours ne comporte qu’une seule action, aucune attente/décision, ou optimisation de l’heure d’envoi, envisagez de les déplacer vers les campagnes Journey Optimizer. Les campagnes sont mieux adaptées à l’engagement à une seule étape. L’une des principales différences entre Campaign et Parcours est de savoir s’il est important d’écouter activement l’engagement des utilisateurs afin de déterminer l’étape suivante et de lancer une autre action.
* Pour réduire le nombre d’activités au sein d’un parcours, vérifiez les étapes de la condition. Il y aura de nombreux cas où vous pourrez déplacer les conditions dans la définition de segment ou la composition de l’audience.
* Si les mêmes conditions sont répétées sur plusieurs parcours (contrôles du consentement, suppressions), envisagez de les déplacer dans le cadre de la définition de segment. Par exemple, si vous avez une condition pour vérifier que &quot;l’adresse électronique n’est pas vide&quot; sur plusieurs parcours, cette condition est incluse dans la définition de segment.
* Si votre parcours comporte plusieurs conditions pour diviser l’audience afin d’afficher les nombres à chaque étape, pensez à utiliser Customer Journey Analytics ou d’autres solutions de création de rapports mieux adaptées à l’analyse.
* Si vous approchez de la limite des noeuds sur la zone de travail, envisagez de consolider les actions avec des paramètres ou du contenu dynamiques pour servir le contenu approprié plutôt que des noeuds explicites.
