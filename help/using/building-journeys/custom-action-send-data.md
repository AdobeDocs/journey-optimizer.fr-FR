---
solution: Journey Optimizer
product: journey optimizer
title: Envoyer des données à AEP
description: Découvrez comment envoyer des données à AEP.
feature: Journeys, Use Cases
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: parcours, cas d’utilisation
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 711
ht-degree: 30%

---

# Cas d’utilisation : création d’une action personnalisée pour envoyer des données à [!DNL Adobe Experience Platform]{#send-data-to-aep}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment créer un parcours qui augmente progressivement le volume de vos e-mails à l’aide d’une activité Optimiser avec une condition de limite de profil pour préchauffer votre adresse IP et protéger la réputation de votre expéditeur.

>[!ENDSHADEBOX]

Si vous avez récemment changé de fournisseur de services de messagerie, d&#39;adresse IP, de domaine ou de sous-domaine de messagerie, établissez votre réputation en tant qu&#39;expéditeur. Dans le cas contraire, les diffusions peuvent être bloquées ou déplacées vers les dossiers de spam des destinataires. Pour obtenir des conseils, consultez le [&#x200B; Guide des bonnes pratiques en matière de délivrabilité &#x200B;](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=fr){target="_blank"}.

Pour préchauffer votre adresse IP, vous pouvez augmenter progressivement le nombre de vos diffusions. En savoir plus sur lʼ[optimisation de la délivrabilité dans Journey Optimizer](../reports/deliverability.md).

Ce cas d’utilisation vise à créer un parcours afin dʼaccélérer vos diffusions e-mail. Pour configurer ce parcours, procédez comme suit:

1. Créez un parcours. [En savoir plus](journey-gs.md).

1. Ajoutez une activité **[!UICONTROL Optimiser]** au parcours. [En savoir plus](optimize.md).

1. Dans les paramètres de lʼactivité de **[!UICONTROL Condition]**, définissez le nombre maximal de destinataires pour votre diffusion :

   1. Dans les paramètres d’activité **[!UICONTROL Optimiser]**, sélectionnez la méthode **[!UICONTROL Conditions]** et définissez le champ **[!UICONTROL Type]** sur **[!UICONTROL Limite de profil]**. [En savoir plus](conditions.md#profile_cap).

   1. Définissez le champ **[!UICONTROL Limite]** sur le nombre maximal de destinataires pour cette diffusion.

   ![Condition de limite du profil pour contrôler le volume d’exécution d’une action personnalisée](assets/profile-cap-condition.png)

   Vous pouvez augmenter progressivement cette limite jusqu’au nombre total dʼabonnés.

1. Ajoutez une activité d’action **[!UICONTROL E-mail]** au chemin nominal après lʼactivité **[!UICONTROL Condition]**.

   ![Parcours avec action personnalisée pour l’envoi de données à un système externe](assets/ramp-up-deliveries-message.png)

   Lors de lʼexécution du parcours, le message est envoyé aux profils entrants, dans la limite du nombre maximal de profils que vous avez spécifié. Lorsque cette limite est atteinte, les profils entrants empruntent lʼautre chemin.

1. Complétez le parcours avec les activités de votre choix.

Une fois votre adresse IP préchauffée, vous pouvez supprimer cette condition.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page décrit un cas d’utilisation de réchauffement des adresses IP basé sur un parcours qui augmente progressivement le volume de diffusion des e-mails à l’aide d’une condition de limite de profil pour protéger la réputation de l’expéditeur.

**Intentions:**

* Créez un parcours de réchauffement des adresses IP pour augmenter progressivement le volume d’envoi des e-mails
* Configurez une condition Limite de profil pour limiter le nombre de destinataires par diffusion
* Ajoutez une activité d’action E-mail au chemin de parcours nominal
* Supprimez la condition de limite de profil une fois le réchauffement des adresses IP terminé

**Glossaire:**

* **réchauffement des adresses IP** : processus d’augmentation progressive du volume d’envoi des e-mails à partir d’une nouvelle adresse IP pour établir la réputation de l’expéditeur *(spécifique au produit)*
* **Limite de profils** : type de condition dans Journey Optimizer qui limite le nombre maximal de profils pouvant prendre un chemin de parcours spécifique *(spécifique au produit)*
* **Chemin nominal** : branche principale d’un parcours que les profils suivent lorsque les conditions sont remplies *(spécifique au produit)*

**Mécanismes de sécurisation :**

* Une condition Limite de profil doit être définie sur l’activité Condition pour contrôler le volume de diffusion lors du réchauffement des adresses IP.
* Les profils dépassant la limite sont acheminés vers l’autre chemin d’accès.
* Le parcours doit être recréé ou modifié une fois le réchauffement de l’adresse IP terminé pour supprimer la condition du bouchon.

**Terminologie:**

* Nom canonique : préchauffage d’IP — Acronyme : s.o. — variantes : préchauffage d’IP, préchauffage de la réputation de l’expéditeur
* Synonymes : « Limite de profil » = « condition de limite de destinataire »
* Ne les confondez pas : « réchauffement des adresses IP » ≠ « authentification des e-mails » (la configuration SPF/DKIM/DMARC est distincte).

**FAQ:**

* **Q : Pourquoi dois-je préchauffer mon adresse IP ?** — Les nouvelles adresses IP n&#39;ayant pas d&#39;historique d&#39;envoi, les fournisseurs de boîtes aux lettres peuvent bloquer ou bloquer les messages de dossier de spam jusqu&#39;à ce que leur réputation soit établie.
* **Q : Qu’advient-il des profils qui dépassent la limite de profil ?** — Ils utilisent l&#39;autre chemin défini dans l&#39;activité Condition.
* **Q : Comment puis-je augmenter la limite au fil du temps ?** : modifiez le champ Limite dans les paramètres de l&#39;activité Condition et augmentez-le progressivement pour atteindre le nombre total d&#39;abonnés.
* **Q : Quand puis-je supprimer la condition de limite de profil ?** — Une fois que votre adresse IP dispose d’un historique d’envoi suffisant et que les mesures de délivrabilité sont stables, vous pouvez supprimer la condition du parcours.

+++
