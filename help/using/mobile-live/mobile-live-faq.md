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
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: ht
source-wordcount: '1603'
ht-degree: 100%

---

# Questions fréquentes {#mobile-live-faq}

>[!BEGINSHADEBOX]

* [Commencer avec les activités en direct](get-started-mobile-live.md)
* [Configuration des activités en direct](mobile-live-configuration.md)
* [Intégration des activités en direct au SDK mobile Adobe Experience Platform](mobile-live-configuration-sdk.md)
* [Créer une activité en direct](create-mobile-live.md)
* **[Questions fréquentes](mobile-live-faq.md)**
* [Rapport de campagne d’activités en direct](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

## Questions générales

+++Quelle est la différence entre une activité en direct et une notification push ?

Les activités en direct fournissent des mises à jour persistantes en temps réel sur l’écran de verrouillage et Dynamic Island sans que les utilisateurs et utilisatrices aient à déverrouiller leur appareil. Les notifications push sont des alertes temporaires qui disparaissent une fois ignorées. Les activités en direct restent visibles et peuvent être mises à jour plusieurs fois jusqu’à ce qu’elles soient explicitement terminées.

+++

+++Combien d’activités en direct peuvent être actives à la fois ?

Une application iOS peut exécuter plusieurs activités en direct simultanément, y compris plusieurs qui utilisent le même type `ActivityAttributes`.

Les développeurs et développeuses n’imposent aucune limite stricte sur le nombre d’activités en direct pouvant exister pour un type d’attribut donné. Vous pouvez en démarrer autant que le nécessite la logique de votre application, par exemple, une par diffusion ou trajet en cours. Cependant, iOS applique une limite au niveau du système sur le nombre d’activités en direct pouvant être actives ou visibles à la fois.

En pratique :

* iOS prend généralement en charge jusqu’à environ cinq activités en direct simultanées par application.

* Si vous dépassez ce nombre, le système peut arrêter l’affichage de certaines activités ou terminer les activités plus anciennes pour économiser des ressources.

* Chaque activité active possède une `Activity.id` unique, ce qui vous permet de la mettre à jour ou de la terminer individuellement.

+++

+++L’application doit-elle être ouverte pour que les utilisateurs et utilisatrices puissent recevoir les mises à jour des activités en direct ?

Non. Les activités en direct peuvent être démarrées, mises à jour et terminées à distance, même lorsque l’application est complètement fermée. Il s’agit de l’un des principaux avantages de la fonctionnalité.

+++

+++Quelles versions d’iOS prennent en charge les activités en direct ?

* iOS 16.1+ : prise en charge de base des activités en direct
* iOS 17.2+ : fonctionnalité de démarrage par notification push (démarrage à distance sans ouverture de l’application)
* iOS 18+ : prise en charge des canaux de diffusion pour les activités en direct basées sur l’audience
+++

+++Pendant combien de temps une activité en direct peut-elle rester active ?

Apple limite les activités en direct à **8 heures de mises à jour actives**. Ensuite, le système met automatiquement fin à l’activité, bien qu’elle puisse rester visible dans un état statique pendant **12 heures supplémentaires au maximum** avant d’être supprimée. Vous pouvez également terminer une activité en direct plus tôt en définissant une `dismissalDate` ou en appelant explicitement `activity.end()` dans votre application.

+++

### Questions des développeurs et développeuses

+++Dois-je créer une extension de widget distincte pour les activités en direct ?

Oui. Les activités en direct s’affichent via WidgetKit. Vous devez donc créer une extension de widget dans votre projet Xcode et implémenter la `ActivityConfiguration`.
[En savoir plus sur la configuration des widgets](mobile-live-configuration-sdk.md)

+++

+++Puis-je utiliser la même classe `LiveActivityAttributes` pour les activités dynamiques locales et distantes ?

Oui. La même classe d’attributs fonctionne pour les activités en direct démarrées localement et à distance (démarrage par notification push). Vous devez vous assurer de l’enregistrer avec `Messaging.registerLiveActivity()`.

+++

+++Que se passe-t-il si j’envoie une mise à jour pour une activité en direct qui n’existe pas ?

Si vous envoyez un événement de mise à jour ou de fin pour un `liveActivityID` ou un `channelID` inexistant, la requête échoue silencieusement sur l’appareil. Assurez-vous toujours de suivre les activités en direct actives pour chaque utilisateur et utilisatrice.

+++

+++Puis-je tester des activités en direct dans le simulateur iOS ?

Oui, vous pouvez tester les activités en direct démarrées localement et à distance dans le simulateur iOS.

* **Local** : cela inclut la création, la mise à jour et l’envoi d’activités en direct directement depuis votre application à l’aide des **API ActivityKit**.

* **Distant** : pour tester à distance la fonctionnalité d’activité en direct, intégrez notre SDK de messagerie à votre application et utilisez les API d’exécution fournies pour envoyer à distance des commandes de démarrage, de mise à jour et d’arrêt à votre appareil de test ou votre simulateur iOS. Comme pour les notifications push, qui peuvent actuellement être testées avec l’intégration des SDK Adobe.

+++

+++Comment gérer les mises à jour lorsque l’application fonctionne en arrière-plan ?

Le SDK gère cela automatiquement. Une fois enregistrées, les activités en direct reçoivent des mises à jour même lorsque l’application est arrêtée. Aucun mode d’arrière-plan supplémentaire n’est requis.
+++

+++Quelle est la différence entre `liveActivityID` et `channelID` ?

* `liveActivityID` : utilisé pour les activités en direct individuelles (unitaires) ciblant des utilisateurs et utilisatrices spécifiques. Chaque ID représente une instance d’activité en direct unique.
* `channelID` : utilisé pour diffuser des activités en direct envoyées à des audiences. Tous les utilisateurs et toutes les utilisatrices d’une audience reçoivent les mêmes mises à jour sur le même canal.
+++

+++Puis-je personnaliser l’aspect de la Dynamic Island séparément de l’écran de verrouillage ?

Oui. Le `ActivityConfiguration` dispose de fermetures distinctes pour le contenu de l’écran de verrouillage et celui de la Dynamic Island (états développé, compact et minimal), chaque conception étant indépendante.
+++

+++Dois-je stocker manuellement les jetons push ?

Non. Lorsque vous enregistrez un type d’activité en direct avec `Messaging.registerLiveActivity()`, le SDK collecte et gère automatiquement les jetons push.
+++

### Questions des spécialistes marketing

+++Puis-je personnaliser le contenu de l’activité en direct pour chaque utilisateur et utilisatrice dans une campagne de diffusion ?

Les campagnes de diffusion envoient le même contenu à tous les utilisateurs et à toutes utilisatrices de l’audience. Pour personnaliser le contenu, utilisez des campagnes unitaires (transactionnelles) qui ciblent des utilisateurs et utilisatrices spécifiques.
+++

+++Comment puis-je savoir si mon activité en direct a bien été diffusée ?

[Surveillez vos analyses de campagne](../reports/campaign-global-report-cja-activity.md) dans Adobe Journey Optimizer. Vous pouvez effectuer le suivi des taux de diffusion, des échecs et des mesures d’engagement. Pensez également à implémenter des événements d’analyse personnalisés dans votre application.
+++

+++Puis-je planifier des activités en direct à l’avance ?

L’appel API déclenche immédiatement l’activité en direct. Cependant, vous pouvez planifier vos appels API par l’intermédiaire de vos systèmes back-end ou utiliser les fonctionnalités d’orchestration de Journey Optimizer pour les déclencher au moment approprié.
+++

+++Que se passe-t-il si j’envoie un événement de démarrage pour une activité en direct qui existe déjà ?

Lorsque vous démarrez à distance des activités en direct via les API d’exécution d’Adobe :

* Vous pouvez inclure un en-tête `x-request-id` dans votre requête. Idéalement, chaque `liveActivityID` devrait être associé à un seul `x-request-id`. Ainsi, si plusieurs requêtes sont effectuées avec la même combinaison de `x-request-id` et `liveActivityID`, une seule activité en direct démarrera sur l’appareil et les requêtes en double seront ignorées.

* Si vous n’incluez pas l’en-tête `x-request-id`, chaque requête est traitée indépendamment, ce qui peut entraîner la création de plusieurs activités en direct avec le même `liveActivityID`. Dans ce cas, les futures mises à jour peuvent échouer ou ne s’appliquer qu’à une seule instance active.

* La valeur `x-request-id` ne doit pas être réutilisée pour différents `liveActivityIDs` dans des requêtes d’API distinctes.

+++

+++Puis-je réaliser un test A/B avec différentes expériences d’activité en direct ?

Oui. Créez plusieurs campagnes avec différentes structures de contenu et utilisez les fonctionnalités d’expérimentation d’Adobe Journey Optimizer pour tester celle qui fonctionne le mieux. Assurez-vous que votre application prend en charge toutes les variations d’état du contenu.

+++

+++À quelle fréquence dois-je mettre à jour une activité en direct ?

Mettez-la à jour uniquement lors de changements significatifs des informations, car des mises à jour trop fréquentes peuvent vider la batterie et réduire la qualité de l’expérience client. Pour les scénarios en temps réel, tels que le suivi des diffusions, une fréquence de 30 à 60 secondes est généralement suffisante. Pour du contenu dont les informations changent peu, comme les scores sportifs, effectuez uniquement les mises à jour lors d’événements importants.

+++

+++Puis-je cibler les utilisateurs et utilisatrices selon qu’ils ont activé ou non les activités en direct ?

Vous devrez travailler avec votre équipe de développement pour suivre et transmettre cette préférence à Adobe Experience Platform en tant qu’attribut utilisateur, puis segmenter en fonction de cet attribut.

+++

### Questions relatives à l’API

+++Quelle est la différence entre `timestamp` et `dismissal-date` ?

* `timestamp` : époque actuelle à laquelle l’événement se produit, requise pour tous les événements.
* `dismissal-date` : époque ultérieure à laquelle l’activité en direct doit être automatiquement ignorée, requise uniquement pour les événements d’arrêt.

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

+++Puis-je envoyer des mises à jour d’activité en direct depuis mes propres serveurs back-end ?

Oui, c’est le fonctionnement normal attendu. Votre système back-end appelle l’API Headless Adobe Journey Optimizer pour déclencher des événements d’activité en direct lorsque la logique métier l’exige.

+++

+++Dois-je utiliser des campagnes distinctes pour les événements de démarrage, de mise à jour et d’arrêt ?

Non. Vous pouvez utiliser la même campagne et modifier le champ `event` dans la payload. Cependant, certaines organisations préfèrent utiliser des campagnes distinctes pour un meilleur suivi analytics.

+++

### Questions relatives au dépannage

+++Mon activité en direct démarre, mais ne se met pas à jour. Quel peut être le problème ?

Causes fréquentes :

* `liveActivityID` ou `channelID` ne correspondent pas entre les appels de démarrage et de mise à jour.
* Les champs `content-state` ne correspondent pas votre structure `ContentState`.
* L’activité en direct est déjà terminée.
* Problèmes de connectivité réseau sur l’appareil.

+++

+++Le champ `attributes-type` n’est pas reconnu. Que dois-je faire ?

* Vérifiez que le nom de la classe correspond **exactement** (sensible à la casse) à votre nom de structure Swift.
* Vérifiez que la structure est correctement définie et enregistrée.
* Vérifiez qu’il n’y a pas de faute de frappe dans la payload JSON.
* Vérifiez que la version de l’application installée dispose de l’implémentation de l’activité en direct.

+++

+++Les utilisateurs et utilisatrices voient uniquement la mise à jour de l’activité en direct et non la notification d’alerte. S’agit-il d’un problème connu ?

Non. Le champ `alert` est facultatif et peut être supprimé par iOS dans certaines conditions, par exemple en mode Ne pas déranger. Les activités en direct peuvent être mises à jour de manière silencieuse, ce qui correspond souvent au comportement attendu. Le champ d’alerte est obligatoire pour envoyer des commandes de démarrage à distance, sinon Apple le traite comme une notification silencieuse en arrière-plan.

+++

+++Puis-je supprimer toutes les activités en direct d’un utilisateur ou d’une utilisatrice ?

Vous devez envoyer un événement d’arrêt pour chaque activité en direct. Suivez les activités en direct actives de chaque utilisateur et utilisatrice de vos systèmes afin de les supprimer correctement.

+++

+++Mon widget affiche « Aucune donnée » même si j’ai envoyé une mise à jour. Quel peut être le problème ?

* Vérifiez que l’implémentation de votre widget accède correctement au `context.state` et aux `context.attributes`.
* Vérifiez que les valeurs par défaut ou les états d’erreur sont gérés dans l’interface de votre widget.
* Utilisez le protocole `LiveActivityAssuranceDebuggable` pour déboguer le schéma.
* Vérifiez que les données sont bien reçues en effectuant un test avec Adobe Assurance.
+++
