---
solution: Journey Optimizer
product: journey optimizer
title: Fragments de contenu AEM
description: Découvrir comment accéder aux fragments de contenu AEM et comment les gérer
topic: Content Management
role: User
level: Beginner
source-git-commit: b06229e7a2fc64fbe28154c798b152cca8203a86
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 12%

---

# Prise en main des fragments de contenu Adobe Experience Manager {#aem-fragments}

En intégrant Adobe Experience Manager as a Cloud Service à Adobe Journey Optimizer, vous pouvez désormais incorporer facilement vos fragments de contenu AEM dans le contenu de Journey Optimizer. Cette connexion rationalisée simplifie le processus d’accès au contenu AEM et d’utilisation de celui-ci, ce qui permet de créer des campagnes et des parcours personnalisés et dynamiques.

Pour en savoir plus sur les fragments de contenu AEM, voir [Utilisation des fragments de contenu](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} dans la documentation d’Experience Manager.

## Avant de commencer {#start}

>[!AVAILABILITY]
>
>Pour la clientèle du secteur de la santé, l’intégration n’est activée qu’après l’obtention d’une licence pour les offres complémentaires Journey Optimizer Healthcare Shield et Adobe Experience Manager Enhanced Security.

### Limites {#limitations}

Notez les restrictions suivantes lorsque vous utilisez des fragments de contenu Adobe Experience Manager dans Journey Optimizer :

* **Types de fragments de contenu** : les fragments de contenu simples et les fragments de contenu imbriqués sont pris en charge. Les variations de fragment de contenu ne sont actuellement pas prises en charge.

* **Contenu multilingue** : Seul le flux manuel est pris en charge. Chaque variante de langue doit être créée indépendamment dans Adobe Experience Manager, balisée, publiée et sélectionnée manuellement dans Journey Optimizer. Il n’existe aucun mécanisme automatique de résolution linguistique ou de secours.

* **Accès au référentiel** : Journey Optimizer s’intègre exclusivement au niveau Publication Adobe Experience Manager, où les fragments de contenu sont disponibles via un point d’entrée public non authentifié. Bien que les référentiels de création puissent apparaître dans le sélecteur de référentiel, seuls les fragments de contenu publiés au niveau Publication peuvent être utilisés dans Journey Optimizer.

* **Statut du fragment de contenu** : Journey Optimizer affiche les fragments de contenu avec le statut **Publié** et **Modifié**. Dans tous les cas, seule la dernière version publiée est utilisée. Si un fragment est modifié après publication, ces modifications ne sont pas répercutées dans Journey Optimizer tant que le fragment de contenu n’est pas republié dans Adobe Experience Manager. Il n’existe pas de réconciliation de version automatique entre Adobe Experience Manager et Journey Optimizer.

* **Personalization** : seuls les attributs de profil, les attributs contextuels, les chaînes statiques et les variables prédéclarées sont pris en charge. Les attributs dérivés ou calculés ne sont pas pris en charge.

* **Mises à jour et contrôle de version** : les mises à jour de fragments de contenu nécessitent une republication manuelle depuis Adobe Experience Manager. Il n’existe pas de réconciliation de version automatique entre Adobe Experience Manager et Journey Optimizer. Lorsqu’un fragment de contenu est publié dans Adobe Experience Manager, Journey Optimizer reçoit un événement et des mises à jour du côté Journey Optimizer. En cas de réussite, la mise à jour sera disponible au bout de 5 minutes pour les Parcours unitaires et dans le lot suivant pour les cas d’utilisation par lots.

* **Mise en cache et relecture** : les fragments de contenu sont récupérés en temps réel à partir du niveau Publication Adobe Experience Manager. Il n’existe aucune mise en cache de prérendu ou d’instantané. Les épreuves des campagnes et des parcours reflètent toujours la version publiée la plus récemment du fragment de contenu et les versions historiques ne peuvent pas être verrouillées pour la relecture.

* **Accès utilisateur** : il est recommandé de limiter le nombre d’utilisateurs ayant accès à la publication de fragments de contenu afin de réduire le risque d’erreurs accidentelles.


### Cycle de vie du fragment de contenu

![](assets/do-not-localize/AEM_CF.png)

Les fragments de contenu suivent différentes étapes du cycle de vie en fonction du niveau Adobe Experience Manager dans lequel ils existent. [En savoir plus dans la documentation de Adobe Experience Manager](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

Le contenu est créé et géré au **niveau Auteur**, où les fragments peuvent avoir des statuts tels que Nouveau, Brouillon, Publié, Modifié ou Dépublié. Ces statuts s’appliquent uniquement au **niveau Auteur** et prennent en charge la création et la révision de contenu.

Lorsqu’un fragment de contenu est publié, une copie est créée au **niveau Publication** et exposée via un point d’entrée public non authentifié. Journey Optimizer s’intègre exclusivement à ce **niveau Publication**.

Par conséquent, Journey Optimizer n’affiche que les fragments de contenu publiés ou modifiés et utilise toujours la dernière version publiée. Les modifications apportées après la publication ne sont pas répercutées dans Journey Optimizer tant que le fragment de contenu n’a pas été republié.


## Résolution des problèmes {#troubleshooting}

Si vous rencontrez des problèmes lors de l’utilisation de fragments de contenu Adobe Experience Manager dans Journey Optimizer, reportez-vous aux problèmes et résolutions courants suivants :

| Problème | Cause | Résolution |
|-|-|-|
| **Balise introuvable** ou **fragment de contenu non visible dans le sélecteur** | La syntaxe de la balise Adobe Experience Manager ne correspond pas au format requis `ajo-enabled:{OrgId}/{SandboxName}` | Vérifiez que l’ID de balise utilise l’**ID d’organisation** et le **Nom du sandbox** corrects. Vérifiez qu’il n’y a pas d’espaces ou de séparateurs incorrects. Republiez le fragment de contenu après avoir corrigé la balise . |
| **Le fragment de contenu n’apparaît pas dans la liste** | Le fragment de contenu est à l’état de brouillon ou n’est pas approuvé | Seuls les fragments de contenu approuvés et publiés s’affichent dans le sélecteur Journey Optimizer. Publiez le fragment de contenu dans Adobe Experience Manager et assurez-vous qu’il possède le statut approuvé . |
| **Erreur de variable non définie** | espace réservé Personalization non déclaré dans la balise d’assistance de fragment | Ajoutez tous les paramètres requis dans la balise d’assistance de fragment. Chaque espace réservé utilisé dans le fragment de contenu doit être explicitement déclaré avec son mappage. |
| **L’épreuve affiche un contenu inattendu** | Proof utilise la dernière version publiée de Adobe Experience Manager | Les BAT reflètent toujours la publication la plus récente du fragment de contenu dans Adobe Experience Manager. Si vous avez récemment apporté des modifications à Adobe Experience Manager, republiez le fragment et actualisez l’épreuve. |
| **Erreur de refus d’accès (CPES)** | Rôle utilisateur non autorisé à accéder à certains attributs | Contactez votre administrateur système pour vérifier que votre rôle dispose des autorisations appropriées pour le profil ou les attributs contextuels utilisés dans la personnalisation. |
| **Le fragment affiche du contenu vide ou manquant** | Paramètres de personnalisation requis manquants ou valeurs de secours | Assurez-vous que tous les paramètres requis sont fournis et envisagez d’ajouter des valeurs de secours pour les attributs facultatifs. |

Si le problème persiste, contactez votre représentant Adobe avec des détails sur votre identifiant de fragment de contenu, votre identifiant de campagne ou de parcours, ainsi que tout message d’erreur affiché.
