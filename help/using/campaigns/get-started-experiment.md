---
title: Prise en main de l’expérience de contenu
description: En savoir plus sur l’expérience de contenu dans [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 0036c905b9344a6f99e8525acbe9caab5932f361
workflow-type: tm+mt
source-wordcount: '1512'
ht-degree: 0%

---

# Prise en main des expériences de contenu {#get-started-experiment}

>[!AVAILABILITY]
>
>Actuellement, la fonctionnalité d’expérience de contenu n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en savoir plus, contactez votre représentant Adobe.

## Qu’est-ce qu’une expérience de contenu ?

Les expériences de contenu vous permettent d’optimiser le contenu pour les actions de vos campagnes.

Les expériences sont un ensemble d’essais randomisés, qui, dans le cadre des tests en ligne, signifie que certains utilisateurs sélectionnés de manière aléatoire sont exposés à une variante donnée d’un message et à un autre ensemble d’utilisateurs sélectionnés de manière aléatoire pour un autre traitement. Après l’envoi du message, vous pouvez ensuite mesurer les mesures de résultats qui vous intéressent, par exemple les ouvertures d’emails ou les clics.

## Pourquoi exécuter des expériences ?

![](assets/content_experiment_schema.png)

Les expériences vous permettent d’isoler les modifications qui entraînent des améliorations de vos mesures. Comme illustré dans l’image ci-dessus : certains utilisateurs sélectionnés de manière aléatoire sont exposés à chaque groupe de traitement, ce qui signifie qu’en moyenne, les groupes partagent les mêmes caractéristiques. Ainsi, toute différence de résultats peut être interprétée comme étant due aux différences dans les traitements reçus, c&#39;est-à-dire que vous pouvez établir un lien de cause à effet entre les modifications que vous avez apportées et les résultats qui vous intéressent.

Cela vous permet de prendre des décisions basées sur les données pour optimiser vos objectifs commerciaux.

Pour des expériences de contenu dans Adobe Journey Optimizer, vous pouvez tester des idées telles que :

* **Objet**: Quel pourrait être l&#39;impact d&#39;un changement de ton ou du degré de personnalisation d&#39;un sujet ?
* **Contenu du message**: La modification de la disposition visuelle d&#39;un email entraînera-t-elle un plus grand nombre de clics sur l&#39;email ?

## Conseils pour exécuter des expériences

Lors de l’exécution d’expériences, il est important de suivre certaines bonnes pratiques. Voici quelques conseils pour exécuter ces expériences :

+++Isolez les variables que vous essayez de tester.

Formulez une hypothèse que vous avez l&#39;intention de tester et limitez cette hypothèse au moins peu de modifications possibles afin de déterminer ce qui a eu un impact sur votre diffusion.

Par exemple, une bonne hypothèse peut être de savoir si la personnalisation de l’objet des emails entraîne de meilleurs taux d’ouverture. Cependant, l’ajout d’une modification du contenu du message ou des images peut entraîner une conclusion confuse.
+++

+++Vérifiez que vous utilisez la mesure appropriée.

Déterminez la mesure que vous souhaitez cibler et si les modifications que vous apportez peuvent avoir un impact direct sur cette mesure.

Par exemple, il est peu probable que la modification du contenu du corps du message affecte les taux d’ouverture des emails.
+++

+++Effectuez votre test selon la bonne taille d’audience ou pour une durée suffisante.

Si vous exécutez vos tests plus longtemps, vous pourrez détecter de plus petites différences dans la mesure d’objectif entre les traitements. Cependant, si la valeur de base de votre mesure d’objectif est faible, vous aurez besoin de tailles d’échantillon plus grandes.
Le nombre d’utilisateurs qui doivent être inclus dans votre expérience dépend de la taille de l’effet que vous souhaitez détecter, de la variance ou de la propagation de votre mesure d’objectif, ainsi que de votre tolérance pour les erreurs faux positifs et faux négatifs. Dans les expériences classiques, vous pouvez utiliser une [calculateur de taille d’échantillon](https://experienceleague.adobe.com/tools/calculator/testcalculator.html?lang=fr) pour déterminer la durée pendant laquelle vous devez exécuter votre test.
+++

+++Comprendre l’incertitude statistique

Si vous exécutez une expérience dans laquelle 1 000 utilisateurs ont vu un traitement et que le taux de conversion est défini sur 5 %. S’agit-il du taux de conversion réel si tous vos utilisateurs étaient inclus ? Quel serait le véritable taux de conversion ?
Les méthodes statistiques nous permettent de formaliser cette incertitude. L’un des concepts les plus importants à comprendre lors de l’exécution d’expériences en ligne est que les taux de conversion observés sont cohérents avec un éventail de taux de conversion réels sous-jacents, ce qui signifie que vous devez attendre que ces estimations soient suffisamment précises, avant de tenter de tirer une conclusion. Les intervalles de confiance et le degré de confiance nous aident à quantifier cette incertitude.
+++

+++Formuler de nouvelles hypothèses et tester continuellement

Pour obtenir de véritables informations sur l’entreprise, vous devez vous en tenir à une seule expérience. Au lieu de cela, effectuez des expériences en formulant de nouvelles hypothèses et en effectuant de nouveaux tests avec différentes modifications, sur différents segments, et en examinant l’impact sur les différentes mesures.
+++

## Interprétation des résultats de vos expériences {#interpret-results}

![](assets/experimentation_report_3.png)

Cette section décrit les rapports d’expérience et comment comprendre les différentes quantités statistiques présentées.

Voici quelques instructions pour interpréter les résultats de votre expérience de contenu.

Notez qu’une description complète des résultats doit tenir compte de toutes les preuves disponibles (c’est-à-dire la taille des échantillons, les taux de conversion, les intervalles de confiance, etc.), et pas seulement de la déclaration concluante ou non. Même lorsqu&#39;un résultat n&#39;est pas encore concluant, il peut encore y avoir des preuves convaincantes pour qu&#39;un traitement soit différent d&#39;un autre.

Pour comprendre les calculs statistiques, reportez-vous à cette section [page](../campaigns/experiment-calculations.md).

### 1. Comparaison de mesures normalisées {#normalized-metrics}

Lorsque vous comparez les performances de deux traitements, vous devez toujours comparer les mesures normalisées afin de tenir compte des différences de nombre de profils exposés à chaque traitement.

Par exemple, si l’objectif de l’expérience est défini sur **[!UICONTROL Ouvertures uniques]**, et un traitement donné a été présenté à 10 000 profils avec 200 ouvertures uniques enregistrées, ce qui représente une **[!UICONTROL Taux de conversion]** de 2 %. Pour les mesures non uniques, par exemple la mesure Ouvertures , la mesure normalisée s’affiche sous la forme d’une **[!UICONTROL Comptage par profil]**, tandis que pour les mesures continues telles que le total du prix, la mesure normalisée s’affiche sous la forme d’une **[!UICONTROL Total par profil]**.

### 2. Concentration sur les intervalles de confiance {#confidence-intervals}

Lorsque vous exécutez des expériences sur des échantillons de vos profils, le taux de conversion observé pour un traitement donné représente une estimation du taux de conversion sous-jacent réel.

Par exemple, si le traitement A a une **[!UICONTROL Taux de conversion]** de 3 %, alors que le traitement B a une **[!UICONTROL Taux de conversion]** de 2 %, le traitement A est-il meilleur que le traitement B ? Pour y répondre, nous devons d’abord quantifier l’incertitude de ces taux de conversion observés.

Les intervalles de confiance permettent de quantifier le degré d’incertitude dans les taux de conversion estimés, mais des intervalles de confiance plus larges impliquent plus d’incertitude. À mesure que davantage de profils seront ajoutés à l’expérience, les intervalles seront plus petits, représentant une estimation plus précise. L’intervalle de confiance représente une plage de taux de conversion compatibles avec les données observées.

Si les intervalles de confiance pour deux traitements se chevauchent à peine, cela signifie que les deux traitements ont des taux de conversion différents. Cependant, s’il y a beaucoup de chevauchement entre les intervalles de confiance pour deux traitements, il est plus probable que les deux traitements ont le même taux de conversion.

Adobe utilise 95 % d’intervalles de confiance valides ou de séquences de confiance, ce qui signifie que les résultats peuvent être affichés en toute sécurité à tout moment pendant l’expérience.

### 3. Présentation de l’effet élévateur {#understand-lift}

Le résumé du rapport d’expérience affiche le rapport **[!UICONTROL Effet élévateur sur la ligne de base]**, qui est une mesure de l’amélioration en pourcentage du taux de conversion d’un traitement donné par rapport à la ligne de base. Défini précisément, il s’agit de la différence de performance entre un traitement donné et la ligne de base, divisée par la performance de la ligne de base, exprimée en pourcentage.

### 3. Comprendre la confiance {#understand-confidence}

Bien que vous devriez vous concentrer principalement sur la variable **[!UICONTROL Intervalle de confiance]** pour ce qui est de la performance de chaque traitement, l&#39;Adobe montre aussi la confiance, qui est une mesure probabiliste de la quantité de preuves démontrant qu&#39;un traitement donné est le même que le traitement de base. Une confiance plus élevée indique moins de preuves que l’hypothèse selon laquelle les traitements de base et non de base ont des performances égales. Plus précisément, la confiance affichée est une probabilité (exprimée en pourcentage) que nous aurions observé une différence plus faible dans les taux de conversion entre un traitement donné et la ligne de base, si, en réalité, il n’y a aucune différence dans les taux de conversion sous-jacents réels. En termes de p-valeurs, la confiance affichée est 1 - p-value.

Adobe utilise des valeurs p &quot;Anytime Valid&quot; et &quot;Anytime Valid&quot; conformes aux séquences de confiance décrites ci-dessus.

### 4. Signification statistique

Lors de l’exécution d’expériences, un résultat est considéré comme statistiquement significatif s’il était très peu probable qu’il ait été observé, compte tenu d’une hypothèse nulle selon laquelle un traitement donné et la ligne de base ont des taux de conversion/performances sous-jacents identiques.

Adobe déclare une expérience comme concluante lorsque le degré de confiance est supérieur à 95 %.

## Que faire après l’exécution d’une expérience

Après avoir exécuté votre expérience, plusieurs actions de suivi sont possibles :

* **Déployer des idées gagnantes**

   Avec un résultat sans ambiguïté, vous pouvez déployer cette idée gagnante, soit en remettant le traitement le plus performant à tous vos clients, soit en créant de nouvelles campagnes où la structure du traitement le plus performant est répliquée.
   </br>Notez que dans un environnement dynamique, ce qui fonctionne bien à la fois, peut ne pas bien fonctionner plus tard.

* **Exécution de tests de suivi**

   Parfois, les résultats de vos expériences peuvent ne pas être concluants, soit parce qu’il n’y avait pas suffisamment de profils inclus pour détecter une différence de traitement, soit parce que les traitements que vous avez définis n’étaient pas suffisamment différents.

   Si l’hypothèse que vous testez est toujours pertinente, effectuez un test de relance sur une audience plus grande ou différente, ou modifiez vos traitements pour qu’il y ait des différences plus claires, ce qui peut être la meilleure action de relance.

* **Effectuer des analyses approfondies**

   Le traitement qui fonctionne bien pour une audience peut parfois ne pas être le meilleur traitement pour une autre audience. Effectuer des analyses plus approfondies sur la manière dont les traitements se comportent pour différents segments permet de générer des idées pour de nouveaux tests.

   De même, l’étude des performances de chaque traitement avec des mesures différentes peut également donner une vue plus complète de vos expériences.

   >[!CAUTION]
   >
   >Plus d’analyses signifie une plus grande probabilité de détecter un effet fallacieux, ou un faux positif.


