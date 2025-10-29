---
title: Commencer avec l’approbation des parcours et des campagnes
description: Découvrez comment configurer un processus d’approbation pour vos parcours et campagnes.
role: User
level: Beginner
feature: Approval
exl-id: 92d1439e-5cac-4e7d-85f8-ebf432e9ef7c
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: ht
source-wordcount: '561'
ht-degree: 100%

---

# Commencer avec l’approbation des parcours et des campagnes {#send-proofs}

## Commencer avec les politiques d’approbation {#gs}

Journey Optimizer permet de définir des politiques d’approbation pour que les équipes de marketing puissent s’assurer que les campagnes et les parcours sont examinés et approuvés par les parties prenantes appropriées avant leur mise en ligne.

Les politiques d’approbation introduisent un workflow structuré directement dans l’interface d’utilisation, éliminant ainsi la nécessité de recourir à des supports externes tels que des outils de gestion des e-mails ou des tâches, tout en assurant la gestion et le suivi centralisés de toutes les approbations.

En outre, cette fonctionnalité offre un meilleur contrôle sur la publication de vos parcours et campagnes : le processus d’approbation étant incorporé dans Journey Optimizer, les campagnes et les parcours restent à l’état Verrouillé pendant la révision, ce qui garantit qu’aucune modification ou activation involontaire ne se produit avant que toutes les approbations nécessaires ne soient mises en place.

## Conditions préalables {#prerequisites}

Avant de commencer, vérifiez que les autorisations ci-dessous ont été configurées.

Pour accéder aux parcours et campagnes d’approbation et de publication, les utilisateurs et utilisatrices doivent se voir accorder les autorisations **Approuver et publier des campagnes** et **Approuver et publier des parcours**. [En savoir plus](../administration/permissions.md)

+++  Découvrir comment attribuer des autorisations liées à l’approbation

1. Dans le produit **Autorisations**, accédez à l’onglet **Rôles** et sélectionnez le **Rôle** de votre choix.

1. Cliquez sur **Modifier** pour modifier les autorisations.

1. Ajoutez la ressource **Campagnes**, puis sélectionnez **Approuver et publier des campagnes** dans le menu déroulant.

   ![](assets/permissions_approval.png){zoomable="yes"}

1. Ajoutez la ressource **Parcours**, puis sélectionnez **Approuver et publier des parcours** dans le menu déroulant.

   ![](assets/permissions_approval_2.png){zoomable="yes"}

1. Cliquez sur **Enregistrer** pour appliquer vos modifications.

Les autorisations des personnes déjà affectées à ce rôle seront automatiquement mises à jour.

1. Pour attribuer ce rôle à de nouvelles personnes, accédez à l’onglet **Utilisateurs et utilisatrices** du tableau de bord **Rôles** et cliquez sur **Ajouter un utilisateur ou une utilisatrice**.

1. Saisissez le nom de la personne, son adresse e-mail ou choisissez dans la liste, puis cliquez sur **Enregistrer**.

1. Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez cette [documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/abac/permissions-ui/users).

La personne recevra un e-mail avec des instructions pour accéder à votre instance.

+++

## Vue d’ensemble du processus d’approbation {#process}

Le processus d’approbation global se présente comme suit :

![](assets/approval-process.png){zoomable="yes"}

1. **Configuration des politiques d’approbation**

   L’équipe d’administration crée une politique d’approbation qui définit les conditions dans lesquelles la politique doit s’appliquer aux parcours ou aux campagnes. Vous pouvez par exemple créer une politique d’approbation qui exige que toutes les campagnes planifiées créées par une personne donnée soient approuvées avant d’être activées. [Découvrir comment créer des politiques d’approbation](approval-policies.md)

1. **Envoi de campagne/parcours pour approbation**

   Les personnes à l’origine de la campagne/du parcours créent un parcours ou une campagne et l’envoient pour approbation. La campagne/le parcours passe à l’état En révision, durant lequel aucune modification ne peut être effectuée, sauf si la demande est annulée. [Découvrir comment demander l’approbation](request-approval.md)

   >[!NOTE]
   >
   >Les campagnes et les parcours ne doivent être soumis à approbation que si une politique d’approbation est en place. Si aucune politique de ce type ne s’applique, le créateur ou la créatrice peut publier directement la campagne ou le parcours sans nécessiter d’approbation.

1. **Révision et approbation**

   Les personnes en charge de l’approbation définies dans la politique d’approbation qui s’applique au parcours ou à la campagne reçoivent une notification. Elles peuvent consulter le contenu, l’audience et les paramètres du parcours ou de la campagne. Si des modifications sont nécessaires, la personne en charge de l’approbation les demande et renvoie la campagne à l’état « Version préliminaire » pour les révisions. Une fois que tout est prêt, la personne en charge de l’approbation peut activer et lancer le parcours ou la campagne. [Découvrir comment réviser et approuver une demande](review-approve-request.md)

## Surveiller les demandes d’approbation {#monitor}

Vous pouvez surveiller toutes les demandes d’approbation et de modification qui ont été soumises pour un parcours donné ou une campagne donnée. Pour ce faire, cliquez sur l’icône **[!UICONTROL Afficher le journal d’audit]** située dans la section supérieure droite de la zone de travail du parcours ou de l’écran de révision de la campagne.

![](assets/monitor-requests.png)
