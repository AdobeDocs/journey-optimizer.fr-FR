---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: dd60e576aaded21efd9718341d1c4f26267ae001
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 35%

---

# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){{target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.

## Version de mai 2022 {#may-2022-release}

### Nouvelles fonctionnalités

<!--table>
<thead>
<tr>
<th><strong>Message Frequency Rules</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now set cross-channel business rules that will automatically exclude over-solicited profiles from messages and actions.</p>
<img src="assets/frequency-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/frequency-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>E-mail Cci</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser la fonctionnalité Email Cci (copie carbone invisible) pour stocker les emails envoyés par Adobe Journey Optimizer. Activez cette option dans vos paramètres prédéfinis d’e-mail de sorte que chaque e-mail envoyé soit copié aveuglément vers votre adresse Cci.</p>
<img src="assets/bcc-rn.gif"/>
<p>Pour plus d’informations, consultez la <a href="../configuration/email-settings.md#bcc-email">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Decision Management - AI Ranking auto-optimization model</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use trained model systems in Decision Management. This new capability ranks offers to display for a given profile.</p>
<img src="assets/optimization.gif"/>
<p>For more information, refer to the <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journaux d’audit Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais surveiller les actions effectuées par les utilisateurs sur les ressources Adobe Journey Optimizer.</p>
<img src="assets/audit-rn.gif"/>
<p>Pour plus d'informations, consultez la <a href="../reports/audit-logs.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Personnalisation**

* **Nouvelle fonction d’assistance pour le masquage des caractères** - Le `mask` La fonction d’assistance vous permet de remplacer une partie d’une chaîne par des caractères &quot;X&quot;. [En savoir plus](../personalization/functions/string.md#mask)

**Pages de destination**

* **Landing pages sans formulaire** - Vous pouvez désormais créer et publier une landing page qui ne contient pas de formulaire et ne nécessite aucune action de la part des visiteurs.
* **Modèles de landing page** - Vous pouvez désormais enregistrer une landing page en tant que modèle et la réutiliser lors de la création d&#39;autres landing pages. [En savoir plus](../landing-pages/lp-templates.md)
* **Retour à la Principale page** - Vous pouvez désormais ajouter un lien vers la Principale page à partir de n’importe quelle sous-page de la même page d’entrée.
* **Prise en charge JavaScript personnalisée** - Vous pouvez désormais ajouter du code JavaScript personnalisé au contenu de votre page d’entrée pour appliquer un style avancé ou ajouter des comportements personnalisés à vos pages d’entrée.	[En savoir plus](../landing-pages/lp-custom-js.md)

<!--**Decision management**

* **HTML and JSON files support** - You can now drag and drop external HTML and JSON files from the AEM repository into the offer representation content.-->

**Parcours**

* **Lecture de segment** - Les parcours de lecture en une seule fois de segment sont désormais mis à l’état Terminé 30 jours après l’exécution du parcours. Pour les segments de lecture planifiés, il s’agit de 30 jours après l’exécution de la dernière occurrence. [En savoir plus](../building-journeys/read-segment.md)
* **Editeur d&#39;expression** - Le [limit](../building-journeys/functions/functionlimit.md) a été ajoutée pour vous permettre de limiter le nombre d’éléments d’une liste. Le [sort](../building-journeys/functions/functionsort.md) vous permet désormais de trier un objet de liste. La prise en charge de listObject a également été ajoutée à la fonction [disctinct](../building-journeys/functions/functiondistinct.md) et [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) fonctions.
