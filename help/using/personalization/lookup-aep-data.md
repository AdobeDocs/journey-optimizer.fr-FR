---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser les données Adobe Experience Platform pour la personnalisation (version bêta)
description: Découvrez comment utiliser les données Adobe Experience Platform pour la personnalisation.
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, éditeur
hidefromtoc: true
hide: true
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: a03541b5f1d9c799c30bf1d38b6f187d94c21dff
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 81%

---

# Utiliser les données Adobe Experience Platform pour la personnalisation (version bêta) {#aep-data}

>[!AVAILABILITY]
>
>Cette fonctionnalité est publiée sous forme de version bêta privée.
>
>Pour l’instant, elle n’est disponible que pour le **canal e-mail** et à des fins de test dans le sandbox hors production que vous avez fourni à Adobe et pour les jeux de données requis pour la version bêta.

Journey Optimizer vous permet d’utiliser les données d’Adobe Experience Platform dans l’éditeur de personnalisation pour [personnaliser votre contenu](../personalization/personalize.md). Les étapes sont les suivantes :

1. Ouvrez l’éditeur de personnalisation, disponible dans tout contexte où vous pouvez définir une personnalisation, tel que les messages. [Découvrir comment utiliser l’éditeur de personnalisation](../personalization/personalization-build-expressions.md)

1. Accédez à la liste des fonctions d’assistance et ajoutez la fonction d’assistance **datasetLookup** au volet de code.

   ![](assets/aep-data-helper.png)

1. Cette fonction fournit une syntaxe prédéfinie pour vous permettre d’appeler des champs à partir de vos jeux de données Adobe Experience Platform. La syntaxe se présente comme suit :

   ```
   {{entity.datasetId="datasetId" id="key" result="store"}}
   ```

   * **entity.datasetId** est l’identifiant du jeu de données que vous utilisez.
   * **id** est l’identifiant de la colonne source qui doit être associée à l’identité principale du jeu de données de recherche.

     >[!NOTE]
     >
     >La valeur saisie pour ce champ peut être un identifiant de champ (*profile.couponValue*), un champ transmis dans un événement de parcours (*context.parcours.events.event_ID.couponValue*) ou une valeur statique (*couponAbcd*). Dans tous les cas, le système utilisera la valeur et la recherche dans le jeu de données pour vérifier s’il correspond à une clé.

   * **result** est un nom arbitraire que vous devez fournir pour référencer toutes les valeurs de champ que vous allez récupérer du jeu de données. Cette valeur sera utilisée dans votre code pour appeler chaque champ.

   +++Où récupérer un identifiant de jeu de données ?

   Les identifiants de jeu de données peuvent être récupérés dans l’interface d’utilisation d’Adobe Experience Platform. Découvrez comment utiliser les jeux de données dans la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}.

   ![](assets/aep-data-dataset.png)

+++

1. Adaptez la syntaxe à vos besoins. Dans cet exemple, nous allons récupérer les données relatives aux vols des passagères et passagers. La syntaxe se présente comme suit :

   ```
   {{entity.datasetId="1234567890abcdtId" id=profile.upcomingFlightId result="flight"}}
   ```

   * Nous travaillons dans le jeu de données dont l’identifiant est « 1234567890abcdtId »,
   * Le champ que nous voulons utiliser pour joindre le jeu de données de recherche est *profile.prochainFlightId*,
   * Nous souhaitons inclure toutes les valeurs de champ sous la référence « vol ».

1. Une fois que la syntaxe à appeler dans le jeu de données Adobe Experience Platform a été configurée, vous pouvez spécifier les champs à récupérer. La syntaxe se présente comme suit :

   ```
   {{result.fieldId}}
   ```

   * **result** est la valeur que vous avez attribuée au paramètre **result** dans la fonction d’assistance **MultiEntity**. Dans cet exemple, « vol ».
   * **fieldID** est l’identifiant du champ à récupérer. Cet identifiant est visible dans l’interface d’utilisation d’Adobe Experience Platform lors de la navigation dans votre jeu de données. Développez la section ci-dessous pour afficher un exemple :

     +++Où récupérer un identifiant de champ ?

     Les ID de champs peuvent être récupérés lors de la prévisualisation d’un jeu de données dans l’interface d’utilisation d’Adobe Experience Platform. Découvrez comment prévisualiser les jeux de données dans la [Documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}.

     ![](assets/aep-data-field.png)

+++

   Dans cet exemple, nous allons utiliser des informations relatives à l’heure et à la porte d’embarquement des passagères et passagers. Nous ajoutons donc ces deux lignes :

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. Maintenant que votre code est prêt, vous pouvez compléter votre contenu comme vous le faites habituellement et le tester à l’aide du bouton **Simuler le contenu** pour vérifier la personnalisation. [Découvrir comment prévisualiser et tester votre contenu](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
