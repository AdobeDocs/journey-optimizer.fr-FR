---
solution: Journey Optimizer
product: journey optimizer
title: Convertir des images en modèles HTML
description: Découvrez comment utiliser le convertisseur d’images en HTML optimisé par l’IA pour convertir des conceptions d’image en modèles d’e-mail HTML modifiables.
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
badge: label="Disponibilité limitée" type="Informative"
keywords: e-mail, modèle, image, HTML, IA, conception, convertisseur
exl-id: d13467b7-2f3c-4707-a7e0-9b46cb6cafb1
source-git-commit: 7cfeabc85b9645be9d61ed6458e57e42ea319619
workflow-type: tm+mt
source-wordcount: '1659'
ht-degree: 65%

---

# Convertir des images en modèles HTML {#image-to-html}

>[!AVAILABILITY]
>
>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en bénéficier.

[!DNL Journey Optimizer] vous permet d’accélérer considérablement la création d’e-mails en convertissant des conceptions d’image statiques en modèles de contenu d’e-mail HTML entièrement personnalisables et modulaires.

Grâce à la technologie d’IA générative, un outil intégré analyse la disposition, la typographie, les couleurs et les éléments visuels de votre image et génère un code HTML propre et modulaire qui conserve la fidélité de la conception tout en garantissant une modifiabilité totale avec le [Designer d’e-mail](../email/get-started-email-design.md).

Cette fonctionnalité sans code permet aux marketeurs de transformer les ressources visuelles des concepteurs graphiques ou des outils de conception en modèles d’e-mail réactifs et modifiables qui peuvent être enregistrés et réutilisés dans plusieurs parcours et campagnes, sans avoir à recourir à une expertise technique.

Les principaux avantages sont les suivants :

* **Plus rapide qu’un codage manuel** - Le convertisseur transforme les images en HTML modifiable en quelques minutes, ce qui vous permet d’ignorer le processus manuel de transformation de la maquette en HTML, qui prend beaucoup de temps.
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

## Conversion d’une image en modèle HTML {#convert-image}

Pour convertir une conception d’image en modèle d’e-mail HTML entièrement personnalisable, procédez comme suit.

1. Assurez-vous de disposer d’un fichier image au format JPEG ou PNG contenant votre conception d’e-mail.

   >[!NOTE]
   >
   >Pour de meilleurs résultats, utilisez des images de haute qualité avec des éléments visuels clairs et du texte lisible. La largeur des images doit idéalement être comprise entre 600 et 800 pixels pour correspondre aux dimensions d’e-mail standard.

1. Accédez à la liste des modèles de contenu en sélectionnant **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Modèles de contenu]** dans le menu de gauche.

1. Cliquez sur **[!UICONTROL Créer un modèle]**.

1. Renseignez les détails du modèle et sélectionnez **[!UICONTROL E-mail]** comme canal, puis cliquez sur **[!UICONTROL Créer]**.

1. Dans la section **[!UICONTROL Convertir l’image en modèle]**, procédez comme suit :

   * (Facultatif) Si des thèmes de marque sont définis dans Journey Optimizer pour votre organisation, vous pouvez sélectionner un thème comme entrée afin que l’HTML générée soit mise en forme en fonction de vos paramètres de thème de marque. [En savoir plus sur les thèmes](../email/apply-email-themes.md)

     Les styles tels que la couleur d’arrière-plan, la couleur du bouton, les polices, l’espacement des lignes, les marges et la marge intérieure seront appliqués au modèle généré, ce qui réduit le travail de conception supplémentaire et permet de produire un modèle prêt à l’emploi avec un minimum de modifications.

   * Pour pouvoir charger une image, assurez-vous qu’elle ne contient pas d’informations d’identification personnelle (PII) ou d’autres données sensibles. Cochez ensuite la case correspondante pour confirmer que vous avez examiné le fichier.

   * Cliquez sur le bouton **[!UICONTROL Télécharger l’image]** pour sélectionner votre fichier image.

     ![](../email/assets/email_designer_convert_img.png)

     >[!CAUTION]
     >
     >Lorsque vous chargez une image pour la conversion, tout le contenu actuellement ajouté dans l’e-mail sera supprimé et remplacé par le modèle généré.


1. Après avoir sélectionné l’image, cliquez sur **[!UICONTROL Ouvrir]** pour lancer le processus de conversion optimisé par l’IA.

   >[!NOTE]
   >
   >Le processus de génération peut prendre jusqu’à 5 minutes selon la complexité et la taille de votre conception d’image. Vous pouvez quitter cet écran et travailler sur d’autres tâches pendant que la conversion est en cours.

1. Une fois la conversion terminée, votre modèle de contenu est automatiquement enregistré en tant que brouillon.

   ![](../email/assets/email_designer_converted_img.png)

1. Cliquez sur **[!UICONTROL Modifier le corps de l’e-mail]**. Le modèle converti s’ouvre dans le [Designer d’e-mail](../email/get-started-email-design.md) avec des fonctionnalités de modification complètes. Vous pouvez maintenant :

   * Vérifier, modifier le contenu textuel et appliquer une personnalisation
   * modifier des images et ajouter des liens ;
   * ajuster les couleurs, les polices et le style ;
   * ajouter, supprimer ou réorganiser des composants de contenu.
   * tirer profit de toutes les fonctionnalités du concepteur d’e-mail comme pour tout autre modèle.

   ![](../email/assets/email_designer_html_components.png)

1. Effectuez les ajustements nécessaires pour affiner le modèle et respecter les directives de votre marque.

1. Une fois satisfait de votre modèle, cliquez sur **[!UICONTROL Enregistrer]**.

Votre modèle est maintenant disponible dans la bibliothèque de modèles de contenu et peut être utilisé lors de la création d’e-mails dans des parcours ou des campagnes. [Découvrez comment utiliser les modèles de contenu.](../email/use-email-templates.md)

## Bonnes pratiques {#best-practices}

Pour obtenir des résultats optimaux lors de la conversion d’images en modèles de contenu HTML, suivez ces recommandations.

**Avant de commencer**

* **Enregistrez le contenu existant** : la conversion d’une image en HTML remplacera tout le contenu existant de votre e-mail. Enregistrez toujours votre travail actuel avant d’utiliser cette fonctionnalité.
* **Planifiez votre workflow** : utilisez le convertisseur d’images en HTML au début du processus de création d’e-mail ou assurez-vous que vous souhaitez remplacer tout le contenu actuel.

**Préparation des images**

* **Résolution** : utilisez des images de haute résolution (au moins 1 200 px de large) pour une meilleure reconnaissance du texte et une meilleure détection des éléments.
* **Clarté** : assurez-vous que le texte est clairement lisible et que les éléments visuels sont bien définis.
* **Largeur** : concevez des images aux largeurs d’e-mail standard (600 à 800 px) pour répondre aux exigences courantes des clients de messagerie
* **Format de fichier** : utilisez le format JPEG ou PNG pour éviter les images compressées ou de faible qualité.
* **Conception complète** : incluez la conception complète d’e-mail dans une seule image, de l’en-tête au pied de page.

**Éléments de conception à prendre en compte**

* **Dispositions simples** : les dispositions plus simples et bien structurées se convertissent avec plus de précision que les conceptions très complexes.
* **Éléments standard** : utilisez des modèles de conception d’e-mail courants (en-tête, sections de corps, CTA, pied de page).
* **Lisibilité du texte** : assurez-vous que le contraste entre le texte et l’arrière-plan est suffisant.
* **Polices compatibles avec le web** : les conceptions qui utilisent des polices compatibles avec le web courantes offriront une meilleure fidélité.
* **Évitez le chevauchement des éléments** : séparez clairement les éléments de conception pour une meilleure reconnaissance de la structure.

**Après la conversion**

* **Vérifiez votre brouillon** : une fois la conversion terminée, votre modèle est automatiquement enregistré en tant que brouillon. Examinez attentivement le HTML généré pour en vérifier la précision.
* **Testez minutieusement** : testez l’e-mail sur différents clients de messagerie et appareils.
* **Affinez manuellement** : effectuez les ajustements nécessaires à l’aide des fonctionnalités de modification complètes du concepteur d’e-mail.
* **Alignement de la marque** : vérifiez que les couleurs, les polices et le style correspondent à vos directives de marque.
* **Personnalisation** : ajoutez du contenu dynamique et des jetons de personnalisation selon les besoins.
* **Accessibilité** : consultez et améliorez les fonctionnalités d’accessibilité si nécessaire.

## Mécanismes de sécurisation et recommandations {#limitations}

Gardez à l’esprit les limites suivantes lors de la conversion d’images en modèles de contenu HTML.

* **Interprétation de l’IA** : l’IA génère le HTML en fonction de l’interprétation visuelle de votre image. Les conceptions complexes ou inhabituelles peuvent nécessiter des réglages manuels après la conversion.

* **Précision du texte** : bien que l’IA tente de reconnaître et de reproduire le texte avec précision, vérifiez toujours le contenu du texte et apportez les corrections nécessaires.

* **Contenu dynamique** : le processus de conversion crée un HTML statique en fonction de votre image. Vous devrez ajouter manuellement la personnalisation, le contenu dynamique et le suivi après la conversion.

* **Dispositions complexes** : les conceptions très complexes avec des superpositions complexes, des formes inhabituelles ou des éléments non standard peuvent ne pas se convertir parfaitement. Des conceptions plus simples donnent généralement de meilleurs résultats.

* **Temps de traitement** : le processus de conversion peut prendre jusqu’à 5 minutes selon la complexité et la taille de votre image. Le traitement par l’IA se produit en arrière-plan, ce qui vous permet de travailler sur d’autres tâches sans garder l’écran ouvert. Le modèle est automatiquement enregistré en tant que brouillon une fois la conversion terminée.

* **Disponibilité limitée** : en tant que fonctionnalité en disponibilité limitée, le convertisseur d’images en HTML est régulièrement amélioré. Le fonctionnement et la précision peuvent varier, et vos commentaires permettent d’améliorer la fonctionnalité.

>[!NOTE]
>
>Le convertisseur d’images en HTML est conçu de manière à fournir un point de départ solide pour la création d’e-mails. Le HTML généré doit être examiné et affiné à l’aide du concepteur d’e-mail afin de s’assurer qu’il répond exactement à vos besoins.

## Questions fréquentes {#faq}

+++Qu’advient-il du contenu existant de mon e-mail lorsque j’utilise le convertisseur d’images en HTML ?

Tout le contenu existant de votre e-mail est supprimé et remplacé par le modèle nouvellement généré lorsque vous chargez une image pour la convertir. Assurez-vous d’enregistrer tout contenu important avant d’utiliser cette fonctionnalité. Il est préférable d’utiliser le convertisseur d’images en HTML au début de votre tâche de création d’e-mail.

+++

+++Quels formats de fichiers sont pris en charge ?

Le convertisseur d’images en HTML prend en charge les formats d’images JPEG (.jpg, .jpeg) et PNG (.png).

+++

+++Combien de temps prend le processus de conversion ?

La conversion peut prendre jusqu’à 5 minutes, selon la complexité et la taille de votre image. Le traitement par IA s’effectue en arrière-plan, vous pouvez donc quitter l’application et travailler sur d’autres tâches ; il n’est pas nécessaire de garder la fenêtre ouverte à l’écran. Une fois la conversion terminée, votre fichier est automatiquement enregistré en tant que brouillon pour que vous puissiez l’examiner et le modifier.

+++

+++Puis-je modifier le modèle généré ?

Oui ! Le modèle HTML généré s’ouvre dans le concepteur d’e-mail avec les fonctionnalités d’édition complètes. Vous pouvez modifier tous les aspects du modèle, y compris le texte, les images, le style, la disposition et la structure.

+++

+++Que se passe-t-il si la conversion ne correspond pas exactement à mon projet de conception ?

L’IA fait de son mieux pour interpréter avec précision votre projet de conception, mais des ajustements manuels peuvent être nécessaires. Utilisez le concepteur d’e-mail pour modifier tous les éléments qui nécessitent des ajustements.

+++

+++Puis-je utiliser cette fonctionnalité pour des pages de destination ou d’autres types de contenu ?

Le convertisseur d’images en HTML est actuellement conçu spécifiquement pour les modèles d’e-mails. Pour les autres types de contenu, utilisez les options de conception et d’import standard disponibles dans le concepteur d’e-mail.

+++

+++Ai-je besoin d’autorisations spéciales pour utiliser cette fonctionnalité ?

Le convertisseur d’images en HTML est disponible en disponibilité limitée. Vous avez besoin d’un accès à la disponibilité limitée (contactez votre représentant ou représentante Adobe pour obtenir cet accès) et des autorisations standard du concepteur d’e-mail pour utiliser cette fonctionnalité.

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
* [Importer le contenu de vos e-mails](../email/existing-content.md)
* [Concevoir du contenu en partant de zéro](../email/content-from-scratch.md)
