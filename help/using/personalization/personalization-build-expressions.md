---
solution: Journey Optimizer
product: journey optimizer
title: Ajouter une personnalisation
description: Découvrez comment utiliser l’éditeur de personnalisation pour ajouter une personnalisation.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
mini-toc-levels: 1
keywords: expression, éditeur, à propos, commencer
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: id: e51e8901-97d9-4f7d-a835-503025a90e32id: ac5d9310-7772-40fb-9d78-864562e1bfd6
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 2328
ht-degree: 62%

---

# Ajouter une personnalisation {#build-personalization-expressions}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment utiliser l’éditeur de personnalisation pour ajouter, personnaliser et valider des expressions de personnalisation à partir de sources telles que des attributs de profil, des audiences, des décisions d’offre et des attributs contextuels.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="À propos de l’éditeur de personnalisation"
>abstract="L’éditeur de personnalisation vous permet de sélectionner, organiser, personnaliser et valider toutes les données afin de personnaliser votre contenu."

L’éditeur de personnalisation constitue lʼélément central de la personnalisation dans [!DNL Journey Optimizer]. Il est disponible dans tous les contextes où vous devez définir une personnalisation (par exemple, dans les emails, les notifications push et les offres).

Dans l’interface de l’éditeur de personnalisation, vous pouvez sélectionner, organiser, personnaliser et valider toutes les données afin de personnaliser votre contenu.

![](assets/perso_ee1.png)

## Où puis-je ajouter une personnalisation ? {#where}

Dans **[!DNL Journey Optimizer]**, vous pouvez ajouter une personnalisation dans chaque champ à l’aide de l’icône ![icône d’ajout de personnalisation](assets/do-not-localize/add-perso-icon.svg). Pour plus d’informations, développez les sections ci-dessous.

+++Messages

Dans les messages, vous pouvez ajouter une personnalisation dans différentes parties de vos messages, par exemple dans le champ **[!UICONTROL Objet]**.

![](assets/perso_subject.png)

Vous pouvez également l’ajouter à d’autres sections de votre contenu. Par exemple, pour les [notifications push](../push/push-gs.md), vous pouvez ajouter une personnalisation dans les champs **Titre**, **Corps**, **Son personnalisé**, **Badges** et **Données personnalisées**.

+++

+++Concepteur d’e-mail

Lors de la modification du contenu d’un e-mail dans la Designer d’e-mail](../email/get-started-email-design.md), vous pouvez personnaliser la plupart des éléments de texte à l’aide de l’icône dans la barre d’outils contextuelle.[

![](assets/perso_insert.png)

+++

+++URL

Journey Optimizer vous permet également de personnaliser les **URL** dans vos messages. Les URL personnalisées orientent les destinataires vers des pages spécifiques dʼun site web ou vers un microsite personnalisé, en fonction des attributs du profil. [En savoir plus](../email/url-personalization.md)

![](assets/perso-url.png){width="50%"}

>[!NOTE]
>
>La personnalisation des URL est disponible pour les types de liens suivants : **Lien externe**, **Lien de désabonnement** et **Opt-out**.

+++

+++Configuration du canal e-mail

Lors de la création d’une configuration de canal e-mail, vous pouvez définir des valeurs personnalisées pour les sous-domaines, les en-têtes et les paramètres de tracking des URL. [En savoir plus](../email/surface-personalization.md)

+++

+++Offres

Vous pouvez ajouter une personnalisation lors de l’utilisation de contenu de type texte dans les **représentations de vos offres**. [Découvrir comment créer des offres personnalisées](../offers/offer-library/creating-personalized-offers.md)

+++

## Sources de personnalisation {#sources}

Le volet de navigation vous permet de sélectionner la source pour la personnalisation. Les sources disponibles sont les suivantes :

* **[!UICONTROL Attributs de profil]** : répertorie toutes les références associées au schéma de profil décrit dans la [documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"}.
* **[!UICONTROL Attributs cibles]** : ce dossier est spécifique aux campagnes orchestrées. Il contient des attributs calculés directement dans la zone de travail de la campagne. [Découvrez comment ajouter une personnalisation dans les campagnes orchestrées.](../orchestrated/add-personalization.md)
* **[!UICONTROL Audiences]** : répertorie toutes les audiences créées dans le service de segmentation d’Adobe Experience Platform. En savoir plus dans la documentation sur la segmentation de Adobe Experience Platform [](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr){target="_blank"}.
* **[!UICONTROL Décisions d’offre]** : répertorie toutes les offres associées à un emplacement spécifique. Sélectionnez l’emplacement, puis insérez les offres dans votre contenu. Pour obtenir une documentation complète sur la gestion des offres, consultez [cette section](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL Attributs contextuels]** : lorsqu’une activité d’action de canal (e-mail, notification push, SMS) est utilisée dans un parcours ou une campagne, des attributs contextuels liés aux événements et aux propriétés sont disponibles pour la personnalisation. Un exemple de personnalisation utilisant les attributs contextuels est présenté dans [cette section](personalization-use-case.md). De plus, les réponses d’action personnalisée peuvent être utilisées pour la personnalisation. [Découvrez comment utiliser des réponses d’action personnalisée dans des canaux natifs](../action/action-response.md#response-in-channels).

>[!NOTE]
>
>Si vous ciblez une audience avec des attributs d’enrichissement générés à l’aide d’un workflow de composition, vous pouvez utiliser ces attributs pour personnaliser votre message. [Découvrir comment utiliser les attributs d’enrichissement des audiences](../audience/about-audiences.md#enrichment)

## Ajouter une personnalisation {#add}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="Saisie semi-automatique"
>abstract="Activer cette option permet au système de suggérer et de remplir automatiquement le code au fur et à mesure que vous le tapez. Cette fonctionnalité est disponible uniquement pour les formats HTML et Texte et prend en charge les attributs de profil et de contexte. Si vous désactivez cette option, l’éditeur fournit une saisie automatique du code HTML natif à la place."

C’est dans l’espace de travail central que vous créez votre syntaxe de personnalisation. Pour utiliser un attribut afin de personnaliser votre message, localisez-le dans le volet de navigation de gauche, puis cliquez sur le bouton `+` pour l’ajouter à l’expression.

![](assets/personalization-add-attribute.png)

Le menu à trois points en regard de l’icône `+` vous permet d’obtenir plus de détails sur chaque attribut et d’ajouter ceux que vous utilisez le plus souvent à vos favoris. Vous pouvez accéder aux attributs ajoutés aux favoris à partir du menu **[!UICONTROL Favoris]** dans le volet de navigation.

>[!NOTE]
>
>Par défaut, le volet des attributs affiche uniquement les attributs renseignés. Pour afficher tous les attributs, sélectionnez le bouton ![](assets/do-not-localize/settings-icon.svg) situé au-dessus du champ de recherche et désactivez l’option **[!UICONTROL Afficher uniquement les attributs renseignés]**.

De plus, vous pouvez définir un texte de remplacement par défaut qui s’affichera si un attribut de profil de type chaîne est vide. Pour ce faire, cliquez sur le bouton des points de suspension en regard de l’attribut et sélectionnez **[!UICONTROL Insérer avec un texte de remplacement]**. Rédigez le texte à afficher par défaut si la valeur de l’attribut est vide pour un profil, puis cliquez sur **[!UICONTROL Ajouter]**.

![](assets/attribute-details.png)

Dans l’exemple suivant, l’éditeur de personnalisation vous permet de sélectionner les profils dont l’anniversaire est aujourd’hui, puis de terminer la personnalisation en insérant une offre spécifique correspondant à cette journée.

![](assets/perso_ee2.png)

## Options de modification d’expressions {#options}

L’espace de travail central fournit divers outils pour vous aider à écrire votre expression de personnalisation.

![](assets/perso-workspace.png)

Les options disponibles sont les suivantes :

1. **[!UICONTROL Rechercher]**/**[!UICONTROL Rechercher et remplacer]** : effectuez une recherche dans votre expression et remplacez automatiquement des parties de code.
1. **[!UICONTROL Annuler]** / **[!UICONTROL Rétablir]** : annulez ou rétablissez la dernière opération.
1. **[!UICONTROL Saisie automatique]** : suggère et remplit automatiquement le code au fur et à mesure que vous le tapez. Cette fonctionnalité est disponible uniquement pour les formats HTML et Texte et prend en charge les attributs de profil et de contexte. Si vous désactivez cette option, l’éditeur fournit une saisie automatique du code HTML natif à la place.

   ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"}

1. **[!UICONTROL HTML]** / **[!UICONTROL JSON]** / **[!UICONTROL Texte]** : identifiez le format de votre code. Cela permet au système d’adapter la fonctionnalité de validation et de saisie automatique à la langue sélectionnée.
1. **[!UICONTROL Valider]** : vérifiez la syntaxe de votre expression. En savoir plus dans [cette section](../personalization/personalization-build-expressions.md).
1. **[!UICONTROL Enregistrer en tant que fragment]** : enregistrez votre expression en tant que fragment d’expression. En savoir plus dans [cette section](../content-management/save-fragments.md#save-as-expression-fragment)
1. **[!UICONTROL Taille de police]** : ajuste la taille de la police du contenu dans l’éditeur pour une meilleure lisibilité.
1. **[!UICONTROL Retour à la ligne]** : active ou désactive le retour à la ligne, ce qui permet aux expressions longues d’être affichées sur une seule ligne ou renvoyées à la ligne dans l’éditeur. Les options incluent :
   * **Désactivé** (par défaut) : aucun retour à la ligne. Les lignes longues s’étendent au-delà de la vue de l’éditeur et nécessitent un défilement horizontal.
   * **Activé** : adapte le retour à la ligne à la largeur de l’éditeur.
   * **Retour à la ligne en colonne** : renvoie à la ligne lorsqu’une ligne atteint 80 caractères.
   * **Limité** : le retour à ligne s’adapte à la largeur de l’éditeur ou a lieu quand la ligne atteint 80 caractères, selon la valeur la plus petite.
1. **[!UICONTROL Pastilles]** : affichez les attributs sous la forme de « pastilles » compactes afin d’améliorer la lisibilité en masquant les chemins d’accès aux attributs longs. Cliquez sur un attribut pour afficher son chemin d’accès complet.

   >[!NOTE]
   >
   >Cette option est disponible uniquement pour les attributs de profil, les attributs contextuels et les médias dynamiques.

Dans le volet de navigation, des fonctionnalités supplémentaires sont disponibles pour vous permettre de créer votre expression de personnalisation.

![](assets/perso-features.png)

* **[!UICONTROL Fonctions d’assistance]** : les fonctions d’assistance vous permettent d’effectuer des opérations sur les données, comme des calculs, une mise en forme ou des conversions de données, des conditions, et de les manipuler dans le contexte de la personnalisation. [En savoir plus sur les fonctions d’assistance disponibles](functions/functions.md)

* **[!UICONTROL Favoris]** : les attributs que vous avez ajoutés aux favoris s’affichent dans cette liste. Cela vous permet d’accéder rapidement aux éléments que vous utilisez le plus souvent. Pour ajouter un attribut à vos favoris, cliquez sur le menu à trois points et sélectionnez **[!UICONTROL Ajouter aux favoris]**.

* **[!UICONTROL Conditions]** : utilisez les règles conditionnelles créées dans la bibliothèque pour ajouter du contenu dynamique à vos messages. Vous pouvez ainsi créer plusieurs variantes de votre message en fonction de conditions. [Découvrir comment créer du contenu dynamique](../personalization/get-started-dynamic-content.md)

* **[!UICONTROL Fragments]** :utilisez les fragments d’expression qui ont été créés ou enregistrés dans le sandbox actif. Un fragment est un composant réutilisable pouvant être référencé dans des campagnes et des parcours [!DNL Journey Optimizer]. Cette fonctionnalité permet de construire à l’avance plusieurs blocs de contenu personnalisés qui peuvent être utilisés par les utilisateurs et les utilisatrices marketing pour assembler rapidement des contenus dans le cadre d’un processus de conception amélioré. [Découvrir comment utiliser les fragments d’expression pour la personnalisation](../personalization/use-expression-fragments.md)

>[!TIP]
>
>Vous recherchez des expressions prêtes à l’emploi ? La page **[Recettes](personalization-recipes.md)** fournit des modèles de copier-coller pour les cas d’utilisation les plus courants : formatage des dates, compte à rebours, basculements conditionnels, affichage temporel uniquement, etc.

Une fois votre expression de personnalisation prête, vous devez la faire valider par l’éditeur de personnalisation. En savoir plus dans [cette section](../personalization/personalization-build-expressions.md).

## Mécanismes de validation {#validation-mechanisms}

La validation de l’expression s’effectue automatiquement lorsque vous cliquez sur le bouton **Ajouter** pour fermer la fenêtre de l’éditeur. Vous pouvez également utiliser le bouton **Valider** pour vérifier la syntaxe de votre personnalisation.

![](assets/perso_validation1.png)

Développez la section ci-dessous pour afficher les erreurs courantes qui peuvent se produire lors de la validation de la personnalisation.

+++Erreurs courantes

* **Chemin « XYZ » introuvable**

En cas de référencement d’un champ qui n’est pas défini dans le schéma.

Dans ce cas, **firstName1** n’est pas défini comme attribut dans le schéma du profil :

```
{{profile.person.name.firstName1}}
```

* **Incompatibilité de type pour la variable « XYZ ».: Tableau attendu. Chaîne trouvée.**

En cas de tentative d’itération sur une chaîne plutôt que sur un tableau.

Dans ce cas, **product** n’est pas un tableau :

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Syntaxe des barres de contrôle non valide.`'[XYZ}}'`** trouvé

En cas d’utilisation d’une syntaxe de barres de contrôle non valide.

Les expressions des barres de contrôle sont entourées de **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **Définition de segment non valide**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

+++

Pour les offres, des erreurs spécifiques peuvent se produire. Pour plus d’informations, développez la section ci-dessous :

+++ Erreurs spécifiques liées aux offres

Les erreurs liées à l’intégration des offres dans un email ou une notification push présentent le modèle suivant :

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

La validation est effectuée lors de la validation du contenu de personnalisation dans l’éditeur de personnalisation.

<table> 
 <thead> 
  <tr> 
   <th> Titre de l’erreur<br /> </th> 
   <th> Validation/Résolution <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Ressource avec ID placementID et type OfferPlacement introuvable <br/>
Ressource avec ID activityID et type OfferActivity introuvable<br/></td> 
   <td>Vérifiez que ActivityID et/ou PlacementID sont disponibles</td> 
  </tr> 
   <tr> 
   <td>Impossible de valider la ressource.</td> 
   <td>Le componentType dans l’emplacement doit correspondre à l’offre offerType.</td> 
  </tr> 
   <tr> 
   <td>L’URL publique n’est pas présente dans l’offre offerId.</td> 
   <td>Les offres d’image (toutes les offres personnalisées et de secours associées à la paire décision-emplacement) doivent avoir une URL publique renseignée (l’URL deliveryURL ne doit pas être vide).</td> 
  </tr> 
  <tr> 
   <td>La décision contient des attributs qui ne sont pas des attributs de profil.</td> 
   <td>L’utilisation du modèle d’offre ne doit contenir que les attributs de profil.</td> 
  </tr> 
  <tr> 
   <td>Une erreur s’est produite lors de la récupération de l’utilisation de la décision.</td> 
   <td>Cette erreur peut se produire lorsque l’API tente de récupérer le modèle d’offre.</td> 
  </tr>
  <tr> 
   <td>L’attribut d’offre offer-attribute n’est pas valide.</td> 
   <td>Vérifiez que l’attribut offer-attribute référencé dans le drp d’offre est valide. Voici les attributs valides : <br/>
Image : deliveryURL, linkURL<br/>
Texte : contenu<br/>
HTML : contenu<br/></td> 
  </tr> 
 </tbody> 
</table>

+++

## Référence rapide {#quick-reference}

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

>[!BEGINTABS]

>[!TAB Vue d’ensemble]

**TL;DR**

Cette page explique comment utiliser l’éditeur de personnalisation de Journey Optimizer pour sélectionner, créer, personnaliser et valider des expressions de personnalisation à partir de sources comprenant des attributs de profil, des audiences, des décisions d’offre et des attributs contextuels.

**Intentions**

* Découvrez où la personnalisation peut être ajoutée dans Journey Optimizer (messages, Designer e-mail, URL, configuration des e-mails, offres)
* Sélectionner la source de personnalisation appropriée pour une expression
* Ajouter des attributs et créer des expressions dans l’espace de travail de l’éditeur
* Utiliser les outils de l’éditeur : Rechercher/Remplacer, Saisie automatique, Valider, Pilules, Enregistrer en tant que fragment
* Utiliser les fonctionnalités du volet de navigation : fonctions d’assistance, favoris, conditions, fragments
* Valider les expressions et résoudre les erreurs courantes

>[!TAB Glossaire]

* **Éditeur Personalization** : outil d’interface utilisateur central dans Journey Optimizer pour créer, personnaliser et valider les expressions de personnalisation ; disponible partout où la personnalisation peut être définie. *(spécifique au produit)*
* **Sources Personalization** : catégories de données disponibles pour la création d’expressions : attributs de profil, attributs de cible, audiences, décisions d’offre et attributs contextuels.
* **Attributs contextuels** : données spécifiques au Parcours ou à la campagne (événements, propriétés, réponses d’action personnalisée) disponibles pour personnalisation uniquement lorsqu’une action de canal est utilisée dans un parcours ou une campagne. *(spécifique au produit)*
* **Pilules** : mode d’affichage de l’éditeur de personnalisation qui effectue le rendu des chemins d’accès aux attributs longs en tant que jetons compacts cliquables pour une meilleure lisibilité. Disponible uniquement pour les attributs de profil, les attributs contextuels et Dynamic Media. *(spécifique au produit)*
* **Saisie automatique** : fonctionnalité d’éditeur qui suggère et complète automatiquement le code au fur et à mesure que vous le tapez ; disponible uniquement pour les formats HTML et Texte, et prenant uniquement en charge les attributs de profil et de contexte. *(spécifique au produit)*
* **Fragment d’expression** : composant d’expression de personnalisation réutilisable pouvant être référencé dans les campagnes et les parcours. *(spécifique au produit)*
* **Texte de secours** : chaîne par défaut affichée lorsqu’un attribut de profil de type chaîne est vide pour un profil donné ; configuré par attribut via « Insérer avec un texte de secours ».

>[!TAB  Terminologie ]

* **Nom canonique :** éditeur de personnalisation
* **Ne les confondez pas :** l’éditeur Personalization (utilisé pour créer des expressions de contenu dans les messages, les e-mails, les notifications push et les offres, prend en charge les barres de contrôle et la syntaxe PQL) ≠ l’éditeur d’expression avancé (utilisé dans le parcours pour les conditions sur les sources de données et les informations d’événement, les activités d’attente personnalisées et le mappage des paramètres d’action) fournit des fonctions intégrées et des opérateurs différents de ceux de l’éditeur de personnalisation.
* **Ne pas confondre :** Attributs de profil (basés sur un schéma XDM, disponibles dans tous les contextes) ≠ Attributs contextuels (spécifiques au parcours/à la campagne, disponibles uniquement dans ce contexte) ≠ Attributs de cible (campagnes orchestrées uniquement)
* **À ne pas confondre :** Saisie automatique pour HTML/Texte (suggère la saisie semi-automatique des attributs de personnalisation) ≠ la saisie semi-automatique du code HTML natif (la valeur par défaut de l’éditeur lorsque le bouton (bascule) est désactivé)

>[!TAB Mécanismes de sécurisation et limitations]

* La saisie automatique est disponible uniquement pour les formats HTML et Texte ; elle prend uniquement en charge les attributs de profil et de contexte.
* Le mode d’affichage des pilules n’est disponible que pour les attributs de profil, les attributs contextuels et Dynamic Media.
* La personnalisation de l’URL est disponible uniquement pour les types de lien externe, Lien de désinscription et Lien d’opt-out.
* Par défaut, le volet Attributs affiche uniquement les attributs renseignés ; activez l’option « Afficher uniquement les attributs renseignés » pour afficher tous les attributs de schéma.
* L’utilisation du modèle d’offre ne doit contenir que des attributs de profil ; les attributs autres que de profil dans une décision entraînent une erreur de validation.

>[!TAB FAQ]

**Q : Où la personnalisation peut-elle être ajoutée dans Journey Optimizer ?**

Dans n’importe quel champ contenant l’icône d’ajout de personnalisation, y compris l’objet de l’e-mail, les champs de notification push (titre, corps, son personnalisé, badges, données personnalisées), les éléments textuels du Designer d’e-mail, les URL (lien externe, lien de désinscription, désinscription), les sous-domaines/en-têtes/paramètres de suivi des URL de configuration d’e-mail et les représentations de type texte d’offre.

**Q : Quelles sont les sources de personnalisation disponibles ?**

Attributs de profil, Attributs de cible (campagnes orchestrées uniquement), Audiences, Décisions d’offre et Attributs contextuels (événements de parcours/campagne et réponses d’action personnalisée).

**Q : Comment une expression est-elle validée ?**

La validation s’exécute automatiquement lorsque vous cliquez sur Ajouter pour fermer l’éditeur. Vous pouvez également le déclencher manuellement à l’aide du bouton Valider . Les erreurs courantes sont les suivantes : chemin d’accès introuvable (champ absent du schéma), non-correspondance de type (itération d’une chaîne sous forme de tableau), syntaxe Handlebars non valide et définition de segment non valide.

**Q : Que fait l&#39;option Pilules ?**

Il rend les chemins d’accès aux attributs longs sous la forme de jetons compacts cliquables pour une meilleure lisibilité dans l’éditeur. Disponible uniquement pour les attributs de profil, les attributs contextuels et Dynamic Media.

**Q : Pourquoi est-ce que je ne vois que certains attributs dans le volet des attributs ?**

Par défaut, le volet affiche uniquement les attributs renseignés. Sélectionnez l’icône des paramètres au-dessus du champ de recherche et désactivez « Afficher uniquement les attributs renseignés » pour afficher tous les attributs de schéma.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 54973b31 -->
