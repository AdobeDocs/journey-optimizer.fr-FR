---
solution: Journey Optimizer
product: journey optimizer
title: Actions d'Adobe Campaign Standard
description: En savoir plus sur les actions Adobe Campaign Standard
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: parcours, intégration, standard, campagne, ACS
exl-id: 50565cd9-7415-4c6a-9651-24fefeded3f5
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/spxxZT-JH5yzziL8-oSkJdBcKEppm-4ZzeLC2-laCaM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1484
ht-degree: 51%

---

# Actions [!DNL Adobe Campaign] Standard {#using_campaign_action}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment utiliser les activités d’action Adobe Campaign Standard intégrées E-mail, Push et SMS dans vos parcours en vous appuyant sur les modèles de messagerie transactionnelle Campaign Standard.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acs"
>title="Actions personnalisées"
>abstract="Une intégration est disponible si vous disposez d’[!DNL Adobe Campaign] Standard. Elle permet d’envoyer des e-mails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle d’[!DNL Adobe Campaign]."

Si vous utilisez [!DNL Adobe Campaign] Standard, les activités d’action intégrées suivantes sont disponibles : **[!UICONTROL E-mail]**, **[!UICONTROL Push]** et **[!UICONTROL SMS]**.

>[!NOTE]
>
>Pour cela, vous devez configurer l’action intégrée. Voir [cette page](../action/acs-action.md).

Pour chacun de ces canaux, vous sélectionnez un modèle de message transactionnel [!DNL Adobe Campaign] Standard **template**. Pour les canaux E-mail, SMS et Push intégrés, l’envoi de messages est confié à la messagerie transactionnelle. Cela signifie que si vous souhaitez utiliser un certain modèle de message dans vos parcours, vous devez le publier dans [!DNL Adobe Campaign] Standard. Consultez [cette page](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=fr) pour en savoir plus sur l’utilisation de cette fonctionnalité.

>[!NOTE]
>
>Le message transactionnel Campaign Standard et son événement associé doivent être publiés pour être utilisés dans Journey Optimizer. Si l’événement est publié mais que le message ne l’est pas, il ne sera pas visible dans l’interface de Journey Optimizer. Si le message est publié mais que son événement associé ne l’est pas, il sera visible dans l’interface de Journey Optimizer, mais il ne sera pas utilisable.

Configuration de l’action ![[!DNL Adobe Campaign] Standard dans le parcours &#x200B;](assets/journey59.png)

Vous pouvez utiliser un modèle de message transactionnel basé sur un événement (appelé également en temps réel) ou sur un profil.

>[!NOTE]
>
>Lorsque nous envoyons des messages transactionnels en temps réel (rtEvent) ou acheminons des messages à l’aide d’un système tiers par le biais d’une action personnalisée, une configuration spécifique est requise pour la gestion de la fatigue, des listes bloquées ou des désabonnements. Par exemple, si un attribut « unsubscribe » est stocké dans [!DNL Adobe Experience Platform] ou dans un système tiers, une condition doit être ajoutée avant l’envoi du message pour vérifier cette condition.

Lorsque vous sélectionnez un modèle, tous les champs attendus dans la payload du message sont affichés dans le volet de configuration des activités sous **[!UICONTROL Adresse]** et **[!UICONTROL Données de personnalisation]**. Vous devez faire correspondre chacun de ces champs avec celui que vous souhaitez utiliser, et ce, depuis l’événement ou la source de données. Vous pouvez également utiliser l’éditeur d’expression avancé pour transmettre une valeur manuellement, effectuer une manipulation de données sur les informations récupérées (convertir une chaîne en majuscules, par exemple) ou utiliser des fonctions telles que « if, then, else ». Consultez [cette page](expression/expressionadvanced.md).

![Interface de sélection de modèle de message Campaign Standard](assets/journey60.png)

## E-mail et SMS {#section_asc_51g_nhb}

Les paramètres sont identiques pour **[!UICONTROL E-mail]** et **[!UICONTROL SMS]**.

>[!NOTE]
>
>Lors de l’utilisation du modèle transactionnel d’un profil pour l’e-mail, le mécanisme de désabonnement est automatiquement géré par [!DNL Adobe Campaign] Standard.
>Incluez un bloc de contenu **[!UICONTROL Lien de désinscription]** dans [le modèle d’e-mail transactionnel](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=fr).
>Si vous utilisez un modèle basé sur un événement (rtEvent), incorporez dans le message un lien qui transmet l’e-mail du destinataire sous forme de paramètre d’URL et le dirige vers une page de destination de désinscription.
>Créez la page de destination et assurez-vous que la décision de désabonnement du destinataire est transmise à Adobe.

Vous devez, tout d’abord, choisir un modèle de message transactionnel.

Deux catégories sont disponibles : **[!UICONTROL Adresse]** et **[!UICONTROL Données de personnalisation]**.

Vous pouvez utiliser l’interface pour définir facilement l’emplacement de récupération de l’**[!UICONTROL adresse]** ou des **[!UICONTROL données de personnalisation]**. Vous pouvez parcourir les événements et les champs de la source de données disponible. Vous pouvez également utiliser l’éditeur d’expression avancé pour gérer des cas d’utilisation plus complexes, tels que l’utilisation d’une source de données nécessitant la transmission de paramètres ou l’exécution de manipulations. Consultez [cette page](expression/expressionadvanced.md).

**[!UICONTROL Adresse]**

>[!NOTE]
>
>Cette catégorie n’est visible que si vous sélectionnez un message transactionnel basé sur un « événement ». Pour les messages « profile », le champ **[!UICONTROL Address]** est automatiquement récupéré depuis [!DNL Adobe Campaign] Standard par le système.

Il s’agit des champs dont le système a besoin pour connaître la destination du message. Pour un modèle d’email, il s’agit de l’adresse e-mail. Pour un SMS, il s’agit du numéro de téléphone mobile.

![Configuration des paramètres de message pour l’intégration de Campaign Standard](assets/journey61.png)

**[!UICONTROL Données de personnalisation]**

>[!NOTE]
>
>Vous ne pouvez pas transmettre de collection dans les données de personnalisation. Si le SMS ou l’email transactionnel attend des collections, il ne fonctionnera pas. Notez également qu’un format spécifique est attendu pour les données de personnalisation (par exemple : chaîne, décimal, etc.). Vous devez veiller au respect de cette exigence.

Il s’agit des champs attendus par le message [!DNL Adobe Campaign] Standard . Ils peuvent être utilisés pour personnaliser le message, appliquer une mise en forme conditionnelle ou sélectionner une variante de message spécifique.

![Mappage de champs entre Journey Optimizer et Campaign Standard](assets/journey62.png)

## Notification push {#section_im3_hvf_nhb}

Avant d’utiliser l’activité Notification push, votre application mobile doit être configurée avec Campaign Standard afin d’envoyer des notifications de ce type. Consultez cet [article](https://helpx.adobe.com/fr/campaign/kb/integrate-mobile-sdk.html) pour effectuer les étapes de mise en œuvre nécessaires pour les appareils mobiles.

Vous devez, tout d’abord, choisir une application mobile dans la liste déroulante, ainsi qu’un message transactionnel.

![Éditeur d’expression avancé pour le mappage des paramètres Campaign Standard](assets/journey62bis.png)

Deux catégories sont disponibles : **[!UICONTROL Cible]** et **[!UICONTROL Données de personnalisation]**.

**[!UICONTROL Target]**

>[!NOTE]
>
>Cette catégorie n’est visible que si vous sélectionnez un message basé sur événement. Pour les messages de profil, les champs **[!UICONTROL Target]** sont automatiquement récupérés par le système à l&#39;aide de la réconciliation effectuée par [!DNL Adobe Campaign] Standard.

Dans cette section, vous devez définir la **[!UICONTROL plateforme push]**. La liste déroulante vous permet de sélectionner **[!UICONTROL Apple Push Notification Server]** (iOS) ou **[!UICONTROL Firebase Cloud Messaging]** (Android). Vous avez aussi la possibilité de sélectionner un champ spécifique à partir d’un événement ou d’une source de données, ou de définir une expression avancée.

Vous devez également définir le **[!UICONTROL jeton d’enregistrement]**. L’expression dépend de la manière dont le jeton est défini dans la payload de l’événement ou dans d’autres informations de [!DNL Journey Optimizer]. Il peut s’agir d’un champ simple ou d’une expression plus complexe au cas où le jeton serait défini dans une collection, par exemple :

```
@event{Event_push._experience.campaign.message.profileSnapshot.pushNotificationTokens.first().token}
```

**[!UICONTROL Données de personnalisation]**

>[!NOTE]
>
>Vous ne pouvez pas transmettre de collection dans les données de personnalisation. Si la notification push transactionnelle attend des collections, elle ne fonctionnera pas. Notez également qu’un format spécifique est attendu pour les données de personnalisation (par exemple : chaîne, décimal, etc.). Vous devez veiller au respect de cette exigence.

Il s’agit des champs attendus par le modèle transactionnel utilisé dans votre message [!DNL Adobe Campaign] Standard. Ils peuvent être utilisés pour personnaliser votre message, appliquer une mise en forme conditionnelle ou sélectionner une variante de message spécifique.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page explique comment utiliser les activités intégrées E-mail, SMS et Action push de Adobe Campaign Standard dans les parcours Journey Optimizer via des modèles de messages transactionnels Campaign.

**Intentions:**

* Configuration d’activités d’action E-mail, SMS ou Push dans un parcours à l’aide de l’intégration Adobe Campaign Standard
* Sélectionner et mapper un modèle de message transactionnel Campaign Standard aux champs de parcours
* Mappez les champs Adresse et Données Personalization des événements de parcours ou des sources de données à la payload du message
* Gérer le désabonnement pour les modèles d’e-mails transactionnels basés sur un événement et sur un profil
* Configuration de la plateforme cible des notifications push et du jeton d&#39;enregistrement pour les actions push Campaign Standard

**Glossaire:**

* **Messagerie transactionnelle** : fonctionnalité Adobe Campaign Standard d’envoi de messages déclenchés en temps réel (e-mail, SMS, notification push) en fonction des événements *(spécifiques au produit)*
* **rtEvent** : modèle de message transactionnel d’événement en temps réel dans Adobe Campaign Standard, utilisé pour les *de messagerie basées sur un événement (spécifiques au produit)*
* **Modèle transactionnel de profil** : modèle de message transactionnel Campaign Standard qui utilise les données de profil pour la résolution des destinataires et la gestion des désinscriptions *(spécifique au produit)*
* **Jeton d’enregistrement** : identifiant au niveau de l’appareil requis pour cibler une notification push sur un *d’installation d’application mobile spécifique (spécifique au produit)*

**Mécanismes de sécurisation :**

* L&#39;action intégrée doit être configurée avant utilisation ; consultez la page de configuration de l&#39;action.
* Le message transactionnel Campaign Standard et son événement associé doivent être publiés pour que le modèle soit utilisable dans Journey Optimizer.
* Les collections ne peuvent pas être transmises dans les champs de données Personalization.
* Pour les modèles basés sur un événement (rtEvent), la gestion des désabonnements doit être gérée manuellement avec une condition avant l’envoi.
* Pour les messages push basés sur un profil, les champs Target sont récupérés automatiquement ; la catégorie Target n&#39;est visible que pour les messages d&#39;événement.
* L’application mobile doit être configurée avec Campaign Standard pour que l’activité push puisse être utilisée.

**Terminologie:**

* Nom canonique : Adobe Campaign Standard — Acronyme : ACS — variantes : Campaign Standard
* Synonymes : « message transactionnel d’événement » = « rtEvent » ; « message transactionnel en temps réel » = « rtEvent »
* Ne pas confondre : « modèle transactionnel de profil » (le désabonnement est géré automatiquement) ≠ « modèle transactionnel d&#39;événement » (le désabonnement doit être géré manuellement)

**FAQ:**

* **Q : Quels canaux sont disponibles via l’intégration de Adobe Campaign Standard ?** : les canaux e-mail, SMS et notification push sont disponibles en tant qu’activités d’action intégrées.
* **Q : Le message transactionnel doit-il être publié dans Campaign Standard avant d’être utilisé dans Journey Optimizer ?** — Oui, le message transactionnel et son événement associé doivent être publiés ; un message dépublié ne sera pas utilisable même s&#39;il est visible dans l&#39;interface.
* **Q : Comment le désabonnement est-il géré pour les modèles d’e-mail basés sur le profil ?** — Le désabonnement est automatiquement géré par Adobe Campaign Standard lors de l&#39;utilisation d&#39;un modèle transactionnel de profil ; incluez un bloc de contenu Lien de désabonnement dans le modèle.
* **Q : Puis-je transmettre une collection en tant que données de personnalisation ?** — Non, les collections ne peuvent pas être transmises dans les données Personalization ; le message transactionnel ne doit pas s&#39;attendre à des collections.
* **Q : Où puis-je mapper l’adresse du destinataire d’un e-mail basé sur un événement ?** — La catégorie Adresse dans le volet de configuration de l&#39;activité n&#39;est visible que pour les messages transactionnels d&#39;événement ; pour les messages de profil, l&#39;adresse est récupérée automatiquement.

+++
