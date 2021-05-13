---
title: Contextes de personnalisation dans Journey Optimizer
description: Découvrez dans quels contextes vous pouvez ajouter la personnalisation
source-git-commit: e73b47ab6243b13f82aa1503bd8c751f976f29ee
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 2%

---

# Zones de personnalisation {#personalization-areas}

![](../assets/do-not-localize/badge.png)

Le contenu et l&#39;affichage des messages envoyés par Journey Optimizer peuvent être personnalisés de plusieurs manières.

Tous les champs associés à l’icône de l’éditeur peuvent ouvrir l’éditeur de personnalisation et recevoir du contenu de personnalisation.

![](assets/perso_icon.png)

## Personnaliser vos courriels

Lors de la création du message de canal de courrier électronique, le champ **Objet du message électronique** peut être personnalisé.

![](assets/perso_subject.png)

Dans le concepteur de courrier électronique, vous pouvez personnaliser le contenu :

* Dans le **message** : cliquez à l’intérieur d’un bloc de texte, cliquez sur l’icône **Personnaliser** de la barre d’outils contextuelle et sélectionnez **Insérer la personnalisation**. Pour plus d’informations sur l’interface de Designer d’e-mail, voir cette [section](../design-emails.md).

   ![](assets/perso_insert.png)

* Pour un **lien** : sélectionnez du texte ou une image à l’intérieur d’un bloc de texte, cliquez sur l’icône **Insérer un lien** de la barre d’outils contextuelle. Dans la fenêtre, vous pouvez ajouter un bloc de personnalisation en cliquant sur l&#39;icône **Ajouter la personnalisation**.

   ![](assets/perso_link.png)

## Personnaliser les notifications Push

Dans le **canal Push**, la personnalisation vous permet d’affiner votre notification Push.

Vous pouvez ajouter la personnalisation dans les champs suivants :

* **Titre**
* **Corps**
* **Son personnalisé**
* **Badges**
* **Données personnalisées**

![](assets/perso_push.png)

Pour obtenir une documentation complète sur la configuration des notifications Push, consultez [cette section](../configure-push.md).


## Utilisation de l’éditeur d’expressions

L’éditeur d’expressions est l’élément central de la personnalisation dans Journey Optimizer.

Il est disponible dans tous les contextes où vous devez définir la personnalisation comme les courriels, les notifications Push et les offres.

Dans l’interface de l’éditeur d’expressions, vous sélectionnez, organisez, personnalisez et validez toutes les données afin de créer une personnalisation personnalisée pour votre contenu.

![](assets/perso_ee1.png)

La partie gauche de l’écran affiche un sélecteur de domaine qui vous permet de sélectionner la source à personnaliser.

* **Profil**  : liste toutes les références associées au schéma de profil décrites dans la documentation [ du modèle de données ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr)Adobe Experience Platform (XDM).
* **Appartenance**  au segment : liste tous les segments créés dans le service de segmentation Adobe Experience Platform. Pour plus d&#39;informations sur la segmentation, [cliquez ici](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en).
* **Offres**  : liste toutes les offres associées à un emplacement spécifique. Sélectionnez l’emplacement, puis insérez les offres dans votre contenu. Pour obtenir une documentation complète sur la gestion des offres, consultez [cette section](../../using/offers/get-started/starting-offer-decisioning.md).

Lors de la sélection, la référence est ajoutée dans l’éditeur.

>[!NOTE]
>
>L’icône d’informations en regard de l’icône &quot;+&quot; ouvre une info-bulle fournissant plus de détails pour chaque variable.

Dans l’exemple suivant, l’éditeur d’expressions vous permet de sélectionner les profils qui ont leur anniversaire aujourd’hui, puis de terminer la personnalisation en insérant une offre spécifique correspondant à ce jour.

![](assets/perso_ee2.png)




