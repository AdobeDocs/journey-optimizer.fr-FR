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
source-git-commit: 49cb9734d66dc1aa2a3531c71a687aac00834d82
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Enregistrement DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Définition de l’enregistrement DMARC"
>abstract="Définir l’enregistrement DMARC pour éviter les problèmes de délivrabilité avec les FAI"

>[!CAUTION]
>
>Suite aux récentes annonces Gmail et Yahoo pour les expéditeurs en masse, Journey Optimizer prend désormais en charge la technologie d’authentification DMARC. //Vous devez mettre à jour tous les sous-domaines que vous avez déjà créés sur votre instance pour inclure la prise en charge DMARC.//

Il est important de le faire d&#39;ici le 1er février Doc sera bientôt disponible.

Démarrage le

Vous disposez de deux options :

* Effectuez-le désormais par vous-même : configurez-le avec votre service informatique, lorsque vous le souhaitez.

* Effectuez-le dans AJO - mais dans ce cas, vous devez attendre le 30 janvier.

   * Délégation complète : vous pouvez le faire le 30 janvier (version AJO)

   * Le CNAME le planifie avec votre service informatique, ce qui n’est pas chronophage, mais vous devez le planifier.

Dans le cadre de leur application des bonnes pratiques du secteur, Google et Yahoo exigeront tous deux que vous disposiez d’un enregistrement DMARC pour tout domaine que vous utilisez pour leur envoyer des emails. Cette nouvelle exigence commence à **1er février 2024**.

En savoir plus sur les exigences de Google et de Yahoo pour l’enregistrement DMARC dans [cette section](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

En savoir plus sur les modifications annoncées dans Google et Yahoo sur [cette page](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

DMARC, qui signifie **Authentification, création de rapports et conformité des messages basés sur le domaine**, est un protocole d’authentification d’email qui permet de se protéger contre l’usurpation, le phishing et d’autres activités frauduleuses.

* Authentification des emails :

   * SPF (Sender Policy Framework) : DMARC utilise SPF pour authentifier l’identité du serveur de messagerie. SPF aide à vérifier que le message électronique provient d’une source autorisée en comparant l’adresse IP du serveur d’envoi à une liste d’adresses IP autorisées pour le domaine.
   * DKIM (DomainKeys Identified Mail) : DMARC utilise également DKIM pour ajouter une signature numérique aux emails, permettant au destinataire de vérifier l&#39;intégrité et l&#39;authenticité du message.

* DMARC permet d’empêcher les acteurs malveillants d’envoyer des emails qui semblent provenir de votre domaine. En configurant DMARC, vous pouvez spécifier comment les fournisseurs de messagerie doivent gérer les messages qui ne parviennent pas à s’authentifier, ce qui réduit la probabilité que les emails de phishing parviennent aux destinataires.

* DMARC contribue à améliorer la délivrabilité des emails en fournissant une politique claire que les fournisseurs de messagerie peuvent suivre lorsqu’ils rencontrent des messages prétendant provenir de votre domaine. Cela peut réduire les risques que les emails légitimes soient marqués comme spam ou rejetés.

* En implémentant DMARC, vous pouvez protéger la réputation de votre marque en vous assurant que les tiers non autorisés ne peuvent pas abuser de votre domaine pour le phishing ou d’autres activités malveillantes. Ceci est particulièrement important pour les entreprises et les organisations qui dépendent de la communication par e-mail avec leurs clients et partenaires.

La configuration d’un enregistrement DMARC implique l’ajout d’un enregistrement TXT DNS aux paramètres DNS de votre domaine. Cet enregistrement spécifie votre stratégie DMARC, par exemple s’il faut mettre en quarantaine ou rejeter les messages qui ne parviennent pas à s’authentifier. La mise en oeuvre de DMARC est une étape proactive pour améliorer la sécurité des emails et protéger votre organisation et vos destinataires des menaces basées sur les emails.

[En savoir plus sur DMARC dans le guide des bonnes pratiques de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} pour mieux comprendre l’impact de DMARC sur la délivrabilité des emails.

Si vous n&#39;ajoutez pas DMARC, vous serez mis en quarantaine (au moins).

assurez-vous que vous disposez d’une véritable boîte de réception où vous pouvez recevoir votre contrôle - vous gérez cette boîte de réception (ne doit pas être une boîte de réception d’Adobe).

La recommandation est de 24 car, en règle générale, si elle est inférieure, évaluez votre capacité/vérifiez votre GPT > chat

Google et Yahoo, et probablement tous les autres principaux FAI

pour CNAME dans le flux d’édition, vous devez de nouveau télécharger le fichier CSV (ce qui n’est pas entièrement délégué).

nouvel enregistrement DMARC

Dans RN > Tout placer en premier Tous les sous-domaines doivent être mis à jour avec la prise en charge DMARC



