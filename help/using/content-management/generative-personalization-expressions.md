---
solution: Journey Optimizer
product: journey optimizer
title: Assistant AI pour les expressions Personalization
description: Découvrez comment utiliser l’assistant AI dans Journey Optimizer pour générer des expressions de personnalisation à partir du langage naturel, à partir de l’éditeur de Personalization ou en ligne dans le Designer d’e-mail.
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Intermediate
mini-toc-levels: 1
source-git-commit: 8a905fd7e51c2dac60f4edccb9e9dd790a0dd424
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 4%

---

# Assistant IA pour les expressions de personnalisation{#generative-personalization-expressions}

>[!IMPORTANT]
>
>Avant de commencer à utiliser cette fonctionnalité, lisez la section connexe [Mécanismes de sécurisation et limitations](gs-generative.md#generative-guardrails).
></br>
>
>Vous devez accepter un [contrat d’utilisation](https://www.adobe.com/fr/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html) avant de pouvoir utiliser l’Assistant IA dans Journey Optimizer. Pour plus d’informations, contactez votre représentant ou représentante Adobe.

## Vue d’ensemble {#where-available}

L’[!UICONTROL assistant AI] vous permet de générer une nouvelle personnalisation à partir d’un langage clair, d’expliquer le rôle des expressions existantes et de résoudre les problèmes liés au code sélectionné, de sorte que vous passiez moins de temps sur la syntaxe et la découverte manuelle des champs. Vous pouvez également effectuer une itération sur une sélection ou demander d’autres modifications dans la conversation. Il est disponible à partir de deux points d’entrée :

* **[!UICONTROL Éditeur Personalization]** — là où l&#39;éditeur est disponible (objet, corps et autres champs qui l&#39;ouvrent). Pour savoir où et comment ouvrir l’éditeur, voir [&#x200B; Ajouter une personnalisation &#x200B;](../personalization/personalization-build-expressions.md#where).
* **Modification de texte en ligne dans Email Designer** : directement à partir de la fenêtre contextuelle de modification en ligne lors de la modification d’un composant de texte. Voir [Générer à partir du Designer d’e-mail](#generate-email-designer).

Pour en savoir plus sur la configuration et les langages de l’assistant AI, voir [Prise en main de l’assistant AI](gs-generative.md). Pour connaître les concepts de personnalisation, voir [Prise en main de la personnalisation](../personalization/personalize.md). Pour obtenir des idées rapides, voir [Bonnes pratiques d’invite d’IA](ai-assistant-prompting-guide.md).

Selon le contexte de votre campagne ou de votre parcours, l’assistant peut utiliser les données et construire les éléments déjà exposés par [!UICONTROL l’éditeur de Personalization] par exemple les attributs de profil, l’appartenance à un segment, les fonctions d’assistance et les sources de personnalisation associées.

>[!NOTE]
>
>L’assistant conserve le contexte de vos invites uniquement pendant que [!UICONTROL l’assistant AI] reste ouvert dans cette session. La fermeture de l&#39;assistant ou de l&#39;éditeur efface la conversation ; la prochaine fois que vous ouvrez l&#39;assistant, vous démarrez une nouvelle conversation.

## Générer des expressions de personnalisation {#generate}

Ces étapes couvrent la génération à partir de zéro d’expressions de personnalisation. Pour utiliser du code déjà présent dans l’éditeur, voir [Modifier, corriger ou expliquer le code existant](#edit-existing).

1. Dans votre message ou contenu, ouvrez l&#39;éditeur Personalization **&#x200B;**.

1. Placez le curseur dans l’éditeur à l’endroit où vous souhaitez insérer le code de personnalisation généré, puis cliquez sur le bouton **[!UICONTROL Assistant IA]**.

   ![](assets/ai-perso-access.png)

1. Dans le champ de texte, décrivez l’expression de personnalisation de votre choix en langage clair (par exemple, les attributs de profil, les segments ou la logique dont vous avez besoin), puis cliquez sur **[!UICONTROL Générer]**.

   Vous pouvez également utiliser des invites prêtes à l&#39;emploi de la section **[!UICONTROL Invites rapides]** telles qu&#39;un message de salutations personnalisé, la génération d&#39;un code promotion, etc.

   ![](assets/ai-perso-generate.png)

   >[!NOTE]
   >
   >Toute invite ou question non liée renvoie une erreur hors de portée. Ajustez votre invite et posez une question pertinente sur la personnalisation dont vous avez besoin.

1. Vous pouvez continuer à discuter avec l&#39;assistant dans une conversation à plusieurs tours : cela conserve le contexte de vos invites afin que vous puissiez affiner la même expression étape par étape. Pour recommencer, cliquez sur le bouton **[!UICONTROL Nouvelle session]**.

   ![](assets/ai-perso-question.png)

1. Après avoir généré une expression, cliquez sur **[!UICONTROL Afficher les aperçus pour les profils types]** pour voir comment l’expression est évaluée avec des données d’exemple et pour afficher la payload associée au format JSON. Pour ce contrôle, l’assistant génère un ensemble limité de profils types synthétiques ; ils ne sont ni enregistrés ni stockés dans votre organisation.

   Si vous avez besoin de profils types personnalisés ou supplémentaires, décrivez ce dont vous avez besoin lors de la discussion avec l’assistant et incluez le mot-clé **preview** dans votre invite afin qu’il puisse générer les profils de prévisualisation appropriés pour votre vérification.

   ![](assets/ai-perso-preview-button.png)

   +++Exemple de prévisualisation

   ![](assets/ai-perso-preview.png)

   >[!NOTE]
   >
   >D’autres aperçus servent à la vérification par points. L’assistant est réglé de manière à générer environ un à cinq profils. Si vous demandez un nombre très élevé, la requête peut échouer.

   +++

   >[!NOTE]
   >
   >Ce contrôle permet de vérifier rapidement votre code de personnalisation dans l’éditeur, et non de prévisualiser entièrement le contenu du message. Pour une validation complète de l’expérience, utilisez votre flux de simulation habituel. [Découvrir comment prévisualiser et tester votre contenu](../content-management/preview-test.md)

1. Pour implémenter la sortie dans votre expression de personnalisation, cliquez sur **[!UICONTROL Appliquer]**. La sortie de l’assistant est insérée à l’emplacement du curseur dans l’éditeur de personnalisation. Pour remplacer le code qui est déjà là, sélectionnez d’abord ce code dans l’éditeur, puis utilisez **[!UICONTROL Modifier avec l’assistant AI]** (voir [Modifier, corriger ou expliquer le code existant](#edit-existing)).

   Vous pouvez également copier la sortie et la coller où vous en avez besoin à l’aide de l’icône ![Copier](../orchestrated/assets/do-not-localize/activity-copy.svg) .

## Modifier, corriger ou expliquer le code existant {#edit-existing}

Vous pouvez sélectionner une expression de personnalisation existante et utiliser l’assistant AI pour résoudre les problèmes de personnalisation, expliquer le fonctionnement du code ou demander d’autres modifications.

1. Sélectionnez le code de personnalisation existant dans l’éditeur.

1. Cliquez avec le bouton droit sur la sélection et choisissez **[!UICONTROL Modifier avec l’assistant AI]** afin que l’assistant utilise votre sélection comme contexte.

   ![](assets/ai-perso-right-click.png)

1. **[!UICONTROL Assistant AI]** s’ouvre. Dans **[!UICONTROL Commandes rapides]**, cliquez sur **[!UICONTROL Expliquer]** ou **[!UICONTROL Corriger]**, ou utilisez le champ de texte pour demander d’autres modifications et démarrer une conversation.

   ![](assets/ai-perso-edit.png)

1. Lorsque vous utilisez **[!UICONTROL Correctif]**, cliquez sur **[!UICONTROL Afficher les détails du correctif]** dans la discussion pour afficher une explication du correctif et une liste ligne par ligne avant et après l’aperçu.

   ![](assets/ai-perso-fix.png)

1. Comme lorsque vous générez une expression de personnalisation, cliquez sur **[!UICONTROL Appliquer]** pour implémenter la sortie de l’assistant. Il remplace le code que vous avez sélectionné dans l’éditeur de personnalisation. Par exemple, si vous avez demandé une explication du code, l’application ajoutera des commentaires dans l’expression qui décrivent sa fonction.

## Générer à partir du Designer Email {#generate-email-designer}

[!UICONTROL Assistant AI pour les expressions de personnalisation] est également disponible directement à partir de l’expérience de modification en ligne dans le Designer d’e-mail, sans ouvrir l’[!UICONTROL Éditeur Personalization complet]. L’expression générée est insérée à l’emplacement du curseur dans le composant de texte.

1. Dans le Designer d’e-mail, sélectionnez un composant de texte et commencez à le modifier sur la ligne.

1. Ouvrez la fenêtre contextuelle de personnalisation intégrée de l’une des deux façons suivantes :

   * Saisissez `{{` à l’emplacement où vous souhaitez insérer l’expression ; la fenêtre contextuelle s’ouvre automatiquement.
   * Cliquez sur **[!UICONTROL Utiliser l’IA pour générer]** dans la fenêtre contextuelle de modification en ligne si elle est déjà ouverte.

   ![](assets/ai-perso-email-entry.png)

1. Dans le champ de texte, décrivez l’expression de personnalisation de votre choix en langage clair, puis cliquez sur **[!UICONTROL Générer]**.

1. Consultez le résultat dans l’onglet **[!UICONTROL Expression]** pour voir l’expression générée.

   Passez à l’onglet **[!UICONTROL Aperçu]** pour voir comment l’expression est évaluée à l’aide des exemples de valeurs de profil, afin que vous puissiez vérifier la sortie avant de l’insérer.

   ![](assets/ai-perso-email-result.png)

1. Cliquez sur **[!UICONTROL Insérer]** pour appliquer l’expression à la position du curseur dans le composant de texte. Utilisez **[!UICONTROL Régénérer]** pour générer une nouvelle suggestion ou **[!UICONTROL Réinitialiser]** pour recommencer.

>[!NOTE]
>
>La session [!UICONTROL Assistant AI pour les expressions de personnalisation] dans la fenêtre contextuelle de Designer d’e-mail intégrée est indépendante des sessions dans l’[!UICONTROL Éditeur Personalization]. La fermeture de la fenêtre contextuelle efface la conversation.
