---
title: Surveillance de l’exécution des messages
description: Découvrez les instructions de surveillance et de délivrabilité
feature: Délivrabilité
topic: Gestion de contenu
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 98%

---

# Gérer la délivrabilité {#manage-deliverability}

La délivrabilité est une mesure du succès de vos diffusions atteignant les boîtes de réception de vos destinataires.

**La délivrabilité des emails désigne l’ensemble des caractéristiques qui déterminent la capacité d’un message à atteindre sa destination, par l’intermédiaire d’une adresse email personnelle, dans un délai court, et avec la qualité attendue en termes de contenu et de format.** Ces caractéristiques se répartissent dans quatre catégories principales : qualité des données, message et contenu, infrastructure d’envoi et réputation. Ensemble, elles forment la base d’un programme de délivrabilité des emails réussi.

Le **taux de délivrabilité** correspond au nombre de messages qui ont atteint les boîtes de réception des destinataires comparé au nombre de messages délivrés. Il dépend de nombreux facteurs, notamment :

* Plaintes contre le spam limitées
* Taux de hard bounces faibles
* Qualité des adresses ciblées
* Contenu des messages
* Réputation de l’expéditeur

Pour optimiser la délivrabilité de vos expériences [!DNL Journey Optimizer], nous vous recommandons d’observer les bonnes pratiques répertoriées dans cette section. En règle générale, les problèmes de délivrabilité sont liés à la protection contre le spam mise en œuvre par les fournisseurs d’accès Internet (FAI) et les administrateurs de serveurs de messagerie.

## Réduire les taux de plainte {#reduce-complaint-rate}

Les FAI disposent généralement d’un moyen important pour signaler un message reçu comme étant du spam. Cela permet d’identifier les sources non fiables. En répondant rapidement aux demandes d’opt-out et en montrant ainsi que vous êtes un expéditeur fiable, vous pouvez réduire les taux de plaintes. [En savoir plus sur la gestion des opt-out](consent.md#opt-out-management).

Il est recommandé de ne pas empêcher les destinataires qui le souhaitent de s’exclure en les obligeant à remplir des champs tels que leur adresse email ou leur nom. La landing page du formulaire de désinscription ne doit comporter qu’un seul bouton de validation.

Redoublez d’attention lorsque vous demandez une confirmation supplémentaire : un utilisateur peut posséder deux adresses email redirigées vers la même boîte de réception (par exemple, prénom.nom@club.com et prénom.nom@internet-club.com). Si le profil est capable de se souvenir uniquement de la première adresse et souhaite se désinscrire via un message envoyé à l’autre, le formulaire refusera cette adresse car l’identifiant chiffré et l’adresse email saisie ne correspondront pas.

## Utiliser les listes de suppression {#suppression-lists}

[!DNL Journey Optimizer] gère une liste de suppression qui rassemble les plaintes contre le spam, les hard bounces et soft bounces qui surviennent de manière systématique.

Pour protéger votre délivrabilité, les destinataires dont les adresses se trouvent sur la liste de suppression sont exclus par défaut de toute diffusion future. En effet, un envoi à ces contacts pourrait nuire à votre réputation d’envoi.

[En savoir plus sur la liste](suppression-list.md) de suppression.

## Utiliser les outils de surveillance {#monitoring-tools}

Utilisez les outils proposés par [!DNL Journey Optimizer] pour surveiller votre délivrabilité.

L’onglet **[!UICONTROL Exécutions]** de la liste de messages vous permet de vérifier les performances de vos diffusions au moyen d’un ensemble d’indicateurs en temps réel. Cet onglet affiche, entre autres :
* Le nombre de messages exécutés, envoyés et délivrés avec succès.
* Le nombre de messages ayant été ouverts et le nombre de messages/liens ayant fait l’objet d’un clic.

[En savoir plus sur la surveillance de l’exécution des messages ](message-monitoring.md).

## Adapter le contenu des messages {#adapt-message-content}

Dans une moindre mesure, le contenu de certains messages peut être détecté comme indésirable.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

Pour améliorer votre taux de délivrabilité et vous assurer que vos emails atteignent vos destinataires, suivez les principes ci-dessous lors de la conception du contenu de vos messages :

* **Nom et adresse de l’expéditeur** : l’adresse doit identifier explicitement l’expéditeur qui doit être propriétaire du domaine et l’avoir enregistré. Le registre du domaine ne doit pas être privatisé.

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **Lien de désinscription et landing page** : le lien de désinscription est essentiel. Il doit être visible et valide, et le formulaire doit fonctionner.

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[En savoir plus sur la conception du contenu des emails](design-emails.md).
