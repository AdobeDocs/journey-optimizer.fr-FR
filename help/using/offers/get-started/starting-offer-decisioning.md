---
title: Prise en main de la gestion des décisions
description: Découvrez comment Adobe Journey Optimizer peut vous aider à envoyer à vos clients la bonne offre au bon moment
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# À propos de la gestion des décisions {#about-decision-management}

Utilisation [!DNL Journey Optimizer] pour offrir la meilleure offre et la meilleure expérience à vos clients sur tous les points de contact au bon moment. Une fois conçu, ciblez vos audiences avec des offres personnalisées.

La gestion des décisions facilite la personnalisation grâce à une bibliothèque centrale d’offres marketing et à un moteur de décision qui applique des règles et des contraintes aux profils riches en temps réel créés par Adobe Experience Platform pour vous aider à envoyer à vos clients la bonne offre au bon moment.

La fonctionnalité de gestion des décisions se compose de deux composants principaux :

* Le **Bibliothèque d’offres centralisée** qui est l’interface dans laquelle vous créez et gérez les différents éléments qui composent vos offres, et définissez leurs règles et contraintes.
* Le **Moteur de décision d’offre** qui tire parti des données Adobe Experience Platform et des profils clients en temps réel, ainsi que de la bibliothèque des offres, afin de sélectionner l’heure, les clients et les canaux auxquels les offres seront diffusées.

![](../assets/architecture.png)

Les avantages incluent :

* Amélioration des performances des campagnes grâce à la diffusion d’offres personnalisées sur plusieurs canaux,
* Workflows améliorés : au lieu de créer plusieurs diffusions ou campagnes, les équipes marketing peuvent améliorer les workflows en créant une seule diffusion et en modifiant les offres dans différentes parties du modèle,
* Contrôle du nombre d’affichages d’une offre dans les campagnes et les clients.

➡️ [En savoir plus sur la gestion des décisions dans ces vidéos](#video)


>[!NOTE]
>
>Si vous êtes un [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html)l’utilisateur {target=&quot;_blank&quot;} en exploitant la variable **Offer Decisioning** , toutes les fonctionnalités de gestion de décision décrites dans cette section s’appliquent également à vous.

## Offres et décisions {#about-offers-and-decisions}

Un **Offre** est constitué de contenu, de règles d’éligibilité et de contraintes qui définissent les conditions dans lesquelles il est présenté à vos clients.

Il est créé à l’aide de la fonction **Bibliothèque d’offres**, qui fournit un catalogue d’offres central où vous pouvez associer des règles d’éligibilité et des contraintes à plusieurs éléments de contenu pour créer et publier des offres (voir [Interface utilisateur de la bibliothèque des offres](../get-started/user-interface.md)).

![](../assets/offer_structure.png)

Une fois la bibliothèque des offres enrichie d’offres, vous pouvez intégrer vos offres dans **décisions**.

Les décisions sont des conteneurs pour vos offres qui exploitent le moteur de décision d’offre afin de choisir la meilleure offre à diffuser en fonction de la cible de la diffusion.

## Cas d’utilisation courants {#common-use-cases}

Les fonctionnalités de gestion des décisions et l’intégration à Adobe Experience Platform vous permettent de couvrir de nombreux cas d’utilisation pour vous aider à augmenter l’engagement et la conversion des clients.

* Affichez sur votre site web des offres de la page d’accueil qui correspondent au point ciblé du client visiteur, en fonction des données d’Adobe Experience Platform.

   ![](../assets/website.png)

* Si les clients se rendent près de l’un de vos magasins, envoyez-leur des notifications push leur rappelant les offres disponibles en fonction de leurs attributs (niveau de fidélité, genre, achats précédents, etc.).

   ![](../assets/push_sample.png)

* La gestion des décisions vous aide également à améliorer l’expérience de vos clients lorsque vous contactez votre équipe d’assistance. Les API de gestion de la décision vous permettent d’afficher, sur le portail des agents de votre centre d’appels, des informations sur les offres échangées par le client et les meilleures offres suivantes.

   ![](../../assets/do-not-localize/call-center.png)

## Accorder l’accès à la gestion des décisions {#granting-acess-to-decision-management}

Les autorisations d’accès et d’utilisation des fonctionnalités de prise de décision sont gérées à l’aide de la variable [Adobe Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

Pour accorder l’accès à la fonctionnalité de gestion des décisions, vous devez créer une **[!UICONTROL Product profile]** et attribuez les autorisations correspondantes à vos utilisateurs. En savoir plus sur la gestion [!DNL Journey Optimizer] utilisateurs et autorisations dans [cette section](../../administration/permissions.md).

Les autorisations spécifiques à la gestion de la décision sont répertoriées dans la section [cette section](../../administration/high-low-permissions.md#decisions-permissions).

## Glossaire {#glossary}

Vous trouverez ci-dessous la liste des principaux concepts que vous utiliserez lorsque vous utiliserez la gestion des décisions.

* **Limitation** ou **Limitation de la fréquence**: La limitation est utilisée comme contrainte pour définir le nombre de fois où une offre est présentée. Il existe deux types de limites : le nombre de fois où une offre peut être proposée dans l’audience cible combinée, également appelée &quot;Nombre total de limites&quot;, et le nombre de fois où une offre peut être proposée au même utilisateur final, également appelée &quot;limitation de profil&quot;.

* **Collections**: Les collections sont des sous-ensembles d’offres basés sur des conditions prédéfinies définies par un marketeur, telles que la catégorie de l’offre.

* **Décision**: Une décision contient la logique qui oriente la sélection d’une offre.

* **Règle de décision**: Les règles de décision sont des contraintes ajoutées à une offre personnalisée et appliquées à un profil pour déterminer son éligibilité.

* **Offre éligible**: Une offre éligible répond aux contraintes définies en amont qui peuvent être offertes de manière cohérente à un profil.

* **Gestion des décisions**: Permet de créer et de proposer des expériences d’offres personnalisées aux utilisateurs finaux sur différents canaux et applications à l’aide d’une logique commerciale et de règles de décision.

* **Offres de secours**: Une offre de secours est l’offre par défaut affichée lorsqu’un utilisateur final n’est éligible à aucune des offres personnalisées de la collection.

* **Offre**: Une offre est un message marketing auquel des règles peuvent être associées et qui spécifie qui est éligible pour voir l’offre.

* **Bibliothèque d’offres**: La bibliothèque d’offres est une bibliothèque centrale utilisée pour gérer les offres personnalisées et de secours, les règles de décision et les décisions.

* **Offres personnalisées**: Une offre personnalisée est un message marketing personnalisable basé sur des règles d’éligibilité et des contraintes.

* **Emplacements**: Un emplacement est l’emplacement et ou le contexte dans lequel une offre s’affiche pour un utilisateur final.

* **Priorité**: La priorité est utilisée pour classer les offres qui répondent à toutes les contraintes, telles que l’éligibilité, le calendrier et la limitation.

* **Représentations**: Une représentation est une information utilisée par un canal, comme l’emplacement ou la langue d’affichage d’une offre.

## Vidéos pratiques{#video}

>[!NOTE]
>
>Ces vidéos s’appliquent au service d’application Offer Decisioning basé sur Adobe Experience Platform et ne sont pas spécifiques à [!DNL Adobe Journey Optimizer]. Cependant, ils fournissent des conseils génériques pour utiliser la gestion de la décision dans le contexte de [!DNL Journey Optimizer].

### Qu’est-ce que la gestion des décisions ? {#what-is-offer-decisioning}

La vidéo ci-dessous présente les principales fonctionnalités, l’architecture et les cas pratiques de la gestion des décisions :

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### Définition et gestion des offres {#use-offer-decisioning}

La vidéo ci-dessous montre comment utiliser la gestion de la décision pour définir et gérer vos offres et exploiter les données client en temps réel.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)


