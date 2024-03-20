---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main de la délivrabilité
description: Découvrez les directives relatives à la délivrabilité
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 71%

---

# Prise en main de la délivrabilité {#manage-deliverability}

La délivrabilité est une mesure du succès de vos diffusions atteignant les boîtes de réception de vos destinataires.

>[!NOTE]
>
>Pour les clientes et clients qui accordent des licences pour Healthcare Shield, Adobe utilise le protocole TLS (Transport Layer Security) 1.2 afin de sécuriser l’échange de données entre les systèmes des utilisateurs et utilisatrices (destinataires) et Journey Optimizer (expéditeur). Si le serveur d’e-mails de réception ne prend pas en charge TLS 1.2, les clients rencontreront des problèmes de délivrabilité, notamment le rebond des e-mails vers l’expéditeur.

**La délivrabilité des emails désigne l&#39;ensemble des caractéristiques qui déterminent la capacité d&#39;un message à atteindre sa destination, par l&#39;intermédiaire d&#39;une adresse email personnelle, dans un délai court, et avec la qualité attendue en termes de contenu et de format.** Ces caractéristiques se répartissent dans quatre catégories principales : qualité des données, message et contenu, infrastructure d&#39;envoi et réputation. Ensemble, elles forment la base d&#39;un programme de délivrabilité des emails réussi.

Le **taux de délivrabilité** correspond au nombre de messages qui ont atteint les boîtes de réception des destinataires comparé au nombre de messages délivrés. Il dépend de nombreux facteurs, notamment :

* Plaintes contre le spam limitées
* Taux de rebonds définitifs faibles
* Qualité des adresses ciblées
* Contenu des messages
* Réputation de l&#39;expéditeur

Pour optimiser la délivrabilité de vos expériences [!DNL Journey Optimizer], nous vous recommandons d&#39;observer les bonnes pratiques répertoriées dans cette section. En règle générale, les problèmes de délivrabilité sont liés à la protection contre le spam mise en œuvre par les fournisseurs d&#39;accès Internet (FAI) et les administrateurs de serveurs de messagerie.

Pour en apprendre davantage sur la délivrabilité et en savoir plus sur les termes, concepts et approches clés qui s’y rapportent, consultez le [Guide des bonnes pratiques relatives à la délivrabilité d’Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=fr){target="_blank"}.

## Réduire les taux de plainte {#reduce-complaint-rate}

Les FAI disposent généralement d&#39;un moyen important pour signaler un message reçu comme étant du spam. Cela permet d&#39;identifier les sources non fiables. En répondant rapidement aux demandes d&#39;opt-out et en montrant ainsi que vous êtes un expéditeur fiable, vous pouvez réduire les taux de plaintes. [En savoir plus sur la gestion des désinscriptions](../privacy/opt-out.md#opt-out-management)

Il est recommandé de ne pas empêcher les destinataires qui souhaitent se désabonner de le faire en les obligeant à remplir des champs tels que leur adresse e-mail ou leur nom. La page de destination du formulaire d&#39;opt-out ne doit comporter qu&#39;un seul bouton de validation.

Redoublez d&#39;attention lorsque vous demandez une confirmation supplémentaire : un utilisateur peut posséder deux adresses email redirigées vers la même boîte de réception (par exemple, prénom.nom@club.com et prénom.nom@internet-club.com). Si le profil est capable de se souvenir uniquement de la première adresse et souhaite se désinscrire via un message envoyé à l&#39;autre, le formulaire refusera cette adresse car l&#39;identifiant chiffré et l&#39;adresse email saisie ne correspondront pas.

## Utiliser les listes de suppression {#suppression-lists}

[!DNL Journey Optimizer] gère une liste de suppression qui rassemble les plaintes contre le spam, les rebonds définitifs et les rebonds temporaires qui surviennent de manière systématique.

Pour protéger votre délivrabilité, les destinataires dont les adresses se trouvent sur la liste de suppression sont exclus par défaut de toute diffusion future. En effet, un envoi à ces contacts pourrait nuire à votre réputation d&#39;envoi.

[En savoir plus sur la liste de suppression](suppression-list.md)

## Utiliser les outils de surveillance {#monitoring-tools}

Utilisez les outils proposés par [!DNL Journey Optimizer] pour surveiller votre délivrabilité.

L&#39;onglet **[!UICONTROL Exécutions]** de la liste de messages vous permet de vérifier les performances de vos diffusions au moyen d&#39;un ensemble d&#39;indicateurs en temps réel. Cet onglet affiche, entre autres :
* Le nombre de messages exécutés, envoyés et délivrés avec succès.
* Le nombre de messages ayant été ouverts et le nombre de messages/liens ayant fait l&#39;objet d&#39;un clic.

## Adapter le contenu des messages {#adapt-message-content}

Dans une moindre mesure, le contenu de certains messages peut être détecté comme indésirable.

Pour améliorer votre taux de délivrabilité et vous assurer que vos emails atteignent vos destinataires, suivez les principes ci-dessous lors de la conception du contenu de vos messages :

* **Nom et adresse de l&#39;expéditeur** : l&#39;adresse doit identifier explicitement l&#39;expéditeur qui doit être propriétaire du domaine et l&#39;avoir enregistré. Le registre du domaine ne doit pas être privatisé.

* **Lien de désinscription et page de destination** : le lien de désinscription est essentiel. Il doit être visible et valide, et le formulaire doit fonctionner.

[En savoir plus sur la conception du contenu d&#39;un email](../email/get-started-email-design.md)

## Asseyez votre réputation dʼexpéditeur. {#reputation}

Si vous avez récemment migré vers un autre fournisseur de services de messagerie, dʼadresse IP ou de domaine ou sous-domaine de messagerie, vous devez asseoir votre réputation d’expéditeur. Dans le cas contraire, vos diffusions risquent dʼêtre bloquées voire déplacées dans le dossier des courriers indésirables de la boîte aux lettres des destinataires.

Pour préchauffer votre adresse IP, vous pouvez augmenter progressivement le nombre de vos diffusions. En savoir plus sur ce [cas d’utilisation](../building-journeys/ramp-up-deliveries-uc.md).

## Implémenter DMARC {#dmarc}

Pour vous aider à atténuer le risque que des emails légitimes soient marqués comme spam ou rejetés, et empêcher les problèmes de délivrabilité, [!DNL Journey Optimizer] vous permet de configurer l’enregistrement DMARC pour tous les sous-domaines que vous déléguez à l’Adobe.

DMARC (Domain-based Message Authentication, Reporting, and Conformance) est une méthode d’authentification des emails qui permet aux propriétaires de domaine de protéger leur domaine d’une utilisation non autorisée par des acteurs malveillants.

[En savoir plus sur l’enregistrement DMARC](../configuration/dmarc-record.md)

## Connaître les boucles de rétroaction {#feedback-loops}

Une feedback loop (FBL) est un service proposé par certains FAI qui permet à l&#39;expéditeur de l&#39;email d&#39;être automatiquement averti lorsque l&#39;utilisateur qui reçoit un email choisit de le marquer comme spam (aussi appelé &quot;réclamation&quot;).

Lorsqu’un utilisateur final génère une plainte qui est renvoyée à l’Adobe par le FAI, l’adresse électronique est automatiquement ajoutée au [liste de suppression](../reports/suppression-list.md) et exclus des prochaines diffusions. En effet, l’envoi d’emails aux utilisateurs qui les ont marqués comme spam affecte négativement la réputation de l’expéditeur et peut entraîner des problèmes de délivrabilité. [En savoir plus sur les plaintes relatives au spam](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>Tous les FAI ne fournissent pas une FBL traditionnelle, comme Gmail. Gmail n’offre pas de retour au niveau individuel et ne peut pas être utilisé pour suivre les plaintes liées au spam envoyées à des destinataires individuels, en se concentrant plutôt sur les rapports au niveau agrégé dans leurs outils Postmaster Google. [En savoir plus](https://support.google.com/a/answer/6254652?hl=en){target="_blank"}

Tous les clients Adobe sont automatiquement inscrits dans les FBL classiques des FAI suivants :

* 1&amp;1

* AOL

* BlueTie

* Comcast

* Fastmail

* Gandi

* Italia Online

* La Poste

* Liberty Global (Chello, UPC, Unity Media)

* Locaweb

* Mail.RU

* Microsoft

* OpenSRS

* Rackspace

* SEZNM

* SFR

* SilverSky

* Swisscom

* Synacor

* Telecom Italia

* Telenet

* Telenor

* Telstra

* Terra

* UOL

* Virgin Media

* Yahoo

* Ziggo

Adobe effectue régulièrement des audits de ces FBL pour s’assurer que les dernières FBL disponibles sont ajoutées.
