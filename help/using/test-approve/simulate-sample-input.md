---
solution: Journey Optimizer
product: journey optimizer
title: Testez votre contenu à l’aide d’exemples de données d’entrée (Beta)
description: Découvrez comment prévisualiser du contenu et envoyer un BAT d’email à l’aide d’exemples de données d’entrée à partir d’un fichier CSV ou JSON ou ajouté manuellement.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="Version bêta"
source-git-commit: 678a2fbce1b4048aad6a2214bb41ec3722db2b2d
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 49%

---


# Testez votre contenu à l’aide d’exemples de données d’entrée (Beta) {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simuler à l’aide d’un exemple d’entrée"
>abstract="Dans cet écran, vous pouvez tester différentes variantes de votre contenu en fournissant des valeurs pour les champs de personnalisation par le biais d’un modèle CSV ou JSON, ou en saisissant manuellement les valeurs."

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement disponible pour tous les clients en version bêta publique.

L’optimiseur de parcours vous permet de tester différentes variantes de votre contenu en le prévisualisant et en envoyant des bons à tirer à l’aide d’exemples de données d’entrée téléchargées à partir d’un fichier CSV ou JSON ou ajoutées manuellement. Tous les attributs de profil utilisés dans votre contenu pour la personnalisation sont automatiquement détectés par le système et peuvent être utilisés pour vos tests afin de créer plusieurs variantes.

>[!NOTE]
>
>Pour l’instant, la simulation des variations de contenu n’est disponible que pour les canaux Email, SMS et Notification push .

Pour accéder à cette expérience, cliquez sur le bouton **[!UICONTROL Simuler le contenu]** et sélectionnez **[!UICONTROL Simuler les variations de contenu (Beta)]**.

![](assets/simulate-sample.png)

Les principales étapes pour tester votre contenu sont les suivantes :

1. Ajoutez jusqu’à 30 variantes avec des exemples de données d’entrée, soit en chargeant un fichier, soit en ajoutant manuellement les données. [Découvrir comment ajouter des variantes](#profiles)
1. Vérifiez l’aperçu de votre contenu à l’aide des différentes variantes. [Découvrir comment prévisualiser votre contenu](#preview)
1. Pour le contenu des emails, envoyez jusqu’à 10 BAT aux adresses email à l’aide des différentes variantes. [Découvrir comment envoyer des épreuves](#proofs)


## Mécanismes de sécurisation et limitations {#limitations}

Avant de commencer à tester votre contenu à l’aide des exemples de données d’entrée, tenez compte des mécanismes de sécurisation et des conditions préalables suivants.

* Pour l’instant, le test à l’aide d’exemples de données d’entrée n’est disponible que pour les canaux Email, SMS et Notification push. L’expérience est inaccessible à partir du bouton « Simuler le contenu » dans le concepteur d’e-mail.
* Les fonctionnalités suivantes ne sont pas disponibles dans l’expérience actuelle : rendu de boîte de réception, rapports sur les spams, contenu multilingue et expérience de contenu. Pour utiliser ces fonctionnalités, sélectionnez le bouton **[!UICONTROL Simuler le contenu]** de votre contenu pour accéder à l’interface d’utilisation précédente.
* Seuls les attributs de profil sont actuellement pris en charge. Si des attributs contextuels sont utilisés dans votre contenu à des fins de personnalisation, vous ne pourrez pas tester votre contenu à l’aide de ces attributs.
* Seuls les types de données suivants sont pris en charge lors de la saisie de données pour vos variantes : nombre (entier et décimal), chaîne, valeur booléenne et type de date. Tout autre type de données affiche une erreur.

## Ajouter des variantes {#profiles}

Vous pouvez ajouter jusqu’à 30 variantes pour tester votre contenu, soit à l’aide d’un fichier, soit manuellement.

>[!NOTE]
>
>Les variantes ajoutées servent uniquement à des fins de test pour votre contenu actuel. Les ne sont pas stockés dans Adobe Experience Platform, mais dans la session de votre navigateur utilisateur, ce qui signifie qu’ils ne s’afficheront pas lors de la déconnexion ou lorsque vous travaillez à partir d’un autre appareil.

### Ajouter une variante à l&#39;aide d&#39;un fichier {#file}

Pour ajouter une variante à partir d&#39;un fichier, procédez comme suit :

1. Cliquez sur le lien **[!UICONTROL télécharger l’exemple]** pour récupérer un modèle de fichier, puis sélectionnez le format de fichier à utiliser (CSV, JSON ou JSONLINES).

1. Cliquez sur **[!UICONTROL Télécharger]** , puis stockez le modèle à l’emplacement souhaité.

1. Ouvrez le fichier, puis remplissez le modèle en fonction de vos besoins. Le modèle comprend une colonne pour chaque attribut de profil utilisé dans votre contenu pour la personnalisation.

1. Lorsque votre fichier est prêt, cliquez sur le **[!UICONTROL Charger les données d’entrée]** pour le charger afin de tester votre contenu.

1. Une fois le fichier téléchargé, une zone est ajoutée dans le volet de gauche pour chaque ligne du fichier. Chaque zone contient tous les attributs de profil utilisés dans votre contenu pour la personnalisation. Vous pouvez maintenant utiliser les variantes pour prévisualiser votre contenu dans le volet de droite et envoyer des bons à tirer.

   ![](assets/simulate-custom-variants.png)

### Ajouter manuellement des variantes {#manual}

Pour ajouter manuellement une variante, procédez comme suit :

1. Cliquez sur le bouton **[!UICONTROL Créer un exemple d’entrée]** .

   Une zone est ajoutée dans le volet de gauche avec tous les attributs de profil utilisés dans votre contenu pour la personnalisation.

1. Renseignez les exemples de données d&#39;entrée pour la variante et cliquez sur **[!UICONTROL Enregistrer]**.

   ![](assets/simulate-custom-add.png)

1. Une fois les variantes ajoutées, vous pouvez les utiliser pour prévisualiser votre contenu dans le volet de droite et envoyer des bons à tirer.

## Prévisualiser les variantes de votre contenu {#preview}

Pour prévisualiser votre contenu à l’aide de l’une des variantes, cochez la case correspondante afin de mettre à jour la prévisualisation du contenu dans la section de droite avec les informations renseignées pour cette variante.

Vous pouvez supprimer une variante à tout moment à l’aide du bouton représentant des points de suspension dans le coin supérieur droit et en sélectionnant **[!UICONTROL Supprimer]**. Pour modifier les informations d’une variante, cliquez sur le bouton représentant des points de suspension et sélectionnez **[!UICONTROL Modifier]**.

![](assets/simulate-custom-boxes.png)

## Envoyer des épreuves {#proofs}

Journey Optimizer permet d’envoyer des épreuves à des adresses e-mail tout en empruntant l’identité d’une ou plusieurs variantes ajoutées dans l’écran de simulation. Les étapes sont les suivantes :

1. Vérifiez que des variantes ont été ajoutées pour tester votre contenu et cliquez sur le bouton **[!UICONTROL Envoyer une épreuve]**.

1. Dans le champ **[!UICONTROL Destinataires]**, saisissez l’adresse e-mail à laquelle vous souhaitez envoyer l’épreuve, puis cliquez sur **[!UICONTROL Ajouter]**. Répétez l’opération pour envoyer l’épreuve à d’autres adresses e-mail. Vous pouvez ajouter jusqu’à 10 destinataires d’épreuve.

1. Dans la section inférieure de l’écran, sélectionnez la variante que vous souhaitez utiliser dans l’épreuve. Vous pouvez sélectionner plusieurs variantes, auquel cas l’e-mail contiendra autant d’épreuves que de variantes sélectionnées.

   Pour plus d’informations sur une variante, cliquez sur le lien **[!UICONTROL Afficher les détails du profil]**. Vous pouvez ainsi afficher les informations saisies dans l’écran précédent pour les différentes variantes.

   ![](assets/simulate-custom-proofs.png)

1. Cliquez sur le bouton **[!UICONTROL Envoyer une épreuve]** pour commencer à envoyer l’épreuve.

1. Pour suivre l’envoi de l’épreuve, cliquez sur le bouton **[!UICONTROL Afficher les épreuves]** dans l’écran de simulation de contenu.

![](assets/simulate-custom-sent-proofs.png)
