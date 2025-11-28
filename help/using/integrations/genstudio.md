---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser GenStudio for Performance Marketing dans Journey Optimizer
description: Découvrez comment utiliser GenStudio for Performance Marketing dans Journey Optimizer.
feature: Content Assistant, Integrations
topic: Content Management, Artificial Intelligence
badge: label="Disponibilité limitée" type="Informative"
role: User
level: Beginner, Intermediate
exl-id: c22a44a8-e4e2-453a-9ca2-b80f7c0edc19
source-git-commit: c03fc0e53cdaaa735c4fa48113db7b4f848e33a8
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 46%

---

# Utiliser GenStudio for Performance Marketing {#ajo-genstudio}

>[!CONTEXTUALHELP]
>id="ajo_genstudio_button"
>title="Utiliser un modèle créé avec GenStudio"
>abstract="Grâce à l’intégration transparente à Adobe GenStudio for Performance Marketing, vous pouvez facilement importer un modèle GenStudio amélioré par la technologie d’IA Adobe."

## Commencer avec GenStudio {#gs-genstudio}

[Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/fr/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"} est une application axée sur l’IA générative qui permet aux équipes marketing de créer leurs propres publicités et e-mails afin de mener des campagnes marketing percutantes et personnalisées, tout en respectant les normes de votre marque et les politiques de votre entreprise. La technologie d’IA d’Adobe met à votre disposition une suite complète d’outils qui simplifient la création et la gestion de contenu, ce qui permet aux personnes en charge de la création de se concentrer sur l’innovation.

>[!AVAILABILITY]
>
>* L’intégration de GenStudio dans [!DNL Adobe Journey Optimizer] n’est actuellement pas disponible pour une utilisation avec les offres complémentaires **Healthcare Shield** ou **Privacy and Security Shield**.
>
>* Cette fonctionnalité est disponible uniquement pour le canal e-mail.

Pour améliorer l’efficacité marketing et maintenir la cohérence de la marque, vous pouvez intégrer facilement les expériences [!DNL **GenStudio for Performance Marketing**] avec [!DNL **Adobe Journey Optimizer**]. Vous pouvez ainsi tirer parti de la création de contenu optimisée par l’IA de [!DNL GenStudio], ainsi que des fonctionnalités d’orchestration avancées de [!DNL Journey Optimizer].

![Importer du contenu GenStudio dans Adobe Journey Optimizer](../rn/assets/do-not-localize/genstudio.gif)

>[!INFO]
>
>Pour aller plus loin, consultez cette [vue d’ensemble](https://business.adobe.com/fr/products/genstudio-for-performance-marketing.html#watch-overview){target="_blank"} ainsi qu’une [démonstration](https://business.adobe.com/fr/products/genstudio-for-performance-marketing.html#demo){target="_blank"} de [!DNL Adobe GenStudio for Performance Marketing].

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Conditions préalables {#genstudio-prerequisites}

Pour utiliser l’intégration [!DNL GenStudio for Performance Marketing] avec [!DNL Journey Optimizer], assurez-vous que les exigences suivantes sont remplies :

* Votre organisation doit disposer d’une licence active pour [!DNL GenStudio for Performance Marketing].

* [!DNL GenStudio for Performance Marketing] et [!DNL Adobe Journey Optimizer] doivent appartenir à la même organisation IMS.

* Les utilisateurs doivent disposer au minimum du rôle **collaborateur** ou d’un rôle supérieur pour [!DNL GenStudio for Performance Marketing] les fonctionnalités d’intégration. [En savoir plus sur les rôles utilisateur dans GenStudio](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/user-roles){target="_blank"}

<!--To access the GenStudio integration in [!DNL Adobe Journey Optimizer] feature, users need to be granted the **xxx** permission. [Learn more](../administration/permissions.md)

>[!IMPORTANT]
>
>* Before starting using this capability, read out related [Guardrails and Limitations](#generative-guardrails).-->

<!--Guardrails and limitations {#genstudio-guardrails}

General guidelines for using the GenStudio integration in [!DNL Adobe Journey Optimizer] for email generation are listed below:

See if guidelines/limitations such as the ones listed [here](../content-management/gs-generative.md#generative-guardrails) for AI Assistant can apply.

The following limitations apply to GenStudio integration in [!DNL Adobe Journey Optimizer]:-->

## Utilisation des fonctionnalités de GenStudio dans Journey Optimizer {#use-genstudio}

L’intégration entre [!DNL GenStudio for Performance Marketing] et [!DNL Journey Optimizer] permet aux équipes marketing de votre entreprise de mieux collaborer afin de rationaliser les processus.

Par exemple, une personne spécialiste du marketing technique, qui utilise [!DNL Journey Optimizer] pour concevoir et automatiser des campagnes e-mail, peut collaborer avec une personne spécialiste du marketing de performance qui crée du contenu à l’aide de [!DNL GenStudio].

Grâce à cette intégration, les deux personnes spécialistes peuvent collaborer pour intégrer facilement du contenu conforme à la marque depuis [!DNL GenStudio] dans [!DNL Journey Optimizer], afin de diffuser des e-mails attrayants ciblant des segments de clientèle spécifiques et générant des ventes.

### Fonctionnalités principales {#genstudio-capabilities}

Cette intégration offre de puissantes fonctionnalités à votre organisation marketing :

* **Génération de contenu optimisée par l’IA** : utilisez l’IA générative d’Adobe pour créer plusieurs variations d’e-mail sur la marque de manière efficace, avec des suggestions de copie intelligentes et des éléments de conception.

* **Intégration transparente des workflows** : exportez les modèles d’e-mail Journey Optimizer vers GenStudio, créez des variations à l’aide d’invites d’IA et réimportez-les dans Journey Optimizer dans le cadre d’un processus simplifié.

* **Gestion centralisée des ressources** : accédez à GenStudio ContentHub, optimisé par Adobe Experience Manager Assets, pour organiser, stocker et récupérer toutes les ressources numériques dans un emplacement centralisé.

* **Expérimentation de contenu** : importez plusieurs variations d’e-mail GenStudio dans Journey Optimizer et tirez parti des fonctionnalités d’expérimentation pour tester et identifier le contenu le plus performant.

* **Informations axées sur les performances** : suivez les performances des campagnes avec des analyses optimisées par l’IA pour comprendre quels éléments créatifs trouvent un écho auprès de votre audience et optimiser les campagnes futures.

### Cas d’utilisation courants {#genstudio-use-cases}

L’intégration entre [!DNL GenStudio for Performance Marketing] et [!DNL Journey Optimizer] prend en charge divers scénarios marketing :

* **Campagnes de lancement de produit** : générez rapidement plusieurs variantes d’e-mail pour les annonces de produit, testez-les avec différents segments d’audience et mettez à l’échelle la version gagnante sur l’ensemble de votre base de clients.

* **Promotions de vacances et saisonnières** : produisez du contenu de campagne sensible au temps à l’échelle à l’aide de modèles GenStudio, assurant ainsi la cohérence de la marque tout en respectant des délais serrés.

* **Tests A/B à grande échelle** : créez de nombreuses variations de contenu dans GenStudio et testez-les systématiquement dans Journey Optimizer pour améliorer en permanence les performances des e-mails.

* **Personnalisation multi-segment** : générez du contenu personnalisé pour différents profils clients dans GenStudio, puis déployez chaque variation sur son segment correspondant dans Journey Optimizer pour une pertinence maximale.

## Utilisation de l’intégration GenStudio {#how-to-use}

Le workflow d’intégration se compose de deux étapes principales : exportation d’un modèle de Journey Optimizer vers GenStudio et réimportation d’expériences GenStudio dans Journey Optimizer.

### Exporter un modèle HTML de Journey Optimizer vers GenStudio {#export-from-ajo-to-genstudio}

Commencez par exporter un modèle HTML [!DNL Journey Optimizer], y compris les directives de votre marque, vers [!DNL GenStudio for Performance Marketing]. Suivez les étapes ci-dessous.

1. Dans [!DNL Journey Optimizer], accédez au contenu de votre e-mail dans un parcours ou une campagne. [Voici comment procéder](../email/get-started-email-design.md#key-steps)

1. Dans le Concepteur d’e-mail, sélectionnez **[!UICONTROL Exporter le HTML]** à partir du bouton **[!UICONTROL Plus]**.

   ![](assets/genstudio-export-template.png){zoomable="yes"}

1. Chargez ce modèle exporté HTML dans [!DNL GenStudio for Performance Marketing]. <!--Make sure you detect the fields that the generative AI uses to insert content in order to create an actionable template.-->

   >[!NOTE]
   >
   >Découvrez comment charger un modèle HTML dans [!DNL GenStudio] dans la section dédiée du [Guide d’utilisation d’Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/fr/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#templates-from-ajo-and-marketo){target="_blank"}.

1. Dans GenStudio, utilisez ce modèle pour créer plusieurs variantes d’e-mail à l’aide de prompts d’IA, puis enregistrez-les.

   >[!NOTE]
   >
   >Découvrez comment créer des expériences d’e-mail dans la [section](https://experienceleague.adobe.com/fr/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience){target="_blank"} dédiée à GenStudio.

### Tirer profit des expériences GenStudio dans Journey Optimizer {#leverage-genstudio-experiences}

Une fois que vous avez créé des variations d’e-mail dans GenStudio, réimportez-les dans [!DNL Journey Optimizer] pour les utiliser dans vos campagnes. Suivez les étapes ci-après.

1. Dans [!DNL Journey Optimizer], [ajoutez un e-mail](../email/create-email.md) à une campagne.

1. Depuis l’écran de configuration de la campagne, accédez à l’écran [Modifier le contenu](../email/create-email.md#define-email-content), puis cliquez sur **[!UICONTROL Modifier le corps de l’e-mail]** pour ouvrir le Concepteur d’e-mail. [Voici comment procéder](../email/get-started-email-design.md#key-steps)

1. Sur la page d’accueil du Concepteur d’e-mail, sélectionnez **[!UICONTROL Importer le HTML]**, puis cliquez sur le bouton **[!UICONTROL Adobe GenStudio for Performance Marketing]**.

   ![](assets/genstudio-pem-import-email.png){zoomable="yes"}

1. Parcourez les expériences GenStudio pour commencer à créer votre contenu. Vous pouvez filtrer les expériences selon plusieurs critères tels que les produits, les personas, les marques ou même les couleurs.

   <!--![](assets/genstudio-filter-experiences.png){zoomable="yes"}-->

1. Sélectionnez une expérience et cliquez sur **[!UICONTROL Utiliser]**.

   ![](assets/genstudio-use-experience.png){zoomable="yes"}

1. Sélectionnez le dossier dans lequel vous souhaitez importer l’expérience GenStudio.

   ![](assets/genstudio-choose-destination.png){zoomable="yes"}

1. Le contenu sélectionné s’affiche dans le Concepteur d’e-mail.

   ![](assets/genstudio-email-content.png){zoomable="yes"}

   >[!NOTE]
   >
   >Les expériences GenStudio [créées à partir d’un modèle [!DNL Journey Optimizer]  &#x200B;](#export-from-ajo-to-genstudio) sont importées directement dans le Designer d’e-mail avec des fonctionnalités d’édition complètes. Les expériences GenStudio créées sans modèle de [!DNL Journey Optimizer] sont importées en [mode de compatibilité](../email/existing-content.md), qui peut comporter des fonctionnalités de modification limitées.

1. Utilisez les [&#x200B; outils d’édition de contenu d’e-mail &#x200B;](../email/content-from-scratch.md) et [&#x200B; champs de personnalisation &#x200B;](../personalization/personalize.md) pour modifier votre e-mail selon vos besoins. Enregistrez votre contenu.

1. Retournez à la page récapitulative de la campagne, puis cliquez sur **[!UICONTROL Créer une expérience]** pour lancer une expérimentation. [Découvrir comment créer une expérience de contenu](../content-management/content-experiment.md)

   <!--![](assets/genstudio-create-experiment.png){zoomable="yes"}-->

1. Créez plusieurs traitements et répétez les étapes ci-dessus pour importer et utiliser rapidement les autres variantes d’expérience d’e-mail que vous avez créées dans [!DNL GenStudio].

   ![](assets/genstudio-define-treatments.png){zoomable="yes"}

1. Enregistrez vos modifications et [activez](../campaigns/review-activate-campaign.md) la campagne.

1. Après avoir exécuté l’expérience, suivez les performances de vos traitements de campagne avec le [rapport de campagne d’expérimentation](../reports/campaign-global-report-cja-experimentation.md). Vous pourrez ensuite interpréter les résultats de votre expérience. [Voici comment procéder](../content-management/get-started-experiment.md#interpret-results)

## Questions fréquentes {#genstudio-faq}

Trouvez des réponses aux questions courantes sur l’intégration [!DNL GenStudio for Performance Marketing] à [!DNL Journey Optimizer].

+++Puis-je utiliser l’intégration de GenStudio pour des canaux autres que l’e-mail ?

Actuellement, l’intégration [!DNL GenStudio for Performance Marketing] est disponible uniquement pour le canal e-mail. La prise en charge de canaux supplémentaires peut être ajoutée dans les prochaines versions.
+++

+++L’intégration de GenStudio est-elle disponible pour tous les clients Journey Optimizer ?

L’intégration n’est actuellement pas disponible pour les organisations qui utilisent les offres complémentaires **Healthcare Shield** ou **Privacy and Security Shield**.
+++

+++Puis-je modifier le contenu GenStudio après l’avoir importé dans Journey Optimizer ?

Oui, après avoir importé des expériences GenStudio dans [!DNL Journey Optimizer], vous pouvez utiliser le Designer d’e-mail [outils d’édition de contenu](../email/content-from-scratch.md) et ajouter des [champs de personnalisation](../personalization/personalize.md) pour personnaliser davantage le contenu de votre e-mail.
+++

+++Qu’advient-il des expériences GenStudio créées sans modèle Journey Optimizer ?

Les expériences GenStudio créées à partir d’un modèle de [!DNL Journey Optimizer] sont importées directement dans le Designer d’e-mail. Les expériences GenStudio créées sans [!DNL Journey Optimizer]modèle sont importées en [mode de compatibilité](../email/existing-content.md).
+++

+++Puis-je tester plusieurs variations d’e-mail GenStudio dans Journey Optimizer ?

Oui, vous pouvez créer plusieurs traitements de contenu en important différentes variations d’e-mail GenStudio et utiliser la fonctionnalité de Journey Optimizer [expérimentation de contenu](../content-management/content-experiment.md) pour tester la variation la plus performante avec votre audience.
+++

+++Comment GenStudio assure-t-il la cohérence de la marque ?

GenStudio utilise des contrôles de marque optimisés par l’IA pour s’assurer que tout le contenu généré respecte les normes et directives de votre marque. Lorsque vous chargez des modèles qui incluent des éléments de votre marque, GenStudio applique ces normes à toutes les variations de contenu créées dans la plateforme.
+++

+++Puis-je collaborer avec d’autres membres de l’équipe sur des expériences GenStudio ?

Oui, GenStudio est conçu pour la collaboration. Plusieurs membres de l’équipe disposant des autorisations appropriées peuvent collaborer à la création et à l’amélioration des expériences d’e-mail avant de les importer dans [!DNL Journey Optimizer].
+++

## Vidéo pratique {#video}

Découvrez le processus d’export d’un modèle d’e-mail de Journey Optimizer vers GenStudio for Performance Marketing, de création d’e-mails conformes à la marque à l’aide du modèle dans GenStudio et de réimport transparent dans Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3456038/?quality=12)