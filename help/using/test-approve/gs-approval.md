---
title: Commencer avec l’approbation des parcours et des campagnes
description: Découvrez comment configurer un processus d’approbation pour vos parcours et campagnes.
role: User
level: Beginner
feature: Approval
exl-id: 92d1439e-5cac-4e7d-85f8-ebf432e9ef7c
TQID: https://experienceleague.adobe.com/dKfstmm0ilHKUATU-sz7c04IZBu2O7Ju-srPPoKJVl4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 984
ht-degree: 100%

---

# Commencer avec l’approbation des parcours et des campagnes {#send-proofs}

## Commencer avec les politiques d’approbation {#gs}

[!DNL Journey Optimizer] permet de définir un processus d’approbation pour que les équipes marketing puissent s’assurer que les campagnes et les parcours sont examinés et approuvés par les parties prenantes appropriées avant leur mise en ligne.

Les politiques d’approbation introduisent un workflow structuré directement dans l’interface d’utilisation, éliminant ainsi la nécessité de recourir à des supports externes tels que des outils de gestion des e-mails ou des tâches, tout en assurant la gestion et le suivi centralisés de toutes les approbations.

En outre, cette fonctionnalité offre un meilleur contrôle sur la publication de vos parcours et campagnes : le processus d’approbation étant incorporé dans Journey Optimizer, les campagnes et les parcours restent à l’état Verrouillé pendant la révision, ce qui garantit qu’aucune modification ou activation involontaire ne se produit avant que toutes les approbations nécessaires ne soient mises en place.

## Conditions préalables {#prerequisites}

Avant de commencer, vérifiez que les autorisations ci-dessous ont été configurées.

Pour approuver et publier les parcours et campagnes, les utilisateurs et utilisatrices doivent disposer des autorisations **Approuver et publier des campagnes** et **Approuver et publier des parcours**. [En savoir plus](../administration/permissions.md)

+++  Découvrir comment attribuer des autorisations liées aux approbations

1. Dans le produit **Autorisations**, accédez à l’onglet **Rôles** et sélectionnez le **Rôle** de votre choix.

1. Cliquez sur **Modifier** pour modifier les autorisations.

1. Ajoutez la ressource **Campagnes**, puis sélectionnez **Approuver et publier des campagnes** dans le menu déroulant.

   ![Attribuer l’autorisation d’approbation et de publication des campagnes](assets/permissions_approval.png){zoomable="yes"}

1. Ajoutez la ressource **Parcours**, puis sélectionnez **Approuver et publier des parcours** dans le menu déroulant.

   ![Attribuer l’autorisation d’approbation et de publication des parcours](assets/permissions_approval_2.png){zoomable="yes"}

1. Cliquez sur **Enregistrer** pour appliquer vos modifications.

Les autorisations des personnes déjà affectées à ce rôle seront automatiquement mises à jour.

1. Pour attribuer ce rôle à de nouvelles personnes, accédez à l’onglet **Utilisateurs et utilisatrices** du tableau de bord **Rôles** et cliquez sur **Ajouter un utilisateur ou une utilisatrice**.

1. Saisissez le nom de la personne, son adresse e-mail ou choisissez dans la liste, puis cliquez sur **Enregistrer**.

1. Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez [cette documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/abac/permissions-ui/users).

La personne recevra un e-mail avec des instructions pour accéder à votre instance.

+++

## Vue d’ensemble du processus d’approbation {#process}

Le processus d’approbation global se présente comme suit :

![Flux du processus d’approbation](assets/approval-process.png){zoomable="yes"}

1. **Configuration des politiques d’approbation**

   Un administrateur ou une administratrice crée une politique d’approbation qui définit les conditions dans lesquelles la politique doit s’appliquer aux parcours ou aux campagnes. Vous pouvez par exemple créer une politique d’approbation qui exige que toutes les campagnes planifiées créées par une personne donnée soient approuvées avant d’être activées. [Découvrir comment créer des politiques d’approbation](approval-policies.md)

1. **Envoi de campagne/parcours pour approbation**

   Les personnes à l’origine de la campagne/du parcours créent un parcours ou une campagne et l’envoient pour approbation. La campagne/le parcours passe à l’état En révision, durant lequel aucune modification ne peut être effectuée, sauf si la demande est annulée. [Découvrir comment demander l’approbation](request-approval.md)

   >[!NOTE]
   >
   >Les campagnes et les parcours ne doivent être soumis à approbation que si une politique d’approbation est en place. Si aucune politique de ce type ne s’applique, le créateur ou la créatrice peut publier directement la campagne ou le parcours sans nécessiter d’approbation.

1. **Révision et approbation**

   Les personnes en charge de l’approbation définies dans la politique d’approbation qui s’applique au parcours ou à la campagne reçoivent une notification. Elles peuvent consulter le contenu, l’audience et les paramètres du parcours ou de la campagne. Si des modifications sont nécessaires, la personne en charge de l’approbation les demande et renvoie la campagne à l’état « Version préliminaire » pour les révisions. Une fois que tout est prêt, la personne en charge de l’approbation peut activer et lancer le parcours ou la campagne. [Découvrir comment réviser et approuver une demande](review-approve-request.md)

## Surveiller les demandes d’approbation {#monitor}

Vous pouvez surveiller toutes les demandes d’approbation et de modification qui ont été soumises pour un parcours donné ou une campagne donnée. Pour ce faire, cliquez sur l’icône **[!UICONTROL Afficher le journal d’audit]** située dans la section supérieure droite de la zone de travail du parcours ou de l’écran de révision de la campagne.

![Journal d’audit des demandes d’approbation](assets/monitor-requests.png)

## Questions fréquentes {#faq}

+++Dois-je créer une politique d’approbation pour chaque campagne ou parcours ?

Non. Les politiques d’approbation sont conditionnelles. Vous ne devez créer une politique que si vous souhaitez imposer la révision d’un ensemble spécifique de campagnes ou de parcours (par exemple, toutes les campagnes planifiées créées par une équipe donnée). Si aucune politique ne s’applique à une campagne ou à un parcours, le créateur ou la créatrice peut publier directement sans demander d’approbation.

+++

+++Que se passe-t-il si la personne approbatrice n’est pas disponible ?

La demande reste « En révision » jusqu’à ce qu’une personne approbatrice s’en charge. Vous pouvez annuler la demande (ce qui redonne à l’élément le statut « Brouillon ») et la soumettre à nouveau dès que la personne approbatrice appropriée est disponible. L’équipe d’administration peut également mettre à jour la politique d’approbation pour ajouter des personnes approbatrices.

+++

+++Puis-je modifier une campagne ou un parcours lorsqu’il est en attente d’approbation ?

Non. Une fois soumis(e) à approbation, la campagne ou le parcours est verrouillé(e) au statut « En révision ». Pour apporter des modifications, la personne créatrice ou approbatrice doit d’abord annuler la demande. L’élément retrouve son statut « Brouillon » et peut être modifié avant un nouvel envoi.

+++

+++Je ne vois pas l’autorisation Approuver et publier dans la liste déroulante. Que dois-je vérifier ?

Vérifiez que vous ajoutez d’abord la bonne ressource. L’autorisation **Approuver et publier des campagnes** nécessite l’ajout de la ressource **Campagnes** au rôle et l’autorisation **Approuver et publier des parcours** nécessite l’ajout de la ressource **Parcours**. Les deux ressources doivent être ajoutées séparément. [Découvrez comment attribuer des autorisations liées à l’approbation.](#prerequisites)

+++

+++Comment [!DNL Journey Optimizer] détermine-t-il la politique d’approbation à appliquer lorsque plusieurs politiques sont applicables ?

Lorsque plusieurs politiques d’approbation actives peuvent s’appliquer au même parcours ou à la même campagne, la politique **activée la plus récemment** est prioritaire. Les groupes d’utilisateurs approbateurs définis dans cette politique sont ceux qui sont avertis et qui traitent la demande.

[En savoir plus](approval-policies.md#multiple-policies)

+++

+++Si la personne qui soumet la demande appartient à plusieurs groupes d’utilisateurs, peut-elle choisir à quel groupe la demande d’approbation est envoyée ?

Non. La personne qui soumet la demande ne peut pas sélectionner manuellement le groupe d’utilisateurs qui reçoit la demande d’approbation. Les groupes d’utilisateurs spécifiés dans la politique d’approbation qui s’applique (selon la [priorité de la politique](approval-policies.md#multiple-policies)) sont automatiquement avertis.

+++

## Ressources supplémentaires

* **[Créer des politiques de validation](approval-policies.md)** ; découvrez comment configurer des politiques de validation pour appliquer des workflows de révision aux campagnes et aux parcours.
* **[Demande d’approbation](request-approval.md)** ; découvrez comment soumettre du contenu pour approbation et suivre le statut de la demande.
* **[Révision et approbation des demandes](review-approve-request.md)** ; découvrez comment examiner, approuver ou refuser des demandes d’approbation en tant que personne en charge de l’approbation.
* **[Simuler avec des données d’exemple](simulate-sample-input.md)** ; découvrez comment tester et valider le contenu à l’aide de données de profil d’exemple.
