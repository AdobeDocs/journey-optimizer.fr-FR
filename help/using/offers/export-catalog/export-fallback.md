---
title: Jeu de données sur les offres de secours
description: Cette section liste tous les champs utilisés dans le jeu de données exporté pour les offres de secours.
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '1008'
ht-degree: 7%

---

# Jeu de données des offres de secours {#fallback-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les offres de secours est mis à jour.

![](../../assets/dataset-fallback.png)

Le lot le plus récent du jeu de données qui a réussi s&#39;affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d&#39;Offres dans [cette section](../export-catalog/access-dataset.md).

Voici la liste de tous les champs qui peuvent être utilisés dans le jeu de données **[!UICONTROL Decision Object Repository - Fallback Offres]**.

## Identifiant

**Champ:** _id 
**Titre:** Identifier 
**Description:** Identificateur unique de l’enregistrement.
**Type :** Chaîne

## _expérience

**Champ:** _experience 
**Type:** objet

### prise de décision

**Champ:** Type de 
**prise de décision:** objet

#### caractéristiques

**Champ:** caractéristiques 
**Titre:Option** Décision Caractéristiques 
**Description:Propriétés ou attributs** supplémentaires appartenant à cette option de décision particulière. Différentes instances peuvent présenter des caractéristiques différentes (clés dans la carte). Les caractéristiques sont des paires nom-valeur utilisées pour distinguer une option de décision des autres. Les caractéristiques sont utilisées comme valeurs dans le contenu qui représente cette option de décision et comme fonctionnalités pour analyser et optimiser les performances d&#39;une option. Lorsque chaque instance possède le même attribut ou la même propriété, cet aspect doit être modélisé en tant que schéma d&#39;extension dérivé des détails de l’option de décision.
**Type:** objet

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### Contenu

**Champ:** contenu 
**Titre:Détails du** contenu 
**Description:Eléments** de contenu pour rendre l’élément de décision dans différents contextes. Une seule option de décision peut comporter plusieurs variantes de contenu. Le contenu est une information destinée à une audience destinée à être consommée dans une expérience (numérique). Le contenu est diffusé par canal dans un emplacement particulier.
**Type:** tableau

* **règle**

   **Champ:** composants
   **Description :** composants du contenu représentant l’option de décision, y compris toutes leurs variantes de langue. Les composants spécifiques sont identifiés par &quot;dx:format&quot;, &quot;dc:subject&quot; et &quot;dc:language&quot; ou une combinaison de ces composants. Ces métadonnées permettent de localiser ou de représenter le contenu associé à une offre et de l’intégrer selon le contrat de placement.
   **Type:** tableau
   **Obligatoire:** &quot;_type&quot;, &quot;_dc&quot;  <!--TBC?-->

   * **Type de composant de contenu**

      **Champ:** _type
      **Titre:Type de composant** de contenu
      **Description :** ensemble énuméré d’URI où chaque valeur correspond à un type donné au composant de contenu. Certains consommateurs des représentations de contenu s’attendent à ce que la valeur @type soit une référence au schéma qui décrit les propriétés supplémentaires du composant de contenu.
      **Type :** Chaîne

   * **_dc**

      **Champ:** _dc
      **Type:** objet
      **Obligatoire:** &quot;format&quot;

      * **Format**

         **Champ:** format
         **Titre:** Format
         **Description :** La manifestation physique ou numérique de la ressource. En règle générale, Format doit inclure le type de support de la ressource. Le format peut être utilisé pour déterminer le logiciel, le matériel ou tout autre équipement nécessaire pour afficher ou exploiter la ressource. Il est recommandé de sélectionner une valeur dans un vocabulaire contrôlé (par exemple, la liste de [Types de médias Internet](http://www.iana.org/ assignations/types de médias/) définissant les formats de supports informatiques).
         **Type :**Chaîne
         **Exemple :** &quot;application/vnd.adobe.photoshop&quot;

      * **Langue**

         **Champ:** langue
         **Titre:** Langue
         **Description :** la ou les langues de la ressource. \nLes langues sont spécifiées dans le code de langue tel que défini dans [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), qui fait partie du BCP 47, utilisé ailleurs dans XDM.
         **Type:** tableau
         **Exemples:** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;
   * **_repo**

      **Champ:** _repo
      **Type:** objet

      * **identifiant**

         **Champ:** id
         **Description :** identifiant unique facultatif permettant de référencer la ressource dans un référentiel de contenu. Lorsque les API de plateforme sont utilisées pour récupérer la représentation, le client peut s&#39;attendre à ce qu&#39;une propriété \&quot;repo:resolveUrl\&quot; supplémentaire récupère la ressource.
         **Type :**Chaîne
         **Exemple :** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

      * **name**

         **Champ:** nom
         **Description :** Quelques conseils sur l&#39;emplacement du référentiel qui stocke l&#39;actif externe par le \&quot;repo:id\&quot;.
         **Type :** Chaîne

      * **repositoryID**

         **Champ:** repositoryID
         **Description :** identifiant unique facultatif permettant de référencer la ressource dans un référentiel de contenu. Lorsque les API de plateforme sont utilisées pour récupérer la représentation, le client peut s&#39;attendre à ce qu&#39;une propriété \&quot;repo:resolveUrl\&quot; supplémentaire récupère la ressource.
         **Type :**Chaîne
         **Exemple :** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

      * **resolveURL**

         **Champ:** resolveURL
         **Description :** localisateur de ressources unique facultatif pour lire la ressource dans un référentiel de contenu. Il sera ainsi plus facile d’obtenir la ressource sans que le client comprenne où la ressource est gérée et les API à appeler. Il s’agit d’un lien HAL, mais la sémantique est plus simple et plus utile.
         **Type :**Chaîne
         **Exemple:** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;
   * **content**

      **Champ:** contenu
      **Description :** champ facultatif contenant directement du contenu. Au lieu de référencer le contenu dans un référentiel de ressources, le composant peut contenir directement du contenu simple. Ce champ n’est pas utilisé pour les ressources de contenu composites, complexes et binaires.
      **Type :** Chaîne

   * **deliveryURL**

      **Champ:** deliveryURL
      **Description :** localisateur de ressources unique facultatif pour obtenir le fichier à partir d’un réseau de diffusion de contenu ou d’un point de terminaison de service. Cette URL permet d’accéder publiquement à la ressource par un agent utilisateur.
      **Type :**Chaîne
      **Exemple :** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

   * **linkURL**

      **Champ:** linkURL
      **Description :** un localisateur de ressources unique facultatif pour les interactions utilisateur. Cette URL permet de renvoyer l’utilisateur final dans un agent utilisateur et peut faire l’objet d’un suivi.
      **Type :**Chaîne
      **Exemple :** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;



* **Placement**

   **Champ:** placement
   **Titre:** Emplacement
   **Description :** Placement à respecter. La valeur est l’URI (@id) de l’emplacement d’offre qui est référencé. Voir schéma https://ns.adobe.com/experience/decisioning/placement.
   **Type :** Chaîne

#### État du cycle de vie

**Champ:** lifecycleStatus 
**Title:** Lifecycle Status 
**** Description:Lifecycle status permet d’exécuter des workflows avec un objet. L’état peut avoir une incidence lorsqu’un objet est visible ou jugé pertinent. Les modifications d’état sont effectuées par les clients ou les services qui utilisent les objets.
**Type :** chaîne Valeurs 
**possibles :** &quot;Version préliminaire&quot;, &quot;Approuvé&quot;, &quot;En direct&quot;, &quot;Terminé&quot;, &quot;Archivé&quot;, valeur 
**par défaut :** &quot;Version préliminaire&quot;

#### Nom de l’option de décision

**Champ:** nom 
**Titre:** Décision Option Nom 
**Description:** Option Nom affiché dans diverses interfaces utilisateur.
**Type :** Chaîne

#### Balises

**Champ:** balises 
**Titre:** Balises 
**Description:** Ensemble de balises associées à cette entité. Les balises sont utilisées dans les expressions de filtrage pour limiter le stock global à un sous-ensemble (catégorie).
**Type:** tableau

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

### Option de décision ETag

**Champ :** balise 
**Titre :** Option de décision ETag 
**Description :** la révision à laquelle l&#39;objet de l&#39;option de décision se trouvait au moment de la prise de l&#39;instantané.
**Type :** Chaîne
