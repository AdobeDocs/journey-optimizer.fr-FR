---
solution: Journey Optimizer
product: journey optimizer
title: Bonnes pratiques relatives aux SMS pour l’optimisation des coûts
description: Découvrez comment optimiser les coûts des messages SMS en gérant les limites de caractères, le codage et la personnalisation dans Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Intermediate
source-git-commit: 13b3c8aa7fce85029167ef31feb7272e4877b7b0
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Bonnes pratiques pour l’optimisation des coûts des SMS {#sms-cost-optimization}

Les SMS sont généralement facturés par les fournisseurs en fonction d’une limite de 160 caractères par message. L&#39;envoi de SMS peut entraîner des coûts supplémentaires si les messages sont divisés en plusieurs parties.

Suivez ces instructions pour optimiser votre stratégie de messagerie et réduire les dépenses.

## Conserver les messages courts {#keep-messages-short}

Journey Optimizer autorise jusqu’à 1 500 caractères dans le corps d’un SMS. Un avertissement s’affiche lorsque vous dépassez cette limite et les messages au-delà de ce seuil déclenchent une erreur.

La plupart des fournisseurs de SMS prennent en charge le codage GSM 7 bits, où un seul SMS peut contenir jusqu’à 160 caractères. Les messages dépassant cette longueur sont automatiquement partagés en plusieurs parties SMS (concaténation) :

* **Moins de 160 caractères** : 1 partie SMS
* **161-306 caractères** : 2 parties SMS
* **307-459 caractères** : 3 parties SMS

**Pour minimiser les coûts** visez à conserver les messages de moins de 160 caractères afin qu’ils soient facturés en tant que partie unique du SMS.

Par exemple, un message de 1 600 caractères peut consommer 10 crédits SMS, même s’il apparaît comme un message unique dans Journey Optimizer.

## Évitez les caractères spéciaux qui augmentent la longueur {#avoid-special-characters}

Certains caractères, tels que `| ^ € { } [ ] ~ \`, sont comptés comme deux caractères dans le codage GSM. L’inclusion de ces caractères peut entraîner un dépassement plus rapide de la limite de 160 caractères **votre message**.

## Empêcher le codage UCS-2 {#prevent-ucs2-encoding}

Si le message contient des caractères non GSM, tels que du texte en chinois ou en arabe, des symboles de marque ou des retours en dur d’outils de formatage riches, le message sera codé par le fournisseur à l’aide d’UCS-2, qui ne prend en charge que 70 caractères par SMS.

L’utilisation de l’encodage UCS-2 peut augmenter le nombre de caractères et, par conséquent, affecter la facturation des messages avec votre fournisseur de services.

Par exemple, un message Unicode de 200 caractères sera diffusé en 3 parties SMS.

## Bonnes pratiques de création {#authoring-best-practices}

Composez le SMS final directement dans Journey Optimizer ou collez-le à partir d’applications en texte brut.

Évitez d’utiliser des applications de texte enrichi, car elles peuvent introduire des caractères masqués ou des sauts de ligne qui déclenchent le codage UCS-2, ce qui peut augmenter à la fois le nombre de parties SMS et les coûts associés.

## Vérifier le nombre de caractères avant l’envoi {#check-character-count}

Utilisez des applications en texte brut ou le menu Journey Optimizer **[!UICONTROL Simuler du contenu]** pour vérifier le nombre de caractères.

Lorsque Journey Optimizer affiche le nombre de caractères, espaces compris, lors de la simulation du contenu, notez les points suivants :

* Il n’inclut **&#x200B;**&#x200B;les caractères générés par la personnalisation dynamique ou certains caractères spéciaux.

* Le comptage **x/1500** sert d’indicateur visuel de la limite technique de la charge utile, et non de la limite par message, par exemple la limite de 7 bits du GSM à 160 caractères.

* Adobe prend en charge le codage UTF-8 dans l’éditeur, qui diffère du codage GSM-7 bits.

## Comprendre le reporting {#understanding-reporting}

Le compte rendu des performances de **Journey Optimizer** compte l&#39;ensemble du message comme un envoi, indépendamment des parties SMS.

Le **rapport du fournisseur** reflète le nombre réel de parties de message SMS utilisées pour la diffusion et doit être référencé pour confirmer la facturation et tout dépassement potentiel. Si Adobe est votre fournisseur de SMS via Sinch, vous recevrez ce rapport de facturation séparément tous les mois.

## Considérations relatives à Personalization {#personalization-considerations}

La personnalisation dynamique peut augmenter la longueur d’un message. Par exemple, le fait de remplacer une variable par un prénom long peut ajouter des caractères supplémentaires.

## Ressources supplémentaires {#additional-resources}

Consultez les caractères pris en charge et les règles de codage dans [Sinch Character Support Guide](https://developers.sinch.com/docs/sms/resources/message-info/character-support/)

