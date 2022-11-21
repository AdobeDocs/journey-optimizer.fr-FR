---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des données dans [!DNL Journey Optimizer]
description: Découvrez comment utiliser les données dans [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 2dcfcc8d7006c92e046152db5ac1288bdde8b063
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 4%

---

# Prise en main de la gestion des données dans [!DNL Journey Optimizer] {#about-data}

La richesse et la couverture des données des clients finaux sont les éléments qui définissent la force et le succès de toute solution d’expérience client ; et ces données sont sacrées et d’une valeur maximale pour un client donné. La sélection de technologies est désormais intrinsèquement intégrée à l’évaluation rigoureuse des fonctionnalités de Data Management.

Avec Adobe Journey Optimizer, vous pouvez facilement gérer, conserver et exporter ces données vers des plateformes ou des systèmes qui font partie de votre pile technologique.

**Mes données, mes règles** - Journey Optimizer crée continuellement (et en temps réel) un ensemble riche de données de profil client, en plus de toutes les données de parcours et de données d’offre inhérentes à ses opérations. Les versions de navigateur des données utilisateur ingérées à partir de vos bases de données sont enrichies et transformées en données de grande valeur avec une couverture et une profondeur. Vous voulez que ces données soient sûres et omniprésentes, de sorte que vous puissiez exploiter leur valeur dans votre écosystème informatique global.

Dans l’ensemble, la flexibilité que vous souhaitez obtenir de vos données se divise en trois parties :


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinations" src="assets/do-not-localize/dest.png" /> 
    <br>Disponible dans d’autres destinations : bien que Journey Optimizer optimise et intègre les données pour offrir une expérience client hyper-personnalisée, vous souhaitez que ces données soient contenues dans d’autres systèmes de votre paysage technologique global, tout en recherchant d’autres moyens d’exploiter ces données.
    <div>
     <a href="../start/ajo-integrations.md">En savoir plus</a></div>
    </div>
    <br>
  </td>
</tr>
  <td>
    <div><img alt="rétention" src="assets/do-not-localize/retention.png" />  
    <br>Conservée pendant une durée spécifiée : les réglementations du secteur ou régionales (telles que le RGPD ou le CCPA) ou les politiques internes de gouvernance des données stipulent la durée ou la durée spécifiée pendant laquelle les données doivent être conservées ou archivées dans le lac de données Adobe Experience Platform. <a href="../privacy/get-started-privacy.md">En savoir plus</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <div><img alt="policy" src="assets/do-not-localize/policy.png" /> 
    <br>Suppression d’une base de données dans un délai convenu pour votre politique - La suppression des données est un aspect essentiel de la protection des données et une étape clé de tous les processus de gouvernance des données. Journey Optimizer peut produire plus de données que nécessaire. En outre, vous souhaitez prendre la plus grande attention à ce qui se passe après la durée requise pour un jeu de données, que ce soit en raison de son utilité ou de sa réglementation. Le contrôle dont vous avez besoin consiste à supprimer des données à un moment donné. <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html">En savoir plus sur l’hygiène des données dans la documentation Adobe Experience Platform</a></div>
  </td>
</tr>
</table>

Adobe Experience Platform, sur lequel Journey Optimizer est créé, vous offre les niveaux de contrôle des données les plus élevés au cours de l’engagement, ainsi qu’à la fin de l’engagement. Dans Journey Optimizer, vous avez un contrôle total sur les données (qui sont introduites ou générées par Journey Optimizer), la gouvernance superposée à ces données et les destinations vers lesquelles ces données sont envoyées.

Toutes les données sont considérées comme la propriété des clients et ne peuvent être conservées, chiffrées, distribuées ou détruites qu’à votre demande. L&#39;Adobe agit comme votre fiduciaire, sans aucun droit sur vos données.

Vous pouvez utiliser la flexibilité des données de Journey Optimizer pour répondre à vos besoins spécifiques liés à la conservation, l’archivage ou la suppression des données :

* **Extraction/exportation de données**: Vous pouvez lancer l’extraction des données source à tout moment via l’API d’accès aux données sans pénalités ni délais. Le [API Data Access](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target=&quot;_blank&quot;} fournit aux utilisateurs une interface RESTful axée sur la capacité de découverte et l’accessibilité des jeux de données ingérés dans l’Experience Platform. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Notez que le contenu utilisé dans les parcours ou les campagnes ne peut pas être extrait via l’API ou les méthodes de destination mentionnées ci-dessus.

* **Rétention des données du service de profil**: Pour les données de série comportementale et temporelle ajoutées à n’importe quel profil, vous pouvez choisir d’utiliser le paramètre par défaut de Journey Optimizer, qui permet de conserver ces données pendant 30 jours au maximum à compter de la date de leur ajout à un profil, ou jusqu’à une autre période sélectionnée par vous. Le délai au cours duquel l’Adobe conserve ces données varie d’un contrat à l’autre. Il est précisé dans la politique de conservation des données d’une organisation.

   En savoir plus sur les expirations d’événements d’expérience dans [Documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target=&quot;_blank&quot;}.

* **Purge et mécanismes d&#39;archivage**: La purge des données et l’archivage peuvent être librement définis et automatisés dans Journey Optimizer afin d’automatiser les stratégies de conservation des données. Il est possible de définir différentes stratégies de vieillissement pour les différentes entités de données. Des mécanismes d’exportation peuvent également être définis pour exporter automatiquement les données obsolètes avant qu’elles ne soient purgées ou archivées.

   L’espace de travail Nettoyage des données dans l’interface utilisateur d’Adobe Experience Platform vous permet de créer et de surveiller diverses tâches de nettoyage de données, notamment la suppression des identités des clients et la planification des expirations de jeux de données. Cet espace de travail est disponible avec le Bouclier de sécurité et de confidentialité et le Bouclier de santé. Pour en savoir plus, consultez la [documentation d’Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html){target=&quot;_blank&quot;}.

* **Lac de données et suppressions**: Les données client stockées dans le lac de données peuvent être conservées par Journey Optimizer :

   * pendant 7 jours afin de faciliter l’intégration des données client dans les services de profil, après quoi elles peuvent être supprimées de manière permanente, ou
   * jusqu’à ce que vous choisissiez d’être supprimé par vous


* **Extraction de données à l’arrêt/à la sortie de l’engagement**: Lorsque le contrat est résilié, vos données sont complètement supprimées de l’espace de stockage d’Adobe. Vous pouvez également extraire des extraits de profil complets avant de mettre fin à un accord. Cette fonctionnalité n’engendre aucuns frais supplémentaires. Cela peut être fait à tout moment et pas seulement à la fermeture.

Les méthodes ci-dessus sont définies contractuellement et décrites en détail dans l’accord de traitement des données (DPA) qui, au début d’un engagement, est d’accord avec vous. Les applications Adobe, y compris Journey Optimizer, sont conçues selon le principe selon lequel les données de chaque client doivent être traitées comme une ressource de données propriétaire de ce client.
