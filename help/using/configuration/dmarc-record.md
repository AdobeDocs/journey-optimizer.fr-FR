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
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '905'
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

Par conséquent, Adobe vous recommande vivement de vous assurer que les enregistrements DMARC sont configurés pour tous les sous-domaines que vous avez délégués à l’Adobe dans [!DNL Journey Optimizer]. Suivez les étapes ci-dessous qui s’appliquent à votre cas :

* Si vous avez [entièrement délégué](delegate-subdomain.md#full-subdomain-delegation) vos sous-domaines d’envoi à Adobe, suivez l’une des deux options ci-dessous :

   * Configuration de DMARC sur le domaine parent de vos sous-domaines délégués **dans votre solution d’hébergement**.

   * Configuration de DMARC sur vos sous-domaines délégués **à l’aide de la fonction à venir dans la fonction [!DNL Journey Optimizer] Interface utilisateur d’administration** - sans travail supplémentaire sur votre solution d’hébergement.

* Si vous avez configuré [Délégation CNAME](delegate-subdomain.md#cname-subdomain-delegation) pour vos sous-domaines d’envoi, suivez l’une des deux options ci-dessous :

   * Configurez DMARC sur vos sous-domaines ou sur le domaine parent de vos sous-domaines. **dans votre solution d’hébergement**.

   * Configuration de DMARC sur vos sous-domaines délégués **à l’aide de la fonction à venir dans la fonction [!DNL Journey Optimizer] Interface utilisateur d’administration**. Cependant, il nécessite également une entrée dans votre solution d’hébergement. Par conséquent, assurez-vous de vous coordonner avec votre service informatique afin qu’il puisse effectuer la mise à jour dès que la variable [!DNL Journey Optimizer] Cette fonctionnalité est disponible (le 30 janvier). <!--and be ready on February 1st, 2024-->

**Plus d’informations sur [!DNL Journey Optimizer] La fonctionnalité DMARC à venir sera bientôt disponible.**

>[!NOTE]
>
>En savoir plus sur l’implémentation de DMARC dans [Guide des bonnes pratiques de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} pour mieux comprendre l’impact sur la délivrabilité des emails.

## Qu’est-ce que DMARC ?

DMARC, qui signifie **Authentification, création de rapports et conformité des messages basés sur le domaine**, est une méthode/un protocole d’authentification d’email qui permet aux propriétaires de domaine de protéger leur domaine d’une utilisation non autorisée.

En proposant un moyen d’authentifier le domaine de l’expéditeur, il permet d’empêcher les acteurs malveillants d’envoyer des emails qui semblent provenir de votre domaine.

DMARC fournit également des commentaires sur l’état d’authentification des emails et permet aux expéditeurs de contrôler ce qui arrive aux emails qui ne parviennent pas à s’authentifier. Cela inclut des options de surveillance, de mise en quarantaine ou de rejet du courrier, selon la politique DMARC mise en oeuvre.

<!--Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.-->

DMARC propose trois options de stratégie :

* Monitor (p=none) : indique au fournisseur de messagerie/FAI de faire tout ce qu&#39;il ferait normalement au message.
* Quarantaine (p=quarantaine) : indique au fournisseur de messagerie ou à l’ISP de diffuser du courrier électronique qui ne transmet pas DMARC au dossier spam ou courrier indésirable du destinataire.
* Rejeter (p=rejeter) : indique au fournisseur de messagerie/FAI de bloquer les emails qui ne transmettent pas DMARC, ce qui entraîne un rebond.

## Comment fonctionne DMARC ?

SPF et DKIM sont tous deux utilisés pour associer un email à un domaine et travailler ensemble pour authentifier un email. DMARC va plus loin et contribue à empêcher les usurpations en faisant correspondre le domaine vérifié par DKIM et SPF. Pour transmettre DMARC, un message doit transmettre SPF ou DKIM. Si l’authentification de ces deux erreurs échoue, DMARC échoue et l’email est envoyé conformément à la stratégie DMARC que vous avez sélectionnée.

* SPF (Sender Policy Framework) : DMARC utilise SPF pour authentifier l’identité du serveur de messagerie. SPF aide à vérifier que le message électronique provient d’une source autorisée en comparant l’adresse IP du serveur d’envoi à une liste d’adresses IP autorisées pour le domaine.
* DKIM (DomainKeys Identified Mail) : DMARC utilise également DKIM pour ajouter une signature numérique aux emails, permettant au destinataire de vérifier l&#39;intégrité et l&#39;authenticité du message.

>[!NOTE]
>
>DMARC nécessite un alignement entre l’adresse &quot;De&quot; et l’adresse &quot;Chemin retour&quot;.


<!--

* DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

* DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

-->


## Implémenter DMARC {#implement-dmarc}

Pour mettre en oeuvre DMARC, procédez comme suit qui s’applique à votre cas.

* Si vous n&#39;ajoutez pas DMARC, vous serez mis en quarantaine (au moins).

### Sous-domaines entièrement délégués

Définissez l’action que le serveur du destinataire doit effectuer en cas d’échec de DMARC.

DMARC propose trois options de stratégie :

* Monitor (p=none) : indique au fournisseur de messagerie/FAI de faire tout ce qu&#39;il ferait normalement au message. Il s’agit de la valeur par défaut.
* Quarantaine (p=quarantaine) : indique au fournisseur de messagerie ou à l’ISP de diffuser du courrier électronique qui ne transmet pas DMARC au dossier spam ou courrier indésirable du destinataire.
* Rejeter (p=rejeter) : indique au fournisseur de messagerie/FAI de bloquer les emails qui ne transmettent pas DMARC, ce qui entraîne un rebond.

Emails pour recevoir des rapports DMARC agrégés et des rapports d&#39;échec DMARC médico-légal : vous pouvez ajouter jusqu&#39;à 5 adresses.

* Assurez-vous que vous disposez d’une véritable boîte de réception où vous pouvez recevoir votre contrôle : vous gérez cette boîte de réception (ne doit pas être une boîte de réception d’Adobe).

Pourcentage applicable des emails à appliquer DMARC :

Intervalle de création de rapports : la recommandation est de 24, car c’est généralement ce que les FAI ont.
si vous en avez moins, évaluez votre capacité / vérifiez votre GPT > chat

Si un enregistrement DMARC est détecté, vous pouvez copier-coller les mêmes valeurs que répertoriées ou les modifier, si nécessaire.

Si vous ne mettez rien, les valeurs par défaut seront utilisées.

### Sous-domaines délégués à l’aide de CNAME

pour CNAME dans le flux d’édition, vous devez télécharger à nouveau le fichier CSV (et non pour délégué entièrement).





