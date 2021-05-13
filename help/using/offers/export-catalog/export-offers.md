---
title: Jeu de données d’offres personnalisées
description: Cette section liste tous les champs utilisés dans le jeu de données exporté pour les offres.
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '1948'
ht-degree: 5%

---

# Jeu de données d&#39;offres personnalisées {#offers-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les offres de contenu personnalisées est mis à jour.

![](../../assets/dataset-offers.png)

Le lot le plus récent du jeu de données qui a réussi s&#39;affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d&#39;Offres dans [cette section](../export-catalog/access-dataset.md).

Voici la liste de tous les champs qui peuvent être utilisés dans le jeu de données **[!UICONTROL Decision Object Repository - Personalized Offres]**.

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

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

#### calendarConstraints

**Champ:** calendarConstraints 
**Titre:Détails de la contrainte** Calendrier 
**Description:Les contraintes** Calendrier déterminent si une option de décision est valide dans une plage de dates. En dehors de cette plage de dates, l&#39;option ne peut pas être proposée.
**Type:** objet

* **Date et heure de fin**

   **Champ:** endDate
   **Titre:Date et heure de** fin
   **Description :** date de fin de validité des options de décision. Les options qui ont dépassé leur date de fin ne peuvent plus être proposées dans le processus de décision.
   **Type :** Chaîne

* **Date et heure du début**

   **Champ:** startDate
   **Titre:Date et heure** du Début
   **Description :** date de début de validité des options de décision. Les options qui n&#39;ont pas atteint leur date de début ne peuvent pas encore être proposées dans le processus de prise de décision.
   **Type :** Chaîne

#### caractéristiques

**Champ:** caractéristiques 
**Titre:Option** Décision Caractéristiques 
**Description:Propriétés ou attributs** supplémentaires appartenant à cette option de décision particulière. Différentes instances peuvent présenter des caractéristiques différentes (clés dans la carte). Les caractéristiques sont des paires nom-valeur utilisées pour distinguer une option de décision des autres. Les caractéristiques sont utilisées comme valeurs dans le contenu qui représente cette option de décision et comme fonctionnalités pour analyser et optimiser les performances d&#39;une option. Lorsque chaque instance possède le même attribut ou la même propriété, cet aspect doit être modélisé en tant que schéma d&#39;extension dérivé des détails de l’option de décision.
**Type:** objet

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
         **Description :** La manifestation physique ou numérique de la ressource. En règle générale, Format doit inclure le type de support de la ressource. Le format peut être utilisé pour déterminer le logiciel, le matériel ou tout autre équipement nécessaire pour afficher ou exploiter la ressource. Il est recommandé de sélectionner une valeur dans un vocabulaire contrôlé (par exemple, la liste de [Types de médias Internet](http://www.iana.org/assignments/media-types/) définissant les formats de médias informatiques).
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

#### profileConstraints

**Champ :** profileConstraints 
**Titre : Détails de la contrainte de** Profil 
**Description :** Les contraintes de profil déterminent si une option est éligible pour cette identité de profil, à l&#39;heure actuelle, dans ce contexte. Si la contrainte de profil n&#39;a pas besoin de prendre en compte les valeurs de chacune des options, c&#39;est-à-dire qu&#39;elle est invariante des options de la sélection d&#39;options, la contrainte de profil qui prend la valeur &quot;false&quot; annule l&#39;ensemble de la sélection d&#39;options. D’un autre côté, une règle de contrainte de profil qui prend une option en tant que paramètre est évaluée pour chaque option de qualification de la sélection d’options.
**Type:** objet

* **Description**

   **Champ:** description
   **Titre:** Description
   **Description : description des contraintes** de Profil. Il est utilisé pour transmettre des intentions lisibles sur la façon et les raisons pour lesquelles cette contrainte de profil a été construite et/ou sur l&#39;option qui sera incluse ou exclue par elle.
   **Type :** Chaîne

* **Règle d’éligibilité**

   **Champ:** éligibilitéRule
   **Titre:** Règle d&#39;éligibilité
   **Description :** référence à une règle de décision qui renvoie true ou false pour un profil donné et/ou d’autres objets XDM contextuels donnés. La règle est utilisée pour déterminer si l’option est admissible pour un profil donné. La valeur est l’URI (@id) de la règle de décision référencée. Voir schéma https://ns.adobe.com/experience/decisioning/rule.
   **Type :** Chaîne

* **Type de contrainte de profil**

   **Champ:** profileConstraintType
   **Titre:Type de contrainte de** Profil
   **Description :** détermine si des contraintes sont actuellement définies et comment les contraintes sont exprimées. Il peut s’agir d’une règle ou d’un ou plusieurs abonnements de segment.
   **Type :**Chaîne
   **Valeurs possibles :**
   * &quot;aucun&quot;
   * &quot;éligibilitéRule&quot; : &quot;La contrainte de profil est exprimée sous la forme d’une règle unique qui doit être évaluée sur true avant que l’action contrainte ne soit autorisée.&quot;
   * &quot;anySegments&quot; : &quot;La contrainte de profil est exprimée en un ou plusieurs segments et le profil doit être membre d&#39;au moins l&#39;un d&#39;eux avant que l&#39;action contrainte ne soit autorisée.&quot;
   * &quot;allSegments&quot; : &quot;La contrainte de profil est exprimée en un ou plusieurs segments et le profil doit en être membre pour que l&#39;action restreinte soit autorisée.&quot;
   * &quot;règles&quot; : &quot;La contrainte de profil est exprimée sous la forme d&#39;un certain nombre de règles différentes, par exemple l&#39;éligibilité, l&#39;applicabilité, l&#39;adaptabilité, qui doivent toutes être vérifiées avant que l&#39;action contrainte ne soit autorisée.&quot;
      **Valeur par défaut :** &quot;none&quot;

* **Identifiants de segment**

   **Champ:** segmentIdentities
   **Titre:Identifiants de** segment
   **Description:** Identifiants des segments
   **Type:** tableau

   * **Identifiant**

      **Champ:** _id
      **Titre:** identifiant
      **Description :** identité du segment dans l’espace de nommage associé.
      **Type :** Chaîne

   * **Espace de noms**

      **Champ:** espace de nommage
      **Titre:** Espace de nommage
      **Description :** espace de nommage associé à l’ `xid` attribut.
      **Type:** objet
      **Obligatoire:** &quot;code&quot;

      * **Code**

         **Champ:** code
         **Titre:** Code
         **Description :** Le code est un identifiant lisible pour l&#39;espace de nommage et peut être utilisé pour demander l&#39;identifiant d&#39;espace de nommage technique utilisé pour le traitement des graphiques d&#39;identité.
         **Type :** Chaîne
   * **Identifiant d’expérience**

      **Champ:** xid
      **Titre:identifiant** d’expérience
      **Description :** Lorsqu’elle est présente, cette valeur représente un identifiant de espace de nommage croisé unique pour tous les identifiants d’étendue d’espace de nommage dans tous les espaces de nommage.
      **Type :** Chaîne


#### classement

**Champ:** classement 
**Titre:** Classement Détails 
**Description:** Classement (priorité). Définit ce qui est considéré comme la \&quot;meilleure action\&quot; compte tenu du contexte du critère de décision. Parmi toutes les options sélectionnées qui répondent à la contrainte d&#39;éligibilité, l&#39;ordre de classement décidera des options supérieures (ou supérieures N) à proposer.
**Type:** objet

* **Evaluation des commandes**

   **Champ:** ordre
   **Titre:Évaluation de** commande
   **Description :** Évaluation d&#39;un ordre relatif d&#39;une ou de plusieurs options de décision. Les options dont les valeurs ordinales sont supérieures sont sélectionnées pour les options dont les valeurs ordinales sont inférieures. Les valeurs déterminées par cette méthode peuvent être ordonnées mais les distances entre elles ne peuvent pas être mesurées et ni les sommes ni les produits ne peuvent être calculés. La médiane et le mode sont les seules mesures de tendance centrale qui peuvent être utilisées pour les données ordinales.
   **Type:** objet

   * **Fonction de score**

      **Champ:** fonction
      **Titre:Fonction** de score
      **Description :** Référence à une fonction qui calcule un score numérique pour cette option de décision. Les options de décision seront ensuite classées en fonction de ce score. La valeur de cette propriété est l’URI (@id) de la fonction à appeler avec l’option on à la fois. Voir schéma https://ns.adobe.com/experience/decisioning/function.
      **Type :** Chaîne

   * **Type d&#39;évaluation de commande**

      **Champ:** orderEvaluationType
      **Titre:Type d’évaluation de** commande
      **Description :** indique le mécanisme d&#39;évaluation de l&#39;ordre utilisé, la priorité statique des options de décision, une fonction de notation qui calcule une valeur numérique pour chaque option ou une stratégie de classement qui reçoit une liste pour la commander.
      **Type :**Chaîne
      **Valeurs possibles :** &quot;static&quot;, &quot;scoringFunction&quot;, &quot;meilleures stratégies&quot;

   * **Stratégie de classement**

      **Champ:** classementStratégie
      **Titre:Stratégie de** classement
      **Description :** Référence à une stratégie qui classe une option de liste de décision. Les options de décision seront renvoyées dans une liste ordonnée. La valeur de cette propriété est l’URI (@id) de la fonction à appeler avec l’option on à la fois. Voir schéma https://ns.adobe.com/experience/decisioning/rankingStrategy.
      **Type :** Chaîne

* **Priorité**

   **Champ:** priorité
   **Titre:** Priorité
   **Description :** priorité d’une option de décision unique par rapport à toutes les autres options. Les options pour lesquelles aucune fonction de commande n’est fournie sont prioritaires à l’aide de cette propriété. Les options ayant des valeurs de priorité plus élevées sont sélectionnées avant les options de priorité plus faible. Si plusieurs options admissibles partagent la valeur de priorité la plus élevée, une option est choisie de façon aléatoire uniforme et utilisée pour la proposition de décision.
   **Type:** integer
   **Valeur minimale :** 0
   **Valeur par défaut :** 0

#### balises

**Champ:** balises 
**Titre:** Balises 
**Description:** Ensemble de balises associées à cette entité. Les balises sont utilisées dans les expressions de filtrage pour limiter le stock global à un sous-ensemble (catégorie).
**Type:** tableau

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**Champ:** _repo 
**Type:** objet

### Option de décision ETag

**Champ :** balise 
**Titre :** Option de décision ETag 
**Description :** la révision à laquelle l&#39;objet de l&#39;option de décision se trouvait au moment de la prise de l&#39;instantané.
**Type :** Chaîne



