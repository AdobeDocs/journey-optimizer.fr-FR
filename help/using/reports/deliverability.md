---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main de la délivrabilité
description: Découvrez les directives relatives à la délivrabilité
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: 8f33dda7-9bd5-4293-8d0d-222205cbc7d5
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Prise en main de la délivrabilité {#manage-deliverability}

La délivrabilité est une mesure du succès de vos diffusions atteignant vos boîtes de réception de destinataires.

>[!NOTE]
>
>Pour les clients qui achètent des licences pour Healthcare Shield, Adobe utilise TLS (Transport Layer Security) 1.2 pour sécuriser l’échange de données entre les systèmes des utilisateurs (destinataires) et Journey Optimizer (expéditeur). Si le serveur de messagerie de réception ne prend pas en charge TLS 1.2, les clients rencontreront des problèmes de délivrabilité, notamment le rebond des courriers électroniques vers l’expéditeur.

**Délivrabilité des emails** fait référence à l’ensemble des caractéristiques qui déterminent la capacité d’un message à atteindre sa destination, par le biais d’une adresse électronique personnelle, dans un délai court, et avec la qualité attendue en termes de contenu et de format. Ces caractéristiques se divisent en quatre catégories principales : qualité des données, message et contenu, infrastructure d’envoi et réputation. Ensemble, ils forment la base d’un programme de délivrabilité des emails réussi.

Le **taux de délivrabilité** est le nombre de messages qui ont atteint la boîte de réception du destinataire par rapport au nombre de messages qui ont été remis. Elle dépend de nombreux facteurs, notamment :

* Demandes de spam limitées
* Taux de hard bounce bas
* Qualité des adresses ciblées
* Contenu du message
* Réputation de l&#39;expéditeur

Pour optimiser la délivrabilité de votre [!DNL Journey Optimizer] , nous vous recommandons d’utiliser les bonnes pratiques répertoriées dans cette section. Les problèmes de délivrabilité sont généralement liés à la protection contre les spams mise en place par les fournisseurs d&#39;accès à Internet (FAI) et les administrateurs de serveurs de messagerie.

Pour une analyse plus approfondie de ce qu&#39;est la délivrabilité et pour en savoir plus sur les termes, concepts et approches clés de la délivrabilité, reportez-vous à la section [Guide des bonnes pratiques en matière de délivrabilité d’Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html){target=&quot;_blank&quot;}.

## Réduction du taux de plaintes {#reduce-complaint-rate}

Les FAI disposent généralement d’un moyen important de signaler un message reçu comme spam. Cela permet d’identifier les sources non fiables. En respectant rapidement les demandes d&#39;opposition et en montrant ainsi que vous êtes un expéditeur fiable, vous pouvez réduire les taux de plaintes. [En savoir plus sur la gestion des désinscriptions](../privacy/opt-out.md#opt-out-management).

En règle générale, n’essayez pas d’interférer avec les destinataires qui souhaitent se désinscrire en leur demandant de remplir des champs tels que leur adresse électronique ou leur nom, par exemple. La landing page de désinscription ne doit comporter qu&#39;un seul bouton de validation.

Faites attention lorsque vous demandez une confirmation supplémentaire : un utilisateur peut avoir deux adresses électroniques redirigées vers la même boîte (par exemple : firstname.lastname@club.com et firstname.lastname@internet-club.com). Si le profil n&#39;est en mesure de se souvenir que de la première adresse et souhaite se désabonner via un message envoyé à l&#39;autre adresse, le formulaire le refuse car l&#39;identifiant crypté et l&#39;adresse email renseignée ne correspondent pas.

## Listes de suppression d’utilisation {#suppression-lists}

[!DNL Journey Optimizer] gère une liste de suppression qui rassemble les plaintes pour spam, les hard bounces et les soft bounces qui se produisent de manière cohérente.

Pour protéger votre délivrabilité, les destinataires dont les adresses figurent sur la liste de suppression sont par défaut exclus de toutes les futures diffusions, car envoyer à ces contacts peut nuire à votre réputation d&#39;envoi.

[En savoir plus sur la liste de suppression](suppression-list.md).

## Utilisation des outils de surveillance {#monitoring-tools}

Utiliser les fonctionnalités proposées par [!DNL Journey Optimizer] pour surveiller votre délivrabilité.

Le **[!UICONTROL Executions]** de la liste des messages vous permet de vérifier les performances de vos diffusions au moyen d’un ensemble d’indicateurs en temps réel. Cet onglet affiche, entre autres :
* Nombre de messages qui ont été exécutés, envoyés et remis avec succès.
* Le nombre de messages ouverts et le nombre de messages/liens ayant fait l’objet d’un clic.

## Adaptation du contenu des messages {#adapt-message-content}

Dans une moindre mesure, le contenu de certains messages peut être détecté comme spam.

Pour améliorer votre taux de délivrabilité et vous assurer que vos emails parviennent à vos destinataires, suivez les principes ci-dessous lors de la conception du contenu de votre message :

* **Nom et adresse de l&#39;expéditeur**: L&#39;adresse doit identifier explicitement l&#39;expéditeur. Le domaine doit appartenir à l’expéditeur et être enregistré auprès de lui. Le registre des domaines ne doit pas être privatisé.

* **Désabonner le lien et la landing page**: Le lien de désabonnement est essentiel. Il doit être visible et valide, et le formulaire doit être fonctionnel.

[En savoir plus sur la conception du contenu d&#39;un email](../email/get-started-email-design.md).

## Établir votre réputation en tant qu’expéditeur

Si vous avez récemment migré vers un autre fournisseur de services de messagerie, une adresse IP, un domaine de messagerie ou un sous-domaine, vous devez établir votre réputation en tant qu’expéditeur. Sinon, vos diffusions peuvent être bloquées ou déplacées dans le dossier spam de la boîte aux lettres des destinataires.

Pour réchauffer votre adresse IP, vous pouvez augmenter progressivement le nombre de vos diffusions. Voir [cas pratique](../building-journeys/ramp-up-deliveries-uc.md).
