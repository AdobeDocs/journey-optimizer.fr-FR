---
solution: Journey Optimizer
product: journey optimizer
title: Configurer les paramètres d’e-mail
description: Découvrez comment configurer les paramètres d’e-mail au niveau de la surface de canal
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: e7add9627a9938b861ddbcc40f168f41c871119b
workflow-type: tm+mt
source-wordcount: '1433'
ht-degree: 100%

---

# Configurer les paramètres d’e-mail {#email-settings}

Pour commencer à créer un e-mail, vous devez configurer les surfaces du canal e-mail qui définissent tous les paramètres techniques requis pour vos messages. [Découvrez comment créer des surfaces](../configuration/channel-surfaces.md).

Définissez les paramètres d’e-mail dans la section dédiée de la configuration de la surface du canal.

![](assets/preset-email-settings.png)

La configuration de surface d’e-mail est récupérée pour envoyer des communications en suivant la logique ci-dessous :

* Pour les parcours par lots et en rafale, cela ne s’applique pas à l’exécution par lots ou en rafale qui avait déjà démarré avant que la configuration de surface d’e-mail ne soit effectuée. La modification sera récupérée lors de la prochaine périodicité ou de la nouvelle exécution.

* Pour les messages transactionnels, la modification est immédiatement récupérée pour la communication suivante (délai de cinq minutes maximum).

>[!NOTE]
>
>Les paramètres de surface d’e-mail mis à jour seront automatiquement récupérés dans le(s) parcours ou campagne(s) où la surface est utilisée.

## Type d’e-mail {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Définition de la catégorie d’e-mail"
>abstract="Sélectionnez le type d’e-mails qui sera envoyé lors de l’utilisation de cette surface : Marketing pour les messages promotionnels, qui nécessitent le consentement de l’utilisateur, ou Transactionnel pour les messages non commerciaux, qui peuvent également être envoyés aux profils désabonnés dans des contextes spécifiques."

Dans la section **TYPE DʼE-MAIL**, sélectionnez le type de message à envoyer grâce à la surface : **Marketing** ou **Transactionnel**.

* Choisissez **Marketing** pour les e-mails promotionnels : ces messages nécessitent le consentement de l’utilisateur.

* Choisissez **Transactionnel** pour les e-mails non commerciaux tels que les confirmations de commande, les notifications de réinitialisation de mot de passe ou les informations de diffusion, par exemple.

>[!CAUTION]
>
>Les e-mails **transactionnels** peuvent être envoyés aux profils qui se sont désabonnés des communications marketing. Ces messages ne peuvent être envoyés que dans des contextes spécifiques.

Lors de la création d’un message, vous devez choisir une surface de canal valide correspondant à la catégorie que vous avez sélectionnée pour votre e-mail.

## Sous-domaine et groupes d’adresses IP {#subdomains-and-ip-pools}

Dans la section **Sous-domaine et groupes d’adresses IP**, vous devez effectuer les actions suivantes :

1. Sélectionnez le sous-domaine à utiliser pour envoyer les e-mails. [En savoir plus](../configuration/about-subdomain-delegation.md)

1. Sélectionnez le groupe d’adresses IP à associer à la surface. [En savoir plus](../configuration/ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

Vous ne pouvez pas poursuivre la création de la surface lorsque le groupe d’adresses IP sélectionné est en cours d’[édition](../configuration/ip-pools.md#edit-ip-pool) (statut **[!UICONTROL Traitement en cours]**) et n’a jamais été associé au sous-domaine sélectionné. Sinon, la version la plus ancienne de l’association groupe d’adresses IP/sous-domaine sera toujours utilisée. Si c’est le cas, enregistrez la surface en tant que brouillon, puis réessayez une fois que le groupe d’adresses IP a le statut **[!UICONTROL Succès]**.

>[!NOTE]
>
>Pour les environnements hors production, Adobe ne crée pas de sous-domaines de test d’usine et n’accorde pas l’accès à un groupe d’adresses IP d’envoi partagé. Vous devez [déléguer vos propres sous-domaines](../configuration/delegate-subdomain.md) et utiliser les adresses IP du groupe affecté à votre organisation.

## List-Unsubscribe {#list-unsubscribe}

Si vous choisissez [sélection d&#39;un sous-domaine](#subdomains-and-ip-pools) dans la liste, l&#39;option **[!UICONTROL Activer List-Unsubscribe]** s&#39;affiche.

![](assets/preset-list-unsubscribe.png)

Cette option est affichée par défaut.

Si vous la laissez activée, un lien de désabonnement sera automatiquement inclus dans l&#39;en-tête de l&#39;e-mail, par exemple :

![](assets/preset-list-unsubscribe-header.png)

Si vous désactivez cette option, aucun lien de désabonnement ne s&#39;affichera dans l&#39;en-tête de l&#39;e-mail.

Le lien de désabonnement se compose de deux éléments :

* Une **adresse e-mail de désabonnement**, à laquelle toutes les requêtes de désabonnement sont envoyées.

   Dans [!DNL Journey Optimizer], l’adresse e-mail de désabonnement est l’adresse par défaut **[!UICONTROL Mailto (unsubscribe)]** affichée dans la surface de canal, en fonction du [sous-domaine sélectionné](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* L’**URL de désabonnement**, qui est l’URL de la page de destination vers laquelle l’utilisateur sera redirigé une fois désabonné.

   Si vous ajoutez un [lien d&#39;opt-out en un clic](../privacy/opt-out.md#one-click-opt-out) pour un message créé à l’aide de cette surface, l’URL de désabonnement sera l&#39;URL définie pour le lien d&#39;opt-out en un clic.

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >Si vous n&#39;ajoutez pas de lien d&#39;opt-out en un clic dans le contenu de votre message, aucune page de destination ne sera affichée pour l&#39;utilisateur.

Apprenez-en davantage sur l&#39;ajout d’un lien de désinscription dans l&#39;en-tête de vos messages dans [cette section](../privacy/opt-out.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## Paramètres d’en-tête {#email-header}

Dans la section **[!UICONTROL Paramètres d’en-tête]**, saisissez les noms d’expéditeur et les adresses e-mail associées au type d’e-mails envoyés à l’aide de cette surface.

* **[!UICONTROL Nom de l’expéditeur ou de l’expéditrice]** : le nom de l’expéditeur ou de l’expéditrice, tel que le nom de votre marque.

* **[!UICONTROL E-mail de l’expéditeur]** : adresse e-mail que vous souhaitez utiliser pour vos communications.

* **[!UICONTROL Répondre à (nom)]** : le nom qui sera utilisé lorsque le destinataire clique sur le bouton **Répondre** de son logiciel de messagerie.

* **[!UICONTROL Répondre à (e-mail)]** : adresse e-mail qui sera utilisée lorsque le destinataire clique sur le bouton **Répondre** de son logiciel de messagerie. [En savoir plus](#reply-to-email)

* **[!UICONTROL Message d’erreur]** : toutes les erreurs générées par les FAI après quelques jours de diffusion de l’e-mail (bounces asynchrones) sont reçues sur cette adresse.

>[!CAUTION]
>
>Les adresses **[!UICONTROL e-mail expéditeur]** et **[!UICONTROL e-mail d’erreur]** doivent utiliser le [sous-domaine délégué](../configuration/about-subdomain-delegation.md) actuel. Par exemple, si le sous-domaine délégué est *marketing.luma.com*, vous pouvez utiliser *contact@marketing.luma.com* et *error@marketing.luma.com*.

![](assets/preset-header.png)

>[!NOTE]
>
>Les adresses doivent commencer par une lettre (A-Z) et ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait dʼunion `-`.

### Adresse e-mail de réponse {#reply-to-email}

Lors de la définition de l’adresse **[!UICONTROL Répondre à (e-mail)]**, vous pouvez indiquer toute adresse e-mail à condition qu’il s’agisse d’une adresse valide, au format approprié et sans erreur de frappe.

Pour assurer une bonne gestion des réponses, procédez comme suit :

* La boîte de réception utilisée pour les réponses reçoit tous les e-mails de réponse, y compris les notifications d’absence du bureau et les challenge-réponses, afin de vous assurer que vous avez mis en place un processus manuel ou automatisé pour traiter les e-mails entrant dans cette boîte de réception.

* Assurez-vous que la boîte de réception dédiée dispose de suffisamment de capacité pour recevoir tous les e-mails de réponse envoyés à l’aide de la surface d’e-mail. Si la boîte de réception renvoie des rebonds, il se peut que certaines réponses de vos clients ne soient pas reçues.

* Les réponses doivent être traitées en tenant compte des obligations de confidentialité et de conformité, car elles peuvent contenir des données à caractère personnel (PII).

* Ne marquez pas les messages comme spam dans la boîte de réception de réponse, car cela aura un impact sur tous les autres e-mails envoyés à cette adresse.

### Transférer un e-mail {#forward-email}

Si vous souhaitez transférer vers une adresse e-mail spécifique tous les e-mails reçus par [!DNL Journey Optimizer] pour le sous-domaine délégué, contactez l’Assistance clientèle d’Adobe. Vous devrez fournir les éléments suivants :

* Adresse e-mail de transfert de votre choix. Notez que le domaine de l’adresse e-mail de transfert ne peut correspondre à aucun sous-domaine délégué à Adobe.
* Nom de votre sandbox.
* Nom de la surface pour laquelle l’adresse e-mail de transfert sera utilisée.
* L’adresse **[!UICONTROL Répondre à (e-mail)]** actuelle définie au niveau de la surface de canal.

>[!NOTE]
>
>Il ne peut y avoir qu’une seule adresse e-mail de transfert par sous-domaine. Par conséquent, si plusieurs surfaces utilisent le même sous-domaine, la même adresse e-mail de transfert doit être utilisée pour tous les sous-domaines.

L’adresse e-mail de transfert sera configurée par Adobe. Cela peut prendre 3 à 4 jours.

## E-mail Cci {#bcc-email}

Vous pouvez envoyer une copie identique (ou une copie carbone invisible) des e-mails envoyés par [!DNL Journey Optimizer] vers une boîte de réception Cci où ils seront stockés à des fins de conformité ou d’archivage.

Pour ce faire, activez la fonctionnalité **[!UICONTROL E-mail Cci]** au niveau de la surface de canal. [En savoir plus](../configuration/archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

## Paramètres de reprise de lʼe-mail {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="Réglage de la période de reprise"
>abstract="Les reprises sont effectuées pendant 3,5 jours (84 heures) lorsqu’une diffusion d’e-mail échoue en raison d’une erreur de soft bounce temporaire. Vous pouvez ajuster cette période de reprise par défaut en fonction de vos besoins."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/retries.html?lang=fr" text="À propos des reprises"

Vous pouvez configurer les **Paramètres de reprise de lʼe-mail**.

![](assets/preset-retry-parameters.png)

Par défaut, la [période de reprise](../configuration/retries.md#retry-duration) est définie sur 84 heures, mais vous pouvez ajuster ce paramètre pour mieux l’adapter à vos besoins.

Vous devez saisir une valeur entière (en heures ou minutes) dans la plage suivante :

* Pour les e-mails marketing, la période de reprise minimale est de 6 heures.
* Pour les e-mails transactionnels, la période de reprise minimale est de 10 minutes.
* Pour les deux types d’e-mail, la période de reprise maximale est de 84 heures (soit 5 040 minutes).

En savoir plus sur les reprises dans [cette section](../configuration/retries.md).

## Tracking des URL {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Définir les paramètres de tracking d’URL"
>abstract="Cette section décrit comment ajouter automatiquement des paramètres de tracking aux URL présentes dans votre contenu d’e-mail. Cette fonctionnalité est facultative."

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="Prévisualiser les paramètres de tracking d’URL"
>abstract="Prévisualisez comment les paramètres de tracking seront ajoutés aux adresses URL présentes dans votre contenu d’e-mail."

Vous pouvez utiliser les **[!UICONTROL paramètres de tracking d’URL]** pour mesurer l’efficacité de vos efforts marketing sur l’ensemble des canaux. Cette fonctionnalité est facultative.

Les paramètres définis dans cette section seront ajoutés à la fin des URL incluses dans le contenu de votre e-mail. Vous pouvez ensuite capturer ces paramètres dans des outils d’analyse web tels qu’Adobe Analytics ou Google Analytics, et créer divers rapports de performances.

<!--Three URL tracking parameters are auto-populated as an example when you create a channel surface. You can edit these and add up to 10 tracking parameters using the **[!UICONTROL Add new parameter]** button.-->

Vous pouvez ajouter jusqu’à 10 paramètres de tracking à l’aide du bouton **[!UICONTROL Ajouter un nouveau paramètre]**.

![](assets/preset-url-tracking.png)

Pour configurer un paramètre de tracking d’URL, vous pouvez saisir directement les valeurs souhaitées dans les champs **[!UICONTROL Nom]** et **[!UICONTROL Valeur]**.

<!--You can also choose from a list of predefined values by navigating to the following objects:
* Journey attributes: **Source id**, **Source name**, **Source version id**
* Action attributes: **Action id**, **Action name**
* Offer decisioning attributes: **Offer id**, **Offer name**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>Do not select a folder: make sure to browse to the necessary folder and select a profile attribute to use as a tracking parameter value.-->

Vous pouvez également modifier chaque champ **[!UICONTROL Valeur]** à l’aide de l’[Éditeur d’expression](../personalization/personalization-build-expressions.md). Cliquez sur l’icône d’édition pour ouvrir l’éditeur. De là, vous pouvez sélectionner les attributs contextuels de votre choix et/ou modifier directement le texte.

![](assets/preset-url-tracking-editor.png)

>[!NOTE]
>
>Vous pouvez combiner des valeurs de texte de saisie et utiliser des attributs contextuels à partir de l’éditeur d’expression. Chaque champ **[!UICONTROL Valeur]** peut contenir jusqu’à 255 caractères au total.

<!--You can drag and drop the parameters to reorder them.-->

Vous trouverez ci-dessous des exemples d’URL compatibles avec Adobe Analytics et Google Analytics.

* URL compatible avec Adobe Analytics : `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* URL compatible avec Google Analytics : `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

Vous pouvez prévisualiser de manière dynamique l’URL de tracking obtenue. Chaque fois que vous ajoutez, modifiez ou supprimez un paramètre, la prévisualisation est automatiquement mise à jour.

![](assets/preset-url-tracking-preview.png)