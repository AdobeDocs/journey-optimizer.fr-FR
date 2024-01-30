---
solution: Journey Optimizer
product: journey optimizer
title: Respecter les nouvelles exigences DMARC
description: Découvrez pourquoi et quand vous devez définir l’enregistrement DMARC dans Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: sous-domaine, domaine, courrier, dmarc, enregistrement
source-git-commit: 11d42198436319cebb67446527e9fd8d0f80cfbc
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 5%

---

# Respecter les nouvelles exigences DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="En savoir plus sur la mise à jour DMARC obligatoire"
>abstract="Dans le cadre de l’application des bonnes pratiques du secteur, Google et Yahoo exigent tous deux que vous disposiez d’un **Enregistrement DMARC** pour tout domaine que vous utilisez pour leur envoyer des emails, en commençant par **1er février 2024**.<br>Par conséquent, vous devez vous assurer que les enregistrements DMARC sont configurés pour tous les sous-domaines que vous avez délégués à Adobe dans Journey Optimizer."

DMARC (Domain-based Message Authentication, Reporting, and Conformance) est une méthode d’authentification email qui permet aux propriétaires de domaine de protéger leur domaine d’une utilisation non autorisée. En offrant une politique claire aux fournisseurs de messagerie/FAI, elle permet d&#39;empêcher les acteurs malveillants d&#39;envoyer des emails prétendant provenir de votre domaine. La mise en oeuvre de DMARC réduit le risque que les emails légitimes soient marqués comme spam ou rejetés et améliore la délivrabilité de vos emails.


Dans le cadre de l’application des bonnes pratiques du secteur, Google et Yahoo! exigent tous deux qu’une **Enregistrement DMARC** pour tout domaine que vous utilisez pour leur envoyer des emails. Cette nouvelle exigence s’applique à partir de **1er février 2024**. [En savoir plus](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html#dmarc){target="_blank"}.

>[!CAUTION]
>
>Ne pas se conformer à cette nouvelle exigence de Gmail et Yahoo ! est susceptible d’entraîner l’entrée ou le blocage des emails dans le dossier spam.

Par conséquent, Adobe vous recommande vivement de vous assurer que les enregistrements DMARC sont configurés pour tous les sous-domaines que vous avez délégués à l’Adobe dans [!DNL Journey Optimizer]. Suivez les étapes ci-dessous qui s’appliquent à votre cas :

* Si vous avez [entièrement délégué](delegate-subdomain.md#full-subdomain-delegation) vos sous-domaines d’envoi à Adobe, procédez comme suit :

   * Configuration de DMARC sur le domaine parent de vos sous-domaines délégués **dans votre solution d’hébergement**.
or
   * Configuration de DMARC sur vos sous-domaines délégués **dans le[!DNL Journey Optimizer]** Configuration de l’interface utilisateur - sans travail supplémentaire sur votre solution d’hébergement. [Voici comment procéder.](dmarc-record.md#implement-dmarc)

* Si vous avez configuré vos sous-domaines d’envoi avec [CNAME](delegate-subdomain.md#cname-subdomain-delegation), suivez l’une des options ci-dessous :

   * Configurez DMARC sur vos sous-domaines ou sur le domaine parent de vos sous-domaines. **dans votre solution d’hébergement**.
or
   * Configuration de DMARC sur vos sous-domaines délégués **dans le[!DNL Journey Optimizer]** de l’interface utilisateur de configuration. [Voici comment procéder.](dmarc-record.md#implement-dmarc)

     Toutefois, avec la délégation CNAME, elle nécessite également une entrée dans votre solution d’hébergement. Par conséquent, assurez-vous de vous coordonner avec votre service informatique afin qu’il puisse effectuer la mise à jour dès que la variable [!DNL Journey Optimizer] Cette fonctionnalité est disponible (le 30 janvier). [En savoir plus](dmarc-record.md#implement-dmarc)

**À compter du 30 janvier, vous aurez accès à une interface en libre-service pour la mise en oeuvre DMARC. En savoir plus dans [cette section](dmarc-record.md#implement-dmarc).**

Les dernières chronologies partagées par Google et Yahoo sont les suivantes :

* GOOGLE :

   * **Février 2024** - Les rebonds temporaires conçus pour avertir la non-conformité commenceront. Si vous n’êtes pas encore en conformité, les e-mails seront toujours livrés normalement après un court délai. Si vous êtes entièrement en conformité, il n’y aura pas de rebonds temporaires et vous ne serez pas affecté.

   * **Avril 2024** - Les blocs commenceront pour les expéditeurs qui ne sont pas conformes à l’exigence DMARC. Seule une partie des emails non conformes sera d&#39;abord bloquée, le pourcentage de ces derniers étant bloqué au fil du temps.

   * **1er juin 2024** - Tout expéditeur qui n’est pas entièrement conforme fera l’objet d’un blocage.

* Yahoo n&#39;a pas fourni de dates exactes, mais a déclaré que &quot;le déploiement de l&#39;application commencera en février 2024. L’application sera progressivement déployée&quot;.

>[!NOTE]
>
>Si vous avez des questions ou avez besoin d’aide, contactez votre conseiller en délivrabilité d’Adobe ou votre représentant Adobe.

**Liens utiles**

* En savoir plus sur DMARC dans la section [Guide des bonnes pratiques de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"}
* Pour plus d’informations sur ces modifications, voir [Guide des bonnes pratiques de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html){target="_blank"}
* Lire [Annonce Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Lire [Yahoo ! annonce](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}
