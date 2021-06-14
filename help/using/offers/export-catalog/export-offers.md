---
title: Jeu de données d'offres personnalisées
description: Cette section répertorie tous les champs utilisés dans le jeu de données exporté pour les offres.
feature: Offres
topic: Intégrations
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '2012'
ht-degree: 100%

---

# Jeu de données d&#39;offres personnalisées {#offers-dataset}

Chaque fois qu&#39;une offre est modifiée, le jeu de données généré automatiquement pour les offres de contenu personnalisé est mis à jour.

![](../../assets/dataset-offers.png)

Le dernier lot du jeu de données s&#39;affiche à droite. La vue hiérarchique du schéma du jeu de données s&#39;affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque des offres dans [cette section](../export-catalog/access-dataset.md).

Vous trouverez ci-dessous la liste de tous les champs pouvant être utilisés dans le jeu de données **[!UICONTROL Référentiel d&#39;objets de décision - Offres personnalisées]**.

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

## Identifiant

**Champ :** _id 
**Titre :** identifiant
**Description :** identifiant unique de l&#39;enregistrement.
**Type :** chaîne

## _experience

**Champ :** _experience
**Type :** objet

### _experience > prise de décisions

**Champ :** prise de décisions
**Type :** objet

#### _experience > prise de décisions > calendarConstraints

**Champ :** calendarConstraints 
**Titre :** détails sur les contraintes de calendrier
**Description :** les contraintes de calendrier déterminent si une option de décision est valide sur une période. En dehors de cette période, l&#39;option ne peut pas être proposée.
**Type :** objet

* **Date et heure de fin**

   **Champ :** endDate
   **Titre :** date et heure de fin
   **Description :** date de fin de validité des options de décision. Les options qui ont dépassé leur date de fin ne peuvent plus être proposées dans le processus de prise de décision.
   **Type :** chaîne

* **Date et heure de début**

   **Champ :** startDate
   **Titre :** date et heure de début
   **Description :** date de début de validité des options de décision. Les options qui n&#39;ont pas atteint leur date de début ne peuvent pas encore être proposées dans le processus de prise de décision.
   **Type :** chaîne

#### _experience > prise de décisions > caractéristiques

**Champ :** caractéristiques 
**Titre :** caractéristiques de l&#39;option de décision
**Description :** propriétés ou attributs supplémentaires appartenant à cette option de décision spécifique. Différentes instances peuvent avoir différentes caractéristiques (clés dans le mappage). Les caractéristiques sont des paires nom-valeur utilisées pour distinguer une option de décision des autres. Les caractéristiques sont utilisées comme valeurs dans le contenu qui représente cette option de décision et comme fonctionnalités pour analyser et optimiser les performances d&#39;une option. Lorsque chaque instance possède le même attribut ou la même propriété, cet aspect doit être modélisé en tant que schéma d&#39;extension qui dérive du détail de l&#39;option de décision.
**Type :** objet

#### _experience > prise de décisions > contenu

**Champ :** contenu 
**Title :** détails du contenu 
**Description :** éléments de contenu pour effectuer le rendu de l&#39;élément de décision dans différents contextes. Une seule option de décision peut avoir plusieurs variantes de contenu. Le contenu est une information destinée à une audience pour être utilisée dans une expérience (numérique). Le contenu est diffusé par le biais de canaux à un emplacement spécifique.
**Type :** tableau

**_experience > prise de décisions > contenu > composants**

**Champ :** composants 
**Description :** composants du contenu représentant l&#39;option de décision, y compris toutes leurs variantes linguistiques. Les composants spécifiques sont identifiés par &#39;dx:format&#39;, &#39;dc:subject&#39; et &#39;dc:language&#39; ou une combinaison de ces composants. Ces métadonnées sont utilisées pour localiser ou représenter le contenu associé à une offre et l&#39;intégrer selon le contrat d&#39;emplacement.
**Type :** tableau 
**Obligatoire :** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > prise de décisions > contenu > composants > Type du composant du contenu**

   **Champ :** _type
   **Titre :** type du composant du contenu
   **Description :** jeu énuméré d&#39;URI où chaque valeur correspond à un type donné au composant de contenu. Certains consommateurs des représentations de contenu s&#39;attendent à ce que la valeur @type soit une référence au schéma qui décrit les propriétés supplémentaires du composant de contenu.
   **Type :** chaîne

* **_experience > prise de décisions > contenu > composants > _dc**

   **Champ :** _dc
   **Type :** objet
   **Obligatoire :** &quot;format&quot;

   * **Format**

      **Champ :** format
      **Titre :** format
      **Description :** manifestation physique ou numérique de la ressource. En règle générale, le format doit inclure le type de média de la ressource. Le format peut être utilisé pour déterminer le logiciel, le matériel ou tout autre équipement nécessaire pour afficher ou exploiter la ressource. Il est recommandé de sélectionner une valeur dans un vocabulaire contrôlé (par exemple, la liste des [types de média Internet](http://www.iana.org/assignments/media-types/) définissant les formats de médias informatiques).
      **Type :** chaîne
      **Exemple :** &quot;application/vnd.adobe.photoshop&quot;

   * **Langue**
      **Champ :** language
      **Titre :** langue
      **Description :** la ou les langues de la ressource. \nLes langues sont spécifiées dans le code de langue comme défini dans [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), qui fait partie de BCP 47, utilisé ailleurs dans XDM.
      **Type :** tableau
      **Exemples :** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **_experience > prise de décisions > contenu > composants > _repo**

   **Champ :** _repo
   **Type :** objet

   * **identifiant**

      **Champ :** id
      **Description :** identifiant unique facultatif permettant de référencer la ressource dans un référentiel de contenu. Lorsque les API de Platform sont utilisées pour récupérer la représentation, le client peut s&#39;attendre à une propriété supplémentaire \&quot;repo:resolveUrl\&quot; pour récupérer la ressource.
      **Type :** chaîne
      **Exemple :** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **name**

      **Champ :** nom
      **Description :** conseils sur l&#39;emplacement du référentiel qui stocke la ressource externe par le \&quot;repo:id\&quot;.
      **Type :** chaîne

   * **repositoryID**

      **Champ :** repositoryID
      **Description :** identifiant unique facultatif permettant de référencer la ressource dans un référentiel de contenu. Lorsque les API de Platform sont utilisées pour récupérer la représentation, le client peut s&#39;attendre à une propriété supplémentaire \&quot;repo:resolveUrl\&quot; pour récupérer la ressource.
      **Type :** chaîne
      **Exemple :** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **Champ :** resolveURL
      **Description :** localisateur de ressource unique facultatif pour lire la ressource dans un référentiel de contenu. Cela facilite l&#39;obtention de la ressource sans que le client comprenne où la ressource est gérée et les API à appeler. Ceci est similaire à un lien HAL, mais la sémantique est plus simple et plus pertinente.
      **Type :** chaîne
      **Exemple :** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **_experience > prise de décisions > contenu > composants > contenu**

   **Champ :** contenu
   **Description :** champ facultatif pour contenir directement le contenu. Au lieu de référencer le contenu dans un référentiel de ressources, le composant peut contenir directement du contenu simple. Ce champ n&#39;est pas utilisé pour les ressources de contenu composites, complexes et binaires.
   **Type :** chaîne

* **_experience > prise de décisions > contenu > composants > deliveryURL**

   **Champ :** deliveryURL
   **Description :** localisateur de ressource unique facultatif pour obtenir la ressource à partir d&#39;un réseau de diffusion de contenu ou d&#39;un point d&#39;entrée de service. Cette URL permet d&#39;accéder publiquement à la ressource par un agent utilisateur.
   **Type :** chaîne
   **Exemple :** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > prise de décisions > contenu > composants > linkURL**

   **Champ :** linkURL
   **Description :** localisateur de ressource unique facultatif pour les interactions utilisateur. Cette URL est utilisée pour renvoyer l&#39;utilisateur final vers un agent utilisateur et peut être suivie.
   **Type :** chaîne
   **Exemple :** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience > prise de décisions > contenu > Emplacement**

**Champ :** emplacement
**Titre :** emplacement 
**Description :** emplacement à respecter. La valeur est l&#39;URI (@id) de l&#39;emplacement d&#39;offre qui est référencé. Voir le schéma https://ns.adobe.com/experience/decisioning/placement.
**Type :** chaîne

#### _experience > prise de décisions > Statut du cycle de vie

**Champ :** lifecycleStatus 
**Titre :** statut du cycle de vie 
**Description :** le statut du cycle de vie permet d&#39;exécuter des workflows avec un objet. Le statut peut avoir une incidence lorsqu&#39;un objet est visible ou considéré comme pertinent. Les modifications de statut sont effectuées par les clients ou les services qui utilisent les objets.
**Type :** chaîne 
**Valeurs possibles :** &quot;Draft&quot; (par défaut), &quot;Approved&quot;, &quot;Live&quot;, &quot;Completed&quot;, &quot;Archived&quot;

#### _experience > prise de décisions > Nom de l&#39;option de décision

**Champ :** nom 
**Titre :** nom de l&#39;option de décision 
**Description :** nom de l&#39;option affiché dans différentes interfaces utilisateur.
**Type :** chaîne

#### _experience > prise de décisions > profileConstraints

**Champ :** profileConstraints 
**Titre :** détails des contraintes de profil 
**Description :** les contraintes de profil déterminent si une option est éligible pour cette identité de profil, à ce stade, dans ce contexte. Si la contrainte de profil n&#39;a pas besoin de prendre en compte les valeurs de chacune des options, c&#39;est-à-dire qu&#39;elle est invariante par rapport aux options de la sélection d&#39;options, la contrainte de profil qui évalue &#39;false&#39; annule toute la sélection d&#39;options. D&#39;un autre côté, une règle de contrainte de profil qui utilise une option comme paramètre est évaluée pour chaque option de qualification de la sélection d&#39;options.
**Type :** objet

**_experience > prise de décisions > profileConstraints > Description**

**Champ :** description 
**Titre :** description 
**Description :** description de la contrainte de profil. Utilisé pour transmettre des intentions lisibles par l&#39;homme sur la manière ou les raisons pour lesquelles cette contrainte de profil a été construite et/ou sur l&#39;option qui sera incluse ou exclue par cette contrainte.
**Type :** chaîne

**_experience > prise de décisions > profileConstraints > Règle d&#39;éligibilité**

**Champ :** eligibilityRule
**Titre :** règle d&#39;éligibilité
**Description :** référence à une règle de décision qui renvoie true ou false pour un profil donné et/ou d&#39;autres objets XDM contextuels donnés. La règle permet de décider si l&#39;option est admissible pour un profil donné. La valeur est l&#39;URI (@id) de la règle de décision référencée. Voir le schéma https://ns.adobe.com/experience/decisioning/rule.
**Type :** chaîne

**_experience > prise de décisions > profileConstraints > Type de contrainte de profil**

**Champ :** profileConstraintType
**Titre :** type de contrainte de profil
**Description :** détermine si des contraintes sont actuellement définies et comment elles sont exprimées. Cela peut se faire avec une règle ou avec un ou plusieurs appartenances au segment.
**Type :** chaîne
**Valeurs possibles :**
* &quot;none&quot; (par défaut)
* &quot;eligibilityRule&quot; : &quot;La contrainte de profil est exprimée sous la forme d&#39;une règle unique qui doit être évaluée sur true avant que l&#39;action contrainte ne soit autorisée.&quot;
* &quot;anySegments&quot; : &quot;La contrainte de profil est exprimée sous la forme d&#39;un ou plusieurs segments et le profil doit être membre d&#39;au moins l&#39;un d&#39;eux avant que l&#39;action limitée ne soit autorisée.&quot;
* &quot;allSegments&quot; : &quot;La contrainte de profil est exprimée sous la forme d&#39;un ou plusieurs segments et le profil doit être un membre de tous ces segments avant que l&#39;action limitée ne soit autorisée.&quot;
* &quot;rules&quot; : &quot;La contrainte de profil est exprimée sous la forme d&#39;un certain nombre de règles différentes, par exemple l&#39;éligibilité, l&#39;applicabilité, l&#39;adaptabilité, qui doivent toutes être évaluées sur true avant que l&#39;action limitée ne soit autorisée.&quot;

**_experience > prise de décisions > profileConstraints > Identifiants de segments**

**Champ :** segmentIdentities
**Titre :** identifiants de segment
**Description :** identifiants des segments
**Type :** tableau

* **Identifiant**

   **Champ :** _id
   **Titre :** identifiant
   **Description :** identité du client dans l&#39;espace de noms connexe.
   **Type :** chaîne

* **Espace de noms**

   **Champ :** espace de noms
   **Titre :** espace de noms
   **Description :** espace de noms associé à l&#39;attribut `xid`.
   **Type :** objet
   **Obligatoire :** &quot;code&quot;

   * **Code**

      **Champ :** code
      **Titre :** code
      **Description :** le code est un identifiant lisible par l&#39;homme pour l&#39;espace de noms et peut être utilisé pour demander l&#39;identifiant technique d&#39;espace de noms utilisé pour le traitement des graphiques d&#39;identités.
      **Type :** chaîne

* **Identifiant d&#39;expérience**

   **Champ :** xid
   **Titre :** identifiant de l&#39;expérience
   **Description :** lorsqu&#39;elle est présente, cette valeur représente un identifiant d&#39;espace de noms croisé unique pour tous les identifiants d&#39;espace de noms inclus dans tous les espaces de noms.
   **Type :** chaîne

#### _experience > prise de décisions > classement

**Champ :** classement
**Titre :** détails du classement
**Description :** classement (priorité). Définit ce qui est considéré comme la \&quot;meilleure action\&quot; selon le contexte du critère de décision. Parmi toutes les options sélectionnées qui répondent à la contrainte d&#39;éligibilité, l&#39;ordre de classement décidera de la ou des (N premières) options proposées.
**Type :** objet

**_experience > prise de décisions > classement > Évaluation de l&#39;ordre**

**Champ :** ordre
**Titre :** évaluation de l&#39;ordre
**Description :** évaluation d&#39;un ordre relatif d&#39;une ou de plusieurs options de décision. Les options avec des valeurs ordinales plus élevées sont sélectionnées à la place de n&#39;importe quelle option avec des valeurs ordinales plus faibles. Les valeurs déterminées par cette méthode peuvent être ordonnées, mais les distances entre elles ne peuvent pas être mesurées et, ni les sommes ni les produits ne peuvent être calculés. La médiane et le mode sont les seules mesures de tendance centrale qui peuvent être utilisées pour les données ordinales.
**Type :** objet

* **Fonction de notation**

   **Champ :** fonction
   **Titre :** fonction de notation
   **Description :** référence à une fonction qui calcule un score numérique pour cette option de décision. Les options de décision sont ensuite classées selon ce score. La valeur de cette propriété est l&#39;URI (@id) de la fonction à appeler avec une option à la fois. Voir le schéma https://ns.adobe.com/experience/decisioning/function.
   **Type :** chaîne

* **Type d&#39;évaluation de l&#39;ordre**

   **Champ :** orderEvaluationType
   **Titre :** type d&#39;évaluation de l&#39;ordre
   **Description :** indique le mécanisme d&#39;évaluation de l&#39;ordre utilisé, la priorité statique des options de décision, une fonction de notation qui calcule une valeur numérique pour chaque option ou une stratégie de classement qui reçoit une liste pour la classer.
   **Type :** chaîne
   **Valeurs possibles :** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;rankingStrategy&quot;

* **Stratégie de classement**

   **Champ :** rankingStrategy
   **Titre :** stratégie de classement
   **Description :** référence à une stratégie qui classe une liste d&#39;options de décision. Les options de décision sont renvoyées dans une liste classée. La valeur de cette propriété est l&#39;URI (@id) de la fonction à appeler avec une option à la fois. Voir le schéma https://ns.adobe.com/experience/decisioning/rankingStrategy.
   **Type :** chaîne

**_experience > prise de décisions > classement > Priorité**

**Champ :** priorité 
**Titre :** priorité 
**Description :** priorité d&#39;une seule option de décision par rapport à toutes les autres options. Les options pour lesquelles aucune fonction d&#39;ordre n&#39;est fournie sont classées par priorité à l&#39;aide de cette propriété. Les options avec des valeurs de priorité plus élevée sont sélectionnées avant toute option de priorité plus faible. Si plusieurs options admissibles partagent la valeur de priorité la plus élevée, une option est choisie de manière aléatoire uniforme et utilisée pour la proposition de décision.
**Type :** entier 
**Valeur minimum :** 0 
**Valeur par défaut :** 0

#### _experience > prise de décisions > balises

**Champ :** balises
**Titre :** balises 
**Description :** jeu de balises associées à cette entité. Les balises sont utilisées dans les expressions de filtre pour contraindre l&#39;inventaire global à un sous-ensemble (catégorie).
**Type :** tableau

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**Champ :** _repo 
**Type :** objet

### _repo > Etag d’option de décision

**Champ :** etag
**Titre :** ETag d’option de décision
**Description :** révision à laquelle l&#39;objet de l&#39;option de décision se trouvait lors de la prise de l&#39;instantané.
**Type :** chaîne



