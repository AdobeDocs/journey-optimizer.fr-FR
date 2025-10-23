---
title: Exemples de personnalisation de modèles
description: Exemples de personnalisations Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '131'
ht-degree: 100%

---

# E-mail d’ordonnances de programmes de santé {#plan-prescription}

Un profil contient des programmes de santé, et chaque programme inclut des ordonnances. Les ordonnances comportent différents états, tels que « prêt », « rappel » ou « récupéré ».

Dans ce cas d’utilisation, nous souhaitons envoyer un seul e-mail à chaque profil, contenant toutes les ordonnances qui sont prêtes à être récupérées ou rappelées. Cliquez sur chaque onglet ci-dessous pour plus d’informations sur la syntaxe à utiliser pour mettre en œuvre ce cas d’utilisation.

>[!BEGINTABS]

>[!TAB Message affiché]

<p>Bonjour Jean Dupont,</p>
<p>Voici les ordonnances qui sont prêtes à être récupérées ou qui ont été rappelées :</p>

**Programme de santé A**

<ul>

<li>
      <strong>ID d’ordonnance :</strong> pres1<br>
      <strong>Nom :</strong> Médicament A<br>
      <strong>État :</strong> prêt
   </li>

<li>
      <strong>ID d’ordonnance :</strong> pres2<br>
      <strong>Nom :</strong> Médicament B<br>
      <strong>État :</strong> rappel
   </li>

</ul>

**Programme de santé B**

<ul>

<li>
      <strong>ID d’ordonnance :</strong> pres4<br>
      <strong>Nom :</strong> Médicament D<br>
      <strong>État :</strong> prêt
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
