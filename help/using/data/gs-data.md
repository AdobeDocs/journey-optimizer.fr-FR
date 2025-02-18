---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main de la gestion des données dans Journey Optimizer
description: Découvrez comment utiliser les données dans Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: données, gestion, platform
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 46c4d3081603115db71b01a05f12187cd7e0d34c
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 98%

---

# Prise en main de la gestion des données {#about-data}

La richesse et la couverture des données des clients et clientes finaux sont des éléments qui définissent la force et le succès de toute solution d’expérience client. Pour tout(e) client(e), ces données revêtent un caractère sacré et sont d’une valeur inestimable. La sélection de technologies est désormais intrinsèquement intégrée à l’évaluation rigoureuse des fonctionnalités de gestion des données.

Avec [!DNL Adobe Journey Optimizer], vous pouvez facilement gérer, conserver et exporter vos données vers les autres plateformes ou systèmes que vous utilisez.

**Mes données, mes règles** : [!DNL Adobe Journey Optimizer] crée en continu (et en temps réel) un jeu riche de données sur le profil client, en plus de toutes les données sur les parcours et les offres qui sont inhérentes à ses opérations. Les versions provisoires des données utilisateur ingérées à partir de vos bases de données sont enrichies et transformées en données de grande valeur, dotées de portée et de profondeur. Vous voulez que ces données soient sûres et en même temps omniprésentes, afin d’en tirer parti dans votre écosystème informatique tout entier.

En général, la flexibilité que vous souhaitez obtenir de vos données est la suivante :


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinations" src="assets/do-not-localize/dest.png" />
<br>Disponible dans d’autres destinations : bien qu’[!DNL Adobe Journey Optimizer] optimise et intègre les données pour offrir une expérience client hyper-personnalisée, vous souhaitez que ces données puissent se retrouver dans d’autres systèmes de votre paysage technologique, tout en recherchant d’autres moyens d’exploiter ces données.
    <div>
     <a href="../integrations/ajo-integrations.md">En savoir plus</a></div>
    </div>
    <br>
  </td>
</tr>
</table>

<!--td>
    <div><img alt="retention" src="assets/do-not-localize/retention.png" />  
    <br>Retained for a stipulated duration – Industry or regional regulations (such as GDPR or CCPA) or internal data governance policies stipulate how long or how short a duration, data needs to be maintained or archived in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Learn more</a></div>
  </td>
</tr>
<tr style="border: 0;"-->
<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="politique" src="assets/do-not-localize/policy.png" />
<br>Suppression d’une base de données dans un délai convenu pour votre politique - la suppression des données est un aspect important de la protection des données et une étape clé dans tous les processus de gouvernance des données. [!DNL Adobe Journey Optimizer] peut produire plus de données que nécessaire. En outre, vous devriez prêter la plus grande attention à ce qui se passe après la durée requise pour un jeu de données, que ce soit en raison de son utilité ou de sa réglementation. Le contrôle dont vous avez besoin consiste à supprimer des données à un moment donné. 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">En savoir plus</a>.</div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], sur laquelle est créé, vous offre les niveaux de contrôle des données les plus élevés lors de l’engagement, ainsi qu’à la fin de l’engagement.[!DNL Adobe Journey Optimizer] Dans [!DNL Journey Optimizer], vous avez un contrôle total sur les données (qui sont introduites ou générées par [!DNL Journey Optimizer]), la gouvernance superposée à ces données et les destinations vers lesquelles ces données sont envoyées.

Toutes les données sont considérées comme la propriété des clients et ne peuvent être conservées, chiffrées, distribuées ou détruites qu’à votre requête. Adobe agit comme votre fiduciaire, sans aucun droit sur vos données.

Vous pouvez utiliser la flexibilité des données de [!DNL Journey Optimizer] pour répondre à vos besoins spécifiques liés à la conservation, l’archivage ou la suppression des données :

* **Extraction/exportation des données** : vous pouvez lancer l’extraction des données sources à tout moment à travers l’API d’accès aux données sans pénalités ni retards. L’[API Data Access](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=fr){target="_blank"} fournit aux utilisateurs et utilisatrices une interface RESTful axée sur la capacité de découverte et l’accessibilité des jeux de données ingérés dans [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

  Notez que le contenu utilisé dans les parcours ou les campagnes ne peut pas être extrait à travers l’API ou les méthodes de destination mentionnées ci-dessus.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer's default setting of retaining this data for up to 91 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization's data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **Purge et mécanismes d’archivage** : la purge et l’archivage des données peuvent être librement définis et automatisés dans [!DNL Adobe Journey Optimizer] afin d’automatiser les politiques de conservation des données. Il est possible de définir différentes politiques de vieillissement pour les différentes entités de données. Des mécanismes d’exportation peuvent également être définis pour exporter automatiquement les données âgées avant qu’elles ne soient purgées ou archivées.

  L’espace de travail Hygiène des données vous permet de créer et de surveiller diverses tâches d’hygiène des données, notamment la suppression des identités des client(e)s et la planification des expirations de jeux de données. Cet espace de travail est disponible avec Security &amp; Privacy Shield et Healthcare Shield. En savoir plus sur [cette page](../privacy/data-hygiene.md).

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Extraction de données à l’arrêt/à la fin de l’engagement** : lorsque le contrat est résilié, vos données sont complètement supprimées de l’espace de stockage Adobe. Vous pouvez également extraire des extraits de profil complets avant de résilier un contrat. Cette fonctionnalité n’engendre aucun frais supplémentaire. Cela peut être fait à tout moment et pas seulement à la résiliation.

Les méthodes ci-dessus sont définies contractuellement et décrites en détail dans l’accord de traitement des données (DPA) qu’Adobe passe avec vous au début du contrat. Les applications Adobe, y compris [!DNL Journey Optimizer], sont conçues selon le principe selon lequel les données de chaque client et cliente doivent être traitées comme une ressource de données propriétaire de ce client ou de cette cliente.
