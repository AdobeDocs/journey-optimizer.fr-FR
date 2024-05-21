---
solution: Journey Optimizer
product: journey optimizer
title: Sources de données externes
description: Découvrez comment configurer des sources de données externes
feature: Journeys, Data Sources, Integrations
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: externe, sources, données, configuration, connexion, tiers
exl-id: f3cdc01a-9f1c-498b-b330-1feb1ba358af
source-git-commit: 815595f907ed3ea05b7772a1df96187509351bf9
workflow-type: tm+mt
source-wordcount: '1541'
ht-degree: 99%

---

# Sources de données externes {#external-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_custom"
>title="Sources de données externes"
>abstract="Les sources de données externes vous permettent de définir une connexion à des systèmes tiers ; par exemple, si vous utilisez un système de réservation d’hôtels pour vérifier si la personne a réservé une chambre. Contrairement à la source de données Adobe Experience Platform intégrée, vous pouvez créer autant de sources de données externes que nécessaire."

Les sources de données externes vous permettent de définir une connexion à des systèmes tiers ; par exemple, si vous utilisez un système de réservation d’hôtels pour vérifier si la personne a réservé une chambre. Contrairement à la source de données Adobe Experience Platform intégrée, vous pouvez créer autant de sources de données externes que nécessaire.

>[!NOTE]
>
>Les mécanismes de sécurisation lorsque vous utilisez des systèmes externes sont répertoriés dans [cette page](../configuration/external-systems.md).

>[!NOTE]
>
>Les réponses étant désormais prises en charge, vous devez utiliser des actions personnalisées au lieu de sources de données pour les cas d’utilisation de sources de données externes.

Les API REST utilisant POST ou GET et renvoyant JSON sont prises en charge. Les modes d’authentification simple, personnalisé et par clé API sont pris en charge.

Prenons l’exemple d’un service API météorologique que je souhaite utiliser pour personnaliser les comportements de mon parcours en fonction des données météorologiques en temps réel.

Voici deux exemples de l’appel API :

* _https://api.adobeweather.org/weather?city=London,uk&amp;appid=1234_
* _https://api.adobeweather.org/weather?lat=35&amp;lon=139&amp;appid=1234_

L’appel est composé d’une URL principale (_https://api.adobeweather.org/weather_), de deux jeux de paramètres (« city » pour la ville et « lat/long » pour la latitude et la longitude) et de la clé API (appid).

Les principales étapes nécessaires pour créer et configurer une source de données externe sont les suivantes :

1. Dans la liste des sources de données, cliquez sur **[!UICONTROL Créer une source de données]** pour créer une source de données externe.

   ![](assets/journey25.png)

   Le volet de configuration de la source de données s’ouvre alors dans la partie droite de l’écran.

   ![](assets/journey26.png)

1. Attribuez un nom à votre source de données.

   >[!NOTE]
   >
   >Seuls les caractères alphanumériques et les traits de soulignement sont autorisés. La longueur maximale est de 30 caractères.

1. Ajoutez une description à la source de données. Cette étape est facultative.
1. Ajoutez l&#39;URL du service externe. Dans notre exemple : _https://api.adobeweather.org/weather_.

   >[!CAUTION]
   >
   >Nous vous recommandons vivement d&#39;utiliser le protocole HTTPS pour des raisons de sécurité. Notez également que l’utilisation des adresses Adobe qui ne sont pas publiques et des adresses IP n’est pas autorisée.

   ![](assets/journey27.png)

1. Configurez l’authentification en fonction de la configuration du service externe : **[!UICONTROL Aucune authentification]**, **[!UICONTROL Simple]**, **[!UICONTROL Personnalisée]** ou **[!UICONTROL Clé API]**.

   Pour le mode d’authentification simple, vous devez renseigner un nom d’utilisateur ou d’utilisatrice et un mot de passe.

   >[!NOTE]
   >
   >Lorsque l’appel d’authentification est effectué, la chaîne `<username>:<password>`, codée en base64, est ajoutée dans l’en-tête Authentification.

   Pour plus d’informations sur le mode d’authentification personnalisée, reportez-vous à [cette section](../datasource/external-data-sources.md#custom-authentication-mode). Dans notre exemple, nous choisissons le mode d’authentification de clé API :

   * **[!UICONTROL Type]** : « clé API »
   * **[!UICONTROL Nom]** : « appid » (il s’agit du nom du paramètre de la clé API)
   * **[!UICONTROL Valeur]** : « 1234 » (valeur de la clé API)
   * **[!UICONTROL Emplacement]** : « Paramètre de requête » (la clé API se trouve dans l’URL)

   ![](assets/journey28.png)

1. Ajoutez un nouveau groupe de champs pour chaque jeu de paramètres d’API en cliquant sur **[!UICONTROL Ajouter un nouveau groupe de champs]**. Seuls les caractères alphanumériques et les traits de soulignement sont autorisés dans le nom du groupe de champs. La longueur maximale est de 30 caractères. Dans cet exemple, nous devons créer deux groupes de champs, un pour chaque jeu de paramètres (city et long/lat).

Pour le jeu de paramètres « long/lat », nous créons un groupe de champs avec les informations suivantes :

* **[!UICONTROL Utilisé(e) dans]** : affiche le nombre de parcours qui utilisent un groupe de champs. Vous pouvez cliquer sur l’icône **[!UICONTROL Afficher les parcours]** pour faire apparaître la liste des parcours utilisant ce groupe de champs.
* **[!UICONTROL Méthode]** : sélectionnez la méthode POST ou GET. Dans notre exemple, nous choisissons la méthode GET.
* **[!UICONTROL Valeurs dynamiques]** : saisissez les différents paramètres, séparés par une virgule (« long,lat » dans notre exemple). Étant donné que les valeurs des paramètres dépendent du contexte d’exécution, elles sont définies dans les parcours. [En savoir plus](../building-journeys/expression/expressionadvanced.md)
* **[!UICONTROL Payload en réponse]** : cliquez dans le champ **[!UICONTROL Payload]** et collez un exemple de la payload renvoyée par l’appel. Dans cet exemple, nous avons utilisé une payload trouvée sur un site web d’API météo. Vérifiez que les types de champs sont corrects. À chaque appel de l’API, le système récupère tous les champs contenus dans l’exemple de payload. Notez que vous pouvez cliquer sur **[!UICONTROL Coller une nouvelle payload]** si vous souhaitez modifier la payload actuellement transmise.

* **[!UICONTROL Payload envoyée]** : ce champ ne figure pas dans notre exemple. Il n’est disponible que si vous sélectionnez la méthode POST. Collez la payload qui sera envoyée au système tiers.

Dans le cas d’un appel GET nécessitant un ou plusieurs paramètres, vous devez indiquer ce(s) dernier(s) dans le champ **[!UICONTROL Valeurs dynamiques]**. Ils sont alors automatiquement ajoutés à la fin de l’appel. Dans le cas d’un appel POST, vous devez :

* répertorier les paramètres à transmettre au moment de l’appel dans le champ **[!UICONTROL Valeurs dynamiques]** (« identifiant » dans l’exemple ci-dessous) ;
* spécifier les paramètres avec la même syntaxe dans le corps de la payload envoyée. Pour ce faire, vous devez ajouter : « param » : « nom de votre paramètre » (« identifiant » dans l’exemple ci-dessous). Respectez la syntaxe ci-dessous :

  ```
  {"id":{"param":"identifier"}}
  ```

![](assets/journey29.png)

Cliquez sur **[!UICONTROL Enregistrer]**.

La source de données est maintenant configurée et prête à être utilisée dans vos parcours ; par exemple, dans vos conditions ou pour personnaliser un e-mail. Si la température est supérieure à 30° C, vous pouvez choisir d’envoyer une communication spécifique.

## Mode d’authentification personnalisé {#custom-authentication-mode}

>[!CONTEXTUALHELP]
>id="jo_authentication_payload"
>title="À propos de l&#39;authentification personnalisée"
>abstract="Le mode d&#39;authentification personnalisé, utilisé pour l&#39;authentification complexe, permet d&#39;appeler les protocoles d&#39;encapsulage d&#39;API tels qu&#39;OAuth2. L&#39;exécution de l&#39;action est un processus en deux étapes. Tout d&#39;abord, un appel au point d&#39;entrée est effectué pour générer le jeton d&#39;accès. Ensuite, le jeton d&#39;accès est injecté dans la requête HTTP de l&#39;action."

Ce mode d’authentification est utilisé pour une authentification complexe. Il est fréquemment utilisé pour appeler les protocoles d’encapsulage d’API, comme OAuth2, afin de récupérer un jeton d’accès à injecter dans la requête HTTP réelle pour l’action.

Lorsque vous configurez l’authentification personnalisée, vous pouvez cliquer sur le bouton ci-dessous pour vérifier si la payload d’authentification personnalisée est correctement configurée.

![](assets/journey29-bis.png)

Si le test réussit, le bouton devient vert.

![](assets/journey29-ter.png)

Avec cette authentification, l’exécution de l’action est un processus en deux étapes :

1. Appelez le point d’entrée pour générer le jeton d’accès.
1. Appelez l’API REST en injectant correctement le jeton d’accès.


>[!NOTE]
>
>**Cette authentification se compose de deux parties.**

### Définition du point d’entrée à appeler pour générer le jeton d’accès{#custom-authentication-endpoint}

* endpoint : URL à utiliser pour générer le point d’entrée
* méthode de la requête HTTP sur le point d’entrée (GET ou POST)
* headers : paires clé-valeur à injecter en tant qu’en-têtes dans cet appel, le cas échéant
* body : décrit le corps de l’appel en cas d’utilisation de la méthode POST. Nous prenons en charge une structure de corps limitée, définie dans bodyParams (paires clé-valeur). bodyType décrit le format et le codage du corps dans l’appel :
   * &#39;form&#39; : signifie que le type de contenu sera application/x-www-form-urlencoded (jeu de caractères UTF-8) et que les paires clé/valeur seront sérialisées comme suit : key1=value1&amp;key2=value2&amp;…
   * &#39;json&#39; : signifie que le type de contenu sera application/json (jeu de caractères UTF-8) et que les paires clé-valeur seront sérialisées sous la forme d’un objet json, tel quel : _{ &quot;key1&quot;: &quot;value1&quot;, &quot;key2&quot;: &quot;value2&quot;, ...}_

### Définition de la méthode d’injection du jeton d’accès dans la requête HTTP de l’action{#custom-authentication-access-token}

* authorizationType : définit la manière dont le jeton d’accès généré doit être injecté dans l’appel HTTP pour l’action. Les valeurs possibles sont les suivantes :

   * bearer : indique que le jeton d’accès doit être injecté dans l’en-tête Authorization ; par exemple, _Authorization: Bearer &lt;jeton d’accès>_
   * header : indique que le jeton d’accès doit être injecté en tant qu’en-tête ; nom d’en-tête défini par la propriété tokenTarget. Par exemple, si la propriété tokenTarget est myHeader, le jeton d’accès est injecté sous la forme d’un en-tête : _myHeader: &lt;jeton d’accès>_.
   * queryParam : indique que le jeton d’accès doit être injecté en tant que queryParam, le nom du paramètre de requête défini par la propriété tokenTarget. Par exemple, si le paramètre tokenTarget est myQueryParam, l’URL de l’appel d’action est _&lt;url>?myQueryParam=&lt;jeton d’accès>_

* tokenInResponse : indique comment extraire le jeton d’accès de l’appel d’authentification. Cette propriété peut être :
   * &#39;response&#39; : indique que la réponse HTTP est le jeton d’accès.
   * Un sélecteur dans un fichier json (en supposant que la réponse soit au format JSON ; les autres formats, comme XML, ne sont pas pris en charge). Le format de ce sélecteur est _json://&lt;chemin d’accès à la propriété du jeton d’accès>_. Par exemple, si la réponse de l’appel est _{ &quot;access_token&quot;: &quot;theToken&quot;, &quot;timestamp&quot;: 12323445656 }_, tokenInResponse sera _json: //access_token_.

Le format de cette authentification est le suivant :

```
{
    "type": "customAuthorization",
    "endpoint": "<URL of the authentication endpoint>",
    "method": "<HTTP method to call the authentication endpoint, in 'GET' or 'POST'>",
    (optional) "headers": {
        "<header name>": "<header value>",
        ...
    },
    (optional, mandatory if method is 'POST') "body": {
        "bodyType": "<'form'or 'json'>,
        "bodyParams": {
            "param1": value1,
            ...
        }
    },
    "tokenInResponse": "<'response' or json selector in format 'json://<field path to access token>'",
    "cacheDuration": {
        (optional, mutually exclusive with 'duration') "expiryInResponse": "<json selector in format 'json://<field path to expiry>'",
        (optional, mutually exclusive with 'expiryInResponse') "duration": <integer value>,
        "timeUnit": "<unit in 'milliseconds', 'seconds', 'minutes', 'hours', 'days', 'months', 'years'>"
    },
    "authorizationType": "<value in 'bearer', 'header' or 'queryParam'>",
    (optional, mandatory if authorizationType is 'header' or 'queryParam') "tokenTarget": "<name of the header or queryParam if the authorizationType is 'header' or 'queryParam'>",
}
```

>[!NOTE]
>
>Encode64 est la seule fonction disponible dans la payload d’authentification.

Vous pouvez modifier la durée de mise en cache du jeton pour une source de données d’authentification personnalisée. Vous trouverez ci-dessous un exemple de payload d’authentification personnalisée. La durée de mise en cache est définie dans le paramètre « cacheDuration ». Elle spécifie la durée de conservation du jeton généré dans le cache. L’unité peut être en millisecondes, secondes, minutes, heures, jours, mois, années.

Voici un exemple pour le type d’authentification du porteur :

```
{
  "authentication": {
    "type": "customAuthorization",
    "authorizationType": "Bearer",
    "endpoint": "https://<your_auth_endpoint>/epsilon/oauth2/access_token",
    "method": "POST",
    "headers": {
      "Authorization": "Basic EncodeBase64(<epsilon Client Id>:<epsilon Client Secret>)"
    },
    "body": {
      "bodyType": "form",
      "bodyParams": {
        "scope": "cn mail givenname uid employeeNumber",
        "grant_type": "password",
        "username": "<epsilon User Name>",
        "password": "<epsilon User Password>"
      }
    },
    "tokenInResponse": "json://access_token",
    "cacheDuration": {
      "duration": 5,
      "timeUnit": "minutes"
    }
  }
}
```

>[!NOTE]
>
>Le jeton d’authentification est mis en cache par parcours : si deux parcours utilisent la même action personnalisée, chaque parcours dispose de son propre jeton mis en cache. Ce jeton n’est pas partagé entre ces parcours.
>
>La durée de mise en cache permet d’éviter un trop grand nombre d’appels aux points d’entrée d’authentification. La rétention des jetons d’authentification est mise en cache dans les services, il n’y a aucune persistance. Si un service est redémarré, il commence par un cache propre. Par défaut, la durée de mise en cache est de 1 heure. Dans la payload de l’authentification personnalisée, elle peut être adaptée en spécifiant une autre durée de rétention.
>

Voici un exemple pour le type d’authentification de l’en-tête :

```
{
  "type": "customAuthorization",
  "authorizationType": "header",
  "tokenTarget": "x-auth-token",
  "endpoint": "https://myapidomain.com/v2/user/login",
  "method": "POST",
  "headers": {
    "x-retailer": "any value"
  },
  "body": {
    "bodyType": "form",
    "bodyParams": {
      "secret": "any value",
      "username": "any value"
    }
  },
  "tokenInResponse": "json://token",
  "cacheDuration": {
    "expiryInResponse": "json://expiryDuration",
    "timeUnit": "minutes"
  }
}
```

Voici un exemple de réponse de l’appel API de connexion :

```
{
  "token": "xDIUssuYE9beucIE_TFOmpdheTqwzzISNKeysjeODSHUibdzN87S",
  "expiryDuration" : 5
}
```
