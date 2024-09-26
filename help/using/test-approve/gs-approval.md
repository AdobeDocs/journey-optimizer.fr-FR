---
title: Prise en main de la validation des parcours et campagnes
description: Découvrez comment configurer un processus d’approbation pour vos parcours et campagnes.
role: User
level: Beginner
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: dd4173698d7034173b7ae9f44afec397d62a6f78
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 18%

---


# Prise en main de la validation des parcours et campagnes {#send-proofs}

>[!AVAILABILITY]
>
> Actuellement, les stratégies d’approbation ne sont disponibles que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

## Prise en main des stratégies d’approbation {#gs}

Journey Optimizer vous permet de configurer un processus d’approbation qui permet aux équipes marketing de vérifier que les campagnes et les parcours sont examinés et approuvés par les parties prenantes appropriées avant qu’ils ne soient mis en ligne.

Les stratégies de validation introduisent un workflow structuré directement dans l’interface utilisateur, éliminant ainsi la nécessité de recourir à des supports externes tels que des outils de gestion des emails ou des tâches, et assurant la gestion et le suivi centralisés de toutes les validations.

En outre, cette fonctionnalité offre un meilleur contrôle sur la publication de vos parcours et campagnes : le processus d’approbation étant incorporé dans Journey Optimizer, les campagnes et les parcours restent dans un état &quot;verrouillé&quot; pendant la révision, ce qui garantit qu’aucune modification ou activation involontaire ne se produit avant que toutes les validations nécessaires ne soient mises en place.

## Conditions préalables {#prerequisites}

Avant de commencer, vérifiez que les autorisations ci-dessous ont été configurées.

Pour accéder aux parcours et campagnes d’approbation et de publication, les utilisateurs doivent se voir accorder les autorisations **Approuver et publier des campagnes** et **Approuver et publier des Parcours**. [En savoir plus](../administration/permissions.md)

+++  Découvrez comment attribuer des autorisations liées à l’approbation

1. Dans le produit **Autorisations**, accédez à l’onglet **Rôles** et sélectionnez le **Rôle** de votre choix.

1. Cliquez sur **Modifier** pour modifier les autorisations.

1. Ajoutez la ressource **Campagnes**, puis sélectionnez **Approuver et publier des campagnes** dans le menu déroulant.

   ![](assets/permissions_approval.png){zoomable="yes"}

1. Ajoutez la ressource **Parcours**, puis sélectionnez **Approuver et publier des Parcours** dans le menu déroulant.

   ![](assets/permissions_approval_2.png){zoomable="yes"}

1. Cliquez sur **Enregistrer** pour appliquer vos modifications.

Les autorisations des personnes déjà affectées à ce rôle seront automatiquement mises à jour.

1. Pour attribuer ce rôle à de nouvelles personnes, accédez à l’onglet **Utilisateurs et utilisatrices** du tableau de bord **Rôles** et cliquez sur **Ajouter un utilisateur ou une utilisatrice**.

1. Saisissez le nom de la personne, son adresse e-mail ou choisissez dans la liste, puis cliquez sur **Enregistrer**.

1. Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez cette [documentation](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/abac/permissions-ui/users).

La personne recevra un e-mail avec des instructions pour accéder à votre instance.

+++

## Présentation du processus de validation {#process}

Le processus global d&#39;approbation est le suivant :

![](assets/approval-process.png){zoomable="yes"}

1. **Configuration des stratégies d’approbation**

   Un administrateur crée une stratégie de validation qui définit les conditions dans lesquelles la stratégie doit s’appliquer aux parcours ou aux campagnes. Vous pouvez par exemple créer une stratégie d’approbation qui exige que toutes les campagnes planifiées créées par un utilisateur donné soient approuvées avant d’être activées. [Découvrez comment créer des stratégies d’approbation](approval-policies.md)

1. **Envoi de campagne/parcours pour approbation**

   Les créateurs de la campagne/du parcours créent un parcours ou une campagne et l’envoient pour approbation. La campagne/le parcours entre dans un état &quot;En révision&quot;, durant lequel aucune modification ne peut être effectuée, sauf si la demande est annulée. [Découvrez comment demander l’approbation](request-approval.md)

   >[!NOTE]
   >
   >Les campagnes et les parcours ne doivent être soumis à validation que si une stratégie de validation est en place. Si aucune stratégie de ce type ne s’applique, le créateur peut publier directement la campagne ou le parcours sans nécessiter d’approbation.

1. **Révision et approbation**

   Le ou les approbateurs définis dans la politique de validation qui s&#39;applique au parcours ou à l&#39;opération reçoivent une notification. Ils peuvent consulter le contenu, l’audience et les paramètres du parcours ou de la campagne. Si des modifications sont nécessaires, l’approbateur les demande, renvoyant la campagne à &quot;Version préliminaire&quot; pour les révisions. S’ils sont prêts, ils peuvent activer et lancer le parcours ou la campagne. [Découvrez comment réviser et approuver une requête](review-approve-request.md)

## Surveiller les demandes d’approbation {#monitor}

Vous pouvez surveiller toutes les demandes d’approbation et de modification qui ont été soumises pour un parcours ou une campagne donné. Pour ce faire, cliquez sur le bouton **[!UICONTROL Afficher le journal d’audit]** situé dans la section supérieure droite du canevas de parcours ou de l’écran de révision de la campagne.

![](assets/monitor-requests.png)
