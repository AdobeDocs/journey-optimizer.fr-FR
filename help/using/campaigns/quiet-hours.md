---
solution: Journey Optimizer
product: journey optimizer
title: Heures calmes
description: Découvrez comment empêcher l’envoi de communications pendant des périodes spécifiques à l’aide de règles d’heures creuses
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: heures creuses, exclusions de temps, règles métier, ensembles de règles, planning, campagnes
exl-id: [TO BE GENERATED]
hide: yes
hidefromtoc: yes
source-git-commit: 11bccd63afa1bf5aafcd1dff70c8193ea754d256
workflow-type: tm+mt
source-wordcount: 980
ht-degree: 9%

---

# Heures calmes {#quiet-hours}

>[!AVAILABILITY]
>
>Les règles d’heures creuses ne sont actuellement disponibles que pour un ensemble d’organisations (disponibilité limitée). Pour être ajouté à la liste d’attente, contactez votre représentant ou représentante Adobe.

Les heures creuses vous permettent de définir des exclusions basées sur l’heure pour les canaux E-mail, SMS, Notification push et WhatsApp. EIles garantissent qu’aucun message n’est envoyé pendant des périodes spécifiques, ce qui vous aide à respecter les préférences de la clientèle et les exigences de conformité.

Vous pouvez appliquer des heures creuses par le biais de jeux de règles, qui peuvent être affectés à des actions individuelles dans des campagnes ou des parcours pour un contrôle précis.

## Pourquoi utiliser Quiet Hours ? {#why-quiet-hours}

Les heures calmes vous permettent d’améliorer l’expérience client et de maintenir la conformité de plusieurs manières :

* **Respectez les préférences des clients** : évitez d’envoyer des messages à des heures inopportunes (par exemple, tard le soir ou tôt le matin), ce qui peut avoir un impact négatif sur la réputation de la marque et la fidélisation de la clientèle.

* **Améliorer l’engagement** : en envoyant des messages lorsque les clients sont plus susceptibles de les voir et d’agir dessus, vous augmentez l’efficacité de vos communications.

* **Conformité juridique** : certains États et certaines régions interdisent les messages marketing SMS à des heures spécifiques. Les heures calmes vous aident à respecter les réglementations telles que la TCPA et les lois spécifiques aux SMS.

* **Optimiser le minutage** : si un délai trop long s’est écoulé depuis qu’un message a été planifié, il se peut qu’il ne soit plus pertinent. Les heures calmes vous permettent de supprimer des messages obsolètes ou de les conserver jusqu’à un moment approprié.

## Fonctionnement des heures calmes {#how-quiet-hours-work}

Les heures calmes sont implémentées par le biais de règles métier que vous créez et appliquez à vos campagnes et parcours à l’aide d’ensembles de règles.

Lorsqu’un message est planifié pour être envoyé pendant une période calme, [!DNL Adobe Journey Optimizer] prend l’une des deux actions suivantes en fonction de votre configuration :

* **Ignorer** : le message est définitivement supprimé et n’est jamais envoyé.
* **File d’attente** : le message est conservé et envoyé automatiquement dès que la période de temps calme se termine.

Le système évalue les heures creuses en fonction du fuseau horaire du destinataire, qui peut être :

* Fuseau horaire spécifié dans le profil du client
* Fuseau horaire déduit en fonction d’autres données de profil et d’événement
* Fuseau horaire fixe que vous spécifiez dans la règle

>[!NOTE]
>
>Fenêtre de pré-suppression : le système commence à supprimer les communications 30 minutes avant le début des heures calmes, en s’assurant qu’aucun message n’est diffusé une fois que la période calme commence.

## Créer une règle d&#39;heures silencieuses {#create-quiet-hours-rule}

Pour créer une règle d’heures creuses :

1. Accédez à **[!UICONTROL Administration]** > **[!UICONTROL Règles métier]**.

1. Dans la section **[!UICONTROL Ensembles de règles]**, créez un ensemble de règles ou sélectionnez-en un existant auquel vous souhaitez ajouter la règle d’heures creuses.

1. Cliquez sur **[!UICONTROL Créer une règle]** et sélectionnez **[!UICONTROL Heures creuses]** comme type de règle.

1. Configurez les paramètres des heures creuses :

   * **Nom de la règle** : attribuez un nom explicite à votre règle.

   * **Période** : définissez à quel moment les heures calmes doivent s’appliquer :
      * **Heures de la journée** : définissez des heures spécifiques (par exemple, de 20 :00 à 8 :00).
      * **Jours de la semaine** : sélectionnez des jours spécifiques (par exemple, les week-ends).
      * **Dates personnalisées** : choisissez des dates calendaires spécifiques (par exemple, des jours fériés).

   * **Fuseau horaire** : sélectionnez le mode de détermination du fuseau horaire :
      * **Fuseau horaire local de l’utilisateur** : utilisez le fuseau horaire du profil de chaque destinataire
      * **Fuseau horaire spécifique** : appliquez un fuseau horaire fixe (par exemple, Est, Centre).

   * **Action** : choisissez ce qu&#39;il advient des messages pendant les heures calmes :
      * **Ignorer** : les messages sont définitivement supprimés
      * **File d’attente** : les messages sont conservés et envoyés lorsque les heures calmes se terminent

1. Cliquez sur **[!UICONTROL Enregistrer]** pour créer la règle.

## Appliquer des heures creuses aux campagnes et aux parcours {#apply-quiet-hours}

Une fois que vous avez créé une règle d’heures creuses, vous devez l’appliquer à vos campagnes ou parcours :

1. Ouvrez la campagne ou le parcours où vous souhaitez appliquer des heures calmes.

1. Accédez à l’action (E-mail, SMS, Push ou WhatsApp) que vous souhaitez contrôler.

1. Dans la configuration de l’action, recherchez la section **[!UICONTROL Jeu de règles]**.

1. Sélectionnez l’ensemble de règles contenant votre règle d’heures creuses.

1. Enregistrez vos modifications.

La règle des heures calmes s’applique désormais à cette action spécifique. Tous les messages envoyés par le biais de cette action respecteront la configuration des heures calmes.

>[!NOTE]
>
>Les règles d’heures creuses s’appliquent aux communications planifiées et déclenchées par un événement. Assurez-vous que votre jeu de règles est correctement configuré pour gérer votre cas d’utilisation.

## Considérations relatives aux fuseaux horaires {#timezone-considerations}

Lors de l’utilisation de l’option **Fuseau horaire local de l’utilisateur**, [!DNL Adobe Journey Optimizer] recherche les informations de fuseau horaire dans l’ordre suivant :

1. **Attribut de fuseau horaire du profil** : fuseau horaire explicitement spécifié dans le profil du client
2. **Fuseau horaire déduit** : fuseau horaire calculé en fonction d’autres données de profil et signaux comportementaux

Si aucun de ces éléments n’est disponible, le système risque de ne pas appliquer correctement les heures calmes. Veillez à ce que vos profils client incluent des informations de fuseau horaire pour des résultats optimaux.

Lors de l’utilisation d’un **fuseau horaire spécifique**, tous les destinataires reçoivent (ou ne reçoivent pas) des messages en fonction de ce fuseau horaire unique, quel que soit leur emplacement réel.

## Mécanismes de sécurisation et limitations {#guardrails-limitations}

Tenez compte des points suivants lorsque vous utilisez des heures calmes :

* **Durée d’activation** : l’activation complète d’une règle ou d’un jeu de règles peut prendre jusqu’à 20 minutes. Planifiez en conséquence lors de la création ou de la modification de règles.

* **Délai d’activation de la campagne** : après avoir associé les règles métier, attendez au moins 10 minutes avant d’activer un parcours ou d’envoyer une campagne pour vous assurer que les règles sont correctement appliquées.

* **Limites des ensembles de règles** : actuellement, vous pouvez avoir jusqu’à 3 ensembles de règles actifs pour le domaine du canal et 5 pour le domaine du parcours.

* **Taux de publication des messages** : lorsque des heures calmes se terminent et que des messages placés dans la file d’attente sont publiés, ils sont envoyés à un taux allant jusqu’à 5 000 messages par seconde par organisation.

* **Non pris en charge dans** : les règles relatives aux heures creuses ne sont actuellement pas disponibles pour l’orchestration des campagnes.

* **Exécution d’essai** : les règles d’heures calmes ne sont pas évaluées lors des exécutions d’exécution d’essai en parcours.

## Création de rapports {#reporting}

Vous pouvez suivre l’impact des heures creuses sur vos campagnes et parcours grâce aux fonctionnalités de création de rapports standard :

* **Rapport à tout moment** : la section « Causes d’exclusion » indique le volume de clients qui n’ont pas reçu de communications en raison de règles relatives aux heures creuses, ainsi que le nom de l’ensemble de règles spécifique.

* **Rapport dynamique** : (le cas échéant) affiche des statistiques en temps réel sur les profils qui attendent actuellement en raison d’heures calmes ou qui ont été ignorés en raison d’heures calmes.

## Étapes suivantes {#next-steps}

Une fois vos règles d’heures creuses configurées et appliquées, vous pouvez :

* Vérifiez votre campagne ou votre parcours pour vous assurer que les règles sont correctement associées
* Activer votre campagne ou votre parcours
* Surveillez l’impact des heures creuses dans vos rapports

