---
solution: Journey Optimizer
product: journey optimizer
title: Questions fréquentes
description: Questions fréquentes sur les activités en direct
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e7e994ca-aa0c-4e86-8710-c87430b74188
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 48%

---

# Questions fréquentes {#mobile-live-faq}

## Questions générales

+++Quelle est la différence entre une activité En ligne et une notification push ?

L’activité en direct fournit des mises à jour persistantes en temps réel sur l’écran de verrouillage et l’île dynamique sans que les utilisateurs aient à déverrouiller leur appareil. Les notifications push sont des alertes temporaires qui disparaissent une fois ignorées. L’activité active reste visible et peut être mise à jour plusieurs fois jusqu’à ce qu’elle soit explicitement terminée.

+++

+++Combien d’instances d’activités dynamiques peuvent être actives à la fois ?

Une application iOS peut exécuter plusieurs instances d’activités dynamiques simultanément, y compris plusieurs instances qui utilisent le même type d’`ActivityAttributes`.

Les développeurs n’imposent aucune limite stricte quant au nombre d’instances d’activité dynamique pouvant exister pour un type d’attribut donné. Vous pouvez en démarrer autant que le nécessite la logique de votre application, par exemple, une par diffusion ou trajet en cours. Cependant, iOS applique une limite au niveau du système sur le nombre d’instances d’activité dynamiques pouvant être actives ou visibles à la fois.

En pratique :

* iOS prend généralement en charge jusqu’à environ cinq instances d’activité en direct simultanées par application.

* Si vous dépassez ce nombre, le système risque de ne plus afficher certaines instances d’activité ou d’arrêter les anciennes pour économiser des ressources.

* Chaque instance d’activité active comporte un `Activity.id` unique, ce qui vous permet de la mettre à jour ou de la terminer individuellement.

+++

+++Les utilisateurs doivent-ils ouvrir l’application pour recevoir les mises à jour des activités en direct ?

Non. L’activité en direct peut être démarrée, mise à jour et terminée à distance, même lorsque l’application est complètement fermée. Il s’agit de l’un des principaux avantages de la fonctionnalité.

+++

+++Quelles versions d’iOS prennent en charge l’activité Live ?

* iOS 16.1+ : prise en charge de base des activités en direct
* iOS 17.2+ : fonctionnalité de démarrage par notification push (démarrage à distance sans ouverture de l’application)
* iOS 18+ : prise en charge des canaux de diffusion pour l’activité en direct basée sur l’audience
+++

+++Pendant combien de temps une activité Live peut-elle rester active ?

Apple limite l&#39;activité en direct à **8 heures de mises à jour actives**. Ensuite, le système met automatiquement fin à l’activité, bien qu’elle puisse rester visible dans un état statique pendant **12 heures supplémentaires au maximum** avant d’être supprimée. Vous pouvez également terminer une activité active plus tôt en définissant un `dismissalDate` ou en appelant explicitement `activity.end()` dans votre application.

+++

### Questions des développeurs et développeuses

+++Dois-je créer une extension de widget distincte pour l’activité Live ?

Oui. L’activité en direct est affichée via WidgetKit. Vous devez donc créer une extension de widget dans votre projet Xcode et implémenter le `ActivityConfiguration`.
[En savoir plus sur la configuration des widgets](mobile-live-configuration-sdk.md)

+++

+++Puis-je utiliser la même classe `LiveActivityAttributes` pour l’activité Live locale et distante ?

Oui. La même classe d’attributs fonctionne pour les activités dynamiques démarrées localement et à distance (push-to-start). Vous devez vous assurer de l’enregistrer avec `Messaging.registerLiveActivity()`.

+++

+++Que se passe-t-il si j’envoie une mise à jour pour une activité Live qui n’existe pas ?

Si vous envoyez un événement de mise à jour ou de fin pour un `liveActivityID` ou un `channelID` inexistant, la requête échoue silencieusement sur l’appareil. Assurez-vous toujours de suivre les instances d’activités dynamiques actives pour chaque utilisateur.

+++

+++Puis-je tester l’activité En direct dans le simulateur iOS ?

Oui, vous pouvez tester l’activité active démarrée localement et l’activité active démarrée à distance dans le simulateur iOS.

* **Local** : cela inclut la création, la mise à jour et l’envoi d’une activité Live directement depuis votre application à l’aide des API **ActivityKit**.

* **Distant** : pour tester à distance la fonctionnalité d’activité en direct, intégrez notre SDK de messagerie à votre application et utilisez les API d’exécution fournies pour envoyer à distance le démarrage, la mise à jour et l’arrêt de votre appareil de test ou de votre simulateur iOS. Comme pour les notifications push, qui peuvent actuellement être testées avec l’intégration des SDK Adobe.

+++

+++Comment gérer les mises à jour lorsque l’application fonctionne en arrière-plan ?

Le SDK gère cela automatiquement. Une fois enregistrée, l’activité Live reçoit des mises à jour même lorsque l’application est arrêtée. Aucun mode d’arrière-plan supplémentaire n’est requis.
+++

+++Quelle est la différence entre `liveActivityID` et `channelID` ?

* `liveActivityID` : utilisé pour les activités en direct individuelles (unitaires) ciblant des utilisateurs et utilisatrices spécifiques. Chaque identifiant représente une instance d’activité active unique.
* `channelID` : utilisé pour l’activité de diffusion en direct envoyée aux audiences. Tous les utilisateurs et toutes les utilisatrices d’une audience reçoivent les mêmes mises à jour sur le même canal.
+++

+++Puis-je personnaliser l’aspect de la Dynamic Island séparément de l’écran de verrouillage ?

Oui. Le `ActivityConfiguration` dispose de fermetures distinctes pour le contenu de l’écran de verrouillage et celui de la Dynamic Island (états développé, compact et minimal), chaque conception étant indépendante.
+++

+++Dois-je stocker manuellement les jetons push ?

Non. Lorsque vous enregistrez un type d’activité en direct avec `Messaging.registerLiveActivity()`, le SDK collecte et gère automatiquement les jetons push.
+++

+++Existe-t-il des limites aux démarrages distants de l’activité Live ?

Oui. Les démarrages à distance via `ActivityKit` sont soumis à des limites appliquées par le système. Si vous tentez plusieurs demandes de démarrage en succession rapide, iOS peut rejeter d’autres démarrages en raison des quotas d’activité en direct ou des contraintes budgétaires. Après environ 5 tentatives de démarrage consécutives, les requêtes suivantes commencent à échouer jusqu’à ce qu’une brève période de refonte soit passée.

+++

+++Quel est le budget alloué aux mises à jour prioritaires ?

Apple ne spécifie pas de limite numérique exacte pour les mises à jour d&#39;activité haute priorité `(priority: 10)` Live. Le système gère un budget interne dynamique qui limite la fréquence d’envoi de ces mises à jour. Si un trop grand nombre de mises à jour hautement prioritaires sont publiées en peu de temps, iOS peut ralentir ou retarder les mises à jour suivantes.

Pour minimiser le ralentissement :

* **Équilibrer les niveaux de priorité** : combinez les mises à jour de `(priority: 5)` standard et de haute `(priority: 10)` en fonction de l’importance.
* **Utilisez la priorité élevée avec parcimonie** : réservez la priorité élevée aux mises à jour urgentes, telles que la progression de la diffusion, le statut de la commande ou les scores de sport en direct.
* **Prise en charge des mises à jour fréquentes** : incluez `NSSupportsLiveActivitiesFrequentUpdates` dans le `Info.plist` de votre application et définissez-le sur **OUI** si vous avez besoin de mises à jour fréquentes.

+++

### Questions des spécialistes marketing

+++Puis-je personnaliser le contenu de l’activité en direct pour chaque utilisateur dans une campagne de diffusion ?

Les campagnes de diffusion envoient le même contenu à tous les utilisateurs et à toutes utilisatrices de l’audience. Pour personnaliser le contenu, utilisez des campagnes unitaires (transactionnelles) qui ciblent des utilisateurs et utilisatrices spécifiques.
+++

+++Comment savoir si mon activité Live a bien été diffusée ?

[Surveillez vos analyses de campagne](../reports/campaign-global-report-cja-activity.md) dans Adobe Journey Optimizer. Vous pouvez effectuer le suivi des taux de diffusion, des échecs et des mesures d’engagement. Pensez également à implémenter des événements d’analyse personnalisés dans votre application.
+++

+++Puis-je planifier une activité en direct à l’avance ?

L’appel API déclenche immédiatement l’activité Live . Cependant, vous pouvez planifier vos appels API par l’intermédiaire de vos systèmes back-end ou utiliser les fonctionnalités d’orchestration de Journey Optimizer pour les déclencher au moment approprié.
+++

+++Que se passe-t-il si j’envoie un événement « start » pour une activité Live qui existe déjà ?

Lors du démarrage à distance d’une activité Live via les API d’exécution d’Adobe :

* Vous pouvez inclure un en-tête `x-request-id` dans votre requête. Idéalement, chaque `liveActivityID` devrait être associé à un seul `x-request-id`. Cela permet de s’assurer que si plusieurs demandes sont effectuées avec la même combinaison de `x-request-id` et de `liveActivityID`, une seule instance d’activité active sera démarrée sur l’appareil et les demandes en double seront ignorées.

* Si l’en-tête `x-request-id` est omis, chaque demande est traitée indépendamment, ce qui peut entraîner la création de plusieurs instances d’activité Dynamique avec le même `liveActivityID`. Dans ce cas, les futures mises à jour peuvent échouer ou ne s’appliquer qu’à une seule instance active.

* La valeur `x-request-id` ne doit pas être réutilisée pour différents `liveActivityIDs` dans des requêtes d’API distinctes.

+++

+++Puis-je tester différentes expériences d’activité en direct ?

Oui. Créez plusieurs campagnes avec différentes structures de contenu et utilisez les fonctionnalités d’expérimentation d’Adobe Journey Optimizer pour tester celle qui fonctionne le mieux. Assurez-vous que votre application prend en charge toutes les variations d’état du contenu.

+++

+++À quelle fréquence dois-je mettre à jour une activité Live ?

Mettez-la à jour uniquement lors de changements significatifs des informations, car des mises à jour trop fréquentes peuvent vider la batterie et réduire la qualité de l’expérience client. Pour les scénarios en temps réel, tels que le suivi des diffusions, une fréquence de 30 à 60 secondes est généralement suffisante. Pour du contenu dont les informations changent peu, comme les scores sportifs, effectuez uniquement les mises à jour lors d’événements importants.

+++

+++Puis-je cibler les utilisateurs en fonction de l’activation ou non de l’activité Live ?

Vous devrez travailler avec votre équipe de développement pour suivre et transmettre cette préférence à Adobe Experience Platform en tant qu’attribut utilisateur, puis segmenter en fonction de cet attribut.

+++

### Questions relatives à l’API

+++Quelle est la différence entre `timestamp` et `dismissal-date` ?

* `timestamp` : époque actuelle à laquelle l’événement se produit, requise pour tous les événements.
* `dismissal-date` : une période ultérieure où l’activité Live doit automatiquement être ignorée, obligatoire uniquement pour les événements de « fin ».

+++

+++Dois-je envoyer tous les champs `attributes` à chaque appel de mise à jour ?

Oui, en fonction de votre classe `LiveActivityAttribute`.

* Tous les champs de votre objet d’attributs, y compris `liveActivityData`, doivent être inclus dans chaque appel, pour le démarrage, les mises à jour ou l’arrêt.
* Seuls les champs `content-state` représentent ce qui change dynamiquement sur une activité en direct en cours d’exécution.
* Ajoutez également un objet d’alerte pour vous assurer que la notification push soit visible par l’utilisateur ou l’utilisatrice, et qu’elle ne reste pas silencieuse en arrière-plan. Obligatoire uniquement pour les cas de démarrage.

+++

+++Quel format les horodatages d’époque doivent-ils avoir ?

Utilisez l’horodatage d’époque Unix en **secondes** et non en millisecondes. Par exemple : `1759937682`

+++

+++Puis-je utiliser le même `requestId` pour plusieurs appels API ?

Non. Chaque requête d’API doit comporter un `requestId` unique pour garantir l’idempotence et un suivi approprié. Utilisez des UUID ou des identifiants uniques similaires.

+++

+++Quelle authentification faut-il utiliser pour l’API Headless ?

Reportez-vous à la [documentation sur les campagnes déclenchées par API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) pour connaître les exigences d’authentification, y compris les jetons OAuth et les clés d’API.

+++

+++Que se passe-t-il si mon appel API échoue ?

Implémentez une logique de nouvelle tentative avec un intervalle exponentiel. Recherchez des codes d’erreur et des messages dans la réponse de l’API pour diagnostiquer les problèmes. Les échecs sont généralement dus à des ID de campagne non valides, à des payloads incorrectes ou à des problèmes d’authentification.

+++

+++Puis-je envoyer des mises à jour d’activité en direct depuis mes propres serveurs principaux ?

Oui, c’est le fonctionnement normal attendu. Votre serveur principal appelle l’API Adobe Journey Optimizer Headless pour déclencher des événements d’activité en direct lorsque la logique commerciale l’exige.

+++

+++Dois-je utiliser des campagnes distinctes pour les événements de démarrage, de mise à jour et d’arrêt ?

Non. Vous pouvez utiliser la même campagne et modifier le champ `event` dans la payload. Cependant, certaines organisations préfèrent utiliser des campagnes distinctes pour un meilleur suivi analytics.

+++

### Questions relatives au dépannage

+++Mon activité Live démarre mais ne se met pas à jour. Quel peut être le problème ?

Causes fréquentes :

* `liveActivityID` ou `channelID` ne correspondent pas entre les appels de démarrage et de mise à jour.
* Les champs `content-state` ne correspondent pas votre structure `ContentState`.
* L&#39;activité Live est déjà terminée.
* Problèmes de connectivité réseau sur l’appareil.
* L’heure d’époque utilisée comme horodatage n’est pas à jour.

+++

+++Le champ `attributes-type` n’est pas reconnu. Que dois-je faire ?

* Vérifiez que le nom de la classe correspond **exactement** (sensible à la casse) à votre nom de structure Swift.
* Vérifiez que la structure est correctement définie et enregistrée.
* Vérifiez qu’il n’y a pas de faute de frappe dans la payload JSON.
* Vérifiez que la version de l’application installée dispose de l’implémentation de l’activité en direct.

+++

+++Les utilisateurs voient uniquement la mise à jour de l’activité en direct et non la notification d’alerte. S’agit-il d’un problème connu ?

Non. Le champ `alert` est facultatif et peut être supprimé par iOS dans certaines conditions, par exemple en mode Ne pas déranger. L’activité en direct peut se mettre à jour en silence, ce qui correspond souvent au comportement prévu. Le champ d’alerte est obligatoire pour envoyer des commandes de démarrage à distance, sinon Apple le traite comme une notification silencieuse en arrière-plan.

+++

+++Puis-je supprimer ou effacer toutes les instances d’activité dynamiques d’un utilisateur ?

Vous devez envoyer un événement « end » pour chaque instance d’activité active Live. Effectuez le suivi des instances d’activité dynamiques actives pour chaque utilisateur de vos systèmes afin de pouvoir les nettoyer correctement.

+++

+++Mon widget affiche « Aucune donnée » même si j’ai envoyé une mise à jour. Quel peut être le problème ?

* Vérifiez que l’implémentation de votre widget accède correctement au `context.state` et aux `context.attributes`.
* Vérifiez que les valeurs par défaut ou les états d’erreur sont gérés dans l’interface de votre widget.
* Utilisez le protocole `LiveActivityAssuranceDebuggable` pour déboguer le schéma.
* Vérifiez que les données sont bien reçues en effectuant un test avec Adobe Assurance.
+++
