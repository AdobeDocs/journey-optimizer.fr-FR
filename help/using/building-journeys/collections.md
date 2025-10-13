---
solution: Journey Optimizer
product: journey optimizer
title: Transmission dynamique des collections à l’aide d’actions personnalisées
description: Envoi d'un message à l'aide de Campaign v7/v8
feature: Journeys, Use Cases, Custom Actions, Collections
topic: Content Management
role: Developer, Data Engineer
level: Experienced
exl-id: 8832d306-5842-4be5-9fb9-509050fcbb01
version: Journey Orchestration
source-git-commit: 8f25fd5110777c148246864b364d02e4c6bf00da
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 58%

---


# Transmission dynamique des collections à l’aide d’actions personnalisées{#passing-collection}

Vous pouvez transmettre une collection dans des paramètres d’action personnalisés qui seront renseignés dynamiquement au moment de l’exécution. Deux types de collections sont pris en charge :

* **collections simples** : tableaux de types de données simples, par exemple avec une listString :

  ```json
  {
   "deviceTypes": [
       "android",
       "ios"
   ]
  }
  ```

* o **collections d’objets** : tableau d’objets JSON, par exemple :

  ```json
  {
  "products":[
     {
        "id":"productA",
        "name":"A",
        "price":20.1
     },
     {
        "id":"productB",
        "name":"B",
        "price":10.0
     },
     {
        "id":"productC",
        "name":"C",
        "price":5.99
     }
   ]
  }
  ```


## Procédure générale {#general-procedure}

Dans cette section, nous utilisons l’exemple de payload JSON suivant. Il s’agit d’un tableau d’objets avec un champ qui est une collection simple.

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "A",
        "price": 20.1,
        "color":"blue",
        "locations": [
          "Paris",
          "London"
        ]
      },
      {
        "id": "productB",
        "name": "B",
        "price": 10.99
      }
    ]
  }
}
```

Vous pouvez voir que `products` est un tableau de deux objets . Vous devez avoir au moins un objet.

1. Créez votre action personnalisée. En savoir plus sur [cette page](../action/about-custom-action-configuration.md).

1. Dans la section **[!UICONTROL Paramètres d’action]**, collez l’exemple JSON. La structure affichée est statique : lorsque vous collez la payload, tous les champs sont définis comme des constantes.

   ![](assets/uc-collection-1.png)

1. Si nécessaire, ajustez les types de champs. Les types de champs suivants sont pris en charge pour les collections : listString, listInteger, listDecimal, listBoolean, listDateTime, listDateTimeOnly, listDateOnly, listObject

   >[!NOTE]
   >
   >Le type de champ est automatiquement déduit en fonction de l’exemple de payload.

1. Si vous souhaitez transmettre des objets de façon dynamique, vous devez les définir en tant que variables. Dans cet exemple, nous définissons `products` comme variable. Tous les champs d’objet inclus dans l’objet sont automatiquement définis sur des variables.

   >[!NOTE]
   >
   >Le premier objet de l’exemple de payload est utilisé pour définir les champs.

1. Pour chaque champ, définissez le libellé qui sera affiché dans la zone de travail du parcours.

   ![](assets/uc-collection-2.png){width="70%" align="left"}

1. Créez votre parcours et ajoutez l’action personnalisée que vous avez créée. En savoir plus sur [cette page](../building-journeys/using-custom-actions.md).

1. Dans la section **[!UICONTROL Paramètres d’action]**, définissez le paramètre de tableau (`products` dans notre exemple) à l’aide de l’éditeur d’expression avancé.

   ![](assets/uc-collection-3.png)

1. Pour chacun des champs d’objet suivants, saisissez le nom de champ correspondant à partir du schéma XDM source. Si les noms sont identiques, cela n’est pas nécessaire. Dans notre exemple, il nous suffit de définir `product id` et « color ».

   ![](assets/uc-collection-4.png){width="50%" align="left"}

Pour le champ de tableau, vous pouvez également utiliser l’éditeur d’expression avancé pour effectuer une manipulation de données. Dans l’exemple suivant, nous utilisons les fonctions [filter](functions/functionfilter.md) et [intersect](functions/functionintersect.md) :

![](assets/uc-collection-5.png)

## Limites {#limitations}

* **Prise en charge des tableaux imbriqués dans les actions personnalisées**

  Adobe Journey Optimizer prend en charge les tableaux d’objets imbriqués dans les actions personnalisées **payloads de réponse**, mais cette prise en charge est limitée dans les **payloads de requête**.

  Dans les payloads de requête, les tableaux imbriqués ne sont pris en charge que s’ils contiennent un nombre fixe d’éléments, comme défini dans la configuration d’action personnalisée. Par exemple, si un tableau imbriqué comprend toujours exactement trois éléments, il peut être configuré comme une constante. Lorsque le nombre d’éléments doit être dynamique, seuls les tableaux non imbriqués (tableaux au niveau inférieur) peuvent être définis comme variables.

  Exemple :

   1. L’exemple suivant illustre un **cas d’utilisation non pris en charge**.

      Dans cet exemple, le tableau products comprend un tableau imbriqué (`locations`) avec un nombre dynamique d’éléments, qui n’est pas pris en charge dans les payloads de la requête.

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "locations": [
            { "name": "Paris" },
            { "name": "London" }
            ]
         }
      ]
      }
      ```

   2. Exemple pris en charge, avec des éléments fixes définis comme des constantes.

      Dans ce cas, les emplacements imbriqués sont remplacés par des champs fixes (`location1`, `location2`), ce qui permet à la payload de rester valide dans la configuration prise en charge.

      ```json
      {
      "products": [
         {
            "id": "productA",
            "name": "A",
            "price": 20,
            "location1": { "name": "Paris" },
            "location2": { "name": "London" }
         }
      ]
      }
      ```


* Pour tester les collections à l’aide du mode test, vous devez utiliser le mode Affichage du code. Le mode Affichage du code n’est pas pris en charge pour les événements métier pour l’instant. Vous ne pouvez envoyer qu’une collection avec un seul élément.


## Cas particuliers{#examples}

Pour les types et les tableaux de tableaux hétérogènes, le tableau est défini avec le type listAny. Vous pouvez uniquement mapper des éléments individuels, mais ne pouvez pas modifier le tableau en variable.

![](assets/uc-collection-heterogeneous.png){width="70%" align="left"}

Exemple de type hétérogène :

```json
{
    "data_mixed-types": [
        "test",
        "test2",
        null,
        0
    ]
}
```

Exemple de tableau de tableaux :

```json
{
    "data_multiple-arrays": [
        [
            "test",
            "test1",
            "test2"
        ]
    ]
}
```

**Rubrique connexe**

[Utilisation d’actions personnalisées](../building-journeys/using-custom-actions.md)
