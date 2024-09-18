---
solution: Journey Optimizer
product: journey optimizer
title: Créer du contenu multilingue avec traduction automatisée
description: En savoir plus sur le contenu multilingue dans Journey Optimizer
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: commencer, démarrer, contenu, expérience
exl-id: 38e82eb2-67d9-4a7d-8c1f-77dab20bcec4
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: a190b5547c2d8e13563391bd9d784add75c55fd4
workflow-type: ht
source-wordcount: '1617'
ht-degree: 100%

---

# Créer du contenu multilingue avec traduction automatisée {#multilingual-automated}

>[!CONTEXTUALHELP]
>id="ajo_multi_add_provider"
>title="Ajouter un fournisseur"
>abstract="Ajoutez des fournisseurs de traduction et des paramètres régionaux si nécessaire. Vous pouvez ainsi gérer les fournisseurs et paramètres régionaux actifs pour votre projet, ce qui vous donne la possibilité d’ajuster les ressources et de cibler les audiences en fonction de vos besoins actuels et de la portée de votre projet."

>[!CONTEXTUALHELP]
>id="ajo_multi_edit_provider"
>title="Modifier un fournisseur"
>abstract="Modifiez les fournisseurs de traduction existants et ajoutez des paramètres régionaux selon les besoins. Cette fonctionnalité vous permet de contrôler les fournisseurs et paramètres régionaux actifs pour votre projet, ce qui vous offre la possibilité d’ajuster les ressources et de cibler des audiences spécifiques en fonction de vos besoins actuels et des objectifs du projet."

>[!AVAILABILITY]
>
>Le contenu multilingue n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

Avec le flux automatisé, vous pouvez simplement sélectionner la langue cible et le fournisseur de langues. Votre contenu est alors directement envoyé pour être traduit, prêt à être révisé une fois terminé.

Pour créer du contenu multilingue à l’aide de la traduction automatisée, procédez comme suit :

1. [Créer vos paramètres régionaux](#create-locale).

1. [Créez un projet de langue](#create-translation-project).

1. [Créez des paramètres de langue](#create-language-settings).

1. [Créez un contenu multilingue](#create-a-multilingual-campaign).

1. [Vérifiez votre tâche de traduction (facultatif)](#review-translation-project).

## Créer un paramètre régional {#create-locale}

>[!CONTEXTUALHELP]
>id="ajo_multi_add_locale"
>title="Ajouter un paramètre régional"
>abstract="Lors de la configuration de vos préférences linguistiques, vous avez la possibilité de créer des paramètres régionaux supplémentaires si ceux qui vous sont demandés ne sont pas disponibles pour votre contenu multilingue."

Lors de la configuration des paramètres de langue, comme décrit dans la section [Créer vos paramètres de langue](#language-settings), si un paramètre régional spécifique n’est pas disponible pour votre contenu multilingue, vous avez la possibilité de créer autant de paramètres régionaux que nécessaire à l’aide du menu **[!UICONTROL Traduction]**.

1. Dans le menu **[!UICONTROL Gestion de contenu]**, accédez à **[!UICONTROL Traduction]**.

1. Dans l’onglet **[!UICONTROL Dictionnaire des paramètres régionaux]**, cliquez sur **[!UICONTROL Ajouter un paramètre régional]**.

   ![](assets/locale_1.png)

1. Sélectionnez votre code de paramètre régional dans la liste **[!UICONTROL Langue]** et la **[!UICONTROL Région]** associée.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour créer votre paramètre régional.

   ![](assets/locale_2.png)

## Créer un projet de traduction {#translation-project}

>[!CONTEXTUALHELP]
>id="ajo_multi_create_project"
>title="Créer un projet"
>abstract="Pour commencer à créer du contenu multilingue, démarrez votre projet de traduction en identifiant les paramètres régionaux cible, en sélectionnant la langue appropriée ou le dialecte régional pour votre audience. Ensuite, choisissez un fournisseur de traduction qui s’aligne sur les besoins de votre projet."

>[!CONTEXTUALHELP]
>id="ajo_multi_edit_project"
>title="Modifier un projet"
>abstract="Mettez à jour votre projet de traduction pour incorporer d’autres paramètres régionaux, ce qui vous permet de développer votre contenu pour atteindre une audience plus large."

Démarrez votre projet de traduction en spécifiant les paramètres régionaux cibles, en indiquant la langue ou la région spécifique pour votre contenu. Vous pouvez ensuite choisir votre fournisseur de traduction.

1. Dans le menu **[!UICONTROL Traduction]**, sous **[!UICONTROL Gestion de contenu]**, cliquez sur **[!UICONTROL Créer un projet]** dans l’onglet **[!UICONTROL Projets]**.

   ![](assets/translation_project_1.png)

1. Saisissez un **[!UICONTROL nom]** et une **[!UICONTROL description]**.

1. Sélectionnez le **[!UICONTROL paramètre régional source]**.

   ![](assets/translation_project_2.png)

1. Choisissez si vous souhaitez activer les options suivantes :

   * **[!UICONTROL Publier automatiquement les traductions approuvées]** : une fois les traductions approuvées, elles sont automatiquement intégrées dans la campagne sans intervention manuelle.
   * **[!UICONTROL Activer le processus de révision]** : applicable uniquement aux paramètres régionaux avec traduction humaine. Cela permet à un réviseur ou à une réviseuse interne d’évaluer et d’approuver ou de rejeter efficacement le contenu traduit. [En savoir plus](#review-translation-project)

1. Cliquez sur **[!UICONTROL Ajouter un paramètre régional]** pour accéder au menu et définir les langues de votre projet de traduction.

   Si un **[!UICONTROL paramètre régional]** est manquant, vous pouvez le créer manuellement au préalable à partir du menu **[!UICONTROL Traduction]** ou par API. Voir [Créer un paramètre régional](#create-locale).

   ![](assets/translation_project_3.png)

1. Sélectionnez dans la liste vos **[!UICONTROL paramètres régionaux cibles]** et choisissez le **[!UICONTROL prestataire de services de traduction]** que vous souhaitez utiliser pour chaque paramètre régional.

   Les paramètres du **[!UICONTROL prestataire de services de traduction]** sont accessibles à partir du menu **[!UICONTROL Traduction]** dans la section du menu **[!UICONTROL Administration]**.

   >[!NOTE]
   >
   >La gestion des contrats avec le prestataire de services de traduction n’entre pas dans le cadre de cette fonctionnalité. Assurez-vous que vous disposez d’un contrat valide et actif avec le partenaire de services de traduction désigné.
   >
   ></br>Le prestataire de services de traduction détient la propriété de la qualité du contenu traduit.

1. Cliquez sur **[!UICONTROL Ajouter un paramètre régional]** lorsque vous avez terminé de lier votre paramètre régional cible au prestataire de services de traduction approprié. Cliquez ensuite sur **[!UICONTROL Enregistrer]**.

   Notez que si un fournisseur est grisé pour un paramètre régional cible, cela indique que le fournisseur ne prend pas en charge ce paramètre régional particulier.

   ![](assets/translation_project_4.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** lorsque votre projet de traduction est configuré.

Votre projet de traduction est maintenant créé et peut être utilisé dans une campagne multilingue.

## Créer des paramètres de langue {#language-settings}

Dans cette section, vous pouvez définir votre langue principale et les paramètres régionaux associés pour gérer votre contenu multilingue. Vous pouvez également choisir l’attribut que vous souhaitez utiliser pour rechercher des informations relatives à la langue du profil.

1. Dans le menu **[!UICONTROL Administration]**, accédez à **[!UICONTROL Canal]** > **[!UICONTROL Paramètres généraux]**.

1. Dans le menu **[!UICONTROL Paramètres de langue]**, cliquez sur **[!UICONTROL Créer des paramètre de langue]**.

   ![](assets/language_settings_1.png)

1. Saisissez le nom de vos **[!UICONTROL Paramètres de langue]**.

1. Choisissez l’option **[!UICONTROL Projet de traduction]**.

1. Dans le champ **[!UICONTROL Projet de traduction]**, cliquez sur **[!UICONTROL Modifier]** et sélectionnez le **[!UICONTROL projet de traduction]** créé précédemment.

   Les paramètres régionaux précédemment configurés sont automatiquement importés.

   ![](assets/language_settings_2.png)

1. Dans le menu **[!UICONTROL Préférence d’envoi]**, sélectionnez l’attribut à rechercher pour trouver des informations sur les langues de profil.

1. Cliquez sur **[!UICONTROL Modifier]** en regard de votre **[!UICONTROL Paramètre régional]** pour le personnaliser davantage et ajouter des **[!UICONTROL Préférences de profil]**.

   ![](assets/language_settings_3.png)

1. Si votre **[!UICONTROL projet de traduction]** est mis à jour, cliquez sur **[!UICONTROL Actualiser]** pour refléter ces modifications dans vos **[!UICONTROL Paramètres de langue]**.

   ![](assets/language_settings_4.png)

1. Cliquez sur **[!UICONTROL Envoyer]** pour créer vos **[!UICONTROL paramètres de langue]**.

<!--
1. Access the **[!UICONTROL channel configurations]** menu and create a new channel configuration or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.


1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Créer un contenu multilingue {#create-multilingual-campaign}

Une fois que vous avez configuré votre projet de traduction et les paramètres de langue, vous pouvez créer votre campagne ou votre parcours et personnaliser votre contenu pour vos différents paramètres régionaux.

1. Commencez par créer et configurer votre [campagne](../campaigns/create-campaign.md) par e-mail, SMS ou notification push ou votre [parcours](../building-journeys/journeys-message.md), selon vos besoins.

1. Une fois votre contenu principal créé, cliquez sur **[!UICONTROL Enregistrer]** et revenez à l’écran de configuration de la campagne

1. Cliquez sur **[!UICONTROL Ajouter des langues]**.  [En savoir plus](#create-language-settings)

   ![](assets/multilingual-campaign-automated-1.png)

1. Sélectionnez les **[!UICONTROL Paramètres de langue]** précédemment créés.

   ![](assets/multilingual-campaign-automated-2.png)

1. Maintenant que vos Paramètres régionaux sont importés, cliquez sur **[!UICONTROL Envoyer pour traduction]** pour transférer votre contenu au fournisseur de traduction sélectionné précédemment.

   ![](assets/multilingual-campaign-automated-3.png)

1. Une fois que votre contenu est envoyé pour traduction, il n’est plus modifiable. Pour apporter des modifications au contenu d’origine, cliquez sur l’icône de verrouillage.

   Notez que si vous souhaitez apporter des modifications à ce contenu, vous devez créer un projet de traduction et le renvoyer pour traduction.

   ![](assets/multilingual-campaign-automated-4.png)

1. Cliquez sur **[!UICONTROL Ouvrir la traduction]** pour accéder à votre projet de traduction et le réviser.

   ![](assets/multilingual-campaign-automated-5.png)

1. Dans cette page, suivez le statut de votre projet de traduction :

   * **[!UICONTROL Traduction en cours]** : votre fournisseur travaille activement sur la traduction.

     Si vous avez sélectionné **Approvisionnement** lors de la configuration des **paramètres de langue**, vous pouvez traduire votre contenu directement dans votre projet de traduction. [En savoir plus](#manage-ht-project)

   * **[!UICONTROL Prêt pour la révision]** : le processus de révision est prêt à commencer, ce qui vous permet d’accéder à la traduction et de la rejeter ou de l’approuver.

     Si vous avez sélectionné l’option **[!UICONTROL Activer le workflow de révision]** dans votre **[!UICONTROL projet de traduction]**, vous pouvez réviser la traduction directement dans Journey Optimizer une fois la traduction effectuée par le prestataire de services de traduction sélectionné. [En savoir plus](#review-translation-project)

   * **[!UICONTROL Révisé]** : la traduction a été approuvée et peut être publiée et envoyée à la campagne.

   * **[!UICONTROL Prêt à publier]** : la traduction automatique est terminée et peut désormais être envoyée à votre campagne.

   * **[!UICONTROL Terminé]** : la traduction est désormais disponible dans votre campagne.

   ![](assets/multilingual-campaign-automated-6.png)

1. Une fois votre traduction terminée, votre contenu multilingue est prêt à être envoyé.

   ![](assets/translation_review_9.png)

1. Cliquez sur **[!UICONTROL Examiner pour activer]** pour afficher un résumé de la campagne.

   Le résumé vous permet de modifier votre campagne si nécessaire et de vérifier si un paramètre est incorrect ou manquant.

1. Parcourez votre contenu multilingue pour afficher le rendu dans chaque langue.

   ![](assets/multilingual-campaign-automated-7.png)

1. Vérifiez que votre campagne est correctement configurée, puis cliquez sur **[!UICONTROL Activer]**.

Vous pouvez maintenant activer votre campagne ou votre parcours. Après l’envoi, vous pouvez mesurer l’impact de votre parcours ou de votre campagne multilingue dans les rapports.

## Gérer un projet de traduction d’approvisionnement {#manage-ht-project}

>[!CONTEXTUALHELP]
>id="ajo_multi_insourcing_project"
>title="Approvisionner un projet de traduction"
>abstract="L’approvisionnement d’un projet de traduction vous permet de gérer et d’exécuter des traductions directement dans votre projet de traduction, en rationalisant le processus et en maintenant un meilleur contrôle sur la qualité et la cohérence de la traduction."

Si vous avez sélectionné Approvisionnement lors de la configuration des paramètres de langue, vous pouvez traduire votre contenu directement dans votre projet de traduction.

1. Dans votre **[!UICONTROL Projet de traduction]**, accédez au menu **[!UICONTROL Plus d’actions]** et sélectionnez **[!UICONTROL Approvisionnement]**.

   ![](assets/inhouse-translation-1.png)

1. Vous pouvez exporter votre fichier CSV pour la traduction à l’aide de logiciels de traduction externes. Vous pouvez également réimporter le fichier CSV dans votre projet de traduction en cliquant sur le bouton **[!UICONTROL Importer le CSV]**.

   ![](assets/inhouse-translation-3.png)

1. Cliquez sur **[!UICONTROL Modifier]** pour ajouter le contenu de votre traduction.

   ![](assets/inhouse-translation-2.png)

1. Si vous souhaitez publier le texte traduit, cliquez sur **[!UICONTROL Finaliser]**.

## Réviser votre projet de traduction {#review-translation-project}

>[!CONTEXTUALHELP]
>id="ajo_multi_review_project"
>title="Réviser votre projet de traduction"
>abstract="Une fois la traduction terminée par votre fournisseur, vous pouvez consulter les résultats directement dans Journey Optimizer. Vous pouvez ainsi évaluer l’exactitude et la qualité de la traduction, en vous assurant qu’elle s’aligne sur vos attentes et les exigences du projet avant de la finaliser."

>[!CONTEXTUALHELP]
>id="ajo_multi_preview_project"
>title="Prévisualiser votre projet de traduction"
>abstract="La fenêtre Prévisualisation vous permet de visualiser l’affichage du contenu traduit dans chaque langue. Cette fonctionnalité vous permet d’examiner le rendu et de vous assurer que le contenu s’affiche correctement et efficacement dans toutes les langues sélectionnées."

Si vous avez sélectionné l’option **[!UICONTROL Activer le workflow de révision]** dans votre **[!UICONTROL projet de traduction]**, vous pouvez réviser la traduction directement dans Journey Optimizer une fois la traduction effectuée par le fournisseur de traduction sélectionné.

Notez que si cette option est désactivée, une fois la traduction effectuée par votre fournisseur, le statut de la tâche de traduction est automatiquement défini sur **[!UICONTROL Révisé]**, ce qui vous permet de poursuivre rapidement en cliquant sur **[!UICONTROL Publier]**.

1. Une fois votre traduction effectuée par votre fournisseur, vous pouvez accéder à la traduction pour révision à partir de votre **[!UICONTROL projet de traduction]** ou directement depuis votre **[!UICONTROL campagne]**.

   Dans le menu **[!UICONTROL Plus d’actions]**, cliquez sur **[!UICONTROL Réviser]**.

   ![](assets/translation_review_1.png)

1. Dans la fenêtre Réviser, parcourez votre contenu traduit et acceptez ou rejetez chaque chaîne de traduction.

   ![](assets/translation_review_3.png)

1. Cliquez sur **[!UICONTROL Modifier]** pour modifier le contenu de votre chaîne de traduction.

   ![](assets/translation_review_2.png)

1. Saisissez votre traduction mise à jour et cliquez sur **[!UICONTROL Confirmer]** lorsque vous avez terminé.

   ![](assets/translation_review_4.png)

1. Vous pouvez également choisir **[!UICONTROL Tout rejeter]** ou **[!UICONTROL Tout approuver]** directement.

   Lorsque vous sélectionnez **[!UICONTROL Tout rejeter]**, ajoutez un commentaire, puis cliquez sur **[!UICONTROL Rejeter]**.

1. Cliquez sur **[!UICONTROL Aperçu]** pour vérifier le rendu de votre contenu traduit dans chaque langue.

1. Si vous souhaitez publier le texte traduit, cliquez sur **[!UICONTROL Finaliser]**.

   ![](assets/translation_review_5.png)

1. Dans votre **[!UICONTROL projet de traduction]**, sélectionnez l’un de vos projets pour accéder à plus de détails. Si vous avez rejeté la traduction, vous pouvez choisir de la renvoyer pour traduction.

   ![](assets/translation_review_6.png)

1. Une fois que le statut de votre **[!UICONTROL projet de traduction]** est défini sur Révisé, vous pouvez l’envoyer à votre campagne.

   Dans le menu **[!UICONTROL Plus d’actions]**, cliquez sur **[!UICONTROL Publier]**.

   ![](assets/translation_review_7.png)

1. Dans votre campagne, vérifiez que le statut de votre traduction est passé à **[!UICONTROL Traduction terminée]**. Vous pouvez maintenant envoyer votre contenu multilingue, reportez-vous à l’étape 10 de [cette section](#create-multilingual-campaign).

   ![](assets/translation_review_9.png)

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.


-->
