---
title: Alertes dans les messages
description: Découvrez comment vérifier la validation du contenu des messages et résoudre les problèmes.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 89f445f2-df8a-4d2d-afe8-4f8b9cb001d9
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 100%

---

# Alertes sur vos messages {#publish-manage-messages}

## Vérifications avant publication {#message-alerting}

Lorsque vous créez votre message, des alertes vous avertissent si vous devez effectuer des opérations importantes avant de le publier.

Les alertes s’affichent en haut à droite de l’écran, comme illustré ci-dessous :

![](assets/message-alerts.png)

>[!NOTE]
>
>Si ce bouton ne s’affiche pas, aucune alerte n’a été détectée.

Deux types d’alertes peuvent avoir lieu :

* Les **avertissements** se rapportent aux recommandations et aux bonnes pratiques. Par exemple, un message s’affiche si le lien de d’opt-out est manquant.

* Les **erreurs** vous empêchent de publier le message tant qu’elles ne sont pas corrigées. Par exemple, un message vous avertit que l’objet est manquant.

Tous les avertissements et erreurs possibles sont détaillés [ci-dessous](#alerts-and-warnings).

>[!CAUTION]
>
> Vous devez résoudre toutes les alertes d’**erreur** avant de procéder à la publication.

## Liste des avertissements et des erreurs {#alerts-and-warnings}

Les paramètres et les éléments vérifiés par le système sont répertoriés ci-dessous. Vous trouverez également des informations sur la façon d’adapter votre configuration pour résoudre les problèmes correspondants.

**Avertissements** :

* **[!UICONTROL Lien d’opt-out ne figurant pas dans le corps de l’email]** : il est recommandé d’ajouter un lien d’opt-out dans le corps de votre email. Découvrez comment configurer ce lien dans [cette section](consent.md).

* **[!UICONTROL Version texte du contenu HTML vide]** : n’oubliez pas de définir une version texte du corps de votre email, car elle sera utilisée lorsque le contenu HTML ne peut pas être affiché. Découvrez comment créer cette version texte dans [cette section](create-email-content.md#generate-text-version).

* **[!UICONTROL Lien vide figurant dans le corps de l’email]** : vérifiez que tous les liens de votre email sont corrects. Découvrez comment gérer le contenu et les liens dans [cette section](create-email-content.md).

* **[!UICONTROL La taille de l’email dépasse la limite de 100 Ko]** : pour une diffusion optimale, veillez à ce que la taille de votre email ne dépasse pas 100 Ko. Découvrez comment modifier le contenu des emails dans [cette section](create-email-content.md).

**Erreurs** :

* **[!UICONTROL Ligne d’objet absente]** : la ligne d’objet d’email est obligatoire. Découvrez comment définir et personnaliser cette ligne dans [cette section](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

* **[!UICONTROL Variante push vide]** : cette erreur s’affiche lorsque le titre ou le corps de la notification push est manquant. Découvrez comment définir le contenu des notifications push dans [cette section](create-push.md).

* **[!UICONTROL Variante d’email vide]** : cette erreur s’affiche si le contenu de l’email n’est pas configuré. Découvrez comment concevoir le contenu des emails dans [cette section](design-emails.md).

* **[!UICONTROL Préréglage absent]** : vous ne pouvez pas publier votre message si le préréglage que vous avez sélectionné est supprimé après la création du message. Si cette erreur se produit, sélectionnez un autre préréglage dans les **[!UICONTROL Propriétés]** du message. Pour en savoir plus sur le branding, consultez [cette section](configuration/about-subdomain-delegation.md).

* **[!UICONTROL La payload iOS/Android push dépasse la limite de 4 Ko]** : la taille de la notification push ne peut pas dépasser 4 Ko. Pour respecter cette limite, essayez de réduire l’utilisation des images ou des émoticônes. Découvrez comment gérer le contenu de vos notifications push dans [cette section](create-push.md).

>[!CAUTION]
>
> Pour pouvoir publier votre message, vous devez résoudre toutes les alertes d’**erreur**.

<!--Other issues can stop publication such as:
* The push notification title is empty-->
