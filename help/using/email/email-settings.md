---
solution: Journey Optimizer
product: journey optimizer
title: Configurer les paramètres d’e-mail
description: Découvrez comment configurer les paramètres d’e-mail au niveau de la surface de canal
feature: Surface
topic: Administration
role: Admin
level: Intermediate
keywords: paramètres, e-mail, configuration
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 5e58db84275d78c5248f1d617328799d71bb10d1
workflow-type: tm+mt
source-wordcount: '2258'
ht-degree: 87%

---

# Configurer les paramètres d’e-mail {#email-settings}

Pour commencer à créer un e-mail, vous devez configurer les surfaces du canal e-mail qui définissent tous les paramètres techniques requis pour vos messages. [Découvrez comment créer des surfaces](../configuration/channel-surfaces.md).

Définissez les paramètres d’e-mail dans la section dédiée de la configuration de la surface du canal.

![](assets/preset-email-settings.png)

La configuration de surface d’e-mail est récupérée pour envoyer des communications en suivant la logique ci-dessous :

* Pour les parcours par lots, cela ne s’applique pas à l’exécution par lots qui avait déjà démarré avant que la configuration de surface d’e-mail ne soit effectuée. La modification sera récupérée lors de la prochaine périodicité ou de la nouvelle exécution.

* Pour les messages transactionnels, la modification est immédiatement récupérée pour la communication suivante (délai de cinq minutes maximum).

>[!NOTE]
>
>Les paramètres de surface d’e-mail mis à jour seront automatiquement récupérés dans le(s) parcours ou campagne(s) où la surface est utilisée.

## Type d’e-mail {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="Définition de la catégorie d’e-mail"
>abstract="Sélectionnez le type d’e-mails qui sera envoyé lors de l’utilisation de cette surface : Marketing pour les messages promotionnels, qui nécessitent le consentement de l’utilisateur, ou Transactionnel pour les messages non commerciaux, qui peuvent également être envoyés aux profils désabonnés dans des contextes spécifiques."

Dans la section **Type d’e-mail**, sélectionnez le type de message à envoyer grâce à la surface : **[!UICONTROL Marketing]** ou **[!UICONTROL Transactionnel]**.

* Choisissez **Marketing** pour les e-mails promotionnels, tels que les promotions hebdomadaires pour un magasin de vente au détail. Ces messages requièrent le consentement de l’utilisateur ou de l’utilisatrice.

* Choisissez **Transactionnel** pour les e-mails non commerciaux tels que les confirmations de commande, les notifications de réinitialisation de mot de passe ou les informations de diffusion, par exemple. Ces e-mails peuvent être envoyés aux profils qui **se sont désabonnés** des communications marketing. Ces messages ne peuvent être envoyés que dans des contextes spécifiques.

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

Une fois qu’un groupe d’adresses IP a été sélectionné, les informations PTR sont visibles lorsque vous pointez sur les adresses IP affichées sous la liste déroulante du groupe d’adresses IP. [En savoir plus sur les enregistrements PTR](../configuration/ptr-records.md)

![](assets/email-surface-ptr-record.png)

>[!NOTE]
>
>Si un enregistrement PTR n’est pas configuré, contactez votre représentant(e) Adobe.

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

En outre, lors de la définition de l’adresse **[!UICONTROL Répondre à (e-mail)]**, veillez à utiliser un sous-domaine possédant une configuration d’enregistrement MX valide, sinon le traitement de surface d’e-mail échouera.

Si vous obtenez une erreur lors de l’envoi de la surface d’e-mail, cela signifie que l’enregistrement MX n’est pas configuré pour le sous-domaine de l’adresse que vous avez saisie. Contactez votre administrateur ou administratrice pour configurer l’enregistrement MX correspondant ou utilisez une autre adresse avec une configuration d’enregistrement MX valide.

>[!NOTE]
>
>Si le sous-domaine de l’adresse que vous avez saisie est un domaine qui a été [entièrement délégué](../configuration/delegate-subdomain.md#full-subdomain-delegation) à Adobe, contactez votre gestionnaire de compte Adobe.

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

Pour ce faire, activez la fonctionnalité **[!UICONTROL E-mail Cci]** au niveau de la surface de canal. [En savoir plus](../configuration/archiving-support.md#bcc-email).

![](assets/preset-bcc.png)

En outre, lors de la définition de l’adresse **[!UICONTROL E-mail en Cci]**, veillez à utiliser un sous-domaine possédant une configuration d’enregistrement MX valide, sinon le traitement de surface d’e-mail échouera.

Si vous obtenez une erreur lors de l’envoi de la surface d’e-mail, cela signifie que l’enregistrement MX n’est pas configuré pour le sous-domaine de l’adresse que vous avez saisie. Contactez votre administrateur ou administratrice pour configurer l’enregistrement MX correspondant ou utilisez une autre adresse avec une configuration d’enregistrement MX valide.

## Envoi à des adresses email supprimées {#send-to-suppressed-email-addresses}

>[!CONTEXTUALHELP]
>id="ajo_surface_suppressed_addresses"
>title="Remplacer la priorité de la liste de suppression"
>abstract="Vous pouvez décider d’envoyer des messages transactionnels aux profils même si leurs adresses email se trouvent sur la liste de suppression de Adobe Journey Optimizer en raison d’une plainte de spam. Par défaut, cette option est désactivée."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/manage-suppression-list.html" text="Gérer la liste de suppression"

>[!IMPORTANT]
>
>Cette option n’est disponible que si vous avez sélectionné l’option **[!UICONTROL Transactionnel]** type d’email. [En savoir plus](#email-type)

Dans [!DNL Journey Optimizer], toutes les adresses électroniques marquées comme hard bounces, soft bounces et spams sont automatiquement collectées dans la variable [liste de suppression](../configuration/manage-suppression-list.md) et exclus de l’envoi dans un parcours ou une campagne.

Cependant, vous pouvez décider de poursuivre l’envoi des messages du **transactionnel** saisissez des profils même si leurs adresses email figurent sur la liste de suppression en raison d’une plainte de spam de l’utilisateur.

En effet, les messages transactionnels contiennent généralement des informations utiles et attendues, telles qu’une confirmation de commande ou une notification de réinitialisation de mot de passe. Par conséquent, même s’ils ont signalé l’un de vos messages marketing comme spam, la plupart du temps, vous souhaitez que vos clients reçoivent ce type d’email non commercial.

Pour inclure les adresses électroniques supprimées en raison d’une plainte de spam dans votre audience de message transactionnel, sélectionnez l’option correspondante dans la **[!UICONTROL Envoyer aux adresses email supprimées]** .

![](assets/preset-suppressed-email-addresses.png)

>[!NOTE]
>
>Par défaut, cette option est désactivée.

Cette option est une bonne pratique en matière de délivrabilité. Elle est désactivée par défaut pour garantir que les clients qui se sont désinscrits ne sont pas contactés. Vous pouvez toutefois modifier cette option par défaut, qui vous permet ensuite d’envoyer des messages transactionnels à vos clients.

Une fois cette option activée, bien qu’un client ait marqué votre email marketing comme indésirable, ce client pourra recevoir vos messages transactionnels à l’aide de la surface actuelle. Veillez toujours à gérer les préférences de désinscription conformément aux bonnes pratiques en matière de délivrabilité.

## Liste de contrôle {#seed-list}

>[!CONTEXTUALHELP]
>id="ajo_surface_seed_list"
>title="Ajouter une liste de contrôle"
>abstract="Sélectionnez la liste de contrôle de votre choix pour ajouter automatiquement des adresses internes spécifiques à vos audiences. Ces adresses de contrôle seront incluses au moment de l’exécution de la diffusion et recevront une copie exacte du message à des fins de vérification."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html?lang=fr#use-seed-list" text="Que sont les listes de contrôle ?"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html#create-seed-list" text="Créer des listes de contrôle"


Une liste de contrôle dans [!DNL Journey Optimizer] vous permet d’inclure automatiquement des adresses de contrôle d’e-mail spécifiques dans vos diffusions. [En savoir plus](../configuration/seed-lists.md)

>[!CAUTION]
>
>Actuellement, cette fonctionnalité s’applique uniquement au canal e-mail.

Sélectionnez la liste qui vous intéresse dans la section **[!UICONTROL Liste de contrôle]**. Découvrez comment créer une liste de contrôle dans [cette section](../configuration/seed-lists.md#create-seed-list).

![](../configuration/assets/seed-list-surface.png)

>[!NOTE]
>
>Une seule liste de contrôle peut être sélectionnée à la fois.

Lorsque la surface actuelle est utilisée dans une campagne ou un parcours, les adresses e-mail de la liste de contrôle sélectionnée sont incluses au moment de l’exécution de la diffusion, ce qui signifie qu’elles recevront une copie de la diffusion à des fins de vérification.

Découvrez comment utiliser la liste de contrôle dans une campagne ou un parcours dans [cette section](../configuration/seed-lists.md#use-seed-list).

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

Vous pouvez ajouter jusqu’à 10 paramètres de tracking à l’aide du bouton **[!UICONTROL Ajouter un nouveau paramètre]**.

![](assets/preset-url-tracking.png)

Pour configurer un paramètre de tracking d’URL, vous pouvez saisir directement les valeurs souhaitées dans les champs **[!UICONTROL Nom]** et **[!UICONTROL Valeur]**.

Vous pouvez également modifier chaque champ **[!UICONTROL Valeur]** à l’aide de l’[Éditeur d’expression](../personalization/personalization-build-expressions.md). Cliquez sur l’icône d’édition pour ouvrir l’éditeur. De là, vous pouvez sélectionner les attributs contextuels de votre choix et/ou modifier directement le texte.

![](assets/preset-url-tracking-editor.png)

Les valeurs prédéfinies suivantes sont disponibles via l’éditeur d’expression :

* **ID d’action source** : ID de l’action e-mail ajoutée au parcours ou à la campagne.

* **Nom de l’action source** : nom de l’action e-mail ajoutée au parcours ou à la campagne.

* **ID source** : ID du parcours ou de la campagne avec lequel l’e-mail a été envoyé.

* **Nom de la source** : nom du parcours ou de la campagne avec lequel l’e-mail a été envoyé.

* **ID de la version source** : ID du parcours ou de la version de campagne avec lequel l’e-mail a été envoyé.

* **ID de l’offre** : ID de l’offre utilisée dans l’e-mail.

>[!NOTE]
>
>Vous pouvez combiner des valeurs de texte de saisie et utiliser des attributs contextuels à partir de l’éditeur d’expression. Chaque champ **[!UICONTROL Valeur]** peut contenir un certain nombre de caractères jusqu’à une limite de 5 Ko.

<!--You can drag and drop the parameters to reorder them.-->

Vous trouverez ci-dessous des exemples d’URL compatibles avec Adobe Analytics et Google Analytics.

* URL compatible avec Adobe Analytics : `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* URL compatible avec Google Analytics : `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

Vous pouvez prévisualiser de manière dynamique l’URL de tracking obtenue. Chaque fois que vous ajoutez, modifiez ou supprimez un paramètre, la prévisualisation est automatiquement mise à jour.

![](assets/preset-url-tracking-preview.png)

>[!NOTE]
>
>Vous pouvez également ajouter des paramètres de suivi personnalisés et dynamiques aux liens présents dans le contenu de votre e-mail, mais cela n’est pas possible au niveau de la surface. Vous devez le faire lors de la création de votre message à l’aide du Concepteur d’e-mail. [En savoir plus](message-tracking.md#url-tracking).
