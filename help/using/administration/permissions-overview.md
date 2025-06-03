---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des utilisateurs et des utilisatrices - Vue d’ensemble
description: Découvrez comment définir et gérer les autorisations.
feature: Access Management
topic: Administration
role: Admin, Architect
level: Intermediate
keywords: autorisations, droits, restrictions, accès, sandbox
exl-id: b8e266b1-d8eb-4c77-9341-9761b82609b0
source-git-commit: 8093af8c3e7484f9ebed8dbc50065bcff0459581
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 38%

---

# Prise en main du contrôle d’accès {#permissions-overview}

[!DNL Journey Optimizer] vous permet de définir et de gérer les autorisations attribuées à différents utilisateurs. Les autorisations sont un ensemble de droits et de restrictions qui autorisent ou refusent l&#39;accès aux fonctionnalités du produit.

Le contrôle d’accès pour [!DNL Journey Optimizer] est fourni via l’**Autorisations** dans Adobe Experience Cloud. Cette fonctionnalité exploite les rôles et les politiques, liant les utilisateurs et utilisatrices à des autorisations et des sandbox.

Pour configurer le contrôle d’accès de Journey Optimizer, vous devez disposer des privilèges d’administrateur système ou produit pour votre organisation. Le rôle minimum qui permet d’accorder ou de retirer des autorisations est un administrateur ou une administratrice de produit. Les autres rôles d’administrateur ou d’administratrice qui peuvent gérer les autorisations sont les administrateurs ou administratrices système (aucune restriction). Pour plus d’informations, consultez l’article [Centre d’aide Adobe](https://helpx.adobe.com/fr/enterprise/using/admin-roles.html){target="_blank"} sur les rôles administratifs .

<!-- A high-level workflow for gaining and assigning access permissions can be summarized as follows:

* After licensing [!DNL Journey Optimizer], an email is sent to the administrator specified during licensing.
* The administrator logs in to Adobe Admin Console and selects [!DNL Journey Optimizer] from the list of products on the overview page.
* To grant access to [!DNL Journey Optimizer], it is recommended that the administrator add users to the default product profile
* In Experience Platform Permissions, the administrator can create new roles or edit the permissions and users for any existing roles.
* When creating or editing a role, the administrator adds users to the role using the users tab, and grants permissions to these users (such as "Read Datasets" or "Manage Schemas") by editing the role's permissions. Similarly, the administrator can assign access to sandboxes using the same editing option.
* When users log in to the Journey Optimizer user interface, their access to capabilities is driven by the permissions that have been granted to them from the previous step. For example, if a user does not have the View Datasets permission, the Datasets tab in the side menu will not be visible to that user.-->


La gestion des utilisateurs dans [!DNL Journey Optimizer] repose sur les concepts clés suivants :

* **[!UICONTROL Rôle]** : les rôles font référence à un ensemble d’utilisateurs qui partagent les mêmes autorisations et sandbox. Ces rôles vous permettent de gérer facilement l’accès et les autorisations pour différents groupes d’utilisateurs et d’utilisatrices au sein de votre organisation. Un rôle s’accompagne d’un ensemble de droits unitaires qui permettent aux utilisateurs et utilisatrices d’accéder à certaines fonctionnalités ou à certains objets de l’interface. Avec [!DNL Journey Optimizer], vous pouvez choisir parmi un éventail de **[!UICONTROL rôles]** préexistants, chacun avec différents niveaux d’autorisations, à affecter à vos utilisateurs et utilisatrices. En savoir plus sur les **rôles intégrés** disponibles sur [cette page](ootb-product-profiles.md).

* **[!UICONTROL Autorisations]** : droits unitaires qui permettent de définir les autorisations attribuées aux **[!UICONTROL Rôles]**. Chaque autorisation est regroupée sous des ressources, par exemple Parcours ou Offres, ce qui représente les différentes fonctionnalités ou objets dans [!DNL Journey Optimizer]. Pour en savoir plus, consultez la section [Niveaux d’autorisation](high-low-permissions.md).

  ![](assets/do-not-localize/permissions_2.png)

* **[!UICONTROL Sandbox]** : sandbox virtuels qui divisent les instances en environnements virtuels distincts et isolés. Les sandbox sont affectées par le biais de rôles dans les autorisations. En savoir plus sur [l’utilisation des sandbox](sandboxes.md).

* **Contrôle d’accès basé sur l’objet** : libellés pour limiter l’accès à un objet. Cette approche protège les ressources numériques sensibles contre les utilisateurs non autorisés et assure une protection supplémentaire des données personnelles. En savoir plus sur la [Gestion des accès basée sur les objets](object-based-access.md).

* **Contrôle d’accès basé sur les attributs** : autorisations de gérer l’accès aux données pour des équipes ou des groupes d’utilisateurs spécifiques. Le contrôle d’accès basé sur les attributs permet aux administrateurs de contrôler l’accès à des objets et/ou fonctionnalités spécifiques en fonction d’attributs. Les attributs peuvent être des métadonnées ajoutées à un objet, comme un libellé ajouté à un champ ou à un segment de schéma. Un administrateur définit des politiques d’accès qui incluent des attributs pour gérer les autorisations d’accès des utilisateurs. En savoir plus sur la [Gestion des accès basée sur les attributs](attribute-based-access.md).


## Explorons plus en détail

Maintenant que vous connaissez les concepts du contrôle d’accès dans **[!DNL Journey Optimizer]**, il est temps d’examiner plus en détail ces sections de documentation pour commencer à configurer les autorisations.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="permissions.md">
<img alt="Autorisations" src="assets/do-not-localize/role.jpg">
</a>
<div>
<a href="permissions.md"><strong>Accorder l’accès</strong></a>
</div>
<p>
</td>
<td>
<a href="ootb-permissions.md">
<img alt="Autorisations intégrées" src="assets/do-not-localize/select.jpg">
</a>
<div>
<a href="ootb-permissions.md"><strong>Autorisations intégrées</strong></a>
</div>
<p>
</td>
<td>
<a href="sandboxes.md">
<img alt="gestion des sandbox" src="assets/do-not-localize/sandboxes.jpg">
</a>
<div>
<a href="sandboxes.md"><strong>Gestion des sandbox</strong></a>
</div>
<p>
</td>
<td>
<td>
<a href="attribute-based-access.md">
<img alt="Contrôle d’accès basé sur les attributs" src="assets/do-not-localize/data-access.jpeg">
</a>
<div>
<a href="attribute-based-access.md"><strong> Contrôle d’accès basé sur les attributs </strong></a>
</div>
<p>
</td>
<td>
</tr></table>
