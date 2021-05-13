---
title: Prise en main de l’export de catalogues d’offres
description: Cette section liste tous les champs utilisés dans le jeu de données exporté pour les décisions.
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '1487'
ht-degree: 4%

---

# Jeu de données de décisions {#decisions-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les décisions est mis à jour.

![](../../assets/dataset-activities.png)

Le lot le plus récent du jeu de données qui a réussi s&#39;affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d&#39;Offres dans [cette section](../export-catalog/access-dataset.md).

Voici la liste de tous les champs qui peuvent être utilisés dans le référentiel d&#39;objets de décision **[!UICONTROL Decision Object Repository - Decision]** dataset (anciennement appelé référentiel d&#39;objets de décision - Activités).

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

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

#### critères

**Champ:** critère 
**Titre:** Critère 
**Description:** Définit un ensemble de critères de décision où chacun contient un ensemble de contraintes.
**Type:** tableau

* **description**

   **Champ:** description
   **Titre:** Description
   **Description : description du** critère. Il est utilisé pour transmettre des intentions lisibles sur la façon dont ce critère a été construit et sur la façon dont il influe sur la décision.
   **Type :** Chaîne

* **optionSelection**

   **Champ:** optionSelection
   **Titre:Sélection** d’options
   **Description :** La sélection d&#39;options définit la validité/l&#39;applicabilité des options dans ce contexte.
   **Type:** objet

   * **Description**

      **Champ:** description
      **Titre:** Description
      **Description : description de la sélection** Option. Il est utilisé pour transmettre des intentions lisibles sur la façon et les raisons pour lesquelles cette sélection d&#39;options a été construite et/ou sur l&#39;option qui va correspondre.
      **Type :** Chaîne

   * **Filtre d’options**

      **Champ:** filtre
      **Titre:Filtre** d’options
      **Description :** référence à un filtre basé sur les balises qui correspond aux options d’un inventaire à l’aide de leurs balises jointes. La valeur est l’URI (@id) de la règle de décision référencée. Voir schéma https://ns.adobe.com/experience/decisioning/filter.
      **Type :** Chaîne

   * **Type de contrainte de profil**

      **Champ:** optionSelectionType
      **Titre:Type de contrainte de** Profil
      **Description :** détermine si des contraintes sont actuellement définies et comment les contraintes sont exprimées. Il peut s’agir d’une requête de filtrage ou d’une ou plusieurs adhésions de segment.
      **Type :**Chaîne
      **Valeurs possibles :** &quot;directList&quot;, &quot;filter&quot;
      **Valeur par défaut :** &quot;none&quot;

   * **Liste d’options**

      **Champ:** options
      **Titre:Liste** Option
      **Description :** liste qui spécifie directement les options sans évaluer une requête de filtre. Vous pouvez spécifier une liste d&#39;option ou une règle de filtre d&#39;option.
      **Type:** tableau

      <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

* **placements**

   **Champ:** placement
   **Titre:Restrictions** de positionnement
   **Description :** La contrainte de placement indique que ce critère ne s&#39;applique qu&#39;aux emplacements répertoriés. Seule la sélection d&#39;options prise en compte est lorsque l&#39;emplacement ciblé se trouve dans la liste `xdm:placements`. Sinon, l’ensemble des critères de décision est ignoré. Lorsque la liste xdm:placements est omise ou vide, le critère est pris en compte pour tout placement ciblé. Les emplacements répertoriés ici imposent des critères implicites pour la sélection d&#39;options. Une option à prendre en compte doit comporter une représentation pour l’emplacement ciblé.
   **Type:** tableau

   * **Identificateur de positionnement**

   **Titre:Identifiant** de positionnement
   **Description :** Référence à une entité de placement. La valeur est l’URI (@id) du placement référencé. Voir schéma https://ns.adobe.com/experience/decisioning/placement.
   **Type :** Chaîne

* **profileConstraints**

   **Champ:** profileConstraints
   **Titre:Contrainte** de Profil
   **Description :** La contrainte de profil détermine si une sélection d&#39;option est éligible pour cette identité de profil en ce moment, dans ce contexte. Si la contrainte de profil n&#39;a pas besoin de prendre en compte les valeurs de chacune des options, c&#39;est-à-dire qu&#39;elle est invariante des options de la sélection d&#39;options, la contrainte de profil qui prend la valeur &quot;false&quot; annule l&#39;ensemble de la sélection d&#39;options. D’un autre côté, une règle de contrainte de profil qui prend une option en tant que paramètre est évaluée pour chaque option de qualification de la sélection d’options.
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
      **Description :** Identifiants des segments.
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



* **classement**

   **Champ:** classement
   **Titre:Détails** du classement
   **Description :** Classement (priorité). Définit comment la \&quot;meilleure option\&quot; est déterminée en fonction du contexte du critère de décision. Parmi toutes les options sélectionnées qui répondent aux contraintes de profil, le classement décidera de la ou des options supérieures (ou supérieures N) à proposer.
   **Type:** objet

   * **order**

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


#### Date et heure de fin de l’activité

**Champ :** endTime 
**Title:** Activité End Date and Time 
**Description:** Decision end date and end time. La propriété a la sémantique de la propriété &quot;endTime&quot; de schéma.org définie sur http://schema.org/Action.
**Type :** Chaîne

#### Option de secours

**Champ :** secours 
**Titre :** Option de secours 
**Description :** La référence à une option de secours utilisée lors de la prise de décision dans le cadre de cette décision ne remplit aucune des options habituelles (cela se produit généralement lorsque des contraintes strictes sont appliquées). La valeur est l’URI (@id) de l’option de secours référencée.
**Type :** Chaîne

#### Nom de l’activité

**Champ:** nom 
**Titre:Nom de l’** Activité 
**Description:Nom de la** décision qui s’affiche dans différentes interfaces utilisateur.
**Type :** Chaîne

#### Date et heure de début de l’activité

**Champ :** startTime 
**Title:** Activité Début Date et heure 
**Description : début** de décision Date et heure de fin. La propriété a la sémantique de la propriété &#39;startTime&#39; de schéma.org définie sur http://schema.org/Action.
**Type :** Chaîne

## _repo

**Champ:** _repo 
**Type:** objet

### Activité ETag

**Champ :** balise 
**Titre:** Activité ETag 
**Description :** la révision à laquelle l&#39;objet de décision se trouvait au moment de la prise de l&#39;instantané.
**Type :** Chaîne
