---
solution: Journey Optimizer
product: journey optimizer
title: Respecter la nouvelle exigence DMARC
description: Découvrez pourquoi et quand vous devez définir l’enregistrement DMARC dans Journey Optimizer.
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: sous-domaine, domaine, courrier, dmarc, enregistrement
exl-id: 15b10a61-6ecd-4ffa-b1c2-21e862263f6d
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Respecter la nouvelle exigence DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="En savoir plus sur la mise à jour DMARC obligatoire"
>abstract="Dans le cadre de l’application des bonnes pratiques du secteur, Google et Yahoo exigent tous deux que vous disposiez d’un **enregistrement DMARC** pour tout domaine utilisé pour leur envoyer des e-mails, à compter du **1er février 2024**.<br>Par conséquent, vous devez vous assurer que les enregistrements DMARC sont configurés pour tous les sous-domaines que vous avez délégués à Adobe dans Journey Optimizer."

DMARC (Domain-based Message Authentication, Reporting, and Conformance, soit Authentification, création de rapports et conformité des messages basés sur le domaine) est une méthode d’authentification d’e-mail qui permet aux personnes propriétaires de domaine de protéger leur domaine d’une utilisation non autorisée. En fournissant une politique claire aux fournisseurs de messagerie/FAI, elle permet d’empêcher des entités malveillantes d’envoyer des e-mails prétendant provenir de votre domaine. L’implémentation de DMARC réduit le risque que les e-mails légitimes soient marqués comme spam ou rejetés et améliore la délivrabilité de vos e-mails.

Dans le cadre de l’application des bonnes pratiques du secteur, Google et Yahoo! exigent tous deux que vous disposiez d’un **enregistrement DMARC** pour tout domaine utilisé pour leur envoyer des e-mails. Cette nouvelle exigence s’applique dès le **1er février 2024**.

>[!CAUTION]
>
>Ne pas se conformer à cette nouvelle exigence de Gmail et Yahoo! est susceptible d’entraîner la réception des e-mails dans le dossier de spam ou leur blocage.

Par conséquent, Adobe vous recommande vivement de vous assurer que les enregistrements DMARC sont configurés pour tous les sous-domaines que vous avez délégués à Adobe dans [!DNL Journey Optimizer]. Suivez les étapes ci-dessous qui s’appliquent à votre cas :

* Si vous avez [entièrement délégué](delegate-subdomain.md#set-up-subdomain) vos sous-domaines d’envoi à Adobe, suivez l’une des deux options ci-dessous :

   * Configurez DMARC sur le domaine parent de vos sous-domaines délégués **dans votre solution d’hébergement**.
or
   * Configurez DMARC sur vos sous-domaines délégués **dans l’interface utilisateur de configuration[!DNL Journey Optimizer]**, et ce sans travail supplémentaire à effectuer sur votre solution d’hébergement. [Voici comment procéder](dmarc-record.md#implement-dmarc)

* Si vous avez configuré vos sous-domaines d’envoi avec [CNAME](delegate-subdomain.md#cname-subdomain-setup), suivez l’une des options ci-dessous :

   * Configurez DMARC sur vos sous-domaines ou sur le domaine parent de vos sous-domaines **dans votre solution d’hébergement**.
or
   * Configurez DMARC sur vos sous-domaines délégués **dans l’interface utilisateur de configuration[!DNL Journey Optimizer]**. [Voici comment procéder](dmarc-record.md#implement-dmarc)

  Toutefois, la configuration CNAME nécessite également une entrée supplémentaire dans votre solution d’hébergement. Par conséquent, assurez-vous de vous coordonner avec votre service informatique afin qu’il puisse effectuer la mise à jour détaillée dans [cette section](dmarc-record.md#implement-dmarc).

<!--The most recent timelines shared by Google and Yahoo! are as follows:

* Google:

    * **February 2024** – Temporary bounces designed to provide warning of non-compliance will begin. Emails will still be delivered as normal after a short delay if you are not yet in compliance. If you are fully in compliance there will be no temporary bounces and you will not be affected.

    * **April 2024** – Blocks will begin for senders who are not in compliance with DMARC requirement. Only a portion of non-compliant email will be blocked at first, with the percentage blocked increasing over time.

    * **June 1st, 2024** – Any sender not in full compliance will experience blocking.

* Yahoo! has not provided exact dates, but has said "the rollout of enforcement will begin in February 2024. Enforcement will be gradually rolled out".
-->

>[!NOTE]
>
>Si vous avez des questions ou avez besoin d’aide, contactez votre consultant ou consultante en délivrabilité Adobe, ou encore votre représentant ou représentante Adobe.

**Liens utiles**

* Découvrez DMARC dans le [Guide des bonnes pratiques en matière de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=fr#about){target="_blank"}.
* Consultez l’[annonce Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}.
* Consultez l’[annonce Yahoo! ](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}.

<!--Find more guidance about these changes in the [Deliverability Best Practice Guide]-->
