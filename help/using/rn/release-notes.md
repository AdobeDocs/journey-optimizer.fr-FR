---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 30d197f3eab05e2e38025189a6948a6c0fbd6d54
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 63%

---

# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){{target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.

## Version d’août 2022 {#aug-2022-release}

### Nouvelles fonctionnalités

<!--table>
<thead>
<tr>
<th><strong>Create and manage campaigns in Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use Journey Optimizer campaigns to deliver one-time content to a specific segment using various channels. When using journeys, actions are designed to be executed in sequence. With campaigns actions are performed simultaneously, either immediately, or based on a specified schedule. </p>
<p>For more information, refer to the <a href="../campaigns/get-started-with-campaigns.md">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Envoyer des SMS à vos utilisateurs (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer, personnaliser et envoyer des SMS dans Journey Optimizer, grâce à une intégration à <b>Sinch</b> ou <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Découvrez comment créer et envoyer un SMS dans cette <a href="../messages/create-sms.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->



### Améliorations

**Reporting**

* Le tableau et le graphique des stratégies de consentement sont désormais disponibles dans les rapports globaux par Parcours. Ces widgets vous permettent de suivre les profils exclus des stratégies de vos actions personnalisées. [En savoir plus](../reports/journey-global-report.md#journey-global)

   Pour avoir accès aux derniers widgets, vous devrez réinitialiser les différents tableaux de bord de rapports. Pour plus d’informations sur la personnalisation des tableaux de bord, reportez-vous à la section [la documentation détaillée ;](../reports/global-report.md).

**Administration**

* Il est désormais possible de mettre à jour le Principal numéro de téléphone à utiliser pour le canal SMS. [En savoir plus](../configuration/primary-email-addresses.md)