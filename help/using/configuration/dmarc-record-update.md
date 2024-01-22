---
solution: Journey Optimizer
product: journey optimizer
title: Mise à jour DMARC obligatoire
description: Découvrez pourquoi et quand vous devez définir l’enregistrement DMARC dans Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: sous-domaine, domaine, courrier, dmarc, enregistrement
hide: true
hidefromtoc: true
source-git-commit: a93f1c81cceaee4f55cd7555284c4d8016ed4e21
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 3%

---

# Mise à jour DMARC obligatoire {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="En savoir plus sur la mise à jour DMARC obligatoire"
>abstract="Dans le cadre de l’application des bonnes pratiques du secteur, Google et Yahoo exigent tous deux que vous disposiez d’un **Enregistrement DMARC** pour tout domaine que vous utilisez pour leur envoyer des emails, en commençant par **1er février 2024**. <br>Par conséquent, vous devez vous assurer que les enregistrements DMARC sont configurés pour tous les sous-domaines que vous avez délégués à Adobe dans Journey Optimizer."

Dans le cadre de l’application des bonnes pratiques du secteur, Google et Yahoo exigent tous deux que vous disposiez d’un **Enregistrement DMARC** pour tout domaine que vous utilisez pour leur envoyer des emails. Cette nouvelle exigence commence à **1er février 2024**.

En savoir plus sur Google et les exigences de Yahoo dans [cette section](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Si vous ne respectez pas cette nouvelle exigence de Gmail et Yahoo, les emails seront probablement envoyés dans le dossier spam ou bloqués.

Par conséquent, Adobe vous recommande vivement de vous assurer que les enregistrements DMARC sont configurés pour tous les sous-domaines que vous avez délégués à l’Adobe dans [!DNL Journey Optimizer]. Suivez les étapes ci-dessous qui s’appliquent à votre cas :

<!--
* Set up DMARC on your subdomains, or on the parent domain of your subdomains, **in your hosting solution**. You can do it as of now.

* Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI** - with no extra work on your hosting solution. This feature will be available on January 30, 2024.

    >[!CAUTION]
    >
    >If you have set up [CNAME delegation](delegate-subdomain.md#cname-subdomain-delegation) for your sending subdomains, it will also require some entry into your hosting solution. Make sure you coordinate with your IT department so that they can perform the update as soon as the [!DNL Journey Optimizer] feature is available (on January 30, 2024). (and be ready on February 1st, 2024)

    More details on the [!DNL Journey Optimizer] DMARC upcoming feature will come soon.
-->

* Si vous avez [entièrement délégué](delegate-subdomain.md#full-subdomain-delegation) vos sous-domaines d’envoi à Adobe, suivez l’une des deux options ci-dessous :

   * Configuration de DMARC sur le domaine parent de vos sous-domaines délégués **dans votre solution d’hébergement**.

   * Configuration de DMARC sur vos sous-domaines délégués **à l’aide de la fonction à venir dans la fonction [!DNL Journey Optimizer] Interface utilisateur d’administration** - sans travail supplémentaire sur votre solution d’hébergement.

* Si vous avez configuré [Délégation CNAME](delegate-subdomain.md#cname-subdomain-delegation) pour vos sous-domaines d’envoi, suivez l’une des deux options ci-dessous :
   * Configurez DMARC sur vos sous-domaines ou sur le domaine parent de vos sous-domaines. **dans votre solution d’hébergement**.
   * Configuration de DMARC sur vos sous-domaines délégués **à l’aide de la fonction à venir dans la fonction [!DNL Journey Optimizer] Interface utilisateur d’administration**. Cependant, il nécessite également une entrée dans votre solution d’hébergement. Par conséquent, assurez-vous de vous coordonner avec votre service informatique afin qu’il puisse effectuer la mise à jour dès que la variable [!DNL Journey Optimizer] Cette fonctionnalité est disponible (le 30 janvier). <!--and be ready on February 1st, 2024-->

**Plus d’informations sur [!DNL Journey Optimizer] La fonctionnalité DMARC à venir sera bientôt disponible.**

>[!NOTE]
>
>Si vous avez des questions ou avez besoin d’aide, contactez votre conseiller en délivrabilité d’Adobe ou votre représentant Adobe.

Les dernières chronologies partagées par Google et Yahoo sont les suivantes :

* GOOGLE :

   * **Février 2024** - Les rebonds temporaires conçus pour avertir la non-conformité commenceront. Si vous n’êtes pas encore en conformité, les e-mails seront toujours livrés normalement après un court délai. Si vous êtes entièrement en conformité, il n’y aura pas de rebonds temporaires et vous ne serez pas affecté.

   * **Avril 2024** - Les blocs commenceront pour les expéditeurs qui ne sont pas conformes à l’exigence DMARC. Seule une partie des emails non conformes sera d&#39;abord bloquée, le pourcentage de ces derniers étant bloqué au fil du temps.

   * **1er juin 2024** - Tout expéditeur qui n’est pas entièrement conforme fera l’objet d’un blocage.

* Yahoo n&#39;a pas fourni de dates exactes, mais a déclaré que &quot;le déploiement de l&#39;application commencera en février 2024. L’application sera progressivement déployée&quot;.

>[!NOTE]
>
>En savoir plus sur l’implémentation de DMARC dans [Guide des bonnes pratiques de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} pour mieux comprendre l’impact sur la délivrabilité des emails.
