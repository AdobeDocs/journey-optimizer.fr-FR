---
title: Implémentation d’applications monopages
description: Découvrez comment mettre en œuvre les vues SPA dans Journey Optimizer.
feature: Web Channel
topic: Content Management
role: User
level: Intermediate
exl-id: c36d793d-0aa6-4a7a-94f2-dbfe6b644df8
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 100%

---

# Implémenter des applications monopages (SPA) {#web-spa-implementation}

Le SDK Web d’Adobe Experience Platform offre des fonctionnalités riches qui permettent à votre entreprise de personnaliser les technologies de nouvelle génération côté client, telles que les applications monopages (SPA).

Les sites web traditionnels fonctionnaient sur des modèles de navigation « page à page », appelés également applications multi-pages dans lesquelles les conceptions de site web étaient étroitement couplées à des URL et les transitions d’une page web à une autre nécessitaient un chargement de page.

Les applications web modernes, comme les applications monopages, adoptent plutôt un modèle qui projette rapidement le rendu de l’interface utilisateur du navigateur, ce qui est souvent indépendant des rechargements de page. Ces expériences peuvent être déclenchées par des interactions client, comme faire défiler, cliquer et faire bouger le curseur. À mesure de l’évolution des paradigmes du Web moderne, la pertinence des événements génériques traditionnels, comme le chargement des pages, pour déployer la personnalisation et les expériences ne fonctionnent plus.

![](assets/web-spa-vs-traditional-lifecycle.png)

## Avantages du SDK Web Adobe Experience Platform pour les SPA {#web-spa-benefits}

Voici quelques avantages offerts par le SDK Web Adobe Experience Platform pour vos applications monopages :

* Capacité à mettre en cache toutes les offres au chargement de la page afin de passer de plusieurs appels au serveur à un seul appel au serveur.
* Amélioration considérable de l’expérience client sur votre site, car les offres sont immédiatement affichées via le cache, sans délai par les appels tradictionnels au serveur.
* La configuration unique des développeurs et développeuses permet aux spécialistes du marketing de créer et d’exécuter des activités de personnalisation et d’expérimentation via l’éditeur visuel web Adobe Journey Optimizer sur votre SPA.

## Vues XDM et applications monopages {#web-spa-xdm}

L&#39;éditeur web Adobe **[!UICONTROL Journey Optimizer]** tire parti d’un concept appelé Vues : un groupe logique d’éléments visuels qui, ensemble, forment une expérience pour application monopage. Une application monopage peut donc être considérée comme une transition entre les vues (et pas entre les URL) basée sur les interactions des utilisateurs et utilisatrices. Une vue peut généralement représenter un site entier, une seule page ou des éléments visuels regroupés dans une page.

Pour montrer plus de détails sur les vues, l’exemple suivant utilise un hypothétique site d’e-commerce.

* Après avoir accédé au site d’accueil, une image principale fait la promotion de collections saisonnières ainsi que des différents catalogues de produits disponibles sur le site. Dans ce cas, une vue peut être définie pour la totalité de l’écran d’accueil. Cette vue pourrait simplement être nommée « accueil ».

  ![](assets/web-spa-home.png)

* À mesure que le client ou la cliente s’intéresse de plus en plus aux produits de l’entreprise, il ou elle décide de cliquer sur le lien **Hommes**. Comme pour la page d’accueil, l’intégralité de la page **Hommes** peut être définie comme une vue. Cette vue pourrait être nommée « hommes ».

  ![](assets/web-spa-men.png)

* Étant donné qu’une vue peut être définie comme un site entier ou un groupe d’éléments visuels sur un site, les quatre produits affichés sur le site de produits peuvent être regroupés et considérés comme une vue. Cette vue pourrait être nommée « produits ».

  ![](assets/web-spa-men-products.png)

* Lorsque le client ou la cliente décide de cliquer sur le bouton **TOUS LES PRODUITS POUR HOMMES** pour voir d’autres produits sur le site, l’URL du site web ne change pas dans ce cas, mais une vue peut être créée ici pour représenter uniquement la deuxième ligne des produits affichés. Le nom de la vue pourrait être « page-produits-2 ».

* Le client ou la cliente décide d’acheter quelques produits sur le site et passe à l’écran de passage en caisse. L’écran du panier lui-même peut être associé à une vue nommée « panier ». Vous pouvez également disposer d’une vue différente dans l’écran de passage en caisse pour afficher les produits recommandés en dessous.

  ![](assets/web-spa-cart.png)

Le concept de vues peut être étendu bien plus loin. Ce ne sont que quelques exemples de vues qui peuvent être définies sur un site.

## Implémenter des vues XDM {#implement-xdm-views}

Les vues XDM peuvent être utilisées dans Adobe Journey Optimizer pour permettre aux spécialistes du marketing de lancer des campagnes de personnalisation et d’expérimentation web sur une application monopage via l’éditeur visuel web Journey Optimizer.

Pour effectuer une configuration de développeur ou développeuse unique, procédez comme suit :

1. Installez le [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=fr){target="_blank"} et vérifiez la page [Conditions préalables pour le canal web](web-prerequisites.md).

2. Déterminez toutes les vues XDM de votre application monopage que vous souhaitez personnaliser.

3. Après avoir défini les vues XDM, vous devez implémenter la fonction `sendEvent()` avec `renderDecisions` défini sur `true` et la vue XDM correspondante dans votre application monopage pour leur diffuser du contenu. La vue XDM doit être transmise dans `xdm.web.webPageDetails.viewName`. Cette étape permet aux spécialistes du marketing de découvrir ces vues dans l’éditeur web de Journey Optimizer et d’y appliquer des modifications de contenu :

```
 alloy("sendEvent", {
  "renderDecisions": true,
  "xdm": {
   "web": {
    "webPageDetails": {
    "viewName":"home"
   }
  }
 }
});
```

>[!NOTE]
>
>Au premier appel `sendEvent()`, toutes les vues XDM qui doivent être rendues à l’utilisateur ou l’utilisatrice finale seront récupérées et mises en cache. Les appels `sendEvent()` suivants avec des vues XDM transmises seront lus à partir du cache et rendus sans appel au serveur.

## Exemples de fonctions `sendEvent()`

Cette section présente deux exemples montrant comment invoquer la fonction `sendEvent()` dans React pour une application monopage hypothétique d’e-commerce.

### Exemple 1 : page d’accueil du test A/B {#web-spa-sample-1}

L’équipe marketing souhaite exécuter des tests A/B sur l’ensemble de la page d’accueil.

![](assets/web-spa-home.png)

Pour exécuter des tests A/B sur l’ensemble du site d’accueil, `sendEvent()` doit être appelé avec `viewName` XDM défini sur `home` :

```
function onViewChange() {

  var viewName = window.location.hash; // or use window.location.pathName if router works on path and not hash

  viewName = viewName || 'home'; // view name cannot be empty

  // Sanitize viewName to get rid of any trailing symbols derived from URL

  if (viewName.startsWith('#') || viewName.startsWith('/')) {
    viewName = viewName.substr(1);
  }

  alloy("sendEvent", {
    "renderDecisions": true,

    "xdm": {
      "web": {
        "webPageDetails": {
          "viewName":"home"
        }
      }
    }
  });
}

// react router v4

const history = syncHistoryWithStore(createBrowserHistory(), store);

history.listen(onViewChange);

// react router v3

<Router history={hashHistory} onUpdate={onViewChange} >
```

### Exemple 2 : produits personnalisés {#web-spa-sample-2}

L’équipe marketing souhaite personnaliser la deuxième ligne de produits en définissant la couleur du libellé du prix en rouge après qu’un utilisateur ou une utilisatrice a cliqué pour afficher tous les produits Hommes.

![](assets/web-spa-men-products.png)

```
function onViewChange(viewName) {

  alloy("sendEvent", {
    "renderDecisions": true,
    "xdm": {
      "web": {
        "webPageDetails": {
          "viewName": viewName
        }
      }
    }
  });
}

class Products extends Component {

  render() {
    return (

        <button type="button" onClick={this.handleLoadMoreClicked}>All Men's Products</button>
    );
  }

  handleLoadMoreClicked() {
    var page = this.state.page + 1; // assuming page number is derived from component's state
    this.setState({page: page});
    onViewChange('PRODUCTS-PAGE-' + page);
  }

}
```
