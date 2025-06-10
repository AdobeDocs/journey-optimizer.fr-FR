---
title: Commencer avec la prise de décisions
description: En savoir plus sur la prise de décisions
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 4839c3c70dcc524da5f3cc394d5573ce5755ea64
workflow-type: ht
source-wordcount: '537'
ht-degree: 100%

---

# Commencer avec la prise de décisions {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="Qu’est-ce que la prise de décisions ?"
>abstract="La prise de décisions est un nouvel outil, en plus de la gestion des décisions, permettant de sélectionner les meilleurs éléments du moteur de décision et de les diffuser à chaque individu. Elle nécessite une configuration supplémentaire pour pouvoir être utilisée."

## Qu’est-ce que la prise de décision ? {#about}

La prise de décision simplifie la personnalisation en offrant un catalogue centralisé d’offres marketing connues sous le nom d’« éléments de décision » et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque personne.

Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes grâce au [nouveau canal d’expérience basé sur le code](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/code-based-experience/get-started-code-based), désormais accessible dans les campagnes Journey Optimizer.

>[!IMPORTANT]
>
>Les politiques de décision, dans la prise de décisions, ne peuvent être utilisées que dans des campagnes d’expérience basée sur du code.

➡️ Un cas d’utilisation de bout en bout montrant comment créer des décisions et les utiliser dans des expériences de contenu avec le canal d’expérience basé sur du code est présenté dans [cette section](experience-decisioning-uc.md).

## Étapes clés de la prise de décision {#steps}

Les principales étapes pour utiliser la prise de décision sont les suivantes :

1. **Attribuez les autorisations appropriées**. La prise de décision n’est disponible que pour les utilisateurs et les utilisatrices ayant accès à un **[!UICONTROL rôle]** associé à la prise de décision, comme les Gestionnaires de décisions. Si vous ne pouvez pas accéder à la prise de décision, vos autorisations doivent être étendues.

   +++Découvrir comment attribuer le rôle de personne gestionnaire de décision

   1. Pour attribuer un rôle à un utilisateur ou une utilisatrice dans le produit [!DNL Permissions], accédez à l’onglet **[!UICONTROL Rôles]** et sélectionnez le rôle de personne gestionnaire de décision.

      ![](assets/decision_permission_1.png)

   1. Dans l’onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter un utilisateur]**.

      ![](assets/decision_permission_2.png)

   1. Saisissez le nom ou l’adresse e-mail de votre utilisateur ou utilisatrice, ou sélectionnez l’utilisateur ou l’utilisatrice dans la liste, puis cliquez sur **[!UICONTROL Enregistrer]**.

      Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez la [documentation relative à l’ajout d’utilisateurs et d’utilisatrices](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   La personne doit alors recevoir un e-mail la redirigeant vers votre instance.

+++

1. **Configurez des attributs personnalisés** : personnalisez le catalogue d’éléments selon vos besoins spécifiques en configurant des attributs personnalisés dans le schéma du catalogue.

   ➡️ [Découvrez comment configurer le catalogue d’éléments.](catalogs.md)

1. **Créez des éléments de décision** pour les afficher à l’audience ciblée.

   ➡️ [Découvrez comment créer des éléments de prise de décisions](items.md) dans l’interface d’uttilisattion (et dans la [documentation de l’API](api-reference/decisions-items/create.md)).

1. **Organisez des collections** : utilisez des collections pour classer les éléments de décision en fonction de règles basées sur des attributs. Incorporez des collections dans vos stratégies de sélection afin de déterminer la collection d’éléments de décision à prendre en compte.

   ➡️ [Découvrez comment gérer les collections d’éléments](collections.md) dans l’interface d’utilisation (et dans la [documentation de l’API](api-reference/items-collections/create.md)).

1. **Créez des règles de décision** : les règles de décision sont utilisées dans les éléments de décision et/ou les stratégies de sélection pour déterminer qui a accès à l’affichage d’un élément de décision.

   ➡️ [Découvrez comment créer des règles de décision](rules.md).

1. **Mettez en œuvre des méthodes de classement** : créez des méthodes de classement et appliquez-les dans les stratégies de sélection afin de déterminer l’ordre de priorité de sélection des éléments de décision.

   ➡️ [Découvrez comment créer des méthodes de classement.](ranking.md)

1. **Créez des stratégies de sélection** : créez des stratégies de sélection qui tirent parti des collections, des règles de décision et des méthodes de classement afin d’identifier les éléments de décision pouvant être affichés dans les profils.

   ➡️ [Découvrez comment créer des stratégies de sélection](selection-strategies.md) dans l’interface d’utilisation (et dans la documentation de l’[API](api-reference/selection-strategies/create.md)).

1. **Créez une politique de décision et incorporez-la dans votre campagne basée sur du code** : les politiques de décision combinent plusieurs stratégies de sélection pour déterminer les éléments de décision éligibles à afficher pour l’audience prévue.

   ➡️ [Découvrez comment utiliser les politiques de décision](create-decision.md)
➡️ Pour diffuser l’offre par l’intermédiaire du canal d’expérience basé sur du code, suivez les étapes d’implémentation de [cette section](../code-based/code-based-implementation-samples.md).

Pour consulter un cas d’utilisation complet montrant comment utiliser les décisions dans une expérience basée sur du code, accédez à [cette section](experience-decisioning-uc.md).
