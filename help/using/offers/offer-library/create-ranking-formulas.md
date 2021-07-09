---
title: Création de formules de classement
description: Découvrez comment créer des formules de classement dans Adobe Experience Platform.
feature: Offres
topic: Intégrations
role: User
level: Intermediate
source-git-commit: 70d3bdaeec2a7a8f282b0e1a79bc751f7f837663
workflow-type: ht
source-wordcount: '246'
ht-degree: 100%

---

# Création de formules de classement {#create-ranking-formulas}

## À propos des formules de classement {#about-ranking-formulas}

Les **formules de classement** vous permettent de définir des règles déterminant quelle offre doit être présentée en premier pour un emplacement donné au lieu de prendre en compte les scores de priorité des offres.

Les formules de classement sont exprimées en **syntaxe PQL** et peuvent exploiter les attributs de profil, les données contextuelles et les attributs d&#39;offre. Pour plus d&#39;informations sur l&#39;utilisation de la syntaxe PQL, reportez-vous à la [documentation dédiée](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=fr).

Après avoir créé une formule de classement, vous pouvez l&#39;affecter à un placement dans une décision (précédemment connue sous le nom d&#39;activité d&#39;offre). Voir à ce propos la section [Configuration de la sélection des offres dans les décisions](../offer-activities/configure-offer-selection.md).

## Création d&#39;une formule de classement {#create-ranking-formula}

Pour créer une formule de classement, procédez comme suit :

1. Accédez au menu **[!UICONTROL Composants]**, puis sélectionnez l&#39;onglet **[!UICONTROL Classements.]** La liste des classements précédemment créés s&#39;affiche.

   ![](../../assets/rankings-list.png)

1. Cliquez sur **[!UICONTROL Créer un classement]** pour créer une formule de classement.

   ![](../../assets/ranking-create-formula.png)

1. Spécifiez le nom, la description et la formule de la formule de classement.

   Dans cet exemple, nous voulons augmenter la priorité de toutes les offres contenant l&#39;attribut « chaud » en cas de météo avec températures chaudes. Pour ce faire, **contextData.weather=hot** a été transmis dans l&#39;appel de décision.

   ![](../../assets/ranking-syntax.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**. Votre formule de classement est créée. Vous pouvez la sélectionner dans la liste pour obtenir des détails et la modifier ou la supprimer.

   Elle est maintenant prête à être utilisée dans une décision pour classer les offres éligibles à un emplacement (voir [Configuration de la sélection des offres dans les décisions](../offer-activities/configure-offer-selection.md)).

   ![](../../assets/ranking-formula-created.png)
