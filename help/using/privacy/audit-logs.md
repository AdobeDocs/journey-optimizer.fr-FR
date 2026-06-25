---
solution: Journey Optimizer
product: journey optimizer
title: Actions d’audit sur les ressources Journey Optimizer
description: Découvrez comment effectuer le suivi des actions effectuées sur les ressources Journey Optimizer.
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
TQID: https://experienceleague.adobe.com/Usk3qin9P4IZlKw-gEI4zaKO-aRtaKq9-0GMVlOecjA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4e89993a998268ae2810c949d0669bf6dc458dd6
workflow-type: ht
source-wordcount: 380
ht-degree: 100%

---

# Actions d’audit sur les ressources Journey Optimizer {#track-changes}

>[!BEGINSHADEBOX]

**Sur cette page :** consultez les journaux d’audit qui enregistrent les actions des utilisateurs et des utilisatrices sur les ressources Journey Optimizer pour vous permettre d’accroître la visibilité, de résoudre les problèmes et de montrer la conformité aux réglementations et aux politiques de gestion des données.

>[!ENDSHADEBOX]

## À propos des journaux d’audit {#audit-logs}

>[!IMPORTANT]
>
>Pour afficher et exporter le journal d’audit, l’autorisation **[!DNL View User Activity Log]** doit vous avoir été accordée. [En savoir plus](../administration/ootb-product-profiles.md)

Avec Journey Optimizer, vous pouvez identifier les actions effectuées par les utilisateurs du système sur divers services et fonctionnalités tels que les parcours, les messages, les pages de destination, etc.

Cela vous permet d’accroître la visibilité des activités exécutées dans le système, de résoudre les problèmes et d’aider votre entreprise à se conformer aux réglementations et aux politiques de gestion des données d’entreprise.

Chaque action est enregistrée avec des métadonnées dans des « journaux d’audit » qui sont accessibles dans Adobe Experience Platform. Pour plus d’informations sur les journaux d’audit, y compris sur leur affichage et leur gestion dans l’interface d’utilisation ou l’API, reportez-vous à la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=fr).

![](assets/audit-logs.png)

## Types d’événements capturés par les logs d’audit {#events}

Le tableau ci-dessous présente les actions sur lesquelles les ressources Journey Optimizer sont enregistrées par les logs d’audit. La liste complète des actions capturées dans les logs d’audit est disponible dans la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=fr#category).

>[!NOTE]
>
>Les logs d’audit liés à la **gestion des décisions** ne sont visibles qu’à partir du fichier CSV qui peut être téléchargé à l’aide du bouton **[!UICONTROL Télécharger le journal]**.

| Ressource | Action |
|-----------|------------------|
| Campagne AJO | Créer/Supprimer/Mettre à jour/Activer/Arrêter |
| Paramètre général du canal AJO | Créer / Supprimer / Mettre à jour |
| Groupe d’adresses IP AJO | Créer / Supprimer / Mettre à jour |
| Page de destination AJO | Créer / Supprimer / Mettre à jour / Publier / Dépublier |
| Modèle HTML de page de destination AJO | Créer / Supprimer / Mettre à jour |
| Préréglage de la page de destination AJO | Créer / Supprimer / Mettre à jour |
| Sous-domaine de page de destination AJO | Créer / Supprimer / Mettre à jour |
| Préréglage de message AJO | Créer / Supprimer / Mettre à jour |
| Enregistrement PTR AJO | Créer / Supprimer / Mettre à jour |
| Modèle d’expression enregistré AJO | Créer / Supprimer / Mettre à jour |
| Informations d’identification de l’API SMS AJO | Créer / Supprimer / Mettre à jour |
| Sous-domaine AJO | Créer / Supprimer / Mettre à jour |
| Liste de suppression AJO | Créer / supprimer / télécharger un fichier CSV |
| Groupe de champs | Créer / Supprimer / Mettre à jour |
| Parcours | Créer / Supprimer / Mettre à jour / Arrêter / Publier |
| Action personnalisée de parcours | Créer / Supprimer / Mettre à jour |
| Source de données de parcours | Créer / Supprimer / Mettre à jour |
| Événement de parcours | Créer / Supprimer / Mettre à jour |
| Fragment de parcours | Créer / Supprimer / Mettre à jour / Activer / Archiver |
| Règle de fréquence des messages | Créer / Supprimer / Mettre à jour |
| Stratégie de classement | Créer / Supprimer / Mettre à jour |
