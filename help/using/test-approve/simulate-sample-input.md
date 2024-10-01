---
solution: Journey Optimizer
product: journey optimizer
title: Tester votre contenu à l’aide d’exemples de données d’entrée
description: Découvrez comment prévisualiser le contenu d’un email et envoyer des bons à tirer à l’aide d’exemples de données d’entrée.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Version bêta"
hide: true
hidefromtoc: true
source-git-commit: 100c9ca994199a3b90650ebfbabbf0b7ac8726c2
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 8%

---


# Tester votre contenu à l’aide d’exemples de données d’entrée {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simuler à l’aide d’un exemple d’entrée"
>abstract="Dans cet écran, vous pouvez tester différentes variantes du contenu de votre e-mail en fournissant des valeurs pour les champs de personnalisation via un modèle CSV (télécharger un fichier CSV) ou en saisissant manuellement les valeurs."

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement disponible en version bêta pour les utilisateurs sélectionnés uniquement.

Parcours optimizer vous permet de tester différentes variantes du contenu de votre email en le prévisualisant et en envoyant des bons à tirer à l’aide d’exemples de données d’entrée téléchargées à partir d’un fichier CSV ou ajoutées manuellement. Tous les attributs de profil utilisés dans votre contenu pour la personnalisation sont automatiquement détectés par le système et peuvent être utilisés pour vos tests afin de créer plusieurs variantes.

Pour accéder à cette expérience, cliquez sur le bouton **[!UICONTROL Simuler le contenu]** et sélectionnez **[!UICONTROL Simuler avec CSV(Beta)]**.

![](assets/simulate-sample.png)

Les principales étapes pour tester votre contenu sont les suivantes :

1. Ajoutez jusqu’à 30 variantes avec des exemples de données d’entrée, soit en chargeant un fichier CSV, soit en ajoutant manuellement les données. [Découvrez comment ajouter des variantes](#profiles)
1. Vérifiez l&#39;aperçu de votre contenu à l&#39;aide des différentes variantes. [Découvrez comment prévisualiser votre contenu](#preview)
1. Envoyer jusqu&#39;à 10 BAT aux adresses email à l&#39;aide des différentes variantes. [Découvrir comment envoyer des BAT](#proofs)


## Mécanismes de sécurisation et limitations {#limitations}

Avant de commencer à tester votre contenu à l’aide des exemples de données d’entrée, tenez compte des barrières de sécurité et des conditions préalables suivantes.

* Pour l’instant, le test à l’aide de données d’entrée d’exemple n’est disponible que pour le canal email. L’expérience est inaccessible à partir du bouton &quot;Simuler le contenu&quot; dans le Designer email.
* Les fonctionnalités suivantes ne sont pas disponibles dans l&#39;expérience actuelle : Inbox rendering, rapports sur les spams, contenu multilingue et expérience de contenu. Pour utiliser ces fonctionnalités, cliquez sur le bouton **[!UICONTROL Simuler le contenu]** de votre contenu pour accéder à l’interface utilisateur précédente.
* Seuls les attributs de profil sont actuellement pris en charge. Si des attributs contextuels sont utilisés dans votre contenu à des fins de personnalisation, vous ne pourrez pas tester votre contenu à l’aide de ces attributs.
* Seuls les types de données suivants sont pris en charge lors de la saisie de données pour vos variantes : nombre (entier et décimal), chaîne, valeur booléenne et type de date. Tout autre type de données affiche une erreur.

## Ajouter des variantes {#profiles}

Vous pouvez ajouter jusqu’à 30 variantes pour tester votre contenu, soit à l’aide d’un fichier CSV, soit manuellement :

* Pour télécharger des exemples de données d’entrée à partir d’un fichier CSV, cliquez sur le lien **[!UICONTROL Télécharger CSV]** pour récupérer un modèle de fichier CSV. Ces modèles incluent une colonne pour chaque attribut de profil utilisé dans votre contenu pour la personnalisation.

  Renseignez le fichier CSV, puis cliquez sur le **[!UICONTROL Charger les données d’entrée]** pour le charger afin de tester votre contenu.

* Pour ajouter manuellement une variante, cliquez sur le bouton **[!UICONTROL Créer un exemple d’entrée]** et renseignez les exemples de données d’entrée pour la variante. Un champ s’affiche pour chaque attribut de profil utilisé dans votre contenu pour la personnalisation.

  ![](assets/simulate-custom-add.png)

Une fois les profils sélectionnés, une zone s&#39;affiche pour chaque variante sur le côté gauche de l&#39;écran. Vous pouvez utiliser ces profils pour prévisualiser votre contenu et envoyer des bons à tirer.

>[!NOTE]
>
>Les variantes ajoutées servent uniquement à des fins de test pour votre contenu actuel. Les ne sont pas stockés dans Adobe Experience Platform, mais dans la session de votre navigateur utilisateur, ce qui signifie qu’ils ne s’afficheront pas lors de la déconnexion ou si vous travaillez sur un autre appareil.

## Prévisualiser vos variantes de contenu {#preview}

Pour prévisualiser votre contenu à l&#39;aide de l&#39;une des variantes, cochez la case correspondante afin de mettre à jour l&#39;aperçu du contenu dans la section droite avec les informations renseignées pour cette variante.

Vous pouvez supprimer une variante à tout moment à l’aide du bouton représentant des points de suspension dans le coin supérieur droit et en sélectionnant **[!UICONTROL Supprimer]**. Pour éditer les informations d&#39;une variante, cliquez sur le bouton représentant des points de suspension et sélectionnez **[!UICONTROL Modifier]**.

![](assets/simulate-custom-boxes.png)

## Envoyer des BAT {#proofs}

Journey Optimizer permet d&#39;envoyer des BAT à des adresses email tout en empruntant l&#39;identité d&#39;une ou plusieurs variantes ajoutées dans l&#39;écran de simulation. Les étapes sont les suivantes :

1. Vérifiez que des variantes ont été ajoutées pour tester votre contenu et cliquez sur le bouton **[!UICONTROL Envoyer le bon à tirer]** .

1. Dans le champ **[!UICONTROL Destinataires]**, saisissez l&#39;adresse email à laquelle vous souhaitez envoyer le BAT, puis cliquez sur **[!UICONTROL Ajouter]**. Répétez l’opération pour envoyer le BAT à des adresses email supplémentaires. Vous pouvez ajouter jusqu’à 10 destinataires de BAT.

1. Dans la section inférieure de l&#39;écran, sélectionnez la variante que vous souhaitez utiliser dans le BAT. Vous pouvez sélectionner plusieurs variantes, auquel cas l&#39;email contiendra autant de BAT que de variantes sélectionnées.

   Pour plus d&#39;informations sur une variante, cliquez sur le lien **[!UICONTROL Afficher les détails du profil]** . Vous pouvez ainsi afficher les informations saisies dans l&#39;écran précédent pour les différentes variantes.

   ![](assets/simulate-custom-proofs.png)

1. Cliquez sur le bouton **[!UICONTROL Envoyer le bon à tirer]** pour commencer à envoyer le bon à tirer.

1. Pour suivre l&#39;envoi du BAT, cliquez sur le bouton **[!UICONTROL Afficher les bons à tirer]** dans l&#39;écran de simulation de contenu.

![](assets/simulate-custom-sent-proofs.png)
