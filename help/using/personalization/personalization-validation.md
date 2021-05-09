---
title: Validation de la personnalisation
description: En savoir plus sur la validation de la personnalisation et comment résoudre les problèmes
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Validation de la personnalisation {#personalization-validation}

![](../assets/do-not-localize/badge.png)

## Mécanismes de validation

Dans l’écran de l’éditeur d’Expressions, le bouton **Valider** permet de valider la syntaxe de personnalisation.

>[!NOTE]
> La validation est automatiquement effectuée lorsque vous cliquez sur **Ajouter** pour fermer la fenêtre de l&#39;éditeur.


![](assets/perso_validation1.png)

>[!IMPORTANT]
> Si la syntaxe de personnalisation n’est pas valide, vous ne pouvez pas fermer la fenêtre de l’éditeur d’expressions.


## Erreurs courantes

* **Chemin &quot;XYZ&quot; introuvable**

Lorsque vous essayez de référencer un champ qui n’est pas défini dans le schéma.

Dans ce cas, **firstName1** n&#39;est pas défini comme attribut dans le schéma du profil :

```
{{profile.person.name.firstName1}}
```

* **Incompatibilité de type pour la variable &quot;XYZ&quot;. Tableau attendu. Chaîne trouvée.**

Lorsque vous essayez d’effectuer une itération sur une chaîne plutôt que sur un tableau :

Dans ce cas, **product** n&#39;est pas un tableau :

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Syntaxe des barres de poignées non valide.`‘[XYZ}}’`** trouvé

Lorsque la syntaxe des barres de poignées est incorrecte.

Les expressions de barres de poignées sont entourées de **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **Définition de segment non valide**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

### Erreurs spécifiques liées aux offres

Les erreurs liées à l’intégration des offres dans un message électronique ou Push ont le modèle suivant :

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

La validation est effectuée pendant la publication du message ou pendant la validation du contenu de la personnalisation dans l’éditeur d’Expressions.

<table> 
 <thead> 
  <tr> 
   <th> Titre de l’erreur<br /> </th> 
   <th> Validation / Résolution <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Ressource avec ID placementID et type OfferPlacement introuvable <br/>
Ressource avec ID activityID et type OfferActivity introuvable<br/></td> 
   <td>Vérifiez si l’ID d’activité et/ou l’ID de placement sont disponibles.</td> 
  </tr> 
   <tr> 
   <td>Impossible de valider la ressource.</td> 
   <td>Le componentType dans le Placement doit correspondre à l’offre offerType.</td> 
  </tr> 
   <tr> 
   <td>L’URL publique n’est pas présente dans l’ID d’offre d’offre.</td> 
   <td>Les Offres d’image (toutes personnalisées et de secours associées à la paire de choix et de placement) doivent avoir une URL publique renseignée (l’URL de diffusion ne doit pas être vide).</td> 
  </tr> 
  <tr> 
   <td>La décision (précédemment connue sous le nom d'activité d'offre) contient des attributs non profils.</td> 
   <td>Offres L'utilisation du modèle ne doit contenir que les attributs de profil.</td> 
  </tr> 
  <tr> 
   <td>Une erreur s'est produite lors de la récupération de l'utilisation de la décision.</td> 
   <td>Cette erreur peut se produire lorsque l'API tente de récupérer le modèle d'offre.</td> 
  </tr>
  <tr> 
   <td>L'attribut d'Offre offre-attribut n'est pas valide.</td> 
   <td>Vérifiez si l'attribut d'offre référencé dans l'offre drp est valide. Voici les attributs valides : <br/>
Image : deliveryURL, linkURL<br/>
Texte : content<br/>
HTML : content<br/></td> 
  </tr> 
 </tbody> 
</table>

