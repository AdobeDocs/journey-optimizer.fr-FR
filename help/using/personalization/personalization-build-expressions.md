---
title: À propos de l’éditeur d’expression
description: Découvrez comment utiliser l’éditeur d’expression.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 100%

---

# À propos de l’éditeur d’expression {#build-personalization-expressions}

L&#39;éditeur d&#39;expression est lʼélément central de la personnalisation dans [!DNL Journey Optimizer]. Il est disponible dans tous les contextes où vous devez définir une personnalisation (par exemple, dans les emails, les notifications push et les offres).

Dans l&#39;interface de l&#39;éditeur d&#39;expression, vous sélectionnez, organisez, personnalisez et validez toutes les données afin de personnaliser votre contenu.

![](assets/perso_ee1.png)

La partie gauche de l&#39;écran affiche un sélecteur de domaine qui vous permet de sélectionner la source en vue de la personnalisation.

![](assets/perso_ee3.png)

Les sources disponibles sont les suivantes :

* **[!UICONTROL Attributs de profil]** : répertorie toutes les références associées au schéma de profil décrit dans la [documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target=&quot;_blank&quot;}.
* **[!UICONTROL Abonnements aux segments]** : répertorie tous les segments créés dans le service Adobe Experience Platform Segmentation. Vous trouverez [ici](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr){target=&quot;_blank&quot;} plus d’informations sur la segmentation.
* **[!UICONTROL Décisions d’offre]** : répertorie toutes les offres associées à un emplacement spécifique. Sélectionnez l’emplacement, puis insérez les offres dans votre contenu. Pour obtenir une documentation complète sur la gestion des offres, consultez [cette section](../messages/deliver-personalized-offers.md).
* **[!UICONTROL Attributs contextuels]** : lorsque le **Message** est utilisé dans un parcours, les champs de parcours contextuels sont disponibles dans ce menu. En savoir plus dans [cette section](personalization-use-case.md).
* **[!UICONTROL Fonctions helper]** : répertorie toutes les fonctions helper disponibles pour effectuer des opérations sur les données, comme des calculs, une mise en forme ou des conversions de données, des conditions, et les manipuler dans le contexte de la personnalisation. En savoir plus dans [cette section](functions/functions.md).

Lorsqu&#39;elle est sélectionnée, la référence est ajoutée dans l&#39;éditeur.

>[!NOTE]
>
>L&#39;icône d&#39;informations située en regard de l&#39;icône « + » ouvre une info-bulle fournissant plus de détails sur chaque variable.
>
>Vous pouvez ajouter vos attributs les plus fréquemment utilisés aux favoris. En savoir plus dans [cette section](personalization-favorites.md).

Dans lʼexemple suivant, lʼéditeur dʼexpression vous permet de sélectionner les profils qui ont leur anniversaire aujourdʼhui, puis de terminer la personnalisation en insérant une offre spécifique correspondant à ce jour.

![](assets/perso_ee2.png)

Une fois votre expression de personnalisation prête, vous devez la faire valider par l’éditeur d’expression. En savoir plus dans [cette section](personalization-validation.md).
