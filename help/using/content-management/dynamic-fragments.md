---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation de fragments dynamiques
description: Découvrez comment utiliser la résolution dynamique de fragment dans Adobe Journey Optimizer pour sélectionner et injecter des fragments au moment de l’exécution en fonction des attributs de profil, des recherches de jeux de données ou des données contextuelles.
feature: Fragments
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: dynamique, fragment, expression, personnalisation, exécution
source-git-commit: b4affc5b905236419928a65cd173173b49058827
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 3%

---

# Utilisation de fragments dynamiques {#dynamic-fragments}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment utiliser la résolution de fragment dynamique dans Adobe Journey Optimizer pour sélectionner le fragment publié qui est injecté dans un message au moment de l’exécution, en fonction des attributs de profil, des recherches de jeux de données ou des données contextuelles transmises au moment de l’envoi.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] prend en charge la **résolution de fragment dynamique** au moment de l’exécution, ce qui vous permet de sélectionner le fragment publié qui est injecté dans un message en fonction des attributs de profil, des recherches de jeux de données ou des données contextuelles transmises au moment de l’envoi. Cela permet d’obtenir du contenu hautement personnalisé sans dupliquer la logique de campagne ou de parcours.

## Vue d’ensemble {#overview}

Les **fragments statiques** sont incorporés dans un message au moment de la conception ; le même fragment est utilisé pour chaque destinataire. **Les fragments dynamiques** résolvent l’identifiant de fragment au moment de l’exécution par destinataire, ce qui signifie que différents profils peuvent recevoir des blocs de contenu entièrement différents dans la même campagne ou le même parcours.

Les identifiants de fragments dynamiques peuvent provenir de trois sources :

* Une **recherche de jeu de données** par exemple, un jeu de données de recommandations indexé par style ou produit
* Un **attribut de profil** stocké dans Adobe Experience Platform
* **Données contextuelles** transmises directement dans la requête API au moment de l’envoi

>[!NOTE]
>
>L’utilisation de la fonction d’assistance `datasetLookup` dans les fragments d’expression est actuellement disponible pour un nombre limité de clientes et clients. Pour en bénéficier, contactez votre représentant ou représentante Adobe.

## Conditions préalables {#prerequisites}

Avant d’utiliser des fragments dynamiques, assurez-vous que les éléments suivants sont en place :

* Vous disposez des autorisations requises pour créer et publier des fragments dans [!DNL Journey Optimizer]. [En savoir plus](../administration/ootb-product-profiles.md#content-library-manager)
* Le fragment que vous souhaitez référencer est **publié** (statut : **En ligne**). Les brouillons de fragments ne peuvent pas être résolus au moment de l’exécution.
* Si vous résolvez l’ID de fragment à partir d’un jeu de données, le schéma du jeu de données inclut un champ qui stocke l’ID de fragment, et le jeu de données est [activé pour la recherche](../data/lookup-aep-data.md).
* Tous les attributs de profil auxquels le fragment dynamique lui-même fait référence sont inclus dans le chemin d’exportation du message ou sont disponibles dans le profil au moment de l’envoi.

>[!CAUTION]
>
>Les validations liées aux fragments sont ignorées dans le flux de fragment dynamique. Les identifiants de fragment non valides apparaissent comme des échecs de diffusion d’exécution plutôt que comme des erreurs de validation initiale. Vérifiez toujours que les identifiants de fragment référencés sont valides et publiés avant d’activer une campagne.

## Étape 1 : créer et publier le fragment {#create-fragment}

Avant de référencer un fragment de manière dynamique, il doit être publié dans [!DNL Journey Optimizer].

1. Dans [!DNL Journey Optimizer], accédez à **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Fragments]**.

1. Sélectionnez **[!UICONTROL Créer un fragment]** et créez le contenu. [Découvrez comment créer des fragments](create-fragments.md)

1. Lorsque le contenu est prêt, cliquez sur **[!UICONTROL Publier]**. La publication est asynchrone et peut prendre quelques secondes. Vérifiez que le fragment passe à l’état **actif** avant de continuer.

1. Notez l’**ID de fragment** dans la vue des détails du fragment ou dans la réponse de l’API Fragments. Vous référencerez cet identifiant dans le message.

>[!NOTE]
>
>Vous pouvez récupérer tous les identifiants de fragment publiés par programmation à l’aide de l’API `GET /fragments`. Consultez la documentation des API Journey Optimizer [](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"} pour plus d’informations.

## Étape 2 : créez le message avec une référence de fragment dynamique {#author-message}

Dans l’éditeur de personnalisation, insérez l’espace réservé du fragment dynamique en utilisant la syntaxe suivante :

```handlebars
{{fragment id=dynamic_fragment_id}}
```

L’identifiant `dynamic_fragment_id` est un nom de variable. Sa valeur doit être résolue avant que la recherche de fragment ne soit effectuée. Vous la résolvez à l’aide d’une expression de recherche de jeu de données, d’un attribut de profil ou de données contextuelles.

### Résoudre à partir d’une recherche de jeu de données {#resolve-from-dataset}

Si l’identifiant du fragment est stocké dans un jeu de données AEP (par exemple, une table de mappage style-à-fragment), utilisez la fonction d’assistance `datasetLookup` pour le résoudre :

```handlebars
{{
  {datasetLookup datasetId="<your-dataset-id>" key=profile.style attribute="fragmentId"}
}}

{{fragment id=dynamic_fragment_id}}
```

Dans cet exemple, le jeu de données contient des lignes indexées par une valeur de style (telle que `style1`). Pour un profil donné, la recherche récupère la valeur de la colonne `fragmentId` correspondante et l’affecte à `dynamic_fragment_id`, qui est ensuite utilisée pour résoudre le fragment.

>[!NOTE]
>
>L’utilisation de la fonction d’assistance `datasetLookup` dans les fragments d’expression est actuellement disponible pour un nombre limité de clientes et clients. Pour en bénéficier, contactez votre représentant ou représentante Adobe. Pour plus d’informations sur les recherches de jeux de données dans la personnalisation, consultez [Utilisation des données Adobe Experience Platform](../data/lookup-aep-data.md).

### Résoudre à partir des données contextuelles {#resolve-from-context}

Si l’ID de fragment est fourni au moment de l’envoi dans le contexte de la requête API, référencez-le à l’aide de l’espace de noms `context` :

```handlebars
{{fragment id=context.audiencePayload.fragmentId}}
```

Le chemin d’accès `context.audiencePayload` est le préfixe requis pour tous les attributs provenant d’un fichier d’audience CSV ou transmis via le contexte de la requête API. Le nom de la colonne du fichier CSV (par exemple, `fragmentId`) suit le préfixe .

### Résoudre à partir d’un attribut de profil {#resolve-from-profile}

Si l’identifiant du fragment est stocké en tant qu’attribut de profil dans Adobe Experience Platform, référencez-le directement :

```handlebars
{{fragment id=profile.mi.fragmentId}}
```

## Étape 3 : Configurer votre jeu de données pour l’approche de recherche {#configure-dataset}

Si vous utilisez l’approche de recherche de jeu de données, mettez à jour le schéma et les données du jeu de données pour qu’ils contiennent l’identifiant du fragment.

1. Dans votre jeu de données de recommandations ou de mappage, ajoutez une colonne (par exemple, `fragmentId`) qui stocke l’identifiant du fragment AJO publié pour chaque ligne.

1. Pour chaque style ou variante (par exemple, `style1`, `style2`), renseignez la colonne `fragmentId` avec l’identifiant de fragment correspondant.

1. Assurez-vous que le jeu de données est ingéré dans Adobe Experience Platform et [ activé pour la recherche](../data/lookup-aep-data.md).

1. Vérifiez que tous les attributs de profil référencés dans le fragment dynamique sont capturés dans le message ou dans un fragment statique afin d’empêcher tout rendu vide au moment de l’exportation.

**Exemple de structure de jeu de données :**

| Colonne | Exemple de valeur |
|---|---|
| style | style1 |
| fragmentId | &lt;fragment-id-1> |
| style | style2 |
| fragmentId | &lt;fragment-id-2> |

## Étape 4 : transmettre les données contextuelles au moment de l’envoi {#pass-context-data}

Si vous résolvez l’ID de fragment à partir des données contextuelles (par exemple, à partir d’un fichier de recommandation d’audience CSV), transmettez l’ID de fragment dans la requête API sous le préfixe de contexte requis.

Lors de l&#39;utilisation de l&#39;API de relecture Campaign, incluez l&#39;identifiant du fragment dans l&#39;objet `context` :

```json
{
  "recipients": [
    {
      "userId": "<profile-email>",
      "namespace": "email"
    }
  ],
  "inChannelData": {
    "channel": "email",
    "emailAddresses": ["<delivery-address>"]
  },
  "context": {
    "audiencePayload": {
      "fragmentId": "<published-fragment-id>",
      "systemSource": "<optional-system-value>"
    }
  }
}
```

Le préfixe `context.audiencePayload` est obligatoire. Les attributs imbriqués sous cette clé mappent directement aux colonnes du fichier d’audience CSV lors de l’exécution de la campagne active.

## Étape 5 : Vérifier et valider {#proof-validate}

Avant d’activer la campagne, utilisez l’API de vérification de campagne pour vérifier que le fragment dynamique est correctement résolu et que la sortie d’e-mail générée est correcte.

1. Déclenchez une tâche d’épreuve à l’aide du point d’entrée `POST /campaigns/{id}/proofs`. Dans la demande de BAT, transmettez l’identifiant de fragment à tester sous `context.audiencePayload.fragmentId`.

1. Interroger le statut de la tâche d’épreuve à l’aide du point d’entrée `GET /campaigns/{id}/proofs/{proofId}` jusqu’à ce que le statut soit `Submitted` ou `Failed`.

1. Vérifiez l’e-mail diffusé pour vous assurer que le fragment de contenu correct est rendu.

1. Si le contenu du fragment est manquant ou incorrect, vérifiez que l’identifiant du fragment est valide, que le fragment est publié et que tous les attributs de profil requis sont présents.

Pour plus d&#39;informations sur l&#39;API Campaign, consultez la documentation des API Journey Optimizer [](https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve){target="_blank"}.

## Mécanismes de sécurisation et limitations {#guardrails}

>[!CAUTION]
>
>OLAC (Object-Level Access Control) n’est pas appliqué pour les fragments dans le modèle de fragment dynamique. Assurez-vous que vos exigences de contrôle d’accès sont prises en compte au niveau de la campagne et de l’audience.

Les restrictions suivantes s’appliquent lors de l’utilisation de fragments dynamiques :

* **Couverture des attributs de profil au moment de l’exportation** : le fragment est choisi au moment de l’exécution par profil. Les attributs de profil requis par le fragment dynamique ne sont pas connus à l’avance. Si le fragment dynamique repose sur un attribut de profil qui n’était pas présent dans le message d’origine ou dans tout fragment statique référencé dans le message, ce champ peut devenir vide dans le chemin d’exportation.

* **Aucune validation de fragment initiale** : les validations liées aux fragments sont ignorées dans ce flux. Les identifiants de fragment incorrects ou dépubliés apparaissent comme des échecs de diffusion d’exécution plutôt que comme des erreurs de validation affichées dans l’interface utilisateur.

* **Modification du schéma requise pour l’approche par jeu de données** : l’utilisation du chemin de recherche par ID nécessite la mise à jour du schéma du jeu de données pour stocker et transmettre l’identifiant du fragment, ainsi que la plomberie nécessaire pour l’alimenter dans le pipeline de messages.

* **Capture d’attributs pour l’exportation** : assurez-vous que tous les attributs utilisés dans le fragment dynamique sont capturés dans le message ou dans des fragments statiques pour empêcher tout rendu vide dans le chemin d’exportation.

D’autres mécanismes de sécurisation s’appliquant aux fragments sont disponibles dans [cette section](../start/guardrails.md#fragments-guardrails).

## Traitement des erreurs {#error-handling}

Si la résolution d’un fragment dynamique échoue au moment de l’exécution, un événement d’exclusion est généré pour le profil affecté. Actuellement, tous les échecs de rendu de fragment sont classés comme un type d’erreur globale unique.

Pour déboguer les échecs de résolution de fragment :

1. Vérifiez les rapports de diffusion de la campagne pour les événements d’exclusion.
1. Vérifiez que l’ID de fragment transmis au moment de l’exécution correspond à un fragment publié.
1. Vérifiez que tous les attributs de profil requis par le fragment sont présents dans le profil au moment de l’envoi.
1. Utilisez l’[API de relecture](#proof-validate) pour tester des identifiants de fragment spécifiques avant d’activer la campagne.
