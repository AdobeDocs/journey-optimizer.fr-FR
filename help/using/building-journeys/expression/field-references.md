---
solution: Journey Optimizer
product: journey optimizer
title: Références de champ
description: En savoir plus sur les références de champ dans les expressions avancées
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: parcours, champ, expression, événement
exl-id: 2348646a-b205-4b50-a08f-6625e92f44d7
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 96%

---

# Références de champ {#field-references}

Il est possible d’associer une référence de champ à un événement ou à un groupe de champs. Les seules informations significatives sont le nom du champ et son chemin d’accès.

Si vous utilisez des caractères spéciaux dans un champ, vous devez utiliser des guillemets doubles ou des guillemets simples. Voici les cas où les guillemets sont nécessaires :

* Le champ commence par des caractères numériques.
* Le champ commence par le caractère « - ».
* Le champ contient d’autres caractères que : _a_-_z_, _A_-_Z_, _0_-_9_, _ , _-_

Par exemple, si votre champ est _3h_: _#{OpenWeather.weatherData.rain.&#39;3h&#39;} > 0_

```json
// event field
@event{<event name>.<XDM path to the field>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id}

// field group
#{<data source name>.<field group name>.<path to the field>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address}
```

Dans l’expression, les champs d’événement sont référencés par « @ » et les champs de source de données par « # ».

Une couleur de syntaxe permet de distinguer visuellement les champs d’événements (vert) des groupes de champs (bleu).

## Valeurs par défaut des références de champ {#default-value}

Il est possible d’associer une valeur par défaut à un nom de champ. La syntaxe se présente comme suit :

```json
// event field
@event{<event name>.<XDM path to the field>, defaultValue: <default value expression>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue: "example@adobe.com"}
// field group
#{<data source name>.<field group name>.<path to the field>, defaultValue: <default value expression>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address, defaultValue: "example@adobe.com"}
```

>[!NOTE]
>
>Le type du champ et la valeur par défaut doivent être identiques. Par exemple, `@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue : 2}` n’est pas valide, car la valeur par défaut est un entier alors que la valeur attendue doit être une chaîne.

Exemples :

```json
// for an event 'OrderEvent' having the following payload:
{
    "orderId": "12345"
}
 
expression example:
- @event{OrderEvent.orderId}                                    -> "12345"
- @event{OrderEvent.producdId, defaultValue : "not specified" } -> "not specified" // default value, productId is not a field present in the payload
- @event{OrderEvent.productId}                                  -> null
 
 
// for an entity 'Profile' on datasource 'ACP' having fields person/lastName, with fetched data such as:
{
    "person": {
        "lastName":"Snow"
    },
    "emails": [
        { "email":"john.snow@winterfell.westeros" },
        { "email":"snow@thewall.westeros" }
    ]
}
 
expression examples:
- #{ACP.Profile.person.lastName}                 -> "Snow"
- #{ACP.Profile.emails.at(1).email}              -> "snow@thewall.westeros"
- #{ACP.Profile.person.age, defaultValue : -1}   -> -1 // default value, age is not a field present in the payload
- #{ACP.Profile.person.age}                      -> null
```

Vous pouvez ajouter n&#39;importe quel type d&#39;expression comme valeur par défaut. La seule contrainte est que l&#39;expression doit renvoyer le type de données attendu. Lors de l&#39;utilisation d&#39;une fonction, l’encapsulation de la fonction avec () est requise.

```
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.any.time, defaultValue : (now())} 
== date("2022-02-10T00:00:00Z")
```

## Référence à un champ dans les collections

Les éléments définis dans les collections sont référencés à l’aide des fonctions spécifiques `all`, `first` et `last`. Pour plus d’informations, consultez [cette page](../expression/collection-management-functions.md).

Exemple :

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all()
```

## Référence à un champ défini dans un mapping

### Fonction `entry`

Pour récupérer un élément dans un mapping, il faut utiliser la fonction d’entrée avec une clé donnée. Elle est par exemple utilisée lors de la définition de la clé d’un événement, selon l’espace de noms sélectionné. Pour plus d’informations, consultez [cette page](../../event/about-creating.md#select-the-namespace).

```json
@event{MyEvent.identityMap.entry('Email').first().id}
```

Dans cette expression, nous obtenons l’entrée correspondant à la clé « E-mail » du champ « IdentityMap » d’un événement. L’entrée « E-mail » est une collection, dans laquelle nous obtenons l’« id » dans le premier élément en utilisant « first() ». Pour plus d’informations, consultez [cette page](../expression/collection-management-functions.md).

### Fonction `firstEntryKey`

Pour récupérer la première clé d’entrée d’un mappage, utilisez la fonction `firstEntryKey`. 

Cet exemple montre comment récupérer la première adresse e-mail des abonnés d’une liste spécifique :

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
```

Dans cet exemple, la liste d’abonnements est nommée `daily-email`. Les adresses e-mail sont définies comme des clés dans le mappage `subscribers`, qui est lié au mappage de la liste d’abonnements. 

### Fonction `keys`

Pour récupérer toutes les clés d’un mapping, utilisez la fonction `keys`. 

Cet exemple montre comment récupérer, pour un profil spécifique, toutes les adresses e-mail associées aux abonnés d’une liste spécifique :

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-mail').subscribers.keys()
```

## Valeurs de paramètre d’une source de données (valeurs dynamiques de la source de données)

Si vous sélectionnez un champ d’une source de données externe qui nécessite l’appel d’un paramètre, un nouvel onglet s’affiche à droite pour vous permettre de spécifier ce paramètre. Consultez [cette page](../expression/expressionadvanced.md).

Dans les cas d’utilisation plus complexes, si vous souhaitez inclure les paramètres de la source de données dans l’expression principale, vous pouvez définir leurs valeurs à l’aide du mot-clé _params_. Un paramètre peut être constitué de n’importe quelle expression valide, même provenant d’une autre source de données contenant également un autre paramètre.

>[!NOTE]
>
>Lorsque vous définissez les valeurs de paramètre dans l’expression, l’onglet de droite disparaît. 

Utilisez la syntaxe suivante :

```json
#{<datasource>.<field group>.fieldName, params: {<params-1-name>: <params-1-value>, <params-2-name>: <params-2-value>}}
```

* **`<params-1-name>`** : nom exact du premier paramètre de la source de données.
* **`<params-1-value>`** : valeur du premier paramètre. Il peut s’agir de n’importe quelle expression valide.

Exemple :

```json
#{Weather.main.temperature, params: {localisation: @event{Profile.address.localisation}}}
#{Weather.main.temperature, params: {localisation: #{GPSLocalisation.main.coordinates, params: {city: @event{Profile.address.city}}}}}
```
