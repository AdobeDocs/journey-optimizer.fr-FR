---
title: Configurer les paramètres d’e-mail
description: Découvrez comment configurer les paramètres de courrier électronique au niveau de la surface du canal
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 8766f64c4ea7985c6c9d6e4ba022ef6b1fc0dbed
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 63%

---

# Configurer les paramètres d’e-mail {#email-settings}

Définissez les paramètres de l&#39;email dans la section dédiée de la surface du canal (c&#39;est-à-dire la configuration du paramètre prédéfini du message). Découvrez comment créer des surfaces dans [cette section](channel-surfaces.md).

![](assets/preset-email-settings.png)

## Type d’e-mail {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Définition de la catégorie d’e-mail"
>abstract="Sélectionnez le type de message qui sera envoyé lors de l&#39;utilisation de cette surface : Marketing pour les messages promotionnels, qui nécessitent un consentement de l’utilisateur, ou Transactionnel pour les messages non commerciaux, qui peuvent également être envoyés aux profils désabonnés dans des contextes spécifiques."

Dans le **TYPE D&#39;EMAIL** , sélectionnez le type de message qui sera envoyé avec la surface : **Marketing** ou **Transactionnel**.

* Choisir **Marketing** pour un email promotionnel : ces messages requièrent le consentement de l’utilisateur.

* Choisir **Transactionnel** pour les emails non commerciaux tels que la confirmation de commande, les notifications de réinitialisation de mot de passe ou les informations de diffusion, par exemple.

>[!CAUTION]
>
>**Transactionnel** les emails peuvent être envoyés aux profils qui se sont désabonnés des communications marketing. Ces messages ne peuvent être envoyés que dans des contextes spécifiques.

When [créer un message](../messages/get-started-content.md#create-new-message), vous devez choisir une surface de canal valide correspondant à la catégorie que vous avez sélectionnée pour votre email.

## Sous-domaine et groupes d’adresses IP {#subdomains-and-ip-pools}

Dans la section **DÉTAILS DU SOUS-DOMAINE ET DU GROUPE DʼADRESSES IP**, vous devez effectuer les actions suivantes :

1. Sélectionnez le sous-domaine à utiliser pour envoyer les e-mails. [En savoir plus](about-subdomain-delegation.md)

1. Sélectionnez le pool d’adresses IP à associer à la surface. [En savoir plus](ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

Vous ne pouvez pas poursuivre la création de surface lorsque le pool IP sélectionné se trouve sous [edition](ip-pools.md#edit-ip-pool) (**[!UICONTROL Traitement]** (status) et n’a jamais été associé au sous-domaine sélectionné. Sinon, la version la plus ancienne de l’association groupe d’adresses IP/sous-domaine sera toujours utilisée. Si c’est le cas, enregistrez la surface en tant que brouillon et réessayez une fois que le pool IP a la valeur **[!UICONTROL Succès]** statut.

>[!NOTE]
>
>Pour les environnements hors production, Adobe ne crée pas de sous-domaines de test d’usine et n’accorde pas l’accès à un groupe d’adresses IP d’envoi partagé. Vous devez [déléguer vos propres sous-domaines](delegate-subdomain.md) et utiliser les adresses IP du groupe affecté à votre organisation.

## List-Unsubscribe {#list-unsubscribe}

Si vous choisissez [sélection d&#39;un sous-domaine](#subdomains-and-ip-pools) dans la liste, l&#39;option **[!UICONTROL Activer List-Unsubscribe]** s&#39;affiche.

![](assets/preset-list-unsubscribe.png)

Cette option est affichée par défaut.

Si vous la laissez activée, un lien de désabonnement sera automatiquement inclus dans l&#39;en-tête de l&#39;e-mail, par exemple :

![](assets/preset-list-unsubscribe-header.png)

Si vous désactivez cette option, aucun lien de désabonnement ne s&#39;affichera dans l&#39;en-tête de l&#39;e-mail.

Le lien de désabonnement se compose de deux éléments :

* Une **adresse e-mail de désabonnement**, à laquelle toutes les requêtes de désabonnement sont envoyées.

   Dans [!DNL Journey Optimizer], l’adresse électronique de désabonnement est la valeur par défaut. **[!UICONTROL Mailto (unsubscribe)]** adresse affichée à la surface du canal, en fonction de la variable [sous-domaine sélectionné](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* L&#39;**URL de désabonnement**, qui est l&#39;URL de la page de destination vers laquelle l&#39;utilisateur sera redirigé une fois désabonné.

   Si vous ajoutez une [lien d’exclusion en un clic](../messages/consent.md#one-click-opt-out) pour un message créé à partir de cette surface, l&#39;URL de désabonnement sera l&#39;URL définie pour le lien de désinscription en un clic.

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >Si vous n&#39;ajoutez pas de lien de désinscription en un clic dans le contenu de votre message, aucune page de destination ne sera affichée pour l&#39;utilisateur.

Apprenez-en davantage sur l&#39;ajout d’un lien de désinscription dans l&#39;en-tête de vos messages dans [cette section](../messages/consent.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## Paramètres d’en-tête{#email-header}

Dans le **[!UICONTROL PARAMÈTRES D’EN-TÊTE]** , renseignez les noms et adresses email de l&#39;expéditeur associés au type d&#39;emails envoyés à partir de cette surface.

>[!CAUTION]
>
>Les adresses e-mail doivent utiliser le [sous-domaine délégué](about-subdomain-delegation.md) actuellement sélectionné.

* **[!UICONTROL Nom de l’expéditeur]** : le nom de l&#39;expéditeur, tel que le nom de votre marque.

* **[!UICONTROL E-mail de l&#39;expéditeur]** : adresse e-mail que vous souhaitez utiliser pour vos communications. Par exemple, si le sous-domaine délégué est *marketing.luma.com*, vous pouvez utiliser *contact@marketing.luma.com*.

* **[!UICONTROL Répondre à (nom)]** : le nom qui sera utilisé lorsque le destinataire clique sur le bouton **Répondre** de son logiciel de messagerie.

* **[!UICONTROL Répondre à (e-mail)]** : adresse e-mail qui sera utilisée lorsque le destinataire clique sur le bouton **Répondre** de son logiciel de messagerie. Vous devez utiliser une adresse définie sur le sous-domaine délégué (par exemple, *reply@marketing.luma.com*), sinon les e-mails seront ignorés.

* **[!UICONTROL Message d’erreur]** : toutes les erreurs générées par les FAI après quelques jours de diffusion de l’e-mail (bounces asynchrones) sont reçues sur cette adresse.

![](assets/preset-header.png)

>[!NOTE]
>
>Les adresses doivent commencer par une lettre (A-Z) et ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait dʼunion `-`.

### Transférer un e-mail {#forward-email}

Si vous souhaitez transférer vers une adresse e-mail spécifique tous les e-mails reçus par [!DNL Journey Optimizer] pour le sous-domaine délégué, contactez l’Assistance clientèle d’Adobe. Vous devrez fournir les éléments suivants :

* Adresse e-mail de transfert de votre choix. Notez que le domaine de l’adresse e-mail de transfert ne peut correspondre à aucun sous-domaine délégué à Adobe.
* Nom de votre sandbox.
* Nom de la surface pour laquelle l’adresse email de transfert sera utilisée.
* La variable **[!UICONTROL Répondre à (email)]** adresse définie au niveau de la surface du canal.

>[!NOTE]
>
>Il ne peut y avoir qu’une seule adresse e-mail de transfert par sous-domaine. Par conséquent, si plusieurs surfaces utilisent le même sous-domaine, la même adresse électronique doit être utilisée pour toutes.

L’adresse e-mail de transfert sera configurée par Adobe. Cela peut prendre 3 à 4 jours.

## E-mail Cci {#bcc-email}

Vous pouvez envoyer une copie identique (ou une copie carbone invisible) des e-mails envoyés par [!DNL Journey Optimizer] vers une boîte de réception Cci où ils seront stockés à des fins de conformité ou d’archivage.

Pour ce faire, activez l’option **[!UICONTROL EMAIL Cci]** fonctionnalité facultative au niveau de la surface du canal. [En savoir plus](bcc-email.md)

![](assets/preset-bcc.png)

## Paramètres de reprise de lʼe-mail {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="Réglage de la période de reprise"
>abstract="Les reprises sont effectuées pendant 3,5 jours (84 heures) lorsqu’une diffusion email échoue en raison d’une erreur de soft bounce temporaire. Vous pouvez ajuster cette période de reprise par défaut en fonction de vos besoins."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/monitor-reputation/retries.html?lang=fr" text="À propos des reprises"

Vous pouvez configurer la variable **PARAMÈTRES DE REPRISE D’EMAIL**.

![](assets/preset-retry-parameters.png)

Par défaut, la [période de reprise](retries.md#retry-duration) est définie sur 84 heures, mais vous pouvez ajuster ce paramètre pour mieux l’adapter à vos besoins.

Vous devez saisir une valeur entière (en heures ou minutes) dans la plage suivante :

* Pour les e-mails marketing, la période de reprise minimale est de 6 heures.
* Pour les e-mails transactionnels, la période de reprise minimale est de 10 minutes.
* Pour les deux types d’e-mail, la période de reprise maximale est de 84 heures (soit 5 040 minutes).

En savoir plus sur les reprises dans [cette section](retries.md).

## Tracking des URL {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="Définir les paramètres de tracking d’URL"
>abstract="Cette section décrit comment ajouter automatiquement des paramètres de tracking aux URL présentes dans votre contenu d’e-mail. Cette fonctionnalité est facultative."

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="Prévisualiser les paramètres de tracking d’URL"
>abstract="Prévisualisez comment les paramètres de tracking seront ajoutés aux adresses URL présentes dans votre contenu d’e-mail."

Vous pouvez utiliser **[!UICONTROL PARAMÈTRES DE SUIVI DES URL]** pour mesurer l’efficacité de vos efforts marketing sur l’ensemble des canaux. Cette fonctionnalité est facultative.

Les paramètres définis dans cette section seront ajoutés à la fin des URL incluses dans le contenu de votre e-mail. Vous pouvez ensuite capturer ces paramètres dans des outils d’analyse web tels qu’Adobe Analytics ou Google Analytics, et créer divers rapports de performances.

![](assets/preset-url-tracking.png)

Trois paramètres de suivi d’URL sont automatiquement renseignés par exemple lorsque vous créez une surface de canal. Vous pouvez les modifier et ajouter jusqu’à 10 paramètres de tracking à l’aide du bouton **[!UICONTROL Ajouter un nouveau paramètre]**.

Pour configurer un paramètre de tracking d’URL, vous pouvez saisir directement les valeurs souhaitées dans les champs **[!UICONTROL Nom]** et **[!UICONTROL Valeur]**.

<!--You can also choose from a list of predefined values by navigating to the following objects:
* Journey attributes: **Source id**, **Source name**, **Source version id**
* Action attributes: **Action id**, **Action name**
* Offer decisioning attributes: **Offer id**, **Offer name**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>Do not select a folder: make sure to browse to the necessary folder and select a profile attribute to use as a tracking parameter value.-->

Vous pouvez également modifier chaque **[!UICONTROL Valeur]** à l’aide du champ [Éditeur d’expression](../personalization/personalization-build-expressions.md). Cliquez sur l’icône d’édition pour ouvrir l’éditeur. De là, vous pouvez sélectionner les attributs contextuels de votre choix et/ou modifier directement le texte.

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