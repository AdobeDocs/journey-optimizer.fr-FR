---
title: Utilisation d’actions personnalisées
description: Découvrez comment utiliser des actions personnalisées
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: ht
source-wordcount: '326'
ht-degree: 100%

---

# Utilisation d’actions personnalisées {#section_f2c_hbg_nhb}

Le volet de configuration des activités affiche les paramètres de configuration de l’URL et les paramètres d’authentification configurés pour l’action personnalisée. [En savoir plus](../action/about-custom-action-configuration.md).

>[!NOTE]
>
>Vous ne pouvez pas transmettre une simple collection dans les paramètres d’une action personnalisée. Les champs de collection plus complexes (tableaux d’objets) ne sont pas pris en charge.  Notez également qu’un format spécifique est attendu pour les paramètres (par exemple : chaîne, décimal, etc.). Vous devez veiller au respect de cette exigence.

## Configuration d&#39;URL

### Chemin dynamique

Si l’URL contient un chemin dynamique, spécifiez le chemin dans le champ **[!UICONTROL Chemin]**.

>[!NOTE]
>
>Vous ne pouvez pas configurer la partie statique de l’URL dans le parcours, mais dans la configuration globale de l’action personnalisée. [En savoir plus](../action/about-custom-action-configuration.md).

Pour concaténer des champs et des chaînes de texte brut, utilisez les fonctions String ou le signe plus (+) dans l’éditeur d’expression avancé. Placez les chaînes de texte brut entre guillemets simples (&#39;) ou entre guillemets doubles (&quot;). [En savoir plus](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=fr){target=&quot;_blank&quot;}.

Ce tableau présente un exemple de configuration :

| Champ | Valeur |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Chemin | `The id of marketingCampaign + '/messages'` |

L’URL concaténée se présente comme suit :

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;Identifiant de campagne\>`/messages`

![](../assets/journey-custom-action-url.png)

### En-têtes

La section **[!UICONTROL Configuration de l’URL]** affiche les champs d’en-tête dynamiques, mais pas les champs d’en-tête constants. Les champs d’en-tête dynamique sont des champs d’en-tête HTTP dont la valeur est configurée comme variable. [En savoir plus](../action/about-custom-action-configuration.md).

Si nécessaire, spécifiez la valeur des champs d’en-tête dynamique :

1. Sélectionnez l’action personnalisée dans le parcours.
1. Dans le volet de configuration, cliquez sur l’icône en forme de crayon en regard du champ d’en-tête de la section **[!UICONTROL Configuration de l’URL]**.

   ![](../assets/journey-dynamicheaderfield.png)

1. Sélectionnez un champ et cliquez sur **[!UICONTROL OK]**.

## Paramètres d’action

Dans la section **[!UICONTROL Paramètres d’action]**, les paramètres de message sont définis en tant que _« Variable »_. Pour ces paramètres, vous pouvez indiquer où obtenir ces informations (événements ou sources de données, par exemple), transmettre les valeurs manuellement ou utiliser l’éditeur d’expression avancé pour des cas d’utilisation plus complexes (tels qu’une manipulation de données et une autre utilisation des fonctions). Voir la [documentation d’Adobe Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=fr){target=&quot;_blank&quot;}.

**Rubriques connexes**

[Configurer une action](../action/about-custom-action-configuration.md)
