---
solution: Journey Optimizer
product: journey optimizer
title: Types d’erreur d’e-mail
description: Accédez à la liste de toutes les erreurs d’e-mail possibles lors de l’envoi de diffusions avec Journey Optimizer.
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: reprises, rebond, temporaire, ignoré, définitif, optimizer, erreur
hide: true
hidefromtoc: true
exl-id: a8908b11-2288-4d53-897c-3f99cb5ceab4
source-git-commit: 0cb73489981659c3f231b9def40e0e483ed3aef8
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 100%

---

# Types d’erreur d’e-mail {#email-error-types}

Les motifs possibles d’un échec de diffusion sont multiples : Le tableau ci-dessous présente toutes les erreurs qui peuvent se produire lors de l’envoi de diffusions par e-mail avec [!DNL Journey Optimizer], ainsi que leur description et leur type d’erreur.

Ces erreurs se trouvent dans le [Jeu de données d’événement de retour de message AJO](../data/datasets-query-examples.md#message-feedback-event-dataset) qui contient les logs de diffusion des messages, y compris des informations sur toutes les diffusions de messages provenant de [!DNL Journey Optimizer], et les enregistrements de retours des FAI de messagerie sur les rebonds.

| Libellé de l&#39;erreur | Type d&#39;erreur | Valeur technique | Description |
| --- | --- | --- | --- |
| **Indéterminé** | Ignoré | 1 | Impossible de classer le message de rebond SMTP reçu du FAI. |
| **Destinataire non valide** | Rebond définitif | 10 | L’adresse de la personne destinataire n’est pas valide. |
| **Personne destinataire refusée** | Rebond définitif | 15 | Le FAI de la personne destinataire a refusé le message et il peut bloquer l’expéditeur ou l’expéditrice si la personne destinataire n’est pas supprimée. |
| **Rebond temporaire** | Rebond temporaire | 20 | Le message a temporairement échoué. Il peut réussir lors de prochaines reprises. |
| **Échec du DNS** | Rebond temporaire | 21 | La diffusion du message a fait l’objet d’un échec DNS temporaire. Il peut réussir lors de prochaines reprises. |
| **Boîte pleine** | Rebond temporaire | 22 | La diffusion du message a temporairement échoué, car la boîte de réception de la personne destinataire était pleine. |
| **Trop grande** | Ignoré | 23 | La diffusion du message a temporairement échoué, car la taille du message a dépassé la limite de la personne destinataire. |
| **Délai dépassé** | Ignoré | 24 | La diffusion du message a échoué, car la validité du message a expiré ou l’envoi du message au FAI a pris trop de temps. |
| **Échec de l’administration** | Administration | 25 | La diffusion a échoué en raison d’une configuration de politique dans l’infrastructure d’envoi d’e-mail. |
| **Rebond générique : aucune personne destinataire** | Ignoré | 30 | Le message n’a pas pu être remis, car la personne destinataire n’a pas été identifiée. |
| **Rebond générique** | Ignoré | 40 | La diffusion du message a temporairement échoué pour des raisons non spécifiées. |
| **Blocage de message** | Ignoré | 50 | La diffusion a temporairement échoué en raison de limites de volume ou de débit élevées imposées par le FAI. |
| **Blocage de spam** | Ignoré | 51 | La diffusion a temporairement échoué, car le FAI a considéré les domaines ou les adresses IP de la personne expéditrice comme une source de spam connue. |
| **Contenu indésirable** | Ignoré | 52 | La diffusion a temporairement échoué, car le FAI a classé le contenu de l’e-mail comme spam. |
| **Relais refusé** | Rebond temporaire | 54 | Le message n’a pas pu être accepté, car le domaine de destination n’est pas sur la liste autorisée pour le relais. |
| **Réponse automatique** | Ignoré | 60 | Ces messages sont ignorés par [!DNL Journey Optimizer] lorsqu’ils sont reçus, sauf si le transfert est activé. |
| **Échec transitoire** | Ignoré | 70 | La diffusion pourra faire l’objet d’une reprise à un débit limité ou pourra être différée en cas de suspension. |
| **Réponse au défi** | Rebond temporaire | 100 | La diffusion peut échouer de façon permanente, car [!DNL Journey Optimizer] ne prend pas en charge un mécanisme d’authentification de réponse au défi. |
