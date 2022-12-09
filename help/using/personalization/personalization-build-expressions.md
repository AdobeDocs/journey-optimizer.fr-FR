---
solution: Journey Optimizer
product: journey optimizer
title: A propos de l'éditeur d'expression
description: Découvrez comment utiliser l’éditeur d’expression.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# A propos de l&#39;éditeur d&#39;expression {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="A propos de l&#39;éditeur d&#39;expression"
>abstract="L’éditeur d’expression vous permet de sélectionner, organiser, personnaliser et valider toutes les données afin de créer une personnalisation personnalisée de votre contenu."

L’éditeur d’expression est l’élément central de la personnalisation dans [!DNL Journey Optimizer]. Il est disponible dans tous les contextes où vous devez définir la personnalisation comme les emails, les notifications push et les offres.

Dans l’interface de l’éditeur d’expression, vous allez sélectionner, organiser, personnaliser et valider toutes les données afin de créer une personnalisation personnalisée de votre contenu.

![](assets/perso_ee1.png)

La partie gauche de l’écran affiche un sélecteur de domaine qui vous permet de sélectionner la source de la personnalisation.

![](assets/perso_ee3.png)

Les sources disponibles sont les suivantes :

* **[!UICONTROL Profile attributes]** : répertorie toutes les références associées au schéma de profil décrit dans la section [Documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Segment memberships]** : répertorie tous les segments créés dans Adobe Experience Platform Segmentation service. Plus d’informations sur la segmentation disponibles [here](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Offer decisions]** : répertorie toutes les offres associées à un emplacement spécifique. Sélectionnez l’emplacement, puis insérez les offres dans votre contenu. Pour obtenir une documentation complète sur la gestion des offres, reportez-vous à la section [cette section](../email/add-offers-email.md).
* **[!UICONTROL Contextual attributes]** : lorsqu’une activité d’action de canal (email, push, SMS) est utilisée dans un parcours, les champs de parcours contextuels sont disponibles via ce menu. En savoir plus dans [cette section](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : répertorie toutes les fonctions d’assistance disponibles pour effectuer des opérations sur les données, telles que les calculs, le formatage ou les conversions des données, les conditions et les manipuler dans le contexte de la personnalisation. En savoir plus dans [cette section](functions/functions.md).

Cliquez sur le bouton + pour ajouter un attribut dans l&#39;éditeur.

>[!NOTE]
>
>Le menu de points de suspension en regard de l’icône &quot;+&quot; vous permet d’obtenir plus de détails sur chaque variable et d’ajouter vos attributs utilisés le plus souvent à [favoris](personalization-favorites.md).

![](assets/attribute-details.png)

Dans l&#39;exemple suivant, l&#39;éditeur d&#39;expression permet de sélectionner les profils dont la date de naissance est la veille, puis de compléter la personnalisation en insérant une offre spécifique correspondant à cette journée.

![](assets/perso_ee2.png)

Une fois votre expression de personnalisation prête, vous devez la faire valider par l&#39;éditeur d&#39;expression. En savoir plus dans [cette section](personalization-validation.md).
