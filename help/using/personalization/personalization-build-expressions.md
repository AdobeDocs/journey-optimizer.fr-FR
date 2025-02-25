---
solution: Journey Optimizer
product: journey optimizer
title: À propos de l’éditeur de personnalisation
description: Découvrez comment utiliser l’éditeur de personnalisation.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, éditeur, à propos, commencer
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 19d33bf2d455aaca3fd0e961bebe5dd1d1f5b32c
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 93%

---

# Commencer avec l’éditeur de personnalisation {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="À propos de l’éditeur de personnalisation"
>abstract="L’éditeur de personnalisation vous permet de sélectionner, organiser, personnaliser et valider toutes les données afin de personnaliser votre contenu."

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="Saisie semi-automatique"
>abstract="Activer cette option permet au système de compléter automatiquement votre code et de faire des suggestions lorsque vous saisissez votre expression. Cette option est disponible uniquement pour les formats HTML et Texte."

L’éditeur de personnalisation constitue lʼélément central de la personnalisation dans [!DNL Journey Optimizer]. Il est disponible dans tous les contextes où vous devez définir une personnalisation (par exemple, dans les emails, les notifications push et les offres).

Dans l’interface de l’éditeur de personnalisation, vous sélectionnez, organisez, personnalisez et validez toutes les données afin de personnaliser votre contenu.

![](assets/perso_ee1.png)

## Sources de personnalisation disponibles {#sources}

La partie gauche de l&#39;écran affiche un sélecteur de domaine qui vous permet de sélectionner la source en vue de la personnalisation. Les sources disponibles sont les suivantes :

* **[!UICONTROL Attributs de profil]** : répertorie toutes les références associées au schéma de profil décrit dans la [documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"}.
* **[!UICONTROL Audiences]** : répertorie toutes les audiences créées dans le service de segmentation d’Adobe Experience Platform. Vous trouverez [ici](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr){target="_blank"} plus d’informations sur la segmentation.
* **[!UICONTROL Décisions d’offre]** : répertorie toutes les offres associées à un emplacement spécifique. Sélectionnez l’emplacement, puis insérez les offres dans votre contenu. Pour obtenir une documentation complète sur la gestion des offres, consultez [cette section](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL Attributs contextuels]** : lorsqu’une activité d’action de canal (e-mail, notification push, SMS) est utilisée dans un parcours ou une campagne, des attributs contextuels liés aux événements et aux propriétés sont disponibles pour la personnalisation. Un exemple de personnalisation utilisant les attributs contextuels est présenté dans [cette section](personalization-use-case.md).
* **[!UICONTROL Fonctions d’assistance]** : répertorie toutes les fonctions d’assistance disponibles pour effectuer des opérations sur les données, comme des calculs, une mise en forme ou des conversions de données, des conditions, et les manipuler dans le contexte de la personnalisation. En savoir plus dans [cette section](functions/functions.md).

## Ajouter des attributs de personnalisation {#add}

Cliquez sur le bouton « + » pour ajouter un attribut à votre expression de personnalisation.

Le menu Points de suspension en regard de l’icône « + » vous permet d’obtenir plus de détails sur chaque variable et d’ajouter les attributs les plus fréquemment utilisés à vos favoris. [Découvrez comment ajouter des attributs aux favoris](personalization-favorites.md)

>[!NOTE]
>
>Si vous ciblez une audience avec des attributs d’enrichissement générés à l’aide d’un workflow de composition, vous pouvez utiliser ces attributs pour personnaliser votre message. [Découvrir comment utiliser les attributs d’enrichissement des audiences](../audience/about-audiences.md#enrichment)

De plus, vous pouvez définir un texte de remplacement par défaut qui s’affichera si un attribut de profil de type chaîne est vide. Pour ce faire, cliquez sur le bouton des points de suspension en regard de l’attribut et sélectionnez **[!UICONTROL Insérer avec un texte de remplacement]**. Rédigez le texte à afficher par défaut si la valeur de l’attribut est vide pour un profil, puis cliquez sur **[!UICONTROL Ajouter]**.

![](assets/attribute-details.png)

Dans l’exemple suivant, l’éditeur de personnalisation vous permet de sélectionner les profils dont l’anniversaire est aujourd’hui, puis de terminer la personnalisation en insérant une offre spécifique correspondant à cette journée.

![](assets/perso_ee2.png)

Une fois votre expression de personnalisation prête, vous devez la faire valider par l’éditeur de personnalisation. En savoir plus dans [cette section](personalization-validation.md).
