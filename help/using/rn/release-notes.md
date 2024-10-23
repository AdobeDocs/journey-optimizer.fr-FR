---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 5ffa0937bd9f23f29c8f02d2951cccac73d75f1b
workflow-type: tm+mt
source-wordcount: '1717'
ht-degree: 86%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour. [!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Mises à jour d’octobre 2024 {#24-10-rn}

**date de publication** à venir : 28-30 octobre 2024

Les [fonctionnalités](#24-10-features) et [améliorations](#24-10-improvements) répertoriées ci-dessous ont été publiées ce mois-ci.

### Nouvelles fonctionnalités {#24-10-features}

<table>
<thead>
<tr>
<th><strong>Validations dans les parcours et les opérations (Disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce aux politiques d’approbation, vous pouvez désormais configurer un processus d’approbation dans Journey Optimizer qui permet aux équipes marketing de s’assurer que les campagnes et les parcours sont examinés et approuvés par les parties prenantes appropriées avant qu’ils ne soient mis en ligne.</p>
<p>Pour plus d’informations, consultez la <a href="../test-approve/gs-approval.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
<p>Date de disponibilité : 21 octobre 2024</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mise à jour de l’expérience de création de rapports (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les rapports Journey Optimizer sont désormais disponibles dans l’ensemble (GA). Ils s’accompagnent d’une interopérabilité améliorée avec les fonctionnalités des Customer Journey Analytics, de la normalisation des rapports sur les deux plateformes et de l’amélioration de la cohérence et de la fiabilité des données. L’intégration transparente entre Journey Optimizer et Customer Journey Analytics fournit une meilleure visibilité des mesures de performance, ce qui aide les utilisateurs et les utilisatrices à prendre des décisions plus éclairées.</p>
<p>Avec la disponibilité générale, quatre nouvelles fonctionnalités sont introduites : la possibilité de créer des mesures simples, de créer et de publier des audiences, de poser des questions ad hoc à l’aide d’Insight Builder et de planifier des rapports qui seront automatiquement envoyés par courriel aux destinataires clés.</p>
<p>Pour plus d’informations, consultez la <a href="../reports/report-cja-manage.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Date de disponibilité : 16 octobre 2024</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Expériences basées sur le code dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce au nouveau canal d’expérience basée sur le code, Adobe Journey Optimizer vous permet d’effectuer des tests et des personnalisations avancés pour l’une de vos propriétés entrantes, ce qui vous permet de diffuser facilement des expériences personnalisées sur différents points de contact (touchpoints) tels que des applications web, des applications mobiles, des applications de bureau, des consoles vidéo, des appareils connectés à la télévision, des téléviseurs intelligents, des kiosques, des distributeurs automatiques, des périphériques IoT, etc. Le canal d’expérience basée sur le code est désormais disponible dans la zone de travail du parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../code-based/create-code-based.md">documentation détaillée</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>Date de disponibilité : 1er octobre_2024</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Expériences web dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec le canal web, Adobe Journey Optimizer vous permet de personnaliser l’expérience web que vous diffusez à votre clientèle par le biais de parcours web entrants. Le canal web est désormais disponible dans la zone de travail du parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../web/create-web.md">documentation détaillée</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>Date de disponibilité : 1er octobre_2024</p>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>L’expérience actuelle en matière de rapports sera abandonnée à compter de janvier 2025. À partir de cette date, la nouvelle expérience de création de rapports deviendra la norme. Nous vous recommandons de vous familiariser avec les nouvelles fonctionnalités pour garantir une transition fluide.
>
> [Découvrir la nouvelle interface de création de rapports de Journey Optimizer](../reports/report-gs-cja.md)

### Améliorations {#24-10-improvements}

**Parcours** : date de disponibilité : 3 octobre 2024

* **Paramètres dans les actions personnalisées** : les paramètres NULL et facultatifs sont désormais pris en charge dans les actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md#define-the-message-parameters)

**Gouvernance des données et politiques de consentement** : date de disponibilité : 7 octobre 2024

* L’application des **politiques de gouvernance des données** a désormais lieu sur tous les canaux dans Journey Optimizer. Pour les clientes et clients qui ont créé des politiques dans Adobe Experience Platform, ces dernières sont appliquées aux actions marketing dans le cadre des configurations des canaux. Lorsque vous créez du contenu à l’aide d’une configuration, le système vérifie tous les champs de personnalisation à la recherche de toute violation de gouvernance des données. Si une violation est trouvée, la publication d’un parcours ou d’une campagne n’est pas possible. [En savoir plus](../action/action-privacy.md)

* Les **politiques de consentement personnalisé** s’appliquent désormais à tous les canaux Journey Optimizer. Lors de l’application, avant l’envoi d’un message ou avant la diffusion d’une expérience entrante, le système vérifie que la personne a donné son consentement pour utiliser des champs de personnalisation dans le contenu qu’elle reçoit. Si aucun consentement n’est donné, l’expérience ne s’affiche pas. [En savoir plus](../action/consent.md)

  >[!NOTE]
  >
  >Les politiques de consentement ne sont actuellement disponibles que pour les organisations qui ont acheté les offres complémentaires Adobe **Healthcare Shield** et **Privacy and Security Shield**.

**Audiences** : date de disponibilité : 8 octobre 2024

* Lors du ciblage d’une audience de fichier CSV, vous pouvez désormais utiliser les attributs du fichier dans l’éditeur de personnalisation et dans le créateur de règles de parcours et de campagnes. [En savoir plus](../audience/about-audiences.md)

* L’utilisation des audiences et des attributs du chargement personnalisé (fichiers CSV) est désormais disponible avec Healthcare Shield ou Privacy and Security Shield.

**Prise de décision** - Date de disponibilité : 8 octobre 2024

Lors de l’ajout d’une stratégie de décision à une campagne basée sur du code avec la prise de décision (précédemment appelée prise de décision d’expérience), vous pouvez désormais sélectionner manuellement des éléments de décision uniques, en plus des stratégies de sélection. En outre, vous pouvez désormais sélectionner plusieurs offres de secours. Cela garantit qu’un certain nombre d’éléments de décision sont renvoyés. [En savoir plus](../experience-decisioning/create-decision.md)

## Version de septembre 2024 {#24-9-rn}

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

**Date de publication** : 24-26 septembre 2024

### Nouvelles fonctionnalités {#24-9-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Cartes de contenu pour les applications mobiles et les sites web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les cartes de contenu sont une nouvelle fonctionnalité de messagerie numérique d’Adobe Journey Optimizer qui fournit du contenu personnalisé et attrayant, directement dans les applications mobiles et les sites web. Contrairement aux notifications push traditionnelles, les cartes de contenu s’intègrent de manière transparente à l’interface d’utilisation, en offrant des mises à jour persistantes et non intrusives qui améliorent l’interaction et l’expérience des utilisateurs et utilisatrices.</p>
<p>Grâce à cette fonctionnalité, les spécialistes du marketing peuvent présenter du contenu multimédia pertinent aux utilisateurs et utilisatrices, augmenter l’engagement des personnes et veiller à ce que les messages importants soient affichés sans interrompre le parcours d’utilisation.</p>
<p>Pour plus d’informations, consultez la <a href="../content-card/get-started-content-card.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/content-card.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Approbations dans les parcours et les campagnes (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce aux politiques d’approbation, vous pouvez désormais configurer un processus d’approbation dans Journey Optimizer qui permet aux équipes marketing de s’assurer que les campagnes et les parcours sont examinés et approuvés par les parties prenantes appropriées avant qu’ils ne soient mis en ligne.</p>
<p>Les politiques d’approbation ne sont actuellement disponibles que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../test-approve/gs-approval.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Email Content Locking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now allows you to lock content in email templates, either by locking the entire template or specific structures and component. This allows you to prevent unintentional edits or deletions, giving you greater control over template customization, and improving the efficiency and reliability of your email campaigns.</p>
<p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Critères de sortie globale dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous définissez maintenant des critères de sortie au niveau du parcours. En ajoutant des critères de sortie, vous faites quitter le parcours aux profils dès qu’un événement se produit (un achat, par exemple) ou qu’ils répondent aux critères d’une audience. Cela évite à l’utilisateur ou à l’utilisatrice de recevoir d’autres communications du parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-properties.md#exit-criteria">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Accélérateur de contenu de l’assistant IA </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une fois que vous avez créé et personnalisé votre message, placez votre contenu au niveau supérieur avec l’accélérateur de contenu de l’assistant d’IA dans Journey Optimizer. Vous pouvez désormais utiliser l’assistant d’IA pour optimiser l’impact de votre message en testant différents titres et images principaux. Chaque variante est gérée en tant que traitement unique, afin de la mesurer et de la comparer pour savoir quel titre génère le plus de clics.</p>
<p>Découvrez une expérience pratique avec <a href="https://experienceleague.adobe.com/fr/apps/journey-optimizer/ai-assistant-content-accelerator">notre aperçu des fonctionnalités en direct</a>, conçu pour vous permettre d’explorer directement ses fonctionnalités et de les comprendre pleinement.</a>.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/gs-generative.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/>
<p>Date de disponibilité : 12 septembre 2024</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configuration de canal guidée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La configuration de canal guidée vous permet d’automatiser et de valider la configuration de canal dans une expérience unifiée, ce qui accélère le processus de prise en main de Journey Optimizer. Cette nouvelle configuration guidée simplifie la configuration rapide des canaux, en s’assurant que toutes les ressources nécessaires sont facilement installées et qu’elles fonctionnent dans Experience Platform, Journey Optimizer et la Collecte de données. Cela permet aux équipes d’ingénierie marketing, produit et données de lancer rapidement la création de campagnes et de parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/set-mobile-config.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/guided-setup.gif"/>
<p>Date de disponibilité : 3 septembre 2024</p>
</br>
</td>
</tr>
</tbody>
</table>


### Améliorations {#24-9-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Audiences** : date de disponibilité : 17 septembre 2024

**Utilisation de la licence** : le tableau de bord Utilisation de la licence affiche désormais les profils engageables au lieu des audiences engageables. [En savoir plus](../audience/license-usage.md)

**Gestion de contenu**

Vous pouvez désormais exporter des modèles de contenu et des fragments entre les sandbox. [En savoir plus](../configuration/copy-objects-to-sandbox.md)

**Parcours**

* **Améliorations des rapports dynamiques** : les rapports dynamiques fournissent des informations sur les performances de vos parcours au cours des dernières 24 heures. Nous les avons améliorés en ajoutant de nouvelles mesures (profils entrés, sortis, ignorés et profils en erreur), ce qui vous permet de mieux comprendre le comportement et les performances des utilisateurs et utilisatrices directement à partir de la zone de travail du parcours. [En savoir plus](../building-journeys/report-journey.md)


* (Date de disponibilité : 10 septembre) **Reprises automatiques sur la Lecture d’audience** : les reprises sont désormais appliquées par défaut sur les parcours déclenchés par l’audience (commençant par une **Lecture d’audience** ou un **Événement métier**) lors de la récupération du traitement d’export. Si une erreur se produit lors de la création du traitement d’export, des reprises sont effectuées toutes les 10 minutes, pendant 1 heure au maximum. Après cela, nous considérerons cela comme un échec. Ces types de parcours peuvent donc être exécutés jusqu’à 1 heure après l’heure planifiée. [En savoir plus](../building-journeys/read-audience.md#retries)

**Canal e-mail**

* **En-tête du message dans l’e-mail envoyé et copie en Cci** : un nouvel en-tête a été ajouté à tous les e-mails. La valeur de cet en-tête est propre à chaque e-mail envoyé et à sa copie d’e-mail en Cci correspondante. Cet en-tête est également stocké dans les jeux de données de retour des messages et des commentaires en Cci, ce qui permet de réconcilier la copie en Cci et les informations d’e-mail envoyées correspondantes. [En savoir plus](../configuration/archiving-support.md#bcc-header)

* **Notation de spam** (disponibilité générale) : vous pouvez désormais vérifier la notation de spam de votre contenu dans un **rapport de spam** dédié. Grâce à SpamAssassin, Adobe Journey Optimizer peut désormais tester le contenu de vos e-mails et lui attribuer un score pour indiquer si les FAI ou les fournisseurs de messagerie le considèrent comme un spam ou non. [En savoir plus](../content-management/spam-report.md)

**Canal SMS**

* **Modifier les informations d’identification de l’API** : vous pouvez désormais modifier les paramètres dans les informations d’identification de l’API SMS, y compris les mises à jour des mots-clés et réponses d’inclusion/exclusion.

**API**

* **API de simulation de campagne** : utilisez cette API pour déclencher le traitement de BAT d’une campagne. L’envoi du BAT de campagne est un processus asynchrone. L’API renvoie un BATJobId qui peut être utilisé pour vérifier le statut du BAT. [En savoir plus](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}

* (Date de disponibilité : 10 septembre) La [documentation de l’API Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} est désormais interactive. Explorez les points d’entrée de l’API directement à partir des pages de la documentation pour obtenir des commentaires immédiats et accélérer votre implémentation technique.


  Toutes les pages de référence de l’API possèdent désormais une fonctionnalité **Essayer**. Cette fonctionnalité vous permet de tester les appels API directement sur la page du site web de la documentation. [Obtenez les informations d’authentification requises](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} et commencez à utiliser la fonctionnalité pour explorer les points d’entrée de l’API.

  Utilisez cette nouvelle fonctionnalité pour explorer les requêtes envoyées et les réponses issues des points d’entrée de l’API, afin d’obtenir des commentaires immédiats et d’accélérer votre implémentation technique.

  >[!CAUTION]
  >
  >Notez qu’en utilisant la fonctionnalité d’API interactive sur les pages de documentation, vous effectuez de vrais appels API vers les points d’entrée. Gardez cela à l’esprit lorsque vous effectuez des tests dans des sandbox de production.

**Configuration**

* **Plans de préchauffage des adresses IP** : cette fonctionnalité est désormais disponible pour l’ensemble de la clientèle, y compris les organisations qui ont acheté les offres complémentaires Adobe **Healthcare Shield** ou **Privacy and Security Shield**. [En savoir plus](../configuration/ip-warmup-gs.md)


![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.