---
solution: Journey Optimizer
product: journey optimizer
title: Questions fréquentes
description: FAQ sur les activités en direct
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '1603'
ht-degree: 1%

---

# Questions fréquentes {#mobile-live-faq}

>[!BEGINSHADEBOX]

* [Prise en main de l’activité Live](get-started-mobile-live.md)
* [Configuration de l’activité en direct](mobile-live-configuration.md)
* [Intégration d’une activité en direct à Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)
* [Créer une activité Live](create-mobile-live.md)
* **[Questions fréquentes](mobile-live-faq.md)**
* [Rapport de campagne d’activité dynamique](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

## Questions générales

+++Quelle est la différence entre une activité en direct et une notification push ?

Les activités en direct fournissent des mises à jour persistantes en temps réel sur l’écran de verrouillage et l’île dynamique sans que les utilisateurs aient à déverrouiller leur appareil. Les notifications push sont des alertes temporaires qui disparaissent une fois ignorées. Les activités en direct restent visibles et peuvent être mises à jour plusieurs fois jusqu’à ce qu’elles soient explicitement terminées.

+++

+++Combien d’activités en direct peuvent être actives à la fois ?

Une application iOS peut exécuter plusieurs activités dynamiques simultanément, y compris plusieurs qui utilisent le même type d’`ActivityAttributes`.

Les développeurs n’imposent aucune limite stricte sur le nombre d’activités en direct pouvant exister pour un type d’attribut donné. Vous pouvez démarrer autant de programmes que le nécessite votre logique d’application, par exemple, un par diffusion ou parcours en cours. Cependant, iOS applique une limite au niveau du système sur le nombre d’activités dynamiques pouvant être actives ou visibles à la fois.

En pratique :

* iOS prend généralement en charge jusqu’à environ cinq activités en direct simultanées par application.

* Si vous dépassez ce nombre, le système peut arrêter l’affichage de certaines activités ou arrêter les activités plus anciennes pour économiser des ressources.

* Chaque activité active possède un `Activity.id` unique, ce qui vous permet de la mettre à jour ou de la terminer individuellement.

+++

+++L’application doit-elle être ouverte pour que les utilisateurs puissent recevoir les mises à jour des activités en direct ?

Non. Les activités en direct peuvent être démarrées, mises à jour et terminées à distance, même lorsque l’application est complètement fermée. Il s’agit de l’un des principaux avantages de la fonctionnalité.

+++

+++Quelles versions d’iOS prennent en charge les activités en direct ?

* iOS 16.1+ : prise en charge de base des activités en direct
* iOS 17.2+ : fonctionnalité de démarrage par notification push (démarrage à distance sans ouverture de l’application)
* iOS 18+ : prise en charge des canaux de diffusion pour les activités en direct basées sur l’audience
+++

+++Pendant combien de temps une activité en direct peut-elle rester active ?

Apple limite les activités en direct à **8 heures de mises à jour actives**. Ensuite, le système met automatiquement fin à l’activité, bien qu’elle puisse rester visible dans un état statique pendant 12 heures supplémentaires au maximum **&#x200B;**&#x200B;avant d’être supprimée. Vous pouvez également terminer une activité active plus tôt en définissant un `dismissalDate` ou en appelant explicitement `activity.end()` dans votre application.

+++

### Questions du développeur

+++Dois-je créer une extension de widget distincte pour les activités en direct ?

Oui. Les activités en direct s’affichent via WidgetKit. Vous devez donc créer une extension de widget dans votre projet Xcode et implémenter le `ActivityConfiguration`.
[En savoir plus sur la configuration du widget](mobile-live-configuration-sdk.md)

+++

+++Puis-je utiliser la même classe `LiveActivityAttributes` pour les activités en direct locales et distantes ?

Oui. La même classe d’attributs fonctionne pour les activités en direct démarrées localement et à distance (push-to-start). Vous devez vous assurer de l’enregistrer auprès de `Messaging.registerLiveActivity()`.

+++

+++Que se passe-t-il si j’envoie une mise à jour pour une activité active qui n’existe pas ?

Si vous envoyez un événement de mise à jour ou de fin pour un `liveActivityID` ou un `channelID` inexistant, la requête échoue silencieusement sur l’appareil. Assurez-vous toujours de suivre les activités en direct actives pour chaque utilisateur.

+++

+++Puis-je tester des activités en direct dans le simulateur iOS ?

Oui, vous pouvez tester les activités en direct démarrées localement et à distance dans le simulateur iOS.

* **Local** : cela inclut la création, la mise à jour et l’envoi d’activités en direct directement depuis votre application à l’aide des API **ActivityKit**.

* **Distant** : pour tester à distance la fonctionnalité d’activité en direct, intégrez notre SDK de messagerie à votre application et utilisez les API d’exécution fournies pour envoyer à distance le démarrage, la mise à jour et l’arrêt de votre appareil de test ou de votre simulateur iOS. De la même manière que les notifications push peuvent être testées actuellement avec l&#39;intégration des SDK Adobe.

+++

+++Comment gérer les mises à jour lorsque l’application est en arrière-plan ?

Le SDK gère cela automatiquement. Une fois enregistrées, les activités en direct reçoivent des mises à jour même lorsque l’application est arrêtée. Aucun mode d’arrière-plan supplémentaire n’est requis.
+++

+++Quelle est la différence entre `liveActivityID` et `channelID` ?

* `liveActivityID` : utilisé pour les activités en direct individuelles (unitaires) ciblant des utilisateurs spécifiques. Chaque identifiant représente une instance d’activité dynamique unique.
* `channelID` : utilisé pour diffuser des activités en direct envoyées aux audiences. Tous les utilisateurs et utilisatrices de l’audience reçoivent les mêmes mises à jour sur le même canal.
+++

+++Puis-je personnaliser l’aspect de l’îlot dynamique séparément de l’écran de verrouillage ?

Oui. Le `ActivityConfiguration` dispose de fermetures distinctes pour le contenu Verrouiller l’écran et le contenu Dynamic Island (états développé, compact et minimal), chaque conception étant indépendante.
+++

+++Dois-je stocker manuellement les jetons push ?

Non. Lorsque vous enregistrez un type d’activité en direct avec `Messaging.registerLiveActivity()`, SDK collecte et gère automatiquement les jetons push pour vous.
+++

### Questions du spécialiste marketing

+++Puis-je personnaliser le contenu de l’activité en direct pour chaque utilisateur dans une campagne de diffusion ?

Les campagnes de diffusion envoient le même contenu à tous les utilisateurs de l’audience. Pour le contenu personnalisé, utilisez des campagnes unitaires (transactionnelles) ciblant des utilisateurs individuels.
+++

+++Comment savoir si mon activité en direct a bien été diffusée ?

[Surveillez vos analyses de campagne](../reports/campaign-global-report-cja-activity.md) dans Adobe Journey Optimizer. Vous pouvez effectuer le suivi des taux de diffusion, des échecs et des mesures d’engagement. Pensez également à implémenter des événements d’analyse personnalisés dans votre application.
+++

+++Puis-je planifier des activités en direct à l’avance ?

L’appel API déclenche immédiatement l’activité dynamique. Cependant, vous pouvez planifier vos appels API par l’intermédiaire de vos systèmes principaux ou utiliser les fonctionnalités d’orchestration de Journey Optimizer pour les horodater de manière appropriée.
+++

+++Que se passe-t-il si j’envoie un événement « start » pour une activité active qui existe déjà ?

Lors du démarrage à distance d’activités en direct via les API d’exécution d’Adobe :

* Vous pouvez inclure un en-tête `x-request-id` dans votre requête. Idéalement, il devrait y avoir une relation un-à-un entre chaque `liveActivityID` et son `x-request-id` correspondant. Ainsi, si plusieurs demandes sont effectuées avec la même combinaison de `x-request-id` et de `liveActivityID`, une seule activité active sera démarrée sur l’appareil et les demandes en double seront ignorées.

* Si l’en-tête `x-request-id` est omis, chaque demande est traitée indépendamment, ce qui peut entraîner la création de plusieurs activités en direct avec la même `liveActivityID`. Dans ce cas, les futures mises à jour peuvent échouer ou ne s’appliquer qu’à une seule des instances actives.

* La valeur `x-request-id` ne doit pas être réutilisée sur différentes `liveActivityIDs` dans des requêtes d’API distinctes.

+++

+++Puis-je tester différentes expériences d’activité en direct ?

Oui. Créez plusieurs campagnes avec différentes structures de contenu et utilisez les fonctionnalités d’expérimentation de Adobe Journey Optimizer pour tester celle qui fonctionne le mieux. Assurez-vous que votre application prend en charge toutes les variations d’état du contenu.

+++

+++À quelle fréquence dois-je mettre à jour une activité active ?

Mettez à jour uniquement lorsque des informations significatives changent, car des mises à jour trop fréquentes peuvent vidanger la batterie et réduire la qualité de l’expérience utilisateur. Pour les scénarios en temps réel, tels que le suivi des diffusions, une fréquence de 30 à 60 secondes est généralement acceptable. Pour le contenu qui change plus lentement, comme les scores de sport, mettez à jour uniquement les événements significatifs.

+++

+++Puis-je cibler les utilisateurs en fonction de l’activation ou non des activités en direct ?

Vous devrez travailler avec votre équipe de développement pour suivre et transmettre cette préférence à Adobe Experience Platform en tant qu’attribut utilisateur, puis segmenter en fonction de cet attribut.

+++

### Questions relatives à l’API

+++Quelle est la différence entre `timestamp` et `dismissal-date` ?

* `timestamp` : heure actuelle de l’époque à laquelle l’événement se produit, requise pour tous les événements.
* `dismissal-date` : une période ultérieure où l’activité dynamique doit être automatiquement ignorée, obligatoire uniquement pour les événements de « fin ».

+++

+++Dois-je envoyer tous les champs `attributes` à chaque appel de mise à jour ?

Oui, en fonction de votre classe `LiveActivityAttribute`.

* Tous les champs de votre objet d’attributs, y compris `liveActivityData`, doivent être inclus dans chaque appel, pour le début, les mises à jour ou la fin.
* Seuls les champs `content-state` représentent ce qui change réellement dynamiquement sur une activité active en cours d’exécution.
* Ajoutez également un objet d’alerte pour vous assurer que la notification push est traitée comme une notification visible par l’utilisateur, et non comme une notification en arrière-plan silencieuse. Obligatoire uniquement pour les cas de « début » et facultatif.

+++

+++Dans quel format les horodatages epoch doivent-ils être ?

Utilisez le temps Unix epoch en **secondes** et non en millisecondes. Par exemple : `1759937682`

+++

+++Puis-je utiliser le même `requestId` pour plusieurs appels API ?

Non. Chaque requête d’API doit comporter un `requestId` unique pour garantir l’idempotence et le suivi approprié. Utilisez des UUID ou des identifiants uniques similaires.

+++

+++Quelle authentification est requise pour l’API Headless ?

Reportez-vous à la [Documentation sur les campagnes déclenchées par API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/) pour connaître les exigences d’authentification, y compris les jetons OAuth et les clés API.

+++

+++Que se passe-t-il si mon appel API échoue ?

Implémentez la logique de reprise avec une interruption exponentielle. Recherchez des codes d’erreur et des messages dans la réponse de l’API pour diagnostiquer les problèmes. Les échecs courants incluent les identifiants de campagne non valides, les payloads incorrects ou les problèmes d’authentification.

+++

+++Puis-je envoyer des mises à jour d’activité en direct depuis mes propres serveurs principaux ?

Oui, c&#39;est le comportement prévu. Votre serveur principal appelle l’API Adobe Journey Optimizer Headless pour déclencher des événements Live Activity lorsque la logique commerciale l’exige.

+++

+++Ai-je besoin d’une campagne différente pour les événements de début, de mise à jour et de fin ?

Non. Vous pouvez utiliser la même campagne et modifier le champ `event` dans la payload. Cependant, certaines organisations préfèrent des campagnes distinctes pour un meilleur suivi Analytics.

+++

### Résolution des questions

+++Mon activité Live démarre mais ne se met pas à jour. Quel pourrait être le problème ?

Causes fréquentes :

* `liveActivityID` ou `channelID` incohérents entre les appels de démarrage et de mise à jour.
* `content-state` champs ne correspondent pas à votre structure de `ContentState`.
* L’activité Live est déjà terminée.
* Problèmes de connectivité réseau sur l’appareil.

+++

+++Le champ `attributes-type` n&#39;est pas reconnu. Que dois-je vérifier ?

* Assurez-vous que le nom de la classe correspond **exactement** (sensible à la casse) à votre nom de structure Swift
* Vérifiez que le struct est correctement défini et enregistré
* Rechercher les fautes de frappe dans la payload JSON
* Vérifiez que la version d’application installée dispose de la mise en œuvre Live Activity .

+++

+++Les utilisateurs voient uniquement la mise à jour de l’activité active et non la notification d’alerte. S’agit-il d’un problème connu ?

Non. Le champ `alert` est facultatif et peut être supprimé par iOS dans certaines conditions, par exemple en mode Ne pas déranger . Les activités en direct peuvent être mises à jour en silence, ce qui correspond souvent au comportement prévu. Le champ d’alerte est obligatoire pour l’envoi de démarrages distants, sinon Apple le traite comme une notification en arrière-plan silencieuse.

+++

+++Puis-je supprimer ou effacer toutes les activités dynamiques d’un utilisateur ?

Vous devez envoyer un événement de « fin » pour chaque activité active en direct. Suivez les activités actives de chaque utilisateur de vos systèmes afin de pouvoir les nettoyer correctement.

+++

+++Mon widget affiche « Aucune donnée » même si j’ai envoyé une mise à jour. Quel pourrait être le problème ?

* Vérifiez que l’implémentation de votre widget accède correctement aux `context.state` et aux `context.attributes`.
* Vérifiez que les valeurs par défaut ou les états d’erreur sont gérés dans votre interface de widget.
* Utilisez le protocole `LiveActivityAssuranceDebuggable` pour déboguer le schéma.
* Testez avec Adobe Assurance pour voir si des données sont reçues.
+++
