---
title: Optimiser le texte des e-mails pour les boîtes de réception d’IA
description: Affinez la couche de texte brut de l’e-mail dans Journey Optimizer afin que les clients de boîte de réception assistés par l’IA puissent utiliser vos offres et vos appels à l’action lorsqu’ils résument l’intention de l’e-mail ou l’extraient, dans le Designer d’e-mail avec optimisation grâce à l’IA.
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
source-git-commit: 43444cc8c49bd50dce54995c70b4fc8ef0976119
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 1%

---

# Optimiser le texte des e-mails pour les boîtes de réception d’IA {#email-text-optimizer}

[!DNL Adobe Journey Optimizer] est fourni avec une fonctionnalité de canal e-mail qui vous permet de structurer la [version texte](../email/text-version-email.md) de vos messages pour améliorer les expériences de boîte de réception assistée par l’IA, telles que les [!DNL Apple Intelligence] et les [!DNL Google Gemini] dans [!DNL Gmail], afin qu’ils puissent répondre aux questions et résumer le courrier plus précisément en fonction de votre contenu, avec de meilleurs résultats.

>[!NOTE]
>
>Cette fonctionnalité modifie uniquement le texte brut, et non la version HTML du contenu de votre e-mail.

Avec cet optimiseur de texte d’e-mail, vous pouvez vous assurer que la version en texte brut du contenu de votre e-mail est améliorée pour les expériences de boîte de réception assistée par IA, de sorte que les informations que vous fournissez aux fonctionnalités d’IA de ces fournisseurs de boîte de réception d’e-mail soient exactement celles que vous souhaitez fournir.

## Fonctionnement {#how-it-works}

Les questions standard que les destinataires peuvent poser dans les expériences de boîte de réception assistée par l’IA sont les suivantes *De quoi s’agit cet e-mail ?* ou *quelles sont ces offres ?*.

* Les réponses fournies par ces assistants d’IA peuvent être un bref résumé (par exemple, le message est promotionnel, mentionne un accès anticipé à VIP et une vente, et inclut des liens vers des catégories de produits), mais omettent toujours les objectifs qui préoccupaient le professionnel du marketing, car les assistants déduisent de tout texte qu’ils voient réellement, et pas nécessairement de l’histoire complète que vous souhaitiez raconter.

* En outre, les assistants peuvent rechercher de manière proactive des remises ou des coupons liés à la marque et les inclure dans la réponse, de sorte que l’utilisateur ne regarde plus uniquement ce que votre message a réellement promis. Ce comportement est utile pour les utilisateurs finaux, mais dilue le contrôle pour les spécialistes marketing qui ont besoin de réponses pour suivre les termes réels de l’envoi.

Pour éviter ces problèmes, [!DNL Journey Optimizer] réécrit le texte brut afin que les coupons, les périodes de remise, les appels à l’action et d’autres priorités apparaissent au premier plan dans une copie linéaire claire. L’objectif est que l’IA dédiée aux boîtes de réception puisse ancrer les résumés et les questions/réponses dans vos offres et actions définies, au lieu de s’appuyer sur une partie de texte mince par défaut ou sur des résultats web sans rapport.

>[!IMPORTANT]
>
>Les comportements exacts des assistants d’IA dépendent du fournisseur de boîte de réception et de la version du modèle. Une fois votre e-mail diffusé, les réponses et les résumés fournis par les clients d’IA externes peuvent être incorrects, incomplets ou mélangés avec des résultats web.
>
>La fonctionnalité Optimiser le texte des e-mails pour les boîtes de réception de l’IA améliore uniquement le texte brut que vous créez dans Journey Optimizer ; elle ne garantit pas la façon dont un assistant tiers interprétera ou affichera le message. En savoir plus sur les [limites et risques de l’IA de boîte de réception tierce](#inbox-ai-risks).

## Cas d’utilisation recommandés {#use-cases}

<!--
* **Critical details only in images** — Offers, promo codes, or deadlines shown in banners or graphics are invisible in plain text. Use the optimizer (and manual edits) so the same facts appear as text, improving extraction by AI summaries and text-only clients.-->

* **Texte généré automatiquement dense ou fragmenté** — Lorsque le texte brut par défaut est difficile à analyser, l’optimisation peut produire un récit linéaire plus clair avec des offres et des liens explicites.

* **Contrôle des questions/réponses dans la boîte de réception** — Lorsque vous prévoyez que les destinataires interrogent les assistants *sur le sujet de l’e-mail* ou *sur les offres*, une version en texte brut fort réduit les résumés partiels et réduit la dépendance aux réponses web qui ne sont pas liées à votre copie approuvée.

## Optimiser pour les expériences de boîte de réception d’IA {#optimize-with-ai}

>[!IMPORTANT]
>
>Avant de commencer à utiliser cette fonctionnalité, lisez les [Risques et limites](#inbox-ai-risks) associés.
>
>Pour accéder à cette fonctionnalité, vous devez accepter un contrat d’utilisation qui s’affiche la première fois que vous utilisez Generative AI dans [!DNL Journey Optimizer]. Pour plus d’informations, consultez les [instructions d’utilisation de Adobe Experience Cloud Generative AI](https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

Pour optimiser la version en texte brut de votre e-mail pour les boîtes de réception de l’IA avec [!DNL Journey Optimizer], procédez comme suit.

1. Ouvrez l’e-mail dans le Designer d’e-mail[&#x200B; (à partir d’une campagne, d’un parcours ou d’un modèle, selon votre workflow).](../email/content-from-scratch.md)

1. Sélectionnez l’icône **[!UICONTROL Texte brut]** pour ouvrir la version texte de votre e-mail. [En savoir plus](../email/text-version-email.md)

   ![Sélectionnez l’icône Texte brut pour ouvrir la version texte de votre e-mail](assets/text-optimizer-text-icon.png){zoomable="yes"}

1. La version texte de votre e-mail s’affiche. Cliquez sur le bouton **[!UICONTROL Optimiser pour la boîte de réception IA]** pour générer une version en texte brut améliorée qui met en surbrillance les informations clés pour la lecture et la synthèse assistées par IA.

   ![Bouton Optimiser pour la boîte de réception IA dans la vue de version texte](assets/text-optimizer-for-ai-button.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >Lorsque vous cliquez sur le bouton **[!UICONTROL Optimiser pour la boîte de réception de l’IA]**, l’option **[!UICONTROL Synchroniser avec HTML]** est automatiquement désactivée. [En savoir plus](../email/text-version-email.md#plain-text-custom)

1. Si c’est la première fois que vous utilisez Generative AI dans [!DNL Journey Optimizer], il vous sera demandé d’accepter le contrat d’utilisation. Pour en savoir plus, consultez les [instructions d’utilisation d’Adobe Generative AI](https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

   ![Boîte de dialogue du contrat d’utilisation Generative AI dans Journey Optimizer](assets/text-optimizer-agreement.png){width=50%}

   Cliquez sur **[!UICONTROL Accepter]** pour continuer.

1. Le texte généré s’affiche. Passez en revue les modifications, modifiez-les si nécessaire, puis enregistrez votre e-mail comme d’habitude.

   ![Texte généré dans la vue de version texte](assets/text-optimizer-output.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >L’optimiseur de texte d’e-mail met uniquement à jour le corps du texte brut. Cela ne modifie pas la conception, la disposition ou les images d’HTML.

1. Vous pouvez revenir à la version HTML de votre e-mail à tout moment en cliquant sur l’icône **[!UICONTROL Basculer vers la vue Bureau]**. Les modifications apportées à la version texte sont conservées.

   >[!CAUTION]
   >
   >Si vous réactivez l’option **[!UICONTROL Synchroniser avec HTML]**, vos modifications seront perdues et remplacées par du contenu texte généré à partir de la version d’HTML.

## Risques et limites de l’IA dédiée aux boîtes de réception tierces {#inbox-ai-risks}

La fonctionnalité Optimiser le texte des e-mails pour les boîtes de réception IA vous permet de préparer du texte brut sur la manière dont les fournisseurs de messagerie peuvent traiter vos envois [!DNL Journey Optimizer]. Il ne contrôle pas les produits de ces fournisseurs. Une fois qu’un message est diffusé, toutes les fonctionnalités d’IA de [!DNL Gmail], [!DNL Apple] Mail, [!DNL Outlook] ou d’autres clients fonctionnent selon leurs conditions, modèles et politiques, et non selon Adobe.

* **Présentation imprévisible** — Les résumés, les bulles de notification et les réponses conversationnelles peuvent omettre des offres, donner des prix ou des dates erronés, fusionner du contenu avec des résultats web sans rapport ou paraphraser d&#39;une manière qui ne correspond plus à votre copie approuvée. Le comportement change lorsque les fournisseurs mettent à jour les modèles ou l&#39;interface utilisateur sans préavis.

* **Pas de garantie de parité avec HTML** — Les destinataires qui dépendent des aperçus ou des réponses de l&#39;assistant risquent de ne jamais voir l&#39;intégralité de la conception d&#39;HTML, vos images ou vos pieds de page légaux. Ce qu’ils pensent que le message « dit » pourrait provenir uniquement d’un court résumé généré par l’IA.

* **Confidentialité, conformité et utilisation des données** — L&#39;IA dédiée aux boîtes de réception peut traiter le contenu des messages sur l&#39;infrastructure du fournisseur, sous réserve de la politique de confidentialité, de la conservation et des règles régionales de ce fournisseur. Les organisations des secteurs réglementés doivent évaluer si l&#39;utilisation de ces fonctionnalités par les destinataires affecte leurs obligations, quelle que soit la manière dont l&#39;e-mail a été créé en [!DNL Journey Optimizer].

* **Marque et risque juridique** — Des résumés d&#39;IA incorrects ou incomplets peuvent toujours créer de la confusion ou des différends chez les clients au sujet de promotions, de conditions ou d&#39;un langage de désinscription. L’optimiseur améliore le calque de texte que vous fournissez ; il ne garantit pas que le modèle d’un tiers le reproduira fidèlement.

* **[!UICONTROL Optimiser pour la boîte de réception de l’IA]** dans [!DNL Journey Optimizer] — L’action de temps de création dans le Designer d’e-mail est un système distinct des assistants de boîte de réception des utilisateurs finaux. Vérifiez toujours le texte brut généré avant l’envoi.

## Rubriques connexes {#related-topics}

* [Gestion de la version texte d’un e-mail](../email/text-version-email.md)
* [Commencer la conception d’e-mails](../email/get-started-email-design.md)
* Pour les fonctionnalités génératives d’Adobe en général, consultez [Prise en main de l’assistant d’IA pour la création de contenu](gs-generative.md).
