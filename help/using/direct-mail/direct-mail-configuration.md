---
title: Configuration du publipostage direct
description: Découvrez comment configurer le canal Publipostage direct dans Journey Optimizer
feature: Direct Mail, Surface
topic: Content Management
role: User
level: Experienced
keyword: direct, mail, configuration, direct-mail, provider
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
source-git-commit: 916239c98c982acf9c6f999316e46036d36b2098
workflow-type: tm+mt
source-wordcount: '1708'
ht-degree: 82%

---

# Configuration du publipostage direct {#direct-mail-configuration}

[!DNL Journey Optimizer] vous permet de personnaliser et de générer les fichiers requis par les fournisseurs de publipostage direct pour envoyer du courrier à vos clients.

Lors de la [création d’un message de publipostage direct](../direct-mail/create-direct-mail.md), vous définissez les données de l’audience ciblée, y compris les informations de contact sélectionnées (adresse postale par exemple). Un fichier contenant ces données sera alors automatiquement généré et exporté vers un serveur, où votre fournisseur de publipostage direct pourra les récupérer et prendre en charge l’envoi.

Avant de pouvoir générer ce fichier, vous devez créer les éléments suivants :

1. [Une configuration du routage des fichiers](#file-routing-configuration) pour spécifier le serveur sur lequel le fichier sera exporté et chiffré, le cas échéant.

1. [Une configuration du courrier](#direct-mail-configuration) qui fait référence à la configuration du routage des fichiers. Si vous n’avez configuré aucune option de routage de fichier, vous ne pourrez pas créer de configuration de courrier.


>[!CAUTION]
>
>* Pour créer une configuration de routage de fichier, vous devez disposer de l’autorisation intégrée **[!DNL Manage file routing]**. [En savoir plus](../administration/ootb-product-profiles.md#content-library-manager)
>
>* Les fichiers de courrier ne sont générés qu’au moment de l’export. Le système ne stocke pas indéfiniment les exports plus anciens. Pour une sauvegarde plus longue ou permanente, configurez une option de routage des fichiers (SFTP ou espace de stockage dans le cloud).

## Configurer le routage des fichiers {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Définir la configuration du routage des fichiers"
>abstract="Une fois que vous avez créé un message de publipostage direct, le fichier contenant les données de l’audience ciblée sera généré et exporté vers un serveur. Vous devez spécifier les détails du serveur afin que votre fournisseur de publipostage direct puisse accéder à ce fichier et l’utiliser pour diffuser du publipostage direct."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/channels/direct-mail/create-direct-mail" text="Créer un message de publipostage direct"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Définir la configuration du routage des fichiers"
>abstract="Vous devez définir l’endroit où le fichier sera exporté pour que votre fournisseur de publipostage direct puisse l’utiliser."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Configuration du routage des fichiers"
>abstract="Sélectionnez la configuration du routage des fichiers de votre choix, qui définit l’endroit où le fichier sera exporté pour que votre fournisseur de publipostage direct puisse l’utiliser."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Sélectionnez le type de serveur pour votre fichier"
>abstract="Choisissez le type de serveur à utiliser pour l’export de vos fichiers de publipostage direct : Amazon S3, SFTP, Azure ou Zone d’atterrissage des données."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Choisissez la région AWS"
>abstract="Sélectionnez la région géographique du serveur AWS où vous souhaitez exporter vos fichiers de publipostage direct. En règle générale, il est préférable de choisir la région la plus proche du lieu où se trouve votre fournisseur de publipostage direct."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_frequency"
>title="Choisir la région AWS"
>abstract="Si votre configuration du routage des fichiers sera envoyée via des parcours, vous pouvez spécifier la fréquence à laquelle le fichier sera envoyé au serveur."

>[!NOTE]
>
>[!DNL Journey Optimizer] prend actuellement en charge Amazon S3, SFTP, Azure et Zone d’atterrissage des données.

Pour diffuser un message de publipostage direct, [!DNL Journey Optimizer] génère et exporte vers un serveur le fichier contenant les données de votre audience ciblée.

Vous devez spécifier les détails du serveur afin que votre fournisseur de publipostage direct puisse accéder à ce fichier et l’utiliser pour diffuser du courrier.

Pour configurer le routage des fichiers, suivez les étapes ci-dessous.

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres de publipostage direct]** > **[!UICONTROL Routage des fichiers]**, puis cliquez sur **[!UICONTROL Créer une configuration de routage de fichiers]**.

   ![](assets/file-routing-config-button.png){width="800" align="center"}

1. Attribuez un nom à votre configuration.

1. Sélectionnez le type de serveur à utiliser pour l’export de vos fichiers de publipostage direct : Amazon S3, SFTP, Azure ou Zone d’atterrissage des données.

   ![](assets/file-routing-config-type.png){width="800" align="center"}

1. Renseignez les champs spécifiques à chaque type de serveur, comme indiqué dans les onglets ci-dessous.

>[!BEGINTABS]

>[!TAB Amazon S3]

Si vous avez sélectionné **[!UICONTROL Amazon S3]** en tant que **[!UICONTROL type de serveur]**, renseignez les détails et les informations d’identification de votre serveur :

* **nom du compartiment AWS**:To pour savoir où trouver votre nom de compartiment AWS, reportez-vous à [cette page](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingBucket.html).

* **Clé d’accès AWS** : pour savoir où trouver votre ID de la clé d’accès AWS, consultez [cette page](https://docs.aws.amazon.com/IAM/latest/UserGuide/security-creds.html#access-keys-and-secret-access-keys).

* **Clé d’accès AWS** : pour savoir où trouver votre clé secrète AWS, consultez [cette page](https://aws.amazon.com/fr/blogs/security/wheres-my-secret-access-key/).

* **Région AWS** : sélectionnez la **[!UICONTROL région AWS]** où se trouve l’infrastructure du serveur. Les régions AWS sont des zones géographiques qu’AWS utilise pour héberger ses infrastructures cloud. En règle générale, il est préférable de choisir la région la plus proche de l’emplacement de votre fournisseur de publipostage direct.

![](assets/file-routing-config-aws-region.png){width="800" align="center"}

>[!TAB SFTP]

Si vous avez sélectionné **[!UICONTROL SFTP]** en tant que **[!UICONTROL type de serveur]**, renseignez les détails et les informations d’identification de votre serveur :

* **[!UICONTROL Type d’authentification]** : sélectionnez le type d’authentification utilisé pour la connexion au serveur (mot de passe ou clé SSH).

* **[!UICONTROL Compte]** : nom du compte utilisé pour se connecter au serveur SFTP.

* **[!UICONTROL Adresse du serveur]** : URL du serveur SFTP.

* **[!UICONTROL Port]** : numéro de port de la connexion SFTP.

* **[!UICONTROL Mot de passe]**/**[!UICONTROL Clé SSH]** : mot de passe ou clé SSH utilisés pour la connexion au serveur SFTP.

![](assets/file-routing-config-sftp-detail.png)

>[!TIP]
>
>Lors de l’utilisation de l’authentification par clé SSH, la clé doit être une clé privée OpenSSH codée en **Base64**. S’il s’agit d’un fichier au format PPK, utilisez l’outil PuTTY pour le convertir au format OpenSSH. Pour obtenir des instructions détaillées, voir [cette section](#ssh-key-generation).

>[!NOTE]
>
>Pour spécifier un chemin d’accès sur le serveur afin d’enregistrer le fichier, mettez à jour le **[!UICONTROL nom de fichier]** de la campagne de publipostage direct afin d’inclure le chemin d’accès souhaité. [En savoir plus](create-direct-mail.md#extraction-file)

>[!TAB Azure]

Si vous avez sélectionné **[!UICONTROL Azure]** en tant que **[!UICONTROL type de serveur]**, renseignez les détails et les informations d’identification de votre serveur :

* **Chaîne de connexion Azure** : pour rechercher votre **chaîne de connexion Azure**, consultez [cette page](https://learn.microsoft.com/fr-fr/azure/storage/common/storage-configure-connection-string#configure-a-connection-string-for-an-azure-storage-account).

  La **chaîne de connexion Azure** doit suivre le format présenté ci-dessous :

  `DefaultEndpointsProtocol=[http|https];AccountName=myAccountName;AccountKey=myAccountKey`

* **Nom du conteneur** : pour rechercher votre **nom du conteneur**, consultez [cette page](https://learn.microsoft.com/fr-fr/azure/storage/blobs/blob-containers-portal).

  Le **nom du conteneur** doit contenir uniquement le nom du conteneur sans aucune barre oblique.

  >[!NOTE]
  >
  >Pour spécifier un chemin d’accès dans le conteneur afin d’enregistrer le fichier, mettez à jour le **[!UICONTROL nom de fichier]** de la campagne de publipostage direct afin d’inclure le chemin d’accès souhaité. [En savoir plus](create-direct-mail.md#extraction-file)

  ![](assets/file-routing-config-azure-detail.png)

>[!TAB Zone d’atterrissage des données]

Si vous avez sélectionné **[!UICONTROL Zone d’atterrissage des données]** en tant que **[!UICONTROL type de serveur]**, aucun détail spécifique n’est nécessaire.

![](assets/file-routing-config-dlz-detail.png)

L&#39;ensemble de la clientèle d’[!DNL Adobe Experience Platform] est approvisionné avec un conteneur Zone d’atterrissage des données par sandbox. Pour en savoir plus sur la zone d’atterrissage des données, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"}.

>[!ENDTABS]

Pour chiffrer le fichier, copiez-collez votre clé de chiffrement dans le champ **[!UICONTROL Clé de chiffrement PGP/GPG]**.

Si votre configuration du routage des fichiers sera envoyée via des parcours, vous pouvez spécifier la fréquence à laquelle le fichier sera envoyé au serveur.

![](assets/file-routing-journey.png)

Une fois que vous avez renseigné les détails de votre type de serveur, sélectionnez **[!UICONTROL Envoyer]**. La configuration du routage des fichiers est créée avec le statut **[!UICONTROL Actif]**. Elle est maintenant prête à être utilisée dans une [configuration de publipostage direct](#direct-mail-surface).

Vous pouvez également sélectionner **[!UICONTROL Enregistrer comme brouillon]** pour créer la configuration du routage des fichiers, mais vous ne pourrez pas la sélectionner pour une configuration tant qu’elle ne sera pas **[!UICONTROL Active]**.

### Générer une clé SSH pour l’authentification SFTP {#ssh-key-generation}

Si vous utilisez le protocole SFTP avec l’authentification par clé SSH, vous devez disposer d’une clé privée OpenSSH codée en Base64. Si la clé n’est pas correctement formatée, vous pouvez rencontrer des erreurs de connexion lors de la configuration du routage de vos fichiers.

+++Générer une clé privée OpenSSH codée en Base64

1. Dans PuTTYgen, générez votre paire de clés. RSA avec 2 048 bits ou plus est recommandé.
1. Sélectionnez **Conversions** > **Exporter la clé OpenSSH** dans le menu.
1. Lorsque vous y êtes invité, choisissez d’enregistrer la clé privée **sans protection de phrase secrète**.
1. Dans la boîte de dialogue d’enregistrement, sélectionnez **Tous les fichiers (*.*)** comme type de fichier pour vous assurer que la clé est enregistrée en tant que texte brut et non en tant que fichier .ppk.
1. Ouvrez le fichier enregistré avec un éditeur de texte et vérifiez son format :
   * Le fichier doit commencer par `-----BEGIN RSA PRIVATE KEY-----` (cinq tirets avant et après).
   * Il ne devrait pas y avoir de libellé indiquant le chiffrement.
   * Le fichier doit se terminer par `-----END RSA PRIVATE KEY-----` (cinq tirets avant et après).
1. Copiez le **contenu entier du fichier** (y compris les marqueurs `-----BEGIN/END RSA PRIVATE KEY-----`) et codez-le en Base64 à l’aide d’un outil tel que [Coder et décoder en Base64](https://www.base64encode.org/).

   >[!NOTE]
   >
   >Dans la sortie de codage Base64, supprimez toute mise en forme MIME. La clé encodée doit être une seule chaîne continue.

1. Vous pouvez désormais coller la clé SSH codée en Base64 dans le champ dédié de Journey Optimizer.

>[!CAUTION]
>
>Après l&#39;encodage Base64, la clé ne contiendra plus les marqueurs `-----BEGIN/END RSA PRIVATE KEY-----` et ne devra pas inclure de sauts de ligne. La clé publique correspondante doit être ajoutée au fichier des clés autorisées de votre serveur SFTP.

Pour plus d’informations sur la connexion de votre compte SFTP à Experience Platform, consultez [cette documentation](https://experienceleague.adobe.com/en/docs/experience-platform/sources/connectors/cloud-storage/sftp).

+++

## Créer une configuration de publipostage direct {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Définir les paramètres du publipostage direct"
>abstract="Une configuration de publipostage direct contient les paramètres de formatage du fichier qui contient les données de l’audience ciblée et qui seront utilisées par le fournisseur du publipostage direct. Vous devez également définir l’endroit où le fichier sera exporté en sélectionnant la configuration du routage du fichier."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/channels/direct-mail/direct-mail-configuration#file-routing-configuration" text="Configurer le routage des fichiers"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="Définir le seuil de partage des fichiers"
>abstract="Vous devez définir le nombre maximum d’enregistrements pour chaque fichier contenant les données d’audience. Vous pouvez sélectionner un nombre compris entre 1 et 200 000 enregistrements. Une fois le seuil spécifié atteint, un autre fichier sera créé pour les enregistrements restants."

Pour pouvoir diffuser un publipostage direct avec [!DNL Journey Optimizer], vous devez créer une configuration de canal pour définir les paramètres de formatage du fichier qui sera utilisé par le fournisseur du courrier.

Une configuration de publipostage direct doit également inclure la configuration du routage des fichiers qui définit le serveur sur lequel votre fichier de publipostage direct sera exporté.

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez **[!UICONTROL Paramètres généraux]** > **[!UICONTROL Configurations de canal]**. Cliquez sur le bouton **[!UICONTROL Créer une configuration de canal]**. [En savoir plus](../configuration/channel-surfaces.md)

   ![](assets/direct-mail-config-1.png)

1. Saisissez un nom et une description (facultatif) pour la configuration, puis sélectionnez le canal à configurer.

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à la configuration, vous pouvez sélectionner **[!UICONTROL Gérer l’accès]**. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../administration/object-based-access.md)

1. Sélectionnez le canal **[!UICONTROL Publipostage direct]**.

   ![](assets/direct-mail-config-2.png)

1. Sélectionnez une **[!UICONTROL Action marketing]** ou plusieurs pour associer des politiques de consentement aux messages utilisant cette configuration. Toutes les politiques de consentement associées à cette action marketing sont utilisées afin de respecter les préférences de vos clientes et clients. [En savoir plus](../action/consent.md#surface-marketing-actions)

1. Définissez les paramètres du publipostage direct dans la section dédiée de la configuration du canal.

   ![](assets/surface-direct-mail-settings.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. Sélectionnez le format du fichier : **[!UICONTROL CSV]** ou **[!UICONTROL Texte délimité]**.

1. Si vous sélectionnez **[!UICONTROL Texte délimité]**, définissez le séparateur de colonne de votre choix : tabulation, point-virgule, barre verticale ou esperluette.

   ![](assets/surface-direct-mail-column-separator.png)

1. Sélectionnez la **[!UICONTROL Configuration du routage des fichiers]** parmi celles que vous avez créées. Ceci définit l’endroit où le fichier sera exporté pour que votre fournisseur de publipostage direct l’utilise.

   >[!CAUTION]
   >
   >Si vous n’avez configuré aucune option de routage de fichier, vous ne pourrez pas créer de configuration de publipostage direct. [En savoir plus](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. Envoyez la configuration de publipostage direct.

Vous pouvez désormais [créer un publipostage direct](../direct-mail/create-direct-mail.md) dans une campagne. Une fois la campagne lancée, le fichier contenant les données de l’audience ciblée sera automatiquement exporté vers le serveur que vous avez défini. Le fournisseur de publipostage direct pourra alors récupérer ce fichier et poursuivre la diffusion du publipostage direct.

>[!NOTE]
>
>Les lignes en double où toutes les valeurs de la ligne sont identiques sont automatiquement supprimées du fichier.

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.

-->