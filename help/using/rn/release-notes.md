---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: ht
source-wordcount: '233'
ht-degree: 100%

---

# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.


## Version d’octobre 2022 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### Améliorations {#oct-2022-improvements}

**Parcours**

* L’option **Forcer une reprise sur une périodicité** a été ajoutée dans les paramètres de planning de lecture de segment récurrent. Cette option permet de faire en sorte que tous les profils toujours présents dans le parcours le quittent automatiquement lors de la prochaine exécution. Lorsque l’option est désactivée, les profils doivent terminer le parcours avant de pouvoir entrer à nouveau dans une autre occurrence. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Administration**

* Un message a été ajouté à l’interface utilisateur pour signaler que les configurations du sous-domaine, du sous-domaine de la page de destination, de l’enregistrement PTR et du groupe d’adresses IP sont communes à toutes les sandbox. Toute modification de l’une de ces configurations aura donc un impact sur les sandbox de production.
* Les étapes de chargement de la liste de suppression au format CSV à partir de l’interface utilisateur ont été modifiées. [En savoir plus](../configuration/manage-suppression-list.md#download-suppression-list)

**Campagnes**

* Désormais, vous pouvez archiver les campagnes terminées et arrêtées. [En savoir plus](../campaigns/modify-stop-campaign.md#archive)
