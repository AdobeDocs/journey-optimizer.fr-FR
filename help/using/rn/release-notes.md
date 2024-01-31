---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 146a142afeb47debac0d56963e48225a85b0f2c4
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 28%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.

## Notes de mise à jour initiales de janvier 2024 {#jan-2024}

**Date de publication**: 30-31 janvier 2024

### Nouvelles fonctionnalités{#jan24-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Mises à jour de délivrabilité</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer prend désormais en charge la technologie d’authentification DMARC.</p>
<p>À compter du 1er février 2024, Google et Yahoo! Vous devez disposer d’un enregistrement DMARC pour tout domaine que vous utilisez pour leur envoyer des emails. Assurez-vous que l’enregistrement DMARC est configuré pour tous les sous-domaines que vous avez délégués ou que vous déléguez à Adobe dans Journey Optimizer.</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/dmarc-record-update.md">documentation détaillée</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Cas d’utilisation des classeurs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Tirez parti d’un catalogue de playbooks de cas d’utilisation spécifiques au secteur dans Real-Time CDP et Journey Optimizer pour répondre aux cas d’utilisation courants que vous pouvez exécuter à l’aide de Adobe Experience Platform et de l’Adobe Parcours Optimiser.</p><p>Une fois que vous avez choisi le playbook qui correspond le mieux à vos besoins, vous pouvez lui permettre de générer les ressources nécessaires à la prise en charge de votre cas d’utilisation, tels que les parcours, les messages, les schémas ou les segments, et de les personnaliser dans votre schéma pour accélérer leur valorisation.</p>
<p>Pour plus d’informations, consultez la <a href="../start/playbooks.md">documentation détaillée</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Améliorations {#jan24-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Reporting**

* **Nouveaux widgets de ventilation basés sur des domaines** - De nouveaux widgets ont été ajoutés pour améliorer vos rapports Campaign et Parcours. La variable **Motifs de rebond par domaine**, **Envoyé et diffusé par domaines**, **Ouvertures et clics par domaine** et **Rebonds et erreurs par domaine** Les widgets fournissent une ventilation détaillée au niveau du domaine pour les mesures clés de diffusion et de suivi des emails. [En savoir plus](../reports/channel-report.md)

**Canal SMS**

* **Double opt-in** - Le workflow Double opt-in pour les SMS garantit que les utilisateurs s’engagent explicitement à recevoir des messages lorsque la demande est lancée à partir de leur appareil. Les utilisateurs lancent le processus de consentement en envoyant un SMS entrant. Une fois qu’ils ont confirmé leur consentement, un message de relance est envoyé, demandant une vérification finale. Si un profil utilisateur n’existe pas, il est créé lors de la confirmation. [En savoir plus](../sms/sms-configuration.md#create-api)

  Notez que cette fonctionnalité est disponible avec les fournisseurs SMS Sinch et Infobip.

**Parcours**

* **Durée des événements de réaction** : durée maximale que vous pouvez définir dans la variable **Événements de réaction** est désormais de 29 jours au lieu de 30. [En savoir plus](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Lecture d’audience**  - La variable **Lecture d’audience** L’activité repose désormais sur le jeu de données d’instantané de profil pour les segments par lot, qui n’est généré qu’une fois par jour après l’exécution de la tâche par lots quotidienne planifiée. Par conséquent, les données seront actualisées jusqu’à la dernière tâche par lot quotidienne. [En savoir plus](../building-journeys/read-audience.md)

* **Groupes de champs** - Cette version corrige un problème qui empêchait l’enregistrement des groupes de champs dans certains cas.

**Règles de fréquence**

* **Limite de fréquence hebdomadaire et quotidienne** - Vous pouvez désormais spécifier le nombre maximum de messages envoyés à un profil client au cours d’une semaine ou d’un jour, en plus du mois. Le plafond de fréquence est basé sur la période calendaire sélectionnée et est réinitialisé au début de la période correspondante. [En savoir plus](../configuration/frequency-rules.md#create-new-rule)

**Gestion des décisions**

* **Limitation de la fréquence sur Edge** - Le compteur de limitation de fréquence est maintenant mis à jour et disponible dans une décision de l’API Edge Decisioning en moins de 3 secondes. [En savoir plus](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)