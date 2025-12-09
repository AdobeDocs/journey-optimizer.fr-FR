---
title: Catalogue d’éléments
description: Découvrir comment utiliser le catalogue d’éléments
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
version: Journey Orchestration
source-git-commit: 20408838a030ceeb8e61f5e1b80d910a8a21b87d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 87%

---

# Configurer le catalogue d’éléments {#catalog}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="Définir les attributs personnalisés"
>abstract="Les attributs personnalisés sont des attributs spécifiques, adaptés à vos besoins, que vous pouvez affecter à un élément de décision. Ils sont créés dans le schéma de catalogue des éléments de décision."

Dans la prise de décision, les catalogues servent de conteneurs centraux pour organiser les éléments de décision. Chaque catalogue est lié à un schéma Adobe Experience Platform, englobant tous les attributs affectés à un élément de décision.

Pour l’instant, tous les éléments de décision créés sont consolidés dans un seul catalogue « Offres », accessible via le menu **[!UICONTROL Catalogues]**.

![](assets/catalogs-list.png)

## Mécanismes de sécurisation et limitations

Pour garantir des performances et une cohérence optimales, la prise de décision applique les mécanismes de sécurisation et limitations suivants :

* **Types de données pris en charge**

  Pour l’instant, la prise de décision prend exclusivement en charge les types de données suivants : chaîne, entier, booléen, date, DateHeure, ressource de prise de décision et objet. Aucun champ ne se trouvant dans ces types de données ne pourra pas être utilisé lors de la création d’un élément de décision ou d’un catalogue.


* **Limite d’attributs personnalisés**

  Chaque élément de décision peut inclure jusqu’à 100 attributs personnalisés.

* **Restrictions d’imbrication**

  Un maximum de quatre niveaux d’imbrication est pris en charge. Les images ne sont pas prises en charge au dernier niveau.

## Accéder au schéma du catalogue et le modifier {#access-catalog-schema}

Pour accéder au schéma du catalogue où les attributs des éléments de décision sont stockés, procédez comme suit :

1. Dans la liste des éléments, cliquez sur le bouton **[!UICONTROL Modifier le schéma]** situé en regard du bouton **[!UICONTROL Créer un élément]**.

1. Le schéma du catalogue s’ouvre dans un nouvel onglet, selon la structure ci-dessous :

   * Le nœud **`_experience`** comprend des attributs d’éléments de décision standard tels que le nom, la date de début et de fin et la description.
   * Le nœud **`_<imsOrg>`** héberge les attributs d’éléments de décision personnalisés, où `<imsOrg>` est remplacé par le nom de votre organisation (par exemple, `_luma` pour la société Luma). Par défaut, aucun attribut personnalisé n’est configuré, mais vous pouvez en ajouter autant que nécessaire pour répondre à vos besoins. Une fois cette opération terminée, les attributs personnalisés s’affichent dans l’écran de création de l’élément de décision à côté des attributs standard.

   ![](assets/catalogs-schema.png)

1. Pour ajouter un attribut personnalisé au schéma, développez le nœud de votre organisation (par exemple, **`_luma`**) et cliquez sur le bouton « + » à l’emplacement souhaité dans la structure.

   ![](assets/catalogs-add.png)

1. Renseignez les champs nécessaires pour l’attribut ajouté et cliquez sur **[!UICONTROL Appliquer]**.

   La valeur saisie sur un attribut avec l’attribut de ressource de prise de décision est une URL publique. La plupart du temps, cela pointe vers une image.

   Vous trouverez des informations détaillées sur l’utilisation des schémas Adobe Experience Platform dans la [Documentation du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=fr).

1. Une fois les attributs personnalisés souhaités ajoutés, enregistrez le schéma. Le nouveau champ est désormais disponible dans l’écran de création des éléments de décision, dans la section **[!UICONTROL Attributs personnalisés]**.


   L’exemple ci-dessous montre un écran de création d’élément avec des attributs personnalisés tels que des objets définis dans le schéma.

   ![](assets/custom-attributes.png)

