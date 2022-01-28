---
title: Personnalisation du contenu dans Journey Optimizer
description: Prise en main de la personnalisation
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 244f05998098bf1770d5f33c955f09688f58ffe7
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 89%

---

# Prise en main de la personnalisation{#add-personalization}

Découvrez les fonctionnalités de personnalisation de [!DNL Adobe Journey Optimizer] pour adapter vos messages à chaque destinataire spécifique en exploitant les données et informations que vous possédez à son sujet. Il peut s’agir de son prénom, de ses centres d’intérêt, de son lieu de vie, de ce qu’il a acheté, etc.

➡️ [Découvrez comment personnaliser un message dans ces vidéos](#video-perso)

[!DNL Journey Optimizer] utilise une syntaxe de personnalisation simple **intégrée** basée sur Handlebars, qui vous permet de créer des expressions avec du contenu placé entre des accolades doubles **{{}}**. Vous pouvez ajouter plusieurs expressions dans le même contenu ou champ sans restriction. En savoir plus dans [Syntaxe de personnalisation](personalization-syntax.md).

La personnalisation est basée sur les données de profil gérées par le schéma **Profil individuel XDM** défini dans Adobe Experience Platform. Pour en savoir plus, consultez la [documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target=&quot;_blank&quot;}.

>[!CAUTION]
>Le schéma **Profil individuel XDM** est le seul que vous pouvez utiliser pour personnaliser le contenu dans [!DNL Journey Optimizer].

**Exemples :**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Lors du traitement du message (e-mail et push), Journey Optimizer remplace l&#39;expression par les données contenues dans la base de données Experience Cloud Platform : `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` devient &quot;Hello John Doe&quot;.


## Contextes de personnalisation{#personalization-areas}

Le contenu et l&#39;affichage des messages diffusés par [!DNL Journey Optimizer] peuvent être personnalisés de plusieurs façons différentes.

Dans chaque champ contenant l&#39;icône de l&#39;éditeur, vous pouvez ouvrir l&#39;éditeur de personnalisation (également appelé Éditeur d&#39;expression) et définir la personnalisation.

![](assets/perso_icon.png)

### Personnaliser vos emails

Lorsque vous créez un e-mail, vous pouvez ajouter une personnalisation dans le champ **[!UICONTROL Ligne d’objet]** du message. 

![](assets/perso_subject.png)

Dans le Concepteur d&#39;email, vous pouvez personnaliser le contenu :

* Dans le **message** : cliquez dans un bloc de texte, puis cliquez sur l&#39;icône **Personnaliser** dans la barre d&#39;outils contextuelle et sélectionnez le champ **Insérer une personnalisation**. Pour plus d&#39;informations sur l&#39;interface du Concepteur d&#39;email, reportez-vous à [cette section](../design-emails.md).

   ![](assets/perso_insert.png)

* Pour un **lien** : sélectionnez du texte ou une image à l&#39;intérieur d&#39;un bloc de texte, puis cliquez sur l&#39;icône **Insérer un lien** de la barre d&#39;outils contextuelle. Dans la fenêtre, vous pouvez ajouter un bloc de personnalisation en cliquant sur l&#39;icône **Ajouter une personnalisation**.

   ![](assets/perso_link.png)

Dans les deux cas, vous accédez à l’éditeur de personnalisation.

![](assets/perso_ee.png)

### Personnalisation de vos notifications push

Vous pouvez également personnaliser vos **notifications push** dans les champs suivants :

* **Titre**
* **Corps**
* **Son personnalisé**
* **Badges**
* **Données personnalisées**

![](assets/perso_push.png)

Pour en savoir plus sur la configuration des notifications push, consultez [cette section](../push-gs.md).

### Personnalisation de vos offres {#personalize-offers}

Vous pouvez également accéder à l’éditeur de personnalisation lors de l’ajout de contenu de type texte aux représentations de vos offres.

Pour en savoir plus sur la gestion du contenu avec la gestion des décisions, consultez [cette section](../offers/offer-library/creating-personalized-offers.md#custom-text).

## Utilisation de l&#39;éditeur d&#39;expression {#use-expression-editor}

L&#39;éditeur d&#39;expression est l&#39;élément central de la personnalisation dans [!DNL Journey Optimizer].

Il est disponible dans tous les contextes où vous devez définir une personnalisation (par exemple, dans les emails, les notifications push et les offres).

Dans l&#39;interface de l&#39;éditeur d&#39;expression, vous sélectionnez, organisez, personnalisez et validez toutes les données afin de personnaliser votre contenu.

![](assets/perso_ee1.png)

La partie gauche de l&#39;écran affiche un sélecteur de domaine qui vous permet de sélectionner la source en vue de la personnalisation.

![](assets/perso_ee3.png)

Les sources disponibles sont les suivantes :

* **[!UICONTROL Attributs de profil]** : répertorie toutes les références associées au schéma de profil décrit dans la [documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Abonnements aux segments]** : répertorie tous les segments créés dans le service Adobe Experience Platform Segmentation. Vous trouverez [ici](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr){target=&quot;_blank&quot;} plus d’informations sur la segmentation.
* **[!UICONTROL Décisions d’offre]** : répertorie toutes les offres associées à un emplacement spécifique. Sélectionnez l’emplacement, puis insérez les offres dans votre contenu. Pour obtenir une documentation complète sur la gestion des offres, consultez [cette section](../deliver-personalized-offers.md).
* **[!UICONTROL Attributs contextuels]** : lorsque le **Message** est utilisé dans un parcours, les champs de parcours contextuels sont disponibles dans ce menu. En savoir plus dans [cette section](personalization-use-case.md).
* **[!UICONTROL Fonctions helper]** : répertorie toutes les fonctions helper disponibles pour effectuer des opérations sur les données, comme des calculs, une mise en forme ou des conversions de données, des conditions, et les manipuler dans le contexte de la personnalisation. En savoir plus dans [cette section](functions/functions.md).

Lorsqu&#39;elle est sélectionnée, la référence est ajoutée dans l&#39;éditeur.

>[!NOTE]
>
>L&#39;icône d&#39;informations située en regard de l&#39;icône « + » ouvre une info-bulle fournissant plus de détails sur chaque variable.

Dans l&#39;exemple suivant, l&#39;éditeur d&#39;expression vous permet de sélectionner les profils dont l&#39;anniversaire est aujourd&#39;hui, puis de terminer la personnalisation en insérant une offre spécifique correspondant à cette journée.

![](assets/perso_ee2.png)

### Ajouter aux favoris{#fav}

L’ajout d’attributs différents à votre menu favoris permet d’accéder rapidement aux éléments que vous utilisez le plus souvent. Pour ajouter un attribut à vos favoris, cliquez sur le menu ellipse et choisissez **[!UICONTROL Ajouter aux favoris]**.

![](assets/favorite-option.png)

Pour accéder aux éléments que vous avez préférés, utilisez le **[!UICONTROL Favoris]** dans le menu déroulant.

![](assets/favorite-menu.png)

Dans cette liste, vous pouvez ajouter rapidement l’objet de personnalisation à votre expression active.

![](assets/favorite-list.png)

Si vous ne souhaitez plus voir un élément dans votre liste de favoris, vous pouvez le supprimer des favoris.

![](assets/favorite-remove.png)

## Tutoriels vidéo{#video-perso}

Découvrez comment utiliser les informations d’événement contextuelles d’un parcours pour personnaliser un message.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Découvrez comment utiliser les informations d’événement contextuelles d’un parcours pour personnaliser un message.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
