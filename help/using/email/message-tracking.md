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
TQID: https://experienceleague.adobe.com/mY-h-cTs9mlZH5XJNS9Yv3pxGVoRn-pBTHAh8TlBi8I
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: c6e980f5-2d4f-494f-beef-186b9ecf1513id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: f550d0f2-143d-4093-9463-467fbec95fccid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: beb7a3c1-66ab-4786-b879-7621375b3c40id: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: e0eb8757-182f-49f3-94a4-1587d16f5094id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ebb3a1face3a72a52ec365c519ac2686c97ad187
workflow-type: tm+mt
source-wordcount: 1464
ht-degree: 82%

---

# Ajouter des liens et suivre les messages {#tracking}

Utilisez [!DNL Journey Optimizer] pour ajouter des liens à votre contenu et suivre les messages envoyés afin de surveiller le comportement de vos destinataires.

>[!NOTE]
>
>Lorsque des liens sont inclus dans votre contenu, ils expirent **25 mois** après l’envoi du message, à l’exception des liens vers une page miroir, qui expirent après **90 jours**. Après ce délai, les liens ne sont plus disponibles.

## Activer le suivi {#enable-tracking}

Vous pouvez activer le suivi au niveau des e-mails en cochant les options **[!UICONTROL Ouvertures d’e-mails]** et/ou **[!UICONTROL Clics sur l’e-mail]** lorsque vous créez votre message dans un parcours ou une campagne, comme indiqué dans les onglets ci-dessous :

>[!BEGINTABS]

>[!TAB Activer le tracking dans un parcours]

![](assets/message-tracking-journey.png)

>[!TAB Activer le tracking dans une campagne]

![](assets/message-tracking-campaign.png)

>[!ENDTABS]

>[!NOTE]
>
>Les deux options sont activées par défaut.

Lorsqu’elles sont activées, ces options effectuent le suivi du comportement des destinataires de vos messages :

* La mesure **[!UICONTROL Ouvertures d’e-mails]** vérifie le nombre de messages ouverts.
* La mesure **[!UICONTROL Clics sur l’e-mail]** calcule le nombre de clics effectués sur les liens contenus dans un e-mail.

### Suivi sur plusieurs e-mails {#track-across-multiple-emails}

Un identifiant de tracking unique (urlID) n’est généré que lorsque le **URL** et le **label** sont uniques. Les liens qui partagent la même URL et ont le même libellé effectif (y compris lorsque le libellé est vide) réutilisent le même urlID, ce qui signifie que vous ne pouvez pas déterminer sur quel lien l’utilisateur a cliqué.

Pour suivre la même URL dans plusieurs e-mails (ou plusieurs fois dans un seul e-mail), utilisez un libellé unique pour chaque URL similaire ; autrement, [!DNL Journey Optimizer] ne pourrez pas suivre le lien sur lequel l’utilisateur a cliqué. Vous pouvez définir des libellés distincts dans le Designer Email ou, pour HTML, via l’attribut `data-label` .

| URL | Balise | Libellé | Comportement de l’urlID |
| --- | --- | --- | --- |
| `https://www.example.com` | First | (vide) | Obtient un urlID (par exemple, A) |
| `https://www.example.com` | Second | (vide) | Réutilise l’urlID A — impossible de déterminer le lien sur lequel l’utilisateur a cliqué |
| `https://www.example.com` | Troisième | Première étiquette | Obtient un urlID (par exemple, B) |
| `https://www.example.com` | Quatrième | Deuxième libellé | Obtient un urlID (par exemple C) |

## Insertion de liens {#insert-links}

Lorsque le [suivi est activé](#enable-tracking), tous les liens inclus dans le contenu du message font l’objet d’un suivi.

>[!NOTE]
>
>Les liens des fragments utilisés dans un e-mail font également l’objet d’un suivi. [En savoir plus sur les fragments](../content-management/fragments.md)

Pour insérer des liens dans le contenu de votre e-mail, procédez comme suit :

1. Sélectionnez un élément (texte ou image) et cliquez sur **[!UICONTROL Insérer un lien]** dans la barre d’outils contextuelle.

   ![](assets/message-tracking-insert-link.png)

1. Choisissez le type de lien que vous souhaitez créer :

   * Sélectionnez **[!UICONTROL Lien externe]** pour insérer un lien vers une URL externe.

   * Sélectionnez **[!UICONTROL Page de destination]** pour insérer un lien vers une page de destination. [En savoir plus](../landing-pages/create-lp.md)

   * Sélectionnez **[!UICONTROL Opt-out en un clic]** pour insérer un lien permettant aux utilisateurs et utilisatrices de se désabonner rapidement de vos communications sans avoir à confirmer l’opt-out. [En savoir plus](email-opt-out.md#one-click-opt-out).

   * Sélectionnez **[!UICONTROL Abonnement/opt-in externe]** pour insérer un lien permettant d’accepter de recevoir des communications de votre marque.

   * Sélectionnez **[!UICONTROL Désabonnement/opt-out externe]** pour insérer un lien permettant de se désabonner des communications de votre marque. En savoir plus sur la gestion des opt-outs dans [cette section](email-opt-out.md#email-opt-out).

   * Sélectionnez **[!UICONTROL Page miroir]** pour ajouter un lien vers la page miroir de l’e-mail. [En savoir plus](#mirror-page)

   * Sélectionnez **[!UICONTROL Lien profond]** pour insérer un lien vers une application mobile. Cela permet aux utilisateurs et utilisatrices d’accéder directement au contenu in-app approprié au lieu d’être redirigés vers des navigateurs ou des boutiques d’applications, en préservant le contexte et l’engagement. [En savoir plus](deeplinks.md)

     >[!IMPORTANT]
     >
     >Avant d’utiliser les liens profonds, assurez-vous d’avoir terminé les [étapes de configuration](deeplinks.md#configuration) correspondantes dans Journey Optimizer et implémenté [gestion des liens profonds](deeplinks.md#mobile-implementation) dans votre application mobile. Si vous ne l’avez pas fait, le lien profond ne dirigera pas les utilisateurs vers le contenu in-app prévu.
     >
     >Assurez-vous également que [le suivi des liens est activé](#enable-tracking) pour votre message, de sorte que l’URL soit réécrite via les systèmes Adobe.

1. Saisissez l’URL de votre choix dans le champ correspondant, ou sélectionnez une page de destination et définissez les styles et paramètres du lien. [En savoir plus](#adjust-links)

   >[!NOTE]
   >
   >Pour l’interprétation des URL, [!DNL Journey Optimizer] est conforme à la syntaxe URI ([norme RFC 3986](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}), ce qui désactive certains caractères internationaux spéciaux dans les URL. Lors de l’envoi du BAT ou de l’e-mail, si une erreur impliquant une URL ajoutée à votre contenu vous est renvoyée, vous pouvez encoder la chaîne comme solution de contournement.

1. Vous pouvez personnaliser vos liens. [En savoir plus](url-personalization.md)

1. Enregistrez vos modifications.

1. Une fois le lien créé, vous pouvez toujours le modifier à partir des volets **[!UICONTROL Paramètres]** et **[!UICONTROL Styles]** à droite.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>Les e-mails de type marketing doivent inclure un [lien d’exclusion](../privacy/opt-out.md#opt-out-decision-management), qui n’est pas obligatoire pour les messages transactionnels. La catégorie du message (**[!UICONTROL Marketing]** ou **[!UICONTROL Transactionnel]**) est définie au niveau de la [configuration des canaux](email-settings.md#email-type), lors de la création du message.

Une fois le message envoyé, la période de conservation d’un lien est de **25 mois**. Après ce délai, le lien n’est plus disponible.

>[!CAUTION]
>
>Lorsque les **libellé** et **URL** d’un bouton sont rendus modifiables dans un [fragment personnalisable](../content-management/customizable-fragments.md), les rapports de suivi affichent l’URL au lieu du libellé du bouton.

## Lien vers une page miroir {#mirror-page}

La page miroir est une version en ligne de votre e-mail. L’ajout d’un lien vers la page miroir constitue une bonne pratique de marketing par e-mail. Les utilisateurs et utilisatrices consultent la page miroir d’un e-mail en cas de problème d’affichage des images dans leur boîte de réception ou lorsque ces dernières sont endommagées. Il est également recommandé de fournir une version en ligne pour des raisons d’accessibilité ou pour faciliter le partage sur les réseaux sociaux.

La page miroir générée par Adobe Journey Optimizer contient toutes les données de personnalisation.

Pour ajouter un lien vers une page miroir dans votre e-mail, [insérez un lien](#insert-links) et sélectionnez **[!UICONTROL Page miroir]** comme type de lien.

![](assets/message-tracking-mirror-page.png)

La page miroir est automatiquement créée. Une fois l&#39;e-mail envoyé, lorsque les destinataires cliquent sur le lien de la page miroir, le contenu de l’email s&#39;affiche dans leur navigateur web par défaut.

La période de conservation d’une page miroir est de **90 jours**. Une fois ce délai écoulé, la page miroir n’est plus disponible.

>[!CAUTION]
>
>* Les liens de pages miroir sont générés automatiquement et ne peuvent pas être modifiés. Ils contiennent toutes les données personnalisées et chiffrées nécessaires pour générer l’e-mail original. Par conséquent, l’utilisation d’attributs personnalisés ayant des valeurs élevées peut générer des URL de pages miroir longues et empêcher le fonctionnement du lien dans les navigateurs web qui appliquent une longueur maximale d’URL.
>
>* Lors de la création d’e-mails qui reposent fortement sur la personnalisation d’exécution (par exemple, les boucles `#each`, les objets imbriqués, les données de payload volumineuses), les URL de page miroir peuvent devenir trop volumineuses, en particulier dans les campagnes déclenchées par API qui utilisent des données contextuelles volumineuses provenant des payloads. Cela peut entraîner des erreurs HTTP (404, 422, 502) dans les navigateurs ou les clients de messagerie. Adobe recommande de limiter la largeur et la profondeur des champs dynamiques, de réduire la dépendance à l’égard de fragments complexes et de simplifier les structures de personnalisation pour éviter les échecs de lien.
>
>* Dans le [BAT](../content-management/proofs.md) envoyé aux profils de test, le lien vers la page miroir n’est pas actif. Il n’est activé que dans les messages finaux.

## Personnaliser l’aspect du lien et la cible {#adjust-links}

Vous pouvez ajuster vos liens, par exemple en les soulignant, en modifiant leur couleur ou en sélectionnant leur cible.  Ces modifications sont définies dans les volets **[!UICONTROL Paramètres]** et **[!UICONTROL Styles]** de la section de droite de l’éditeur de contenu.

### Cible {#link-target}

L’attribut **cible** est utilisé pour contrôler l’emplacement d’ouverture d’une page liée. L’ajout d’un attribut cible dans une balise d’ancrage peut indiquer si le lien doit s’ouvrir dans un nouvel onglet, dans le même onglet ou dans un autre cadre.

Pour définir la cible d’un lien, procédez comme suit :

1. Dans un composant **[!UICONTROL Texte]** contenant un lien, sélectionnez ce dernier.

1. Dans l’onglet **[!UICONTROL Paramètres]**, sélectionnez l’emplacement où s’ouvre le lien dans le menu déroulant **[!UICONTROL Cible]**. Les actions possibles sont répertoriées ci-dessous :

   * **[!UICONTROL Aucune]** : ouvre le lien dans le même cadre que celui sur lequel l’utilisateur a cliqué (par défaut).
   * **[!UICONTROL Vierge]** : ouvre le lien dans une nouvelle fenêtre ou un nouvel onglet.
   * **[!UICONTROL Self]** : ouvre le lien dans le même cadre que celui sur lequel l’utilisateur a cliqué.
   * **[!UICONTROL Parent]** : ouvre le lien dans le cadre parent.
   * **[!UICONTROL Haut]** : ouvre le lien dans le corps complet de la fenêtre.

   ![](assets/link_2.png)

1. Enregistrez vos modifications.


### Souligner le lien {#link-underline}

Cochez la case **[!UICONTROL Souligner le lien]** pour souligner le texte du libellé de votre lien.

![](assets/link_1.png)

### Couleur du lien {#link-color}

Pour modifier la couleur de votre lien, cliquez sur **[!UICONTROL Couleur du lien]** dans l’onglet **[!UICONTROL Styles]**.

![](assets/link_3.png)


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

La création de rapports sur les ouvertures et les clics est disponible dans le [rapport dynamique](../reports/live-report.md) et dans le [rapport Customer Journey Analytics](../reports/report-gs-cja.md).

## Personnalisation du suivi des URL {#url-tracking}

Pour obtenir des conseils détaillés sur la personnalisation des URL (notamment sur la personnalisation des paramètres de tracking d’URL et sur la personnalisation d’une URL complète/de base), consultez la section [Personnalisation des URL](url-personalization.md).

