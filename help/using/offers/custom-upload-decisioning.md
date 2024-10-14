---
title: Utilisation des audiences de chargement personnalisées pour la prise de décision
description: Découvrez comment tirer parti des audiences de chargement personnalisées pour la prise de décision.
feature: Decision Management
role: User
level: Intermediate
source-git-commit: 1e46321de543196277613889c438dc6756e45652
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 1%

---


# Utilisation des audiences de chargement personnalisées pour la prise de décision {#custom-upload-decisioning}

Avec Journey Optimizer, vous pouvez exploiter les données des audiences créées à l’aide du téléchargement personnalisé (fichier CSV) dans Adobe Experience Platform pour prendre en charge vos workflows de gestion des décisions. Cela s’avère particulièrement utile lorsque les données ne sont pas nécessaires sur le profil, mais qu’elles sont toujours essentielles à la prise de décision.

Les données des audiences de chargement personnalisées peuvent être exploitées dans la gestion de la décision pour :

1. Critères d’éligibilité des offres et des décisions.
2. Personnaliser le contenu dans les représentations des offres.

Pour plus d’informations sur les audiences de chargement personnalisées, reportez-vous aux sections :
* [Prise en main d’audiences et de Journey Optimizer](../audience/about-audiences.md)
* [Importation d’une audience dans Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}

## À lire absolument {#must-read}

* Cette fonctionnalité est prise en charge uniquement dans **la gestion de la décision**, et non dans la prise de décision (anciennement appelée &quot;prise de décision d’expérience&quot;).
* Elle est disponible exclusivement via les demandes **API de prise de décision (Hub)** et n’est pas prise en charge par l’ **API de prise de décision Edge** ou la **prise de décision par lots**.
 
## Utilisation d’une audience de chargement personnalisée comme critères d’éligibilité {#eligibilty}

Vous pouvez utiliser une audience de téléchargement personnalisé comme critère d’éligibilité au niveau de l’offre ou de la décision. Une fois ajoutés, ces critères peuvent exclure des offres ou collections d’offres de l’éligibilité. Voici les différents emplacements où vous pouvez exploiter les audiences de chargement personnalisées pour affiner l’éligibilité des offres et des décisions :

* Créez une règle de décision à l’aide d’une audience de téléchargement personnalisée :

   1. Lors de la création d’une règle, accédez à l’onglet **Audiences** et recherchez votre audience CSV dans la liste. Faites glisser et déposez l’audience dans le canevas des règles.
   1. Utilisez l’onglet **Attributs** et accédez aux schémas d’enrichissement liés à l’audience sélectionnée pour accéder à toutes les données du fichier CSV et les utiliser dans votre règle. Vous pouvez ainsi utiliser un champ du fichier CSV pour affiner votre règle. [Découvrez comment créer une règle de décision](../offers/offer-library/creating-decision-rules.md)
   1. Enregistrez la règle. Une fois la règle créée, elle peut être utilisée au niveau de l’offre et de la décision pour affiner leur éligibilité.

  ![](assets/csv-rule.png)

* Utiliser des audiences de chargement personnalisées comme contrainte d’offre. [Découvrir comment ajouter des contraintes à une offre](../offers/offer-library/add-constraints.md)

  Lors de la création d’une offre, à l’étape **Ajouter des contraintes** , vous pouvez effectuer l’une des opérations suivantes :

   * Utiliser l&#39;audience de téléchargement personnalisé pour définir l&#39;éligibilité d&#39;une offre,
   * Appliquez une règle qui exploite l’audience de téléchargement personnalisé.

  ![](assets/csv-offer.png)

* Utilisez des audiences de téléchargement personnalisées au niveau de la décision.

  Lors de la configuration d’une décision, à l’étape **Ajouter une portée de décision**, vous pouvez utiliser des audiences de téléchargement personnalisées comme critère d’évaluation pour une collection d’offres. [Découvrez comment définir la portée de la décision](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

  ![](assets/csv-decision.png)

## Utilisation d’une audience de chargement personnalisée pour personnaliser les représentations des offres

Les audiences de chargement personnalisées peuvent également être utilisées pour personnaliser le contenu des représentations des offres en référençant les données du fichier CSV. [Découvrez comment ajouter des représentations à une offre](../offers/offer-library/add-representations.md)

Pour pouvoir exploiter les attributs d’une audience de téléchargement personnalisée à des fins de personnalisation, vous devez d’abord ajouter l’audience personnalisée comme contrainte. Pour ce faire, lors de la création d’une offre, à l’étape **Ajouter des contraintes** , ajoutez l’audience en tant que contraintes ou sélectionnez une règle en exploitant l’audience de téléchargement personnalisée.

![](assets/csv-offer.png)

Une fois l’audience ajoutée comme contrainte, vous pouvez utiliser ses attributs pour personnaliser le contenu de représentation. Pour ce faire, accédez à l’onglet **Attributs de profil** et recherchez l’audience de téléchargement personnalisée. Sélectionnez les attributs pertinents de l’audience pour personnaliser le contenu de l’offre.

![](assets/csv-perso.png)
