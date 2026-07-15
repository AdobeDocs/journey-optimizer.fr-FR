---
solution: Journey Optimizer
product: journey optimizer
title: Créer du contenu dynamique
description: Découvrez comment ajouter du contenu dynamique à vos messages.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: expression, éditeur, dynamique, contenu
exl-id: 639ad7df-0d0f-4c9b-95d1-f3101267aae2
TQID: https://experienceleague.adobe.com/j9jmVxc9Pn53hghR-2sUGXjcczfQibs5XTGuD7gwiI4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
  - id: e51e8901-97d9-4f7d-a835-503025a90e32
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1262
ht-degree: 50%

---

# Créer du contenu dynamique {#dynamic-content}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment utiliser des règles conditionnelles pour ajouter du contenu dynamique à vos messages, à la fois dans les expressions de personnalisation et en tant que variantes de composant de contenu dans le Designer d’e-mail.

>[!ENDSHADEBOX]

Adobe Journey Optimizer vous permet d’utiliser des règles conditionnelles créées dans la bibliothèque pour ajouter du contenu dynamique à vos messages.

Du contenu dynamique peut être créé dans n’importe quel champ que vous pouvez personnaliser à l’aide de l’éditeur de personnalisation. Cela inclut l’objet, les liens, le contenu des notifications push ou les représentations des offres de type texte. [En savoir plus sur la personnalisation](personalize.md)

De plus, vous pouvez utiliser des règles conditionnelles dans le Concepteur d’e-mail pour créer plusieurs variantes d’un composant de contenu.

## Ajouter du contenu dynamique aux expressions {#perso-expressions}

Les étapes suivantes permettent d’ajouter du contenu dynamique aux expressions :

1. Accédez au champ dans lequel vous souhaitez ajouter du contenu dynamique, puis ouvrez l’éditeur de personnalisation.

1. Sélectionnez le menu **[!UICONTROL Conditions]** pour afficher la liste des règles conditionnelles disponibles. Cliquez sur le bouton + à côté d’une règle pour l’ajouter à l’expression actuelle.

   Vous pouvez également créer une règle en sélectionnant **[!UICONTROL Créer]**. [Découvrez comment créer des conditions.](create-conditions.md)

   ![](assets/conditions-expression.png)

1. Entre les balises `{%if}` et `{%/if}`, ajoutez le contenu que vous souhaitez afficher si la règle conditionnelle est respectée. Vous pouvez ajouter autant de règles que nécessaire pour créer plusieurs variantes d’une expression.

   Dans l’exemple ci-dessous, deux variantes ont été créées pour un contenu SMS, selon la préférence linguistique du destinataire.

   ![](assets/conditions-language-sample.png)

1. Une fois que votre contenu est prêt, vous pouvez prévisualiser différentes variantes à l’aide de l’une ou l’autre des méthodes de simulation : cliquez sur **[!UICONTROL Simuler du contenu]** pour tester les variations de contenu avec des exemples de données d’entrée ou la génération automatique de l’IA, ou cliquez sur **[!UICONTROL Simuler du contenu]**, puis sélectionnez **[!UICONTROL Simuler du contenu (profils AEP)]** dans la liste déroulante pour prévisualiser avec des profils de test. [Découvrez comment tester et prévisualiser des messages](../content-management/preview-test.md).

   ![](assets/conditions-preview.png)

>[!CAUTION]
>
>Si le rendu du concepteur d’e-mail échoue après l’ajout de blocs conditionnels, vérifiez que la syntaxe de chaque nouvelle condition est correcte et qu’il n’existe aucune instruction en double ou conflictuelle. Si les problèmes persistent,envisagez de recréer les sections problématiques dans un nouveau modèle et de tester chaque bloc conditionnel progressivement.


## Ajouter du contenu dynamique dans les e-mails {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="Contenu conditionnel"
>abstract="Utilisez des règles conditionnelles pour créer plusieurs variantes d’un composant de contenu. Si aucune des conditions n’est remplie lors de l’envoi du message, le contenu de la variante Par défaut s’affiche."

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="Contenu conditionnel"
>abstract="Utilisez une règle conditionnelle enregistrée dans la bibliothèque ou créez-en une."

Les étapes de création de variantes d’un composant de contenu dans le concepteur d’e-mails sont les suivantes :

1. Dans le [concepteur d’e-mail](../email/content-from-scratch.md), sélectionnez un composant de contenu, puis cliquez sur **[!UICONTROL Activer le contenu conditionnel]**.

   ![](assets/conditions-enable-conditional.png)

1. Le volet **[!UICONTROL Contenu conditionnel]** s’affiche à gauche. Dans ce volet, vous pouvez créer plusieurs variantes du composant de contenu sélectionné à l’aide de conditions.

   Configurez votre première variante en sélectionnant le bouton **[!UICONTROL Sélectionner la condition]**.

   ![](assets/conditions-apply.png)

1. La bibliothèque de conditions s’affiche. Sélectionnez la règle conditionnelle à associer à la variante, puis cliquez sur **[!UICONTROL Sélectionner]**. Dans cet exemple, nous allons adapter le texte du composant en fonction de la langue préférée du destinataire.

   ![](assets/conditions-select.png)

   Vous pouvez également créer une règle en cliquant sur **[!UICONTROL Créer]**. [Découvrez comment créer des conditions.](create-conditions.md)

1. La règle conditionnelle est associée à la variante. Pour une meilleure lisibilité, renommez la variante en sélectionnant l’action **[!UICONTROL Renommer]** à partir de l’icône Plus d’actions.

   ![](assets/conditions-rename.png)

1. Configurez la manière dont le composant doit s’afficher si la règle est respectée lors de l’envoi du message. Dans cet exemple, nous allons afficher le texte en français s’il s’agit de la langue préférée du destinataire.

   ![](assets/conditions-design.png)

1. Ajoutez autant de variantes que nécessaire pour le composant de contenu. Vous pouvez basculer à tout moment entre les différentes variantes pour vérifier comment le composant de contenu s’affichera en fonction des règles conditionnelles.

   >[!NOTE]
   >
   >* Si aucune des règles définies dans les variantes n’est respectée lors de l’envoi du message, le composant de contenu affiche le contenu défini dans la variable **[!UICONTROL Variante par défaut]**.
   >
   >* Le contenu conditionnel sera évalué par rapport aux règles associées dans l’ordre d’affichage des variantes. La variante par défaut est toujours affichée si aucune autre condition n’est remplie.
   >
   >* Lors de la simulation ou du rendu de BAT pour les e-mails contenant plusieurs variantes conditionnelles, Journey Optimizer peut nécessiter davantage de temps de traitement. Si vous rencontrez des délais d’expiration ou des messages d’erreur, pensez à réduire le nombre total de variantes ou à simplifier les règles conditionnelles. En savoir plus sur le test de votre contenu sur [cette page](../content-management/preview-test.md).


1. Pour supprimer une variante, cliquez sur l’icône Plus d’actions située en regard de la variante souhaitée et sélectionnez **[!UICONTROL Supprimer]**.

   ![](assets/conditions-delete.png)

## Référence rapide {#quick-reference}

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

>[!BEGINTABS]

>[!TAB Vue d’ensemble]

**TL;DR**

Cette page explique comment utiliser des règles conditionnelles pour ajouter du contenu dynamique aux messages, soit par le biais de balises d’expression dans l’éditeur de personnalisation, soit en tant que variantes de composant de contenu dans le Designer d’e-mail.

**Intentions**

* Ajouter du contenu dynamique aux expressions de personnalisation à l’aide de balises conditionnelles `{%if%}`/`{%/if%}`
* Prévisualiser plusieurs variantes de contenu dynamique à l’aide de la simulation
* Activation du contenu conditionnel sur un composant de contenu Designer d’e-mail
* Créer plusieurs variantes de composant chacune liée à une règle conditionnelle
* Gérer la variante par défaut affichée lorsqu’aucune condition n’est remplie au moment de l’envoi

>[!TAB Glossaire]

* **Contenu dynamique** : contenu du message qui varie en fonction des règles conditionnelles. Un contenu différent est affiché selon que les conditions définies sont remplies au moment de l’envoi. *(spécifique au produit)*
* **Contenu conditionnel** : une fonctionnalité de Designer d’e-mail qui applique des règles conditionnelles à un composant de contenu, ce qui crée plusieurs variantes d’affichage. *(spécifique au produit)*
* **Variante par défaut** : contenu affiché pour un composant lorsqu’aucune des règles conditionnelles définies n’est remplie lors de l’envoi du message. *(spécifique au produit)*
* **`{%if%}`/ `{%/if%}` balises** : syntaxe d’expression de l’éditeur de Personalization utilisée pour encapsuler des blocs de contenu qui s’affichent uniquement lorsqu’une règle conditionnelle est remplie.

>[!TAB  Terminologie ]

* **Nom canonique :** contenu dynamique — variantes : contenu conditionnel, contenu personnalisé
* **Synonymes :** « contenu conditionnel » (libellé de l’interface utilisateur de Designer d’e-mail) = « contenu dynamique » (terme général utilisé dans l’ensemble)
* **Ne pas confondre :** l’ajout de contenu dynamique dans les expressions (à l’aide de balises `{%if%}` dans l’éditeur de personnalisation) ≠ l’ajout de contenu dynamique dans les e-mails (création de variantes de composants dans le Designer d’e-mail - deux workflows distincts)
* **Ne pas confondre :** « Variante par défaut » (affichée lorsqu’aucune règle conditionnelle n’est remplie) ≠ une variante nommée (chacune associée à une règle conditionnelle spécifique)

>[!TAB Mécanismes de sécurisation et limitations]

* Les variantes de contenu conditionnel sont évaluées par rapport aux règles associées dans l’ordre dans lequel elles sont affichées. La variante par défaut est toujours affichée si aucune autre condition n’est remplie.
* Lors de la simulation ou du rendu de BAT pour les e-mails avec plusieurs variantes conditionnelles, Journey Optimizer peut nécessiter davantage de temps de traitement. Envisagez de réduire le nombre de variantes ou de simplifier les règles conditionnelles en cas de dépassements de délai ou d’erreurs.
* Si le rendu du Designer d’e-mail échoue après l’ajout de blocs conditionnels, vérifiez que la syntaxe de chaque condition est correcte et qu’il n’existe aucune instruction en double ou conflictuelle.

>[!TAB FAQ]

**Q : Que se passe-t-il si aucune des conditions définies n’est remplie lors de l’envoi du message ?**

Le composant de contenu affiche le contenu défini dans la Variante par défaut .

**Q : Dans quel ordre les variantes de contenu conditionnel sont-elles évaluées ?**

Les variantes sont évaluées par rapport aux règles associées dans l’ordre dans lequel elles sont affichées. La variante par défaut est toujours affichée si aucune autre condition n’est remplie.

**Q : Où le contenu dynamique peut-il être ajouté dans Journey Optimizer ?**

Dans tous les champs où la personnalisation peut être ajoutée (notamment les objets, les liens, le contenu des notifications push et les représentations d&#39;offres de type texte) via l&#39;éditeur de personnalisation et dans les composants de contenu de Designer d&#39;e-mail via des variantes conditionnelles.

**Q : Que dois-je faire si le rendu du Designer d’e-mail échoue après l’ajout de blocs conditionnels ?**

Vérifiez que la syntaxe de chaque condition est correcte et qu&#39;il n&#39;existe aucune instruction en double ou conflictuelle. Si les problèmes persistent, recréez les sections problématiques dans un nouveau modèle et testez chaque bloc conditionnel de manière incrémentielle.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: e6005d80 -->
