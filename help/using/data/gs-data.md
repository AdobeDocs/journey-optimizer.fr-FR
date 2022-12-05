---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des données dans  [!DNL Journey Optimizer]
description: Découvrez comment utiliser les données dans  [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 2dcfcc8d7006c92e046152db5ac1288bdde8b063
workflow-type: ht
source-wordcount: '891'
ht-degree: 100%

---

# Prise en main de la gestion des données dans [!DNL Journey Optimizer] {#about-data}

La richesse et la couverture des données des clients finaux sont des éléments qui définissent la force et le succès de toute solution d’expérience client ; et ces données sont sacrées et d’une valeur maximale pour un client donné. La sélection de technologies est désormais intrinsèquement intégrée à l’évaluation rigoureuse des fonctionnalités de gestion des données.

Adobe Journey Optimizer vous permet de gérer, conserver et exporter en toute facilité ces données vers des plateformes ou systèmes faisant partie de votre pile technologique.

**Mes données, mes règles** : Journey Optimizer crée en continu (et en temps réel) un jeu riche de données sur le profil client, en plus de toutes les données sur les parcours et les offres qui sont inhérentes à ses opérations. Les versions provisoires des données utilisateur ingérées à partir de vos bases de données sont enrichies et transformées en données de grande valeur, dotées de portée et de profondeur. Vous voulez que ces données soient sûres et en même temps omniprésentes, afin d’en tirer parti dans votre écosystème informatique tout entier.

Dans l’ensemble, la flexibilité que vous souhaitez obtenir de vos données se divise en trois parties :


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinations" src="assets/do-not-localize/dest.png" /> 
 <br>Disponible dans d’autres destinations : bien que Journey Optimizer optimise et intègre les données pour offrir une expérience client hyper-personnalisée, vous souhaitez que ces données puissent se retrouver dans d’autres systèmes de votre paysage technologique, tout en recherchant d’autres moyens d’exploiter ces données.
    <div>
     <a href="../start/ajo-integrations.md">En savoir plus</a></div>
    </div>
    <br>
  </td>
</tr>
  <td>
    <div><img alt="rétention" src="assets/do-not-localize/retention.png" />  
    <br>Conservée pendant une durée spécifiée : les réglementations du secteur ou régionales (telles que le RGPD ou le CCPA) ou les politiques internes de gouvernance des données indiquent la durée pendant laquelle les données doivent être conservées ou archivées dans le lac de données Adobe Experience Platform. <a href="../privacy/get-started-privacy.md">En savoir plus</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <div><img alt="politique" src="assets/do-not-localize/policy.png" /> 
    <br>Suppression d’une base de données dans un délai convenu pour votre politique - la suppression des données est un aspect important de la protection des données et une étape clé dans tous les processus de gouvernance des données. Journey Optimizer peut produire plus de données que nécessaire. En outre, vous souhaitez prêter plus d’attention à ce qui se passe après la durée requise pour un jeu de données, que ce soit en raison de son utilité ou de sa réglementation. Le contrôle dont vous avez besoin consiste à supprimer des données à un moment donné. <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html?lang=fr">Pour en savoir plus sur l’hygiène de données, consultez la documentation relative à Adobe Experience Platform.</a></div>
  </td>
</tr>
</table>

Adobe Experience Platform, sur lequel Journey Optimizer est créé, vous offre les niveaux de contrôle des données les plus élevés lors de l’engagement, ainsi qu’à la fin de l’engagement. Dans Journey Optimizer, vous avez un contrôle total sur les données (qui sont introduites ou générées par Journey Optimizer), la gouvernance superposée à ces données et les destinations vers lesquelles ces données sont envoyées.

Toutes les données sont considérées comme la propriété des clients et ne peuvent être conservées, chiffrées, distribuées ou détruites qu’à votre requête. Adobe agit comme votre fiduciaire, sans aucun droit sur vos données.

Vous pouvez utiliser la flexibilité des données de Journey Optimizer pour répondre à vos besoins spécifiques liés à la conservation, l’archivage ou la suppression des données :

* **Extraction/exportation des données** : vous pouvez lancer l’extraction des données sources à tout moment à travers l’API d’accès aux données sans pénalités ni délais. L’[API Data Access](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=fr){target=&quot;_blank&quot;} fournit aux utilisateurs une interface REST axée sur la capacité de découverte et l’accessibilité des jeux de données ingérés dans Experience Platform. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Notez que le contenu utilisé dans les parcours ou les campagnes ne peut pas être extrait à travers l’API ou les méthodes de destination mentionnées ci-dessus.

* **Conservation des données du service de profil** : pour les données comportementales et de séries temporelles ajoutées à n’importe quel profil, vous pouvez choisir d’utiliser le paramètre par défaut de Journey Optimizer, qui permet de conserver ces données pendant 30 jours au maximum à compter de la date de leur ajout à un profil, ou jusqu’à une autre période sélectionnée par vous. Le délai pendant lequel Adobe conserve ces données varie d’un contrat à l’autre et il est précisé dans la politique de conservation des données d’une entreprise.

   E savoir plus sur l’expiration d’un événement d’expérience dans la [documentation relative à Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html?lang=fr){target=&quot;_blank&quot;}.

* **Purge et mécanismes d’archivage** : la purge et l’archivage des données peuvent être librement définis et automatisés dans Journey Optimizer afin d’automatiser les politiques de conservation des données. Il est possible de définir différentes politiques de vieillissement pour les différentes entités de données. Des mécanismes d’exportation peuvent également être définis pour exporter automatiquement les données âgées avant qu’elles ne soient purgées ou archivées.

   L’espace de travail Hygiène des données dans l’interface utilisateur d’Adobe Experience Platform vous permet de créer et de surveiller diverses tâches d’hygiène des données, notamment la suppression des identités des clients et la planification des expirations de jeux de données. Cet espace de travail est disponible avec Security &amp; Privacy Shield (Bouclier de sécurité et de confidentialité) et Healthcare Shield (Bouclier santé). Pour en savoir plus, consultez la [documentation d’Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html?lang=fr){target=&quot;_blank&quot;}.

* **Lac de données et suppressions** : les données clients stockées dans le lac de données peuvent être conservées par Journey Optimizer :

   * pendant 7 jours afin de faciliter l’intégration des données clients dans les services de profil, après quoi elles peuvent être supprimées de manière permanente, ou
   * jusqu’à ce que vous choisissiez de les supprimer.


* **Extraction de données à l’arrêt/à la fin de l’engagement** : lorsque le contrat est résilié, vos données sont complètement supprimées de l’espace de stockage Adobe. Vous pouvez également extraire des extraits de profil complets avant de résilier un contrat. Cette fonctionnalité n’engendre aucun frais supplémentaire. Cela peut être fait à tout moment et pas seulement à la résiliation.

Les méthodes ci-dessus sont définies contractuellement et décrites en détail dans l’accord de traitement des données (DPA) qu’Adobe passe avec vous au début du contrat. Les applications Adobe, y compris Journey Optimizer, sont conçues selon le principe selon lequel les données de chaque client et cliente doivent être traitées comme une ressource de données propriétaire de ce client ou de cette cliente.
