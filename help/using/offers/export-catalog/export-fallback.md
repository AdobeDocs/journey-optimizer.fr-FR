---
title: Jeu de données d’offres de secours
description: Cette section répertorie tous les champs utilisés dans le jeu de données exporté pour les offres de secours.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---

# Jeu de données d’offres de secours {#fallback-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les offres de secours est mis à jour.

![](../assets/dataset-fallback.png)

Le dernier lot réussi du jeu de données s’affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d’offres dans [cette section](../export-catalog/access-dataset.md).

Voici la liste de tous les champs pouvant être utilisés dans la variable **[!UICONTROL Decision Object Repository - Fallback Offers]** jeu de données.

## Identifiant {#identifier}

**Champ :** _id
**Titre :** Identifiant
**Description :** Identifiant unique de l’enregistrement.
**Type :** string

## _experience {#experience}

**Champ :** _experience
**Type :** objet

### _experience > prise de décision

**Champ :** prise de décision
**Type :** objet

#### _experience > prise de décision > caractéristiques

**Champ :** caractéristiques
**Titre :** Caractéristiques de l’option de décision
**Description :** Propriétés ou attributs supplémentaires appartenant à cette option de décision particulière. Différentes instances peuvent avoir des caractéristiques différentes (clés dans le mappage). Les caractéristiques sont des paires nom-valeur utilisées pour distinguer une option de décision des autres. Les caractéristiques sont utilisées comme valeurs dans le contenu qui représente cette option de décision et comme fonctionnalités pour analyser et optimiser les performances d’une option. Lorsque chaque instance possède le même attribut ou la même propriété, cet aspect doit être modélisé en tant que schéma d’extension qui dérive du détail de l’option de décision.
**Type :** objet

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### _experience > prise de décision > contenu

**Champ :** contenu
**Titre :** Détails du contenu
**Description :** Éléments de contenu pour effectuer le rendu de l’élément de décision dans différents contextes. Une seule option de décision peut avoir plusieurs variantes de contenu. Le contenu est une information destinée à une audience destinée à être utilisée dans une expérience (numérique). Le contenu est diffusé par le biais de canaux à un emplacement spécifique.
**Type :** tableau

**_experience > prise de décision > contenu > composants**

**Champ :** components
**Description :** Composants du contenu représentant l’option de décision, y compris toutes leurs variantes linguistiques. Les composants spécifiques sont identifiés par &quot;dx:format&quot;, &quot;dc:subject&quot; et &quot;dc:language&quot; ou une combinaison de ces composants. Ces métadonnées sont utilisées pour localiser ou représenter le contenu associé à une offre et l’intégrer selon le contrat d’emplacement.
**Type :** tableau
**Obligatoire :** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > prise de décision > contenu > composants > Type de composant de contenu**

   **Champ :** _type
   **Titre :** Type de composant de contenu
   **Description :** Un ensemble énuméré d’URI où chaque valeur correspond à un type donné au composant de contenu. Certains consommateurs des représentations de contenu s’attendent à ce que la valeur @type soit une référence au schéma qui décrit les propriétés supplémentaires du composant de contenu.
   **Type :** string

* **_experience > prise de décision > contenu > composants > _dc**

   **Champ :** _dc
   **Type :** objet
   **Obligatoire :** &quot;format&quot;

   * **Format**

      **Champ :** format
      **Titre :** Format
      **Description :** Manifestation physique ou numérique de la ressource. En règle générale, le format doit inclure le type de média de la ressource. Le format peut être utilisé pour déterminer le logiciel, le matériel ou tout autre équipement nécessaire pour afficher ou exploiter la ressource. Il est recommandé de sélectionner une valeur dans un vocabulaire contrôlé (par exemple, la liste des [Types de médias Internet](http://www.iana.org/ assignments/media-types/) définition des formats de médias informatiques).
      **Type :** string
      **Exemple :** &quot;application/vnd.adobe.photoshop&quot;

   * **Langue**

      **Champ :** language
      **Titre :** Langue
      **Description :** La ou les langues de la ressource. \nLes langues sont spécifiées dans le code de langue tel que défini dans [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), qui fait partie de BCP 47, utilisé ailleurs dans XDM.
      **Type :** tableau
      **Exemples :** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experience > prise de décision > contenu > composants > _repo**

   **Champ :** _repo
   **Type :** objet

   * **id**

      **Champ :** id
      **Description :** Identifiant unique facultatif permettant de référencer la ressource dans un référentiel de contenu. Lorsque les API de Platform sont utilisées pour récupérer la représentation, le client peut s’attendre à une propriété supplémentaire \&quot;repo:resolveUrl\&quot; pour récupérer la ressource.
      **Type :** string
      **Exemple :** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

      **Champ :** name
      **Description :** Quelques conseils sur l’emplacement du référentiel qui stocke la ressource externe par le \&quot;repo:id\&quot;.
      **Type :** string

   * **repositoryID**

      **Champ :** repositoryID
      **Description :** Identifiant unique facultatif permettant de référencer la ressource dans un référentiel de contenu. Lorsque les API de Platform sont utilisées pour récupérer la représentation, le client peut s’attendre à une propriété supplémentaire \&quot;repo:resolveUrl\&quot; pour récupérer la ressource.
      **Type :** string
      **Exemple :** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **Champ :** resolveURL
      **Description :** Un localisateur de ressource unique facultatif pour lire la ressource dans un référentiel de contenu. Cela facilite l’obtention de la ressource sans que le client ne comprenne où la ressource est gérée et les API à appeler. Ceci est similaire à un lien HAL, mais la sémantique est plus simple et plus utile.
      **Type :** string
      **Exemple :** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_experience > prise de décision > contenu > composants > contenu**

   **Champ :** content
   **Description :** Champ facultatif permettant de conserver directement le contenu. Au lieu de référencer le contenu dans un référentiel de ressources, le composant peut contenir directement du contenu simple. Ce champ n’est pas utilisé pour les ressources de contenu composites, complexes et binaires.
   **Type :** string

* **_experience > prise de décision > contenu > composants > deliveryURL**

   **Champ :** deliveryURL
   **Description :** Un localisateur de ressource unique facultatif pour obtenir la ressource à partir d’un réseau de diffusion de contenu ou d’un point d’entrée de service. Cette URL est utilisée pour accéder publiquement à la ressource par un agent utilisateur.
   **Type :** string
   **Exemple :** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > prise de décision > contenu > composants > linkURL**

   **Champ :** linkURL
   **Description :** Un localisateur de ressource unique facultatif pour les interactions utilisateur. Cette URL est utilisée pour renvoyer l’utilisateur final vers dans un agent utilisateur et peut être suivie.
   **Type :** string
   **Exemple :** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience > prise de décision > contenu > Emplacement**

**Champ :** placement
**Titre :** Emplacement
**Description :** Placement à respecter. La valeur est l’URI (@id) de l’emplacement d’offre référencé. Voir schéma https://ns.adobe.com/experience/decisioning/placement.
**Type :** string

#### _experience > prise de décision > État du cycle de vie

**Champ :** lifecycleStatus
**Titre :** État du cycle de vie
**Description :** L’état de cycle de vie permet d’exécuter des workflows avec un objet. L’état peut avoir une incidence lorsqu’un objet est visible ou considéré comme pertinent. Les modifications d’état sont effectuées par les clients ou les services qui utilisent les objets.
**Type :** string
**Valeurs possibles :** &quot;Version préliminaire&quot; (par défaut), &quot;Approuvé&quot;, &quot;En direct&quot;, &quot;Terminé&quot;, &quot;Archivé&quot;

#### _experience > prise de décision > Nom de l’option de décision

**Champ :** name
**Titre :** Nom de l’option de décision
**Description :** Nom de l’option qui s’affiche dans différentes interfaces utilisateur.
**Type :** string

#### _experience > prise de décision > balises

**Champ :** tags
**Titre :** Balises
**Description :** Ensemble de balises associées à cette entité. Les balises sont utilisées dans les expressions de filtre pour contraindre l’inventaire global à un sous-ensemble (catégorie).
**Type :** tableau

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo {#repo}

**Champ :** _repo
**Type :** objet

### _repo > Option de décision ETag

**Champ :** etag
**Titre :** Option de décision ETag
**Description :** La révision à laquelle se trouvait l’objet d’option de décision lors de la prise de l’instantané.
**Type :** string
