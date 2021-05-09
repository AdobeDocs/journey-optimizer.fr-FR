---
title: Jeu de données d’offres personnalisées
description: Cette section liste tous les champs utilisés dans le jeu de données exporté pour les offres.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '1794'
ht-degree: 0%

---

# Jeu de données d&#39;offres personnalisées {#offers-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les offres de contenu personnalisées est mis à jour.

![](../assets/dataset-offers.png)

Le lot le plus récent du jeu de données qui a réussi s&#39;affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d&#39;Offres dans [cette section](../export-catalog/access-dataset.md).

Les offres personnalisées forment l’ensemble de choix pour une décision. L&#39;objectif de la prise de décision est de prendre un grand stock d&#39;articles et d&#39;appliquer de nombreuses règles de contrainte à cet inventaire pour le réduire, puis de classer les options admissibles selon un critère. Les propositions qui en résultent réunissent et personnalisent l&#39;expérience pour des individus spécifiques.

Voici la liste de tous les champs qui peuvent être utilisés dans le jeu de données **[!UICONTROL Decision Object Repository - Personalized Offres]**.

## Identificateur

Identificateur unique de l&#39;enregistrement.
Type : string

## _expérience

### prise de décision

#### calendarConstraints

**Détails** de contrainte de calendrier. Les contraintes de calendrier déterminent si une option de décision est valide dans une plage de dates. En dehors de cette plage de dates, l&#39;option ne peut pas être proposée.
Type : objet

* **Date et heure de fin**

   Date de fin de validité des options de décision. Les options qui ont dépassé leur date de fin ne peuvent plus être proposées dans le processus de décision.

   Type : string

* **Date et heure du début**

   La date de début d&#39;une décision peut être valide. Les options qui n&#39;ont pas atteint leur date de début ne peuvent pas encore être proposées dans le processus de prise de décision.

   Type : string

#### caractéristiques

**Caractéristiques** des options de décision. Autres propriétés ou attributs appartenant à cette option de décision particulière. Différentes instances peuvent présenter des caractéristiques différentes (clés dans la carte). Les caractéristiques sont des paires nom-valeur utilisées pour distinguer une option de décision des autres. Les caractéristiques sont utilisées comme valeurs dans le contenu qui représente cette option de décision et comme fonctionnalités pour analyser et optimiser les performances d&#39;une option. Lorsque chaque instance possède le même attribut ou la même propriété, cet aspect doit être modélisé en tant que schéma d&#39;extension dérivé des détails de l’option de décision.

Type : objet

#### Contenu

**Détails** du contenu. Éléments de contenu pour rendre l’élément de décision dans différents contextes. Une seule option de décision peut comporter plusieurs variantes de contenu. Le contenu est une information destinée à une audience destinée à être consommée dans une expérience (numérique). Le contenu est diffusé par canal dans un emplacement particulier.

Type : tableau

* ****
composantsComposants du contenu représentant l’option de décision, y compris toutes leurs variantes de langue. Les composants spécifiques sont identifiés par &quot;dx:format&quot;, &quot;dc:subject&quot; et &quot;dc:language&quot; ou une combinaison de ces composants. Ces métadonnées permettent de localiser ou de représenter le contenu associé à une offre et de l’intégrer selon le contrat de placement.

   * **Content Component**
TypeEnsemble énuméré d&#39;URI où chaque valeur correspond à un type donné au composant de contenu. Certains consommateurs des représentations de contenu s’attendent à ce que la valeur @type soit une référence au schéma qui décrit les propriétés supplémentaires du composant de contenu.
Type : string

   * **_dc**

      * ****
FormatLa manifestation physique ou numérique de la ressource. En règle générale, Format doit inclure le type de support de la ressource. Le format peut être utilisé pour déterminer le logiciel, le matériel ou tout autre équipement nécessaire pour afficher ou exploiter la ressource. Il est recommandé de sélectionner une valeur dans un vocabulaire contrôlé (par exemple, la liste de [Types de médias Internet](http://www.iana.org/ assignations/types de médias/) définissant les formats de supports informatiques).

         Type : string

         Exemple : &quot;application/vnd.adobe.photoshop&quot;

      * ****
LangueLangue ou langue de la ressource.\nLes langues sont spécifiées dans le code de langue tel que défini dans [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), qui fait partie du BCP 47, utilisé ailleurs dans XDM.

         Type : string

         Exemples : &quot;/n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;
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

         Exemple : &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

      * **resolveURL**

         Un localisateur de ressources unique facultatif pour lire la ressource dans un référentiel de contenu. Il sera ainsi plus facile d’obtenir la ressource sans que le client comprenne où la ressource est gérée et les API à appeler. Il s’agit d’un lien HAL, mais la sémantique est plus simple et plus utile.

         Type : string

         Exemple : &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&amp;quot&quot;
   * **content**

      Champ facultatif qui permet de conserver directement le contenu. Au lieu de référencer le contenu dans un référentiel de ressources, le composant peut contenir directement du contenu simple. Ce champ n’est pas utilisé pour les ressources de contenu composites, complexes et binaires.

      Type : string

   * **deliveryURL**

      Un localisateur de ressources unique facultatif pour obtenir la ressource à partir d’un réseau de diffusion de contenu ou d’un point de terminaison de service. Cette URL permet d’accéder publiquement à la ressource par un agent utilisateur.

      Type : string

      Exemple : &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

   * **linkURL**

      Un localisateur de ressources unique facultatif pour les interactions utilisateur. Cette URL permet de renvoyer l’utilisateur final dans un agent utilisateur et peut faire l’objet d’un suivi.

      Type : string

      Exemple : https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg



* **Placement**

   Emplacement à respecter. La valeur est l’URI (@id) de l’emplacement d’offre référencé. Voir schéma https://ns.adobe.com/experience/decisioning/placement.

#### État du cycle de vie

L’état du cycle de vie permet d’exécuter des workflows avec un objet. L’état peut avoir une incidence lorsqu’un objet est visible ou jugé pertinent. Les modifications d’état sont effectuées par les clients ou les services qui utilisent les objets.
Type : string
Valeurs possibles : Version préliminaire, approuvée, en direct, terminée, archivée

#### Nom de l’option de décision

Nom de l’option. Le nom s’affiche dans différentes interfaces utilisateur.
Type : string

#### Détails de contrainte de profil

Les contraintes de profil déterminent si une option est éligible pour cette identité de profil, à l&#39;heure actuelle, dans ce contexte. Si la contrainte de profil n&#39;a pas besoin de prendre en compte les valeurs de chacune des options, c&#39;est-à-dire qu&#39;elle est invariante des options de la sélection d&#39;options, la contrainte de profil qui prend la valeur &quot;false&quot; annule l&#39;ensemble de la sélection d&#39;options. D’un autre côté, une règle de contrainte de profil qui prend une option en tant que paramètre est évaluée pour chaque option de qualification de la sélection d’options.
Type : objet

* **Description**

   Description de la contrainte de profil. Il est utilisé pour transmettre des intentions lisibles sur la façon et les raisons pour lesquelles cette contrainte de profil a été construite et/ou sur l&#39;option qui sera incluse ou exclue par elle.
Type : string

* **règle d&#39;éligibilité**

   Référence à une règle de décision qui renvoie true ou false pour un profil donné et/ou d’autres objets XDM contextuels donnés. La règle est utilisée pour déterminer si l’option est admissible pour un profil donné. La valeur est l’URI (@id) de la règle de décision référencée. Voir schéma https://ns.adobe.com/experience/decisioning/rule.

   Type : string

* **Type de contrainte de profil**

   Détermine si des contraintes sont actuellement définies et comment les contraintes sont exprimées. Il peut s’agir d’une règle ou d’un ou plusieurs abonnements de segment.
Type : string
Valeurs possibles :

   * none

   * &quot;éligibilitéRule&quot; : &quot;La contrainte de profil est exprimée sous la forme d&#39;une règle unique qui doit être évaluée sur true avant d&#39;autoriser l&#39;action contrainte&quot;,

   * &quot;Tout segment&quot; : &quot;La contrainte de profil est exprimée en un ou plusieurs segments et le profil doit être membre d&#39;au moins l&#39;un d&#39;eux avant que l&#39;action contrainte ne soit autorisée&quot;,

   * &quot;Tous les segments&quot; : &quot;La contrainte de profil est exprimée en un ou plusieurs segments et le profil doit en être membre pour que l&#39;action limitée soit autorisée&quot;,

   * &quot;règles&quot; : &quot;La contrainte de profil est exprimée sous la forme d&#39;un certain nombre de règles différentes, par exemple l&#39;éligibilité, l&#39;applicabilité, l&#39;adaptabilité, qui doivent toutes être vérifiées avant que l&#39;action contrainte ne soit autorisée.&quot;

* **Identifiants de segment**

   Identifiants des segments

   * **Identificateur**

      Identité du segment dans l’espace de nommage associé.

      Type : string

   * **Espace de nommage**

      Espace de nommage associé à l&#39;attribut `xid`.

      Type : objet

      * **Code**

         Le code est un identifiant lisible par l&#39;homme pour l&#39;espace de nommage et peut être utilisé pour demander l&#39;ID d&#39;espace de nommage technique utilisé pour le traitement des graphiques d&#39;identité.

         Type : string
   * **Identifiant d’expérience**

      Lorsqu’elle est présente, cette valeur représente un identifiant de espace de nommage croisé unique pour tous les identifiants d’étendue d’espace de nommage dans tous les espaces de nommage.

      Type : string


#### Détails du classement

Classement (priorité). Définit ce qui est considéré comme la \&quot;meilleure action\&quot; compte tenu du contexte du critère de décision. Parmi toutes les options sélectionnées qui répondent à la contrainte d&#39;éligibilité, l&#39;ordre de classement décidera des options supérieures (ou supérieures N) à proposer.

Type : objet

* **Evaluation des commandes**

   Évaluation d&#39;un ordre relatif d&#39;une ou de plusieurs options de décision. Les options dont les valeurs ordinales sont supérieures sont sélectionnées pour les options dont les valeurs ordinales sont inférieures. Les valeurs déterminées par cette méthode peuvent être ordonnées mais les distances entre elles ne peuvent pas être mesurées et ni les sommes ni les produits ne peuvent être calculés. La médiane et le mode sont les seules mesures de tendance centrale qui peuvent être utilisées pour les données ordinales.

   Type : objet

   * **Fonction de score**

      Référence à une fonction qui calcule un score numérique pour cette option de décision. Les options de décision seront ensuite classées en fonction de ce score. La valeur de cette propriété est l’URI (@id) de la fonction à appeler avec l’option on à la fois. Voir schéma https://ns.adobe.com/experience/decisioning/function.

      Type : string

   * **Type d&#39;évaluation de commande**

      Spécifie le mécanisme d&#39;évaluation des commandes utilisé, la priorité statique des options de décision, une fonction de notation qui calcule une valeur numérique pour chaque option ou une stratégie de classement qui reçoit une liste pour la commander.

      Type : string

      Valeurs possibles : &quot;static&quot;, &quot;scoringFunction&quot;, &quot;placeStrategy&quot; <!--(TBC)-->

   * **Stratégie de classement**

      Référence à une stratégie qui classe une option de liste de décision. Les options de décision seront renvoyées dans une liste ordonnée. La valeur de cette propriété est l’URI (@id) de la fonction à appeler avec l’option on à la fois. Voir schéma https://ns.adobe.com/experience/decisioning/rankingStrategy.

      Type : string

* **Priorité**

   La priorité d’une option de décision unique par rapport à toutes les autres options. Les options pour lesquelles aucune fonction de commande n’est fournie sont prioritaires à l’aide de cette propriété. Les options ayant des valeurs de priorité plus élevées sont sélectionnées avant les options de priorité plus faible. Si plusieurs options admissibles partagent la valeur de priorité la plus élevée, une option est choisie de façon aléatoire uniforme et utilisée pour la proposition de décision.

   Type : integer

   Valeur minimale : 0

   Valeur par défaut : 0

#### Balises

Ensemble de balises associé à cette entité. Les balises sont utilisées dans les expressions de filtrage pour limiter le stock global à un sous-ensemble (catégorie).

* **éléments**

   Identificateur d’un objet de balise. La valeur est @id de la balise référencée. Voir schéma des balises : https://ns.adobe.com/experience/decisioning/tag.

## _repo

### Option de décision ETag

Révision à laquelle l&#39;objet d&#39;option de décision se trouvait lors de la prise de l&#39;instantané.

Type : string



