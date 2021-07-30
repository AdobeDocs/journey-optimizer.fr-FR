---
title: Délégation de sous-domaines
description: Découvrez comment déléguer vos sous-domaines
internal: n
snippet: y
feature: Paramétrage de l’application
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 100%

---


# Délégation de sous-domaines dans [!DNL Journey Optimizer]

La création d&#39;un sous-domaine pour les campagnes e-mail permet aux marques d&#39;isoler différents types de trafic (marketing par rapport à entreprise, par exemple) dans des pools d&#39;adresses IP spécifiques et avec des domaines particuliers, ce qui accélère le processus de réchauffement des adresses IP et améliore la délivrabilité globale. Si vous partagez un domaine et qu&#39;il est bloqué ou ajouté à la liste bloquée, il peut y avoir un impact sur la diffusion des e-mails de votre entreprise. Les problèmes de réputation ou les blocages d&#39;un domaine particulier de vos communications marketing par e-mail auront un impact spécifique sur ce flux de messagerie. L&#39;utilisation de votre domaine principal comme adresse d&#39;expéditeur pour différents flux d&#39;e-mails peut également interrompre l&#39;authentification par e-mail, ce qui bloque ou place vos messages dans le dossier des courriers indésirables.

Un sous-domaine est une division de votre domaine qui peut être utilisée pour isoler vos marques ou divers types de trafics (par ex. messages transactionnels et communications marketing).

Prenons l&#39;exemple du domaine « mybrand.com », utilisé pour envoyer des communications transactionnelles et marketing. Dans ce cas, vous pouvez décider de configurer deux sous-domaines :

* le sous-domaine « info.mybrand.com » pour vos communications transactionnelles (confirmation des achats, réinitialisation de mots de passe, etc.),
* Et le sous-domaine « marketing.mybrand.com » pour vos emails de prospection.

Ce faisant, vous contribuerez à préserver la réputation de votre domaine et des autres sous-domaines. Par exemple, si les sous-domaines « marketing.mybrand.com » se retrouvaient ajoutés à la liste bloquée par les fournisseurs de services Internet en raison d&#39;une mauvaise délivrabilité, cela empêcherait le domaine « mybrand.com » entier et le sous-domaine « info.mybrand.com » d&#39;être ajoutés à la liste bloquée.

Lors de la mise en œuvre d&#39;une solution, des exigences doivent être satisfaites pour les composants orientés vers l&#39;extérieur : par exemple, configurer les liens et les pages web à suivre, afficher les pages miroir, etc.

Bien que ces exigences soient gérées au moyen de composants hébergés à la fois par Adobe et le client, elles incluent des URL visibles par les destinataires des emails. Afin d&#39;éviter que des URL indiquant la solution technique sous-jacente ou le fournisseur d&#39;hébergement ne soient installées, il est possible de configurer des sous-domaines pour rendre cette opération transparente pour les destinataires des emails.

**En savoir plus**

* Découvrez comment [déléguer vos sous-domaines](delegate-subdomain.md) directement à partir de l&#39;interface.
* Découvrez comment [ajouter des enregistrements Google TXT](google-txt.md) à vos sous-domaines pour réussir la diffusion des e-mails aux adresses Gmail.
* Découvrez comment [accéder aux enregistrements PTR](ptr-records.md) générés pour vos sous-domaines, ce qui permet aux serveurs de messagerie de les vérifier.
