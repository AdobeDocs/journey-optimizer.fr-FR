---
title: Jeu de données d’offres personnalisées
description: Cette section répertorie tous les champs utilisés dans le jeu de données exporté pour les offres.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '1951'
ht-degree: 0%

---

# Jeu de données d’offres personnalisées {#offers-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les offres de contenu personnalisé est mis à jour.

![](../assets/dataset-offers.png)

Le dernier lot réussi du jeu de données s’affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d’offres dans [cette section](../export-catalog/access-dataset.md).

Voici la liste de tous les champs pouvant être utilisés dans la variable **[!UICONTROL Decision Object Repository - Personalized Offers]** jeu de données.

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

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

#### _experience > prise de décision > calendarConstraints

**Champ :** calendarConstraints
**Titre :** Détails de la contrainte du calendrier
**Description :** Les contraintes du calendrier déterminent si une option de décision est valide sur une période donnée. En dehors de cette période, l’option ne peut pas être proposée.
**Type :** objet

* **Date et heure de fin**

   **Champ :** endDate
   **Titre :** Date et heure de fin
   **Description :** La date de fin de validité des options de décision. Les options qui ont dépassé leur date de fin ne peuvent plus être proposées dans le processus de prise de décision.
   **Type :** string

* **Date et heure de début**

   **Champ :** startDate
   **Titre :** Date et heure de début
   **Description :** La date de début de validité des options de décision. Les options qui n’ont pas atteint leur date de début ne peuvent pas encore être proposées dans le processus de prise de décision.
   **Type :** string

#### _experience > prise de décision > caractéristiques

**Champ :** caractéristiques
**Titre :** Caractéristiques de l’option de décision
**Description :** Propriétés ou attributs supplémentaires appartenant à cette option de décision particulière. Différentes instances peuvent avoir des caractéristiques différentes (clés dans le mappage). Les caractéristiques sont des paires nom-valeur utilisées pour distinguer une option de décision des autres. Les caractéristiques sont utilisées comme valeurs dans le contenu qui représente cette option de décision et comme fonctionnalités pour analyser et optimiser les performances d’une option. Lorsque chaque instance possède le même attribut ou la même propriété, cet aspect doit être modélisé en tant que schéma d’extension qui dérive du détail de l’option de décision.
**Type :** objet

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
      **Description :** Manifestation physique ou numérique de la ressource. En règle générale, le format doit inclure le type de média de la ressource. Le format peut être utilisé pour déterminer le logiciel, le matériel ou tout autre équipement nécessaire pour afficher ou exploiter la ressource. Il est recommandé de sélectionner une valeur dans un vocabulaire contrôlé (par exemple, la liste des [Types de médias Internet](http://www.iana.org/assignments/media-types/) définition des formats de médias informatiques).
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

#### _experience > prise de décision > profileConstraints

**Champ :** profileConstraints
**Titre :** Détails de la contrainte de profil
**Description :** Les contraintes de profil déterminent si une option est éligible à cette identité de profil, à ce stade, dans ce contexte. Si la contrainte de profil n’a pas besoin de prendre en compte les valeurs de chacune des options, c’est-à-dire qu’elle est invariante des options de la sélection de l’option, la contrainte de profil qui évalue &quot;false&quot; annule toute la sélection d’options. D’un autre côté, une règle de contrainte de profil qui utilise une option comme paramètre est évaluée pour chaque option admissible de la sélection d’option.
**Type :** objet

**_experience > prise de décision > profileConstraints > Description**

**Champ :** description
**Titre :** Description
**Description :** Description des contraintes de profil. Il est utilisé pour transmettre des intentions lisibles par l’utilisateur sur la manière ou les raisons pour lesquelles cette contrainte de profil a été construite et/ou sur l’option qui y sera incluse ou exclue.
**Type :** string

**_experience > prise de décision > profileConstraints > Règle d’éligibilité**

**Champ :** éligibilitéRule
**Titre :** Règle d’éligibilité
**Description :** Référence à une règle de décision qui renvoie true (vrai) ou false (faux) pour un profil donné et/ou d’autres objets XDM contextuels donnés. La règle permet de décider si l’option est admissible pour un profil donné. La valeur est l’URI (@id) de la règle de décision référencée. Voir schéma https://ns.adobe.com/experience/decisioning/rule.
**Type :** string

**_experience > prise de décision > profileConstraints > Type de contrainte de profil**

**Champ :** profileConstraintType
**Titre :** Type de contrainte de profil
**Description :** Détermine si des contraintes sont actuellement définies et comment les contraintes sont exprimées. Il peut s’agir d’une règle ou d’un ou plusieurs abonnements au segment.
**Type :** string
**Valeurs possibles :**
* &quot;none&quot; (par défaut)
* &quot;éligibilitéRule&quot;: &quot;La contrainte de profil est exprimée sous la forme d’une règle unique qui doit être évaluée sur true avant que l’action contrainte ne soit autorisée.&quot;
* &quot;anySegments&quot;: &quot;La contrainte de profil est exprimée en un ou plusieurs segments et le profil doit être membre d’au moins l’un d’eux avant que l’action limitée ne soit autorisée.&quot;
* &quot;allSegments&quot;: &quot;La contrainte de profil est exprimée en un ou plusieurs segments et le profil doit être un membre de tous ces segments avant que l’action limitée ne soit autorisée.&quot;
* &quot;rules&quot; : &quot;La contrainte de profil est exprimée sous la forme d’un certain nombre de règles différentes, par exemple l’éligibilité, l’applicabilité, l’adaptabilité, qui doivent toutes être évaluées sur true avant que l’action contrainte ne soit autorisée.&quot;

**_experience > prise de décision > profileConstraints > Identifiants de segment**

**Champ :** segmentIdentities
**Titre :** Identifiants de segment
**Description :** Identifiants des segments
**Type :** tableau

* **Identifiant**

   **Champ :** _id
   **Titre :** Identifiant
   **Description :** Identité du segment dans l’espace de noms associé.
   **Type :** string

* **Espace de noms**

   **Champ :** namespace
   **Titre :** Espace de noms
   **Description :** L’espace de noms associé au `xid` attribut.
   **Type :** objet
   **Obligatoire :** &quot;code&quot;

   * **Code**

      **Champ :** code
      **Titre :** Code
      **Description :** Le code est un identifiant lisible par l’utilisateur de l’espace de noms et peut être utilisé pour demander l’identifiant technique de l’espace de noms utilisé pour le traitement du graphique d’identités.
      **Type :** string

* **Identifiant d’expérience**

   **Champ :** xid
   **Titre :** Identifiant d’expérience
   **Description :** Lorsqu’elle est présente, cette valeur représente un identifiant d’espace de noms croisé unique pour tous les identifiants d’espace de noms définis dans tous les espaces de noms.
   **Type :** string

#### _experience > prise de décision > ranking

**Champ :** ranking
**Titre :** Détails du classement
**Description :** Classement (priorité). Définit ce qui est considéré comme la \&quot;meilleure action\&quot; selon le contexte du critère de décision. Parmi toutes les options sélectionnées qui répondent à la contrainte d’éligibilité, l’ordre de classement décidera de la ou des N premières options proposées.
**Type :** objet

**_experience > prise de décision > ranking > Order Evaluation**

**Champ :** order
**Titre :** Évaluation des commandes
**Description :** Évaluation d’un ordre relatif d’une ou de plusieurs options de décision. Les options avec des valeurs ordinales plus élevées sont sélectionnées sur toutes les options avec des valeurs ordinales plus faibles. Les valeurs déterminées par cette méthode peuvent être ordonnées, mais les distances entre elles ne peuvent être mesurées et ni les sommes ni les produits ne peuvent être calculés. La médiane et le mode sont les seules mesures de tendance centrale qui peuvent être utilisées pour les données ordinales.
**Type :** objet

* **Fonction de notation**

   **Champ :** function
   **Titre :** Fonction de notation
   **Description :** Référence à une fonction qui calcule un score numérique pour cette option de décision. Les options de décision sont ensuite classées selon ce score. La valeur de cette propriété est l’URI (@id) de la fonction à appeler avec l’option on à la fois. Voir schéma https://ns.adobe.com/experience/decisioning/function.
   **Type :** string

* **Type d’évaluation de commande**

   **Champ :** orderEvaluationType
   **Titre :** Type d’évaluation de commande
   **Description :** Indique le mécanisme d’évaluation de la commande utilisé, la priorité statique des options de décision, une fonction de notation qui calcule une valeur numérique pour chaque option ou une stratégie de classement qui reçoit une liste pour la classer.
   **Type :** string
   **Valeurs possibles :** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

* **Stratégie de classement**

   **Champ :** rankingStrategy
   **Titre :** Stratégie de classement
   **Description :** Référence à une stratégie qui classe une liste d’options de décision. Les options de décision sont renvoyées dans une liste classée. La valeur de cette propriété est l’URI (@id) de la fonction à appeler avec l’option on à la fois. Voir schéma https://ns.adobe.com/experience/decisioning/rankingStrategy.
   **Type :** string

**_experience > prise de décision > ranking > Priority**

**Champ :** priority
**Titre :** Priorité
**Description :** La priorité d’une option de décision unique par rapport à toutes les autres options. Les options pour lesquelles aucune fonction de commande n’est donnée sont classées par priorité à l’aide de cette propriété. Les options avec des valeurs de priorité plus élevée sont sélectionnées avant toute option de priorité plus faible. Si plusieurs options admissibles partagent la valeur de priorité la plus élevée, une option est choisie de manière aléatoire uniforme et utilisée pour la proposition de décision.
**Type :** entier
**Valeur minimale :** 0
**Valeur par défaut :** 0

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
