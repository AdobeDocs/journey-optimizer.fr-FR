---
title: Créer des formules de classement
description: Découvrez comment créer des formules de classement dans Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Créer des formules de classement {#create-ranking-formulas}

## A propos des formules de classement {#about-ranking-formulas}

**Les** formules de classement vous permettent de définir des règles qui détermineront quelle offre doit être présentée en premier pour un placement donné, plutôt que de prendre en compte les scores de priorité des offres.

Les formules de classement sont exprimées en **syntaxe PQL** et peuvent exploiter les attributs de profil, les données contextuelles et les attributs d&#39;offre. Pour plus d’informations sur l’utilisation de la syntaxe PQL, consultez la [documentation dédiée](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html).

Une fois qu&#39;une formule de classement a été créée, vous pouvez l&#39;affecter à un emplacement dans une décision (précédemment appelée activité d&#39;offre). Pour plus d&#39;informations à ce sujet, voir [Configurer la sélection des offres dans les décisions](../offer-activities/configure-offer-selection.md).

## Créer une formule de classement {#create-ranking-formula}

Pour créer une formule de classement, procédez comme suit :

* Accédez au menu **[!UICONTROL Composants]**, puis sélectionnez l&#39;onglet **[!UICONTROL Classements]**.

* Cliquez sur **[!UICONTROL Créer une formule]** pour créer une nouvelle formule de classement.

   ![](../assets/ranking-create-formula.png)

* Indiquez le nom, la description et la formule de la formule de classement.

   Dans cet exemple, nous voulons augmenter la priorité de toutes les offres avec l&#39;attribut &quot;chaud&quot; si le temps réel est chaud. Pour ce faire, **contextData.weather=hot** a été transmis dans l’appel de décision.

   ![](../assets/ranking-syntax.png)

* Cliquez sur **[!UICONTROL Enregistrer]**. Votre formule de classement est créée. Vous pouvez la sélectionner dans la liste pour obtenir des détails et la modifier ou la supprimer.

   Il est maintenant prêt à être utilisé dans une décision de classement des offres admissibles pour un placement (voir [Configurer la sélection des offres dans les décisions](../offer-activities/configure-offer-selection.md)).

   ![](../assets/ranking-formula-created.png)
