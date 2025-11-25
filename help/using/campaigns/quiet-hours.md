---
solution: Journey Optimizer
product: journey optimizer
title: Heures creuses
description: Découvrez comment empêcher l’envoi de communications pendant des périodes spécifiques à l’aide de règles d’heures creuses.
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: heures creuses, exclusions d’horaires, règles métier, ensembles de règles, planning, campagnes
hide: true
hidefromtoc: true
source-git-commit: e5243565241551fab98a79fa118618535ce58de8
workflow-type: ht
source-wordcount: '980'
ht-degree: 100%

---

# Heures creuses {#quiet-hours}

>[!AVAILABILITY]
>
>Les règles d’heures creuses ne sont actuellement disponibles que pour un ensemble d’organisations (disponibilité limitée). Pour un ajout à la liste d’attente, contactez votre représentant ou représentante Adobe.

Les heures creuses vous permettent de définir des exclusions basées sur l’heure pour les canaux E-mail, SMS, Notification push et WhatsApp. EIles garantissent qu’aucun message n’est envoyé pendant des périodes spécifiques, ce qui vous aide à respecter les préférences de la clientèle et les exigences de conformité.

Vous pouvez appliquer des heures creuses par le biais de jeux de règles, qui peuvent être affectés à des actions individuelles dans des campagnes ou des parcours pour un contrôle précis.

## Pourquoi utiliser les heures creuses ? {#why-quiet-hours}

Les heures creuses vous permettent d’améliorer l’expérience de la clientèle et d’assurer la conformité de plusieurs manières :

* **Respectez les préférences des clientes et clients** : évitez d’envoyer des messages à des heures inopportunes (par exemple, tard le soir ou tôt le matin), ce qui peut avoir un impact négatif sur la réputation de la marque et la fidélisation de la clientèle.

* **Améliorez l’engagement** : en envoyant des messages lorsque les personnes sont plus susceptibles de les voir et d’y réagir, vous augmentez l’efficacité de vos communications.

* **Conformité juridique** : certains États et certaines régions interdisent les messages marketing par SMS à des heures spécifiques. Les heures creuses vous aident à respecter les réglementations telles que la TCPA et les lois spécifiques aux SMS.

* **Optimisez le timing** : si un délai trop long s’est écoulé depuis la planification d’un message, il se peut qu’il ne soit plus pertinent. Les heures creuses vous permettent de supprimer des messages obsolètes ou de les conserver jusqu’à un moment approprié.

## Fonctionnement des heures creuses {#how-quiet-hours-work}

Les heures creuses sont mises en œuvre par le biais de règles métier que vous créez et appliquez à vos campagnes et parcours à l’aide d’ensembles de règles.

Lorsqu’un message est planifié pour être envoyé pendant la période d’heures creuses, [!DNL Adobe Journey Optimizer] prend l’une des deux mesures suivantes en fonction de votre configuration :

* **Suppression** : le message est définitivement supprimé et n’est jamais envoyé.
* **File d’attente** : le message est conservé et envoyé automatiquement dès que la période d’heures creuses se termine.

Le système évalue les heures creuses en fonction du fuseau horaire des destinataires, qui peut être :

* Fuseau horaire spécifié dans le profil du client ou de la cliente
* Fuseau horaire déduit en fonction d’autres données de profil et d’événement
* Fuseau horaire fixe que vous spécifiez dans la règle

>[!NOTE]
>
>Fenêtre de pré-suppression : le système commence à supprimer les communications 30 minutes avant le début des heures creuses, en s’assurant qu’aucun message n’est diffusé une fois que la période d’heures creuses commence.

## Créer une règle d’heures creuses {#create-quiet-hours-rule}

Pour créer une règle d’heures creuses :

1. Accédez à **[!UICONTROL Administration]** > **[!UICONTROL Règles métier]**.

1. Dans la section **[!UICONTROL Ensembles de règles]**, créez un ensemble de règles ou sélectionnez-en un existant auquel vous souhaitez ajouter la règle d’heures creuses.

1. Cliquez sur **[!UICONTROL Créer une règle]** et sélectionnez **[!UICONTROL Heures creuses]** comme type de règle.

1. Configurez les paramètres des heures creuses :

   * **Nom de la règle** : attribuez un nom explicite à votre règle.

   * **Période** : définissez à quel moment les heures creuses doivent s’appliquer :
      * **Heures de la journée** : définissez des heures spécifiques (par exemple, de 20 h:00 à 8 h:00).
      * **Jours de la semaine** : sélectionnez des jours spécifiques (par exemple, les week-ends).
      * **Dates personnalisées** : choisissez des dates calendaires spécifiques (par exemple, des jours fériés).

   * **Fuseau horaire** : sélectionnez le mode de détermination du fuseau horaire :
      * **Fuseau horaire local de l’utilisateur ou de l’utilisatrice** : utilisez le fuseau horaire du profil de chaque destinataire
      * **Fuseau horaire spécifique** : appliquez un fuseau horaire fixe (par exemple, Est, Centre).

   * **Action** : choisissez ce qu’il advient des messages pendant les heures creuses :
      * **Suppression** : les messages sont définitivement supprimés.
      * **File d’attente** : les messages sont conservés et envoyés à la fin des heures creuses.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour créer la règle.

## Appliquer des heures creuses aux campagnes et aux parcours {#apply-quiet-hours}

Une fois que vous avez créé une règle d’heures creuses, vous devez l’appliquer à vos campagnes ou parcours :

1. Ouvrez la campagne ou le parcours où vous souhaitez appliquer des heures creuses.

1. Accédez à l’action (e-mail, SMS, notification push ou WhatsApp) que vous souhaitez contrôler.

1. Dans la configuration de l’action, recherchez la section **[!UICONTROL Jeu de règles]**.

1. Sélectionnez le jeu de règles contenant votre règle d’heures creuses.

1. Enregistrez vos modifications.

La règle des heures creuses s’applique désormais à cette action spécifique. Tous les messages envoyés par le biais de cette action respecteront la configuration des heures creuses.

>[!NOTE]
>
>Les règles d’heures creuses s’appliquent aux communications planifiées et déclenchées par un événement. Assurez-vous que votre jeu de règles est correctement configuré pour gérer votre cas d’utilisation.

## Considérations relatives aux fuseaux horaires {#timezone-considerations}

Lors de l’utilisation de l’option **Fuseau horaire local de l’utilisateur ou de l’utilisatrice**, [!DNL Adobe Journey Optimizer] recherche les informations de fuseau horaire dans l’ordre suivant :

1. **Attribut de fuseau horaire du profil** : fuseau horaire explicitement spécifié dans le profil du client ou de la cliente
2. **Fuseau horaire déduit** : fuseau horaire calculé en fonction d’autres données de profil et de signaux comportementaux

Si aucun de ces éléments n’est disponible, le système risque de ne pas appliquer correctement les heures creuses. Veillez à ce que les profils de vos clientes et clients incluent des informations de fuseau horaire pour des résultats optimaux.

Lors de l’utilisation d’un **fuseau horaire spécifique**, les destinataires reçoivent (ou ne reçoivent pas) de messages en fonction de ce fuseau horaire unique, quel que soit leur emplacement réel.

## Mécanismes de sécurisation et limitations {#guardrails-limitations}

Tenez compte des points suivants lorsque vous utilisez des heures creuses :

* **Délai d’activation** : l’activation complète d’un jeu de règles peut prendre jusqu’à 20 minutes. Planifiez en conséquence lors de la création ou de la modification de règles.

* **Délai d’activation de la campagne** : après avoir associé les règles métier, attendez au moins 10 minutes avant d’activer un parcours ou d’envoyer une campagne pour vous assurer que les règles sont correctement appliquées.

* **Limites des jeux de règles** : actuellement, vous pouvez avoir jusqu’à 3 jeux de règles actifs pour le domaine du canal et 5 pour le domaine du parcours.

* **Taux de publication des messages** : lorsque des heures creuses se terminent et que les messages placés dans la file d’attente sont publiés, ils sont envoyés à un taux allant jusqu’à 5 000 messages par seconde par organisation.

* **Incompatibilité** : les règles relatives aux heures creuses ne sont actuellement pas disponibles pour l’orchestration de campagne.

* **Test à blanc** : les règles d’heures creuses ne sont pas évaluées lors des exécutions de test à blanc des parcours.

## Création de rapports {#reporting}

Vous pouvez suivre l’impact des heures creuses sur vos campagnes et parcours grâce aux fonctionnalités de création de rapports standard :

* **Rapport complet** : la section « Causes d’exclusion » indique le nombre de clientes et clients qui n’ont pas reçu de communications en raison de règles relatives aux heures creuses, ainsi que le nom du jeu de règles spécifique.

* **Rapport dynamique** : (le cas échéant) affiche des statistiques en temps réel sur les profils actuellement en attente en raison d’heures creuses ou qui ont été ignorés en raison d’heures creuses.

## Étapes suivantes {#next-steps}

Une fois vos règles d’heures creuses configurées et appliquées, vous pouvez :

* vérifier votre campagne ou votre parcours pour vous assurer que les règles sont correctement associées ;
* activer votre campagne ou parcours ;
* surveiller l’impact des heures creuses dans vos rapports.

