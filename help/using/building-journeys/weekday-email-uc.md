---
solution: Journey Optimizer
product: journey optimizer
title: Envoyer des e-mails uniquement les jours de la semaine
description: Découvrez comment configurer un parcours pour envoyer des e-mails uniquement les jours de la semaine dans  [!DNL Adobe Journey Optimizer]
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: parcours, cas d’utilisation, jours de la semaine, condition, e-mail, planification
version: Journey Orchestration
exl-id: 2f313e59-ee50-473c-9346-8859889346ec
TQID: https://experienceleague.adobe.com/qUt7t5LTYSQW278Pafx2-1t-DboRz9tU5IRpVhuEqLc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1622
ht-degree: 59%

---

# Envoyer des e-mails uniquement les jours de la semaine {#send-emails-only-on-weekdays}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment configurer un parcours qui envoie des e-mails uniquement les jours de la semaine, en mettant en file d’attente les entrées de week-end pour la diffusion du lundi à l’aide d’une activité de condition et les activités d’attente avec des formules personnalisées.

>[!ENDSHADEBOX]

Ce cas pratique montre comment configurer un parcours dans [!DNL Adobe Journey Optimizer] qui envoie des e-mails uniquement les jours de la semaine (du lundi au vendredi). Pour les profils qui rejoignent le parcours le week-end (samedi ou dimanche), les e-mails sont automatiquement mis en file d’attente et envoyés le lundi à une heure spécifiée. Cela garantit un engagement optimal en diffusant des messages pendant la semaine de travail.

## Vue d’ensemble de cas d’utilisation

**Le défi** : veiller à ce que les e-mails ne soient envoyés que les jours de la semaine, même si les profils peuvent rejoindre le parcours le week-end. Pour les entrées pendant les week-ends, les e-mails doivent être placés en file d’attente et envoyés le lundi à une heure spécifique.

**La solution** : utiliser une activité de condition pour identifier le jour de la semaine. Pour les entrées pendant les week-ends, les activités d’attente avec des formules personnalisées retardent l’envoi de l’e-mail jusqu’au lundi. Les entrées pendant les jours de la semaine passent directement à l’étape d’envoi de l’e-mail.

Cette approche vous explique comment utiliser une activité de condition pour vérifier si le jour en cours est le samedi ou le dimanche, implémenter des activités d’attente avec des formules personnalisées pour les entrées pendant les week-ends, mettre en file d’attente les e-mails de week-end pour une diffusion le lundi à une heure spécifique et envoyer immédiatement les e-mails pour les entrées pendant les jours de la semaine (du lundi au vendredi).

Cette approche est idéale pour les campagnes par e-mail B2B (business-to-business), les newsletters et les communications professionnelles, les annonces liées à l’entreprise, les mises à jour de produits liés au travail et toute campagne marketing pour laquelle la diffusion pendant les week-ends n’est pas souhaitée.

>[!NOTE]
>
>Pour implémenter ce cas d’utilisation, vous avez besoin d’une instance Adobe Journey Optimizer active avec une [surface de canal e-mail](../configuration/channel-surfaces.md) configurée, une [audience](../audience/about-audiences.md) ou un [événement](../event/about-events.md) pour déclencher le parcours, ainsi qu’une compréhension de base des [conditions de parcours &#x200B;](conditions.md) et des [expressions](expression/expressionadvanced.md).

## Étapes dʼimplémentation

Suivez ces étapes pour créer un flux d’e-mail en semaine uniquement.

### Étape 1 : créer votre parcours

1. Accédez à **[!UICONTROL Gestion des Parcours]** > **[!UICONTROL Parcours]** dans [!DNL Adobe Journey Optimizer].

1. Cliquez sur **[!UICONTROL Créer un parcours]** pour [créer un parcours](journey-gs.md).

1. Configurez les [propriétés du parcours](journey-properties.md).

1. Choisissez le point d’entrée de votre parcours :
   * **[Lecture d’audience](read-audience.md)** : pour les campagnes par lots ciblant une audience spécifique
   * **[Événement](../event/about-events.md)** : pour les parcours déclenchés en temps réel en fonction du comportement client

### Étape 2 : ajoutez une activité de condition pour vérifier le jour de la semaine

Juste après le début du parcours, ajoutez une activité **[!UICONTROL Condition]** pour vérifier si le jour actuel est un samedi ou un dimanche. Le workflow sera ainsi divisé en conséquence.

1. Faites glisser et déposez une activité [**[!UICONTROL Optimiser &#x200B;]**](optimize.md) sur la zone de travail après votre point d’entrée.

1. Cliquez sur l’activité **[!UICONTROL Condition]** pour ouvrir son panneau de configuration.

1. Sélectionnez **[!UICONTROL Condition temporelle]** comme type de condition.

1. Sélectionnez **[!UICONTROL Jour de la semaine]** comme option de filtrage temporel.

1. Pour le **premier chemin (samedi)**, sélectionnez **samedi** uniquement. Libellez ce chemin « Samedi ».

1. Cliquez sur **[!UICONTROL Ajouter un chemin]** pour créer une deuxième condition.

1. Pour le **deuxième chemin (dimanche)**, sélectionnez **[!UICONTROL Jour de la semaine]** et choisissez **Dimanche** uniquement. Libellez ce chemin « Dimanche ».

   ![Configuration des conditions du samedi et du dimanche dans l’éditeur d’expression](assets/weekday-email-uc-condition-expression.png)


1. Cochez **[!UICONTROL Afficher le chemin pour d’autres cas que ceux ci-dessus]** pour créer un chemin pour les entrées pendant les jours de la semaine (lundi à vendredi).

>[!NOTE]
>
>Le fuseau horaire utilisé pour l’évaluation des jours de la semaine est défini au niveau du parcours dans les propriétés du parcours, et non au niveau de la condition. Le [fuseau horaire](timezone-management.md) du parcours utilisé dans la formule est le fuseau horaire configuré du parcours, et non celui des destinataires.

### Étape 3 : configurer les activités d&#39;attente pour les entrées du week-end

Pour les profils qui rejoignent le parcours le samedi ou le dimanche, utilisez les activités **[!UICONTROL Attente]** avec des formules personnalisées pour reporter l’envoi de l’e-mail au lundi, à l’heure souhaitée.

Dans l’activité **[!UICONTROL Attente]**, utilisez la formule suivante :

```javascript
toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))
```

Où :

* **X** correspond au nombre de jours d’attente :
   * Utiliser **2** pour le samedi (attendre jusqu’au lundi)
   * Utiliser **1** pour le dimanche (attendre jusqu’au lundi)
* **H** est l’heure d’envoi souhaitée (par exemple, **9** pour 9 h)


**Exemple pour le samedi :**

```javascript
toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))
```

**Exemple pour le dimanche :**

```javascript
toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))
```

Pour implémenter ceci dans votre parcours :

1. Sur le **chemin de samedi**, ajoutez une activité **[!UICONTROL Attente]** après la condition.

1. Sélectionnez **[!UICONTROL Durée]** comme type d’attente.

1. Cliquez sur **[!UICONTROL Mode avancé]** pour saisir la formule personnalisée.

1. Saisissez : `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))`

   ![Parcours avec trois chemins de condition : samedi, dimanche et jours de la semaine](assets/weekday-email-uc-paths.png)

1. Répétez les mêmes étapes pour le **chemin de dimanche**, en utilisant : `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))`

>[!TIP]
>
>Pour les heures d’ouverture plus complexes (p. ex., envoyer seulement entre 9 h et 17 h les jours de semaine), vous pouvez améliorer davantage la formule et les conditions.

### Étape 4 : branche de jour de semaine

Pour les profils rejoignant le parcours du lundi au vendredi, passez à l’étape d’envoi d’e-mail comme d’habitude.

1. Dans le **chemin de jour de la semaine** (chemin « autres cas »), passez directement à l’ajout d’une activité d’action **[!UICONTROL E-mail]**. Aucune activité **[!UICONTROL Attente]** n’est nécessaire pour les entrées pendant les jours de la semaine.

1. Configurez votre e-mail selon vos besoins.

### Étape 5 : terminer le flux de parcours

Après les activités **[!UICONTROL Attente]** sur les chemins de samedi et dimanche, les trois chemins (samedi, dimanche et jours de la semaine) doivent tous être dirigés vers la même activité d’action **[!UICONTROL E-mail]**. Ajoutez une activité **[!UICONTROL Fin]** après l’e-mail.

### Vue d’ensemble des workflows visuels

Le workflow de parcours complet suit cette logique :

* **Début** → **[!UICONTROL Condition]** : est-ce le samedi ou le dimanche ?
   * **Oui (samedi) :** **[!UICONTROL attendre]** jusqu’au lundi 9 h → **[!UICONTROL Envoyer un e-mail]**
   * **Oui (dimanche) :** **[!UICONTROL attendre]** jusqu’au lundi 9 h → **[!UICONTROL Envoyer un e-mail]**
   * **Non (du lundi au vendredi) :** **[!UICONTROL envoyer un e-mail]** immédiatement

Ainsi, tous les e-mails sont envoyés uniquement les jours de la semaine, les entrées pendant les week-ends étant automatiquement mises en file d’attente pour la diffusion le lundi.

### Étape 6 : tester votre parcours

Avant de publier, testez minutieusement votre logique de parcours en mode test de [!DNL Adobe Journey Optimizer] pour confirmer que tout fonctionne comme prévu :

1. Cliquez sur le bouton **[!UICONTROL Tester]** en haut à droite.

1. Activez le [mode test](testing-the-journey.md).

1. Créez des [profils de test](../audience/creating-test-profiles.md) avec des heures d’entrée simulées pour différents jours de la semaine :
   * **Entrée le samedi** : vérifiez que le profil suit le chemin du samedi, attend et reçoit un e-mail le lundi à l’heure spécifiée.
   * **Entrée le dimanche** : vérifiez que le profil suit le chemin du dimanche, attend et reçoit un e-mail le lundi à l’heure spécifiée.
   * **Entrées du lundi au vendredi** : vérifiez que les e-mails sont envoyés immédiatement sans attente.

1. Examinez la visualisation du parcours pour vous assurer que les profils suivent les chemins d’accès conditionnels appropriés (samedi, dimanche ou jour de la semaine).

1. Recherchez des [erreurs ou avertissements](troubleshooting.md) dans le parcours.

1. Vérifiez que les formules d’attente calculent la durée correcte pour l’heure de diffusion souhaitée le lundi.

>[!IMPORTANT]
>
>Testez toujours votre logique de parcours en mode test pour vous assurer que les activités d’attente se comportent comme prévu. Utilisez le mode de test pour simuler différents scénarios d’entrée et vérifier que les entrées pendant les week-ends sont correctement placées en file d’attente pour la diffusion le lundi. Pour plus d’informations, consultez les [bonnes pratiques de test de parcours](testing-the-journey.md).

### Étape 7 : publier votre parcours

Une fois les tests effectués :

1. Cliquez sur **[!UICONTROL Publier]** en haut à droite.

1. Confirmez la [publication](publish-journey.md).

1. Surveillez les performances du parcours à l’aide des [rapports de parcours](report-journey.md) et des [rapports dynamiques](../reports/journey-live-report.md).


## Rubriques connexes

* [Optimiser les activités](optimize.md) - Découvrez comment créer différents chemins d’accès dans votre parcours.
* [Utiliser des conditions dans un parcours](conditions.md) : guide détaillé sur les conditions de parcours
* [Activité d’attente](wait-activity.md) : configurer des durées d’attente et des formules
* [Fonctions de date](functions/date-functions.md) : référence complète pour les fonctions de date et d’heure
* [Éditeur d’expression](expression/expressionadvanced.md) : créer des expressions complexes
* [Bonnes pratiques relatives aux parcours &#x200B;](journey-gs.md#best-practices) : approches recommandées pour la conception de parcours

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page propose un cas pratique détaillé pour configurer un parcours qui envoie des e-mails uniquement les jours de la semaine en utilisant une condition de jour de la semaine et des formules d’attente personnalisées pour retarder les entrées du week-end jusqu’au lundi.

**Intentions:**

* Configurez une activité Condition pour brancher un parcours en fonction du jour de la semaine (samedi, dimanche ou jour de la semaine)
* Écrivez des expressions d’attente personnalisées à l’aide de `toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))` pour retarder les profils de week-end jusqu’au lundi
* Créez un parcours à trois chemins qui fusionne tous les chemins en une seule action e-mail
* Testez la logique d’e-mail en semaine uniquement à l’aide de profils de test avec différents jours d’entrée simulés
* Publier et surveiller un parcours qui supprime la diffusion d’e-mails le week-end

**Glossaire:**

* **Condition de temps** : type d’activité de condition dans Journey Optimizer qui embranche les chemins de parcours en fonction de critères de date/heure tels que le jour de la semaine *(spécifiques au produit)*
* **nowWithDelta** : fonction d’expression qui renvoie le décalage date/heure actuel d’un nombre spécifié de jours ou d’autres unités *(spécifiques au produit)*
* **setHours** : fonction d’expression qui définit une heure spécifique sur une valeur de date/heure donnée *(spécifique au produit)*
* **toDateTimeOnly** : fonction d’expression qui convertit une valeur au format de `dateTimeOnly` requis par les activités d’attente personnalisées *(spécifiques au produit)*

**Mécanismes de sécurisation :**

* Le fuseau horaire utilisé pour l’évaluation du jour de la semaine correspond au fuseau horaire configuré pour le parcours (défini dans les propriétés du parcours), et non à celui du destinataire individuel.
* Une surface de canal e-mail active et une audience ou un événement pour déclencher le parcours sont requis pour implémenter ce cas d’utilisation.
* Une compréhension de base des conditions du parcours et de l’éditeur d’expression avancé est une condition préalable.
* Testez toujours le parcours en mode test avant de le publier pour vérifier que les formules d’attente produisent l’heure de diffusion correcte du lundi.

**Terminologie:**

* Nom canonique : planification des e-mails le jour de la semaine — Acronyme : aucun — variantes : e-mails le jour de la semaine uniquement, diffusion e-mail aux heures de bureau
* Synonymes : « Chemin du samedi » / « Chemin du dimanche » = « Chemins du week-end » ; « Chemin des autres cas » = « Chemin du jour de la semaine »
* Ne pas confondre : fuseau horaire du parcours (utilisé pour l’évaluation du jour de la semaine) ≠ fuseau horaire local du destinataire

**FAQ:**

* **Q : Quelle formule retarde l&#39;entrée du samedi au lundi à 9 h ?** — Utiliser `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))` sur le chemin du samedi (2 jours vers l&#39;avant le lundi).
* **Q : Quelle formule retarde l&#39;entrée du dimanche au lundi à 9 h ?** — Utiliser `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))` sur le chemin du dimanche (1 jour vers l&#39;avant le lundi).
* **Q : Quel fuseau horaire est utilisé lors de l’évaluation de la condition du jour de la semaine ?** — Fuseau horaire configuré du parcours défini dans les propriétés du parcours ; il ne s’agit pas du fuseau horaire local du destinataire.
* **Q : Les entrées de jour de la semaine ont-elles besoin d’une activité Attente ?** : non, les profils qui entrent du lundi au vendredi accèdent directement à l’activité d’action E-mail sans attendre.
* **Q : Comment puis-je tester que les entrées du week-end sont correctement placées en file d’attente ?** — En mode test, créez des profils de test avec des heures d’entrée simulées le samedi et le dimanche, vérifiez qu’ils suivent le bon chemin conditionnel et recevez l’e-mail le lundi à l’heure configurée.

+++
