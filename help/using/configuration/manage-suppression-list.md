---
title: Gestion de la liste de suppression
description: 'Découvrez comment accéder à la liste de suppression de Journey Optimizer et la gérer '
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: 4b515b497de3721794f22c6833ed1f5269110171
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 8%

---


# Gérer la liste de suppression {#manage-suppression-list}

Avec [!DNL Journey Optimizer], vous pouvez surveiller toutes les adresses électroniques qui sont automatiquement exclues de l’envoi dans un parcours, telles que :

* Adresses non valides (hard bounces) ou présentant un soft bounce constant, et susceptibles d’affecter la réputation de votre email si vous continuez à les inclure dans vos diffusions.
* Les destinataires qui déposent une plainte pour courrier indésirable contre l’un de vos emails.

<!--Profiles who unsubscribe from your sendings. Learn more on [opting-out](../consent.md). NOT TRUE as confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

Ces adresses électroniques sont automatiquement collectées dans la **liste de suppression** Journey Optimizer. En savoir plus dans [cette section](../suppression-list.md).

## Accéder à la liste de suppression {#access-suppression-list}

Pour accéder à la liste détaillée des adresses email exclues, ouvrez le menu **[!UICONTROL Canaux]** > **[!UICONTROL Configuration des emails]** > **[!UICONTROL Général]**, puis cliquez sur le lien **[!UICONTROL Afficher les listes de suppression]** .

![](../assets/suppression-list-link.png)

Des filtres sont disponibles pour vous aider à parcourir la liste.

![](../assets/suppression-list-filters.png)

<!--suppression date,  category and reason, but on staging, only creation date filter is available-->

<!--You can also download the list as a CSV file for analysis and reporting purpose. Won't be available.-->

## Catégories de suppression et raisons {#suppression-categories-and-reasons}

Lorsqu’un message ne parvient pas à être envoyé à une adresse électronique, Journey Optimizer détermine les raisons de l’échec de la diffusion et l’associe à une catégorie de suppression.

Les catégories de suppression sont les suivantes :

* **Hard** : L’adresse électronique est immédiatement envoyée à la liste de suppression.

* **Soft** : Les erreurs de type Soft envoient une adresse à la liste de suppression une fois que le compteur d’erreurs a atteint le seuil limite. [En savoir plus sur les reprises](retries.md)

* **Ignoré**:
   * Lorsque l’erreur s’est produite pour une adresse électronique valide, mais qu’elle est considérée comme temporaire (une tentative de connexion ayant échoué ou un problème technique temporaire, par exemple), l’adresse électronique est ajoutée à la liste de suppression une fois que le compteur d’erreurs a atteint le seuil limite. [En savoir plus sur les reprises](retries.md).
   * Lorsque l&#39;erreur est le résultat d&#39;une plainte de spam, l&#39;adresse email du destinataire qui a émis la plainte est immédiatement envoyée à la liste de suppression.

<!--**Manual**: You can also manually add an email address to the suppression list. => Manual category will be available when manually adding an address to the suppression list (via API)-->

>[!NOTE]
>
>Pour en savoir plus sur les soft bounces et les hard bounces, consultez la section [Types de diffusion en échec](../suppression-list.md#delivery-failures) .

Pour chaque adresse électronique répertoriée, vous pouvez également vérifier la **[!UICONTROL raison]** de son exclusion et la date/l’heure de son ajout à la liste de suppression.

![](../assets/suppression-list-temp.png)
<!--to replace with suppression-list.png when Manual category is available (through API)-->

Les motifs possibles d’une diffusion en échec sont les suivants :

| Motif | Description | Catégorie de suppression |
---------|----------|--------- |
| **[!UICONTROL Indéterminé]** | La raison du rebond reçue de l’agent de transfert de messagerie (MTA) du domaine du destinataire n’a pas pu être identifiée. | Ignoré |
| **[!UICONTROL Destinataire non valide]** | Le destinataire n&#39;est pas valide ou n&#39;existe pas. | Hard |
| **[!UICONTROL Soft Bounce]** | Le message soft a rebondi pour une raison autre que les erreurs soft répertoriées dans ce tableau, par exemple lors de l’envoi du taux autorisé recommandé par un FAI. | Soft |
| **[!UICONTROL Échec du DNS]** | Le message a rebondi en raison d’un échec du DNS. | Soft |
| **[!UICONTROL Boîte pleine]** | Le message a rebondi car la boîte du destinataire était pleine et ne pouvait pas accepter d’autres messages. | Soft |
| **[!UICONTROL Trop grande]** | Le message a rebondi car il était trop volumineux pour le destinataire. [](retries.md) Les récupérations seront effectuées : vous pouvez éditer la taille du message et le réinjecter pour diffusion. | Ignoré |
| **[!UICONTROL Délai dépassé]** | Le message a expiré, ce qui signifie qu’il a soft bounce et a atteint la limite de reprise du message (3,5 jours). | Ignoré |
| **[!UICONTROL Échec de l’administration]** | Le message a échoué conformément aux stratégies configurées par l’administrateur du système d’envoi. <!--For example, if emails are blackholed at the global, domain or binding level using the "blackhole" directive, this bounce code is used.--> | Ignoré |
| **[!UICONTROL Rebond générique : No RCPT]** | Aucun destinataire n’a pu être déterminé pour le message. | Ignoré |
| **[!UICONTROL Rebond générique]** | Le message a échoué pour des raisons non spécifiées. | Ignoré |
| **[!UICONTROL Bloc de messagerie]** | Le message a été bloqué par le destinataire (c&#39;est-à-dire le MTA du destinataire). | Ignoré |
| **[!UICONTROL Bloc de spam]** | Le message a été bloqué par le destinataire comme provenant d’une source de spam connue. Il peut s’agir, par exemple, d’un bloc IP d’envoi. | Ignoré |
| **[!UICONTROL Contenu indésirable]** | Le contenu du message a été bloqué par le destinataire (MTA du destinataire) en tant que spam. | Ignoré |
| **[!UICONTROL Pièce jointe interdite]** | Le message a été bloqué par le récepteur car il contenait une pièce jointe. | Ignoré |
| **[!UICONTROL Relais refusé]** | Le message a été bloqué par le récepteur car le relais n’est pas autorisé. | Soft |
| **[!UICONTROL Réponse automatique]** | Le message est un message de réponse automatique/de vacances. | Ignoré |
| **[!UICONTROL Échec transitoire]** | La transmission des messages a été temporairement retardée. | Ignoré |
| **[!UICONTROL Réponse au défi]** | Le message est une enquête de réponse aux défis. | Soft |

>[!NOTE]
>
>Les utilisateurs désabonnés ne reçoivent pas d’e-mails de [!DNL Journey Optimizer]. Par conséquent, leurs adresses électroniques ne peuvent pas être envoyées à la liste de suppression. Leur choix est géré au niveau de l’Experience Platform. En savoir plus sur [opt-out](../consent.md).

<!--
Removed from the table provided by SparkPost/Momentum:
| **[!UICONTROL Subscribe]** | The message is a subscribe request. | Ignored |
| **[!UICONTROL Unsubscribe]** | The message is an unsubscribe request. | Hard |
-->

<!--Note to add eventually: If a user is subscribed and [!DNL Journey Optimizer] fails to send emails to their subscribed email address, they will get added to the suppression list. (not sure it's possible to subscribe through AJO or need to find reference to Experience Platform doc?)-->


