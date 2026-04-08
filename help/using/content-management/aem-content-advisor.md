---
solution: Journey Optimizer
product: journey optimizer
title: Accéder au gestionnaire de contenu Adobe Experience Manager
description: Découvrez comment accéder à Adobe Experience Manager Content Advisor et l’utiliser pour découvrir des ressources et des fragments de contenu à l’aide de la recherche sémantique optimisée par l’IA dans Adobe Journey Optimizer.
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 842d69e3-be7f-4a81-8161-6c6ecd571f95
source-git-commit: cc047508f06d0ac7eb4313dad125f2fe9ac3cbc7
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# Utiliser le gestionnaire de contenu Adobe Experience Manager {#aem-content-advisor}

>[!AVAILABILITY]
>
>Le gestionnaire de contenu Adobe Experience Manager est disponible uniquement dans les workflows de création de canal.

Le gestionnaire de contenu Adobe Experience Manager remplace la découverte déterministe par une découverte normalisée pilotée par l’intention à partir d’une surface unifiée. Il permet la découverte unifiée et optimisée par l’IA d’Assets et des fragments de contenu directement dans les workflows de création de Journey Optimizer, ce qui améliore la productivité des marketeurs et l’efficacité des campagnes.

## Fonctions disponibles

### Pour Assets {#asset-features}

Le gestionnaire d’accès de Adobe Experience Manager offre les fonctionnalités de ressource suivantes :

+++ Recherche sémantique IA

Recherchez des ressources en utilisant un langage naturel au lieu de mots-clés ou de noms de fichier exacts. Décrivez vos besoins en langage simple, par exemple « café dans les montagnes », et l’IA trouve des ressources pertinentes du point de vue du contexte en fonction du sens et du contenu, et pas seulement des correspondances textuelles.

![](assets/content-advisor-2.png){zoomable="yes"}

+++

+++ Historique de recherche récent

Accédez à vos recherches récentes pour réutiliser rapidement des mots-clés et des contextes. Cela vous permet de gagner du temps lorsque vous travaillez sur des campagnes similaires ou lorsque vous devez affiner les recherches précédentes.

![](assets/content-advisor-4.png){zoomable="yes"}

+++ 

+++ Charger le brief

Chargez un document de résumé marketing pour faire apparaître automatiquement les ressources qui correspondent à votre contexte de campagne. L’IA analyse votre résumé et suggère des ressources pertinentes en fonction du contenu et des exigences décrits dans le document.

![](assets/content-advisor-5.png){zoomable="yes"}

+++

+++ Panneau d’informations sur les ressources

Affichez les métadonnées et les propriétés détaillées de n’importe quelle ressource à l’aide de l’icône **Info**. Cela inclut les dimensions des ressources, la taille du fichier, la date de création, les balises et d’autres informations pertinentes pour vous aider à prendre des décisions éclairées.

![](assets/content-advisor-6.png){zoomable="yes"}

+++

+++ Panneau Dynamic Media

Accédez aux rendus dynamiques, aux recadrages intelligents et aux modifications à la volée en fonction de la configuration du référentiel.

![](assets/content-advisor-1.png){zoomable="yes"}

Le panneau Dynamic Media permet d’accéder aux rendus dynamiques, aux recadrages intelligents et aux modifications à la volée. Vous pouvez saisir des modificateurs directement dans le panneau pour créer des rendus personnalisés.

**Disponibilité**

La disponibilité de Dynamic Media dépend de la configuration de votre référentiel :

* **Scene7** : disponible pour les ressources publiées (à l’exception des vidéos et de PDF). [En savoir plus sur les modificateurs Scene7 Dynamic Media](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-is-http-modifiers.html){target="_blank"}

* **OpenAPI** : disponible pour les ressources approuvées (sauf la vidéo). [En savoir plus sur Dynamic Media avec les modificateurs OpenAPI](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/image-profiles.html){target="_blank"}

* **Scene7 et OpenAPI** : disponible lorsque les deux configurations existent et que la ressource répond aux critères.

**Sélection de pile**

Les boutons affichés dépendent de la configuration de votre référentiel :

* **bouton Scene7 uniquement** : le référentiel dispose de la configuration Scene7 et la ressource est publiée sur Dynamic Media.
* **Bouton OpenAPI uniquement** : le référentiel dispose de la configuration OpenAPI et la ressource est approuvée.
* **Les deux boutons** : le référentiel comporte à la fois des configurations et la ressource est publiée et approuvée.
+++

### Pour le fragment de contenu {#content-fragment-features}

Le gestionnaire d’accès de Adobe Experience Manager offre les fonctionnalités de fragment de contenu suivantes :

+++ Liste des vues de modèles 

Basculez entre les vues Miniature et Tableau pour parcourir les fragments de contenu au format le plus adapté à votre workflow. La vue Miniature fournit un contexte visuel, tandis que la vue Tableau affiche des informations détaillées dans un format structuré.

![](assets/content-advisor-7.png){zoomable="yes"}

+++

+++ Panneau Infos 

Cliquez sur l’icône **[!UICONTROL Info]** pour ouvrir un panneau de droite affichant les variations de fragment, les propriétés et les détails **[!UICONTROL Référencé par]**. La section **[!UICONTROL Référencé par]** présente toutes les entités Adobe Experience Manager où le fragment est utilisé, avec des liens pour afficher ces références directement dans Adobe Experience Manager.

![](assets/content-advisor-8.png){zoomable="yes"}

+++

+++ Ouvrir dans Adobe Experience Manager

Ouvrez rapidement un fragment de contenu directement dans Adobe Experience Manager pour le modifier à l’aide de l’icône en regard du titre. Cette intégration transparente vous permet de basculer entre Journey Optimizer et Adobe Experience Manager sans perdre de contexte.

![](assets/content-advisor-9.png){zoomable="yes"}

+++

+++ Aperçu JSON

Prévisualisez la structure JSON des fragments de contenu dans un format de tableau organisé et épuré. Cela vous permet de comprendre la structure de données du fragment et de vérifier le contenu avant de l’utiliser dans vos campagnes.

![](assets/content-advisor-10.png){zoomable="yes"}

+++

## Accéder au gestionnaire de contenu Adobe Experience Manager {#access}

Pour accéder au gestionnaire d’accès de Adobe Experience Manager dans Journey Optimizer, procédez comme suit :

1. Créez une campagne dans Adobe Journey Optimizer et ajoutez une action de canal, par exemple E-mail.

1. Cliquez sur **[!UICONTROL Modifier le contenu]** puis sur **[!UICONTROL Modifier le corps de l’e-mail]** pour ouvrir l’éditeur de contenu.

1. Faites glisser et déposez un composant HTML ou Texte dans le contenu de votre e-mail.

1. Pointez sur le composant et cliquez sur **[!UICONTROL Afficher le code source]** (pour les composants HTML) ou **[!UICONTROL Ajouter un Personalization]** (pour les composants Texte).

1. Dans l’éditeur Personalization, choisissez votre point d’entrée de contenu :

   * Pour ajouter une ressource, cliquez sur **** puis **[!UICONTROL Ouvrir le gestionnaire de contenu AEM]**.

     ![](assets/content-advisor-11.png){zoomable="yes"}

   * Pour ajouter un fragment de contenu Adobe Experience Manager, cliquez sur **[!UICONTROL Fragment de contenu AEM]** puis **[!UICONTROL Ouvrir le gestionnaire de contenu AEM]**.

     ![](assets/content-advisor-12.png){zoomable="yes"}

1. Sélectionnez votre référentiel Adobe Experience Manager.

   ![](assets/content-advisor-13.png){zoomable="yes"}

1. Recherchez et sélectionnez la ressource ou le fragment de contenu à utiliser, puis insérez-le dans votre contenu.
