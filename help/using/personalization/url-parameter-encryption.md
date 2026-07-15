---
solution: Journey Optimizer
product: journey optimizer
title: Paramètres de chiffrement de l’URL
description: Découvrez comment chiffrer les paramètres de requête d’URL sensibles afin que les informations d’identification personnelles ne soient pas exposées en texte brut sur les liens de suivi et les pages de destination Journey Optimizer.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
keywords: chiffrement, URL, tracking, page de destination, registre des clés, personnalisation, sécurité, confidentialité, sandbox
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1348
ht-degree: 1%

---

# Paramètres de chiffrement de l’URL {#url-parameter-encryption}

>[!BEGINSHADEBOX]

**Sur cette page :** Découvrez comment chiffrer les paramètres de requête d’URL sensibles afin que les informations d’identification personnelle ne soient pas exposées en texte brut, y compris la manière dont les administrateurs créent, font pivoter et révoquent des clés dans le registre des clés Sandbox de Adobe Journey Optimizer.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Actuellement, cette fonctionnalité n’est disponible que pour le canal E-mail .

## Pourquoi utiliser le chiffrement des paramètres d’URL ? {#why-url-parameter-encryption}

Les liens de tracking et les URL de page de destination personnalisés incluent souvent des attributs de profil, des identifiants, des jetons ou d’autres valeurs dans la chaîne de requête. Ces paramètres sont généralement visibles en tant que texte brut dans l’e-mail ou le SMS et ils restent lisibles si quelqu’un copie, partage ou met en signet le lien. Cela peut constituer un risque pour la sécurité et la confidentialité lorsque les valeurs peuvent inclure des informations d’identification personnelle (PII) ou d’autres données sensibles qu’elles doivent protéger.

[!DNL Journey Optimizer] fournit un assistant de chiffrement dans l’éditeur de personnalisation afin que vous puissiez chiffrer n’importe quelle valeur d’expression au moment du rendu (par exemple, un attribut de profil, un jeton ou une chaîne que vous avez créée à partir de plusieurs champs). Le chiffrement nécessite toujours une clé provenant du registre de votre organisation.

Vous chiffrez uniquement les paramètres de requête de votre choix à l’aide de clés gérées par les administrateurs dans un registre au niveau du sandbox, de sorte que les valeurs confidentielles ne restent pas exposées en texte clair lorsque le lien est partagé ou inspecté.

### Fonctionnement {#how-it-works}

* **Administrateurs** utilisez le registre des clés pour [créer des clés](#create-keys) et [gérer des clés](#manage-keys) conformément aux politiques de sécurité de votre entreprise.
* **Spécialistes du marketing** insérez l’assistant `Encrypt` dans l’éditeur de personnalisation et transmettez la valeur à protéger, ainsi qu’un identifiant de clé active dans le registre. Pour connaître la syntaxe et les options, voir [cette section](functions/helpers.md#url-parameter-encryption-helper).

>[!IMPORTANT]
>
>Le déchiffrement est la responsabilité de votre organisation. [!DNL Journey Optimizer] chiffre les valeurs lors du rendu du message. Votre site web, votre application ou votre API doit déchiffrer les paramètres à l’aide des mêmes matériaux et processus cryptographiques que vous définissez, conformément à votre modèle de sécurité.

### Exemple

Une URL de page de destination peut utiliser un paramètre de requête tel que `token` dont la valeur est un jeton de chaîne (par exemple, une payload JSON avec des identifiants d’offre ou de profil). Sans chiffrement, ce jeton de chaîne est visible en tant que texte brut dans le lien. Encapsuler cette valeur avec l’assistant de chiffrement remplace la payload sensible par le texte chiffré dans l’URL tout en laissant le reste du lien inchangé.

## Création de clés {#create-keys}

Avant de pouvoir utiliser l’assistant de chiffrement des paramètres d’URL, vous devez créer une clé. Pour ce faire, procédez comme suit.

>[!IMPORTANT]
>
>Pour accéder aux clés et les gérer, vous devez disposer des autorisations **Afficher le registre des clés** et **Gérer le registre des clés** accordées. [En savoir plus](../administration/high-low-permissions.md#administration-permissions)

1. Accédez à **[!UICONTROL Administration]** > **[!UICONTROL Configurations]**.

1. Cliquez sur le bouton **[!UICONTROL Gérer]** pour ouvrir le **[!UICONTROL Registre des clés]**.

   ![Section Registre des clés du menu Administration](assets/encryption-key-registry.png){width="80%"}

1. À l’aide du bouton dédié, créez les clés selon les besoins de votre organisation.

   ![Bouton Créer une clé dans la section Registre des clés](assets/encryption-create-key.png){width="80%"}

1. Attribuez-leur un libellé ou un identifiant clair que vos équipes peuvent référencer dans l’éditeur de personnalisation.

   ![Détails clés dans la section Registre des clés](assets/encryption-key-details.png){width="80%"}

1. Cliquez sur **[!UICONTROL Soumettre]** pour confirmer vos modifications.

Une fois une clé créée, les marketeurs peuvent utiliser l&#39;assistant [chiffrement des paramètres d&#39;URL](functions/helpers.md#url-parameter-encryption-helper) de l&#39;éditeur de personnalisation pour chiffrer les valeurs spécifiques qu&#39;ils placent dans les paramètres de requête d&#39;URL.

## Gérer des clés {#manage-keys}

Pour gérer les clés, procédez comme suit.

1. Accédez au **[!UICONTROL Registre des clés]**. Toutes les clés créées pour le sandbox actuel s’affichent dans une vue de liste.

   ![Vue Liste du registre des clés](assets/encryption-key-registry-list.png){width="100%"}

1. Cliquez sur une clé avec le statut **[!UICONTROL Actif]** pour ouvrir les détails de la clé.

   ![Détails des clés actives](assets/encryption-key-active-details.png){width="80%"}

1. Cliquez sur le bouton **[!UICONTROL Révoquer]** pour désactiver définitivement la clé du nouveau chiffrement.

   Une fois qu’une clé est révoquée, les tentatives de l’utiliser dans l’assistant doivent échouer au moment du rendu. Les entrées révoquées restent visibles pour l’audit ; vos équipes peuvent toujours avoir besoin du matériel correspondant pour déchiffrer les payloads plus anciennes sur vos propres systèmes.

1. Cliquez sur le bouton **[!UICONTROL Rotation]** pour fournir un nouveau matériau de clé tout en conservant un identifiant de clé stable où vos parcours et campagnes le référencent déjà.

   Les documents antérieurs sont conservés dans le registre avec un statut révoqué et une raison appropriée (par exemple, un horodatage de rotation), et une nouvelle ligne ou version reflète la clé active.

   >[!NOTE]
   >
   >Seules les clés actives doivent être sélectionnées pour chiffrer les nouvelles valeurs dans l’éditeur de personnalisation. N’utilisez pas de clés révoquées pour le nouveau contenu.

## Référence rapide {#quick-reference}

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

>[!BEGINTABS]

>[!TAB Vue d’ensemble]

**TL;DR**

Cette page explique comment les administrateurs créent, font pivoter et révoquent des clés de chiffrement dans le registre des clés au niveau du sandbox Journey Optimizer, ce qui permet aux spécialistes marketing de chiffrer des paramètres de requête d’URL sensibles afin que les informations d’identification personnelles ne soient pas exposées en texte brut dans les liens de suivi et les pages de destination.

**Intentions**

* Comprendre pourquoi le chiffrement des paramètres d’URL est nécessaire (données sensibles et PII visibles dans des chaînes de requête en texte brut)
* Création de clés de chiffrement dans le registre des clés du sandbox (tâche d’administration nécessitant des autorisations spécifiques)
* Révoquer une clé pour la désactiver définitivement pour un nouveau chiffrement
* Faire pivoter une clé pour fournir un nouveau matériel cryptographique tout en conservant le même identifiant
* Utiliser l’assistant `Encrypt` dans l’éditeur de personnalisation pour protéger des valeurs de paramètre de requête spécifiques

>[!TAB Glossaire]

* **Registre des clés** : référentiel au niveau du sandbox dans Journey Optimizer (Administration > Configurations) où les administrateurs créent et gèrent des clés de chiffrement utilisées par l’assistant de chiffrement du paramètre d’URL. *(spécifique au produit)*
* **Assistant de chiffrement (`Encrypt`)** : fonction d’assistance dans l’éditeur de personnalisation qui chiffre une valeur d’expression au moment du rendu, en remplaçant les informations d’identification personnelle par un texte chiffré dans les paramètres de requête d’URL. *(spécifique au produit)*
* **Révoquer (clé)** : acte de désactivation permanente d’une clé pour un nouveau chiffrement ; l’entrée de clé reste visible dans le registre pour l’audit et les payloads plus anciennes peuvent toujours l’exiger pour le déchiffrement sur les systèmes de l’entreprise.
* **Rotation (clé)** : acte consistant à fournir un nouveau matériel cryptographique pour une clé tout en maintenant son identifiant stable, de sorte que les campagnes et parcours qui référencent déjà cette clé n’ont pas besoin d’être mis à jour.
* **PII (informations d’identification personnelle)** : données qui peuvent identifier un individu, comme les attributs de profil, les jetons ou les identifiants d’offre, qui doivent être protégées lorsqu’elles sont incluses dans les paramètres de requête d’URL.

>[!TAB  Terminologie ]

* **Nom canonique :** chiffrement des paramètres d’URL — Variantes : chiffrement des URL, chiffrement des paramètres de requête, obscurcissement des paramètres d’URL
* **Synonymes:** « registre des clés » = « Registre des clés » (libellé de l’interface utilisateur dans Administration > Configurations)
* **Ne pas confondre :** Révoquer (désactive définitivement la clé pour le nouveau chiffrement ; l’entrée reste pour l’audit) ≠ Roter (remplace le matériel cryptographique mais garde le même identifiant de clé actif pour le nouveau chiffrement)

>[!TAB Mécanismes de sécurisation et limitations]

* Le chiffrement des paramètres d’URL est actuellement disponible uniquement pour le canal E-mail.
* Nécessite des autorisations **Afficher le registre des clés** et **Gérer le registre des clés** pour accéder aux clés et les gérer.
* Le déchiffrement est la responsabilité de l&#39;organisation. Journey Optimizer chiffre les valeurs au moment du rendu ; le site web, l’application ou l’API doivent déchiffrer les paramètres à l’aide du même matériel et des mêmes processus cryptographiques que ceux définis par l’organisation.
* Seules les clés actives doivent être utilisées pour chiffrer les nouvelles valeurs dans l’éditeur de personnalisation. Les clés révoquées ne doivent pas être utilisées pour un nouveau contenu.
* Les clés révoquées restent visibles dans le registre à des fins d’audit. Les systèmes de l’entreprise peuvent toujours en avoir besoin pour déchiffrer les anciennes payloads.

>[!TAB FAQ]

**Q : Qui est responsable du déchiffrement ?**

Le déchiffrement est la responsabilité de l&#39;organisation. Journey Optimizer chiffre les valeurs lors du rendu du message. Le site web, l’application ou l’API doit déchiffrer les paramètres de requête à l’aide du même matériel et des mêmes processus cryptographiques que ceux définis par l’entreprise.

**Q : Quelle est la différence entre Révoquer et Faire pivoter ?**

La révocation désactive définitivement une clé pour un nouveau chiffrement tout en gardant l’entrée visible dans le registre pour l’audit (les payloads plus anciennes peuvent toujours avoir besoin de la clé pour le déchiffrement sur les systèmes de l’entreprise). Rotate fournit du nouveau matériel cryptographique pour une clé tout en conservant le même identifiant de clé, de sorte que les campagnes et les parcours qui la référencent continuent à fonctionner sans mises à jour.

**Q : Quelles sont les autorisations requises pour gérer les clés ?**

Autorisations **Afficher le registre des clés** et **Gérer le registre des clés**.

**Q : Quels canaux prennent en charge le chiffrement des paramètres d’URL ?**

Actuellement, seul le canal E-mail .

**Q : Une clé révoquée peut-elle être utilisée pour un nouveau chiffrement ?**

Non. Une fois qu’une clé est révoquée, les tentatives de l’utiliser dans l’assistant de chiffrement doivent échouer au moment du rendu. N’utilisez pas de clés révoquées pour le nouveau contenu.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: c594ce24 -->
