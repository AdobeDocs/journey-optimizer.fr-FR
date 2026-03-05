---
solution: Journey Optimizer
product: journey optimizer
title: Modification de modèles d’e-mail à l’aide de l’éditeur HTML avancé
description: Utilisez le mode Expert pour afficher et modifier la source de contenu d’e-mail HTML dans l’éditeur WYSIWYG, avec un contrôle d’indicateur de fonctionnalité, des mécanismes de sécurisation et une validation de l’enregistrement.
feature: Templates
topic: Content Management
role: User
hidefromtoc: true
hide: true
level: Experienced
source-git-commit: 74102069afa519898149de33f890568950571f26
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 5%

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

Lorsque vous utilisez l’éditeur HTML avancé, les mécanismes de sécurisation suivants sont en place pour protéger la compatibilité du contenu et définir les attentes.

* Actuellement, il n’existe **aucun processus de validation** dans l’éditeur HTML avancé. Les erreurs de syntaxe et les dispositions rompues ne sont pas vérifiées. Veillez à examiner attentivement votre contenu avant d’enregistrer.

* Les futures mises à jour du système peuvent annuler les modifications apportées au balisage par défaut. Gardez à l’esprit que **vos modifications peuvent être remplacées**.

* Les problèmes causés par le code personnalisé et les modifications manuelles **ne peuvent pas être résolus** ni par l’équipe d’assistance [!DNL Adobe]. Assurez-vous de disposer d’une sauvegarde de votre contenu au cas où vous auriez besoin de revenir à une version précédente.

* Pour garantir la compatibilité du contenu, l’enregistrement **n’est pas disponible** dans la vue HTML avancée. Lorsque vous êtes prêt à enregistrer vos modifications, vous devez revenir à la vue Bureau.

>[!WARNING]
>
>L’éditeur HTML avancé dans le modèle de contenu n’est pas identique au mode **[!UICONTROL Coder le vôtre]** dans le Designer d’e-mail. En mode [!UICONTROL Coder le vôtre], vous ne pouvez pas revenir à l’éditeur visuel ; une fois que vous avez choisi ce chemin, vous restez en édition uniquement codée. L’éditeur HTML avancé, en revanche, vous permet de basculer entre les vues HTML et Bureau (visuelle) à tout moment. [En savoir plus sur l’éditeur de code](../email/code-content.md).

## Basculer vers la vue HTML avancée {#switch-to-desktop-view}

1. Ouvrez ou créez un [modèle d’e-mail](../content-management/create-content-templates.md) et ouvrez le [Designer d’e-mail](../email/get-started-email-design.md) pour modifier le contenu.

1. Cliquez sur le bouton **[!UICONTROL HTML]** dans le coin supérieur droit de l’écran.

   ![](assets/email-template-expert-mode-button.png)

1. Lors de la première ouverture de l’éditeur HTML avancé, un message d’avertissement s’affiche. Examinez-le attentivement et cliquez sur **[!UICONTROL OK]** pour continuer. [En savoir plus](#guardrails)

   >[!NOTE]
   >
   >Cet avertissement s’affiche uniquement la première fois que vous ouvrez l’éditeur HTML avancé et se réinitialise chaque mois.

   ![](assets/email-template-expert-mode-warning.png)

1. L’éditeur HTML avancé s’affiche.

   ![](assets/email-template-expert-mode.png)

1. Ajoutez les modifications souhaitées au contenu de votre e-mail.

   >[!WARNING]
   >
   >Veillez à saisir le code HTML et CSS correct, car il n’existe aucun processus de validation de la syntaxe et aucune prise en charge n’est fournie par [!DNL Adobe]. [En savoir plus](#guardrails)

1. L’enregistrement n’est pas disponible dans la vue HTML avancée. Revenez à la vue Bureau pour enregistrer vos modifications.

   &lt;![](assets/email-template-expert-mode-save.png)

   >[!NOTE]
   >
   >Le contenu ne peut être enregistré dans la vue Bureau que pour des raisons de compatibilité du contenu. Vos modifications sont conservées lorsque vous changez de vue.
