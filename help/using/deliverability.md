---
title: Surveillance de l’exécution des messages
description: Apprenez à surveiller et à fournir des directives
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# Gérer la délivrabilité {#manage-deliverability}

![](assets/do-not-localize/badge.png)

La délivrabilité est une mesure du succès de vos diffusions dans vos boîtes de réception destinataires.

**La** délivrabilité des courriels se rapporte à l&#39;ensemble des caractéristiques qui déterminent la capacité d&#39;un message à atteindre sa destination, par l&#39;intermédiaire d&#39;une adresse de courriel personnelle, dans un délai court, et avec la qualité attendue en termes de contenu et de format. Ces caractéristiques se répartissent en quatre catégories principales : qualité des données, message et contenu, infrastructure d’envoi et réputation. Ensemble, ils forment la base d&#39;un programme de livraison de courrier électronique réussi.

Le **taux de délivrabilité** correspond au nombre de messages qui ont atteint les boîtes de réception des destinataires par rapport au nombre de messages qui ont été remis. Elle dépend de nombreux facteurs, notamment :

* Plaintes de spam limitées
* Taux de rebond dur bas
* Qualité des adresses ciblées
* Contenu du message
* Connaissance de l&#39;expéditeur

Pour optimiser la délivrabilité de vos expériences [!DNL Journey Optimizer], nous vous recommandons d’utiliser les meilleures pratiques répertoriées dans cette section. Les problèmes de délivrabilité sont généralement liés à la protection contre le spam mise en oeuvre par les prestataires Internet (FAI) et les administrateurs de serveurs de messagerie.

## Réduire le taux de plainte {#reduce-complaint-rate}

Les FAI disposent généralement d&#39;un moyen de rapports important d&#39;un message reçu en tant que spam. Cela permet d&#39;identifier les sources non fiables. En répondant rapidement aux demandes d’exclusion et en montrant que vous êtes un expéditeur fiable, vous pouvez réduire les taux de plaintes. [En savoir plus sur la gestion](consent.md#opt-out-management) des exclusions.

En règle générale, n’essayez pas d’empêcher les destinataires qui souhaitent s’exclure en les obligeant à remplir des champs tels que leur adresse électronique ou leur nom, par exemple. Le landing page de désinscription ne doit comporter qu’un seul bouton de validation.

Faites attention lorsque vous demandez une confirmation supplémentaire : un utilisateur peut voir deux adresses électroniques redirigées vers la même zone (par exemple : firstname.lastname@club.com et firstname.lastname@internet-club.com). Si le profil est capable de se souvenir de la première adresse seulement et souhaite se désabonner via un message envoyé à l&#39;autre, le formulaire refusera cette adresse car l&#39;identifiant chiffré et l&#39;adresse électronique saisie ne correspondent pas.

## Listes de suppression d&#39;exploitation {#suppression-lists}

[!DNL Journey Optimizer] gère une liste de suppression qui collecte les plaintes de spam, les rebonds durs et les rebonds doux qui se produisent de manière cohérente.

Pour protéger votre délivrabilité, les destinataires dont les adresses sont sur la liste de suppression sont exclus par défaut de toutes les diffusions futures, car envoyer à ces contacts pourrait nuire à votre réputation d&#39;envoi.

[En savoir plus sur les listes](suppression-lists.md) de suppression.

## Utiliser les outils de surveillance {#monitoring-tools}

Utilisez les fonctionnalités offertes par [!DNL Journey Optimizer] pour surveiller votre délivrabilité.

L&#39;onglet **[!UICONTROL Exécutions]** de la liste de messages vous permet de vérifier les performances de vos diffusions au moyen d&#39;un ensemble d&#39;indicateurs en temps réel. Cet onglet affiche, entre autres :
* Nombre de messages exécutés, envoyés et remis avec succès.
* Nombre de messages qui ont été ouverts et nombre de messages/liens qui ont fait l’objet d’un clic.

[En savoir plus sur la surveillance de l’exécution](message-monitoring.md) des messages.

## Adapter le contenu du message {#adapt-message-content}

Dans une moindre mesure, le contenu de certains messages peut être détecté comme indésirable.

<!--The use of certain words or of exclamation points in the subject line and within the messages can be read as signs of spam.

Spammers are also known to replace text with images to stop offending text from being analyzed automatically by anti-spam filters. In response to this, a message (in HTML format) with a high proportion of images, or images as attachments, may end up being blocked.-->

Pour améliorer votre taux de délivrabilité et vous assurer que vos courriels atteignent vos destinataires, suivez les principes ci-dessous lors de la conception du contenu de votre message :

* **Nom et adresse** de l&#39;expéditeur : L&#39;adresse doit identifier explicitement l&#39;expéditeur. Le domaine doit être détenu par l&#39;expéditeur et enregistré auprès de celui-ci. Le registre des domaines ne doit pas être privatisé.

<!--* **Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).
* **Personalize your email**: Personalizing the email increases the chances of your message being opened.
* **Images and text**: Respect a decent text/image ratio (for example 60% text and 40% images).-->
* **Désabonner le lien et le landing page** : Le lien de désabonnement est essentiel. Il doit être visible et valide et le formulaire doit être fonctionnel.

<!--**Use tools** offered by Journey Optimizer to optimize the content of your email (delivery analysis, anti-spam analysis).-->

[En savoir plus sur la conception de contenu](design-emails.md) de courrier électronique.
