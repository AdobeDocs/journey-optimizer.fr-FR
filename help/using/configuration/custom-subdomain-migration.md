---
solution: Journey Optimizer
product: journey optimizer
title: Migration d’un sous-domaine de messagerie de CNAME vers la délégation personnalisée
description: Découvrez comment migrer un sous-domaine de page de destination ou d’e-mail de la délégation CNAME vers la délégation personnalisée dans Journey Optimizer.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Intermediate
keywords: sous-domaine, délégation, migration, CNAME, délégation personnalisée
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 3148a105551b920c4402c7b3c093aca1bb012061
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 22%

---

# Migration d’un sous-domaine de messagerie de CNAME vers la délégation personnalisée {#migrate-cname-to-custom}

>[!AVAILABILITY]
>
>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en bénéficier.

Si votre sous-domaine est actuellement configuré avec des [CNAME](about-subdomain-delegation.md#cname-subdomain-setup), vous pouvez le migrer vers la méthode **[!UICONTROL Délégation personnalisée]** pour répondre aux politiques de sécurité de votre entreprise. Vous avez ainsi la propriété et le contrôle complets de vos sous-domaines et certificats dans [!DNL Journey Optimizer]. [En savoir plus sur les sous-domaines personnalisés](delegate-custom-subdomain.md)

Dans le cadre de ce processus, vous devez :

* [Supprimer les enregistrements DNS existants](#delete-dns) de votre solution d’hébergement
* [Téléchargez le certificat SSL](#upload-ssl-certificate) obtenu auprès de l’autorité de certification
* Suivez les étapes [&#x200B; Feedback Loop &#x200B;](#feedback-loop) en vérifiant la propriété du domaine et l’adresse e-mail de reporting.
* [Copiez l’enregistrement de validation d’URL du réseau CDN SSL](#copy-ssl-cdn-url-record) généré par Adobe dans votre plateforme d’hébergement

Pour migrer votre sous-domaine, procédez comme suit.

## Avant de commencer {#before-you-begin}

Avant de commencer le processus de migration, passez en revue les informations importantes ci-dessous.

>[!IMPORTANT]
>
>Vous pouvez uniquement migrer un sous-domaine configuré avec la [méthode CNAME](delegate-subdomain.md#cname-subdomain-setup).

* Assurez-vous que la **méthode de délégation personnalisée est activée** pour votre organisation (cette fonctionnalité est actuellement à disponibilité limitée ; contactez votre représentant Adobe pour obtenir l’accès). [En savoir plus](delegate-custom-subdomain.md)
* Assurez-vous qu’aucune configuration de canal active n’utilise ce sous-domaine. Le processus de migration interrompra leur fonctionnalité.
* Assurez-vous qu’aucune campagne ou parcours actif n’utilise une configuration de canal liée à ce sous-domaine, car cela peut entraîner des perturbations de la diffusion.
* Gardez à l’esprit que les temps d’arrêt commencent dès que vous entrez dans le flux de migration. Le sous-domaine passe à l’état **[!UICONTROL Brouillon]** pendant le processus et n’est pas disponible tant que la configuration n’est pas terminée.
* Par conséquent, il est recommandé d’**effectuer les étapes préalables à la migration avant de démarrer le processus de migration** afin que votre certificat SSL soit prêt et que les temps d’arrêt soient réduits. [En savoir plus](#start-migration)

## Démarrer la migration {#start-migration}

Suivez les étapes ci-dessous pour commencer à migrer un sous-domaine donné.

1. Accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres d’e-mail]** > **[!UICONTROL Sous-domaines]**.

1. Sélectionnez un sous-domaine configuré avec des CNAME et ouvrez-le.

1. Vous pouvez utiliser la section **[!UICONTROL Génération de la demande de signature de certificat avant la migration]** pour générer la demande de signature de certificat afin de l’envoyer à l’autorité de certification. Le certificat SSL sera alors prêt lorsque le processus de migration démarrera. [Voici comment procéder](#send-csr-to-ca)

   >[!IMPORTANT]
   >
   >Les étapes de pré-migration sont facultatives à ce stade, mais vivement recommandées. Les terminer **avant** de commencer la migration réduit les temps d’arrêt et permet d’assurer une transition fluide.

   ![](assets/subdomain-migrate-pre-migration-csr.png){width="70%"}

1. Sélectionnez **[!UICONTROL Migrer maintenant]** dans la section dédiée.

   <!--![](assets/subdomain-migrate-to-custom.png){width=90%}-->

1. Vérifiez les [informations affichées](#before-you-begin).

   >[!WARNING]
   >
   >Les temps d’arrêt commencent dès que vous entrez dans le flux de migration. Assurez-vous donc qu’ils n’ont aucune incidence sur vos campagnes et parcours actifs.

1. Cliquez sur **[!UICONTROL Oui]**. Le sous-domaine passe au statut **[!UICONTROL Brouillon]** et n’est pas disponible tant que la configuration n’est pas terminée.

## Générer et envoyer la demande de signature de certificat à l’autorité de certification {#send-csr-to-ca}

Pour terminer la migration, vous avez besoin d’un certificat SSL émis par une autorité de certification (CA). Pour recevoir ce certificat SSL, vous devez d’abord générer une demande de signature de certificat (CSR) et l’envoyer à l’autorité de certification.

Que vous ayez déjà commencé le processus de migration ou non, suivez les étapes ci-dessous pour générer et envoyer votre nouvelle demande de signature de certificat.

1. Cliquez sur **[!UICONTROL Régénérer la CSR]**.

1. Remplissez le formulaire qui affiche et régénérez la demande de signature de certificat (CSR).

   ![](assets/subdomain-migrate-regenerate-csr.png){width="60%"}

   >[!NOTE]
   >
   >La longueur de la clé peut être de 2 048 ou 4 096 bits uniquement. Elle ne peut plus être modifiée une fois le sous-domaine envoyé.

1. Cliquez sur **[!UICONTROL Télécharger la CSR]** et enregistrez le formulaire sur votre ordinateur local.

1. Envoyez-le à l’autorité de certification pour obtenir votre certificat SSL. Avant d’envoyer cette CSR à votre autorité de certification pour signature, prenez en compte les points suivants :

   * La CSR téléchargée à l’étape 3 est réservée à data.subdomain.com.

   * Toutefois, le certificat doit couvrir à la fois data.subdomain.com et cdn.subdomain.com en tant qu’entrées de noms alternatifs de l’objet (SAN) dans un seul certificat. Par exemple, si vous déléguez example.adobe.com, alors data.subdomain.com correspond à data.example.adobe.com et cdn.subdomain.com correspond à cdn.example.adobe.com.

   * Les sous-domaines de données (data.example.adobe.com) et de CDN (cdn.example.adobe.com) doivent être ajoutés en tant qu’entrées d’homologue dans le même certificat.

   * La plupart des autorités de certification vous permettent d’ajouter des SAN supplémentaires (tels que le sous-domaine du CDN) pendant le processus de signature.

      * Par le biais du portail de l’autorité de certification (recommandé, le cas échéant), ou
      * En faisant une demande manuelle à leur équipe d’assistance si l’option de portail n’est pas disponible.

   * Après la signature, l’autorité de certification émettra un certificat unique couvrant à la fois le domaine de données et le sous-domaine du CDN.

## Supprimer les enregistrements DNS existants {#delete-dns}

Après avoir commencé le processus de migration, vous devez supprimer les enregistrements DNS existants de votre solution d’hébergement. Suivez les étapes ci-après.

1. La liste des enregistrements actuellement configurés dans vos serveurs DNS s’affiche.

1. Accédez à votre solution d’hébergement de domaine et supprimez les entrées CNAME existantes de votre hébergement DNS.

1. Assurez-vous que tous les enregistrements DNS ont été supprimés. Une fois l’opération terminée, cochez la case « Je confirme avoir supprimé les enregistrements requis du site d’hébergement ».

   ![](assets/subdomain-migrate-delete-dns.png){width="75%"}

## Charger le certificat SSL {#upload-ssl-certificate}

Dans la section **[!UICONTROL Certificat SSL]** , vous devez charger un nouveau certificat SSL vers [!DNL Journey Optimizer].

Avant cela, vérifiez les éléments suivants :

* Si vous avez déjà envoyé votre demande de signature de certificat à l’autorité de certification dans le cadre des [étapes préalables à la migration](#start-migration), assurez-vous d’avoir reçu votre certificat SSL.

* Si vous ne l’avez pas déjà fait, suivez les étapes pour [générer, télécharger et envoyer la CSR](#send-csr-to-ca).

<!--
    * Click **[!UICONTROL Regenerate CSR]** and fill the form to generate the Certificate Signing Request.

    * Click **[!UICONTROL Download CSR]** to save the form to your local computer.

    * Send the CSR to the Certificate Authority to get your SSL certificate.-->

1. Une fois votre certificat SSL récupéré, cliquez sur **[!UICONTROL Télécharger le certificat]**.

   ![](assets/subdomain-migrate-ssl-certificate.png){width="75%"}

1. Téléchargez le certificat SSL au format [!DNL Journey Optimizer] .pem avec la chaîne de certificats complète. Voici un exemple de format de fichier .pem :

   ```
   -----BEGIN CERTIFICATE-----
   MIIDXTCCAkWgAwIBAgIJALc3... (base64 encoded data)
   -----END CERTIFICATE-----
   ```

1. Cochez la case « Je confirme avoir téléchargé le certificat SSL ».

## Boucle de rétroaction complète {#feedback-loop}

Suivez ensuite les étapes de la boucle des commentaires pour vérifier la propriété du domaine et l’adresse e-mail de reporting.

![](assets/subdomain-migrate-feedback-loop.png){width="75%"}

Le processus est le même que lors de la configuration d’un nouveau sous-domaine personnalisé. Suivez les étapes présentées dans la page [Configurer un sous-domaine personnalisé](delegate-custom-subdomain.md#feedback-loop-steps).

## Copiez l’enregistrement de validation de l’URL du réseau CDN SSL {#copy-ssl-cdn-url-record}

Pour terminer le processus de migration, copiez l’enregistrement de validation d’URL CDN SSL généré par Adobe dans votre plateforme d’hébergement. Le processus est le même que lors de la configuration d’un nouveau sous-domaine personnalisé. Suivez les étapes présentées dans la page [Configurer un sous-domaine personnalisé](delegate-custom-subdomain.md#copy-ssl-cdn-url-record).

Après l’envoi, vous devez attendre qu’Adobe effectue les vérifications requises, ce qui peut prendre jusqu’à 3 heures. [En savoir plus](delegate-subdomain.md#submit-subdomain)

Une fois que le sous-domaine est à nouveau actif, aucune modification n’est nécessaire aux configurations de canal existantes qui l’utilisent. Elles continuent à fonctionner comme avant.

**Voir également**

* [Configurer un sous-domaine personnalisé](delegate-custom-subdomain.md)
* [Méthodes de délégation de sous-domaine](about-subdomain-delegation.md#subdomain-delegation-methods)
