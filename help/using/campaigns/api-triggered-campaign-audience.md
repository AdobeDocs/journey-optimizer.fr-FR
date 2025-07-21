---
solution: Journey Optimizer
product: journey optimizer
title: Définir l’audience de la campagne déclenchée par l’API
description: Découvrez comment définir l’audience de campagne déclenchée par l’API.
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, déclenchées par l’API, REST, optimizer, messages
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 57%

---


# Définir l’audience de la campagne déclenchée par l’API {#api-audience}

Utilisez l’onglet **[!UICONTROL Audience]** pour définir l’audience de la campagne.

![](assets/campaign-audience.png)

1. **Sélectionnner l’audience**

   * Pour les campagnes déclenchées par l’API marketing, cliquez sur le bouton **[!UICONTROL Sélectionner une audience]** pour afficher la liste des audiences Adobe Experience Platform disponibles. [En savoir plus sur les audiences](../audience/about-audiences.md).

     >[!IMPORTANT]
     >
     >L’utilisation des audiences et des attributs de la [composition d’audiences](../audience/get-started-audience-orchestration.md) est actuellement indisponible avec Healthcare Shield ou Privacy and Security Shield.

   * Pour les campagnes déclenchées par l’API transactionnelle , les profils ciblés doivent être définis dans l’appel API. Un seul appel API prend en charge jusqu’à 20 personnes destinataires uniques. Chacune de ces personnes doit disposer d’un identifiant d’utilisateur ou d’utilisatrice unique, les doublons n’étant pas autorisés. Pour en savoir plus, consultez la documentation de l’API [Exécution de message interactif](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution/operation/postIMUnitaryMessageExecution){target="_blank"}

1. **Sélectionner le type d’identité**

   Dans le champ **[!UICONTROL Type d’identité]**, choisissez le type de clé à utiliser pour identifier les personnes dans l’audience sélectionnée. Vous pouvez soit utiliser un type d’identité existant, soit en créer un nouveau à l’aide du service d’identités Adobe Experience Platform. Les espaces de noms d’identité standard sont répertoriés dans [cette page](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

   Un seul type d’identité est autorisé par campagne. Les individus appartenant à un segment qui n’a pas le type d’identité sélectionné parmi leurs différentes identités ne peuvent pas être ciblés par la campagne. Pour en savoir plus sur les types d’identité et les espaces de noms, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=fr){target="_blank"}.

1. **Activer la création de profil lors de l’exécution de la campagne**

   Dans certains cas, vous devrez peut-être envoyer des messages transactionnels à des profils qui n’existent pas dans le système, Par exemple, si un utilisateur inconnu tente de réinitialiser le mot de passe sur votre site web. Lorsqu’un profil n’existe pas dans la base de données, Journey Optimizer vous permet de le créer automatiquement lors de l’exécution de la campagne afin de permettre l’envoi du message à ce profil.

   Pour activer la création de profil lors de l’exécution de la campagne, activez l’option **[!UICONTROL Créer de nouveaux profils]**. Si cette option est désactivée, les profils inconnus sont refusés pour tout envoi et l’appel API échoue.

   ![](assets/api-triggered-create-profile.png)

   >[!IMPORTANT]
   >
   >Cette option est fournie pour la **création de profil à très petit volume** dans un cas d’utilisation d’envoi transactionnel à large volume, avec la majorité des profils déjà existants dans la plateforme.
   >
   >Les profils inconnus sont créés dans le jeu de données **Jeu de données de profil de messagerie interactive AJO**, dans trois espaces de noms par défaut (e-mail, téléphone et ECID), respectivement pour chaque canal sortant (e-mail, SMS et notification push). Cependant, si vous utilisez un espace de noms personnalisé, l’identité est créée avec le même espace de noms personnalisé.

## Étapes suivantes {#next}

Une fois que la configuration et le contenu de votre campagne sont prêts, vous pouvez planifier son exécution. [En savoir plus](api-triggered-campaign-schedule.md)
