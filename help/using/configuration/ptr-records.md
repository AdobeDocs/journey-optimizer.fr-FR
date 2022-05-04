---
title: Enregistrements PTR
description: Découvrez comment gérer les enregistrements PTR
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: 5596c851b70cc38cd117793d492a15fd4ce175ef
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 90%

---

# Enregistrements PTR {#ptr-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record"
>title="Enregistrements PTR des sous-domaines"
>abstract="Un enregistrement pointeur (PTR) est un type d’enregistrement DNS qui fournit le nom de domaine associé à une adresse IP, ce qui permet aux serveurs de messagerie de réception de vérifier les adresses IP des expéditeurs."

## À propos des enregistrements PTR {#about-ptr-records}

Un enregistrement pointeur (PTR) est un type d&#39;enregistrement DNS (Domain Name System) qui fournit le nom de domaine associé à une adresse IP.

Avec les enregistrements PTR, les serveurs de messagerie de réception peuvent vérifier l’authenticité des serveurs de messagerie d’envoi en identifiant si leurs adresses IP correspondent aux noms avec lesquels les serveurs se connectent.

## Accès aux enregistrements PTR de vos sous-domaines {#access-ptr-records}

Une fois [quʼun sous-domaine est délégué ](delegate-subdomain.md)dans Adobe Journey Optimizer, un enregistrement PTR est automatiquement créé et associé à ce sous-domaine. Vous pouvez y accéder à partir du menu **[!UICONTROL Canaux]**/**[!UICONTROL Configuration de l’e-mail]**/**[!UICONTROL Enregistrements PTR]**. 

![](assets/ptr-records.png)

La liste affiche les enregistrements PTR générés pour chaque sous-domaine délégué, en utilisant la syntaxe ci-dessous :

* &quot;r&quot; pour l&#39;enregistrement,
* &quot;xx&quot; pour les deux derniers chiffres de l&#39;adresse IP,
* nom du sous-domaine.

Vous pouvez ouvrir un enregistrement PTR de la liste pour afficher le nom de sous-domaine et l&#39;adresse IP associés.

## Modifier un enregistrement PTR {#edit-ptr-record}

Vous pouvez modifier un enregistrement PTR pour modifier le sous-domaine associé à une adresse IP. 

>[!CAUTION]
>
>Procédez avec une attention particulière lors de la modification des enregistrements PTR. En cas de doute, contactez un expert en délivrabilité.<!--why?-->

>[!NOTE]
>
>Vous ne pouvez pas modifier les champs **[!UICONTROL IP]** et **[!UICONTROL Enregistrement PTR]**.

### Sous-domaines entièrement délégués {#fully-delegated-subdomains}

Pour modifier un enregistrement PTR avec un sous-domaine qui est [entièrement délégué](delegate-subdomain.md#full-subdomain-delegation) à Adobe, procédez comme suit.

1. Dans la liste, cliquez sur un nom d’enregistrement PTR pour l’ouvrir.

   ![](assets/ptr-record-select.png)

1. Sélectionnez un sous-domaine [entièrement délégué](delegate-subdomain.md#full-subdomain-delegation) à Adobe dans la liste.

   ![](assets/ptr-record-subdomain.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer vos modifications.

### Sous-domaines délégués à l’aide de la méthode CNAME {#edit-ptr-subdomains-cname}

Pour modifier un enregistrement PTR avec un sous-domaine délégué à Adobe à l’aide de la [méthode CNAME](delegate-subdomain.md#cname-subdomain-delegation), procédez comme suit.

1. Dans la liste, cliquez sur un nom d’enregistrement PTR pour l’ouvrir.

   ![](assets/ptr-record-select-cname.png)

1. Sélectionnez dans la liste un sous-domaine délégué à Adobe à l’aide de la [méthode CNAME](delegate-subdomain.md#cname-subdomain-delegation).

   ![](assets/ptr-record-subdomain-cname.png)

1. Vous devez créer un nouvel enregistrement DNS direct sur votre plateforme d’hébergement. Pour ce faire, copiez lʼenregistrement généré par Adobe. Une fois lʼopération terminée, cochez la case « Je confirme… ».

   ![](assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >Si vous recevez le message « Veuillez d’abord créer un DNS direct, puis réessayer », procédez comme suit :
   >   * Vérifiez auprès du fournisseur DNS si l’enregistrement DNS direct a bien été créé.
   >   * Les enregistrements sur les serveurs DNS peuvent ne pas se synchroniser immédiatement. Patientez quelques minutes, puis réessayez.


1. Cliquez sur **[!UICONTROL Enregistrer]** pour confirmer vos modifications.

## Vérification des détails de la mise à jour de l’enregistrement PTR {#check-ptr-record-update}

Une fois que vous avez confirmé la modification de l’enregistrement PTR, la variable **[!UICONTROL Traitement]** s’affiche en regard du nom de l’enregistrement PTR dans la liste.

![](assets/ptr-record-updating.png)

>[!NOTE]
>
>Le [traitement des mises à jour](#processing) peut prendre jusqu’à quelques heures.

Pour vérifier les détails de la mise à jour de l’enregistrement PTR, cliquez sur l’icône en regard de celui-ci. En savoir plus sur les statuts associés aux différentes icônes dans [cette section](#ptr-record-update-statuses).

![](assets/ptr-record-recent-update.png)

Vous pouvez voir des informations telles que l’état de mise à jour et les modifications demandées. 

![](assets/ptr-record-updates.png)

## États de mise à jour des enregistrements PTR {#ptr-record-update-statuses}

Une mise à jour d’enregistrement PTR peut afficher les états suivants :

* ![](assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL En cours de traitement]** : la mise à jour de l’enregistrement PTR a été envoyée et fait l’objet d’un processus de vérification.
* ![](assets/do-not-localize/ptr-record-success.png) **[!UICONTROL Réussite]** : l’enregistrement PTR mis à jour a été vérifié et le nouveau sous-domaine est désormais associé à l’adresse IP.
* ![](assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL Échec]** : une ou plusieurs vérifications ont échoué lors de la vérification de la mise à jour de l’enregistrement PTR.

### En cours de traitement {#processing}

Plusieurs contrôles de délivrabilité seront effectués pour vérifier la validité du nouveau sous-domaine à associer à l’adresse IP. Cela peut prendre jusqu’à quelques heures.

>[!NOTE]
>
>Vous ne pouvez pas modifier un enregistrement PTR pendant que la mise à jour est en cours. Vous pouvez toujours cliquer sur son nom, mais le champ **[!UICONTROL Sous-domaine]** est grisé. Les modifications ne seront pas répercutées tant que la mise à jour n’aura pas réussi. 

Pendant le processus de validation, l’ancien sous-domaine est toujours associé à l’adresse IP. 

### Réussite {#success}

Une fois le processus de validation réussi, le nouveau sous-domaine est automatiquement associé à l’adresse IP. 

### Échec {#failes}

Si le processus de validation échoue, l’ancien enregistrement PTR s’affiche. Le sous-domaine valide précédemment associé à l’adresse IP reste inchangé. 

Les types d’erreur de mise à jour possibles sont les suivants :
* Échec de la création d’un nouveau DNS direct pour l’enregistrement PTR
* Échec de la mise à jour de l’enregistrement
* Échec de la réintégration des affinités

En cas d’échec de la mise à jour, l’enregistrement PTR est à nouveau modifiable. Vous pouvez cliquer sur son nom et mettre à nouveau à jour le sous-domaine. 
