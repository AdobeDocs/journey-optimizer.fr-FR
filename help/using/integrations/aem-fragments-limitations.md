---
solution: Journey Optimizer
product: journey optimizer
title: Considérations sur les fragments de contenu Adobe Experience Manager et résolution des problèmes
description: Considérations et problèmes courants liés aux fragments de contenu AEM dans Journey Optimizer.
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# Considérations et résolution des problèmes {#aem-fragments-limitations}

## Considérations principales {#considerations}

Tenez compte des points suivants lors de l’utilisation de fragments de contenu provenant de [!DNL Adobe Experience Manager] dans [!DNL Journey Optimizer] :

* **Types de fragment de contenu**
   * Les fragments de contenu simples, les fragments de contenu imbriqués et les **variations de fragment de contenu** sont pris en charge. Sélectionnez la variation lorsque vous insérez le fragment dans [!DNL Journey Optimizer]. Si vous ne sélectionnez pas de variation, la variation **Principal** (le contenu principal du fragment dans [!DNL Adobe Experience Manager]) est utilisée.

* **Contenu multilingue**
   * Chaque variation doit être créée, balisée et publiée dans [!DNL Adobe Experience Manager]. Dans [!DNL Journey Optimizer], sélectionnez la variation de fragment correspondant à chaque langue ou paramètre régional du message.
   * Il n’existe pas de résolution automatique de langue ni de basculement entre les variations.

* **Accès au référentiel**
   * [!DNL Journey Optimizer] s’intègre uniquement au niveau [!DNL Adobe Experience Manager] **Publication** (Sites, Fragments de contenu). Les fragments de contenu sont disponibles via un point d’entrée public non authentifié.
   * Les référentiels de création peuvent apparaître dans le sélecteur de référentiels, mais seuls les fragments publiés sur **Publier** peuvent être utilisés dans [!DNL Journey Optimizer].

* **Statut du fragment de contenu**
   * Les fragments peuvent afficher l’état **[!UICONTROL Publié]** ou **[!UICONTROL Modifié]** ; [!DNL Journey Optimizer] utilise toujours la **dernière version publiée**.
   * Les modifications apportées après la publication ne sont pas répercutées dans [!DNL Journey Optimizer] tant que le fragment n’a pas été republié dans [!DNL Adobe Experience Manager]. Il n’existe pas de réconciliation de version automatique entre les deux produits.

* **Personnalisation**
   * Pris en charge : attributs de profil, attributs contextuels, chaînes statiques et variables prédéclarées.
   * Non pris en charge : attributs dérivés ou calculés.

* **Mises à jour et contrôle de version**
   * Les mises à jour nécessitent une republication manuelle à partir de [!DNL Adobe Experience Manager]. Il n’existe pas de réconciliation de version automatique.
   * Lorsqu’un fragment de contenu est publié ou republié dans [!DNL Adobe Experience Manager], [!DNL Journey Optimizer] le met à jour et actualise **toutes les variations de ce fragment qui sont référencées** dans les campagnes ou parcours actifs.
   * L’[!DNL Adobe Experience Manager] [action de publication](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/assets/manage/manage-publication) peut être retardée. Une fois l’opération terminée, [!DNL Journey Optimizer] reçoit un événement et actualise le contenu.
   * Après une mise à jour réussie, les modifications sont généralement disponibles dans les **5 minutes environ** pour les parcours unitaires, et dans le **lot suivant** pour les cas d’utilisation par lots.

* **Mise en cache et vérification**
   * Lorsqu’un fragment est ajouté pour la première fois à une campagne ou un parcours, [!DNL Journey Optimizer] le met en cache. Si vous sélectionnez un fragment qui a déjà été utilisé ailleurs via **[!UICONTROL Ouvrir le sélecteur AEM CF]**, il est chargé à partir du cache [!DNL Journey Optimizer].
   * Après avoir republié un fragment modifié dans [!DNL Adobe Experience Manager], [!DNL Journey Optimizer] écoute l’événement et met à jour le cache.
   * Les épreuves reflètent toujours la version **la plus récemment publiée** ; vous ne pouvez pas verrouiller une version historique pour la relecture.

## Dépannage {#troubleshooting}

Si vous rencontrez des problèmes lors de l’utilisation de fragments de contenu Adobe Experience Manager dans Journey Optimizer, reportez-vous aux problèmes et résolutions courants suivants :

| Problème | Cause | Résolution |
|-|-|-|
| **Balise introuvable** ou **fragment de contenu non visible dans le sélecteur** | La syntaxe de la balise Adobe Experience Manager ne correspond pas au format requis `ajo-enabled:{OrgId}/{SandboxName}` | Vérifiez que l’ID de balise utilise l’**ID d’organisation** et le **Nom du sandbox** corrects. Vérifiez qu’il n’y a pas d’espaces ou de séparateurs incorrects. Republiez le fragment de contenu après avoir corrigé la balise . |
| **Le fragment de contenu n’apparaît pas dans la liste** | Le fragment de contenu est à l’état de brouillon ou n’est pas publié | Seuls les fragments de contenu approuvés et publiés s’affichent dans le sélecteur Journey Optimizer. Publiez le fragment de contenu dans Adobe Experience Manager et assurez-vous qu’il possède le statut publié . |
| **Erreur de variable non définie** | espace réservé Personalization non déclaré dans la balise d’assistance de fragment | Ajoutez tous les paramètres requis dans la balise d’assistance de fragment. Chaque espace réservé utilisé dans le fragment de contenu doit être explicitement déclaré avec son mappage. |
| **L’épreuve affiche un contenu inattendu** | Proof utilise la dernière version publiée de Adobe Experience Manager | Les BAT reflètent toujours la publication la plus récente du fragment de contenu dans Adobe Experience Manager. Si vous avez récemment apporté des modifications à Adobe Experience Manager, republiez le fragment et actualisez l’épreuve. |
| **Erreur de refus d’accès (CPES)** | Rôle utilisateur non autorisé à accéder à certains attributs | Contactez votre administrateur système pour vérifier que votre rôle dispose des autorisations appropriées pour le profil ou les attributs contextuels utilisés dans la personnalisation. |
| **Le fragment affiche du contenu vide ou manquant** | Paramètres de personnalisation requis manquants ou valeurs de secours | Assurez-vous que tous les paramètres requis sont fournis et envisagez d’ajouter des valeurs de secours pour les attributs facultatifs. |
| **L’image n’est pas rendue ou semble endommagée** | L’URL de l’image dans le fragment de contenu est un chemin relatif ou inaccessible à partir du canal | Utilisez des URL **absolues** (`https://...`) pour les champs d’image. Les chemins relatifs depuis Adobe Experience Manager ne sont pas pris en charge. Confirmez l’URL dans un navigateur ou un aperçu de message. |
| **Le lien Experience League AEM renvoie 404** | Signet obsolète, aperçu de la version ou page d’aide d’AEM dépubliée | Ouvrez la rubrique [Fragments de contenu avec Adobe Journey Optimizer](https://experienceleague.adobe.com/fr/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} de la documentation Experience Manager active et accédez à la table des matières de la page, ou recherchez le nom de la section (par exemple, **Configuration Dispatcher**). |

Si le problème persiste, contactez votre représentant Adobe avec des détails sur votre identifiant de fragment de contenu, votre identifiant de campagne ou de parcours, ainsi que tout message d’erreur affiché.
