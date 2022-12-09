---
title: Extension Visual Editing Helper
description: Découvrez l’extension Chrome Visual Editing Helper qui vous permet de créer et de prévisualiser des pages web dans Journey Optimizer.
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: f4a0ec45-d624-4f80-b888-42e5987cdc4f
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Extension Visual Editing Helper {#visual-editing-helper}

Afin de créer rapidement et de prévisualiser vos expériences web, l’extension de navigateur Adobe Experience Cloud Visual Editing Helper pour Google Chrome vous permet de charger des sites web de manière fiable dans Adobe [!DNL Journey Optimizer] web designer.

>[!NOTE]
>
>La fonctionnalité de canal web est actuellement disponible en version bêta pour sélectionner uniquement les utilisateurs.

## Installation de l’extension Visual Editing Helper {#install-visual-editing-helper}

Pour obtenir et installer l’extension de navigateur Visual Editing Helper, procédez comme suit.

1. Dans la boutique Web Google Chrome, accédez au [Assistant d’édition visuelle d’Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca)Extension de navigateur {target=&quot;_blank&quot;}.

1. Cliquez sur **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]**.

1. Créez une campagne de canal web dans [!DNL Journey Optimizer]. [Découvrez comment](author-web.md#create-web-campaign)

1. Ouvrez le [!DNL Journey Optimizer] web designer pour commencer à créer votre expérience web. [En savoir plus](author-web.md)

1. Assurez-vous que l’extension de navigateur Visual Editing Helper est activée dans la barre d’outils du navigateur Chrome en cliquant sur l’icône correspondante.

   ![](assets/web-visual-editing-extension.png)

L’assistant d’édition visuelle d’Adobe Experience Cloud est désormais automatiquement activé lorsqu’un site web est ouvert dans la variable [!DNL Journey Optimizer] web designer pour optimiser la création.

L’extension ne dispose d’aucun paramètre conditionnel et gère automatiquement tous les paramètres, y compris les paramètres des cookies SameSite.

>[!NOTE]
>
>Certains sites web peuvent ne pas s’ouvrir de manière fiable dans la variable [!DNL Journey Optimizer] web designer pour l’une des raisons suivantes :
>
> * Le site web a des politiques de sécurité strictes.
> * Le site web est dans un iframe.
> * Le site d’assurance qualité ou d’évaluation du client n’est pas disponible pour le monde extérieur (le site est interne).


## Dépannage

Lors de l’utilisation d’Adobe [!DNL Journey Optimizer] concepteur web, si vous tentez de charger un site web dont le chargement échoue, un message s’affiche vous suggérant d’installer le [Extension Visual Editing Helper du navigateur](#install-visual-editing-helper).

Si le SDK Web d’Adobe Experience Platform n’est pas encore mis en oeuvre sur le site web, un message s’affiche dans le concepteur web pour vous suggérer d’installer l’extension de navigateur Visual Editing Helper et d’implémenter l’ [SDK Web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=&quot;_blank&quot;}.

Si le site ne se charge pas ou se comporte de manière inattendue, un correctif potentiel consiste à accepter les cookies sur votre site web dans le navigateur avant de tenter de le charger dans Adobe. [!DNL Journey Optimizer].

Pour les pages sous authentification, si le chargement de la page de connexion échoue ou si, après avoir tenté de vous connecter, vous n’êtes toujours pas connecté, essayez d’abord de vous connecter dans un autre onglet de votre navigateur, puis chargez le site web dans Adobe. [!DNL Journey Optimizer] web designer.
