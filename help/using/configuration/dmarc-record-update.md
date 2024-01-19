---
solution: Journey Optimizer
product: journey optimizer
title: Enregistrement DMARC
description: Découvrez comment définir l’enregistrement DMARC dans Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: sous-domaine, domaine, courrier, dmarc, enregistrement
hide: true
hidefromtoc: true
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 19%

---

# Mise à jour importante de l’enregistrement DMARC{#dmarc-record}


>[!CAUTION]
>
>Suite aux récentes annonces Gmail et Yahoo pour les expéditeurs en masse, Journey Optimizer prend désormais en charge la technologie d’authentification DMARC.

Dans le cadre de leur application des bonnes pratiques du secteur, Google et Yahoo exigeront tous deux que vous disposiez d’un enregistrement DMARC pour tout domaine que vous utilisez pour leur envoyer des emails. Cette nouvelle exigence commence à **1er février 2024**.

En savoir plus sur les exigences de Google et de Yahoo pour l’enregistrement DMARC dans [cette section](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

En savoir plus sur les modifications annoncées dans Google et Yahoo sur [cette page](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Vous disposez ensuite d’une action ou des étapes suivantes pour votre section qui indiquent :

Vous devez le configurer pour tous vos sous-domaines.
* Si vous nous avez entièrement délégué le domaine, deux options s’offrent à vous.
   * Configurez DMARC sur le domaine parent du domaine délégué dans votre solution d’hébergement, OU
   * Configurez DMARC sur le domaine délégué à l’aide de notre fonctionnalité à venir dans l’interface utilisateur d’administration sans travail supplémentaire sur l’hébergement de la solution.
* Si vous avez configuré le CNAME pour vos domaines d’envoi, deux options s’offrent à vous.
   * Configurez DMARC sur le sous-domaine OU le domaine parent du sous-domaine dans votre solution d’hébergement, OU
   * Configurez DMARC à l’aide de notre fonctionnalité à venir dans l’interface utilisateur d’administration. Cependant, cela ne nécessitera pas seulement notre interface utilisateur, mais également l’entrée dans la solution d’hébergement.

D’autres détails sur notre prochaine fonctionnalité seront bientôt disponibles.

En outre, vous pouvez inclure l’impact s’il n’est pas défini en copiant la section appropriée pour DMARC depuis la section inférieure (copiée à partir du lien ci-dessus). Soit nous sortons simplement des choses liées à DMARC. Ou ici, vous pouvez apprendre que l’annonce est pour DMARC et un clic de désabonnement et voici la dernière chronologie des deux fonctionnalités.

Des mises à jour des calendriers ont été publiées depuis l&#39;annonce initiale en octobre.

Les dernières en date se présentent comme suit :

Gmail :

* Février 2024 : les rebonds temporaires destinés à avertir de la non-conformité seront mis en place. Si vous n’êtes pas encore en conformité, les e-mails seront toujours livrés normalement après un court délai. Si vous êtes entièrement en conformité, il n’y aura pas de rebonds temporaires et vous ne remarquerez rien.
* Avril 2024 : les blocages commenceront pour les expéditeurs et expéditrices qui ne sont pas en conformité avec toutes les règles, à l’exception de List-Unsubscribe 1-Click. Seule une partie des e-mails non conformes sera bloquée dans un premier temps, le pourcentage de blocage augmentant au fil du temps.
* 1er juin 2024 : l’ensemble des expéditeurs et expéditrices qui ne sont pas en conformité totale, y compris List-Unsubscribe 1-Click, seront bloqués.

Yahoo :

N’a pas fourni de dates exactes, mais a déclaré que &quot;le déploiement de l’application commencera en février 2024. L’application sera progressivement déployée&quot;.
