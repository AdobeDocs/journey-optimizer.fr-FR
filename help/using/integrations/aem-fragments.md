---
solution: Journey Optimizer
product: journey optimizer
title: Fragments de contenu AEM
description: Découvrir comment accéder aux fragments de contenu AEM et comment les gérer
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: 92690f1b3f73c75d9b81746b49836a24ebf7c457
workflow-type: tm+mt
source-wordcount: '1510'
ht-degree: 37%

---

# Fragments de contenu Adobe Experience Manager {#aem-fragments}

En intégrant Adobe Experience Manager as a Cloud Service à Adobe Journey Optimizer, vous pouvez désormais incorporer facilement vos fragments de contenu AEM dans le contenu de Journey Optimizer. Cette connexion rationalisée simplifie le processus d’accès au contenu AEM et d’utilisation de celui-ci, ce qui permet de créer des campagnes et des parcours personnalisés et dynamiques.

Pour en savoir plus sur les fragments de contenu AEM, voir [Utilisation des fragments de contenu](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} dans la documentation d’Experience Manager.

## Avant de commencer {#start}

>[!AVAILABILITY]
>
>Pour la clientèle du secteur de la santé, l’intégration n’est activée qu’après l’obtention d’une licence pour les offres complémentaires Journey Optimizer Healthcare Shield et Adobe Experience Manager Enhanced Security.

### Limites {#limitations}

Notez les restrictions suivantes lorsque vous utilisez des fragments de contenu Adobe Experience Manager dans Journey Optimizer :

* **Types de fragments de contenu** : les fragments de contenu simples et les fragments de contenu imbriqués sont pris en charge. Les variations de fragment de contenu ne sont actuellement pas prises en charge.

* **Contenu multilingue** : Seul le flux manuel est pris en charge. Chaque variante de langue doit être créée indépendamment dans Adobe Experience Manager, balisée, publiée et sélectionnée manuellement dans Journey Optimizer. Il n’existe aucun mécanisme automatique de résolution linguistique ou de secours.

* **Accès au référentiel** : Journey Optimizer s’intègre exclusivement au niveau Publication Adobe Experience Manager, où les fragments de contenu sont disponibles via un point d’entrée public non authentifié. Bien que les référentiels de création puissent apparaître dans le sélecteur de référentiel, seuls les fragments de contenu publiés au niveau Publication peuvent être utilisés dans Journey Optimizer.

* **Statut du fragment de contenu** : Journey Optimizer affiche les fragments de contenu avec le statut **Publié** et **Modifié**. Dans tous les cas, seule la dernière version publiée est utilisée. Si un fragment est modifié après publication, ces modifications ne sont pas répercutées dans Journey Optimizer tant que le fragment de contenu n’est pas republié dans Adobe Experience Manager. Il n’existe pas de réconciliation de version automatique entre Adobe Experience Manager et Journey Optimizer.

* **Personalization** : seuls les attributs de profil, les attributs contextuels, les chaînes statiques et les variables prédéclarées sont pris en charge. Les attributs dérivés ou calculés ne sont pas pris en charge.

* **Mises à jour et contrôle de version** : les mises à jour de fragments de contenu nécessitent une republication manuelle depuis Adobe Experience Manager. Il n’existe pas de réconciliation de version automatique entre Adobe Experience Manager et Journey Optimizer. Lorsqu’un fragment de contenu est publié dans Adobe Experience Manager, Journey Optimizer reçoit un événement et des mises à jour du côté Journey Optimizer. En cas de réussite, la mise à jour sera disponible au bout de 5 minutes pour les Parcours unitaires et dans le lot suivant pour les cas d’utilisation par lots.

* **Mise en cache et relecture** : les fragments de contenu sont récupérés en temps réel à partir du niveau Publication Adobe Experience Manager. Il n’existe aucune mise en cache de prérendu ou d’instantané. Les épreuves des campagnes et des parcours reflètent toujours la version publiée la plus récemment du fragment de contenu et les versions historiques ne peuvent pas être verrouillées pour la relecture.

* **Accès utilisateur** : il est recommandé de limiter le nombre d’utilisateurs ayant accès à la publication de fragments de contenu afin de réduire le risque d’erreurs accidentelles.

### Flux de synchronisation du contenu {#content-sync-flow}

L’intégration entre Adobe Experience Manager et Journey Optimizer suit ce flux de données :

1. **[Créer et créer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#creating-a-content-fragment)** : le contenu est créé et configuré dans Adobe Experience Manager en tant que fragments de contenu.

1. **[Balisage](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#manage-tags)** : les fragments de contenu doivent être balisés avec la balise spécifique à Journey Optimizer (`ajo-enabled:{OrgId}/{SandboxName}`).

1. **[Publication](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#publishing-and-previewing-a-fragment)** : les fragments de contenu sont publiés dans Adobe Experience Manager, ce qui les rend disponibles pour Journey Optimizer.

1. **[Accès](#aem-add)** : Journey Optimizer récupère et affiche les fragments de contenu disponibles à partir de l’instance de publication Adobe Experience Manager en temps réel.

1. **[Intégration](#aem-add)** : les fragments de contenu sont sélectionnés et intégrés dans les campagnes ou les parcours.

Lorsqu’un fragment de contenu est publié dans Adobe Experience Manager, un événement est envoyé pour mettre à jour le contenu côté Journey Optimizer. Si la mise à jour est réussie, le fragment de contenu est disponible dans les 5 minutes environ pour les parcours unitaires et dans le lot de traitement suivant pour les cas d’utilisation par lots. Une fois que la mise à jour est disponible dans Journey Optimizer, le contenu publié le plus récent est utilisé dans toutes les campagnes et tous les parcours applicables.

### Cycle de vie du fragment de contenu

![](assets/do-not-localize/AEM_CF.png)

Les fragments de contenu suivent différentes étapes du cycle de vie en fonction du niveau Adobe Experience Manager dans lequel ils existent. [En savoir plus dans la documentation de Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

Le contenu est créé et géré au **niveau Auteur**, où les fragments peuvent avoir des statuts tels que Nouveau, Brouillon, Publié, Modifié ou Dépublié. Ces statuts s’appliquent uniquement au **niveau Auteur** et prennent en charge la création et la révision de contenu.

Lorsqu’un fragment de contenu est publié, une copie est créée au **niveau Publication** et exposée via un point d’entrée public non authentifié. Journey Optimizer s’intègre exclusivement à ce **niveau Publication**.

Par conséquent, Journey Optimizer n’affiche que les fragments de contenu publiés ou modifiés et utilise toujours la dernière version publiée. Les modifications apportées après la publication ne sont pas répercutées dans Journey Optimizer tant que le fragment de contenu n’a pas été republié.

## Créer et affecter une balise dans Experience Manager

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

1. Sélectionnez un **[!UICONTROL fragment de contenu]** dans la liste des éléments à importer dans votre contenu Journey Optimizer.

1. Cliquez sur **[!UICONTROL Afficher les filtres]** pour affiner votre liste de fragments de contenu.

   Par défaut, le filtre Fragment de contenu est préréglé pour afficher uniquement le contenu approuvé.

   ![](assets/aem_campaign_4.png)

1. Après avoir sélectionné votre **[!UICONTROL fragment de contenu]**, cliquez sur **[!UICONTROL Sélectionner]** pour l’ouvrir.

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
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.-->

   ![](assets/aem_campaign_6.png)

1. Pour activer la personnalisation en temps réel, tous les espaces réservés utilisés dans un **[!UICONTROL fragment de contenu]** doivent être explicitement déclarés par l’utilisateur ou l’utilisatrice en tant que paramètres dans la balise helper du fragment. Vous pouvez mapper ces espaces réservés aux attributs de profil, aux attributs contextuels, aux chaînes statiques ou aux variables prédéfinies à l’aide des méthodes suivantes :

   1. **Mappage de profil ou d’attribut contextuel** : attribuez l’espace réservé à un profil ou à un attribut contextuel, par exemple name = profile.person.name.firstName.

   1. **Mappage de chaîne statique** : attribuez une valeur de chaîne fixe en la plaçant entre guillemets doubles, par exemple name = &quot;John&quot;.

   1. **Mappage de variables** : référencez une variable déclarée précédemment dans le même HTML, par exemple name = &#39;variableName&#39;.
Dans ce cas, assurez-vous que **_variableName_** est déclaré avant d’ajouter l’identifiant du fragment, en utilisant la syntaxe suivante :

      ```html
      {% let variableName = attribute name %} 
      ```

   Dans l’exemple ci-dessous, l’espace réservé **_name_** est mappé sur l’attribut **_profile.person.name.firstName_** dans le fragment.

   ![](assets/aem_campaign_9.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**. Vous pouvez maintenant tester et vérifier le contenu de votre message, comme indiqué dans [cette section](../content-management/preview.md).
Une fois que vous avez effectué vos tests et validé le contenu, vous pouvez [envoyer votre campagne](../campaigns/review-activate-campaign.md) ou [publier votre parcours](../building-journeys/publish-journey.md) pour votre audience.

Adobe Experience Manager permet d’identifier les campagnes ou parcours Journey Optimizer qui utilisent un fragment de contenu. En savoir plus dans la documentation d’[Adobe Experience Manager](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references).

## Résolution des problèmes {#troubleshooting}

Si vous rencontrez des problèmes lors de l’utilisation de fragments de contenu Adobe Experience Manager dans Journey Optimizer, reportez-vous aux problèmes et résolutions courants suivants :

| Problème | Cause | Résolution |
|-|-|-|
| **Balise introuvable** ou **fragment de contenu non visible dans le sélecteur** | La syntaxe de la balise Adobe Experience Manager ne correspond pas au format requis `ajo-enabled:{OrgId}/{SandboxName}` | Vérifiez que l’ID de balise utilise l’**ID d’organisation** et le **Nom du sandbox** corrects. Vérifiez qu’il n’y a pas d’espaces ou de séparateurs incorrects. Republiez le fragment de contenu après avoir corrigé la balise . |
| **Le fragment de contenu n’apparaît pas dans la liste** | Le fragment de contenu est à l’état de brouillon ou n’est pas approuvé | Seuls les fragments de contenu approuvés et publiés s’affichent dans le sélecteur Journey Optimizer. Publiez le fragment de contenu dans Adobe Experience Manager et assurez-vous qu’il possède le statut approuvé . |
| **Erreur de variable non définie** | espace réservé Personalization non déclaré dans la balise d’assistance de fragment | Ajoutez tous les paramètres requis dans la balise d’assistance de fragment. Chaque espace réservé utilisé dans le fragment de contenu doit être explicitement déclaré avec son mappage. |
| **L’épreuve affiche un contenu inattendu** | Proof utilise la dernière version publiée de Adobe Experience Manager | Les BAT reflètent toujours la publication la plus récente du fragment de contenu dans Adobe Experience Manager. Si vous avez récemment apporté des modifications à Adobe Experience Manager, republiez le fragment et actualisez l’épreuve. |
| **Erreur de refus d’accès (CPES)** | Rôle utilisateur non autorisé à accéder à certains attributs | Contactez votre administrateur système pour vérifier que votre rôle dispose des autorisations appropriées pour le profil ou les attributs contextuels utilisés dans la personnalisation. |
| **Le fragment affiche du contenu vide ou manquant** | Paramètres de personnalisation requis manquants ou valeurs de secours | Assurez-vous que tous les paramètres requis sont fournis et envisagez d’ajouter des valeurs de secours pour les attributs facultatifs. |

Si le problème persiste, contactez votre représentant Adobe avec des détails sur votre identifiant de fragment de contenu, votre identifiant de campagne ou de parcours, ainsi que tout message d’erreur affiché.
