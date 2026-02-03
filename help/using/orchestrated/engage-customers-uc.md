---
solution: Journey Optimizer
product: journey optimizer
title: Interagir avec les clientes et clients en fonction de leur activité de navigation
description: Interagir avec les clientes et clients en fonction de leur activité de navigation
feature: Use Cases
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 98%

---

# Interagir avec les clientes et clients en fonction de leur activité de navigation {#engage-customers-uc}

>[!BEGINSHADEBOX]

Notez que ce cas d’utilisation commence par une audience qui existe déjà dans Experience Platform. Il s’agit d’une audience de comportement web en temps réel qui collecte l’activité de navigation. [En savoir plus dans Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/rtcdp/intro/rtcdp-intro/get-started#audiences)

**Schémas requis pour ce cas d’utilisation :**

* **Destinataires** : utilisé comme dimension de ciblage, avec les champs `email` et `churnprop`
* **Liste de souhaits** : avec les champs `description`, `priceref` et `imageurl`

➡️ [Découvrez comment configurer des schémas relationnels](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-interest-14.png){zoomable="yes"}

Cette campagne cible les clients et clientes qui ont parcouru la catégorie des équipements de sport. L’audience est dédupliquée et segmentée en fonction du risque d’attrition, c’est-à-dire la probabilité qu’une personne cesse d’interagir ou d’effectuer des achats.

Les clients et clientes à haut risque sont rassemblés dans une nouvelle audience qui sera ensuite utilisée pour une communication spécifique, tandis que les clients et clientes à faible et moyen risque évoluent dans un parcours en plusieurs étapes avec des e-mails personnalisés et des suivis.

1. Commencez par configurer une nouvelle campagne destinée au **réengagement des listes de souhaits**. Vous garantissez ainsi que vos messages se concentrent sur la clientèle qui a déjà affiché ses intentions d’achat en enregistrant les produits sur sa liste de souhaits.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Renseignez les **[!UICONTROL paramètres de campagne]** tels que le nom, la description, les dates de début et de fin de la campagne ainsi que les balises pertinentes.

1. Ajoutez une activité **[!UICONTROL Lecture d’audience]** pour sélectionner une audience prédéfinie à partir d’Adobe Experience Platform. Ici, il s’agit des clients et clientes qui ont parcouru la catégorie des équipements de sport sur votre site web.

   Les destinataires sont identifiés avec l’adresse e-mail, sélectionnée dans le champ **[!UICONTROL Entité]**.

   ![](assets/uc-interest-1.png){zoomable="yes"}

1. Ajoutez une activité **[!UICONTROL Déduplication]** pour supprimer les adresses e-mail en double dans votre audience, pour garantir que chaque personne ne reçoit qu’un seul message.

1. Cliquez sur **[!UICONTROL Ajouter un attribut]** et sélectionnez e-mail comme attribut pour la déduplication.

   ![](assets/uc-interest-2.png){zoomable="yes"}

1. Ajoutez ensuite une activité **[!UICONTROL Partage]** pour segmenter les clients et les clientes en fonction de la probabilité d’attrition, ce qui vous permet d’offrir des expériences personnalisées adaptées à chaque groupe.

   ![](assets/uc-interest-3.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Ajouter un segment]** pour créer trois groupes :

   * Risque faible

   * Risque moyen

   * Risque élevé

   ![](assets/uc-interest-5.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Créer un filtre]** pour définir la probabilité d’attrition de chaque groupe.

   Utilisez l’**éditeur de conditions** pour définir les valeurs qui déterminent le risque d’attrition de chaque personne.

   ![](assets/uc-interest-6.png){zoomable="yes"}

1. Chaque segment est géré différemment :

   * [Risque faible/moyen](#low-medium-risk)
   * [Risque élevé](#high-risk)

1. Une fois votre campagne testée et prête, cliquez sur **[!UICONTROL Publier]** pour la mettre en ligne.

Une fois la campagne exécutée, explorez le tableau de bord de rapports pour passer en revue les indicateurs de performances et les informations clés.

➡️ [En savoir plus sur la création de rapports](../reports/campaign-global-report-cja.md)

## Segments à risque élevé {#high-risk}

Créez un segment d’audience spécifique pour les clients et clientes qui présentent un risque élevé d’attrition. Cette audience est ensuite utilisée pour une communication distincte et ciblée.

1. Sélectionnez **[!UICONTROL Enregistrer l’audience]**.

   ![](assets/uc-interest-7.png){zoomable="yes"}

1. Ajoutez un **[!UICONTROL libellé]** à votre audience et choisissez le **[!UICONTROL champ de mappage de profils]**, en l’occurrence **recipients-email**.

   ![](assets/uc-interest-8.png){zoomable="yes"}

Cette audience est ensuite enregistrée dans Experience Cloud, où elle peut être utilisée ultérieurement pour une campagne ciblée spécifique.

## Segments à risque faible/moyen {#low-medium-risk}

Pour les clients et clientes qui présentent un risque d’attrition faible ou moyen, configurez une campagne en plusieurs étapes visant à renforcer l’engagement :

1. Associez les risques faible et moyen à une activité **[!UICONTROL Union]**.

   ![](assets/uc-interest-9.png){zoomable="yes"}

1. Ajoutez une activité **[!UICONTROL Enrichissement]** pour personnaliser la campagne avec une liste de souhaits et des informations sur les produits.

1. Cliquez sur **[!UICONTROL Ajouter un attribut]** pour créer les trois attributs suivants :

   * `Wishlist > description`
   * `Wishlist > priceref`
   * `Wishlist > imageurl`

   Le message est ainsi enrichi d’informations détaillées sur les listes de souhaits.

   ![](assets/uc-interest-10.png){zoomable="yes"}

1. Créez une nouvelle audience pour le reciblage en fonction de l’engagement avec les e-mails.

   Nous créons ici une audience basée sur les événements de clic dans les e-mails afin de recibler toutes les personnes qui ont interagi avec un e-mail envoyé précédemment en cliquant sur un lien qu’il contenait.

   ![](assets/uc-interest-11.png){zoomable="yes"}

1. Répartissez l’engagement de manière équilibrée pour envoyer un suivi par SMS ou par notification push et encourager les conversions.

   ![](assets/uc-interest-12.png){zoomable="yes"}

1. Créez le contenu du message pour chaque canal, y compris les attributs de profil, tels que le nom du destinataire, ainsi que des données d’enrichissement telles que les articles de la liste de souhaits, afin de personnaliser chaque message.

   ![](assets/uc-interest-13.png){zoomable="yes"}
