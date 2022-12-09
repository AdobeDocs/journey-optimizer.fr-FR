---
solution: Journey Optimizer
product: journey optimizer
title: Validation de la personnalisation
description: En savoir plus sur la validation de la personnalisation et comment résoudre les problèmes.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Validation de la personnalisation {#personalization-validation}

## Mécanismes de validation {#validation-mechanisms}

Dans le **Editeur d&#39;expression** , utilisez la méthode **Valider** pour vérifier votre syntaxe de personnalisation.

>[!NOTE]
> La validation s’exécute automatiquement lorsque vous cliquez sur le bouton **Ajouter** pour fermer la fenêtre de l&#39;éditeur.

![](assets/perso_validation1.png)

>[!IMPORTANT]
> Si la syntaxe de personnalisation n&#39;est pas valide, vous ne pouvez pas fermer la fenêtre de l&#39;éditeur d&#39;expression.

## Erreurs courantes {#common-errors}

* **Chemin &quot;XYZ&quot; introuvable**

Lorsque vous essayez de référencer un champ qui n’est pas défini dans le schéma.

Dans ce cas **firstName1** n’est pas défini comme attribut dans le schéma de profil :

```
{{profile.person.name.firstName1}}
```

* **Non-correspondance de type pour la variable &quot;XYZ&quot;. Tableau attendu. Chaîne trouvée.**

Lorsque vous essayez d’effectuer une itération sur une chaîne au lieu d’un tableau :

Dans ce cas **product** n’est pas un tableau :

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Syntaxe des Guidons non valide. Trouvé`‘[XYZ}}’`**

Lorsque la syntaxe handlebars n’est pas valide.

Les expressions Handlebars sont entourées de **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **Définition de segment non valide**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## Erreurs spécifiques liées aux offres {#specific-errors}

Les erreurs liées à l&#39;intégration des offres dans un email ou un message push ont le modèle suivant :

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

La validation est effectuée lors de la validation du contenu de personnalisation dans l’éditeur d’expression.

<table> 
 <thead> 
  <tr> 
   <th> Titre de l’erreur<br /> </th> 
   <th> Validation/Résolution <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Ressource avec ID de placement et type OfferPlacement introuvable <br/>
Ressource avec l’ID d’activité et type OfferActivity introuvable<br/></td> 
   <td>Vérifiez si l’ID d’activité et/ou l’ID de référencement sont disponibles.</td> 
  </tr> 
   <tr> 
   <td>La ressource n’a pas pu être validée.</td> 
   <td>Le componentType dans l’emplacement doit correspondre à l’offre offerType .</td> 
  </tr> 
   <tr> 
   <td>L’URL publique n’est pas présente dans offerId.</td> 
   <td>L’URL publique doit être renseignée pour les offres d’image (toutes les offres personnalisées et de secours associées à la paire décision-placement) (deliveryURL ne doit pas être vide).</td> 
  </tr> 
  <tr> 
   <td>La décision contient des attributs qui ne sont pas des profils.</td> 
   <td>L’utilisation du modèle d’offres ne doit contenir que les attributs de profil.</td> 
  </tr> 
  <tr> 
   <td>Une erreur s’est produite lors de la récupération de l’utilisation de la décision.</td> 
   <td>Cette erreur peut se produire lorsque l’API tente de récupérer le modèle d’offre.</td> 
  </tr>
  <tr> 
   <td>Attribut d’offre attribut non valide.</td> 
   <td>Vérifiez si l’attribut d’offre référencé dans la liste d’offres est valide. Voici les attributs valides : <br/>
Image : deliveryURL, linkURL<br/>
Texte : content<br/>
HTML : content<br/></td> 
  </tr> 
 </tbody> 
</table>
