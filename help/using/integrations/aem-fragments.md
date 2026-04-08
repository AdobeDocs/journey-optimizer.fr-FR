---
solution: Journey Optimizer
product: journey optimizer
title: Fragments de contenu AEM
description: Découvrir comment accéder aux fragments de contenu AEM et comment les gérer
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '1274'
ht-degree: 34%

---

# Utilisation de fragments de contenu Adobe Experience Manager {#aem-fragments}

>[!AVAILABILITY]
>
>Cette intégration s’applique à **Adobe Experience Manager as a Cloud Service Sites**, pour les **fragments de contenu** uniquement. Journey Optimizer lit les fragments du niveau **Publication** (et non Auteur).

L’intégration entre Adobe Experience Manager et Journey Optimizer suit ce flux de données :

1. **[Configurer le Dispatcher](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer#dispatcher-configuration){target="_blank"}** : pour permettre à Journey Optimizer d’accéder aux fragments de contenu de Adobe Experience Manager via l’API de gestion des fragments de contenu, vous devez d’abord configurer le Dispatcher. Il s’agit d’une condition préalable à l’intégration.

1. **[Créer et créer](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#creating-a-content-fragment)** : le contenu est créé et configuré dans Adobe Experience Manager en tant que fragments de contenu.

1. **[Balisage](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#manage-tags)** : les fragments de contenu doivent être balisés avec la balise spécifique à Journey Optimizer (`ajo-enabled:{OrgId}/{SandboxName}`).

1. **[Publication](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#publishing-and-previewing-a-fragment)** : les fragments de contenu sont publiés dans Adobe Experience Manager, ce qui les rend disponibles pour Journey Optimizer.

1. **[Accès](#aem-add)** : Journey Optimizer récupère et affiche les fragments de contenu disponibles à partir de l’instance de publication Adobe Experience Manager en temps réel.

1. **[Intégration](#aem-add)** : les fragments de contenu sont sélectionnés et intégrés dans les campagnes ou les parcours.

Lorsqu’un fragment de contenu est publié dans Adobe Experience Manager, un événement est envoyé pour mettre à jour le contenu côté Journey Optimizer. Si la mise à jour est réussie, le fragment de contenu est disponible dans les 5 minutes environ pour les parcours unitaires et dans le lot de traitement suivant pour les cas d’utilisation par lots. Une fois que la mise à jour est disponible dans Journey Optimizer, le contenu publié le plus récent est utilisé dans toutes les campagnes et tous les parcours applicables.

>[!AVAILABILITY]
>
>Pour les clients du secteur de la santé, l’intégration n’est activée que sous licence pour les offres complémentaires Journey Optimizer Healthcare Shield et Adobe Experience Manager Extended Security for Healthcare.

## Créer et affecter une balise dans Experience Manager

>[!IMPORTANT]
>
>Pour permettre à Journey Optimizer d’accéder aux fragments de contenu d’Adobe Experience Manager via l’API Content Fragment Management, vous devez d’abord [configurer Dispatcher](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer#dispatcher-configuration){target="_blank"}.

Avant d’utiliser votre fragment de contenu dans Journey Optimizer, vous devez créer une balise spécifique à Journey Optimizer :

1. Accédez à votre environnement **Experience Manager**.

1. Dans le menu **Outils**, sélectionnez **Balisage**.

   ![](assets/do-not-localize/aem_tag_1.png)

1. Cliquez sur **Créer une balise**.

1. Assurez-vous que l’identifiant respecte la syntaxe suivante : `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

1. Cliquez sur **Créer**.

1. Définissez votre modèle de fragment de contenu comme indiqué dans la documentation d’[Experience Manager](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"} et attribuez la balise Journey Optimizer que vous venez de créer.

Cette connexion en temps réel permet de s’assurer que votre contenu est toujours à jour, mais signifie également que toute modification des fragments publiés affectera immédiatement les campagnes et les parcours actifs.

Vous pouvez maintenant commencer à créer et configurer votre fragment de contenu pour une utilisation ultérieure dans Journey Optimizer. En savoir plus dans la documentation d’[Adobe Experience Manager](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing){target="_blank"}.

## Ajouter des fragments de contenu Experience Manager {#aem-add}

Après avoir créé et personnalisé vos fragments de contenu AEM, vous pouvez maintenant les importer dans votre campagne ou parcours Journey Optimizer.

1. Créez votre [campagne](../campaigns/create-campaign.md) ou [parcours](../building-journeys/journey-gs.md).

1. Pour accéder à votre fragment de contenu AEM, cliquez sur l’icône ![Personnalisation](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) dans n’importe quel champ de texte ou ouvrez le code source à l’aide d’un composant de contenu HTML.

   ![](assets/aem_campaign_2.png)

1. Dans le menu **[!UICONTROL Fragment de contenu AEM]** du volet de gauche, cliquez sur **[!UICONTROL Ouvrir le sélecteur AEM CF]**.

   ![](assets/aem_campaign_3.png)

1. Parcourez la liste et sélectionnez un **[!UICONTROL fragment de contenu]** à importer dans votre contenu Journey Optimizer.

   >[!NOTE]
   >
   > Si le fragment comporte une ou plusieurs variations **publiées**, une liste déroulante **[!UICONTROL Variation]** s’affiche dans le sélecteur. Si aucune **[!UICONTROL Variation]** n’est sélectionnée, la variation **Principal** est utilisée automatiquement. En savoir plus dans [Utilisation de variations de fragments de contenu](#aem-variations).

1. Cliquez sur **[!UICONTROL Afficher les filtres]** pour affiner votre liste de fragments de contenu.

   Par défaut, le filtre Fragment de contenu est préréglé pour afficher uniquement le contenu approuvé.

   ![](assets/aem_campaign_4.png)

1. Après avoir sélectionné votre **[!UICONTROL fragment de contenu]**, cliquez sur **[!UICONTROL Sélectionner]** pour l’ajouter.

   ![](assets/aem_campaign_5.png)

1. Cliquez sur **[!UICONTROL Afficher le fragment]** pour consulter les informations relatives au fragment. Notez que l’ouverture du menu **[!UICONTROL Informations sur le fragment]** met l’éditeur en mode lecture seule.

   Sélectionnez **[!UICONTROL Aperçu]** dans le menu de droite pour afficher votre fragment dans Adobe Experience Manager.

   ![](assets/aem_campaign_7.png)

1. Cliquez sur l’![icône Plus d’actions](assets/do-not-localize/Smock_MoreSmallList_18_N.svg) pour accéder au menu avancé de votre fragment :

   * **[!UICONTROL Intervertir le fragment]**
   * **[!UICONTROL Explorer les références]**
   * **[!UICONTROL Ouvrir dans AEM]**

   ![](assets/aem_campaign_8.png)

1. Sélectionnez les champs de votre **[!UICONTROL fragment]** à ajouter à votre contenu.

   <!--
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.
-->

    ![](assets/aem_campaign_6.png)

1. Pour surfacer une URL d’image stockée dans un attribut de fragment de contenu, par exemple un chemin ou un champ d’URL à partir du modèle de fragment, insérez-la dans votre HTML avec une balise `<img>` et l’attribut de fragment comme source, par exemple :

   ```html
   <img src="[insert your AEM Content Fragment attribute here]">
   ```

   >[!NOTE]
   >
   >Les URL d’images relatives provenant de Adobe Experience Manager ne sont pas prises en charge. Utilisez des URL **absolues**.

1. Sélectionnez **Pilules : désactivée** pour permettre à l’expérience des pilules d’améliorer la lisibilité en masquant les chemins d’accès aux attributs longs.

   ![](assets/aem_campaign_10.png)

1. Pour utiliser des **espaces réservés de personnalisation** créés dans Adobe Experience Manager dans le texte de votre fragment, définissez-les dans le fragment de contenu de Adobe Experience Manager comme suit : `{{name}}`.

   Dans Journey Optimizer, ces jetons sont des espaces réservés. Une fois l’expérience **pilules** activée, ils apparaissent dans la section **[!UICONTROL Fragment de contenu AEM]** du rail de droite à côté des champs de fragment.

1. Pour activer la personnalisation en temps réel, tous les espaces réservés utilisés dans un **[!UICONTROL fragment de contenu]** doivent être explicitement déclarés par l’utilisateur ou l’utilisatrice en tant que paramètres dans la balise helper du fragment. Mappez ces espaces réservés aux attributs de profil, aux attributs contextuels, aux chaînes statiques ou aux variables prédéfinies comme suit :

   1. **Mappage de profil ou d’attribut contextuel** : attribuez l’espace réservé à un profil ou à un attribut contextuel, par exemple name = profile.person.name.firstName.

   1. **Mappage de chaîne statique** : attribuez une valeur de chaîne fixe en la plaçant entre guillemets doubles, par exemple name = &quot;John&quot;.

   1. **Mappage de variables** : référencez une variable déclarée précédemment dans le même HTML, par exemple name = &#39;variableName&#39;.
Dans ce cas, assurez-vous que **_variableName_** est déclaré avant d’ajouter l’identifiant du fragment, en utilisant la syntaxe suivante :

      ```html
      {% let variableName = attribute name %} 
      ```

   Dans l’exemple ci-dessous, l’espace réservé **_month_** est mappé à l’attribut **_profile.person.bornDate_** dans le fragment.

   ![](assets/aem_campaign_9.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**. Vous pouvez maintenant tester et vérifier le contenu de votre message, comme indiqué dans [cette section](../content-management/preview.md).

   <!--Note that the Content Fragment you selected stays active for this message. When you open the Personalization Editor in another field or content block, you can keep working with the same fragment from the **[!UICONTROL AEM Content Fragment]** section and add more fields without reopening **[!UICONTROL Open AEM CF selector]**.-->

Une fois que vous avez effectué vos tests et validé le contenu, vous pouvez [envoyer votre campagne](../campaigns/review-activate-campaign.md) ou [publier votre parcours](../building-journeys/publish-journey.md) pour votre audience.

Adobe Experience Manager permet d’identifier les campagnes ou parcours Journey Optimizer qui utilisent un fragment de contenu. En savoir plus dans la documentation d’[Adobe Experience Manager](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references){target="_blank"}.

## Utilisation des variations de fragments de contenu {#aem-variations}

Dans Adobe Experience Manager, chaque fragment de contenu est constitué des éléments suivants :

* **Principal** : le contenu principal du fragment, qui existe toujours, ne peut pas être supprimé et constitue la base de toutes les variations.
* **Variations** : une ou plusieurs permutations de **Principal** que les auteurs créent pour des canaux ou des scénarios spécifiques. Les variations sont présentes dans le fragment non comme des ressources distinctes et peuvent être comparées et synchronisées avec **Principal**.

Exemples de cas d’utilisation de variation :

* Une version courte de copie pour une notification push et une version plus longue pour l’e-mail.
* Réglages régionaux de la tonalité sans créer de fragment distinct.
* Messages spécifiques à un canal (par exemple, web par rapport à mobile).

➡️ [En savoir plus dans la documentation Adobe Experience Manager](https://experienceleague.adobe.com/fr/docs/experience-manager-65/content/assets/content-fragments/content-fragments-variations)

Journey Optimizer vous permet de choisir la variation à utiliser lorsque vous insérez un fragment. De ce fait, différentes campagnes ou parcours peuvent s’appuyer sur différents rendus du même contenu source dans Adobe Experience Manager sans dupliquer les fragments.

Pour sélectionner une variation :

1. Ouvrez une [campagne](../campaigns/create-campaign.md) ou un [parcours &#x200B;](../building-journeys/journey-gs.md).

1. Cliquez sur l’icône ![](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) dans n’importe quel champ de texte, ou ouvrez la source HTML à partir d’un composant de contenu HTML.

1. Dans **[!UICONTROL Fragment de contenu]**, cliquez sur **[!UICONTROL Ouvrir le sélecteur CF]**.

   ![](assets/aem_campaign_3.png)

1. Pour sélectionner un fragment de contenu Adobe Experience Manager spécifique aux paramètres régionaux dans la vue Tableau, utilisez **[!UICONTROL Personnaliser le tableau]** afin d’ajouter la colonne **[!UICONTROL Langue]**. Les valeurs des paramètres régionaux s’affichent dans le tableau, ce qui vous permet d’identifier et de sélectionner le fragment approprié.

   ![](assets/cf-variation-2.png)

1. Sélectionnez votre **[!UICONTROL fragment de contenu]**.

1. Cliquez sur l’icône ![informations](assets/do-not-localize/info-icon.svg) pour ouvrir le menu **[!UICONTROL Détails]**. Si le fragment comporte une ou plusieurs variations publiées, une liste déroulante **[!UICONTROL Variation]** s’affiche en regard des détails du fragment.

   ![](assets/cf-variation-5.png)

1. Dans le menu **[!UICONTROL Détails rapides]**, cliquez sur **[!UICONTROL Explorer les références]** pour ouvrir les options associées dans Adobe Experience Manager pour les détails de variation, la prévisualisation et le BAT, le cas échéant.

1. Choisissez votre variation, puis cliquez sur **[!UICONTROL Sélectionner]**.

   >[!NOTE]
   >
   > Si vous ne sélectionnez pas de variation ou si le fragment a été ajouté avant que la prise en charge de variation ne soit disponible, Journey Optimizer utilise automatiquement la variation **Principal** au moment de la diffusion.

Après avoir inséré un fragment avec une variation, sa republication dans Adobe Experience Manager met automatiquement à jour chaque **variation référencée** dans les campagnes ou parcours actifs. Les aperçus et les BAT utilisent toujours la variation que vous avez choisie, avec le contenu publié le plus récent pour cette variation.
