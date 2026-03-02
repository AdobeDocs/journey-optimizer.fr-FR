---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Fonctions prises en charge dans l’éditeur d’expression
description: Découvrez les fonctions d’éditeur de personnalisation prises en charge dans la gestion des décisions (Offer Decisioning).
badge: label="Hérité" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
source-git-commit: 8dcac6e63f6a38874b3aff4996fc317e3606cb9b
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 37%

---

# Fonctions prises en charge dans l’éditeur d’expression {#personalization-editor-supported-functions}

Dans la gestion des décisions, vous créez des expressions à l’aide de l’éditeur de personnalisation. Vous utilisez cet éditeur en particulier lorsque :

* **Définir le contenu de l&#39;offre** - lorsque vous [ajoutez des représentations](offer-library/add-representations.md) et personnalisez le contenu de l&#39;offre (images, texte, liens)
* **Création de règles de décision** - lorsque vous [définissez l’éligibilité](offer-library/creating-decision-rules.md) pour les offres
* **Création de formules de classement** - lorsque vous [créez des formules de classement](ranking/create-ranking-formulas.md) pour classer les offres

Le serveur principal d’Offer Decisioning prend uniquement en charge un **sous-ensemble** des fonctions disponibles dans l’éditeur de personnalisation. Cette page répertorie toutes les fonctions que vous pouvez utiliser en toute sécurité. Développez chaque section pour afficher les opérateurs, les assistants et les fonctions pris en charge.

## Liste des fonctions prises en charge {#supported-functions-list}

+++ Opérateurs

* `+` `-` `*` `/` `%` (arithmétique)
* `and` `or` `!` (logique)
* `=` `!=` `>` `>=` `<` `<=` (comparaison)

+++

+++ Assistants

* Each
* Avec
* Si
* Unless
* Let
* Valeur de secours par défaut
* fragment
* datasetLookup
* externalDataLookup (Alpha)
* En ligne
* Url
* Métadonnées d’exécution
* valueAtPath

+++

+++ Fonctions de chaîne

| Nom d’affichage | Nom interne |
|--------------|---------------|
| Minuscules | lowerCase |
| Majuscules | upperCase |
| Étui chameau | camelCase |
| Casse du titre | titleCase |
| Supprimer | trim |
| Supprimer à gauche | leftTrim |
| Supprimer à droite | rightTrim |
| Est vide | isEmpty |
| Égal à ignorer la casse | equalsIgnoreCase |
| Différent de Ignorer la casse | notEqualWithIgnoreCase |
| Remplacer | replace |
| Tout remplacer | replaceAll |
| Concat | concat |
| Partage | split |
| Encode64 | encode64 |
| Longueur | length |
| MD5 | md5 |
| SHA256 | sha256 |
| Comme | comme |
| Commence par | startsWith |
| Ne commence pas par | doNotStartWith |
| Se termine par | se termine par |
| Ne se termine pas par | doNotEndWith |
| Contient | contient |
| Ne contient pas | neContientPas |
| Égal à | est égal à |
| Différent de | notEqualTo |
| Correspond à | matches |
| Groupe d’expressions régulières | regexGroup |
| Chaîne en nombre | stringToNumber |
| Chaîne à date | stringToDate |
| En date/heure | toDateTime |
| To Date Time Only | toDateTimeOnly |
| Extraire le domaine de l’e-mail | extractEmailDomain |
| Extraire le nom d’utilisateur de l’e-mail | extractEmailUsername |
| N’est pas vide | isNotEmpty |
| Index de | indexOf |
| Dernier index de | lastIndexOf |
| Sous-chaîne | substr |
| En valeur booléenne | toBool |
| Chaîne en entier | string_to_integer |
| Masque | masque |
| Obtenir la devise formatée | formatCurrency |
| Obtenir la valeur unicode du caractère | charCodeAt |
| Obtenir le code QR pour tout texte | qrCode |

+++

+++ Fonctions de tableau, liste et ensemble

| Nom d’affichage | Nom interne |
|--------------|---------------|
| Distinct | distinct |
| Dans | in |
| Pas dans | notIn |
| Intersections | intersectes |
| Sous-ensemble de | subsetOf |
| Sur-ensemble de | sur-ensemble de |
| Inclut | inclut |
| Trier et obtenir les N premiers dans le tableau | topN |
| Trier et obtenir les N derniers dans le tableau | bottomN |
| Premier élément | tête |
| Nombre | count |
| Somme | sum |
| Moyenne | moyenne |
| Minimum | min |
| Maximum | max |

+++

+++ Fonctions de mappage

| Nom d’affichage | Nom interne |
|--------------|---------------|
| Obtenir | get |
| Clés | keys |
| Valeurs | valeurs |

+++

+++ Fonctions d’objet

| Nom d’affichage | Nom interne |
|--------------|---------------|
| Est nul | isNull |
| N’est pas nul | isNotNull |

+++

+++ Fonctions mathématiques

| Nom d’affichage | Nom interne |
|--------------|---------------|
| En pourcentage | toPercentage |
| Arrondir à l’unité supérieure | roundUp |
| Arrondir à l’unité inférieure | roundDown |
| En précision | toPrecision |
| Absolu | absolu |
| Aléatoire | random |
| En hexadécimal | toHexString |
| Obtenir le nombre en paramètre régional | formatNumber |
| To String | toString |
| To Int | toInt |
| To Long | toLong |

+++

+++ Fonctions de date et d’heure

| Nom d’affichage | Nom interne |
|--------------|---------------|
| Now | now |
| Obtenir la CurrentZonedDateTime | getCurrentZonedDateTime |
| À ce jour | toDate |
| To Time | toTime |
| En date/heure | toDateTime |
| To Date Time Only | toDateTimeOnly |
| À ce jour uniquement | toDateOnly |
| To Time Only | toTimeOnly |
| Vers le fuseau horaire | toTimeZone |
| Mettre en forme la date | formatDate |
| Date et heure du format | formatDateTime |
| Format de l’heure | formatTime |
| Analyser la date | parseDate |
| Date et heure de l’analyse | parseDateTime |
| Temps d&#39;analyse | parseTime |
| Ajouter des jours | addDays |
| Ajouter des mois | addMonths |
| Ajouter des années | addYears |
| Ajouter des heures | addHours |
| Ajouter des minutes | addMinutes |
| Ajouter des secondes | addSeconds |
| Soustraire les jours | subtractDays |
| Soustraire les mois | subtractMonths |
| Soustraire années | subtractYears |
| Soustraire heures | subtractHours |
| Soustraire les minutes | subtractMinutes |
| Soustraire les secondes | subtractSeconds |
| Différence en jours | diffDays |
| Différence en mois | diffMonths |
| Différence en années | diffYears |
| Différence en heures | diffHours |
| Différence en minutes | diffMinutes |
| Différence en secondes | diffSeconds |
| Début de journée | startOfDay |
| Fin de journée | endOfDay |
| Est avant | isBefore |
| Est après | isAfter |

+++

+++ Fonctions d’URL

| Nom d’affichage | Nom interne |
|--------------|---------------|
| Encoder l’URL | encodeUrl |
| Décoder l’URL | decodeUrl |
| Obtenir le paramètre de requête d’URL | getUrlQueryParam |
| Obtenir le protocole URL | getUrlProtocol |
| Obtenir l’hôte d’URL | getUrlHost |

+++

>[!NOTE]
>
>Si vous utilisez une fonction qui ne figure pas dans la liste ci-dessus, l’expression peut échouer à l’exécution ou produire des résultats inattendus. Pour obtenir l’ensemble complet des fonctions disponibles dans [!DNL Journey Optimizer] personnalisation, voir [Liste des fonctions d’assistance](../personalization/functions/functions.md). Seul le sous-ensemble documenté sur cette page est pris en charge dans Offer Decisioning.
