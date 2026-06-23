---
solution: Journey Optimizer
product: journey optimizer
title: Rapport de parcours
description: Découvrez comment utiliser les données des e-mails du rapport de parcours
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 82558447-9d42-4fac-8fc1-fded9bf4bfcc
TQID: https://experienceleague.adobe.com/nZejBuTk9AqwR77k6-odCK66c2UbGwMspElt2-1riz4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: beb7a3c1-66ab-4786-b879-7621375b3c40
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 287a228854060d5d34dbcfdf4da7bc4add8821bd
workflow-type: tm+mt
source-wordcount: 1228
ht-degree: 82%

---

# Rapport de parcours d’e-mail {#journey-global-report}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment lire les mesures relatives aux e-mails dans le rapport de parcours, y compris les tendances envoi et clic, le statut de diffusion, les statistiques d’envoi et de tracking, les domaines de messagerie, les liens suivis, les objets, ainsi que les raisons de bounce et d’exclusion.

>[!ENDSHADEBOX]

>[!INFO]
>
>Depuis qu’Apple a introduit de nouvelles fonctionnalités de protection de la confidentialité pour son application Mail native, y compris la protection de la confidentialité dans Mail, les expéditeurs ne sont plus en mesure d’utiliser les pixels de tracking pour collecter des données sur les profils qui ont activé la protection de la confidentialité dans Mail d’Apple. Par conséquent, la capacité de Adobe Journey Optimizer à suivre les ouvertures d’e-mail à l’aide de pixels de suivi peut être affectée.
> [En savoir plus](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-classic-blogs/the-impact-of-apple-ios-privacy-changes-on-email-marketing-and/ba-p/699780?profile.language=fr) sur l’impact des modifications apportées à la confidentialité d’Apple iOS sur le marketing par e-mail.
> 
> Nous vous recommandons de vous concentrer sur les clics et les mesures de conversion plutôt que sur les taux d’ouverture pour obtenir des informations plus précises.

>[!BEGINSHADEBOX]

Vous pouvez accéder à votre rapport de parcours par e-mail en cliquant sur le bouton **[!UICONTROL Afficher le rapport]** dans votre parcours. [En savoir plus](report-gs-cja.md)

![](assets/report-access-jo.png)

>[!ENDSHADEBOX]

## Tendance diffusés et clics {#delivered-click}

![](assets/cja-journey-email-delivered.png)

Le graphe **[!UICONTROL Tendances diffusés et clics]** présente une analyse détaillée de l’engagement de vos profils vis-à-vis de vos e-mails, offrant des informations précieuses sur l’intéraction de différents domaines avec votre contenu.

+++ En savoir plus sur les mesures de tendance Diffusés et clics

* **[!UICONTROL Diffusés]** : nombre d’e-mails envoyés avec succès, par rapport au nombre total d’e-mails envoyés.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans vos e-mails.

+++

## Statut de la diffusion {#delivery-status}

![](assets/cja-journey-email-delivery-stat.png)

Le graphe **[!UICONTROL Statut de diffusion]** vous permet de visualiser les performances de vos e-mails en un coup d’œil. Effectuez le suivi des mesures clés telles que les diffusions et les rebonds, afin de comprendre rapidement l’efficacité du parcours de vos e-mails.

+++ En savoir plus sur les mesures de statut de la diffusion

* **[!UICONTROL Diffusés]** : nombre d’e-mails envoyés avec succès, par rapport au nombre total d’e-mails envoyés.

* **[!UICONTROL Rebonds pour les canaux sortants]** : nombre total d’erreurs cumulées lors de la procédure d’envoi et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs sortantes]** : nombre total d’erreurs survenues au cours de la procédure d’envoi, empêchant l’envoi à des profils.

* **[!UICONTROL Exclus]** : nombre de profils qui ont été exclus par Adobe Journey Optimizer.

+++

## Statistiques d’envoi {#email-sending-statistics}

![](assets/cja-journey-email-sending-stat.png)

Le tableau **[!UICONTROL Statistiques d’envoi]** vous aide à comprendre les performances de vos e-mails dans vos parcours. Il suit des mesures clés telles que les taux de diffusion et les interactions, ce qui vous donne des informations précieuses pour optimiser votre stratégie d’envoi d’e-mails afin d’améliorer la portée et l’engagement.

+++ En savoir plus sur les mesures de statistiques d’envoi

* **[!UICONTROL Ciblés]** : nombre de profils qui remplissent les critères de l’audience avant l’application des exclusions, des suppressions ou des suppressions de consentement. Dans les parcours dont la rentrée est activée, un profil peut être ciblé plusieurs fois.

* **[!UICONTROL Envois]** : nombre total d’e-mails envoyés.

* **[!UICONTROL Diffusés]** : nombre d’e-mails envoyés avec succès, par rapport au nombre total de messages envoyés.

* **[!UICONTROL Diffusés uniques]** : nombre de profils ayant reçu au moins un e-mail.

* **[!UICONTROL Rebonds pour les canaux sortants]** : nombre total d’erreurs cumulées lors de la procédure d’envoi et du traitement automatique des retours par rapport au nombre total de messages envoyés.

* **[!UICONTROL Erreurs sortantes]** : nombre total d’erreurs survenues au cours de la procédure d’envoi, empêchant l’envoi à des profils.

* **[!UICONTROL Exclusions sortantes]** : nombre de profils qui ont été exclus par Adobe Journey Optimizer.

+++

## Statistiques de tracking {#email-tracking}

![](assets/cja-journey-email-track-stat.png)

Le tableau **[!UICONTROL E-mail – Statistiques de tracking]** offre un compte rendu détaillé de l’activité de profil associée aux e-mails inclus dans votre parcours. Cela inclut des mesures sur les ouvertures, les clics et d’autres indicateurs d’engagement pertinents, offrant une vue d’ensemble complète de la manière dont les profils interagissent avec le contenu de vos e-mails.

+++ En savoir plus sur la mesure Statistiques de tracking

* **[!UICONTROL Taux de clics (CTR)]** : pourcentage d’utilisateurs et d’utilisatrices ayant interagi avec l’e-mail.

* **[!UICONTROL Taux d’ouverture par clic (CTOR)]** : nombre de fois où l’e-mail a été ouvert.

* **[!UICONTROL Taux d’ouverture]** : pourcentage de profils ayant ouvert l’e-mail au moins une fois, par rapport au nombre d’e-mails diffusés.

* **[!UICONTROL Estimation des ouvertures d’e-mail]** : estimation du nombre total d’ouvertures d’e-mail, prenant en compte les ouvertures directes par les profils et les ouvertures automatisées déclenchées par les serveurs de messagerie. Cette mesure prend en compte les ouvertures déclenchées par les serveurs de messagerie à des fins d’analyse de la confidentialité ou de la sécurité en appliquant un taux d’ouverture calculé à partir des destinataires qui ont ouvert manuellement l’e-mail par rapport à ceux dont les e-mails n’ont été ouverts que par des serveurs de messagerie.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans vos e-mails.

* **[!UICONTROL Estimation des clics]** : nombre de clics sur un contenu de votre message, à l’exclusion du trafic de robots identifiés et des interactions non humaines (NHI).

* **[!UICONTROL Plaintes relatives aux spams]** : nombre de fois où un message a été déclaré comme spam ou courrier indésirable.

* **[!UICONTROL Désabonnements]** : nombre de clics sur le lien de désabonnement ou sur la page de destination associée.

+++

## Domaines d’e-mails {#email-domains}

![](assets/cja-email-email-domains.png)

Le tableau **[!UICONTROL Domaines des e-mails]** offre une répartition très détaillée des e-mails classés par domaine, ce qui permet d’obtenir des informations précises sur les mesures de performance des parcours de vos e-mails. Cette analyse exhaustive vous permet de comprendre le comportement de différents domaines en réponse au contenu de vos e-mails.

+++ En savoir plus sur les mesures des domaines d’e-mails

* **[!UICONTROL Envois]** : nombre total d’e-mails envoyés.

* **[!UICONTROL Diffusés]** : nombre d’e-mails envoyés avec succès, par rapport au nombre total d’e-mails envoyés.

* **[!UICONTROL Ouvertures d’e-mails]**: nombre d’ouvertures de vos e-mails dans un parcours.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans vos e-mails.

* **[!UICONTROL Rebonds pour les canaux sortants]** : nombre total d’erreurs cumulées lors de la procédure d’envoi et du traitement automatique des retours par rapport au nombre total d’e-mails envoyés.

* **[!UICONTROL Erreurs sortantes]** : nombre total d’erreurs survenues au cours de la procédure d’envoi, empêchant l’envoi à des profils.

* **[!UICONTROL Exclusions sortantes]** : nombre de profils qui ont été exclus par Adobe Journey Optimizer.

+++

## Libellés suivis {#track-link-label}

![](assets/cja-journey-tracked-link-labels.png)

Le tableau **[!UICONTROL Libellés suivis]** offre une vue d’ensemble complète des libellés de lien dans vos e-mails, en mettant en évidence ceux qui génèrent le trafic de visiteurs le plus élevé. Cette fonctionnalité vous permet d’identifier et de hiérarchiser les liens les plus populaires.

+++ En savoir plus sur les mesures des libellés des liens de suivi

* **[!UICONTROL Clics uniques]** : nombre de profils qui ont cliqué sur un contenu dans un e-mail.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans vos e-mails.

* **[!UICONTROL Estimation des clics]** : nombre de clics sur un contenu de votre message, à l’exclusion du trafic de robots identifiés et des interactions non humaines (NHI).
+++

## URL des liens de suivi {#track-link-url}

![](assets/cja-journey-tracked-link-urls.png)

Le tableau **[!UICONTROL URL des liens de suivi]** fournit une vue d’ensemble complète des URL de votre e-mail qui attirent le plus de visiteurs et de visiteuses. Cela vous permet d’identifier et de hiérarchiser les liens les plus populaires, ce qui améliore votre compréhension de l’engagement des profils avec du contenu spécifique dans vos e-mails.

+++ En savoir plus sur les mesures des URL des liens de suivi

* **[!UICONTROL Clics uniques]** : nombre de profils qui ont cliqué sur un contenu dans un e-mail.

* **[!UICONTROL Clics]** : nombre de clics sur un contenu dans vos e-mails.

* **[!UICONTROL Estimation des clics]** : nombre de clics sur un contenu de votre message, à l’exclusion du trafic de robots identifiés et des interactions non humaines (NHI).
+++


## Objets des e-mails {#email-subject}

![](assets/cja-email-subject.png)

Le tableau **[!UICONTROL Objets des e-mails]** fournit une vue d’ensemble complète des objets des e-mails qui attirent le plus de visiteurs et de visiteuses. Cette ressource offre des informations précieuses sur la dynamique d’engagement des audiences.

+++ En savoir plus sur les mesures des objets des e-mails

* **[!UICONTROL Diffusés]** : nombre d’e-mails envoyés avec succès, par rapport au nombre total d’e-mails envoyés.

* **[!UICONTROL Diffusés uniques]** : nombre de profils différents ayant reçu au moins un e-mail, en veillant à ce que les doublons ne soient pas comptés.
+++

## Raisons de rebond {#email-bounce-reasons}

![](assets/cja-journey-email-bounce.png)

Le tableau **[!UICONTROL Raisons de rebond]** compile les données disponibles relatives aux rebonds de messages, fournissant des informations détaillées sur les raisons spécifiques des rebonds d’e-mails.

Pour plus d’informations sur les rebonds, consultez la page [Liste de suppression](../reports/suppression-list.md).

## Causes d’exclusion {#email-excluded}

![](assets/cja-journey-email-excluded.png)

Le tableau **[!UICONTROL Causes d’exclusion]** présente une vue d’ensemble complète des différents facteurs qui ont abouti à l’exclusion des profils d’utilisateurs et d’utilisatrices de l’audience ciblée, entraînant la non-réception du message.

Consultez [cette page](exclusion-list.md) pour obtenir la liste complète des causes d’exclusion.

## Raisons des erreurs {#email-errors}

Le tableau **[!UICONTROL Causes d’erreur]** offre une visibilité des erreurs spécifiques survenues pendant le processus d’envoi, fournissant des informations précieuses sur la nature et l’occurrence des erreurs.
