---
solution: Journey Optimizer
product: journey optimizer
title: Modification de modèles d’e-mail à l’aide de l’éditeur HTML avancé
description: Utilisez le mode Expert pour afficher et modifier la source de contenu d’e-mail HTML dans l’éditeur WYSIWYG, avec un contrôle d’indicateur de fonctionnalité, des mécanismes de sécurisation et une validation de l’enregistrement.
feature: Templates
topic: Content Management
role: User
level: Experienced
exl-id: 0c586565-0c65-435f-986d-cd08b59de159
source-git-commit: 145944952ad9aca752085588526f71e8034b8611
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 7%

---

# Modification de modèles d’e-mail à l’aide de l’éditeur HTML avancé {#email-template-expert-mode}

>[!AVAILABILITY]
>
>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en bénéficier.

L’**éditeur HTML avancé** est un mode expert qui vous permet d’afficher et de modifier le code source brut des modèles de contenu d’e-mail directement à partir de l’interface [!DNL Journey Optimizer] de Designer d’e-mail.

Cette fonctionnalité vous permet d’insérer des expressions avancées, telles que des conditions, directement dans la source. Lorsque vous revenez à la vue visuelle (Bureau), le contenu est rendu à nouveau afin que vous puissiez vérifier son aspect et continuer à le modifier dans l’une ou l’autre des vues.

>[!NOTE]
>
>Cette fonctionnalité n’est disponible que dans les modèles de contenu et pour le canal E-mail .

## Mécanismes de sécurisation {#guardrails}

Lorsque vous utilisez l’éditeur HTML avancé, les mécanismes de sécurisation suivants protègent la compatibilité du contenu et définissent les attentes.

* L’éditeur HTML avancé **ne valide pas** votre code. Il ne vérifie pas les erreurs de syntaxe ou les mises en page rompues. Examinez attentivement votre contenu avant d’enregistrer.

* Les futures mises à jour du système peuvent remplacer les modifications apportées aux balises par défaut. **Vos modifications peuvent ne pas persister**.

* L’équipe d’assistance [!DNL Adobe] **ne peut pas résoudre les problèmes liés au code personnalisé et aux modifications manuelles**. Conservez une sauvegarde de votre contenu au cas où vous auriez besoin d’effectuer une restauration.

* Vous ne pouvez pas simuler le contenu dans la vue HTML avancée. Basculez vers la vue Bureau pour prévisualiser votre contenu.

* Pour garantir la compatibilité du contenu, **vous ne pouvez pas enregistrer** dans la vue HTML avancée. Revenez à la vue Bureau lorsque vous êtes prêt à enregistrer vos modifications.

>[!WARNING]
>
>L’éditeur HTML avancé dans le modèle de contenu n’est pas identique au mode **[!UICONTROL Coder le vôtre]** dans le Designer d’e-mail. En mode [!UICONTROL Coder le vôtre], vous ne pouvez pas revenir à l’éditeur visuel ; une fois que vous avez choisi ce chemin, vous restez en édition uniquement codée. L’éditeur HTML avancé, en revanche, vous permet de basculer entre les vues HTML et Bureau (visuelle) à tout moment. [En savoir plus sur l’éditeur de code](../email/code-content.md).

## Basculer vers la vue HTML avancée {#switch-to-html-view}

Pour ouvrir l’éditeur HTML avancé et modifier la source du modèle, procédez comme suit.

1. Ouvrez ou créez un [modèle d’e-mail](../content-management/create-content-templates.md) et ouvrez le [Designer d’e-mail](../email/get-started-email-design.md) pour modifier le contenu.

1. Cliquez sur le bouton **[!UICONTROL HTML]** dans le coin supérieur droit de l’écran.

   ![Emplacement du bouton HTML dans la barre d’outils Designer d’email](assets/email-template-expert-mode-button.png)

1. Lors de la première ouverture de l’éditeur HTML avancé, un message d’avertissement s’affiche. Examinez-le attentivement et cliquez sur **[!UICONTROL OK]** pour continuer. [En savoir plus](#guardrails)

   ![Boîte de dialogue d’avertissement lors de la première ouverture de l’éditeur HTML avancé](assets/email-template-expert-mode-warning.png){zoomable="yes"}

   >[!NOTE]
   >
   >Cet avertissement s’affiche uniquement la première fois que vous ouvrez l’éditeur HTML avancé et se réinitialise chaque mois.

1. L’éditeur HTML avancé s’affiche.

   ![Interface avancée de l’éditeur HTML affichant le code source du modèle d’e-mail](assets/email-template-expert-mode.png)

1. Ajoutez les modifications souhaitées au contenu de votre e-mail.

   >[!WARNING]
   >
   >Veillez à saisir le code HTML et CSS correct, car il n’existe aucun processus de validation de la syntaxe et aucune prise en charge n’est fournie par [!DNL Adobe]. [En savoir plus](#guardrails)

1. La simulation et l’enregistrement de contenu ne sont pas disponibles dans la vue HTML avancée pour des raisons de compatibilité. Revenez à la vue Bureau pour prévisualiser votre contenu et enregistrer vos modifications.

   ![Revenez à la vue Bureau pour enregistrer vos modifications](assets/email-template-expert-mode-save.png){zoomable="yes"}

   >[!NOTE]
   >
   >Vos modifications sont conservées lorsque vous changez de vue.

<!--
    ![](assets/email-template-expert-mode-simulate.png){zoomable="yes"}-->

## Rubriques connexes

* [Codage de votre propre contenu d&#39;e-mail](../email/code-content.md)
* [Créer des modèles de contenu](create-content-templates.md)
* [Prise en main du concepteur d’e-mail](../email/get-started-email-design.md)

