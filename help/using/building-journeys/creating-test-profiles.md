---
title: Créer un profil de test
description: Découvrez comment créer un profil de test
feature: Parcours
topic: Gestion de contenu
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 76%

---

# Création de profils de test {#create-test-profiles}

![](../assets/do-not-localize/badge.png)

Les profils de test sont requis lors de l’utilisation du mode test dans un parcours. Vous pouvez transformer un [profil existant](../building-journeys/creating-test-profiles.md#turning-profile-into-test) en profil de test ou [créer un profil de test](../building-journeys/creating-test-profiles.md#create-test-profiles-csv). Pour savoir comment utiliser le mode test, consultez [cette section](../building-journeys/testing-the-journey.md).

Il existe différentes manières de créer un profil de test dans Adobe Experience Platform. Dans cette documentation, nous nous concentrons sur deux méthodes : le téléchargement d’un [fichier CSV](../building-journeys/creating-test-profiles.md#create-test-profiles-csv) et l’utilisation d’[appels d’API](../building-journeys/creating-test-profiles.md#create-test-profiles-api). Vous pouvez également télécharger un fichier json dans un jeu de données. Pour ce faire, reportez-vous à la [documentation sur l’ingestion de données](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=fr#add-data-to-dataset).

La création d’un profil de test est similaire à la création de profils classiques dans Adobe Experience Platform. Pour plus d’informations, consultez la [documentation du profil client en temps réel](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr).

## Conditions préalables{#test-profile-prerequisites}

Pour pouvoir créer des profils, il vous faut d’abord créer un schéma ainsi qu’un jeu de données dans Adobe [!DNL Journey Optimizer].

Tout d’abord, vous devez **créer un schéma**. Procédez de la façon suivante :

1. Dans la section ADMINISTRATION, cliquez sur **[!UICONTROL Schémas]**.
   ![](../assets/test-profiles-0.png)
1. Cliquez sur **[!UICONTROL Créer un schéma]** dans le coin supérieur droit, puis sélectionnez un type de schéma, par exemple **Profil individuel XDM**.
   ![](../assets/test-profiles-1.png)
1. Sélectionnez les groupes de champs appropriés. Veillez à ajouter le groupe de champs **Détails du test de profil** .
   ![](../assets/test-profiles-1-ter.png)
Une fois que vous avez terminé, cliquez sur  **[!UICONTROL Ajouter des groupes de champs]** : la liste des groupes de champs s’affiche dans l’écran aperçu du schéma.
   ![](../assets/test-profiles-2.png)

   >[!NOTE]
   >
   >* Cliquez sur le nom du schéma pour le modifier et mettre à jour ses propriétés.
      >
      >
   * Cliquez sur le bouton **[!UICONTROL Ajouter]** dans la section Groupes de champs pour sélectionner d’autres groupes de champs à ajouter au schéma.


1. Dans la liste des champs, cliquez sur le champ que vous souhaitez définir comme l’identité principale.
   ![](../assets/test-profiles-3.png)
1. Dans le panneau de droite **[!UICONTROL Propriétés du champ]**, cochez les options ****[!UICONTROL Identité]** et ****[!UICONTROL Identité Principal]** et sélectionnez un espace de noms. Si vous souhaitez que l’identité principale soit une adresse e-mail, choisissez l’espace de noms **E-mail**. Cliquez sur **Appliquer**.
   ![](../assets/test-profiles-4.png)
1. Sélectionnez le schéma et activez l’option **[!UICONTROL Profil]** dans les **[!UICONTROL Propriétés du schéma]**.
   ![](../assets/test-profiles-5.png)
1. Cliquez sur **Enregistrer**.

>[!NOTE]
>
>Pour plus d’informations sur la création de schémas, consultez la [documentation XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=fr#prerequisites).

Vous devez ensuite **créer le jeu de données** dans lequel les profils seront importés. Procédez de la façon suivante :

1. Accédez à **[!UICONTROL Jeux de données]**, puis cliquez sur **[!UICONTROL Créer un jeu de données]**.
   ![](../assets/test-profiles-6.png)
1. Choisissez **[!UICONTROL Créer un jeu de données à partir d’un schéma]**.
   ![](../assets/test-profiles-7.png)
1. Sélectionnez le schéma créé précédemment, puis cliquez sur **[!UICONTROL Suivant]**.
   ![](../assets/test-profiles-8.png)
1. Choisissez un nom, puis cliquez sur **[!UICONTROL Terminer]**.
   ![](../assets/test-profiles-9.png)
1. Activez l’option **[!UICONTROL Profil]**.
   ![](../assets/test-profiles-10.png)

>[!NOTE]
>
> Pour plus d’informations sur la création de jeux de données, consultez la [documentation du service de catalogue](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=fr#getting-started).

## Transformer un profil en profil de test{#turning-profile-into-test}

Vous pouvez transformer un profil existant en profil de test : vous pouvez mettre à jour les attributs de profil de la même manière que lorsque vous créez un profil.

Pour ce faire, il suffit d’utiliser une activité d’action **[!UICONTROL Mettre à jour le profil]** dans un parcours et de remplacer le champ booléen testProfile par true.

Votre parcours sera composé d’une activité **[!UICONTROL Lecture de segment]** et **[!UICONTROL Mettre à jour le profil]**. Vous devez d’abord créer un segment ciblant les profils que vous souhaitez transformer en profils de test.

>[!NOTE]
>
> Puisque vous allez mettre à jour le champ **testProfile**, les profils sélectionnés doivent inclure ce champ. Le schéma associé doit avoir le mixin **Détails du test de profil**. Consultez [cette section](../building-journeys/creating-test-profiles.md#test-profiles-prerequisites).

1. Accédez à **Segments**, puis **Créer un segment**, en haut à droite.
   ![](../assets/test-profiles-22.png)
1. Définissez un nom pour votre segment et créez le segment : choisissez le ou les champs et la ou les valeurs pour cibler les profils de votre choix.
   ![](../assets/test-profiles-23.png)
1. Cliquez sur **Enregistrer** et vérifiez que les profils sont correctement ciblés par le segment.
   ![](../assets/test-profiles-24.png)

   >[!NOTE]
   >
   > Le calcul des segments peut prendre un certain temps. En savoir plus sur les segments dans [cette section](../segment/about-segments.md).

1. Créez maintenant un parcours et commencez par une activité d’orchestration **[!UICONTROL Lecture de segment]**.
1. Sélectionnez le segment créé précédemment et l’espace de noms utilisé par vos profils.
   ![](../assets/test-profiles-25.png)
1. Ajoutez une activité d’action **[!UICONTROL Mettre à jour le profil]**.
1. Sélectionnez le schéma, le champ **testProfiles**, le jeu de données et définissez la valeur sur **True**. Pour ce faire, dans le champ **[!UICONTROL VALUE]** , cliquez sur l&#39;icône **Pen** à droite, sélectionnez **[!UICONTROL Mode avancé]** et saisissez **true**.
   ![](../assets/test-profiles-26.png)
1. Ajoutez une activité **Fin** et cliquez sur **[!UICONTROL Publier]**.
1. Dans la section **[!UICONTROL Segments]** , vérifiez que les profils ont été correctement mis à jour.
   ![](../assets/test-profiles-28.png)

   >[!NOTE]
   >
   > Pour plus d’informations sur l’activité **[!UICONTROL Mettre à jour le profil]**, consultez [cette section](../building-journeys/update-profiles.md).

## Création d’un profil de test à l’aide d’un fichier csv{#create-test-profiles-csv}

Dans Adobe Experience Platform, vous pouvez créer des profils en téléchargeant un fichier CSV contenant les différents champs de profil dans votre jeu de données. Cette méthode est la plus simple.

1. Créez un fichier CSV simple à l’aide d’un tableur.
1. Ajoutez une colonne pour chaque champ nécessaire. Assurez-vous d’ajouter le champ de l’identité principale (« personID » dans l’exemple ci-dessus) et le champ « testProfile » défini sur « true ».
   ![](../assets/test-profiles-11.png)
1. Ajoutez une ligne par profil et remplissez les valeurs de chaque champ.
   ![](../assets/test-profiles-12.png)
1. Enregistrez la feuille de calcul au format CSV. Assurez-vous que les virgules sont utilisées comme séparateurs.
1. Accédez à Adobe Experience Platform **Workflows**.
   ![](../assets/test-profiles-14.png)
1. Sélectionnez **Mapper un CSV à un schéma XDM**, puis cliquez sur **Lancer**.
   ![](../assets/test-profiles-16.png)
1. Sélectionnez le jeu de données dans lequel vous souhaitez importer les profils. Cliquez sur **Suivant**.
   ![](../assets/test-profiles-17.png)
1. Cliquez sur **Choisir les fichiers** et sélectionnez votre fichier CSV. Une fois le fichier téléchargé, cliquez sur **Suivant**.
   ![](../assets/test-profiles-18.png)
1. Mappez les champs CSV source aux champs du schéma, puis cliquez sur **Terminer**.
   ![](../assets/test-profiles-19.png)
1. L’import de données démarre. Le statut passe de **Traitement** à **Succès**. Cliquez sur **Aperçu du jeu de données**, dans le coin supérieur droit.
   ![](../assets/test-profiles-20.png)
1. Vérifiez que les profils de test ont été correctement ajoutés.
   ![](../assets/test-profiles-21.png)

Vos profils de test sont ajoutés et peuvent désormais être utilisés lors du test d’un parcours. Reportez-vous à [cette section](../building-journeys/testing-the-journey.md).
>[!NOTE]
>
> Pour plus d’informations sur les imports de fichiers CSV, consultez la [documentation sur l’ingestion de données](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=fr#tutorials).

## Créer des profils de test à l’aide des appels API{#create-test-profiles-api}

Vous pouvez également créer des profils de test au moyen d’appels d’API. En savoir plus sur cette [page](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html).

Vous devez utiliser un schéma de profil contenant le mixin « Détails du test de profil ». L’indicateur testProfile fait partie de ce mixin.

Lors de la création d’un profil, veillez à transmettre la valeur : testProfile = true.

Veuillez noter que vous pouvez également mettre à jour un profil existant pour remplacer son indicateur testProfile par « true ».

Voici un exemple d’appel API pour créer un profil de test :

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
