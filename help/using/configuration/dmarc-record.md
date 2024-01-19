---
solution: Journey Optimizer
product: journey optimizer
title: Enregistrement DMARC
description: Découvrez comment définir l’enregistrement DMARC dans Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: sous-domaine, domaine, courrier, dmarc, enregistrement
source-git-commit: f9d3234a64ad659660c2d2c4ad24ab5c240cb857
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 1%

---

# Enregistrement DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Définition de l’enregistrement DMARC"
>abstract="Définissez l’enregistrement DMARC pour éviter des problèmes de délivrabilité avec les FAI. Dans le cadre de leur application des bonnes pratiques du secteur, Google et Yahoo exigent tous deux que vous disposiez d’un enregistrement DMARC pour tout domaine que vous utilisez pour leur envoyer des emails."

>[!CAUTION]
>
>Suite aux récentes annonces Gmail et Yahoo pour les expéditeurs en masse, Journey Optimizer prend désormais en charge la technologie d’authentification DMARC.

<!--TO ADD TO AJO HOME PAGE (first tab)

>[!TAB Mandatory DMARC update]

As part of their enforcing industry best practices, Google and Yahoo will both be requiring that you have a DMARC record for any domain you use to send email to them, starting on **February 1st, 2024**. Make sure that you have DMARC record set up for all the subdomains that you have delegated to Adobe in Journey Optimizer.

[![image](using/assets/do-not-localize/learn-more-button.svg)](using/configuration/dmarc-record-update.md)
-->

Dans le cadre de l’application des bonnes pratiques du secteur, Google et Yahoo exigent tous deux que vous disposiez d’un **Enregistrement DMARC** pour tout domaine que vous utilisez pour leur envoyer des emails. Cette nouvelle exigence commence à **1er février 2024**.

En savoir plus sur Google et les exigences de Yahoo dans [cette section](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Si vous ne respectez pas cette nouvelle exigence de Gmail et Yahoo, les emails seront probablement envoyés dans le dossier spam ou bloqués.

Par conséquent, Adobe vous recommande vivement de vous assurer que les enregistrements DMARC sont configurés pour tous les sous-domaines que vous avez délégués à l’Adobe dans [!DNL Journey Optimizer]. Suivez l’une des deux options ci-dessous :

* Configurez DMARC sur vos sous-domaines ou sur le domaine parent de vos sous-domaines, **dans votre solution d’hébergement**.

* Configuration de DMARC sur vos sous-domaines délégués **à l’aide de la nouvelle fonctionnalité de la fonction [!DNL Journey Optimizer] Interface utilisateur d’administration** - sans travail supplémentaire sur votre solution d’hébergement. [En savoir plus](#implement-dmarc)

  >[!CAUTION]
  >
  >Si vous avez configuré [Délégation CNAME](delegate-subdomain.md#cname-subdomain-delegation) pour vos sous-domaines d’envoi, une entrée dans votre solution d’hébergement sera également nécessaire. Assurez-vous de vous coordonner avec votre service informatique afin qu’il puisse effectuer la mise à jour dès que la variable [!DNL Journey Optimizer] Cette fonctionnalité est disponible (le 30 janvier 2024). <!--and be ready on February 1st, 2024-->

>[!NOTE]
>
>En savoir plus sur l’implémentation de DMARC dans [Guide des bonnes pratiques de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} pour mieux comprendre l’impact sur la délivrabilité des emails.

## Qu’est-ce que DMARC ?

DMARC, qui signifie **Authentification, création de rapports et conformité des messages basés sur le domaine**, est un protocole d’authentification d’email qui permet de se protéger contre l’usurpation, le phishing et d’autres activités frauduleuses.

* Authentification des emails :

   * SPF (Sender Policy Framework) : DMARC utilise SPF pour authentifier l’identité du serveur de messagerie. SPF aide à vérifier que le message électronique provient d’une source autorisée en comparant l’adresse IP du serveur d’envoi à une liste d’adresses IP autorisées pour le domaine.
   * DKIM (DomainKeys Identified Mail) : DMARC utilise également DKIM pour ajouter une signature numérique aux emails, permettant au destinataire de vérifier l&#39;intégrité et l&#39;authenticité du message.

* DMARC permet d’empêcher les acteurs malveillants d’envoyer des emails qui semblent provenir de votre domaine. En configurant DMARC, vous pouvez spécifier comment les fournisseurs de messagerie doivent gérer les messages qui ne parviennent pas à s’authentifier, ce qui réduit la probabilité que les emails de phishing parviennent aux destinataires.

* DMARC contribue à améliorer la délivrabilité des emails en fournissant une politique claire que les fournisseurs de messagerie peuvent suivre lorsqu’ils rencontrent des messages prétendant provenir de votre domaine. Cela peut réduire les risques que les emails légitimes soient marqués comme spam ou rejetés.

* En implémentant DMARC, vous pouvez protéger la réputation de votre marque en vous assurant que les tiers non autorisés ne peuvent pas abuser de votre domaine pour le phishing ou d’autres activités malveillantes. Ceci est particulièrement important pour les entreprises et les organisations qui dépendent de la communication par e-mail avec leurs clients et partenaires.

La configuration d’un enregistrement DMARC implique l’ajout d’un enregistrement TXT DNS aux paramètres DNS de votre domaine. Cet enregistrement spécifie votre stratégie DMARC, par exemple s’il faut mettre en quarantaine ou rejeter les messages qui ne parviennent pas à s’authentifier. La mise en oeuvre de DMARC est une étape proactive pour améliorer la sécurité des emails et protéger votre organisation et vos destinataires des menaces basées sur les emails.

## Implémenter DMARC {#implement-dmarc}

* Si vous n&#39;ajoutez pas DMARC, vous serez mis en quarantaine (au moins).

* Assurez-vous que vous disposez d’une véritable boîte de réception où vous pouvez recevoir votre contrôle : vous gérez cette boîte de réception (ne doit pas être une boîte de réception d’Adobe).

La recommandation est 24, car c&#39;est généralement ce que les FAI ont.
si vous en avez moins, évaluez votre capacité / vérifiez votre GPT > chat

Si un enregistrement DMARC est détecté, vous pouvez copier-coller les mêmes valeurs que répertoriées ou les modifier, si nécessaire.

Si vous ne mettez rien, les valeurs par défaut seront utilisées.

### Sous-domaines entièrement délégués

### Sous-domaines délégués à l’aide de CNAME

pour CNAME dans le flux d’édition, vous devez télécharger à nouveau le fichier CSV (et non pour délégué entièrement).





