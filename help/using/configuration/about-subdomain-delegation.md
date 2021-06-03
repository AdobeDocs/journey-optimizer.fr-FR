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
source-git-commit: da995c56b59fb191934788c7aea9048123a2fe6d
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 72%

---


# Prise en main de la délégation de sous-domaine

## Isolez vos marques pour protéger votre réputation

Un sous-domaine est une division de votre domaine qui peut être utilisée pour isoler vos marques ou divers types de trafic (messages transactionnels, informations marketing, etc.).
Prenons l&#39;exemple du domaine « mybrand.com », utilisé pour envoyer des communications transactionnelles et marketing. Dans ce cas, vous pouvez décider de configurer deux sous-domaines :

* le sous-domaine « info.mybrand.com » pour vos communications transactionnelles (confirmation des achats, réinitialisation de mots de passe, etc.),
* Et le sous-domaine « marketing.mybrand.com » pour vos emails de prospection.

Ce faisant, vous contribuerez à préserver la réputation de votre domaine et des autres sous-domaines. Par exemple, si les sous-domaines « marketing.mybrand.com » se retrouvaient ajoutés à la liste bloquée par les fournisseurs de services Internet en raison d’une mauvaise délivrabilité, cela empêcherait le domaine « mybrand.com » entier et le sous-domaine « info.mybrand.com » d’être ajoutés à la liste bloquée.

## Gardez les URL de ressources transparentes pour les clients

Lors de la mise en œuvre d’une solution, des exigences doivent être satisfaites pour les composants orientés vers l’extérieur : par exemple, configurer les liens et les pages web à suivre, afficher les pages miroir, etc.

Bien que ces exigences soient gérées au moyen de composants hébergés à la fois par Adobe et le client, elles incluent des URL visibles par les destinataires des emails. Afin d’éviter que des URL indiquant la solution technique sous-jacente ou le fournisseur d’hébergement ne soient installées, il est possible de configurer des sous-domaines pour rendre cette opération transparente pour les destinataires des emails. [En savoir plus sur la délégation de domaine](https://helpx.adobe.com/fr/campaign/kb/domain-name-delegation.html).

## Délégation de sous-domaines dans Journey Optimizer

Journey Optimizer propose plusieurs fonctionnalités pour vous aider à gérer les sous-domaines :

* [Déléguez directement vos ](delegate-subdomain.md) sous-domaines à partir de l’interface,
* [Ajoutez des ](google-txt.md) enregistrements TXT Google à vos sous-domaines pour assurer la diffusion réussie des emails vers les adresses Gmail,
* [Accédez aux ](ptr-records.md) enregistrements PTR générés pour vos sous-domaines, ce qui vous permet de les vérifier en envoyant des serveurs de messagerie.
