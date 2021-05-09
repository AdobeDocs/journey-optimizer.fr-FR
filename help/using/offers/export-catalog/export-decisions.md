---
title: Commencer avec l'exportation de catalogues d'offres
description: Cette section liste tous les champs utilisés dans le jeu de données exporté pour les décisions.
translation-type: tm+mt
source-git-commit: d96a2b179ce652a119b6008e02b1409666f36402
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---

# Jeu de données de décisions {#decisions-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les décisions est mis à jour.

![](../assets/dataset-activities.png)

Le lot le plus récent du jeu de données qui a réussi s&#39;affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d&#39;Offres dans [cette section](../export-catalog/access-dataset.md).

Une décision (anciennement appelée décision d&#39;offre) est utilisée pour contrôler le processus de prise de décision. Il spécifie le filtre appliqué au stock total pour réduire les offres par rubrique/catégorie, le placement pour réduire le stock aux offres qui correspondent techniquement à l&#39;espace réservé pour l&#39;offre et spécifie une option de secours si les contraintes combinées disqualifient toutes les offres de personnalisation disponibles.

Voici la liste de tous les champs qui peuvent être utilisés dans le référentiel d&#39;objets de décision **[!UICONTROL Decision Object Repository - Decision]** dataset (anciennement appelé référentiel d&#39;objets de décision - Activités).

## Identificateur

Identificateur unique de l&#39;enregistrement.

Type : string

## _expérience

### prise de décision

#### critères

Définit un ensemble de critères de décision où chacun contient un ensemble de contraintes.

Type : tableau

* **Description**

   Description du critère. Il est utilisé pour transmettre des intentions lisibles sur la façon dont ce critère a été construit et sur la façon dont il influe sur la décision.

   Type : string

* **Sélection de l’option**

   La sélection d’options définit la validité/l’applicabilité des options dans ce contexte.

   Type : objet

   * **Description**

      Description de la sélection des options. Il est utilisé pour transmettre des intentions lisibles sur la façon et les raisons pour lesquelles cette sélection d&#39;options a été construite et/ou sur l&#39;option qui va correspondre.

      Type : string

   * **Filtre d’options**

      Référence à un filtre basé sur des balises qui correspond aux options d’un inventaire à l’aide de leurs balises jointes. La valeur est l’URI (@id) de la règle de décision référencée. Voir schéma https://ns.adobe.com/experience/decisioning/filter.

      Type : string

   * **Type de contrainte de profil**

      Détermine si des contraintes sont actuellement définies et comment les contraintes sont exprimées. Il peut s’agir d’une requête de filtrage ou d’une ou plusieurs adhésions de segment.

      Type : string

   * **Liste d’options**

      Liste qui spécifie directement les options sans évaluer une requête de filtre. Vous pouvez spécifier une liste d&#39;option ou une règle de filtre d&#39;option.

      Type : tableau

      <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option.-->

* **placements**

   La contrainte de placement indique que ce critère ne s&#39;applique qu&#39;aux emplacements répertoriés. Seule la sélection d&#39;options prise en compte est lorsque l&#39;emplacement ciblé se trouve dans la liste `xdm:placements`. Sinon, l’ensemble des critères de décision est ignoré. Lorsque la liste xdm:placements est omise ou vide, le critère est pris en compte pour tout placement ciblé. Les emplacements répertoriés ici imposent des critères implicites pour la sélection d&#39;options. Une option à prendre en compte doit comporter une représentation pour l’emplacement ciblé.

   Type : tableau

   * **Identificateur de positionnement**

   Référence à une entité de placement. La valeur est l’URI (@id) du placement référencé. Voir schéma https://ns.adobe.com/experience/decisioning/placement.

   Type : string

* **Contrainte de profil**

   La contrainte de profil détermine si une sélection d&#39;option est éligible pour cette identité de profil en ce moment, dans ce contexte. Si la contrainte de profil n&#39;a pas besoin de prendre en compte les valeurs de chacune des options, c&#39;est-à-dire qu&#39;elle est invariante des options de la sélection d&#39;options, la contrainte de profil qui prend la valeur &quot;false&quot; annule l&#39;ensemble de la sélection d&#39;options. D’un autre côté, une règle de contrainte de profil qui prend une option en tant que paramètre est évaluée pour chaque option de qualification de la sélection d’options.

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

      Valeurs possibles : &quot;none&quot;, &quot;entitlementRule&quot;, &quot;anySegments&quot;, &quot;allSegments&quot;, &quot;rules&quot;

      Valeur par défaut : &quot;none&quot;

   * **Identifiants de segment**

      Identifiants des segments

      Chaîne : tableau

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


* **Détails du classement**

   Classement (priorité). Définit comment la \&quot;meilleure option\&quot; est déterminée en fonction du contexte du critère de décision. Parmi toutes les options sélectionnées qui répondent aux contraintes de profil, le classement décidera de la ou des options supérieures (ou supérieures N) à proposer.

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

      * **Stratégie de classement**

         Référence à une stratégie qui classe une option de liste de décision. Les options de décision seront renvoyées dans une liste ordonnée. La valeur de cette propriété est l’URI (@id) de la fonction à appeler avec l’option on à la fois. Voir schéma https://ns.adobe.com/experience/decisioning/rankingStrategy.

         Type : string
   * **Priorité**

      La priorité d’une option de décision unique par rapport à toutes les autres options. Les options pour lesquelles aucune fonction de commande n’est fournie sont prioritaires à l’aide de cette propriété. Les options ayant des valeurs de priorité plus élevées sont sélectionnées avant les options de priorité plus faible. Si plusieurs options admissibles partagent la valeur de priorité la plus élevée, une option est choisie de façon aléatoire uniforme et utilisée pour la proposition de décision.

      Type : integer

      Valeur minimale : 0

      Valeur par défaut : 0


#### Date et heure de fin de l&#39;Activité

Date et heure de fin de la décision. La propriété a la sémantique de la propriété &quot;endTime&quot; de schéma.org définie sur http://schema.org/Action.

Type : string

#### Option de secours

La référence à une option de secours utilisée lors de la prise de décision dans le cadre de cette décision ne remplit aucune des options habituelles (cela se produit généralement lorsque des contraintes strictes sont appliquées). La valeur est l’URI (@id) de l’option de secours référencée.

Type : string

#### Nom de l’Activité

Nom de la décision affiché dans diverses interfaces utilisateur.

Type : string

#### Début d&#39;Activité Date et heure

Début de décision et heure de fin. La propriété a la sémantique de la propriété &#39;startTime&#39; de schéma.org définie sur http://schema.org/Action.

Type : string

## _repo

### Activité ETag

Révision à laquelle l&#39;objet de décision se trouvait lors de la prise de l&#39;instantané.

Type : string
