---
title: Configuration de la prise en charge de la messagerie web in-app dans Web SDK
description: Découvrez comment configurer l’extension de balise Web SDK pour prendre en charge la messagerie Web in-app.
feature: In App
topic: Content Management
role: Developer
level: Intermediate
keywords: in-app, message, sdk web, configuration
source-git-commit: 4a7f98ce24af02658620485840d11190c0954c09
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 1%

---

# Configuration de la prise en charge de la messagerie web in-app dans Web SDK

Les messages in-app sont des notifications que vous pouvez envoyer aux utilisateurs et utilisatrices dans votre application web, les guidant vers des points ciblés spécifiques.

Vous pouvez utiliser ces notifications à différentes fins, par exemple pour promouvoir de nouvelles fonctionnalités, présenter des offres spéciales ou faciliter l’intégration des utilisateurs et utilisatrices.

En utilisant les messages in-app, vous pouvez interagir efficacement avec votre audience et l’orienter vers des aspects importants de votre application.

## Conditions préalables {#prerequisites}

### Version de l’extension de balise Web SDK {#extension-version}

La fonctionnalité de messagerie Web in-app nécessite la dernière version de l’extension de balise Web SDK.

### Configuration d’un CSP pour la messagerie web in-app {#csp}

Lorsque vous configurez la messagerie Web In-App, vous devez inclure la directive suivante dans votre CSP :

```
default-src  blob:;
```

Pour plus d’informations sur la configuration d’une CSP, consultez la [documentation sur la collecte de données](https://experienceleague.adobe.com/docs/experience-platform/edge/use-cases/configuring-a-csp.html){target="_blank"}.

## Configuration de la messagerie Web In-App à l’aide de l’extension de balise Web SDK {#tag-extension}

Reportez-vous à la page [Configuration de l’extension de balise Web SDK](https://experienceleague.adobe.com/fr/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration){target="_blank"} pour savoir où trouver les paramètres décrits ci-dessous.

Après avoir [installé](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html#install-the-web-sdk-tag-extension){target="_blank"} l’extension de balise Web SDK, suivez les étapes ci-dessous pour configurer l’extension pour la messagerie web in-app.

Dans la section ****, cochez l&#39;option **[!UICONTROL Activer le stockage de personnalisation]**. Cette option permet au SDK Web de suivre les expériences qui ont été vues par l’utilisateur ou l’utilisatrice à travers les chargements de page.

![Image illustrant l’option de stockage de la personnalisation dans la page de configuration de l’extension de balise.](assets/enable-personalization-storage.png)

La messagerie web in-app prend en charge deux types de déclencheurs :

* [Envoi de données à Experience Platform](#send-data-platform)
* [Déclenchement manuel des messages](#manual-trigger)

Reportez-vous aux sections suivantes pour configurer l’extension de balise Web SDK en fonction des déclencheurs que vous souhaitez utiliser.

### Étapes de configuration du déclencheur **[!UICONTROL Envoyer les données à Experience Platform]** {#send-data-platform}

1. Sélectionnez la propriété de balise qui contient votre extension Web SDK et [créez une règle](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/managing-resources/rules.html#create-a-rule){target="_blank"} avec les paramètres suivants :

   * **[!UICONTROL Extension]** : [!UICONTROL Core]
   * **[!UICONTROL Type D’Événement]** : [!UICONTROL Bibliothèque Chargée (Haut De Page)]

   ![Image illustrant l’écran de configuration de l’événement.](assets/rule-configuration.png)

1. Sélectionnez **[!UICONTROL Conserver les modifications]** pour enregistrer la configuration de l’événement.

1. Vous devez maintenant ajouter une action à la règle que vous avez créée. Dans la section [!DNL Actions], sélectionnez **[!UICONTROL Ajouter]**.

   Utilisez les paramètres **[!UICONTROL Action]** suivants :

   * **[!UICONTROL Extension]** : [!UICONTROL Adobe Experience Platform Web SDK]
   * **[!UICONTROL Type d’action]** : [!UICONTROL Envoyer l’événement]

   ![Image illustrant l’écran Modifier la règle.](assets/add-action.png)

1. Dans la partie droite de l’écran, dans la section ****, activez l’option **[!UICONTROL Rendre les décisions de personnalisation visuelle]**.

   ![Image illustrant l’écran de configuration de la personnalisation.](assets/render-visual-personalization.png)

1. Dans la partie droite de l’écran, dans la section **[!UICONTROL Contexte de décision]**, définissez les paires **[!UICONTROL Clé]**/**[!UICONTROL Valeur]** que vous avez utilisées dans la configuration de votre campagne, pour être qualifiées pour le message in-app.

   ![Image illustrant l’écran de configuration de la personnalisation.](assets/decision-context.png)

1. Sélectionnez **[!UICONTROL Conserver les modifications]** pour enregistrer votre configuration.

1. Vous devez ensuite ajouter la règle nouvellement créée à la bibliothèque de propriétés de balises. Pour ce faire, accédez à **[!UICONTROL Flux de publication]** et sélectionnez la règle que vous avez précédemment créée.

   ![Image illustrant l’écran de la bibliothèque.](assets/add-rule-to-library.png)

1. Après avoir ajouté la règle à la bibliothèque, sélectionnez **[!UICONTROL Enregistrer et créer dans le développement]**.

   ![Image illustrant l’écran de configuration de la personnalisation.](assets/publish-flow.png)

Le processus de configuration est maintenant terminé et votre message est prêt à être affiché à vos utilisateurs.

### Étapes de configuration pour l’utilisation de déclencheurs manuels {#manual-trigger}

1. Sélectionnez la propriété de balise qui contient votre extension Web SDK, puis [créez une règle](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/managing-resources/rules.html#create-a-rule){target="_blank"} avec les paramètres suivants :

   * **[!UICONTROL Extension]** : [!UICONTROL Core]
   * **[!UICONTROL Type D’Événement]** : [!UICONTROL Clic]

1. Définissez le déclencheur pour un élément spécifique de la page, identifié par un sélecteur CSS de votre choix.

   ![Image illustrant l’écran de configuration de l’événement.](assets/event-configuration-manual.png)

1. Vous devez ajouter une action à la règle que vous avez créée. Dans la section [!DNL Actions], sélectionnez **[!UICONTROL Ajouter]** et utilisez les paramètres **[!UICONTROL Action]** suivants :

   * **[!UICONTROL Extension]** : [!UICONTROL Adobe Experience Platform Web SDK]
   * **[!UICONTROL Type d’action]** : [!UICONTROL évaluation des ensembles de règles]

   ![Image illustrant l’écran Modifier la règle.](assets/add-action.png)

1. Sur le côté droit de l’écran, activez l’option **[!UICONTROL Rendre les décisions de personnalisation visuelle]**.

   ![Image illustrant l’écran de configuration de la personnalisation.](assets/manual-trigger-render.png)

1. Dans la partie droite de l’écran, dans la section **[!UICONTROL Contexte de décision]**, définissez les paires **[!UICONTROL Clé]**/**[!UICONTROL Valeur]** que vous avez utilisées dans la configuration de votre campagne, pour être qualifiées pour le message in-app.

   ![Image illustrant l’écran de configuration de la personnalisation.](assets/manual-trigger-decision-context.png)

1. Sélectionnez **[!UICONTROL Conserver les modifications]** pour enregistrer votre configuration.

1. Ajoutez la règle que vous venez de créer à la bibliothèque de propriétés de balise. Pour ce faire, accédez à **[!UICONTROL Flux de publication]** et sélectionnez la règle que vous avez précédemment créée.

   ![Image illustrant l’écran de la bibliothèque.](assets/add-rule-to-library.png)

1. Après avoir ajouté la règle à la bibliothèque, sélectionnez **[!UICONTROL Enregistrer et créer dans le développement]**.

   ![Image illustrant l’écran de configuration de la personnalisation.](assets/publish-flow.png)

Le processus de configuration est maintenant terminé et votre message est prêt à être affiché à vos utilisateurs.

## Configuration de la messagerie Web In-App à l’aide de la bibliothèque JavaScript Web SDK {#js-library}

Au lieu d’utiliser l’extension de balise Web SDK, vous pouvez également configurer la messagerie Web In-App directement à partir de la bibliothèque JavaScript Web SDK.

Vous pouvez afficher des messages web in-app depuis Adobe Journey Optimizer de deux façons.

### Méthode 1 : récupérer automatiquement le contenu de personnalisation {#automatic}

Pour que Web SDK récupère automatiquement le contenu de personnalisation au chargement de la page, utilisez la commande `sendEvent` , comme illustré dans l’exemple ci-dessous.

```js
  alloy("sendEvent", {
      renderDecisions: true,
      personalization: {
          surfaces: ['#welcome']
      }
  });
```

### Méthode 2 : récupérer manuellement le contenu de personnalisation en fonction de l’action de l’utilisateur {#manual}

Pour afficher le contenu de personnalisation uniquement après que l’utilisateur a effectué une action spécifique, utilisez la commande `evaluateRulesets` comme illustré dans l’exemple ci-dessous.

Dans cet exemple, le contenu de personnalisation s’affiche lorsqu’un utilisateur clique sur le bouton **[!UICONTROL Acheter maintenant]** de votre site web.

```js
 alloy("evaluateRulesets", {
     renderDecisions: true,
     personalization: {
         decisionContext: {
             "userAction": "buy_now"
         }
     }
 });
```

### Configuration du stockage de personnalisation {#personalization-storage}

Vous pouvez choisir d’afficher des messages in-app aux utilisateurs et utilisatrices pour un nombre défini de fois, ou à chaque fois qu’ils ou elles visitent une page, via l’option de configuration `personalizationStorageEnabled`.

Dans la configuration [Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html){target="_blank"} définissez l’option `personalizationStorageEnabled` en fonction de vos besoins :

* `personalizationStorageEnabled: true` déclenche le message in-app avec la fréquence que vous avez définie dans votre [campagne](create-in-app-web.md#configure-inapp).
* `personalizationStorageEnabled: false` déclenche le message in-app à chaque chargement de page.
