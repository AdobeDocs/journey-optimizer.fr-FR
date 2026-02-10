---
solution: Journey Optimizer
product: journey optimizer
title: Référence des codes d’erreur
description: Découvrez les codes d’erreur courants dans  [!DNL Adobe Journey Optimizer]  et comment les résoudre
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: erreur, codes, dépannage, parcours, campagne, messages
exl-id: 84924153-1bb5-465a-b91c-797628fc816c
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '2381'
ht-degree: 94%

---

# Référence des codes d’erreur {#error-codes}

[!DNL Adobe Journey Optimizer] utilise des codes d’erreur normalisés pour vous aider à identifier et à résoudre rapidement les problèmes liés aux parcours, aux campagnes et aux configurations de messages. La compréhension de ces codes d’erreur peut réduire considérablement le temps de dépannage et vous aider à maintenir des performances de campagne optimales.

## Comprendre la structure des codes d’erreur {#error-code-structure}

[!DNL Adobe Journey Optimizer] codes d’erreur suivent un modèle de dénomination cohérent qui permet d’identifier le composant et le type de problème :

* **Préfixe de service** : indique quel service de [!DNL Adobe Journey Optimizer] a généré l’erreur.
Exemples : CJMPTS (Service Push/Transport), CJMRT (Exécution Du Parcours), CJMMAS (Service De Création De Messages), CJMCMP (Campaign), CJMTL (Couche De Transport), CJMRPS (Service De Création De Rapports/Approvisionnement)
* **Numéro d’erreur** : identifiant unique de la condition d’erreur spécifique
* **Code d’état HTTP** : code d’état HTTP standard (par exemple, 400, 403, 422, 500)

Exemple : `CJMRT-030012-422` indique une erreur d’exécution de parcours (CJMRT) avec le numéro d’erreur 030012 et le statut HTTP 422 (Entité non traitable).

## Où trouver les codes d’erreur {#find-error-codes}

Les codes d’erreur apparaissent à plusieurs emplacements dans [!DNL Adobe Journey Optimizer] :

* Rapports et journaux d’exécution de parcours
* Écrans d’activation de campagne
* Avertissements relatifs à la validation des messages
* Notifications et alertes système
* Réponses des API (lors de l’utilisation d’API REST)

Lorsqu’une erreur se produit, notez le code d’erreur complet et l’ID de requête qui l’accompagne, car ils sont essentiels pour le dépannage et l’assistance.

## Codes d’erreur courants par service {#error-codes-by-service}

Utilisez cette section pour rechercher les codes d&#39;erreur regroupés par service.

### CJMPTS : erreurs des services de notification push et de transport {#cjmpts-errors}

Ces erreurs se produisent lors des opérations de diffusion des notifications push et de transport des messages.

| Code d’erreur | Description | Cause principale | Résolution |
|------------|-------------|-----------|-----------|
| **CJMPTS-1410-500** | Erreur de serveur interne sur l’action d’envoi de notification push/canal | Panne du serveur principal du canal, informations d’identification arrivées à expiration, mauvaise configuration ou bug du fournisseur | &#x200B;1. Réessayez après un délai.<br/>2. Vérifiez les configurations et les quotas des fournisseurs.<br/>3. Vérifiez que les informations d’identification push sont valides.<br/>4. Testez avec un autre canal.<br/>5. Si le problème persiste, contactez l’assistance Adobe avec l’ID de demande.<br/><br/>**Documentation associée** : [Configuration push](../push/push-configuration.md) |
| **CJMPTS-1006-404** | Échec de la notification push/SMS avec « ressource introuvable » | Le fournisseur/canal référencé n’existe pas, est mal orthographié ou a été supprimé. | &#x200B;1. Examinez et corrigez les références et les ID de fournisseur/canal.<br/>2. Vérifiez la configuration des sandbox/organisations.<br/>3. Vérifiez que les configurations de canal sont actives.<br/>4. Recréez la configuration du canal si nécessaire.<br/><br/>**Documentation associée** : [Surfaces de canal](../configuration/channel-surfaces.md) |
| **CJMPTS-1510-500** | Erreur de serveur interne lors de l’envoi via canal push | Dysfonctionnement du serveur principal de notifications push/transport ; erreur du fournisseur ou de l’infrastructure | &#x200B;1. Vérifiez les paramètres d’approvisionnement des canaux.<br/>2. Vérifiez que les informations d’identification push sont valides.<br/>3. Réessayez l’opération.<br/>4. En cas de persistance, contactez l’assistance Adobe avec l’ID de demande <br/><br/>**Documentation connexe** : [Configuration push](../push/push-configuration.md) |
| **CJMPTS-1023-500** | Erreur de serveur interne lors de l’envoi/du processus de notifications push (passerelles tierces) | Dysfonctionnement temporaire du cloud ou erreur de service inconnue | &#x200B;1. Vérifiez la configuration du fournisseur/canal.<br/>2. Vérifiez le statut de la passerelle tierce.<br/>3. Réessayez après quelques minutes.<br/>4. Consulter les journaux pour plus d’informations <br/><br/>**Documentation connexe** : [Notifications push](../push/create-push.md) |
| **CJMPTS-1310-500** | Erreur interne du service de rendu (aperçu ou envoi en direct) | Échec du moteur de rendu de modèle en aval, généralement en raison de problèmes de syntaxe JSON/modèle | &#x200B;1. Validez la syntaxe et la structure du modèle.<br/>2. Vérifiez que toutes les variables de personnalisation sont valides.<br/>3. Utilisez une payload de test pour identifier le problème.<br/>4. Simplifiez la complexité du modèle si nécessaire <br/><br/>**Documentation connexe** : [Modèles de message](../content-management/content-templates.md), [Syntaxe de la personnalisation](../personalization/personalization-syntax.md). |

### CJMRT : erreurs d’exécution de parcours et d’API {#cjmrt-errors}

Ces erreurs se produisent lors de l’exécution du parcours, du traitement des événements et des opérations de l’API.

| Code d’erreur | Description | Cause principale | Résolution |
|------------|-------------|-----------|-----------|
| **CJMRT-110001-500** | Nombre maximal d’exécutions dépassé pour l’étape du workflow (par exemple, l’étape Approvisionnement d’affinité IP expire) | La tâche de workflow/d’approvisionnement ne s’est pas terminée dans les délais/reprises autorisés, souvent en raison d’un retard d’infrastructure/de service ou d’un problème temporaire de serveur principal. | &#x200B;1. Réessayez après un certain temps.<br/>2. Vérifiez la page [Statut Adobe](https://status.adobe.com/fr) en cas de pannes.<br/>3. Transmettez les informations relatives au workflow/à la tâche/à l’organisation à l’assistance Adobe.<br/>4. Fournissez des journaux et des captures réseau si disponibles <br/><br/>**Documentation connexe** : [Dépannage de parcours &#x200B;](troubleshooting.md). |
| **CJMRT-000071-400** | Requête incorrecte pendant l’événement de parcours/test ou l’appel API | La payload/les paramètres sont incorrects ou manquants ; l’entrée fait référence à une ressource inexistante ou inactive. | &#x200B;1. Consultez le corps de la requête pour obtenir les détails de l’erreur.<br/>2. Corrigez la référence ou le paramètre.<br/>3. Supprimez la configuration avancée, puis réessayez.<br/>4. Ajoutez les fonctionnalités une par une pour identifier le problème <br/><br/>**Documentation connexe** : [Dépannage de parcours](troubleshooting.md), [Configuration des événements](../event/about-events.md). |
| **CJMRT-000013-401** | Erreur non autorisée lors de l’opération d’exécution du message/de l’événement API | Échec de l’authentification : le jeton a expiré, les autorisations sont manquantes, l’intégration, l’utilisateur ou l’utilisatrice a perdu l’accès à l’environnement. | &#x200B;1. Vérifiez les autorisations et les rôles.<br/>2. Actualisez le jeton d’authentification.<br/>3. Utilisez un compte utilisateur, utilisatrice, service valide connu.<br/>4. Consultez les affectations de profils de produit <br/><br/>**Documentation connexe** : [Autorisations](../administration/permissions.md). |
| **CJMRT-080605-400** | Requête incorrecte provenant de l’exécution du parcours (par exemple, déclencheur de nœud, action, etc.) | La configuration fait référence à une fonctionnalité/un modèle/un canal supprimé/renommé ou obsolète. | &#x200B;1. Validez toutes les références de ressources.<br/>2. Vérifiez la configuration du parcours et les indicateurs de fonctionnalité.<br/>3. Mettez à jour les références défectueuses.<br/>4. Consultez les mises à jour et migrations système récentes.<br/><br/>**Documentation associée** : [Création de parcours](journey-gs.md) |
| **CJMRT-030012-422** | Entité non traitable : échec d’une action, événement non valide ou payload incorrecte | Données d’entrée non valides (par exemple, audience, événement ou attribut inexistant) | &#x200B;1. Vérifiez à nouveau la structure de la payload d’entrée/d’événement.<br/>2. Vérifiez que les objets référencés (audiences, jeux de données) existent et sont actifs.<br/>3. Vérifiez que tous les champs obligatoires sont présents.<br/>4. Testez avec une payload fiable.<br/><br/>**Documentation associée** : [Dépannage de parcours &#x200B;](troubleshooting.md), [configuration d’événements](../event/about-events.md). |
| **CJMRT-130004-400** | Requête incorrecte : entrée incorrecte dans la configuration du nœud ou du canal de parcours | La configuration ou la payload du parcours fait référence à une ressource supprimée ou non valide. | &#x200B;1. Vérifiez la configuration du nœud de parcours.<br/>2. Vérifiez que toutes les ressources référencées (messages, audiences, actions) existent.<br/>3. Corrigez ou mettez à jour les références défectueuses.<br/>4. Recréez la configuration du parcours si nécessaire.<br/><br/>**Documentation associée** : [Création de parcours](journey-gs.md), [actions personnalisées](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | Conflit : la ressource existe déjà. | Tentative de création d’une ressource avec un ID ou un nom en double | &#x200B;1. Utilisez des identifiants et des noms uniques pour toutes les ressources.<br/>2. Recherchez les ressources existantes avec le même identifiant.<br/>3. Supprimez ou renommez des objets en conflit.<br/>4. Consultez les conventions de nommage.<br/><br/>**Documentation associée** : [Création de parcours &#x200B;](journey-gs.md) |
| **CJMRT-170016-400** | Requête incorrecte pendant la configuration/prévisualisation du parcours | Dépendance requise manquante ou lien de modèle défectueux pour la payload | &#x200B;1. Vérifiez que toutes les ressources requises sont actives.<br/>2. Vérifiez que les modèles et les blocs de contenu sont publiés.<br/>3. Vérifiez que toutes les dépendances sont correctement liées.<br/>4. Consultez les résultats du mode test du parcours.<br/><br/>**Documentation associée** : [Tester des parcours](testing-the-journey.md), [dépendances de parcours &#x200B;](journey-gs.md) |
| **CJMRT-080608-400** | Requête incorrecte dans le domaine/canal/délégation | Enregistrements DNS requis ou configuration des e-mails/SMS manquante | &#x200B;1. Terminez la configuration DNS pour les domaines des e-mails.<br/>2. Vérifiez que la délégation des sous-domaines est terminée.<br/>3. Exécutez à nouveau les assistants de configuration.<br/>4. Accordez du temps pour la propagation du DNS (jusqu’à 72 heures).<br/><br/>**Documentation associée** : [Surfaces de canal](../configuration/channel-surfaces.md), [délégation de sous-domaines](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | Erreur interne sur la payload | Bug de données/configuration du serveur principal ou configuration non prise en charge | &#x200B;1. Effectuez à nouveau l’opération.<br/>2. Simplifiez la configuration si vous utilisez des fonctionnalités avancées.<br/>3. Signalez le problème à l’assistance Adobe avec l’identifiant de requête et la payload exacte.<br/>4. Recherchez les problèmes connus dans les notes de mise à jour.<br/><br/>**Documentation associée** : [Dépannage de parcours](troubleshooting.md). |

### CJMMAS : erreurs du service de création de messages {#cjmmas-errors}

Ces erreurs se produisent lors de la création, de la modification ou de la publication de messages, de préréglages et de contenu.

| Code d’erreur | Description | Cause principale | Résolution |
|------------|-------------|-----------|-----------|
| **CJMMAS-1732-500** | Échec de l’épreuve : toutes les ressources ne sont pas publiées lors de l’envoi de l’épreuve/test avec une ressource AEM. | La ressource récemment publiée ne se trouve pas encore dans AJO. Incohérence de l’ID de ressource. Utilisation de référentiels croisés. Décalage de synchronisation AEM | &#x200B;1. Utilisez uniquement les identifiants de ressources publiés à partir du référentiel/de l’environnement approprié.<br/>2. Laissez le temps pour la synchronisation entre AEM et AJO.<br/>3. Réessayez avec une ressource fiable.<br/>4. Vérifiez le statut de publication des ressources dans AEM.<br/><br/>**Documentation associée** : [Intégration de ressources](../integrations/assets.md) |
| **CJMMAS-1069-500** | Erreur interne lors de l’enregistrement ou de la publication du modèle de message | Exception du serveur principal (bug d’infrastructure/de service ou problème de contenu). Balisage/fonctionnalité non pris en charge. | &#x200B;1. Simplifiez ou réduisez la complexité du modèle.<br/>2. Ajoutez à nouveau du contenu progressivement pour identifier le problème.<br/>3. Vérifiez la [page Statut d’Adobe](https://status.adobe.com/fr).<br/>4. Supprimez les fonctionnalités ou le balisage non pris en charge.<br/><br/>**Documentation associée** : [Modèles de contenu](../content-management/content-templates.md) |
| **CJMMAS-1149-400** | Requête incorrecte lors de l’enregistrement d’un message, d’un préréglage ou d’une variante | Champs obligatoires manquants dans le message ou mauvaise configuration | &#x200B;1. Renseignez tous les champs obligatoires (marqués d’un astérisque).<br/>2. Validez la configuration du message/préréglage.<br/>3. Vérifiez les formats et les contraintes des valeurs de champ.<br/>4. Vérifiez les messages de validation dans l’interface d’utilisation.<br/><br/>**Documentation associée** : [Canal d’e-mail](../email/get-started-email.md), [surfaces de canal](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | Entité impossible à traiter dans la modification du préréglage de message | Erreur de validation, champ non pris en charge ou syntaxe incorrecte | &#x200B;1. Corrigez les erreurs de syntaxe/de champ comme indiqué.<br/>2. Faites une comparaison avec une configuration fiable.<br/>3. Utilisez la validation de l’interface d’utilisation des messages avant d’enregistrer.<br/>4. Vérifiez les exigences de champ dans la documentation.<br/><br/>**Documentation associée** : [Préréglages de message](../configuration/channel-surfaces.md), [paramètres d’e-mail](../email/email-settings.md) |
| **CJMMAS-1300-500** | Erreur interne lors de la création du message | Panne du serveur principal en raison d’un problème d’infrastructure, de contenu volumineux ou d’une interruption de service | &#x200B;1. Simplifiez le modèle/contenu (réduisez la taille/la complexité).<br/>2. Effectuez à nouveau l’opération.<br/>3. Enregistrez le travail progressivement.<br/>4. Si l’erreur persiste, signalez-le à l’assistance Adobe.<br/><br/>**Documentation associée** : [Modèles de contenu](../content-management/content-templates.md) |
| **CJMMAS-2001-200** | Statut de réussite mais bannière d’erreur : lien d’exclusion manquant | Lien de désabonnement obligatoire manquant dans la variante d’e-mail | &#x200B;1. Ajoutez un lien d’exclusion/de désabonnement à toutes les variantes d’e-mail.<br/>2. Assurez-vous que le lien est présent dans chaque version linguistique.<br/>3. Utilisez l’assistant de personnalisation pour insérer un lien d’exclusion.<br/>4. Testez toutes les variantes avant la publication.<br/><br/>**Documentation associée** : [Gestion du droit d’opposition](../privacy/opt-out.md), [conception d’e-mail](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | Action interdite lors de la mise à jour/publication d’un modèle ou d’un préréglage | L’utilisateur ou l’utilisatrice ne dispose pas des autorisations/rôles requis ou l’action n’est pas autorisée dans l’état actuel. | &#x200B;1. Vérifiez que l’utilisateur ou l’utilisatrice dispose des autorisations appropriées (gestionnaire des messages, auteur/autrice, etc.).<br/>2. Vérifiez le statut du préréglage ou du modèle (brouillon, publié, archivé).<br/>3. Demandez l’accès à l’administrateur ou administratrice si nécessaire.<br/>4. Vérifiez les affectations de profils de produit.<br/><br/>**Documentation associée** : [Autorisations](../administration/permissions.md), [contrôle d’accès](../administration/permissions-overview.md) |

### CJMCMP : erreurs de campagne {#cjmcmp-errors}

Ces erreurs se produisent lors de la création, de la configuration et de l’activation de la campagne.

| Code d’erreur | Description | Cause principale | Résolution |
|------------|-------------|-----------|-----------|
| **CJMCMP-6003-400** | « Il y a au moins une campagne incorrecte » lors de la publication ou du test d’un parcours/message. | Le nœud référence une campagne manquante, dépubliée ou non valide. Le parcours hérité ou cloné ne crée pas de campagnes intégrées. | &#x200B;1. Ouvrez chaque nœud de message et vérifiez la configuration.<br/>2. Rétablissez la liaison ou ajoutez à nouveau des nœuds de message.<br/>3. Activez le mode test pour forcer la création de campagnes intégrées.<br/>4. Accédez au nouvel assistant de parcours si le problème est fréquent.<br/><br/>**Documentation associée** : [Création de parcours](journey-gs.md), [test de parcours &#x200B;](testing-the-journey.md). |
| **CJMCMP-2003-400** | Bannière d’interface d’utilisation : « L’expérience est incorrecte » dans le concepteur d’e-mails | Expérience/fournisseur de données obsolète ou manquant. Échec du nettoyage de l’expérience, incompatibilité de schéma ou bug de validation de l’interface d’utilisation. | &#x200B;1. Supprimez les champs d’expérience inutilisés.<br/>2. Validez les connexions des schémas et des fournisseurs de données.<br/>3. Rechargez l’interface d’utilisation et effacez la mémoire cache du navigateur.<br/>4. Recréez le nœud/l’e-mail si le problème n’est pas résolu.<br/><br/>**Documentation associée** : [Expériences de contenu](../content-management/content-experiment.md) |
| **CJMCMP-3001-400** | Simulation/prévisualisation : « filtre de type de surface incorrect » | Le nœud créé à l’aide de la structure héritée envoie type=surfaceId, le serveur principal attend brandingPresetId. | &#x200B;1. Supprimez et recréez le nœud concerné.<br/>2. Utilisez la nouvelle version/le nouveau modèle de parcours.<br/>3. Utilisez le mode test pour effacer la configuration.<br/>4. Recréez en bloc des nœuds si le problème est généralisé.<br/><br/>**Documentation associée** : [Surfaces de canal](../configuration/channel-surfaces.md), [simulation de messages](../content-management/preview.md) |
| **CJMCMP-2050-400** | Requête incorrecte dans l’activation ou l’approbation de la campagne | Les références de la campagne ne sont pas valides ou comportent un segment ou une politique manquant. | &#x200B;1. Contrôlez toutes les configurations de nœud de campagne.<br/>2. Vérifiez que les liens de la politique/du segment sont à jour et valides.<br/>3. Mettez à jour avec la configuration appropriée.<br/>4. Testez à nouveau la campagne avant l’activation.<br/><br/>**Documentation associée** : [Création des campagnes](../campaigns/create-campaign.md), [approbation des campagnes](../test-approve/gs-approval.md) |

### CJMTL : erreurs de couche de transport {#cjmtl-errors}

Ces erreurs se produisent lors des opérations de transport et de diffusion des messages.

| Code d’erreur | Description | Cause principale | Résolution |
|------------|-------------|-----------|-----------|
| **CJMTL-010018-422** | « Personnalisation non autorisée dans le nom de domaine » lors de l’enregistrement/de l’envoi de contenu | La validation trop stricte a temporairement interrompu la personnalisation dynamique du domaine href. | &#x200B;1. Refactorisez les liens si vous utilisez des variables de domaine.<br/>2. Vérifiez que la dernière version d’AJO est utilisée.<br/>3. Effectuez à nouveau l’opération.<br/>4. Utilisez des domaines statiques si le problème persiste.<br/><br/>**Documentation associée** : [Syntaxe de personnalisation](../personalization/personalization-syntax.md), [conception d’e-mail](../email/content-from-scratch.md) |
| **CJMTL-010011-422** | Entité impossible à traiter : l’envoi de notifications push/SMS/e-mail échoue et indique « champ non valide ». | Données de payload ou de destinataire/contact manquantes ou non valides | &#x200B;1. Inspectez les journaux pour détecter les erreurs de champ spécifiques.<br/>2. Corrigez des informations de profil/contact.<br/>3. Validez avec le profil de test.<br/>4. Refactorisez le format de payload selon les besoins.<br/><br/>**Documentation associée** : [Gestion des profils](../audience/get-started-profiles.md), [profils de test](../audience/creating-test-profiles.md) |

### CJMRPS : erreurs du service de rapports et d’approvisionnement {#cjmrps-errors}

Ces erreurs se produisent lors des opérations de configuration des rapports et d’approvisionnement des jeux de données.

| Code d’erreur | Description | Cause principale | Résolution |
|------------|-------------|-----------|-----------|
| **CJMRPS-1047-409** | « Conflit. Le jeu de données a déjà été ajouté » lors de l’ajout d’un jeu de données de rapport. | Tentative d’ajout d’un jeu de données déjà configuré | &#x200B;1. Vérifiez la configuration du jeu de données dans les paramètres des rapports.<br/>2. N’ajoutez pas à nouveau les jeux de données déjà présents.<br/>3. Utilisez les listes de contrôle de migration officielles pour les rapports de migration.<br/>4. Supprimez les références de jeux de données en double.<br/><br/>**Documentation associée** : [Vue d’ensemble des rapports](../reports/gs-reports.md), [rapports de campagne](../reports/campaign-global-report-cja.md), [rapports de parcours](../reports/journey-global-report-cja.md). |

## Approche générale de dépannage {#troubleshooting-approach}

Lorsque vous rencontrez un code d’erreur, suivez cette approche systématique :

1. **Identifiez l’erreur** : notez le code d’erreur complet, le statut HTTP et tout message ou ID de requête associé.

2. **Recherchez le service** : utilisez le préfixe du service (CJMPTS, CJMRT, CJMMAS, CJMCMP, CJMTL, CJMRPS) pour identifier le composant concerné.

3. **Vérifiez le code d’état** :
   * **400 (requête incorrecte)** : vérifiez les données d’entrée et la configuration.
   * **403 (Interdit)**: vérifiez les autorisations et les droits d’accès.
   * **409 (Conflit)** : recherchez les ressources en double ou en conflit.
   * **422 (entité non traitable)** : validez des données par rapport aux exigences du schéma.
   * **500 (erreur de serveur interne)** : réessayez et signalez éventuellement le problème à l’assistance.

4. **Vérifiez les modifications récentes** : tenez compte de ce qui a été modifié récemment (mises à jour de parcours, nouvelles campagnes, modifications de configuration, etc.).

5. **Consultez la documentation** : utilisez les liens fournis dans ce guide pour accéder à la documentation détaillée sur la fonctionnalité affectée.

6. **Réessayez si nécessaire** : pour les erreurs de la série 500, réessayez après quelques minutes pour résoudre les problèmes transitoires.

7. **Signalez si nécessaire** : si l’erreur persiste après les étapes de résolution suivantes, contactez l’assistance Adobe et indiquez ce qui suit :
   * Code d’erreur complet
   * ID de requête (si disponible)
   * Procédure à suivre
   * Détails de configuration pertinents

## Bonnes pratiques pour éviter les erreurs courantes {#best-practices}

Utilisez ces pratiques pour réduire les erreurs évitables et améliorer la fiabilité.

### Avant l’activation du parcours {#journey-best-practices}

* **Validez toutes les ressources** : assurez-vous que toutes les audiences référencées, les événements, les sources de données et les actions personnalisées sont correctement configurés.
* **Testez en profondeur** : utilisez le mode test pour identifier les problèmes avant la publication ([En savoir plus](testing-the-journey.md)).
* **Validez les volumes** : utilisez le test à blanc pour valider la portée de l’audience et la logique de branche avant la mise en ligne ([En savoir plus](journey-dry-run.md)).
* **Vérifiez les autorisations** : vérifiez que vous disposez des droits d’accès nécessaires pour tous les composants.
* **Vérifiez les dépendances** : assurez-vous que tous les messages et contenus liés sont publiés.

### Pendant la création des messages {#message-best-practices}

* **Remplissez les champs obligatoires** : renseignez toujours tous les champs obligatoires avant d’enregistrer.
* **Incluez des liens d’exclusion** : ajoutez des liens de désabonnement à toutes les variantes d’e-mail ([En savoir plus](../privacy/opt-out.md)).
* **Validez la personnalisation** : testez tout le contenu dynamique avec des profils types ([En savoir plus](../personalization/personalization-build-expressions.md)).
* **Facilitez la gestion des modèles** : évitez les modèles trop complexes susceptibles de causer des problèmes de rendu.

### Pour la gestion des campagnes {#campaign-best-practices}

* **Vérifiez les données d’audience** : assurez-vous que les audiences cibles sont correctement configurées et renseignées.
* **Vérifiez le statut d’approbation** : comprenez les exigences d’approbation avant de tenter l’activation ([En savoir plus](../test-approve/gs-approval.md)).
* **Configurations du moniteur** : vérifiez régulièrement la validité des surfaces et des préréglages de canal.
* **Planifiez les modifications DNS** : laissez suffisamment de temps à la propagation DNS lors de la mise à jour des domaines.

## Ressources supplémentaires {#additional-resources}

* [Dépannage de parcours](troubleshooting.md)
* [Résolution des problèmes d’exécution](troubleshooting-execution.md)
* [Résolution des problèmes liés aux activités entrantes](troubleshooting-inbound.md)
* [Résolution des problèmes liés aux actions personnalisées](../action/troubleshoot-custom-action.md)
* [Questions fréquentes sur le parcours](journey-faq.md)
* [Mécanismes de sécurisation et limitations](../start/guardrails.md)

## Obtention d’une assistance {#getting-support}

Si vous rencontrez des erreurs persistantes qui ne peuvent pas être résolues à l’aide de ce guide :

1. **Collectez des informations** : collectez le code d’erreur, l’identifiant de requête, la date et l’heure, et les étapes à reproduire.
2. **Vérifiez le statut du système** : consultez le [statut d’Adobe](https://status.adobe.com/fr){target="_blank"} pour connaître les problèmes de service connus.
3. **Recherchez dans la documentation** : consultez [Adobe Experience League](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=fr){target="_blank"} pour trouver des solutions.
4. **Engager la communauté** : Posez vos questions dans la [[!DNL Adobe Journey Optimizer] Communauté](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
5. **Contactez l’assistance Adobe** : envoyez un ticket d’assistance avec tous les détails pertinents.

>[!NOTE]
>
>Cette référence de code d’erreur est continuellement mise à jour au fur et à mesure que de nouveaux codes sont identifiés et documentés. Pour obtenir les informations les plus récentes, consultez régulièrement les [[!DNL Adobe Journey Optimizer] blogs de la communauté](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs){target="_blank"}.

**Rubriques connexes**

* [Démystifier [!DNL Adobe Journey Optimizer] Codes D’Erreur : Partie 1](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884){target="_blank"}
* [Démystifier [!DNL Adobe Journey Optimizer] Codes D’Erreur : Partie 2](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661){target="_blank"}
