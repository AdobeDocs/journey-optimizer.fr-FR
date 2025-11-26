---
solution: Journey Optimizer
product: journey optimizer
title: Délégation de sous-domaines dans [!DNL Journey Optimizer]
description: Découvrez comment déléguer vos sous-domaines.
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: sous-domaine, optimizer, délégation
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: 1746efa82611d232b5af07b271739417b4e36e8c
workflow-type: ht
source-wordcount: '982'
ht-degree: 100%

---

# Délégation de sous-domaines dans [!DNL Journey Optimizer] {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="Vos sous-domaines délégués s’affichent ici."
>abstract="Déléguez votre premier sous-domaine. Une fois la délégation terminée, les enregistrements PTR sont créés et les canaux d’e-mail sont activés."

La création d’un sous-domaine pour les campagnes par e-mail permet aux marques d’isoler différents types de trafic (marketing par rapport à entreprise, par exemple) dans des groupes d’adresses IP spécifiques et avec des domaines particuliers, ce qui accélère le processus de préchauffage des adresses IP et améliore la délivrabilité globale.

Si vous partagez un domaine et qu&#39;il est bloqué ou ajouté à la liste bloquée, il peut y avoir un impact sur la diffusion des e-mails de votre entreprise. Les problèmes de réputation ou les blocages d&#39;un domaine particulier de vos communications marketing par e-mail auront un impact spécifique sur ce flux de messagerie. L’utilisation de votre domaine principal comme adresse d’expéditeur pour différents flux d’e-mails peut également interrompre l’authentification par e-mail, ce qui bloque ou place vos messages dans le dossier des courriers indésirables.

>[!CAUTION]
>
>Vous ne pouvez pas utiliser le même domaine d’envoi pour envoyer des messages depuis [!DNL Adobe Journey Optimizer] et à partir d’un autre produit, tel que [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage].

## Pourquoi configurer des sous-domaines ? {#why-set-up-subdomains}

Un sous-domaine est une division de votre domaine qui peut être utilisée pour isoler vos marques ou divers types de trafics (par ex. messages transactionnels et communications marketing).

Prenons l&#39;exemple du domaine « mybrand.com », utilisé pour envoyer des communications transactionnelles et marketing. Dans ce cas, vous pouvez décider de configurer deux sous-domaines :

* le sous-domaine « info.mybrand.com » pour vos communications transactionnelles (confirmation des achats, réinitialisation de mots de passe, etc.),
* et le sous-domaine « marketing.mybrand.com » pour vos emails de prospection.

Ce faisant, vous contribuerez à préserver la réputation de votre domaine et des autres sous-domaines. Par exemple, si les sous-domaines « marketing.mybrand.com » se retrouvaient ajoutés à la liste bloquée par les fournisseurs de services Internet en raison d&#39;une mauvaise délivrabilité, cela empêcherait le domaine « mybrand.com » entier et le sous-domaine « info.mybrand.com » d&#39;être ajoutés à la liste bloquée.

Lors de la mise en œuvre d&#39;une solution, des exigences doivent être satisfaites pour les composants orientés vers l&#39;extérieur : par exemple, configurer les liens et les pages web à suivre, afficher les pages miroir, etc.

Bien que ces exigences soient gérées au moyen de composants hébergés à la fois par Adobe et le client, elles incluent des URL visibles par les destinataires des emails. Afin d&#39;éviter que des URL indiquant la solution technique sous-jacente ou le fournisseur d&#39;hébergement ne soient installées, il est possible de configurer des sous-domaines pour rendre cette opération transparente pour les destinataires des emails.

**En savoir plus**

* Découvrez comment [déléguer vos sous-domaines](delegate-subdomain.md) directement à partir de l&#39;interface.
* Découvrez comment [ajouter des enregistrements Google TXT](google-txt.md) à vos sous-domaines pour réussir la diffusion des e-mails aux adresses Gmail.
* Découvrez comment [accéder aux enregistrements PTR](ptr-records.md) générés pour vos sous-domaines, ce qui permet aux serveurs de messagerie de les vérifier.

## Méthodes de configuration de sous-domaine {#subdomain-delegation-methods}

La configuration de sous-domaine vous permet de configurer une sous-section de votre domaine (techniquement, une « zone DNS ») à utiliser avec Adobe Campaign.

Les méthodes de configuration disponibles sont les suivantes :

### Déléguer entièrement un sous-domaine à Adobe (recommandé) {#full-subdomain-delegation}

[!DNL Journey Optimizer] vous permet de déléguer entièrement vos sous-domaines à Adobe directement à partir de l&#39;interface du produit. Ainsi, Adobe sera en mesure de diffuser des messages en tant que service géré en contrôlant et en gérant tous les aspects du DNS nécessaires à la diffusion, au rendu et au suivi des campagnes par e-mail.

<!--The subdomain is fully delegated to Adobe. Adobe is able to control and maintain all aspects of DNS that are required for delivering, rendering and tracking messages.-->

Vous pouvez compter sur Adobe pour gérer lʼinfrastructure DNS requise afin de répondre aux exigences de délivrabilité standard de vos domaines de marketing par e-mail, tout en continuant à gérer et à contrôler le DNS de leurs domaines de messagerie internes.

>[!IMPORTANT]
>
>La délégation complète de sous-domaine est la méthode préconisée.

Découvrez comment déléguer entièrement un sous-domaine à Adobe dans [cette section](delegate-subdomain.md#set-up-subdomain).

### Configurer un sous-domaine avec des CNAME {#cname-subdomain-setup}

Si des politiques de restriction par domaine sont en vigueur et que vous souhaitez quʼAdobe nʼait quʼun contrôle partiel sur le DNS, vous pouvez choisir dʼeffectuer toutes les activités liées au DNS de votre côté.

La configuration de sous-domaines CNAME permet de créer un sous-domaine et d’utiliser des CNAME pour pointer vers des enregistrements spécifiques à Adobe. Grâce à cette configuration, vous partagez avec Adobe la responsabilité de la maintenance du DNS afin de configurer un environnement pour l’envoi, le rendu et le tracking des e-mails.

>[!CAUTION]
>
>La méthode CNAME est recommandée si les politiques de votre organisation interdisent la méthode de délégation complète de sous-domaine. Cette approche nécessite que vous mainteniez et gériez les enregistrements DNS vous-même.
>
>Adobe ne pourra pas vous aider à modifier, tenir à jour ou gérer le DNS dʼun sous-domaine configuré par la méthode CNAME.

Découvrez comment créer un sous-domaine à l’aide de CNAME pour pointer vers des enregistrements spécifiques à Adobe dans [cette section](delegate-subdomain.md#cname-subdomain-setup).

### Utiliser un sous-domaine personnalisé {#custom-subdomain-delegation}

La méthode de délégation personnalisée vous permet de contrôler et de gérer tous les aspects du DNS nécessaires à la diffusion, au rendu et au suivi des messages.

Dans ce cas, vous possédez et gérez entièrement vos propres sous-domaines et avez un contrôle total sur les certificats générés dans le cadre de ce processus.

Découvrez comment configurer un domaine personnalisé dans [cette section](delegate-custom-subdomain.md).

## Comparaison des méthodes de configuration

Le tableau ci-dessous résume le fonctionnement de ces méthodes, ainsi que le niveau d’effort impliqué :
<!--
| Configuration method | How it works | Level of effort |
|---|---|---|
| **Full delegation** | Create the subdomain and namespace record. Adobe will then configure all DNS records required for Adobe Campaign.<br/><br/>In this setup, Adobe is fully responsible for managing the subdomain and all the DNS records. | Low |
| **CNAME method** |  Create the subdomain and namespace record. Adobe will then provide the records to be placed in your DNS servers and will configure the corresponding values in Adobe Campaign DNS servers.<br/><br/>In this setup, both you and Adobe share responsibility for maintaining DNS. | High |-->


| Méthode de configuration | Fonctionnement | Niveau d&#39;effort |
|---|---|---|
| **Délégation complète** | Créez l’enregistrement du sous-domaine et de l’espace de noms. Adobe configurera alors tous les enregistrements DNS nécessaires à Adobe Campaign.<br/><br/>Dans cette configuration, Adobe est entièrement responsable de la gestion du sous-domaine et de tous les enregistrements DNS. | Faible |
| **Méthode CNAME** | Créez l’enregistrement du sous-domaine et de l’espace de noms. Adobe fournira alors les enregistrements à placer sur vos serveurs DNS et configurera les valeurs correspondantes sur les serveurs DNS Adobe Campaign.<br/><br/>Dans cette configuration, vous partagez avec Adobe la responsabilité de la maintenance du DNS. | Élevé |
| **Méthode de délégation personnalisée** | Création de l’enregistrement du sous-domaine et de l’espace de noms : Adobe fournira ensuite les enregistrements à placer dans vos serveurs DNS. Chargez le certificat SSL obtenu auprès de l’autorité de certification et suivez les étapes du système de feedback en vérifiant la propriété du domaine et l’adresse e-mail de signalement.<br/><br/>Dans cette configuration, vous avez l’entière responsabilité de la gestion du DNS. | Très élevé |

Des informations supplémentaires sur la configuration de domaine sont disponibles dans [cette documentation](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=fr){target="_blank"}.

Si vous avez des questions concernant les méthodes de configuration de sous-domaine, contactez Adobe ou l’assistance clientèle pour obtenir des conseils sur la délivrabilité.


