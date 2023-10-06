---
title: Implémentation d’applications d’une seule page
description: Découvrez comment mettre en oeuvre SPA vues dans Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Intermediate
exl-id: c36d793d-0aa6-4a7a-94f2-dbfe6b644df8
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 3%

---

# Mise en oeuvre d’applications d’une seule page (SPA) {#web-spa-implementation}

Le SDK Web de Adobe Experience Platform offre des fonctionnalités riches qui permettent à votre entreprise d’exécuter la personnalisation sur les technologies côté client de nouvelle génération, telles que les applications d’une seule page (SPA).

Les sites web traditionnels fonctionnent sur des modèles de navigation &quot;page à page&quot;, également appelés applications multi-pages, où les conceptions de site web sont étroitement couplées à des URL et les transitions d’une page web à une autre nécessitent un chargement de page.

Les applications web modernes, telles que les applications d’une seule page (SPA), ont adopté à la place un modèle qui propulse l’utilisation rapide du rendu de l’interface utilisateur du navigateur, souvent indépendant des rechargements de page. Ces expériences peuvent être déclenchées par des interactions client, telles que des défilés, des clics et des mouvements de curseur. À mesure que les paradigmes du web moderne évoluent, la pertinence des événements génériques traditionnels, tels qu’un chargement de page, pour déployer la personnalisation et l’expérimentation ne fonctionne plus.

![](assets/web-spa-vs-traditional-lifecycle.png)

## Avantages du SDK Web Adobe Experience Platform pour SPA {#web-spa-benefits}

Voici quelques avantages de l’utilisation du SDK Web Adobe Experience Platform pour vos applications d’une seule page :

* Capacité à mettre en cache toutes les offres au chargement de la page afin de passer de plusieurs appels serveur à un seul appel serveur.
* Améliorez considérablement l’expérience utilisateur de votre site, car les offres sont immédiatement affichées via le cache sans délai intégré aux appels serveur traditionnels.
* La configuration unique des développeurs permet aux marketeurs de créer et d’exécuter des activités de personnalisation et d’expérimentation via l’éditeur visuel web Adobe Journey Optimizer sur votre SPA.

## Vues XDM et applications d’une seule page {#web-spa-xdm}

L&#39;Adobe **[!UICONTROL Journey Optimizer]** l’éditeur web tire parti d’un concept appelé vues : un groupe logique d’éléments visuels qui, ensemble, constituent une expérience SPA. Une application d’une seule page peut donc être considérée comme une transition entre les vues, au lieu des URL, selon les interactions de l’utilisateur. Une vue peut généralement représenter un site entier, une seule page ou des éléments visuels regroupés dans une page.

Pour expliquer plus en détail les vues, l’exemple suivant utilise un hypothétique site de commerce électronique.

* Après avoir accédé au site d’accueil, une image principale fait la promotion de collections saisonnières ainsi que des différents catalogues de produits disponibles sur le site. Dans ce cas, une vue peut être définie pour l’ensemble de l’écran d’accueil. Ce point de vue pourrait simplement être appelé &quot;maison&quot;.

  ![](assets/web-spa-home.png)

* À mesure que le client s’intéresse de plus en plus aux produits que l’entreprise vend, il décide de cliquer sur le bouton **Hommes** lien. Tout comme la page d’accueil, l’intégralité de la variable **Hommes** peut être définie comme une vue. Ce point de vue pourrait être appelé &quot;men&quot;.

  ![](assets/web-spa-men.png)

* Une vue pouvant être définie comme un site entier ou un groupe d’éléments visuels sur un site, les quatre produits affichés sur le site de produits peuvent être regroupés et considérés comme une vue. Cette vue peut être appelée &quot;produits&quot;.

  ![](assets/web-spa-men-products.png)

* Lorsque le client décide de cliquer sur la variable **TOUS LES PRODUITS POUR HOMMES** pour explorer d’autres produits sur le site, l’URL du site web ne change pas dans ce cas, mais une vue peut être créée ici pour représenter uniquement la deuxième ligne des produits affichés. Le nom de la vue peut être &quot;products-page-2&quot;.

* Le client décide d’acheter quelques produits sur le site et passe à l’écran de passage en caisse. L’écran du panier lui-même peut être associé à une vue nommée &quot;panier&quot;. Vous pouvez également disposer d’une vue différente dans l’écran de passage en caisse pour gérer les produits recommandés ci-dessous.

  ![](assets/web-spa-cart.png)

Le concept de vision peut être étendu bien plus loin que cela. Ce ne sont que quelques exemples de vues qui peuvent être définies sur un site.

## Implémentation des vues XDM {#implement-xdm-views}

Les vues XDM peuvent être exploitées dans Adobe Journey Optimizer pour permettre aux marketeurs d’exécuter des campagnes de personnalisation et d’expérimentation web sur SPA via l’éditeur visuel web Journey Optimizer.

Pour effectuer une configuration de développeur unique, procédez comme suit :

1. Installer [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=fr){target="_blank"} et vérifiez la variable [conditions préalables pour le canal web](web-prerequisites.md) page.

2. Déterminez toutes les vues XDM de votre application d’une seule page que vous souhaitez personnaliser.

3. Après avoir défini les vues XDM, vous devez mettre en oeuvre la variable `sendEvent()` fonction avec `renderDecisions` défini sur `true` et la vue XDM correspondante dans votre application d’une seule page. La vue XDM doit être transmise `xdm.web.webPageDetails.viewName`. Cette étape permet aux marketeurs de découvrir ces vues dans l’éditeur web de Journey Optimizer et d’y appliquer des modifications de contenu :

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
>Le premier `sendEvent()` tous les affichages XDM qui doivent être rendus à l’utilisateur final seront récupérés et mis en cache. Suivant `sendEvent()` Les appels avec des vues XDM transmises seront lus à partir du cache et rendus sans appel au serveur.

## `sendEvent()` exemples de fonctions

Cette section présente deux exemples d’appel de la méthode `sendEvent()` dans React pour une SPA de commerce électronique hypothétique.

### Exemple 1 : page d’accueil du test A/B {#web-spa-sample-1}

L’équipe marketing souhaite exécuter des tests A/B sur l’ensemble de la page d’accueil.

![](assets/web-spa-home.png)

Pour exécuter des tests A/B sur l’ensemble du site d’accueil, `sendEvent()` doit être appelé avec XDM `viewName` défini sur `home`:

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

### Exemple 2 : produits personnalisés {#web-spa-sample-2}

L’équipe marketing souhaite personnaliser la deuxième ligne de produits en définissant la couleur du libellé du prix sur rouge après qu’un utilisateur ait cliqué pour afficher tous les produits Men.

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
