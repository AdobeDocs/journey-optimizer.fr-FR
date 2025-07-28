---
solution: Journey Optimizer
product: journey optimizer
title: Types d'erreur e-mail
description: Accédez à la liste de toutes les erreurs e-mail possibles lors de l’envoi de diffusions avec Journey Optimizer.
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: reprises, bounce, soft, ignoré, hard, optimizer, erreur
hide: true
hidefromtoc: true
source-git-commit: 817f7c88bfc2b40a7ce39575b4ad02fb372d429d
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 19%

---


# Types d&#39;erreur e-mail {#email-error-types}

Les raisons possibles d’un échec de diffusion sont multiples. Le tableau ci-dessous détaille toutes les erreurs qui peuvent se produire lors de l’envoi de diffusions e-mail avec [!DNL Journey Optimizer], ainsi que leur description et leur type d’erreur.

Ces erreurs se trouvent dans le [Jeu de données d’événement de retour de message AJO](../data/datasets-query-examples.md#message-feedback-event-dataset) qui contient les logs de diffusion des messages, y compris des informations sur toutes les diffusions de messages provenant de [!DNL Journey Optimizer], et les enregistrements de retours des FAI de messagerie sur les bounces.

| Libellé de l&#39;erreur | Type d&#39;erreur | Valeur technique | Description |
| --- | --- | --- | --- |
| **Indéterminé** | Ignoré | 1 | Impossible de classer le message de rebond SMTP reçu du FAI. |
| **Destinataire non valide** | Rebond définitif | 10 | L&#39;adresse du destinataire n&#39;est pas valide. |
| **Destinataire refusé** | Rebond définitif | 15 | Le FAI du destinataire a refusé le message et le FAI peut bloquer l’expéditeur si le destinataire n’est pas supprimé. |
| **Rebond temporaire** | Rebond temporaire | 20 | Le message a subi un échec temporaire. Il peut réussir lors de prochaines reprises. |
| **Échec du DNS** | Rebond temporaire | 21 | La diffusion du message a subi un échec DNS temporaire. Il peut réussir lors de prochaines reprises. |
| **Boîte pleine** | Rebond temporaire | 22 | Le message a temporairement échoué, car la boîte aux lettres du destinataire était pleine. |
| **Trop grande** | Ignoré | 23 | Le message a temporairement échoué, car la taille du message a dépassé la limite du destinataire. |
| **Délai dépassé** | Ignoré | 24 | La diffusion du message a échoué car la validité du message a expiré ou l&#39;envoi du message au FAI a pris trop de temps. |
| **Échec de l&#39;administrateur** | Administration | 25 | La diffusion a échoué en raison d&#39;une configuration de politique dans l&#39;infrastructure d&#39;envoi d&#39;email. |
| **Rebond générique : AUCUN RCPT** | Ignoré | 30 | Le message n’a pas pu être remis car le destinataire n’a pas été identifié. |
| **Rebond générique** | Ignoré | 40 | Le message a rencontré un échec de diffusion temporaire pour des raisons non spécifiées. |
| **Blocage du message** | Ignoré | 50 | La diffusion a connu une défaillance temporaire en raison de limites de volume ou de débit élevées imposées par le FAI. |
| **Blocage de spam** | Ignoré | 51 | La diffusion a temporairement échoué, car le FAI a considéré les domaines ou les adresses IP de l&#39;expéditeur comme une source de spam connue. |
| **Contenu indésirable** | Ignoré | 52 | La diffusion a temporairement échoué, car le FAI a classé le contenu de l’e-mail comme spam. |
| **Relais refusé** | Rebond temporaire | 54 | Le message n’a pas pu être accepté, car le domaine de destination n’est pas sur la liste autorisée pour le relais. |
| **Réponse automatique** | Ignoré | 60 | Ces messages sont ignorés par les [!DNL Journey Optimizer] lorsqu’ils sont reçus, sauf si le transfert est activé. |
| **Échec transitoire** | Ignoré | 70 | La diffusion sera relancée à un rythme ralenti ou pourra être différée en cas de suspension. |
| **Réponse au défi** | Rebond temporaire | 100 | La diffusion peut échouer de manière permanente, car [!DNL Journey Optimizer] ne prend pas en charge un mécanisme d’authentification de réponse au défi. |
