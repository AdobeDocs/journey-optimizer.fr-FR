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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 300
ht-degree: 92%

---

# Cas d’utilisation : améliorez vos diffusions{#use-case-ramp-up-your-deliveries}

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
