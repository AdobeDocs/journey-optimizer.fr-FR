---
solution: Journey Optimizer
product: journey optimizer
title: Ajustement de l'alignement vertical et la marge intérieure dans Journey Optimizer
description: Découvrez comment ajuster l'alignement vertical et la marge intérieure
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: alignement vertical, éditeur d’e-mail, marge intérieure
exl-id: 1e1d90ff-df5d-4432-a63a-a32d0d281d48
TQID: https://experienceleague.adobe.com/vJhROWi5ZiOLJrESMe-oUkmve1vSXrE5sNewDLpv-eE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 381
ht-degree: 100%

---

# Ajuster l’alignement vertical et la marge intérieure {#alignment-and-padding}

Dans cet exemple, nous allons ajuster la marge intérieure et l&#39;alignement vertical à l&#39;intérieur d&#39;un composant de structure composé de trois colonnes.

1. Sélectionnez le composant de structure directement dans l’email ou à l’aide de l’**[!UICONTROL arborescence de navigation]** disponible dans le menu de gauche.

1. Dans la barre d&#39;outils, cliquez sur **[!UICONTROL Sélectionner une colonne]** et choisissez celle à modifier. Vous pouvez également la sélectionner dans l&#39;arborescence.

   Les paramètres modifiables de cette colonne sont affichés dans l’onglet **[!UICONTROL Styles]**.

   ![](assets/alignment_2.png)

1. Sous **[!UICONTROL Alignement]**, sélectionnez **[!UICONTROL Haut]**, **[!UICONTROL Milieu]** ou **[!UICONTROL Bas]**.

   ![](assets/alignment_3.png)

1. Sous **[!UICONTROL Marge intérieure]**, définissez la marge intérieure pour tous les côtés.

   Sélectionner **[!UICONTROL Marge intérieure différente pour chaque côté]** si vous souhaitez mieux définir la marge intérieure. Cliquez sur l’icône représentant un verrou pour interrompre la synchronisation.

   ![](assets/alignment_4.png)

1. Procédez de la même façon pour ajuster l’alignement et la marge intérieure des autres colonnes.

1. Enregistrez vos modifications.

>[!TIP]
>
>Lors de la conception de contenu d’e-mail pour Gmail sur les appareils Android, assurez-vous que les images et les séparateurs utilisent la marge intérieure des colonnes plutôt que de grandes marges fixes. Gmail sur Android effectue souvent un rendu surdimensionné des images et incorrect des marges, ce qui entraîne un débordement de la disposition ou une réduction des lignes de séparation. Utilisez une largeur d’image plus petite ou utilisez la marge intérieure basée sur les colonnes pour un affichage cohérent.

## Gérer la marge intérieure des fragments avec la navigation par chemin de navigation {#fragment-padding-breadcrumb}

Lorsque vous utilisez des [fragments](../content-management/fragments.md) dans le Concepteur d’e-mail, des marges intérieures masquées ou résiduelles peuvent altérer le rendu sur les appareils mobiles par rapport à l’affichage sur les ordinateurs. Cela est particulièrement fréquent lorsque des fragments ont été déverrouillés ou lorsque l’[héritage a été rompu](use-visual-fragments.md#break-inheritance), car les styles restants peuvent rester dans la colonne ou les composants de texte sous-jacents.

Pour identifier et modifier la marge intérieure résiduelle dans les fragments :

1. Utilisez l’**[!UICONTROL arborescence de navigation]** ou cliquez directement sur les éléments dans l’éditeur pour sélectionner chaque structure parent ou colonne de votre fragment. Vous pouvez ainsi repérer les marges intérieures ou extérieures masquées qui peuvent être spécifiques aux appareils mobiles.

1. Après avoir sélectionné l’élément dans le chemin de navigation, accédez à l’onglet **[!UICONTROL Styles]** à droite.

1. Passez en revue les paramètres de **[!UICONTROL marge intérieure]** et supprimez-la ou réajustez-la selon les besoins pour obtenir un ajustement parfait sur les appareils mobiles.

1. Si des problèmes d’ajustement persistent lors de la réutilisation de fragments, répétez ce processus pour d’autres colonnes ou composants de texte dans le fragment.

>[!NOTE]
>
>Ce comportement est prévisible lorsque des fragments sont insérés et supprimés plusieurs fois, car les règles de style peuvent s’accumuler. Vérifiez toujours la marge intérieure à l’aide de la navigation dans le chemin de navigation, en particulier si vous ciblez des appareils mobiles.