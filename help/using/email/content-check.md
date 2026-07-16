---
solution: Journey Optimizer
product: journey optimizer
title: Vérifications de contenu dans le Designer Email
description: Découvrez comment utiliser les vérifications de contenu dans le Designer d’e-mail pour détecter les problèmes HTML et CSS avant d’envoyer vos e-mails dans Journey Optimizer.
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: e-mail, vérification de contenu, HTML, CSS, validation, rendu, qualité
source-git-commit: 74bd6eeb380f433f08002024aba873906213aad4
workflow-type: tm+mt
source-wordcount: '1310'
ht-degree: 6%

---


# Vérification du contenu dans le Concepteur d’e-mail {#content-check}

>[!CONTEXTUALHELP]
>id="ajo_email_content_check"
>title="Valider le contenu de votre e-mail"
>abstract="Les vérifications de contenu détectent automatiquement les problèmes HTML et CSS dans votre e-mail avant l’envoi. Elles signalent les balises non prises en charge, les éléments div vides et les limites de taille qui peuvent interrompre le rendu dans Gmail ou Microsoft Outlook. Les problèmes apparaissent sous forme d’erreurs, d’avertissements ou de notifications d’informations, avec des détails contextuels et des correctifs en un clic, le cas échéant."

[!DNL Journey Optimizer] comprend une validation technique automatisée directement dans le Designer d’e-mail, ce qui vous permet de détecter les problèmes HTML et CSS avant l’envoi.

Les résultats sont affichés sous forme d’erreurs, d’avertissements ou d’informations dans le panneau de création, avec des détails contextuels et des correctifs en un clic le cas échéant, afin que les problèmes puissent être résolus sans quitter le Designer d’e-mail.

## Vérifications d’accès au contenu {#access-content-checks}

Les vérifications de contenu sont toujours disponibles dans la Designer Email. Pour les afficher, cliquez sur l’icône Problèmes dans le rail de droite pour ouvrir le volet **[!UICONTROL Vérification de contenu]** — tous les problèmes détectés y sont répertoriés.

![Volet de vérification du contenu du Designer Email présentant des problèmes](assets/content-check.png)

>[!NOTE]
>
>Les vérifications sont automatiquement exécutées par rapport à l’état actuel de votre e-mail et après chaque modification. [En savoir plus](#recalculation)

Les contrôles sont affichés avec trois niveaux de gravité :

| Gravité | Couleur | Description |
|---|---|---|
| **Erreur** | Rouge | Un problème critique qui provoquera des échecs de diffusion ou de rendu. Résoudre avant envoi. |
| **Avertissement** | Orange | Un problème potentiel qui peut affecter le rendu dans des clients de messagerie spécifiques. Recommandé pour examen et résolution. |
| **Info** | Bleu | Avis d’information sur une condition qui ne bloque pas l’envoi, mais qui peut affecter la maintenabilité à long terme de votre contenu. |

Lorsqu’aucun problème n’est détecté, le volet affiche **Aucun problème détecté** et l’icône correspondante est verte.

![Volet de vérification du contenu du Designer d’e-mail sans problème](assets/content-check-no-issues.png)

Selon le problème, vous pouvez afficher plus de contexte, appliquer un correctif en un clic ou enregistrer votre e-mail pour actualiser un résultat de vérification.

* Pour certains problèmes détectés, vous pouvez cliquer sur le bouton **[!UICONTROL Afficher les détails]** pour afficher plus de contexte. Cliquez sur **[!UICONTROL Masquer les détails]** pour réduire l’image.
  ![Volet de vérification du contenu dans le Designer d’e-mail avec des détails](assets/content-check-details.png){width="80%"}
* De même, vous pouvez cliquer sur le bouton **[!UICONTROL Afficher le correctif]** et appliquer un correctif en un clic, le cas échéant. Si le correctif ne peut pas être appliqué automatiquement, un message s’affiche et vous devez résoudre le problème manuellement.
  ![Volet de vérification Contenu du Designer Email avec le bouton Appliquer le correctif](assets/content-check-fix.png){width="80%"}

### Recalcul des chèques {#recalculation}

La plupart des contrôles, tels que les éléments HTML non pris en charge, les balises div vides et la taille d’HTML, sont recalculés chaque fois que vous modifiez votre e-mail. Ils reflètent donc toujours votre contenu actuel.

D’autres contrôles, tels que la taille de la feuille de style CSS, sont calculés à partir du contenu sérialisé (la version de votre e-mail telle qu’elle est chargée ou enregistrée), et non à partir de l’état de modification en direct dans le Designer d’e-mail. Dans ce cas, le contenu enregistré peut différer légèrement de ce que vous voyez lors de la modification. Si vous apportez des modifications sans enregistrer, un libellé **[!UICONTROL Vérification obsolète]** apparaît pour indiquer que le résultat peut ne plus être précis. Enregistrez votre e-mail pour actualiser le calcul.

![Volet de vérification Contenu du Designer Email avec le libellé de vérification Obsolète](assets/content-check-stale.png){width="100%"}

## Correction des problèmes détectés {#fix-issues}

Les tableaux ci-dessous répertorient tous les messages possibles et l’action recommandée pour chacun d’eux. Développez la catégorie correspondant au message affiché dans le volet **[!UICONTROL Vérification de contenu]**.

+++ Éléments HTML non pris en charge

| Message | Gravité | Que faire |
|---|---|---|
| Votre contenu contient une balise `<script>`, qui n’est prise en charge dans aucun système de messagerie. Supprimez-la pour éviter des problèmes de diffusion et de rendu. | Erreur | Recherchez et supprimez toutes les balises `<script>` de votre contenu HTML. |
| Votre contenu contient une balise `<base>`, ce qui peut entraîner des problèmes de résolution de liens et de ressources dans le Designer d’e-mail. Pour corriger ce problème, vous devez le supprimer. | Erreur | Supprimez la balise `<base>` de votre HTML. |
| Votre contenu contient une balise meta HTML avec renouvellement, qui n’est pas prise en charge dans le Designer de messagerie. Supprimez-le pour éviter tout comportement inattendu. | Avertissement | Supprimez la balise de méta-actualisation de votre HTML. |
| Votre contenu contient des balises div vides, ce qui peut entraîner des problèmes de disposition dans Microsoft Outlook (MSO). Pour corriger ce problème, supprimez les balises div vides et utilisez plutôt l’espacement des éléments frères. | Avertissement | Supprimez les éléments de `<div>` vides et ajustez la marge intérieure ou la marge sur les éléments environnants pour conserver l’espacement. |

+++

+++ Problèmes CSS

| Message | Gravité | Que faire |
|---|---|---|
| La taille totale de CSS dépasse la limite de 16 Ko de Gmail et provoquera des problèmes de rendu dans Gmail. | Erreur | Utilisez **[!UICONTROL Appliquer le correctif]** pour supprimer automatiquement les règles CSS inutilisées ou simplifier manuellement vos styles. |
| La taille totale de CSS est proche de la limite de 16 Ko de Gmail et peut entraîner des problèmes de rendu si d’autres fichiers CSS sont ajoutés. | Avertissement | Utilisez **[!UICONTROL Appliquer le correctif]** pour supprimer les règles CSS inutilisées ou réduire les styles avant d’ajouter plus de contenu. |
| La taille totale de CSS de ce fragment dépasse 3 Ko. Si vous combinez cela avec d’autres fragments, le CSS total de l’e-mail pourrait dépasser la limite de 16 Ko de Gmail et provoquer des problèmes de rendu. | Avertissement | Simplifiez le CSS dans ce fragment pour conserver le CSS de l’e-mail combiné inférieur à 16 Ko. |
| Le contenu contient des règles CSS inutilisées. Cela peut entraîner des problèmes de rendu dans Gmail. | Avertissement | Utilisez **[!UICONTROL Appliquer le correctif]** pour supprimer automatiquement les règles CSS qui référencent des éléments qui ne sont plus présents dans l’e-mail. |

<!--
| Message | Severity | What to do |
|---|---|---|
| Your content has modifications to the system-generated default CSS. These changes may be overridden by future Email Designer updates. To preserve your styles, add them using the Custom CSS feature instead. | Info | Move your custom styles to [Custom CSS](custom-css.md) to ensure they are preserved across Email Designer updates. |
-->

+++

+++ Taille d’HTML

| Message | Gravité | Que faire |
|---|---|---|
| La taille estimée d’HTML dépasse la limite de 100 Ko de Gmail et provoquera des problèmes de rendu dans Gmail. La taille réelle d’HTML peut différer au moment de l’envoi. | Erreur | Réduire le contenu des e-mails : supprimez les éléments inutiles, simplifiez la structure ou divisez le contenu en plusieurs envois. |
| La taille estimée d’HTML est proche de la limite de 100 Ko de Gmail et peut entraîner des problèmes de rendu si d’autres HTML sont ajoutées. La taille réelle d’HTML peut différer au moment de l’envoi. | Avertissement | Simplifiez le contenu avant d’en ajouter d’autres. Les e-mails dépassant la limite de Gmail seront tronqués pour les destinataires. |
| La taille estimée d’HTML pour ce fragment dépasse 20 Ko. La combinaison de ce paramètre avec d’autres fragments peut entraîner un dépassement de la limite de 100 Ko du nombre total d’e-mails HTML dans Gmail et des problèmes de rendu. La taille réelle d’HTML peut différer au moment de l’envoi. | Avertissement | Réduisez la taille d’HTML dans ce fragment pour que la taille de l’e-mail total reste inférieure à la limite de 100 Ko de Gmail. |

+++

## À propos d’HTML et de la taille CSS {#size-estimation}

Les valeurs de taille HTML et CSS affichées dans le Designer d’e-mail sont des **estimations calculées au moment de la création**. Ils reflètent la payload complète générée telle qu’elle existe dans l’éditeur à ce moment-là et incluent les éléments suivants :

* **Structure HTML** - tous les balises, balises, wrappers de disposition et styles intégrés
* **CSS intégré** - Le Designer d’e-mail intègre les styles avant le calcul de la taille, qui est standard pour les clients de messagerie, mais qui gonfle le chiffre brut par rapport à une feuille de style externe
* **Contenu texte** - tous les jetons de copie et de personnalisation, comptabilisés à leur longueur d’espace réservé (pas leur valeur résolue)
* **Fragments** - tous les fragments référencés sont développés en ligne, de sorte que chaque fragment contribue à son poids HTML/CSS total
* **Blocs conditionnels (if-else)** - **toutes les branches** sont inclus dans l’estimation de taille au moment de la création, car les conditions ne sont pas évaluées avant l’heure d’envoi
* **Images** - seule la référence de l’image (URL src) est comptabilisée, et non les données d’image binaires elles-mêmes

### Pourquoi l’estimation peut différer de la taille diffusée {#size-estimate-difference}

La taille affichée est une estimation de la limite supérieure dans le pire des cas, et non l’e-mail exact qu’un destinataire recevra. Il peut différer pour les raisons suivantes :

* **Contenu conditionnel** : à l’envoi, seule la branche correspondant au profil du destinataire est rendue. Un modèle affichant 120 Ko dans l’éditeur peut générer un e-mail de 60 Ko pour la plupart des destinataires.
* **Jetons Personalization** : les jetons d’espace réservé sont comptabilisés à leur longueur de jeton brute. Les valeurs résolues sont généralement plus courtes.
* **Optimisation de la taille d’HTML** : si l’option **[!UICONTROL Optimiser la taille d’HTML]** est activée, les espaces, les commentaires et les caractères redondants sont supprimés au moment de l’envoi, ce qui réduit la payload finale. [En savoir plus](create-email.md#optimize-html-size)

### Ce que les avertissements de taille signifient pour les auteurs {#size-warnings}

Les avertissements de taille (par exemple, HTML dépassant 100 Ko) sont des **signaux proactifs** qui vous aident à optimiser votre e-mail avant l’envoi. Il ne s’agit pas de blocs durs et ils ne reflètent pas la taille exacte que les destinataires verront. Ils existent pour aider à éviter :

* E-mails coupés par Gmail, qui clipe les messages à environ 102 Ko d’HTML
* Rendu lent sur les appareils mobiles ou sur les connexions à faible bande passante
