---
solution: Journey Optimizer
product: journey optimizer
title: Personnaliser les URL dans les e-mails
description: Découvrez les bonnes pratiques et les limites de la génération dynamique d’URL tout en maintenant un tracking fiable
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: url, lien, personnalisation, tracking, codage, accolades
source-git-commit: 36fad8d6c200118210794249fa12263ae70e5422
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 14%

---

# Personnaliser les URL dans les e-mails {#url-personalization}

Les URL personnalisées vous permettent de diffuser des expériences contextuelles par le biais de vos e-mails [!DNL Journey Optimizer], comme la génération de liens spécifiques aux destinataires ou l’ajout de paramètres dynamiques.

Ils orientent les destinataires vers des pages spécifiques d’un site web ou vers un microsite personnalisé, en fonction des attributs du profil.

## Personnaliser une URL {#personalize-url}

Pour personnaliser une URL, procédez comme suit.

1. Dans le Designer Email, sélectionnez un élément dans le contenu et [insérez un lien](message-tracking.md#insert-links) à l&#39;aide de la barre d&#39;outils contextuelle.

   >[!IMPORTANT]
   >
   >Personalization n’est disponible que pour les **[!DNL Opt-Out]** **[!UICONTROL Lien externe]**, **[!UICONTROL Lien de désinscription]** et . Veillez à sélectionner un type de lien approprié.

1. Sélectionnez l’icône de personnalisation.

   ![](assets/message-tracking-insert-link-perso.png)

1. Utilisez l’éditeur de personnalisation pour ajouter les attributs de profil avec lesquels vous souhaitez personnaliser l’URL.

1. Enregistrez vos modifications.

Voici quelques exemples d’URL personnalisées :

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!NOTE]
>
>Lorsque vous modifiez une URL personnalisée dans l’éditeur de personnalisation, les fonctions d’assistance et l’appartenance aux audiences sont désactivées pour des raisons de sécurité.
>
>Les espaces ne sont pas pris en charge dans les jetons de personnalisation utilisés dans les URL.

Pour un rendu et un suivi fiables, suivez les [bonnes pratiques et mécanismes de sécurisation](#best-practices) ci-dessous.

## Personnaliser une URL complète/de base {#personalize-complete-base-url}

Journey Optimizer prend également en charge la personnalisation de l’URL **entière** ou du **domaine de base** d’une URL, par exemple :

```html
<a href="{{profile.social.link}}" />
<a href="{{profile.social.baseUrl}}/profile" />
<a href="https://{{profile.social.baseUrl}}/profile" />
```

>[!IMPORTANT]
>
>Pour activer la personnalisation complète ou de base de l’URL, contactez Adobe et fournissez votre liste de domaines acceptés. Cela est nécessaire pour éviter les redirections non sécurisées.

## Personnaliser les paramètres de tracking d’URL {#personalize-url-tracking-parameters}

Le [tracking des URL](url-tracking.md) est géré au niveau de la configuration des canaux et s&#39;applique à toutes les URL incluses dans le contenu de votre message. Vous pouvez également personnaliser les paramètres de tracking d’URL d’un lien individuel dans le Designer Email. Vous pouvez ainsi ajouter un paramètre spécifique au destinataire à un seul lien (par exemple, pour transmettre un identifiant à vos outils d’analyse web).

Pour ce faire, [insérez un lien](message-tracking.md#insert-links), sélectionnez l’icône de personnalisation, ajoutez le paramètre de tracking des URL et sélectionnez l’attribut de profil de votre choix dans l’[éditeur de personnalisation](../personalization/personalization-build-expressions.md).

![](assets/message-tracking-perso-parameter.png)

Répétez les étapes ci-dessus pour chaque lien auquel vous souhaitez ajouter ce paramètre de tracking.

Désormais, lorsque l’e-mail est envoyé, ce paramètre est automatiquement ajouté à la fin de l’URL. Vous pouvez ensuite capturer ce paramètre dans les outils d’analyse web ou dans les rapports de performances.

>[!NOTE]
>
>Pour vérifier l’URL finale, vous pouvez [envoyer un BAT](../content-management/proofs.md) et cliquer sur le lien dans le contenu de l’e-mail une fois que vous avez reçu le BAT. L’URL doit afficher le paramètre de tracking. Par exemple : <https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>

## Bonnes pratiques et mécanismes de sécurisation {#best-practices}

Pour que les liens restent valides, cliquables et traçables, suivez les bonnes pratiques et les mécanismes de sécurisation ci-dessous.

### Accolades pour les URL dynamiques {#use-braces}

Lors de l’insertion d’une URL contenant des éléments de personnalisation, utilisez trois accolades (`{{{ ... }}}`) pour la partie dynamique de l’URL. Cela empêche l’échappement de modifier les caractères spéciaux (par exemple `/` et `+`) et permet d’éviter les URL rompues, les redirections incorrectes ou les problèmes de suivi.

Voici un exemple :

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>L’utilisation de la sortie brute (`{{{ ... }}}`) signifie que la valeur est insérée en l’état. Utilisez-le uniquement avec des valeurs de confiance et conçues pour être sécurisées par une URL (par exemple, les valeurs que vous générez ou validez en amont).

### Tracking correct des URL {#enable-url-tracking}

* Lors de l’utilisation de la personnalisation pour générer l’URL, assurez-vous que la valeur résolue commence par `http`/`https` pour chaque destinataire. Dans le cas contraire, le tracking risque de ne pas être appliqué et le lien risque de ne pas se comporter comme prévu.

* N’utilisez pas de logique dynamique telle que des instructions `let`, `each` ou `if` directement dans le champ URL de l’éditeur de personnalisation. Elles sont désactivées pour des raisons de sécurité.

* Si votre scénario implique une logique complexe pour générer des URL personnalisées, évitez de placer cette logique directement dans le champ URL de l’éditeur de personnalisation. Au lieu de cela :
   * Ajoutez la logique et les instructions nécessaires dans le contenu HTML au-dessus ou à proximité du champ URL.
   * Générez et stockez séparément les attributs personnalisés, puis référencez-les dans le contenu de votre e-mail.

### Encodage et longueur de l’URL {#encoding}

* Les règles de syntaxe URI ([norme RFC 3986](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}) s’appliquent à toutes les URL de votre contenu d’e-mail. Cependant, les URL personnalisées sont plus susceptibles de présenter des problèmes de codage, car les valeurs spécifiques au destinataire peuvent introduire des caractères réservés (par exemple dans les paramètres de requête). Par conséquent, assurez-vous que vos valeurs dynamiques sont codées URL (en particulier les espaces, les `&`, les `#`, les `%` et les `+`) et évitez d’utiliser des `+` pour les valeurs de requête.

* Les URL très longues peuvent être tronquées ou rejetées par les navigateurs, les clients de messagerie ou les systèmes en aval. Par exemple, les URL de page miroir peuvent augmenter considérablement lorsque la personnalisation d’exécution est importante. Veillez à ce que les payloads personnalisées soient petites et évitez d’incorporer des objets volumineux dans des URL.

### Étapes de validation recommandées {#validation}

Avant d’activer un parcours ou une campagne, suivez les recommandations ci-dessous :

* Envoyez un [BAT](../content-management/proofs.md) et cliquez sur les liens pour confirmer que l’URL résolue commence par `http`/`https` et conserve la structure attendue.
* Si des paramètres de tracking sont ajoutés, confirmez que l’URL finale les inclut (via les paramètres de tracking d’URL au niveau de la configuration ou les paramètres de tracking par lien).

