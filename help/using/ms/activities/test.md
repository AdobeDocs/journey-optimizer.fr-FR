---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Test dans vos campagnes à plusieurs étapes
description: Découvrez comment utiliser l’activité Test
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 64%

---

# Test {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Activité Test"
>abstract="L’activité **Test** est une activité de **contrôle de flux**. Il permet d’activer des transitions en fonction de conditions spécifiées."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Conditions"
>abstract="L’activité **Test** peut avoir plusieurs transitions sortantes. Lors de l’exécution de la campagne en plusieurs étapes, chaque condition est testée de manière séquentielle jusqu’à ce que l’une d’elles soit remplie. Si aucune des conditions n’est remplie, la campagne à plusieurs étapes se poursuit sur le chemin de la **[!UICONTROL condition par défaut]**. Si aucune condition par défaut n’est activée, la campagne à plusieurs étapes s’arrête à ce stade."

L’activité **Test** est une activité de **contrôle de flux**. Il permet d’activer des transitions en fonction de conditions spécifiées.

## Configurer l’activité Test {#test-configuration}

Pour configurer l’activité **Test**, procédez comme suit :

1. Ajoutez une activité **Test** à votre campagne à plusieurs étapes.

1. Par défaut, l’activité **[!UICONTROL Test]** présente un test booléen simple. Si la condition définie dans la transition « True » est remplie, cette transition sera activée. Sinon, une transition « False » par défaut sera activée.

1. Pour configurer la condition associée à une transition, cliquez sur l’icône **[!UICONTROL Ouvrir la boîte de dialogue de personnalisation]**. Utilisez l’éditeur d’expression pour définir les règles d’activation de cette transition. Vous pouvez également utiliser des variables d’événement, des conditions et des fonctions de date/heure. [Découvrir comment travailler avec les variables d’événement et l’éditeur d’expression](../event-variables.md)

   De plus, vous pouvez modifier le champ **[!UICONTROL Libellé]** pour personnaliser le nom de la transition sur la zone de travail de campagne à plusieurs étapes.

   ![](../assets/workflow-test-default.png)

1. Vous pouvez ajouter plusieurs transitions de sortie à une activité **[!UICONTROL Test]**. Pour cela, cliquez sur le bouton **[!UICONTROL Ajouter une condition]** et configurez le libellé et la condition associée pour chaque transition.
v
1. Lors de l’exécution de la campagne en plusieurs étapes, chaque condition est testée de manière séquentielle jusqu’à ce que l’une d’elles soit remplie. Si aucune des conditions n’est remplie, les campagnes à plusieurs étapes se poursuivent sur le chemin de la **[!UICONTROL condition par défaut]**. Si aucune condition par défaut n’est activée, les workflows s’arrêtent à ce stade.

## Exemple {#example}

Dans cet exemple, différentes transitions sont activées en fonction du nombre de profils ciblés par une activité **[!UICONTROL Créer une audience]** :

* Si plus de 10 000 profils sont ciblés, un e-mail est envoyé.
* Pour 1 000 à 10 000 profils, un SMS est envoyé.
* Si les profils ciblés sont inférieurs à 1 000, ils sont dirigés vers une transition « Ne pas contacter ».

![](../assets/workflow-test-example.png)

Pour ce faire, la variable d’événement `vars.recCount` a été utilisée dans les conditions « E-mail » et « SMS » pour comptabiliser le nombre de profils ciblés et activer la transition appropriée.

![](../assets/workflow-test-example-config.png)
