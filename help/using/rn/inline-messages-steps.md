---
title: Étapes de migration vers la création en ligne de parcours
description: Étapes de migration vers la création en ligne de parcours
exl-id: 8412a0bd-674c-4d6a-aa5b-443655d2943a
source-git-commit: 1ab038e8b2f0582ad947400c7d070a70e1a84b9b
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 100%

---

# Étapes de migration vers la création en ligne{#migration-steps}

Le nouveau processus de création de contenu dans Adobe Journey Optimizer est décrit dans cette [page](../rn/inline-messages.md). Une conversion automatique de parcours est effectuée pour vous. Cela dit, nous avons besoin de votre aide pour certaines étapes.

>[!VIDEO](https://video.tv.adobe.com/v/344699)

Les principales phases et étapes sont les suivantes :

**[Avant la migration](../rn/inline-messages-steps.md#migration-step-1)**

1. Sur les sandbox hors production, arrêtez tous les parcours actifs et fermés. [En savoir plus](../rn/inline-messages-steps.md#migration-step-1-1)
1. Sur la sandbox de production, arrêtez tous les parcours ad hoc actifs sans profil. [En savoir plus](../rn/inline-messages-steps.md#migration-step-1-2)

**[Après la première itération](../rn/inline-messages-steps.md#migration-step-2)**

1. Vérifiez si des erreurs se sont glissées sur vos parcours actifs migrés. [En savoir plus](../rn/inline-messages-steps.md#migration-step-2-1)
1. Répertoriez toutes les nouvelles versions créées par la migration. [En savoir plus](../rn/inline-messages-steps.md#migration-step-2-2)
1. Testez-les et publiez-les l’une après l’autre. [En savoir plus](../rn/inline-messages-steps.md#migration-step-2-3)
1. Répertoriez toutes les versions actives. [En savoir plus](../rn/inline-messages-steps.md#migration-step-2-4)
1. Recherchez les erreurs sur les brouillons migrés. [En savoir plus](../rn/inline-messages-steps.md#migration-step-2-5)

**[Après la seconde itération](../rn/inline-messages-steps.md#migration-step-3)**

1. Vérifiez les deux phases de migration. [En savoir plus](../rn/inline-messages-steps.md#migration-step-3-1)
1. Arrêtez les versions précédentes. [En savoir plus](../rn/inline-messages-steps.md#migration-step-3-2)

**[Avant la troisième et dernière itération](../rn/inline-messages-steps.md#migration-step-4)**

Vérifiez que tout a été migré avant l’obsolescence.

<br> 

## Avant la migration (25 juillet){#migration-step-1}

### 1. Arrêtez tous les parcours actifs et fermés{#migration-step-1-1}

Sur les **sandboxes hors production**, arrêtez tous les parcours actifs et fermés. Cela permet au processus de migration automatique de migrer tous les parcours de ces sandboxes sans aucune action de votre part. Après la migration, vous pourrez dupliquer les versions de parcours arrêtées et les utiliser.

### 2. Arrêtez tous les parcours ad hoc actifs sans profil encore présent{#migration-step-1-2}

Sur la **sandbox de production**, arrêtez tous les parcours ad hoc actifs qui ne contiennent plus de profils.

+++Comment trouver ces parcours ?

Pour trouver ces parcours, accédez au menu **Parcours** et filtrez la liste sur « Statut = Actif » et « Type = Lecture de segment ». Vous pouvez également classer les parcours par ordre chronologique, de la date de publication la plus ancienne à la plus récente.

![](assets/inline-migration-steps1.png)

Ouvrez-les de haut en bas.

* Vérifiez que le parcours a un message.
* Vérifiez qu’il ne s’agit pas de parcours récurrents. Ce ne sont pas des parcours ad hoc. Vous souhaitez très probablement les garder actifs. Par exemple, celui-ci est un parcours récurrent (et non ad hoc) :

   ![](assets/inline-migration-steps2.png)

* Si vous avez utilisé des récepteurs d’attente ou d’événement dans ces parcours, les profils peuvent encore être à l’intérieur. Examinez la date d’exécution du parcours et ajoutez les heures/jours que vous avez définis dans vos récepteurs d’attente ou d’événements pour déduire la date réelle à laquelle il n’y a plus de profils à l’intérieur. Si cette date est passée, vous pouvez arrêter le parcours. Sinon, ce parcours passe automatiquement au statut « Terminé » 30 jours après la date de son exécution.

+++

**Remarques importantes**

* Évitez de fermer les parcours avant la date de migration (25 juillet). Sachant que le script de migration ne migrera pas les parcours actifs ou fermés, limiter le nombre de parcours fermés dans la sandbox de production limitera également le nombre d’actions manuelles nécessaires après la migration.

* Si vous avez des parcours actifs qui ne sont pas de la dernière version, c’est-à-dire que vous avez créé une autre version de parcours dans le brouillon, publiez-la ou supprimez-la.

* Si des messages ne sont pas utilisés dans les parcours et que vous souhaitez les conserver, enregistrez-les en tant que modèles. Voir cette [page](../design/email-templates.md#save-as-template). Notez que vous pourrez toujours y accéder jusqu’à leur obsolescence.

## Après la première itération de la migration (25 juillet){#migration-step-2}

La migration se déroule en deux phases : la phase automatique (de nuit, entre le 25 et le 26 juillet) et la phase manuelle (à partir du 26 juillet) qui nécessite des éléments d’action.

Pour la phase automatisée, reportez-vous à cette [page](../rn/inline-messages.md#process). Pour la phase manuelle, voici les actions à effectuer sur la **sandbox de production** :

<!--
_On non-production sandboxes:_

**1. Check the migration status report for any error**

Click the **Check status** button in the top banner and check that there has been no error during the automatic migration and that there is nothing left to migrate. 

![](assets/inline-migration-steps3.png)

Look for the "ERROR" status. 

![](assets/inline-migration-steps4.png)

* If there is no error, you are good to go.
* If there are errors, look for the error by searching "errorMessage". The following error is expected as migration of multi-channel messages is not supported: "Migration of multi-channel messages is not supported". You will have to rebuild this journey.

    ![](assets/inline-migration-steps5.png)

_On the production sandbox:_

-->

### 1. Vérifiez si des erreurs se sont glissées sur vos parcours actifs migrés.{#migration-step-2-1}

Vérifiez les erreurs éventuelles sur les parcours actifs migrés automatiquement dans le rapport de statut ([en savoir plus](../rn/inline-messages.md#status)). Cliquez sur le bouton **Vérifier le statut** dans la bannière supérieure.

![](assets/inline-migration-steps3.png)

Recherchez &quot;ERROR_NEW_VERSION_CREATION&quot; :

![](assets/inline-migration-steps6.png)

* En l’absence d’erreur, cela signifie que toutes les versions de parcours actives nécessitant une migration ont été traitées et qu’un nouveau brouillon migré a été automatiquement créé.

* Si une erreur s’affiche, vous pouvez rechercher &quot;errorMessage&quot; et vérifier le message d’erreur dans les journaux. Les messages multicanaux ne sont pas migrés. Vous devrez créer un autre parcours.

   ![](assets/inline-migration-steps5.png)

* Pour toute autre erreur, veuillez contacter votre CSM ou tout représentant Adobe pour obtenir des conseils.

### 2. Répertoriez toutes les nouvelles versions créées par la migration{#migration-step-2-2}

Elles sont marquées comme [MIGRÉE] dans le libellé du parcours et la date de création est mise à jour.

![](assets/inline-migration-steps7.png)

### 3. Testez-les et publiez-les l’une après l’autre{#migration-step-2-3}

Vérifiez que le parcours doit toujours être exécuté en production. Si la [préparation avant migration](../rn/inline-messages-steps.md#migration-step-1) n’a pas été correctement effectuée, vous pourriez avoir une nouvelle version créée pour un parcours ponctuel qui n’est plus nécessaire.

Testez votre brouillon du parcours qui contient désormais des actions de canal en ligne.

Publiez votre nouvelle version de parcours. La version active précédente passe alors au statut « Fermé ».

### 4. Répertoriez toutes les versions actives{#migration-step-2-4}

Elles devraient toutes être marquées comme récentes. Dans le cas contraire, recherchez la version la plus récente, testez-la et publiez-la.

![](assets/inline-migration-steps8.png)

### 5. Recherchez les erreurs sur les brouillons migrés {#migration-step-2-5}

Cliquez sur le bouton **Vérifier le statut** dans la bannière supérieure ([en savoir plus](../rn/inline-messages.md#status)) et vérifiez qu’il n’y a pas eu d’erreur lors de la migration automatique et qu’il n’y a plus rien à migrer. N’oubliez pas que tout parcours avec des erreurs (avec des messages) sera obsolète après le 5 septembre (sur toutes les sandboxes).

![](assets/inline-migration-steps11.png)

Recherchez le statut &quot;ERROR&quot;.

![](assets/inline-migration-steps9.png)

* S’il n’y a pas d’erreur, tout est prêt.

* S’il y a des erreurs, trouvez-les en cherchant &quot;errorMessage&quot;. L’erreur suivante est attendue, car la migration des messages multicanaux n’est pas prise en charge : &quot;La migration des messages multicanaux n’est pas prise en charge&quot;. Vous devrez reconstruire ce parcours.

![](assets/inline-migration-steps5.png)

## Après la deuxième itération (1er août){#migration-step-3}

La deuxième itération a lieu la nuit entre le 1er et le 2 août.

<!--
_On non-production sandboxes:_

**1. Check at the status report**

Click the **Check status** button in the top banner and check that all journeys have been migrated and there's nothing left to migrate. If there is an error or something left to migrate, please reach out to your CSM or Adobe representative for guidance.

-->

Si toutes les étapes précédentes ont été effectuées à temps, tous vos parcours ont été migrés, sauf ceux qui sont fermés et ceux qui contiennent des erreurs. Voici les étapes à suivre sur la **sandbox de production** :

### 1. Vérifiez les deux phases de migration{#migration-step-3-1}

S’il n’y a pas d’erreurs, vous ne devriez pas avoir de parcours avec le statut &quot;eligibilityStatus&quot;, sous &quot;toMigrate&quot; et &quot;createNewVersion&quot;. Dans l’exemple suivant, il y a une &quot;ERROR&quot; et une &quot;ERROR_NEW_VERSION_CREATION&quot;.

![](assets/inline-migration-steps10.png)

### 2. Arrêtez les versions précédentes{#migration-step-3-2}

Si vous n’avez pas publié de nouvelles versions de parcours (voir cette [section](../rn/inline-messages-steps.md#migration-step-2-3)) à temps, c’est-à-dire avant l’itération 2 (1er août), alors publiez la version la plus récente.

>[!NOTE]
>
>Arrêtez la version précédente ou vous la perdrez, ainsi que les rapports associés.

## Avant la troisième et dernière itération (5 septembre){#migration-step-4}

Entre le 1er août et le 5 septembre, vous devrez vérifier que tout a été migré et qu’il n’y a plus aucun parcours utilisant des messages. Sinon, ils seront obsolètes le 5 septembre.
