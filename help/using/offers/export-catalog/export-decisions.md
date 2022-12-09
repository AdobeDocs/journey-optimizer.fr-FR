---
title: Jeu de données de décisions
description: Cette section répertorie tous les champs utilisés dans le jeu de données exporté pour les décisions.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: 353aaf2bc4f32b1b0d7bfc2f7f4f48537cc79df4
workflow-type: tm+mt
source-wordcount: '1524'
ht-degree: 0%

---

# Jeu de données de décisions {#decisions-dataset}

Chaque fois qu’une offre est modifiée, le jeu de données généré automatiquement pour les décisions (anciennement appelé activités) est mis à jour.

![](../assets/dataset-activities.png)

Le dernier lot réussi du jeu de données s’affiche à droite. La vue hiérarchique du schéma du jeu de données s’affiche dans le volet de gauche.

>[!NOTE]
>
>Découvrez comment accéder aux jeux de données exportés pour chaque objet de votre bibliothèque d’offres dans [cette section](../export-catalog/access-dataset.md).

Voici la liste de tous les champs pouvant être utilisés dans la variable **[!UICONTROL Decision Object Repository - Decisions]** jeu de données (anciennement appelé référentiel d’objets de décision - Activités).

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

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

#### _experience > prise de décision > critères

**Champ :** critères
**Titre :** Critères
**Description :** Définit un ensemble de critères de décision pour lesquels chacun contient un ensemble de contraintes.
**Type :** tableau

**_experience > prise de décision > critères > description**

**Champ :** description
**Titre :** Description
**Description :** Description du critère. Il est utilisé pour transmettre des intentions lisibles par l&#39;homme sur la façon dont ce critère a été construit ou pourquoi et sur la façon dont il influence la décision.
**Type :** string

**_experience > prise de décision > critères > optionSelection**

**Champ :** optionSelection
**Titre :** Sélection d’options
**Description :** La sélection d’options définit la validité/l’applicabilité des options dans ce contexte.
**Type :** objet

* **Description**

   **Champ :** description
   **Titre :** Description
   **Description :** Description de la sélection des options. Il est utilisé pour transmettre des intentions lisibles par l’utilisateur sur la façon dont cette option a été créée ou pourquoi cette sélection a été créée et/ou quelle option sera correspondante.
   **Type :** string

* **Filtre d’options**

   **Champ :** filter
   **Titre :** Filtre d’options
   **Description :** Référence à un filtre basé sur les balises qui correspond aux options d’un inventaire à l’aide des balises qui y sont associées. La valeur est l’URI (@id) de la règle de décision référencée. Voir schéma https://ns.adobe.com/experience/decisioning/filter.
   **Type :** string

* **Type de contrainte de profil**

   **Champ :** optionSelectionType
   **Titre :** Type de contrainte de profil
   **Description :** Détermine si des contraintes sont actuellement définies et comment les contraintes sont exprimées. Il peut s’agir d’une requête de filtre ou d’un ou plusieurs appartenances à un segment.
   **Type :** string
   **Valeurs possibles :** &quot;none&quot; (par défaut), &quot;directList&quot;, &quot;filter&quot;

* **Liste d’options**

   **Champ :** options
   **Titre :** Liste d’options
   **Description :** Liste qui spécifie directement les options sans évaluer une requête de filtre. Vous pouvez spécifier une liste d’options ou une règle de filtrage d’options.
   **Type :** tableau

   <!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

**_experience > prise de décision > critères > emplacements**

**Champ :** emplacements
**Titre :** Restrictions de positionnement
**Description :** La contrainte d’emplacement indique que ce critère s’applique uniquement aux emplacements répertoriés. Uniquement lorsque l’emplacement ciblé se trouve dans la variable `xdm:placements` liste est l’option sélectionnée. Sinon, l’intégralité des critères de décision est ignorée. Lorsque la liste &quot;xdm:emplacements&quot; est omise ou vide, le critère est pris en compte pour tout emplacement ciblé. Les emplacements répertoriés ici imposent des critères implicites pour la sélection de l’option. Une option à prendre en compte doit comporter une représentation pour l’emplacement ciblé.
**Type :** tableau

* **Identifiant de référencement**

   **Titre :** Identifiant de référencement
   **Description :** Référence à une entité d’emplacement. La valeur est l’URI (@id) de l’emplacement référencé. Voir schéma https://ns.adobe.com/experience/decisioning/placement.
   **Type :** string

**_experience > prise de décision > critères > profileConstraints**

**Champ :** profileConstraints
**Titre :** Contrainte de profil
**Description :** La contrainte de profil détermine si une sélection d’options est éligible pour cette identité de profil à ce moment, dans ce contexte. Si la contrainte de profil n’a pas besoin de prendre en compte les valeurs de chacune des options, c’est-à-dire qu’elle est invariante des options de la sélection de l’option, la contrainte de profil qui évalue &quot;false&quot; annule toute la sélection d’options. D’un autre côté, une règle de contrainte de profil qui utilise une option comme paramètre est évaluée pour chaque option admissible de la sélection d’option.
**Type :** objet

* **_experience > prise de décision > critères > profileConstraints > Description**

   **Champ :** description
   **Titre :** Description
   **Description :** Description des contraintes de profil. Il est utilisé pour transmettre des intentions lisibles par l’utilisateur sur la manière ou les raisons pour lesquelles cette contrainte de profil a été construite et/ou sur l’option qui y sera incluse ou exclue.
   **Type :** string

* **_experience > prise de décision > critères > profileConstraints > Règle d’éligibilité**

   **Champ :** éligibilitéRule
   **Titre :** Règle d’éligibilité
   **Description :** Référence à une règle de décision qui renvoie true (vrai) ou false (faux) pour un profil donné et/ou d’autres objets XDM contextuels donnés. La règle permet de décider si l’option est admissible pour un profil donné. La valeur est l’URI (@id) de la règle de décision référencée. Voir schéma https://ns.adobe.com/experience/decisioning/rule.
   **Type :** string

* **_experience > prise de décision > critères > profileConstraints > Type de contrainte de profil**

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

* **_experience > prise de décision > critères > profileConstraints > segmentIdentities**

   **Champ :** segmentIdentities
   **Titre :** Identifiants de segment
   **Description :** Identifiants des segments.
   **Type :** tableau

   * **Identifiant**

      **Champ :** _id
      **Titre :** Identifiant
      **Description :** Identité du segment dans l’espace de noms associé.
      **Type :** string

   * **namespace**

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


**_experience > prise de décision > critères > classement**

**Champ :** ranking
**Titre :** Détails du classement
**Description :** Classement (priorité). Définit la manière dont la \&quot;meilleure option\&quot; est déterminée selon le contexte du critère de décision. Parmi toutes les options sélectionnées qui respectent les contraintes de profil, le classement décidera de la ou des N premières options à proposer.
**Type :** objet

* **_experience > prise de décision > critères > classement > ordre**

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

* **_experience > prise de décision > critères > classement > Priorité**

   **Champ :** priority
   **Titre :** Priorité
   **Description :** La priorité d’une option de décision unique par rapport à toutes les autres options. Les options pour lesquelles aucune fonction de commande n’est donnée sont classées par priorité à l’aide de cette propriété. Les options avec des valeurs de priorité plus élevée sont sélectionnées avant toute option de priorité plus faible. Si plusieurs options admissibles partagent la valeur de priorité la plus élevée, une option est choisie de manière aléatoire uniforme et utilisée pour la proposition de décision.
   **Type :** entier
   **Valeur minimale :** 0
   **Valeur par défaut :** 0

#### _experience > prise de décision > Date et heure de fin de l’activité

**Champ :** endTime
**Titre :** Date et heure de fin de l’activité
**Description :** Date et heure de fin de la décision (anciennement appelée activité). La propriété a la sémantique de la propriété &quot;endTime&quot; de schema.org définie sur http://schema.org/Action.
**Type :** string

#### _experience > prise de décision > Option de secours

**Champ :** secours
**Titre :** Option de secours
**Description :** La référence à une option de secours utilisée lors de la prise de décision dans le contexte de cette décision ne remplit aucune des conditions requises pour l’une des options standard (cela se produit généralement lorsque des contraintes difficiles sont appliquées). La valeur est l’URI (@id) de l’option de secours référencée.
**Type :** string

#### _experience > prise de décision > Nom de l’activité

**Champ :** name
**Titre :** Nom de l’activité
**Description :** Nom de décision (anciennement appelé activité) affiché dans différentes interfaces utilisateur.
**Type :** string

#### _experience > prise de décision > Date et heure de début de l’activité

**Champ :** startTime
**Titre :** Date et heure de début de l’activité
**Description :** Date et heure de début de la décision (anciennement appelée activité). La propriété a la sémantique de la propriété &quot;startTime&quot; de schema.org définie sur http://schema.org/Action.
**Type :** string

## _repo {#repo}

**Champ :** _repo
**Type :** objet

### _repo > Activity ETag

**Champ :** etag
**Titre :** Activity ETag
**Description :** La révision à laquelle se trouvait l’objet de décision (anciennement appelé activité) lorsque l’instantané a été pris.
**Type :** string
