---
solution: Journey Optimizer
product: journey optimizer
title: Fragments de contenu AEM
description: Découvrir comment accéder aux fragments de contenu AEM et comment les gérer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: 1af75a0e6bfc2c3b9c565c3190f46d137a68d32e
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 82%

---

# Fragments de contenu Adobe Experience Manager {#aem-fragments}

En intégrant Adobe Experience Manager à Adobe Journey Optimizer, vous pouvez désormais incorporer facilement vos fragments de contenu AEM dans le contenu de vos e-mails Journey Optimizer. Cette connexion rationalisée simplifie le processus d’accès au contenu AEM et d’utilisation de celui-ci, ce qui permet de créer des campagnes et des parcours personnalisés et dynamiques.

Pour en savoir plus sur le fragment de contenu AEM, consultez la [documentation Experience Manager](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments).

## Limites {#limitations}

* Disponible uniquement pour le canal E-mail.

* Les utilisateurs et utilisatrices ne peuvent actuellement pas changer l’instance AEM à laquelle ils sont connectés, car chaque sandbox est limité à une seule instance.

* Il est recommandé de limiter le nombre de personnes autorisées à publier des fragments de contenu afin de réduire le risque d’erreurs accidentelles dans les e-mails.

* Pour le contenu multilingue, seul le flux manuel est pris en charge.

* Les variantes ne sont actuellement pas prises en charge.

* Vous devez créer une balise spécifique à Journey Optimizer.

+++ Découvrir comment créer votre balise Journey Optimizer

   1. Accédez à votre environnement **Experience Manager**.

   1. Dans le menu **Outils**, accédez à l’onglet **Général** et sélectionnez **Balisage**.

   1. Cliquez sur **Créer une balise**.

   1. Assurez-vous que l’identifiant respecte la syntaxe suivante : `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

   1. Cliquez sur **Créer**.

  Vous pouvez maintenant affecter cette balise Journey Optimizer à vos fragments de contenu.
+++

## Ajouter des fragments de contenu AEM {#aem-add}

Après avoir créé et personnalisé vos [fragments de contenu AEM](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/authoring/fragments/content-fragments), vous pouvez maintenant les importer dans votre campagne ou votre parcours Journey Optimizer.

1. Après avoir créé votre [campagne](../email/create-email.md) ou votre [parcours ](../email/create-email.md) avec une action d’e-mail, accédez au concepteur d’e-mail pour configurer le contenu des e-mails. [En savoir plus](../email/get-started-email-design.md)

1. Cliquez à l’intérieur d’un bloc de texte ou dans la ligne d’objet et sélectionnez **[!UICONTROL Ajouter une personnalisation]** dans la barre d’outils contextuelle.

   ![](assets/aem_campaign_2.png)

1. Dans le menu **[!UICONTROL Fragment de contenu AEM]** du volet de gauche, cliquez sur **[!UICONTROL Ouvrir le sélecteur AEM CF]**.

   ![](assets/aem_campaign_3.png)

1. Sélectionnez un **[!UICONTROL fragment de contenu]** dans la liste des éléments à importer dans votre contenu Journey Optimizer.

1. Cliquez sur **[!UICONTROL Afficher les filtres]** pour affiner votre liste de fragments de contenu.

   Par défaut, le filtre Fragment de contenu est prédéfini pour afficher uniquement le contenu approuvé.

   ![](assets/aem_campaign_4.png)

1. Après avoir sélectionné votre **[!UICONTROL fragment de contenu]**, cliquez sur **[!UICONTROL Sélectionner]** pour l’ouvrir.

   ![](assets/aem_campaign_5.png)

1. Sélectionnez les champs de votre **[!UICONTROL fragment de contenu]** à ajouter à votre contenu. Vous pouvez ajouter votre contenu ou copier sa valeur.

   Notez que si vous choisissez de copier la valeur, les futures mises à jour du **[!UICONTROL fragment de contenu]** ne seront pas répercutées dans votre campagne ou votre parcours.

   ![](assets/aem_campaign_6.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** et vérifiez votre message dans l’aperçu. Vous pouvez maintenant tester et vérifier le contenu de votre message, comme indiqué dans [cette section](../content-management/preview.md).

Une fois les tests effectués et le contenu validé, vous pouvez envoyer l’e-mail à votre audience avec votre [campagne](../campaigns/review-activate-campaign.md) ou votre [parcours](../building-journeys/publishing-the-journey.md).
