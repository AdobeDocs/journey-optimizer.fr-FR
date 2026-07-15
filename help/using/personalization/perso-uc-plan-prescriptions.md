---
title: Exemples de personnalisation de modèles
description: Exemples de personnalisations Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
TQID: https://experienceleague.adobe.com/fZtkkz9pvdZ3G7ojmHlNhasxawVbXmBHX-uznq6hseY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 522
ht-degree: 21%

---

# E-mail d’ordonnances de programmes de santé {#plan-prescription}

>[!BEGINSHADEBOX]

**Sur cette page :** Suivez un cas d’utilisation de personnalisation qui effectue une itération sur des tableaux de profils imbriqués avec des règles conditionnelles pour créer un plan d’intégrité en répertoriant les ordonnances qui sont prêtes à être récupérées ou rappelées.

>[!ENDSHADEBOX]

Un profil contient des programmes de santé, et chaque programme inclut des ordonnances. Les ordonnances comportent différents états, tels que « prêt », « rappel » ou « récupéré ».

Dans ce cas d’utilisation, nous souhaitons envoyer un seul e-mail à chaque profil, contenant toutes les ordonnances qui sont prêtes à être récupérées ou rappelées. Cliquez sur chaque onglet ci-dessous pour plus d’informations sur la syntaxe à utiliser pour mettre en œuvre ce cas d’utilisation.

>[!BEGINTABS]

>[!TAB Message affiché]

<p>Bonjour Jean Dupont,</p>
<p>Voici les ordonnances qui sont prêtes à être récupérées ou qui ont été rappelées :</p>

**Programme de santé A**

<ul>

<li>
      <strong>Prescription ID:</strong> pres1<br>
      <strong>Nom : </strong> Médicament A<br>
      <strong>State:</strong> ready
   </li>

<li>
      <strong>Prescription ID:</strong> pres2<br>
      <strong>Nom :</strong> Médicament B<br>
      <strong>State:</strong> rappel
   </li>

</ul>

**Programme de santé B**

<ul>

<li>
      <strong>Prescription ID:</strong> pres4<br>
      <strong>Nom :</strong> D de médicament<br>
      <strong>State:</strong> ready
   </li>

</ul>

>[!TAB Modèle HTML]

```html
<p>Hi {{profile.person.firstName}} {{profile.person.lastName}},</p>
<p>Here are the prescriptions that are either ready for pick up or have been recalled:</p>
{{#each profile.plans as |plan|}}
<h3>{{plan.name}}</h3>
<ul>
   {{#each plan.prescriptions as |prescription|}}
   {%#if prescription.state = "ready" or prescription.state = "recall"%}
   <li>
      <strong>Prescription ID:</strong> {{prescription.prescription_id}}<br>
      <strong>Name:</strong> {{prescription.name}}<br>
      <strong>State:</strong> {{prescription.state}}
   </li>
   {%/if%}
   {{/each}}
</ul>
{{/each}}
```

>[!TAB Données de profil]

```javascript
{
  "profile": {
    "person": {
      "firstName": "John",
      "lastName": "Doe"
    },
    "plans": [
      {
        "planId": "plan1",
        "name": "Health Plan A",
        "prescriptions": [
          {
            "prescription_id": "pres1",
            "name": "Medication A",
            "state": "ready"
          },
          {
            "prescription_id": "pres2",
            "name": "Medication B",
            "state": "recall"
          }
        ]
      },
      {
        "planId": "plan2",
        "name": "Health Plan B",
        "prescriptions": [
          {
            "prescription_id": "pres3",
            "name": "Medication C",
            "state": "picked up"
          },
          {
            "prescription_id": "pres4",
            "name": "Medication D",
            "state": "ready"
          }
        ]
      }
    ]
  }
}
```

>[!ENDTABS]

## Référence rapide {#quick-reference}

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

>[!BEGINTABS]

>[!TAB Vue d’ensemble]

**TL;DR**

Cette page présente un cas d’utilisation complet de la personnalisation : itération sur des tableaux de profils imbriqués (plans d’intégrité contenant des ordonnances) avec filtrage conditionnel pour afficher uniquement les ordonnances aux états « prêt » ou « rappel » dans un e-mail.

**Intentions**

* Voir un exemple de sortie rendu d’un e-mail de plan d’intégrité personnalisé
* Comprenez le modèle HTML utilisant des blocs de `{{#each}}` et de `{%#if%}` imbriqués pour l’itération de tableau conditionnel.
* Comprenez la structure de données de profil requise : un tableau `plans` où chaque plan contient un tableau `prescriptions` avec des champs `state`

>[!TAB Glossaire]

* **Itération imbriquée** : utilisation de boucles `{{#each}}` dans d’autres boucles `{{#each}}` pour parcourir les structures de tableau à plusieurs niveaux dans les données de profil (par exemple, plans → prescriptions).
* **État de la prescription** : champ sur chaque objet de prescription indiquant son statut de cycle de vie dans ce cas d’utilisation ; les valeurs utilisées sont « ready », « reminder » et « picked up ». *(spécifique au cas d’utilisation)*
* **`{%#if%}`/`{%/if%}`** : syntaxe de bloc conditionnelle utilisée dans les modèles de message pour filtrer les éléments de tableau lors de l’itération (distincte de la syntaxe Handlebars à double `{{#if}}`).

>[!TAB  Terminologie ]

* **Nom canonique :** itération de tableau imbriqué — variantes : boucles imbriquées, chacune imbriquée, itération à plusieurs niveaux
* **À ne pas confondre :** `{{#each}}` / `{{/each}}` (syntaxe d’itération Handlebars, accolades doubles) ≠ `{%#if%}` / `{%/if%}` (syntaxe conditionnelle, accolades en pourcentage) — les deux sont utilisés ensemble dans ce modèle
* **Ne pas confondre :** « prêt » (prescription disponible pour le retrait) ≠ « rappel » (la prescription a été retirée) ≠ « prélevé » (prescription déjà collectée — exclue de la sortie par le filtre conditionnel)

>[!TAB FAQ]

**Q : Quels états de prescription sont inclus dans la sortie de l’e-mail ?**

Seules les ordonnances dont l&#39;état est « ready » ou « reminder » s&#39;affichent. Les prescriptions avec l’état « sélectionné » sont exclues par le filtre conditionnel `{%#if prescription.state = "ready" or prescription.state = "recall"%}`.

**Q : Quelle structure de données de profil est requise pour ce cas d’utilisation ?**

Un profil avec un tableau `plans`, où chaque objet de plan contient un tableau `prescriptions`. Chaque objet de prescription doit comporter des champs `prescription_id`, `name` et `state`.

**Q : Comment les plans et les ordonnances sont-ils itérés dans le modèle ?**

La boucle de `{{#each profile.plans as |plan|}}` externe effectue une itération sur chaque plan d’intégrité. À l’intérieur, `{{#each plan.prescriptions as |prescription|}}` effectue une itération sur les prescriptions de chaque plan et un bloc conditionnel filtre uniquement les états « prêt » ou « rappel ».

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 4b68d597 -->
