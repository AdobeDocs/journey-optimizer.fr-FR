---
solution: Journey Optimizer
product: journey optimizer
title: Bonnes pratiques relatives aux SMS pour l’optimisation des coûts
description: Découvrez comment optimiser les coûts des SMS en maîtrisant les limites de caractères, le codage et la personnalisation dans Journey Optimizer.
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: c8c156da-8482-4932-9c15-45ab83c173e7
TQID: https://experienceleague.adobe.com/ccUbyMiVNBULBlaYAb-z6-WFGcWURtmelyKUy7v2g2o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a4c92daab69394e6a736517f2e23a941135f7eb4
workflow-type: tm+mt
source-wordcount: 544
ht-degree: 100%

---

# Bonnes pratiques pour l’optimisation des coûts des SMS {#sms-cost-optimization}

Les SMS sont généralement facturés par les fournisseurs sur la base d’une limite de 160 caractères par message. L’envoi de SMS peut générer des coûts supplémentaires si les messages sont divisés en plusieurs parties.

Suivez ces instructions pour optimiser votre stratégie d’envoi de messages et réduire les dépenses.

## Rester concis {#keep-messages-short}

Journey Optimizer autorise jusqu’à 1 500 caractères dans le corps d’un SMS. Un avertissement s’affiche lorsque vous dépassez cette limite et les messages au-delà de ce seuil déclenchent une erreur.

La plupart des fournisseurs de SMS prennent en charge le codage GSM 7 bits, qui permet à un SMS de contenir jusqu’à 160 caractères. Les messages qui dépassent cette longueur sont automatiquement partagés en plusieurs parties de SMS (concaténation) :

* **Moins de 160 caractères** : 1 partie de SMS
* **Entre 161 et 306 caractères** : 2 parties de SMS
* **Entre 307 et 459 caractères** : 3 parties de SMS

**Pour réduire les coûts** rédigez des messages contenant moins de 160 caractères afin qu’ils soient facturés comme une seule partie de SMS.

Par exemple, un message de 1 600 caractères consomme 10 crédits SMS, même s’il apparaît comme un message unique dans Journey Optimizer.

## Éviter les caractères spéciaux qui augmentent la longueur {#avoid-special-characters}

Certains caractères, tels que `| ^ &euro; { } [ ] ~ \`, comptent pour deux caractères dans le codage GSM. En utilisant ces caractères dans votre message, vous risquez de dépasser plus rapidement la **limite de 160 caractères**.

## Éviter le codage UCS-2 {#prevent-ucs2-encoding}

Si le message contient des caractères non GSM, tels que du texte en chinois ou en arabe, des symboles de marque déposée ou des retours à la ligne causés par des outils de mise en forme avancée, le message sera codé par le fournisseur à l’aide d’UCS-2, qui ne prend en charge que 70 caractères par SMS.

L’utilisation du codage UCS-2 peut augmenter le nombre de caractères et, par conséquent, avoir un impact sur la facturation des messages par votre fournisseur de services.

Par exemple, un message Unicode de 200 caractères sera envoyé en 3 parties de SMS.

## Bonnes pratiques de création {#authoring-best-practices}

Rédigez le SMS final directement dans Journey Optimizer ou collez-le à partir d’applications en texte brut.

Évitez d’utiliser des applications en texte enrichi, car elles peuvent introduire des caractères masqués ou des sauts de ligne qui déclenchent l’utilisation du codage UCS-2, ce qui peut augmenter à la fois le nombre de parties de SMS et les coûts associés.

## Vérifier le nombre de caractères avant l’envoi {#check-character-count}

Utilisez des applications en texte brut ou le menu Journey Optimizer **[!UICONTROL Simuler le contenu]** pour vérifier le nombre de caractères.

Lorsque Journey Optimizer affiche le nombre de caractères, espaces compris, lors de la simulation du contenu, tenez compte des points suivants :

* Il n’inclut **pas** les caractères générés par la personnalisation dynamique ni certains caractères spéciaux.

* Le **comptage x/1500** sert d’indicateur visuel de la limite technique de la payload, et non de la limite par message, par exemple la limite de 160 caractères du codage GSM 7 bits.

* Adobe prend en charge le codage UTF-8 dans l’éditeur, qui diffère du codage GSM-7.

## Présentation du reporting {#understanding-reporting}

Le **reporting de Journey Optimizer** compte l’ensemble du message comme un envoi, indépendamment des parties de SMS.

Le **reporting du fournisseur** reflète le nombre de parties de SMS réellement envoyées. Vous devez le consulter afin de vérifier la facturation et tout éventuel dépassement. Si Adobe est votre fournisseur de SMS via Sinch, vous recevrez ce rapport de facturation séparément tous les mois.

## Considérations relatives à la personnalisation {#personalization-considerations}

La personnalisation dynamique peut augmenter la longueur d’un message. Par exemple, le fait de remplacer une variable par un long prénom peut ajouter des caractères supplémentaires.

## Ressources supplémentaires {#additional-resources}

Consultez les caractères pris en charge et les règles de codage dans le [guide Sinch de prise en charge des caractères](https://developers.sinch.com/docs/sms/resources/message-info/character-support/).
