---
solution: Journey Optimizer
product: journey optimizer
title: Créer un profil de test
description: Découvrez comment créer un profil de test
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: bd5e053a-69eb-463b-add3-8b9168c8e280
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '1375'
ht-degree: 100%

---

# Créer des profils de test {#create-test-profiles}

Les profils de test sont requis lors de l’utilisation du [mode test](../building-journeys/testing-the-journey.md) dans un parcours ainsi que pour [prévisualiser et tester le contenu](../design/preview.md).

Il existe plusieurs façons de créer des profils de test. Vous trouverez sur cette page des informations détaillées pour :

* Transformer un [profil existant](#turning-profile-into-test) en profil de test.

* Créer des profils de test en chargeant un [fichier CSV](#create-test-profiles-csv) ou en utilisant des [appels d’API](#create-test-profiles-api).

   Outre ces deux méthodes, Adobe Journey Optimizer est fourni avec un [cas d’utilisation intégré](#use-case-1) spécifique pour faciliter la création de profils de test.

Vous pouvez également charger un fichier JSON dans un jeu de données existant. Pour en savoir plus à ce sujet, consultez la [documentation sur l&#39;ingestion des données](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=fr#add-data-to-dataset){target=&quot;_blank&quot;}.

Veuillez noter que la création d&#39;un profil de test est similaire à la création de profils classiques dans Adobe Experience Platform. Pour plus d&#39;informations, consultez la [documentation du profil client en temps réel](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target=&quot;_blank&quot;}.

➡️ [Découvrez comment créer des profils de test dans cette vidéo](#video)

## Conditions préalables {#test-profile-prerequisites}

Pour pouvoir créer des profils, il vous faut d’abord créer un schéma ainsi qu’un jeu de données dans Adobe [!DNL Journey Optimizer].

Pour **créer un schéma**, procédez comme suit :

1. Dans la section du menu DATA MANAGEMENT, cliquez sur **[!UICONTROL Schémas]**.
   ![](assets/test-profiles-0.png)
1. Cliquez sur **[!UICONTROL Créer un schéma]** dans le coin supérieur droit, puis sélectionnez un type de schéma, par exemple **Profil individuel XDM**.
   ![](assets/test-profiles-1.png)
1. Sélectionnez les groupes de champs appropriés. Veillez à ajouter le groupe de champs **Détails du profil de test**.
   ![](assets/test-profiles-1-ter.png)
Une fois que vous avez terminé, cliquez sur **[!UICONTROL Ajouter des groupes de champs]** : la liste des groupes de champs s&#39;affiche dans l&#39;écran aperçu du schéma.
   ![](assets/test-profiles-2.png)

   >[!NOTE]
   >
   >* Cliquez sur le nom du schéma pour le modifier et mettre à jour ses propriétés.
   >
   >* Cliquez sur le bouton **[!UICONTROL Ajouter]** dans la section Groupes de champs pour sélectionner d&#39;autres groupes de champs à ajouter au schéma.


1. Dans la liste des champs, cliquez sur le champ que vous souhaitez définir comme l&#39;identité principale.
   ![](assets/test-profiles-3.png)
1. Dans le volet de droite **[!UICONTROL Propriétés du champ]**, vérifiez les options **[!UICONTROL Identité]** et **[!UICONTROL Identité principale]**, puis sélectionnez un espace de noms. Si vous souhaitez que l&#39;identité principale soit une adresse e-mail, choisissez l&#39;espace de noms **[!UICONTROL E-mail]**. Cliquez sur **[!UICONTROL Appliquer]**.
   ![](assets/test-profiles-4bis.png)
1. Sélectionnez le schéma et activez l&#39;option **[!UICONTROL Profil]** dans le volet **[!UICONTROL Propriétés du schéma]**.
   ![](assets/test-profiles-5.png)
1. Cliquez sur **Enregistrer**.

>[!NOTE]
>
>Pour plus d&#39;informations sur la création de schémas, consultez la [documentation XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=fr#prerequisites){target=&quot;_blank&quot;}.

Vous devez ensuite **créer le jeu de données** dans lequel les profils seront importés. Procédez de la façon suivante :

1. Accédez à **[!UICONTROL Jeux de données]**, puis cliquez sur **[!UICONTROL Créer un jeu de données]**.
   ![](assets/test-profiles-6.png)
1. Choisissez **[!UICONTROL Créer un jeu de données à partir d&#39;un schéma]**.
   ![](assets/test-profiles-7.png)
1. Sélectionnez le schéma créé précédemment, puis cliquez sur **[!UICONTROL Suivant]**.
   ![](assets/test-profiles-8.png)
1. Choisissez un nom, puis cliquez sur **[!UICONTROL Terminer]**.
   ![](assets/test-profiles-9.png)
1. Activez l&#39;option **[!UICONTROL Profil]**.
   ![](assets/test-profiles-10.png)

>[!NOTE]
>
> Pour plus d&#39;informations sur la création de jeux de données, consultez la [documentation du service de catalogue](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=fr#getting-started){target=&quot;_blank&quot;}.

## Cas d’utilisation interne au produit{#use-case-1}

Depuis la page d’accueil d&#39;Adobe Journey Optimizer, vous pouvez exploiter le cas d’utilisation interne au produit des profils de test. Ce cas pratique facilite la création de profils de test utilisés pour les parcours de test avant la publication.

![](assets/use-cases-home.png)

Cliquez sur le bouton **[!UICONTROL Commencer]** pour lancer le cas d’utilisation.

Les informations affichées sont requises :

1. **Espace de noms d’identité** : [espace de noms d’identité](../segment/get-started-identity.md) utilisé pour identifier de manière unique les profils de test. Par exemple, si l&#39;e-mail est utilisé pour identifier les profils de test, l’espace de noms d’identité **E-mail** doit être sélectionné. Si l’identifiant unique est le numéro de téléphone, l’espace de noms d’identité **Téléphone** doit être sélectionné.

2. **Fichier CSV** : fichier séparé par des virgules contenant la liste des profils de test à créer. Le cas d’utilisation exige un format prédéfini pour le fichier CSV contenant la liste des profils de test à créer. Chaque ligne du fichier doit inclure les champs suivants dans l’ordre correct :

   1. **ID de personne** : identifiant unique du profil de test. Les valeurs de ce champ doivent refléter l’espace de noms d’identité sélectionné. (Par exemple, si **Téléphone** est sélectionné pour l’espace de noms d’identité, les valeurs de ce champ doivent être des numéros de téléphone. De même, si **E-mail** est sélectionné, les valeurs de ce champ doivent être des e-mails.)
   1. **Adresse e-mail** : adresse e-mail du profil de test. (Le champ **ID de personne** et le champ **Adresse e-mail** peuvent potentiellement contenir les mêmes valeurs si **E-mail** est sélectionné comme espace de noms d’identité.)
   1. **Prénom** : prénom du profil de test.
   1. **Nom** : nom du profil de test.
   1. **Ville** : ville de résidence du profil de test.
   1. **Pays** : pays de résidence du profil de test.
   1. **Genre** : genre du profil de test. Les valeurs disponibles sont **homme**, **femme** et **non_spécifié**

Après avoir sélectionné l’espace de noms d’identité et fourni le fichier CSV au format ci-dessus, cliquez sur le bouton **[!UICONTROL Exécuter]** en haut à droite. Le cas d’utilisation peut prendre quelques minutes. Lorsque le cas d’utilisation a terminé le traitement et la création des profils de test, une notification est envoyée à l’utilisateur.

>[!NOTE]
>
>Les profils de test peuvent remplacer les profils existants. Avant d’exécuter le cas d’utilisation, assurez-vous que le fichier CSV contient uniquement des profils de test et qu’il est exécuté sur le bon environnement Sandbox.

## Transformation d&#39;un profil en profil de test{#turning-profile-into-test}

Vous pouvez transformer un profil existant en profil de test : vous pouvez mettre à jour les attributs de profil de la même manière que lorsque vous créez un profil.

Pour ce faire, une méthode simple consiste à utiliser une activité d’action **[!UICONTROL Mettre à jour le profil]** dans un parcours et à redéfinir le champ booléen **testProfile** de false à true.

Votre parcours sera composé d&#39;une activité **[!UICONTROL Lecture de segment]** et **[!UICONTROL Mettre à jour le profil]**. Vous devez d&#39;abord créer un segment ciblant les profils que vous souhaitez transformer en profils de test.

>[!NOTE]
>
> Puisque vous allez mettre à jour le champ **testProfile**, les profils sélectionnés doivent inclure ce champ. Le schéma associé doit avoir le groupe de champs **Détails du test de profil**. Consultez [cette section](../segment/creating-test-profiles.md#test-profiles-prerequisites).

1. Accédez à **Segments**, puis à **Créer un segment**, en haut à droite.
   ![](assets/test-profiles-22.png)
1. Définissez un nom pour votre segment et créez le segment : choisissez le ou les champs et la ou les valeurs pour cibler les profils de votre choix.
   ![](assets/test-profiles-23.png)
1. Cliquez sur **Enregistrer** et vérifiez que les profils sont correctement ciblés par le segment.
   ![](assets/test-profiles-24.png)

   >[!NOTE]
   >
   > Le calcul des segments peut prendre un certain temps. En savoir plus sur les segments dans [cette section](../segment/about-segments.md).

1. Créez maintenant un parcours et commencez par une activité d&#39;orchestration **[!UICONTROL Lecture de segment]**.
1. Sélectionnez le segment créé précédemment et l&#39;espace de noms utilisé par vos profils.
   ![](assets/test-profiles-25.png)
1. Ajoutez une activité d&#39;action **[!UICONTROL Mettre à jour le profil]**.
1. Sélectionnez le schéma, le champ **testProfiles** et le jeu de données et définissez la valeur sur **true**. Pour ce faire, dans le champ **[!UICONTROL VALUE]**, cliquez sur l&#39;icône **Stylo** à droite, sélectionnez **[!UICONTROL Mode avancé]** et saisissez **true**.
   ![](assets/test-profiles-26.png)
1. Cliquez sur **[!UICONTROL Publier]**.
1. Dans la section **[!UICONTROL Segments]**, vérifiez que les profils ont été correctement mis à jour.
   ![](assets/test-profiles-28.png)

   >[!NOTE]
   >
   > Pour plus d&#39;informations sur l&#39;activité **[!UICONTROL Mettre à jour le profil]**, consultez [cette section](../building-journeys/update-profiles.md).

## Création d&#39;un profil de test à l&#39;aide d&#39;un fichier CSV{#create-test-profiles-csv}

Dans Adobe Experience Platform, vous pouvez créer des profils en téléchargeant un fichier CSV contenant les différents champs de profil dans votre jeu de données. Cette méthode est la plus simple.

1. Créez un fichier CSV simple à l&#39;aide d&#39;un tableur.
1. Ajoutez une colonne pour chaque champ nécessaire. Assurez-vous d&#39;ajouter le champ de l&#39;identité principale (« personID » dans l&#39;exemple ci-dessus) et le champ « testProfile » défini sur « true ».
   ![](assets/test-profiles-11.png)
1. Ajoutez une ligne par profil et remplissez les valeurs de chaque champ.
   ![](assets/test-profiles-12.png)
1. Enregistrez la feuille de calcul au format CSV. Assurez-vous que les virgules sont utilisées comme séparateurs.
1. Accédez aux **workflows** d&#39; Adobe Experience Platform.
   ![](assets/test-profiles-14.png)
1. Sélectionnez **Mapper un CSV à un schéma XDM**, puis cliquez sur **Lancer**.
   ![](assets/test-profiles-16.png)
1. Sélectionnez le jeu de données dans lequel vous souhaitez importer les profils. Cliquez sur **Suivant**.
   ![](assets/test-profiles-17.png)
1. Cliquez sur **Choisir les fichiers** et sélectionnez votre fichier CSV. Une fois le fichier téléchargé, cliquez sur **Suivant**.
   ![](assets/test-profiles-18.png)
1. Mappez les champs CSV source aux champs du schéma, puis cliquez sur **Terminer**.
   ![](assets/test-profiles-19.png)
1. L&#39;import de données démarre. Le statut passe de **Traitement** à **Succès**. Cliquez sur **Aperçu du jeu de données**, dans le coin supérieur droit.
   ![](assets/test-profiles-20.png)
1. Vérifiez que les profils de test ont été correctement ajoutés.
   ![](assets/test-profiles-21.png)

Vos profils de test sont ajoutés et peuvent désormais être utilisés lors du test d&#39;un parcours. Reportez-vous à [cette section](../building-journeys/testing-the-journey.md).
>[!NOTE]
>
> Pour plus d&#39;informations sur les imports de fichiers CSV, consultez la [documentation sur l&#39;ingestion de données](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=fr#tutorials){target=&quot;_blank&quot;}.

## Création de profils de test à l&#39;aide d&#39;appels d&#39;API{#create-test-profiles-api}

Vous pouvez également créer des profils de test au moyen d&#39;appels d&#39;API. Pour en savoir plus, consultez la [documentation d’Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}.

Vous devez utiliser un schéma de profil contenant le groupe de champs « Détails du test de profil ». L&#39;indicateur testProfile fait partie de ce groupe de champs.
Lors de la création d&#39;un profil, veillez à transmettre la valeur : testProfile = true.

Veuillez noter que vous pouvez également mettre à jour un profil existant pour remplacer son indicateur testProfile par « true ».

Voici un exemple d&#39;appel API pour créer un profil de test :

```
curl -X POST \
'https://dcs.adobedc.net/collection/xxxxxxxxxxxxxx' \
-H 'Cache-Control: no-cache' \
-H 'Content-Type: application/json' \
-H 'Postman-Token: xxxxx' \
-H 'cache-control: no-cache' \
-H 'x-api-key: xxxxx' \
-H 'x-gw-ims-org-id: xxxxx' \
-d '{
"header": {
"msgType": "xdmEntityCreate",
"msgId": "xxxxx",
"msgVersion": "xxxxx",
"xactionid":"xxxxx",
"datasetId": "xxxxx",
"imsOrgId": "xxxxx",
"source": {
"name": "Postman"
},
"schemaRef": {
"id": "https://example.adobe.com/mobile/schemas/xxxxx",
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"xdmEntity": {
"_id": "xxxxx",
"_mobile":{
"ECID": "xxxxx"
},
"testProfile":true
}
}
}'
```

## Vidéo pratique {#video}

Découvrez comment créer des profils de test.

>[!VIDEO](https://video.tv.adobe.com/v/334236?quality=12)
