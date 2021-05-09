---
title: Délégation de sous-domaines
description: Découvrez comment déléguer vos sous-domaines
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a65cefd0bbd15ffa389bac910eaceb40181cb38d
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Commencer la délégation de sous-domaines

## A propos de la délégation de sous-domaines

### Isoler vos marques pour protéger votre réputation

Un sous-domaine est une division de votre domaine qui peut être utilisée pour isoler vos marques ou divers types de trafic (messages transactionnels, informations marketing, etc.).
Prenons l&#39;exemple du domaine &quot;mybrand.com&quot;, qui est utilisé pour envoyer des communications transactionnelles et marketing. Dans ce cas, vous pouvez décider de configurer deux sous-domaines :

* sous-domaine &quot;info.mybrand.com&quot; pour vos communications transactionnelles (confirmation des achats, réinitialisation du mot de passe, etc.),
* sous-domaine &quot;marketing.mybrand.com&quot; pour vos messages électroniques de prospection.

Ce faisant, vous contribuerez à préserver la réputation de votre domaine et des autres sous-domaines. Par exemple, si les sous-domaines &quot;marketing.mybrand.com&quot; ont été ajoutés à la liste bloquée par des Prestataires Internet en raison d’une mauvaise délivrabilité, cela empêcherait l’ajout de l’ensemble du domaine &quot;mybrand.com&quot; et du sous-domaine &quot;info.mybrand.com&quot; à la liste bloquée.

### Conserver la transparence des URL de vos ressources pour les clients

Lors de la mise en oeuvre d’une solution, les composants externes sont requis : il s&#39;agit notamment de la configuration des liens et des pages Web à suivre, de l&#39;affichage des pages miroir, etc.

Bien que ces exigences soient gérées au moyen de composants hébergés à la fois par l’Adobe et le client, elles incluent des URL visibles par les destinataires des courriels. Afin d’éviter que des URL indiquant la solution technique sous-jacente ou le fournisseur d’hébergement ne soient installées, il est possible de configurer des sous-domaines pour rendre cette opération transparente pour les destinataires des courriels. [En savoir plus sur la délégation](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html) de domaine.

## Délégation de sous-domaines à Journey Optimizer

Journey Optimizer propose plusieurs fonctionnalités pour vous aider à gérer les sous-domaines :

* [Déléguer vos ](delegate-subdomain.md) sous-domaines directement à partir de l&#39;interface,
* [Ajoutez les ](google-txt.md) enregistrements Google TXT dans vos sous-domaines pour garantir la diffusion des courriers électroniques aux adresses Gmail,
* [Accédez aux ](ptr-records.md) enregistrements PTR générés pour vos sous-domaines, ce qui vous permet de les vérifier en envoyant des serveurs de messagerie.
