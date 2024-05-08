---
title: Prise en main de la prise de décision basée sur l’expérience
description: En savoir plus sur Experience Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilité limitée"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 63%

---

# Commencer avec la prise de décision basée sur l’expérience {#get-started-experience-decisioning}

>[!AVAILABILITY]
>
>Cette prise de décision basée sur l’expérience n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.
>
>Pour l’instant, la fonctionnalité n’est pas disponible pour les clients qui ont acheté l’Adobe. **Bouclier sanitaire** et **Protection de la vie privée et protection** offres complémentaires.

## Présentation d’Experience Decisioning {#about}

Experience Decisioning simplifie la personnalisation en offrant un catalogue centralisé d’offres marketing connues sous le nom d’« éléments de décision » et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque individu.

Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes grâce au nouveau canal d’expérience basé sur le code, désormais accessible dans les campagnes Journey Optimizer. Les stratégies de décision de prise de décision d’expérience ne peuvent être utilisées que dans des campagnes d’expérience basées sur du code.

## Étapes clés d’Experience Decisioning {#steps}

Les principales étapes pour travailler avec Experience Decisioning sont les suivantes :

1. **Attribuer les autorisations appropriées**. La prise de décision d’expérience n’est disponible que pour les utilisateurs ayant accès à une prise de décision liée à l’expérience **[!UICONTROL rôle]** comme les gestionnaires de décision. Si vous ne pouvez pas accéder à Experience Decisioning, vos autorisations doivent être étendues.

   +++Découvrez comment affecter le rôle des gestionnaires de décision

   1. Pour affecter un rôle à un utilisateur dans la variable [!DNL Permissions] produit, accédez à la **[!UICONTROL Rôles]** et sélectionnez Gestionnaire de décisions.

      ![](assets/decision_permission_1.png)

   1. Dans l’onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter un utilisateur]**.

      ![](assets/decision_permission_2.png)

   1. Saisissez le nom ou l’adresse e-mail de votre utilisateur ou utilisatrice, ou sélectionnez l’utilisateur ou l’utilisatrice dans la liste, puis cliquez sur **[!UICONTROL Enregistrer]**.

      Si l’utilisateur n’a pas été créé précédemment, reportez-vous à la section [Ajout de la documentation sur les utilisateurs](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   L’utilisateur ou l’utilisatrice doit alors recevoir un e-mail le ou la redirigeant vers votre instance.

+++

1. **Configuration des attributs personnalisés**: personnalisez le catalogue d’éléments selon vos besoins spécifiques en configurant des attributs personnalisés dans le schéma du catalogue.

1. **Créez des éléments de décision** pour l’afficher à l’audience ciblée.

1. **Organisez des collections** : utilisez des collections pour classer les éléments de décision en fonction de règles basées sur des attributs. Incorporez des collections dans vos stratégies de sélection afin de déterminer la collection d’éléments de décision à prendre en compte.

1. **Créez des règles de décision** : les règles de décision sont utilisées dans les éléments de décision et/ou les stratégies de sélection pour déterminer qui a accès à un élément de décision.

1. **Mettez en œuvre des méthodes de classement** : créez des méthodes de classement et appliquez-les dans les stratégies de décision afin de déterminer l’ordre de priorité de sélection des éléments de décision.

1. **Créez des stratégies de sélection** : créez des stratégies de sélection qui tirent parti des collections, des règles de décision et des méthodes de classement afin d’identifier les éléments de décision pouvant être affichés dans les profils.

1. **Incorporez une politique de décision dans une campagne basée sur du code** : les politiques de décision combinent plusieurs stratégies de sélection pour déterminer les éléments de décision éligibles à afficher pour l’audience prévue.
