---
solution: Journey Optimizer
product: journey optimizer
title: Accélération de vos diffusions
description: Découvrez comment accélérer vos diffusions
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
hide: true
keywords: délivrabilité, parcours, cas d’utilisation, e-mail, réputation
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/en0jMw69ddHSQrIH05-9FfGuDwNKb36f5Lp3fLp2oAk
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 807
ht-degree: 34%

---

# Cas d’utilisation : améliorez vos diffusions{#use-case-ramp-up-your-deliveries}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment créer un parcours qui accélère progressivement vos diffusions e-mail à l’aide de l’activité Optimiser et d’une limite de profil, ce qui vous permet de préchauffer une nouvelle adresse IP et d’établir votre réputation d’expéditeur.

>[!ENDSHADEBOX]

Si vous avez récemment migré vers un autre fournisseur de services de messagerie, dʼadresse IP ou de domaine ou sous-domaine de messagerie, vous devez asseoir votre réputation d’expéditeur. Dans le cas contraire, vos diffusions risquent dʼêtre bloquées voire déplacées dans le dossier des courriers indésirables de la boîte aux lettres des destinataires. Découvrez comment accroître la réputation de vos e-mails grâce au préchauffage dʼadresses IP dans le [Guide des bonnes pratiques en matière de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=fr){target="_blank"}.

Pour préchauffer votre adresse IP, vous pouvez augmenter progressivement le nombre de vos diffusions. En savoir plus sur lʼ[optimisation de la délivrabilité dans Journey Optimizer](../reports/deliverability.md).

Ce cas d’utilisation vise à créer un parcours afin dʼaccélérer vos diffusions e-mail. Pour configurer ce parcours, procédez comme suit:

1. Créez un parcours. [En savoir plus](journey-gs.md).

1. Ajoutez une activité **[!UICONTROL Optimiser]** au parcours. [En savoir plus](optimize.md).

1. Dans les paramètres de lʼactivité de **[!UICONTROL Condition]**, définissez le nombre maximal de destinataires pour votre diffusion :

   1. Dans les paramètres d’activité **[!UICONTROL Optimiser]**, sélectionnez la méthode **[!UICONTROL Conditions]** et définissez le champ **[!UICONTROL Type]** sur **[!UICONTROL Limite de profil]**. [En savoir plus](conditions.md#profile_cap).

   1. Définissez le champ **[!UICONTROL Limite]** sur le nombre maximal de destinataires pour cette diffusion.

   ![Configuration des conditions de limite de profil pour contrôler le volume de diffusion](assets/profile-cap-condition.png)

   Vous pouvez augmenter progressivement cette limite jusqu’au nombre total dʼabonnés.

1. Ajoutez une activité d’action **[!UICONTROL E-mail]** au chemin nominal après lʼactivité **[!UICONTROL Condition]**.

   ![Configuration des messages e-mail dans un parcours d’accélération de la diffusion](assets/ramp-up-deliveries-message.png)

   Lors de lʼexécution du parcours, le message est envoyé aux profils entrants, dans la limite du nombre maximal de profils que vous avez spécifié. Lorsque cette limite est atteinte, les profils entrants empruntent lʼautre chemin.

1. Complétez le parcours avec les activités de votre choix.

Une fois votre adresse IP préchauffée, vous pouvez supprimer cette condition.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

- **TL;DR:** Ce cas pratique décrit comment créer un parcours Adobe Journey Optimizer qui augmente progressivement le volume de diffusion des e-mails à l’aide d’une condition Limite de profil pour protéger la réputation de l’expéditeur lors du réchauffement de l’adresse IP.

**Intentions:**
- Créez un parcours pour augmenter progressivement le volume de diffusion des e-mails pour le réchauffement des adresses IP
- Configurez une condition Limite de profil pour limiter le nombre de destinataires par exécution de diffusion
- Protéger la réputation de l&#39;expéditeur lors du changement de fournisseur de services de messagerie, d&#39;adresse IP ou de domaine
- Supprimez la condition de limitation du volume une fois l’adresse IP entièrement préchauffée

**Glossaire:**
- **Préchauffage d’une adresse IP** : processus d’augmentation progressive du volume d’envoi d’e-mails à partir d’une nouvelle adresse IP ou d’un nouveau domaine pour établir la réputation de l’expéditeur avec les fournisseurs de boîtes aux lettres *(spécifique au produit)*
- **Limite de profils** : type de condition dans l’activité Optimiser qui limite le nombre maximal de profils qui reçoivent un message au cours d’une *d’exécution de parcours donnée (spécifique au produit)*
- **Optimiser l’activité** : activité de zone de travail de parcours utilisée pour appliquer des conditions, des règles de ciblage ou une expérimentation afin de contrôler la façon dont les profils traversent un *de parcours (spécifique au produit)*

**Mécanismes de sécurisation :**
- Une condition Limite de profil doit être définie dans la méthode Conditions de l’activité d’optimisation pour contrôler le volume de diffusion.
- Les profils qui dépassent la limite empruntent l’autre chemin d’accès défini dans le parcours.
- La limite de profil doit être augmentée progressivement au fil du temps jusqu’au nombre total d’abonnés.

**Terminologie:**
- Nom canonique : diffusions en montée en puissance — Acronyme : none — variantes : réchauffement des adresses IP, réchauffement des adresses IP, montée en puissance de la diffusion
- Synonymes : « Préchauffage d’adresses IP » = « Préchauffage d’adresses IP » = « Création de la réputation de l’expéditeur »
- Ne les confondez pas : « Limite de profil » ≠ « limite de taille d’audience » (la limite de profil est une limite de diffusion par exécution ; la taille d’audience est le nombre total de profils qualifiés)

**FAQ:**
- **Q : Pourquoi dois-je augmenter les diffusions lors du passage à une nouvelle adresse IP ou un nouveau domaine ?** — Une nouvelle adresse IP ou un nouveau domaine n&#39;a pas d&#39;historique d&#39;envoi, de sorte que les fournisseurs de boîtes aux lettres peuvent bloquer ou envoyer des messages de dossier de spam jusqu&#39;à ce qu&#39;une réputation positive soit établie par un volume croissant et progressif.
- **Q : Comment la condition Limite de profil contrôle-t-elle le volume de diffusion ?** — Définit un nombre maximal de profils pouvant recevoir le message dans une seule exécution de parcours ; les profils au-delà de cette limite prennent plutôt un autre chemin.
- **Q : Quand puis-je supprimer la condition Limite de profil ?** — Une fois que l&#39;adresse IP est complètement préchauffée et que votre réputation de l&#39;expéditeur est établie, vous pouvez supprimer la condition du parcours.
- **Q : Puis-je augmenter la limite progressivement au fil du temps ?** — Oui ; vous pouvez mettre à jour le champ Limite dans la condition Limite de profil pour augmenter progressivement le nombre de destinataires par exécution jusqu’à atteindre le nombre total d’abonnés.

+++
