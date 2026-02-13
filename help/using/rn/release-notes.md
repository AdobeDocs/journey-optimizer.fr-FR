---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7263e5ace72823ce7a3a184d2842f9bba495c068
workflow-type: tm+mt
source-wordcount: '1537'
ht-degree: 31%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continue, ce qui permet à Adobe de diffuser régulièrement de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements.

En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Notes de préversion de février 2026 {#feb-26-01-rn}

**Les notes de version préliminaire ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les notes de mise à jour, à la date de publication.

Voir également les [Notes de mise à jour préliminaires d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Date de publication** : 17-18 février 2026

### Nouvelles fonctionnalités {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>Vague d’envoi des messages sortants</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez planifier la diffusion des messages sortants provenant de <strong>campagnes</strong> ou <strong>parcours </strong> par <strong>lots</strong> contrôlés dans le temps.</p>
<p>L’envoi de vagues offre les avantages suivants :</p>
<ul>
<li>Meilleure <strong>délivrabilité</strong> - Répartissez les envois au fil du temps pour aider à maintenir une forte <strong>réputation de l'expéditeur</strong> et réduire le risque d'être marqué comme spam.</li>
<li><strong>Contrôle de charge</strong> - Évitez de surcharger les systèmes en aval (par exemple les centres d’appels, les pages de destination) en limitant le nombre de messages diffusés en même temps.</li>
<li>Cas d’utilisation importants et sensibles au facteur temps : adaptés aux audiences importantes ou lorsque vous devez contrôler le timing (par exemple, capacité du centre d’appel, montée en réputation ou offres limitées dans le temps).</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>arbitrage de parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser des <strong>formules</strong> et <strong>modèles d’IA</strong> pour améliorer automatiquement les <strong>scores de priorité de parcours </strong> en fonction des attributs du profil client et des facteurs contextuels, afin que les clients puissent accéder aux parcours les plus pertinents.</p>
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (<strong>Disponibilité limitée</strong>). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent : création de contenu de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Optimisé par <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> est disponible dans Journey Optimizer et vous permet d’analyser les parcours via une <strong>interface en langage naturel</strong>. Vous pouvez désormais également générer et gérer du contenu spécifique à un canal directement dans Journey Agent, ce qui permet de créer du contenu pour des canaux tels que les e-mails et les notifications push, d’appliquer et de prévisualiser des modèles, d’affiner le ton et le style par le biais d’invites et d’ouvrir le contenu dans <strong>Content Designer</strong> pour une modification contextuelle.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activités mobiles en direct</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les <strong>Activités en direct</strong> fournissent des <strong>mises à jour en temps réel</strong> et des expériences interactives dans les applications mobiles, ce qui permet aux utilisateurs de rester informés des événements ou tâches en cours directement sur l’écran de leur appareil. Cette fonctionnalité améliore l’engagement en fournissant des informations en direct, telles que le suivi de la progression, les mises à jour d’événement ou le contenu interactif, sans que les utilisateurs et utilisatrices ouvrent l’application.</p>
<p>Publiée précédemment en version bêta, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activité d’action dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer prend en charge une nouvelle <strong>activité d’action</strong> générique qui vous permet de configurer des actions uniques et des <strong>groupes d’actions entrants à actions multiples</strong>, ce qui permet une configuration d’action rationalisée dans la zone de travail de parcours <strong></strong>. Cette nouvelle fonctionnalité permet notamment les opérations suivantes :</p>
<ul>
<li>Configuration d’action native simplifiée dans la zone de travail de parcours</li>
<li>Création de groupes d’actions entrantes multi-actions</li>
<li>La possibilité d’ajouter <strong>optimisation</strong> à toute action de canal intégrée.</li>
<li>Possibilité d’ajouter des options <strong>expérimentation</strong> et <strong>multilingues</strong> à n’importe quelle action.</li>
</ul>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de notifications push web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer prend désormais en charge les <strong>notifications push web</strong>, en étendant le canal push au-delà des applications mobiles. Vous pouvez facilement diffuser des notifications vers les navigateurs mobiles et de bureau, ce qui vous permet d’atteindre les clientes et clients directement sur leurs appareils sans avoir besoin d’une application. Cette amélioration vous permet d’interagir avec les utilisateurs et utilisatrices à l’aide de messages personnalisés et opportuns en temps réel, en exploitant les mêmes <strong>workflows de création</strong> et <strong>fonctionnalités de ciblage</strong> déjà disponibles pour les notifications push mobiles.</p>
<p>Publiée précédemment en version bêta, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p>Date de disponibilité : samedi 13 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activité de décision de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle <strong>activité de décision de contenu</strong> est désormais disponible dans la zone de travail de parcours <strong></strong> pour intégrer des <strong>offres personnalisées</strong> directement dans vos parcours clients. Cette activité vous permet de diffuser du contenu basé sur des décisions et de référencer ces offres dans l’ensemble de votre parcours, dans des conditions de création d’embranchements basés sur l’éligibilité, dans des actions personnalisées pour transmettre des données d’offre à des systèmes externes et dans d’autres activités pour créer des expériences client entièrement personnalisées.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/content-decision.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : jeudi 11 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API d’outils de migration en libre-service</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Les API d’outil de migration</strong> sont désormais disponibles pour migrer par programmation les entités <strong>Gestion des décisions</strong> vers <strong>Prise de décision</strong>, avec les fonctionnalités suivantes :</p>
<ul>
<li>Portées de migration flexibles (<strong>sandbox</strong>, <strong>offre</strong> ou <strong>décision</strong> niveau)</li>
<li>Automatisé <strong>analyse des dépendances</strong> et validation</li>
<li><strong> Prise en charge des restaurations </strong> pour les migrations terminées</li>
<li>Des rapports de migration détaillés avec les mappages d’objet</li>
</ul>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/decisioning-migration-api.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 3 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Surveillance des actions personnalisées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Renseignez davantage insight sur l’intégrité et les performances de vos <strong> points d’entrée d’action personnalisés </strong> avec un nouveau <strong> tableau de bord de surveillance </strong> et des données d’événement d’étape de <strong>parcours enrichies</strong>. Effectuez le suivi des appels réussis, des erreurs, du débit, des temps de réponse et des temps d’attente de la file d’attente pour comprendre rapidement quand, où et pourquoi des anomalies se produisent.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../action/reporting.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 3 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prise en charge de la prise de décision dans le canal SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais personnaliser et optimiser le contenu de vos <strong>SMS</strong> avec <strong>Decisioning</strong>. Utilisez <strong>Scores de priorité</strong>, <strong>Formules</strong> ou <strong>Modèles d’IA</strong> pour afficher le meilleur contenu à l’intention de vos clients.</p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/create-decision.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 2 février 2026</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#feb-26-01-improv}

Les améliorations de cette version sont présentées ci-dessous.

#### Configuration

* **Utilisation des événements d’expérience dans les expressions de parcours** - À compter du 1er avril 2026, l’utilisation des attributs d’événement d’expérience dans les expressions de parcours ne sera plus prise en charge pour les organisations qui n’ont pas utilisé cette fonctionnalité au cours des 90 derniers jours. Cette fonctionnalité n’est déjà plus disponible pour les nouvelles organisations clientes depuis le 8 juillet 2025. Pour obtenir des alternatives, consultez [Recherche d’événement d’expérience dans les parcours ](../building-journeys/exp-event-lookup.md).


* **Changement de méthode de délégation de sous-domaine** - Vous pouvez désormais passer d’une méthode <strong>délégation de sous-domaine</strong> à une autre. Vous pouvez ainsi migrer des domaines à l’aide du mode de délégation <strong>CNAME</strong> vers la méthode <strong>délégation personnalisée</strong> afin de respecter les politiques de sécurité de votre entreprise.

  **Remarque** : cette fonctionnalité n’est disponible que pour un ensemble d’organisations (<strong>Disponibilité limitée</strong>). Pour en bénéficier, contactez votre représentant ou représentante Adobe.


#### Concepteur d’e-mail

* **Utiliser un thème de marque pour convertir une image en modèle d’e-mail** - Lors de la conversion d’une image en modèle d’e-mail dans Journey Optimizer, vous pouvez désormais utiliser un <strong>thème</strong> comme entrée afin que l’HTML générée suive vos <strong>paramètres de marque</strong>. Les styles tels que la couleur d’arrière-plan, la couleur du bouton, les polices, l’espacement des lignes, les marges et la marge intérieure sont appliqués automatiquement, ce qui réduit le travail de conception manuel et fournit un modèle prêt à l’emploi avec un minimum de modifications.


* **Mettre à jour les marques avec un nouvel onglet de couleur** - <strong>Directives relatives à la marque</strong> vous aident à vous assurer que votre marque est présentée de manière cohérente à tous les points de contact. La nouvelle <strong>section Couleurs</strong> définit les normes du système de couleurs de votre marque et décrit comment les couleurs sont sélectionnées, organisées et appliquées à travers les expériences. Elle garantit une utilisation cohérente des couleurs primaires, secondaires, d’accentuation et neutres pour soutenir une identité de marque cohérente, accessible et reconnaissable.


#### IA

* **Intégration de modèles Firefly personnalisés et de modèles de génération d’images tiers** - Activez l’intégration transparente des modèles <strong>Firefly standard et personnalisés</strong>, ainsi que des modèles d’image tiers <strong> approuvés</strong> (par exemple, NanoBanana), pour offrir une plus grande flexibilité, un meilleur contrôle et un meilleur alignement de la marque lors de la génération d’images. Vous pouvez ainsi sélectionner le meilleur modèle pour chaque cas d’utilisation : Firefly standard pour les besoins généraux, Firefly personnalisé pour la génération sur marque ou modèles tiers approuvés pour des scénarios spécialisés ou expérimentaux.


#### Décisions pour les expériences

* **Prise en charge de l’entrée Edge pour l’utilisation des données Adobe Experience Platform dans la prise de décision** - La prise en charge de la prise de décision de <strong>la recherche de données Experience Platform</strong> inclut désormais des cas d’utilisation de canal <strong>entrant Edge</strong>. La fonctionnalité reste à disponibilité limitée. La disponibilité générale de la fonctionnalité de recherche de données sous-jacente n’est pas encore annoncée (AEP/dépendance du produit).

  **Remarque** : cette fonctionnalité n’est disponible que pour un ensemble d’organisations (<strong>Disponibilité limitée</strong>). Pour en bénéficier, contactez votre représentant ou représentante Adobe.


* **Aperçu d’Experience Decisioning dans le canal d’expérience basé sur le code** - Vous pouvez désormais prévisualiser <strong>éléments de décision</strong> lors de la configuration d’<strong>Experience Decisioning</strong> avec le canal <strong>Expérience basée sur le code</strong>. L’aperçu est disponible directement dans l’interface de création avant la mise en ligne.


* **Observabilité du modèle d’IA pour le classement des offres** - Journey Optimizer vous permet désormais de surveiller l’<strong>intégrité</strong>, le <strong>statut de formation</strong> et les <strong>performances</strong> de vos modèles d’<strong>IA</strong> dans Decisioning, afin que vous puissiez vérifier le succès de la formation, résoudre les problèmes et comprendre l’impact sur vos résultats. Cette fonctionnalité est disponible uniquement pour les modèles d’optimisation personnalisés (et non pour l’optimisation automatique).


* **Joindre des fragments aux éléments de décision** - Journey Optimizer permet désormais de joindre des <strong>fragments</strong> aux <strong>éléments de décision</strong> qui peuvent être utilisés dans les campagnes d’expérience basées sur le code par le biais de <strong>politiques de décision</strong>.

  **Remarque** : cette fonctionnalité, précédemment disponible en disponibilité limitée, est désormais disponible dans tous les environnements (disponibilité générale).

  Date de disponibilité : 12 février 2026.


#### Parcours

* **Plusieurs actions entrantes dans les parcours** - Pour simplifier votre orchestration des parcours, vous pouvez désormais définir plusieurs <strong>actions entrantes</strong> dans un seul parcours. Précédemment disponible dans les campagnes, cette fonctionnalité vous permet de diffuser simultanément plusieurs <strong>expériences basées sur du code</strong> <strong>messages in-app</strong>, <strong>cartes de contenu</strong> ou <strong>actions web</strong> à différents emplacements, chaque action contenant du contenu spécifique.

  **Remarque** : cette fonctionnalité, précédemment disponible en disponibilité limitée, est désormais disponible dans tous les environnements (disponibilité générale).


* **Webhooks SMS** : les <strong>webhooks</strong> sont désormais pris en charge par tous les fournisseurs de SMS. Vous pouvez configurer chaque webhook en fonction de son objectif : <strong>Webhooks entrants</strong> pour capturer les messages entrants et <strong>Webhooks de commentaires</strong> pour recevoir les accusés de réception des diffusions, les mises à jour de statut et d’autres événements liés aux messages. [En savoir plus](../sms/sms-webhook.md)

  Date de disponibilité : 2 février 2026.