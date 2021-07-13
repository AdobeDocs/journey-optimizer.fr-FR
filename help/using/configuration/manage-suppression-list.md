---
title: Gestion de la liste de suppression
description: 'Découvrez comment accéder à la liste de suppression de Journey Optimizer et la gérer '
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
feature: Paramétrage de l'application
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 97%

---


# Gestion de la liste de suppression {#manage-suppression-list}

Avec [!DNL Journey Optimizer], vous pouvez surveiller toutes les adresses e-mail qui sont automatiquement exclues de l&#39;envoi dans un parcours, telles que :

* Les adresses non valides (hard bounces) ou qui font l&#39;objet de soft bounces systématiques et qui sont susceptibles de nuire à votre réputation en matière d&#39;e-mails si vous continuez à les inclure dans vos diffusions.
* Les destinataires qui déposent une plainte pour spam contre l&#39;un de vos e-mails.

<!--Profiles who unsubscribe from your sendings. Learn more on [opting-out](../consent.md). NOT TRUE as confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

Ces adresses e-mail sont automatiquement collectées dans la **liste de suppression** de Journey Optimizer. En savoir plus dans [cette section](../suppression-list.md).

## Accéder à la liste de suppression {#access-suppression-list}

Pour accéder à la liste détaillée des adresses e-mail exclues, ouvrez le menu **[!UICONTROL Canaux]** > **[!UICONTROL Configuration des e-mails]** > **[!UICONTROL Général]**, puis cliquez sur le lien **[!UICONTROL Afficher les listes de suppression]**.

![](../assets/suppression-list-link.png)

Des filtres sont disponibles pour vous aider à parcourir la liste.

![](../assets/suppression-list-filters.png)

<!--suppression date,  category and reason, but on staging, only creation date filter is available-->

<!--You can also download the list as a CSV file for analysis and reporting purpose. Won't be available.-->

## Catégories de suppression et motifs {#suppression-categories-and-reasons}

Lorsqu&#39;un message ne parvient pas à être envoyé à une adresse e-mail, Journey Optimizer détermine les motifs de l&#39;échec de la diffusion et l&#39;associe à une catégorie de suppression.

Les catégories de suppression sont les suivantes :

* **Hard** : l&#39;adresse e-mail est immédiatement envoyée à la liste de suppression.

* **Soft** : les erreurs de type Soft envoient une adresse à la liste de suppression une fois que le compteur d&#39;erreurs a atteint le seuil limite. [En savoir plus sur les reprises](retries.md)

* **Ignoré** :
   * Lorsque l&#39;erreur s&#39;est produite pour une adresse e-mail valide, mais qu&#39;elle est considérée comme temporaire (une tentative de connexion ayant échoué ou un problème technique temporaire, par exemple), l&#39;adresse e-mail est ajoutée à la liste de suppression une fois que le compteur d&#39;erreurs a atteint le seuil limite. [En savoir plus sur les reprises.](retries.md).
   * Lorsque l&#39;erreur est le résultat d&#39;une plainte contre les spams, l&#39;adresse e-mail du destinataire qui a émis la plainte est immédiatement envoyée à la liste de suppression.

<!--**Manual**: You can also manually add an email address to the suppression list. => Manual category will be available when manually adding an address to the suppression list (via API)-->

>[!NOTE]
>
>Pour en savoir plus sur les soft bounces et les hard bounces, consultez la section [Types de diffusion en échec](../suppression-list.md#delivery-failures).

Pour chaque adresse e-mail répertoriée, vous pouvez également vérifier le **[!UICONTROL motif]** de son exclusion et la date/l&#39;heure de son ajout à la liste de suppression.

![](../assets/suppression-list-temp.png)
<!--to replace with suppression-list.png when Manual category is available (through API)-->

Les motifs possibles d&#39;une diffusion en échec sont les suivants :

| Motif | Description | Catégorie de suppression |
---------|----------|--------- |
| **[!UICONTROL Indéterminé]** | La raison du rebond reçue de l’agent de transfert de message (MTA) du domaine du destinataire n’a pas pu être identifiée. | Ignoré |
| **[!UICONTROL Destinataire non valide]** | Le destinataire n&#39;est pas valide ou n&#39;existe pas. | Hard |
| **[!UICONTROL Soft Bounce]** | Le message a fait l&#39;objet d&#39;un soft bounce pour un motif autre que les erreurs soft répertoriées dans ce tableau, par exemple lors d&#39;un envoi supérieur au taux autorisé recommandé par un FAI. | Soft |
| **[!UICONTROL Échec du DNS]** | Le message a fait l&#39;objet d&#39;un bounce en raison d&#39;un échec du DNS. | Soft |
| **[!UICONTROL Boîte pleine]** | Le message a fait l&#39;objet d&#39;un bounce, car la boîte du destinataire était pleine et ne pouvait pas accepter d&#39;autres messages. | Soft |
| **[!UICONTROL Trop grande]** | Le message a fait l&#39;objet d&#39;un bounce, car il était trop volumineux pour le destinataire. Des [nouvelles tentatives](retries.md) seront effectuées : vous pouvez modifier la taille du message et le réinjecter pour diffusion. | Ignoré |
| **[!UICONTROL Délai dépassé]** | Le message a expiré, ce qui signifie qu&#39;il a fait l&#39;objet d&#39;un soft bounce et a atteint la limite de tentatives du message (3,5 jours). | Ignoré |
| **[!UICONTROL Échec de l&#39;administrateur]** | Le message a échoué conformément aux stratégies configurées par l&#39;administrateur du système d&#39;envoi. <!--For example, if emails are blackholed at the global, domain or binding level using the "blackhole" directive, this bounce code is used.--> | Ignoré |
| **[!UICONTROL Bounce générique : Pas de RCPT]** | Aucun destinataire n&#39;a pu être déterminé pour le message. | Ignoré |
| **[!UICONTROL Bounce générique]** | Le message a échoué pour des raisons non spécifiées. | Ignoré |
| **[!UICONTROL Blocage du message]** | Le message a été bloqué par le destinataire (c&#39;est-à-dire le MTA du destinataire). | Ignoré |
| **[!UICONTROL Blocage de spam]** | Le message a été bloqué par le destinataire comme provenant d&#39;une source de spam connue. Il peut s&#39;agir, par exemple, du blocage d&#39;une adresse IP d&#39;envoi. | Ignoré |
| **[!UICONTROL Contenu indésirable]** | Le contenu du message a été bloqué par le destinataire (MTA du destinataire) en tant que spam. | Ignoré |
| **[!UICONTROL Pièce jointe interdite]** | Le message a été bloqué par le destinataire, car il contenait une pièce jointe. | Ignoré |
| **[!UICONTROL Relais refusé]** | Le message a été bloqué par le destinataire, car le relais n&#39;est pas autorisé. | Soft |
| **[!UICONTROL Réponse automatique]** | Le message est un message de réponse automatique/de vacances. | Ignoré |
| **[!UICONTROL Échec transitoire]** | La transmission des messages a été temporairement retardée. | Ignoré |
| **[!UICONTROL Réponse au défi]** | Le message est une enquête de réponse au défi. | Soft |

>[!NOTE]
>
>Les utilisateurs désabonnés ne reçoivent pas d&#39;e-mails de [!DNL Journey Optimizer]. Par conséquent, leurs adresses e-mail ne peuvent pas être envoyées à la liste de suppression. Leur choix est géré au niveau d&#39;Experience Platform. En savoir plus sur la [désinscription](../consent.md).

<!--
Removed from the table provided by SparkPost/Momentum:
| **[!UICONTROL Subscribe]** | The message is a subscribe request. | Ignored |
| **[!UICONTROL Unsubscribe]** | The message is an unsubscribe request. | Hard |
-->

<!--Note to add eventually: If a user is subscribed and [!DNL Journey Optimizer] fails to send emails to their subscribed email address, they will get added to the suppression list. (not sure it's possible to subscribe through AJO or need to find reference to Experience Platform doc?)-->


