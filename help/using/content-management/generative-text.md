---
solution: Journey Optimizer
product: journey optimizer
title: Générer du texte avec l’assistant IA
description: Découvrez comment générer du texte avec l’assistant IA dans Journey Optimizer.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
exl-id: 9dd3970c-cf24-424c-b734-f30571374942
TQID: https://experienceleague.adobe.com/-XlVD0y5JOVf04u8AolPd3c5MQmt9h39gC-aulCjp6c
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: d6e0d39b-5df3-4c72-8263-fd834397ee97
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: dc3ac795cd3cbfbd3dd3adfe6f220641d331081f
workflow-type: tm+mt
source-wordcount: 1694
ht-degree: 91%

---

# Générer du texte avec l’assistant IA {#generative-text}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment générer, affiner et finaliser le contenu textuel de la marque avec l’assistant AI pour les canaux e-mail, web, de page de destination, de notification push et de SMS dans Adobe Journey Optimizer.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Avant de commencer à utiliser cette fonctionnalité, lisez les [Mécanismes de sécurisation et limites](gs-generative.md#generative-guardrails) associés.
></br>
>
>Vous devez accepter un [contrat d’utilisation](https://www.adobe.com/fr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) avant de pouvoir utiliser l’Assistant IA dans Journey Optimizer. Pour plus d’informations, contactez votre représentant ou représentante Adobe.

Utilisez l’assistant IA dans Journey Optimizer pour générer du contenu engageant et adapté à votre audience. Que vous ayez besoin d’enrichir le contenu des e-mails, de créer du contenu web attrayant, de concevoir un texte de page de destination convaincant, d’écrire des messages de notification push ou de composer des SMS, l’assistant IA vous aide à diffuser du texte percutant.

## Pour les canaux e-mail et web {#email-web-channels}

L’assistant IA peut générer du texte de grande qualité pour vos campagnes par e-mail, vos expériences web et vos pages de destination. Cette fonctionnalité vous permet de créer des messages attrayants et conformes à votre marque, qui résonnent auprès de votre audience sur l’ensemble des points de contact numériques.

### Accès et configuration {#access-configure}

Avant de pouvoir commencer à générer du texte avec l’assistant IA, vous devez configurer votre campagne ou votre parcours et accéder à l’éditeur de contenu. Pour préparer votre espace de travail et ouvrir le panneau de l’assistant IA, procédez comme suit.

1. Créez et configurez votre campagne ou votre parcours :

   * **E-mail** : après avoir créé et configuré votre campagne, cliquez sur **[!UICONTROL Modifier le contenu]**. [En savoir plus](../email/create-email.md)
   * **Web** : après avoir créé et configuré votre page web, cliquez sur **[!UICONTROL Modifier la page web]**. [En savoir plus](../web/create-web.md)
   * **Page de destination** : après avoir créé et configuré votre page de destination, cliquez sur **[!UICONTROL Ouvrir le concepteur]**. [En savoir plus](../landing-pages/create-lp.md)

1. Sélectionnez un **[!UICONTROL composant de texte]** pour cibler uniquement un contenu spécifique et accédez au menu **[!UICONTROL Assistant IA]** (ou **[!UICONTROL Afficher l’assistant IA]** pour le web).

   ![Composant de texte sélectionné avec le menu Assistant IA ouvert](assets/text-genai-1.png){zoomable="yes"}

### Générer du contenu {#generate-content}

Découvrez comment créer des prompts clairs, affiner les paramètres et générer du texte personnalisé à l’aide de l’assistant IA, en veillant à ce que vos messages s’alignent sur votre marque et vos objectifs de communication.

1. Activez l’option **[!UICONTROL Utiliser le contenu original]** pour que l’Assistant IA personnalise le nouveau contenu en fonction du contenu sélectionné.

1. Sélectionnez votre **[!UICONTROL Marque]** pour vous assurer que le contenu généré par l’IA correspond aux spécifications de celle-ci. [En savoir plus](brands.md) sur les marques.

1. Affinez le contenu en décrivant ce que vous souhaitez générer dans le champ **[!UICONTROL Prompt]**.

   Si vous avez besoin d’aide pour concevoir votre prompt, accédez à la **[!UICONTROL Bibliothèque de prompts]** qui offre un large éventail d’idées d’invites pour améliorer vos campagnes.

   ![Panneau de génération de texte de l’assistant IA avec champ de prompt et sélecteur de marque](assets/text-genai-2.png){zoomable="yes"}

1. Adaptez votre prompt avec l’option **[!UICONTROL Paramètres de texte]** :

   * **[!UICONTROL Stratégie de communication]** : choisissez le style de communication le plus adapté au texte généré.
   * **[!UICONTROL Langues]** : sélectionnez la langue du contenu généré.
   * **[!UICONTROL Ton]** : le ton doit trouver écho auprès de votre audience. Que vous souhaitiez communiquer de façon informative, ludique ou convaincante, l’assistant IA peut adapter le message en conséquence.
   * **Longueur de texte** : utilisez le curseur pour sélectionner la longueur souhaitée de votre texte.

   ![Paramètres de texte développés affichant les options](assets/text-genai-4.png){zoomable="yes"}

1. Depuis le menu **[!UICONTROL Ressources de marque]**, cliquez sur **[!UICONTROL Charger une ressource de marque]** pour ajouter toute ressource de marque incluant du contenu pouvant fournir du contexte supplémentaire à l’Assistant IA ou sélectionnez-en une chargée précédemment.

   Les fichiers précédemment chargés sont disponibles dans la liste déroulante **[!UICONTROL Ressources de marque chargées]**. Activez simplement les ressources que vous souhaitez inclure dans votre génération.

   ![Menu déroulant Ressources de marque](assets/text-genai-3.png){zoomable="yes"}

1. Lorsque votre prompt est prêt, cliquez sur **[!UICONTROL Générer]**.

### Affiner et finaliser {#refine-finalize}

Découvrez comment réviser le texte généré, apporter des améliorations et appliquer une personnalisation pour finaliser votre contenu, créer des messages soignés et attrayants prêts à être diffusés.

1. Parcourez les **[!UICONTROL variations]** générées.

   Cliquez sur **[!UICONTROL Aperçu]** pour afficher une version en plein écran de la variation sélectionnée ou cliquez sur **[!UICONTROL Appliquer]** pour remplacer votre contenu actuel.

1. Cliquez sur l’icône de pourcentage pour afficher votre **[!UICONTROL score d’alignement sur la marque]** et identifier tout décalage avec votre marque.

   En savoir plus sur le [score d’alignement sur la marque](brands-score.md).

   ![Variations de texte générées avec le score d’alignement sur la marque](assets/text-genai-6.png){zoomable="yes"}

1. Accédez à l’option **[!UICONTROL Affiner]** dans la fenêtre **[!UICONTROL Aperçu]** pour accéder à d’autres fonctionnalités de personnalisation :

   * **[!UICONTROL Utiliser comme contenu de référence]** : la variante choisie servira de contenu de référence pour générer d’autres résultats.

   * **[!UICONTROL Reformuler]** : réécrivez le message tout en préservant sa signification. Cette option vous permet de générer une autre formulation, d’améliorer le flux ou d’ajuster les expressions sans modifier le message principal.

   * **[!UICONTROL Utiliser un langage simplifié]** : utilisez l’assistant IA pour simplifier votre langage, garantissant ainsi clarté et accessibilité pour une audience plus large.

   * **[!UICONTROL Changer de ton]** : ajustez le ton du message pour mieux correspondre à votre style de communication, c’est-à-dire le rendre plus convivial, professionnel, urgent ou inspirant.

   * **[!UICONTROL Modifier la stratégie de communication]** : modifiez l’approche des messages en fonction de vos objectifs, par exemple créer un sentiment d’urgence ou mettre en avant un aspect attractif et enthousiasmant.

   ![Menu des options d’affinement](assets/text-genai-5.png){zoomable="yes"}

1. Ouvrez l’onglet **[!UICONTROL Alignement sur la marque]** pour voir comment votre contenu s’aligne sur vos [directives de marque](brands.md).

1. Cliquez sur **[!UICONTROL Sélectionner]** une fois que vous avez trouvé le contenu approprié.

1. Insérez des champs de personnalisation pour personnaliser votre contenu en fonction des données des profils. Ensuite, utilisez une méthode de simulation pour contrôler le rendu et vérifier les paramètres de personnalisation : cliquez sur **[!UICONTROL Simuler du contenu]** pour tester les variations de contenu avec des exemples de données d’entrée ou la génération automatique de l’IA, ou cliquez sur **[!UICONTROL Simuler du contenu]**, puis sélectionnez **[!UICONTROL Simuler du contenu (profils AEP)]** dans la liste déroulante pour obtenir un aperçu avec des profils de test. [En savoir plus](../content-management/preview-test.md)

1. Examinez et activez votre contenu :
   * **E-mail** : lorsque vous avez défini le contenu, l’audience et le planning, vous pouvez préparer votre campagne par e-mail. [En savoir plus](../campaigns/review-activate-campaign.md)
   * **Web** : une fois que vous avez défini les paramètres de la campagne web et que vous avez modifié le contenu selon vos besoins, vous pouvez passer en revue et activer votre campagne web. [En savoir plus](../web/create-web.md#activate-web-campaign)
   * **Page de destination** : une fois votre page de destination prête, vous pouvez la publier afin de pouvoir l’utiliser dans un message. [En savoir plus](../landing-pages/create-lp.md#publish-landing-page)

## Pour les canaux mobiles {#mobile-channels}

L’assistant IA peut générer du contenu texte attrayant pour vos notifications push et vos SMS, ce qui vous permet de créer des communications mobiles attrayantes qui touchent votre audience sur l’ensemble des points de contact mobiles.

### Accès et configuration {#mobile-access-configure}

Avant de commencer à générer du texte avec l’assistant IA pour les canaux mobiles, vous devez configurer votre campagne et accéder à l’assistant IA. La méthode d’accès varie légèrement entre les notifications push et les SMS.

1. Créez et configurez votre campagne mobile :
   * **Notifications push** : après avoir créé et configuré votre campagne de notifications push, cliquez sur **[!UICONTROL Modifier le contenu]**. [En savoir plus](../push/create-push.md)
   * **SMS** : après avoir créé et configuré votre campagne SMS, cliquez sur **[!UICONTROL Modifier le contenu]**. [En savoir plus](../mobile/create-mobile-message.md)

1. Renseignez les **[!UICONTROL Détails de base]** de votre campagne. Une fois terminé, cliquez sur **[!UICONTROL Modifier le contenu]**.

1. Personnalisez votre message selon vos besoins :
   * **Notifications push** : [en savoir plus](../push/design-push.md)
   * **SMS** : [en savoir plus](../mobile/create-mobile-message.md)

1. Accédez à l’assistant IA :
   * **Pour les notifications push** : cliquez sur le menu **[!UICONTROL Modifier le texte avec l’assistant IA]** en regard des champs **[!UICONTROL Titre]** ou **[!UICONTROL Message]**. Vous pouvez également accéder directement au menu **Assistant IA**.

     ![Écran de composition des notifications push avec bouton Modifier le texte avec l’assistant IA](assets/push-text-1.png){zoomable="yes"}

   * **Pour les SMS** : cliquez sur le menu **[!UICONTROL Modifier le texte avec l’assistant IA]** en regard de votre **[!UICONTROL Message]** ou accédez au menu **[!UICONTROL Afficher l’assistant IA]**.

     ![Éditeur de messages SMS avec le panneau Assistant IA ouvert](assets/sms-genai-1.png){zoomable="yes"}

### Générer du contenu {#mobile-generate-content}

Une fois que vous avez accédé à l’assistant IA, vous pouvez configurer les paramètres de génération afin de créer du contenu mobile correspondant à votre marque et aux objectifs de la campagne. Personnalisez les paramètres de texte, ajoutez des ressources de marque et fournissez des prompts pour guider l’IA dans la génération de variations pertinentes.

1. Sélectionnez votre **[!UICONTROL Marque]** pour vous assurer que le contenu généré par l’IA correspond aux spécifications de celle-ci. [En savoir plus](brands.md) sur les marques.

   Notez que cette fonctionnalité est disponible en version Private Beta et sera progressivement disponible pour l’ensemble de la clientèle dans les versions ultérieures.

1. Affinez le contenu en décrivant ce que vous souhaitez générer dans le champ **[!UICONTROL Prompt]**.

   Si vous avez besoin d’aide pour concevoir votre prompt, accédez à la **[!UICONTROL Bibliothèque de prompts]** qui offre un large éventail d’idées d’invites pour améliorer vos campagnes. [En savoir plus sur les bonnes pratiques relatives aux prompts](ai-assistant-prompting-guide.md)

   ![Assistant IA avec champ et options de prompt](assets/push-genai-2.png){zoomable="yes"}

1. **Pour les notifications push**, sélectionnez le champ à générer : Titre et/ou Message.

1. Adaptez votre prompt avec l’option **[!UICONTROL Paramètres de texte]** :

   * **[!UICONTROL Stratégie de communication]** : choisissez le style de communication le plus adapté au texte généré.
   * **[!UICONTROL Langues]** : sélectionnez la langue du contenu généré.
   * **[!UICONTROL Ton]** : le ton doit trouver écho auprès de votre audience. Que vous souhaitiez communiquer de façon informative, ludique ou convaincante, l’assistant IA peut adapter le message en conséquence.

     ![Panneau Paramètres de texte](assets/push-genai-4.png){zoomable="yes"}

1. Dans le menu **[!UICONTROL Contenu de référence]**, cliquez sur **[!UICONTROL Charger un fichier]** pour ajouter toute ressource de marque incluant du contenu pouvant fournir du contexte supplémentaire à l’assistant IA, ou sélectionnez-en une chargée précédemment.

   Les fichiers précédemment chargés sont disponibles dans la liste déroulante **[!UICONTROL Contenu de référence chargé]**. Activez simplement les ressources que vous souhaitez inclure dans votre génération.

1. Lorsque votre prompt est prêt, cliquez sur **[!UICONTROL Générer]**.

### Affiner et finaliser {#mobile-refine-finalize}

Après avoir généré des variations de texte pour vos messages mobiles, vous pouvez affiner les résultats pour vous assurer qu’ils répondent exactement à vos besoins. Examinez l’alignement sur la marque, ajustez le ton et le langage, puis préparez le contenu pour l’activation.

1. Après la génération, parcourez les **[!UICONTROL variations]**.

1. Cliquez sur l’icône de pourcentage pour afficher votre **[!UICONTROL score d’alignement sur la marque]** et identifier tout décalage avec votre marque.

   En savoir plus sur le [score d’alignement sur la marque](brands-score.md).

   ![Variations de texte générées avec le score d’alignement sur la marque](assets/push-genai-5.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Aperçu]** pour afficher une version en plein écran de la variation sélectionnée ou cliquez sur **[!UICONTROL Appliquer]** pour remplacer votre contenu actuel.

1. Accédez à l’option **[!UICONTROL Affiner]** dans la fenêtre **[!UICONTROL Aperçu]** pour accéder à d’autres fonctionnalités de personnalisation :

   * **[!UICONTROL Utiliser comme contenu de référence]** : la variante choisie servira de contenu de référence pour générer d’autres résultats.

   * **[!UICONTROL Reformuler]** : réécrivez le message tout en préservant sa signification. Cette option vous permet de générer une autre formulation, d’améliorer le flux ou d’ajuster les expressions sans modifier le message principal.

   * **[!UICONTROL Utiliser un langage simplifié]** : utilisez l’assistant IA pour simplifier votre langage, garantissant ainsi clarté et accessibilité pour une audience plus large.

   * **[!UICONTROL Traduire]** : simplifiez votre texte pour garantir la clarté et l’accessibilité afin de toucher une audience plus large.

   * **[!UICONTROL Changer de ton]** : ajustez le ton du message pour mieux correspondre à votre style de communication, c’est-à-dire le rendre plus convivial, professionnel, urgent ou inspirant.

   * **[!UICONTROL Modifier la stratégie de communication]** : modifiez l’approche des messages en fonction de vos objectifs, par exemple créer un sentiment d’urgence ou mettre en avant un aspect attractif et enthousiasmant.

     ![Menu Affiner](assets/push-genai-6.png){zoomable="yes"}

1. Ouvrez l’onglet **[!UICONTROL Alignement sur la marque]** pour voir comment votre contenu s’aligne sur vos [directives de marque](brands.md).

1. Cliquez sur **[!UICONTROL Sélectionner]** une fois que vous avez trouvé le contenu approprié.

1. Insérez des champs de personnalisation pour personnaliser votre contenu en fonction des données des profils. Ensuite, utilisez une méthode de simulation pour contrôler le rendu et vérifier les paramètres de personnalisation : cliquez sur **[!UICONTROL Simuler du contenu]** pour tester les variations de contenu avec des exemples de données d’entrée ou la génération automatique de l’IA, ou cliquez sur **[!UICONTROL Simuler du contenu]**, puis sélectionnez **[!UICONTROL Simuler du contenu (profils AEP)]** dans la liste déroulante pour obtenir un aperçu avec des profils de test. [En savoir plus](../content-management/preview-test.md)

Lorsque vous avez défini le contenu, l’audience et le planning, vous pouvez préparer votre campagne mobile. [En savoir plus](../campaigns/review-activate-campaign.md)
