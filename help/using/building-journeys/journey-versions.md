---
title: Versions de parcours
description: En savoir plus sur les versions de parcours
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8d5ea4c1-bf23-4b58-8654-c251b90c3458
source-git-commit: 1acc5a137661a47abd60c03167e9ef39998de621
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Versions de parcours{#journey-versions}

Dans la liste des parcours, toutes les versions de parcours sont accompagnées d&#39;un numéro. Voir [cette page](../building-journeys/using-the-journey-designer.md).

Lorsque vous recherchez un parcours, les versions les plus récentes apparaissent en haut de la liste la première fois que vous ouvrez l&#39;application. Vous pouvez ensuite définir l&#39;ordre de tri souhaité ; l&#39;application le conservera en tant que préférence utilisateur. La version du parcours est également affichée en haut de l&#39;interface d&#39;édition des parcours, au-dessus de la zone de travail.

![](assets/journeyversions1.png)

>[!NOTE]
>
>Dans la plupart des cas, un profil ne peut pas être présent plusieurs fois dans le même parcours, en même temps. Si la rentrée est activée, un profil peut entrer à nouveau dans un parcours, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours. [En savoir plus](../building-journeys/journey-end.md)

Si vous devez apporter des modifications à un parcours actif, vous devez en créer une nouvelle version.

>[!NOTE]
>
>Pour en savoir plus sur les éléments de sécurité et les limitations des versions de parcours, voir [cette page](../start/guardrails.md#journey-versions-limitations).

1. Ouvrez la dernière version de votre parcours actif, cliquez sur **[!UICONTROL Créer une version]**, puis confirmez.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >Vous ne pouvez créer une version qu&#39;à partir de la dernière version d&#39;un parcours.

1. Effectuez vos modifications, cliquez sur **[!UICONTROL Publier]**, puis confirmez.

   ![](assets/journeyversions3.png)

Aussitôt le parcours publié, les individus commencent à accéder à la dernière version. Les clients qui ont déjà accédé à une version antérieure y restent jusqu&#39;à la fin du parcours. En cas de rentrée ultérieure dans le même parcours, les clients accéderont à la version la plus récente.

Les versions de parcours peuvent être arrêtées individuellement. Toutes les versions des parcours portent le même nom.

>[!NOTE]
>
>Lorsque vous publiez une nouvelle version d&#39;un parcours, la version précédente se termine automatiquement et passe au statut **Fermé**. Aucune entrée dans le parcours ne sera effectuée. Même si vous arrêtez la dernière version, la version précédente restera fermée.
