---
title: Contextes de personnalisation dans Journey Optimizer
description: Découvrez dans quels contextes vous pouvez ajouter la personnalisation.
source-git-commit: 741fe2b614e3ded57c4a7ecd9b7333bdd99ab359
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 80%

---

# Contexte et outil de personnalisation {#personalization-areas}

![](../assets/do-not-localize/badge.png)

Le contenu et l’affichage des messages diffusés par Journey Optimizer peuvent être personnalisés de plusieurs façons différentes.

Tous les champs associés à l’icône de l’éditeur peuvent ouvrir l’éditeur de personnalisation et recevoir du contenu de personnalisation.

![](assets/perso_icon.png)

## Personnaliser vos emails

Lorsque vous créez un email, vous pouvez ajouter une personnalisation dans le champ **Objet de l&#39;email** du message.

![](assets/perso_subject.png)

Dans le Concepteur d’email, vous pouvez personnaliser le contenu :

* Dans le **message** : cliquez dans un bloc de texte, puis cliquez sur l’icône **Personnaliser** dans la barre d’outils contextuelle et sélectionnez le champ **Insérer une personnalisation**. Pour plus d’informations sur l’interface du Concepteur d’email, reportez-vous à [cette section](../design-emails.md).

   ![](assets/perso_insert.png)

* Pour un **lien** : sélectionnez du texte ou une image à l’intérieur d’un bloc de texte, puis cliquez sur l’icône **Insérer un lien** de la barre d’outils contextuelle. Dans la fenêtre, vous pouvez ajouter un bloc de personnalisation en cliquant sur l’icône **Ajouter une personnalisation**.

   ![](assets/perso_link.png)

## Personnaliser les notifications push

Vous pouvez également personnaliser vos **notifications push** dans les champs suivants :

* **Titre**
* **Corps**
* **Son personnalisé**
* **Badges**
* **Données personnalisées**

![](assets/perso_push.png)

Pour en savoir plus sur la configuration des notifications push, consultez [cette section](../create-push.md).

## Utiliser l’éditeur d’expression

L’éditeur d’expression est l’élément central de la personnalisation dans Journey Optimizer.

Il est disponible dans tous les contextes où vous devez définir une personnalisation (par exemple, dans les emails, les notifications push et les offres).

Dans l’interface de l’éditeur d’expression, vous sélectionnez, organisez, personnalisez et validez toutes les données afin de personnaliser votre contenu.

![](assets/perso_ee1.png)

La partie gauche de l’écran affiche un sélecteur de domaine qui vous permet de sélectionner la source en vue de la personnalisation.

* **Profil** : répertorie toutes les références associées au schéma de profil décrit dans la [ documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr).
* **Appartenance à un segment** : répertorie tous les segments créés dans le service Adobe Experience Platform Segmentation. Vous trouverez [ici](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en) plus d’informations sur la segmentation
* **Offres** : répertorie toutes les offres associées à un emplacement spécifique. Sélectionnez l’emplacement, puis insérez les offres dans votre contenu. Pour obtenir une documentation complète sur la gestion des offres, consultez [cette section](../deliver-personalized-offers.md)
* **Contexte**  : lorsque l&#39;activité  **** Messagerie est utilisée dans un parcours, les champs de parcours contextuels sont disponibles dans ce menu. Consultez [cette section](personalization-use-case.md)
* **Fonctions**  d’assistance : répertorie toutes les fonctions d’assistance disponibles pour effectuer des opérations sur les données, telles que les calculs, le formatage ou les conversions des données, les conditions et les manipuler dans le contexte de la personnalisation. [En savoir plus](functions/functions.md)



Lorsqu’elle est sélectionnée, la référence est ajoutée dans l’éditeur.

>[!NOTE]
>
>L’icône d’informations située en regard de l’icône « + » ouvre une info-bulle fournissant plus de détails sur chaque variable.

Dans l’exemple suivant, l’éditeur d’expression vous permet de sélectionner les profils dont l’anniversaire est aujourd’hui, puis de terminer la personnalisation en insérant une offre spécifique correspondant à cette journée.

![](assets/perso_ee2.png)




