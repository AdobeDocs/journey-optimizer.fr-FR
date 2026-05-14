---
solution: Journey Optimizer
product: journey optimizer
title: Ajouter des métadonnées au contenu de votre e-mail
description: Découvrez comment améliorer la lisibilité et l’accessibilité du contenu de votre e-mail avec les métadonnées dans Journey Optimizer.
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: pré-en-tête, éditeur, résumé, e-mail
exl-id: 7ed52b2e-eabf-414f-b169-4b004733dea9
TQID: https://experienceleague.adobe.com/apen1-tlKZ3bnGV9X1RacDk1LXt7sJBQNfTQiaFAyYA
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
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 100%

---

# Ajouter des métadonnées au contenu de votre e-mail {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="Définir un pré-en-tête"
>abstract="Un pré-en-tête est un bref résumé qui suit l’objet d’un e-mail lorsque vous le visualisez depuis votre client de messagerie. Dans de nombreux cas, il fournit un bref résumé de l’e-mail, généralement en une seule phrase."

Lors de la conception de vos e-mails, vous pouvez définir des méta-attributs supplémentaires pour votre contenu afin d’en améliorer la lisibilité et l’accessibilité. Le [concepteur d’e-mail](get-started-email-design.md) [!DNL Journey Optimizer] vous permet de définir les éléments suivants :

![](assets/email_body_settings_ex.png)

* **[!UICONTROL Pré-en-tête]** : il s’agit d’un bref résumé qui suit l’objet d’un e-mail lorsque vous le visualisez depuis votre client de messagerie. Dans de nombreux cas, il fournit un bref résumé de l’e-mail, généralement en une seule phrase.

  >[!NOTE]
  >
  >Les pré-en-têtes ne sont pas pris en charge par tous les clients de messagerie. Le pré-en-tête ne s’affiche pas s’il n’est pas pris en charge.

* **[!UICONTROL Titre du document]** : ce champ, qui correspond à l’élément `<title>`, fournit des informations descriptives sur le contenu de votre e-mail, généralement affichées sous la forme d’une infobulle lorsque vous pointez dessus. Il peut aider les utilisateurs et utilisatrices en situation de handicap en fournissant un contexte supplémentaire et peut contribuer à une meilleure compréhension de votre contenu par les moteurs de recherche.

* **[!UICONTROL Langue du document]** : pour garantir l’accessibilité, vous pouvez spécifier la langue que les lecteurs d’écran utiliseront pour convertir le texte et les images en parole ou en braille (pour les personnes ayant des déficiences visuelles ou des troubles de l’apprentissage). Ce paramètre correspond à l’attribut `lang` dans l’élément `<html>`.

Pour configurer ces paramètres, procédez comme suit.

1. À partir du [concepteur d’e-mail](content-from-scratch.md), ajoutez au moins un **[!UICONTROL composant Structure]** pour commencer à concevoir votre e-mail.

1. Cliquez sur **[!UICONTROL Corps]** dans l’**[!UICONTROL arborescence de navigation]** à gauche ou en haut du volet de droite.

   ![](assets/email_body.png)

1. Dans l’onglet **[!UICONTROL Paramètres]**, saisissez du texte dans les champs **[!UICONTROL Pré-en-tête]**, **[!UICONTROL Titre du document]** et/ou **[!UICONTROL Langue du document]**.

1. Vous pouvez également cliquer sur l’icône de personnalisation en regard de chaque champ pour personnaliser votre contenu à partir des attributs de profil, des audiences, des attributs contextuels, etc. [En savoir plus sur la personnalisation](../personalization/personalization-build-expressions.md)

   ![](assets/email_body_settings.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer vos modifications.