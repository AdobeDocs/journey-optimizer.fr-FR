---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour 2024
description: Notes de mise à jour 2024 pour Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: bae533c5-1bfc-48bf-9f8d-1145383c040c
source-git-commit: d0fa6d9f3a5d61310e8d072513b199e513a66138
workflow-type: tm+mt
source-wordcount: '1582'
ht-degree: 100%

---

# Notes de mise à jour 2024 {#release-notes-2024}

Cette page répertorie toutes les fonctionnalités et améliorations pour [!DNL Journey Optimizer] publiées en 2024.


## Notes de mise à jour d’avril 2024 {#apr-2024}

**Date de publication** : 2 mai 2024

### Nouvelles fonctionnalités {#apr-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>MMS (service de messagerie multimédia) - tous les fournisseurs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec le canal SMS, vous pouvez maintenant améliorer votre communication en envoyant des MMS, ce qui vous permet de partager des images, des GIF ou des vidéos avec vos clientes et clients. Initialement disponibles uniquement avec Sinch, les MMS sont désormais également pris en charge par Infobip et Twilio.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Amélioration du concepteur de parcours et des rapports dynamiques</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dans cette version, nous avons amélioré l’interface d’utilisation de la zone de travail de parcours afin d’offrir une expérience client plus intuitive et efficace. Les activités sont plus claires et présentent plus d’informations sur la zone de travail de parcours avec moins de clics.</p>
<img src="assets/new-canvas3.gif"/>
<p>Outre la conception améliorée de la zone de travail de parcours, vous pouvez désormais afficher les mesures de création de rapports pour les dernières 24 heures directement dans la zone de travail de parcours. </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong>Note</strong> : ces modifications seront progressivement déployées dans tous les environnements à compter de la version d’avril.</p>
<p>Pour plus d’informations, consultez la <a href="new-canvas.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Améliorations {#apr-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Configuration**

* Vous pouvez désormais sélectionner une action marketing au niveau de la surface de canal. Lorsqu’elles sont utilisées dans une surface, toutes les politiques de consentement associées à cette action marketing sont utilisées afin de respecter les préférences de vos clientes et clients. [En savoir plus](../action/consent.md#surface-marketing-actions)
* L’utilisation du contrôle d’accès au niveau de l’objet est désormais disponible pour les surfaces de canal. [En savoir plus](../configuration/channel-surfaces.md#create-channel-surface)
* Lors de l’activation du désabonnement de la liste dans une surface de canal, vous pouvez maintenant définir le niveau de consentement pour vous aligner sur la manière dont vous gérez le consentement de toutes les autres sources. [En savoir plus](../email/email-settings.md#list-unsubscribe)

**Gestion de contenu**

* Vous pouvez désormais simuler des modèles de contenu pour tous les canaux. [En savoir plus](../content-management/content-templates.md#test-templates).

**Personnalisation**

* La nouvelle fonction d’assistant **toInt** est disponible dans l’éditeur d’expression. Elle vous permet de convertir n’importe lequel de ces types (nombre, double, entier, long, flottant, court, octet, booléen, chaîne) en entier. [En savoir plus](../personalization/functions/math.md#to-int)



## Notes de mise à jour de mars 2024 {#mar-2024}

**Date de publication** : 19-20 mars 2024

### Nouvelle fonctionnalité {#mar-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Expériences basées sur le code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce au nouveau canal d’expérience basé sur le code, Adobe Journey Optimizer vous permet d’effectuer des tests et des personnalisations avancés pour l’une de vos propriétés entrantes, ce qui vous permet de diffuser facilement des expériences personnalisées sur différents points de contact (touchpoints) tels que des applications web, des applications mobiles, des applications de bureau, des consoles vidéo, des appareils connectés à la télévision, des téléviseurs intelligents, des kiosques, des distributeurs automatiques, des périphériques IoT, etc.</p>
<P>Les fonctionnalités principales sont les suivantes :</p>
<ul><li> Personnalisation universelle : étendez les expériences personnalisées sur tous les points de contact, en assurant un parcours utilisateur cohérent et personnalisé.</li>
<li>Précision granulaire de la modification : modifiez du contenu spécifique à des emplacements spécifiques dans vos applications ou pages web.</li>
<li>Mise en œuvre polyvalente : prise en charge des méthodes de mise en œuvre côté serveur, basées sur les API ou basées sur le SDK pour une intégration transparente à votre environnement de développement.</li></ul></p>
<p>Pour plus d’informations, consultez la <a href="../code-based/get-started-code-based.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/code-based.gif"> 
</tr>
</tbody>
</table>

### Améliorations {#mar-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Modèles de contenu**

* **Miniatures** : un mode de **vue Grille** est désormais disponible pour les modèles de contenu, affichant ainsi les miniatures afin d’améliorer l’accès visuel. Actuellement, seuls les modèles HTML d’e-mail sont pris en charge. [En savoir plus](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Cette fonctionnalité est publiée en disponibilité limitée pour un petit groupe de personnes.

**Parcours**

De nouveaux statuts intermédiaires ont été ajoutés au cycle de vie de création de parcours :

* Statut **Publication** entre le statut **Brouillon** et le statut **Actif**
* Statut **Arrêt en cours** entre le statut **Actif** et le statut **Arrêté**
* Statuts **Activer le mode test** ou **Désactiver le mode test** entre le statut **Brouillon** et le statut **Brouillon (test)**

Lorsqu’un parcours se trouve dans un état intermédiaire, il est en lecture seule. [En savoir plus](../building-journeys/journey-gs.md#filter)

## Notes de mise à jour de février 2024 {#feb-2024}

**Date de publication** : 21-22 février 2024

### Nouvelles fonctionnalités{#feb-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.


<table>
<thead>
<tr>
<th><strong>Messagerie in-app web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser la nouvelle fonctionnalité de messagerie in-app web pour afficher du contenu personnalisé directement sur les sites web, par le biais de messages de superposition modale. Cette fonctionnalité vous permet d’interagir efficacement avec les visiteurs et visiteuses web, ce qui améliore l’interaction, la rétention et les taux de conversion des utilisateurs et utilisatrices.<br/><br/></p>
<p>Pour plus d’informations, consultez la <a href="../in-app/create-in-app-web.md">documentation détaillée</a>.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modèles de contenu multicanaux</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En plus de la fonctionnalité E-mail, des modèles de contenu sont désormais disponibles pour les canaux suivants : Push, In-app, SMS et Courrier, chaque canal ayant des types de modèles dédiés. Pour E-mail, vous pouvez maintenant sélectionner le type de contenu, ce qui vous permet d’enregistrer l’objet dans le cadre de votre modèle d’e-mail. <br/><br/></p>
<p>Pour plus d’informations, consultez la <a href="../content-management/content-templates.md">documentation détaillée</a>.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif"> 
</tr>
</tbody>
</table>


### Améliorations {#feb-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Audiences**

* **Listes de contrôle** : les variantes sont désormais prises en charge lors de l’utilisation de **listes de contrôle**. Les adresses de contrôle reçoivent une copie de toutes les variantes du même message (telles que les différents traitements d’une expérience de contenu). [En savoir plus](../configuration/seed-lists.md)

Antérieurement disponibles en version bêta, les améliorations suivantes sont désormais disponibles pour tous les utilisateurs et utilisatrices :

* Vous pouvez désormais cibler les **audiences créées par le biais de la composition de l’audience** et utiliser les attributs d’enrichissement dans les parcours. [En savoir plus](../building-journeys/read-audience.md)

* Vous pouvez désormais cibler les **audiences chargées à partir d’un fichier CSV** dans les parcours et les campagnes. [En savoir plus](../audience/about-audiences.md#segments-in-journey-optimizer)

  >[!AVAILABILITY]
  >
  >* L’utilisation d’audiences et d’attributs provenant de la composition de l’audience et du chargement personnalisé (fichier CSV) n’est actuellement pas disponible avec Healthcare Shield ou Privacy and Security Shield.
  >* L’amélioration du **chargement de l’audience à partir d’un fichier CSV** sera progressivement déployée dans les jours qui suivront la version initiale. Certains utilisateurs et utilisatrices ont un accès immédiat, mais d’autres peuvent rencontrer un retard avant que cela ne soit disponible dans leur environnement.

**Parcours**

* **Filtrer vos parcours** : vous pouvez désormais utiliser les **dates personnalisées pour filtrer l’inventaire des parcours**, en plus des filtres de dates prédéfinis existants. Vous pouvez ainsi affiner la liste en affichant les parcours créés ou publiés à une date spécifique, au cours d’un mois donné, sur une année entière ou dans des périodes spécifiées. [En savoir plus](../building-journeys/journey-gs.md#filter)
* **Actions personnalisées** : vous pouvez maintenant mettre à jour l’en-tête **content-type**. Ce nouveau **content-type** doit référencer le contenu JSON. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration)
* **Configuration** : l’attribut identityMap dans stepEvents est maintenant prérenseigné. L’identité principale est définie comme « primary = true ». [En savoir plus](../reports/sharing-field-list.md)
* **Interface utilisateur** : la barre supérieure, dans les écrans de parcours, a été réorganisée pour une expérience améliorée. Parmi les différentes mises à jour, l’icône « crayon » permettant d’accéder aux propriétés du parcours s’affiche désormais à gauche de la barre supérieure, en regard du nom du parcours. [En savoir plus](../building-journeys/journey-gs.md#change-properties)

**Canal SMS**

* **Mots-clés opt-in/opt-out** : lors de la configuration de votre canal SMS, vous pouvez désormais personnaliser les **mots-clés opt-in et opt-out** selon vos préférences. Journey Optimizer déclenche la réponse en fonction de ces mots-clés spécifiés. [En savoir plus](../sms/sms-configuration.md)

**Campagnes**

* **Campagnes déclenchées par l’API** : le code cURL généré après l’activation d’une campagne déclenchée par une API a été amélioré. Il inclut désormais toutes les variables de personnalisation (profil et contexte) utilisées dans le message. [En savoir plus](../campaigns/api-triggered-campaigns.md#execute)

**Règles de fréquence**

* En plus des canaux E-mail et Push, vous pouvez maintenant créer des règles de fréquence pour les canaux SMS et Courrier. Les règles de fréquence excluent automatiquement les profils sur-sollicités des messages et actions lorsque la limite de fréquence est atteinte. [En savoir plus](../configuration/frequency-rules.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## Notes de mise à jour de janvier 2024 {#jan-2024}

**Date de publication** : 30-31 janvier 2024

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
<p>Journey Optimizer prend désormais en charge la technologie d’authentification DMARC.</p>
<p>À compter du 1er février 2024, Google et Yahoo! exigent que vous disposiez d’un enregistrement DMARC pour tout domaine utilisé pour leur envoyer des e-mails. Vérifiez que l’enregistrement DMARC est configuré pour tous les sous-domaines que vous avez déjà délégués ou que vous déléguez actuellement à Adobe dans Journey Optimizer.</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/dmarc-record-update.md">documentation détaillée</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
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
<p>Tirez profit d’un catalogue de playbooks de cas d’utilisation spécifiques à des secteurs d’activité dans Real-Time CDP et Journey Optimizer pour traiter les cas d’utilisation courants que vous pouvez exécuter à l’aide d’Adobe Experience Platform et d’Adobe Journey Optimizer.</p><p>Une fois que vous avez choisi le playbook qui correspond le mieux à vos besoins, vous pouvez lui permettre de générer les ressources nécessaires à la prise en charge de votre cas d’utilisation, telles que des parcours, des messages, des schémas ou des segments, et de les personnaliser dans votre schéma pour réduire le délai de rentabilisation.</p>
<p>Pour plus d’informations, consultez la <a href="../start/playbooks.md">documentation détaillée</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Améliorations {#jan24-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Création de rapports**

* **Nouveaux widgets de répartition basés sur des domaines** – Ajout de nouveaux widgets pour améliorer vos rapports Campaign et Journey. Les widgets **Raisons de rebond par domaine**, **Envoyés et diffusés par domaine**, **Ouvertures et clics par domaine** et **Rebonds et erreurs par domaine** fournissent une répartition détaillée des mesures principales de diffusion et de suivi des e-mails au niveau du domaine. [En savoir plus](../reports/channel-report.md)

**Canal SMS**

* **Double opt-in** – Le workflow Double opt-in pour les SMS garantit que les utilisateurs et les utilisatrices s’engagent explicitement à recevoir des messages lorsque la demande est envoyée à partir de leur appareil. Les utilisateurs et utilisatrices démarrent le processus de consentement en envoyant un SMS entrant. Une fois qu’ils ont confirmé leur consentement, un message de réponse est envoyé, demandant une vérification finale. Si un profil d’utilisateur ou d’utilisatrice n’existe pas, il est créé lors de la confirmation. [En savoir plus](../sms/sms-configuration.md)

  Notez que cette fonctionnalité est disponible avec les fournisseurs SMS Sinch et Infobip.

**Parcours**

* **Durée des événements de réaction** – La durée maximale que vous pouvez définir dans les **Événements de réaction** est désormais de 29 jours au lieu de 30. [En savoir plus](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Lecture d’audience** – L’activité **Lecture d’audience** repose désormais sur le jeu de données d’instantané de profil pour les segments par lots, qui n’est généré qu’une fois par jour après l’exécution du traitement par lots quotidien planifié. Par conséquent, les données sont à jour depuis le dernier traitement par lots quotidien. [En savoir plus](../building-journeys/read-audience.md)

* **Groupes de champs** – Cette version corrige un problème qui empêchait l’enregistrement de groupes de champs dans certains cas.

* La prise en charge de `<listObject>` a été modifiée dans plusieurs fonctions.

**Règles de fréquence**

* **Limite de fréquence hebdomadaire** – Vous pouvez désormais spécifier le nombre maximum de messages envoyés à un profil client par semaine, en plus de l’option par mois. La limite de fréquence est basée sur la période calendaire sélectionnée et est réinitialisée au début de la période correspondante. [En savoir plus](../configuration/frequency-rules.md#create-new-rule)

  >[!NOTE]
  >
  >Une limite de fréquence quotidienne est également disponible à la demande. Contactez votre représentant ou représentante Adobe.

**Gestion des décisions**

* **Capping de la fréquence sur Edge** – Le compteur de capping de fréquence est maintenant mis à jour et disponible dans une décision de l’API Edge Decisioning en moins de 3 secondes. [En savoir plus](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
