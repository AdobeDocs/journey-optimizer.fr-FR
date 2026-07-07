---
solution: Journey Optimizer
product: journey optimizer
title: Conseils de la CNIL sur les pixels de tracking email
description: Découvrez les conseils mis à jour de la CNIL sur les pixels de tracking e-mail et les contrôles Adobe Journey Optimizer qui peuvent prendre en charge vos efforts de conformité.
feature: Privacy, Consent Management
topic: Content Management
role: User
level: Intermediate
keywords: CNIL, tracking, pixel, e-mail, consentement, opt-out, confidentialité
source-git-commit: 66b0ca498ae2b39575ed57118739234d1f54c887
workflow-type: tm+mt
source-wordcount: '1466'
ht-degree: 1%

---


# Comprendre les nouveaux conseils de la CNIL sur les pixels de tracking email {#cnil-pixel-tracking}

>[!BEGINSHADEBOX]

**Sur cette page :** Découvrez la recommandation d’avril 2026 de la CNIL sur les pixels de tracking e-mail et découvrez les contrôles Adobe Journey Optimizer (basculements de tracking des ouvertures, suivi au niveau des liens, gestion du consentement, mécanismes de désinscription et suppression) qui peuvent soutenir vos efforts de conformité.

>[!ENDSHADEBOX]

>[!NOTE]
>
>Cette page est fournie à titre d’information uniquement. Il ne s&#39;agit pas d&#39;un avis juridique et ne garantit pas votre conformité avec la loi applicable. Les fonctionnalités du produit Adobe Journey Optimizer décrites ci-dessous sont des éléments de base qui, configurés et utilisés de manière appropriée, peuvent prendre en charge une implémentation conforme. Chaque client est responsable de déterminer et de respecter ses obligations en vertu de la loi applicable.

## Vue d’ensemble {#overview}

Le 14 avril 2026, la *Commission Nationale de l&#39;Informatique et des Libertés* (CNIL), autorité française de protection des données, a publié une [recommandation sur l&#39;utilisation des pixels de tracking dans les emails](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf). Ces conseils clarifient le moment où le consentement est requis et soulignent l’importance de bonnes pratiques de consentement pour le suivi des pixels d’e-mail. Cette politique peut avoir un impact sur les pratiques d’envoi pour toute entité diffusant des e-mails aux abonnés basés en France.

La CNIL a prévu un délai de trois mois à compter de la date de la recommandation pour que les entreprises informent leurs destinataires d&#39;emails (« utilisateurs ») de la présence des pixels de tracking, de leur finalité et du droit de désinscription des utilisateurs. Pendant cette période de transition, les clients doivent informer les utilisateurs du suivi des pixels et fournir un droit d’opposition si nécessaire. **La CNIL devrait commencer ses activités d’application après le 14 juillet 2026.**

Alors que la CNIL et d’autres organismes de réglementation clarifient les conseils sur le tracking des pixels et les problèmes associés, Adobe continuera à surveiller les mises à jour et à informer les clients des fonctionnalités techniques des produits Adobe qui prennent en charge le marketing par e-mail, y compris Adobe Journey Optimizer.

Adobe Journey Optimizer fournit des contrôles qui peuvent aider les clients à gérer le suivi des ouvertures au niveau de la diffusion. Il incombe aux clients de déterminer leurs propres obligations de conformité en vertu des conseils de la CNIL et d’autres lois applicables, mais ces fonctionnalités peuvent soutenir les efforts de conformité des clients.

## Qu’est-ce qu’un pixel de tracking e-mail ? {#tracking-pixel}

Un pixel de tracking d’e-mail est une image transparente 1x1 incorporée dans l’HTML d’un e-mail. Lorsque le client de messagerie du destinataire charge cette image, le pixel envoie un ping à un serveur qui enregistre des données telles qu’une date et une heure, un type d’appareil, un client de messagerie et parfois une adresse IP pour un emplacement approximatif. Ce journal est ensuite lié à l’enregistrement d’un destinataire, ce qui permet aux spécialistes marketing de voir si un e-mail est ouvert.

## Service clientèle {#support}

Les clients qui demandent de l’aide pour mettre en œuvre les modifications décrites ci-dessus peuvent interagir avec leur écosystème Adobe existant. Pour toute question technique sur les fonctionnalités Adobe référencées, contactez votre responsable du succès client ou votre gestionnaire de compte technique.

## Fonctionnalité de Adobe Journey Optimizer liée au tracking e-mail {#ajo-functionality}

Adobe Journey Optimizer fournit plusieurs contrôles natifs pour aider les clients à répondre aux éléments du guide de la CNIL. Les sections ci-dessous décrivent les fonctionnalités pertinentes du produit.

### Classification de type d&#39;email {#email-type}

Dans Adobe Journey Optimizer, chaque configuration de canal e-mail est classée comme marketing ou transactionnel. Cette classification détermine si le consentement de l’abonné est requis avant l’envoi.

* **E-mails marketing** : communications promotionnelles envoyées aux abonnés inscrits. Le consentement de l’utilisateur est requis. Ces e-mails respectent automatiquement les préférences de suppression et de désinscription.
* **E-mails transactionnels** : communications non commerciales (par exemple, confirmations de commande, réinitialisations de mot de passe). Elles peuvent être envoyées aux profils qui se sont désabonnés des communications marketing, sous réserve de la loi applicable.

Le type d’e-mail est défini au niveau de la [configuration du canal](../email/email-settings.md#email-type). Lors de la création d’un e-mail dans un parcours ou une campagne, les auteurs doivent sélectionner une configuration de canal dont le type d’e-mail correspond à la nature de la communication. Cette classification indique les contrôles de consentement appliqués avant la diffusion.

### Ouvrir les contrôles de tracking {#open-tracking}

Adobe Journey Optimizer permet aux spécialistes marketing de contrôler le suivi des ouvertures (c’est-à-dire le pixel 1x1) au niveau des messages individuels. Lors de la création d’un e-mail dans un parcours ou une campagne, deux options de tracking sont disponibles dans le panneau des propriétés du message :

* **[!UICONTROL Ouvertures d’e-mails]** : contrôle si le pixel de suivi d’ouverture est inclus dans l’e-mail. Cette option est activée par défaut.
* **[!UICONTROL Clics sur l’e-mail]** : contrôle le suivi des clics sur les liens. Cette option est également activée par défaut.

Pour désactiver le suivi des ouvertures pour un e-mail spécifique, désélectionnez l’option **[!UICONTROL Ouvertures d’e-mails]** lors de la création de votre message. Lorsqu’elle est désactivée, cette option empêche la collecte des données de suivi des ouvertures pour cette diffusion. Pour les organisations qui envoient des messages à des abonnés français, passez en revue les paramètres de suivi des ouvertures pour tous les parcours et campagnes actifs avant la date d’application.

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
Clarify whether unchecking "Email opens" fully removes the 1x1 tracking pixel from the delivered HTML, or whether the pixel is still present in the HTML but open data is suppressed at the data processing layer only. The current wording ("prevents open tracking data from being collected") is intentionally neutral. If the pixel is removed: update to state this explicitly. If the pixel remains but data is not processed: reword to make that distinction clear, to avoid misleading customers seeking CNIL compliance.
-->

[Découvrez comment suivre vos messages](../email/message-tracking.md)

### Gestion du suivi au niveau des liens {#link-tracking}

Au-delà du bouton (bascule) de suivi des ouvertures par message, Adobe Journey Optimizer Email Designer offre un contrôle granulaire sur les URL suivies. À l’aide du panneau **[!UICONTROL Liens]** dans le Designer d’e-mail, les auteurs peuvent afficher toutes les URL suivies dans un message et définir le mode de suivi pour chaque lien individuellement.

Les modes de suivi disponibles pour chaque lien sont les suivants :

* **Tracké** : active le tracking sur cette URL.
* **Opt-out** : désigne cette URL en tant qu’URL d’opt-out ou de désabonnement.
* **Page miroir** : désigne cette URL en tant que lien de page miroir.
* **Jamais** : le tracking n’est jamais activé pour cette URL, quels que soient les paramètres au niveau du message.

La définition de liens spécifiques sur **Jamais** peut vous assurer que certaines URL ne sont pas suivies, même lorsque le suivi au niveau des messages est activé.

[Découvrez comment gérer le tracking dans le Designer d’e-mail](../email/message-tracking.md#manage-tracking)

### Capture et gestion du consentement {#consent-management}

Adobe Journey Optimizer gère le consentement par le biais du [schéma de consentement et de préférences](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=fr){target="_blank"} de Adobe Experience Platform (AEP). Les préférences de consentement sont stockées au niveau du profil et automatiquement appliquées lors du parcours et de l’exécution de la campagne.

Les principaux attributs de consentement relatifs au suivi des e-mails sont les suivants :

* **`consents.marketing.email.val`** : champ principal de consentement au marketing par e-mail. Une valeur `y` indique opt-in ; `n` indique opt-out. Une valeur vide est traitée comme un consentement par défaut (cette valeur par défaut peut être modifiée lors de l’intégration).

### Mécanismes d&#39;opt-out et de retrait {#opt-out}

Adobe Journey Optimizer offre plusieurs mécanismes permettant aux abonnés de se désabonner des communications et de gérer leurs préférences. Tous mettent à jour les attributs de consentement du profil dans Adobe Experience Platform.

**Désabonnement en un clic (en-tête de l’e-mail)**

Lorsque l’option **[!UICONTROL Activer List-Unsubscribe]** est activée dans la configuration du canal e-mail, une URL de désabonnement en un clic et une adresse e-mail sont automatiquement ajoutées à l’en-tête de l’e-mail. Les destinataires peuvent se désabonner directement de leur client de messagerie sans cliquer dans le corps de l’e-mail. Cette option est activée par défaut pour les nouvelles configurations de canal.

[Découvrez comment configurer List-Unsubscribe](../email/list-unsubscribe.md)

**Désinscription en un clic (corps de l’e-mail)**

Les auteurs peuvent insérer un lien de désinscription en un clic directement dans le contenu de l’e-mail à l’aide du Designer d’e-mail. Lorsqu&#39;un destinataire clique sur ce lien, sa préférence est mise à jour immédiatement. Le processus d’opt-out peut être défini de l’une des manières suivantes :

* **Niveau du canal** : exclut le profil de toutes les futures communications par e-mail via le canal.
* **Niveau d’identité** : exclut uniquement l’adresse e-mail spécifique utilisée dans le message actuel.

[Découvrez comment ajouter un lien de désinscription en un clic](../email/email-opt-out.md#one-click-opt-out)

**Centre de préférences via les landing pages**

La fonctionnalité de page de destination native de Adobe Journey Optimizer permet aux entreprises de créer des centres de préférences où les abonnés peuvent gérer leurs préférences de communication et de suivi. Lorsqu’un abonné envoie un formulaire de centre de préférences, ses choix sont réécrits sur leurs attributs de profil AEP dans le groupe de champs Consentement et préférences .

Pour les scénarios de conformité à la CNIL, une page de destination du centre de préférences peut être liée à partir du pied de page de l&#39;e-mail (distinct du lien de désabonnement) afin que les destinataires puissent gérer leurs préférences de tracking indépendamment de leur statut d&#39;abonnement.

[Découvrez comment gérer les préférences de vos clients](../action/preference-center.md)

### Traitement et application du consentement {#consent-enforcement}

Lorsqu’un destinataire se désinscrit par l’un des mécanismes ci-dessus, les événements suivants se produisent :

* L’attribut de consentement du profil (`consents.marketing.email.val`) est remplacé par `n` dans Adobe Experience Platform.
* Le profil est immédiatement exclu des futurs envois d’e-mails marketing dans les parcours et les campagnes.
* Les informations concernant les désinscriptions sont stockées dans le jeu de données du service de consentement AEP.
* Journey Optimizer effectue une vérification du consentement au niveau du canal avant chaque envoi, en s’assurant que les profils désinscrits ne reçoivent pas de communications marketing.

[En savoir plus sur la gestion des désinscriptions](opt-out.md)

### Politiques de consentement {#consent-policies}

Les entreprises peuvent créer et appliquer des politiques de consentement dans Adobe Journey Optimizer afin de s’assurer que seuls les profils répondant à des critères de consentement spécifiques reçoivent des communications. Les politiques de consentement peuvent être associées aux configurations de canal via des actions marketing.

[Découvrez comment utiliser les politiques de consentement.](../action/consent.md)

### Liste de suppression et re-sollicitation {#suppression}

Adobe Journey Optimizer gère automatiquement une liste de suppression qui inclut les adresses e-mail entraînant des hard bounces, des soft bounces ou des plaintes contre le spam. Les profils de la liste de suppression sont exclus des futurs envois marketing.

L’API REST de suppression Journey Optimizer fournit un contrôle programmatique supplémentaire sur les messages sortants, ce qui permet aux entreprises de gérer le comportement de suppression et de place sur la liste autorisée via l’API.

[Découvrez comment gérer la liste de suppression](../configuration/manage-suppression-list.md)

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
AJO has no native equivalent of Campaign v8's "lastPixelRefusalDate" field or re-solicitation typology rule. If re-solicitation governance for pixel consent refusal is required, customers would likely need to: (a) create a custom XDM date field to capture the pixel refusal date, and (b) build an AEP audience that filters out profiles where that date falls within the last six months, then use that audience as a suppression filter in campaigns/journeys. Confirm with Engineering: (1) whether this guidance should be included in this article, and (2) whether any native AJO improvements are planned in this area.
-->

### Création de rapports {#reporting}

Le reporting sur les e-mails de Adobe Journey Optimizer fournit des mesures d’ouverture et de clic via les rapports [dynamiques](../reports/live-report.md) et [rapports Customer Journey Analytics](../reports/report-gs-cja.md). Lorsque le suivi **[!UICONTROL Ouvertures d’e-mails]** est désactivé pour un message, les données ouvertes ne sont pas collectées pour cette diffusion ; les rapports ne reflètent que les clics et d’autres signaux d’engagement.

