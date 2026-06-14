---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des profils dans Journey Optimizer
description: Découvrez comment créer et gérer des profils dans Adobe Journey Optimizer
feature: Profiles
role: User
level: Beginner
exl-id: be3936e4-8185-4031-9daf-95eea58077d0
TQID: https://experienceleague.adobe.com/QpLGV-y5qbtmksC-99GU5PtaV-mUA-imew8JDj7-weA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3id: b32bb433-f8c6-4931-8e52-e657230a3bf2id: e95b6013-acbe-46e9-a3b5-b80e14088d7did: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: a51edc00631334874d111d8350ee7b0eb8e81aa5
workflow-type: tm+mt
source-wordcount: 527
ht-degree: 78%

---

# Prise en main des profils {#profiles-gs}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment le profil client en temps réel dans Adobe Journey Optimizer unifie les données client provenant de sources en ligne, hors ligne et tierces en une seule vue et comment accéder au tableau de bord des profils.

>[!ENDSHADEBOX]

## À propos des profils

Tirez profit du profil client en temps réel dans [!DNL Adobe Journey Optimizer] pour obtenir une vue d’ensemble de chaque client en combinant des données issues de plusieurs canaux, notamment des données en ligne, hors ligne, CRM et tierces. Les **profils** vous permettent de consolider vos données client en une vue unifiée offrant un compte horodaté et exploitable de chaque interaction client.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

**Real-time Customer Profile&#x200B;** - Intégrez les attributs et les événements du client provenant de sources en ligne, hors ligne et pseudonymes dans un profil unique et unifié. &#x200B;Utilisez le profil pour impliquer les clients avec des expériences personnalisées en temps réel sur plusieurs points de contact. &#x200B;

**Ingestion de données** : connectez-vous à diverses sources de données pour ingérer des données comportementales, transactionnelles, financières et opérationnelles. Ingérez des données en temps réel ou par le biais de chargements par lots pour maintenir les profils à jour en permanence. Les profils ne sont pas créés directement dans l’interface [!DNL Journey Optimizer] ; ils sont automatiquement créés ou mis à jour dans Adobe Experience Platform lors de l’ingestion des données.

>[!NOTE]
>
>Lors de l’ingestion de données, les e-mails sont sensibles à la casse. Cela signifie que des profils peuvent être créés en double (par exemple, un profil pour John.Greene@luma.com, un autre pour john.greene@luma.com) et utilisés lors du ciblage du destinataire correspondant dans vos parcours et campagnes [!DNL Journey Optimizer].

**Graphique d’identités** - Combinez des données provenant de différentes sources à l’aide des identités du client, telles que les identifiants de fidélité ou les identifiants système CRM. &#x200B;Créez une vue d’ensemble complète du client en mappant les relations entre les différentes identités dans les jeux de données d’une marque. &#x200B;

**Engagement client** - Utilisez le profil client en temps réel pour offrir des expériences contextuelles personnalisées, telles que des offres et des messages ciblés. &#x200B;Impliquez les clients sur différents canaux, notamment les campagnes marketing, le service clientèle et les mises à jour transactionnelles. &#x200B;

**Partage de données** : partagez des profils clients avec les principaux fournisseurs d’espace de stockage dans le cloud tels qu’Amazon Web Services, Microsoft Azure et Google Cloud. Utilisez des profils partagés pour la création de rapports, l’archivage données ou une analyse plus approfondie avec des outils de Business Intelligence.

>[!MORELIKETHIS]
>
>* [Commencer avec la gestion des données dans Journey Optimizer](../data/gs-data.md)
>* [Documentation sur le profil client en temps réel](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=fr){target="_blank"}
>* [Mécanismes de sécurisation par défaut pour les données de profil client en temps réel et la segmentation](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/guardrails){target="_blank"}
>* [Documentation sur l’ingestion de données](https://experienceleague.adobe.com/fr/docs/experience-platform/ingestion/home){target="_blank"}

## Tableau de bord des profils

Pour accéder aux profils, accédez au menu **[!UICONTROL Client ou cliente]**/**[!UICONTROL Profils]** dans le volet de navigation de gauche.

>[!NOTE]
>
>Si votre organisation débute avec [!DNL Adobe Journey Optimizer] et ne dispose pas encore de jeux de données ou de politiques de fusion actifs, le tableau de bord **Profils** n’est pas visible. À la place, l’onglet **Vue d’ensemble** affiche des liens vers la documentation d’Adobe Experience Platform pour vous aider à commencer à utiliser le profil client en temps réel. Pour découvrir comment utiliser le **tableau de bord du profil**, ainsi que pour obtenir des informations détaillées sur les mesures affichées dans le tableau de bord, consultez [cette section](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=fr){target="_blank"}.

Vous pouvez rassembler des données issues de plusieurs sources et les combiner pour obtenir une vue complète de chacun de vos clients ou chacune de vos clientes. Lors de la combinaison de ces données, les politiques de fusion sont les règles utilisées pour déterminer quelle est la priorité des données et quelles données sont combinées pour créer cette vue unifiée. En savoir plus sur les **politiques de fusion** dans cette [documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr){target="_blank"}.

![](assets/profiles-home.png)

## Vidéo pratique {#video}

Découvrez comment Adobe Experience Platform assemble et met à jour des profils clients en temps réel et la façon dont vous pouvez y accéder et les utiliser.

>[!VIDEO](https://video.tv.adobe.com/v/27251?quality=12)
