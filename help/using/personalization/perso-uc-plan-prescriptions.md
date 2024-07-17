---
title: Exemples de Personalization de modèles
description: Exemples de Journey Optimizer Personalization
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: f1d6c293fb8b22085911ab45c18f944a63b9655b
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# Email d’ordonnances de plans d’intégrité {#plan-prescription}

Un profil contient des plans d’intégrité, et chaque plan inclut des ordonnances. Les descriptions comportent différents états, tels que &quot;prêt&quot;, &quot;rappel&quot; ou &quot;relevé&quot;.

Dans ce cas pratique, nous souhaitons envoyer un seul email à chaque profil, y compris toutes les ordonnances qui sont prêtes à être prises ou rappelées. Cliquez sur chaque onglet ci-dessous pour plus d’informations sur la syntaxe à utiliser pour mettre en oeuvre ce cas pratique.

>[!BEGINTABS]

>[!TAB Message rendu]

<p>Bonjour John Doe,</p>
<p>Voici les ordonnances qui sont prêtes à être récupérées ou qui ont été rappelées :</p>

**Plan d’intégrité A**

<ul>

<li>
      <strong>ID de description :</strong> presse1<br>
      <strong>Nom :</strong> Médicament A<br>
      <strong>État :</strong> prêt
   </li>

<li>
      <strong>ID de description :</strong> pres2<br>
      <strong>Nom : </strong> Médicament B<br>
      <strong>État :</strong> rappel
   </li>

</ul>

**Plan d’intégrité B**

<ul>

<li>
      <strong>ID de description :</strong> presse4<br>
      <strong>Nom : </strong> Médicament D<br>
      <strong>État :</strong> prêt
   </li>

</ul>

>[!TAB Modèle d’HTML]

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
