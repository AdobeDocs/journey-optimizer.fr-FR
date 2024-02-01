---
solution: Journey Optimizer
product: journey optimizer
title: Respecter les nouvelles exigences DMARC
description: Découvrez pourquoi et quand vous devez définir l’enregistrement DMARC dans Journey Optimizer.
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: sous-domaine, domaine, courrier, dmarc, enregistrement
source-git-commit: c5da9e9cfd5c03d7c6898e492582e5cc3e466447
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 41%

---

# Respecter les nouvelles exigences DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="En savoir plus sur la mise à jour DMARC obligatoire"
>abstract="Dans le cadre de l’application des bonnes pratiques du secteur, Google et Yahoo exigent tous deux que vous disposiez d’un **Enregistrement DMARC** pour tout domaine que vous utilisez pour leur envoyer des emails, en commençant par **1er février 2024**.<br>Par conséquent, vous devez vous assurer que les enregistrements DMARC sont configurés pour tous les sous-domaines que vous avez délégués à Adobe dans Journey Optimizer."

DMARC (Domain-based Message Authentication, Reporting, and Conformance) est une méthode d’authentification email qui permet aux propriétaires de domaine de protéger leur domaine d’une utilisation non autorisée. En offrant une politique claire aux fournisseurs de messagerie/FAI, elle permet d&#39;empêcher les acteurs malveillants d&#39;envoyer des emails prétendant provenir de votre domaine. La mise en oeuvre de DMARC réduit le risque que les emails légitimes soient marqués comme spam ou rejetés et améliore la délivrabilité de vos emails.


Dans le cadre de l’application des bonnes pratiques du secteur, Google et Yahoo! exigent tous deux qu’une **Enregistrement DMARC** pour tout domaine que vous utilisez pour leur envoyer des emails. Cette nouvelle exigence s’applique à partir de **1er février 2024**. [En savoir plus](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html#dmarc){target="_blank"}.

>[!CAUTION]
>
>Ne pas se conformer à cette nouvelle exigence de Gmail et Yahoo ! est susceptible d’entraîner l’entrée ou le blocage des emails dans le dossier spam.

Par conséquent, Adobe vous recommande vivement de vous assurer que les enregistrements DMARC sont configurés pour tous les sous-domaines que vous avez délégués à Adobe dans [!DNL Journey Optimizer]. Suivez les étapes ci-dessous qui s’appliquent à votre cas :

* Si vous avez [entièrement délégué](delegate-subdomain.md#full-subdomain-delegation) vos sous-domaines d’envoi à Adobe, procédez comme suit :

   * Configuration de DMARC sur le domaine parent de vos sous-domaines délégués **dans votre solution d’hébergement**.
or
   * Configuration de DMARC sur vos sous-domaines délégués **dans le[!DNL Journey Optimizer]** Configuration de l’interface utilisateur - sans travail supplémentaire sur votre solution d’hébergement. [Voici comment procéder.](dmarc-record.md#implement-dmarc)

* Si vous avez configuré vos sous-domaines d’envoi avec [CNAME](delegate-subdomain.md#cname-subdomain-delegation), suivez l’une des options ci-dessous :

   * Configurez DMARC sur vos sous-domaines ou sur le domaine parent de vos sous-domaines. **dans votre solution d’hébergement**.
or
   * Configuration de DMARC sur vos sous-domaines délégués **dans le[!DNL Journey Optimizer]** de l’interface utilisateur de configuration. [Voici comment procéder.](dmarc-record.md#implement-dmarc)

  Toutefois, avec la délégation CNAME, elle nécessite également une entrée dans votre solution d’hébergement. Par conséquent, assurez-vous de vous coordonner avec votre service informatique afin qu’il puisse effectuer la mise à jour détaillée dans la section [cette section](dmarc-record.md#implement-dmarc).


Les dernières chronologies partagées par Google et Yahoo sont les suivantes :

* Google :

   * **Février 2024** : les rebonds temporaires destinés à avertir de la non-conformité seront mis en place. Si vous n’êtes pas encore en conformité, les e-mails seront toujours livrés normalement après un court délai. Si vous êtes en totale conformité, il n’y aura pas de rebond temporaire, ni aucune incidence pour vous.

   * **Avril 2024** : les blocages commenceront pour les expéditeurs et expéditrices qui ne sont pas en conformité avec DMARC. Seule une partie des e-mails non conformes sera bloquée dans un premier temps, le pourcentage de blocage augmentant au fil du temps.

   * **1er juin 2024** : l’ensemble des expéditeurs et expéditrices qui ne sont pas en conformité totale seront bloqués.

* Yahoo n’a pas fourni de dates exactes, mais a déclaré que « la règle sera appliquée à partir de février 2024. Son application se fera progressivement ».

>[!NOTE]
>
>Si vous avez des questions ou avez besoin d’aide, contactez votre consultant ou consultante en délivrabilité Adobe, ou encore votre représentant ou représentante Adobe.

**Liens utiles**

* En savoir plus sur DMARC dans la section [Guide des bonnes pratiques de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=fr#about){target="_blank"}
* Pour plus d’informations sur ces modifications, voir [Guide des bonnes pratiques de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html){target="_blank"}
* Lire [Annonce Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Lire [Yahoo ! annonce](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}
