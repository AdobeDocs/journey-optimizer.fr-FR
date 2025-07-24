---
title: Assistant de recherche de données externes
description: Guide complet d’utilisation de l’assistant de recherche de données externes pour la personnalisation dynamique dans Adobe Journey Optimizer.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
hide: true
hidefromtoc: true
badge: label="Disponibilité limitée" type="Informative"
exl-id: eae8a09a-5d27-4a80-b21f-7f795d800602
source-git-commit: 5df643d2b0623d40779d155e406467d622d3d753
workflow-type: tm+mt
source-wordcount: '1198'
ht-degree: 1%

---

# Assistant de recherche de données externes

L’assistant `externalDataLookup` de l’éditeur de personnalisation [!DNL Journey Optimizer] peut être utilisé pour récupérer dynamiquement des données à partir d’un point d’entrée externe afin de les utiliser pour générer du contenu pour les canaux entrants tels que les canaux Expérience basée sur le code, Web et Message In-App.

>[!AVAILABILITY]
>
>Cette fonctionnalité est réservée à un nombre restreint d’organisations (disponibilité limitée).

Pour utiliser l&#39;helper, vous devez d&#39;abord définir une Action dans le menu **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**. Une action permet de configurer des détails sur un point d’entrée externe, tels que l’URL, la méthode GET par rapport à POST, les paramètres d’en-tête, les paramètres de requête, le schéma JSON du corps POST et le schéma JSON de réponse.

Une fois l’action définie, elle peut être utilisée à la fois :

* Dans les parcours, dans une activité Action personnalisée pour récupérer du contenu,
* Dans les parcours et les campagnes entrantes, dans un assistant externalDataLookup pour récupérer des données dans une action entrante.

## Mécanismes de sécurisation et limites

Reportez-vous également à la section Actions personnalisées dans [!DNL Journey Optimizer] campagnes et Parcours de canaux entrants #GuardrailsandGuidelines .

* **Délai d’expiration par défaut** - Par défaut, [!DNL Journey Optimizer] utilise un délai d’expiration de 300 ms lors de l’appel d’un point d’entrée externe. Contactez votre représentant Adobe pour augmenter ce délai d’expiration pour un point d’entrée.
* **Exploration du schéma de réponse et validation des expressions** - Dans l’éditeur de personnalisation, vous ne pouvez pas parcourir le schéma de la réponse de point d’entrée lors de l’insertion d’expressions. [!DNL Journey Optimizer] ne valide pas les références aux attributs JSON de la réponse utilisée dans les expressions.
* **Types de données pris en charge pour les paramètres** - Les types de données pris en charge pour les paramètres de variable de payload à remplacer via l’assistant externalDataLookup sont `String`, `Integer`, `Decimal`, `Boolean`, `listString`, `listInt`, `listInteger` et `listDecimal`.
* **Actualisation automatique pour les actions mises à jour** - Les modifications apportées à une configuration d’action ne sont pas répercutées dans les appels externalDataLookup correspondants dans les campagnes et parcours dynamiques. Pour qu’une modification soit prise en compte, vous devez copier ou modifier les campagnes ou parcours actifs qui utilisent l’action dans un assistant externalDataLookup.
* **Substitution de variable** - Pour l’instant, l’utilisation des variables n’est pas prise en charge dans les paramètres de l’assistant externalDataLookup.
* **Chemin dynamique** - Pour l’instant, le chemin URL dynamique n’est pas pris en charge.
* **Rendu en plusieurs passages** - Le rendu en plusieurs passages est pris en charge.
* **Authentification** - Pour l’instant, les options d’authentification dans la configuration de l’action ne sont pas prises en charge par l’assistant externalDataLookup. En attendant, pour l’authentification par clé API ou d’autres clés d’autorisation en texte brut, vous pouvez les spécifier comme champs d’en-tête dans la configuration de l’action.

## Configuration d’une action et utilisation de l’assistant

Pour définir une action et utiliser l’assistant de personnalisation, procédez comme suit :

1. Créez une action pour configurer le point d’entrée pour la recherche. Cette opération ne doit être effectuée qu’une seule fois pour chaque point d’entrée et doit être effectuée par un utilisateur technique. [Découvrez comment configurer une action personnalisée](../action/about-custom-action-configuration.md)

   Notez l’ID d’action et copiez-le.

   ![](assets/external-data-action.png)

1. Créer une campagne entrante ou une action de parcours. Pour cet exemple, nous montrons comment utiliser l’assistant externalDataLookup dans une action JSON d’expérience basée sur du code, mais il peut être utilisé dans un champ de personnalisation dans n’importe quel canal entrant.

1. Modifiez le contenu de l’action, accédez à Fonctions d’assistance dans l’éditeur de personnalisation, puis accédez à **[!UICONTROL Fonctions d’assistance]** > **[!UICONTROL Helpers]**.

1. Cliquez sur le bouton `+` pour insérer l&#39;assistant externalDataLookup . L’expression d’assistance est insérée dans l’éditeur, avec des valeurs d’espace réservé pour les `actionId` et les `result`.

   ![](assets/external-data-personalization.png)

   Remplacez les valeurs des espaces réservés comme suit :

   * `actionId` : collez l’ID d’action copié précédemment.
   * `result` : définissez le nom de votre choix. Vous utiliserez cette variable de résultat pour accéder au contenu récupéré.

1. Ajoutez les valeurs de paramètre de variable à transmettre dans le cadre de l’appel de point d’entrée. Par exemple, voici comment transmettre un paramètre de langue et un paramètre d’éléments max.

   ![](assets/external-data-personalization-example.png)

1. Utilisez la variable result pour accéder aux données récupérées et les insérer dans le contenu de l’action entrante. Par exemple, voici comment renvoyer un tableau JSON d’éléments récupérés à partir du point d’entrée .

   ![](assets/external-data-personalization-result.png)

## Fonctionnement

### Exécution

Lorsqu’une action entrante inclut un assistant externalDataLookup, le point d’entrée est appelé dynamiquement au moment où la demande de personnalisation [!DNL Journey Optimizer] est reçue et traitée par AEP Edge Network.

Cela signifie que le point d’entrée externe doit être en mesure de gérer au moins autant de charge et de débit simultanés que le client envoie pour la surface donnée à AEP Edge Network.

### Syntaxe

`{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}`

### Transmettre les paramètres

Lorsque le point d’entrée externe est appelé, toutes les valeurs d’en-tête constantes, les paramètres de requête et la valeur de payload de requête définis dans l’action sont envoyés avec les valeurs fournies dans la configuration de l’action.

Pour toutes les valeurs d’en-tête de variable, les paramètres de requête/chemin ou les valeurs de payload de requête, vous pouvez transmettre des valeurs de manière dynamique à l’aide de paramètres à l’assistant externalDataLookup.

Noms des paramètres :

* Paramètres d&#39;en-tête : `header.<parameter-name>`
* Paramètres de requête : `query.<parameter-name>`
* Paramètres de payload : `payload.<parameter-name>`
* Paramètres de chemin : `dynamic_path.<parameter-name>`

Par exemple :

```
{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}`
```

Les valeurs de paramètre peuvent être des valeurs fixes ou elles peuvent être personnalisées en référençant des champs de profil ou d’autres attributs contextuels, par exemple :

```
{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
```

Les paramètres de payload peuvent être fournis à l’aide de la notation par points pour référencer des attributs JSON imbriqués, par exemple :

```
{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}
```

### Accès au résultat

Pour accéder aux données récupérées à partir d’un appel de recherche de point d’entrée externe, vous pouvez référencer les champs définis dans la payload de réponse dans la définition d’action à l’aide d’expressions de personnalisation et de fonctions d’assistance.

Par exemple, si la payload de réponse dans l’action ressemble à ceci :

```
{
    "videos": [
        {
            "id": "integer",
            "title": "string",
            "description": "string",
            "thumbnail_url": "string",
            "video_page_url": "string",
            "url": "string",
            "video_type": "string",
            "start_timestamp": "dateOnly",
            "created_on": "dateOnly",
            ...
        }
    ]
}
```

Ensuite, par exemple, vous pouvez récupérer et accéder à la description de la première vidéo dans une action Experience HTML basée sur du code comme suit :

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Vous pouvez, par exemple, récupérer et lire en boucle les éléments afin de renvoyer un tableau d’éléments dans une action JSON d’expérience basée sur du code comme suit :

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
[
{{#each result.videos as |item|}}
    {                                                  
        "title": "{{item.title}}",
        "url": "{{item.video_page_url}}",
        "thumbnail_url": "{{item.thumbnail_url}}",
        "start_timestamp": "{{item.start_timestamp}}"
    },
{{/each}}
]
```

## Résolution des problèmes

### Délais d’expiration et gestion des erreurs

[!DNL Journey Optimizer] utilise un délai d’expiration strict lors de l’appel du point d’entrée externe afin de conserver des caractéristiques de performances à faible latence et à débit élevé pour AEP Edge Network.

Si le point d’entrée expire ou qu’une autre erreur de ce type atteint le point d’entrée, la variable résultante est vide. Dans ce cas, toutes les références aux attributs dans la variable de résultat seront également vides. Si vous affichez simplement l’attribut dans le contenu, il s’affiche comme vide. Si vous tentez de lire en boucle un attribut de tableau dans le résultat , aucun élément n’est renvoyé.

Si vous souhaitez gérer plus efficacement les délais d’expiration ou les erreurs en affichant le contenu de secours, vous pouvez vérifier si le résultat de la recherche est vide et afficher le contenu de secours dans ce cas.

Par exemple, vous pouvez afficher une valeur de secours pour un seul attribut comme celui-ci :

```
First video description: {%=result.videos[0].description ?: "none found" %}
```

ou vous pouvez effectuer le rendu conditionnel d’un bloc de contenu entier comme suit :

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
{%#if result%}
   ... do something with result ...
{%else%}
    ... return fallback content ...
{%/if%}
```

### Débogage

Pour faciliter le débogage, les détails de délai d’expiration et d’erreur pour les recherches de données externes sont inclus dans la vue Edge Delivery d’AEP Assurance. Si vous ne voyez pas les résultats attendus pour un assistant externalDataLookup dans une action entrante, vous pouvez démarrer une session Assurance, lancer un appel [!DNL Journey Optimizer] à partir d&#39;une implémentation web ou mobile et utiliser la vue Edge Delivery pour vérifier les détails de temporisation ou d&#39;erreur.

Par exemple :

Sous la section Edge Delivery de la trace d’assurance dans le cadre des détails d’exécution, un nouveau bloc customActions a été ajouté avec des détails de requête et de réponse similaires à celui ci-dessous. La section Erreurs doit vous aider à déboguer en cas de problèmes lors de l’exécution de l’action personnalisée

![](assets/external-data-troubleshoot.png "width=50%")

## FAQ

* Comment transmettre un attribut contextuel de la requête en tant que paramètre à une recherche de données externe ?

  Utilisez le menu Attributs contextuels > Flux de données > Événement pour parcourir le schéma d’événement d’expérience que vous utilisez et insérer l’attribut approprié en tant que valeur de paramètre comme suit :

  ```
  {{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}
  ```

* Effectuez-[!DNL Journey Optimizer] une mise en cache des réponses des points d’entrée externes ?

  Pas actuellement. Cette fonctionnalité sera prise en charge à l’avenir.
