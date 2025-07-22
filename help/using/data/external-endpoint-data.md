---
solution: Journey Optimizer
product: journey optimizer
title: Personnaliser du contenu à l’aide des données d’un point d’entrée externe
description: Découvrez comment récupérer dynamiquement des données à partir d’un point d’entrée externe pour personnaliser le contenu entrant.
badge: label="Disponibilité limitée" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: expression, éditeur
source-git-commit: f5d1bc27afadbf875fe4dd3149ce090a8773e0f9
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 1%

---


# Personnaliser du contenu à l’aide des données d’un point d’entrée externe {#data-endpoint}

>[!AVAILABILITY]
>
>Cette fonctionnalité est réservée à un nombre restreint d’organisations (disponibilité limitée).

Journey Optimizer vous permet d’exploiter les données d’un point d’entrée externe pour personnaliser votre contenu dans les canaux entrants tels que les canaux Expérience basée sur le code, Web et Message In-App.

Pour ce faire, une fonction d’assistance dédiée, `externalDataLookup`, est disponible dans l’éditeur de personnalisation. Pour utiliser l’assistant , vous devez d’abord définir une [!DNL Journey Optimizer] **Action** dans laquelle vous configurez les détails sur le point d’entrée externe.

## À lire absolument

### Exécution

Lorsqu’une action entrante inclut un assistant externalDataLookup, le point d’entrée est appelé dynamiquement au moment de la réception et du traitement de la demande de personnalisation par l’[!DNL Adobe Experience Platform] Edge Network. Cela signifie que le point d’entrée externe doit être en mesure de gérer au moins autant de charge et de débit simultanés que le client envoie pour la surface donnée à AEP Edge Network.

### Authentification

Les options d’authentification de la configuration d’action ne sont actuellement pas prises en charge par l’assistant externalDataLookup.
En attendant, pour l’authentification par clé API ou d’autres clés d’autorisation en texte brut, vous pouvez les spécifier comme champs d’en-tête dans la configuration de l’action.
Pour les points d’entrée internes Adobe UNIQUEMENT : contactez le service Ingénierie AJO pour activer l’authentification basée sur les jetons de service pour un point d’entrée.

### Mécanismes de sécurisation et limitations

Reportez-vous également à la section Actions personnalisées dans les campagnes et Parcours de canaux entrants AJO#GuardrailsandGuidelines .

Par défaut, AJO utilise un délai d’expiration de 300 ms lors de l’appel d’un point d’entrée externe. Contactez le service Ingénierie AJO pour augmenter ce délai d’expiration pour un point d’entrée.
Dans l’éditeur Personalization, AJO ne vous permet pas de parcourir le schéma de la réponse de point d’entrée lors de l’insertion d’expressions et ne valide pas les références aux attributs JSON de la réponse utilisée dans les expressions.
Les types de données pris en charge pour les paramètres de variable de payload à remplacer via l’assistant externalDataLookup sont String, Integer, Decimal, Boolean, listString, listInt, listInteger, listDecimal
Les modifications apportées à une configuration d’action ne sont pas répercutées dans les appels externalDataLookup correspondants dans les campagnes et parcours dynamiques. Pour qu’une modification soit prise en compte, vous devez copier ou modifier les campagnes ou parcours actifs qui utilisent l’action dans un assistant externalDataLookup.
L’utilisation des variables n’est pas encore prise en charge dans les paramètres de l’assistant de recherche de données externes.
Le chemin URL dynamique n’est actuellement pas pris en charge.  - Améliorations des actions personnalisées entrantes#DynamicPathSegments

## Création d’une action

Créez une action pour configurer le point d’entrée pour la recherche. Cette opération ne doit être effectuée qu’une seule fois pour chaque point d’entrée et doit être effectuée par un utilisateur technique. Voir cette page.

La même action peut être utilisée à la fois dans une activité **[!UICONTROL Action personnalisée]** pour récupérer du contenu dans un parcours et dans une fonction d’assistance `externalDataLookup` pour récupérer des données dans une action entrante dans un parcours ou une campagne.

Accédez au menu **[!UICONTROL Administration]** / **[!UICONTROL Configurations]**.

Notez l’ID d’action et copiez-le pour l’utiliser à l’étape 6.


## Personnaliser le contenu à l’aide de données récupérées

### Ajouter la fonction d’assistance à votre contenu

1. Créer une campagne entrante ou une action de parcours et modifier son contenu.

1. Localisez le contenu où vous souhaitez utiliser les données récupérées à partir du point d’entrée externe et accédez à l’éditeur de personnalisation.

1. Sélectionnez le menu Fonctions d’assistance et recherchez la fonction d’assistance `externalDataLookup`.

1. Sélectionnez pour insérer la syntaxe associée dans votre code et remplacer les valeurs des paramètres `actionId` et `result` comme suit :

   * `actionId` : collez l’identifiant d’action copié lors de la création de l’action.
   * `result` : définissez ce paramètre sur le nom de votre choix. Vous utiliserez cette variable de résultat pour accéder au contenu récupéré.

1. Ajoutez les valeurs de paramètre de variable à transmettre dans le cadre de l’appel de point d’entrée. Par exemple, voici comment transmettre un paramètre de langue et un paramètre d’éléments max.

### Personnalisation à l’aide des données récupérées

Pour accéder aux données récupérées à partir d’un appel de recherche de point d’entrée externe, vous pouvez référencer les champs définis dans la payload de réponse dans la définition d’action à l’aide d’expressions de personnalisation et de fonctions d’assistance.

Utilisez la variable `result` pour accéder aux données récupérées et les insérer dans le contenu de l’action entrante. Par exemple, voici comment renvoyer un tableau JSON d’éléments récupérés à partir du point d’entrée .

Prenons l’exemple ci-dessous, où le payload de réponse dans l’action a été configuré comme suit :

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

Exemple Personalization 1 : affichez la description de la première vidéo dans une action Experience HTML basée sur du code :

```
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}
 
First video description: <b>result.videos[0].description</b>
```

Exemple Personalization 2 : renvoi d’un tableau d’éléments dans une action JSON d’expérience basée sur du code :

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

## Délais d’expiration et gestion des erreurs

AJO applique un délai d’expiration strict lors de l’appel du point d’entrée externe afin de conserver des caractéristiques de performances à faible latence et à débit élevé pour AEP Edge Network.

Si le point d’entrée expire ou qu’une autre erreur de ce type atteint le point d’entrée, la variable résultante est vide. Dans ce cas, toutes les références aux attributs dans la variable de résultat seront également vides. Si vous affichez simplement l’attribut dans le contenu, il s’affiche comme vide. Si vous tentez de lire en boucle un attribut de tableau dans le résultat , aucun élément n’est renvoyé.

Si vous souhaitez gérer plus efficacement les délais d’expiration ou les erreurs en affichant le contenu de secours, vous pouvez vérifier si le résultat de la recherche est vide et afficher le contenu de secours dans ce cas.

Par exemple, vous pouvez afficher une valeur de secours pour un seul attribut comme celui-ci :

Première description de la vidéo : {%=result.vidéos[0].description ? : « aucun trouvé » %}


ou vous pouvez effectuer le rendu conditionnel d’un bloc de contenu entier comme suit :

{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result"}}

{%#if résultat%}
... faire quelque chose avec le résultat ...
{%else%}
... renvoyer le contenu de secours ...
{%/if%}
Débogage
Pour faciliter le débogage, les détails de délai d’expiration et d’erreur pour les recherches de données externes sont inclus dans la vue Edge Delivery d’AEP Assurance. Si vous ne voyez pas les résultats attendus pour un assistant externalDataLookup dans une action entrante, vous pouvez démarrer une session Assurance, lancer un appel AJO à partir d&#39;une implémentation web ou mobile et utiliser la vue Edge Delivery pour vérifier les détails de temporisation ou d&#39;erreur.

Par exemple :

Sous la section Edge Delivery de la trace d’assurance dans le cadre des détails d’exécution, un nouveau bloc customActions a été ajouté avec .

les détails de la requête et de la réponse similaires à celui ci-dessous. La section Erreurs doit vous aider à déboguer en cas de problèmes lors de l’exécution de l’action personnalisée

## Questions fréquentes

+++Comment transmettre un attribut contextuel de la requête en tant que paramètre à une recherche de données externe ?

Utilisez le menu Attributs contextuels > Flux de données > Événement pour parcourir le schéma d’événement d’expérience que vous utilisez et insérer l’attribut approprié en tant que valeur de paramètre comme suit :

`{{externalDataLookup actionId="..." result="result" query.myQueryParameter=context.datastream.event.<schemaId>.my.xdm.attribute}}`

+++

+++AJO effectue-t-il une mise en cache des réponses de point d’entrée externe ?

Pas actuellement. Cette fonctionnalité sera prise en charge à l’avenir.

+++









Syntaxe
{{externalDataLookup actionId="d130c8e2-9a2d-45d5-bcb6-bc39865b4a56" result="result" optional-parameters...}}



Transmettre les paramètres
Lorsque le point d’entrée externe est appelé, toutes les valeurs d’en-tête constantes, les paramètres de requête et la valeur de payload de requête définis dans l’action sont envoyés avec les valeurs fournies dans la configuration de l’action.

Pour toutes les valeurs d’en-tête de variable, les paramètres de requête/chemin ou les valeurs de payload de requête, vous pouvez transmettre des valeurs de manière dynamique à l’aide de paramètres à l’assistant externalDataLookup.

Noms des paramètres :

Paramètres d’en-tête : en-tête.<parameter-name>
Paramètres de requête : requête.<parameter-name>
Paramètres de payload : payload.<parameter-name>
Paramètres de chemin : dynamic_path.<parameter-name>
Par exemple :

{{externalDataLookup actionId="..." result="result" header.myHeaderParameter="value1" query.myQueryParameter="value2" payload.myPayloadParameter="value3"}}
Les valeurs de paramètre peuvent être des valeurs fixes ou elles peuvent être personnalisées en référençant des champs de profil ou d’autres attributs contextuels, par exemple :

{{externalDataLookup actionId="..." result="result" query.myQueryParameter=profile.myProfileValue}}
Les paramètres de payload peuvent être fournis à l’aide de la notation par points pour référencer des attributs JSON imbriqués, par exemple :

{{externalDataLookup actionId="..." result="result" payload.context.channel="web"}}