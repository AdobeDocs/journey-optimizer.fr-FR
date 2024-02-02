---
solution: Journey Optimizer
product: journey optimizer
title: Enregistrement DMARC
description: Découvrir comment définir l’enregistrement DMARC dans Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: sous-domaine, domaine, courrier, dmarc, enregistrement
source-git-commit: cdc3e0ffaddb2ad83ad1703c1858773d09557859
workflow-type: tm+mt
source-wordcount: '1364'
ht-degree: 10%

---

# Enregistrement DMARC {#dmarc-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_record"
>title="Définir l’enregistrement DMARC"
>abstract="DMARC est une méthode d’authentification d’email qui permet aux propriétaires de domaine de protéger leur domaine d’une utilisation non autorisée et d’éviter les problèmes de délivrabilité avec les fournisseurs de messagerie.<br>Dans le cadre de l’application des bonnes pratiques du secteur, Google et Yahoo! Vous devez disposer d’un enregistrement DMARC pour tout domaine que vous utilisez pour leur envoyer des emails."

## Qu’est-ce que DMARC ? {#what-is-dmarc}

DMARC (Domain-based Message Authentication, Reporting, and Conformance) est une méthode d’authentification email qui permet aux propriétaires de domaine de protéger leur domaine d’une utilisation non autorisée. En offrant une politique claire aux fournisseurs de messagerie/FAI, elle permet d&#39;empêcher les acteurs malveillants d&#39;envoyer des emails prétendant provenir de votre domaine. La mise en oeuvre de DMARC réduit le risque que les emails légitimes soient marqués comme spam ou rejetés et améliore la délivrabilité de vos emails.

DMARC propose également des rapports sur les messages dont l’authentification échoue, ainsi qu’un contrôle sur la gestion des emails qui ne transmettent pas la validation DMARC. Selon l’implémentation [Stratégie DMARC](#dmarc-policies), ces emails peuvent être surveillés, mis en quarantaine ou rejetés. Ces fonctionnalités vous permettent de prendre des mesures pour atténuer les erreurs potentielles et les corriger.

<!--To help you prevent deliverability issues by allowing ISPs to authenticate your sending domains - while gaining visibility and control over mail that fail this authentication, [!DNL Journey Optimizer] will soon be supporting the DMARC technology directly in its administration interface.-->

Pour vous aider à éviter les problèmes de délivrabilité tout en prenant le contrôle des emails qui ne parviennent pas à s&#39;authentifier, [!DNL Journey Optimizer] prend désormais en charge la technologie DMARC directement dans son interface d’administration. [En savoir plus](#implement-dmarc)

### Comment DMARC fonctionne-t-il ? {#how-dmarc-works}

SPF et DKIM sont tous deux utilisés pour associer un e-mail à un domaine et permettent d’authentifier les e-mails. DMARC va plus loin et contribue à empêcher les usurpations en faisant correspondre le domaine vérifié par DKIM et SPF.

>[!NOTE]
>
>Dans Journey Optimizer, SPF et DKIM sont configurés pour vous.

Pour transmettre DMARC, un message doit transmettre SPF ou DKIM :

* SPF (Sender Policy Framework) permet de vérifier que le message électronique provient d’une source autorisée en comparant l’adresse IP du serveur d’envoi à une liste d’adresses IP autorisées pour le domaine.
* DKIM (DomainKeys Identified Mail) ajoute une signature numérique aux emails, permettant au destinataire de vérifier l&#39;intégrité et l&#39;authenticité du message.

Si l’une ou l’autre de ces authentifications échoue, DMARC échoue et l’email est envoyé conformément à la stratégie DMARC que vous avez sélectionnée.

<!--DMARC requires alignment between the 'From" and 'Return-Path' address.-->

### Stratégies DMARC {#dmarc-policies}

Si un email ne parvient pas à s’authentifier DMARC, vous pouvez décider quelle action sera appliquée à ce message. DMARC propose trois options de politique :

* Surveiller (p=none) : indique au fournisseur de messagerie/FAI d’appliquer la procédure normale au message.
* Quarantaine (p=quarantine) : indique au fournisseur de messagerie/FAI d’envoyer les e-mails qui ne passent pas DMARC vers le dossier spam ou de courrier indésirable des personnes destinataires.
* Rejeter (p=reject) : indique au fournisseur de messagerie/FAI de bloquer les e-mails qui ne passent pas DMARC, ce qui entraîne un rebond.

>[!NOTE]
>
>Découvrez comment définir la stratégie DMARC avec [!DNL Journey Optimizer] in [cette section](#set-up-dmarc).

## Mise à jour des exigences DMARC {#dmarc-update}

Dans le cadre de l’application des bonnes pratiques du secteur, Google et Yahoo! exigent que vous ayez une **Enregistrement DMARC** pour tout domaine que vous utilisez pour leur envoyer des emails. Cette nouvelle exigence s’applique à partir de **1er février 2024**.

En savoir plus sur Google et Yahoo!s requis dans [cette section](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html#dmarc){target="_blank"}.

>[!CAUTION]
>
>Ne pas se conformer à cette nouvelle exigence de Gmail et Yahoo ! est susceptible d’entraîner l’entrée ou le blocage des emails dans le dossier spam. [En savoir plus](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html#how-will-this-impact-me-as-a-marketer%3F){target="_blank"}.

Par conséquent, Adobe vous recommande vivement de prendre les mesures suivantes :

* Assurez-vous que la variable **Enregistrement DMARC** configurer pour **tous les sous-domaines que vous avez déjà délégués ;** pour Adobe dans [!DNL Journey Optimizer]. [Voici comment procéder.](#check-subdomains-for-dmarc)

* When **délégation de tout nouveau sous-domaine** pour Adobe, vous pouvez **configuration de DMARC** directly **dans le [!DNL Journey Optimizer] interface d’administration**. [Voici comment procéder.](#implement-dmarc)

## Implémentation de DMARC dans [!DNL Journey Optimizer] {#implement-dmarc}

La variable [!DNL Journey Optimizer] L’interface d’administration vous permet de configurer l’enregistrement DMARC pour tous les sous-domaines que vous avez déjà délégués ou que vous déléguez à Adobe. Les étapes détaillées sont décrites ci-dessous.

### Vérification des sous-domaines existants pour DMARC {#check-subdomains-for-dmarc}

Pour vous assurer que l’enregistrement DMARC est configuré pour tous les sous-domaines que vous avez délégués dans [!DNL Journey Optimizer], suivez les étapes ci-dessous.

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Sous-domaines]**, puis cliquez sur **[!UICONTROL Configurer le sous-domaine]**.

1. Pour chaque sous-domaine délégué, cochez la case **[!UICONTROL Enregistrement DMARC]** colonne . Si aucun enregistrement n’a été trouvé pour un sous-domaine donné, une alerte s’affiche.

   ![](assets/dmarc-record-alert.png)

   >[!CAUTION]
   >
   >Pour se conformer aux nouvelles exigences de Gmail et Yahoo! et éviter les problèmes de délivrabilité avec les principaux FAI, il est recommandé de configurer l’enregistrement DMARC pour tous les sous-domaines délégués. [En savoir plus](dmarc-record-update.md)

1. Sélectionnez un sous-domaine auquel aucun enregistrement DMARC n’est associé et renseignez les champs **[!UICONTROL Enregistrement DMARC]** en fonction des besoins de votre entreprise. Les étapes de remplissage des champs d’enregistrement DMARC sont présentées dans la section [cette section](#implement-dmarc).

1. Tenez compte des deux options ci-dessous :

   * Si vous modifiez un sous-domaine configuré avec [CNAME](delegate-subdomain.md#cname-subdomain-delegation), vous devez copier l’enregistrement DNS pour DMARC dans votre solution d’hébergement pour générer les enregistrements DNS correspondants.

     ![](assets/dmarc-record-edit-cname.png)

     Vérifiez que l’enregistrement DNS a été généré dans votre solution d’hébergement de domaine et cochez la case &quot;Je confirme...&quot;.

   * Si vous modifiez un sous-domaine [entièrement délégué](delegate-subdomain.md#full-subdomain-delegation) pour Adobe, il vous suffit de renseigner la variable **[!UICONTROL Enregistrement DMARC]** champs détaillés dans [cette section](#implement-dmarc). Aucune autre action n’est requise.

     ![](assets/dmarc-record-edit-full.png)

1. Enregistrez vos modifications.

### Configuration de DMARC pour les nouveaux sous-domaines {#set-up-dmarc}

Lors de la délégation de nouveaux sous-domaines à Adobe dans [!DNL Journey Optimizer], un enregistrement DMARC sera créé dans DNS pour votre domaine. Suivez les étapes ci-dessous pour mettre en oeuvre DMARC.

>[!CAUTION]
>
>Pour se conformer aux nouvelles exigences de Gmail et Yahoo! et éviter les problèmes de délivrabilité avec les principaux FAI, il est recommandé de configurer l’enregistrement DMARC pour tous les sous-domaines délégués. [En savoir plus](dmarc-record-update.md)

<!--If you fail to comply with the new requirement from Gmail and Yahoo! to have DMARC record for all sending domains, your emails are expected to land into the spam folder or to get blocked.-->

1. Configurez un nouveau sous-domaine. [Voici comment procéder.](delegate-subdomain.md)

1. Accédez au **[!UICONTROL Enregistrement DMARC]** .

   Si le sous-domaine comporte un enregistrement DMARC existant et s’il est récupéré par [!DNL Journey Optimizer], vous pouvez utiliser les mêmes valeurs que celles mises en surbrillance dans l’interface ou les modifier si nécessaire.

   ![](assets/dmarc-record-found.png)

   >[!NOTE]
   >
   >Si vous n’ajoutez aucune valeur, les valeurs par défaut préremplies seront utilisées.

1. Définissez l’action que le serveur du destinataire doit effectuer en cas d’échec de DMARC. Selon le [Stratégie DMARC](#dmarc-policies) sélectionnez l’une des trois options à appliquer :

   * **[!UICONTROL Aucun]** (valeur par défaut) : indique au destinataire de n’effectuer aucune action sur les messages qui ne parviennent pas à l’authentification DMARC, tout en envoyant des rapports d’email à l’expéditeur.
   * **[!UICONTROL Quarantaine]**: indique au serveur de messagerie de réception de mettre en quarantaine les emails qui ne parviennent pas à l’authentification DMARC. Cela signifie généralement de placer ces messages dans le dossier spam ou courrier indésirable du destinataire.
   * **[!UICONTROL Rejeter]**: indique au destinataire de refuser complètement (rebond) tout courrier électronique pour le domaine qui échoue à l’authentification. Lorsque cette stratégie est activée, seul le courrier électronique vérifié comme authentifié à 100 % par votre domaine aura une chance d’être placé dans une boîte de réception.

   >[!NOTE]
   >
   >Il est recommandé de déployer lentement la mise en oeuvre DMARC en réaffectant votre stratégie DMARC à partir de **Aucun**, à **Quarantaine**, à **Rejeter** en comprenant l’impact potentiel de DMARC.

1. Vous pouvez éventuellement ajouter une ou plusieurs adresses électroniques de votre choix pour indiquer où **Rapports DMARC** dans les emails qui [échec de l&#39;authentification](#how-dmarc-works) doit s’inscrire dans votre entreprise. Vous pouvez ajouter jusqu’à cinq adresses pour chaque rapport.

   >[!NOTE]
   >
   >Assurez-vous que votre contrôle contient une véritable boîte de réception (et non un Adobe) dans laquelle vous pouvez recevoir ces rapports.

   Il existe deux rapports différents générés par les FAI que les expéditeurs peuvent recevoir par le biais des balises RUA/RUF dans leur stratégie DMARC :

   * **Agrégat de rapports** (RUA) : elles ne contiennent aucune information d’identification personnelle qui pourrait être sensible au RGPD.
   * **Rapports d&#39;erreurs judiciaires** (RUF) : ils contiennent des adresses électroniques sensibles au RGPD. Avant d’utiliser , vérifiez en interne comment traiter les informations qui doivent être conformes au RGPD.

   >[!NOTE]
   >
   >Ces rapports hautement techniques fournissent un aperçu des courriers électroniques qui ont fait l’objet d’une tentative d’usurpation. Il est préférable de les digérer à l’aide d’un outil tiers.

1. Sélectionnez la variable **pourcentage applicable** de courriers électroniques pour DMARC.

   Ce pourcentage dépend de votre confiance dans votre infrastructure de messagerie et de la tolérance envers les faux positifs (emails légitimes marqués comme frauduleux). Il est courant que les organisations commencent par définir la stratégie DMARC sur **Aucun**, augmentez progressivement le pourcentage de la politique DMARC et surveillez de près l’impact sur la diffusion correcte des emails.

   >[!NOTE]
   >
   >Collaborez avec vos administrateurs de messagerie et votre équipe informatique pour augmenter progressivement le pourcentage lorsque vous gagnez en confiance dans vos pratiques d’authentification des emails.

   Une bonne pratique consiste à viser un taux de conformité DMARC élevé, idéalement proche de 100 %, afin de maximiser les avantages de sécurité tout en réduisant le risque de faux positifs.

1. Sélectionnez une **intervalle de rapports** entre 24 et 168 heures. Il permet aux propriétaires de domaine de recevoir des mises à jour régulières des résultats de l’authentification des emails et de prendre les mesures nécessaires pour améliorer la sécurité des emails.

   <!--The DMARC reporting interval is specified in the DMARC policy published in the DNS (Domain Name System) records for a domain. The reporting interval can be set to daily, weekly, or another specified frequency, depending on the domain owner's preferences.

    The default value (24 hours) is generally the email providers' expectation.-->


<!--

Setting up a DMARC record involves adding a DNS TXT record to your domain's DNS settings. This record specifies your DMARC policy, such as whether to quarantine or reject messages that fail authentication. Implementing DMARC is a proactive step towards enhancing email security and protecting both your organization and your recipients from email-based threats.

DMARC helps prevent malicious actors from sending emails that appear to come from your domain. By setting up DMARC, you can specify how email providers should handle messages that fail authentication checks, reducing the likelihood that phishing emails will reach recipients.

DMARC helps improve email deliverability by providing a clear policy for email providers to follow when encountering messages claiming to be from your domain. This can reduce the chances of legitimate emails being marked as spam or rejected.

DMARC helps protect against email spoofing, phishing, and other fraudulent activities.

It allows you to decide how a mailbox provider should handle emails that fail SPF and DKIM checks, providing a way to authenticate the sender's domain and prevent unauthorized use of the domain for malicious purposes.

## What are the benefits of DMARC? {#dmarc-benefits}

The key benefits or DMARC are as folllows:

* DMARC allows email receivers to easily identify the authentication of emails, which could potentially improve delivery.

* It offers reporting on which messages fail SPF and/or DKIM, enabling senders to gain visibility.

* This increased visibility allows for steps to be taken to mitigate further errors. It gives senders a degree of control over what happens with mail that does not pass either of these authentication methods.

-->







