---
solution: Journey Optimizer
product: journey optimizer
title: Suivre vos messages
description: Découvrez comment ajouter des liens et suivre les messages envoyés
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: liens, tracking, surveillance, e-mail
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 100%

---

# Ajouter des liens et suivre les messages {#tracking}

Utilisez [!DNL Journey Optimizer] pour ajouter des liens à votre contenu et suivre les messages envoyés afin de surveiller le comportement de vos destinataires.

## Activation du suivi {#enable-tracking}

Vous pouvez activer le tracking au niveau des e-mails en cochant les options **[!UICONTROL Ouvertures d’e-mails]** et/ou **[!UICONTROL Cliquer sur l’e-mail]** lorsque vous créez votre message dans un parcours ou une campagne.

>[!BEGINTABS]

>[!TAB Activer le tracking dans un parcours]

![](assets/message-tracking-journey.png)

>[!TAB Activer le tracking dans une campagne]

![](assets/message-tracking-campaign.png)

>[!ENDTABS]

>[!NOTE]
>
>Les deux options sont activées par défaut.

Vous pourrez ainsi suivre le comportement de vos destinataires via :

* **[!UICONTROL Ouvertures d’e-mails]** : messages ayant été ouverts.
* **[!UICONTROL Clics sur l&#39;e-mail]** : clics sur les liens dans un e-mail.

## Insertion de liens {#insert-links}

Lors de la conception d&#39;un message, vous pouvez ajouter des liens à votre contenu.

>[!NOTE]
>
>Lorsque le [suivi est activé](#enable-tracking), tous les liens inclus dans le contenu du message sont suivis.

Pour insérer des liens dans le contenu de votre e-mail, procédez comme suit :

1. Sélectionnez un élément et cliquez sur **[!UICONTROL Ajouter un lien]** dans la barre d&#39;outils contextuelle.

   ![](assets/message-tracking-insert-link.png)

1. Choisissez le type de lien que vous souhaitez créer :

   * **[!UICONTROL Lien externe]** : insérez un lien vers une URL externe.

   * **[!UICONTROL Page de destination]** : insérez un lien vers une page de destination. [En savoir plus](../landing-pages/get-started-lp.md).

   * **[!UICONTROL Opt-out en un clic]** : insérez un lien pour permettre aux utilisateurs et utilisatrices de se désabonner rapidement de vos communications sans avoir à confirmer leur opt-out. [En savoir plus](email-opt-out.md#one-click-opt-out).

   * **[!UICONTROL Abonnement/opt-in externe]** : insérez un lien pour accepter la réception de communications de votre marque.

   * **[!UICONTROL Désabonnement/opt-out externe]** : insérez un lien pour se désabonner de la réception des communications de votre marque. En savoir plus sur la gestion des processus d’opt-out dans [cette section](email-opt-out.md#opt-out-management).

   * **[!UICONTROL Page miroir]** : insérez un lien pour afficher le contenu de l’e-mail dans un navigateur web. [En savoir plus](#mirror-page).

1. Saisissez l’URL de votre choix dans le champ correspondant, ou sélectionnez une page de destination et définissez les styles et paramètres du lien. [En savoir plus](#adjust-links).

   >[!NOTE]
   >
   >Pour interpréter les URL, [!DNL Journey Optimizer] se conforme à la syntaxe URI ([Norme RFC 3986](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}), qui désactive certains caractères internationaux spéciaux dans les URL. Lors de l’envoi du BAT ou de l’e-mail, si une erreur impliquant une URL ajoutée à votre contenu vous est renvoyée, vous pouvez encoder la chaîne comme solution de contournement.

1. Vous pouvez personnaliser vos liens. [En savoir plus](../personalization/personalization-syntax.md#perso-urls).

1. Enregistrez vos modifications.

1. Une fois le lien créé, vous pouvez toujours le modifier à partir des volets **[!UICONTROL Paramètres]** et **[!UICONTROL Styles]** à droite.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>Les e-mails de type marketing doivent inclure un [lien d’exclusion](../privacy/opt-out.md#opt-out-management), qui n’est pas obligatoire pour les messages transactionnels. La catégorie du message (**[!UICONTROL Marketing]** ou **[!UICONTROL Transactionnel]**) est définie au niveau de la [configuration des canaux](../configuration/channel-surfaces.md#email-type), lors de la création du message.

## Ajuster les liens {#adjust-links}

Vous pouvez ajuster vos liens à l’aide des volets **[!UICONTROL Paramètres]** et **[!UICONTROL Styles]** à droite. Vous pouvez souligner un lien, en modifier la couleur ou sélectionner sa cible.

1. Dans un composant **[!UICONTROL Texte]** contenant un lien, sélectionnez ce dernier.

1. Dans l’onglet **[!UICONTROL Paramètres]**, choisissez comment votre audience sera redirigée à l’aide du menu déroulant **[!UICONTROL Cible]** :

   * **[!UICONTROL Aucune]** : ouvre le lien dans le même cadre que celui sur lequel l’utilisateur a cliqué (par défaut).
   * **[!UICONTROL Vierge]** : ouvre le lien dans une nouvelle fenêtre ou un nouvel onglet.
   * **[!UICONTROL Self]** : ouvre le lien dans le même cadre que celui sur lequel l’utilisateur a cliqué.
   * **[!UICONTROL Parent]** : ouvre le lien dans le cadre parent.
   * **[!UICONTROL Haut]** : ouvre le lien dans le corps complet de la fenêtre.

   ![](assets/link_2.png)

1. Cochez la case **[!UICONTROL Souligner le lien]** pour souligner le texte du libellé de votre lien.

   ![](assets/link_1.png)

1. Pour modifier la couleur de votre lien, cliquez sur **[!UICONTROL Couleur du lien]** dans l’onglet **[!UICONTROL Styles]**.

   ![](assets/link_3.png)

1. Enregistrez vos modifications.

## Lien vers une page miroir {#mirror-page}

La page miroir est une page HTML accessible en ligne via un navigateur web. Son contenu est identique à celui de votre e-mail.

Pour ajouter un lien vers une page miroir dans votre e-mail, [insérez un lien](#insert-links) et sélectionnez **[!UICONTROL Page miroir]** comme type de lien.

![](assets/message-tracking-mirror-page.png)

La page miroir est automatiquement créée.

>[!IMPORTANT]
>
>Les liens de pages miroir sont générés automatiquement et ne peuvent pas être modifiés. Ils contiennent toutes les données personnalisées et chiffrées nécessaires pour générer l’e-mail original. Par conséquent, l’utilisation d’attributs personnalisés dotés de valeurs élevées peut générer des URL de pages miroir longues et empêcher le fonctionnement du lien dans les navigateurs web appliquant une longueur maximale d’URL.

Une fois l&#39;e-mail envoyé, lorsque les destinataires cliquent sur le lien de la page miroir, le contenu de l’email s&#39;affiche dans leur navigateur web par défaut.

>[!NOTE]
>
>Dans le [BAT](../content-management/proofs.md) envoyé aux profils de test, le lien vers la page miroir n’est pas actif. Il n&#39;est activé que dans les messages finaux.

La période de conservation d’une page miroir est de 60 jours. Passé ce délai, la page miroir n’est plus disponible.

## Gestion du suivi {#manage-tracking}

Le [Concepteur d&#39;e-mail](content-from-scratch.md) permet de gérer les URL suivies, par exemple modifier le type de suivi pour chaque lien.

1. Cliquez sur l&#39;icône **[!UICONTROL Liens]** du volet de gauche pour afficher la liste de toutes les URL de votre contenu qui feront l&#39;objet d&#39;un suivi.

   Cette liste permet d&#39;avoir une vue centrale et de localiser chaque URL dans le contenu de l&#39;e-mail.

1. Pour modifier un lien, cliquez sur l&#39;icône de crayon correspondante.

1. Si nécessaire, vous pouvez modifier le **[!UICONTROL Type de tracking]** :

   ![](assets/message-tracking-edit-a-link.png)

   Pour chaque URL suivie, vous pouvez définir le mode de tracking sur l&#39;une des valeurs suivantes :

   * **[!UICONTROL Tracké]** : active le tracking sur cette URL.
   * **[!UICONTROL Opt-out]** : considère cette URL comme une option d&#39;opt-out ou une URL de désabonnement.
   * **[!UICONTROL Page miroir]** : considère cette URL comme une URL de page miroir.
   * **[!UICONTROL Jamais]** : n’active jamais le suivi de cette URL.

La création de rapports sur les ouvertures et les clics est disponible dans le [rapport dynamique](../reports/live-report.md) et dans le [rapport global](../reports/global-report.md).

## Personnaliser le suivi des URL {#url-tracking}

Généralement, le [tracking des URL](email-settings.md#url-tracking) est géré au niveau de la configuration, mais les attributs de profil ne sont pas pris en charge. Actuellement, la seule façon de le faire est de [personnaliser les URL](../personalization/personalization-syntax.md#perso-urls) dans le concepteur d’e-mail.

Pour ajouter des paramètres de tracking d’URL personnalisés à vos liens, procédez comme suit.

1. Sélectionnez un lien et cliquez sur **[!UICONTROL Insérer un lien]** dans la barre d’outils contextuelle.

1. Sélectionnez l’icône de personnalisation. Elle nʼest disponible que pour les types de liens suivants : **Lien externe**, **Lien de désinscription** et **Opt-out**.

   ![](assets/message-tracking-insert-link-perso.png)

1. Ajoutez le paramètre de suivi des URL et sélectionnez l’attribut de profil de votre choix dans l’éditeur de personnalisation.

   ![](assets/message-tracking-perso-parameter.png)

1. Enregistrez vos modifications.

1. Répétez les étapes ci-dessus pour chaque lien auquel vous souhaitez ajouter ce paramètre de tracking.

Désormais, lorsque l’e-mail est envoyé, ce paramètre est automatiquement ajouté à la fin de l’URL. Vous pouvez ensuite capturer ce paramètre dans les outils d’analyse web ou dans les rapports de performances.

>[!NOTE]
>
>Pour vérifier l’URL finale, vous pouvez [envoyer un BAT](../content-management/preview-test.md#send-proofs) et cliquer sur le lien dans le contenu de l’e-mail une fois que vous avez reçu le BAT. L’URL doit afficher le paramètre de tracking. Dans l’exemple ci-dessus, l’URL finale est : <https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>.
