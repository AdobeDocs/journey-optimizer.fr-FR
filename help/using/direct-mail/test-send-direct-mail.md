---
solution: Journey Optimizer
product: journey optimizer
title: Vérifier et envoyer un message de publipostage direct
description: Découvrez comment vérifier et envoyer un message de publipostage direct dans Journey Optimizer.
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
TQID: https://experienceleague.adobe.com/4GZKFKOx-D-RT1mssiV5vpmZQSJGVbGMro8Q-suhtPE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 114f184e73298bf79d666ef7b17755498c93df83
workflow-type: tm+mt
source-wordcount: 582
ht-degree: 73%

---

# Vérifier et envoyer un message de publipostage direct {#direct-mail-test-send}

Découvrez comment prévisualiser le fichier d’extraction, valider et activer votre campagne ou votre parcours de publipostage direct et gérer le consentement du courrier postal dans Journey Optimizer.

## Avant de commencer {#before-you-start}

Avant de tester et d’envoyer un message de publipostage direct, [créez le message et configurez le fichier d’extraction](create-direct-mail.md). Vérifiez que vous avez également terminé [configuration du canal courrier](direct-mail-configuration.md).

## Prévisualiser le fichier d’extraction {#preview-dm}

Une fois le contenu du fichier d’extraction défini, vous pouvez utiliser des profils de test pour le prévisualiser. Si vous avez inséré du contenu personnalisé, vous pouvez vérifier l’affichage de celui-ci dans le message à l’aide des données de profil de test.

Pour ce faire, cliquez sur **[!UICONTROL Simuler du contenu]**, ajoutez ensuite un profil de test pour vérifier le rendu du fichier d’extraction à l’aide des données de profil de test.

![Simuler l’aperçu du contenu pour un fichier d’extraction de publipostage direct](assets/direct-mail-simulate.png){width="800" align="center"}

Vous trouverez des informations détaillées sur la sélection des profils de test et la prévisualisation de votre contenu dans la section [Gestion de contenu](../content-management/preview-test.md).

Une fois que le contenu du fichier est prêt à être envoyé, fermez l’écran de simulation, puis cliquez sur le bouton **[!UICONTROL Examiner pour activer]**.

## Valider et activer la campagne par courrier {#dm-validate}

>[!IMPORTANT]
>
> Si votre campagne est soumise à une politique de validation, vous devrez demander l’approbation afin de pouvoir envoyer votre campagne par courrier. [En savoir plus](../test-approve/gs-approval.md)

Avant d’activer la campagne de publipostage direct, assurez-vous que la campagne ou le parcours et le fichier d’extraction sont correctement configurés. Pour cela, vérifiez les alertes dans la section supérieure de l’éditeur. Certaines d’entre elles sont de simples avertissements, mais d’autres peuvent vous empêcher d’envoyer le message. Deux types d’alertes peuvent se produire : avertissements et erreurs.

* Les **avertissements** se rapportent aux recommandations et aux bonnes pratiques. Par exemple, un message d’avertissement s’affiche si votre SMS est vide.

* Les **erreurs** vous empêchent de publier la campagne tant qu’elles ne sont pas corrigées. Par exemple, un message d’erreur vous avertit lorsque l’objet est manquant.

![Examinez et activez l’écran affichant les alertes de validation des campagnes de publipostage direct](assets/direct-mail-review.png){width="800" align="center"}

Lorsque votre campagne de publipostage direct est prête, effectuez la configuration de votre [parcours &#x200B;](../building-journeys/journey-gs.md) ou [campagne](../campaigns/create-campaign.md) pour l’envoyer.

>[!NOTE]
>
>Le fichier exporté se termine par défaut par une nouvelle ligne. Cela garantit la compatibilité avec les outils de traitement des données standard.

Une fois l’envoi effectué, vous pouvez mesurer l’impact de votre campagne ou de votre parcours par publipostage direct dans les rapports. Pour plus d’informations sur les rapports de publipostage direct, reportez-vous aux sections suivantes :
* [Rapport de campagne par courrier](../reports/campaign-global-report-cja-direct.md)
* [Rapport de parcours de courrier](../reports/journey-global-report-cja-direct.md)

## Gérer le consentement relatif au courrier {#dm-consent-management}

Dans [!DNL Journey Optimizer], le consentement est géré par le [Schéma de consentement](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=fr){target="_blank"} d’Experience Platform. Par défaut, la valeur du champ de consentement est vide et traitée comme un consentement pour recevoir vos communications.

Si un profil s’est désabonné de la réception de courrier, dans les attributs de profil d’Experience Platform correspondants, la valeur de `consents.marketing.postalMail.val` sera `n` et le profil correspondant sera exclu des prochaines diffusions.

Pour l’activer à nouveau, l’attribut de profil doit être redéfini sur `consents.marketing.postalMail.val` : `y`.

Pour gérer les attributs d’un profil, accédez à Experience Platform et au profil en sélectionnant un espace de noms d’identité et une valeur d’identité correspondante. Pour en savoir plus, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=fr#getting-started){target="_blank"}.

En savoir plus sur la gestion des opt-outs de Journey Optimizer dans [cette section](../privacy/opt-out.md).

## Rubriques connexes {#related-topics}

* [Commencer à utiliser le courrier](get-started-direct-mail.md)
* [Créer un message de publipostage direct](create-direct-mail.md)
* [Configurer le canal courrier](direct-mail-configuration.md)
* [Prévisualiser et tester le contenu](../content-management/preview-test.md)

Pour des questions courantes sur le publipostage direct, voir [Prise en main du publipostage direct](get-started-direct-mail.md).
