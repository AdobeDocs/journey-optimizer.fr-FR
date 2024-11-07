---
title: Prise en main de la prise de décision
description: En savoir plus sur la prise de décision
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 22eae783ec2a7db2209b2a12b78b286e4f97ee1b
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 81%

---

# Prise en main de la prise de décision {#get-started-experience-decisioning}

## Présentation de la prise de décision {#about}

La prise de décision simplifie la personnalisation en offrant un catalogue centralisé d’offres marketing connues sous le nom d’« éléments de décision » et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque individu.

Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes grâce au [nouveau canal d’expérience basé sur le code](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/code-based-experience/get-started-code-based), désormais accessible dans les campagnes Journey Optimizer. Les stratégies de décision ne peuvent être utilisées que dans des campagnes d’expérience basées sur du code.


## Étapes clés de prise de décision {#steps}

Les principales étapes à suivre pour utiliser le service de prise de décision sont les suivantes :

1. **Attribuez les autorisations appropriées**. La prise de décision n’est disponible que pour les utilisateurs ayant accès à un **[!UICONTROL rôle]** lié à la prise de décision, tel que les gestionnaires de décision. Si vous ne pouvez pas accéder à la prise de décision, vos autorisations doivent être étendues.

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

1. **Créez des éléments de décision** pour l’afficher à l’audience ciblée.

1. **Organisez des collections** : utilisez des collections pour classer les éléments de décision en fonction de règles basées sur des attributs. Incorporez des collections dans vos stratégies de sélection afin de déterminer la collection d’éléments de décision à prendre en compte.

1. **Créez des règles de décision** : les règles de décision sont utilisées dans les éléments de décision et/ou les stratégies de sélection pour déterminer qui a accès à un élément de décision.

1. **Mettez en œuvre des méthodes de classement** : créez des méthodes de classement et appliquez-les dans les stratégies de décision afin de déterminer l’ordre de priorité de sélection des éléments de décision.

1. **Créez des stratégies de sélection** : créez des stratégies de sélection qui tirent parti des collections, des règles de décision et des méthodes de classement afin d’identifier les éléments de décision pouvant être affichés dans les profils.

1. **Incorporez une politique de décision dans une campagne basée sur du code** : les politiques de décision combinent plusieurs stratégies de sélection pour déterminer les éléments de décision éligibles à afficher pour l’audience prévue.
