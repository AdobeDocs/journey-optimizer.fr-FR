---
solution: Journey Optimizer
product: journey optimizer
title: Impliquer les clients en parcourant l’activité
description: Impliquer les clients en parcourant l’activité
feature: Use Cases
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 2%

---

# Impliquer les clients en parcourant l’activité {#engage-customers-uc}

>[!BEGINSHADEBOX]

Notez que ce cas d’utilisation commence par une audience qui existe déjà dans Experience Platform, en particulier une audience de comportement web en temps réel qui collecte l’activité de navigation au fur et à mesure qu’elle se produit. [En savoir plus dans Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/rtcdp/intro/rtcdp-intro/get-started#audiences)

**Schémas nécessaires pour ce cas d’utilisation :**

* **Destinataires** : utilisé comme dimension de ciblage, avec les champs : `email`, `churnprop`
* **Liste de souhaits** : avec champs : `description`, `priceref`, `imageurl`

➡️ [Découvrez comment configurer des schémas basés sur des modèles](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-interest-14.png){zoomable="yes"}

Cette campagne cible les clients qui ont parcouru la catégorie des équipements d’exercice. L’audience est dédupliquée et segmentée en fonction du risque de résiliation et de la probabilité qu’une personne cesse d’interagir ou d’acheter.

Les clients à haut risque sont rassemblés dans une nouvelle audience qui sera ensuite utilisée pour une communication spécifique, tandis que les clients à faible et moyen risque passent par un parcours en plusieurs étapes avec des e-mails personnalisés et des suivis.

1. Commencez par mettre en place une nouvelle campagne spécifiquement destinée à **Réengagement des listes de souhaits**. Cela garantit que votre messagerie se concentre sur les clients qui ont déjà affiché leur intention d’achat en enregistrant les produits sur leur liste de souhaits.

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. Renseignez vos **[!UICONTROL Paramètres de campagne]** tels que le nom, la description, les dates de début et de fin de la campagne et les balises pertinentes.

1. Ajoutez une activité **[!UICONTROL Lecture d’audience]** pour sélectionner une audience prédéfinie à partir de Adobe Experience Platform. Ici, il s’agit des clients qui ont parcouru la catégorie d’équipement d’exercice sur votre site web.

   Les destinataires sont identifiés avec leur adresse e-mail sélectionnée dans le champ **[!UICONTROL Entité]**.

   ![](assets/uc-interest-1.png){zoomable="yes"}

1. Ajoutez une activité **[!UICONTROL Déduplication]** pour supprimer les adresses e-mail en double de votre audience, en veillant à ce que chaque client ne reçoive qu’un seul message.

1. Cliquez sur **[!UICONTROL Ajouter un attribut]** et sélectionnez e-mail comme attribut pour la déduplication.

   ![](assets/uc-interest-2.png){zoomable="yes"}

1. Ajoutez ensuite une activité **[!UICONTROL Partage]** pour segmenter les clients et les clientes en fonction de leur probabilité de perte de clientèle, ce qui vous permet de fournir des expériences personnalisées adaptées à chaque groupe de clients et clientes.

   ![](assets/uc-interest-3.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Ajouter un segment]** pour créer trois groupes :

   * Faible risque

   * risque Medium

   * Risque élevé

   ![](assets/uc-interest-5.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Créer un filtre]** pour définir la probabilité de résiliation pour chaque groupe.

   Utilisez l’**éditeur de conditions** pour définir les valeurs spécifiques qui déterminent le risque de résiliation de chaque client.

   ![](assets/uc-interest-6.png){zoomable="yes"}

1. Chaque segment est géré différemment :

   * [Risque faible/moyen](#low-medium-risk)
   * [Risque élevé](#high-risk)

1. Une fois votre campagne testée et prête, cliquez sur **[!UICONTROL Publier]** pour la mettre en ligne.

Une fois la campagne exécutée, explorez le tableau de bord de création de rapports pour passer en revue les mesures de performances et les informations clés.

➡️ [En savoir plus sur le reporting](../reports/campaign-global-report-cja.md)

## Segments à haut risque {#high-risk}

Pour les clients identifiés comme présentant un risque élevé de perte de clientèle, créez un segment d’audience dédié. Cette audience est ensuite utilisée pour une communication distincte et ciblée.

1. Ajoutez une **[!UICONTROL Enregistrer l’audience]**.

   ![](assets/uc-interest-7.png){zoomable="yes"}

1. Ajoutez un **[!UICONTROL Libellé]** à votre audience et choisissez le **[!UICONTROL Champ de mappage de profil]**, ici **recipients-email**.

   ![](assets/uc-interest-8.png){zoomable="yes"}

Cette audience est ensuite enregistrée dans Experience Cloud, où elle peut être utilisée ultérieurement pour une campagne ciblée spécifique.

## Segments à faible/moyen risque {#low-medium-risk}

Pour les clients présentant un risque de perte de clientèle faible et moyen, lancez une campagne en plusieurs étapes visant à renforcer l’engagement :

1. Associez les risques Faible et Medium à une activité **[!UICONTROL Union]**.

   ![](assets/uc-interest-9.png){zoomable="yes"}

1. Ajoutez une activité **[!UICONTROL Enrichissement]** pour personnaliser la campagne avec une liste de souhaits et des informations sur les produits.

1. Cliquez sur **[!UICONTROL Ajouter un attribut]** pour créer les trois attributs suivants :

   * `Wishlist > description`
   * `Wishlist > priceref`
   * `Wishlist > imageurl`

   Le message est ainsi enrichi d’informations de liste de souhaits détaillées.

   ![](assets/uc-interest-10.png){zoomable="yes"}

1. Créez une nouvelle audience pour le reciblage en fonction de l’engagement avec les e-mails.

   Nous créons ici une audience basée sur les événements de clic sur les e-mails, afin de recibler toutes les personnes qui ont interagi avec un e-mail précédemment envoyé et, plus précisément, qui ont cliqué sur un lien contenu dans ce message.

   ![](assets/uc-interest-11.png){zoomable="yes"}

1. Divisez l’engagement de manière égale pour envoyer un suivi par SMS ou par notifications push afin d’encourager les conversions.

   ![](assets/uc-interest-12.png){zoomable="yes"}

1. Créez le contenu du message pour chaque canal, y compris les attributs de profil, tels que le nom du destinataire, ainsi que des données d’enrichissement telles que des éléments de liste de souhaits, afin de personnaliser chaque message.

   ![](assets/uc-interest-13.png){zoomable="yes"}
