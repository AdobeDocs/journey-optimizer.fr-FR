---
title: Utiliser le rapport de spam
description: Découvrez comment utiliser le rapport de spam.
feature: Preview
role: User
level: Beginner
badge: label="Version bêta"
hide: true
hidefromtoc: true
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: 8dacf28f4c3217a57e648b3c80e1724d9794c9ea
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 34%

---

# Rapport Email spam {#spam-report}

[!DNL Journey Optimizer] vous permet de vérifier les performances de votre contenu par rapport au filtrage du spam et de vous assurer que vos messages arrivent dans les boîtes de réception de vos clientes et clients, et non dans les spams.

Lors de l&#39;édition ou de la prévisualisation du contenu de votre email, la variable **[!UICONTROL Rapport Spam]** fournit une notation et des conseils afin d’améliorer les scores de chaque élément répertorié.

Cela vous permet de déterminer si un message risque d’être considéré comme indésirable par les outils anti-spam utilisés à sa réception et d’agir dans le cas contraire. De nombreux fournisseurs de messagerie utilisent des outils dans le cadre de leur processus de filtrage du spam. L’envoi d’emails avec un mauvais score peut considérablement affecter votre délivrabilité.


>[!CAUTION]
>
>* Cette fonctionnalité est actuellement disponible uniquement en version bêta privée.
>
>* Pour l’instant, l’analyse du rapport de spam ne peut être effectuée que pour le contenu en anglais.
>
>* >
>Le rapport Spam est informatif et n&#39;empêche pas l&#39;envoi de messages dont le score est mauvais.

Pour accéder au **[!UICONTROL Rapport Spam]**, suivez les étapes ci-dessous.

1. Dans l’écran **[!UICONTROL Simuler]**, cliquez sur le bouton **[!UICONTROL Rapport de spam]**.

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. Une vérification anti-spam est automatiquement effectuée et la fenêtre **[!UICONTROL Rapport de spam]** affiche les résultats. Elle indique comment se comporte votre contenu en termes de disposition du corps, de structure, de taille d’image, de mots déclencheurs de spam, le cas échéant, etc.

   ![](assets/spam-report-high-score.png)

1. Vérifiez les scores et les descriptions de chaque élément.

   Plus le score est bas, mieux c&#39;est. Si le score est supérieur à 5, un avertissement s&#39;affiche : il indique que certains messages peuvent être bloqués ou marqués comme spam à la réception.

1. Selon cette notation, si vous considérez que certains éléments peuvent être améliorés, modifiez votre contenu dans la variable [Concepteur d&#39;email](../email/content-from-scratch.md) et effectuez les mises à jour nécessaires.

1. Une fois vos modifications effectuées, revenez à la **[!UICONTROL Rapport Spam]** pour vous assurer que votre score a été amélioré.

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
