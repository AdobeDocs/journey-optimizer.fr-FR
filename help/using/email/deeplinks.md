---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser et configurer des liens profonds dans les e-mails et les SMS
description: Découvrez comment ajouter des liens profonds au contenu des e-mails et des SMS et comment implémenter la gestion des liens profonds dans les applications iOS et Android.
feature: Email, SMS
topic: Content Management
role: User, Developer
level: Intermediate
keywords: lien profond, lien profond, liens universels, liens d’application, e-mail, sms
source-git-commit: a3b48494fe64842121c5c3711cdd7117b30747a4
workflow-type: tm+mt
source-wordcount: '1327'
ht-degree: 1%

---


# Utiliser et configurer des liens profonds dans les e-mails et les SMS {#deeplinks}

Les liens profonds vous permettent d’orienter les destinataires d’un e-mail ou d’un SMS vers un écran ou un contenu spécifique dans votre application mobile. Cela permet d’amener les personnes directement à l’expérience in-app prévue, sans les acheminer via un navigateur web ou une boutique d’applications, de sorte que le parcours reste pertinent et intégré à la marque.

Lorsque vos destinataires cliquent sur le lien profond, ils sont redirigés directement vers le contenu in-app prévu, **à condition que vous ayez terminé** :

* les [&#x200B; étapes de configuration &#x200B;](#configuration) dans Journey Optimizer ;

* les étapes [mise en œuvre de l’application mobile](#mobile-implementation) pour iOS et Android dans votre application mobile.

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer] prend en charge les liens profonds pour iOS et Android à l’aide d’URL suivies (`/ee/v1/mclick/*`) afin d’assurer la compatibilité et le suivi des clics.

## Création de liens profonds {#authoring}

>[!CAUTION]
>
>Les liens profonds ne fonctionneront pas tant que vous n’aurez pas terminé les étapes [configuration](#configuration) et [implémentation de l’application mobile](#mobile-implementation) sur cette page.

### Email {#authoring-email}

Pour les e-mails , vous disposez de deux options pour insérer un lien profond :

* **Email Designer** : assurez-vous que [le suivi des liens est activé](message-tracking.md#enable-tracking). Sélectionnez l’élément à lier (texte, bouton ou image), cliquez sur **[!UICONTROL Insérer un lien]** dans la barre d’outils contextuelle, puis choisissez **[!UICONTROL Lien profond]** pour saisir l’URL de votre lien profond. [En savoir plus sur l&#39;insertion de liens](message-tracking.md#insert-links)

* **Éditeur Personalization (code)** : insérez le lien profond directement dans HTML à l&#39;aide du fragment de code suivant :

  ```html
  <a class="arc-link" data-nl-type="DEEPLINK" href="<<deeplink_url>>" id="acr-link-7821368" style="text-decoration:underline;" target="_blank" data-tracking-type="DEEPLINK">Click Here</a>
  ```

  Remplacez `<<deeplink_url>>` par l’URL de votre lien profond et utilisez un `id` unique pour chaque bloc afin d’éviter les conflits.

### SMS {#authoring-sms}

Pour les SMS, les liens profonds sont créés à l’aide de la fonction d’assistance **Url** de l’éditeur de personnalisation. Pour en savoir plus sur l’ajout de liens à du contenu SMS, consultez [cette section](../mobile/design-mobile.md#sms-content).

Pour insérer des liens profonds dans le contenu d&#39;un SMS, utilisez la syntaxe suivante :

```
{{url originalUrl='<<url>>' type='DEEPLINK' action='CLICK'}}
```

Remplacez `<<url>>` par l’URL réelle du lien profond.

## Configuration dans Journey Optimizer {#configuration}

Pour pouvoir utiliser des liens profonds dans les e-mails et les SMS pour vos applications mobiles, procédez comme suit.

>[!NOTE]
>
>Cette section s’applique lorsque vous utilisez **liens universels (iOS)** et **liens d’application (Android)** (liens profonds basés sur HTTPS).

1. Dans Journey Optimizer, déléguez le sous-domaine dans lequel la liaison profonde est activée. [En savoir plus](../configuration/delegate-subdomain.md)

1. Hébergez le fichier AASA pour iOS et le fichier assetLinks.json pour Android sur votre sous-domaine. Contactez l’[Assistance clientèle d’](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} ou votre représentant Adobe en indiquant les détails ci-dessous :

   * **Pour iOS (AASA)** :
      * Sous-domaine délégué
      * ID de bundle de l&#39;application
   * **Pour Android (assetLinks.json)** :
      * Sous-domaine délégué
      * ID de bundle de l&#39;application
      * Empreinte du certificat SHA-256

>[!IMPORTANT]
>
>Les liens profonds via l’infrastructure Adobe s’appliquent lorsque le suivi des liens est activé pour votre message, dans les paramètres [&#x200B; suivi des e-mails &#x200B;](message-tracking.md#enable-tracking) ou dans la section **[!UICONTROL Suivi des actions]** pour les campagnes par SMS. Les clics sur les liens profonds suivis utilisent des URL sous `/ee/v1/mclick/*`, qu’Adobe héberge et résout.
>
>Pour les liens **non suivis**, l’URL n’est pas réécrite via les systèmes Adobe. Vous devez configurer des liens universels ou des liens d’application sur vos propres domaines et hébergement afin que ces liens ouvrent votre application comme prévu.

## Implémentation des applications mobiles {#mobile-implementation}

Cette section explique comment implémenter des liens profonds mobiles avec [!DNL Adobe Journey Optimizer], de sorte que, dans une configuration **HTTPS** standard (liens universels et liens d’application), une seule URL puisse :

* Ouvrez un écran spécifique dans votre application mobile lors de l’installation de l’application, ou
* Ouvrez votre site web comme solution de secours lorsque l’application n’est pas installée.

Lorsque le suivi des liens est activé pour votre message, [!DNL Journey Optimizer] continue à suivre ces clics, les inclut dans les rapports et peut les utiliser dans des [expériences de contenu](../content-management/content-experiment.md) si vous les exécutez sur le message.

Cette section fournit des modèles d’implémentation courants pour les liens profonds. Votre configuration exacte dépend de l&#39;architecture et de la structure de routage de votre application.

### iOS (liens universels) {#ios-implementation}

1. Dans Xcode, sélectionnez votre cible via **[!UICONTROL Signature et fonctionnalités]** > **[!UICONTROL + fonctionnalité]** > **[!UICONTROL domaines associés]**.
1. Ajoutez des entrées pour les sous-domaines délégués, par exemple :

   ```text
   applinks:www.mybusiness.com
   applinks:data.email.mybusiness.com
   ```

1. Gérez les liens universels dans l’application et obtenez le lien d’origine à partir de l’en-tête de réponse.

   +++ Exemple : iOS 13+ avec des scènes

   ```swift
   class SceneDelegate: UIResponder, UIWindowSceneDelegate {
   
       func scene(_ scene: UIScene,
                 continue userActivity: NSUserActivity) {
           guard userActivity.activityType == NSUserActivityTypeBrowsingWeb,
                 let incomingURL = userActivity.webpageURL else {
               return
           }
   
           handleUniversalLink(url: incomingURL)
       }
   
       private func handleUniversalLink(url: URL) {
           // Only handle AJO tracked mobile clicks
           guard url.host == "data.email.mybusiness.com",
                 url.path.hasPrefix("/ee/v1/mclick") else {
               // Could also handle direct www.mybusiness.com links here
               return
           }
   
           resolveTrackedUrlAndRoute(url)
       }
   
       private func resolveTrackedUrlAndRoute(_ trackedUrl: URL) {
           var request = URLRequest(url: trackedUrl)
           request.httpMethod = "GET"
   
           URLSession.shared.dataTask(with: request) { _, response, error in
               guard error == nil,
                     let httpResponse = response as? HTTPURLResponse,
                     let locationValue = httpResponse.allHeaderFields["Location"] as? String,
                     let finalUrl = URL(string: locationValue) else {
                   return
               }
   
               DispatchQueue.main.async {
                   self.routeToDestination(finalUrl)
               }
           }.resume()
       }
   
       private func routeToDestination(_ url: URL) {
           // Example: map URL paths to screens
           // https://www.mybusiness.com/dashboard/offers/coupons
           // → OffersViewController for Coupons
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>L’application doit effectuer une **&#x200B;**&#x200B;sur l’URL `mclick` et lire l’en-tête **`Location`**, puis effectuer le routage en fonction de l’URL **finale**.
>
>N’ouvrez pas simplement l’URL `mclick` dans Safari, car cela va à l’encontre de l’objectif des liens profonds.

### Android (Liens d’application) {#android-implementation}

1. Ajoutez le filtre d’intention App Link dans votre application Android.

   ```xml
   <activity
       android:name=".DeepLinkActivity"
       android:exported="true">
   
       <intent-filter android:autoVerify="true">
           <action android:name="android.intent.action.VIEW" />
           <category android:name="android.intent.category.DEFAULT" />
           <category android:name="android.intent.category.BROWSABLE" />
   
           <data
               android:scheme="https"
               android:host="data.email.mybusiness.com"
               android:pathPrefix="/ee/v1/mclick" />
       </intent-filter>
   
   </activity>
   ```

1. Mettez en œuvre le gestionnaire de liens profonds.

   +++ A Kotlin :

   ```kotlin
   class DeepLinkActivity : AppCompatActivity() {
   
       override fun onCreate(savedInstanceState: Bundle?) {
           super.onCreate(savedInstanceState)
   
           val trackedUri = intent?.data
           if (trackedUri == null ||
               trackedUri.host != "data.email.mybusiness.com" ||
               !trackedUri.path.orEmpty().startsWith("/ee/v1/mclick")) {
               finish()
               return
           }
   
           resolveTrackedUrlAndRoute(trackedUri)
       }
   
       private fun resolveTrackedUrlAndRoute(trackedUri: Uri) {
           lifecycleScope.launch(Dispatchers.IO) {
               try {
                   val finalUrl = followRedirect(trackedUri.toString())
                   withContext(Dispatchers.Main) {
                       routeToDestination(finalUrl)
                       finish()
                   }
               } catch (e: Exception) {
                   // Optionally log error, fallback to browser
                   finish()
               }
           }
       }
   
       private fun followRedirect(trackedUrl: String): Uri {
           val client = OkHttpClient.Builder()
               .followRedirects(false) // We want to read Location ourselves
               .build()
   
           val request = Request.Builder()
               .url(trackedUrl)
               .get()
               .build()
   
           client.newCall(request).execute().use { response ->
               val location = response.header("Location")
                   ?: throw IllegalStateException("Missing Location header")
               return Uri.parse(location)
           }
       }
   
       private fun routeToDestination(finalUri: Uri) {
           // Example: interpret https://www.mybusiness.com/dashboard/offers/coupons
           // and open the correct Activity / Fragment
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>Comme iOS, l’application doit appeler l’URL `mclick` et utiliser l’en-tête **`Location`** pour déterminer la destination finale.
>
>Utilisez `followRedirects(false)` pour contrôler la gestion des redirections et consigner les analyses avec précision si nécessaire.
>
>La logique de routage est spécifique à l’application. Définissez un mappage clair des URL vers les écrans.

## Pratiques recommandées {#deeplink-best-practices}

* **Utiliser des chemins stables** : privilégiez les itinéraires qui résistent aux modifications de l’interface utilisateur de l’application (par exemple, `/account/orders` au lieu de `/tab/3/view/2`).
* **Compte pour les chemins suivis** : lorsque le suivi des liens est activé, le lien sur lequel l’utilisateur a cliqué peut utiliser des modèles de chemins suivis (par exemple, `/ee/v1/mclick/`). Assurez-vous que votre routeur peut analyser l’URL finale après la résolution du lien suivi.
* **Garder les paramètres prévisibles** : définissez un schéma de paramètres cohérent (par exemple, `?orderId=12345`).
* **Évitez les données sensibles dans les URL** : ne placez pas de secrets ou de données personnelles directement dans l’URL du lien profond.
* **Tester votre lien profond** : envoyez un BAT et cliquez sur le lien profond sur un appareil sur lequel l’application est installée.
* **Valider sur des appareils réels** : les liens universels et les comportements de résolution des liens suivis sont plus fiables à valider sur des appareils physiques que sur des simulateurs.
* **Valider le routage côté application** : si le lien profond n’ouvre pas l’écran attendu, validez le routage côté application et le format de l’URL (hôte/chemin/requête et codage de l’URL).
* **Gardez à l’esprit l’initialisation de l’application** : le comportement des liens d’application/liens universels est le plus fiable après l’installation et l’ouverture de l’application au moins une fois.

## Résolution des problèmes et FAQ {#troubleshooting-faq}

+++ L’application ne s’ouvre pas lorsque j’appuie sur le lien profond.

* Vérifiez que l’URL correspond à l’hôte et aux modèles de chemin que votre application est enregistrée pour gérer, y compris les chemins de clics suivis lorsque le suivi des liens est activé (par exemple, les chemins sous `/ee/v1/mclick/`).
* Pour les liens universels d’iOS et les liens d’applications Android, vérifiez que l’association de domaine (AASA/`assetlinks.json`) est correctement configurée et accessible.
* Test sur un appareil réel (les simulateurs/émulateurs peuvent se comporter différemment pour l’association de liens).

+++

+++ L’application s’ouvre mais n’accède pas à l’écran attendu.

* Vérifiez que le routeur côté application analyse correctement le chemin/la requête de l’URL.
* Vérifiez l’encodage de l’URL : les caractères réservés doivent être encodés en URL.
* Validez les noms et les valeurs des paramètres qui correspondent à ce que le routeur attend.

+++

+++ Que se passe-t-il si l’application n’est pas installée ?

* Si la même URL HTTPS peut être diffusée par votre site web, le lien peut ouvrir une page web comme solution de secours lorsque l’application n’est pas installée (configurez la destination et le routage web en conséquence).

+++

+++ Comment inclure en toute sécurité des caractères spéciaux dans les paramètres ?

Valeurs de paramètre de requête codées par URL. Cela réduit les problèmes de diffusion et de rendu et permet d’éviter les erreurs d’analyse dans votre application.

+++

+++ Comment devrions-nous tester de bout en bout ?

* Créez une épreuve avec un lien profond, cliquez dessus sur les appareils iOS et Android (scénarios installés et non installés).
* Valider :
   * La valeur du lien e-mail ou SMS final (hôte/chemin/requête)
   * Association au niveau du système d’exploitation (si vous utilisez des liens universels/d’application)
   * Le résultat du routage in-app

+++

+++ J’ai une application, mais différents sous-domaines pour l’organisation. Dois-je demander la création d’AASA et assetLinks.json pour chaque sous-domaine ?

Oui. Si vous souhaitez créer des liens profonds sur chaque sous-domaine délégué, demandez une configuration AASA et `assetlinks.json` pour chaque sous-domaine qui doit prendre en charge la fonctionnalité.

+++

+++ L’URL que je configure doit-elle utiliser un format de lien profond (par exemple, `appname://path`) ?

Vous pouvez utiliser un modèle d’URL personnalisé (par exemple, `appname://path`), mais l’approche recommandée est un lien universel ou un lien d’application (`https://`), qui correspond à la configuration basée sur HTTPS dans les sections Configuration et implémentation de cette page.

+++

+++ Les paramètres UTM sur l’URL seront-ils disponibles dans l’application mobile pour Analytics ?

Oui. Les paramètres UTM que vous configurez dans [!DNL Journey Optimizer] sont inclus dans l’URL finale renvoyée dans l’en-tête `Location` lorsque votre application effectue un GET sur l’URL `mclick`. Vous pouvez donc les utiliser pour les analyses in-app.

+++

+++ Quelle est l’expérience utilisateur pour les URL `/ee/v1/click/` ?

Le lien s’ouvre dans le navigateur web par défaut de l’appareil (comportement de suivi des clics standard), au lieu d’être traité comme un lien profond de l’application par le biais du flux de `mclick` décrit sur cette page.

+++
