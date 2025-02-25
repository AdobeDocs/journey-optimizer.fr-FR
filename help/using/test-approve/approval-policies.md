---
title: Créer et gérer des politiques d’approbation
description: Découvrez comment créer et gérer des politiques d’approbation.
role: User
level: Beginner
feature: Approval
exl-id: e518cb3c-f361-43a4-b9a5-ec070c612e75
source-git-commit: 99099cb6b705cb5a7b97652154c42f0565fdfdb9
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 83%

---

# Créer et gérer des politiques d’approbation {#approval-policies}


>[!CONTEXTUALHELP]
>id="ajo_approval_policy_request_approval"
>title="Demander l’approbation"
>abstract="Demander l’approbation"

>[!CONTEXTUALHELP]
>id="ajo_approval_policy_request_change"
>title="Demander une modification"
>abstract="Demander une modification"


>[!NOTE]
>
>Pour créer des politiques d’approbation, vous devez disposer de droits d’administration du système ou du produit dans Adobe Experience Platform. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/home)

Les politiques d’approbation permettent à l’équipe d’administration d’établir un processus de validation pour les parcours et les campagnes. Ce système décrit des conditions spécifiques qui déterminent si un parcours ou une campagne nécessite une approbation. Ces politiques peuvent être d’une complexité variable, allant du simple fait d’exiger que toutes les campagnes soient examinées par une personne ou une équipe spécifique à l’établissement de critères en fonction de la personne qui a créé la campagne.

## Créer des politiques d’approbation {#create-policies}

>[!CONTEXTUALHELP]
>id="ajo_permissions_approval_policy"
>title="Nouvelle politique d’approbation"
>abstract="Dans cet écran, saisissez le nom et sélectionnez le contexte de la stratégie d&#39;approbation, puis créez les conditions pour déterminer qui peut lancer la demande d&#39;approbation et qui peut la valider."

Pour créer une politique d’approbation, procédez comme suit :

1. Dans Journey Optimizer, dans le menu **[!UICONTROL Administration]**, accédez à **[!UICONTROL Autorisations]**, puis à **[!UICONTROL Politiques]**.

   ![](assets/policy_create_1.png)

1. Cliquez sur **[!UICONTROL Créer]** dans l’onglet **[!UICONTROL Politique d’approbation]**, sélectionnez **[!UICONTROL Politique d’approbation]**, puis cliquez sur **[!UICONTROL Confirmer]**.

1. Saisissez un **[!UICONTROL nom]** et une **[!UICONTROL description]** pour la politique.

1. Indiquez si la politique s’appliquera à des **[!UICONTROL parcours]** ou à des **[!UICONTROL campagnes]**.

   ![](assets/policy_create_2.png)

Vous pouvez maintenant affiner les conditions pour spécifier qui peut initier la demande d&#39;approbation et qui peut la valider.

## Définir les conditions des politiques d’approbation {#conditions}

Pour définir les conditions associées à une politique d’approbation, procédez comme suit :

1. Accédez à votre **[!UICONTROL politique d’approbation]**.

1. Dans le menu **[!UICONTROL Si]**, cliquez sur **[!UICONTROL Ajouter une condition]** pour définir quel objet ou quelle personne déclenchera une demande d’approbation.

1. Sélectionnez la **[!UICONTROL catégorie]**, la **[!UICONTROL règle de correspondance]** et les **[!UICONTROL options]** appropriées.

   Par exemple, « Si Action correspond à un Courrier » ou « Si Nom du demandeur ou de la demandeuse correspond à Jean Dupont ».

   ![](assets/policy_condition_1.png)

+++ En savoir plus sur les catégories et options disponibles
   <table>
    <tr>
      <th>Catégorie</th>
      <th>Option</th>
    </tr>
    <tr>
      <td rowspan="3">Type de campagne</td>
      <td>Planifié (marketing)</td>
    </tr>
    <tr>
    <td>Déclenché par l’API (marketing)</td>
    </tr>
    <tr>
    <td>Déclenché par l’API (transactionnel)</td>
    </tr>
    <tr>
    <td rowspan="8">Action</td>
    <td>In-app</td>
    </tr>
    <tr>
    <td>Notification push</td>
   </tr>
    <tr>
    <td>SMS</td>
    </tr>
    <tr>
    <td>E-mail</td>
    </tr>
    <tr>
    <td>Courrier</td>
    </tr>
    <tr>
    <td>Web</td>
    </tr>
    <tr>
    <td>Basé sur le code</td>
    </tr>
    <tr>
    <td>Carte de contenu</td>
    </tr>
    <tr>
    <td>Nom du demandeur ou de la demandeuse</td>
    <td>Nom et adresse e-mail du demandeur désigné ou de la demandeuse désignée</td>
    </tr>
    <tr>
    <td>Groupe d’utilisateurs et d’utilisatrices du demandeur ou de la demandeuse</td>
    <td>Nom du groupe d’utilisateurs et d’utilisatrices des demandeurs et demandeuses désignés</td>
    </tr>
    </table>


1. Pour ajouter d’autres critères, cliquez sur **[!UICONTROL Ajouter une condition]** pour définir des règles supplémentaires et sélectionnez **[!UICONTROL Et]** ou **[!UICONTROL Ou]** pour spécifier la manière dont les conditions sont connectées.

1. Dans le menu **[!UICONTROL Envoyer ensuite la demande d’approbation à]**, cliquez sur **[!UICONTROL Ajouter une condition]** pour définir qui peut accepter la demande d’approbation.

1. Dans la liste déroulante **[!UICONTROL Catégorie]**, indiquez si vous souhaitez choisir un groupe d’utilisateurs et d’utilisatrices ou une individuelle.

1. Ensuite, dans la liste déroulante **[!UICONTROL Option]**, sélectionnez le groupe d’utilisateurs et d’utilisatrice ou la personne spécifique.

   La personne sélectionnée ou le groupe d’utilisateurs et d’utilisatrices sélectionné sera responsable de la validation de la demande d’approbation.

   ![](assets/policy_condition_2.png)

1. Pour ajouter d’autres critères, cliquez sur **[!UICONTROL Ajouter une condition]** pour définir des règles supplémentaires et sélectionnez **[!UICONTROL Et]** ou **[!UICONTROL Ou]** pour spécifier la manière dont les conditions sont connectées.

1. Une fois votre politique entièrement configurée, cliquez sur **[!UICONTROL Enregistrer]**.

Vous pouvez maintenant activer votre politique d’approbation pour l’appliquer.

## Activer et gérer des politiques d’approbation {#activate-policies}

Pour appliquer votre stratégie d&#39;approbation, vous devez l&#39;activer. Pour ce faire, procédez comme suit :

1. Accédez à votre **[!UICONTROL politique d’approbation]**.

1. Cliquez ensuite sur **[!UICONTROL Activer]** pour appliquer les conditions configurées à votre environnement.

   >[!NOTE]
   >
   >Une fois activée, les politiques ne peuvent pas être modifiées. Pour modifier les conditions, désactivez d’abord la politique.

   ![](assets/policy_activate_1.png)

1. Dans le menu **[!UICONTROL Politique]**, ouvrez les options avancées pour **[!UICONTROL modifier]**, **[!UICONTROL désactiver]** ou **[!UICONTROL dupliquer]** la politique selon les besoins.

   ![](assets/policy_activate_2.png)
