---
title: Exemples de personnalisation de modèles
description: Exemples de personnalisations Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
TQID: https://experienceleague.adobe.com/fZtkkz9pvdZ3G7ojmHlNhasxawVbXmBHX-uznq6hseY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: cb09dcb7-3367-4b63-b02c-8a1356eb876eid: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: dab4adbad12736a8e9045f0d4095490d96ceaed9
workflow-type: tm+mt
source-wordcount: 116
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
