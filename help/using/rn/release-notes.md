---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 84%

---

# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){{target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.

## Version de mai 2022 {#may-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Règles de fréquence des messages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des règles métier cross-canal qui excluront automatiquement les profils sursollicités des messages et actions.</p>
<img src="assets/frequency-rn.gif"/>
<p>Pour plus d’informations, consultez la <a href="../configuration/frequency-rules.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Email BCC</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Availability date: <strong>May, 31</strong></p>
<p>You can now use the Email BCC (blind carbon copy) capability to store emails sent by Adobe Journey Optimizer. Enable this option in your email presets so that every email sent is blind-copied to your BCC address.</p>
<img src="assets/bcc-rn.gif"/>
<p>For more information, refer to the <a href="../configuration/email-settings.md#bcc-email">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Gestion des décisions - Modèle d’optimisation automatique du classement AI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser des systèmes de modèle formés dans la gestion de la décision. Cette nouvelle fonctionnalité classe les offres à afficher pour un profil donné.</p>
<img src="assets/optimization.gif"/>
<p>Pour plus d’informations, consultez la <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

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

* **Nouvelle fonction d’assistance pour le masquage des caractères** : la fonction d’assistance `mask` vous permet de remplacer une partie d’une chaîne par des caractères « X ». [En savoir plus](../personalization/functions/string.md#mask)

**Pages de destination**

* **Pages de destination sans formulaire** : vous pouvez maintenant créer et publier une page de destination qui ne contient pas de formulaire et ne nécessite aucune action de la part des visiteurs.
* **Modèles de page de destination** : vous pouvez maintenant enregistrer une page de destination en tant que modèle et la réutiliser lors de la création d’autres pages de destination. [En savoir plus](../landing-pages/lp-templates.md)
* **Retour à la page principale** : vous pouvez maintenant ajouter un lien vers la page principale à partir de n’importe quelle sous-page de la même page de destination.
* **Prise en charge de code JavaScript personnalisé** : vous pouvez désormais ajouter du code JavaScript personnalisé au contenu de votre page de destination pour appliquer un style avancé ou ajouter des comportements personnalisés à vos pages de destination.	[En savoir plus](../landing-pages/lp-custom-js.md)

**Parcours**

* **Lecture de segment** : les parcours de lecture de segment en une seule fois sont désormais mis à l’état Terminé 30 jours après l’exécution du parcours. Pour la lecture de segment planifiée, cela se passe 30 jours après l’exécution de la dernière occurrence. [En savoir plus](../building-journeys/read-segment.md)
* **Éditeur d&#39;expression** : la fonction [limit](../building-journeys/functions/functionlimit.md) a été ajoutée pour vous permettre de limiter le nombre d’éléments d’une liste. La fonction [sort](../building-journeys/functions/functionsort.md) vous permet désormais de trier un objet de liste. La prise en charge de listObject a également été ajoutée aux fonctions [Disctinct](../building-journeys/functions/functiondistinct.md) et [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md).

**Administration**

* **Mise à jour du tableau de bord d’utilisation des licences** - Le tableau de bord de l’utilisation de la licence disponible dans la [!DNL Adobe Journey Optimizer] L’interface utilisateur reflète désormais la valeur exacte de la variable **Sous licence** Richesse moyenne des profils. Vous verrez une baisse de cette représentation de mesure, ce qui signifie que la limite de licence est désormais correctement signalée. [En savoir plus](../start/licence-usage.md)
