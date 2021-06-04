---
title: Délégation de sous-domaines
description: Découvrez comment déléguer vos sous-domaines
internal: n
snippet: y
source-git-commit: e569e992530df5429ffb96f78ba28b53de0ded81
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 71%

---


# Délégation de sous-domaine dans [!DNL Journey Optimizer]

La création d&#39;un sous-domaine pour les campagnes par email permet aux marques d&#39;isoler différents types de trafic (marketing par rapport à entreprise, par exemple) dans des pools d&#39;adresses IP spécifiques et avec des domaines particuliers, ce qui accélère le processus de réchauffement des adresses IP et améliore la délivrabilité globale. Si vous partagez un domaine et qu’il est bloqué ou ajouté à la liste bloquée, cela peut avoir un impact sur la diffusion de votre courrier d’entreprise. Les problèmes de réputation ou les blocages d&#39;un domaine particulier de vos communications marketing par email auront un impact spécifique sur ce flux de messagerie. L&#39;utilisation de votre domaine principal comme adresse d&#39;expéditeur pour différents flux d&#39;email peut également interrompre l&#39;authentification par email, ce qui bloque ou place vos messages dans le dossier des courriers indésirables.

Un sous-domaine est une division de votre domaine qui peut être utilisée pour isoler vos marques ou divers types de trafic, par exemple les messages transactionnels et les communications marketing.

Prenons l&#39;exemple du domaine « mybrand.com », utilisé pour envoyer des communications transactionnelles et marketing. Dans ce cas, vous pouvez décider de configurer deux sous-domaines :

* le sous-domaine « info.mybrand.com » pour vos communications transactionnelles (confirmation des achats, réinitialisation de mots de passe, etc.),
* Et le sous-domaine « marketing.mybrand.com » pour vos emails de prospection.

Ce faisant, vous contribuerez à préserver la réputation de votre domaine et des autres sous-domaines. Par exemple, si les sous-domaines « marketing.mybrand.com » se retrouvaient ajoutés à la liste bloquée par les fournisseurs de services Internet en raison d’une mauvaise délivrabilité, cela empêcherait le domaine « mybrand.com » entier et le sous-domaine « info.mybrand.com » d’être ajoutés à la liste bloquée.

Lors de la mise en œuvre d’une solution, des exigences doivent être satisfaites pour les composants orientés vers l’extérieur : par exemple, configurer les liens et les pages web à suivre, afficher les pages miroir, etc.

Bien que ces exigences soient gérées au moyen de composants hébergés à la fois par Adobe et le client, elles incluent des URL visibles par les destinataires des emails. Afin d’éviter que des URL indiquant la solution technique sous-jacente ou le fournisseur d’hébergement ne soient installées, il est possible de configurer des sous-domaines pour rendre cette opération transparente pour les destinataires des emails.

**En savoir plus**

* Découvrez comment [déléguer vos sous-domaines](delegate-subdomain.md) directement à partir de l’interface
* Découvrez comment [ajouter des enregistrements TXT Google](google-txt.md) à vos sous-domaines pour garantir la diffusion réussie des emails aux adresses Gmail.
* Découvrez comment [accéder aux enregistrements PTR](ptr-records.md) générés pour vos sous-domaines, ce qui permet de les vérifier en envoyant des serveurs de messagerie.
