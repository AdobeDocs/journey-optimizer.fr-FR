---
solution: Journey Optimizer
product: journey optimizer
title: Envoyer des e-mails uniquement les jours de la semaine
description: Découvrez comment configurer un parcours pour envoyer des e-mails uniquement les jours de la semaine dans Adobe Journey Optimizer
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: parcours, cas d’utilisation, jours de la semaine, condition, e-mail, planification
version: Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: c8d5160b473faac873b765fc5daead935a83760d
workflow-type: tm+mt
source-wordcount: '1872'
ht-degree: 0%

---

# Envoyer des e-mails uniquement les jours de la semaine {#send-emails-only-on-weekdays}

Ce cas pratique montre comment configurer un parcours dans Adobe Journey Optimizer qui envoie des e-mails uniquement les jours de la semaine (du lundi au vendredi). Pour les profils qui rejoignent le parcours le week-end (samedi ou dimanche), les e-mails sont automatiquement mis en file d’attente et envoyés le lundi à une heure spécifiée. Cela garantit un engagement optimal en diffusant des messages pendant la semaine de travail.

## Présentation du cas d’utilisation

**Le défi** : veiller à ce que les e-mails ne soient envoyés que les jours de la semaine, même si les profils peuvent entrer sur le parcours le week-end. Pour les entrées du week-end, les e-mails doivent être placés en file d’attente et envoyés le lundi à une heure spécifique.

**La solution** : utilisez une activité de condition pour identifier le jour de la semaine. Pour les entrées de week-end, les activités d’attente avec des formules personnalisées retardent l’e-mail jusqu’au lundi. Les entrées de jour de la semaine passent directement à l’étape d’envoi de l’e-mail.

Cette approche vous montre comment :

* Utilisez une activité de condition pour vérifier si le jour en cours est samedi ou dimanche
* Implémenter des activités d’attente avec des formules personnalisées pour les entrées de week-end
* Mettre en file d’attente les e-mails de week-end pour une diffusion le lundi à une heure spécifique
* Envoyer immédiatement des e-mails pour les entrées de jour de la semaine (lundi à vendredi)

Cette approche est idéale pour :

* Campagnes par e-mail business-to-business (B2B)
* Newsletters et communications professionnelles
* Annonces liées à l’entreprise
* Mises à jour de produits liés au travail
* Toute campagne marketing pour laquelle la diffusion du week-end n’est pas souhaitée

>[!VIDEO]
>
>Regardez le tutoriel vidéo détaillé [pas à pas](#how-to-video) au bas de cette page pour voir l’implémentation complète.

## Conditions préalables

Pour mettre en œuvre ce cas d’utilisation, vous devez :

* Une instance Adobe Journey Optimizer active
* Une [surface de canal e-mail](../configuration/channel-surfaces.md) configurée
* Une [audience](../audience/about-audiences.md) ou [événement](../event/about-events.md) pour déclencher le parcours
* Compréhension de base des [conditions de parcours &#x200B;](condition-activity.md) et [expressions](expression/expressionadvanced.md)

## Étapes dʼimplémentation

### Étape 1 : création de votre parcours

1. Accédez à **[!UICONTROL Gestion des Parcours]** > **[!UICONTROL Parcours]** dans Adobe Journey Optimizer.

1. Cliquez sur **[!UICONTROL Créer un Parcours]** pour créer un parcours. [En savoir plus sur la création de parcours &#x200B;](journey-gs.md)

1. Configurez les propriétés du parcours :
   * **Name** : campagne par e-mail en semaine
   * **Description** : envoie des e-mails uniquement les jours de la semaine (lundi à vendredi).
   * Définir l’espace de noms approprié à votre cas d’utilisation

[En savoir plus sur les propriétés du parcours](journey-properties.md)

1. Choisissez votre point d’entrée de parcours :
   * **[Lecture d’audience](read-audience.md)** : pour les campagnes par lots ciblant une audience spécifique
   * **[Événement](../event/about-events.md)** : pour les parcours déclenchés en temps réel en fonction du comportement du client

### Étape 2 : ajoutez une activité Condition pour vérifier le jour de la semaine

Juste après le début du parcours, ajoutez une activité **[!UICONTROL Condition]** pour vérifier si le jour en cours est le samedi ou le dimanche. Le workflow sera ainsi divisé en plusieurs branches en conséquence.

1. Faites glisser et déposez une activité **[!UICONTROL Condition]** sur la zone de travail après votre point d’entrée. [En savoir plus sur les activités de condition](condition-activity.md)

1. Cliquez sur l’activité Condition pour ouvrir son panneau de configuration.

1. Dans la section **[!UICONTROL Type de condition]**, sélectionnez **[!UICONTROL Condition de Source de données]**. [En savoir plus sur les types de conditions](condition-activity.md#data_source_condition)

### Étape 3 : configurer la condition pour identifier le samedi

Créez le premier chemin de condition pour identifier les entrées du samedi.

1. Cliquez sur **[!UICONTROL Mode avancé]** pour ouvrir l’éditeur d’expression. [En savoir plus sur l’éditeur d’expression](expression/expressionadvanced.md)

1. Saisissez l’expression suivante pour vérifier si le jour en cours est le samedi :

   ```javascript
   dayOfWeek(now()) == 7
   ```

   Cette méthode utilise la fonction `dayOfWeek()` avec `now()` pour obtenir la date du jour. [En savoir plus sur les fonctions de date](functions/date-functions.md)

   ![Configuration de la condition du samedi dans l&#39;éditeur d&#39;expression](assets/weekday-email-uc-condition-expression.png)

1. Cliquez sur **[!UICONTROL Ok]** pour enregistrer la condition.

1. Libellez ce chemin comme « Samedi ».

### Étape 4 : ajouter un deuxième chemin de condition pour dimanche

1. Dans l’activité Condition , cliquez sur **[!UICONTROL Ajouter un chemin d’accès]** pour créer une deuxième condition.

1. Dans l’éditeur d’expression du deuxième chemin d’accès, saisissez :

   ```javascript
   dayOfWeek(now()) == 1
   ```

   Cette option permet de vérifier si le jour en cours est le dimanche.

1. Libellez ce chemin comme étant « Dimanche ».

1. Cochez **[!UICONTROL Afficher le chemin pour d’autres cas que celui ou ceux ci-dessus]** pour créer un chemin pour les entrées de jour de la semaine (lundi à vendredi).

   **Valeurs du jour de la semaine :**
   * 1 = Dimanche
   * 2 = Lundi
   * 3 = Mardi
   * 4 = Mercredi
   * 5 = Jeudi
   * 6 = vendredi
   * 7 = Samedi

>[!NOTE]
>
>La fonction `dayOfWeek()` renvoie un entier représentant le jour de la semaine, où 1 correspond au dimanche et 7 au samedi. Cela suit la norme ISO-8601 pour la numérotation des jours.

### Étape 4 : Configurer les activités d’attente pour les entrées de week-end

Pour les profils qui s’enregistrent le samedi ou le dimanche, utilisez les activités d’attente avec des formules personnalisées pour retarder l’e-mail jusqu’au lundi à l’heure souhaitée.

![Parcours avec trois chemins de condition : samedi, dimanche et jours de la semaine](assets/weekday-email-uc-paths.png)

**Pour le chemin du samedi :**

1. Ajoutez une activité **[!UICONTROL Attente]**. [En savoir plus sur les activités d’attente](wait-activity.md)

1. Sélectionnez **[!UICONTROL Durée]** comme type d’attente.

1. Cliquez sur **[!UICONTROL Mode avancé]** pour saisir une formule personnalisée.

1. Entrez la formule suivante pour attendre jusqu&#39;au lundi à 9 h :

   ```javascript
   toDuration("PT" + (48 - getHourOfDay(now())) + "H")
   ```

   Ou utilisez cette formule alternative :

   ```javascript
   setHours(nowWithDelta(2, "days"), 9)
   ```

   **Explication** : cette formule calcule le temps d&#39;attente du samedi au lundi à 9 h. La valeur X=2 représente 2 jours en avant (samedi + 2 jours = lundi). [En savoir plus sur les fonctions de date](functions/date-functions.md#nowWithDelta)

**Pour le chemin du dimanche :**

1. Ajoutez une activité **[!UICONTROL Attente]**.

1. Sélectionnez **[!UICONTROL Durée]** comme type d’attente.

1. Cliquez sur **[!UICONTROL Mode avancé]** pour saisir une formule personnalisée.

1. Entrez la formule suivante pour attendre jusqu&#39;au lundi à 9 h :

   ```javascript
   setHours(nowWithDelta(1, "days"), 9)
   ```

   **Explication** : cette formule attend 1 jour (dimanche + 1 jour = lundi) et définit l’heure sur 9 heures. La valeur X=1 représente 1 jour en avant, et H=9 représente 9 h.

>[!TIP]
>
>Vous pouvez personnaliser le paramètre heure (H) à tout moment où vous souhaitez que l’e-mail soit envoyé le lundi. Par exemple, remplacez 9 par 10 pour 10 h ou par 14 pour 14 h.

### Étape 5 : configurer le chemin d’accès du jour de la semaine

Pour le **Chemin d’accès en semaine** (du lundi au vendredi) :

1. Procédez directement à l’ajout d’une activité d’action **[!UICONTROL E-mail]**. Aucune activité d’attente n’est nécessaire pour les entrées de jour de la semaine. [En savoir plus sur les actions e-mail](journeys-message.md)

1. Configurez votre e-mail :
   * Sélectionnez ou créez votre [contenu d’e-mail](../email/get-started-email-design.md)
   * Configurez les [&#x200B; paramètres d’e-mail &#x200B;](../email/email-settings.md)
   * Configurez [personnalisation](../personalization/personalize.md) selon les besoins

1. Ajoutez une activité **[!UICONTROL Fin]** après l’e-mail. [En savoir plus sur les activités de fin](end-activity.md)

### Étape 6 : fusionner les chemins de week-end dans l’e-mail

Après les activités d’attente sur les chemins samedi et dimanche, fusionnez-les dans la même activité d’action E-mail :

1. Dans l’activité Attente du samedi , ajoutez une action **[!UICONTROL E-mail]**.

1. Dans l’activité Attente le dimanche , connectez-vous à la même action E-mail .

1. Le chemin d’accès au jour de la semaine doit également être transmis à cette action e-mail.


### Étape 7 : Tester votre parcours

Avant de publier, testez minutieusement votre logique de parcours en mode test Adobe Journey Optimizer pour confirmer que tout fonctionne comme prévu :

1. Cliquez sur le bouton **[!UICONTROL Test]** dans le coin supérieur droit.

1. Activez le mode test. [Découvrez comment tester votre parcours &#x200B;](testing-the-journey.md)

1. Créez des [profils de test](../audience/creating-test-profiles.md) avec des heures d’entrée simulées pour différents jours de la semaine :
   * **Entrée du samedi** : vérifiez que le profil suit le chemin du samedi, attend et reçoit un e-mail le lundi à l’heure spécifiée
   * **Entrée du dimanche** : vérifiez que le profil suit le chemin du dimanche, attend et reçoit un e-mail le lundi à l’heure spécifiée
   * **Entrées du lundi au vendredi** : vérifiez que les e-mails sont envoyés immédiatement sans attente.

1. Consultez la visualisation du parcours pour vous assurer que les profils suivent les chemins d’accès conditionnels appropriés (samedi, dimanche ou jour de la semaine).

1. Recherchez d’éventuelles erreurs ou avertissements dans le parcours. [En savoir plus sur la résolution des problèmes liés aux parcours &#x200B;](troubleshooting.md)

1. Vérifiez que les formules d’attente calculent la durée correcte pour l’heure de livraison du lundi souhaitée.

>[!IMPORTANT]
>
>Testez toujours minutieusement la logique de votre parcours avant de le publier en production. Utilisez le mode Test pour simuler différents scénarios d’entrée et vérifier que les entrées du week-end sont correctement placées en file d’attente pour la diffusion du lundi. [En savoir plus sur les bonnes pratiques en matière de tests de parcours &#x200B;](testing-the-journey.md)

### Étape 8 : publier votre parcours

Une fois le test terminé :

1. Cliquez sur **[!UICONTROL Publier]** dans le coin supérieur droit.

1. Confirmez la publication. [En savoir plus sur la publication de parcours &#x200B;](publish-journey.md)

1. Surveillez les performances du parcours à l’aide des rapports de Parcours [&#128279;](report-journey.md) et [rapports dynamiques](../reports/journey-live-report.md).

## Bonnes pratiques et remarques

### Optimiser le workflow avec des formules améliorées

Pour améliorer votre workflow et gérer des besoins métier plus complexes :

* **Heures d’ouverture complexes** : étendez les formules pour tenir compte des jours fériés, des fuseaux horaires ou d’heures d’ouverture spécifiques au-delà de la vérification de base en semaine.

* **Délais de diffusion personnalisés** : ajustez le paramètre d’heure (H) dans la formule d’attente pour qu’il corresponde à votre heure d’envoi optimale. Par exemple, si 10 heures du matin affichent de meilleurs taux d’engagement, modifiez la formule pour utiliser l’heure 10.

* **Prise en charge de plusieurs fuseaux horaires** : envisagez de créer des parcours distincts pour différentes régions géographiques afin d’assurer une diffusion le lundi dans le fuseau horaire local de chaque destinataire.

### Gestion des fuseaux horaires

La fonction `now()` et l’exécution du parcours utilisent le fuseau horaire configuré au niveau du parcours. Tenez compte des points suivants :

* **Fuseau horaire du Parcours** : assurez-vous que le fuseau horaire du parcours correspond à vos besoins. Configurez-le dans les propriétés du parcours avant de le publier. [En savoir plus sur la gestion des fuseaux horaires](timezone-management.md).

* **Audiences globales** : si votre audience s’étend sur plusieurs fuseaux horaires, la vérification du jour de la semaine a lieu dans le fuseau horaire configuré du parcours, et non dans le fuseau horaire local du destinataire.

* **Planification localisée** : pour une diffusion spécifique au fuseau horaire, créez des parcours distincts pour différentes régions ou utilisez les paramètres de fuseau horaire dans l’activité Lecture d’audience.

### Entrée sur le parcours et synchronisation

* **Lecture de parcours d’audience** : pour les parcours par lots, [planifiez la Lecture d’audience](read-audience.md#schedule) à déclencher à un moment adapté à votre audience. Les exécutions tôt le matin (par exemple, à 6 :00) sont fréquentes pour les communications d’entreprise.

* **parcours basés sur un événement** : la condition sera évaluée immédiatement à la réception de l’événement. Les profils qui entrent le week-end attendront automatiquement le lundi. [En savoir plus sur les événements](../event/about-events.md)

* **Considérations relatives au délai d’attente** : assurez-vous que vos paramètres de délai d’attente de [parcours &#x200B;](journey-properties.md#timeout) prennent en compte la période d’attente maximale (jusqu’à 2 jours du samedi au lundi).

### Les tests sont essentiels

Comme indiqué dans le guide de mise en œuvre, testez toujours la logique de votre parcours pour confirmer que tout fonctionne comme prévu :

* Utilisez le **mode test** pour simuler différents scénarios d’entrée sans envoyer d’e-mails réels
* Testez les trois chemins : entrées du samedi, entrées du dimanche et entrées du jour de la semaine
* Vérifier que les calculs de durée d’attente sont corrects
* Confirmer que la diffusion du lundi a lieu à l’heure spécifiée
* Vérifier la visualisation du parcours pour assurer un routage correct du chemin

### Rentrée et fréquence

* Pour les campagnes récurrentes, configurez les paramètres **[!UICONTROL Rentrée]** de manière appropriée. [En savoir plus sur les paramètres de rentrée](entry-management.md)

* Si les profils peuvent rejoindre à nouveau le parcours, ils feront l’objet d’une vérification sur le jour de la semaine à chaque fois, afin que les entrées du week-end soient toujours placées en file d’attente pour le lundi.

* Pensez à ajouter des [règles de limitation de la fréquence](../conflict-prioritization/journey-capping.md) pour éviter une messagerie excessive si les profils peuvent être saisis fréquemment à nouveau.

## Variantes avancées

### Ciblage par jour spécifique

Pour envoyer des e-mails uniquement certains jours (par exemple, les mardis et jeudis), modifiez la condition :

```javascript
dayOfWeek(now()) == 3 or dayOfWeek(now()) == 5
```

Pour tous les autres jours, ajoutez une activité Attente qui calcule le nombre de jours jusqu’au mardi ou jeudi suivant.

### Des heures d&#39;envoi différentes pour des jours différents

Vous pouvez créer plusieurs chemins avec différentes formules d’attente pour différents comportements de week-end :

* **livraison samedi → mercredi** : utiliser `nowWithDelta(4, "days")`
* **Diffusion dimanche → mardi** : utilisez `nowWithDelta(2, "days")`

Vous bénéficiez ainsi d’une plus grande flexibilité dans votre planning d’envoi.

### Diffusion pendant les heures d’ouverture

Pour garantir une diffusion pendant les heures de bureau, ajustez le paramètre heure dans votre formule d’attente. Par exemple, pour une diffusion à 14 h au lieu de 9 h :

```javascript
setHours(nowWithDelta(1, "days"), 14)
```

Vous pouvez également ajouter une deuxième condition après l’Attente pour vérifier si l’heure actuelle correspond aux heures ouvrables précédant l’envoi.

### Exclusion des vacances

Pour exclure les jours fériés, ajoutez un chemin de condition supplémentaire qui vérifie des dates spécifiques :

```javascript
toDateTimeOnly(now()) == toDateTimeOnly("2024-12-25T00:00:00")
```

Si la condition correspond à un jour férié, ajoutez une activité Attente pour la retarder au jour ouvrable suivant. [En savoir plus sur les fonctions de comparaison de dates](functions/date-functions.md)

## Rubriques connexes

* [À propos des activités de condition](condition-activity.md) - Découvrez comment créer différents chemins dans votre parcours
* [Conditions d’utilisation dans un parcours &#x200B;](conditions.md) - Guide détaillé sur les conditions de parcours
* [Activité d’attente](wait-activity.md) - Configuration des durées d’attente et des formules
* [Fonctions de date](functions/date-functions.md) - Référence complète pour les fonctions de date et d’heure
* [Éditeur d’expression](expression/expressionadvanced.md) - Créer des expressions complexes
* [Tester le parcours &#x200B;](testing-the-journey.md) - Valider la logique de parcours avant la publication
* [Gestion des fuseaux horaires](timezone-management.md) - Gérer les différents fuseaux horaires dans les parcours
* [Bonnes pratiques relatives aux Parcours &#x200B;](journey-gs.md#best-practices) - Approches recommandées pour la conception de parcours

## Vidéo pratique

Découvrez comment envoyer des e-mails uniquement les jours de la semaine à l’aide de Adobe Journey Optimizer. Cette vidéo présente l’implémentation étape par étape des activités de condition et des formules d’attente pour mettre en file d’attente les entrées de week-end pour la diffusion du lundi.

>[!VIDEO](https://video.tv.adobe.com/v/3469330?quality=12&learn=on)

## Ressources supplémentaires

* [Documentation relative à l’éditeur d’expression](expression/expressionadvanced.md) - Créer et valider des expressions de parcours
* [guide du concepteur de Parcours &#x200B;](using-the-journey-designer.md) - Principal de la zone de travail de parcours
* [Présentation des cas d’utilisation de Parcours &#x200B;](jo-use-cases.md) - Explorez d’autres modèles et exemples de parcours
* [Article de blog de la communauté : Comment envoyer des e-mails uniquement les jours de semaine](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/how-to-send-emails-only-on-weekdays-in-adobe-journey-optimizer/ba-p/760400?profile.language=fr){target="_blank"} - Article de blog original avec des exemples détaillés

