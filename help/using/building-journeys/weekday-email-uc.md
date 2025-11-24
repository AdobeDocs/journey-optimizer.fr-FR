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
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: c92e5bacdab179587b9cdec6bbde962a597b8de8
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%

---

# Envoyer des e-mails uniquement les jours de la semaine {#send-emails-only-on-weekdays}

Ce cas pratique montre comment configurer un parcours dans Adobe Journey Optimizer qui envoie des e-mails uniquement les jours de la semaine (du lundi au vendredi). Pour les profils qui rejoignent le parcours le week-end (samedi ou dimanche), les e-mails sont automatiquement mis en file d’attente et envoyés le lundi à une heure spécifiée. Cela garantit un engagement optimal en diffusant des messages pendant la semaine de travail.

## Présentation du cas d’utilisation

**Le défi** : veiller à ce que les e-mails ne soient envoyés que les jours de la semaine, même si les profils peuvent entrer sur le parcours le week-end. Pour les entrées du week-end, les e-mails doivent être placés en file d’attente et envoyés le lundi à une heure spécifique.

**La solution** : utilisez une activité de condition pour identifier le jour de la semaine. Pour les entrées de week-end, les activités d’attente avec des formules personnalisées retardent l’e-mail jusqu’au lundi. Les entrées de jour de la semaine passent directement à l’étape d’envoi de l’e-mail.

Cette approche vous explique comment utiliser une activité de condition pour vérifier si le jour en cours est le samedi ou le dimanche, implémenter des activités d’attente avec des formules personnalisées pour les entrées de week-end, mettre en file d’attente les e-mails de week-end pour une diffusion du lundi à une heure spécifique et envoyer immédiatement les e-mails pour les entrées de jour de la semaine (du lundi au vendredi).

Cette approche est idéale pour les campagnes par e-mail B2B (business-to-business), les newsletters et les communications professionnelles, les annonces liées à l’entreprise, les mises à jour de produits liés au travail et toute campagne marketing pour laquelle la diffusion du week-end n’est pas souhaitée.

>[!NOTE]
>
>Pour implémenter ce cas d’utilisation, vous avez besoin d’une instance Adobe Journey Optimizer active avec une [surface de canal e-mail](../configuration/channel-surfaces.md) configurée, une [audience](../audience/about-audiences.md) ou [événement](../event/about-events.md) pour déclencher le parcours, ainsi qu’une compréhension de base des [conditions de parcours ](condition-activity.md) et [expressions](expression/expressionadvanced.md).


## Étapes dʼimplémentation

### Étape 1 : création de votre parcours

1. Accédez à **[!UICONTROL Gestion des Parcours]** > **[!UICONTROL Parcours]** dans Adobe Journey Optimizer.

1. Cliquez sur **[!UICONTROL Créer un Parcours]** pour créer un parcours. [En savoir plus sur la création de parcours ](journey-gs.md)

1. Configurez les [propriétés du parcours ](journey-properties.md).

1. Choisissez votre point d’entrée de parcours :
   * **[Lecture d’audience](read-audience.md)** : pour les campagnes par lots ciblant une audience spécifique
   * **[Événement](../event/about-events.md)** : pour les parcours déclenchés en temps réel en fonction du comportement du client

### Étape 2 : ajoutez une activité Condition pour vérifier le jour de la semaine

Juste après le début du parcours, ajoutez une activité **[!UICONTROL Condition]** pour vérifier si le jour en cours est le samedi ou le dimanche. Le workflow sera ainsi divisé en plusieurs branches en conséquence.

1. Faites glisser et déposez une activité **[!UICONTROL Condition]** sur la zone de travail après votre point d’entrée. [En savoir plus sur les activités de condition](condition-activity.md)

1. Cliquez sur l’activité **[!UICONTROL Condition]** pour ouvrir son panneau de configuration.

1. Sélectionnez **[!UICONTROL Condition de temps]** comme type de condition.

1. Sélectionnez **[!UICONTROL Jour de la semaine]** comme option de filtrage temporel.

1. Pour le **premier chemin (samedi)**, sélectionnez **samedi** uniquement. Libellez ce chemin comme « Samedi ».

1. Cliquez sur **[!UICONTROL Ajouter un chemin]** pour créer une deuxième condition.

1. Pour le **deuxième chemin (dimanche)**, sélectionnez **[!UICONTROL Jour de la semaine]** et choisissez **Dimanche** uniquement. Libellez ce chemin comme étant « Dimanche ».

   ![Configuration des conditions du samedi et du dimanche dans l&#39;éditeur d&#39;expression](assets/weekday-email-uc-condition-expression.png)


1. Cochez **[!UICONTROL Afficher le chemin pour d’autres cas que celui ou ceux ci-dessus]** pour créer un chemin pour les entrées de jour de la semaine (lundi à vendredi).

>[!NOTE]
>
>Le fuseau horaire utilisé pour l’évaluation du jour de la semaine est défini au niveau du parcours dans les propriétés du parcours, et non au niveau de la condition. Le fuseau horaire du parcours utilisé dans la formule est celui configuré pour le parcours, et non celui du destinataire. [En savoir plus sur la gestion des fuseaux horaires](timezone-management.md).

### Étape 3 : Configurer les activités d’attente pour les entrées de week-end

Pour les profils qui s’enregistrent le samedi ou le dimanche, utilisez les activités **[!UICONTROL Attente]** avec des formules personnalisées pour reporter l’e-mail au lundi, à l’heure souhaitée.

Dans l&#39;activité **[!UICONTROL Attente]**, la formule est la suivante :

```javascript
toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))
```

Où ce qui suit est vrai :

* **X** correspond au nombre de jours d&#39;attente :
   * Utiliser **2** pour le samedi (attendre le lundi)
   * Utiliser **1** pour le dimanche (attendre le lundi)
* **H** est l&#39;heure que vous souhaitez envoyer (par exemple, **9** pour 9 h)


**Exemple pour le samedi :**

```javascript
toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))
```

**Exemple pour dimanche :**

```javascript
toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))
```

Pour implémenter cette fonction dans votre parcours :

1. Sur le chemin **Saturday**, ajoutez une activité **[!UICONTROL Wait]** après la condition.

1. Sélectionnez **[!UICONTROL Durée]** comme type d’attente.

1. Cliquez sur **[!UICONTROL Mode avancé]** pour saisir la formule personnalisée.

1. Enter : `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))`

   ![Parcours avec trois chemins de condition : samedi, dimanche et jours de la semaine](assets/weekday-email-uc-paths.png)

1. Répétez les mêmes étapes pour le chemin **dimanche**, en utilisant : `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))`

>[!TIP]
>
>Pour les heures d&#39;ouverture plus complexes (p. ex., envoyer seulement entre 9 h et 17 h les jours de semaine), vous pouvez améliorer davantage la formule et les conditions.

### Étape 4 : Branche de jour de semaine

Pour les profils qui s’enregistrent du lundi au vendredi, passez à l’étape Envoyer un e-mail comme d’habitude.

1. Dans le chemin **Jour de la semaine** (chemin « autres cas »), passez directement à l’ajout d’une activité d’action **[!UICONTROL E-mail]**. Aucune activité **[!UICONTROL Attente]** n’est nécessaire pour les entrées de jour de la semaine.

1. Configurez votre e-mail selon vos besoins.

### Étape 5 : terminer le flux de parcours

Après les activités **[!UICONTROL Attente]** sur les chemins samedi et dimanche, les trois chemins (samedi, dimanche et jours de la semaine) doivent tous être dirigés vers la même activité d’action **[!UICONTROL E-mail]**. Ajoutez une activité **[!UICONTROL Fin]** après l’e-mail.

### Présentation visuelle des workflows

Le workflow de parcours complet suit cette logique :

* **Début** → **[!UICONTROL Condition]** : Est-ce le samedi ou le dimanche ?
   * **Oui (samedi) :** **[!UICONTROL Attendez]** jusqu’au lundi 9 h → **[!UICONTROL Envoyer un e-mail]**
   * **Oui (dimanche) :** **[!UICONTROL Attendez]** jusqu’au lundi 9 h → **[!UICONTROL Envoyer un e-mail]**
   * **Non (du lundi au vendredi) :** **[!UICONTROL Envoyer un e-mail]** immédiatement

Ainsi, tous les e-mails sont envoyés uniquement les jours de la semaine, les entrées du week-end étant automatiquement mises en file d’attente pour la diffusion du lundi.

### Étape 6 : test du parcours

Avant de publier, testez minutieusement votre logique de parcours en mode test Adobe Journey Optimizer pour confirmer que tout fonctionne comme prévu :

1. Cliquez sur le bouton **[!UICONTROL Test]** dans le coin supérieur droit.

1. Activez le mode test. [Découvrez comment tester votre parcours ](testing-the-journey.md)

1. Créez des [profils de test](../audience/creating-test-profiles.md) avec des heures d’entrée simulées pour différents jours de la semaine :
   * **Entrée du samedi** : vérifiez que le profil suit le chemin du samedi, attend et reçoit un e-mail le lundi à l’heure spécifiée
   * **Entrée du dimanche** : vérifiez que le profil suit le chemin du dimanche, attend et reçoit un e-mail le lundi à l’heure spécifiée
   * **Entrées du lundi au vendredi** : vérifiez que les e-mails sont envoyés immédiatement sans attente.

1. Consultez la visualisation du parcours pour vous assurer que les profils suivent les chemins d’accès conditionnels appropriés (samedi, dimanche ou jour de la semaine).

1. Recherchez d’éventuelles erreurs ou avertissements dans le parcours. [En savoir plus sur la résolution des problèmes liés aux parcours ](troubleshooting.md)

1. Vérifiez que les formules d’attente calculent la durée correcte pour l’heure de livraison du lundi souhaitée.

>[!IMPORTANT]
>
>Testez toujours votre logique de parcours en mode test pour vous assurer que les activités d’attente se comportent comme prévu. Utilisez le mode Test pour simuler différents scénarios d’entrée et vérifier que les entrées du week-end sont correctement placées en file d’attente pour la diffusion du lundi. [En savoir plus sur les bonnes pratiques en matière de tests de parcours ](testing-the-journey.md)

### Étape 7 : publier votre parcours

Une fois le test terminé :

1. Cliquez sur **[!UICONTROL Publier]** dans le coin supérieur droit.

1. Confirmez la publication. [En savoir plus sur la publication de parcours ](publish-journey.md)

1. Surveillez les performances du parcours à l’aide des rapports de Parcours [](report-journey.md) et [rapports dynamiques](../reports/journey-live-report.md).


## Rubriques connexes

* [À propos des activités de condition](condition-activity.md) - Découvrez comment créer différents chemins dans votre parcours
* [Conditions d’utilisation dans un parcours ](conditions.md) - Guide détaillé sur les conditions de parcours
* [Activité d’attente](wait-activity.md) - Configuration des durées d’attente et des formules
* [Fonctions de date](functions/date-functions.md) - Référence complète pour les fonctions de date et d’heure
* [Éditeur d’expression](expression/expressionadvanced.md) - Créer des expressions complexes
* [Bonnes pratiques relatives aux Parcours ](journey-gs.md#best-practices) - Approches recommandées pour la conception de parcours
* [Article de blog de la communauté : Comment envoyer des e-mails uniquement les jours de semaine](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/how-to-send-emails-only-on-weekdays-in-adobe-journey-optimizer/ba-p/760400){target="_blank"} - Article de blog original avec des exemples détaillés

