---
title: Diffusion de décisions par lots dans le publipostage direct
description: Utilisez Experience Decisioning pour personnaliser les fichiers d’extraction de publipostage direct ou pour exporter des données de prise de décision à utiliser dans les systèmes en aval
feature: Decisioning, Direct Mail
topic: Integrations
role: User
level: Intermediate
keywords: prise de décision par lots, publipostage direct, prise de décision
source-git-commit: 1b4e12b9433a819a3be34c4f01c489af1d6091ed
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---


# Diffusion de décisions par lots dans le publipostage direct {#batch-decisioning-direct-mail}

Avec la diffusion de décisions par lots, la diffusion de décisions sélectionne le ou les meilleurs éléments de décision pour chaque profil et inclut ces résultats dans le fichier d’extraction du courrier. Vous pouvez renvoyer plusieurs éléments par profil en définissant **[!UICONTROL Nombre d’éléments]** lors de la configuration de la politique de décision. Le fichier exporté peut être utilisé pour la personnalisation du publipostage direct ou pour des cas d’utilisation par lots dans lesquels vous exportez des profils et des attributs de décision vers un autre système.

La diffusion de décisions par lots dans le publipostage direct prend en charge deux cas d’utilisation principaux :

* **Publipostage direct avec prise de décision** - Personnalisez le publipostage physique par destinataire. Par exemple, choisissez la meilleure image ou offre pour chaque profil à l&#39;aide des règles d&#39;éligibilité et du classement (priorité ou formules). Le fichier d’extraction inclut les données de profil plus les attributs de l’élément de décision sélectionné ou des éléments sélectionnés (par exemple, l’URL de l’image de l’offre) pour votre fournisseur de publipostage direct.
* **Exportation par lots pour les systèmes en aval** - Exportez des profils et leurs résultats de prise de décision (par exemple, les identifiants d’offre, les attributs) pour les utiliser dans un autre système. Vous exécutez la diffusion de décisions par lots et exportez le fichier sur votre serveur ; les outils en aval (par exemple, un fournisseur de services de messagerie tiers) utilisent ces données pour leurs propres campagnes ou processus.

>[!NOTE]
>
>Cette page se concentre sur les aspects spécifiques à la prise de décision de l’utilisation de la diffusion de décisions par lots avec le publipostage direct. Pour obtenir des informations complètes sur la configuration et l’utilisation du canal courrier, notamment le routage des fichiers, la configuration du canal et la configuration des fichiers d’extraction, reportez-vous aux sections [Prise en main du courrier](../direct-mail/get-started-direct-mail.md) et [Création d’un message de publipostage direct](../direct-mail/create-direct-mail.md).

## Présentation des workflows {#workflow}

1. **Création d’une campagne ou d’un parcours de publipostage direct** : créez un parcours ou une campagne, sélectionnez l’action **[!UICONTROL Publipostage direct]**, choisissez une configuration de publipostage direct et définissez l’audience.

   ➡️ [Découvrez comment créer un message de publipostage direct](../direct-mail/create-direct-mail.md)

1. **Ajoutez une politique de décision** :

   1. Cliquez sur **[!UICONTROL Modifier le contenu]** pour configurer le fichier d’extraction.
   1. Ajoutez une colonne au fichier d’extraction et ouvrez l’éditeur de personnalisation à l’aide de l’icône ![](assets/do-no-localize/editor-icon.svg) .

      ![](assets/decision-policy-dm-add.png)

   1. Accédez au menu **[!UICONTROL Prise de décision]** pour créer une politique de décision. Dans la configuration de la politique, définissez **[!UICONTROL Nombre d’éléments]** si vous avez besoin de plusieurs éléments de décision par profil, puis configurez la stratégie de sélection et la solution de secours facultative.

      ![](assets/decision-policy-dm-create.png)

   ➡️ [Découvrez comment ajouter et configurer une politique de décision dans le publipostage direct](create-decision-policy.md#add)

1. **Personnaliser le fichier de publipostage direct avec des attributs de décision** : pour les colonnes qui doivent contenir le résultat de la décision, ouvrez l’éditeur Personalization, accédez à **[!UICONTROL Politiques de décision]** et sélectionnez **[!UICONTROL Insérer une politique]** pour ajouter le code de votre politique de décision.

   Utilisez les attributs d’élément de décision renvoyés afin que les informations d’offre sélectionnées soient incluses dans le fichier d’extraction pour chaque profil. Lorsque plusieurs éléments sont renvoyés, mappez les attributs de chaque élément dans vos colonnes à l’aide de la boucle de `#each` de politique.

   ➡️ [Découvrez comment utiliser les politiques de décision dans les messages - Onglet Courrier](use-decision-policy.md)

1. Utilisez **[!UICONTROL Simuler du contenu]** avec un profil de test pour prévisualiser la ligne exportée (y compris la valeur de prise de décision).

   ![](assets/batch-decisioning-simulate.png)

   ➡️ [Découvrez comment prévisualiser et tester votre contenu](../content-management/preview-test.md)

1. Activez la campagne ou publiez le parcours pour générer et exporter le fichier (délimité par un fichier CSV ou texte) vers votre serveur configuré.

   ➡️ [Découvrez comment vérifier et activer une campagne](../campaigns/review-activate-campaign.md) | [Découvrez comment publier un parcours ](../building-journeys/publish-journey.md)

## Exemple de publipostage direct + prise de décision {#example-direct-mail}

Exemple : un module fitness retailer envoie une carte postale personnalisée à chaque client avec l’une des dix images possibles. Ils utilisent Decisioning pour sélectionner la meilleure image par profil.

1. Créez 10 éléments de décision (un par image), chacun avec des règles d’éligibilité (par exemple, l’âge, le sexe).
2. Ajoutez-les à une collection et créez une stratégie de sélection avec une méthode de classement (par exemple, priorité manuelle ou formule).
3. Dans une campagne ou un parcours de publipostage direct, activez la prise de décision et ajoutez une politique de décision qui utilise cette stratégie de sélection.
4. Dans le fichier d’extraction, ajoutez une colonne dont les données correspondent à l’attribut d’élément de décision qui contient l’image choisie (par exemple, l’URL de l’image de l’offre). Les autres colonnes peuvent être le nom complet, l’adresse, l’état, le code postal, etc.
5. Lorsque la campagne s’exécute, chaque profil obtient une ligne dans l’exportation avec l’image sélectionnée pour ce profil. Le fournisseur de publipostage direct utilise ce fichier pour générer le publipostage physique.

Vous pouvez utiliser l’option **[!UICONTROL Simuler du contenu]** avec un profil de test pour afficher les résultats de la prise de décision (par exemple, l’image) qui seraient exportés pour ce profil.

## Cas pratique d’export par lots (middleware) {#example-batch-export}

Certains clients utilisent la diffusion de décisions par lots pour exporter des profils et leurs résultats de décision en vue de les utiliser dans d’autres systèmes (par exemple, un CRM ou un fournisseur de services de messagerie). Le flux est :

1. Configurez le publipostage direct (routage des fichiers + configuration des canaux) comme ci-dessus.
2. Créez une campagne ou un parcours de publipostage direct et ajoutez une politique de décision.
3. Ajoutez des colonnes pour les champs de profil et pour les attributs d’élément de décision dont vous avez besoin dans l’exportation.
4. Activer la campagne. Le fichier est exporté vers votre serveur (par exemple, Amazon S3 ou SFTP).
5. Votre système en aval récupère le fichier et utilise les données de profil et de prise de décision pour ses propres campagnes ou processus.

Cela prend en charge les cas d’utilisation de prise de décision par lots via le canal courrier avec Experience Decisioning.

## Documentation connexe {#related}

* [Créer un message de publipostage direct](../direct-mail/create-direct-mail.md) - Configurez le fichier d’extraction et activez la prise de décision
* [Créer des politiques de décision](create-decision-policy.md#add) - Ajoutez une politique de décision dans l’onglet Courrier
* [Configuration du publipostage direct](../direct-mail/direct-mail-configuration.md) - Routage des fichiers et configuration des canaux
* [Prise en main de Decisioning](gs-experience-decisioning.md) - Concepts et mécanismes de sécurisation
