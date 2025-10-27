---
solution: Journey Optimizer
product: journey optimizer
title: Référence des codes d’erreur
description: Découvrez les codes d’erreur courants dans Adobe Journey Optimizer et comment les résoudre
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: erreur, codes, dépannage, parcours, campagne, messages
source-git-commit: 584d860d0908f354389037be860757dabe1c1e3f
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 1%

---


# Référence des codes d’erreur {#error-codes}

Adobe Journey Optimizer utilise des codes d’erreur normalisés pour vous aider à identifier et à résoudre rapidement les problèmes liés aux parcours, aux campagnes et aux configurations de messages. La compréhension de ces codes d’erreur peut réduire considérablement le temps de dépannage et vous aider à maintenir des performances optimales de la campagne.

## Comprendre la structure du code d’erreur {#error-code-structure}

Les codes d’erreur Adobe Journey Optimizer suivent un modèle de dénomination cohérent qui permet d’identifier le composant et le type de problème :

* **Préfixe de service** : indique quel service Adobe Journey Optimizer a généré l’erreur (par exemple, CJMPTS pour le service de notification push/transport, CJMRT pour l’exécution du Parcours, CJMMAS pour le service de création de messages).
* **Numéro d’erreur** : identifiant unique de la condition d’erreur spécifique
* **Code d’état HTTP** : Code d’état HTTP standard (par exemple, 400, 403, 422, 500)

Exemple : `CJMRT-030012-422` indique une erreur d’exécution de Parcours (CJMRT) avec le numéro d’erreur 030012 et le statut HTTP 422 (Entité non traitable).

## Où trouver les codes d’erreur {#find-error-codes}

Les codes d’erreur apparaissent à plusieurs emplacements dans Adobe Journey Optimizer :

* Rapports et journaux d’exécution de parcours
* Écrans d’activation de la campagne
* Avertissements relatifs à la validation des messages
* Notifications et alertes système
* Réponses des API (lors de l’utilisation d’API REST)

Lorsqu’une erreur se produit, notez le code d’erreur complet et l’ID de requête qui l’accompagne, car ils sont essentiels pour le dépannage et la réaffectation de l’assistance.

## Codes d’erreur courants par service {#error-codes-by-service}

### CJMPTS : erreurs des services de notification push et de transport {#cjmpts-errors}

Ces erreurs se produisent lors des opérations de diffusion des notifications push et de transport des messages.

| Code d’erreur | Description | Cause principale | Résolution |
|------------|-------------|-----------|-----------|
| **CJMPTS-1510-500** | Erreur de serveur interne lors de l’envoi du canal push | Dysfonctionnement du serveur principal de notifications push/transport ; erreur du fournisseur ou de l’infrastructure | &#x200B;1. Vérifiez les paramètres d’approvisionnement des canaux<br/>2. Vérifiez que les informations d&#39;identification push sont valides<br/>3. Réessayez l’opération<br/>4. En cas de persistance, contactez l’assistance Adobe avec l’ID de demande <br/><br/>**documentation associée** : [configuration push](../push/push-configuration.md) |
| **CJMPTS-1023-500** | Erreur de serveur interne lors de l’envoi/du processus de notifications push (passerelles tierces) | Dysfonctionnement temporaire du cloud ou erreur de service inconnue | &#x200B;1. Vérifiez la configuration du fournisseur/canal<br/>2. Vérifiez le statut de la passerelle tierce<br/>3. Réessayez après quelques minutes<br/>4. Consultez les journaux pour plus d’informations <br/><br/>**contexteDocumentation connexe** : [Notifications push](../push/create-push.md) |
| **CJMPTS-1310-500** | Erreur interne du service de rendu (aperçu ou envoi en direct) | Échec du moteur de rendu de modèle en aval, généralement en raison de problèmes de syntaxe JSON/modèle | &#x200B;1. Validez la syntaxe et la structure du modèle<br/>2. Vérifiez que toutes les variables de personnalisation sont valides<br/>3. Utilisez une payload de test pour identifier le problème<br/>4. Simplifiez la complexité du modèle si nécessaire <br/><br/>**Documentation connexe** : [Modèles de message](../content-management/content-templates.md), [Syntaxe Personalization](../personalization/personalization-syntax.md) |

### CJMRT : erreurs d’exécution de Parcours et d’API {#cjmrt-errors}

Ces erreurs se produisent lors de l’exécution du parcours, du traitement des événements et des opérations de l’API.

| Code d’erreur | Description | Cause principale | Résolution |
|------------|-------------|-----------|-----------|
| **CJMRT-030012-422** | Entité non traitable : action en échec, événement non valide ou payload incorrecte | Données d’entrée non valides (par exemple, audience, événement ou attribut inexistant) | &#x200B;1. Vérifiez à nouveau la structure de la payload d’entrée/d’événement<br/>2. Vérifiez que les objets référencés (audiences, jeux de données) existent et sont actifs<br/>3. Vérifiez que tous les champs obligatoires sont présents<br/>4. Testez avec une payload, dont le fonctionnement a été vérifié&#x200B;<br/><br/>**Documentation connexe** : [Dépannage de Parcours &#x200B;](troubleshooting.md), [Configuration des événements](../event/about-events.md) |
| **CJMRT-130004-400** | Requête incorrecte - entrée incorrecte dans la configuration du nœud ou du canal de parcours | Les références de configuration ou de payload du parcours sont supprimées ou ne sont pas valides | &#x200B;1. Vérifiez la configuration du nœud de parcours <br/>2. Vérifiez que toutes les ressources référencées (messages, audiences, actions) existent<br/>3. Correction ou mise à jour des références rompues<br/>4. Reconstruire la configuration du parcours si nécessaire <br/><br/>**Documentation connexe** : [création du Parcours &#x200B;](journey-gs.md), [Actions personnalisées](../action/about-custom-action-configuration.md) |
| **CJMRT-000032-409** | Conflit - la ressource existe déjà | Tentative de création d’une ressource avec un ID ou un nom en double | &#x200B;1. Utilisez des identifiants et des noms uniques pour toutes les ressources<br/>2. Recherchez les ressources existantes avec le même identifiant<br/>3. Supprimer ou renommer des objets en conflit<br/>4. Consultez les conventions de nommage <br/><br/>**documentation connexe** : [versions de Parcours &#x200B;](journey-gs.md#journey-versions) |
| **CJMRT-170016-400** | Requête incorrecte pendant la configuration/prévisualisation du parcours | Dépendance requise manquante ou lien de modèle rompu pour la payload | &#x200B;1. Vérifiez que toutes les ressources requises sont actives<br/>2. Vérifiez que les modèles et les blocs de contenu sont publiés<br/>3. Vérifiez que toutes les dépendances sont correctement liées<br/>4. Consultez les résultats du mode parcours test <br/><br/>**documentation connexe** : [Test des parcours &#x200B;](testing-the-journey.md), [dépendances de Parcours &#x200B;](journey-gs.md) |
| **CJMRT-080608-400** | Requête incorrecte dans le domaine/canal/délégation | Enregistrements DNS requis ou configuration d’e-mail/SMS manquante | &#x200B;1. Configuration DNS complète pour les domaines de messagerie<br/>2. Vérifiez que la délégation des sous-domaines est terminée<br/>3. Exécutez à nouveau les Assistants Configuration<br/>4. Accordez du temps pour la propagation du DNS (jusqu’à 72 heures)<br/><br/>**Documentation connexe** : [Surfaces de canal](../configuration/channel-surfaces.md), [Délégation de sous-domaine](../configuration/delegate-subdomain.md) |
| **CJMRT-110100-500** | Erreur interne sur la payload | Bogue de données/configuration du serveur principal ou configuration non prise en charge | &#x200B;1. Réessayez l’opération<br/>2. Simplifiez la configuration si vous utilisez des fonctionnalités avancées<br/>3. Transmettez-le au support Adobe avec l’identifiant de requête et la payload exacte<br/>4. Recherchez les problèmes connus dans les notes de mise à jour <br/><br/>**documentation connexe** : [Dépannage du Parcours &#x200B;](troubleshooting.md) |

### CJMAS : erreurs du service de création de messages {#cjmmas-errors}

Ces erreurs se produisent lors de la création, de la modification ou de la publication de messages, de préréglages et de contenu.

| Code d’erreur | Description | Cause principale | Résolution |
|------------|-------------|-----------|-----------|
| **CJMMAS-1149-400** | Requête incorrecte lors de l’enregistrement d’un message, d’un préréglage ou d’une variante | Champs obligatoires manquants dans le message ou mauvaise configuration | &#x200B;1. Renseignez tous les champs obligatoires (marqués d’un astérisque)<br/>2. Validez la configuration du message/préréglage<br/>3. Vérifiez les formats et les contraintes des valeurs de champ<br/>4. Consultez les messages de validation dans l’interface utilisateur <br/><br/>**documentation connexe** : [canal e-mail](../email/get-started-email.md), [surfaces de canal](../configuration/channel-surfaces.md) |
| **CJMMAS-2073-422** | Entité impossible à traiter dans la modification du préréglage de message | Erreur de validation, champ non pris en charge ou syntaxe incorrecte | &#x200B;1. Corrigez les erreurs de syntaxe/de champ comme indiqué<br/>2. Comparez-la à une configuration dont le fonctionnement a été vérifié<br/>3. Utilisez la validation de l’interface utilisateur des messages avant d’enregistrer<br/>4. Consultez les exigences de champ dans la documentation <br/><br/>**documentation connexe** : [Préréglages de message](../configuration/channel-surfaces.md), [Paramètres d’e-mail](../email/email-settings.md) |
| **CJMMAS-1300-500** | Erreur interne lors de la création du message | Panne du serveur principal en raison d’un problème d’infrastructure, de contenu volumineux ou d’une interruption de service | &#x200B;1. Simplifiez le modèle/contenu (réduisez la taille/la complexité)<br/>2. Réessayez l’opération<br/>3. Enregistrez le travail de manière incrémentielle<br/>4. Si l’erreur persiste, signalez-le à l’assistance Adobe <br/><br/>**documentation connexe** : [Modèles de contenu](../content-management/content-templates.md) |
| **CJMMAS-2001-200** | Statut de réussite mais bannière d’erreur : lien d’opt-out manquant | Lien de désabonnement obligatoire manquant dans la variante d’e-mail | &#x200B;1. Ajoutez un lien d’exclusion/de désabonnement à toutes les variantes d’e-mail<br/>2. Assurez-vous que le lien est présent dans chaque version <br/> langue 3. Utilisez l’assistant de personnalisation pour insérer un lien d’exclusion<br/>4. Tester toutes les variantes avant la publication <br/><br/>**Documentation connexe** : [Gestion du processus d’opt-out](../privacy/opt-out.md), [Conception d’e-mail](../email/content-from-scratch.md) |
| **CJMMAS-1603-403** | Interdit lors de la mise à jour/publication d’un modèle ou d’un préréglage | L’utilisateur ne dispose pas des autorisations/rôles requis ou l’action n’est pas autorisée dans l’état actuel | &#x200B;1. Vérifiez que l’utilisateur dispose des autorisations appropriées (Gestionnaire des messages, Auteur, etc.)<br/>2. Vérifiez le statut du paramètre prédéfini/du modèle (brouillon, publié, archivé)<br/>3. Demandez l’accès à l’administrateur si nécessaire<br/>4. Consultez les affectations de profils de produit <br/><br/>**documentation connexe** : [Autorisations](../administration/permissions.md), [Contrôle d’accès](../administration/permissions-overview.md) |

### CJMCMP : erreurs de campagne {#cjmcmp-errors}

Ces erreurs se produisent lors de la création, de la configuration et de l’activation de la campagne.

| Code d’erreur | Description | Cause principale | Résolution |
|------------|-------------|-----------|-----------|
| **CJMCMP-2050-400** | Requête incorrecte dans l’activation ou la validation de la campagne | Les références de la campagne ne sont pas valides ou comportent un segment ou une politique manquant | &#x200B;1. Contrôlez toutes les configurations de nœud de campagne<br/>2. Vérifiez que les liens de la politique/du segment sont à jour et valides<br/>3. Mettez à jour avec la configuration appropriée<br/>4. Tester à nouveau la campagne avant l’activation <br/><br/>**Documentation connexe** : [création de campagne](../campaigns/create-campaign.md), [validation de la campagne](../test-approve/gs-approval.md) |

## Approche générale de dépannage {#troubleshooting-approach}

Lorsque vous rencontrez un code d’erreur, suivez cette approche systématique :

1. **Identifier l’erreur** : notez le code d’erreur complet, le statut HTTP et tout message ou ID de requête associé.

2. **Rechercher le service** : utilisez le préfixe du service (CJMPTS, CJMRT, CJMMAS, CJMCMP) pour identifier le composant concerné.

3. **Vérifiez le code d’état** :
   * **400 (requête incorrecte)** : vérifiez les données d’entrée et la configuration
   * **403 (Interdit)** vérifier les autorisations et les droits d’accès
   * **409 (Conflit)** : Recherchez les ressources en double ou en conflit
   * **422 (entité non traitable)** : validation des données par rapport aux exigences du schéma
   * **500 (erreur de serveur interne)** : réessayez et réaffectez éventuellement le problème à l’assistance

4. **Vérifier les modifications récentes** : tenir compte de ce qui a été modifié récemment (mises à jour de parcours, nouvelles campagnes, modifications de configuration, etc.).

5. **Consulter la documentation** : utilisez les liens fournis dans ce guide pour accéder à la documentation détaillée sur la fonctionnalité affectée.

6. **Réessayer si nécessaire** : pour les erreurs de la série 500, une simple reprise après quelques minutes résout souvent les problèmes transitoires.

7. **Escalader si nécessaire** : si l’erreur persiste après les étapes de résolution suivantes, contactez l’assistance Adobe à l’adresse :
   * Code d’erreur complet
   * ID de requête (si disponible)
   * Procédure à suivre
   * Détails de configuration pertinents

## Bonnes pratiques pour éviter les erreurs courantes {#best-practices}

### Avant activation du parcours {#journey-best-practices}

* **Valider toutes les ressources** : assurez-vous que toutes les audiences référencées, les sources de données et les actions personnalisées sont actives
* **Test approfondi** : utilisez le mode test pour identifier les problèmes avant la publication ([En savoir plus](testing-the-journey.md)).
* **Vérification des autorisations** : vérifiez que vous disposez des droits d’accès nécessaires pour tous les composants
* **Vérifier les dépendances** : assurez-vous que tous les messages et contenus liés sont publiés

### Lors de la création de messages {#message-best-practices}

* **Remplir les champs obligatoires** : toujours remplir tous les champs obligatoires avant d’enregistrer
* **Inclure des liens de désabonnement** : ajoutez des liens de désabonnement à toutes les variantes d’e-mail ([En savoir plus](../privacy/opt-out.md)).
* **Valider la personnalisation** : tester tout le contenu dynamique avec des profils types ([En savoir plus](../personalization/personalization-build-expressions.md))
* **Faciliter la gestion des modèles** : évitez les modèles trop complexes susceptibles de causer des problèmes de rendu

### Pour la gestion des campagnes {#campaign-best-practices}

* **Vérification des données d’audience** : assurez-vous que les audiences cibles sont correctement configurées et renseignées
* **Vérifier le statut d’approbation** : comprendre les exigences d’approbation avant de tenter l’activation ([En savoir plus](../test-approve/gs-approval.md))
* **Configurations du moniteur** : vérifiez régulièrement la validité des surfaces et des préréglages de canal
* **Planifier les modifications DNS** : laissez suffisamment de temps à la propagation DNS lors de la mise à jour des domaines

## Ressources supplémentaires {#additional-resources}

* [Dépannage de parcours](troubleshooting.md)
* [Résolution des problèmes d’exécution](troubleshooting-execution.md)
* [Résolution des problèmes liés aux activités entrantes](troubleshooting-inbound.md)
* [Dépannage des actions personnalisées](../action/troubleshoot-custom-action.md)
* [FAQ sur le parcours](journey-faq.md)
* [Mécanismes de sécurisation et limitations](../start/guardrails.md)

## Obtention d’une assistance {#getting-support}

Si vous rencontrez des erreurs persistantes qui ne peuvent pas être résolues à l’aide de ce guide :

1. **Collecter des informations** : collecter le code d’erreur, l’identifiant de requête, les horodatages et les étapes à reproduire
2. **Vérification de l’état du système** : consultez [État d’Adobe](https://status.adobe.com/fr){target="_blank"} pour connaître les problèmes de service connus
3. **Rechercher dans la documentation** : consultez [Adobe Experience League](https://experienceleague.adobe.com/docs/journey-optimizer.html?lang=fr){target="_blank"} pour trouver des solutions.
4. **Engager la communauté** : posez des questions dans la communauté [Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer?profile.language=fr){target="_blank"}
5. **Contactez l’assistance Adobe** : envoyez un ticket d’assistance avec tous les détails pertinents

>[!NOTE]
>
>Cette référence de code d’erreur est continuellement mise à jour au fur et à mesure que de nouveaux codes sont identifiés et documentés. Pour obtenir les informations les plus récentes, consultez régulièrement les [blogs de la communauté Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/bg-p/journey-optimizer-blogs?profile.language=fr){target="_blank"}.

**Rubriques connexes**

* [Démystifier les codes d’erreur Adobe Journey Optimizer : partie 1](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/ba-p/760884?profile.language=fr){target="_blank"}
* [Démystifier les codes d’erreur Adobe Journey Optimizer : partie 2](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/demystifying-adobe-journey-optimizer-error-codes-root-causes-and/bc-p/782661?profile.language=fr){target="_blank"}

