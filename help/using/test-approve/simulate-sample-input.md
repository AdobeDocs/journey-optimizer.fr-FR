---
solution: Journey Optimizer
product: journey optimizer
title: Tester votre contenu à l’aide d’exemples de données d’entrée
description: Découvrez comment prévisualiser le contenu d’un e-mail et envoyer des épreuves à l’aide d’exemples de données d’entrée.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Version bêta"
hide: true
hidefromtoc: true
source-git-commit: 100c9ca994199a3b90650ebfbabbf0b7ac8726c2
workflow-type: ht
source-wordcount: '769'
ht-degree: 100%

---


# Tester votre contenu à l’aide d’exemples de données d’entrée {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simuler à l’aide d’un exemple d’entrée"
>abstract="Dans cet écran, vous pouvez tester différentes variantes du contenu de votre e-mail en fournissant des valeurs pour les champs de personnalisation via un modèle CSV (télécharger un fichier CSV) ou en saisissant manuellement les valeurs."

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement disponible en version bêta pour certains utilisateurs et utilisatrices uniquement.

Journey Optimizer vous permet de tester différentes variantes du contenu de votre e-mail en le prévisualisant et en envoyant des épreuves à l’aide d’exemples de données d’entrée chargées à partir d’un fichier CSV ou ajoutées manuellement. Tous les attributs de profil utilisés dans votre contenu pour la personnalisation sont automatiquement détectés par le système et peuvent être utilisés pour vos tests afin de créer plusieurs variantes.

Pour accéder à cette expérience, cliquez sur le bouton **[!UICONTROL Simuler le contenu]** et sélectionnez **[!UICONTROL Simuler avec un fichier CSV (version bêta)]**.

![](assets/simulate-sample.png)

Les principales étapes pour tester votre contenu sont les suivantes :

1. Ajoutez jusqu’à 30 variantes avec des exemples de données d’entrée, soit en chargeant un fichier CSV, soit en ajoutant manuellement les données. [Découvrir comment ajouter des variantes](#profiles)
1. Vérifiez l’aperçu de votre contenu à l’aide des différentes variantes. [Découvrir comment prévisualiser votre contenu](#preview)
1. Envoyez jusqu’à 10 épreuves aux adresses e-mail à l’aide des différentes variantes. [Découvrir comment envoyer des épreuves](#proofs)


## Mécanismes de sécurisation et limitations {#limitations}

Avant de commencer à tester votre contenu à l’aide des exemples de données d’entrée, tenez compte des mécanismes de sécurisation et des conditions préalables suivants.

* Pour l’instant, le test à l’aide d’exemples de données d’entrée n’est disponible que pour le canal e-mail. L’expérience est inaccessible à partir du bouton « Simuler le contenu » dans le concepteur d’e-mail.
* Les fonctionnalités suivantes ne sont pas disponibles dans l’expérience actuelle : rendu de boîte de réception, rapports sur les spams, contenu multilingue et expérience de contenu. Pour utiliser ces fonctionnalités, sélectionnez le bouton **[!UICONTROL Simuler le contenu]** de votre contenu pour accéder à l’interface d’utilisation précédente.
* Seuls les attributs de profil sont actuellement pris en charge. Si des attributs contextuels sont utilisés dans votre contenu à des fins de personnalisation, vous ne pourrez pas tester votre contenu à l’aide de ces attributs.
* Seuls les types de données suivants sont pris en charge lors de la saisie de données pour vos variantes : nombre (entier et décimal), chaîne, valeur booléenne et type de date. Tout autre type de données affiche une erreur.

## Ajouter des variantes {#profiles}

Vous pouvez ajouter jusqu’à 30 variantes pour tester votre contenu, soit à l’aide d’un fichier CSV, soit manuellement :

* Pour charger des exemples de données d’entrée à partir d’un fichier CSV, cliquez sur le lien **[!UICONTROL Télécharger CSV]** pour récupérer un modèle de fichier CSV. Ces modèles incluent une colonne pour chaque attribut de profil utilisé dans votre contenu à des fins de personnalisation.

  Renseignez le fichier CSV, puis cliquez sur **[!UICONTROL Charger les données d’entrée]** pour les charger afin de tester votre contenu.

* Pour ajouter manuellement une variante, cliquez sur le bouton **[!UICONTROL Créer un exemple d’entrée]** et renseignez les exemples de données d’entrée pour la variante. Un champ s’affiche pour chaque attribut de profil utilisé dans votre contenu à des fins de personnalisation.

  ![](assets/simulate-custom-add.png)

Une fois les profils sélectionnés, une zone s’affiche pour chaque variante sur le côté gauche de l’écran. Vous pouvez utiliser ces profils pour prévisualiser votre contenu et envoyer des épreuves.

>[!NOTE]
>
>Les variantes ajoutées servent uniquement à des fins de test pour votre contenu actuel. Les variantes ne sont pas stockées dans Adobe Experience Platform, mais dans la session de votre navigateur, ce qui signifie qu’elles ne s’afficheront pas lors de la déconnexion ou si vous travaillez sur un autre appareil.

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
