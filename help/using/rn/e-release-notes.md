---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour anticipées de Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 97967e8043df9b75d3120e4a7bfccff700f5d57f
workflow-type: ht
source-wordcount: '558'
ht-degree: 100%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans les [notes de mise à jour](release-notes.md).

Les notes de mise à jour ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md), à la date de publication.

## Notes de mise à jour anticipées de janvier 2024 {#e-2024}

**Date de publication** : 20-31 janvier 2024

### Nouvelles fonctionnalités{#e-features}

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
<p>Journey Optimizer prend désormais en charge la technologie d’authentification DMARC.</p>
<p>À compter du 1er février 2024, Google et Yahoo! exigeront que vous disposiez d’un enregistrement DMARC pour tout domaine utilisé pour leur envoyer des e-mails. Vérifiez que l’enregistrement DMARC est configuré pour tous les sous-domaines que vous avez déjà délégués ou que vous déléguez actuellement à Adobe dans Journey Optimizer.</p>
<!--img src="assets/channel-reports.png"/-->
<p>Pour plus d’informations, consultez la <a href="../configuration/dmarc-record.md">documentation détaillée</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Playbooks de cas d’utilisation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Tirez profit d’un catalogue de playbooks de cas d’utilisation spécifiques à des secteurs d’activité dans Real-Time CDP et Journey Optimizer pour traiter les cas d’utilisation courants que vous pouvez exécuter à l’aide d’Adobe Experience Platform et d’Adobe Journey Optimizer.</p><p>Une fois que vous avez choisi le playbook qui correspond le mieux à vos besoins, vous pouvez lui permettre de générer les ressources nécessaires à la prise en charge de votre cas d’utilisation, telles que des parcours, des messages, des schémas ou des segments, et de les personnaliser dans votre schéma pour réduire le délai de rentabilisation.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
<!--<p>For more information, refer to the <a href="../start/playbooks.md">detailed documentation</a>.</p>-->
</tr>
</tbody>
</table>

### Améliorations {#e-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Création de rapports**

* **Nouveaux widgets de répartition basés sur les domaines** – Ajout de nouveaux widgets pour améliorer vos rapports Campaign et Journey. Les widgets **Raisons de rebond par domaine**, **Envoyés et diffusés par domaine**, **Ouvertures et clics par domaine** et **Rebonds et erreurs par domaine** fournissent une répartition détaillée des mesures principales de diffusion et de suivi des e-mails au niveau du domaine. [En savoir plus](../reports/channel-report.md)

**Canal SMS**

* **Double opt-in** – Le workflow Double opt-in pour les SMS garantit que les utilisateurs et les utilisatrices s’engagent explicitement à recevoir des messages lorsque la demande est envoyée à partir de leur appareil. Les utilisateurs et utilisatrices démarrent le processus de consentement en envoyant un SMS entrant. Une fois qu’ils ont confirmé leur consentement, un message de réponse est envoyé, demandant une vérification finale. Si un profil d’utilisateur ou d’utilisatrice n’existe pas, il est créé lors de la confirmation. [En savoir plus](../sms/sms-configuration.md#create-api)

  Notez que cela s’applique uniquement aux fournisseurs SMS Sinch et Infobip.

**Parcours**

* **Durée des événements de réaction** – La durée maximale que vous pouvez définir dans les **Événements de réaction** est désormais de 29 jours au lieu de 30. [En savoir plus](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Lecture d’audience** – L’activité Lecture d’audience repose désormais sur le jeu de données d’instantané de profil pour les segments par lots, qui n’est généré qu’une fois par jour après l’exécution du traitement par lots quotidien planifié. Par conséquent, les données sont à jour depuis le dernier traitement par lots quotidien.

* **Groupes de champs** – Correction d’un problème qui empêchait l’enregistrement des groupes de champs dans certains cas.

* **Éditeur d’expression** – Nous prenons désormais en charge le type de données listObject dans toutes les expressions et dans les fonctions supplémentaires. [Plus d’informations](../building-journeys/expression/functions.md)

**Règles de fréquence**

* **Limite de fréquence hebdomadaire et quotidienne** – Vous pouvez désormais spécifier le nombre maximum de messages envoyés à un profil client au cours d’une semaine ou d’un jour, en plus du mois. La limite de fréquence est basée sur la période calendaire sélectionnée et est réinitialisée au début de la période correspondante. [En savoir plus](../configuration/frequency-rules.md#create-new-rule)

**Gestion des décisions**

* **Capping de la fréquence sur Edge** – Le compteur de capping de fréquence est maintenant mis à jour et disponible dans une décision de l’API Edge Decisioning en moins de 3 secondes.