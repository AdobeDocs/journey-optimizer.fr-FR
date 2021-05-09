---
title: Jeu de données sur les offres de secours
description: Cette section liste tous les champs utilisés dans le jeu de données exporté pour les offres de secours.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Jeu de données des offres de secours {#fallback-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les offres de secours est mis à jour.

![](../assets/dataset-fallback.png)

Le lot le plus récent du jeu de données qui a réussi s&#39;affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d&#39;Offres dans [cette section](../export-catalog/access-dataset.md).

Voici la liste de tous les champs qui peuvent être utilisés dans le jeu de données **[!UICONTROL Decision Object Repository - Fallback Offres]**.

## Identifiant

Identificateur unique de l&#39;enregistrement.

Type : chaîne

## _expérience

### prise de décision

#### caractéristiques

**Caractéristiques** des options de décision. Autres propriétés ou attributs appartenant à cette option de décision particulière. Différentes instances peuvent présenter des caractéristiques différentes (clés dans la carte). Les caractéristiques sont des paires nom-valeur utilisées pour distinguer une option de décision des autres. Les caractéristiques sont utilisées comme valeurs dans le contenu qui représente cette option de décision et comme fonctionnalités pour analyser et optimiser les performances d&#39;une option. Lorsque chaque instance possède le même attribut ou la même propriété, cet aspect doit être modélisé en tant que schéma d&#39;extension dérivé des détails de l’option de décision.

Type : objet

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### Contenu

**Détails** du contenu. Éléments de contenu pour rendre l’élément de décision dans différents contextes. Une seule option de décision peut comporter plusieurs variantes de contenu. Le contenu est une information destinée à une audience destinée à être consommée dans une expérience (numérique). Le contenu est diffusé par canal dans un emplacement particulier.

Type : tableau

* **composants**

   Composants du contenu représentant l’option de décision, y compris toutes leurs variantes de langue. Les composants spécifiques sont identifiés par &quot;dx:format&quot;, &quot;dc:subject&quot; et &quot;dc:language&quot; ou une combinaison de ces composants. Ces métadonnées permettent de localiser ou de représenter le contenu associé à une offre et de l’intégrer selon le contrat de placement.

   Type : tableau

   * **Type de composant de contenu**

      Ensemble énuméré d’URI où chaque valeur correspond à un type donné au composant de contenu. Certains consommateurs des représentations de contenu s’attendent à ce que la valeur @type soit une référence au schéma qui décrit les propriétés supplémentaires du composant de contenu.

      Type : string

   * **_dc**

      * **Format**

         Manifestation physique ou numérique de la ressource. En règle générale, Format doit inclure le type de support de la ressource. Le format peut être utilisé pour déterminer le logiciel, le matériel ou tout autre équipement nécessaire pour afficher ou exploiter la ressource. Il est recommandé de sélectionner une valeur dans un vocabulaire contrôlé (par exemple, la liste de [Types de médias Internet](http://www.iana.org/ assignations/types de médias/) définissant les formats de supports informatiques).

         Type : string

      * **Langue**

         La ou les langues de la ressource.\nLes langues sont spécifiées dans le code de langue tel que défini dans [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), qui fait partie du BCP 47, utilisé ailleurs dans XDM.

         Type : string
   * **_repo**

      * **id**

         Identificateur unique facultatif pour référencer la ressource dans un référentiel de contenu. Lorsque les API de plateforme sont utilisées pour récupérer la représentation, le client peut s&#39;attendre à ce qu&#39;une propriété \&quot;repo:resolveUrl\&quot; supplémentaire récupère la ressource.

         Type : string

      * **name**

         Quelques conseils sur l&#39;emplacement du référentiel qui stocke l&#39;actif externe par le \&quot;repo:id\&quot;.

         Type : string

      * **repositoryID**

         Identificateur unique facultatif pour référencer la ressource dans un référentiel de contenu. Lorsque les API de plateforme sont utilisées pour récupérer la représentation, le client peut s&#39;attendre à ce qu&#39;une propriété \&quot;repo:resolveUrl\&quot; supplémentaire récupère la ressource.

         Type : string

      * **resolveURL**

         Un localisateur de ressources unique facultatif pour lire la ressource dans un référentiel de contenu. Il sera ainsi plus facile d’obtenir la ressource sans que le client comprenne où la ressource est gérée et les API à appeler. Il s’agit d’un lien HAL, mais la sémantique est plus simple et plus utile.

         Type : string
   * **content**

      Champ facultatif qui permet de conserver directement le contenu. Au lieu de référencer le contenu dans un référentiel de ressources, le composant peut contenir directement du contenu simple. Ce champ n’est pas utilisé pour les ressources de contenu composites, complexes et binaires.

      Type : string

   * **deliveryURL**

      Un localisateur de ressources unique facultatif pour obtenir la ressource à partir d’un réseau de diffusion de contenu ou d’un point de terminaison de service. Cette URL permet d’accéder publiquement à la ressource par un agent utilisateur.

      Type : string

   * **linkURL**

      Un localisateur de ressources unique facultatif pour les interactions utilisateur. Cette URL permet de renvoyer l’utilisateur final dans un agent utilisateur et peut faire l’objet d’un suivi.

      Type : string



* **Placement**

   Emplacement à respecter. La valeur est l’URI (@id) de l’emplacement d’offre référencé. Voir schéma https://ns.adobe.com/experience/decisioning/placement.

   Type : string



#### État du cycle de vie

L’état du cycle de vie permet d’exécuter des workflows avec un objet. L’état peut avoir une incidence lorsqu’un objet est visible ou jugé pertinent. Les modifications d’état sont effectuées par les clients ou les services qui utilisent les objets.

Type : string

Valeurs possibles : &quot;brouillon&quot;, &quot;approuvé&quot;, &quot;en direct&quot;, &quot;terminé&quot;, &quot;archivé&quot;

Valeur par défaut : &quot;draft&quot;

#### Nom de l’option de décision

Nom d’option affiché dans diverses interfaces utilisateur.

Type : string

#### Balises

Ensemble de balises associé à cette entité. Les balises sont utilisées dans les expressions de filtrage pour limiter le stock global à un sous-ensemble (catégorie).

Type : tableau

## _repo

### Option de décision ETag

Révision à laquelle l&#39;objet d&#39;option de décision se trouvait lors de la prise de l&#39;instantané.

Type : string
