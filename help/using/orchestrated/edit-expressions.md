---
solution: Journey Optimizer
product: journey optimizer
title: Modifier les expressions
description: Découvrir comment modifier les expressions
exl-id: bf0a905f-00af-4ed7-9e4f-bf8cb0af9ea9
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: ht
source-wordcount: '2034'
ht-degree: 100%

---


# Modifier les expressions {#edit-expressions}

>[!NOTE]
>
>La section ci-dessous fournit des informations sur l’utilisation de l’éditeur d’expression pour créer des règles. Gardez à l’esprit que la syntaxe utilisée pour créer des règles diffère de celle utilisée pour ajouter de la personnalisation.

## Utiliser l’éditeur d’expression {#edit}

L’édition d’une expression consiste à saisir manuellement des conditions pour former une règle. Ce mode permet d’utiliser des fonctions avancées, vous permettant ainsi de manipuler les valeurs utilisées afin de réaliser des requêtes spécifiques comme la manipulation de dates, de chaînes, de champs numériques et le tri.

L’éditeur d’expression est accessible avec le bouton **[!UICONTROL Modifier une expression]** du créateur de règles, disponible pour les champs **[!UICONTROL Attribut]** et **[!UICONTROL Valeur]** lors de la configuration d’une condition personnalisée.

| Accéder depuis le champ **Attribut** | Accéder depuis le champ **Valeur** |
| --- | --- |
| ![Éditeur d’expression pour le champ Attribut](assets/rule-builder-expression-access-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} | ![Éditeur d’expression pour le champ Valeur](assets/rule-builder-expression-access-value.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

L’éditeur d’expression fournit :

* un **champ de saisie (1)**, dans lequel l’expression est définie ;
* la liste des **champs (2)** disponibles, utilisables dans l’expression et correspondant à la dimension de ciblage de la requête ;
* des **fonctions d’assistance (3)**, triées par catégorie.

Modifiez l’expression en saisissant une expression directement dans le champ de saisie. Pour ajouter un champ ou une fonction d’assistance, placez le curseur dans l’expression à l’endroit où vous souhaitez l’ajouter, puis cliquez sur le bouton +.

![Interface de l’éditeur d’expression](assets/rule-builder-expression-editor.png){zoomable="yes"}

## Fonctions d’assistance

L’outil d’édition de requêtes permet d’utiliser des fonctions avancées pour réaliser un filtrage complexe en fonction des résultats souhaités et des types de données manipulées. Les fonctions suivantes sont disponibles :

### Agrégat

Les fonctions d’agrégat effectuent des calculs sur un jeu de valeurs.

<table>
<tbody>
<tr>
<td><strong>Nom</strong></td>
<td><strong>Description</strong></td>
<td><strong>Syntaxe</strong></td>
</tr>
<tr>
<td><strong>Avg</strong></td>
<td>Renvoie la moyenne d'une colonne de type numérique</td>
<td>Avg(&lt;valeur&gt;)</td>
</tr>
<tr>
<td><strong>Number</strong></td>
<td>Compte les valeurs non nulles d'une colonne</td>
<td>Count(&lt;valeur&gt;)</td>
</tr>
<tr>
<td><strong>CountAll</strong></td>
<td>Compte les valeurs retournées (tous champs confondus)</td>
<td>CountAll()</td>
</tr>
<tr>
<td><strong>Countdistinct</strong></td>
<td>Compte les valeurs distinctes non nulles d'une colonne</td>
<td>Countdistinct(&lt;valeur&gt;)</td>
</tr>
<tr>
<td><strong>Max</strong></td>
<td>Renvoie la valeur maximum d'une colonne de type nombre, chaîne ou date</td>
<td>Max(&lt;valeur&gt;)</td>
</tr>
<tr>
<td><strong>Min</strong></td>
<td>Renvoie la valeur minimum d’une colonne de type nombre, chaîne ou date</td>
<td>Min(&lt;valeur&gt;)</td>
</tr>
<tr>
<td><strong>StdDev</strong></td>
<td>Renvoie l’écart type d’une colonne de type nombre, chaîne ou date</td>
<td>StdDev(&lt;valeur&gt;)</td>
</tr>
<tr>
<td><strong>StringAgg</strong></td>
<td>Renvoie la concaténation des valeurs d'une colonne de type chaîne, séparée par le caractère dans le deuxième argument</td>
<td>StringAgg(&lt;Valeur&gt;,&lt;Chaîne&gt;)</td>
</tr>
<tr>
<td><strong>Sum</strong></td>
<td>Renvoie la somme des valeurs d'une colonne de type nombre, chaîne ou date</td>
<td>Sum(&lt;valeur&gt;)</td>
</tr>
</tbody>
</table>

### Date

Les fonctions de date manipulent les valeurs de date ou d’heure.

<table>
<tbody>
<tr>
<td><strong>Nom</strong></td>
<td><strong>Description</strong></td>
<td><strong>Syntaxe</strong></td>
</tr>
<tr>
<td><strong>AddDays</strong></td>
<td>Ajoute un nombre de jours à une date.</td>
<td>AddDays(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>AddHours</strong></td>
<td>Ajoute un nombre d’heures à une date.</td>
<td>AddHours(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>AddMinutes</strong></td>
<td>Ajoute un nombre de minutes à une date.</td>
<td>AddMinutes(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>AddMonths</strong></td>
<td>Ajoute un nombre de mois à une date.</td>
<td>AddMonths(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>AddSeconds</strong></td>
<td>Ajoute un nombre de secondes à une date.</td>
<td>AddSeconds(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>AddYears</strong></td>
<td>Ajoute un nombre d’années à une date.</td>
<td>AddYears(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>ConvertNTZ</strong></td>
<td>Convertit l’horodatage NTZ (horodatage sans fuseau horaire) en TZ (horodatage avec fuseau horaire) en application de la valeur TZ de session définie.</td>
<td>ConvertNTZ(&lt;date+heure&gt;)</td>
</tr>
<tr>
<td><strong>DateCmp</strong></td>
<td>Compare deux dates</td>
<td>DateCmp(&lt;date&gt;, &lt;date&gt;)</td>
</tr>
<tr>
<td><strong>DateOnly</strong></td>
<td>Renvoie la date uniquement (avec heure à 00:00).</td>
<td>DateOnly(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>Day</strong></td>
<td>Renvoie le nombre représentant le jour de la date.</td>
<td>Day(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>DayOfYear</strong></td>
<td>Renvoie le numéro du jour dans l'année de la date</td>
<td>DayOfYear(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>DaysAgo</strong></td>
<td>Renvoie la date correspondant à la date courante moins n jours</td>
<td>DaysAgo(&lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>DaysAgoInt</strong></td>
<td>Renvoie la date (entier aaaammjj) correspondant à la date courante moins n jours</td>
<td>DaysAgoInt(&lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>DaysDiff</strong></td>
<td>Renvoie le nombre de jours entre deux dates.</td>
<td>DaysDiff(&lt;date de fin&gt;, &lt;date de début&gt;)</td>
</tr>
<tr>
<td><strong>DaysOld</strong></td>
<td>Renvoie l’ancienneté en jours d’une date.</td>
<td>DaysOld(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>GetDate</strong></td>
<td>Renvoie la date système courante du serveur.</td>
<td>GetDate()</td>
</tr>
<tr>
<td><strong>Hour</strong></td>
<td>Renvoie l’heure de la date</td>
<td>Hour(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>HoursDiff</strong></td>
<td>Renvoie le nombre d’heures entre deux dates</td>
<td>HoursDiff(&lt;date de fin&gt;, &lt;date de début&gt;)</td>
</tr>
<tr>
<td><strong>Minute</strong></td>
<td>Renvoie les minutes de la date.</td>
<td>Minute(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>MinutesDiff</strong></td>
<td>Renvoie le nombre de minutes entre deux dates.</td>
<td>MinutesDiff(&lt;date de fin&gt;, &lt;date de début&gt;)</td>
</tr>
<tr>
<td><strong>Month</strong></td>
<td>Renvoie le nombre représentant le mois de la date.</td>
<td>Month(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>MonthsAgo</strong></td>
<td>Renvoie la date correspondant à la date courante moins n mois.</td>
<td>MonthsAgo(&lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>MonthsDiff</strong></td>
<td>Renvoie le nombre de mois entre deux dates.</td>
<td>MonthsDiff(&lt;date de fin&gt;, &lt;date de début&gt;)</td>
</tr>
<tr>
<td><strong>MonthsOld</strong></td>
<td>Renvoie l’ancienneté en mois d’une date.</td>
<td>MonthsOld(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>Oldest</strong></td>
<td>Renvoie la date la plus ancienne d’une plage.</td>
<td>Oldest(&lt;date, date&gt;)</td>
</tr>
<tr>
<td><strong>Second</strong></td>
<td>Renvoie les secondes de la date.</td>
<td>Second(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>SecondsDiff</strong></td>
<td>Renvoie le nombre de secondes entre deux dates.</td>
<td>SecondsDiff(&lt;date de fin&gt;, &lt;date de début&gt;)</td>
</tr>
<tr>
<td><strong>SubDays</strong></td>
<td>Enlève un nombre de jours à une date.</td>
<td>SubDays(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>SubHours</strong></td>
<td>Enlève un nombre d’heures à une date.</td>
<td>SubHours(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>SubMinutes</strong></td>
<td>Enlève un nombre de minutes à une date.</td>
<td>SubMinutes(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>SubMonths</strong></td>
<td>Enlève un nombre de mois à une date.</td>
<td>SubMonths(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>SubSeconds</strong></td>
<td>Enlève un nombre de secondes à une date.</td>
<td>SubSeconds(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>SubYears</strong></td>
<td>Enlève un nombre d’années à une date.</td>
<td>SubYears(&lt;date&gt;, &lt;nombre&gt;)</td>
</tr>
<tr>
<td><strong>ToDate</strong></td>
<td>Convertit une date+heure en date seule</td>
<td>ToDate(&lt;date + heure&gt;)</td>
</tr>
<tr>
<td><strong>ToDateTime</strong></td>
<td>Convertit une chaîne en date+heure</td>
<td>ToDateTime(&lt;chaîne&gt;)</td>
</tr>
<tr>
<td><strong>ToTimestamp</strong></td>
<td>Convertir une chaîne en date et heure.</td>
<td>ToTimestamp(&lt;chaîne&gt;)</td>
</tr>
<tr>
<td><strong>ToTimeZone</strong></td>
<td>Convertit une date et une heure en fuseau horaire</td>
<td>ToTimeZone(&lt;date&gt;, &lt;fuseau horaire&gt;)</td>
</tr>
<tr>
<td><strong>TruncDate</strong></td>
<td>Arrondit une date et une heure à la seconde.</td>
<td>TruncDate(@lastModified, &lt;nombre de secondes&gt;)</td>
</tr>
<tr>
<td><strong>TruncDateTZ</strong></td>
<td>Arrondit une date+heure à la seconde près</td>
<td>TruncDateTZ(&lt;date&gt;, &lt;nombre de secondes&gt;, &lt;fuseau horaire&gt;)</td>
</tr>
<tr>
<td><strong>TruncQuarter</strong></td>
<td>Arrondit une date au trimestre.</td>
<td>TruncQuarter(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>TruncTime</strong></td>
<td>Arrondit la partie heure à la seconde.</td>
<td>TruncTime(&lt;date&gt;, &lt;nombre de secondes&gt;)</td>
</tr>
<tr>
<td><strong>TruncWeek</strong></td>
<td>Arrondit une date à la semaine.</td>
<td>TruncWeek(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>TruncYear</strong></td>
<td>Arrondit une date+heure au premier janvier de l’année.</td>
<td>TruncYear(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>WeekDay</strong></td>
<td>Renvoie le numéro du jour dans la semaine de la date (0=lundi, 6=dimanche)</td>
<td>WeekDay(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>Year</strong></td>
<td>Renvoie le nombre représentant l’année de la date.</td>
<td>Year(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>YearAndMonth</strong></td>
<td>Renvoie le nombre représentant l’année et le mois de la date.</td>
<td>YearAndMonth(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>YearsAgo</strong></td>
<td>Renvoie le nombre d’années entre une date donnée et la date actuelle.</td>
<td>YearsAgo(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>YearsDiff</strong></td>
<td>Renvoie le nombre d’années entre deux dates.</td>
<td>YearsDiff(&lt;date de fin&gt;, &lt;date de début&gt;)</td>
</tr>
<tr>
<td><strong>YearsOld</strong></td>
<td>Renvoie l’ancienneté en années d’une date.</td>
<td>YearsOld(&lt;date&gt;)</td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>Notez que la fonction **DateOnly** prend uniquement en compte le fuseau horaire du serveur, et non celui de l’opérateur.


### Géomarketing

Les fonctions de géomarketing sont utilisées pour manipuler des valeurs géographiques.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nom</strong><br /> </td> 
   <td> <strong>Description</strong><br /> </td> 
   <td> <strong>Syntaxe</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Distance</strong><br /> </td> 
   <td> Renvoie la distance entre deux points donnés par leur longitude et leur latitude, exprimées en degrés.<br /> </td> 
   <td> Distance(&lt;Longitude A&gt;, &lt;Latitude A&gt;, &lt;Longitude B&gt;, &lt;Latitude B&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Numérique

Les fonctions numériques sont utilisées pour convertir du texte en nombres.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nom</strong><br /> </td> 
   <td> <strong>Description</strong><br /> </td> 
   <td> <strong>Syntaxe</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> Renvoie la valeur absolue d'un nombre<br /> </td> 
   <td> Abs(&lt;nombre&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> Renvoie le plus petit entier supérieur ou égal à un nombre<br /> </td> 
   <td> Ceil(&lt;nombre&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> Renvoie le plus grand entier supérieur ou égal à un nombre<br /> </td> 
   <td> Floor(&lt;nombre&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> Renvoie le plus grand de deux nombres<br /> </td> 
   <td> Greatest(&lt;nombre 1&gt;, &lt;nombre 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> Renvoie le plus petit de deux nombres<br /> </td> 
   <td> Least(&lt;nombre 1&gt;, &lt;nombre 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> Renvoie le reste de la division entiers de n1 par n2<br /> </td> 
   <td> Mod(&lt;nombre 1&gt;, &lt;nombre 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> Renvoie la proportion en pourcentage entre deux nombres<br /> </td> 
   <td> Percent(&lt;nombre 1&gt;, &lt;nombre 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> Renvoie une valeur aléatoire<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> Arrondit un nombre à n décimales près<br /> </td> 
   <td> Round(&lt;nombre&gt;, &lt;nombre de décimales&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> Renvoie le signe du nombre<br /> </td> 
   <td> Sign(&lt;nombre&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> Convertit un entier en réel<br /> </td> 
   <td> ToDouble(&lt;nombre&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> Convertit un réel en entier 64 bits<br /> </td> 
   <td> ToInt64(&lt;nombre&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> Convertit un réel en entier<br /> </td> 
   <td> ToInteger(&lt;nombre&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> Tronque n1 à n2 décimales<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Autres

Ce tableau contient les autres fonctions disponibles.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nom</strong><br /> </td> 
   <td> <strong>Description</strong><br /> </td> 
   <td> <strong>Syntaxe</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AESEncrypt</strong><br /> </td> 
   <td> Chiffrer la chaîne fournie dans l’argument<br /> </td> 
   <td> AESEncrypt(&lt;valeur&gt;)<br /> </td> 
  </tr>
  <tr> 
   <td> <strong>Case</strong><br /> </td> 
   <td> Renvoie la valeur 1 si la condition est vérifiée. Sinon, renvoie la valeur 2.<br /> </td> 
   <td> Case(When(&lt;condition&gt;, &lt;valeur 1&gt;), Else(&lt;valeur 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> Efface le Flag dans la valeur<br /> </td> 
   <td> ClearBit(&lt;identifiant&gt;, &lt;flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Coalesce</strong><br /> </td> 
   <td> Renvoie la valeur 2 si la valeur 1 est nulle ou vide (null), sinon renvoie la valeur 1<br /> </td> 
   <td> Coalesce(&lt;valeur 1&gt;, &lt;valeur 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> Renvoie la valeur 3 si la valeur 1 = la valeur 2. Sinon, renvoie la valeur 4.<br /> </td> 
   <td> Decode(&lt;valeur 1&gt;, &lt;valeur 2&gt;, &lt;valeur 3&gt;, &lt;valeur 4&gt;)<br /> </td>  
  </tr>

<tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> Renvoie la valeur 1 (ne peut être utilisée qu'en paramètre de la fonction Case)<br /> </td> 
   <td> Else(&lt;valeur 1&gt;, &lt;valeur 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> Extrait le domaine d'une adresse e-mail<br /> </td> 
   <td> GetEmailDomain(&lt;valeur&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> Récupère l'URL du serveur de page miroir<br /> </td> 
   <td> GetMirrorURL(&lt;valeur&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> Renvoie la valeur 1 si l’expression est vraie. Sinon, renvoie la valeur 2.<br /> </td> 
   <td> Iif(&lt;condition&gt;, &lt;valeur 1&gt;, &lt;valeur 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> Indique si le Flag est présent dans la valeur<br /> </td> 
   <td> IsBitSet(&lt;identifiant&gt;, &lt;flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> Renvoie la valeur 2 si la chaîne 1 est vide, sinon renvoie la valeur 3<br /> </td> 
   <td> IsEmptyString(&lt;valeur 1&gt;, &lt;valeur 2&gt;, &lt;valeur 3&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NewUUID</strong><br /> </td> 
   <td> Renvoie un ID unique<br /> </td> 
   <td> NewUUID()<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> Renvoie la chaîne vide si l'argument n'a pas de valeur (null)<br /> </td> 
   <td> NoNull(&lt;valeur&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> Renvoie le numéro de la ligne<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> Force le Flag dans la valeur<br /> </td> 
   <td> SetBit(&lt;identifiant&gt;, &lt;flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> Convertit un nombre en booléen<br /> </td> 
   <td> ToBoolean(&lt;nombre&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> Renvoie la valeur 1 si l’expression est vraie. Sinon, renvoie la valeur 2 (ne peut être utilisée qu’en paramètre de la fonction Case).<br /> </td> 
   <td> When(&lt;condition&gt;, &lt;valeur 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Chaîne

Les fonctions de chaîne sont utilisées pour manipuler un ensemble de chaînes.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nom</strong><br /> </td> 
   <td> <strong>Description</strong><br /> </td> 
   <td> <strong>Syntaxe</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> Indique si tous les paramètres sont non nuls et non vides<br /> </td> 
   <td> AllNonNull2(&lt;chaîne&gt;, &lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> Indique si tous les paramètres sont non nuls et non vides<br /> </td> 
   <td> AllNonNull3(&lt;chaîne&gt;, &lt;chaîne&gt;, &lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ascii</strong><br /> </td> 
   <td> Renvoie la valeur ascii du premier caractère de la chaîne.<br /> </td> 
   <td> Ascii(&lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> Renvoie le caractère de code ascii n<br /> </td> 
   <td> Char(&lt;nombre&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> Retourne la position de la chaîne 2 dans la chaîne 1.<br /> </td> 
   <td> Charindex(&lt;chaîne&gt;, &lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>dataLength</strong><br /> </td> 
   <td> Renvoie la taille de la chaîne en octets <br /> </td> 
   <td> dataLength(&lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> Renvoie la nième (de 1 à n) ligne de la chaîne<br /> </td> 
   <td> GetLine(&lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> Renvoie le troisième paramètre si les deux premiers paramètres sont égaux. Sinon, renvoie le dernier paramètre.<br /> </td> 
   <td> IfEquals(&lt;chaîne&gt;, &lt;chaîne&gt;, &lt;chaîne&gt;, &lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> Indique si le memo passé en paramètre est nul<br /> </td> 
   <td> IsMemoNull(&lt;memo&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> Concatène les chaînes passées en paramètres. Ajoute des espaces entre les chaînes si nécessaire.<br /> </td> 
   <td> JuxtWords(&lt;chaîne&gt;, &lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> Concatène les chaînes passées en paramètres. Ajoute des espaces entre les chaînes si nécessaire.<br /> </td> 
   <td> JuxtWords3(&lt;chaîne&gt;, &lt;chaîne&gt;, &lt;chaîne&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> Renvoie les n premiers caractères de la chaîne<br /> </td> 
   <td> Left(&lt;chaîne&gt;, &lt;nombre&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> Renvoie la longueur de la chaîne<br /> </td> 
   <td> Length(&lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Line</strong><br /> </td> 
   <td> Extraire la ligne n de la chaîne<br /> </td> 
   <td> Line(&lt;chaîne&gt;,&lt;nombre&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> Renvoie la chaîne en minuscules<br /> </td> 
   <td> Lower(&lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> Renvoie la chaîne complétée à gauche<br /> </td> 
   <td> LPad (&lt;Chaîne&gt;, &lt;Nombre&gt;, &lt;Caractère&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> Ote les espaces à gauche de la chaîne<br /> </td> 
   <td> Ltrim(&lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> Renvoie une représentation hexadécimale de la clé MD5 d'une chaîne<br /> </td> 
   <td> Md5Digest(&lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> Indique si le mémo contient la chaîne passée en paramètre<br /> </td> 
   <td> MemoContains(&lt;memo&gt;, &lt;chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>NodeValue</strong><br /> </td> 
   <td> Extrait la valeur d’un champ XML de son XPath et des données de champ<br /> </td> 
   <td> NodeValue (&lt;Chaîne&gt;, &lt;Chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> Remplace toutes les occurrences d’une valeur de chaîne spécifiée par une autre valeur de chaîne.<br /> </td> 
   <td> Replace(&lt;Chaîne&gt;,&lt;Chaîne&gt;,&lt;Chaîne&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> Renvoie les n derniers caractères de la chaîne<br /> </td> 
   <td> Right(&lt;chaîne&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> Renvoie la chaîne complétée à droite<br /> </td> 
   <td> RPad(&lt;chaîne&gt;, &lt;nombre&gt;, &lt;caractère&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> Ote les espaces à droite de la chaîne<br /> </td> 
   <td> Rtrim(&lt;chaîne&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> Représentation hexadécimale de la clé SHA256 d’une chaîne.<br /> </td> 
   <td> Sha256Digest (&lt;Chaîne&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> Représentation hexadécimale de la clé SHA512 d’une chaîne.<br /> </td> 
   <td> Sha512Digest (&lt;Chaîne&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> Renvoie la chaîne avec la première lettre de chaque mot en majuscule<br /> </td> 
   <td> Smart(&lt;chaîne&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> Extrait la sous-chaîne débutant au caractère n1 de la chaîne et de longueur n2<br /> </td> 
   <td> Substring(&lt;chaîne&gt;, &lt;départ&gt;, &lt;longueur&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> Convertit le nombre en chaîne<br /> </td> 
   <td> ToString(&lt;nombre&gt;, &lt;nombre&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> Renvoie la chaîne en majuscules<br /> </td> 
   <td> Upper(&lt;chaîne&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> Renvoie la clé étrangère d'un lien passée en premier paramètre, si les deux autres paramètres sont égaux<br /> </td> 
   <td> VirtualLink(&lt;nombre&gt;, &lt;nombre&gt;, &lt;nombre&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> Renvoie la clé étrangère (texte) d'un lien passée en premier paramètre, si les deux autres paramètres sont égaux<br /> </td> 
   <td> VirtualLinkStr(&lt;chaîne&gt;, &lt;nombre&gt;, &lt;nombre&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### Période

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Nom</strong><br /> </td> 
   <td> <strong>Description</strong><br /> </td> 
   <td> <strong>Syntaxe</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_Over__</strong><br /> </td> 
   <td> Exécutez l’appel de fonction SQL saisi en tant que 1er paramètre, sur Partition ou Trier selon les champs saisis en tant que 2e paramètre.<br /> </td> 
   <td> _Over_ (&lt;Valeur&gt;, &lt;Valeur&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> Applique un tri descendant<br /> </td> 
   <td> Desc(&lt;valeur 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> Trie le résultat au sein de la partition<br /> </td> 
   <td> OrderBy(&lt;valeur 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> Partitionne le résultat d'une requête sur une table<br /> </td> 
   <td> PartitionBy(&lt;valeur 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> Génère un numéro de ligne en fonction de la partition de la table et d'un ordre de tri.<br /> </td> 
   <td> RowNum(PartitionBy(&lt;valeur 1&gt;), OrderBy(&lt;valeur 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
