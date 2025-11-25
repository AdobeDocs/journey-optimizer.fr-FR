---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec la délivrabilité
description: Découvrez les directives relatives à la délivrabilité
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: ht
source-wordcount: '1138'
ht-degree: 100%

---

# Commencer avec la délivrabilité {#manage-deliverability}

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

Les FAI disposent généralement d&#39;un moyen important pour signaler un message reçu comme étant du spam. Cela permet d&#39;identifier les sources non fiables. En répondant rapidement aux demandes d&#39;opt-out et en montrant ainsi que vous êtes un expéditeur fiable, vous pouvez réduire les taux de plaintes. [En savoir plus sur la gestion des désinscriptions](../privacy/opt-out.md#opt-out-decision-management)

Il est recommandé de ne pas empêcher les destinataires qui souhaitent se désabonner de le faire en les obligeant à remplir des champs tels que leur adresse e-mail ou leur nom. La page de destination du formulaire d&#39;opt-out ne doit comporter qu&#39;un seul bouton de validation.

Redoublez d&#39;attention lorsque vous demandez une confirmation supplémentaire : un utilisateur peut posséder deux adresses email redirigées vers la même boîte de réception (par exemple, prénom.nom@club.com et prénom.nom@internet-club.com). Si le profil est capable de se souvenir uniquement de la première adresse et souhaite se désinscrire via un message envoyé à l&#39;autre, le formulaire refusera cette adresse car l&#39;identifiant chiffré et l&#39;adresse email saisie ne correspondront pas.

## Utiliser les listes de suppression {#suppression-lists}

[!DNL Journey Optimizer] gère une liste de suppression qui rassemble les plaintes contre le spam, les rebonds définitifs et les rebonds temporaires qui surviennent de manière systématique.

Pour protéger votre délivrabilité, les destinataires dont les adresses se trouvent sur la liste de suppression sont exclus par défaut de toute diffusion future. En effet, un envoi à ces contacts pourrait nuire à votre réputation d&#39;envoi.

[En savoir plus sur la liste de suppression](suppression-list.md)

## Utiliser les outils de surveillance {#monitoring-tools}

Utilisez les fonctionnalités de reporting proposées par [!DNL Journey Optimizer] pour surveiller votre délivrabilité.

Les rapports sur les campagnes et les parcours permettent de vérifier les performances de vos diffusions au moyen d’un ensemble d’indicateurs en temps réel. Ils affichent entre autres :

* Le nombre de messages exécutés, envoyés et délivrés avec succès.
* Le nombre de messages ayant été ouverts et le nombre de messages/liens ayant fait l&#39;objet d&#39;un clic.

En savoir plus sur le [rapport dynamique](../reports/live-report.md) et le [rapport de toutes les périodes](../reports/report-gs-cja.md).

## Adapter le contenu des messages {#adapt-message-content}

Dans une moindre mesure, le contenu de certains messages peut être détecté comme indésirable.

Pour améliorer votre taux de délivrabilité et vous assurer que vos emails atteignent vos destinataires, suivez les principes ci-dessous lors de la conception du contenu de vos messages :

* **Nom et adresse de l&#39;expéditeur** : l&#39;adresse doit identifier explicitement l&#39;expéditeur qui doit être propriétaire du domaine et l&#39;avoir enregistré. Le registre du domaine ne doit pas être privatisé.

* **Lien de désinscription et page de destination** : le lien de désinscription est essentiel. Il doit être visible et valide, et le formulaire doit fonctionner.

[En savoir plus sur la conception du contenu des e-mails](../email/get-started-email-design.md)

## Asseyez votre réputation dʼexpéditeur. {#reputation}

Si vous avez récemment migré vers un autre fournisseur de services de messagerie, dʼadresse IP ou de domaine ou sous-domaine de messagerie, vous devez asseoir votre réputation d’expéditeur. Dans le cas contraire, vos diffusions risquent dʼêtre bloquées voire déplacées dans le dossier des courriers indésirables de la boîte aux lettres des destinataires.

Quand vous envoyez des e-mails sur une toute nouvelle adresse IP, vous pouvez désormais facilement exécuter des workflows de préchauffage d’adresses IP directement à partir de l’interface d’utilisation.

Adobe Journey Optimizer offre un moyen standardisé et efficace de préchauffer vos adresses IP en respectant les bonnes pratiques de délivrabilité optimale.

[En savoir plus sur les plans de préchauffage d’adresses IP](../configuration/ip-warmup-gs.md)

<!--To warm up your IP, you can gradually ramp up the number of your deliveries. Learn more in this [use case](../building-journeys/ramp-up-deliveries-uc.md).-->

## Implémenter DMARC {#dmarc}

Pour vous aider à atténuer le risque que des e-mails légitimes soient marqués comme spam ou rejetés, et empêcher les problèmes de délivrabilité, [!DNL Journey Optimizer] vous permet de configurer l’enregistrement DMARC pour tous les sous-domaines que vous déléguez à Adobe.

DMARC (Domain-based Message Authentication, Reporting, and Conformance, soit Authentification, création de rapports et conformité des messages basés sur le domaine) est une méthode d’authentification d’e-mail qui permet aux personnes propriétaires de domaine de protéger leur domaine d’une utilisation non autorisée par des entités malveillantes.

[En savoir plus sur l’enregistrement DMARC](../configuration/dmarc-record.md)

## Connaître les systèmes de feedback {#feedback-loops}

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Certains sous-domaines peuvent ne pas être disponibles."
>abstract="Certains sous-domaines ne peuvent actuellement pas être sélectionnés en raison de l’enregistrement en attente du système de feedback. Ce processus peut prendre jusqu’à 10 jours ouvrables. Une fois cette opération terminée, vous pouvez choisir parmi tous les sous-domaines disponibles."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation" text="Commencer avec la délégation de sous-domaines"

Un système de feedback (FBL) est un service proposé par certains FAI qui permet à l’expéditeur ou l’expéditrice de l’e-mail de recevoir automatiquement un avertissement lorsque l’utilisateur ou l’utilisatrice qui reçoit un e-mail choisit de le marquer comme spam (également appelé une « plainte »).

Lorsqu’un utilisateur final ou une utilisatrice finale génère une plainte qui est renvoyée à Adobe par le FAI, l’adresse e-mail est automatiquement ajoutée à la [liste de suppression](../reports/suppression-list.md) et exclue des diffusions suivantes. En effet, l’envoi d’e-mails aux utilisateurs ou utilisatrices qui les ont marqués comme spam affecte négativement la réputation de l’expéditeur ou l’expéditrice et peut entraîner des problèmes de délivrabilité. [En savoir plus sur les plaintes relatives aux spams](../reports/suppression-list.md#spam-complaints)

>[!IMPORTANT]
>
>Tous les FAI ne fournissent pas une FBL traditionnelle, Gmail par exemple. Gmail ne fournit pas de retour au niveau individuel et ne peut pas être utilisé pour suivre les plaintes relatives aux spams envoyées à des destinataires individuels, en se concentrant plutôt sur les rapports au niveau agrégé dans ses outils Google Postmaster Tools. [En savoir plus](https://support.google.com/a/answer/6254652?hl=fr){target="_blank"}

L’ensemble des clientes et des clients Adobe est automatiquement inscrit sur les FBL traditionnelles des FAI suivants :

* 1&amp;1

* AOL

* BlueTie

* Comcast

* Fastmail

* Gandi

* Italia Online

* La Poste

* Liberty Global (Chello, UPC, Unity Media)

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

## Utiliser le relais SMTP {#smtp-relay}

[!DNL Journey Optimizer] utilise des agents de transfert d’e-mails (MTA) et des adresses IP détenus par Adobe pour diffuser vos e-mails aux fournisseurs d’accès Internet (FAI). Cependant, dans certains cas, vous pouvez souhaiter acheminer les diffusions finales par e-mail via vos propres MTA et adresses IP, ou effectuer des validations finales sur les e-mails avant de les envoyer à vos destinataires.

Dans ce cas, vous pouvez choisir de relayer vos e-mails vers des serveurs SMTP hébergés par votre organisation au lieu de les envoyer directement de Journey Optimizer aux FAI.

>[!AVAILABILITY]
>
>La capacité de relais SMTP est disponible à la demande. Contactez votre représentant ou représentante Adobe.
