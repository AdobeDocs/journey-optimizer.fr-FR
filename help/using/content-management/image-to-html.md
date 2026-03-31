---
solution: Journey Optimizer
product: journey optimizer
title: Convertir des images en modèles de contenu d’e-mail
description: Découvrez comment utiliser le convertisseur Image vers HTML optimisé par l’IA pour convertir des conceptions d’image en modèles de contenu d’e-mail modifiables
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
keywords: e-mail, modèle, image, HTML, IA, conception, convertisseur
exl-id: d13467b7-2f3c-4707-a7e0-9b46cb6cafb1
source-git-commit: 8c6de43fd60849d1e236183a3c8a81ce20a227ca
workflow-type: tm+mt
source-wordcount: '2043'
ht-degree: 19%

---

# Convertir des images en modèles de contenu d’e-mail {#image-to-html}

[!DNL Journey Optimizer] vous permet d’accélérer considérablement la création d’e-mails en convertissant des conceptions d’image statiques en modèles de contenu d’e-mail entièrement personnalisables et modulaires.

>[!AVAILABILITY]
>
>Pour utiliser cette fonctionnalité, votre entreprise doit avoir signé l’addendum [!DNL Generative AI] avec Adobe. En cas de doute, contactez votre représentant Adobe.
>
>Cette fonctionnalité est disponible uniquement pour le canal E-mail .

Grâce à la technologie d’IA générative, un outil intégré analyse la mise en page, la typographie, les couleurs et les éléments visuels de votre image et génère un contenu HTML propre et modulaire qui conserve la fidélité de la conception tout en garantissant une modifiabilité totale avec le [Designer d’e-mail](../email/get-started-email-design.md).

Cette fonctionnalité sans code permet aux marketeurs de transformer les ressources visuelles des concepteurs graphiques ou des outils de conception en modèles d’e-mail réactifs et modifiables qui peuvent être enregistrés et réutilisés dans plusieurs parcours et campagnes, sans avoir à recourir à une expertise technique.

>[!IMPORTANT]
>
>Avant de commencer à utiliser cette fonctionnalité, lisez les [mécanismes de sécurisation et recommandations](#limitations) associés.

Les principaux avantages sont les suivants :

* **Plus rapide qu’un codage manuel** - Le convertisseur transforme les images en contenu modifiable en quelques minutes, ce qui vous permet d’ignorer le processus manuel de transformation de la maquette en HTML, qui prend beaucoup de temps.
* **Aucune compétence technique requise** - Les professionnels du marketing peuvent produire et ajuster des modèles sans assistance en matière de conception ou de développement.
* **Réutilisable dans toutes les campagnes** - Enregistrez les modèles dans votre bibliothèque et utilisez-les dans n’importe quel parcours ou campagne.
* **Reste fidèle à la conception** - La sortie correspond à votre disposition et à votre style tout en étant entièrement compatible avec le Designer d’e-mail.

<!--* **Design fidelity**: Maintain visual consistency with your original design while creating fully editable content
* **Email compatibility**: Generate HTML that works seamlessly with the Email Designer and across email clients-->

+++ Cas d’utilisation courants

Le convertisseur d’images en HTML est idéal pour :

* **Migration de plateforme** : vous effectuez une migration depuis une autre plateforme de marketing par e-mail ? Convertissez vos conceptions d’e-mail existantes en modèles HTML prêts pour la [!DNL Journey Optimizer] sans avoir à reconstruire à partir de zéro.
* **Conversion des maquettes de conception** : transformez les maquettes de conception d’outils tels que Photoshop, Figma ou d’autres logiciels de conception en modèles d’e-mail fonctionnels.
* **Création rapide de modèles** : générez rapidement des modèles d’e-mail pour les campagnes sensibles au facteur temps, sans attendre les ressources de développement.
* **Création de bibliothèques de modèles** : créez une bibliothèque complète de modèles cohérents avec la marque que les membres de l’équipe non techniques peuvent personnaliser et déployer.
* **Réduction des dépendances techniques** : permettez aux spécialistes marketing de créer et d’itérer indépendamment sur des modèles d’e-mail, ce qui accélère l’exécution des campagnes.

+++

## Accéder à l’image vers le convertisseur HTML {#access-image-to-html}

**Addendum avec Adobe**

Pour accéder à cette fonctionnalité, votre entreprise doit avoir signé l’addendum [!DNL Generative AI] avec Adobe. En cas de doute, contactez votre représentant Adobe.

**Autorisations**

* Pour accéder aux modèles et en créer, votre rôle doit inclure l’autorisation **[!UICONTROL Gérer les modèles de contenu]** (sous la ressource **Gestion de contenu**). [En savoir plus sur les autorisations](../administration/permissions.md)

* Pour utiliser l’image dans le convertisseur HTML, l’autorisation **Générer le contenu** doit vous avoir été accordée. Découvrez comment attribuer des autorisations liées à la génération de contenu dans [cette section](../content-management/gs-generative.md#generative-access).

**Accord**

Avant de pouvoir utiliser cette fonctionnalité, vous devez accepter un contrat d’utilisation qui s’affiche la première fois que vous utilisez l’IA générative dans [!DNL Journey Optimizer]. Pour plus d’informations, consultez les [instructions d’utilisation de Adobe Experience Cloud Generative AI](https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

## Mécanismes de sécurisation et recommandations {#limitations}

Gardez à l’esprit les limites et recommandations suivantes lors de la conversion d’images en modèles de contenu d’e-mail.

**Pertinence**

* **Interprétation de l’IA** : l’IA génère du contenu HTML statique en fonction de l’interprétation visuelle de votre image. Il fournit un point de départ solide pour la création d’e-mails, mais doit être examiné et affiné à l’aide de la Designer d’e-mail afin de s’assurer qu’elle répond exactement à vos besoins. Vous devez ajouter manuellement la personnalisation, le contenu dynamique et le suivi après la conversion, si nécessaire.

* **Précision du texte** : bien que l’IA tente de reconnaître et de reproduire le texte avec précision, vérifiez toujours le contenu du texte et apportez les corrections nécessaires. Vérifiez les [instructions d’utilisation d’Adobe Generative AI](https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

**Sélection d’images**

* **PII et données sensibles** : veillez à sélectionner une image qui ne contient aucune information d’identification personnelle (PII) ou d’autres données sensibles.

* **Taille de l’image** : vous ne pouvez pas charger d’images dont la taille est supérieure à 10 Mo.

* **Images de haute qualité** : pour de meilleurs résultats, utilisez des images claires et de haute qualité : images nettes, texte lisible et éléments de disposition bien définis. Les images floues, sombres ou encombrées réduisent la qualité de conversion. La largeur des images doit idéalement être comprise entre 600 et 800 pixels pour correspondre aux dimensions d’e-mail standard.

* **Dispositions simples** : les conceptions très complexes avec des superpositions complexes, des formes inhabituelles ou des éléments non standard peuvent ne pas se convertir parfaitement. Des conceptions plus simples donnent généralement de meilleurs résultats.

**Traitement**

* **Actualiser la page** : le résultat ne s’affiche pas automatiquement tant que vous n’avez pas actualisé la page.

* **Temps de traitement** : la conversion se termine souvent en **environ 5 minutes**, selon la complexité et la taille de l’image. Les images très volumineuses ou complexes peuvent parfois prendre jusqu’à 10 minutes ; attendez puis actualisez pour afficher le résultat.

<!--
* **Background processing**: The AI processing happens in the background, so you can work on other tasks without keeping the screen open. The template is automatically saved as a draft once the conversion is complete.

**Feedback is welcome!** Use the dedicated section to share your thoughts and suggestions with Adobe to help us improve the feature.-->

## Conversion d’une image en modèle HTML {#convert-image}

Pour convertir une conception d’image en modèle de contenu d’e-mail entièrement personnalisable, procédez comme suit.

1. Assurez-vous de disposer d’un fichier image au format JPEG ou PNG contenant votre conception d’e-mail.

   >[!IMPORTANT]
   >
   >La taille de l’image ne peut pas dépasser **10 Mo**. Pour de meilleurs résultats, utilisez une image **claire et de haute qualité** avec des visuels nets, du texte lisible et des éléments de disposition bien définis.

1. Accédez à la liste des modèles de contenu en sélectionnant **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Modèles de contenu]** dans le menu de gauche.

1. Cliquez sur **[!UICONTROL Créer un modèle]**.

1. Renseignez les détails du modèle et sélectionnez **[!UICONTROL E-mail]** comme canal, puis cliquez sur **[!UICONTROL Créer]**.

1. Dans la section **[!UICONTROL Convertir l’image en modèle]**, procédez comme suit :

   * (Facultatif) Si des thèmes de marque sont définis dans Journey Optimizer pour votre organisation, vous pouvez sélectionner un thème comme entrée afin que l’HTML générée soit mise en forme en fonction de vos paramètres de thème de marque. [En savoir plus sur les thèmes](../email/apply-email-themes.md)

     Les styles tels que la couleur d’arrière-plan, la couleur du bouton, les polices, l’espacement des lignes, les marges et la marge intérieure seront appliqués au modèle généré, ce qui réduit le travail de conception supplémentaire et permet de produire un modèle prêt à l’emploi avec un minimum de modifications.

   * Pour pouvoir charger une image, assurez-vous qu’elle ne contient pas d’informations d’identification personnelle (PII) ou d’autres données sensibles. Cochez l’option correspondante pour confirmer que vous avez révisé le fichier.

   * Cliquez sur le bouton **[!UICONTROL Télécharger l’image]** pour sélectionner votre fichier image.

     ![Éditeur de modèles de contenu d’e-mail Journey Optimizer avec la section Convertir l’image en modèle](../email/assets/email_designer_convert_img.png){width=80%}

     >[!CAUTION]
     >
     >Lorsque vous chargez une image pour la conversion, tout le contenu actuellement ajouté dans l’e-mail sera supprimé et remplacé par le modèle généré.

1. Si c’est la première fois que vous utilisez Generative AI dans [!DNL Journey Optimizer], il vous sera demandé d’accepter le contrat d’utilisation. Pour en savoir plus, consultez les [instructions d’utilisation d’Adobe Generative AI](https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

   ![Boîte de dialogue du contrat d’utilisation Generative AI dans Journey Optimizer](../email/assets/email_designer_convert_agreement.png){width=50%}

   Cliquez sur **[!UICONTROL Accepter]** pour continuer.

1. Après avoir sélectionné l’image, cliquez sur **[!UICONTROL Ouvrir]** pour lancer le processus de conversion optimisé par l’IA, qui se termine souvent en **environ 5 minutes**, selon la complexité et la taille de votre conception d’image.

   >[!NOTE]
   >
   >Les images très volumineuses peuvent prendre jusqu’à 10 minutes dans certains cas. Vous pouvez quitter cet écran et travailler sur d’autres tâches pendant que la conversion est en cours.

1. **Actualisez la page** pour afficher la sortie. Une fois la conversion terminée, le contenu généré s’affiche et est automatiquement enregistré en tant que brouillon.

   >[!IMPORTANT]
   >
   >Le résultat ne s’affiche pas automatiquement tant que vous n’avez pas actualisé.

   ![Modèle de contenu d’e-mail affichant le brouillon généré à partir de la conversion d’image](../email/assets/email_designer_converted_img.png){width=90%}

1. Utilisez la section **[!UICONTROL Image vers commentaires du convertisseur de modèles]** pour partager vos idées et suggestions avec Adobe afin de nous aider à améliorer la fonctionnalité.
   ![Section Commentaires dans Journey Optimizer avec une zone de texte pour partager vos pensées et suggestions](../email/assets/email_designer_converter_feedback.png){width=70%}

1. Cliquez sur **[!UICONTROL Modifier le corps de l’e-mail]**. Le modèle converti s’ouvre dans le Designer d’e-mail[ avec des fonctionnalités de modification complètes. ](../email/get-started-email-design.md) Vous pouvez maintenant :

   * Vérifier, modifier le contenu textuel et appliquer une personnalisation
   * modifier des images et ajouter des liens ;
   * ajuster les couleurs, les polices et le style ;
   * ajouter, supprimer ou réorganiser des composants de contenu.
   * tirer profit de toutes les fonctionnalités du concepteur d’e-mail comme pour tout autre modèle.

   Designer d’e-mail dans Journey Optimizer affichant le modèle converti en tant que composants de contenu modulaires à modifier![](../email/assets/email_designer_html_components.png)

   Effectuez les ajustements nécessaires pour affiner le modèle et respecter les directives de votre marque.

1. Une fois satisfait de votre modèle, cliquez sur **[!UICONTROL Enregistrer]**.

Votre modèle est maintenant disponible dans la bibliothèque de modèles de contenu et peut être utilisé lors de la création d’e-mails dans des parcours ou des campagnes. [Découvrez comment utiliser les modèles de contenu.](../email/use-email-templates.md)

## Bonnes pratiques {#best-practices}

Pour obtenir des résultats optimaux lors de la conversion d’images en modèles de contenu d’e-mail, suivez ces recommandations.

+++Avant de commencer

* **Enregistrer le contenu existant** : la conversion d’une image remplace tout le contenu existant dans votre modèle d’e-mail. Enregistrez toujours votre travail actuel avant d’utiliser cette fonctionnalité.
* **Planifier votre workflow** : utilisez cette fonctionnalité au début de votre processus de création d’e-mail ou assurez-vous que vous êtes prêt à remplacer tout le contenu actuel.

+++

+++Préparation des images

* **Résolution** : utilisez des images haute résolution pour une meilleure reconnaissance du texte et une meilleure détection des éléments.
* **Clarté** : utilisez une image claire : le texte doit être facile à lire et les éléments visuels bien définis. Évitez les fichiers sources flous, à faible contraste ou bruyants.
* **Largeur** : concevez des images aux largeurs d’e-mail standard (600 à 800 px) pour répondre aux exigences standard des clients de messagerie.
* **Format de fichier** : utilisez le format JPEG ou PNG pour éviter les images compressées ou de faible qualité.
* **Conception complète** : incluez la conception complète d’e-mail dans une seule image, de l’en-tête au pied de page.

+++

+++Considérations relatives à la conception

* **Mises en page simples** : les mises en page plus simples et bien structurées se convertissent plus précisément que les conceptions très complexes.
* **Éléments standard** : utilisez des modèles de conception d’e-mail courants (en-tête, sections de corps, CTA, pied de page).
* **Lisibilité du texte** : assurez-vous que le contraste entre le texte et l’arrière-plan est suffisant.
* **Polices sécurisées pour le web** : les conceptions qui utilisent des polices sécurisées pour le web courantes auront une meilleure fidélité.
* **Évitez le chevauchement des éléments** : conservez des éléments de conception clairement séparés pour une meilleure reconnaissance de la structure.

+++

+++Après la conversion

* **Actualiser pour afficher les résultats** : après environ 5 minutes (ou jusqu’à 10 minutes pour les images très volumineuses), actualisez la page pour que la conversion terminée s’affiche.
* **Vérifiez votre brouillon** : une fois la conversion terminée, votre modèle est automatiquement enregistré en tant que brouillon. Prenez le temps d’examiner attentivement le contenu généré pour en vérifier la précision.
* **Tester minutieusement** : tester l’e-mail sur différents clients de messagerie et appareils. [Découvrez comment prévisualiser et tester du contenu](preview-test.md).
* **Affiner manuellement** : effectuez les ajustements nécessaires en utilisant les fonctionnalités d’édition complètes du [Designer d’e-mail](../email/get-started-email-design.md).
* **Alignement des marques** : vérifiez que les couleurs, les polices et le style correspondent à vos directives de marque, en utilisant les thèmes, le cas échéant. [En savoir plus sur les thèmes des emails](../email/apply-email-themes.md).
* **** : ajoutez du contenu dynamique et des jetons de personnalisation selon les besoins. [En savoir plus sur la personnalisation](../personalization/personalize.md).
* **Accessibilité** : passez en revue et améliorez les fonctionnalités d’accessibilité si nécessaire. [En savoir plus sur le contenu d’e-mail accessible](../email/accessible-content.md).

+++

+++Vos commentaires sont les bienvenus !

Utilisez la section dédiée pour partager vos idées et suggestions avec Adobe afin de nous aider à améliorer la fonctionnalité.

+++






## Questions fréquentes {#faq}

+++Qu’advient-il de mon contenu d’e-mail existant lorsque je convertis une image en modèle de contenu ?

Tout le contenu existant de votre e-mail est supprimé et remplacé par le modèle nouvellement généré lorsque vous chargez une image pour la convertir. Assurez-vous d’enregistrer tout contenu important avant d’utiliser cette fonctionnalité. Il est préférable d’utiliser cette fonctionnalité au début de votre processus de création d’e-mail.

+++

+++Quels formats de fichiers sont pris en charge ?

Le convertisseur prend en charge les formats d’image JPEG (.jpg, .jpeg) et PNG (.png).

+++

+++Combien de temps prend le processus de conversion ?

La conversion se termine souvent en 5 minutes environ, selon la complexité et la taille de votre conception d’image. Les images très volumineuses peuvent parfois prendre jusqu’à 10 minutes ; patientez quelques instants, puis actualisez. Le traitement de l’IA s’effectue en arrière-plan, ce qui vous permet de quitter l’application et d’effectuer d’autres tâches ; il n’est pas nécessaire de garder l’écran ouvert. Une fois la conversion terminée, votre fichier est automatiquement enregistré en tant que brouillon pour que vous puissiez le réviser et le modifier.

+++

+++Puis-je modifier le modèle généré ?

Oui ! Le modèle de contenu généré s’ouvre dans le Designer d’e-mail avec des fonctionnalités de modification complètes. Vous pouvez modifier tous les aspects du modèle, y compris le texte, les images, le style, la disposition et la structure.

+++

+++Que se passe-t-il si la conversion ne correspond pas exactement à mon projet de conception ?

L’IA fait de son mieux pour interpréter avec précision votre projet de conception, mais des ajustements manuels peuvent être nécessaires. Utilisez le concepteur d’e-mail pour modifier tous les éléments qui nécessitent des ajustements.

+++

+++Puis-je utiliser cette fonctionnalité pour des pages de destination ou d’autres types de contenu ?

Le convertisseur image en HTML est actuellement conçu spécifiquement pour les modèles de contenu d’e-mail. Pour les autres types de contenu, utilisez les options de conception et d’import standard disponibles dans le concepteur d’e-mail.

+++

+++Ai-je besoin d’autorisations spéciales pour utiliser cette fonctionnalité ?

Cette fonctionnalité est disponible pour tous les clients qui ont signé l’addendum [!DNL Gen AI] avec Adobe. Si vous ne savez pas si votre entreprise a signé l’addendum, contactez votre représentant ou représentante Adobe.

+++

+++Puis-je réutiliser des modèles convertis dans plusieurs campagnes ?

Oui ! Les modèles créés avec le convertisseur d’images en HTML sont automatiquement enregistrés dans la bibliothèque de modèles de contenu. Vous pouvez y accéder et les réutiliser dans n’importe quel e-mail dans vos parcours et campagnes. [En savoir plus](content-templates.md)

+++

+++Puis-je l’utiliser pour migrer à partir d’une plateforme ?

Oui ! Le convertisseur d’images en HTML est idéal pour migrer à partir d’autres plateformes de marketing par e-mail. Il vous suffit d’exporter ou d’effectuer des captures d’écran de vos conceptions d’e-mails existantes issues de votre plateforme précédente, et de les convertir en modèles HTML prêts à être utilisés dans AJO sans avoir à les recréer à partir de zéro.

+++

## Rubriques connexes {#related-topics}

* [Commencer avec les modèles de contenu](content-templates.md)
* [Créer des modèles de contenu](create-content-templates.md)
* [Utiliser des modèles d’e-mail](../email/use-email-templates.md)
* [Utiliser les thèmes d’e-mail](../email/apply-email-themes.md)
* [Commencer la conception d’e-mails](../email/get-started-email-design.md)
