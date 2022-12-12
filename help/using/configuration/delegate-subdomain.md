---
solution: Journey Optimizer
product: journey optimizer
title: Délégation d’un sous-domaine
description: Découvrez comment déléguer vos sous-domaines.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: 61c90f39fa2bddb384e5581e3935c43d4691c355
workflow-type: tm+mt
source-wordcount: '1704'
ht-degree: 0%

---

# Délégation d’un sous-domaine {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="Délégation de sous-domaine"
>abstract="Journey Optimizer vous permet de déléguer vos sous-domaines à Adobe. Vous pouvez entièrement déléguer un sous-domaine à Adobe, ce qui est la méthode recommandée. Vous pouvez également créer un sous-domaine à l’aide de CNAME pour pointer vers des enregistrements spécifiques à Adobe, mais cette approche nécessite que vous gardiez et gériez les enregistrements DNS vous-même."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation.html#subdomain-delegation-methods" text="Méthodes de configuration de sous-domaine"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="Délégation de sous-domaine"
>abstract="Pour commencer à envoyer des emails, vous allez déléguer votre sous-domaine à Adobe. Une fois cette opération terminée, les enregistrements DNS, les boîtes de réception, l’expéditeur, les adresses de réponse et de rebond seront configurés pour vous."

La délégation de nom de domaine est une méthode qui permet au propriétaire d’un nom de domaine (techniquement : une zone DNS) pour déléguer une sous-section (techniquement : une zone DNS en dessous, qui peut être appelée sous-zone) vers une autre entité. En tant que client, si vous gérez la zone &quot;example.com&quot;, vous pouvez déléguer la sous-zone &quot;marketing.example.com&quot; à Adobe. En savoir plus sur [délégation de sous-domaine](about-subdomain-delegation.md)

>[!NOTE]
>
>Par défaut, [!DNL Journey Optimizer] le contrat de licence vous permet de déléguer jusqu’à 10 sous-domaines. Contactez votre contact Adobe si vous souhaitez augmenter cette limite.

Vous pouvez déléguer entièrement un sous-domaine ou créer un sous-domaine à l’aide de CNAME pour pointer vers des enregistrements spécifiques à Adobe.

>[!CAUTION]
>
>La délégation complète de sous-domaine est la méthode recommandée. En savoir plus sur les différences entre les deux [Méthodes de configuration de sous-domaine](about-subdomain-delegation.md#subdomain-delegation-methods).
>
>La configuration de sous-domaine est commune à tous les environnements. Par conséquent, toute modification apportée à un sous-domaine aura également un impact sur les environnements de test de production.

## Délégation complète de sous-domaine {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="Générer les enregistrements DNS correspondants"
>abstract="Pour déléguer entièrement un nouveau sous-domaine à Adobe, vous devez copier-coller les informations du serveur de noms Adobe affichées dans l’interface de Journey Optimizer dans votre solution d’hébergement de domaine afin de générer les enregistrements DNS correspondants. Pour déléguer un sous-domaine à l’aide de CNAME, vous devez également copier-coller l’enregistrement de validation de l’URL CDN SSL. Une fois les vérifications effectuées, le sous-domaine est prêt à être utilisé pour diffuser les messages."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/delegate-subdomain.html#cname-subdomain-delegation" text="Délégation de sous-domaine CNAME"

[!DNL Journey Optimizer] vous permet de déléguer entièrement vos sous-domaines à Adobe directement à partir de l’interface du produit. Ce faisant, Adobe sera en mesure de diffuser des messages en tant que service géré en contrôlant et en gérant tous les aspects du DNS nécessaires à la diffusion, au rendu et au suivi des campagnes email.

Vous pouvez vous fier à Adobe pour gérer l’infrastructure DNS nécessaire pour répondre aux exigences de délivrabilité standard de votre secteur pour vos domaines d’envoi de marketing par e-mail, tout en continuant à gérer et à contrôler le DNS de vos domaines d’email internes.

Pour déléguer entièrement un nouveau sous-domaine à Adobe, procédez comme suit :

1. Accédez au **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Subdomains]** , puis cliquez sur **[!UICONTROL Set up subdomain]**.

   ![](assets/subdomain-delegate.png)

1. Sélectionner **[!UICONTROL Fully delegated]** de la **[!UICONTROL Set up method]** .

   ![](assets/subdomain-method-full.png)

1. Indiquez le nom du sous-domaine à déléguer.

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >La délégation d’un sous-domaine non valide à Adobe n’est pas autorisée. Veillez à saisir un sous-domaine valide détenu par votre entreprise, tel que marketing.yourcompany.com.
   >
   >Notez que les sous-domaines à plusieurs niveaux tels que email.marketing.yourcompany.com ne sont actuellement pas pris en charge.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. La liste des enregistrements à placer dans vos serveurs DNS s&#39;affiche. Copiez ces enregistrements un par un ou en téléchargeant un fichier CSV, puis accédez à votre solution d’hébergement de domaine pour générer les enregistrements DNS correspondants.

1. Assurez-vous que tous les enregistrements DNS ont été générés dans votre solution d’hébergement de domaine. Si tout est configuré correctement, cochez la case &quot;Je confirme...&quot;, puis cliquez sur **[!UICONTROL Submit]**.

   ![](assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Vous pouvez créer des enregistrements et envoyer ultérieurement la configuration du sous-domaine à l’aide de la variable **[!UICONTROL Save as draft]** bouton . Vous pourrez ensuite reprendre la délégation de sous-domaine en l’ouvrant à partir de la liste de sous-domaines.

1. Une fois la délégation de sous-domaine complète envoyée, le sous-domaine s’affiche dans la liste avec la variable **[!UICONTROL Processing]** statut. Pour plus d’informations sur les statuts des sous-domaines, reportez-vous à la section [cette section](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-processing.png)

   Avant de pouvoir utiliser ce sous-domaine pour envoyer des messages, vous devez attendre qu’Adobe effectue les vérifications requises, qui peuvent prendre jusqu’à 3 heures. En savoir plus dans [cette section](#subdomain-validation).

   >[!NOTE]
   >
   >Tous les enregistrements manquants, c’est-à-dire les enregistrements non encore créés sur votre solution d’hébergement, seront répertoriés.

1. Une fois les vérifications effectuées, le sous-domaine reçoit la valeur **[!UICONTROL Success]** statut. Il est prêt à être utilisé pour diffuser des messages.

   >[!NOTE]
   >
   >Le sous-domaine sera marqué comme **[!UICONTROL Failed]** si vous ne créez pas l’enregistrement de validation sur votre solution d’hébergement.

Une fois qu’un sous-domaine est délégué à Adobe dans [!DNL Journey Optimizer], un enregistrement PTR est automatiquement créé et associé à ce sous-domaine. [En savoir plus](ptr-records.md)

>[!CAUTION]
>
>L’exécution parallèle de sous-domaines n’est actuellement pas prise en charge dans [!DNL Journey Optimizer]. Si vous tentez d’envoyer un sous-domaine pour délégation lorsqu’un autre possède la propriété **[!UICONTROL Processing]** , vous obtiendrez un message d’erreur.

## Délégation de sous-domaine CNAME {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="Générer les enregistrements DNS et de validation correspondants"
>abstract="Pour déléguer un sous-domaine à l’aide de CNAME, vous devez copier-coller les informations du serveur de noms Adobe et l’enregistrement de validation de l’URL CDN SSL affiché dans l’interface de Journey Optimizer sur votre plateforme d’hébergement. Une fois les vérifications effectuées, le sous-domaine est prêt à être utilisé pour diffuser les messages."

Si vous disposez de stratégies de restriction spécifiques à un domaine et que vous souhaitez qu’Adobe n’ait qu’un contrôle partiel sur le DNS, vous pouvez choisir d’exécuter toutes les activités liées au DNS de votre côté.

La délégation de sous-domaine CNAME vous permet de créer un sous-domaine et d’utiliser des CNAME pour pointer vers des enregistrements spécifiques à Adobe. Grâce à cette configuration, vous partagez avec Adobe la responsabilité de la maintenance du DNS afin de configurer un environnement pour l’envoi, le rendu et le suivi des emails.

>[!CAUTION]
>
>La méthode CNAME est recommandée si les stratégies de votre entreprise limitent la méthode de délégation de sous-domaine complète. Cette approche nécessite que vous gardiez et gériez vos enregistrements DNS vous-même. Adobe ne pourra pas vous aider à modifier, gérer ou gérer le DNS d’un sous-domaine configuré à l’aide de la méthode CNAME.

➡️ [Découvrez comment créer un sous-domaine à l’aide de CNAME pour pointer vers des enregistrements spécifiques à Adobe dans cette vidéo](#video)

Pour déléguer un sous-domaine à l’aide de CNAME, procédez comme suit :

1. Accédez au **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Subdomains]** , puis cliquez sur **[!UICONTROL Set up subdomain]**.

1. Sélectionnez la **[!UICONTROL CNAME set up]** .

   ![](assets/subdomain-method-cname.png)

1. Indiquez le nom du sous-domaine à déléguer.

   >[!CAUTION]
   >
   >La délégation d’un sous-domaine non valide à Adobe n’est pas autorisée. Veillez à saisir un sous-domaine valide détenu par votre entreprise, tel que marketing.yourcompany.com.
   >
   >Notez que les sous-domaines à plusieurs niveaux tels que email.marketing.yourcompany.com ne sont actuellement pas pris en charge.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. La liste des enregistrements à placer dans vos serveurs DNS s&#39;affiche. Copiez ces enregistrements un par un ou en téléchargeant un fichier CSV, puis accédez à votre solution d’hébergement de domaine pour générer les enregistrements DNS correspondants.

1. Assurez-vous que tous les enregistrements DNS ont été générés dans votre solution d’hébergement de domaine. Si tout est paramétré correctement, cochez la case &quot;Je confirme...&quot;.

   ![](assets/subdomain-create-dns-confirm.png)

   >[!NOTE]
   >
   >Vous pouvez créer les enregistrements ultérieurement à l’aide du **[!UICONTROL Save as draft]** bouton . Vous pourrez alors reprendre la délégation de sous-domaine à ce stade en l’ouvrant à partir de la liste de sous-domaines.

1. Patientez jusqu’à ce qu’Adobe vérifie que ces enregistrements sont générés sans erreur sur votre solution d’hébergement. Ce processus peut prendre jusqu’à 2 minutes.

   >[!NOTE]
   >
   >Tous les enregistrements manquants, c’est-à-dire les enregistrements non encore créés sur votre solution d’hébergement, seront répertoriés.

1. Adobe génère un enregistrement de validation d’URL CDN SSL. Copiez cet enregistrement de validation dans votre plateforme d’hébergement. Si vous avez correctement créé cet enregistrement sur votre solution d’hébergement, cochez la case &quot;Je confirme...&quot;, puis cliquez sur **[!UICONTROL Submit]**.

   ![](assets/subdomain-cdn-url-validation.png)

   >[!NOTE]
   >
   >Vous pouvez également créer l’enregistrement de validation et envoyer ultérieurement la configuration du sous-domaine à l’aide de la variable **[!UICONTROL Save as draft]** bouton . Vous pourrez ensuite reprendre la délégation de sous-domaine en l’ouvrant à partir de la liste de sous-domaines.

1. Une fois la délégation de sous-domaine CNAME envoyée, le sous-domaine s’affiche dans la liste avec la variable **[!UICONTROL Processing]** statut. Pour plus d’informations sur les statuts des sous-domaines, reportez-vous à la section [cette section](about-subdomain-delegation.md#access-delegated-subdomains).

   Avant de pouvoir utiliser ce sous-domaine pour envoyer des messages, vous devez attendre qu’Adobe effectue les vérifications requises, qui prennent généralement 2 à 3 heures. En savoir plus dans [cette section](#subdomain-validation).

1. Une fois les vérifications réussies<!--i.e Adobe validates the record you created and installs it-->, le sous-domaine reçoit la valeur **[!UICONTROL Success]** statut. Il est prêt à être utilisé pour diffuser des messages.

   >[!NOTE]
   >
   >Le sous-domaine sera marqué comme **[!UICONTROL Failed]** si vous ne créez pas l’enregistrement de validation sur votre solution d’hébergement.

Lors de la validation de l’enregistrement et de l’installation du certificat, Adobe crée automatiquement l’enregistrement PTR pour le sous-domaine CNAME. [En savoir plus](ptr-records.md)

>[!CAUTION]
>
>L’exécution parallèle de sous-domaines n’est actuellement pas prise en charge dans [!DNL Journey Optimizer]. Si vous tentez d’envoyer un sous-domaine pour délégation lorsqu’un autre possède la propriété **[!UICONTROL Processing]** , vous obtiendrez un message d’erreur.

## Validation de sous-domaine {#subdomain-validation}

Les vérifications et actions ci-dessous seront effectuées jusqu’à ce que le sous-domaine soit vérifié et puisse être utilisé pour envoyer des messages.

>[!NOTE]
>
>Ces étapes sont effectuées par Adobe et peuvent prendre jusqu’à 3 heures.

1. **Pre-validate**: Adobe vérifie si le sous-domaine a été délégué à Adobe DNS (enregistrement NS, enregistrement SOA, configuration de zone, enregistrement propriétaire). Si l’étape de prévalidation échoue, une erreur est renvoyée avec la raison correspondante, sinon Adobe passe à l’étape suivante.

1. **Configuration du DNS pour le domaine**:

   * **Enregistrement MX**: Mail eXchange record : enregistrement du serveur de messagerie qui traite les emails entrants envoyés au sous-domaine.
   * **Enregistrement SPF**: Enregistrement Sender Policy Framework : répertorie les adresses IP des serveurs de messagerie qui peuvent envoyer des emails à partir du sous-domaine.
   * **Enregistrement DKIM**: DomainKeys Identified Mail : utilise le cryptage de la clé publique-privée pour authentifier le message afin d’éviter les usurpations.
   * **A**: Mappage IP par défaut.
   * **CNAME**: Un enregistrement de nom canonique ou CNAME est un type d’enregistrement DNS qui associe un nom d’alias à un nom de domaine vrai ou canonique.

1. **Créer des URL de tracking et miroir**: si le domaine est email.example.com, le domaine tracking/miroir sera data.email.example.com. Il est sécurisé en installant le certificat SSL.

1. **Configuration de CDN CloudFront**: si le réseau de diffusion de contenu n’est pas déjà configuré, Adobe le prévoit pour l’ID de votre organisation.

1. **Créer un domaine CDN**: si le domaine est email.example.com, le domaine CDN est cdn.email.example.com.

1. **Création et ajout d’un certificat SSL CDN**: Adobe crée le certificat CDN pour le domaine CDN et joint le certificat au domaine CDN.

1. **Créer un DNS avancé**: s’il s’agit du premier sous-domaine que vous déléguez, Adobe crée le DNS avant qui est requis pour créer des enregistrements PTR : un pour chacune de vos adresses IP.

1. **Création d’un enregistrement PTR**: L’enregistrement PTR, également appelé enregistrement DNS inversé, est requis par les FAI pour qu’ils ne marquent pas les emails comme spam. Gmail recommande également d’avoir des enregistrements PTR pour chaque adresse IP. Adobe crée des enregistrements PTR uniquement lorsque vous déléguez un sous-domaine pour la première fois, un pour chaque adresse IP, toutes les adresses IP pointant vers ce sous-domaine. Par exemple, si l’adresse IP est *192.1.2.1* et que le sous-domaine est *email.example.com*, l’enregistrement PTR sera : *192.1.2.1 PTR r1.email.example.com*. Vous pouvez mettre à jour l’enregistrement PTR par la suite pour pointer vers le nouveau domaine délégué. [En savoir plus sur les enregistrements PTR](ptr-records.md)

## Vidéo pratique{#video}

Découvrez comment créer un sous-domaine à l’aide de CNAME pour pointer vers des enregistrements spécifiques à Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
